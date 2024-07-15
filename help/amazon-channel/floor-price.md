---
title: "Règle de tarification intelligente : prix du plancher"
description: Utilisez les paramètres de prix plancher pour déterminer le prix le plus bas pour une règle de tarification intelligente afin de gérer vos listes Amazon.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Règle de tarification intelligente : prix plancher

Les sections d’une règle de retarification intelligente incluent :

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Les paramètres [prix plancher](./floor-price.md) protègent automatiquement votre prix le plus bas contre les règles de tarification intelligente. Utilisez ces paramètres pour définir un prix plancher pour vos règles de tarification intelligente, en veillant à ce que vos produits ne soient pas répertoriés sous le prix souhaité.

Les attributs de prix plancher sont basés sur la portée du site web si votre boutique [!DNL Commerce] utilise la portée de la tarification du site web. Voir [Périmètre du prix](./price-scope.md).

Le prix plancher n’est utilisé que lorsque **[!UICONTROL Rule Type]** est défini sur `Intelligent repricing rule`.

## Configurer le prix plancher

Définissez le prix le plus bas dans la section _[!UICONTROL Floor Price]_.

1. Pour **[!UICONTROL Floor Price Source]**, choisissez un attribut de source de prix.

   Sélectionnez l’ [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) qui indique votre limite de plancher relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon soit inférieur au coût de votre article, vous pouvez choisir l’attribut *Cost* .

1. Pour **[!UICONTROL Floor Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez le moment où vous souhaitez que la valeur _[!UICONTROL Floor Price Source]_définie soit ajustée, créant ainsi un prix plancher inférieur pour la règle, avant de l’ajouter à Amazon.

   - `Increase By` - Choisissez le moment où vous souhaitez ajuster la valeur _[!UICONTROL Floor Price Source]_définie, créant ainsi un prix plancher plus élevé pour la règle, avant de l’ajouter à Amazon.

   - `Match` - Choisissez le moment où vous ne souhaitez pas que le prix de la liste fluctue en dessous de la valeur _[!UICONTROL Floor Price Source]_définie. Lorsqu&#39;ils sont définis sur `Match`, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.

1. Laissez la valeur par défaut **[!UICONTROL Apply]** `Apply as percentage`.

1. Pour **[!UICONTROL Floor Adjustment Price]**, saisissez la valeur numérique du pourcentage pour ajuster la valeur _[!UICONTROL Floor Price Source]_.

Dans cet exemple, le prix plancher est fixé à 3 % au-dessus du coût de l’article.

![Exemple de règle de réévaluation intelligente - prix plancher](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Champ | Description |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Sélectionnez l’attribut [!DNL Commerce] qui indique votre limite de plancher relative (prix le plus bas). Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon soit inférieur au coût de votre article, choisissez l’attribut `Cost` . |
| [!UICONTROL Floor Price Action] | Choisissez une action d’ajustement des prix. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez le moment où vous souhaitez que la valeur _[!UICONTROL Floor Price Source]_définie soit ajustée, créant ainsi un prix plancher inférieur pour la règle, avant de l’ajouter à Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez le moment où vous souhaitez ajuster la valeur _[!UICONTROL Floor Price Source]_définie, créant ainsi un prix plancher plus élevé pour la règle, avant de l’ajouter à Amazon.</li><li>**[!UICONTROL Match]** - Choisissez le moment où vous ne souhaitez pas que le prix de la liste fluctue en dessous de la valeur _[!UICONTROL Floor Price Source]_définie. Lorsque cette option est sélectionnée, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Ajustement en pourcentage par rapport à la valeur _[!UICONTROL Floor Price Source]_. |
| [!UICONTROL Floor Adjustment Amount] | Saisissez la valeur numérique pour le pourcentage afin d’ajuster votre valeur _[!UICONTROL Floor Price Source]_. |
