---
title: Traiter les commandes
description: '''Instructions d''expédition et d''annulation [!DNL Walmart Marketplace] commandes d''Adobe Commerce et de Magento Open Source.'''
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Traiter les commandes

Une fois que [!DNL Walmart Marketplace] commandes ont été acquittées et envoyées avec succès à [!DNL Channel Manager], vous utilisez [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) pour traiter la commande.

Le gestionnaire de canaux synchronise les mises à jour vers [!DNL Walmart Marketplace] pour s’assurer que l’état de la commande et les informations d’expédition depuis [!DNL Commerce] correspondent aux données suivies dans [!DNL Walmart Marketplace].

* **Commande d’envois**-Walmart nécessite un numéro de suivi pour toutes les envois. Si certains articles sont en rupture de stock, vous pouvez créer des envois partiels pour envoyer les articles actuellement disponibles. Après l’envoi de l’envoi, les mises à jour de la commande sont synchronisées avec [!DNL Walmart Marketplace]. Ensuite, Walmart informe les clients de l’état de la commande et des détails de livraison.

* **Annulations de commande** - Lorsque vous annulez une commande [!DNL Walmart Marketplace], Walmart nécessite une raison d’annulation qui est incluse dans l’avis d’annulation de commande envoyé au client. La raison de l’annulation s’affiche également dans les informations de paiement de commande [!DNL Commerce]. Après avoir envoyé l’annulation, les mises à jour de stock sont synchronisées avec [!DNL Walmart Marketplace]. Ensuite, Walmart informe les clients de l’état de la commande et des détails de livraison.

  Dans le storefront, vous devez annuler la commande entière. [!DNL Commerce] n’autorise pas les annulations partielles.

* **Demande de remboursement** - Si un retour Walmart Marketplace est demandé pour une commande expédiée, l’ [!UICONTROL Status details] comprend un lien vers le retour. Les retours et les remboursements sont gérés à partir du tableau de bord [Renvoie](return-refund-orders.md).

Lorsque les commandes Commerce sont traitées et que [!DNL Channel Manager] synchronise avec succès les mises à jour d’expédition, d’expédition partielle et d’annulation vers [!DNL Walmart Marketplace], le traitement des commandes est terminé. Les demandes de retour et les remboursements pour les commandes expédiées sont gérés à partir du tableau de bord [Renvoie](return-refund-orders.md).

>[!NOTE]
>
> La synchronisation des mises à jour de commande vers [!DNL Walmart Marketplace] peut prendre jusqu’à cinq minutes. Pour vérifier l’état de la commande, revenez à la page [!DNL Channel Manager] Commandes .

## Envoyer une commande

1. Dans l’Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez **[!UICONTROL Orders]**.

1. Dans la table Commandes , ouvrez la commande à expédier en sélectionnant le **[!UICONTROL Commerce Order Number]**.

1. Créez et envoyez une expédition pour tout ou partie d’une commande en sélectionnant **[!UICONTROL Ship]**.

   ![ Vue détaillée des commandes Commerce pour une [!DNL Walmart Marketplace] commande](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Sélectionnez un opérateur de transport et ajoutez un numéro de suivi en sélectionnant **[!UICONTROL Add tracking number]**.

     ![ Vue détaillée des commandes Commerce pour une [!DNL Walmart Marketplace] commande](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Remplissez le reste du formulaire d’expédition si nécessaire. Voir [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) pour obtenir des instructions détaillées.

1. Après l&#39;envoi de l&#39;envoi, effectuez le suivi de l&#39;[état de la commande](manage-orders.md#about-order-status) dans [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].

Une fois une commande expédiée, vous pouvez traiter les remboursements complets ou partiels de [!DNL Channel Manager] pour les articles inclus dans la commande en fonction des demandes de retour reçues de [!DNL Walmart Marketplace]. Voir [Commandes de retour et de retour](return-refund-orders.md).

## Annuler une commande

1. Dans l’Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour un magasin de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL Orders]**.

1. Dans la table Commandes, ouvrez la [page des détails de la commande](manage-orders.md#view-order-detail) en sélectionnant **[!UICONTROL Commerce Order Number]** pour que la commande soit annulée.

   ![ Vue détaillée des commandes Commerce pour une [!DNL Walmart Marketplace]commande](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Annuler la commande.

   * Sélectionnez **Annuler** dans le menu Détails de la commande.

   * Sur le formulaire [!UICONTROL Cancel Order], sélectionnez le **[!UICONTROL Cancellation reason]**.

   ![ Vue détaillée des commandes Commerce pour une [!DNL Walmart Marketplace] commande](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Sélectionnez **[!UICONTROL Cancel Order]**.

1. Après avoir soumis l&#39;annulation, effectuez le suivi de l&#39;[état de la commande](manage-orders.md#about-order-status) dans [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].

## Correction des erreurs d’ordre

Des erreurs peuvent se produire pendant le processus de synchronisation des commandes à partir de [!DNL Walmart Marketplace] ou pendant le processus de mise à jour des commandes pour les envois, les envois partiels et les annulations.

Si l’opération de synchronisation pour une expédition, une expédition partielle ou une mise à jour d’annulation échoue, la page [!DNL Channel Manager] Commandes affiche le statut _Erreur_ pour la commande. Pour vous assurer que les informations d’expédition et d’annulation de commande sont correctement reflétées dans le compte Walmart Marketplace, mettez manuellement à jour la commande dans votre boutique [!DNL Walmart Marketplace].


