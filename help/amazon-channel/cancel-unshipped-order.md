---
title: Annuler une commande Amazon non expédiée
description: Annuler une commande en attente ou partiellement expédiée (non expédiée) via votre compte Amazon [!DNL Seller Central] .
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# Annuler une commande Amazon non expédiée

Les commandes Amazon ne peuvent être annulées que si elles ont le statut `Unshipped`. Si la commande est en attente ou partiellement expédiée (non expédiée), elle ne peut être annulée que via votre compte [!DNL Amazon Seller Central]. Si l’élément a été expédié, les retours et les exchanges doivent également être gérés dans votre compte [!DNL Amazon Seller Central].

>[!NOTE]
>
>Pour les tâches autres que l&#39;annulation d&#39;une commande :
>
>- Si [import de commande](./order-settings.md) est activé, les commandes sont gérées dans le [[!DNL Commerce] workflow des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- Si [import de commande](./order-settings.md) est désactivé, vous devez gérer vos commandes dans [!DNL Amazon Seller Central].

## Annuler une commande à l’état `Unshipped`

1. Cliquez sur **[!UICONTROL View Store]** sur la carte du magasin.

1. Dans la section _[!UICONTROL Recent Orders]_du tableau de bord du magasin, cliquez sur un numéro de commande.

   La page _[!UICONTROL Amazon Order Details]_s’affiche.

1. Cliquez sur **[!UICONTROL Cancel Order]** dans la barre d’en-tête.

   Cette option s’affiche uniquement pour les commandes dont l’état est `Unshipped`.

1. Pour **[!UICONTROL Reason for cancellation]**, choisissez une option.

1. Cliquez sur **[!UICONTROL Confirm]**.

   La commande est annulée et l’état est mis à jour vers `Canceled` dans les détails de la commande.

La notification d’annulation est envoyée à votre compte [!DNL Amazon Seller Central] et le client associé à la commande est également informé. L’état de la commande [!DNL Commerce] correspondante, le cas échéant, passe à `Complete`.
