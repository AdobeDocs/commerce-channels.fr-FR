---
title: "Introduction à [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permet aux commerçants de vendre facilement des produits dans la variable [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Introduction à [!DNL Amazon Sales Channel]

En tant que marchand Adobe Commerce ou Magento Open Source, vous pouvez utiliser la variable [!DNL Amazon Sales Channel] pour intégrer vos magasins à la plus grande destination mondiale de shopping sur Internet. Cette extension active les ventes Amazon en se connectant [!DNL Commerce] avec votre [!DNL Amazon Seller Central] de rendre compte et de fournir à la fois l’automatisation et la synchronisation des données de catalogue et de commande. Gérez complètement toutes les listes Amazon, implémentez des règles de tarification simples ou intelligentes, et gérez vos commandes et vos stocks au moyen d’une seule [!DNL Commerce] tableau de bord.

Après [intégration](./amazon-onboarding-home.md), [!DNL Commerce] devient un &quot;centre de commande central&quot; pour gérer et contrôler vos listes, commandes et stocks Amazon, ainsi que les tarifs de votre boutique Amazon. [Intégration de magasin](./store-integration.md) se connecte à [!DNL Commerce] instance et Amazon pour synchroniser les données entre les deux plateformes. Le canal de vente Amazon vous permet d’effectuer les opérations suivantes :

- [Onboard](./amazon-onboarding-home.md) et intégrer un ou plusieurs [!DNL Amazon Seller Central] comptes avec Adobe Commerce ou Magento Open Source.

- Importez et synchronisez vos listes Amazon existantes et faites correspondre vos produits à vos [!DNL Commerce] catalogue, création d’un catalogue de produits centralisé.

- Créez et gérez des listes Amazon pour les produits de votre [!DNL Commerce] catalogue.

- Afficher et exécuter (envoyer) les commandes dans [!DNL Commerce] et Amazon, synchroniser l’état de la commande, les informations de paiement et de remboursement.

- Afficher les journaux pour l’analyse et les erreurs pour [prix compétitifs](./competitive-price-analysis.md), [répertorier les modifications](./listing-changes-log.md), et [problèmes de communication](./communication-errors-log.md).

Accédez à vos magasins Amazon pour afficher et gérer toutes ces fonctionnalités, informations de compte, listes, commandes, etc. sur le canal de vente Amazon [page d&#39;accueil](./amazon-sales-channel-home.md).

## Promotions et tarifs

Avec le [!DNL Amazon Sales Channel] , vous pouvez :

- Synchroniser les tarifs des listes Amazon avec [!DNL Commerce] prix du catalogue (ou attribut de prix alternatif).

- Activer MSRP [tarif de mise en service](./listing-price.md#configure-listing-price-settings) dans vos listes Amazon pour augmenter la proposition de valeur client.

- Activation et gestion [Prix publicitaire minimal (MAP)](./listing-price.md#configure-listing-price-settings) dans vos listes Amazon.

- Configurer d’autres [TVA](./listing-price.md#configure-listing-price-settings) dans vos tarifs Amazon.

- Définissez une valeur personnalisée pour la &quot;quantité disponible&quot; dans votre [paramètres stock/quantité](./stock-quantity.md#configure-stock--quantity-settings) pour afficher avec vos listes Amazon afin d’augmenter l’urgence de l’acheteur.

## Règles de tarifs

Avec le [!DNL Amazon Sales Channel] , vous pouvez :

- Créer empilables, flexibles et complexes [règles de tarification](./pricing-products.md) pour gérer vos tarifs Amazon pour les ventes quotidiennes ou les promotions saisonnières.

- Créer [floor](./floor-price.md) et [ceiling](./optional-ceiling-price.md) pour protéger vos prix les plus bas et les plus élevés.

- Création et gestion [règles de retarification intelligente](./intelligent-repricing-rules.md) qui ajustent automatiquement la tarification de votre produit par rapport à d’autres concurrents Amazon ([concurrent le plus faible](./lowest-competitor-pricing.md) et [Buy Box](./buy-box-competitor-pricing.md) prix).

## Gestion des flux de catalogue

Avec le [!DNL Amazon Sales Channel] , vous pouvez :

- Importez vos listes Amazon existantes (produits) et faites-les correspondre aux produits existants ou créez des produits dans votre [!DNL Commerce] catalogue.

- Publiez votre [!DNL Commerce] produits vers Amazon pour créer des listes Amazon.

- Créer [overrides](./creating-editing-overrides.md) pour définir un prix individuel, le temps de traitement, la condition et le message des notes du vendeur.

- Importation et mappage du produit [Attributs](./attributes-view.md) de vos listes Amazon pour qu’elles correspondent automatiquement aux produits de votre [!DNL Commerce] catalogue.

- Définissez plusieurs paramètres de recherche pour qu’ils correspondent aux listes Amazon [!DNL Commerce] catalogue.

- Définir [règles de liste](./listing-rules.md) pour déterminer lequel de vos [!DNL Commerce] les produits peuvent être répertoriés dans Amazon.

- Définir une valeur par défaut [temps de traitement](./product-listing-actions.md) pour vos nouvelles listes Amazon.

- Faire correspondre les conditions de liste en fonction d’un [!DNL Commerce] attribut.

- Ajoutez des notes de vendeur pour chaque type de condition (facultatif).

- Mettez en oeuvre des seuils de quantité lors de l’importation de listes Amazon dans votre [!DNL Commerce] catalogue.

- Afficher les recommandations [améliorations des listes](./listing-improvements.md).

## Gestion des commandes et service client

Avec le [!DNL Amazon Sales Channel] , vous pouvez :

- Commandes d’assistance et de traitement dans Amazon et [!DNL Commerce].

- [Importer](./order-settings.md#configure-order-settings) vos commandes Amazon dans [!DNL Commerce] ou laissez-les dans Amazon.

- Définissez lequel de vos [!DNL Commerce] boutiques de sites web à associer à vos commandes Amazon pour l&#39;import et la gestion des commandes.

- Afficher, annuler et envoyer des commandes depuis [!DNL Commerce] et/ou Amazon selon votre [paramètres d’exécution](./fulfilled-by.md).

- Faites correspondre votre état de commande Amazon à un état personnalisé dans [!DNL Commerce] (facultatif).

- Affichez et gérez les erreurs de commande afin de résoudre les problèmes et de vous connecter aux clients.

- Envoyez les données de suivi de commande à votre [!DNL Amazon Seller Central] compte .

- [Annulation des commandes](./cancel-unshipped-order.md) et sélectionnez une réponse de raison.

- Afficher la variable [commande récente](./amazon-store-dashboard.md) informations relatives à vos commandes Amazon.

## Reporting

Avec le [!DNL Amazon Sales Channel] vous pouvez consulter les informations des rapports sur :

- Listes par statut de principal, inactif, éligible et incomplet.

- Commandes en attente d’expédition.

- Commandes les plus récentes.

- Amazon [journal des modifications](./listing-changes-log.md) pour passer en revue les modifications apportées aux flux de produits/listes (telles que le prix et la quantité).

- Produit [Buy Box](./buy-box-competitor-pricing.md) Données sur les tarifs des concurrents.

- Produit [Tarifs des concurrents les plus bas](./lowest-competitor-pricing.md) data.

## Prise en charge des ventes globales

Avec le [!DNL Amazon Sales Channel] , vous pouvez :

- Gérer plusieurs [!DNL Amazon Marketplace] régions (pays).

- Prise en charge de plusieurs devises à l’aide de la variable [Outil de configuration des devises de commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Gérez les envois depuis les emplacements de vos produits et les centres d’exécution Amazon.

## Gestion des clients

Créez votre [!DNL Commerce] base de données client par [import de données client](./order-settings.md#configure-order-settings) associée à vos commandes Amazon. Développez votre potentiel marketing grâce à cette liste étendue de clients grâce à vos [!DNL Amazon Marketplace] listes et [!DNL Commerce] storefront.


Commencer est facile. Un processus d’intégration rapide vous guide dans la création d’un [!DNL Amazon Seller Central] compte et intégration à votre boutique de canaux de vente Amazon et à votre [!DNL Commerce] catalogue pour gérer les listes, commandes, stocks et exécution d’Amazon. Un tableau de bord central affiche les mises à jour d’état pour toutes vos intégrations de magasins de canaux de vente Amazon et vos listes Amazon. Atteindre de nouveaux clients dans le [!DNL Amazon Marketplace] grâce à des processus simplifiés et automatisés, le tout à peu ou aucun des coûts et du travail liés à la mise en place d&#39;un nouveau système.

Après avoir intégré votre [!DNL Amazon Seller Central] , [!DNL Amazon Sales Channel] l’extension vous permet de gérer vos comptes et de synchroniser les données entre [!DNL Commerce] et Amazon. Il vous permet de créer des listes, de gérer les promotions, de définir des prix et de gérer les stocks et l’exécution directement via le [!DNL Commerce] Administrateur. Ces options incluent des règles de tarification qui contrôlent les tarifs d’Amazon pour le même article et ajustent automatiquement vos prix pour qu’ils soient plus compétitifs.

