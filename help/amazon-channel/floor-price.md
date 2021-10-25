---
title: '''Règle de tarification intelligente : Prix plancher"'
description: Utilisez les paramètres de prix plancher pour déterminer le prix le plus bas pour une règle de tarification intelligente pour gérer vos annonces Amazon.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Règle de revalorisation intelligente : prix plancher

Les sections d&#39;une règle de réévaluation intelligente comprennent :

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Le [prix plancher](./floor-price.md) protège automatiquement votre prix le plus bas contre les règles de tarification intelligentes. Utilisez ces paramètres pour définir un plancher (prix le plus bas) pour vos règles de tarification intelligente, en veillant à ce que vos produits ne soient pas répertoriés sous le prix souhaité.

Les attributs de prix plancher sont basés sur la portée du site Web si votre [!DNL Commerce] le magasin utilise la portée de tarification du site web. Voir [Portée du prix](./price-scope.md).

Le prix plancher est utilisé uniquement lorsque **[!UICONTROL Rule Type]** est défini sur `Intelligent repricing rule`.

## Configurer le prix plancher

Définissez votre paramètre de prix le plus bas dans le menu _[!UICONTROL Floor Price]_.

1. Pour **[!UICONTROL Floor Price Source]**, sélectionnez un attribut de source de prix.

   Sélectionnez l’option [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} qui indique votre limite de plancher relative. Par exemple, si vous ne souhaitez pas que le prix de votre annonce Amazon soit inférieur au coût de votre objet, vous devez choisir l’option *Coût* .

1. Pour **[!UICONTROL Floor Price Action]**, choisissez une option.

   - `Decrease By` - Choisissez quand vous souhaitez définir _[!UICONTROL Floor Price Source]_valeur à ajuster à la baisse, créant un prix plancher inférieur pour la règle, avant l&#39;inscription à Amazon.

   - `Increase By` - Choisissez quand vous souhaitez définir _[!UICONTROL Floor Price Source]_à ajuster, créant un prix plancher plus élevé pour la règle, avant d&#39;être cotée en Amazon.

   - `Match` - Choisissez quand vous ne souhaitez pas que le prix d&#39;annonce fluctue en dessous du _[!UICONTROL Floor Price Source]_valeur. Lorsque la valeur est définie sur `Match`, le_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.

1. Laissez le bouton **[!UICONTROL Apply]** par défaut `Apply as percentage`.

1. Pour **[!UICONTROL Floor Adjustment Price]**, entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Floor Price Source]_valeur.

Dans cet exemple, le prix plancher est fixé à 3 % au-dessus du coût de l&#39;article.

![Exemple de règle de tarification intelligente - prix plancher](assets/ob-intelligent-pricde-rule-floor-price.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Floor Price Source] | Sélectionnez l’option [!DNL Commerce] qui indique votre limite relative de plancher (prix le plus bas). Par exemple, si vous ne souhaitez pas que le prix de votre annonce Amazon soit inférieur au coût de votre objet, vous devez choisir l’option `Cost` . |
| [!UICONTROL Floor Price Action] | Sélectionnez une action d&#39;ajustement de tarification. Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez définir _[!UICONTROL Floor Price Source]_valeur à ajuster à la baisse, créant un prix plancher inférieur pour la règle, avant l&#39;inscription à Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez définir _[!UICONTROL Floor Price Source]_à ajuster, créant un prix plancher plus élevé pour la règle, avant d&#39;être cotée en Amazon.</li><li>**[!UICONTROL Match]** - Choisissez quand vous ne souhaitez pas que le prix d&#39;annonce fluctue en dessous du _[!UICONTROL Floor Price Source]_valeur. Lorsque cette option est sélectionnée, la_[!UICONTROL Apply]_ et _[!UICONTROL Floor Adjustment Amount]_sont désactivés.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - Un ajustement en pourcentage par rapport à la _[!UICONTROL Floor Price Source]_valeur. |
| [!UICONTROL Floor Adjustment Amount] | Entrez la valeur numérique du pourcentage pour ajuster votre _[!UICONTROL Floor Price Source]_valeur. |
