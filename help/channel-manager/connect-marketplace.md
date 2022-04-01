---
title: ' [!DNL Walmart Marketplace]'
description: Configure the sales channel and connect to Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: a10ab3f7fa7049e48d83a942f6c5441d8147b12c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# [!DNL Walmart Marketplace]

[!DNL Commerce]

1. [](#select-the-commerce-store-for-the-sales-channel)

1. [ [!DNL Walmart Marketplace] ](#connect-the-channel-to-walmart-marketplace)

1. [](#complete-store-setup)

## Create the sales channel

1. Open Channel Manager.

   - **[!UICONTROL Marketing** > __]**

   - **[!UICONTROL Connect New Store]**

      ![[!DNL Walmart Marketplace][!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Configure the store and connection:

   - **[!UICONTROL store name]**

   - **[!UICONTROL Adobe Commerce site]**

   - **[!UICONTROL email address]**[!DNL Channel Manager]

      ![[!DNL Walmart Marketplace][!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

## Connect the channel to Walmart Marketplace

1. [!DNL Walmart Marketplace Adobe Production API key][!DNL Walmart Marketplace Seller]

   - **[!UICONTROL Get API credentials]**[!DNL Walmart Marketplace Developer Portal]

      If prompted, select your region (US and Canada) and then log in.

      ![[!DNL Walmart Marketplace]](assets/walmart-marketplace-login-page.png)

   - **[!UICONTROL Client ID]****[!UICONTROL Client Secret]**[!UICONTROL Adobe Inc Production API key]

      ![[!DNL Walmart Marketplace API key]](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >[!DNL Adobe Inc]**[!UICONTROL Add New Key for a Solution Provider]** [ [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key)

   - [!DNL Channel Manager]**[!UICONTROL Walmart Connection]**

      [!DNL Channel Manager]

1. [!UICONTROL Save]

   **[!UICONTROL Channel Manager > Marketplace Stores]**

   ![[!DNL Walmart Marketplace API key]](assets/manage-connected-stores.png)


### Troubleshoot connection issues

[](https://developer.walmart.com/faq/us/faq-auth/)

- [!DNL Walmart Developer Portal][!UICONTROL Adobe Inc.]

- Verify that the access configuration for the Walmart Adobe API key has the correct permissions. [](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key)

- [](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/)

## Complete store setup

[!DNL Walmart Marketplace][!DNL Channel Manager Stores]

To complete store setup:

1. [!UICONTROL Marketing** > ****]

   ![[!DNL Walmart Marketplace API key]](assets/connect-commerce-store-config.png)

1. Open a connected sales channel by selecting the pencil icon in a store entry row.

1. Begin sales channel operations.

   - [Add products from your Commerce Catalog to Channel Manager](add-products-to-connected-channel.md)

   - [Publish products to Walmart using product matching](publish-listings-to-marketplace.md)

   - [View and manage inventory and pricing](inventory-and-price-updates.md)

   - View and manage Walmart orders from the Commerce Admin
