---
title: Vue Magasins Amazon
description: Accédez à la vue Amazon Stores (Magasins) pour passer rapidement en revue les statistiques de base de chacun de vos magasins Amazon et les options de gestion des accès.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Vue Magasins Amazon

Lors de l’affichage de la page d’accueil du canal de vente Amazon, la vue _Amazon Stores_ s’ouvre par défaut.

![Vue Magasins Amazon](assets/amazon-sales-channel-home-tabs.png)

La vue _[!UICONTROL Amazon Stores]_affiche une &quot;carte de magasin&quot; pour chacun de vos magasins Amazon, ainsi que certaines options de statistiques et de gestion de base. Les informations récapitulatives affichées dans chaque carte incluent l’état du magasin, la date de création, la date de la dernière mise à jour, les listes qui nécessitent votre attention (par exemple : Listes incomplètes) et le site Web [!DNL Commerce] affecté.

Lors de l’affichage de la vue _[!UICONTROL Amazon Store]_, chaque carte de magasin vous permet d’effectuer les opérations suivantes :

- Pour ouvrir un tableau de bord [de magasin](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.

- Pour modifier l’état d’un magasin ou supprimer un magasin, cliquez sur **[!UICONTROL Action]** et choisissez :

   - **[!UICONTROL Activate]** /  **[!UICONTROL Deactivate]**  - Choisissez de remplacer le statut du magasin par  `Active` ou  `Inactive`, respectivement.

      La modification de l’état `Inactive` d’un magasin à `Active` active les listes et l’activité de commande pour le magasin, en utilisant les paramètres actuels du magasin (tels que les paramètres de liste, les règles de prix et les remplacements).

      La modification de l’état d’un magasin de `Active` à l’état `Inactive` interrompt les listes et l’activité de commande du magasin. Un magasin inactif conserve tous les paramètres du magasin et les listes, mais interrompt temporairement la synchronisation de la gestion des prix, de la quantité et des commandes jusqu’à ce que le magasin soit redéfini sur l’état `Active`. Cette fonctionnalité vous permet de contrôler votre activité de magasin au niveau régional sans avoir à recréer ou à réintégrer votre boutique Amazon ni à perdre des données de ventes et de commandes historiques.

   - **[!UICONTROL Delete]** - Choisissez de supprimer un magasin qui n’est plus nécessaire.

      Choisissez quand vous souhaitez supprimer un magasin Amazon existant et ses paramètres d’intégration avec votre compte [!DNL Amazon Seller Central]. La suppression du compte supprime la boutique du canal de vente Amazon, ainsi que tous les paramètres du compte, listes, journaux et autres informations relatives à cette boutique. Le magasin ne peut pas être récupéré après suppression. Un nouveau magasin doit être créé.

>[!NOTE]
>Pour modifier le site web affecté au magasin lors de l’intégration, vous devez supprimer le magasin et l’ajouter à nouveau avec le site web différent défini lors de l’intégration du magasin.

| Store Card | Description |
|--- |--- |
| Section supérieure | Inclut : <br>Icône de région du magasin, définie lors de l’[intégration du magasin](./store-integration.md).<br> Le affecté  _[!UICONTROL Magento Website]_, défini lors de l’intégration du magasin.<br>Le_[!UICONTROL Status]_ de votre magasin. Options : **[!UICONTROL Active]** - L’intégration de magasin est complète et vérifiée avec Amazon et est disponible pour les activités de vente. **[!UICONTROL Inactive]** - L’intégration du magasin est terminée, mais n’est pas en cours d’utilisation ni disponible pour les activités de vente. Lorsque `Inactive`, vos ventes Amazon sont suspendues. Lorsque `Active`, les recettes commerciales et les paramètres supplémentaires sont enregistrés pour être mis à jour avant l’activation.<br>La  *[!UICONTROL Last Updated]* date de la modification la plus récente de la configuration du magasin Amazon.<br>Date de  *[!UICONTROL Created]* création du magasin Amazon dans le canal de vente Amazon. |
| section du milieu | Inclut un graphique récapitulatif de l’activité de magasin pour les 30 derniers jours et inclut et alerte pour toutes les listes qui nécessitent une attention particulière. |
| Section inférieure | Inclut les options Afficher le magasin et Action .<br>Pour ouvrir le  [tableau de bord](./amazon-store-dashboard.md) du magasin, cliquez sur  **[!UICONTROL View Store]**.<br>Pour activer, désactiver ou supprimer un magasin, cliquez sur  **[!UICONTROL Actions]**. |
