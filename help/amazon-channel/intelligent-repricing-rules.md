---
title: '"Règle de tarification intelligente : Sélectionner le type de règle"'
description: Déterminez le prix de votre offre Amazon en fonction du prix de votre concurrent en créant une règle de retarification intelligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Règle de retarification intelligente : sélectionner le type de règle

>[!IMPORTANT]
>
>Les règles de tarification intelligente ne fonctionnent pas correctement si la région Amazon est définie sur `Inactive` , comme c’est le cas lors de l’intégration. Vos calculs de prix dépendent de vos tarifs d’expédition. Votre région doit se trouver dans `Active` statut de synchronisation de vos tarifs d’expédition depuis Amazon.<br><br>
>
>Pour mettre à jour l’état de votre région dans votre compte Amazon, accédez à Paramètres > Informations du compte > Paramètres de déplacement. Voir [Amazon : État de la liste des vacances](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Une règle de retarification intelligente utilise le prix des concurrents Amazon pour déterminer le prix de votre offre. Les concurrents sont d’autres vendeurs qui répertorient les mêmes produits que les vôtres sur Amazon.

Les sections d’une règle de retarification intelligente incluent :

- Sélectionner le type de règle
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- [Ajustement des prix](./price-adjustment.md)
- [Prix plancher](./floor-price.md)
- [Prix de plafond facultatif](./optional-ceiling-price.md)

## Configuration du type de règle

Définissez le type de règle dans le _[!UICONTROL Select Rule Type]_.

1. Pour **[!UICONTROL Rule Type]**, choisissez `Intelligent repricing rule`.

   Ce paramètre active la variable _[!UICONTROL Competitor Price Source]_et le champ [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md), et [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) sections.

1. Pour **[!UICONTROL Competitor Price Source]**, choisissez une option :

   - **[!UICONTROL Use "Buy Box" Price]** - Choisissez quand vous souhaitez ajuster vos tarifs Amazon en fonction d’Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix du vendeur. A [!DNL Buy Box] Le prix existe lorsque plusieurs vendeurs sur Amazon proposent le même produit. Amazon définit la variable [!DNL Buy Box] vendeur en fonction des exigences de performances. Les marchands cherchent à gagner la [!DNL Buy Box] statut du vendeur et offrir une visibilité maximale de ses listes de produits.

   - **[!UICONTROL Use Lowest Competitor Price]** - Choisissez quand vous souhaitez comparer et ajuster le prix de votre offre par rapport au prix de votre concurrent pour le même produit. Lorsque cette option est sélectionnée, la variable _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.

1. Si cette option est activée, choisissez une option pour **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Choisissez quand vous souhaitez comparer et ajuster vos prix en fonction de tous les prix de concurrent pour le même produit.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Choisissez quand vous souhaitez limiter les concurrents auxquels le prix est comparé pour le même produit. Ce paramètre limite davantage les concurrents en exigeant que leur liste présente un minimum du pourcentage de commentaires positifs choisi avant d’appliquer la règle du prix le plus bas.

1. Si cette option est activée, saisissez une valeur numérique pour **[!UICONTROL Minimum Feedback Count]**.

   Cette valeur numérique facultative permet de réduire davantage les prix compétitifs. Par exemple, si un commerçant a une note de retour positive de 95 %, mais qu’il a uniquement un nombre de retour de `20`, il se peut qu’il ne s’agisse pas d’un concurrent pour lequel vous souhaitez modifier vos tarifs. Cependant, si vous saisissez la valeur `1000`, il faudrait que le marchand ait 95 % de commentaires positifs et un minimum de 1 000 commentaires de marchands.

>[!NOTE]
>
>Vous pouvez utiliser ces options de tarification et de retour de concurrent pour éviter de baser vos prix sur un concurrent qui a de mauvais retours et vend un produit de qualité inférieure.

![Règle de retarification intelligente - sélectionnez le type de règle.](assets/ob-intelligent-price-rule-type.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Rule Type] | Sélectionnez un type de règle. Options :<ul><li>**[!UICONTROL Standard price rule]** - Ce type de règle vous permet d’augmenter ou de diminuer le prix de la mise en vente d’Amazon d’un pourcentage spécifique ou d’un montant fixe en dollars par rapport au _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Ce type de règle vous permet d’ajuster le prix de votre offre Amazon en fonction du prix du concurrent. Lorsque cette option est sélectionnée, la variable _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.</li></ul> |
| [!UICONTROL Competitor Price Source] | Sélectionnez la source de prix souhaitée. Options :<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Choisissez cette option lorsque vous souhaitez ajuster vos tarifs Amazon en fonction d’Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix du vendeur. A [!DNL Buy Box] Le prix existe lorsque plusieurs vendeurs sur Amazon proposent le même produit. Amazon définit la variable [!DNL Buy Box] vendeur en fonction des exigences de performances. Les marchands cherchent à gagner la [!DNL Buy Box] statut du vendeur et offrir une visibilité maximale de ses listes de produits.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Choisissez cette option lorsque vous souhaitez comparer et ajuster le prix de votre annonce au [prix concurrentiel le plus bas](./lowest-competitor-pricing.md) pour le même produit. Lorsque cette option est sélectionnée, la variable _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Principal uniquement si `Use Lowest Competitor Price` est choisie. Options :<ul><li>**[!UICONTROL All Competitor's Prices]** - Choisissez quand vous souhaitez comparer et ajuster vos prix en fonction de tous les prix de concurrent pour le même produit.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Choisissez quand vous souhaitez limiter les concurrents auxquels vous comparez et ajustez vos prix. Ce paramètre limite davantage vos concurrents en exigeant que leur liste contienne un minimum du pourcentage choisi de commentaires positifs, puis utilise le prix le plus bas de ce sous-ensemble de concurrents.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Principal uniquement si `Use Lowest Competitor Price` est choisie. Cette valeur numérique facultative limite davantage la comparaison des prix par rapport à la concurrence. Par exemple, si un commerçant a une évaluation de retour positive de 95 %, mais qu’il a uniquement un nombre de retours de `20`, il se peut qu’il ne s’agisse pas d’un concurrent pour lequel vous souhaitez modifier vos tarifs. Cependant, si vous saisissez la valeur `1000`, il faudrait que le marchand ait 95 % de commentaires positifs et un minimum de 1 000 commentaires de marchands. |
