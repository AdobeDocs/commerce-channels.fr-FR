---
title: '"Règle de tarification intelligente : Prix de plafond facultatif'''
description: Utilisez les paramètres de prix plafond facultatifs pour protéger votre prix de produit le plus élevé contre les règles de tarification intelligente qui gèrent vos listes Amazon.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Règle de tarification intelligente : Prix de plafond facultatif

Les sections d’une règle de retarification intelligente incluent :

- [Sélectionner le type de règle](./intelligent-repricing-rules.md)
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- [Ajustement des prix](./price-adjustment.md)
- [Prix plancher](./floor-price.md)
- Prix de plafond facultatif

Les paramètres de prix plafond automatisés protègent automatiquement vos prix de produit les plus élevés contre les règles de tarification intelligente, ce qui vous permet de définir un plafond (le prix le plus élevé) pour vos règles de tarification intelligente.

## Configurer le prix plafond facultatif

Définissez les paramètres facultatifs du prix le plus élevé dans la variable _[!UICONTROL Optional Ceiling Price]_.

1. Pour **[!UICONTROL Ceiling Price Source]**, choisissez un attribut.

   Sélectionnez votre [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon dépasse le MSRP de votre article, vous pouvez choisir la variable `Manufacturer's Suggested Retail Price` attribut.

1. Pour **[!UICONTROL Ceiling Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez quand vous souhaitez que la variable _[!UICONTROL Ceiling Price Source]_à ajuster, créant ainsi un prix plafond inférieur pour la règle, avant d’être répertoriée dans Amazon.

   - `Increase By` - Choisissez quand vous souhaitez que la variable _[!UICONTROL Ceiling Price Source]_à ajuster, créant ainsi un prix plafond plus élevé pour la règle, avant d’être répertoriée dans Amazon.

   - `Match` - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la valeur définie. _[!UICONTROL Ceiling Price Source]_. Lorsque la variable est définie sur `Match`, la variable_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.

1. Laissez le champ **[!UICONTROL Apply]** par défaut en tant que `Apply as percentage`.

1. Pour **[!UICONTROL Ceiling Adjustment Price]**, saisissez la valeur numérique du pourcentage afin d’ajuster votre _[!UICONTROL Ceiling Price Source]_.

Dans cet exemple, le prix plafond est fixé à 2 % en dessous du MSRP de l’article.

![Règle de retarification intelligente - prix plafond facultatif](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Champ | Description |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Choisissez la [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre dépasse le prix MSRP de votre produit, vous pouvez choisir la variable `Manufacturer's Suggested Retail Price` attribut. |
| [!UICONTROL Ceiling Price Action] | Choisissez une action d’ajustement des prix. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez que la variable _[!UICONTROL Ceiling Price Source]_à ajuster, créant ainsi un prix plafond inférieur pour la règle, avant d’être répertoriée dans Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez que la variable _[!UICONTROL Ceiling Price Source]_à ajuster, créant ainsi un prix plafond plus élevé pour la règle, avant d’être répertoriée dans Amazon.</li><li>**[!UICONTROL Match]** - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la valeur définie. _[!UICONTROL Ceiling Price Source]_. Lorsque la variable est définie sur `Match`, la variable_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajustement en pourcentage par rapport à la valeur _[!UICONTROL Ceiling Price Source]_. |
| [!UICONTROL Ceiling Price Adjustment] | Entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Ceiling Price Source]_. |
