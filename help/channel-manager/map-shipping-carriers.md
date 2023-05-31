---
title: Cartographier les opérateurs de livraison
description: 'Mappez les attributs pour correspondre à [DNL! Commerce] de produits existants [!DNL Walmart Marketplace] listes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].'
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Cartographier les opérateurs de livraison

Avant [traiter les envois de commande](process-orders.md#ship-an-order) pour [!DNL Walmart Marketplace] commandes, mapper Walmart à des compagnies de transport préférées à l&#39;opérateur correspondant dans [!DNL Commerce] afin que les données d’expédition puissent être synchronisées entre [!DNL Walmart] et [!DNL Commerce].

Les opérateurs de commerce qui ne correspondent pas à un opérateur préféré sont étiquetés comme *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**Conditions préalables**

Avant de mapper les opérateurs de transport, effectuez les tâches suivantes :

1. Consultez la section [Méthodes de l’opérateur et bonnes pratiques d’expédition pour la livraison en temps réel](https://sellerhelp.walmart.com/s/guide?article=000009473) pour [!DNL Walmart Marketplace].

1. Vérifiez les [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) et [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) dans votre [!DNL Commerce] magasin pour vous assurer que vous avez optimisé la configuration pour [!DNL Walmart Marketplace sales].

## Mappage des opérateurs de navigation

1. Dans la **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** page, sélectionnez **[!UICONTROL Channel Settings]**.

1. Activé **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Shipping Carriers]**.

   ![Mappage des opérateurs de navigation](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. Pour chaque [!DNL Walmart] opérateur préféré répertorié, sélectionnez [!DNL Commerce] nom de l’opérateur dans la liste déroulante si l’opérateur est disponible.

1. Sélectionner **[!UICONTROL Save]** pour appliquer la configuration.

