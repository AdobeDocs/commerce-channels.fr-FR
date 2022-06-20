---
title: '"[!DNL Walmart] Conditions requises"'
description: '"Vérifiez que vous disposez des[!DNL Walmart Marketplace]informations et ressources à intégrer à Channel Manager."'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 07e1faf90676b404e3f5ee28ddc13d81ea82a5a5
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# [!DNL Walmart] conditions requises

[!DNL Channel Manager] nécessite les ressources et informations suivantes pour configurer une [!DNL Commerce] canal de vente pour [!DNL Walmart Marketplace.]

* Validation de la vente [!DNL Walmart] et informations d’identification pour se connecter au compte Seller Marketplace enregistré.

* Clé API permettant de connecter Adobe Commerce ou Magento Open Source à [!DNL Walmart Marketplace]

   Le [!DNL Walmart Marketplace] La clé API permet l’intégration entre [!DNL Channel Manager] pour Adobe Commerce ou Magento Open Source et Walmart Marketplace. Configurez la clé API dans Seller Central avant de lancer le processus d’intégration du Gestionnaire de canaux.

## Configurez une [!DNL Walmart Seller] account

1. [Envoyer votre demande Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Après avoir obtenu l’approbation de [!DNL Walmart], [Configuration de votre compte Walmart Seller](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Générer une [!DNL Walmart Marketplace] Clé d’API de production

1. Accédez à [!DNL Walmart Marketplace] pour générer un [clé d’API de production du fournisseur de solution pour Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Créez la clé et configurez les autorisations :

   * Sélectionnez Adobe comme fournisseur de solution.

   * Définissez les autorisations comme illustré dans le tableau suivant. Pour plus d’informations, voir [Informations d’identification de l’API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) dans le _Aide pour les vendeurs de Walmart Marketplace_.

   **Configuration de la clé d’API d’Adobe pour Walmart**

   | **Autorisation** | **Paramètre** |
   |----------------|-------------|
   | Contenu | Accès complet |
   | Obtention de flux | Afficher uniquement |
   | Inventaire | Accès complet |
   | Éléments | Accès complet |
   | Heure de latence | Accès complet |
   | Commande | Accès complet |
   | Prix | Accès complet |
   | Rapports | Afficher uniquement |
   | Renvoie | Accès complet |
   | Règles | Accès complet |
   | Expédition | Accès complet |

## [!DNL Walmart Marketplace] État du magasin

Lorsque vous connectez des produits à la marketplace, la disponibilité de la liste dépend de l’état de votre [!DNL Walmart Marketplace] stores :

* Pour les magasins en direct, vos offres de produits sont répertoriées et disponibles à la vente une fois l’opération de correspondance terminée.

* Pour les magasins qui ne sont pas en ligne, vos offres de produits sont mises en scène et ne sont pas visibles par les clients. Lorsque la variable [!DNL Walmart Marketplace] le magasin est mis en ligne, les listes par étapes sont automatiquement transférées vers le magasin en ligne.

![[!DNL Walmart Seller Central] produits intermédiaires](assets/walmart-seller-central-staged.png)

>[!IMPORTANT]
>
>Après [!DNL Channel Manager] est installé et configuré, tous les stocks, prix et mises à jour de commande sont synchronisés automatiquement. Ne connectez pas Channel Manager à un magasin Walmart Marketplace actif tant que vous n’avez pas désactivé les autres intégrations qui mettent à jour les données de produit et de commande et que vous êtes prêt à synchroniser les mises à jour Commerce avec . [!DNL Walmart Marketplace].

