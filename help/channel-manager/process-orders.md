---
title: Traiter les commandes
description: Instructions d’expédition et d’annulation [!DNL Walmart Marketplace] commandes d’Adobe Commerce et de Magento Open Source.
source-git-commit: 90ccbecd6d1433ae1312d79f7ae2d34c8f381b97
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# Traiter les commandes

Si vous utilisez Adobe Commerce et Magento Open Source Order Management pour gérer votre [!DNL Commerce] vente en magasin, processus [!DNL Walmart Marketplace] commandes de Commerce à l’aide d’un workflow similaire.

Lorsque vous traitez une commande dans Commerce, le Gestionnaire de canaux synchronise les mises à jour avec [!DNL Walmart Marketplace]. Cette mise à jour permet de s’assurer que l’état de la commande et les informations d’expédition de Commerce correspondent aux données suivies dans la variable [!DNL Walmart Marketplace].

* **Commande des envois**-Walmart nécessite un numéro de suivi pour toutes les cargaisons. Si la quantité de stock est insuffisante pour remplir une commande entière, vous créez une expédition partielle. Une fois l’envoi envoyé, les mises à jour de la commande sont synchronisées avec [!DNL Walmart Marketplace]. Ensuite, Walmart informe les clients de l’état de la commande et des détails de livraison.

* **Annulations de commande**- Lorsque vous annulez une [!DNL Walmart Marketplace] commande, Walmart requiert une raison d&#39;annulation. La raison de l&#39;annulation est incluse dans le préavis d&#39;annulation de commande envoyé au client. Le motif d’annulation est également affiché dans la variable [!DNL Commerce] informations sur les paiements de commande.

>[!NOTE]
>
> La synchronisation des mises à jour de la commande peut prendre jusqu’à cinq minutes. [!DNL Walmart Marketplace]. Pour vérifier l’état de la commande, revenez à la variable [!DNL Channel Manager] Page Commandes .

## Envoyer une commande

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans la table Commandes , ouvrez la commande à expédier en sélectionnant le **Numéro de commande du commerce**.

1. Créez et envoyez une expédition pour l’ensemble ou une partie d’une commande en sélectionnant **[!UICONTROL Ship]**.

   ![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/order-detail-with-external-order-id.png)

   * Pour choisir un opérateur de transport et ajouter un numéro de tracking, sélectionnez **[!UICONTROL Add tracking number]**.

   * Remplissez le reste du formulaire d’expédition si nécessaire. Voir [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) pour obtenir des instructions détaillées.

1. Après avoir envoyé l’envoi, effectuez le suivi de la variable [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager] pour vérifier que des mises à jour ont été envoyées à [!DNL Walmart Marketplace].

## Annuler une commande

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour un magasin de canaux de vente.

1. Pour afficher [!DNL Walmart Marketplace] commandes, sélectionnez *[!UICONTROL *Orders]**.

1. Dans le tableau Commandes, ouvrez la page Détails de la commande en sélectionnant l’option **Numéro de commande du commerce** pour annuler la commande.

![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/order-detail-with-external-order-id.png)

1. Annuler la commande.

   * Sélectionner **Annuler** dans le menu Détails de la commande.

   * Sur le [!UICONTROL Cancel Order] formulaire, sélectionnez **Motif de l&#39;annulation**.

   ![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/cancel-order-reason-selector.png)

   * Sélectionner **Annuler la commande**.


1. Vérifier que les mises à jour ont été envoyées à [!DNL Walmart Marketplace] en vérifiant la [état de commande](manage-orders.md#about-order-status) in [!DNL Channel Manager].
