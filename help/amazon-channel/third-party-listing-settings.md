---
title: Sales Channel Amazon - [!UICONTROL Third-party Listings]
description: Mettez à jour les paramètres de liste tiers pour déterminer si votre catalogue Commerce importe des produits de vos listes Amazon Seller Central existantes.
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

Les paramètres de liste tiers font partie de vos paramètres de liste de magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord du magasin](./amazon-store-dashboard.md).

Ces paramètres déterminent si votre catalogue [!DNL Commerce] importe des produits de vos listes [!DNL Amazon Seller Central] existantes. Il est recommandé d’importer des listes à partir d’Amazon pour vous assurer que toutes les listes ont des produits [!DNL Commerce] correspondants. Lorsque vos listes font partie de votre catalogue [!DNL Commerce], vous pouvez gérer tous vos produits à partir d’un seul catalogue et utiliser les fonctionnalités du canal de vente Amazon. Ces fonctionnalités comprennent la gestion des commandes et de l’exécution avec Amazon, la retarification intelligente et la gestion des quantités.

Lorsqu’il est configuré pour importer vos listes Amazon, le canal de vente Amazon importe vos listes Amazon dans votre catalogue [!DNL Commerce], en essayant de les faire correspondre aux produits existants. Si une correspondance n’est pas trouvée automatiquement, vous pouvez importer la liste Amazon en tant que nouveau produit [!DNL Commerce] ou la faire correspondre manuellement à la liste.

Si vous choisissez d’importer vos listes Amazon, choisissez les attributs [!DNL Commerce] avec des valeurs pour le SKU du vendeur Amazon et Amazon ASIN. Si vous ne disposez pas des [!DNL Commerce] [attributs de produit](./ob-creating-magento-attributes.md), envisagez de les créer et de les affecter. Le mappage de ces attributs permet de faire correspondre correctement les listes Amazon importées à vos produits [!DNL Commerce].

L’importation initiale des listes démarre lorsque l’ [intégration de magasin](./store-integration.md) est terminée. Par la suite, et en fonction de vos paramètres cron, [!DNL Commerce] recherche continuellement les listes Amazon nouvellement ajoutées (non créées dans Amazon Sales Channel) et met à jour votre catalogue [!DNL Commerce] en fonction de vos paramètres de liste tiers.

## Configuration de paramètres de liste tiers

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord du magasin.

1. Développez la section _[!UICONTROL Third Party Listings]_.

1. Pour **[!UICONTROL Import Third Party Listings]** (obligatoire), choisissez une option :

   - `Import Listing` - (Par défaut) Choisissez quand vous souhaitez que les informations sur les produits de vos listes Amazon soient importées dans votre catalogue de produits [!DNL Commerce]. Cette option est la valeur par défaut et est recommandée.

   - `Do Not Import Listing` - Choisissez quand vous souhaitez [créer et attribuer manuellement de nouveaux produits](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) à votre catalogue [!DNL Commerce] pour vos listes Amazon.

   >[!NOTE]
   >Les champs d’options suivants ne sont actifs que lorsqu’ils sont définis sur `Import Listing`.

1. Pour **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, choisissez l’attribut [!DNL Commerce] correspondant à la valeur de SKU du vendeur Amazon.

1. Pour **[!UICONTROL Attribute That Contains Amazon ASIN]**, choisissez l’attribut [!DNL Commerce] que vous avez créé et faites correspondre cet attribut à Amazon ASIN.

   >[!NOTE]
   >Si vous n’avez pas créé ces attributs [!DNL Commerce] pour vos listes Amazon, reportez-vous à la section [Création d’attributs pour la correspondance Amazon](./ob-creating-magento-attributes.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Listes tierces](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| Champ | Description |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | Obligatoire. Options :<ul><li>**[!UICONTROL Import Listing]** - (Par défaut) Choisissez quand vous souhaitez que les informations sur les produits de vos listes Amazon soient importées dans votre catalogue de produits [!DNL Commerce]. </li><li>**[!UICONTROL Do Not Import Listing]** - Choisissez quand vous souhaitez [créer et attribuer manuellement de nouveaux produits](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) à votre catalogue [!DNL Commerce] pour vos listes Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Actif uniquement lorsque défini sur `Import Listing`.<br>Sélectionnez l’attribut [!DNL Commerce] comme correspondance avec l’attribut Amazon pour le SKU du vendeur Amazon. Si cet attribut n’existe pas, voir [Création d’attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, passez en revue vos [!DNL Commerce] [attributs](./managing-attributes.md) et créez ou modifiez un attribut pour qu’il corresponde à ces données Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Actif uniquement lorsque défini sur `Import Listing`.<br>Sélectionnez l’attribut [!DNL Commerce] correspondant à l’attribut Amazon pour Amazon ASIN. Si cet attribut n’existe pas, voir [Création d’attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, passez en revue vos [!DNL Commerce] [attributs](./managing-attributes.md) et créez ou modifiez un attribut pour qu’il corresponde à ces données Amazon. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
