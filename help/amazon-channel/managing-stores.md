---
title: Vue Magasins Amazon
description: Accédez à la vue Amazon Stores pour consulter rapidement les statistiques de base de chacun de vos magasins Amazon et accéder aux options de gestion.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Vue Magasins Amazon

Lorsque vous affichez la page d&#39;accueil du canal de vente Amazon, le _Amazon Stores_ s’ouvre par défaut.

![Vue Magasins Amazon](assets/amazon-sales-channel-home-tabs.png)

Le _[!UICONTROL Amazon Stores]_affiche une &quot;carte de magasin&quot; pour chacun de vos magasins Amazon, ainsi que des statistiques de base et des options de gestion. Les informations récapitulatives affichées dans chaque carte comprennent chaque statut de magasin, date de création, date de dernière mise à jour, listes nécessitant une attention particulière (exemple : Annonces incomplètes) et les [!DNL Commerce] site Web.

Lors de l’affichage de la _[!UICONTROL Amazon Store]_, chaque carte de magasin vous permet d’effectuer les opérations suivantes :

- Pour ouvrir une boutique [tableau de bord](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.

- Pour modifier l’état d’un magasin ou supprimer un magasin, cliquez sur **[!UICONTROL Action]** et choisissez :

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Choisissez de modifier le statut de la boutique en `Active` ou `Inactive`, respectivement.

      Modification d’un `Inactive` stocker dans `Active` status active les annonces et l&#39;activité de commande pour le magasin, en utilisant les paramètres actuels du magasin de magasins (tels que les paramètres d&#39;annonce, les règles de prix et les remplacements).

      Modification de l’état d’un magasin depuis `Active` à `Inactive` status suspend les annonces et l&#39;activité de commande pour le magasin. Un magasin inactif conserve tous les paramètres de magasin et les annonces, mais arrête temporairement la synchronisation de la gestion des prix, des quantités et des commandes jusqu&#39;à ce que le magasin redevienne `Active` statut. Cette fonctionnalité vous permet de contrôler votre activité de magasin au niveau régional sans avoir à recréer ou à réintégrer votre magasin Amazon ni à perdre des données historiques de commande et de vente.

   - **[!UICONTROL Delete]** - Choisissez de supprimer un magasin qui n’est plus nécessaire.

      Choisissez quand vous souhaitez supprimer un magasin Amazon existant et ses paramètres d’intégration avec votre [!DNL Amazon Seller Central] compte. La suppression du compte supprime le magasin du canal de vente Amazon, ainsi que tous les paramètres de compte, listes, journaux et autres informations associées à ce magasin. Le magasin ne peut pas être récupéré après la suppression, un nouveau magasin doit être créé.

>[!NOTE]
>Pour modifier le site web affecté au magasin lors de l’intégration, vous devez supprimer le magasin et ajouter à nouveau le magasin avec le site web différent défini lors de l’intégration du magasin.

| Carte de magasin | Description |
|--- |--- |
| Section supérieure | Comprend : <br>Icône de région du magasin, définie pendant [intégration de magasin](./store-integration.md).<br> Le _[!UICONTROL Magento Website]_, défini lors de l’intégration du magasin.<br>Le_[!UICONTROL Status]_ de votre magasin. Options : **[!UICONTROL Active]** - L&#39;intégration du magasin est terminée et vérifiée avec Amazon et est disponible pour les activités de vente. **[!UICONTROL Inactive]** - L&#39;intégration du magasin est terminée, mais n&#39;est pas en cours d&#39;utilisation ou disponible pour les activités de vente. Lorsque `Inactive`, vos ventes Amazon sont interrompues. Lorsque `Active`, les recettes commerciales et les paramètres supplémentaires sont enregistrés pour être mis à jour avant l’activation.<br>Le *[!UICONTROL Last Updated]* date de la dernière modification apportée à la configuration du magasin Amazon.<br>Le *[!UICONTROL Created]* date à laquelle le magasin Amazon a été créé dans le canal de vente Amazon. |
| Section médiane | Comprend un tableau récapitulatif des activités des magasins pour les 30 derniers jours et inclut et alerte pour toute annonce nécessitant une attention particulière. |
| Section inférieure | Inclut les options Afficher la Boutique et Action.<br>Pour ouvrir la boutique [tableau de bord](./amazon-store-dashboard.md), cliquez sur **[!UICONTROL View Store]**.<br>Pour activer, désactiver ou supprimer une boutique, cliquez sur **[!UICONTROL Actions]**. |
