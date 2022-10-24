---
title: Mappage des opérateurs de navigation
description: 'Mappez les attributs pour correspondre à [DNL! Commerce] de produits existants [!DNL Walmart Marketplace] listes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].'
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 3f6039ad78ff500c31129bee12d65e291e226567
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Mappage des opérateurs de navigation

Avant [traiter les envois de commande](process-orders.md#ship-an-order) pour [!DNL Walmart Marketplace] commandes, mapper Walmart à des compagnies de transport préférées à l&#39;opérateur correspondant dans [!DNL Commerce] afin que les données d’expédition puissent être synchronisées entre [!DNL Walmart] et [!DNL Commerce].

Les opérateurs de commerce qui ne correspondent pas à un opérateur préféré sont étiquetés comme *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**Conditions préalables**

Avant de mapper les opérateurs de transport, effectuez les tâches suivantes :

1. Consultez la section [Méthodes de l’opérateur et bonnes pratiques d’expédition pour la livraison en temps réel](https://sellerhelp.walmart.com/s/guide?article=000009473) pour [!DNL Walmart Marketplace].

1. Vérifiez les [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) et [[!UICONTROL Shipping Settings]](https://docs.magento.com/user-guide/configuration/sales/shipping-settings.html) dans votre [!DNL Commerce] magasin pour vous assurer que vous avez optimisé la configuration pour [!DNL Walmart Marketplace sales].

## Mappage des opérateurs de navigation

1. Dans la **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** page, sélectionnez **[!UICONTROL Channel Settings]**.

1. Activé **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Shipping Carriers]**.

   ![Mappage des opérateurs de navigation](assets/map-shipping-carriers.png)

1. Pour chaque [!DNL Walmart] opérateur préféré répertorié, sélectionnez [!DNL Commerce] nom de l’opérateur dans la liste déroulante si l’opérateur est disponible.

1. Sélectionner **[!UICONTROL Save]** pour appliquer la configuration.

