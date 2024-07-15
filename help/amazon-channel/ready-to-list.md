---
title: Canal de vente Amazon - [!UICONTROL Ready to List]
description: Le canal de vente Amazon fournit l’onglet Prêt pour la liste pour vous aider à passer en revue les produits Commerce qui répondent à l’éligibilité, mais qui ne sont pas automatiquement répertoriés.
feature: Sales Channels, Products, Merchandising
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

L’onglet _[!UICONTROL Ready to List]_affiche vos produits de catalogue [!DNL Commerce] qui correspondent aux paramètres de votre liste et qui sont prêts à être publiés sur Amazon en tant que **nouvelle**liste. Contrairement aux autres onglets de liste, cet onglet n’apparaît pas toujours sur la page [_[!UICONTROL Product Listings]_](./managing-product-listings.md).

L’onglet _[!UICONTROL Ready to List]_s’affiche uniquement lorsque [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) de vos paramètres de liste est défini sur `Do Not Automatically List Eligible Products`. Ce paramètre indique au canal de vente Amazon que toute nouvelle liste Amazon doit être publiée manuellement.

Lorsque [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) est défini sur `Automatically List Eligible Products`, le canal de vente Amazon publie automatiquement de nouvelles listes pour vos produits de catalogue éligibles. Comme les nouvelles listes sont publiées automatiquement, l&#39;onglet _[!UICONTROL Ready to List]_ne s&#39;affiche pas.

Sous _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]** : choisissez de republier la liste sur [!DNL Amazon Marketplace]. Voir [Publish and Amazon List](./publish-listings-manually.md)

Sous **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_:

- **[!UICONTROL Publish On Amazon]** : choisissez de republier la liste sur [!DNL Amazon Marketplace]. Voir [Publish and Amazon List](./publish-listings-manually.md).

- **[!UICONTROL View Details]** : choisissez d’afficher les détails de la liste, y compris le [journal d’activité de liste](./product-listing-details.md#listing-activity-log), le [prix des concurrents Buy Box](./product-listing-details.md#buy-box-competitor-pricing) et le [prix des concurrents le plus bas](./product-listing-details.md#lowest-competitor-pricing). Cette action est réservée à l’affichage. Aucune modification ne peut être apportée aux détails de la liste. Voir [Afficher les détails](./product-listing-details.md).

Vous disposez de quelques options pour [publier manuellement une nouvelle liste sur Amazon](./publish-listings-manually.md).

>[!NOTE]
>Si des listes sont en cours de traitement, le nombre de listes est affiché dans un message au-dessus des onglets.

![Prêt à répertorier](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## Colonnes par défaut

| Colonne | Description |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | SKU (unité de gestion des stocks) affectée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Un bloc unique de 10 lettres et/ou chiffres qui identifient les éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou nombres qui identifie les éléments. Pour les livres, l&#39;ASIN est le même que le numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l&#39;article est téléchargé dans son catalogue. Vous trouverez un ASIN d’articles sur la page des détails du produit dans Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Condition] | [condition](./product-listing-condition.md) du produit. |
| [!UICONTROL Landed Price] | Le prix de vente du produit plus son prix d’expédition. |
| [!UICONTROL Amazon Quantity] | Quantité disponible lorsque le produit est activement répertorié dans Amazon. |
| [!UICONTROL Status] | État de la liste, défini par Amazon. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_et choisissez une option :<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Causes courantes des listes prêtes à l’emploi

- **[!UICONTROL Ready to List]** - Le produit est associé à un ASIN Amazon et est planifié pour être répertorié. Si [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) est défini sur `Do Not Automatically List Eligible Products` dans les paramètres de liste, cet état représente les produits prêts à être répertoriés manuellement.

- **[!UICONTROL List in Progress]** - La liste de produits a été envoyée à Amazon et attend la confirmation de son acceptation par Amazon.
