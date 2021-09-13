---
title: Workflows d’exécution Amazon
description: L’exécution d’une commande d’une liste Amazon suit une séquence spécifique, de l’envoi de la commande à l’expédition.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Workflows d’exécution Amazon

## Exemple : accomplie par le marchand

| Étape | Description |
|----|----|
| 1 | **Une commande remplie par le commerçant est placée sur Amazon.** Amazon attribue un état de  `Pending` jusqu’à ce que les informations de carte de crédit du client soient vérifiées. Les commandes dont le statut est `Pending` sont automatiquement importées dans le canal de vente Amazon, mais ne s’affichent pas dans l’onglet _[!UICONTROL Orders]_. |
| 2 | **La commande est vérifiée par Amazon.** Une fois vérifié, Amazon remplace l’état par  `Unshipped`. Avec ce changement d’état, la commande est mise à jour dans le canal de vente Amazon et s’affiche dans l’onglet _[!UICONTROL Orders]_. |
| 1 | **Les détails de la commande sont mis à jour.** Le canal de vente Amazon met à jour les détails de la commande avec le prix, l’e-mail du client et le nom du client. Lors de cette mise à jour, la commande Amazon crée la commande [!DNL Commerce] correspondante dans la page de gestion des commandes. Le [!DNL Commerce] numéro de commande est affiché avec les informations de commande sur l&#39;onglet _[!UICONTROL Orders]_. |
| 4 | **Un nouveau compte client est créé.** S’il est configuré dans les paramètres de la commande et si le client n’existe pas dans votre  [!DNL Commerce] base de données, un nouveau client est créé dans votre  [!DNL Commerce] base de données à l’aide des informations client correspondantes provenant de la commande Amazon. Si vous choisissez `No Customer Creation (guest)` dans les paramètres de votre commande, la commande suit le processus invité [!DNL Commerce] et ne crée pas de client dans votre base de données. À ce stade, si votre système [!DNL Commerce] est intégré à un système ERP/OMS/WMS, la commande est récupérée en fonction de l’intégration d’une nouvelle commande placée et créée dans [!DNL Commerce]. |
| 5 | **La commande est expédiée.** Sur la page de traitement des  [!DNL Commerce] commandes, vous envoyez la commande et ajoutez un numéro de suivi. Lorsque tous les éléments sont marqués dans un état `Shipped` :<ul><li>L’état de la commande [!DNL Commerce] passe à `Complete`.</li><li>La commande du canal de vente Amazon passe à l’état `Shipped`.</li><li>Le numéro de suivi est synchronisé avec Amazon et l’état de la commande dans Amazon passe à `Shipped`.</li><li>Les notifications d’expédition sont envoyées au client via Amazon, et non depuis [!DNL Commerce] (selon les politiques d’Amazon). |

## Exemple : satisfaite par Amazon (FBA)

| Étape | Description |
|---|---|
| 1 | **Une commande remplie par Amazon est placée sur Amazon.** |
| 2 | **La commande est importée.** La commande n’est pas importée dans le canal de vente Amazon tant que le  `Shipped` statut de la commande n’a pas été attribué par Amazon. Comme Amazon dispose de l’inventaire de ce produit, il empêche toute interférence avec la gestion de l’entrepôt/de l’inventaire. |
| 1 | **Les détails de la commande sont mis à jour.** S’il est configuré dans vos paramètres de  [commande](./order-settings.md), la commande Amazon crée l’ [!DNL Commerce] ordre correspondant et peut être créée sous la forme d’une commande dont l’état est  `Complete`. |
