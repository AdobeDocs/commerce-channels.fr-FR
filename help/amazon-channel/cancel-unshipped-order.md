---
title: Annuler une commande non expédiée
description: Annuler une commande en attente ou partiellement expédiée (non expédiée) via votre Amazon [!DNL Seller Central] compte.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Annuler une commande non expédiée

Les commandes Amazon ne peuvent être annulées que si elles se trouvent dans un `Unshipped` statut. Si la commande est en attente ou partiellement expédiée (non expédiée), la commande ne peut être annulée que par votre [!DNL Amazon Seller Central] compte. Si l&#39;objet a été expédié, les retours et les échanges doivent également être traités dans votre [!DNL Amazon Seller Central] Compte.

>[!NOTE]
>
>Pour les tâches autres que l’annulation d’une commande :
>
>- Si vous avez [importation de commande](./order-settings.md) activées, les commandes sont gérées dans le noeud [[!DNL Commerce] workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- Si [importation de commande](./order-settings.md) est désactivé, vous devez gérer vos commandes dans [!DNL Amazon Seller Central].


## Annuler la commande dans `Unshipped` statut

1. Cliquez sur **[!UICONTROL View Store]** sur la carte de magasin.

1. Dans la boîte de dialogue _[!UICONTROL Recent Orders]_dans le tableau de bord de la boutique, cliquez sur un numéro de commande.

   Le _[!UICONTROL Amazon Order Details]_s’affiche.

1. Cliquez sur **[!UICONTROL Cancel Order]** dans la barre d’en-tête.

   Cette option s’affiche uniquement pour les commandes dans `Unshipped` statut.

1. Pour **[!UICONTROL Reason for cancellation]**, choisissez une option.

1. Cliquez sur **[!UICONTROL Confirm]**.

   La commande est annulée et l’état est mis à jour en `Canceled` dans les détails de la commande.

La notification d’annulation est envoyée à votre [!DNL Amazon Seller Central] et le client associé à la commande est également informé. Statut de la [!DNL Commerce] le cas échéant, les modifications apportées à `Complete`.
