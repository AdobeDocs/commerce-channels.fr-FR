---
title: Rempli par
description: Utilisez les paramètres Remplir par pour déterminer comment les commandes des annonces Amazon sont exécutées (expédiées).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Rempli par

_[!UICONTROL Fulfilled By]_font partie des paramètres de votre liste de magasins. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres définissent la partie qui remplit (ou expédie) les commandes. Si toutes vos commandes sont exécutées selon une seule méthode, choisissez entre commerçant (vous) ou Amazon. Si vous envisagez d’exécuter des commandes à partir de vos emplacements et d’utiliser Amazon, il est recommandé d’utiliser la troisième option et de configurer une [!DNL Commerce] Attribut de produit.

- **[!UICONTROL Fulfilled by Merchant]** - Choisissez si vous, le commerçant, remplissez toutes les commandes. Lorsqu&#39;une commande est passée, le stock est déduit de votre [!DNL Commerce] catalogue.

- **[!UICONTROL Fulfilled by Amazon]** - Indiquez si Amazon remplit toutes les commandes. Avec cette option, l’inventaire des produits n’est pas déduit de votre [!DNL Commerce] lorsqu’une commande est passée. Le stock de stocks pour les commandes exécutées par Amazon est stocké et déduit de leurs entrepôts. Avant d’affecter cette option, vous devez vérifier dans votre [!DNL Amazon Seller Central] compte pour lequel vos produits sont éligibles _Rempli Par Amazon_ (FBA) exécution. L’inventaire FBA est géré directement via votre [!DNL Amazon Seller Central] Compte. Avec cette méthode d&#39;exécution, le canal de vente Amazon ne partage pas les mises à jour de quantité entre [!DNL Commerce] et Amazon. Par conséquent, tous les outils marketing décrits dans les paramètres Quantité ne sont pas disponibles dans le canal de vente Amazon.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Si vos produits peuvent être réalisés par vous-même et Amazon, vous pouvez souhaiter créer un [!DNL Commerce] Attribut de produit avec des valeurs pour Fulfill By Merchant et Fulfill by Amazon. La définition de cette valeur par produit indique qui exécute les commandes.

La méthode d’exécution est un attribut régional et basée sur **[!UICONTROL Amazon Marketplace Country]** paramètre défini pendant [intégration de magasin](./store-integration.md). Lorsqu’une modification est apportée, la modification affecte toutes les annonces Amazon qui partagent ce [!DNL Amazon Seller SKU] dans vos magasins Amazon qui vendent dans la même région (comme défini dans _[!UICONTROL Amazon Marketplace Country]_pendant [intégration de magasin](./store-integration.md)). Modification d’un partage [!DNL Amazon Seller SKU] aux États-Unis n’affecte pas votre jeu de magasins Amazon pour une autre région (telle que définie lors de l’intégration du magasin).

>[!NOTE]
>
>Lorsqu’une commande est exécutée par Amazon (FBA) et que la commande est importée, vous pouvez voir des données fictives pour certains champs dans les détails de la commande. Voir [Détails de la commande Amazon](./amazon-order-details.md).

## Configurez la [!UICONTROL Fulfilled By] paramètres {#configure-fulfilled-by-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la _[!UICONTROL Fulfilled By]_.

1. Pour **[!UICONTROL Product Fulfilled By]**, choisissez qui remplit (expédie) la commande :

   - `Fulfilled by Merchant` - Le commerçant remplit l&#39;ordre.

   - `Fulfilled by Amazon` - L&#39;entrepôt Amazon remplit la commande.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] indique qui exécute la commande par produit.

      Si cette option est sélectionnée, sélectionnez l’option [!DNL Commerce] que vous souhaitez mapper dans **[!UICONTROL Fulfilled by Attribute]**.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Paramètres d’exécution par](assets/amazon-fulfilled-by.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Options :<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Indiquez si vous répondez aux commandes. Lorsqu&#39;une commande est passée, le stock est déduit de votre [!DNL Commerce] catalogue. Lorsqu&#39;un nouveau produit est créé, la méthode d&#39;exécution de Merchant Fulfill est affectée.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Indiquez si Amazon remplit les commandes. Avec cette méthode d’exécution, l’inventaire des produits n’est pas déduit de votre [!DNL Commerce] lorsqu’une commande est passée. Lorsqu’un produit est créé, il est créé avec _[!UICONTROL Fulfilled by Amazon (FBA)]_comme type d’exécution. Assurez-vous que vos produits sont éligibles à l’exécution FBA dans votre [!DNL Amazon Seller Central] compte. L’inventaire FBA est également géré directement via votre [!DNL Amazon Seller Central] compte. Avec cette méthode de remplissage, les mises à jour de quantité ne sont pas poussées par rapport à votre [!DNL Commerce] , de sorte que vous ne pouvez pas utiliser certains des outils marketing décrits dans [Paramètres Stock/Quantité](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Choisissez si vous disposez d’un [!DNL Commerce] qui détermine s’il est rempli par le commerçant ou rempli par Amazon. Lorsque cette option est sélectionnée, **[!UICONTROL Fulfilled by Attribute]** active.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Sélectionnez l’option [!DNL Commerce] utilisé pour déterminer la méthode d’exécution.<br><br>Par exemple, si l’attribut est _Rempli par_ et vous sélectionnez la valeur d’attribut comme _[!UICONTROL Fulfilled By Merchant]_ou_[!UICONTROL Fulfilled By Amazon (FBA)]_, le système utilise cette valeur comme type d’exécution pour un nouveau produit. En tant que commerçant, vous devez vous assurer que vos produits sont admissibles à l’exécution FBA au sein de votre [!DNL Amazon Seller Central] compte. Le stock FBA est également géré directement via votre compte de vendeur Amazon.<br><br>Les options dépendent des attributs que vous avez configurés pour vos produits Amazon. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
