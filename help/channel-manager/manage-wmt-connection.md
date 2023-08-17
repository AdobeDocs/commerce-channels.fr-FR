---
title: Gérer la connexion à Walmart Marketplace
description: 'Mettez à jour les informations d’identification de l’API pour autoriser la connexion entre un [DNL! Commerce] vue de magasin et la variable [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] listes de produits et synchronisez les données de stock, de prix, de commande et d’expédition entre [!DNL Commerce] et le Walmart.'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Cartographier les opérateurs de livraison

Avant [traiter les envois de commande](process-orders.md#ship-an-order) pour [!DNL Walmart Marketplace] commandes, mapper Walmart à des compagnies de transport préférées à l&#39;opérateur correspondant dans [!DNL Commerce] afin que les données d’expédition puissent être synchronisées entre [!DNL Walmart] et [!DNL Commerce].

Les opérateurs de commerce qui ne correspondent pas à un opérateur préféré sont étiquetés comme *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**Conditions préalables**

Réviser [Exigences de Walmart](walmart-requirements.md) pour le [!DNL Marketplace Seller account].

## Mise à jour des informations de connexion

1. Sur le [!UICONTROL Listings] pour la boutique de canaux de vente, sélectionnez **[!UICONTROL Channel Settings]**.

1. Activé **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Walmart Connection]**.

1. Pour modifier les informations d’identification, sélectionnez **[!UICONTROL Change Credentials]**

   ![Mise à jour des informations d’identification de l’API Walmart pour autoriser la connexion](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. Saisissez le **[!UICONTROL Walmart Client ID]** et **[!UICONTROL Walmart Client Secret]**.

1. Sélectionner **[!UICONTROL Save]** pour appliquer la configuration.
