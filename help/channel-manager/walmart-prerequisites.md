---
title: Conditions préalables de Walmart
description: Vérifiez que vous disposez des informations et des ressources nécessaires à l’intégration de Walmart Marketplace avec Channel Manager.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Conditions préalables de Walmart

Le gestionnaire de canaux nécessite les ressources et informations suivantes pour configurer un canal de vente Commerce pour Walmart Marketplace.

* Validation de la vente sur Walmart et informations d’identification pour se connecter au compte Seller Marketplace enregistré

* Clé API permettant de connecter Adobe Commerce ou Magento Open Source à Walmart Marketplace

   La clé d’API Walmart Marketplace permet l’intégration entre Channel Manager pour Adobe Commerce ou Magento Open Source et Walmart Marketplace. Configurez la clé API dans Seller Central avant de lancer le processus d’intégration du Gestionnaire de canaux.

## Configuration d’un compte Vendeur Marketplace

1. [Envoyer votre demande Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
1. Après avoir obtenu l&#39;accord de Walmart, [Configuration de votre compte Walmart Seller](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Génération d’une clé d’API Walmart Marketplace

1. Accédez à Walmart Marketplace pour générer un événement [clé d’API de production du fournisseur de solution pour Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Créez la clé et configurez les autorisations :

   * Sélectionnez Adobe comme fournisseur de solution.

   * Définissez les autorisations comme illustré dans le tableau suivant. Pour plus d’informations, voir [Informations d’identification de l’API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) dans le _Aide pour les vendeurs de Walmart Marketplace_.

|    **Configuration de la clé d’API d’Adobe pour Walmart**
| **Autorisation** | **Paramètre** | |—|—| | Contenu | Accès complet | | Obtention de flux | Afficher uniquement | | Inventaire | Accès complet | | Éléments | Accès complet | | Heure de relage | Accès complet | | Ordre | Accès complet | | Prix | Accès complet | | Rapports | Afficher uniquement | | Renvoie | Accès complet | | Règles | Accès complet | | Expédition | Accès complet |

## État du magasin Walmart Marketplace

Lorsque vous publiez des produits sur Walmart Marketplace, leur disponibilité dépend du statut de vos magasins Walmart Marketplace :

* Pour les magasins en direct, vos offres de produits sont répertoriées et disponibles à la vente une fois l’opération de correspondance terminée.

* Pour les magasins qui ne sont pas en ligne, vos offres de produits sont mises en scène et ne sont pas visibles par les clients. Lorsque le magasin est mis en ligne, les listes par étapes sont automatiquement transférées vers le magasin par étape.

![[!DNL Walmart Seller Central] produits intermédiaires](assets/walmart-seller-central-staged.png)
