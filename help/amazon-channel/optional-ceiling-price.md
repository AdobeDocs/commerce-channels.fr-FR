---
title: '''Règle de tarification intelligente : Prix plafond facultatif'''
description: Utilisez les paramètres de prix plafond facultatifs pour protéger votre prix de produit le plus élevé contre les règles de tarification intelligente qui gèrent vos annonces Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Règle de revalorisation intelligente : prix plafond facultatif

Les sections d&#39;une règle de réévaluation intelligente comprennent :

- [Sélectionner le type de règle](./intelligent-repricing-rules.md)
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- [Ajustement du prix](./price-adjustment.md)
- [Prix plancher](./floor-price.md)
- Prix plafond facultatif

Les paramètres de prix plafond automatisés protègent automatiquement votre prix de produit le plus élevé contre les règles de tarification intelligentes, ce qui vous permet de fixer un plafond (le prix le plus élevé) pour vos règles de tarification intelligente.

## Configurer le prix plafond facultatif

Définissez vos paramètres de prix les plus élevés en option dans le menu _[!UICONTROL Optional Ceiling Price]_.

1. Pour **[!UICONTROL Ceiling Price Source]**, sélectionnez un attribut.

   Sélectionnez votre [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre annonce Amazon dépasse le MSRP de votre objet, vous choisissez l’option `Manufacturer's Suggested Retail Price` .

1. Pour **[!UICONTROL Ceiling Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez quand vous souhaitez définir _[!UICONTROL Ceiling Price Source]_valeur à ajuster vers le bas, créant un prix plafond plus bas pour la règle, avant l&#39;inscription à Amazon.

   - `Increase By` - Choisissez quand vous souhaitez définir _[!UICONTROL Ceiling Price Source]_à ajuster, créant un prix plafond plus élevé pour la règle, avant d&#39;être cotée en Amazon.

   - `Match` - Choisissez quand vous ne souhaitez pas que le prix d&#39;annonce fluctue au-dessus du _[!UICONTROL Ceiling Price Source]_valeur. Lorsque la valeur est définie sur `Match`, le_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.

1. Laissez le bouton **[!UICONTROL Apply]** par défaut `Apply as percentage`.

1. Pour **[!UICONTROL Ceiling Adjustment Price]**, entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Ceiling Price Source]_valeur.

Dans cet exemple, le prix plafond est fixé à 2 % en dessous du MSRP de l&#39;article.

![Règle de revalorisation intelligente - prix plafond facultatif](assets/ob-intelligent-price-rule-ceiling.png)

| Champ | Description |
|---|---|
| [!UICONTROL Ceiling Price Source] | Sélectionnez l’option [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de la mise en vente de votre produit dépasse le MSRP de votre objet, vous choisissez l’option `Manufacturer's Suggested Retail Price` . |
| [!UICONTROL Ceiling Price Action] | Sélectionnez une action d&#39;ajustement de tarification. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez définir _[!UICONTROL Ceiling Price Source]_valeur à ajuster vers le bas, créant un prix plafond plus bas pour la règle, avant l&#39;inscription à Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez définir _[!UICONTROL Ceiling Price Source]_à ajuster, créant un prix plafond plus élevé pour la règle, avant d&#39;être cotée en Amazon.</li><li>**[!UICONTROL Match]** - Choisissez quand vous ne souhaitez pas que le prix d&#39;annonce fluctue au-dessus du _[!UICONTROL Ceiling Price Source]_valeur. Lorsque la valeur est définie sur `Match`, le_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajustement en pourcentage par rapport à la _[!UICONTROL Ceiling Price Source]_valeur. |
| [!UICONTROL Ceiling Price Adjustment] | Entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Ceiling Price Source]_valeur. |
