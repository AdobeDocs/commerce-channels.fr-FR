---
title: Créer un SKU de fournisseur d’alias Amazon
description: Vous pouvez utiliser le SKU du fournisseur d’alias Amazon pour créer des listes Amazon multirégionales à partir de vos produits de catalogue Commerce.
feature: Sales Channels, Products
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Créer un SKU de fournisseur d’alias Amazon

Un [!DNL Alias Amazon Seller SKU] est utilisé pour créer une liste Amazon à partir du même produit dans votre [!DNL Commerce] catalogue. Si vous êtes un vendeur Amazon expérimenté, vous connaissez peut-être le [SKU global d’Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} et SKU spécifique à Marketplace pour l’inventaire et l’expédition. Conformément à des principes similaires pour le canal de vente Amazon, le SKU du vendeur Amazon contrôle les informations de mise en liste de produits à un niveau multirégional, ainsi que la variable [!DNL Alias Amazon Seller SKU] peut être utilisé pour contrôler les informations sur les listes de produits à un niveau spécifique à une région.

Cette fonction peut être utilisée pour exécuter deux fonctions :

- Créez un [!DNL Alias Amazon Seller SKU] pour l’un des [!DNL Commerce] catalogue de produits pour contrôler les informations de liste spécifiques à une région.

  **Exemple**: vous êtes un vendeur dans les régions des États-Unis et du Canada. N’oubliez pas que chacune de vos boutiques de canaux de vente Amazon ne peut se voir attribuer qu’une seule région Amazon lors de la configuration. Ainsi, vous disposez d’un magasin de canaux de vente Amazon avec une région définie des États-Unis et un autre magasin avec une région définie du Canada. Les deux magasins partagent votre [!DNL Commerce] catalogue pour répertorier les informations dans les deux régions, y compris le SKU du vendeur Amazon et les attributs de produit ASIN. Par conséquent, les listes pour le produit catalogue seraient les mêmes dans les deux magasins, le partage de prix, le stock/la quantité et d’autres attributs de produit. Mais votre stock pour votre Canada stocke des navires provenant d&#39;un emplacement canadien, et vos navires situés aux États-Unis. Par conséquent, vous devez contrôler la quantité de la liste séparément pour chaque magasin. Pour réaliser ce type de contrôle spécifique à une région, vous pouvez créer un SKU de vendeur Amazon d’alias.

  Essentiellement, vous pouvez créer un SKU de vendeur Amazon d’alias lié au même produit de catalogue et utiliser pour republier la même liste dans cette région.

- Créez un [!DNL Alias Amazon Seller SKU] et faites correspondre l’une de vos [!DNL Commerce] cataloguer les produits sur deux listes Amazon.

  **Exemple**: vous disposez d’un produit de catalogue associé à une liste Amazon. Comme Amazon comporte souvent plusieurs listes représentant le même produit, vous découvrez une autre liste Amazon pour le même produit, mais Amazon a affecté un ASIN différent à la liste. Pour accroître la visibilité de votre produit à inclure, vous souhaitez faire correspondre votre produit de catalogue aux différents ASIN et créer des listes pour les deux valeurs ASIN. Pour ce faire, vous pouvez créer un SKU Alias Amazon Seller.

  Essentiellement, vous pouvez créer une [!DNL Alias Amazon Seller SKU] qui peut être utilisé pour faire correspondre un produit de catalogue unique à une deuxième liste Amazon et créer une liste pour le nouvel ASIN correspondant. Dans ce scénario, vous disposez de deux listes Amazon pour le même produit de catalogue.

  Après avoir créé un SKU de vendeur Amazon d’alias, vous pouvez utiliser vos paramètres de liste, règles et remplacements pour contrôler les informations de liste pour la région. Les attributs de produit qui peuvent être définis par région pour une liste incluent la quantité/le stock, la méthode d’exécution, la condition, l’éligibilité du produit et le temps de traitement.

## Utilisé à des fins spécifiques à une région {#region-specific}

Affichez la liste sur la page _[!UICONTROL Product Listings]_page (_[!UICONTROL Inactive]_, _Actif_, _Inéligible_, ou _Terminé_ ).

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create Alias Seller SKU]**.

1. Pour **[!UICONTROL Assign New Seller SKU]**, saisissez une valeur alphanumérique unique.

   Cette valeur doit être unique (non utilisée pour un autre produit ou alias de votre catalogue).

1. Pour **[!UICONTROL Assign New ASIN]**, n’effectuez aucune modification.

   Cette valeur est renseignée automatiquement avec le produit ASIN associé à votre produit de catalogue. La modification de cette valeur correspond à votre produit de catalogue pour deux listes Amazon basées sur ASIN.

1. Activez/désactivez la variable **[!UICONTROL Remove Existing Seller SKU]** au besoin.

   - `Yes` - Choisissez de supprimer la liste et de créer une liste à l’aide des nouvelles informations fournies.

   - `No` - Choisissez de créer une liste et de conserver l’ancienne liste inchangée.

1. Cliquez sur **[!UICONTROL Save Listing Update]**.

## Utilisé pour faire correspondre un seul produit de catalogue à deux listes Amazon

1. Affichez la liste sur la page _[!UICONTROL Product Listings]_page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_, ou _[!UICONTROL Ended]_onglets).

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create Alias Seller SKU]**.

1. Pour **[!UICONTROL Assign New Seller SKU]**, saisissez une valeur alphanumérique unique.

   Cette valeur doit être unique (non utilisée pour un autre produit ou alias de votre catalogue).

1. Pour **[!UICONTROL Assign New ASIN]**, saisissez une valeur alphanumérique unique.

   Cette valeur est renseignée automatiquement avec le produit ASIN associé à votre produit de catalogue. La modification de cette valeur correspond à votre produit de catalogue pour deux listes Amazon basées sur ASIN.

1. Activez/désactivez la variable **[!UICONTROL Remove Existing Seller SKU]** au besoin.

   - `Yes` - Choisissez de supprimer la liste et de créer une liste à l’aide des nouvelles informations fournies.

   - `No` - Choisissez de créer une autre liste et de ne pas changer l’ancienne liste.

1. Cliquez sur **[!UICONTROL Save Listing Update]**.

![créer un SKU de fournisseur d’alias Amazon](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| Champ | Description |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | Saisissez une nouvelle valeur alphanumérique unique à lier au SKU du vendeur Amazon d’origine. Ce nombre est utilisé uniquement par le canal de vente Amazon pour correspondre à votre produit catalogue. Vous pouvez utiliser n’importe quelle valeur de SKU, mais la valeur ne peut être utilisée qu’une seule fois dans votre catalogue. |
| [!UICONTROL Assign New ASIN] | Saisissez la valeur ASIN pour la liste à laquelle vous souhaitez faire correspondre votre produit de catalogue. Ne modifiez ce champ que lorsque vous faites correspondre un seul produit du catalogue à ASIN pour une autre liste du même produit. Cette valeur doit correspondre à l’ASIN attribué par Amazon, sinon la liste ne sera pas rejetée par Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Options :<ul><li>**[!UICONTROL Yes]** - Choisissez de supprimer la liste et de créer une liste à l’aide des nouvelles informations fournies. La nouvelle liste apparaît dans la _[!UICONTROL Active]_et l’ancienne liste se déplace vers le_ Terminé&#x200B;_.</li><li>**[!UICONTROL No]** - Choisissez de créer une autre liste et de ne pas changer l’ancienne liste. Les deux listes apparaissent dans l’onglet Actif après la création de la nouvelle liste.</li></ul> |
