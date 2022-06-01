---
title: Traiter les commandes
description: Instructions d’expédition et d’annulation [!DNL Walmart Marketplace] commandes d’Adobe Commerce et de Magento Open Source.
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: f1c37111df2f566b9673946bb9b2b282506f990c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Traiter les commandes

Après [!DNL Walmart Marketplace] les commandes ont été acquittées et envoyées avec succès à [!DNL Channel Manager], vous utilisez [Gestion des commandes commerciales](https://docs.magento.com/user-guide/sales/orders-workspace.html) pour traiter la commande.

Le Gestionnaire de canaux synchronise les mises à jour avec [!DNL Walmart Marketplace] pour s’assurer que l’état de la commande et les informations d’expédition de Commerce correspondent aux données suivies dans la variable [!DNL Walmart Marketplace].

* **Commande des envois**-Walmart nécessite un numéro de suivi pour toutes les cargaisons. Si certains articles sont en rupture de stock, vous pouvez créer des envois partiels pour envoyer les articles actuellement disponibles. Une fois l’envoi envoyé, les mises à jour de la commande sont synchronisées avec [!DNL Walmart Marketplace]. Ensuite, Walmart informe les clients de l’état de la commande et des détails de livraison.

* **Annulations de commande**- Lorsque vous annulez une [!DNL Walmart Marketplace] Pour commander, Walmart exige une raison d’annulation qui est incluse dans l’avis d’annulation de commande envoyé au client. Le motif d’annulation est également affiché dans la variable [!DNL Commerce] informations sur les paiements de commande.

>[!NOTE]
>
> La synchronisation des mises à jour de la commande peut prendre jusqu’à cinq minutes. [!DNL Walmart Marketplace]. Pour vérifier l’état de la commande, revenez à la variable [!DNL Channel Manager] Page Commandes .

## Envoyer une commande

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans la table Commandes , ouvrez la commande à expédier en sélectionnant le **Numéro de commande du commerce**.

1. Créez et envoyez une expédition pour l’ensemble ou une partie d’une commande en sélectionnant **[!UICONTROL Ship]**.

   ![Affichage des détails d’une commande Commerce pour une [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

   * Sélectionnez un opérateur de transport et ajoutez un numéro de suivi en sélectionnant **[!UICONTROL Add tracking number]**.

      ![Affichage des détails d’une commande Commerce pour une [!DNL Walmart Marketplace] order](assets/order-shipment-add-tracking-number.png)


   * Remplissez le reste du formulaire d’expédition si nécessaire. Voir [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) pour obtenir des instructions détaillées.

1. Après avoir envoyé l’envoi, effectuez le suivi de la variable [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].

## Annuler une commande

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour un magasin de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans le tableau Commandes, ouvrez la page Détails de la commande en sélectionnant l’option **Numéro de commande du commerce** pour annuler la commande.

   ![Affichage des détails d’une commande Commerce pour une[!DNL Walmart Marketplace]order](assets/order-detail-with-external-order-id.png)

1. Annuler la commande.

   * Sélectionner **Annuler** dans le menu Détails de la commande.

   * Sur le [!UICONTROL Cancel Order] formulaire, sélectionnez **Motif de l&#39;annulation**.
   ![Affichage des détails d’une commande Commerce pour une [!DNL Walmart Marketplace] order](assets/cancel-order-reason-selector.png)

   * Sélectionner **Annuler la commande**.


1. Après avoir envoyé l’annulation, effectuez le suivi de la variable [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].
