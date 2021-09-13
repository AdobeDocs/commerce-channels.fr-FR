---
title: Gérer les listes de produits par statut/onglet
description: Lorsque vous gérez vos listes Amazon, vous pouvez appliquer des actions à vos listes en fonction de leur état.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Gérer les listes de produits par statut/onglet

La page _[!UICONTROL Product Listings]_contient plusieurs onglets à partir desquels vous pouvez afficher les statuts de toutes vos listes et faire correspondre vos produits aux listes Amazon.

Les tâches de liste disponibles diffèrent légèrement sur chaque onglet, mais les [contrôles de l’espace de travail](./workspace-controls.md) sont identiques et vous permettent de personnaliser les données qui s’affichent pour vos listes.

Les options situées sous **[!UICONTROL Actions]** peuvent appliquer l’action à plusieurs listes, tandis que les options situées sous **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_peuvent appliquer l’action uniquement à la liste individuelle.

Voir aussi [Gestion des listes par action](./managing-listings-by-action.md).

![Onglets Listes de produits](assets/amazon-product-listings-tabs.png)

| Onglet | Description | Actions |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Affiche vos [!DNL Commerce] produits de catalogue qui correspondent aux paramètres de liste définis, mais qui ne contiennent pas les informations requises par Amazon pour une liste.<br><br>Si  _[!UICONTROL Automatic List Action]_est défini sur  `Automatically List Eligible Products` dans vos  [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres, ces éléments sont les vôtres **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Affiche vos listes Amazon existantes (en fonction des informations reçues d’Amazon) qui ne correspondent pas à un produit de votre catalogue [!DNL Commerce]. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tenter la correspondance automatique<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Affiche vos produits de catalogue prêts à créer des listes Amazon, mais votre boutique n’est pas configurée pour publier automatiquement de nouvelles listes. Cet onglet est utilisé pour publier manuellement vos nouvelles listes.<br><br>Si  _[!UICONTROL Automatic List Action]_est défini sur  `Do Not Automatically List Eligible Products` dans vos  [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres, ces éléments sont les vôtres **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Affiche les produits de votre catalogue qui ont été publiés sur Amazon, mais qu’Amazon n’a pas approuvé la liste pour le statut Principal. | [ FinListing(s) sur ](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>AmazonSwitch to Fulfill by Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Affiche les listes Amazon qui ont été associées à un produit de votre catalogue [!DNL Commerce], qui ont été publiées sur Amazon et qui ont été par Amazon pour un statut Principal. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Basculer vers la version remplie par Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Affiche vos listes Amazon qui répondent aux critères d’un remplacement défini et auxquelles le remplacement a été appliqué. Les remplacements sont prioritaires sur tout autre paramètre de compte. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Affiche vos listes Amazon existantes qui ne sont plus éligibles, en fonction des [paramètres de liste](./listing-settings.md) que vous avez définis. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Basculer vers la version remplie par Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Affiche les listes Amazon qui ont été supprimées manuellement d’Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Accès aux listes de produits

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL View Store]** dans la carte du magasin.

1. Dans le tableau de bord de la boutique, cliquez sur **[!UICONTROL Manage Listings]** dans la section _[!UICONTROL Store Listings]_.
