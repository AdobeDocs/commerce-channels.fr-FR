---
title: AMAZON SALES CHANNEL - [!UICONTROL Third-party Listings]
description: Mettez à jour les paramètres de liste tiers pour déterminer si votre catalogue Commerce importe des produits à partir de vos listes Amazon Seller Central existantes.
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

Les paramètres de liste tiers font partie de vos paramètres de liste de magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord de la boutique](./amazon-store-dashboard.md).

Ces paramètres déterminent si la variable [!DNL Commerce] le catalogue importe les produits à partir de votre [!DNL Amazon Seller Central] des listes. Il est recommandé d’importer des listes à partir d’Amazon afin de s’assurer que toutes les listes correspondent. [!DNL Commerce] produits. Lorsque vos listes font partie de vos [!DNL Commerce] catalogue, vous pouvez gérer tous vos produits à partir d’un seul catalogue et utiliser les fonctionnalités du canal de vente Amazon. Ces fonctionnalités comprennent la gestion des commandes et de l’exécution avec Amazon, la retarification intelligente et la gestion des quantités.

Lorsqu’il est configuré pour importer vos listes Amazon, le canal de vente Amazon importe vos listes Amazon dans vos [!DNL Commerce] Catalogue, en tentant de les faire correspondre aux produits existants. Si une correspondance n’est pas automatiquement trouvée, vous pouvez importer la liste Amazon en tant que nouvelle [!DNL Commerce] produit ou associer manuellement la liste à un produit.

Si vous choisissez d&#39;importer vos listes Amazon, choisissez la [!DNL Commerce] attributs avec des valeurs pour le SKU du vendeur Amazon et Amazon ASIN. Si vous n’avez pas [!DNL Commerce] [attributs de produit](./ob-creating-magento-attributes.md), envisagez de les créer et de les affecter. Le mappage de ces attributs permet de faire correspondre correctement les listes Amazon importées à vos [!DNL Commerce] produits.

L’importation initiale des listes démarre lorsque [intégration de magasin](./store-integration.md) est terminée. Ensuite et en fonction de vos paramètres cron, [!DNL Commerce] recherche continuellement les listes Amazon nouvellement ajoutées (non créées dans Amazon Sales Channel) et met à jour votre [!DNL Commerce] catalogue en fonction de vos paramètres de liste tiers.

## Configuration de paramètres de liste tiers

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord de la boutique.

1. Développez l’objet _[!UICONTROL Third Party Listings]_.

1. Pour **[!UICONTROL Import Third Party Listings]** (obligatoire), sélectionnez une option :

   - `Import Listing` - (Par défaut) Choisissez quand vous souhaitez que les informations sur les produits de vos listes Amazon soient importées dans votre [!DNL Commerce] catalogue de produits. Cette option est la valeur par défaut et est recommandée.

   - `Do Not Import Listing` - Choisissez quand vous souhaitez manuellement [créer et attribuer de nouveaux produits](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) à votre [!DNL Commerce] catalogue pour vos listes Amazon.

   >[!NOTE]
   >Les champs d’options suivants ne sont actifs que lorsqu’ils sont définis sur `Import Listing`.

1. Pour **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, choisissez la variable [!DNL Commerce] qui correspond à la valeur du SKU du vendeur Amazon.

1. Pour **[!UICONTROL Attribute That Contains Amazon ASIN]**, choisissez la variable [!DNL Commerce] que vous avez créé et que vous associez à Amazon ASIN.

   >[!NOTE]
   >Si vous n’avez pas créé ces [!DNL Commerce] attributs de vos listes Amazon, voir [Création d’attributs pour la correspondance Amazon](./ob-creating-magento-attributes.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Listes tierces](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| Champ | Description |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | Obligatoire. Options :<ul><li>**[!UICONTROL Import Listing]** - (Par défaut) Choisissez quand vous souhaitez que les informations sur les produits de vos listes Amazon soient importées dans votre [!DNL Commerce] catalogue de produits. </li><li>**[!UICONTROL Do Not Import Listing]** - Choisissez quand vous souhaitez manuellement [créer et attribuer de nouveaux produits](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) à votre [!DNL Commerce] catalogue pour vos listes Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | actif uniquement lorsque la variable est définie sur `Import Listing`.<br>Choisissez la [!DNL Commerce] comme correspondance avec l’attribut Amazon pour le SKU du vendeur Amazon. Si cet attribut n’existe pas, voir [Création d’attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, passez en revue les [!DNL Commerce] [Attributs](./managing-attributes.md) et créer ou modifier un attribut pour qu’il corresponde à ces données Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | actif uniquement lorsque la variable est définie sur `Import Listing`.<br>Choisissez la [!DNL Commerce] qui correspond à l’attribut Amazon pour Amazon ASIN. Si cet attribut n’existe pas, voir [Création d’attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, passez en revue les [!DNL Commerce] [Attributs](./managing-attributes.md) et créer ou modifier un attribut pour qu’il corresponde à ces données Amazon. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
