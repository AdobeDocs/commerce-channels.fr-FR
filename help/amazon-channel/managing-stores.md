---
title: "[!UICONTROL Amazon Stores] view"
description: Accédez à la vue Amazon Stores (Magasins) pour passer rapidement en revue les statistiques de base de chacun de vos magasins Amazon et les options de gestion des accès.
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores] vue

Lors de l’affichage de la page d’accueil du canal de vente Amazon, la vue _Amazon Stores_ s’ouvre par défaut.

![Vue Magasins Amazon](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

La vue _[!UICONTROL Amazon Stores]_affiche une &quot;carte de magasin&quot; pour chacun de vos magasins Amazon, ainsi que certaines options de statistiques et de gestion de base. Les informations récapitulatives affichées dans chaque carte comprennent l’état du magasin, la date de création, la date de dernière mise à jour, les listes qui nécessitent une attention particulière (par exemple : listes incomplètes) et le site web [!DNL Commerce] affecté.

Lors de l’affichage de la vue _[!UICONTROL Amazon Store]_, chaque carte de magasin vous permet d’effectuer les opérations suivantes :

- Pour ouvrir un magasin [dashboard](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.

- Pour modifier l’état d’un magasin ou supprimer un magasin, cliquez sur **[!UICONTROL Action]** et choisissez :

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Choisissez de remplacer l’état du magasin par `Active` ou `Inactive`, respectivement.

     La modification de l’état d’un magasin `Inactive` sur `Active` active les listes et l’activité de commande pour le magasin, en utilisant les paramètres actuels du magasin (tels que les paramètres de liste, les règles de prix et les remplacements).

     La modification de l’état d’un magasin de `Active` à `Inactive` interrompt les listes et l’activité de commande du magasin. Un magasin inactif conserve tous les paramètres du magasin et les listes, mais interrompt temporairement la synchronisation de la gestion des prix, de la quantité et des commandes jusqu’à ce que le magasin repasse à l’état `Active`. Cette fonctionnalité vous permet de contrôler votre activité de magasin au niveau régional sans avoir à recréer ou à réintégrer votre boutique Amazon ni à perdre des données de ventes et de commandes historiques.

   - **[!UICONTROL Delete]** - Choisissez de supprimer un magasin qui n’est plus nécessaire.

     Choisissez quand vous souhaitez supprimer un magasin Amazon existant et ses paramètres d&#39;intégration avec votre compte [!DNL Amazon Seller Central]. La suppression du compte supprime la boutique du canal de vente Amazon, ainsi que tous les paramètres du compte, listes, journaux et autres informations relatives à cette boutique. Le magasin ne peut pas être récupéré après suppression. Un nouveau magasin doit être créé.

>[!NOTE]
>Pour modifier le site web affecté au magasin lors de l’intégration, vous devez supprimer le magasin et l’ajouter à nouveau avec le site web différent défini lors de l’intégration du magasin.

| Store Card | Description |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Section supérieure | Inclut : <br>Icône de région pour le magasin, définie lors de l’ [intégration du magasin](./store-integration.md).<br> Le _[!UICONTROL Magento Website]_affecté, défini lors de l’intégration du magasin.<br>_[!UICONTROL Status]_ de votre boutique. Options : **[!UICONTROL Active]** - L’intégration du magasin est terminée et vérifiée avec Amazon et est disponible pour l’activité de vente. **[!UICONTROL Inactive]** - L’intégration du magasin est terminée, mais n’est pas en cours d’utilisation ni disponible pour l’activité de vente. Lorsque `Inactive`, vos ventes Amazon sont suspendues. Lorsque `Active`, les recettes commerciales et les paramètres supplémentaires sont enregistrés pour être mis à jour avant l’activation.<br>Date *[!UICONTROL Last Updated]* de la dernière modification de la configuration du magasin Amazon.<br>Date *[!UICONTROL Created]* à laquelle la boutique Amazon a été créée dans le canal de vente Amazon. |
| section du milieu | Inclut un graphique récapitulatif de l’activité de magasin pour les 30 derniers jours et inclut et alerte pour toutes les listes qui nécessitent une attention particulière. |
| Section inférieure | Inclut les options Afficher le magasin et Action .<br>Pour ouvrir le magasin [dashboard](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.<br>Pour activer, désactiver ou supprimer un magasin, cliquez sur **[!UICONTROL Actions]**. |
