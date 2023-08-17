---
title: "[!UICONTROL Amazon Stores] view"
description: Accédez à la vue Amazon Stores (Magasins) pour passer rapidement en revue les statistiques de base de chacun de vos magasins Amazon et les options de gestion des accès.
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores] view

Lors de l’affichage de la page d’accueil du canal de vente Amazon, la variable _Magasins Amazon_ La vue s’ouvre par défaut.

![Vue Magasins Amazon](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

La variable _[!UICONTROL Amazon Stores]_La vue affiche une &quot;carte de magasin&quot; pour chacun de vos magasins Amazon, ainsi que certaines options de statistiques et de gestion de base. Les informations récapitulatives affichées dans chaque carte comprennent l’état de chaque magasin, la date de création, la date de la dernière mise à jour, les listes auxquelles il faut prêter attention (par exemple : listes incomplètes) et l’attribution [!DNL Commerce] site web.

Lors de l’affichage de la variable _[!UICONTROL Amazon Store]_vue, chaque carte de magasin vous permet d’effectuer les opérations suivantes :

- Pour ouvrir une boutique [tableau de bord](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.

- Pour modifier l’état d’un magasin ou supprimer un magasin, cliquez sur **[!UICONTROL Action]** et choisissez :

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Choisissez de modifier le statut du magasin en `Active` ou `Inactive`, respectivement.

     Modification d’un `Inactive` stocker dans `Active` status active les listes et l’activité de commande pour le magasin, à l’aide des paramètres actuels du magasin (tels que les paramètres de liste, les règles de prix et les remplacements).

     Modification de l’état d’un magasin à partir de `Active` to `Inactive` Le statut suspend les listes et l’activité de commande pour le magasin. Un magasin inactif conserve tous les paramètres de magasin et les listes, mais interrompt temporairement la synchronisation de la gestion des prix, des quantités et des commandes jusqu’à ce que le magasin soit de nouveau remplacé par `Active` statut. Cette fonctionnalité vous permet de contrôler votre activité de magasin au niveau régional sans avoir à recréer ou à réintégrer votre boutique Amazon ni à perdre des données de ventes et de commandes historiques.

   - **[!UICONTROL Delete]** - Choisissez de supprimer un magasin qui n’est plus nécessaire.

     Choisissez quand vous souhaitez supprimer un magasin Amazon existant et ses paramètres d’intégration avec votre [!DNL Amazon Seller Central] compte . La suppression du compte supprime la boutique du canal de vente Amazon, ainsi que tous les paramètres du compte, listes, journaux et autres informations relatives à cette boutique. Le magasin ne peut pas être récupéré après suppression. Un nouveau magasin doit être créé.

>[!NOTE]
>Pour modifier le site web affecté au magasin lors de l’intégration, vous devez supprimer le magasin et l’ajouter à nouveau avec le site web différent défini lors de l’intégration du magasin.

| Store Card | Description |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Section supérieure | Inclut : <br>Icône de région du magasin, définie pendant la [intégration de magasin](./store-integration.md).<br> Le _[!UICONTROL Magento Website]_, défini lors de l’intégration du magasin.<br>La variable_[!UICONTROL Status]_ de votre magasin. Options : **[!UICONTROL Active]** - L’intégration du magasin est terminée et vérifiée avec Amazon et est disponible pour les activités de vente. **[!UICONTROL Inactive]** - L’intégration du magasin est terminée, mais n’est pas en cours d’utilisation ni disponible pour les activités de vente. When `Inactive`, vos ventes Amazon sont suspendues. When `Active`, les recettes commerciales et les paramètres supplémentaires sont enregistrés pour être mis à jour avant l’activation.<br>La variable *[!UICONTROL Last Updated]* date de la dernière modification de la configuration du magasin Amazon.<br>La variable *[!UICONTROL Created]* date à laquelle la boutique Amazon a été créée dans le canal de vente Amazon. |
| section du milieu | Inclut un graphique récapitulatif de l’activité de magasin pour les 30 derniers jours et inclut et alerte pour toutes les listes qui nécessitent une attention particulière. |
| Section inférieure | Inclut les options Afficher le magasin et Action .<br>Pour ouvrir le magasin [tableau de bord](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.<br>Pour activer, désactiver ou supprimer un magasin, cliquez sur **[!UICONTROL Actions]**. |
