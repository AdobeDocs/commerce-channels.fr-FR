---
title: Listes tierces
description: Mettez à jour les paramètres d’annonce tiers pour déterminer si votre catalogue Commerce importe des produits à partir de vos annonces Amazon Seller Central existantes.
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Listes tierces

Les paramètres d’annonce tiers font partie de vos paramètres d’annonce de boutique. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres déterminent si [!DNL Commerce] catalogue importe les produits de votre [!DNL Amazon Seller Central] annonces. Il est recommandé d’importer des annonces en provenance d’Amazon, afin de s’assurer que toutes les annonces correspondent [!DNL Commerce] produits. Lorsque vos annonces font partie de votre [!DNL Commerce] , vous pouvez gérer tous vos produits à partir d’un catalogue unique et utiliser les fonctionnalités du canal de vente Amazon. Ces fonctionnalités comprennent la gestion des commandes et de l’exécution avec Amazon, la retarification intelligente et la gestion des quantités.

Lorsqu’il est configuré pour importer vos annonces Amazon, le canal de vente Amazon importe vos annonces Amazon dans votre [!DNL Commerce] , en essayant de les faire correspondre à des produits existants. Si une correspondance n’est pas trouvée automatiquement, vous pouvez importer la liste Amazon en tant que nouvelle [!DNL Commerce] ou faire correspondre manuellement la liste à un produit.

Si vous choisissez d’importer vos annonces Amazon, sélectionnez l’option [!DNL Commerce] avec des valeurs pour les références SKU des vendeurs Amazon et Amazon ASIN. Si vous n&#39;avez pas [!DNL Commerce] [attributs de produit](./ob-creating-magento-attributes.md), envisagez de les créer et de les affecter. Le mappage de ces attributs permet de faire correspondre correctement les listes Amazon importées à vos [!DNL Commerce] produits.

L&#39;importation initiale de la liste démarre lorsque [intégration de magasin](./store-integration.md) est terminé. Après et en fonction de vos paramètres cron, [!DNL Commerce] vérifie en permanence les nouvelles annonces Amazon (non créées dans Sales Channel Amazon) et met à jour votre [!DNL Commerce] en fonction de vos paramètres d’annonce tiers.

## Configuration des paramètres d’annonce tiers

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la _[!UICONTROL Third Party Listings]_.

1. Pour **[!UICONTROL Import Third Party Listings]** (obligatoire), choisissez une option :

   - `Import Listing` - (Par défaut) Choisissez quand vous souhaitez importer dans votre [!DNL Commerce] catalogue de produits. Cette option est la valeur par défaut et est recommandée.

   - `Do Not Import Listing` - Choisissez quand vous souhaitez effectuer manuellement [création et attribution de nouveaux produits](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} vers votre [!DNL Commerce] pour vos annonces Amazon.
   >[!NOTE]
   >Les champs d’options suivants ne sont actifs que lorsque définis sur `Import Listing`.

1. Pour **[!UICONTROL Attribute That Contains Amazon Seller SKU]**, sélectionnez l’option [!DNL Commerce] qui correspond à la valeur SKU du vendeur Amazon.

1. Pour **[!UICONTROL Attribute That Contains Amazon ASIN]**, sélectionnez l’option [!DNL Commerce] que vous avez créé et que vous associez à l’Amazon ASIN.

   >[!NOTE]
   >Si vous ne les avez pas créés [!DNL Commerce] attributs pour vos annonces Amazon, voir [Création d&#39;attributs pour les correspondances Amazon](./ob-creating-magento-attributes.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Listes de tiers](assets/amazon-third-party-listings.png)

| Champ | Description |
|---|---|
| [!UICONTROL Import Third Party Listings] | Obligatoire. Options :<ul><li>**[!UICONTROL Import Listing]** - (Par défaut) Choisissez quand vous souhaitez importer dans votre [!DNL Commerce] catalogue de produits. </li><li>**[!UICONTROL Do Not Import Listing]** - Choisissez quand vous souhaitez effectuer manuellement [création et attribution de nouveaux produits](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} vers votre [!DNL Commerce] pour vos annonces Amazon.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Uniquement actif lorsque la valeur est définie sur `Import Listing`.<br>Sélectionnez l’option [!DNL Commerce] comme correspondance à l’attribut Amazon pour la référence SKU du vendeur Amazon. Si cet attribut n’existe pas, consultez [Création d&#39;attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, consultez votre [!DNL Commerce] [attributs](./managing-attributes.md) et créer ou modifier un attribut correspondant à ces données Amazon. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Uniquement actif lorsque la valeur est définie sur `Import Listing`.<br>Sélectionnez l’option [!DNL Commerce] qui correspond à l’attribut Amazon pour l’ASIN Amazon. Si cet attribut n’existe pas, consultez [Création d&#39;attributs de produit Amazon pour la correspondance Amazon](./ob-creating-magento-attributes.md). Si nécessaire, consultez votre [!DNL Commerce] [attributs](./managing-attributes.md) et créer ou modifier un attribut correspondant à ces données Amazon. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
