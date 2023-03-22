---
title: '''[!DNL Channel Manager] Notes de mise à jour de'
description: Les dernières informations de mise à jour pour [!DNL Channel Manager] d’Adobe Commerce.
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 9cc1b79089771ef9a58d22379197b210d31e1670
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# [!DNL Channel Manager] Notes de mise à jour

Ces notes de mise à jour décrivent la version initiale de [!DNL Channel Manager] et incluent :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités
![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus


## v1.1.0

![Nouveau](../assets/new.svg)<!--CHAN-5204--> **Renvoie et remboursement**: vous pouvez désormais traiter le processus de retour et de remboursement de Walmart Marketplace pour les commandes expédiées via un magasin Adobe Commerce et Magento Open Source Channel Manager. Les informations et les mises à jour sur les retours et les remboursements sont synchronisées entre Walmart et Adobe Commerce afin que les données actives soient disponibles dans les [!DNL Commerce] storefront et [!DNL Walmart Marketplace]. Voir [Commandes de retour et de retour](return-refund-orders.md).

![Fixe](../assets/fix.svg)<!--CHAN-5661--> Correction de la fonction `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` erreur qui se produisait lors de la resynchronisation du Gestionnaire de canaux qui classait les données à l’aide de la variable `bin/magento saas:resync --feed orders` . L’erreur a été résolue en mettant à jour les dépendances des modules du gestionnaire de canaux pour le module d’exportateur de données commerciales, qui a été renommé depuis `magento/module-sales-data-exporter` to `magento/module-sales-orders-data-exporter`.

## v1.0.0

Version initiale, compatible avec les versions commerciales suivantes :

* Open Source (CE) : 2.4.x
* Adobe Commerce (EE) : 2.4.x
* Adobe Commerce for Cloud (CEE) : 2.4.x
* Stabilité : Stable
