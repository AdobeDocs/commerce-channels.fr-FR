---
title: A propos [!DNL Channel Manager]
description: Découvrez comment installer et utiliser [!DNL Channel Manager] pour intégrer Adobe Commerce et les magasins Magento Open Sources à des marchés tiers et créer un canal de vente afin de gérer les listes, les prix, les stocks et les ventes sur le marché de manière transparente, à partir de votre administrateur Commerce.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 7412a3d5b78e206521a048fb56edacd8f11ddb58
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Présentation

Le gestionnaire de canaux pour Adobe Commerce et Magento Open Source offre un espace de travail pratique dans l’administration pour gérer les ventes de canaux sur des marchés tiers tels que Walmart, Amazon et eBay. Augmentez les ventes et accédez aux nouveaux marchés tout en gérant en toute transparence les opérations des canaux de vente auprès de votre administrateur Commerce.

![[!DNL Channel Manager] vue d’administration de l’extension](assets/channel-manager-admin-entry-page.png)

## Présentation de la version bêta

La version bêta de Channel Manager prend en charge les vendeurs Adobe Commerce ou Magento Open Sources qui souhaitent proposer des produits sur Walmart Marketplace.

Cette version prend en charge les fonctionnalités suivantes pour gérer les opérations des canaux de vente :

* Établir une connexion API entre Adobe Commerce ou Magento Open Source et Walmart Marketplace

* Publier des produits de Channel Manager vers Walmart à l’aide de la correspondance de produits

* Affichage de l’état de la liste de produits dans le Gestionnaire de canaux, par exemple *draft*, *traitement*, *correspond à*, *error*.

* Synchroniser les quantités d’inventaire pour les produits correspondants de Commerce à Walmart

* Synchronisation des prix du catalogue pour les produits correspondants de Commerce à Walmart

* Recevez les commandes de Walmart Marketplace et affichez-les dans le [!DNL Commerce] tableau de bord des commandes

### Latence attendue des opérations du Gestionnaire de canaux

La synchronisation des données entre les [!DNL Channel Manager] et lié [!DNL Walmart Marketplace] Le magasin prend du temps. Examinez le temps de traitement attendu pour [!DNL Channel Manager] opérations pour planifier le fonctionnement des canaux de vente.

**Latence estimée pour les opérations du Gestionnaire de canaux**

| **Opération** | **Description** | **Délai attendu** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Ajout de produits à Channel Manager | Sélectionnez des produits dans le catalogue de produits Commerce et importez-les dans le Gestionnaire de canaux. | **Jusqu’à 5 minutes**-Si vous sélectionnez de nombreux produits, par exemple un catalogue de produits entier, le processus d’importation prend plus de temps. |
| Mise en correspondance de produits sur Walmart Marketplace | Sélectionnez les listes de produits dans le Gestionnaire de canaux et envoyez à Walmart pour les faire correspondre. | **Jusqu’à 30 minutes**-Si vous sélectionnez de nombreux produits, le processus de correspondance prend plus de temps en fonction de la quantité sélectionnée. |
| Mises à jour du stock | Lorsque la quantité de stock change dans Commerce. Channel Manager synchronise la mise à jour avec Walmart. | **Jusqu’à 10 minutes** |
| Mises à jour des prix | Lorsqu’un prix de produit change, Channel Manager synchronise la mise à jour avec Walmart. | **Jusqu’à 5 minutes** |
| Commande de synchronisations de Walmart vers Commerce | Le client commande un produit Commerce sur Walmart Marketplace. Walmart envoie la commande à Channel Manager. L’ordre s’affiche dans le tableau de bord de l’ordre. | **Jusqu’à 30 minutes** |
| Commande créée dans Commerce Order Management | Le Gestionnaire de canaux crée la commande Commerce à partir de la commande Walmart et met à jour le tableau de bord des commandes afin d’inclure le numéro de la commande Commerce. | **Jusqu’à 5 minutes** |

## Conditions préalables de Walmart

Vous avez besoin des informations suivantes de Walmart pour intégrer Commerce à Walmart Marketplace :

* Validation de la vente sur Walmart et informations d’identification pour se connecter au compte Seller Marketplace enregistré

* Clé API permettant de connecter Adobe Commerce ou Magento Open Source à Walmart Marketplace

   La clé d’API Walmart Marketplace permet l’intégration entre Channel Manager pour Adobe Commerce ou Magento Open Source et Walmart Marketplace. Configurez la clé API dans Seller Central avant de lancer le processus d’intégration du Gestionnaire de canaux.

### Configuration d’un compte Vendeur Marketplace

1. [Envoyer votre demande Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. Après avoir obtenu l&#39;accord de Walmart, [Configuration de votre compte Walmart Seller](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Génération d’une clé d’API Walmart Marketplace

1. Accédez à Walmart Marketplace pour générer un événement [clé d’API de production du fournisseur de solution pour Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Créez la clé et configurez les autorisations :

   * Sélectionnez Adobe comme fournisseur de solution.

   * Définissez les autorisations comme illustré dans le tableau suivant. Pour plus d’informations, voir [Informations d’identification de l’API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) dans le *Aide pour les vendeurs de Walmart Marketplace*.

|    **Configuration de la clé d’API d’Adobe pour Walmart**
| **Autorisation** | **Paramètre** | |—|—| | Contenu | Accès complet | | Obtention de flux | Afficher uniquement | | Inventaire | Accès complet | | Éléments | Accès complet | | Heure de relage | Accès complet | | Ordre | Accès complet | | Prix | Accès complet | | Rapports | Afficher uniquement | | Renvoie | Accès complet | | Règles | Accès complet | | Expédition | Accès complet |

## État du magasin Walmart Marketplace

Lorsque vous publiez des produits sur Walmart Marketplace, leur disponibilité dépend du statut de vos magasins Walmart Marketplace :

* Pour les magasins en direct, vos offres de produits sont répertoriées et disponibles à la vente dès que l’opération de correspondance est terminée.

* Pour les magasins qui ne sont pas en ligne, vos offres de produits sont mises en scène et ne sont pas visibles par les clients. Dès que le magasin est mis en ligne, les listes par étapes sont automatiquement transmises au magasin par étapes.


![[!DNL Walmart Seller Central] produits intermédiaires](assets/walmart-seller-central-staged.png)
