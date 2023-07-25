---
title: Paramètres d’exécution de par pour les listes Amazon
description: Utilisez les paramètres d’exécution de pour déterminer comment les commandes des listes Amazon sont exécutées (expédiées).
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Paramètres d’exécution de par pour les listes Amazon

_[!UICONTROL Fulfilled By]_font partie des paramètres de liste des magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord de la boutique](./amazon-store-dashboard.md).

Ces paramètres définissent la partie qui remplit (ou expédie) les commandes. Si toutes vos commandes sont exécutées à l’aide d’une seule méthode, faites votre choix entre le marchand (vous) ou Amazon. Si vous prévoyez de respecter les commandes de vos emplacements et d’utiliser Amazon, il est recommandé d’utiliser la troisième option et de configurer une [!DNL Commerce] attribut de produit.

- **[!UICONTROL Fulfilled by Merchant]** - Choisissez si vous, le commerçant, effectuez toutes les commandes. Lorsqu’une commande est passée, le stock est déduit de votre [!DNL Commerce] catalogue.

- **[!UICONTROL Fulfilled by Amazon]** - Choisissez si Amazon répond à toutes les commandes. Avec cette option, l’inventaire des produits n’est pas déduit de votre [!DNL Commerce] catalogue lorsqu’une commande est passée. Le stock des commandes réalisées par Amazon est stocké et déduit de leurs entrepôts. Avant d’affecter cette option, vous devez vérifier dans votre [!DNL Amazon Seller Central] compte pour lequel vos produits sont éligibles _Renseigné Par Amazon_ Exécution (FBA). L’inventaire FBA est directement géré via votre [!DNL Amazon Seller Central] Compte. Avec cette méthode d’exécution, le canal de vente Amazon ne partage pas les mises à jour de quantité entre les [!DNL Commerce] et Amazon. Par conséquent, tous les outils marketing décrits dans la section Paramètres de quantité ne sont pas disponibles pour vous dans le canal de vente Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si vos produits peuvent être satisfaits par vous et Amazon, vous pouvez créer une [!DNL Commerce] Attribut de produit avec des valeurs pour les champs Renseigné par le commerçant et Renseigné par Amazon. La définition de cette valeur par produit indique qui remplit les commandes.

La méthode d’exécution est un attribut régional et basée sur la variable **[!UICONTROL Amazon Marketplace Country]** défini pendant [intégration de magasin](./store-integration.md). Lorsqu’une modification est apportée, la modification affecte toutes les listes Amazon qui partagent ce [!DNL Amazon Seller SKU] dans vos magasins Amazon qui vendent dans la même région (comme défini dans _[!UICONTROL Amazon Marketplace Country]_during [intégration de magasin](./store-integration.md)). Modification d’un partage [!DNL Amazon Seller SKU] aux États-Unis n’affecte pas les magasins Amazon définis pour une autre région (comme défini lors de l’intégration du magasin).

>[!NOTE]
>
>Lorsqu’une commande est satisfaite par Amazon (FBA) et que la commande est importée, vous pouvez voir des données factices pour certains champs dans les détails de la commande. Voir [Détails de la commande Amazon](./amazon-order-details.md).

## Configurez la variable [!UICONTROL Fulfilled By] paramètres {#configure-fulfilled-by-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord de la boutique.

1. Développez l’objet _[!UICONTROL Fulfilled By]_.

1. Pour **[!UICONTROL Product Fulfilled By]**, choisissez qui remplit (expédie) la commande :

   - `Fulfilled by Merchant` - Le marchand remplit l&#39;ordre.

   - `Fulfilled by Amazon` - L’entrepôt Amazon remplit l’ordre.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] indique qui remplit la commande par produit.

     Si vous le souhaitez, choisissez la variable [!DNL Commerce] que vous souhaitez mapper dans **[!UICONTROL Fulfilled by Attribute]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Paramètres remplis par](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| Champ | Description |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | Options :<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Choisissez si vous remplissez les commandes. Lorsqu’une commande est passée, le stock est déduit de votre [!DNL Commerce] catalogue. Lors de la création d’un produit, la méthode d’exécution de Merchant Fulfill est affectée.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Choisissez si Amazon remplit les commandes. Avec cette méthode d’exécution, l’inventaire des produits n’est pas déduit de votre [!DNL Commerce] catalogue lorsqu’une commande est passée. Lorsqu’un produit est créé, il est créé avec _[!UICONTROL Fulfilled by Amazon (FBA)]_comme type d’exécution. Assurez-vous que vos produits sont éligibles à l’exécution FBA dans votre [!DNL Amazon Seller Central] compte . L’inventaire FBA est également directement géré via votre [!DNL Amazon Seller Central] compte . Avec cette méthode d’exécution, les mises à jour de quantité ne sont pas rejetées par rapport à votre [!DNL Commerce] catalogue. Vous ne pouvez donc pas utiliser certains des outils marketing décrits à la section [Paramètres Stock/Quantité](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Choisissez si vous disposez d’une [!DNL Commerce] qui détermine s’il est rempli par le commerçant ou rempli par Amazon. Lorsqu’elle est choisie, **[!UICONTROL Fulfilled by Attribute]** active.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Choisissez la [!DNL Commerce] utilisé pour déterminer la méthode d’exécution.<br><br>Par exemple, si l’attribut est _Exécuté par_ et vous choisissez la valeur d’attribut comme `Fulfilled By Merchant` ou `Fulfilled By Amazon (FBA)`, le système utilise cette valeur comme type d’exécution pour un nouveau produit. En tant que marchand, vous devez vous assurer que vos produits sont éligibles à l’exécution FBA dans votre [!DNL Amazon Seller Central] compte . L’inventaire FBA est également directement géré via votre compte de vendeur Amazon.<br><br>Les options dépendent des attributs que vous configurez pour vos produits Amazon. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
