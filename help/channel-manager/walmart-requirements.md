---
title: '[!DNL Walmart] Exigences'
description: 'Vérifiez que vous disposez des  [!DNL Walmart Marketplace]informations et des ressources nécessaires pour l’intégration avec le Gestionnaire de canaux.'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!DNL Walmart] Exigences

[!DNL Channel Manager] nécessite les ressources et informations suivantes pour configurer un canal de vente [!DNL Commerce] pour [!DNL Walmart Marketplace.]

* Un compte de vendeur [!DNL Walmart]

* Une clé API pour connecter Adobe Commerce ou Magento Open Source à [!DNL Walmart Marketplace]

  La clé d&#39;API [!DNL Walmart Marketplace] permet l&#39;intégration entre [!DNL Channel Manager] pour Adobe [!DNL Commerce] ou Magento Open Source et Walmart Marketplace. Configurez la clé API dans Seller Central avant de lancer le processus d’intégration du Gestionnaire de canaux.

## Configuration d&#39;un compte [!DNL Walmart Seller]

Accédez à [!DNL Walmart Seller Center] pour configurer votre [compte Walmart Seller](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Générer une clé d’API de production [!DNL Walmart Marketplace]

1. Accédez à [!DNL Walmart Marketplace] pour générer une [ clé d&#39;API de production du fournisseur de solution pour Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Créez la clé et configurez les autorisations :

   * Sélectionnez Adobe comme fournisseur de solution.

   * Définissez les autorisations comme illustré dans le tableau suivant. Pour plus d’informations, reportez-vous à la section [Informations d’identification de l’API](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) dans l’ _aide du vendeur Walmart Marketplace_.

   **Configuration de clé API d’Adobe pour Walmart**

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

Lorsque vous connectez des produits au marché, la disponibilité des listes dépend de l’état de vos magasins [!DNL Walmart Marketplace] :

* Pour les magasins en direct, vos offres de produits sont répertoriées et disponibles à la vente une fois l’opération de correspondance terminée.

* Pour les magasins qui ne sont pas en ligne, vos offres de produits sont mises en scène et ne sont pas visibles par les clients. Lorsque le magasin [!DNL Walmart Marketplace] est en ligne, les listes par étapes sont automatiquement transférées vers le magasin en ligne.

![[!DNL Walmart Seller Central] produits intermédiaires](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>Une fois [!DNL Channel Manager] installé et configuré, toutes les mises à jour de stock, de prix et de commande sont synchronisées automatiquement. Ne connectez pas [!DNL Channel Manager] à un magasin Walmart Marketplace actif tant que vous n’avez pas désactivé les autres intégrations qui mettent à jour les données de produit et de commande. Si d’autres intégrations ont été configurées, vérifiez que la quantité et les prix de l’article dans [!DNL Commerce] correspondent aux quantités dans [!DNL Walmart Marketplace] avant de vous connecter à un magasin en ligne.

