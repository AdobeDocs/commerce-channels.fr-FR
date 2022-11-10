---
title: '''[!DNL Walmart] Conditions requises'
description: "Vérifiez que vous disposez des [!DNL Walmart Marketplace]informations et ressources à intégrer à Channel Manager."
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: fd60c8917e4b4e155fb2897ade6e1d96aff2de9d
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# [!DNL Walmart] conditions requises

[!DNL Channel Manager] nécessite les ressources et informations suivantes pour configurer une [!DNL Commerce] canal de vente pour [!DNL Walmart Marketplace.]

* Validation de la vente [!DNL Walmart] et informations d’identification pour se connecter au compte Seller Marketplace enregistré.

* Clé API permettant de connecter Adobe Commerce ou Magento Open Source à [!DNL Walmart Marketplace]

   Le [!DNL Walmart Marketplace] La clé API permet l’intégration entre [!DNL Channel Manager] pour l’Adobe [!DNL Commerce] ou Magento Open Source et le Walmart Marketplace. Configurez la clé API dans Seller Central avant de lancer le processus d’intégration du Gestionnaire de canaux.

## Configurez une [!DNL Walmart Seller] account

1. [Envoyer votre demande Walmart Seller](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Après avoir obtenu l’approbation de [!DNL Walmart], [Configuration de votre compte Walmart Seller](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

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
>Après [!DNL Channel Manager] est installé et configuré, toutes les mises à jour de stock, de prix et de commande sont synchronisées automatiquement. Ne pas se connecter [!DNL Channel Manager] dans un magasin Walmart Marketplace en direct jusqu’à ce que vous ayez désactivé toutes les autres intégrations qui mettent à jour les données de produit et de commande. Si d’autres intégrations ont été configurées, vérifiez la quantité et les prix de l’article dans [!DNL Commerce] correspondent aux quantités en [!DNL Walmart Marketplace] avant de se connecter à un magasin en direct.

