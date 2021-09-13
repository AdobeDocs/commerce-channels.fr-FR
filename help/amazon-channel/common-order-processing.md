---
title: Tâches de traitement des commandes courantes
description: Utilisez le  [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Admin correspondant.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Tâches de traitement de l’ordre commun

[[!DNL Commerce] Le traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} peut gérer vos commandes Amazon, notamment envoyer un courrier électronique à l’acheteur, respecter la commande (livraison), émettre des crédits/remboursements, ajouter des commentaires, etc. Pour gérer vos commandes Amazon, votre paramètre [**Importer des commandes Amazon**](./order-settings.md) doit être défini sur `Enabled` afin que les commandes [!DNL Commerce] correspondantes soient créées à la réception des commandes Amazon. Les informations de commande Amazon s’affichent dans la section *[!UICONTROL Recent Orders]* du tableau de bord du magasin.

Lorsque cette option est activée, les commandes [!DNL Commerce] correspondantes sont créées pour les commandes Amazon et le numéro de commande Amazon s’affiche dans la colonne _[!UICONTROL Order Number]_. Si une commande [!DNL Commerce] correspondante est créée, cliquez sur le numéro de commande pour ouvrir la commande dans la page [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Vous pouvez gérer l’ordre comme vous le faites pour votre autre [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

Le [!DNL Commerce] numéro de commande ne s’affiche pas avec les informations _[!UICONTROL Recent Orders]_. Le [!DNL Commerce] numéro de commande s’affiche uniquement lorsque vous cliquez sur le numéro de commande dans le tableau de bord du magasin et que vous ouvrez la commande dans [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Lors de l’affichage de la commande [!DNL Commerce], le numéro de la commande Amazon apparaît dans la section *[!UICONTROL Payment & Shipping Method]*. Il comprend également des options pour *[!UICONTROL View or Cancel Amazon Order]*et *[!UICONTROL View all Amazon Orders]*, selon l’état d’expédition de la commande.

Voir [annuler une commande non expédiée](./cancel-unshipped-order.md).

![Informations sur les commandes Amazon dans l’ordre de commerce](assets/amazon-order-number-payment-info.png)

Lors du traitement d’une commande Amazon, le canal de vente Amazon met à jour et synchronise les informations de commande avec votre compte [!DNL Amazon Seller Central]. Vos paramètres cron déterminent la fréquence de synchronisation des informations de commande entre Amazon et le canal de vente Amazon.

Les tâches courantes de [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} incluent :

- [Actions de commande](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Recherche de commande](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Traiter une commande](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Afficher une commande](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Traiter une commande](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Informations sur la commande et le compte](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Informations sur l’adresse](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Mode de paiement et de livraison](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Vérifier les éléments classés](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Émettre un crédit/remboursement](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Exécution/livraison d’une commande](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Créer une facture](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Annuler une commande non expédiée](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si une commande est à l’état `Unshipped` , vous pouvez [annuler une commande Amazon](./cancel-unshipped-order.md) sur la page [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Si une commande a été expédiée, elle ne peut pas être annulée.

Voir [Gestion des commandes de commerce](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
