---
title: Publish Listings to Walmart
description: Publish listings for Commerce products to Walmart Marketplace to begin selling.
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: a10ab3f7fa7049e48d83a942f6c5441d8147b12c
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Publish Listings to Walmart

Like other marketplaces, Walmart allows third-party sellers to list items that are sold by others.

The platform uses product identifiers like UPC and GTIN to match items that are already for sale.
For matched products, the existing Walmart Marketplace listing updates to include the Commerce product offer.

Usually, products with the lowest prices appear in the results first, but other factors like reviews also affect placement.

## Match products

When you match products, Channel Manager sends the product data to Walmart Marketplace to search for existing listings with attribute values that match the mapped Commerce product attribute. [](map-product-attributes-for-matching.md)

If a match is found, the existing product listing is updated to add your offer.

### Prerequisites

Before matching products, verify that your product catalog attribute values meet Walmart requirements and configure attribute settings. [](map-product-attributes-for-matching.md)

#### Select and match products

1. Open a connected sales channel.

1. **[!UICONTROL Listings]***[!UICONTROL Draft]*

   ![](assets/products-in-marketplace-sales-channel.png)

1. **[!UICONTROL Match Products]**

   A message indicates the number of products sent for matching.

   ![](assets/products-submit-for-matching.png)

   [!UICONTROL **] It can take up to 30 minutes for Walmart Marketplace to complete the match operation.

### Check match status

1. ****

1. Check the product status.

   ****

   * **[!UICONTROL Match]** Your product offer was published to an existing Walmart Marketplace listing.

   * **[!UICONTROL Error]**

      * An error occurred and the match operation failed.

      * No match was found.

      * [](walmart-prerequisites.md#walmart-marketplace-store-status)

### Check listing on Walmart

[[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items)

### Troubleshoot product match errors

If the product match operation fails, the Walmart Marketplace returns an error code and Channel Manager displays the error status in the product listing information.

**** Common errors returned are incorrectly formatted Product ID values or missing required attributes.

#### Fix Product ID values

| Type | Description | Example |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, the 12-digit number including check-digit. </br></br> | `45678912345``045678912345` |
| GTIN | GTIN-14, the 14-digit number including check-digit. </br></br></br> | `456789123456``0045678912345` |
| EAN | GTIN-13, the 13-digit number including check-digit. </br></br></br> | `4567891234``0004567891234` |

[](https://sellerhelp.walmart.com/s/guide?article=000005844)

## Upload new product listings

For products that have no match on Walmart Marketplace, use a Walmart product category Excel template to bulk upload product listings. You populate the Walmart template using product catalog data exported from your Commerce instance.

For new product listings, check your product catalog to ensure that products you plan to sell on Walmart Marketplace have the attributes required for Walmart Marketplace product listings.

****

| **** | **** |
|--------------------------|-----------------------|
| SKU | Required |
| Product name | Required |
| Product ID type | Required |
| Product ID | Required |
| Brand | Required |
| Short description | Required |
| Selling price | Required |
| Site description | Required |
| Main image URL | Required |
| Shipping weight | Required |
| Key features | Recommended |
| Model number | Recommended |
| Manufacturer name | Recommended |
| Manufacturer part number | Recommended |
| Size | Recommended |
| Color | Recommended |
| Main image URL | Facultatif |
| Additional image URL | Facultatif |
| Manufacturer | Facultatif |

### Prerequisites

* [](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.k2lo9voad1gx)

* In your Commerce product catalog, verify that the catalog configuration for the products to list on Walmart Marketplace have all required attributes and meet Walmart Marketplace Content Guidelines.

* Verify that the cron job is running to complete the export operation.

   * [](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html)

   * [](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html)

### Create the product data file to upload

1. [](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)

   * **[!UICONTROL Add Items]** **[!UICONTROL Add items in bulk]**

      ![](assets/walmart-seller-account-add-items-bulk.png)

   * **[!UICONTROL Full Setup]** Then, select an item category and download the category template.

      ![](assets/walmart-seller-account-full-setup-download.png)

   * Verify that the template includes the required and recommended attributes for the product listing.

1. [!DNL Commerce]

   * [!UICONTROL ********]

   * [!UICONTROL Export][!UICONTROL Entity Type][!UICONTROL ****]

   * [!UICONTROL Entity Attributes]
   ![[!UICONTROL Commerce Admin]](assets/walmart-seller-account-full-setup-download.png)

   Use filters to select and configure the attribute values that apply to the product categories that you sell in. [](https://docs.magento.com/user-guide/system/data-export.html)

   [!UICONTROL ****]

1. [!UICONTROL ****]

   `var/export/folder` [](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html)**

1. Open the Excel template for the Walmart Marketplace product category, and use Excel macro capabilities to merge the exported product data into the Excel template.

1. Upload the Excel file with the exported product data.

   * [](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)

   * [!UICONTROL ********]
   * Drag the completed spreadsheet to the Upload section.
   * [!UICONTROL ****]
   * [!UICONTROL  ****]

[](https://sellerhelp.walmart.com/s/guide?article=000007680)[!DNL **]
