---
title: 'Afficher et gérer les commandes à partir de [!DNL Channel Manager]'
description: 'Afficher et gérer [!DNL Walmart Marketplace] les commandes avec  [!DNL Channel Manager] pour Adobe Commerce et Magento Open Source.'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Afficher et suivre les commandes de [!DNL Channel Manager]

[!DNL Walmart Marketplace] Les données de commande pour les produits [!DNL Commerce] se synchronisent automatiquement vers [!DNL Channel Manager] après le traitement de la commande par [!DNL Walmart].

Du côté [!DNL Commerce], une synchronisation réussie déclenche les actions suivantes :

- [!DNL Channel Manager] envoie un accusé de réception de commande à Walmart.

- Une commande [!DNL Commerce] correspondante est créée à partir de la commande Walmart.

- Les informations de commande mises à jour s’affichent dans le tableau de bord [!DNL Channel Manager] Commandes .

Dans l’administrateur du storefront, vous pouvez afficher les données de commande de [!DNL Channel Manager] en ouvrant la boutique de canaux de vente et en sélectionnant **[!UICONTROL Orders]**.

![ Vue Commandes du gestionnaire de canaux pour gérer [!DNL Walmart Marketplace] commandes](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Il peut s’écouler jusqu’à 35 minutes avant qu’une commande [!DNL Walmart Marketplace] ne s’affiche dans la liste des commandes [!DNL Channel Manager]. [!DNL Walmart] nécessite environ 30 minutes pour traiter les commandes entrantes et les envoyer à [!DNL Channel Manager]. Une fois que le Gestionnaire de canaux a reçu la commande, la création et l’affichage de la commande dans Adobe Commerce ou Magento Open Source prend environ cinq minutes de plus.

## Commandes et descriptions de colonnes

Les tableaux suivants décrivent les commandes et les colonnes disponibles pour les commandes.

**Contrôles pour[!UICONTROL Orders]**

<table>
<tr>
<td><strong>Contrôle</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Triez la vue en sélectionnant l’une des cartes [!UICONTROL Order Status].</td>
</tr>
<tr>
<td>Détails du statut</td>
<td>Fournit des informations sur les erreurs de commande et les demandes de retour. Pour afficher les informations de retour et l’état du remboursement d’une commande, sélectionnez le texte <strong>[!UICONTROL Return requested]</strong> pour ouvrir le tableau de bord [!UICONTROL Returns].</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Pour afficher les détails de la commande, sélectionnez le numéro de commande [!DNL Commerce] dans la table [!UICONTROL Order]. Ensuite, utilisez les options de commande [!DNL Commerce] pour traiter la commande.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Pour modifier la configuration du canal, sélectionnez les informations d’identification de la connexion Walmart, les attributs mappés ou les identifiants d’expédition, les paramètres sélectionnent le numéro de commande [!DNL Commerce] dans la table [!UICONTROL Order]. Ensuite, utilisez les options de commande [!DNL Commerce] pour traiter la commande.</td>
</tr>
</table>


**Descriptions des colonnes**

<table>
<tr>
<td>Champ</td>
<td>Description</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>Numéro de bon de commande attribué à la commande dans le [!DNL Walmart Marketplace]. Lorsqu’une commande est initialement importée vers [!DNL Channel Manager], seul le numéro de commande [!DNL Walmart] s’affiche. Lorsque la commande [!DNL Commerce] est créée, le numéro de commande [!DNL Walmart] est stocké dans l’attribut de produit [!UICONTROL External ID].</td>
</tr>
<tr>
<td>[!DNL Commerce] Numéro de commande</td>
<td>Numéro attribué à la commande [!DNL Commerce] créée à partir de la commande [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>Éléments</td>
<td>Nombre d’éléments commandés sur [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Coût total des articles commandés.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>Date à laquelle la commande a été envoyée au [!DNL Walmart Marketplace] converti en fuseau horaire local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>Date à laquelle la commande doit être expédiée pour répondre aux exigences [!DNL Walmart Marketplace] converties dans le fuseau horaire local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>Date à laquelle la commande doit être envoyée au client pour répondre aux exigences [!DNL Walmart Marketplace] converties dans le fuseau horaire local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>La [[!DNL Walmart Marketplace] méthode d’expédition](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 sélectionnée pour la commande.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Horodatage indiquant la dernière fois que les données de commande ont été mises à jour dans [!DNL Channel Manager] converties en fuseau horaire local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indique l’état actuel de la commande dans le workflow de commande [!DNL Commerce]. L’état initial d’une commande importée depuis [!DNL Walmart Marketplace] est _Open_. D'autres mises à jour d'état se produisent lorsque [!DNL Commerce] commandes sont traitées et [!DNL Channel Manager] synchronise avec succès les mises à jour d'envoi, d'envoi partiel et d'annulation vers [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Fournit des informations plus détaillées sur les commandes en erreur ou les demandes de remboursement.</td>
</tr>
</table>

## État de la commande

[!UICONTROL Order Status] fournit des informations sur l’état actuel de [!DNL Walmart Marketplace] commandes gérées depuis Adobe Commerce ou Magento Open Source. Les mises à jour de l&#39;état de la commande se produisent lorsque [!DNL Channel Manager] reçoit des informations de commande mises à jour de la part du système de commande [!DNL Walmart Marketplace] ou [!DNL Commerce]. Les commandes peuvent avoir les états suivants :

- **[!UICONTROL Shipped]** : commandes qui ont été expédiées à partir du magasin [!DNL Commerce]. Lorsque la commande est envoyée, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour le statut de livraison sur Walmart et fournir le numéro de suivi de la commande pour l&#39;expédition. Une fois la commande expédiée, les articles de commande peuvent être partiellement ou intégralement remboursés si Walmart génère un formulaire d’autorisation de marchandisage de retour. Voir [Renvoie et remboursements](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** : commandes dont certains éléments sont marqués comme étant expédiés et d’autres en attente d’expédition. Lorsque des éléments dans le navire de commande, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour l’état de livraison vers _[!DNL Partially Shipped]_sur Walmart et fournissez le numéro de suivi de commande pour l’expédition.

- **[!UICONTROL Canceled]** : commandes annulées à partir du magasin [!DNL Commerce].

  Une fois l’annulation de la commande terminée, la quantité de stock [!DNL Commerce] est mise à jour pour refléter les articles renvoyés. Ensuite, [!DNL Channel Manager] synchronise la mise à jour avec [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]** : si Walmart Marketplace demande un retour pour les articles de commande qui ont été expédiés, un lien `Return requested` s’affiche dans la colonne [!UICONTROL Status details]. Si vous sélectionnez le lien, le tableau de bord [!UICONTROL Returns] s’ouvre pour visualiser le retour et gérer le processus de remboursement.

- **[!UICONTROL Error]** : commandes comportant des erreurs. Des erreurs peuvent se produire lorsqu’une opération de mise à jour de commande échoue. Par exemple, des erreurs se produisent si [!DNL Channel Manager] ne peut pas recevoir une nouvelle commande de Walmart. Elles peuvent également se produire si [!DNL Channel Manager] ne peut pas envoyer d’envoi de commande ou d’annulation de la mise à jour vers [!DNL Walmart Marketplace]. Si une opération échoue, la page Commandes affiche l’état _Error_ pour la commande. Pour plus d’informations, voir [Correction des erreurs de commande](process-orders.md#fix-shipping-and-annulation- errors).

- **[!UICONTROL Status details]** - Fournit plus d’informations sur les erreurs de commande qui se produisent en raison de problèmes tels que des informations manquantes ou des valeurs non valides, des détails d’expédition incorrects ou une annulation de commande ayant échoué. La description permet de déterminer si l’erreur s’est produite sur l’instance [!DNL Commerce] ou sur l’instance [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si des éléments de commande sont envoyés dans plusieurs envois, l’état de la commande dans [!DNL Channel Manager] reflète l’état de la dernière commande disponible. Par exemple, si le premier élément est livré et qu’aucune erreur n’est renvoyée lorsque les mises à jour de commande sont synchronisées avec [!DNL Channel Manager] et [!DNL Walmart Marketplace], l’état de la commande [!DNL Channel Manager] est _[!UICONTROL Partially Shipped]_. Si un second élément est fourni et que [!DNL Channel Manager] renvoie une erreur, l’état de la commande est mis à jour vers_[!UICONTROL Error]_.

## Commandes de révision

1. Dans l&#39;Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir la page [!UICONTROL Channel Manager Marketplace Stores].

1. Ouvrez la vue de magasin en sélectionnant l’icône représentant un oeil dans une ligne d’entrée de magasin.

1. Pour afficher les informations sur la commande, sélectionnez *[!UICONTROL *Orders]**.

1. Obtenez des informations sur la commande et déterminez les étapes suivantes en vérifiant la colonne **[Status](#order-status)**.

## Vérification des détails de la commande

Une fois qu’une commande est reçue du marketplace et importée dans votre boutique de canaux de vente, utilisez l’ [!DNL Commerce] ID de commande pour afficher les détails de la commande dans Adobe Commerce.

Dans **[!UICONTROL Orders]**, sélectionnez le **[!UICONTROL Commerce Order Number]** pour ouvrir le détail de la commande [!DNL Commerce].

![ Vue détaillée des commandes Commerce pour une [!DNL Walmart Marketplace] commande](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

Dans le storefront Commerce, les commandes importées depuis [!DNL Walmart Marketplace] comportent les informations supplémentaires suivantes incluses dans les données de commande :

- **Informations de paiement et mode d’expédition** : les commandes importées de Walmart incluent les valeurs suivantes pour les champs de paiement et d’expédition :

   - **[!UICONTROL Offline Channel Payment]** : indique que le paiement de la commande est traité hors ligne par [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** : affiche le numéro de commande [!DNL Walmart Marketplace].

   - **[!UICONTROL Channel Shipping - Value]**-Indique que les frais d’expédition sont gérés via [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Ce champ s’affiche uniquement si une commande importée depuis [!DNL Walmart Marketplace] est annulée. Les raisons de l&#39;annulation sont les suivantes :

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Éléments commandés** : cette section répertorie les éléments de commande sur toutes les commandes Commerce. La colonne [!UICONTROL Qty] fournit l’historique des états des éléments de commande. Par exemple, si une commande a été facturée, expédiée et remboursée, vous pouvez voir les transitions d’état.

  ![Historique des statuts des articles commandés de détails de commande [!DNL Walmart Marketplace] commandes](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Pour afficher les détails des factures et des remboursements des articles, sélectionnez les options [!UICONTROL Invoice] et [!UICONTROL Credit Memo] dans le menu de navigation. Vous pouvez également accéder à la Note de crédit directement depuis le tableau de bord [[!UICONTROL Returns]](return-refund-orders.md) de votre boutique de canaux de vente.
