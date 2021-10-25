---
title: Prêt pour la liste
description: Le canal de vente Amazon fournit l'onglet Prêt à dresser la liste pour vous aider à passer en revue les produits commerciaux qui répondent aux critères d'admissibilité mais qui ne sont pas automatiquement répertoriés.
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

Le _[!UICONTROL Ready to List]_affiche votre [!DNL Commerce] produits de catalogue qui répondent aux paramètres de votre annonce et sont prêts à être publiés sur Amazon en tant que **nouveau**liste. Contrairement aux autres onglets de liste, cet onglet n’apparaît pas toujours sur la [_[!UICONTROL Product Listings]_](./managing-product-listings.md) .

Le _[!UICONTROL Ready to List]_apparaît uniquement lorsque [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) dans vos paramètres d&#39;annonce sont définis sur `Do Not Automatically List Eligible Products`. Ce paramètre indique au canal de vente Amazon que toute nouvelle annonce Amazon doit être publiée manuellement.

Lorsque [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) est défini sur `Automatically List Eligible Products`, Amazon Sales Channel publie automatiquement les nouvelles annonces pour vos produits de catalogue éligibles. Étant donné que de nouvelles annonces sont publiées automatiquement, la _[!UICONTROL Ready to List]_n’est pas affiché.

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: Choisissez de republier la liste dans le dossier [!DNL Amazon Marketplace]. Voir [Publication d&#39;une liste Amazon](./publish-listings-manually.md)

Sous **[!UICONTROL Select]** dans la _[!UICONTROL Action]_colonne :

- **[!UICONTROL Publish On Amazon]**: Choisissez de republier la liste dans le dossier [!DNL Amazon Marketplace]. Voir [Publication d&#39;une liste Amazon](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: choisissez d’afficher les détails de la liste, y compris le [Journal d&#39;activité d&#39;annonce](./product-listing-details.md#listing-activity-log), [Prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing)et [Prix compétitif le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est destinée à l’affichage uniquement. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

Vous disposez de quelques options pour effectuer manuellement [publier une nouvelle annonce sur Amazon](./publish-listings-manually.md).

>[!NOTE]
>Si vous avez des annonces en cours de traitement, le nombre d’annonces s’affiche dans un message au-dessus des onglets.

![Prêt pour la liste](assets/amazon-ready-to-list.png)

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Amazon Seller SKU] | La référence SKU (Stock Keeping Unit) attribuée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Bloc unique de 10 lettres et/ou chiffres identifiant des éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou chiffres qui identifie des éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | Le [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix d&#39;annonce du produit plus son prix d&#39;expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié sur Amazon. |
| [!UICONTROL Status] | Statut de la liste, défini par Amazon. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_et choisissez une option :<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causes courantes des listes Prêt à répertorier

- **[!UICONTROL Ready to List]** - Le produit est mis en correspondance avec un Amazon ASIN et doit être mis en vente. Si [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) dans vos paramètres d&#39;annonce sont définis sur `Do Not Automatically List Eligible Products`, ce statut représente les produits prêts à être listés manuellement.

- **[!UICONTROL List in Progress]** - La liste des produits a été soumise à Amazon et attend la confirmation de l&#39;acceptation de Amazon.
