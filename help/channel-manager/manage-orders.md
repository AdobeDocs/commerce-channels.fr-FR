---
title: Gestion des commandes de Walmart Marketplace
description: Affichage et gestion [!DNL Walmart Marketplace] commandes avec [!DNL Channel Manager] pour Adobe Commerce et Magento Open Source.
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 70f8b5487cf1c6507ce8e3cbaec91f4fc883d683
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Gestion des commandes de Walmart Marketplace

[!DNL Walmart Marketplace] commandes pour [!DNL Commerce] les listes de produits sont synchronisées automatiquement avec [!DNL Channel Manager] après que Walmart ait traité la commande. Une fois la synchronisation terminée, vous pouvez afficher les informations de commande en sélectionnant **[!UICONTROL Orders]** depuis la vue de la boutique de canaux connectée dans [!DNL Channel Manager].

![Vue Commandes du gestionnaire de canaux pour gérer les commandes de Walmart Marketplace](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Cela peut prendre jusqu’à 35 minutes pour une [!DNL Walmart Marketplace] l’ordre d’affichage dans la variable [!DNL Channel Manager] liste des commandes. [!DNL Walmart] le traitement des commandes entrantes et leur envoi à [!DNL Channel Manager].  Une fois que le Gestionnaire de canaux a reçu la commande, la création et l’affichage de la commande dans Adobe Commerce ou Magento Open Source prend 5 minutes de plus.

## Commandes de révision

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir le [!UICONTROL Channel Manager Marketplace Stores] page.

1. Ouvrez la vue de magasin en sélectionnant l’icône en forme de crayon dans une ligne d’entrée de magasin.

1. Pour afficher les informations sur la commande, sélectionnez *[!UICONTROL *Orders]**.

## Afficher les détails de la commande

Une fois qu’une commande est reçue du marketplace et importée dans Adobe Commerce ou Magento Open Source, utilisez la variable [!DNL Commerce] Identifiant de commande pour afficher la commande dans Adobe Commerce.

De **[!UICONTROL Orders]**, sélectionnez la variable [!UICONTROL Commerce Order Number] pour ouvrir le [!DNL Commerce]  détails de la commande.

![Vue détaillée des commandes commerciales pour une commande Walmart Marketplace](assets/order-detail-with-external-order-id.png)

### Commandes et descriptions de colonnes

Les tableaux suivants décrivent les commandes et les colonnes disponibles pour les commandes.

**Contrôles pour[!UICONTROL Orders]**
| **Contrôle**                    | **Description**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     | Triez la vue en sélectionnant l’une des options suivantes : [!UICONTROL Order Status] cartes.                                                                                        | | Détails des messages d’erreur | Passez la souris sur le [!UICONTROL Error Status] pour une commande qui affiche le message d’erreur détaillé.                                                                      | | [!UICONTROL View order detail] | Pour afficher les détails de la commande, sélectionnez la variable [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande. |

**Descriptions des colonnes**

| Champ | Description |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | Numéro de commande affecté à la commande dans la variable [!DNL Walmart Marketplace]. Lorsqu’une commande est initialement importée dans [!DNL Channel Manager], seul le numéro de commande Walmart s’affiche. Lorsque la variable [!DNL Commerce] l’ordre est créé, la variable [!DNL Walmart] le numéro de commande est stocké dans la variable [!UICONTROL External ID] attribut de produit. |
| [!DNL Commerce]  Numéro de commande | Le numéro attribué à la variable [!DNL Commerce]  l’ordre créé à partir de [!DNL Walmart Marketplace] commande. |
| Éléments | Nombre d’éléments commandés sur [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Coût total des articles commandés. |
| [!UICONTROL Date Created] | Date à laquelle la commande a été créée dans la variable [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Date à laquelle la commande doit être expédiée pour répondre [!DNL Walmart Marketplace] conditions requises. |
| [!UICONTROL Order Status] | Indique l’état actuel de la commande dans la variable [!DNL Commerce] workflow de commande. L’état est mis à jour lorsque vous ajoutez des produits à [!DNL Channel Manager] et lorsque vous faites correspondre les produits sur la [!DNL Walmart Marketplace]. Si une opération échoue, la liste affiche le statut Erreur . Après avoir corrigé l’erreur, [!DNL Channel Manager] tente à nouveau l’opération et met à jour l’état. |

### À propos de l’état de commande

[!UICONTROL Order Status] fournit des informations sur l’état actuel de [!DNL Walmart Marketplace] commandes gérées depuis Adobe Commerce ou Magento Open Source. Les mises à jour de l’état de commande surviennent lorsque [!DNL Channel Manager] reçoit des informations de commande mises à jour de la part de l’opérateur [!DNL Walmart Marketplace] ou le [!DNL Commerce] système de commande. Les commandes peuvent avoir les états suivants :

* **[!UICONTROL Open]**-Commandes reçues de la part de la fonction [!DNL Walmart Marketplace] prêt à être examiné et traité dans Adobe Commerce ou Magento Open Source.

   Après qu’un client a commandé un produit à partir de la variable [!DNL Walmart Marketplace], la commande d’ouverture peut prendre jusqu’à 35 minutes dans l’espace de travail de l’ordre pour le canal connecté. [!DNL Commerce] le traitement des commandes entrantes et leur envoi à [!DNL Channel Manager]. Une fois que le Gestionnaire de canaux a reçu la commande, il faut 5 minutes de plus pour créer et afficher la variable [!DNL Commerce] commande.

* **[!UICONTROL Processed]**-Commandes qui ont été expédiées, annulées ou remboursées à partir de la variable [!DNL Commerce] magasin.

   Pour afficher toutes les commandes expédiées, annulées et remboursées, sélectionnez la variable **Traités** carte d’état.

* **[!UICONTROL Canceled]**-Commandes annulées à partir de la variable [!DNL Commerce] magasin.

   Une fois la commande annulée, la variable [!DNL Commerce] mises à jour de la quantité de stock pour refléter les éléments renvoyés. Alors, [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]**-Commandes qui ont été remboursées à partir du [!DNL Commerce] magasin.

   Une fois le remboursement effectué, la variable [!DNL Commerce] mises à jour de la quantité de stock pour refléter les articles remboursés. Alors, [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace].

* **[!UICONTROL Error]**- Commandes qui n’ont pas été importées dans le référentiel de commandes en raison d’informations manquantes ou d’autres problèmes.

   Pour afficher les détails du message d’erreur, passez la souris sur l’objet *[!UICONTROL Error]* indicateur d’état. Une fois l’erreur résolue, la commande est mise à jour automatiquement afin d’afficher les informations et l’état actuels.
