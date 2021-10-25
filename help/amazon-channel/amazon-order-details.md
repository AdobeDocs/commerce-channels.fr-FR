---
title: Détails de la commande Amazon
description: Consultez les détails de vos commandes Amazon Marketplace dans l’administrateur Magento Open Source ou Adobe Commerce.
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Détails de la commande Amazon

![Détails de la commande Amazon](assets/amazon-order-details-header.png)

## Afficher les détails de la commande Amazon

1. Cliquez sur **[!UICONTROL View Store]** sur la carte de magasin.

1. Dans la boîte de dialogue _[!UICONTROL Recent Orders]_, cliquez sur un numéro de commande.

   Le _[!UICONTROL Amazon Order Details]_s’ouvre.

>[!NOTE]
>
>Si l’importation de commande est activée dans votre [Paramètres de commande](./order-settings.md) et la commande est [réalisé par Amazon (FBA)](./fulfilled-by.md), vous pouvez voir des données fictives pour certains champs dans les détails de commande. Amazon n&#39;envoie pas les données suivantes pour les commandes FBA.
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`


### Onglet Détails de la commande et de l&#39;expédition

Le _[!UICONTROL Order and Shipping Details]_affiche des informations détaillées sur la commande, telles qu’elles ont été reçues d’Amazon.

>[!IMPORTANT]
>
>Amazon accepte les informations d&#39;adresse non standard qui ne peuvent pas être importées dans le canal de vente Amazon, empêchant ainsi les codes d&#39;état/pays de se mettre à jour correctement pour certaines commandes. Pour corriger les erreurs d’adresse, les champs suivants peuvent être modifiés dans les détails de la commande :
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>N’oubliez pas de cliquer sur **Enregistrer la commande** après avoir effectué des modifications.

![Détails de la commande et de l&#39;expédition](assets/amazon-order-details.png)

### Onglet Articles de commande

Le _[!UICONTROL Order Items]_affiche tous les éléments associés à la commande Amazon, tels qu’ils ont été reçus d’Amazon.

![Détails de l&#39;article de commande](assets/amazon-order-item-details.png)

### Onglet Suivi

Le _[!UICONTROL Tracking]_affiche les informations de suivi associées à l’ordre Amazon.

![Détails du suivi](assets/amazon-order-tracking-details.png)
