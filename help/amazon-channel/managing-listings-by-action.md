---
title: Gérer les listes de produits par action
description: Lorsque vous gérez vos annonces Amazon, vous pouvez appliquer une action à des annonces individuelles ou multiples.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Gestion des annonces de produits par action

Le _[!UICONTROL Product Listings]_contient plusieurs onglets à partir desquels vous pouvez afficher le statut de toutes vos annonces et faire correspondre vos produits aux annonces Amazon.

Les tâches d’énumération disponibles diffèrent légèrement sur chaque onglet, mais le [commandes de l’espace de travail](./workspace-controls.md) sont identiques et vous permettent de personnaliser les données qui s’affichent pour vos annonces.

Options sous **[!UICONTROL Actions]** peut appliquer l’action à plusieurs annonces, tandis que les options sous **[!UICONTROL Select]** dans la _[!UICONTROL Action]_n’appliquez l’action qu’à la liste individuelle.

Voir aussi [Gérer les annonces par statut/onglet](./managing-listings-by-tab.md).

| Action | Description | Onglets |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Utilisé pour déplacer les produits incomplets à travers le processus de correspondance. Pour tenter de rétablir la correspondance, vous devez modifier votre [Liste](./listing-settings.md) et [Recherche de catalogue](./catalog-search.md) pour augmenter le potentiel de correspondance automatique. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Faites correspondre manuellement vos produits de catalogue aux annonces Amazon en sélectionnant une liste à faire correspondre, en saisissant un ASIN à faire correspondre ou en assignant une condition manquante. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Affichez des informations supplémentaires sur vos produits actifs, y compris le journal d’activité d’annonce, qui affiche les modifications sur une UGS/un produit individuel. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Créer un [!DNL Commerce] produit de catalogue à l’aide des informations importées avec la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Tester la correspondance automatique | Tentative d’une correspondance automatique entre [!DNL Commerce] et vos annonces Amazon en fonction des paramètres de critères de recherche. Pour tenter de rétablir la correspondance, vous devez modifier votre [Liste](./listing-settings.md) et [Recherche de catalogue](./catalog-search.md) pour augmenter le potentiel de correspondance automatique. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Sélectionnez manuellement un produit existant dans votre [!DNL Commerce] et attribuez-le à la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Créer un [!DNL Commerce] produit de catalogue à l’aide des informations importées avec la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Action de masse) Utilisé pour mettre à jour une annonce qui a été terminée ou pour répertorier manuellement un produit qui répond aux règles d’éligibilité de votre annonce, mais _[!UICONTROL Product Listing Actions]_n’est pas défini sur `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (Action d&#39;annonce unique) Permet de mettre en vente une annonce qui a été terminée. Cette action est également utilisée pour répertorier manuellement un produit qui répond à vos règles d’éligibilité de mise en vente lorsque _[!UICONTROL Product Listing Actions]_n’est pas défini sur `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Action en masse) Permet de mettre fin manuellement et de supprimer les annonces pour vos produits qui existent sur Amazon. Les annonces terminées peuvent être mises en vente à condition qu’elles respectent les règles d’éligibilité de votre annonce. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Action en haut volume) Modifiez manuellement un &quot;remplacement&quot; existant qui définit le prix, le temps de traitement, la condition et le texte des notes du vendeur pour une annonce individuelle, en ignorant les autres valeurs par défaut, paramètres et règles de mise en vente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Créez manuellement un &quot;remplacement&quot; qui définit le prix, le délai de traitement, la condition et le texte des notes du vendeur pour une annonce individuelle, en ignorant les autres valeurs par défaut, paramètres et règles de la mise en vente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Utilisé si l’ASIN correspondant à votre produit de catalogue doit être modifié (exemple : si le produit a été mis en correspondance avec la mauvaise liste (ASIN). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Peut remplir deux fonctions :<br><br>Peut être utilisé pour créer une relation 1 à 2 entre votre produit de catalogue et deux annonces Amazon. Exemple : Le produit Amazon est répertorié avec des valeurs ASIN différentes. Vous pouvez faire correspondre votre seul produit de catalogue aux deux annonces ASIN pour le produit.<br><br>Peut être utilisé pour contrôler une liste dans différentes régions de Amazon. Exemple : Vous disposez d’un produit de catalogue dont les méthodes d’expédition sont différentes et sont définies en fonction de la région Amazon (la région des États-Unis est FBA et la région du Canada est FBM). Pour contrôler les stocks/quantités, vous pouvez créer une UGS de vendeur d&#39;alias et mettre à jour le même produit dans cette région avec une UGS de vendeur différente. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Utilisé pour modifier la méthode d’exécution associée à votre produit (Rempli par Amazon : FBA ou Fulful by Merchant : FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (Action d’annonce unique) Permet de mettre fin manuellement et de supprimer des annonces pour vos produits qui existent sur Amazon. Les annonces terminées peuvent être mises en vente à condition qu’elles respectent les règles d’éligibilité de votre annonce. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (Action d&#39;annonce unique) Modifiez manuellement un &quot;remplacement&quot; existant qui définit le prix, le délai de traitement, la condition et le texte des notes du vendeur pour une annonce individuelle, en ignorant les autres valeurs par défaut, paramètres et règles de l&#39;annonce. | [[!UICONTROL Overrides]](./overrides.md) |

## Accès aux annonces de produits

1. Sur la _Administrateur_ barre latérale, accédez à **Marketing** > _Canaux_ > **Sales Channel Amazon**.

1. Cliquez sur **Afficher la Boutique** sur la carte de magasin.

1. Dans le tableau de bord de stockage, cliquez sur **Gérer les annonces** dans la _Listes de magasins_ .
