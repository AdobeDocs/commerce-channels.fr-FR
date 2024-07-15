---
title: Gestion des commandes Amazon
description: Vous pouvez activer l’importation des commandes dans vos paramètres de commande afin de gérer plus facilement vos commandes Amazon depuis votre administrateur Commerce.
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Gestion des commandes Amazon

Vous pouvez afficher vos informations de commande Amazon, telles qu’elles ont été reçues d’Amazon, dans la section _[!UICONTROL Recent Orders]_du [tableau de bord du magasin](./amazon-store-dashboard.md) ou sur la page_[!UICONTROL Amazon orders]_ (également appelée vue _[!UICONTROL All Orders]_).

La gestion des commandes Amazon dépend de l’activation ou de la désactivation de l’importation de commandes dans vos [Paramètres de commande](./order-settings.md#configure-order-settings).

## Lorsque l’importation de commande est activée

Après [l&#39;intégration de magasin](./store-integration.md), le paramètre [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) est `Enabled` par défaut. Avec ce paramètre, les [!DNL Commerce] commandes correspondantes sont créées pour vos commandes Amazon et peuvent être gérées dans le workflow [[!DNL Commerce] Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Quels que soient les paramètres d&#39;import de commande, les commandes Amazon qui existaient dans votre compte [!DNL Amazon Seller Central] avant votre [intégration de magasin](./store-integration.md) ne sont pas importées.

Les commandes Amazon importées sont gérées dans le workflow [[!DNL Commerce] Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), comme vos autres [!DNL Commerce] magasins. Cliquez sur le numéro de commande Amazon dans la colonne *[!UICONTROL Order Number]* pour ouvrir la commande dans le [[!DNL Commerce] processus de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Voir [Affichage des commandes Amazon](./amazon-orders-all.md).

### Processus d’import de commande

Lorsqu’une commande est passée sur Amazon et que l’ [import de commande](./order-settings.md) est activé, le processus suivant commence.

| Modifier | Actions |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Une commande est passée sur Amazon. | <ul><li>Amazon définit l’état de la commande sur `Pending`.</li><li>Les informations sur la commande sont envoyées à [!DNL Commerce].</li><li>La commande est ajoutée à la [_table des commandes Amazon_](./amazon-orders-all.md) avec le statut `Pending`.</li></ul> |
| Amazon définit l’état de la commande sur `Unshipped`. | <ul><li>Le changement d’état est envoyé à [!DNL Commerce].</li><li>Dans la table [_Commandes Amazon_ ](./amazon-orders-all.md), l’état de la commande passe à `Unshipped`.</li><li>Dans le [[!DNL Commerce] workflow des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), une commande [!DNL Commerce] correspondante est créée avec le statut `Processing`.</li></ul> |
| Dans le [[!DNL Commerce] workflow des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), la commande [!DNL Commerce] est traitée et l&#39;état passe à `Shipped`. | <ul><li>Dans la table [_Commandes Amazon_ ](./amazon-orders-all.md), l’état de la commande passe à `Shipped`.</li><li>Sur la tâche cron suivante, l’état de la commande passe à `Complete` dans le [[!DNL Commerce] workflow des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Blocage de création de commande

Il existe quelques scénarios qui empêchent la création de l’ordre [!DNL Commerce] correspondant. [!DNL Commerce] Les commandes ne sont pas créées pour les commandes reçues en cas de l’un des problèmes suivants.

| Scénario | Solution |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L’élément n’existe pas dans le catalogue [!DNL Commerce]. | [Créez le produit](./creating-assigning-catalog-products.md) dans votre catalogue [!DNL Commerce] et [ faites-le correspondre manuellement ](./creating-assigning-catalog-products.md) au produit. |
| L’élément du catalogue est désactivé. | Assurez-vous que le [statut du produit](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) est activé. |
| L’article commandé est en rupture de stock. | Mettez à jour ou configurez les [options de produit](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) pour la quantité et la source. |

Lorsque les commandes ne peuvent pas être importées, un message système similaire au suivant s’affiche en haut de l’écran :

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Lorsque le problème est résolu, l’ordre [!DNL Commerce] est créé lors de la synchronisation suivante.

## Lorsque l’importation de commande est désactivée

Si vous ne souhaitez pas importer et gérer vos commandes Amazon dans [!DNL Commerce], vous pouvez modifier le paramètre [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) en `Disabled`. Ce paramètre signifie que lorsque de nouvelles commandes sont reçues d’Amazon, les [!DNL Commerce] commandes correspondantes ne sont pas créées.

Lorsque cette option est désactivée, les informations de commande reçues d’Amazon apparaissent dans la section _[!UICONTROL Recent Orders]_du tableau de bord du magasin et dans la vue_[!UICONTROL All Orders]_. Ces informations de commande sont en lecture seule et vous devez gérer ces commandes dans [!DNL Amazon Seller Central]. Pour ouvrir les détails de la commande dans [!DNL Amazon Seller Central], cliquez sur le numéro de commande Amazon dans la colonne _[!UICONTROL Order Number]_.

Voir aussi [Afficher les commandes Amazon](./amazon-orders-all.md), [Afficher les détails des commandes Amazon](./amazon-order-details.md) et [Tâches de traitement des commandes courantes](./common-order-processing.md).
