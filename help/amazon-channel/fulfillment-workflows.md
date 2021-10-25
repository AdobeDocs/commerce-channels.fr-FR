---
title: Flux de production Amazon
description: L'exécution d'une commande d'une annonce Amazon suit une séquence spécifique depuis l'envoi de la commande jusqu'à l'expédition.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Flux de travaux d’exécution Amazon

## Exemple : accompli par le marchand

| Étape | Description |
|----|----|
| 1 | **Une commande exécutée par le commerçant est passée sur Amazon.** Amazon attribue un statut à `Pending` jusqu&#39;à ce que les informations de carte bancaire du client soient vérifiées. Commandes dans `Pending` statut d&#39;importation automatique dans le canal de vente Amazon, mais ne s&#39;affiche pas sur _[!UICONTROL Orders]_. |
| 2 | **La commande est vérifiée par Amazon.** Une fois la vérification effectuée, Amazon modifie l’état en `Unshipped`. Avec cette modification d’état, la commande est mise à jour dans le canal de vente Amazon et apparaît dans le noeud _[!UICONTROL Orders]_. |
| 3 | **Les détails de la commande sont mis à jour.** Le canal de vente Amazon met à jour les détails de la commande avec le prix, l’adresse électronique du client et le nom du client. Au cours de cette mise à jour, l’ordre Amazon crée les [!DNL Commerce] commande dans la page de gestion des commandes. Le [!DNL Commerce] le numéro de commande s’affiche avec les informations de commande sur la _[!UICONTROL Orders]_. |
| 4 | **Un nouveau compte client est créé.** Si configuré dans vos paramètres de commande et que le client n’existe pas dans votre [!DNL Commerce] , un nouveau client est créé dans votre [!DNL Commerce] à l&#39;aide des informations client correspondantes de la commande Amazon. Si vous avez choisi `No Customer Creation (guest)` dans vos paramètres de commande, la commande suit la [!DNL Commerce] et ne pas créer de client dans votre base de données. À ce stade, si [!DNL Commerce] est intégré à un ERP/OMS/WMS, la commande est récupérée en fonction de l&#39;intégration d&#39;une nouvelle commande en cours de placement et de création à l&#39;intérieur [!DNL Commerce]. |
| 5 | **La commande est expédiée.** De [!DNL Commerce] Page de traitement des commandes, vous expédiez la commande et ajoutez un numéro de suivi. Lorsque tous les éléments sont marqués dans un `Shipped` statut :<ul><li>Le statut de la [!DNL Commerce] ordre des modifications apportées à `Complete`.</li><li>L&#39;état de la commande du canal de vente Amazon devient `Shipped`.</li><li>Le numéro de suivi est synchronisé avec Amazon et l’état de la commande dans Amazon devient `Shipped`.</li><li>Les notifications d’expédition sont envoyées au client via Amazon, et non par [!DNL Commerce] (conformément aux politiques de Amazon). |

## Exemple : réalisé par Amazon (FBA)

| Étape | Description |
|---|---|
| 1 | **Une commande exécutée par Amazon est placée sur Amazon.** |
| 2 | **La commande est importée.** La commande n&#39;est pas importée dans le canal de vente Amazon tant que la commande n&#39;a pas été affectée au `Shipped` par Amazon. Etant donné qu’Amazon possède l’inventaire de ce produit, il évite toute interférence avec votre gestion d’entrepôt/inventaire. |
| 3 | **Les détails de la commande sont mis à jour.** Si configuré dans votre [paramètres de commande](./order-settings.md), l’ordre Amazon crée le fichier [!DNL Commerce] et être créé en tant qu’ordre avec le statut `Complete`. |
