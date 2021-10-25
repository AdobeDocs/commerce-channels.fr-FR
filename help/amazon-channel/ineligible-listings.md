---
title: Annonces non éligibles
description: Le canal de vente Amazon fournit [!UICONTROL Ineligible] pour vous aider à gérer les articles ne sont pas éligibles en tant qu'annonce en fonction de vos règles d'annonce actuelles.
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Annonces non éligibles

Le _[!UICONTROL Ineligible]_affiche la liste de tous les produits actuellement publiés sur Amazon mais qui ne sont pas éligibles en tant qu’annonce en fonction de vos règles d’inscription actuelles. Si un produit précédent était éligible et que les règles de mise en vente sont modifiées pour le rendre maintenant inéligible, la quantité associée à un produit tombe à 0 et le produit est marqué comme_ inéligible _. Cependant, il est toujours présent sur votre [!DNL Amazon Seller Account].

Pour déplacer un produit hors de la _[!UICONTROL Ineligible]_, vous pouvez [modification de vos règles d&#39;annonce](./listing-rules.md) pour permettre à vos produits d’être éligibles.

Les actions disponibles sur le _[!UICONTROL Ineligible]_inclut :

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Choisissez de supprimer toutes les annonces sélectionnées du [!DNL Amazon Marketplace]. Voir [Fin d&#39;une liste Amazon](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Choisissez de modifier les paramètres de remplacement de la liste. Voir [Remplacements](./overrides.md) ou [Modification ou suppression d’un remplacement](./creating-editing-overrides.md#edit-override-single-listing).

Sous **[!UICONTROL Select]** dans la _[!UICONTROL Action]_colonne :

- **[!UICONTROL View Details]**: choisissez d’afficher les détails de la liste, y compris le [Journal d&#39;activité d&#39;annonce](./product-listing-details.md#listing-activity-log), [Prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing)et [Prix compétitif le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est destinée à l’affichage uniquement. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

- **[!UICONTROL Create Override]**: choisissez de créer un remplacement et de l&#39;appliquer à cette liste. Voir [Création d’un remplacement](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: choisissez de modifier l’ASIN affecté à votre produit de catalogue. Cette action est utilisée si un produit de votre catalogue a été associé à un ASIN incorrect. Voir [Modification d’un ASIN affecté](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: choisissez de créer une UGS d&#39;alias qui peut être utilisée pour créer une liste Amazon à partir du même produit de catalogue. Voir [Créer une référence de fournisseur d&#39;alias](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: choisissez de modifier la méthode d&#39;exécution associée à l&#39;ordre. Voir [Configuration des paramètres Remplir par](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: choisissez de supprimer la liste du [!DNL Amazon Marketplace]. Voir [Fin d&#39;une liste Amazon](./end-listings-manually.md).

>[!NOTE]
>Si vous avez des annonces en cours de traitement, le nombre d’annonces s’affiche dans un message au-dessus des onglets.

![Annonces Amazon non éligibles](assets/amazon-ineligible-listings.png)

Les pages d&#39;accueil du canal de vente Amazon partagent certaines parties communes [commandes de l’espace de travail](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

## Colonnes par défaut

| Colonne | Description |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | La référence SKU (Stock Keeping Unit) attribuée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Bloc unique de 10 lettres et/ou chiffres identifiant des éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou chiffres qui identifie des éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | Le [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix d&#39;annonce du produit plus son prix d&#39;expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié sur Amazon. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_et sélectionnez une option :<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[Créer un remplacement](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
