---
title: AMAZON SALES CHANNEL - [!UICONTROL Stock/Quantity]
description: Pour contrôler la synchronisation des détails sur la quantité de produits de votre boutique Commerce avec votre [!DNL Amazon Seller Central] , mettez à jour les paramètres Stock/Quantité .
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]* font partie des paramètres de liste des magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord de la boutique](./amazon-store-dashboard.md).

Ces paramètres sont utilisés pour synchroniser les détails sur la quantité de produits de votre [!DNL Commerce] storefront vers la quantité de votre [!DNL Amazon Seller Central] compte . Cet outil est puissant et peut être utilisé pour de la publicité supplémentaire en affichant l’urgence pour l’acheteur tout en conservant l’organisation de votre inventaire. Par exemple, certains commerçants peuvent avoir 150 articles d’un SKU particulier en stock dans leur entrepôt et veulent s’assurer que les acheteurs Amazon peuvent acheter l’ensemble de leur inventaire. D’autres commerçants peuvent souhaiter ne répertorier qu’un seul élément à la fois pour créer un sentiment de pénurie pour l’utilisateur final. Dans ce cas, définissez *[!UICONTROL Maximum Listed Quantity]* to `1`.

La quantité est un attribut régional et est basée sur la variable **[!UICONTROL Amazon Marketplace Country]** définition pendant [intégration de magasin](./store-integration.md). Lorsqu’une modification est apportée à la quantité d’un produit, elle affecte toutes les listes Amazon qui partagent ce [!DNL Amazon Seller SKU] dans vos magasins Amazon qui vendent dans le même pays. Modification d’un partage [!DNL Amazon Seller SKU] aux États-Unis n’affecte pas les boutiques Amazon configurées pour un autre pays. Votre premier magasin Amazon intégré (avec la date de création la plus ancienne) contrôle la priorité dans les paramètres de quantité.

>[!NOTE]
>
>Pour les utilisateurs d’Adobe Commerce et de Magento Open Source 2.3.x, le canal de vente Amazon prend en charge l’utilisation de l’extension Inventory management sans configuration supplémentaire. Voir [Gestion du stock](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## Configuration des paramètres de stock/quantité {#configure-stock--quantity-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord de la boutique.

1. Développez l’objet **[!UICONTROL Stock / Quantity]** .

1. Pour **[!UICONTROL Out-of-Stock Threshold]** (obligatoire), saisissez une valeur numérique pour la plus petite quantité d’un produit afin de maintenir le produit éligible à sa liste Amazon.

   La valeur par défaut est `0`. Si votre [!DNL Commerce] le stock de produits est inférieur à ce nombre, la liste Amazon correspondante n’est pas éligible aux ventes via Amazon.

1. Pour **[!UICONTROL Maximum Listed Quantity]** (obligatoire), saisissez une valeur numérique pour la quantité que vous souhaitez afficher dans votre liste Amazon.

   Ce paramètre répertorie toutes vos listes Amazon éligibles à la valeur saisie. Lorsqu’un article est vendu, la quantité répertoriée dans Amazon ne change pas. La quantité répertoriée disponible utilise toujours cette valeur, même si la quantité réelle du produit est supérieure ou inférieure. Ce paramètre est généralement utilisé lorsque vous ne gérez pas l’inventaire des produits. Par exemple, vous pouvez avoir un produit dont la quantité est de 80 dans votre [!DNL Commerce] catalogue. Avec défini sur `10`, la liste Amazon affiche toujours une quantité disponible de `10` et ne change pas lorsque la vente est faite pour le produit.

1. Pour **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatoire), saisissez une valeur de quantité à afficher pour vos listes Amazon.

   Amazon exige que vous publiiez une quantité disponible. Pour [!DNL Commerce] produits pour lesquels vous ne pouvez pas gérer de stock mais que vous souhaitez les répertorier sur Amazon, la liste est publiée avec la quantité disponible saisie ici.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Paramètres de stock/quantité](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| Champ | Description |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | Saisissez une valeur numérique pour la plus petite quantité d’un produit afin de maintenir le produit éligible à sa liste Amazon (la valeur par défaut est `0`).<br><br>Si votre [!DNL Commerce] le stock de produits est inférieur à ce nombre, la liste Amazon correspondante n’est pas éligible aux ventes via Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Saisissez une valeur numérique pour la quantité que vous souhaitez afficher dans votre liste Amazon.<br><br>Lorsqu’un article est vendu, la liste Amazon est republiée avec la quantité saisie ici. Ce paramètre est généralement utilisé lorsque vous ne gérez pas l’inventaire des produits.<br><br>Par exemple, vous saisissez la valeur Quantité maximale répertoriée comme `10`. La quantité réelle d’un produit est `80`. Parce que vous avez défini cette valeur sur `10`, la liste Amazon affiche toujours une quantité disponible de `10`. La quantité disponible est toujours affichée avec la valeur définie, même lorsque la quantité de votre stock est inférieure. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Saisissez une valeur pour votre quantité d’affichage pour vos listes Amazon.<br><br>Amazon exige que vous publiiez une quantité disponible. Pour [!DNL Commerce] produits pour lesquels vous ne souhaitez pas gérer de stock mais que vous souhaitez les répertorier sur Amazon, la liste est publiée avec la quantité disponible de la valeur saisie ici. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Exemple : quantité maximale en liste

Lorsqu’un article est vendu, la liste Amazon le reprend à cette quantité.

Par exemple, si vous définissez *[!UICONTROL Maximum Listed Quantity]* as `12`, la liste Amazon affiche une quantité de 12 même si le produit a une [!DNL Commerce] quantité de 80 :

![Exemple de quantité maximale répertoriée 1](assets/amazon-max-listed-quantity.png){width="300"}

Si vous définissez *[!UICONTROL Maximum Listed Quantity]* as `1`, tous les produits éligibles sont répertoriés avec une quantité `1`. Lorsqu’un article est vendu, le système s’intéresse à votre [!DNL Commerce] produit et, s’il existe un stock supplémentaire, recense l’article sur Amazon avec une quantité `1`.

Cette option peut s’avérer utile pour les produits qui sont généralement commandés à une quantité de 1. Cela augmente également l’urgence pour l’acheteur lors de l’affichage de votre liste Amazon.

![Exemple de quantité maximale répertoriée 2](assets/amazon-max-listed-quantity-1.png){width="300"}
