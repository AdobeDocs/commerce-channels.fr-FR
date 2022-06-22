---
title: '"Afficher et suivre les commandes depuis [!DNL Channel Manager]'''
description: '"Afficher et gérer [!DNL Walmart Marketplace] commandes avec [!DNL Channel Manager] pour Adobe Commerce et Magento Open Source.'''
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Afficher et suivre les commandes depuis [!DNL Channel Manager]

[!DNL Walmart Marketplace] données de commande pour [!DNL Commerce] les produits se synchronisent automatiquement avec [!DNL Channel Manager] after [!DNL Walmart] traite l’ordre.

Sur le [!DNL Commerce] côté, une synchronisation réussie déclenche les actions suivantes :

- [!DNL Channel Manager] envoie un accusé de réception de commande à Walmart.

- Un [!DNL Commerce] La commande est créée à partir de la commande Walmart.

- Les informations de commande mises à jour s’affichent dans la variable [!DNL Channel Manager] Tableau de bord des commandes.

Dans l’administrateur du storefront, vous pouvez afficher les données de commande à partir de [!DNL Channel Manager] en ouvrant la boutique de canaux de vente et en sélectionnant **[!UICONTROL Orders]**.

![Vue Commandes du Gestionnaire de canaux [!DNL Walmart Marketplace] commandes](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Cela peut prendre jusqu’à 35 minutes pour une [!DNL Walmart Marketplace] l’ordre d’affichage dans la variable [!DNL Channel Manager] liste des commandes. [!DNL Walmart] le traitement des commandes entrantes et leur envoi à [!DNL Channel Manager]. Une fois que le Gestionnaire de canaux a reçu la commande, la création et l’affichage de la commande dans Adobe Commerce ou Magento Open Source prend environ cinq minutes de plus.

## Commandes et descriptions de colonnes

Les tableaux suivants décrivent les commandes et les colonnes disponibles pour les commandes.

**Contrôles pour[!UICONTROL Orders]**
| **Contrôle**                    | **Description**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     | Triez la vue en sélectionnant l’une des options suivantes : [!UICONTROL Order Status] cartes.                                                                                                                                                                                                           | | Description de l’erreur | Fournit des informations plus détaillées sur les commandes dont l’état est Erreur.                                                                                                                                                                                                            | | [!UICONTROL View order detail] | Pour afficher les détails de la commande, sélectionnez la variable [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande.                                                                                                                    | | [!UICONTROL Channel Settings]  | Pour modifier la configuration du canal, sélectionnez les informations d’identification de la connexion Walmart, les attributs mappés ou les identifiants d’expédition du canal, les paramètres sélectionnent l’ [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande. |


**Descriptions des colonnes**

| Champ | Description |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | Numéro de commande affecté à la commande dans la variable [!DNL Walmart Marketplace]. Lorsqu’une commande est initialement importée dans [!DNL Channel Manager], seule la variable [!DNL Walmart] Le numéro de commande s’affiche. Lorsque la variable [!DNL Commerce] l’ordre est créé, la variable [!DNL Walmart] le numéro de commande est stocké dans la variable [!UICONTROL External ID] attribut de produit. |
| [!DNL Commerce] Numéro de commande | Le numéro attribué à la variable [!DNL Commerce] l’ordre créé à partir de [!DNL Walmart Marketplace] commande. |
| Éléments | Nombre d’éléments commandés sur [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Coût total des articles commandés. |
| [!UICONTROL Date Ordered] | Date à laquelle la commande a été envoyée sur la page [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Date à laquelle la commande doit être expédiée pour répondre [!DNL Walmart Marketplace] conditions requises. |
| [!UICONTROL Deliver By Date] | Date à laquelle la commande doit être envoyée au client pour qu’il réponde [!DNL Walmart Marketplace] conditions requises au format UTC. |
| [!UICONTROL Ship Method] | Le [[!DNL Walmart Marketplace] Méthode d’expédition](https://sellerhelp.walmart.com/s/guide?article=000007893) sélectionné pour la commande. |
| [!UICONTROL Last Update At] | Horodatage indiquant la dernière fois où les données de commande ont été mises à jour dans [!DNL Channel Manager] au format UTC. |
| [!UICONTROL Status] | Indique l’état actuel de la commande dans la variable [!DNL Commerce] workflow de commande. Etat initial d&#39;une commande importée depuis [!DNL Walmart Marketplace] is _Ouvrir_. D’autres mises à jour d’état surviennent lorsque [!DNL Commerce] les commandes sont traitées et [!DNL Channel Manager] synchronise correctement les mises à jour d’expédition, de livraison partielle et d’annulation dans la variable [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | Fournit des informations plus détaillées sur les commandes avec un _[!UICONTROL Error]_statut. |

## État de la commande


[!UICONTROL Order Status] fournit des informations sur l’état actuel de [!DNL Walmart Marketplace] commandes gérées depuis Adobe Commerce ou Magento Open Source. Les mises à jour de l’état de commande surviennent lorsque [!DNL Channel Manager] reçoit des informations de commande mises à jour de la part de l’opérateur [!DNL Walmart Marketplace] ou le [!DNL Commerce] système de commande. Les commandes peuvent avoir les états suivants :

- **[!UICONTROL Shipped]**-Commandes expédiées à partir du [!DNL Commerce] magasin. Lorsque la commande est expédiée, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour le statut de l’expédition sur Walmart et indiquer le numéro de suivi de la commande pour l’expédition.

- **[!UICONTROL Partially Shipped]**: commandes dont certains éléments sont marqués comme étant expédiés et d’autres sont en attente d’expédition. Lorsque des articles sont commandés, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour l’état de livraison en _[!DNL Partially Shipped]_sur Walmart et indiquez le numéro de suivi de la commande pour l’expédition.

- **[!UICONTROL Canceled]**-Commandes annulées à partir de la variable [!DNL Commerce] magasin.

   Une fois la commande annulée, la variable [!DNL Commerce] mises à jour de la quantité de stock pour refléter les éléments renvoyés. Alors, [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace].

- **[!UICONTROL Error]**- Commandes qui comportent des erreurs. Des erreurs peuvent se produire lorsqu’une opération de mise à jour de commande échoue. Par exemple, des erreurs se produisent si [!DNL Channel Manager] ne peut pas recevoir une nouvelle commande de Walmart. Elles peuvent également se produire si [!DNL Channel Manager] ne peut pas envoyer de livraison de commande ou d’annulation à la variable [!DNL Walmart Marketplace]. Si une opération échoue, la page Commandes affiche une _Erreur_ état de la commande. Pour plus d’informations, voir [Correction des erreurs d’ordre](process-orders.md#fix-shipping-and-annulation- errors).

- **[!UICONTROL Error description]**-Fournit des informations détaillées sur les erreurs de commande qui se produisent en raison de problèmes tels que des informations manquantes ou des valeurs non valides, des détails d’envoi incorrects ou une annulation de commande ayant échoué. La description permet de déterminer si l’erreur s’est produite sur la variable [!DNL Commerce] ou sur l’instance [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si des articles de commande sont envoyés dans plusieurs envois, l’état de la commande dans [!DNL Channel Manager] reflète l’état de la dernière commande disponible. Par exemple, si le premier élément est envoyé et qu’aucune erreur n’est renvoyée lorsque les mises à jour de commande sont synchronisées avec [!DNL Channel Manager] et [!DNL Walmart Marketplace], la variable [!DNL Channel Manager] l’état de la commande _[!UICONTROL Partially Shipped]_. Si un second élément est expédié et [!DNL Channel Manager] renvoie une erreur, l’état de la commande est mis à jour vers_[!UICONTROL Error]_.

## Commandes de révision

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir le [!UICONTROL Channel Manager Marketplace Stores] page.

1. Ouvrez la vue de magasin en sélectionnant l’icône représentant un oeil dans une ligne d’entrée de magasin.

1. Pour afficher les informations sur la commande, sélectionnez *[!UICONTROL *Orders]**.

1. Obtenez des informations sur la commande et déterminez les étapes suivantes en vérifiant la variable **[État](#about-order-status)** colonne .

## Afficher les détails de la commande

Une fois qu’une commande est reçue du marketplace et importée dans Adobe Commerce ou Magento Open Source, utilisez la variable [!DNL Commerce] Identifiant de commande pour afficher la commande dans Adobe Commerce.

De **[!UICONTROL Orders]**, sélectionnez la variable **[!UICONTROL Commerce Order Number]** pour ouvrir le [!DNL Commerce] détails de la commande.

![Affichage des détails d’une commande Commerce pour une [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

Dans le storefront Commerce, les commandes importées depuis [!DNL Walmart Marketplace] inclure les informations supplémentaires suivantes dans les données de commande :

- **Informations de paiement et mode d’expédition**-Les commandes importées depuis Walmart comprennent les valeurs suivantes pour les champs de paiement et d’expédition :

   - **[!UICONTROL Offline Channel Payment]**: indique que le paiement de la commande est traité hors ligne par [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**: affiche la variable [!DNL Walmart Marketplace] numéro de commande.

   - **[!UICONTROL Channel Shipping - Value]**-Indique que les frais d’expédition sont gérés par [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Ce champ s’affiche uniquement si une commande importée depuis [!DNL Walmart Marketplace] est annulée. Les raisons de l&#39;annulation sont les suivantes :

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

