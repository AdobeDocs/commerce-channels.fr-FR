---
title: Annonces incomplètes
description: Le canal de vente Amazon fournit [!UICONTROL Incomplete] pour vous aider à identifier et à respecter les exigences d’éligibilité pour vos annonces Amazon incomplètes.
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Annonces incomplètes

Le _[!UICONTROL Incomplete]_répertorie les [!DNL Commerce] produits de catalogue répondant à vos exigences d’éligibilité Amazon (définis dans votre [règles d&#39;inscription](./listing-rules.md)), mais sont des informations manquantes requises par Amazon (telles que l’ASIN Amazon ou une condition de produit définie).

Il existe quatre causes possibles d&#39;une liste incomplète, chacune étant identifiée par son statut.

| Statut | Raison | Action |
|--- |--- |--- |
| Condition manquante | Amazon accepte les annonces dans diverses conditions (par exemple, _Nouveau_, _Rénové_, _Utilisé : Comme Nouveau_) nécessite une condition définie. | Mettre à jour les informations requises et manuellement [assigner une condition](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) à une annonce. |
| Impossible d&#39;assigner à une liste Amazon | Échec de la correspondance automatique de cette liste avec votre catalogue. Si aucune correspondance n’est trouvée, la liste ne peut pas être gérée par l’Sales Channel Amazon | Mettre à jour les informations requises et manuellement [assigner un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) au produit du catalogue pour la mise en correspondance avec la liste. |
| Plusieurs correspondances trouvées | Échec de la correspondance automatique de cette liste avec votre catalogue. Si plusieurs correspondances possibles sont trouvées, vous devez sélectionner la correspondance correcte pour votre produit. | Mettre à jour les informations requises et manuellement [choisir une correspondance de produit](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) pour le produit et la mise en vente. |
| Contient des variantes | Si votre produit comporte des variantes, telles qu’un t-shirt disponible dans différentes tailles ou couleurs, vous devez choisir la variante de votre catalogue à attribuer correctement et la faire correspondre à la liste | Mettre à jour les informations requises et manuellement [choisir la variante correcte](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) pour affecter et faire correspondre à cette liste. |

>[!NOTE]
>Lorsque des annonces incomplètes sont correctement associées à vos produits de catalogue, la liste se déplace de la _[!UICONTROL Incomplete]_et sont publiés dans Amazon en fonction de votre [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) paramètres.

Les actions disponibles sur le _[!UICONTROL Incomplete]_inclut :

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Choisissez de lancer le processus automatique de mise en correspondance des données de vos annonces Amazon avec votre [!DNL Commerce] catalogue. Si les produits ne correspondent pas automatiquement, consultez à nouveau votre [_[!UICONTROL Catalog Search]_](./catalog-search.md) dans vos annonces. Si les annonces ne correspondent pas automatiquement après la mise à jour de votre _[!UICONTROL Catalog Search]_, vous pouvez faire correspondre les produits manuellement dans la boîte de dialogue [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) action.

Sous **[!UICONTROL Select]** dans la _[!UICONTROL Action]_colonne :

- **[!UICONTROL Update Required Info]**: Choisissez lorsque les annonces ne correspondent pas automatiquement à votre catalogue. Vous pouvez [mise en correspondance des produits de catalogue avec les annonces](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found), manuellement [assigner un ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) à une correspondance de catalogue, ou [assigner une condition manquante](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) pour l’annonce.

- **[!UICONTROL View Details]**: choisissez d’afficher les détails de la liste, y compris le [Journal d&#39;activité d&#39;annonce](./product-listing-details.md#listing-activity-log), [Prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing)et [Prix compétitif le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est destinée à l’affichage uniquement. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

>[!NOTE]
>
>Si vous avez des annonces en cours de traitement, le nombre d’annonces s’affiche dans un message au-dessus des onglets.

![Listes Amazon incomplètes](assets/amazon-incomplete-listings.png)

Les pages d&#39;accueil du canal de vente Amazon partagent certaines parties communes [commandes de l’espace de travail](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

| Colonne | Description |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | La référence SKU (Stock Keeping Unit) attribuée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Bloc unique de 10 lettres et/ou chiffres identifiant des éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou chiffres qui identifie des éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | Le [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix d&#39;annonce du produit plus son prix d&#39;expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié sur Amazon. |
| [!UICONTROL Status] | Statut de la liste, défini par Amazon. Voir le tableau d’état ci-dessus. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_et sélectionnez une option :<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
