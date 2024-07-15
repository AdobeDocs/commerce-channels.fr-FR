---
title: Cartographier les opérateurs de livraison
description: 'Mappez les attributs pour correspondre à [DNL! [Commerce] produits aux  [!DNL Walmart Marketplace] listes existantes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Cartographier les opérateurs de livraison

Avant de [traiter les envois de commandes](process-orders.md#ship-an-order) pour [!DNL Walmart Marketplace] commandes, mappez les opérateurs préférés de Walmart à l&#39;opérateur correspondant dans [!DNL Commerce] afin que les données d&#39;expédition puissent être synchronisées entre [!DNL Walmart] et [!DNL Commerce].

Les opérateurs Commerce qui ne correspondent pas à un opérateur préféré sont étiquetés *[!UICONTROL Other Carrier]* sur [!DNL Walmart].

**Conditions préalables**

Avant de mapper les opérateurs de transport, effectuez les tâches suivantes :

1. Examinez les [ bonnes pratiques d’opérateur et d’expédition pour la livraison en temps réel ](https://sellerhelp.walmart.com/s/guide?article=000009473) pour [!DNL Walmart Marketplace].

1. Vérifiez la configuration [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) et [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) dans votre boutique [!DNL Commerce] pour vous assurer que vous avez optimisé la configuration pour [!DNL Walmart Marketplace sales].

## Mappage des opérateurs de navigation

1. Sur la page **[!UICONTROL Listings]** ou **[!UICONTROL Orders]**, sélectionnez **[!UICONTROL Channel Settings]**.

1. Sur **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Shipping Carriers]**.

   ![Mappage des opérateurs de transport ](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. Pour chaque opérateur [!DNL Walmart] préféré répertorié, sélectionnez le nom de l&#39;opérateur [!DNL Commerce] dans la liste déroulante si l&#39;opérateur est disponible.

1. Sélectionnez **[!UICONTROL Save]** pour appliquer la configuration.

