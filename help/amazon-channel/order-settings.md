---
title: Paramètres de commande Amazon
description: Utilisez les paramètres de commande pour déterminer comment les commandes Amazon sont importées et traitées dans votre boutique Commerce.
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Paramètres de commande Amazon

Les paramètres de commande définissent si et comment les commandes Amazon sont importées et traitées dans [!DNL Commerce] et sont accessibles sur le [tableau de bord du magasin](./amazon-store-dashboard.md).

Les paramètres d’importation de commande sont définis sur `Enabled` par défaut, ce qui signifie que vos commandes Amazon apparaissent dans le tableau de bord du magasin et créent les commandes [!DNL Commerce] correspondantes. Les commandes importées peuvent être gérées dans le workflow [!DNL Commerce] [Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Quels que soient vos paramètres de commande, les commandes Amazon qui existaient avant l’intégration de votre magasin ne sont pas importées.

Une fois l’ [intégration de magasin](./store-integration.md) terminée, vous pouvez modifier les paramètres de commande. Si vous définissez vos paramètres de commande sur `Disabled`, les commandes Amazon s’affichent dans le tableau de bord du magasin, mais doivent être gérées dans votre compte [!DNL Amazon Seller Central].

Lorsqu’une commande est créée sur Amazon, elle n’est pas immédiatement importée dans [!DNL Commerce]. Amazon attribue un état `Pending` aux commandes nouvellement créées. Une fois que Amazon a vérifié la commande et le mode de paiement, l’état de la commande est remplacé par `Unshipped`. Ce changement d’état déclenche l’importation de la commande et [!DNL Commerce] crée une commande correspondante.

Les commandes importées depuis Amazon peuvent être gérées dans le [!DNL Commerce] [workflow des commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Voir aussi [Gestion des commandes](./managing-orders.md).

## Configuration des paramètres de commande {#configure-order-settings}

1. Cliquez sur **[!UICONTROL Order Settings]** dans le tableau de bord du magasin.

1. Pour **[!UICONTROL Import Amazon Orders]** (obligatoire), choisissez une option :

   - `Disabled` - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.

   - `Enabled` - (Par défaut) Choisissez quand vous souhaitez créer les [!DNL Commerce] commandes correspondantes lorsque de nouvelles commandes sont reçues d’Amazon. [!DNL Commerce] Les commandes sont créées en fonction de l’état et des niveaux de stock d’Amazon.

     >[!NOTE]
     >
     >L’option Importer les commandes Amazon doit être définie sur `Enabled` pour gérer les commandes Amazon dans le workflow [!DNL Commerce] [commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) . Lorsque la valeur est définie sur `Disabled`, vos commandes Amazon n’ont pas de numéro de commande [!DNL Commerce] correspondant et ne peuvent pas être gérées dans [!DNL Commerce]. Vous gérez ces commandes dans votre compte [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Import Amazon Orders Into Magento Store]**, choisissez à quel [!DNL Commerce] magasin les commandes Amazon sont associées lorsque la commande correspondante est créée dans [!DNL Commerce].

   Ce paramètre est défini par défaut sur la vue de magasin pour le site web sélectionné lorsque vous [ avez ajouté la boutique Amazon](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend des [!DNL Commerce] magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Pour **[!UICONTROL Customer Creation]**, choisissez une option :

   - `No Customer Creation (guest)` - (Par défaut) Sélectionnez cette option lorsque vous ne souhaitez pas créer de compte client dans [!DNL Commerce] à l’aide des données client importées de la commande Amazon. Lorsque cette option est sélectionnée, [!DNL Commerce] traite une commande Amazon importée de la même manière qu’il traite un passage en caisse invité dans [!DNL Commerce].

   - `Build New Customer Account` - Choisissez quand vous souhaitez créer un nouveau compte client dans [!DNL Commerce] en utilisant les données client importées avec la commande Amazon. Cette option vous aide à créer votre base de données client à partir de vos commandes Amazon.

1. Pour **[!UICONTROL Order Number Source]**, choisissez une option :

   - `Build Using Magento Order Number` - (Par défaut) Choisissez le moment où vous souhaitez créer un numéro de commande [!DNL Commerce] unique pour la commande Amazon correspondante à l’aide de l’ [!DNL Commerce] ID de commande attribué de manière incrémentielle.

   - `Build Using Amazon Order Number` - Choisissez le moment où vous souhaitez créer le numéro de commande [!DNL Commerce] à l’aide du numéro de commande attribué par Amazon correspondant.

   >[!NOTE]
   >
   >Une fois une commande importée, le numéro de commande Amazon apparaît dans la liste _[!UICONTROL Recent Orders]_du tableau de bord du magasin. Le numéro de commande [!DNL Commerce] s’affiche lorsque vous affichez les détails de la commande dans l’espace de travail [!DNL Commerce] [Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) .

1. Pour **[!UICONTROL Order Status]** (obligatoire), choisissez une option :

   - `Default Order Status` - (Par défaut) Choisissez quand vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer l’état de commande par défaut défini pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut.

   - `Processing Order Status` - Activé lorsque **[!UICONTROL Order Status]** est défini sur `Custom Order Status`. Sélectionnez l&#39;état que vous souhaitez utiliser pour les commandes nouvellement créées importées depuis Amazon. Les options de ce champ sont basées sur les options d’état par défaut de [!DNL Commerce]. Voir [État de la commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Vous pouvez également créer un état de commande personnalisé qui s’affichera ici pour sélection. Pour créer un état de commande personnalisé, voir [État de commande personnalisée](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save order settings]**.

![Paramètres de commande](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Champ | Description |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | Options :<ul><li>**[!UICONTROL Disabled]** - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.</li><li>**[!UICONTROL Enabled]** - (Par défaut) Choisissez quand vous souhaitez créer les [!DNL Commerce] commandes correspondantes lorsque de nouvelles commandes sont reçues d’Amazon. [!DNL Commerce] Les commandes sont créées en fonction de l’état et des niveaux de stock d’Amazon.</li></ul><br><br>`Enabled` doit être choisi pour gérer les commandes Amazon dans [!DNL Commerce]. Lorsque `Disabled` est sélectionné, vos commandes Amazon sont affichées dans le tableau de bord du magasin, mais les commandes doivent être gérées dans votre compte [!DNL Amazon Seller Central]. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Sélectionnez le [!DNL Commerce] magasin auquel les commandes Amazon sont associées lors de leur création dans l&#39;espace de travail [!DNL Commerce] [Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) . Ce paramètre est défini par défaut sur la vue du magasin pour le site web [!DNL Commerce] sélectionné lorsque vous [ avez ](./store-integration.md) ajouté le magasin Amazon. Si vous souhaitez modifier ce paramètre, la liste des options dépend des [!DNL Commerce] magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Options :<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Par défaut) Sélectionnez cette option lorsque vous ne souhaitez pas créer de compte client dans [!DNL Commerce] à l’aide des données client importées de la commande Amazon. Lorsqu&#39;elle est sélectionnée, cette option indique à [!DNL Commerce] de traiter une commande Amazon importée de la même manière qu&#39;elle traite un passage en caisse invité.</li><li>**[!UICONTROL Build New Customer Account]** - Choisissez quand vous souhaitez créer un nouveau compte client dans votre base de données client [!DNL Commerce] à l’aide des données client importées avec la commande Amazon. Cette option permet de créer votre base de données client [!DNL Commerce] à partir de vos commandes Amazon.</li></ul> |
| Source du numéro de commande | Options :<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Par défaut) Choisissez le moment où vous souhaitez créer un numéro de commande [!DNL Commerce] unique pour la commande Amazon correspondante à l’aide de l’ [!DNL Commerce] ID de commande attribué de manière incrémentielle. </li><li>**Créer à l’aide du numéro de commande Amazon** - Choisissez le moment où vous souhaitez créer le numéro de commande [!DNL Commerce] à l’aide du numéro de commande attribué par Amazon correspondant.</li></ul> |
| Commandes en attente | Options :<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Choisissez le moment où vous ne souhaitez pas que votre quantité de stock [!DNL Commerce] soit affectée par vos commandes Amazon. Choisissez si vous utilisez Amazon pour votre processus d’exécution (FBA). Une fois choisie et que vous recevez une commande Amazon, la quantité commandée n’a aucune incidence sur la quantité de votre stock [!DNL Commerce].</li><li>**[!UICONTROL Reserve Quantity]** - Choisissez quand vous souhaitez que la quantité de commande dans la commande Amazon soit &quot;réservée&quot; dans la quantité de votre stock [!DNL Commerce]. Une fois choisie et que vous recevez une commande Amazon, la quantité commandée &quot;réserve&quot; dans la quantité de votre stock [!DNL Commerce] afin d’empêcher votre stock [!DNL Commerce] de &quot;survendre&quot;. La quantité &quot;réservée&quot; n’est pas disponible à l’achat via votre vitrine [!DNL Commerce].</li></ul> |
| [!UICONTROL Order Status] | Options :<ul><li>**[!UICONTROL Default Order Status]** - (Par défaut) Choisissez quand vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer votre statut de commande par défaut pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** - Choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut. Lorsque cette option est sélectionnée, **[!UICONTROL Processing Order Status]** vous permet de choisir l’état que vous souhaitez utiliser pour les commandes nouvellement créées importées d’Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Activé lorsque _[!UICONTROL Order Status]_est défini sur `Custom Order Status`. Sélectionnez l&#39;état de la commande à affecter aux nouvelles commandes. Les options de ce champ dépendent des options d’état par défaut dans [!DNL Commerce]. Voir [État de la commande](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Vous pouvez également créer un état de commande personnalisé à afficher ici. Pour créer un état de commande personnalisé, voir [État de commande personnalisée] |

## [!DNL Commerce] création de commande

[!DNL Commerce] commandes sont créées pour les commandes Amazon en fonction de l’état et des conditions de stock suivants.

### Création de commande avec Inventory management

>[!NOTE]
>
>Pris en charge uniquement dans les intégrations Adobe Commerce et Magento Open Source 2.3.x.

| Canal d’exécution | [!DNL Commerce] État du stock | État de la commande Amazon | Paramètre [!UICONTROL Create Magento Order] | Inventaire réservé |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | En attente | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | En attente de disponibilité | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Annulé | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Erreur | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | Non expédié | Non | Non |
| FBA | En stock<br>En rupture de stock<br>Ne pas gérer | PartiallyShipped | Non | Non |
| FBA | En stock <br>Ne pas gérer | Expédié | Oui | Non |
| FBA | En rupture de stock | Expédié | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | En attente | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | En attente de disponibilité | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | Annulé | Non | Non |
| FBM | En stock<br>En rupture de stock<br>Ne pas gérer | Erreur | Non | Non |
| FBM | En stock <br>Ne pas gérer | Non expédié | Oui | Oui |
| FBM | En rupture de stock | Non expédié | Non | Non |
| FBM | En stock <br>Ne pas gérer | PartiallyShipped | Oui | Oui |
| FBM | En rupture de stock | PartiallyShipped | Non | Non |
| FBM | En stock <br>Ne pas gérer | Expédié | Oui | Oui |
| FBM | En rupture de stock | Expédié | Non | Non |

>[!NOTE]
>Si une commande Amazon est importée avec un état `Partially Shipped` ou `Shipped`, la réservation d’inventaire créée concerne tous les articles de la commande. Le canal de vente Amazon ne compense pas les articles qui ont déjà été livrés.
>
>Si une commande est exécutée par Amazon (FBA) mais qu’un élément est à l’état `out of stock`, [!DNL Commerce] ne peut pas créer une commande correspondante. Il s’agit d’une limitation des intégrations Inventory management.
