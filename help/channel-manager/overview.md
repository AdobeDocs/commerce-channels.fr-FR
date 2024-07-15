---
title: 'Introduction à [!DNL Channel Manager]'
description: "Découvrez comment installer et utiliser  [!DNL Channel Manager] pour intégrer Adobe Commerce et les magasins Magento Open Sources à Walmart Marketplace et créer un canal de vente pour gérer les listes de places de marché, les prix, les stocks et les ventes de manière transparente à partir de votre administrateur Commerce."
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Présentation de [!DNL Channel Manager]

[!DNL Channel Manager] aide les commerçants à augmenter les ventes, à atteindre de nouveaux clients, à rationaliser les opérations de vente et à gagner du temps en intégrant un catalogue de produits Adobe Commerce ou Magento Open Source à [!DNL Walmart Marketplace].

![[!DNL Channel Manager] extension Admin view](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] prend en charge les commerçants Adobe Commerce ou Magento Open Sources qui souhaitent vendre sur [!DNL Walmart Marketplace] en étendant l’administrateur [!DNL Commerce]. [!DNL Channel Manager] étant installé, les administrateurs de magasin et le personnel d’exploitation peuvent gérer [!DNL Walmart Marketplace] de manière transparente les ventes, les stocks et les prix des produits à partir de l’environnement Commerce.

L’administrateur étendu simplifie les opérations, car les commerçants peuvent utiliser les mêmes processus et workflows pour gérer les ventes à partir de [!DNL Commerce] storefronts et de Walmart Marketplace.

Après avoir installé et configuré [!DNL Channel Manager], vous pouvez utiliser les fonctionnalités suivantes pour gérer les commandes de vente Walmart Marketplace :

* **Gestion des listes** : connectez facilement des listes de produits en faisant correspondre les produits de votre catalogue [!DNL Commerce] aux listes [!DNL Walmart Marketplace] existantes.

* **Inventory management** - Les éléments figurant dans le compte de vendeur du marché du commerce sont automatiquement synchronisés et mis à jour à partir de [!DNL Commerce] pour garantir des niveaux de stock précis.

* **Mises à jour des tarifs** : maintenez des tarifs précis pour les listes de places de marché avec synchronisation automatique des prix. Lorsqu’un prix change dans Adobe Commerce, les modifications sont répercutées sur le marché.

* **Gestion des commandes** : lorsque de nouvelles commandes sont créées sur la marketplace, [!DNL Channel Manager] synchronise les commandes avec Adobe Commerce et envoie des accusés de réception de commande sur la marketplace. Cet acquittement garantit que l’inventaire est réservé pour chaque commande. La dernière étape consiste à créer les commandes correspondantes dans le système Order Management [!DNL Commerce] pour traitement.

* **Gestion des envois** : lorsque les commandes sont marquées comme étant expédiées dans Adobe Commerce, la mise à jour de l’expédition est envoyée à l’ [!DNL Walmart Marketplace]. Cette notification permet de s’assurer que les vendeurs respectent leurs exigences de contrat SLA d’exécution et que les clients reçoivent des notifications de mise à jour de la livraison pour leurs commandes actuelles.

* **Annulations** : lorsque les commandes sont annulées dans Adobe Commerce, [!DNL Channel Manager] envoie des informations de commande mises à jour au marketplace pour répliquer l’action pour la commande correspondante. Une fois l’annulation de la commande terminée, les mises à jour de la quantité de stock [!DNL Commerce] pour refléter les articles renvoyés et les mises à jour de stock sont automatiquement synchronisées avec [!DNL Walmart Marketplace].

* **Renvoie et remboursements** : lorsque Walmart Marketplace demande un retour pour les articles commandés via le canal de vente Adobe Commerce ou Magento Open Source, [!DNL Channel Manager] envoie les informations de demande de retour à la boutique de canaux de vente Commerce pour répliquer la demande de retour. Ensuite, le remboursement peut être traité à l&#39;aide du [!DNL Commerce] [workflow de remboursement](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow), méthode hors ligne. Une fois le remboursement terminé, [!DNL Channel Manager] synchronise la mise à jour avec Walmart afin que l’état du retour dans le compte de vendeur sur le marketplace puisse être mis à jour pour refléter le remboursement.

## Latence attendue des opérations [!DNL Channel Manager]

Les processus de synchronisation des données entre [!DNL Channel Manager] et un magasin [!DNL Walmart Marketplace] lié nécessitent un certain temps. Passez en revue le temps de traitement attendu pour les opérations [!DNL Channel Manager] afin de planifier le fonctionnement des opérations du canal de vente.

**Latence estimée pour les [!DNL Channel Manager] opérations**

| **Opération** | **Description** | **Délai attendu** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Ajout de produits à [!DNL Channel Manager] | Sélectionnez des produits du catalogue de produits [!DNL Commerce] et importez-les dans [!DNL Channel Manager]. | **Jusqu’à cinq minutes** : si vous sélectionnez de nombreux produits, par exemple un catalogue de produits entier, le processus d’importation prend plus de temps. |
| Correspondance de produits sur [!DNL Walmart Marketplace] | Sélectionnez les listes de produits dans [!DNL Channel Manager] et envoyez à Walmart pour correspondance. | **Jusqu’à 30 minutes** : si vous sélectionnez de nombreux produits, le processus de correspondance prend plus de temps en fonction de la quantité sélectionnée. |
| Mises à jour du stock | Lorsque la quantité d’inventaire change dans Commerce, [!DNL Channel Manager] synchronise la mise à jour avec Walmart. | **Jusqu’à 10 minutes** |
| Mises à jour des prix | Lorsqu’un prix de produit change, [!DNL Channel Manager] synchronise la mise à jour avec Walmart. | **Jusqu’à cinq minutes** |
| Commande des synchronisations de Walmart vers [!DNL Commerce] | Le client commande un produit [!DNL Commerce] sur Walmart Marketplace. Walmart envoie la commande à [!DNL Channel Manager]. L’ordre s’affiche dans le tableau de bord de l’ordre. | **Jusqu’à 30 minutes** |
| Ordre créé dans [!DNL Commerce] Order Management | [!DNL Channel Manager] crée la commande [!DNL Commerce] à partir de l’ordre Walmart et met à jour le tableau de bord des commandes afin d’inclure le numéro de commande [!DNL Commerce]. | **Jusqu’à cinq minutes** |
| Mise à jour de l’état de livraison dans [!DNL Commerce] Order Management | Lorsqu’une commande est expédiée depuis Commerce, [!DNL Channel Manager] met à jour l’état d’expédition dans le tableau de bord de la commande et envoie la mise à jour au marché de Walmart afin que le client puisse être informé. | **Jusqu’à cinq minutes** |
| Mise à jour des annulations de commande dans Commerce Order Management | Lorsqu&#39;une commande est annulée à partir de Commerce, [!DNL Channel Manager] met à jour l&#39;état de la commande dans le tableau de bord de la commande et envoie la mise à jour à Walmart Marketplace afin que le client puisse être informé. Une fois l’annulation de la commande terminée, la quantité de stock [!DNL Commerce] est mise à jour pour refléter les articles renvoyés. Ensuite, [!DNL Channel Manager] synchronise la mise à jour avec [!DNL Walmart Marketplace]. | **Jusqu’à cinq minutes** |


