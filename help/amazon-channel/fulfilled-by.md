---
title: Exécuté par
description: Utilisez les paramètres d’exécution de pour déterminer comment les commandes des listes Amazon sont exécutées (expédiées).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 618
ht-degree: 0%

---

# Exécuté par

_[!UICONTROL Fulfilled By]_font partie des paramètres de liste des magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord du magasin](./amazon-store-dashboard.md).

Ces paramètres définissent la partie qui remplit (ou expédie) les commandes. Si toutes vos commandes sont exécutées à l’aide d’une seule méthode, faites votre choix entre le marchand (vous) ou Amazon. Si vous prévoyez de répondre aux commandes de vos emplacements et d’utiliser Amazon, il est recommandé d’utiliser la troisième option et de configurer un attribut de produit [!DNL Commerce].

- **[!UICONTROL Fulfilled by Merchant]** - Choisissez si vous, le commerçant, effectuez toutes les commandes. Lorsqu’une commande est passée, le stock est déduit de votre catalogue [!DNL Commerce].

- **[!UICONTROL Fulfilled by Amazon]** - Choisissez si Amazon répond à toutes les commandes. Avec cette option, l’inventaire des produits n’est pas déduit de votre catalogue [!DNL Commerce] lorsqu’une commande est passée. Le stock des commandes réalisées par Amazon est stocké et déduit de leurs entrepôts. Avant d’attribuer cette option, vous devez vérifier dans votre compte [!DNL Amazon Seller Central] que vos produits sont éligibles pour l’exécution _remplie par Amazon_ (FBA). L’inventaire FBA est directement géré via votre compte [!DNL Amazon Seller Central]. Avec cette méthode d’exécution, le canal de vente Amazon ne partage pas les mises à jour de quantité entre [!DNL Commerce] et Amazon. Par conséquent, tous les outils marketing décrits dans la section Paramètres de quantité ne sont pas disponibles pour vous dans le canal de vente Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si vos produits peuvent être satisfaits par vous et Amazon, vous pouvez créer un attribut de  [!DNL Commerce] produit avec des valeurs pour les champs Renseigné par le commerçant et Renseigné par Amazon. La définition de cette valeur par produit indique qui remplit les commandes.

La méthode d’exécution est un attribut régional et basée sur le paramètre **[!UICONTROL Amazon Marketplace Country]** défini lors de l’[intégration de magasin](./store-integration.md). Lorsqu’une modification est apportée, la modification affecte toutes les listes Amazon qui partagent cette valeur [!DNL Amazon Seller SKU] dans vos magasins Amazon vendus dans la même région (comme défini dans _[!UICONTROL Amazon Marketplace Country]_lors de l’[intégration du magasin](./store-integration.md)). Une modification apportée à une [!DNL Amazon Seller SKU] partagée aux États-Unis n’a aucune incidence sur les magasins Amazon définis pour une autre région (comme défini lors de l’intégration du magasin).

>[!NOTE]
>
>Lorsqu’une commande est satisfaite par Amazon (FBA) et que la commande est importée, vous pouvez voir des données factices pour certains champs dans les détails de la commande. Voir [Détails de la commande Amazon](./amazon-order-details.md).

## Configuration des paramètres [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord du magasin.

1. Développez la section _[!UICONTROL Fulfilled By]_.

1. Pour **[!UICONTROL Product Fulfilled By]**, choisissez qui remplit (expédie) la commande :

   - `Fulfilled by Merchant` - Le marchand remplit l&#39;ordre.

   - `Fulfilled by Amazon` - L’entrepôt Amazon remplit l’ordre.

   - `Assign Fulfilled By Using Magento Product Attribute` - Un  [!DNL Commerce] attribut indique qui remplit la commande par produit.

      Si cette option est sélectionnée, choisissez l’attribut [!DNL Commerce] que vous souhaitez mapper dans **[!UICONTROL Fulfilled by Attribute]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Paramètres remplis par](assets/amazon-fulfilled-by.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Options :<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Choisissez si vous remplissez les commandes. Lorsqu’une commande est passée, le stock est déduit de votre catalogue [!DNL Commerce]. Lors de la création d’un produit, la méthode d’exécution de Merchant Fulfill est affectée.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Choisissez si Amazon remplit les commandes. Avec cette méthode d’exécution, l’inventaire des produits n’est pas déduit de votre catalogue [!DNL Commerce] lorsqu’une commande est passée. Lorsqu’un produit est créé, il est créé avec _[!UICONTROL Fulfilled by Amazon (FBA)]_comme type d’exécution. Assurez-vous que vos produits sont éligibles à l’exécution FBA dans votre compte [!DNL Amazon Seller Central]. L’inventaire FBA est également directement géré via votre compte [!DNL Amazon Seller Central]. Avec cette méthode d’exécution, les mises à jour de quantité ne sont pas publiées par rapport à votre catalogue [!DNL Commerce]. Vous ne pouvez donc pas utiliser certains des outils marketing décrits dans [Paramètres stock/quantité](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Choisissez si vous disposez d’un  [!DNL Commerce] attribut qui détermine s’il est rempli par le marchand ou rempli par Amazon. Une fois sélectionné, **[!UICONTROL Fulfilled by Attribute]** l’active.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Sélectionnez l’attribut [!DNL Commerce] utilisé pour déterminer la méthode d’exécution.<br><br>Par exemple, si l’attribut est  _Fulfill_ Byte (Octets remplis) et que vous choisissez la valeur d’attribut  _[!UICONTROL Fulfilled By Merchant]_ou_[!UICONTROL Fulfilled By Amazon (FBA)]_, le système utilise cette valeur comme type d’exécution pour un nouveau produit. En tant que commerçant, vous devez vous assurer que vos produits sont éligibles à l’exécution FBA dans votre compte [!DNL Amazon Seller Central]. L’inventaire FBA est également directement géré via votre compte de vendeur Amazon.<br><br>Les options dépendent des attributs que vous configurez pour vos produits Amazon. |

**Accès rapide**  -  [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
