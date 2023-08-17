---
title: Annuler une commande Amazon non expédiée
description: Annuler une commande en attente ou partiellement expédiée (non expédiée) via votre Amazon [!DNL Seller Central] compte .
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Annuler une commande Amazon non expédiée

Les commandes Amazon ne peuvent être annulées que si elles se trouvent dans un `Unshipped` statut. Si la commande est en attente ou partiellement expédiée (non expédiée), elle ne peut être annulée que par l’intermédiaire de la fonction [!DNL Amazon Seller Central] compte . Si l’article a été expédié, les retours et les échanges doivent également être gérés dans votre [!DNL Amazon Seller Central] Compte.

>[!NOTE]
>
>Pour les tâches autres que l&#39;annulation d&#39;une commande :
>
>- Si vous avez [import de commande](./order-settings.md) activée, les commandes sont gérées dans la variable [[!DNL Commerce] workflow commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- If [import de commande](./order-settings.md) est désactivé, vous devez gérer vos commandes dans [!DNL Amazon Seller Central].

## Annuler une commande dans `Unshipped` status

1. Cliquez sur **[!UICONTROL View Store]** sur la carte du magasin.

1. Dans le _[!UICONTROL Recent Orders]_dans le tableau de bord de la boutique, cliquez sur un numéro de commande.

   La variable _[!UICONTROL Amazon Order Details]_s’affiche.

1. Cliquez sur **[!UICONTROL Cancel Order]** dans la barre d’en-tête.

   Cette option s’affiche uniquement pour les commandes dans `Unshipped` statut.

1. Pour **[!UICONTROL Reason for cancellation]**, choisissez une option.

1. Cliquez sur **[!UICONTROL Confirm]**.

   La commande est annulée et le statut est mis à jour vers `Canceled` dans les détails de la commande.

La notification d&#39;annulation est envoyée à votre [!DNL Amazon Seller Central] et le client associé à la commande est également informé. L’état de la variable [!DNL Commerce] le cas échéant, la commande est modifiée sur `Complete`.
