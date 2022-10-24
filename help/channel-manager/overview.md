---
title: '"Introduction à [!DNL Channel Manager]'''
description: '''Découvrez comment installer et utiliser [!DNL Channel Manager] pour intégrer Adobe Commerce et les magasins Magento Open Sources à Walmart Marketplace et créer un canal de vente afin de gérer de manière transparente les listes, les tarifs, les stocks et les ventes sur le marché auprès de votre administrateur Commerce."'
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 2e3f8e51b765cda0559d8624d61e1ae9dc1c9667
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Introduction à [!DNL Channel Manager]

[!DNL Channel Manager] aide les commerçants à augmenter leurs ventes, à atteindre de nouveaux clients, à rationaliser leurs opérations de vente et à gagner du temps en intégrant un catalogue de produits Adobe Commerce ou Magento Open Source au [!DNL Walmart Marketplace].

![[!DNL Channel Manager] vue d’administration de l’extension](assets/channel-manager-home.png)

[!DNL Channel Manager] prend en charge les marchands Adobe Commerce ou Magento Open Sources qui souhaitent vendre sur [!DNL Walmart Marketplace] en étendant la variable [!DNL Commerce] Administrateur. Avec [!DNL Channel Manager] installé, les administrateurs de magasin et le personnel opérationnel peuvent gérer [!DNL Walmart Marketplace] les ventes, les stocks et la tarification des produits de l’environnement Commerce.

L’administrateur étendu simplifie les opérations, car les vendeurs peuvent utiliser les mêmes workflows et processus pour gérer les ventes des deux [!DNL Commerce] les vitrines et le Walmart Marketplace.

Après l’installation et la configuration [!DNL Channel Manager], vous pouvez utiliser les fonctionnalités suivantes pour gérer les commandes client de Walmart Marketplace :

* **Gestion des listes**- Connectez facilement des listes de produits en faisant correspondre les produits de votre [!DNL Commerce] Catalogue à existant [!DNL Walmart Marketplace] des listes.

* **Inventory management**- Les éléments figurant dans le compte du vendeur marchand sont automatiquement synchronisés et mis à jour à partir de [!DNL Commerce] pour garantir des niveaux de stock précis.

* **Mises à jour des tarifs**: maintenez des tarifs précis pour les listes de marchés avec synchronisation automatique des prix. Lorsqu’un prix change dans Adobe Commerce, les modifications sont répercutées sur le marché.

* **Gestion des commandes**—Lorsque de nouvelles commandes sont créées sur le marché, [!DNL Channel Manager] synchronise les commandes avec Adobe Commerce et envoie des accusés de réception de commande au marketplace. Cet acquittement garantit que l’inventaire est réservé pour chaque commande. La dernière étape consiste à créer les commandes correspondantes dans le [!DNL Commerce] Système de gestion des commandes pour le traitement.

* **Gestion des envois**: lorsque les commandes sont marquées comme étant expédiées dans Adobe Commerce, la mise à jour de l’expédition est envoyée à la variable [!DNL Walmart Marketplace]. Cette notification permet de s’assurer que les vendeurs respectent leurs exigences de contrat SLA d’exécution et que les clients reçoivent des notifications de mise à jour de la livraison pour leurs commandes actuelles.

* **Annulations**: lorsque les commandes sont annulées dans Adobe Commerce, [!DNL Channel Manager] envoie des informations de commande mises à jour au marketplace afin de répliquer l’action pour la commande de marché correspondante. Une fois la commande annulée, la variable [!DNL Commerce] les mises à jour de la quantité de stock pour refléter les éléments renvoyés et les mises à jour de stock sont synchronisées automatiquement avec [!DNL Walmart Marketplace].

* **Renvoie et remboursement**: lorsque Walmart Marketplace demande un retour pour les articles commandés via le canal de vente Adobe Commerce ou Magento Open Source, [!DNL Channel Manager] envoie les informations de demande de retour à la boutique de canaux de vente Commerce pour répliquer la demande de retour. Ensuite, le remboursement peut être traité à l&#39;aide de l&#39;événement [!DNL Commerce] [workflow de remboursement](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow), méthode hors ligne. Une fois le remboursement effectué, [!DNL Channel Manager] synchronise la mise à jour avec Walmart de sorte que l’état de retour dans le compte de vendeur Marketplace puisse être mis à jour pour refléter le remboursement.

## Latence attendue pour [!DNL Channel Manager] opérations

La synchronisation des données entre les [!DNL Channel Manager] et lié [!DNL Walmart Marketplace] Le magasin prend du temps. Examinez le temps de traitement attendu pour [!DNL Channel Manager] opérations pour planifier le fonctionnement des canaux de vente.

**Latence estimée pour [!DNL Channel Manager] opérations**

| **Opération** | **Description** | **Délai attendu** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Ajouter des produits à [!DNL Channel Manager] | Sélectionnez des produits dans la [!DNL Commerce] catalogue de produits et les importer dans [!DNL Channel Manager]. | **Jusqu’à cinq minutes**-Si vous sélectionnez de nombreux produits, par exemple un catalogue de produits entier, le processus d’importation prend plus de temps. |
| Correspondance de produits sur [!DNL Walmart Marketplace] | Sélectionner les listes de produits dans [!DNL Channel Manager] et envoyer à Walmart pour correspondance. | **Jusqu’à 30 minutes**-Si vous sélectionnez de nombreux produits, le processus de correspondance prend plus de temps en fonction de la quantité sélectionnée. |
| Mises à jour du stock | Lorsque la quantité de stock change dans Commerce, [!DNL Channel Manager] synchronise la mise à jour avec Walmart. | **Jusqu’à 10 minutes** |
| Mises à jour des prix | Lorsqu’un prix de produit change, [!DNL Channel Manager] synchronise la mise à jour avec Walmart. | **Jusqu’à cinq minutes** |
| Commande des synchronisations de Walmart à [!DNL Commerce] | Le client commande une [!DNL Commerce] produit sur Walmart Marketplace. Walmart envoie l&#39;ordre à [!DNL Channel Manager]. L’ordre s’affiche dans le tableau de bord de l’ordre. | **Jusqu’à 30 minutes** |
| Ordre créé dans [!DNL Commerce] Gestion des commandes | [!DNL Channel Manager] crée la variable [!DNL Commerce] Commande à partir de la commande Walmart et met à jour le tableau de bord des commandes afin d’inclure la variable [!DNL Commerce] numéro de commande. | **Jusqu’à cinq minutes** |
| Mise à jour de l’état de livraison dans [!DNL Commerce] Gestion des commandes | Lorsqu’une commande est expédiée à partir de Commerce, [!DNL Channel Manager] met à jour l’état d’expédition dans le tableau de bord de la commande et envoyez la mise à jour à Walmart Marketplace afin que le client puisse être informé. | **Jusqu’à cinq minutes** |
| Mise à jour des annulations de commande dans Commerce Order Management | Lorsqu’une commande est annulée à partir de Commerce, [!DNL Channel Manager] met à jour l’état de la commande dans le tableau de bord de commande et envoie la mise à jour à Walmart Marketplace afin que le client puisse être informé. Une fois la commande annulée, la variable [!DNL Commerce] mises à jour de la quantité de stock pour refléter les éléments renvoyés. Alors, [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace]. | **Jusqu’à cinq minutes** |


