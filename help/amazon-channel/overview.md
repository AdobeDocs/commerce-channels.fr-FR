---
title: "Introduction à [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] permet aux commerçants de vendre facilement des produits dans le  [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Présentation de [!DNL Amazon Sales Channel]

En tant que marchand Adobe Commerce ou Magento Open Source, vous pouvez utiliser l’extension [!DNL Amazon Sales Channel] pour intégrer vos magasins à la plus grande destination mondiale d’achats sur Internet. Cette extension active les ventes Amazon en connectant [!DNL Commerce] à votre compte [!DNL Amazon Seller Central] et en assurant l’automatisation et la synchronisation des données de catalogue et de commande. Gérez complètement toutes les listes Amazon, implémentez des règles de tarification simples ou intelligentes et conservez vos commandes et vos stocks au moyen d’un seul tableau de bord [!DNL Commerce].

Après [l’intégration](./amazon-onboarding-home.md), [!DNL Commerce] devient un &quot;centre de commande central&quot; pour gérer et contrôler vos listes, commandes, stocks et tarifs Amazon pour votre boutique Amazon. [L’intégration de magasin](./store-integration.md) connecte votre instance [!DNL Commerce] et Amazon pour synchroniser les données entre les deux plateformes. Le canal de vente Amazon vous permet d’effectuer les opérations suivantes :

- [Onboard](./amazon-onboarding-home.md) et intégrez un ou plusieurs comptes [!DNL Amazon Seller Central] à Adobe Commerce ou Magento Open Source.

- Importez et synchronisez vos listes Amazon existantes et faites correspondre vos produits à votre catalogue [!DNL Commerce], créant ainsi un catalogue de produits centralisé.

- Créez et gérez des listes Amazon pour les produits de votre catalogue [!DNL Commerce].

- Afficher et exécuter (envoyer) les commandes dans [!DNL Commerce] et Amazon, synchroniser l’état des commandes, les informations de paiement et de remboursement.

- Affichez les journaux pour les analyses et les erreurs pour les [prix compétitifs](./competitive-price-analysis.md), les [ changements de liste](./listing-changes-log.md) et les [problèmes de communication](./communication-errors-log.md).

Accédez aux magasins Amazon pour afficher et gérer toutes ces fonctionnalités, informations de compte, listes, commandes, etc. sur la [page d&#39;accueil](./amazon-sales-channel-home.md) du canal de vente Amazon.

## Promotions et tarifs

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez :

- Synchronisez le prix des listes Amazon avec le prix du catalogue [!DNL Commerce] (ou un attribut de prix alternatif).

- Activez le MSRP [ grève-prix](./listing-price.md#configure-listing-price-settings) dans vos listes Amazon pour augmenter la proposition de valeur client.

- Activez et gérez le [Prix minimum de publicité (MAP)](./listing-price.md#configure-listing-price-settings) dans vos listes Amazon.

- Configurez des [taxes sur la TVA](./listing-price.md#configure-listing-price-settings) supplémentaires dans vos tarifs Amazon.

- Définissez une valeur personnalisée pour &quot;quantité disponible&quot; dans vos [paramètres stock/quantité](./stock-quantity.md#configure-stock--quantity-settings) afin de l’afficher avec vos listes Amazon pour augmenter l’urgence de l’acheteur.

## Règles de tarifs

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez :

- Créez des [ règles de tarification](./pricing-products.md) empilables, flexibles et complexes pour gérer vos tarifs Amazon pour les ventes quotidiennes ou les promotions saisonnières.

- Créez des prix [plancher](./floor-price.md) et [plafond](./optional-ceiling-price.md) pour protéger vos prix les plus bas et les plus élevés.

- Créez et gérez des [règles de tarification intelligente](./intelligent-repricing-rules.md) qui ajustent automatiquement la tarification de votre produit par rapport aux autres concurrents Amazon ([plus faible concurrent](./lowest-competitor-pricing.md) et [Buy Box](./buy-box-competitor-pricing.md) prix).

## Gestion des flux de catalogue

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez :

- Importez vos listes Amazon existantes (produits) et faites-les correspondre à des produits existants ou créez-les dans votre catalogue [!DNL Commerce].

- Publish vos produits [!DNL Commerce] dans Amazon pour créer des listes Amazon.

- Créez des [remplacements](./creating-editing-overrides.md) pour définir un prix individuel, le temps de traitement, la condition et le message des notes du vendeur.

- Importez et mappez le produit [attributes](./attributes-view.md) de vos listes Amazon pour établir une correspondance automatique avec les produits de votre catalogue [!DNL Commerce].

- Définissez plusieurs paramètres de recherche pour qu’ils correspondent aux listes Amazon de votre catalogue [!DNL Commerce].

- Définissez des [règles de liste](./listing-rules.md) pour déterminer lequel de vos [!DNL Commerce] produits peut être répertorié sur Amazon.

- Définissez une [ heure de traitement par défaut](./product-listing-actions.md) pour vos nouvelles listes Amazon.

- Correspondance des conditions de liste basées sur un attribut [!DNL Commerce].

- Ajoutez des notes de vendeur pour chaque type de condition (facultatif).

- Implémentez des seuils de quantité lors de l&#39;import de listes Amazon dans votre catalogue [!DNL Commerce].

- Afficher les [améliorations de liste](./listing-improvements.md) recommandées.

## Gestion des commandes et service client

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez :

- Assistance et traitement des commandes dans Amazon et [!DNL Commerce].

- [Importez](./order-settings.md#configure-order-settings) vos commandes Amazon dans [!DNL Commerce] ou laissez-les dans Amazon.

- Définissez les boutiques de votre site web [!DNL Commerce] à associer à vos commandes Amazon pour l&#39;import et la gestion des commandes.

- Affichez, annulez et envoyez des commandes de [!DNL Commerce] et/ou Amazon selon vos [paramètres d’exécution](./fulfilled-by.md).

- Faites correspondre votre état de commande Amazon à un état personnalisé dans [!DNL Commerce] (facultatif).

- Affichez et gérez les erreurs de commande afin de résoudre les problèmes et de vous connecter aux clients.

- Envoyez des données de suivi de commande à votre compte [!DNL Amazon Seller Central].

- [Annuler les commandes](./cancel-unshipped-order.md) et sélectionner une réponse de motif.

- Affichez les informations sur la [commande récente](./amazon-store-dashboard.md) de vos commandes Amazon.

## Reporting

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez consulter les informations de rapport sur :

- Listes par statut actif, inactif, éligible et incomplet.

- Commandes en attente d’expédition.

- Commandes les plus récentes.

- Le [ journal des modifications de liste d’Amazon ](./listing-changes-log.md) pour passer en revue les modifications de flux de produit/de liste (telles que le prix et la quantité).

- Produit [Buy Box](./buy-box-competitor-pricing.md) Données de tarification des concurrents.

- Données [ du produit sur le prix des concurrents le plus bas](./lowest-competitor-pricing.md).

## Prise en charge des ventes globales

Avec l’extension [!DNL Amazon Sales Channel], vous pouvez :

- Gérer plusieurs régions [!DNL Amazon Marketplace] (pays).

- Prise en charge de plusieurs devises à l’aide de l’[ outil de configuration des devises Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Gérez les envois depuis les emplacements de vos produits et les centres d’exécution Amazon.

## Gestion des clients

Créez votre base de données client [!DNL Commerce] en [important des données client](./order-settings.md#configure-order-settings) associées à vos commandes Amazon. Développez votre potentiel marketing grâce à cette liste étendue de clients grâce à vos [!DNL Amazon Marketplace] listes et à votre vitrine [!DNL Commerce].


La prise en main est facile. Un processus d’intégration rapide vous guide dans la création d’un compte [!DNL Amazon Seller Central] et l’intégration à votre boutique de canaux de vente Amazon et à votre catalogue [!DNL Commerce] pour gérer les listes, les commandes, l’inventaire et l’exécution Amazon. Un tableau de bord central affiche les mises à jour d’état pour toutes vos intégrations de magasins de canaux de vente Amazon et vos listes Amazon. Atteindre de nouveaux clients dans le [!DNL Amazon Marketplace] global avec des processus simplifiés et automatisés - le tout à peu ou pas du tout du coût et de la main d’oeuvre de la configuration d’un nouveau système.

Après l&#39;intégration de votre compte [!DNL Amazon Seller Central], l&#39;extension [!DNL Amazon Sales Channel] vous permet de gérer vos comptes et de synchroniser les données entre [!DNL Commerce] et Amazon. Il vous permet de créer des listes, de gérer les promotions, de définir des prix et de gérer les stocks et l’exécution directement via l’administrateur [!DNL Commerce]. Ces options incluent des règles de tarification qui contrôlent les tarifs d’Amazon pour le même article et ajustent automatiquement vos prix pour qu’ils soient plus compétitifs.

