---
title: Tâches courantes de traitement des commandes Amazon
description: Utilisez la variable [!DNL Commerce] commandes créées pour les commandes Amazon afin de gérer l’activité et le traitement des commandes dans la variable [!UICONTROL Commerce] Administrateur.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 6d221c2c2e9a37a42e9d660aceb3c525fedc511d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Tâches courantes de traitement des commandes Amazon

[Traitement des commandes commerciales](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) Vous pouvez gérer vos commandes Amazon, notamment envoyer un courrier électronique à l’acheteur, honorer la commande (livraison), émettre des crédits/remboursements, ajouter des commentaires, etc. Pour gérer vos commandes Amazon, votre [**Importation de commandes Amazon**](./order-settings.md) doit être défini sur `Enabled` afin que la variable [!DNL Commerce] les commandes sont créées à la réception des commandes Amazon. Les informations de commande Amazon s’affichent dans la variable *[!UICONTROL Recent Orders]* du tableau de bord de la boutique.

Lorsqu’elle est activée, la valeur correspondante [!DNL Commerce] les commandes sont créées pour les commandes Amazon et le numéro de commande Amazon s’affiche dans la variable _[!UICONTROL Order Number]_colonne . Si une valeur [!DNL Commerce] Une commande est créée, cliquez sur le numéro de la commande pour ouvrir la commande dans le [Traitement des commandes commerciales](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) page. Vous pouvez gérer l’ordre comme vous le faites pour les autres [[!DNL Commerce] traitement des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

Le [!DNL Commerce] Le numéro de commande ne s’affiche pas avec la variable _[!UICONTROL Recent Orders]_informations. Le numéro de commande Commerce ne s’affiche que lorsque vous cliquez sur le numéro de commande dans le tableau de bord du magasin et que vous ouvrez la commande dans [Traitement des commandes commerciales](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Lors de l’affichage de la variable [!DNL Commerce] , le numéro de commande Amazon apparaît dans la variable *[!UICONTROL Payment & Shipping Method]*. Elle comprend également des options permettant de *[!UICONTROL View or Cancel Amazon Order]*et *[!UICONTROL View all Amazon Orders]*, selon l’état d’expédition de la commande.

Voir [annuler une commande non expédiée ;](./cancel-unshipped-order.md).

![Informations sur les commandes Amazon dans l’ordre de commerce](assets/amazon-order-number-payment-info.png){width="500"}

Lors du traitement d’une commande Amazon, le canal de vente Amazon met à jour et synchronise les informations de commande avec votre [!DNL Amazon Seller Central] compte . Vos paramètres cron déterminent la fréquence de synchronisation des informations de commande entre Amazon et le canal de vente Amazon.

Commerce commun [traitement des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) les tâches sont les suivantes :

- [Actions de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Recherche de commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Traitement d’une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Afficher une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Traitement d’une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Informations sur la commande et le compte](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Informations sur l’adresse](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Mode de paiement et de livraison](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Vérifier les éléments triés](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Emettre un crédit/remboursement](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Exécution/envoi d’une commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Créer une facture](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Annuler une commande non expédiée](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si une commande est dans `Unshipped` status, vous pouvez [annuler une commande Amazon ;](./cancel-unshipped-order.md) sur le [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) page. Si une commande a été expédiée, elle ne peut pas être annulée.

Voir [Gestion des commandes commerciales](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
