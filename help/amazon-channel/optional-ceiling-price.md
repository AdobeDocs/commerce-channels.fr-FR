---
title: "Règle de tarification intelligente : prix de plafond facultatif"
description: Utilisez les paramètres de prix plafond facultatifs pour protéger votre prix de produit le plus élevé contre les règles de tarification intelligente qui gèrent vos listes Amazon.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Règle de tarification intelligente : prix de plafond facultatif

Les sections d’une règle de retarification intelligente incluent :

- [Sélectionner le type de règle](./intelligent-repricing-rules.md)
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- [Ajustement des prix](./price-adjustment.md)
- [Prix plancher](./floor-price.md)
- Prix de plafond facultatif

Les paramètres de prix plafond automatisés protègent automatiquement vos prix de produit les plus élevés contre les règles de tarification intelligente, ce qui vous permet de définir un plafond (le prix le plus élevé) pour vos règles de tarification intelligente.

## Configurer le prix plafond facultatif

Définissez les paramètres facultatifs du prix le plus élevé dans la section _[!UICONTROL Optional Ceiling Price]_.

1. Pour **[!UICONTROL Ceiling Price Source]**, choisissez un attribut.

   Sélectionnez votre [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon dépasse le MSRP de votre article, choisissez l’attribut `Manufacturer's Suggested Retail Price` .

1. Pour **[!UICONTROL Ceiling Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez le moment où vous souhaitez que la valeur _[!UICONTROL Ceiling Price Source]_définie soit ajustée, créant ainsi un prix plafond inférieur pour la règle, avant de l’ajouter à Amazon.

   - `Increase By` - Choisissez le moment où vous souhaitez ajuster la valeur _[!UICONTROL Ceiling Price Source]_définie, créant ainsi un prix plafond plus élevé pour la règle, avant de l’ajouter à Amazon.

   - `Match` - Choisissez le moment où vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la valeur _[!UICONTROL Ceiling Price Source]_définie. Lorsqu&#39;ils sont définis sur `Match`, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.

1. Laissez la valeur par défaut **[!UICONTROL Apply]** `Apply as percentage`.

1. Pour **[!UICONTROL Ceiling Adjustment Price]**, saisissez la valeur numérique du pourcentage pour ajuster la valeur _[!UICONTROL Ceiling Price Source]_.

Dans cet exemple, le prix plafond est fixé à 2 % en dessous du MSRP de l’article.

![Règle de réévaluation intelligente - Prix plafond facultatif](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Champ | Description |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Sélectionnez l’ [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre liste de produits dépasse le MSRP de votre article, choisissez l’attribut `Manufacturer's Suggested Retail Price` . |
| [!UICONTROL Ceiling Price Action] | Choisissez une action d’ajustement des prix. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez le moment où vous souhaitez que la valeur _[!UICONTROL Ceiling Price Source]_définie soit ajustée, créant ainsi un prix plafond inférieur pour la règle, avant de l’ajouter à Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez le moment où vous souhaitez ajuster la valeur _[!UICONTROL Ceiling Price Source]_définie, créant ainsi un prix plafond plus élevé pour la règle, avant de l’ajouter à Amazon.</li><li>**[!UICONTROL Match]** - Choisissez le moment où vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la valeur _[!UICONTROL Ceiling Price Source]_définie. Lorsqu&#39;ils sont définis sur `Match`, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Ajustement en pourcentage par rapport à la valeur _[!UICONTROL Ceiling Price Source]_. |
| [!UICONTROL Ceiling Price Adjustment] | Saisissez la valeur numérique pour le pourcentage afin d’ajuster votre valeur _[!UICONTROL Ceiling Price Source]_. |
