---
title: Paramètres de commande
description: Utilisez les paramètres Commande pour déterminer comment les commandes Amazon sont importées et traitées dans votre boutique de commerce.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Paramètres de commande

Les paramètres de commande définissent si et comment les commandes Amazon sont importées et traitées dans [!DNL Commerce] et sont accessibles sur la page [tableau de bord de la boutique](./amazon-store-dashboard.md).

Les paramètres d’importation de commande sont définis sur `Enabled` par défaut, ce qui signifie que vos commandes Amazon apparaissent dans le tableau de bord de la boutique et créent les commandes correspondantes. [!DNL Commerce] commandes. Les commandes importées peuvent être gérées dans le [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}.

>[!NOTE]
>
>Quels que soient vos paramètres de commande, les commandes Amazon qui existaient avant l’intégration de votre magasin ne sont pas importées.

Après [intégration de magasin](./store-integration.md) est terminée, vous pouvez modifier les paramètres de commande. Si vous définissez vos paramètres de commande sur `Disabled`, les commandes Amazon s’affichent dans le tableau de bord du magasin, mais doivent être gérées dans votre [!DNL Amazon Seller Central] compte .

Lorsqu’une commande est créée sur Amazon, elle n’est pas immédiatement importée dans [!DNL Commerce]. Amazon affecte une `Pending` état des commandes nouvellement créées. Une fois que Amazon a vérifié la commande et le mode de paiement, l’état de la commande est remplacé par `Unshipped`. Ce changement d’état déclenche l’importation de la commande, et [!DNL Commerce] crée une correspondance, dans l’ordre correspondant.

Les commandes importées depuis Amazon peuvent être gérées dans la variable [!DNL Commerce] [workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}. Voir aussi [Gestion des commandes](./managing-orders.md).

## Configuration des paramètres de commande {#configure-order-settings}

1. Cliquez sur **[!UICONTROL Order Settings]** dans le tableau de bord de la boutique.

1. Pour **[!UICONTROL Import Amazon Orders]** (obligatoire), sélectionnez une option :

   - `Disabled` - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.

   - `Enabled` - (Par défaut) Choisissez le moment où vous souhaitez créer la [!DNL Commerce] commandes lorsque de nouvelles commandes sont reçues d’Amazon. [!DNL Commerce] les commandes sont créées en fonction du statut et des niveaux de stock d&#39;Amazon.

      >[!NOTE]
      >
      >L’option Importer les commandes Amazon doit être définie sur `Enabled` pour gérer les commandes Amazon dans le [!DNL Commerce] [commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}. Lorsque la variable est définie sur `Disabled`, vos commandes Amazon ne comportent pas de [!DNL Commerce] numéro de commande et ne peuvent pas être gérés dans [!DNL Commerce]. Vous gérez ces commandes dans votre [!DNL Amazon Seller Central] compte .

1. Pour **[!UICONTROL Import Amazon Orders Into Magento Store]**, choisissez laquelle [!DNL Commerce] stocker les commandes Amazon associées lors de la création de la commande correspondante dans [!DNL Commerce].

   Ce paramètre affiche par défaut la vue de la boutique pour le site web sélectionné lorsque vous [ajout de la boutique Amazon](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend de la variable [!DNL Commerce] les magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Customer Creation]**, choisissez une option :

   - `No Customer Creation (guest)` - (Par défaut) Choisissez les cas où vous ne souhaitez pas créer de compte client dans [!DNL Commerce] en utilisant les données client importées de la commande Amazon. Lorsqu’elle est choisie, [!DNL Commerce] traite une commande Amazon importée de la même manière qu’elle traite un passage en caisse invité dans [!DNL Commerce].

   - `Build New Customer Account` - Choisissez quand vous souhaitez créer un nouveau compte client dans [!DNL Commerce] en utilisant les données client importées avec la commande Amazon. Cette option vous aide à créer votre base de données client à partir de vos commandes Amazon.

1. Pour **[!UICONTROL Order Number Source]**, choisissez une option :

   - `Build Using Magento Order Number` - (Par défaut) Choisissez le moment où vous souhaitez créer une variable [!DNL Commerce] Numéro de commande de la commande Amazon correspondante à l’aide de la variable [!DNL Commerce] ID de commande attribué de manière incrémentielle.

   - `Build Using Amazon Order Number` - Choisissez quand vous souhaitez créer la variable [!DNL Commerce] numéro de commande à l’aide du numéro de commande attribué par Amazon correspondant.
   >[!NOTE]
   >
   >Une fois une commande importée, le numéro de la commande Amazon apparaît dans la variable _[!UICONTROL Recent Orders]_dans le tableau de bord de la boutique. Le [!DNL Commerce] Le numéro de commande s’affiche lorsque vous affichez les détails de la commande dans la variable [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Espace de travail {target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Order Status]** (obligatoire), sélectionnez une option :

   - `Default Order Status` - (Par défaut) Choisissez le moment où vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer le statut de commande par défaut défini pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

   - `Custom Order Status` - Choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut.

   - `Processing Order Status` - Activé lorsque **[!UICONTROL Order Status]** est défini sur `Custom Order Status`. Sélectionnez l&#39;état que vous souhaitez utiliser pour les commandes nouvellement créées importées depuis Amazon. Les options de ce champ sont basées sur les options d’état par défaut de la section [!DNL Commerce]. Voir [État de la commande](https://docs.magento.com/user-guide/sales/order-status.html). Vous pouvez également créer un état de commande personnalisé qui s’affichera ici pour sélection. Pour créer un état de commande personnalisé, reportez-vous à la section [Statut de la commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save order settings]**.

![Paramètres de commande](assets/amazon-order-settings.png)

| Champ | Description |
|---|---|
| [!UICONTROL Import Amazon Orders] | Options :<ul><li>**[!UICONTROL Disabled]** - Sélectionnez cette option lorsque vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d’Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.</li><li>**[!UICONTROL Enabled]** - (Par défaut) Choisissez le moment où vous souhaitez créer la [!DNL Commerce] commandes lorsque de nouvelles commandes sont reçues d’Amazon. [!DNL Commerce] les commandes sont créées en fonction du statut et des niveaux de stock d&#39;Amazon.</li></ul><br><br>`Enabled` doit être choisi pour gérer les commandes Amazon dans [!DNL Commerce]. When `Disabled` est sélectionné, vos commandes Amazon s’affichent dans le tableau de bord du magasin, mais les commandes doivent être gérées dans votre [!DNL Amazon Seller Central] compte . |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Choisissez laquelle [!DNL Commerce] stocker les commandes Amazon auxquelles elles sont associées lors de leur création dans la variable [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Espace de travail {target=&quot;_blank&quot;}. Ce paramètre est défini par défaut sur le mode Boutique pour la variable [!DNL Commerce] site web sélectionné [ajout de la boutique Amazon](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend de la variable [!DNL Commerce] les magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Options :<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Par défaut) Choisissez les cas où vous ne souhaitez pas créer de compte client dans [!DNL Commerce] en utilisant les données client importées de la commande Amazon. Lorsque cette option est sélectionnée, elle indique : [!DNL Commerce] pour traiter une commande Amazon importée de la même manière qu’elle traite un passage en caisse invité.</li><li>**[!UICONTROL Build New Customer Account]** - Choisissez quand vous souhaitez créer un nouveau compte client dans votre [!DNL Commerce] base de données client à l’aide des données client importées avec la commande Amazon. Cette option vous aide à créer votre [!DNL Commerce] base de données client de vos commandes Amazon.</li></ul> |
| Source du numéro de commande | Options :<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Par défaut) Choisissez le moment où vous souhaitez créer une variable [!DNL Commerce] Numéro de commande de la commande Amazon correspondante à l’aide de la variable [!DNL Commerce] ID de commande attribué de manière incrémentielle. </li><li>**Créer à l’aide du numéro de commande Amazon** - Choisissez quand vous souhaitez créer la variable [!DNL Commerce] numéro de commande à l’aide du numéro de commande attribué par Amazon correspondant.</li></ul> |
| Commandes en attente | Options :<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Choisissez quand vous ne souhaitez pas que votre [!DNL Commerce] quantité de stock affectée par vos commandes Amazon. Choisissez si vous utilisez Amazon pour votre processus d’exécution (FBA). Lorsque vous choisissez de recevoir une commande Amazon, la quantité commandée n’a aucune incidence sur votre [!DNL Commerce] quantité en stock.</li><li>**[!UICONTROL Reserve Quantity]** - Choisissez quand vous souhaitez que la quantité de commande dans Amazon soit &quot;réservée&quot; dans votre [!DNL Commerce] quantité en stock. Lorsque vous choisissez cette option et que vous recevez une commande Amazon, la quantité commandée &quot;réserve&quot; dans votre [!DNL Commerce] quantité de stock pour empêcher votre [!DNL Commerce] stock de &quot;vente excessive&quot;. La quantité &quot;réservée&quot; n’est pas disponible à l’achat via votre [!DNL Commerce] storefront.</li></ul> |
| [!UICONTROL Order Status] | Options :<ul><li>**[!UICONTROL Default Order Status]** - (Par défaut) Choisissez le moment où vous souhaitez que les commandes nouvellement créées importées d’Amazon se voient attribuer votre statut de commande par défaut pour les nouvelles commandes. L’état par défaut des nouvelles commandes (sauf si vous avez créé un état de commande personnalisé pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Choisissez quand vous souhaitez que les commandes nouvellement créées importées depuis Amazon se voient attribuer un statut autre que celui par défaut. Lorsqu’elle est choisie, **[!UICONTROL Processing Order Status]** vous permet de choisir l’état que vous souhaitez utiliser pour les commandes nouvellement créées importées depuis Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Activé lorsque _[!UICONTROL Order Status]_est défini sur `Custom Order Status`. Sélectionnez l&#39;état de la commande à affecter aux nouvelles commandes. Les options de ce champ dépendent des options d’état par défaut de la section [!DNL Commerce]. Voir [État de la commande](https://docs.magento.com/user-guide/sales/order-status.html){target=&quot;_blank&quot;}. Vous pouvez également créer un état de commande personnalisé à afficher ici. Pour créer un état de commande personnalisé, reportez-vous à la section [Statut de la commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}. |

## [!DNL Commerce] création de commande

[!DNL Commerce] les commandes sont créées pour les commandes Amazon en fonction de l’état et des conditions de stock ci-après.

### Création de commande avec Inventory management

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
>Si une commande Amazon est importée dans un `Partially Shipped` ou `Shipped` , la réservation d’inventaire créée est destinée à tous les articles de la commande. Le canal de vente Amazon ne compense pas les articles qui ont déjà été livrés.
>
>Si une commande est effectuée par Amazon (FBA) mais qu’un élément figure dans la variable `out of stock` status, [!DNL Commerce] ne peut pas créer un ordre correspondant. Il s’agit d’une limitation des intégrations Inventory management.
