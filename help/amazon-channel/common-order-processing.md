---
title: Tâches de traitement des commandes courantes
description: Utilisez la [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Administrateur.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Tâches de traitement d&#39;ordre commun

[[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} peut gérer vos commandes Amazon, y compris envoyer un e-mail à l&#39;acheteur, honorer la commande (expédition), émettre des crédits/remboursements, ajouter des commentaires, etc. Pour gérer vos commandes Amazon, votre [**Importer les commandes Amazon**](./order-settings.md) doit être défini sur `Enabled` afin que [!DNL Commerce] les commandes sont créées lors de la réception des commandes Amazon. Les informations sur les commandes Amazon s’affichent dans le dossier *[!UICONTROL Recent Orders]* du tableau de bord de la boutique.

Lorsque cette option est activée, elle correspond [!DNL Commerce] les commandes sont créées pour les commandes Amazon et le numéro de commande Amazon s’affiche dans le _[!UICONTROL Order Number]_colonne. Si une [!DNL Commerce] La commande est créée, cliquez sur le numéro de commande pour ouvrir la commande dans le noeud [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html)Page {target=&quot;_blank&quot;}. Vous pouvez gérer la commande comme vous le faites pour les autres [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

Le [!DNL Commerce] le numéro de commande ne s’affiche pas avec le _[!UICONTROL Recent Orders]_informations. Le [!DNL Commerce] le numéro de commande s’affiche uniquement lorsque vous cliquez sur le numéro de commande dans le tableau de bord de magasin et ouvrez la commande dans [[!DNL Commerce] traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Lors de l’affichage de la [!DNL Commerce] , le numéro de commande Amazon s’affiche dans le champ *[!UICONTROL Payment & Shipping Method]*. Il comprend également des options pour *[!UICONTROL View or Cancel Amazon Order]*et *[!UICONTROL View all Amazon Orders]*, en fonction du statut d&#39;expédition de la commande.

Voir [annulation d’une commande non expédiée](./cancel-unshipped-order.md).

![Amazon des informations de commande dans la commande Commerce](assets/amazon-order-number-payment-info.png)

Lors du traitement d’une commande Amazon, le canal de vente Amazon met à jour et synchronise les informations de commande avec votre [!DNL Amazon Seller Central] compte. Vos paramètres cron déterminent la fréquence de synchronisation des informations de commande entre le canal de vente Amazon et Amazon.

commun [!DNL Commerce] [traitement des commandes](https://docs.magento.com/user-guide/sales/order-processing.html)Les tâches {target=&quot;_blank&quot;} incluent :

- [Actions de commande](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Recherche de commande](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Traitement d’une commande](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Afficher une commande](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Traitement d’une commande](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Informations sur la commande et le compte](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Informations sur l&#39;adresse](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Mode de paiement et d&#39;expédition](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Vérifier les éléments commandés](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Émission d&#39;un crédit/remboursement](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Exécution/expédition d&#39;une commande](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Création d’une facture](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Annuler une commande non expédiée](./cancel-unshipped-order.md)

>[!NOTE]
>
>Si une commande est en `Unshipped` état, vous pouvez [annulation d’une commande Amazon](./cancel-unshipped-order.md) sur [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) . Si une commande a été expédiée, elle ne peut pas être annulée.

Voir [Gestion des commandes commerciales](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
