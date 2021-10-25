---
title: Paramètres de commande
description: Utilisez les paramètres de commande pour déterminer comment les commandes Amazon sont importées et traitées dans votre boutique de commerce.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Paramètres de commande

Les paramètres de commande définissent si et comment les commandes Amazon sont importées et traitées dans [!DNL Commerce] et accessible sur le [tableau de bord de magasin](./amazon-store-dashboard.md).

Les paramètres d’importation de commande sont définis sur `Enabled` par défaut, ce qui signifie que vos commandes Amazon apparaissent sur le tableau de bord de magasin et créent les commandes correspondantes. [!DNL Commerce] ordres. Les commandes importées peuvent être gérées dans le dossier [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}.

>[!NOTE]
>
>Quels que soient vos paramètres de commande, les commandes Amazon qui existaient avant l’intégration de votre magasin ne sont pas importées.

Après [intégration de magasin](./store-integration.md) est terminé, vous pouvez modifier les paramètres de votre commande. Si vous définissez les paramètres de commande sur `Disabled`, les commandes Amazon sont affichées sur le tableau de bord de magasin mais doivent être gérées dans votre [!DNL Amazon Seller Central] compte.

Lorsqu’une commande est créée sur Amazon, elle n’est pas immédiatement importée dans [!DNL Commerce]. Amazon affecte un `Pending` à des commandes nouvellement créées. Une fois que Amazon a vérifié la commande et le mode de paiement, le statut de la commande est remplacé par `Unshipped`. Cette modification d’état déclenche l’importation de commande, et [!DNL Commerce] crée un ordre correspondant.

Les commandes importées d’Amazon peuvent être gérées dans le noeud [!DNL Commerce] [workflow commandes](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}. Voir aussi [Gérer les commandes](./managing-orders.md).

## Configuration des paramètres de commande {#configure-order-settings}

1. Cliquez sur **[!UICONTROL Order Settings]** sur le tableau de bord de la boutique.

1. Pour **[!UICONTROL Import Amazon Orders]** (obligatoire), choisissez une option :

   - `Disabled` - Choisissez quand vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d&#39;Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.

   - `Enabled` - (Par défaut) Choisissez quand vous souhaitez créer le [!DNL Commerce] commandes lorsque de nouvelles commandes sont reçues d&#39;Amazon. [!DNL Commerce] les commandes sont créées en fonction de l&#39;état et des niveaux de stock d&#39;Amazon.

      >[!NOTE]
      >
      >L&#39;option Importer les commandes Amazon doit être définie sur `Enabled` pour gérer les commandes Amazon dans le dossier [!DNL Commerce] [ordres](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}. Lorsque la valeur est définie sur `Disabled`, vos commandes Amazon ne sont pas associées à [!DNL Commerce] numéro de commande et ne peut pas être géré dans [!DNL Commerce]. Vous gérez ces commandes dans votre [!DNL Amazon Seller Central] compte.

1. Pour **[!UICONTROL Import Amazon Orders Into Magento Store]**, choisissez [!DNL Commerce] stocker les commandes Amazon associées lorsque la commande correspondante est créée dans [!DNL Commerce].

   Ce paramètre est défini par défaut sur la vue Store pour le site Web sélectionné lorsque vous [ajout de l&#39;Amazon store](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend de la [!DNL Commerce] les magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Customer Creation]**, choisissez une option :

   - `No Customer Creation (guest)` - (Par défaut) Choisissez lorsque vous ne souhaitez pas créer de compte client dans [!DNL Commerce] en utilisant les données client importées de la commande Amazon. Lorsque cette option est sélectionnée, [!DNL Commerce] traite une commande Amazon importée de la même manière qu&#39;elle traite une extraction d&#39;invité dans [!DNL Commerce].

   - `Build New Customer Account` - Choisissez quand vous souhaitez créer un nouveau compte client dans [!DNL Commerce] en utilisant les données client importées avec la commande Amazon. Cette option vous aide à créer votre base de données client à partir de vos commandes Amazon.

1. Pour **[!UICONTROL Order Number Source]**, choisissez une option :

   - `Build Using Magento Order Number` - (Par défaut) Choisissez quand vous souhaitez créer une [!DNL Commerce] numéro de commande pour la commande Amazon correspondante à l’aide de la [!DNL Commerce] ID de commande affectée par incréments.

   - `Build Using Amazon Order Number` - Choisissez quand vous souhaitez créer le fichier [!DNL Commerce] numéro de commande en utilisant le numéro de commande attribué par Amazon correspondant.
   >[!NOTE]
   >
   >Une fois une commande importée, le numéro de commande Amazon apparaît dans la _[!UICONTROL Recent Orders]_sur le tableau de bord de magasin. Le [!DNL Commerce] Le numéro de commande s’affiche lors de l’affichage des détails de la commande dans le noeud [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Espace de travail {target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Order Status]** (obligatoire), choisissez une option :

   - `Default Order Status` - (Par défaut) Choisissez quand vous souhaitez que les commandes nouvellement créées importées d&#39;Amazon se voient attribuer le statut de commande par défaut défini pour les nouvelles commandes. Le statut par défaut des nouvelles commandes (sauf si vous avez créé un statut de commande personnalisée pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

   - `Custom Order Status` - Choisissez quand vous souhaitez que les commandes nouvellement créées importées d&#39;Amazon se voient attribuer un statut autre que celui par défaut.

   - `Processing Order Status` - Activé lorsque **[!UICONTROL Order Status]** est défini sur `Custom Order Status`. Sélectionnez l’état à utiliser pour les commandes nouvellement créées importées d’Amazon. Les options de ce champ sont basées sur les options d’état par défaut de la section [!DNL Commerce]. Voir [Statut de commande](https://docs.magento.com/user-guide/sales/order-status.html). Vous pouvez également créer un état d’ordre personnalisé à afficher ici pour la sélection. Pour créer un état de commande personnalisé, voir [Statut de commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save order settings]**.

![Paramètres de commande](assets/amazon-order-settings.png)

| Champ | Description |
|---|---|
| [!UICONTROL Import Amazon Orders] | Options :<ul><li>**[!UICONTROL Disabled]** - Choisissez quand vous ne souhaitez pas créer de commandes correspondantes dans [!DNL Commerce] lorsque de nouvelles commandes sont reçues d&#39;Amazon. Lorsque cette option est sélectionnée, tous les autres champs de cette page sont désactivés.</li><li>**[!UICONTROL Enabled]** - (Par défaut) Choisissez quand vous souhaitez créer le [!DNL Commerce] commandes lorsque de nouvelles commandes sont reçues d&#39;Amazon. [!DNL Commerce] les commandes sont créées en fonction de l&#39;état et des niveaux de stock d&#39;Amazon.</li></ul><br><br>`Enabled` doit être choisi pour gérer les commandes Amazon dans [!DNL Commerce]. Lorsque `Disabled` est sélectionné, vos commandes Amazon sont affichées sur le tableau de bord de la boutique, mais les commandes doivent être gérées dans votre [!DNL Amazon Seller Central] compte. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Choisissez [!DNL Commerce] stockez les commandes Amazon associées lorsqu’elles sont créées dans le fichier [!DNL Commerce] [Commandes](https://docs.magento.com/user-guide/sales/orders.html)Espace de travail {target=&quot;_blank&quot;}. Ce paramètre est défini par défaut sur la vue Boutique pour le paramètre [!DNL Commerce] site Web sélectionné lorsque vous [ajout de l&#39;Amazon store](./store-integration.md). Si vous souhaitez modifier ce paramètre, la liste des options dépend de la [!DNL Commerce] les magasins que vous avez configurés dans votre configuration. Voir [Magasins](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Options :<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Par défaut) Choisissez lorsque vous ne souhaitez pas créer de compte client dans [!DNL Commerce] en utilisant les données client importées de la commande Amazon. Lorsque cette option est sélectionnée, elle indique : [!DNL Commerce] pour traiter une commande Amazon importée de la même manière qu&#39;elle traite une extraction d&#39;invité.</li><li>**[!UICONTROL Build New Customer Account]** - Choisissez quand vous souhaitez créer un nouveau compte client dans votre [!DNL Commerce] base de données client utilisant les données client importées avec la commande Amazon. Cette option vous aide à créer votre [!DNL Commerce] base de données client de vos commandes Amazon.</li></ul> |
| Source du numéro de commande | Options :<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Par défaut) Choisissez quand vous souhaitez créer une [!DNL Commerce] numéro de commande pour la commande Amazon correspondante à l’aide de la [!DNL Commerce] ID de commande affectée par incréments. </li><li>**Générer à l’aide du numéro de commande Amazon** - Choisissez quand vous souhaitez créer le fichier [!DNL Commerce] numéro de commande en utilisant le numéro de commande attribué par Amazon correspondant.</li></ul> |
| Commandes en attente | Options :<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Choisissez quand vous ne souhaitez pas que votre [!DNL Commerce] quantité de stock affectée par vos commandes Amazon. Choisissez si vous utilisez Amazon pour votre processus d’exécution (FBA). Lorsque cette option est sélectionnée et que vous recevez une commande Amazon, la quantité commandée n’affecte pas votre [!DNL Commerce] quantité de stock.</li><li>**[!UICONTROL Reserve Quantity]** - Choisissez quand vous souhaitez que la quantité de commande de la commande Amazon soit &quot;réservée&quot; dans votre [!DNL Commerce] quantité de stock. Lorsque vous avez choisi et que vous recevez une commande Amazon, la quantité commandée sera &quot;réservée&quot; dans votre [!DNL Commerce] quantité de stock pour éviter [!DNL Commerce] actions de &quot;vente excessive&quot;. La quantité &quot;réservée&quot; n’est pas disponible à l’achat via votre [!DNL Commerce] vitrine.</li></ul> |
| [!UICONTROL Order Status] | Options :<ul><li>**[!UICONTROL Default Order Status]** - (Par défaut) Choisissez quand vous souhaitez que les commandes nouvellement créées importées d&#39;Amazon se voient attribuer votre statut de commande par défaut pour les nouvelles commandes. Le statut par défaut des nouvelles commandes (sauf si vous avez créé un statut de commande personnalisée pour les nouvelles commandes) est `Pending`. Voir [Commandes de traitement](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Choisissez quand vous souhaitez que les commandes nouvellement créées importées d&#39;Amazon se voient attribuer un statut autre que celui par défaut. Lorsque cette option est sélectionnée, **[!UICONTROL Processing Order Status]** vous permet de choisir l’état que vous souhaitez utiliser pour les commandes nouvellement créées importées d’Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Activé lorsque _[!UICONTROL Order Status]_est défini sur `Custom Order Status`. Sélectionnez le statut de commande que vous souhaitez affecter aux nouvelles commandes. Les options de ce champ dépendent des options d’état par défaut de la section [!DNL Commerce]. Voir [Statut de commande](https://docs.magento.com/user-guide/sales/order-status.html){target=&quot;_blank&quot;}. Vous pouvez également créer un état de commande personnalisé à afficher ici. Pour créer un état de commande personnalisé, voir [Statut de commande personnalisée](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}. |

## [!DNL Commerce] création de commande

[!DNL Commerce] les commandes sont créées pour les commandes Amazon en fonction du statut et des conditions de stock suivants.

### Création de commande avec gestion du stock

>[!NOTE]
>
>Prise en charge dans les intégrations Adobe Commerce et Magento Open Source 2.3.x uniquement.

| Canal d’exécution | [!DNL Commerce] Statut du stock | Statut des commandes Amazon | [!UICONTROL Create Magento Order] Paramètre | Stock réservé |
|---|---|---|---|---|
| FBA | En stock<br>Hors stock<br>Ne pas gérer | En attente | Non | Non |
| FBA | En stock<br>Hors stock<br>Ne pas gérer | Disponibilité en attente | Non | Non |
| FBA | En stock<br>Hors stock<br>Ne pas gérer | Annulé | Non | Non |
| FBA | En stock<br>Hors stock<br>Ne pas gérer | Erreur | Non | Non |
| FBA | En stock<br>Hors stock<br>Ne pas gérer | Non expédié | Non | Non |
| FBA | En stock<br>Hors stock<br>Ne pas gérer | PartiellementExpédié | Non | Non |
| FBA | En stock<br>Ne pas gérer | Expédié | Oui | Non |
| FBA | Hors stock | Expédié | Non | Non |
| FBM | En stock<br>Hors stock<br>Ne pas gérer | En attente | Non | Non |
| FBM | En stock<br>Hors stock<br>Ne pas gérer | Disponibilité en attente | Non | Non |
| FBM | En stock<br>Hors stock<br>Ne pas gérer | Annulé | Non | Non |
| FBM | En stock<br>Hors stock<br>Ne pas gérer | Erreur | Non | Non |
| FBM | En stock<br>Ne pas gérer | Non expédié | Oui | Oui |
| FBM | Hors stock | Non expédié | Non | Non |
| FBM | En stock<br>Ne pas gérer | PartiellementExpédié | Oui | Oui |
| FBM | Hors stock | PartiellementExpédié | Non | Non |
| FBM | En stock<br>Ne pas gérer | Expédié | Oui | Oui |
| FBM | Hors stock | Expédié | Non | Non |

>[!NOTE]
>Si une commande Amazon est importée dans un `Partially Shipped` ou `Shipped` statut, la réservation de stock qui est créée concerne tous les articles de la commande. Le canal de vente Amazon ne compense pas les articles qui ont déjà été expédiés.
>
>Si une commande est exécutée par Amazon (FBA) mais qu&#39;un élément est dans `out of stock` statut, [!DNL Commerce] ne peut pas créer une commande correspondante. Il s&#39;agit d&#39;une limitation des intégrations de gestion des stocks.
