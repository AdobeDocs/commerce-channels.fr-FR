---
title: Stock/Quantité
description: Pour contrôler la synchronisation des détails de quantité de produits de votre boutique de commerce vers votre [!DNL Amazon Seller Central] , mettez à jour les paramètres Stock/Quantité.
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Stock/Quantité

*[!UICONTROL Stock/Quantity]* font partie des paramètres de votre liste de magasins. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres sont utilisés pour synchroniser les détails de quantité du produit à partir de votre [!DNL Commerce] vitrine vers la quantité sur votre [!DNL Amazon Seller Central] compte. Cet outil est puissant et peut être utilisé pour la publicité supplémentaire en affichant l&#39;urgence à l&#39;acheteur tout en conservant votre inventaire organisé. Par exemple, certains commerçants peuvent avoir 150 articles d&#39;une UGS particulière en stock dans leur entrepôt et veulent s&#39;assurer que les acheteurs Amazon peuvent acheter tout leur stock. D&#39;autres commerçants peuvent souhaiter n&#39;énumérer qu&#39;un élément à la fois pour créer un sentiment de pénurie pour l&#39;utilisateur final. Dans ce cas, définissez l’option *[!UICONTROL Maximum Listed Quantity]* à `1`.

Quantité est un attribut régional et basé sur **[!UICONTROL Amazon Marketplace Country]** définir pendant [intégration de magasin](./store-integration.md). Lorsqu&#39;une modification est apportée à la quantité d&#39;un produit, elle affecte toutes les annonces Amazon qui partagent ce [!DNL Amazon Seller SKU] dans vos magasins Amazon qui vendent dans le même pays. Modification d’un partage [!DNL Amazon Seller SKU] aux États-Unis n&#39;affecte pas vos magasins Amazon installés pour un autre pays. Votre premier magasin Amazon intégré (avec la date de création la plus ancienne) contrôle la priorité dans les paramètres de quantité.

>[!NOTE]
>
>Pour les utilisateurs Adobe Commerce et Magento Open Source 2.3.x, le canal de vente Amazon prend en charge l&#39;utilisation de l&#39;extension Gestion des stocks sans configuration supplémentaire. Voir [Gestion des stocks](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target=&quot;_blank&quot;}.

## Configuration des paramètres stock/quantité {#configure-stock--quantity-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la **[!UICONTROL Stock / Quantity]** .

1. Pour **[!UICONTROL Out-of-Stock Threshold]** (obligatoire), entrez une valeur numérique pour la quantité la plus faible d&#39;un produit afin de maintenir le produit admissible à sa liste Amazon.

   La valeur par défaut est `0`. Si [!DNL Commerce] le stock de produits est inférieur à ce nombre, la liste Amazon correspondante n&#39;est pas éligible pour les ventes via Amazon.

1. Pour **[!UICONTROL Maximum Listed Quantity]** (obligatoire), entrez une valeur numérique pour la quantité que vous souhaitez afficher dans votre annonce Amazon.

   Ce paramètre répertorie toutes vos annonces Amazon éligibles à la valeur saisie. Lors de la vente d&#39;un article, la quantité de la mise en vente Amazon ne change pas. La quantité disponible pour la mise en vente utilise toujours cette valeur, même lorsque la quantité réelle du produit est supérieure ou inférieure. Ce paramètre est généralement utilisé lorsque vous ne gérez pas l’inventaire des produits. Par exemple, vous pouvez avoir un produit dont la quantité est de 80 dans votre [!DNL Commerce] catalogue. Avec défini sur `10`, la liste Amazon affiche toujours la quantité disponible de `10` et ne change pas lorsque la vente est faite pour le produit.

1. Pour **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatoire), entrez une valeur de quantité à afficher pour vos annonces Amazon.

   Amazon exige que vous publiiez une quantité disponible. Pour [!DNL Commerce] produits qui ne sont pas définis pour gérer les stocks mais que vous souhaitez répertorier sur Amazon, la liste est publiée avec la quantité disponible saisie ici.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Paramètres Stock/quantité](assets/amazon-stock-quantity.png)

| Champ | Description |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Entrez une valeur numérique pour la quantité la plus faible d’un produit afin de garder le produit éligible pour sa mise en vente Amazon (valeur par défaut : `0`).<br><br>Si [!DNL Commerce] le stock de produits est inférieur à ce nombre, la liste Amazon correspondante n&#39;est pas éligible pour les ventes via Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Entrez une valeur numérique pour la quantité que vous souhaitez afficher dans votre liste Amazon.<br><br>Lors de la vente d&#39;un objet, l&#39;annonce en Amazon est republiée avec la quantité saisie ici. Ce paramètre est généralement utilisé lorsque vous ne gérez pas l’inventaire des produits.<br><br>Par exemple, vous entrez la valeur Quantité maximale répertoriée comme `10`. Votre quantité réelle pour un produit est `80`. Parce que vous avez défini cette valeur sur `10`, la liste Amazon affiche toujours la quantité disponible de `10`. La quantité disponible est toujours affichée avec la valeur définie, même lorsque la quantité de votre stock est inférieure. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Saisissez une valeur pour la quantité affichée pour vos annonces Amazon.<br><br>Amazon exige que vous publiiez une quantité disponible. Pour [!DNL Commerce] produits qui ne sont pas définis pour gérer les stocks mais que vous souhaitez répertorier sur Amazon, la liste est publiée avec la quantité disponible de la valeur saisie ici. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Exemple : Quantité maximale répertoriée

Lorsqu&#39;un objet est vendu, l&#39;annonce Amazon le remet en vente à cette quantité.

Par exemple, si vous définissez *[!UICONTROL Maximum Listed Quantity]* comme `12`, la liste Amazon affiche une quantité de 12, même si le produit a une [!DNL Commerce] quantité de 80 :

![Quantité maximale répertoriée exemple 1](assets/amazon-max-listed-quantity.png)

Si vous définissez *[!UICONTROL Maximum Listed Quantity]* comme `1`, tous les produits éligibles sont répertoriés avec une quantité `1`. Lorsqu&#39;un objet est vendu, le système s&#39;en remet à votre [!DNL Commerce] produit et, s’il existe un stock supplémentaire, reliste l’article sur Amazon avec une quantité de `1`.

Cette option peut être utile pour les produits qui sont généralement commandés à une quantité de 1. Il augmente également l’urgence pour le commerçant lorsqu’il consulte votre annonce Amazon.

![Quantité maximale répertoriée exemple 2](assets/amazon-max-listed-quantity-1.png)
