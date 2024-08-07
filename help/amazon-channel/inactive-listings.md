---
title: Listes Amazon inactives
description: Le canal de vente Amazon fournit l’onglet [!UICONTROL Inactive] pour surveiller vos listes  [!DNL Amazon Marketplace]  actuellement inactives.
feature: Sales Channels, Products
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Listes Amazon inactives

L’onglet _[!UICONTROL Inactive]_affiche vos produits qui ont été publiés sur Amazon mais ne sont pas actifs sur [!DNL Amazon Marketplace]. Vos listes peuvent être inactives pour plusieurs raisons différentes. Par exemple, vous pouvez ne pas être éligible à la liste de cette marque spécifique. Les listes inactives sont dictées par les normes de liste d’Amazon et les autorisations de votre compte [!DNL Amazon Seller Central].

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]** : choisissez de supprimer toutes les listes sélectionnées de [!DNL Amazon Marketplace]. Voir [Fin de la liste Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]** : choisissez de modifier les paramètres de remplacement de la liste. Voir [Overrides](./overrides.md) ou [Modification ou suppression d’un remplacement](./creating-editing-overrides.md#edit-override-single-listing).

Sous **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_:

- **[!UICONTROL View Details]** : choisissez d’afficher les détails de la liste, y compris le [journal d’activité de liste](./product-listing-details.md#listing-activity-log), le [prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing) et le [prix des concurrents le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est réservée à l’affichage. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

- **[!UICONTROL Create Override]** : choisissez de créer un remplacement et de l’appliquer à cette liste. Voir [Création d’un remplacement](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]** : choisissez de modifier l’ASIN affecté à votre produit de catalogue. Cette action est utilisée si un produit de votre catalogue a été associé à un ASIN incorrect. Voir [Modification d’une ASIN affectée](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]** : choisissez de créer un SKU d’alias (unité de gestion des stocks) qui peut être utilisé pour créer une liste Amazon à partir du même produit catalogue. Voir [Création d’un SKU de vendeur d’alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]** : choisissez de modifier la méthode d’exécution associée à la commande. Voir [Configuration de l’exécution par les paramètres](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]** : choisissez de supprimer la liste de [!DNL Amazon Marketplace]. Voir [Fin de la liste Amazon](./end-listings-manually.md).

>[!NOTE]
>
>Si des listes sont en cours de traitement, un message s’affiche au-dessus des onglets pour indiquer le nombre de listes.

![Listes Amazon inactives](assets/amazon-inactive-listings.png){width="600" zoomable="yes"}

Les pages d’accueil du canal de vente Amazon partagent quelques [contrôles d’espace de travail](./workspace-controls.md) courants qui vous permettent de personnaliser les données affichées.

| Colonne | Description |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | SKU (unité de gestion des stocks) affectée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Un bloc unique de 10 lettres et/ou chiffres qui identifient les éléments.<br><br>ASIN désigne les numéros d’identification Amazon Standard. Un ASIN est un bloc unique de 10 lettres et/ou nombres qui identifie les éléments. Pour les livres, l&#39;ASIN est le même que le numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l&#39;article est téléchargé dans son catalogue. Vous trouverez un ASIN d’articles sur la page des détails du produit dans Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix de vente du produit plus son prix d’expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié dans Amazon. |
| [!UICONTROL Status] | État de la liste, défini par Amazon. |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazon ne fournit pas toujours une raison pour les listes inactives et vous pouvez contacter le service clientèle pour résoudre les problèmes de liste. Dans certains cas, Amazon vous en informe. Pour afficher ces réponses, cliquez sur **[!UICONTROL View Details]** dans la colonne _[!UICONTROL Action]_. Si ces problèmes sont résolus et qu’Amazon supprime l’erreur, les produits sont déplacés vers l’onglet_[!UICONTROL Active]_. |
| Action | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_et sélectionnez l’option :<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
