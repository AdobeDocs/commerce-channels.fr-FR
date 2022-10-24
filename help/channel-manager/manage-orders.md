---
title: '"Afficher et gérer les commandes à partir de [!DNL Channel Manager]'''
description: '"Afficher et gérer [!DNL Walmart Marketplace] commandes avec [!DNL Channel Manager] pour Adobe Commerce et Magento Open Source.'''
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 1180c86ee8f087a2fef84d84171d77fd5b33164b
workflow-type: tm+mt
source-wordcount: '1025'
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

<table>
<tr>
<td><strong>Contrôle</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Triez la vue en sélectionnant l’une des options suivantes : [!UICONTROL Order Status] cartes.</td>
</tr>
<tr>
<td>Détails du statut</td>
<td>Fournit des informations sur les erreurs de commande et les demandes de retour. Pour afficher les informations de retour et l’état du remboursement d’une commande, sélectionnez la variable <strong>[!UICONTROL Return requested]</strong> pour ouvrir le texte [!UICONTROL Returns] tableau de bord.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Pour afficher les détails de la commande, sélectionnez la variable [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Pour modifier la configuration du canal, sélectionnez les informations d’identification de la connexion Walmart, les attributs mappés ou les identifiants d’expédition du canal, les paramètres sélectionnent l’ [!DNL Commerce] numéro de commande dans la variable [!UICONTROL Order] table. Ensuite, utilisez [!DNL Commerce] options de commande pour traiter la commande.</td>
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
<td>Numéro de commande affecté à la commande dans la variable [!DNL Walmart Marketplace]. Lorsqu’une commande est initialement importée dans [!DNL Channel Manager], seule la variable [!DNL Walmart] Le numéro de commande s’affiche. Lorsque la variable [!DNL Commerce] l’ordre est créé, la variable [!DNL Walmart] le numéro de commande est stocké dans la variable [!UICONTROL External ID] attribut de produit.</td>
</tr>
<tr>
<td>[!DNL Commerce] Numéro de commande</td>
<td>Le numéro attribué à la variable [!DNL Commerce] l’ordre créé à partir de [!DNL Walmart Marketplace] commande.</td>
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
<td>Date à laquelle la commande doit être expédiée pour respecter [!DNL Walmart Marketplace] conditions requises converties en fuseau horaire local.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>Date à laquelle la commande doit être envoyée au client pour qu’il réponde [!DNL Walmart Marketplace] conditions requises converties en fuseau horaire local.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>Le [[!DNL Walmart Marketplace] Mode d’expédition](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 sélectionné pour la commande.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Horodatage indiquant la dernière fois où les données de commande ont été mises à jour dans [!DNL Channel Manager] converti en fuseau horaire local.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Indique l’état actuel de la commande dans la variable [!DNL Commerce] workflow de commande. Etat initial d'une commande importée depuis [!DNL Walmart Marketplace] est _Open_. D’autres mises à jour d’état surviennent lorsque [!DNL Commerce] les commandes sont traitées et [!DNL Channel Manager] synchronise correctement les mises à jour d’expédition, de livraison partielle et d’annulation dans la variable [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Fournit des informations plus détaillées sur les commandes en erreur ou les demandes de remboursement.</td>
</tr>
</table>

## État de la commande

[!UICONTROL Order Status] fournit des informations sur l’état actuel de [!DNL Walmart Marketplace] commandes gérées depuis Adobe Commerce ou Magento Open Source. Les mises à jour de l’état de commande surviennent lorsque [!DNL Channel Manager] reçoit des informations de commande mises à jour de la part de l’opérateur [!DNL Walmart Marketplace] ou le [!DNL Commerce] système de commande. Les commandes peuvent avoir les états suivants :

- **[!UICONTROL Shipped]**: commandes qui ont été expédiées à partir du [!DNL Commerce] magasin. Lorsque la commande est expédiée, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour le statut de l’expédition sur Walmart et indiquer le numéro de suivi de la commande pour l’expédition. Une fois la commande expédiée, les articles de commande peuvent être partiellement ou intégralement remboursés si Walmart génère un formulaire d’autorisation de marchandisage de retour. Voir [Renvoie et remboursement](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**: commandes dont certains éléments sont marqués comme étant expédiés et d’autres sont en attente d’expédition. Lorsque des articles sont commandés, [!DNL Channel Manager] envoie une mise à jour à [!DNL Walmart Marketplace] pour mettre à jour l’état de livraison en _[!DNL Partially Shipped]_sur Walmart et indiquez le numéro de suivi de la commande pour l’expédition.

- **[!UICONTROL Canceled]**: commandes qui ont été annulées à partir du [!DNL Commerce] magasin.

   Une fois la commande annulée, la variable [!DNL Commerce] mises à jour de la quantité de stock pour refléter les éléments renvoyés. Alors, [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**: si Walmart Marketplace demande un retour pour les articles de commande qui ont été expédiés, une `Return requested` s’affiche dans la variable [!UICONTROL Status details] colonne . La sélection du lien ouvre la [!UICONTROL Returns] tableau de bord pour visualiser le retour et gérer le processus de remboursement.

- **[!UICONTROL Error]**: commandes qui comportent des erreurs. Des erreurs peuvent se produire lorsqu’une opération de mise à jour de commande échoue. Par exemple, des erreurs se produisent si [!DNL Channel Manager] ne peut pas recevoir une nouvelle commande de Walmart. Elles peuvent également se produire si [!DNL Channel Manager] ne peut pas envoyer de livraison de commande ou d’annulation à la variable [!DNL Walmart Marketplace]. Si une opération échoue, la page Commandes affiche une _Erreur_ état de la commande. Pour plus d’informations, voir [Correction des erreurs d’ordre](process-orders.md#fix-shipping-and-annulation- errors).

- **[!UICONTROL Status details]**-Fournit plus d’informations sur les erreurs de commande qui se produisent en raison de problèmes tels que des informations manquantes ou des valeurs non valides, des détails d’envoi incorrects ou une annulation de commande ayant échoué. La description permet de déterminer si l’erreur s’est produite sur la variable [!DNL Commerce] ou sur l’instance [!DNL Walmart Marketplace].

>[!NOTE]
>
>Si des articles de commande sont envoyés dans plusieurs envois, l’état de la commande dans [!DNL Channel Manager] reflète l’état de la dernière commande disponible. Par exemple, si le premier élément est envoyé et qu’aucune erreur n’est renvoyée lorsque les mises à jour de commande sont synchronisées avec [!DNL Channel Manager] et [!DNL Walmart Marketplace], la variable [!DNL Channel Manager] l’état de la commande _[!UICONTROL Partially Shipped]_. Si un second élément est expédié et [!DNL Channel Manager] renvoie une erreur, l’état de la commande est mis à jour vers_[!UICONTROL Error]_.

## Commandes de révision

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** pour ouvrir le [!UICONTROL Channel Manager Marketplace Stores] page.

1. Ouvrez la vue de magasin en sélectionnant l’icône représentant un oeil dans une ligne d’entrée de magasin.

1. Pour afficher les informations sur la commande, sélectionnez *[!UICONTROL *Orders]**.

1. Obtenez des informations sur la commande et déterminez les étapes suivantes en vérifiant la variable **[État](#order-status)** colonne .

## Vérification des détails de la commande

Une fois qu’une commande a été reçue de la marketplace et importée dans votre boutique de canaux de vente, utilisez la variable [!DNL Commerce] Identifiant de commande pour afficher les détails de la commande dans Adobe Commerce.

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

- **Éléments commandés**: cette section répertorie les éléments de commande sur toutes les commandes Commerce. Le [!UICONTROL Qty] fournit l’historique des états des éléments de commande. Par exemple, si une commande a été facturée, expédiée et remboursée, vous pouvez voir les transitions d’état.

   ![Historique de l’état de l’élément ordonné Détails de la commande [!DNL Walmart Marketplace] commandes](assets/order-detail-status-history.png)

Pour afficher les détails sur la facture et le remboursement d’un article, sélectionnez [!UICONTROL Invoice] et [!UICONTROL Credit Memo] dans le menu de navigation. Vous pouvez également accéder directement à l’annotation à partir du [[!UICONTROL Returns]](return-refund-orders.md) tableau de bord de la boutique de canaux de vente.



