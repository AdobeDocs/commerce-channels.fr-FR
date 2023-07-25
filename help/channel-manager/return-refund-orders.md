---
title: Commandes de retour et de remboursement
description: Instructions pour émettre des remboursements complets ou partiels pour les demandes de retour reçues de [!DNL Walmart Marketplace] de [!DNL Channel Manager] pour Adobe Commerce et Magento Open Source.
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Commandes de retour et de remboursement

Lorsqu’un acheteur demande un retour pour des articles commandés achetés via [!DNL Walmart Marketplace], Walmart crée une demande de retour. [!DNL Channel Manager] surveille le canal Marketplace pour ces requêtes et synchronise automatiquement les informations de demande de retour dans le Gestionnaire de canaux.

Côté Commerce, la demande de retour lance le workflow suivant :

1. Le Gestionnaire de canaux crée une requête de retour correspondante avec un état reçu et ajoute le numéro d’ID de retour ([!UICONTROL RMA #]) au [!UICONTROL Returns] tableau de bord. Sur le [!DNL Orders] tableau de bord, le détail de l’état de la commande associée aux mises à jour de retour afin d’inclure une [!UICONTROL Return requested] pour afficher et traiter le retour.

1. Les commerçants traitent le remboursement associé au retour en créant un avoir à la suite de la [Workflow de remboursement Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). Tous les remboursements sont traités à l’aide de la méthode hors ligne.

1. [!DNL Channel Manager] envoie une mise à jour du remboursement à Walmart Marketplace afin que l’état du retour puisse être mis à jour pour refléter le remboursement complet d’Adobe Commerce.

Dans l’administrateur du storefront, vous pouvez afficher et traiter les retours à partir du Gestionnaire de canaux en ouvrant la boutique de canaux de vente et en sélectionnant **[!UICONTROL Returns]**.

![Gestionnaire de canaux : renvoie un tableau de bord pour traiter les remboursements des demandes de retour reçues de [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Vous pouvez uniquement traiter les remboursements pour les commandes expédiées. Dans [!DNL Channel Manager], l’état de la commande doit être [!UICONTROL Shipped]. Dans [!DNL Walmart Marketplace] Compte du vendeur, la commande doit être [!UICONTROL Delivered].

## Commandes et descriptions de colonnes

Les tableaux suivants décrivent les contrôles et les colonnes disponibles pour [!DNL Channel Manager] renvoie .

**Contrôles pour[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Contrôle</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Pour filtrer la vue, sélectionnez l’une des options suivantes : [!UICONTROL Return Status] cartes.</td>
</tr>
<tr>
<td>Détails du statut</td>
<td>Pour les entrées de retour avec la variable [!UICONTROL Received] ou [!UICONTROL Refunded] , vous pouvez créer ou visualiser l’avoir pour le remboursement en sélectionnant le texte associé dans la colonne Détails du statut .</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Pour afficher les détails de la commande, sélectionnez la variable [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] pour ouvrir la commande Commerce.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Pour modifier la configuration du canal, sélectionnez les informations d’identification de la connexion Walmart, les attributs mappés ou les identifiants d’expédition du canal, les paramètres sélectionnent l’ [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande.</td>
</tr>
</table>

**Descriptions des colonnes**

<table>
<tr>
<td><strong>Champ</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>Numéro d’autorisation de marchandisage de retour associé à la demande de retour reçue de [!DNL Walmart Marketplace]. Ce nombre est généré par Walmart Marketplace [!UICONTROL Returns] lorsque le processus de retour est lancé.</td>
</tr>
<tr>
<td>[!DNL Commerce] Numéro de commande</td>
<td>Le [!DNL Commerce] Numéro de commande associé aux éléments inclus dans la demande de retour de Walmart Marketplace. Pour afficher les détails de la commande, sélectionnez le numéro de la commande.</td>
</tr>
<tr>
<td>Demandé</td>
<td>Date à laquelle le retour a été demandé dans la variable [!DNL Walmart Marketplace]
converti en heure locale.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>La date à laquelle le retour doit être remboursé pour être atteint [!DNL Walmart Marketplace] [conditions requises](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) converti en heure locale.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Répertorie le SKU et la quantité de chaque élément répertorié dans le renvoi.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>Valeur totale à rembourser pour les éléments renvoyés.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indique l’état actuel du retour dans la variable [!DNL Commerce] workflow de retour<i>Reçu</i>, <i>Remboursement</i>ou <i>Erreur</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Pour les entrées de retour reçues et remboursées, les détails de statut fournissent un lien pour accéder à l’avoir de crédit pour le traitement du remboursement. Si une erreur se produit au cours de la variable [!DNL Channel Manager] processus de synchronisation entre Adobe Commerce et [!DNL Walmart marketplace], ce champ fournit la description de l’erreur.</td>
</tr>
</table>

## Statut de retour

[!UICONTROL Return Status] fournit des informations sur l’état actuel de [!DNL Walmart Marketplace] demandes de retour gérées à partir d’Adobe Commerce ou de Magento Open Source.

Les mises à jour d’état de retour se produisent lorsque [!DNL Channel Manager] reçoit une requête de retour de la [!DNL Walmart Marketplace] ou lorsque la variable [!DNL Commerce] note de crédit est créée pour traiter le remboursement des articles renvoyés.

Les retours peuvent avoir les états suivants :

* **[!UICONTROL Received]**-Il s’agit de l’état initial de la demande de retour reçue de la fonction [!DNL Walmart Marketplace] magasin. Le marchand peut traiter le remboursement du retour en sélectionnant **[!UICONTROL Create credit memo]** dans le [!UICONTROL Status details].

* **[!UICONTROL Refunded]**: indique qu’un avoir a été créé pour émettre un remboursement pour les articles renvoyés. Les vendeurs peuvent afficher les informations de remboursement en sélectionnant **[!UICONTROL View credit memo]** dans le [!UICONTROL Status details].

* **[!UICONTROL Error]**: renvoie les requêtes qui comportent des erreurs. Des erreurs peuvent se produire lorsque la demande de retour de Walmart contient des données manquantes ou incorrectes. Ou, si [!DNL Channel Manager] ne peut pas envoyer la notification de mise à jour de remboursement à Walmart.

## Scénarios de retour

Les scénarios suivants décrivent comment émettre des remboursements pour différents types de demandes de retour provenant de [!DNL Channel Manager].

* **Retour complet**: si la demande de retour de Walmart Marketplace concerne tous les articles de la commande, mettez à jour la quantité d’avoir à rembourser pour tous les articles.

* **Retour partiel**- Si la demande de retour de Walmart Marketplace concerne uniquement certains articles de commande, mettez à jour la quantité de la note de crédit uniquement pour les articles à rembourser.

* **Retour déjà remboursé par Walmart Marketplace**- Dans certains cas, un remboursement est traité sur [!DNL Walmart Marketplace] avant de traiter le retour dans le Gestionnaire de canaux. Par exemple, si une commande Commerce n’est pas remboursée dans la fenêtre de traitement des remboursements de 48 heures requise par Walmart, Walmart rembourse automatiquement la commande. Dans ce cas, le gestionnaire de canaux synchronise toujours la demande de retour à Adobe Commerce afin que vous puissiez traiter le retour et émettre l’avoir. Ce workflow permet de s’assurer que les détails de la commande sont indiqués dans la section [!DNL Commerce] correspond aux informations de commande dans Walmart Marketplace.

>[!NOTE]
>
> La synchronisation des mises à jour de remboursement avec peut prendre jusqu’à cinq minutes. [!DNL Walmart Marketplace]. Vous pouvez vérifier l’état actuel du retour à partir du [!DNL Channel Manager] [!UICONTROL Returns] tableau de bord.

## Traitement de la demande de remboursement

1. Ouvrez le [!UICONTROL Returns] tableau de bord de la boutique de canaux de vente.

   * Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

   * Vous pouvez consulter les retours en sélectionnant le **[!UICONTROL Returns]** .

     Vous pouvez également accéder aux informations de retour à partir de la [!UICONTROL Orders] page. Rechercher [!UICONTROL Shipped] commandes qui comportent une requête de retour. Sélectionnez ensuite le `Return requested` dans le [!UICONTROL Status Details] pour afficher et traiter la requête.

1. Dans le tableau Retours , recherchez un retour avec la variable *[!UICONTROL Received]* statut.

1. Dans la colonne articles , passez en revue la liste des articles de commande et la quantité à rembourser.

1. Traitez le remboursement en émettant un relevé de crédit.

   * Dans la [!UICONTROL Status Details] colonne, sélectionnez **[!UICONTROL Create credit memo]** pour ouvrir la page Détails de la commande dans [!DNL Commerce].

     Si la commande n’a pas été facturée, la page Détails de la commande affiche un message d’erreur vous invitant à en créer un. Sélectionner **[!UICONTROL Create invoice]**. Alors, [créer et enregistrer la facture](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * Sur la page Détails de la commande, sélectionnez **[!UICONTROL Credit Memo]**.

   * Dans [!UICONTROL Items to Refund] de la section [!UICONTROL Credit Memo], mettez à jour la variable **[!UICONTROL Qty to refund]** et **[!UICONTROL Return to Stock]** informations pour les éléments inclus dans la requête de retour.

     Veillez à ne renvoyer que les éléments répertoriés dans la requête de retour.

   * Pour ajouter un commentaire, saisissez le texte dans le champ **[!UICONTROL Credit Memo Comments]**

   * Sélectionner **[!UICONTROL Refund Offline]**.

Après avoir effectué le remboursement, [!DNL Channel Manager] met à jour l’état de retour dans la variable [!UICONTROL Returns] tableau de bord à [!UICONTROL Refunded] et synchronise la mise à jour avec Walmart pour mettre à jour l’état de retour sur Marketplace.


## Afficher les informations de remboursement pour un retour

Vous pouvez afficher des informations sur les demandes de retour et le traitement des remboursements depuis la variable [!UICONTROL Returns] tableau de bord.

1. Ouvrez le tableau de bord Retours pour votre boutique de canaux de vente.

   * Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Ouvrez la vue du magasin en sélectionnant l’icône représentant un oeil pour une boutique de canaux de vente.

   * Sélectionner **[!UICONTROL Returns]**.

1. Afficher les commandes remboursées en sélectionnant **[!UICONTROL Refunded]** carte d’état.

1. Afficher les détails du remboursement d’un retour en sélectionnant **[!UICONTROL View credit memo]**.

   ![Note de crédit pour le remboursement des articles renvoyés pour un événement [!DNL Walmart Marketplace] order](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Une fois la commande remboursée, la variable [!UICONTROL Orders] le tableau de bord n’affiche pas les informations de retour. Pour afficher les informations de retour, utilisez la variable [!DNL Channel Manager] Renvoie le tableau de bord. Des informations plus détaillées sur les retours et les remboursements sont également disponibles sur la page Détails de la commande .

## Correction des erreurs de retour

Des erreurs peuvent se produire lorsque les informations renvoyées sont reçues de [!DNL Walmart Marketplace]ou lorsque [!DNL Channel Manager] synchronise les mises à jour d’état depuis [!DNL Commerce] to [!DNL Walmart Marketplace].

Si l’opération de synchronisation pour une mise à jour de retour échoue, la variable [!DNL Channel Manager] Le tableau de bord affiche une *[!UICONTROL Error]* statut de l’entrée de retour. Pour vous assurer que les informations de retour et de retour sont reflétées avec précision dans le compte Walmart Marketplace, mettez manuellement à jour la commande dans votre [!DNL Walmart Marketplace] magasin.
