---
title: Gestion des commandes Amazon
description: Vous pouvez activer l’importation des commandes dans vos Paramètres de commande afin de gérer plus facilement vos commandes Amazon depuis votre administrateur Commerce.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Gestion des commandes Amazon

Vous pouvez afficher les informations de commande Amazon, telles qu’elles sont reçues d’Amazon, dans la variable _[!UICONTROL Recent Orders]_de la section [tableau de bord de la boutique](./amazon-store-dashboard.md) ou sur le_[!UICONTROL Amazon orders]_ (également appelée _[!UICONTROL All Orders]_).

La manière dont vous gérez vos commandes Amazon dépend de l’activation ou de la désactivation de l’importation des commandes dans votre [Paramètres de commande](./order-settings.md#configure-order-settings).

## Lorsque l’importation de commande est activée

Après [intégration de magasin](./store-integration.md), la variable [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) paramètre `Enabled` par défaut. Avec ce paramètre, [!DNL Commerce] Les commandes sont créées pour vos commandes Amazon et peuvent être gérées dans la variable [[!DNL Commerce] Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) workflow.

>[!NOTE]
>
>Quels que soient les paramètres d’importation des commandes, les commandes Amazon qui existaient dans votre [!DNL Amazon Seller Central] avant votre [intégration de magasin](./store-integration.md) ne sont pas importées.

Les commandes Amazon importées sont gérées dans la variable [[!DNL Commerce] Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) workflow, comme votre autre [!DNL Commerce] magasins. Cliquez sur le numéro de commande Amazon dans la *[!UICONTROL Order Number]* pour ouvrir l’ordre dans la colonne [[!DNL Commerce] processus de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Voir [Afficher les commandes Amazon](./amazon-orders-all.md).

### Processus d’import de commande

Lorsqu’une commande est passée sur Amazon et [import de commande](./order-settings.md) est activé, le processus suivant commence.

| Modifier | Actions |
|---|---|
| Une commande est passée sur Amazon. | <ul><li>Amazon définit l’état de la commande sur `Pending`.</li><li>Les informations sur la commande sont envoyées à [!DNL Commerce].</li><li>La commande est ajoutée à [_Commandes Amazon_ table](./amazon-orders-all.md) avec un `Pending` statut.</li></ul> |
| Amazon définit l’état de la commande sur `Unshipped`. | <ul><li>Le changement d’état est envoyé à [!DNL Commerce].</li><li>Dans le [_Commandes Amazon_ table](./amazon-orders-all.md), l’état de la commande passe à `Unshipped`.</li><li>Dans le [[!DNL Commerce] workflow commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), un [!DNL Commerce] une commande est créée avec une `Processing` statut.</li></ul> |
| Dans [[!DNL Commerce] workflow commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), la variable [!DNL Commerce] la commande est traitée et l’état devient `Shipped`. | <ul><li>Dans le [_Commandes Amazon_ table](./amazon-orders-all.md), l’état de la commande passe à `Shipped`.</li><li>Lors de la tâche cron suivante, l’état de la commande passe à `Complete` dans le [[!DNL Commerce] workflow commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Blocage de création de commande

Il existe quelques scénarios qui empêchent la création de la variable [!DNL Commerce] commande. [!DNL Commerce] les commandes ne sont pas créées pour les commandes reçues en cas de l’un des problèmes suivants.

| Scénario | Solution |
|---|---|
| L’élément n’existe pas dans la variable [!DNL Commerce] catalogue. | [Création du produit](./creating-assigning-catalog-products.md) dans votre [!DNL Commerce] catalogue et [correspondance manuelle](./creating-assigning-catalog-products.md) au produit. |
| L’élément du catalogue est désactivé. | Assurez-vous que la variable [statut du produit](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) est activée. |
| L’article commandé est en rupture de stock. | Mettez à jour ou configurez le [options de produit](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) pour la quantité et la source. |

Lorsque les commandes ne peuvent pas être importées, un message système similaire au suivant s’affiche en haut de l’écran :

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Lorsque le problème est résolu, la variable [!DNL Commerce] La commande est créée lors de la synchronisation suivante.

## Lorsque l’importation de commande est désactivée

Si vous ne souhaitez pas importer et gérer vos commandes Amazon dans [!DNL Commerce], vous pouvez modifier la variable [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) paramètre sur `Disabled`. Ce paramètre signifie que lorsque de nouvelles commandes sont reçues d’Amazon, la variable [!DNL Commerce] les commandes ne sont pas créées.

Lorsque cette option est désactivée, les informations de commande reçues d’Amazon apparaissent dans la variable _[!UICONTROL Recent Orders]_du tableau de bord du magasin et dans la variable_[!UICONTROL All Orders]_ vue. Ces informations de commande sont en lecture seule et vous devez gérer ces commandes dans [!DNL Amazon Seller Central]. Pour ouvrir les détails de la commande dans [!DNL Amazon Seller Central], cliquez sur le numéro de commande Amazon dans la variable _[!UICONTROL Order Number]_colonne .

Voir aussi [Afficher les commandes Amazon](./amazon-orders-all.md), [Afficher les détails de la commande Amazon](./amazon-order-details.md), et [Tâches de traitement des commandes courantes](./common-order-processing.md).
