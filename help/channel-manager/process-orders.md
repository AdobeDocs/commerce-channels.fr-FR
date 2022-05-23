---
title: Traiter les commandes
description: Instructions d’expédition et d’annulation [!DNL Walmart Marketplace] commandes d’Adobe Commerce et de Magento Open Source.
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Traiter les commandes

Si vous utilisez Adobe Commerce et Magento Open Source Order Management pour gérer votre [!DNL Commerce] vente en magasin, traitement [!DNL Walmart Marketplace] commandes de Commerce à l’aide d’un workflow similaire.

Lorsque vous traitez une commande dans Commerce, le Gestionnaire de canaux synchronise les mises à jour avec [!DNL Walmart Marketplace]. Cette mise à jour permet de s’assurer que l’état de l’inventaire et de la commande des produits de Commerce correspond aux données suivies dans la variable [!DNL Walmart Marketplace] et avertit Walmart d’envoyer des informations sur l’état de la commande et l’expédition aux clients.

>[!NOTE]
>
> La synchronisation des mises à jour de commande peut prendre jusqu’à cinq minutes. [!DNL Walmart Marketplace]. Pour vérifier l’état de la commande, revenez à [!DNL Channel Manager] Commandes.

## Envoyer une commande

Lorsque vous envoyez une commande à partir de Commerce, vous utilisez la variable [[!DNL Commerce Order Management] workflow d&#39;expédition](https://docs.magento.com/user-guide/sales/order-ship.html). Une fois la commande envoyée, les mises à jour sont synchronisées avec [!DNL Walmart Marketplace]. Ensuite, Walmart informe les clients de l’état de la commande et des détails de livraison.

**Condition requise**

Avant d’envoyer des commandes, vérifiez que la variable [paramètres d’expédition de canal et configuration de l’opérateur](map-shipping-carriers.md) meet [!DNL Walmart Marketplace requirements].

### Créer et envoyer l&#39;envoi

Lorsque vous envoyez une [!DNL Walmart Marketplace] commande à partir de [!DNL Commerce], vous devez ajouter un numéro de tracking. Les clients reçoivent le numéro de suivi dans la notification de l’envoi qu’ils reçoivent. [!DNL Walmart].

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir le [!UICONTROL Channel Manager Marketplace Stores] page.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans la table Commandes , ouvrez la commande à expédier en sélectionnant le **Numéro de commande du commerce**.

1. Créez et envoyez une expédition pour l’ensemble ou une partie d’une commande en sélectionnant **[!UICONTROL Ship]**.

   - Pour choisir un opérateur de transport et ajouter un numéro de tracking, sélectionnez **[!UICONTROL Add tracking number]**.

   - Remplissez le reste du formulaire d’expédition si nécessaire. Voir [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) pour obtenir des instructions détaillées.

1. Après avoir envoyé l’envoi, effectuez le suivi de la variable [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].

## Annuler une commande

Lorsque vous annulez une [!DNL Walmart Marketplace] commande, Walmart requiert une raison d&#39;annulation. Lorsque l’annulation de la commande se met à jour vers Walmart, la raison de l’annulation est incluse dans la notification d’annulation envoyée au client.

Le motif d’annulation est également affiché dans la variable [!DNL Commerce] informations sur les paiements de commande.

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir le [!UICONTROL Channel Manager Marketplace Stores] page.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour un magasin de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans le tableau Commandes, ouvrez la page Détails de la commande en sélectionnant l’option **Numéro de commande du commerce** pour annuler la commande.

   ![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/order-detail-with-external-order-id.png)

1. Annuler la commande.

   - Sélectionner **Annuler** dans le menu Détails de la commande.

   - Dans le formulaire Annuler la commande, sélectionnez l’événement **Motif de l&#39;annulation**.

      ![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/order-detail-with-external-order-id.png)

   - Sélectionner **Annuler la commande**.

1. Vérifier que les mises à jour ont été envoyées à [!DNL Walmart Marketplace] en vérifiant la [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager].
