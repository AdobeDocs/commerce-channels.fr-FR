---
title: Détails de la commande Amazon
description: Affichez les détails de vos commandes Amazon Marketplace dans Adobe Commerce ou Magento Open Source Admin.
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Détails de la commande Amazon

![Détails de la commande Amazon](assets/amazon-order-details-header.png)

## Affichage des détails de commande Amazon

1. Cliquez sur **[!UICONTROL View Store]** dans la carte du magasin.

1. Dans la section _[!UICONTROL Recent Orders]_, cliquez sur un numéro de commande.

   La page _[!UICONTROL Amazon Order Details]_s’ouvre.

>[!NOTE]
>
>Si l’importation de commande est activée dans vos [Paramètres de commande](./order-settings.md) et que la commande est [remplie par Amazon (FBA)](./fulfilled-by.md), des données factices peuvent s’afficher pour certains champs dans les détails de la commande. Amazon n’envoie pas les données suivantes pour les commandes FBA.
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


### Onglet Détails de la commande et de l’expédition

L’onglet _[!UICONTROL Order and Shipping Details]_affiche des informations détaillées sur les commandes, telles qu’elles sont reçues d’Amazon.

>[!IMPORTANT]
>
>Amazon accepte les informations d’adresse non standard qui ne peuvent pas être importées dans le canal de vente Amazon, ce qui empêche les codes état/pays de se mettre à jour correctement pour certaines commandes. Pour corriger les erreurs d’adresse, les champs suivants sont modifiables dans les détails de la commande :
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>N’oubliez pas de cliquer sur **Enregistrer la commande** après avoir apporté des modifications.

![Détails de la commande et de l’expédition](assets/amazon-order-details.png)

### Onglet Articles de commande

L’onglet _[!UICONTROL Order Items]_affiche tous les éléments associés à la commande Amazon, tels qu’ils sont reçus d’Amazon.

![Détails de l’article de commande](assets/amazon-order-item-details.png)

### Onglet Tracking

L’onglet _[!UICONTROL Tracking]_affiche les informations de tracking associées à la commande Amazon.

![Détails du suivi](assets/amazon-order-tracking-details.png)
