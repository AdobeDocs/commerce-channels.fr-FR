---
title: Gestion des listes de produits par action
description: Lorsque vous gérez vos listes Amazon, vous pouvez appliquer une action à des listes individuelles ou multiples.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Gestion des listes de produits par action

La page _[!UICONTROL Product Listings]_contient plusieurs onglets à partir desquels vous pouvez afficher les statuts de toutes vos listes et faire correspondre vos produits aux listes Amazon.

Les tâches de liste disponibles diffèrent légèrement sur chaque onglet, mais les [contrôles de l’espace de travail](./workspace-controls.md) sont identiques et vous permettent de personnaliser les données qui s’affichent pour vos listes.

Les options situées sous **[!UICONTROL Actions]** peuvent appliquer l’action à plusieurs listes, tandis que les options situées sous **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_peuvent appliquer l’action uniquement à la liste individuelle.

Voir aussi [Gérer les listes par statut / Onglet](./managing-listings-by-tab.md).

| Action | Description | Onglets |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Utilisé pour remettre les produits incomplets dans le processus de correspondance. Pour tenter de créer une correspondance, vous devez modifier les paramètres [Liste](./listing-settings.md) et [Recherche catalogue](./catalog-search.md) afin d’augmenter le potentiel de correspondance automatique. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Faites correspondre manuellement vos produits de catalogue aux listes Amazon en sélectionnant une liste à faire correspondre, en saisissant un ASIN à faire correspondre ou en affectant une condition manquante. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Affichez des informations supplémentaires sur vos produits principaux, y compris le journal des activités de liste, qui affiche les modifications sur un SKU/produit individuel. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Créez un [!DNL Commerce] catalogue de produits à l’aide des informations importées avec la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Tenter la correspondance automatique | Tenter une correspondance automatique entre votre catalogue [!DNL Commerce] et vos listes Amazon en fonction des paramètres des critères de recherche. Pour tenter de créer une correspondance, vous devez modifier les paramètres [Liste](./listing-settings.md) et [Recherche catalogue](./catalog-search.md) afin d’augmenter le potentiel de correspondance automatique. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Sélectionnez manuellement un produit existant dans votre catalogue [!DNL Commerce] et affectez-le à la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Créez un [!DNL Commerce] catalogue de produits à l’aide des informations importées avec la liste Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Action en masse) Utilisé pour mettre à nouveau en liste une liste qui a été terminée ou pour répertorier manuellement un produit qui répond à l’éligibilité de vos règles de liste, mais votre _[!UICONTROL Product Listing Actions]_n’est pas défini sur `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (Action de liste unique) Utilisé pour remettre en liste une liste qui a été terminée. Cette action est également utilisée pour répertorier manuellement un produit qui répond à l’éligibilité de vos règles de liste lorsque _[!UICONTROL Product Listing Actions]_n’est pas défini sur `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Action en masse) Utilisé pour terminer et supprimer manuellement les listes de vos produits qui existent dans Amazon. Les listes terminées peuvent être rérépertoriées tant qu’elles répondent aux règles d’éligibilité de votre liste. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Action en masse) Modifiez manuellement un &quot;remplacement&quot; existant qui définit le prix, le temps de traitement, la condition et le texte des notes de vendeur pour une liste individuelle, en ignorant les autres paramètres, paramètres et règles de liste par défaut. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Créez manuellement un &quot;remplacement&quot; qui définit le prix, le temps de traitement, la condition et le texte des notes de vendeur pour une liste individuelle, en ignorant les autres paramètres, paramètres et règles de liste par défaut. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Utilisé si ASIN correspond à votre produit de catalogue doit être modifié (exemple : si le produit a été associé à la mauvaise liste (ASIN). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Peut exécuter deux fonctions :<br><br>Peut être utilisé pour créer une relation 1-2 entre votre produit de catalogue et deux listes Amazon. Exemple : Le produit Amazon est répertorié avec différentes valeurs ASIN. Vous pouvez associer votre produit de catalogue à deux listes ASIN pour le produit.<br><br>Peut être utilisé pour contrôler une liste dans différentes régions d’Amazon. Exemple : Vous disposez d’un produit catalogue dont les méthodes de livraison sont différentes et qui est défini en fonction de la région Amazon (la région des États-Unis est FBA et la région du Canada est FBM). Pour contrôler le stock/la quantité, vous pouvez créer un SKU de vendeur d’alias et réinscrire le même produit dans cette région avec un SKU de vendeur différent. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Utilisé pour modifier la méthode d’exécution associée à votre produit (remplie par Amazon : FBA ou Fulful by Merchant : FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (Action de liste unique) Utilisé pour terminer et supprimer manuellement les listes de vos produits qui existent sur Amazon. Les listes terminées peuvent être rérépertoriées tant qu’elles répondent aux règles d’éligibilité de votre liste. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (Action de liste unique) Modifiez manuellement un &quot;remplacement&quot; existant qui définit le prix, le temps de traitement, la condition et le texte des notes de vendeur pour une liste individuelle, en ignorant les autres paramètres, paramètres et règles de liste par défaut. | [[!UICONTROL Overrides]](./overrides.md) |

## Accès aux listes de produits

1. Dans la barre latérale _Admin_, accédez à **Marketing** > _Canaux_ > **Sales Channel Amazon**.

1. Cliquez sur **Afficher le magasin** dans la carte du magasin.

1. Dans le tableau de bord du magasin, cliquez sur **Gérer les listes** dans la section _Listes du magasin_ .
