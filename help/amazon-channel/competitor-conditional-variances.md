---
title: '''Règle de tarification intelligente : Écarts conditionnels des concurrents'
description: Déterminez le prix de votre annonce Amazon en fonction de la tarification et de l’état du produit par un concurrent en créant une règle de tarification intelligente.
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Règle de revalorisation intelligente : écarts conditionnels entre concurrents

Les sections d&#39;une règle de réévaluation intelligente comprennent :

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Une règle de tarification intelligente utilise la tarification des concurrents Amazon pour déterminer le prix de votre annonce. Les concurrents sont d&#39;autres vendeurs qui vendent les mêmes produits que ceux que vous avez mis en vente sur Amazon.

Si un produit présente la même condition, le prix de correspondance de base est le [concurrent le plus bas](./lowest-competitor-pricing.md) prix avec la même condition. Si aucun produit concurrent ne correspond à votre condition, le prix de base correspond alors à d’autres conditions concurrentes disponibles, en commençant par Nouveau, Rénové et en poursuivant par les conditions disponibles. Une fois une condition trouvée, le prix de correspondance de base sera le prix le plus bas dans cette condition.

Si vous avez un produit répertorié avec la condition `Used; Good` et le prix de correspondance de base, et un concurrent a le même produit dans le même état à un prix inférieur, le prix concurrent est utilisé. Si un concurrent n&#39;existe pas avec la même condition, le système vérifie un concurrent avec la condition suivante, qui est `New`. Si un concurrent se trouve avec cette condition, le prix le plus bas est utilisé.

## Configuration des écarts conditionnels de concurrent

Définissez vos écarts de condition dans le fichier _[!UICONTROL Competitor Conditional Variances]_.

Pour **[!UICONTROL Conditional Variance]**, choisissez une option :

- `Use all competitor's product conditions` - (Par défaut) Choisissez quand vous souhaitez comparer votre produit avec toute condition disponible (si une correspondance n’existe pas pour la condition que vous listez).

- `Use Only Matching Competitor's Product Condition` - Choisissez quand vous souhaitez que votre produit ne se compare qu&#39;aux produits de concurrents dans le même état. Si aucune correspondance n’existe, le prix du produit est fixé au _Source de prix Magento_ défini dans votre [Prix d&#39;annonce](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Choisissez d&#39;abord d&#39;essayer de comparer avec votre condition de produit correspondante. S’il n’existe aucune condition correspondante, une variance (en pourcentage) est appliquée par rapport à votre condition de produit et à l’état du concurrent le plus bas.

   Lorsque _[!UICONTROL Apply Variance]_est sélectionnée, des champs de variance supplémentaires s’affichent pour chacune de vos conditions Amazon. Cette fonctionnalité vous permet d’utiliser des règles de réévaluation intelligentes lorsque vous proposez des produits dans des conditions différentes de celles de vos concurrents. Pour comprendre le calcul derrière la variance conditionnelle, vous devez d’abord comprendre que toute variance est déterminée à partir d’un prix de correspondance de base.

   Les options d’écart conditionnel qui s’affichent sont basées sur vos paramètres d’annonce pour `Condition` qui sont mappés à des valeurs de condition à l’aide d’un [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Pour toutes les conditions mappées, vous pouvez définir un pourcentage de variance de 1 à 100. L&#39;exception concerne les objets de collection, auquel cas un pourcentage supérieur à 100 peut être appliqué.

![Règle de revalorisation intelligente - Variations conditionnelles concurrentes](assets/amazon-competitor-cond-variances.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | Options : <ul><li>**[!UICONTROL Use all competitor's product conditions]** - Si une correspondance n’existe pas pour la condition avec laquelle vous listez votre produit, cette option correspond à toute condition disponible. Il tente d’abord de correspondre à votre condition, puis effectue son chemin à partir de la `New` condition à `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** - Cette option correspond à l’état de votre produit. Si aucune correspondance n’existe, les prix du produit au niveau de la propriété _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** - Cette option tente d’abord de correspondre à votre condition de produit. S’il n’existe aucune condition correspondante, elle applique une variance (en pourcentage) par rapport à votre condition de produit et à la condition du concurrent le plus bas.</li></ul><br><br>Les options de variance conditionnelle qui s’affichent en fonction des paramètres de votre liste pour Condition qui sont mappés à des valeurs de condition à l’aide d’un [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Pour toutes les conditions mappées, vous pouvez indiquer un pourcentage de variance de 1 à 100. L&#39;exception concerne les objets de collection, auquel cas un pourcentage supérieur à 100 peut être appliqué.<br><br>Cette fonctionnalité vous permet d’utiliser des règles de réévaluation intelligentes lorsque vous proposez des produits dans des conditions différentes de celles de vos concurrents. Pour comprendre le calcul derrière la variance conditionnelle, vous devez d’abord comprendre que toute variance est déterminée à partir d’un prix de correspondance de base. |

## Calculer la base des écarts conditionnels

- Écart de condition de correspondance de base (BMC) = Écart pour la condition de votre concurrent de prix de correspondance de base. À l’aide de l’exemple précédent, BMC représente la variance de la `New` condition.
- Écart de condition du commerçant (MCV) = Écart pour l&#39;état de votre produit. À l’aide de l’exemple précédent, MCV = la variance de l’attribut `Used; Good` condition.
- Prix de correspondance de base (BMP) = 7,99 $ (expliqué ci-dessus)

La formule de calcul de la base de variance conditionnelle est la suivante :

![formule de calcul de base de la variance conditionnelle](assets/amazon-cond-variance-calc-1.png)

## Exemple

Les paramètres de variance conditionnelle sont les suivants :

![exemple de paramètres de variance conditionnelle](assets/amazon-cond-variances.png)

- BMC = 100 (Condition du concurrent = Nouveau)
- MCV = 80 (condition du commerçant = utilisée ; Bonne)
- BMP = 7,99 $ (prix de base du match = prix le plus bas de la condition de concurrent compensé)

![exemple de calcul de base de variance conditionnelle](assets/amazon-cond-variance-calc-2.png)

En utilisant le calcul de la base d&#39;écarts conditionnels ci-dessus, votre base d&#39;écarts conditionnels = 6,39 $. Ce calcul est la source de prix concurrent utilisée pour vos actions de règles de prix, expliqué plus loin dans [Ajustement du prix](./price-adjustment.md).
