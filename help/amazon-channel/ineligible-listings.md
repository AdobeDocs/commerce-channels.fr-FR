---
title: Listes Amazon non éligibles
description: Le canal de vente Amazon fournit l’onglet [!UICONTROL Ineligible] pour vous aider à gérer les articles qui ne sont pas éligibles en tant que liste en fonction de vos règles de liste actuelles.
feature: Sales Channels, Products
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Listes Amazon non éligibles

L’onglet _[!UICONTROL Ineligible]_affiche une liste de tous les produits actuellement publiés sur Amazon, mais qui ne sont pas éligibles en tant que liste en fonction de vos règles de liste actuelles. Si un produit précédent était éligible et que les règles de liste sont modifiées pour le rendre désormais inéligible, la quantité associée à un produit passe à 0 et le produit est marqué comme_ inéligible _. Cependant, il est toujours présent sur votre [!DNL Amazon Seller Account].

Pour déplacer un produit hors de l’onglet _[!UICONTROL Ineligible]_, vous pouvez [modifier les règles de liste](./listing-rules.md) pour autoriser vos produits à être éligibles.

Les actions disponibles sur l’onglet _[!UICONTROL Ineligible]_sont les suivantes :

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]** : choisissez de supprimer toutes les listes sélectionnées de [!DNL Amazon Marketplace]. Voir [Fin de la liste Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]** : choisissez de modifier les paramètres de remplacement de la liste. Voir [Overrides](./overrides.md) ou [Modification ou suppression d’un remplacement](./creating-editing-overrides.md#edit-override-single-listing).

Sous **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_:

- **[!UICONTROL View Details]** : choisissez d’afficher les détails de la liste, y compris le [journal d’activité de liste](./product-listing-details.md#listing-activity-log), le [prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing) et le [prix des concurrents le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est réservée à l’affichage. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

- **[!UICONTROL Create Override]** : choisissez de créer un remplacement et de l’appliquer à cette liste. Voir [Création d’un remplacement](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]** : choisissez de modifier l’ASIN affecté à votre produit de catalogue. Cette action est utilisée si un produit de votre catalogue a été associé à un ASIN incorrect. Voir [Modification d’une ASIN affectée](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]** : choisissez de créer un SKU d’alias pouvant être utilisé pour créer une liste Amazon à partir du même produit de catalogue. Voir [Création d’un SKU de vendeur d’alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]** : choisissez de modifier la méthode d’exécution associée à la commande. Voir [Configuration de l’exécution par les paramètres](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]** : choisissez de supprimer la liste de [!DNL Amazon Marketplace]. Voir [Fin de la liste Amazon](./end-listings-manually.md).

>[!NOTE]
>Si des listes sont en cours de traitement, le nombre de listes est affiché dans un message au-dessus des onglets.

![Listes Amazon non éligibles](assets/amazon-ineligible-listings.png){width="600" zoomable="yes"}

Les pages d’accueil du canal de vente Amazon partagent quelques [contrôles d’espace de travail](./workspace-controls.md) courants qui vous permettent de personnaliser les données affichées.

## Colonnes par défaut

| Colonne | Description |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | SKU (unité de gestion des stocks) affectée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Un bloc unique de 10 lettres et/ou chiffres qui identifient les éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou nombres qui identifie les éléments. Pour les livres, l&#39;ASIN est le même que le numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l&#39;article est téléchargé dans son catalogue. Vous trouverez un ASIN d’articles sur la page des détails du produit dans Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix de vente du produit plus son prix d’expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié dans Amazon. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_et sélectionnez une option :<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Créer un remplacement](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
