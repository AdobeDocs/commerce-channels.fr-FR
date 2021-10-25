---
title: Gérer les listes de produits par statut/onglet
description: Lorsque vous gérez vos annonces Amazon, vous pouvez appliquer des actions à vos annonces en fonction de leur état.
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Gérer les annonces de produits par statut/onglet

Le _[!UICONTROL Product Listings]_contient plusieurs onglets à partir desquels vous pouvez afficher le statut de toutes vos annonces et faire correspondre vos produits aux annonces Amazon.

Les tâches d’énumération disponibles diffèrent légèrement sur chaque onglet, mais le [commandes de l’espace de travail](./workspace-controls.md) sont identiques et vous permettent de personnaliser les données qui s’affichent pour vos annonces.

Options sous **[!UICONTROL Actions]** peut appliquer l’action à plusieurs annonces, tandis que les options sous **[!UICONTROL Select]** dans la _[!UICONTROL Action]_n’appliquez l’action qu’à la liste individuelle.

Voir aussi [Gérer les annonces par action](./managing-listings-by-action.md).

![Onglets Liste des produits](assets/amazon-product-listings-tabs.png)

| Onglet | Description | Actions |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Affiche votre [!DNL Commerce] les produits de catalogue qui répondent aux paramètres d’annonce définis mais qui manquent des informations requises par Amazon pour une annonce.<br><br>Si _[!UICONTROL Automatic List Action]_est défini sur `Automatically List Eligible Products` dans votre [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres, ces éléments sont vos **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Affiche vos annonces Amazon existantes (en fonction des informations reçues d’Amazon) qui ne correspondent pas à un produit dans votre [!DNL Commerce] catalogue. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Tester la correspondance automatique<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Affiche vos produits de catalogue prêts à créer des annonces Amazon, mais votre magasin est configuré pour ne pas publier automatiquement de nouvelles annonces. Cet onglet permet de publier manuellement vos nouvelles annonces.<br><br>Si _[!UICONTROL Automatic List Action]_est défini sur `Do Not Automatically List Eligible Products` dans votre [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres, ces éléments sont vos **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Affiche les produits de votre catalogue qui ont été publiés sur Amazon, mais Amazon n’a pas approuvé la liste pour l’état Actif. | [Fin Liste(s) sur Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Basculer vers Terminé par Amazon/Marchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Affiche vos annonces Amazon qui ont été associées à un produit dans votre [!DNL Commerce] , ont été publiés à Amazon et ont été par Amazon pour l’état Actif. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Basculer vers Terminé par Amazon/Marchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Affiche vos annonces Amazon qui répondent aux critères d&#39;un remplacement défini et auxquels le remplacement a été appliqué. Les remplacements ont priorité sur tout autre paramètre de compte. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Affiche vos annonces Amazon existantes qui ne sont plus éligibles, en fonction de votre définition [paramètres de liste](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Basculer vers Terminé par Amazon/Marchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Affiche vos annonces Amazon qui ont été manuellement terminées (supprimées) d&#39;Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Accès aux annonces de produits

1. Sur la _Administrateur_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL View Store]** sur la carte de magasin.

1. Dans le tableau de bord de stockage, cliquez sur **[!UICONTROL Manage Listings]** dans la _[!UICONTROL Store Listings]_.
