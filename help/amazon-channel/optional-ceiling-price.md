---
title: '"Règle de tarification intelligente : Prix de plafond facultatif'''
description: Utilisez les paramètres de prix plafond facultatifs pour protéger votre prix de produit le plus élevé contre les règles de tarification intelligente qui gèrent vos listes Amazon.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Règle de retarification intelligente : prix plafond facultatif

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

   Sélectionnez votre [!DNL Commerce] [attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre Amazon dépasse le MSRP de votre article, sélectionnez l’attribut `Manufacturer's Suggested Retail Price` .

1. Pour **[!UICONTROL Ceiling Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez le moment où vous souhaitez que la  _[!UICONTROL Ceiling Price Source]_valeur définie soit ajustée, créant ainsi un prix plafond inférieur pour la règle, avant d’être répertoriée dans Amazon.

   - `Increase By` - Choisissez le moment où vous souhaitez ajuster la  _[!UICONTROL Ceiling Price Source]_valeur définie, créant ainsi un prix plafond plus élevé pour la règle, avant de l’ajouter à Amazon.

   - `Match` - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la  _[!UICONTROL Ceiling Price Source]_valeur définie. Lorsqu’ils sont définis sur `Match`, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.

1. Laissez la valeur par défaut **[!UICONTROL Apply]** `Apply as percentage`.

1. Pour **[!UICONTROL Ceiling Adjustment Price]**, saisissez la valeur numérique du pourcentage pour ajuster votre valeur _[!UICONTROL Ceiling Price Source]_.

Dans cet exemple, le prix plafond est fixé à 2 % en dessous du MSRP de l’article.

![Règle de retarification intelligente - prix plafond facultatif](assets/ob-intelligent-price-rule-ceiling.png)

| Champ | Description |
|---|---|
| [!UICONTROL Ceiling Price Source] | Sélectionnez l’ [!DNL Commerce] [attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} qui indique votre limite de plafond relative. Par exemple, si vous ne souhaitez pas que le prix de votre offre dépasse le MSRP de votre article, vous devez sélectionner l’attribut `Manufacturer's Suggested Retail Price` . |
| [!UICONTROL Ceiling Price Action] | Choisissez une action d’ajustement des prix. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez le moment où vous souhaitez que la  _[!UICONTROL Ceiling Price Source]_valeur définie soit ajustée, créant ainsi un prix plafond inférieur pour la règle, avant d’être répertoriée dans Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez le moment où vous souhaitez ajuster la  _[!UICONTROL Ceiling Price Source]_valeur définie, créant ainsi un prix plafond plus élevé pour la règle, avant de l’ajouter à Amazon.</li><li>**[!UICONTROL Match]** - Sélectionnez cette option lorsque vous ne souhaitez pas que le prix de la liste fluctue au-dessus de la  _[!UICONTROL Ceiling Price Source]_valeur définie. Lorsqu’ils sont définis sur `Match`, les champs_[!UICONTROL Apply]_ et _[!UICONTROL Ceiling Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajustement en pourcentage par rapport à la  _[!UICONTROL Ceiling Price Source]_valeur. |
| [!UICONTROL Ceiling Price Adjustment] | Saisissez la valeur numérique pour le pourcentage afin d’ajuster votre valeur _[!UICONTROL Ceiling Price Source]_. |
