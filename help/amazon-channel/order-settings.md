---
title: Paramètres de commande
description: Utilisez les paramètres Commande pour déterminer comment les commandes Amazon sont importées et traitées dans votre boutique de commerce.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Paramètres de commande

Les paramètres de commande définissent si et comment les commandes Amazon sont importées et traitées dans [!DNL Commerce] et sont accessibles sur le [tableau de bord de la boutique](./amazon-store-dashboard.md).

Les paramètres d’importation de commande sont définis sur `Enabled` par défaut, ce qui signifie que vos commandes Amazon apparaissent dans le tableau de bord du magasin et créent les commandes [!DNL Commerce] correspondantes. Les commandes importées peuvent être gérées dans le workflow [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Quels que soient vos paramètres de commande, les commandes Amazon qui existaient avant l’intégration de votre magasin ne sont pas importées.

Une fois l’[intégration de magasin](./store-integration.md) terminée, vous pouvez modifier les paramètres de commande. Si vous définissez vos paramètres de commande sur `Disabled`, les commandes Amazon s’affichent dans le tableau de bord de la boutique, mais doivent être gérées dans votre compte [!DNL Amazon Seller Central].

Lorsqu’une commande est créée sur Amazon, elle n’est pas immédiatement importée dans [!DNL Commerce]. Amazon attribue un état `Pending` aux commandes nouvellement créées. Une fois qu’Amazon a vérifié le mode de commande et de paiement, l’état de la commande passe à `Unshipped`. Ce changement d’état déclenche l’importation de la commande et [!DNL Commerce] crée une commande correspondante.

Les commandes importées depuis Amazon peuvent être gérées dans le [!DNL Commerce] [workflow des commandes](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Voir aussi [Gestion des commandes](./managing-orders.md).

## Configuration des paramètres de commande {#configure-order-settings}

1. Cliquez sur **[!UICONTROL Order Settings]** dans le tableau de bord du magasin.

1. Pour **[!UICONTROL Import Amazon Orders]** (obligatoire), choisissez une option :

   - `Disabled` - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes  [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.

   - `Enabled` - (Par défaut) Choisissez le moment où vous souhaitez créer les  [!DNL Commerce] commandes correspondantes lors de la réception de nouvelles commandes depuis Amazon. [!DNL Commerce] les commandes sont créées en fonction du statut et des niveaux de stock d&#39;Amazon.

      >[!NOTE]
      >
      >L’option Importer les commandes Amazon doit être définie sur `Enabled` pour gérer les commandes Amazon dans le workflow [!DNL Commerce] [commandes](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Lorsqu’elle est définie sur `Disabled`, vos commandes Amazon n’ont pas de [!DNL Commerce] numéro de commande correspondant et ne peuvent pas être gérées dans [!DNL Commerce]. Vous gérez ces commandes dans votre compte [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Import Amazon Orders Into Magento Store]**, choisissez à quel [!DNL Commerce] magasin les commandes Amazon sont associées lorsque la commande correspondante est créée dans [!DNL Commerce].

   Ce paramètre est défini par défaut sur la vue de la boutique pour le site web sélectionné lorsque vous avez [ajouté la boutique Amazon](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend des [!DNL Commerce] magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Customer Creation]**, choisissez une option :

   - `No Customer Creation (guest)` - (Par défaut) Sélectionnez cette option lorsque vous ne souhaitez pas créer de compte client lors de l’ [!DNL Commerce] utilisation des données client importées à partir de la commande Amazon. Une fois sélectionné, [!DNL Commerce] traite une commande Amazon importée de la même manière qu’il traite un passage en caisse invité dans [!DNL Commerce].

   - `Build New Customer Account` - Choisissez quand vous souhaitez créer un nouveau compte client en  [!DNL Commerce] utilisant les données client importées avec la commande Amazon. Cette option vous aide à créer votre base de données client à partir de vos commandes Amazon.

1. Pour **[!UICONTROL Order Number Source]**, choisissez une option :

   - `Build Using Magento Order Number` - (Par défaut) Choisissez le moment où vous souhaitez créer un numéro de  [!DNL Commerce] commande unique pour la commande Amazon correspondante à l’aide de l’ID de commande  [!DNL Commerce] attribué par incréments.

   - `Build Using Amazon Order Number` - Choisissez le moment où vous souhaitez créer le numéro de  [!DNL Commerce] commande à l’aide du numéro de commande attribué par Amazon correspondant.
   >[!NOTE]
   >
   >Une fois une commande importée, le numéro de commande Amazon apparaît dans la liste _[!UICONTROL Recent Orders]_du tableau de bord du magasin. Le [!DNL Commerce] numéro de commande s’affiche lors de l’affichage des détails de la commande dans l’espace de travail [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Order Status]** (obligatoire), choisissez une option :

   - `Default Order Status` - (Par défaut) Choisissez le moment où vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer le statut de commande par défaut défini pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}.

   - `Custom Order Status` - Choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut.

   - `Processing Order Status` - Activé lorsque  **[!UICONTROL Order Status]** est défini sur  `Custom Order Status`. Sélectionnez l&#39;état que vous souhaitez utiliser pour les commandes nouvellement créées importées depuis Amazon. Les options de ce champ sont basées sur les options d’état par défaut dans [!DNL Commerce]. Voir [État de la commande](https://docs.magento.com/user-guide/sales/order-status.html). Vous pouvez également créer un état de commande personnalisé qui s’affichera ici pour sélection. Pour créer un état de commande personnalisé, voir [État de commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save order settings]**.

![Paramètres de commande](assets/amazon-order-settings.png)

| Champ | Description |
|---|---|
| [!UICONTROL Import Amazon Orders] | Options :<ul><li>**[!UICONTROL Disabled]** - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes  [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.</li><li>**[!UICONTROL Enabled]** - (Par défaut) Choisissez le moment où vous souhaitez créer les  [!DNL Commerce] commandes correspondantes lors de la réception de nouvelles commandes depuis Amazon. [!DNL Commerce] les commandes sont créées en fonction du statut et des niveaux de stock d&#39;Amazon.</li></ul><br><br>`Enabled` doit être choisi pour gérer les commandes Amazon dans  [!DNL Commerce]. Lorsque `Disabled` est sélectionné, les commandes Amazon s’affichent dans le tableau de bord de la boutique, mais les commandes doivent être gérées dans votre compte [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Sélectionnez le [!DNL Commerce] magasin auquel les commandes Amazon sont associées lors de leur création dans l&#39;espace de travail [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Ce paramètre utilise par défaut la vue de la boutique pour le site web [!DNL Commerce] sélectionné lorsque vous [avez ajouté la boutique Amazon](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend des [!DNL Commerce] magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Options :<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Par défaut) Sélectionnez cette option lorsque vous ne souhaitez pas créer de compte client lors de l’ [!DNL Commerce] utilisation des données client importées à partir de la commande Amazon. Lorsqu’elle est sélectionnée, cette option indique à [!DNL Commerce] de traiter une commande Amazon importée de la même manière qu’elle traite un passage en caisse invité.</li><li>**[!UICONTROL Build New Customer Account]** - Choisissez quand vous souhaitez créer un nouveau compte client dans votre base de données de  [!DNL Commerce] clients à l’aide des données client importées avec la commande Amazon. Cette option permet de créer votre [!DNL Commerce] base de données client à partir de vos commandes Amazon.</li></ul> |
| Source du numéro de commande | Options :<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Par défaut) Choisissez le moment où vous souhaitez créer un numéro de  [!DNL Commerce] commande unique pour la commande Amazon correspondante à l’aide de l’ID de commande  [!DNL Commerce] attribué par incréments. </li><li>**Créer à l’aide d’un numéro de commande Amazon**  : choisissez le moment où vous souhaitez créer le numéro de  [!DNL Commerce] commande à l’aide du numéro de commande attribué par Amazon correspondant.</li></ul> |
| Commandes en attente | Options :<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Sélectionnez cette option lorsque vous ne souhaitez pas que la quantité de votre  [!DNL Commerce] stock soit affectée par vos commandes Amazon. Choisissez si vous utilisez Amazon pour votre processus d’exécution (FBA). Lorsque vous choisissez cette option et que vous recevez une commande Amazon, la quantité commandée n’a aucune incidence sur la [!DNL Commerce] quantité de stock.</li><li>**[!UICONTROL Reserve Quantity]** - Choisissez quand vous souhaitez que la quantité de la commande dans Amazon soit &quot;réservée&quot; dans la quantité de votre  [!DNL Commerce] stock. Une fois choisie et que vous recevez une commande Amazon, la quantité commandée &quot;réserve&quot; dans la quantité de votre stock [!DNL Commerce] afin d’empêcher votre stock [!DNL Commerce] de &quot;sur-vendre&quot;. La quantité &quot;réservée&quot; n’est pas disponible à l’achat via votre vitrine [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Options :<ul><li>**[!UICONTROL Default Order Status]** - (Par défaut) Choisissez le moment où vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer votre statut de commande par défaut pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** : choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut. Une fois sélectionné, **[!UICONTROL Processing Order Status]** vous permet de choisir l’état que vous souhaitez utiliser pour les commandes nouvellement créées importées depuis Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Activé lorsque _[!UICONTROL Order Status]_est défini sur `Custom Order Status`. Sélectionnez l&#39;état de la commande à affecter aux nouvelles commandes. Les options de ce champ dépendent des options d’état par défaut dans [!DNL Commerce]. Voir [État de la commande](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}. Vous pouvez également créer un état de commande personnalisé à afficher ici. Pour créer un état de commande personnalisé, voir [État de commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}. |

## [!DNL Commerce] création de commande

[!DNL Commerce] les commandes sont créées pour les commandes Amazon en fonction de l’état et des conditions de stock ci-après.

### Création de commandes avec gestion du stock

>[!NOTE]
>
>Pris en charge uniquement dans les intégrations Adobe Commerce et Magento Open Source 2.3.x.

| Canal d’exécution | [!DNL Commerce] État du stock | État de la commande Amazon | [!UICONTROL Create Magento Order] Paramètre | Inventaire réservé |
|---|---|---|---|---|
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | En attente | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | En attente de disponibilité | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Annulé | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Erreur | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Non expédié | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | PartiallyShipped | Non | Non |
| FBA | En stock<br>Ne pas gérer | Expédié | Oui | Non |
| FBA | En rupture de stock | Expédié | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | En attente | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | En attente de disponibilité | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | Annulé | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | Erreur | Non | Non |
| FBM | En stock<br>Ne pas gérer | Non expédié | Oui | Oui |
| FBM | En rupture de stock | Non expédié | Non | Non |
| FBM | En stock<br>Ne pas gérer | PartiallyShipped | Oui | Oui |
| FBM | En rupture de stock | PartiallyShipped | Non | Non |
| FBM | En stock<br>Ne pas gérer | Expédié | Oui | Oui |
| FBM | En rupture de stock | Expédié | Non | Non |

>[!NOTE]
>Si une commande Amazon est importée dans un état `Partially Shipped` ou `Shipped`, la réservation d’inventaire créée est celle de tous les articles de la commande. Le canal de vente Amazon ne compense pas les articles qui ont déjà été livrés.
>
>Si une commande est exécutée par Amazon (FBA) mais qu’un élément est à l’état `out of stock` , [!DNL Commerce] ne peut pas créer une commande correspondante. Il s’agit d’une limitation des intégrations de gestion du stock.
