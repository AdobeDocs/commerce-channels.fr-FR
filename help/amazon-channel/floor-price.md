---
title: '"Règle de tarification intelligente : Prix plancher'''
description: Utilisez les paramètres de prix plancher pour déterminer le prix le plus bas pour une règle de tarification intelligente afin de gérer vos listes Amazon.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Règle de tarification intelligente : Prix plancher

Les sections d’une règle de retarification intelligente incluent :

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Le [prix plancher](./floor-price.md) les paramètres protègent automatiquement le prix le plus bas du produit des règles de prix intelligentes. Utilisez ces paramètres pour définir un prix plancher pour vos règles de tarification intelligente, en veillant à ce que vos produits ne soient pas répertoriés sous le prix souhaité.

Les attributs de prix plancher sont basés sur la portée du site web si votre [!DNL Commerce] Le magasin utilise la portée du prix du site web. Voir [Étendue du prix](./price-scope.md).

Le prix plancher n’est utilisé que lorsque **[!UICONTROL Rule Type]** est défini sur `Intelligent repricing rule`.

## Configurer le prix plancher

Définissez le paramètre de prix le plus bas dans la _[!UICONTROL Floor Price]_.

1. Pour **[!UICONTROL Floor Price Source]**, choisissez un attribut de source de prix.

   Choisissez la [!DNL Commerce] [attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} qui indique votre limite de plancher relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon soit inférieur au coût de votre article, vous pouvez choisir la variable *Coût* attribut.

1. Pour **[!UICONTROL Floor Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez quand vous souhaitez que la variable _[!UICONTROL Floor Price Source]_à ajuster, créant ainsi un prix plancher inférieur pour la règle, avant d’être répertoriée dans Amazon.

   - `Increase By` - Choisissez quand vous souhaitez que la variable _[!UICONTROL Floor Price Source]_à ajuster, créant ainsi un prix plancher plus élevé pour la règle, avant d’être répertoriée dans Amazon.

   - `Match` - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue en dessous du nombre défini _[!UICONTROL Floor Price Source]_. Lorsque la variable est définie sur `Match`, la variable_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.

1. Laissez le champ **[!UICONTROL Apply]** par défaut en tant que `Apply as percentage`.

1. Pour **[!UICONTROL Floor Adjustment Price]**, saisissez la valeur numérique du pourcentage afin d’ajuster votre _[!UICONTROL Floor Price Source]_.

Dans cet exemple, le prix plancher est fixé à 3 % au-dessus du coût de l’article.

![Exemple de règle de réévaluation intelligente - prix plancher](assets/ob-intelligent-pricde-rule-floor-price.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Floor Price Source] | Choisissez la [!DNL Commerce] qui indique votre limite relative de prix plancher (prix le plus bas). Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon soit inférieur au coût de votre article, vous pouvez choisir la variable `Cost` attribut. |
| [!UICONTROL Floor Price Action] | Choisissez une action d’ajustement des prix. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez que la variable _[!UICONTROL Floor Price Source]_à ajuster, créant ainsi un prix plancher inférieur pour la règle, avant d’être répertoriée dans Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez que la variable _[!UICONTROL Floor Price Source]_à ajuster, créant ainsi un prix plancher plus élevé pour la règle, avant d’être répertoriée dans Amazon.</li><li>**[!UICONTROL Match]** - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue en dessous du nombre défini _[!UICONTROL Floor Price Source]_. Lorsque cette option est sélectionnée, la variable_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajustement en pourcentage par rapport à la valeur _[!UICONTROL Floor Price Source]_. |
| [!UICONTROL Floor Adjustment Amount] | Entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Floor Price Source]_. |
