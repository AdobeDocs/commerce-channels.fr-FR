---
title: Workflows d’exécution Amazon
description: L’exécution d’une commande d’une liste Amazon suit une séquence spécifique, de l’envoi de la commande à l’expédition.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Workflows d’exécution Amazon

## Exemple : rempli par le marchand

| Étape | Description |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Une commande effectuée par le commerçant est placée sur Amazon.** Amazon affecte l’état `Pending` jusqu’à ce que les informations de carte de crédit du client soient vérifiées. Les commandes dont le statut est `Pending` sont automatiquement importées dans le canal de vente Amazon, mais ne s’affichent pas sur l’onglet _[!UICONTROL Orders]_. |
| 2 | **La commande est vérifiée par Amazon.** Une fois vérifié, Amazon remplace l’état par `Unshipped`. Avec ce changement d’état, la commande est mise à jour dans le canal de vente Amazon et s’affiche dans l’onglet _[!UICONTROL Orders]_. |
| 3 | **Les détails de la commande sont mis à jour.** Le canal de vente Amazon met à jour les détails de la commande avec le prix, l’adresse électronique du client et le nom du client. Lors de cette mise à jour, la commande Amazon crée la commande correspondante [!DNL Commerce] dans la page de gestion des commandes. Le numéro de commande [!DNL Commerce] s’affiche avec les informations de commande sur l’onglet _[!UICONTROL Orders]_. |
| 4 | **Un nouveau compte client est créé.** Si ce paramètre est configuré dans les paramètres de commande et que le client n’existe pas dans votre base de données [!DNL Commerce], un nouveau client est créé dans votre base de données [!DNL Commerce] à l’aide des informations client correspondantes de la commande Amazon. Si vous avez choisi `No Customer Creation (guest)` dans les paramètres de votre commande, celle-ci suit le processus invité [!DNL Commerce] et ne crée pas de client dans votre base de données. À ce stade, si votre système [!DNL Commerce] est intégré à un ERP/OMS/WMS, la commande est récupérée en fonction de l’intégration d’une nouvelle commande placée et créée dans [!DNL Commerce]. |
| 5 | **La commande est expédiée.** Sur la page de traitement des commandes [!DNL Commerce], vous envoyez la commande et ajoutez un numéro de suivi. Lorsque tous les éléments sont marqués dans un état `Shipped` :<ul><li>L’état de la commande [!DNL Commerce] passe à `Complete`.</li><li>L’état de la commande du canal de vente Amazon passe à `Shipped`.</li><li>Le numéro de suivi est synchronisé avec Amazon et l’état de l’ordre dans Amazon passe à `Shipped`.</li><li>Les notifications d’expédition sont envoyées au client via Amazon, et non depuis [!DNL Commerce] (selon les stratégies d’Amazon). |

## Exemple : rempli par Amazon (FBA)

| Étape | Description |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Une commande remplie par Amazon est placée sur Amazon.** |
| 2 | **La commande est importée.** La commande n’est pas importée dans le canal de vente Amazon tant que l’état `Shipped` de la commande n’a pas été attribué par Amazon. Comme Amazon dispose de l’inventaire de ce produit, il empêche toute interférence avec la gestion de votre entrepôt/inventaire. |
| 3 | **Les détails de la commande sont mis à jour.** Si elle est configurée dans vos [paramètres de commande](./order-settings.md), la commande Amazon crée la commande [!DNL Commerce] correspondante et peut être créée sous la forme d’une commande dont l’état est `Complete`. |
