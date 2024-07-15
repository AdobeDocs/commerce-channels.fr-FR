---
title: '[!DNL Channel Manager] Notes de mise à jour'
description: Informations les plus récentes sur la version  [!DNL Channel Manager] d’Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Notes de mise à jour [!DNL Channel Manager]

Ces notes de mise à jour décrivent la version initiale de [!DNL Channel Manager] et incluent :

![New](../assets/new.svg) Nouvelles fonctionnalités
![Problème corrigé](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

Voir [Versions à venir](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) pour en savoir plus sur les calendriers de publication et l’assistance.

Voir [Disponibilité du produit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) pour savoir quelles versions d’Adobe Commerce prennent en charge cette extension.

## v2.1.0

*3 octobre 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Le gestionnaire de canaux est désormais compatible avec les versions [ de la version bêta 2.4.7 d’Adobe Commerce ](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html).

## v2.0.0

*20 mars 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![New](../assets/new.svg)<!--CHAN-5893--> Channel Manager est désormais compatible avec Adobe Commerce version 2.4.6.

## v1.1.0

*23 novembre 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![New](../assets/new.svg)<!--CHAN-5204--> **Renvoie et remboursement** : vous pouvez désormais traiter le processus de retour et de remboursement de Walmart Marketplace pour les commandes expédiées par le biais d’un magasin Adobe Commerce et Magento Open Source Channel Manager. Les informations et mises à jour sur les retours et les remboursements sont synchronisées entre Walmart et Adobe Commerce afin que les données actives soient disponibles dans le storefront [!DNL Commerce] et [!DNL Walmart Marketplace]. Voir [Commandes de retour et de retour](return-refund-orders.md).

![Correction](../assets/fix.svg)<!--CHAN-5661--> Correction de l’erreur `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` qui se produisait lors de la resynchronisation du Gestionnaire de canaux avec les données commandées à l’aide de la commande `bin/magento saas:resync --feed orders`. L’erreur a été résolue en mettant à jour les dépendances des modules du gestionnaire de canaux pour le module d’exportateur de données commerciales, qui a été renommé `magento/module-sales-data-exporter` en `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 janvier 2022*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Version initiale de Channel Manager pour une disponibilité générale

