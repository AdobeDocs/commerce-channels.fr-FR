---
title: Gérer les commandes
description: Vous pouvez activer l’importation de commandes dans vos paramètres de commande pour gérer plus facilement vos commandes Amazon à partir de votre administrateur commercial.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 1d1b888db4de4f6e3658af768cd6f5cf30828788
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Gestion des commandes

Vous pouvez afficher vos informations de commande Amazon, telles qu’elles ont été reçues d’Amazon, dans le dossier _[!UICONTROL Recent Orders]_de la section [tableau de bord de magasin](./amazon-store-dashboard.md) ou sur la_[!UICONTROL Amazon orders]_ (également appelée _[!UICONTROL All Orders]_).

La façon dont vous gérez vos commandes Amazon dépend de l’activation ou de la désactivation de l’importation des commandes dans votre [Paramètres de commande](./order-settings.md#configure-order-settings).

## Lorsque l’importation de commande est activée

Après [intégration de magasin](./store-integration.md), le [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) paramètre `Enabled` par défaut. Avec ce paramètre, correspondant [!DNL Commerce] les commandes sont créées pour vos commandes Amazon et peuvent être gérées dans le [[!DNL Commerce] Commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}.

>[!NOTE]
>
>Quels que soient vos paramètres d’importation de commande, Amazon commandes qui existaient dans votre [!DNL Amazon Seller Central] avant [intégration de magasin](./store-integration.md) ne sont pas importés.

Les commandes Amazon importées sont gérées dans le noeud [[!DNL Commerce] Commandes](https://docs.magento.com/user-guide/sales/orders.html)Flux de travaux {target=&quot;_blank&quot;}, tout comme votre [!DNL Commerce] magasins. Cliquez sur le numéro de commande Amazon dans la zone *[!UICONTROL Order Number]* pour ouvrir l’ordre dans la [[!DNL Commerce] processus de commande](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Voir [Afficher les commandes Amazon](./amazon-orders-all.md).

### Traitement de l&#39;importation des commandes

Lorsqu&#39;une commande est passée sur Amazon et [importation de commande](./order-settings.md) est activé, le processus suivant commence.

| Modifier | Actions |
|---|---|
| Une commande est passée sur Amazon. | <ul><li>Amazon définit l’état de la commande sur `Pending`.</li><li>Les informations de commande sont envoyées à [!DNL Commerce].</li><li>La commande est ajoutée à [_Commandes Amazon_ table](./amazon-orders-all.md) avec un `Pending` statut.</li></ul> |
| Amazon modifie l’état de la commande en `Unshipped`. | <ul><li>La modification d’état est envoyée à [!DNL Commerce].</li><li>Dans la boîte de dialogue [_Commandes Amazon_ table](./amazon-orders-all.md), le statut de la commande devient `Unshipped`.</li><li>Dans la boîte de dialogue [[!DNL Commerce] workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, une [!DNL Commerce] commande créée avec un `Processing` statut.</li></ul> |
| Entrée [[!DNL Commerce] workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, le [!DNL Commerce] la commande est traitée et l’état change en `Shipped`. | <ul><li>Dans la boîte de dialogue [_Commandes Amazon_ table](./amazon-orders-all.md), le statut de la commande devient `Shipped`.</li><li>Sur la tâche cron suivante, l&#39;état de la commande devient `Complete` dans la [[!DNL Commerce] workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.</li></ul> |

### Bloqueurs de création de commandes

Il existe quelques scénarios qui empêchent la création de [!DNL Commerce] commande. [!DNL Commerce] les commandes ne sont pas créées pour les commandes reçues lorsque l&#39;un des problèmes suivants se produit.

| Scénario | Solution |
|---|---|
| L&#39;élément n&#39;existe pas dans le fichier [!DNL Commerce] catalogue. | [Création du produit](./creating-assigning-catalog-products.md) dans votre [!DNL Commerce] catalogue et [correspondance manuelle](./creating-assigning-catalog-products.md) c&#39;est au produit. |
| L’élément du catalogue est désactivé. | Assurez-vous que la [statut du produit](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} est activé. |
| L&#39;article commandé est en rupture de stock. | Mettez à jour ou configurez la [options de produit](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;} pour la quantité et la source. |

Lorsque des commandes ne peuvent pas être importées, un message système semblable à celui qui suit s’affiche en haut de l’écran :

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

Lorsque le problème est résolu, la [!DNL Commerce] l’ordre est créé lors de la synchronisation suivante.

## Lorsque l’importation de commande est désactivée

Si vous ne souhaitez pas importer et gérer vos commandes Amazon dans [!DNL Commerce], vous pouvez modifier la [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) paramètre sur `Disabled`. Ce paramètre signifie que, lorsque de nouvelles commandes sont reçues d’Amazon, le [!DNL Commerce] les commandes ne sont pas créées.

Lorsque cette option est désactivée, les informations de commande reçues d’Amazon s’affichent dans le noeud _[!UICONTROL Recent Orders]_dans le tableau de bord de la boutique et dans le dossier_[!UICONTROL All Orders]_ affichage. Ces informations de commande sont en lecture seule et vous devez gérer ces commandes dans [!DNL Amazon Seller Central]. Pour ouvrir les détails de la commande dans [!DNL Amazon Seller Central], cliquez sur le numéro de commande Amazon dans la zone _[!UICONTROL Order Number]_colonne.

Voir aussi [Afficher les commandes Amazon](./amazon-orders-all.md), [Afficher les détails des commandes Amazon](./amazon-order-details.md)et [Tâches de traitement des commandes courantes](./common-order-processing.md).
