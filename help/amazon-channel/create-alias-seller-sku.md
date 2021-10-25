---
title: Création d'une référence de fournisseur d'alias Amazon
description: Vous pouvez utiliser l'UGS du vendeur Alias Amazon pour créer des annonces Amazon multi-régionales à partir de vos produits de catalogue Commerce.
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Création d&#39;une référence de fournisseur d&#39;alias Amazon

An [!DNL Alias Amazon Seller SKU] est utilisé pour créer une liste Amazon à partir du même produit dans votre [!DNL Commerce] catalogue. Si vous êtes un vendeur Amazon expérimenté, vous connaissez peut-être le [Référence SKU globale Amazon](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target=&quot;_blank&quot;} et SKU spécifique à Marketplace pour le stock et l&#39;expédition. Suivant des principes similaires pour le canal de vente Amazon, l’UGS du vendeur Amazon contrôle les informations de mise en vente des produits au niveau multi-régional, ainsi que les [!DNL Alias Amazon Seller SKU] peut être utilisé pour contrôler les informations de mise en vente de produits au niveau d’une région spécifique.

Cette fonction peut être utilisée pour effectuer deux fonctions :

- Créer un [!DNL Alias Amazon Seller SKU] pour l’un de vos [!DNL Commerce] produits de catalogue pour contrôler les informations de liste spécifiques à une région.

   **Exemple**: Vous êtes un vendeur aux États-Unis et au Canada. N&#39;oubliez pas que chaque magasin de votre canal de vente Amazon ne peut se voir attribuer qu&#39;une seule région Amazon pendant la configuration. Ainsi, vous avez un magasin de canaux de vente Amazon avec une région définie des États-Unis et un autre magasin avec une région définie du Canada. Les deux magasins partagent votre [!DNL Commerce] pour afficher des informations dans les deux régions, y compris l’UGS du vendeur Amazon et les attributs de produit ASIN. Ainsi, les annonces pour le produit de catalogue seraient les mêmes dans les deux magasins, le partage de la tarification, le stock/la quantité et d’autres attributs de produit. Toutefois, votre stock pour votre magasin Canada est livré à partir d&#39;un emplacement au Canada et votre magasin américain à partir d&#39;un emplacement aux États-Unis. Ainsi, vous devez contrôler la quantité de la mise en vente séparément pour chaque magasin. Pour effectuer ce type de contrôle spécifique à une région, vous pouvez créer une référence SKU de vendeur d&#39;Alias Amazon.

   Pour l’essentiel, vous pouvez créer une référence SKU de vendeur d’Alias Amazon liée au même produit de catalogue et vous pouvez l’utiliser pour republier la même liste dans cette région.

- Créer un [!DNL Alias Amazon Seller SKU] et faites correspondre l’un de vos [!DNL Commerce] catalogue des produits vers deux annonces Amazon.

   **Exemple**: Vous disposez d’un produit de catalogue correspondant à une liste Amazon. Comme Amazon a fréquemment plusieurs annonces qui représentent le même produit, vous découvrez une autre annonce Amazon pour le même produit, mais Amazon a assigné un ASIN différent à la liste. Pour augmenter la visibilité de votre produit à inclure, vous souhaitez faire correspondre votre produit de catalogue aux différents ASIN et créer des listes pour les deux valeurs ASIN. Pour ce faire, vous pouvez créer une référence SKU de vendeur d&#39;Alias Amazon.

   Pour l’essentiel, vous pouvez créer un [!DNL Alias Amazon Seller SKU] qui peut être utilisé pour faire correspondre un seul produit de catalogue à une deuxième liste Amazon et créer une liste pour le nouveau ASIN mis en correspondance. Dans ce scénario, vous auriez deux annonces Amazon pour le même produit de catalogue.

   Une fois que vous avez créé une UGS de vendeur d&#39;Alias Amazon, vous pouvez utiliser vos paramètres d&#39;annonce, règles et remplacements pour contrôler les informations d&#39;annonce pour la région. Les attributs de produit qui peuvent être définis par région pour une annonce comprennent la quantité/le stock, la méthode d’exécution, la condition, l’éligibilité du produit et le temps de manutention.

## Utilisé à des fins spécifiques à une région {#region-specific}

Afficher la liste sur le _[!UICONTROL Product Listings]_page (_[!UICONTROL Inactive]_, _Actif_, _Inéligible_, ou _Terminé_ ).

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create Alias Seller SKU]**.

1. Pour **[!UICONTROL Assign New Seller SKU]**, entrez une valeur alphanumérique unique.

   Cette valeur doit être unique (non utilisée pour un autre produit ou alias de votre catalogue).

1. Pour **[!UICONTROL Assign New ASIN]**, ne changez rien.

   Cette valeur est remplie automatiquement avec le produit ASIN correspondant à votre produit de catalogue. La modification de cette valeur correspond à votre produit de catalogue en deux annonces Amazon basées sur ASIN.

1. Activer/Désactiver la **[!UICONTROL Remove Existing Seller SKU]** si nécessaire.

   - `Yes` - Choisissez de supprimer la liste et de créer une liste à l&#39;aide des nouvelles informations fournies.

   - `No` - Choisissez de créer une annonce et de conserver l&#39;ancienne annonce inchangée.

1. Cliquez sur **[!UICONTROL Save Listing Update]**.

## Utilisé pour faire correspondre un seul produit de catalogue à deux annonces Amazon

1. Afficher la liste sur le _[!UICONTROL Product Listings]_page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_, ou _[!UICONTROL Ended]_).

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create Alias Seller SKU]**.

1. Pour **[!UICONTROL Assign New Seller SKU]**, entrez une valeur alphanumérique unique.

   Cette valeur doit être unique (non utilisée pour un autre produit ou alias de votre catalogue).

1. Pour **[!UICONTROL Assign New ASIN]**, entrez une valeur alphanumérique unique.

   Cette valeur est remplie automatiquement avec le produit ASIN correspondant à votre produit de catalogue. La modification de cette valeur correspond à votre produit de catalogue en deux annonces Amazon basées sur ASIN.

1. Activer/Désactiver la **[!UICONTROL Remove Existing Seller SKU]** si nécessaire.

   - `Yes` - Choisissez de supprimer la liste et de créer une liste à l&#39;aide des nouvelles informations fournies.

   - `No` - Choisissez de créer une autre annonce et de conserver l&#39;ancienne annonce inchangée.

1. Cliquez sur **[!UICONTROL Save Listing Update]**.

![créer une référence SKU de vendeur d&#39;alias Amazon](assets/amazon-alias-sku-create.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | Entrez une nouvelle valeur alphanumérique unique à lier à la référence SKU du vendeur Amazon d&#39;origine. Ce numéro est uniquement utilisé par le canal de vente Amazon pour correspondre à votre produit de catalogue. Vous pouvez utiliser n’importe quelle valeur SKU, mais cette valeur ne peut être utilisée qu’une seule fois dans votre catalogue. |
| [!UICONTROL Assign New ASIN] | Entrez la valeur ASIN pour la liste à laquelle vous souhaitez faire correspondre votre produit de catalogue. Modifiez uniquement ce champ lors de la correspondance d’un produit de catalogue unique avec l’ASIN pour une autre annonce pour le même produit. Cette valeur doit correspondre à l’ASIN assigné par Amazon ou la liste ne sera pas rejetée par Amazon. |
| [!UICONTROL Remove Existing Seller SKU] | Options :<ul><li>**[!UICONTROL Yes]** - Choisissez de supprimer la liste et de créer une liste à l&#39;aide des nouvelles informations fournies. La nouvelle liste s’affiche dans la boîte de dialogue _[!UICONTROL Active]_, et l’ancienne liste se déplace vers la_ Terminé&#x200B;_.</li><li>**[!UICONTROL No]** - Choisissez de créer une autre annonce et de conserver l&#39;ancienne annonce inchangée. Les deux annonces apparaissent dans l’onglet Actif après la création de la nouvelle annonce.</li></ul> |
