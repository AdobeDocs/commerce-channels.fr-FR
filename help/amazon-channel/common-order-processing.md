---
title: Tâches courantes de traitement des commandes Amazon
description: Utilisez les  [!DNL Commerce] commandes créées pour les commandes Amazon afin de gérer l’activité et le traitement des commandes dans l’administrateur [!UICONTROL Commerce].
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Tâches courantes de traitement des commandes Amazon

[Le traitement des commandes Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) peut gérer vos commandes Amazon, notamment envoyer un courrier électronique à l’acheteur, honorer la commande (livraison), émettre des crédits/remboursements, ajouter des commentaires, etc. Pour gérer vos commandes Amazon, votre paramètre [**Importer des commandes Amazon**](./order-settings.md) doit être défini sur `Enabled` afin que les [!DNL Commerce] commandes correspondantes soient créées lors de la réception des commandes Amazon. Les informations de commande Amazon s’affichent dans la section *[!UICONTROL Recent Orders]* du tableau de bord du magasin.

Lorsque cette option est activée, les commandes [!DNL Commerce] correspondantes sont créées pour les commandes Amazon, et le numéro de commande Amazon s’affiche dans la colonne _[!UICONTROL Order Number]_. Si une commande [!DNL Commerce] correspondante est créée, cliquez sur le numéro de commande pour ouvrir la commande dans la page [Traitement des commandes Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Vous pouvez gérer la commande comme vous le faites pour votre autre [[!DNL Commerce] traitement des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

Le numéro de commande [!DNL Commerce] ne s’affiche pas avec les informations _[!UICONTROL Recent Orders]_. Le numéro de commande Commerce s’affiche uniquement lorsque vous cliquez sur le numéro de commande dans le tableau de bord du magasin et que vous ouvrez la commande dans le [traitement des commandes Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Lors de l’affichage de la commande [!DNL Commerce], le numéro de la commande Amazon apparaît dans la section *[!UICONTROL Payment & Shipping Method]*. Il comprend également des options pour *[!UICONTROL View or Cancel Amazon Order]*et *[!UICONTROL View all Amazon Orders]*, selon l’état d’expédition des commandes.

Voir [annuler une commande non expédiée](./cancel-unshipped-order.md).

![Informations sur la commande Amazon dans l’ordre Commerce](assets/amazon-order-number-payment-info.png){width="500"}

Lors du traitement d’une commande Amazon, le canal de vente Amazon met à jour et synchronise les informations de commande avec votre compte [!DNL Amazon Seller Central]. Vos paramètres cron déterminent la fréquence de synchronisation des informations de commande entre Amazon et le canal de vente Amazon.

Les tâches courantes de [traitement des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) de Commerce sont les suivantes :

- [Actions de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Recherche de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Traiter une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Afficher une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Traiter une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Informations sur la commande et le compte](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Informations sur l’adresse](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Mode de paiement et d’expédition](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Vérifier les éléments commandés](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Émettre un crédit/remboursement](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [ Exécution/envoi d’une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Créer une facture](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Annuler une commande non expédiée](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si une commande est à l’état `Unshipped`, vous pouvez [annuler une commande Amazon](./cancel-unshipped-order.md) sur la page [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Si une commande a été expédiée, elle ne peut pas être annulée.

Voir [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
