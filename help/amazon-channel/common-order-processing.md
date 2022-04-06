---
title: Tâches de traitement des commandes courantes
description: Utilisez la variable [!DNL Commerce] commandes créées pour les commandes Amazon afin de gérer l’activité et le traitement des commandes dans la variable [!UICONTROL Commerce] Administrateur.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Tâches de traitement de l’ordre commun

[[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} peut gérer vos commandes Amazon, notamment envoyer un courrier électronique à l’acheteur, honorer la commande (livraison), émettre des crédits/remboursements, ajouter des commentaires, etc. Pour gérer vos commandes Amazon, votre [**Importation de commandes Amazon**](./order-settings.md) doit être défini sur `Enabled` afin que la variable [!DNL Commerce] les commandes sont créées à la réception des commandes Amazon. Les informations de commande Amazon s’affichent dans la variable *[!UICONTROL Recent Orders]* du tableau de bord de la boutique.

Lorsqu’elle est activée, la valeur correspondante [!DNL Commerce] les commandes sont créées pour les commandes Amazon et le numéro de commande Amazon s’affiche dans la variable _[!UICONTROL Order Number]_colonne . Si une valeur [!DNL Commerce] Une commande est créée, cliquez sur le numéro de la commande pour ouvrir la commande dans le [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html)Page {target=&quot;_blank&quot;}. Vous pouvez gérer l’ordre comme vous le faites pour les autres [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

Le [!DNL Commerce] Le numéro de commande ne s’affiche pas avec la variable _[!UICONTROL Recent Orders]_informations. Le [!DNL Commerce] Le numéro de commande s’affiche uniquement lorsque vous cliquez sur le numéro de commande dans le tableau de bord du magasin et que vous ouvrez la commande dans [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Lors de l’affichage de la variable [!DNL Commerce] , le numéro de commande Amazon apparaît dans la variable *[!UICONTROL Payment & Shipping Method]*. Elle comprend également des options permettant de *[!UICONTROL View or Cancel Amazon Order]*et *[!UICONTROL View all Amazon Orders]*, selon l’état d’expédition de la commande.

Voir [annuler une commande non expédiée ;](./cancel-unshipped-order.md).

![Informations sur les commandes Amazon dans l’ordre de commerce](assets/amazon-order-number-payment-info.png)

Lors du traitement d’une commande Amazon, le canal de vente Amazon met à jour et synchronise les informations de commande avec votre [!DNL Amazon Seller Central] compte . Vos paramètres cron déterminent la fréquence de synchronisation des informations de commande entre Amazon et le canal de vente Amazon.

Courant [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} tâches :

- [Actions de commande](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Recherche de commande](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Traitement d’une commande](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Afficher une commande](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Traitement d’une commande](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Informations sur la commande et le compte](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Informations sur l’adresse](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Mode de paiement et de livraison](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Vérifier les éléments triés](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Emettre un crédit/remboursement](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Exécution/envoi d’une commande](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Créer une facture](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Annuler une commande non expédiée](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si une commande est dans `Unshipped` status, vous pouvez [annuler une commande Amazon ;](./cancel-unshipped-order.md) sur le [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) page. Si une commande a été expédiée, elle ne peut pas être annulée.

Voir [Gestion des commandes commerciales](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
