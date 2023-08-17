---
title: Listes Amazon incomplètes
description: Le canal de vente Amazon fournit la variable [!UICONTROL Incomplete] pour vous aider à identifier et à répondre aux exigences d’éligibilité de vos listes Amazon incomplètes.
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Listes Amazon incomplètes

La variable _[!UICONTROL Incomplete]_répertorie les [!DNL Commerce] catalogue des produits qui répondent à vos exigences d’éligibilité Amazon (définies dans votre [règles de liste](./listing-rules.md)), mais sont des informations manquantes requises par Amazon (comme Amazon ASIN ou une condition de produit définie).

Il existe quatre causes possibles à une liste incomplète, chacune identifiée par son état.

| État | Motif | Action |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Condition manquante | Amazon accepte les listes dans diverses conditions (telles que _Nouveau_, _Réaménagé_, _Utilisé : Comme nouveau_) La liste nécessite une condition définie. | Mise à jour manuelle des informations requises [attribuer une condition ;](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) à une liste. |
| Impossible d’affecter à la liste Amazon | Échec de la correspondance automatique de cette liste avec votre catalogue. Si aucune correspondance n’est trouvée, la liste ne peut pas être gérée par Amazon Sales Channel. | Mise à jour manuelle des informations requises [attribuer un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) au produit du catalogue pour le faire correspondre à la liste. |
| Plusieurs correspondances trouvées | Échec de la correspondance automatique de cette liste avec votre catalogue. Si plusieurs correspondances possibles sont trouvées, vous devez sélectionner la correspondance correcte pour votre produit. | Mise à jour manuelle des informations requises [choix d’une correspondance de produit](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) pour le produit et la liste. |
| Contient des variantes | Si votre produit comporte des variantes, telles qu’un t-shirt disponible dans différentes tailles ou couleurs, vous devez choisir la variante de votre catalogue à attribuer et à associer correctement à la liste. | Mise à jour manuelle des informations requises [choisir la variante correcte](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) pour affecter et associer à cette liste. |

>[!NOTE]
>Lorsque des listes incomplètes sont correctement mises en correspondance avec vos produits de catalogue, la liste est déplacée à partir de la variable _[!UICONTROL Incomplete]_et sont publiés dans Amazon en fonction de vos [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres.

Les actions disponibles sur la page _[!UICONTROL Incomplete]_comprend :

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: choisissez de lancer le processus automatique de mise en correspondance de vos données de liste Amazon avec vos [!DNL Commerce] catalogue. Si les produits ne correspondent pas automatiquement, consultez à nouveau votre [_[!UICONTROL Catalog Search]_](./catalog-search.md) options de vos listes. Si les listes ne correspondent pas automatiquement après la mise à jour de votre _[!UICONTROL Catalog Search]_, vous pouvez associer manuellement les produits dans la variable [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) action.

Sous **[!UICONTROL Select]** dans le _[!UICONTROL Action]_column :

- **[!UICONTROL Update Required Info]**: choisissez cette option lorsque les listes ne correspondent pas automatiquement à votre catalogue. Vous pouvez manuellement [faire correspondre les produits du catalogue aux listes](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), manuellement [attribuer un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) à une correspondance de catalogue ; ou [attribuer une condition manquante](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) pour les listes.

- **[!UICONTROL View Details]**: choisissez d’afficher les détails de la liste, y compris le [Lister le journal d’activité](./product-listing-details.md#listing-activity-log), [Tarifs des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing), et [Tarifs des concurrents les plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est réservée à l’affichage. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

>[!NOTE]
>
>Si des listes sont en cours de traitement, le nombre de listes apparaît dans un message au-dessus des onglets.

![Listes Amazon incomplètes](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Les pages d’accueil du canal de vente Amazon partagent certaines [contrôles workspace](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

| Colonne | Description |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | SKU (unité de gestion des stocks) affectée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Un bloc unique de 10 lettres et/ou chiffres qui identifient les éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou nombres qui identifie les éléments. Pour les livres, l&#39;ASIN est le même que le numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l&#39;article est téléchargé dans son catalogue. Vous trouverez un ASIN d’articles sur la page des détails du produit dans Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | La variable [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix de vente du produit plus son prix d’expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié dans Amazon. |
| [!UICONTROL Status] | État de la liste, défini par Amazon. Voir le tableau Statut ci-dessus. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans le _[!UICONTROL Action]_et sélectionnez une option :<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
