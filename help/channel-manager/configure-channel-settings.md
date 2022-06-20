---
title: Configuration des paramètres de canal
description: Configurez le Gestionnaire de canaux et les paramètres des canaux de vente pour l’authentification, mappez les attributs de catalogue et les opérateurs de livraison requis pour coordonner les opérations de vente entre [!DNL Commerce] et le [!DNL Walmart Marketplace].
source-git-commit: 5c478813af442a4e54cb5c64045698f04d710c9a
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# Configuration des paramètres du canal de vente

Les paramètres du canal de vente permettent la communication et la synchronisation des données entre [!DNL Commerce] et [!DNL Walmart Marketplace] afin que vous puissiez gérer [!DNL Walmart Marketplace] les opérations commerciales de la [!DNL Commerce] Administrateur :

Dans [!DNL Channel Manager], vous configurez certains paramètres de canaux de vente au cours du processus d’intégration. Après l’intégration, vous pouvez afficher et gérer la configuration du canal à partir de la *[!UICONTROL Channel Settings]* page.

- **[Mapper les identifiants uniques](map-catalog-attributes.md)**- Avant de connecter des listes à partir de [!DNL Commerce] to [!DNL Walmart Marketplace], mappez au moins un identifiant unique à partir de votre [!DNL Commerce] Catalogue à l’identifiant correspondant de [!DNL Walmart]. Cette étape doit correspondre à [!DNL Commerce] produits existants [!DNL Walmart] listes et pour synchroniser les données de produit entre [!DNL Commerce] et [!DNL Walmart].

- **[Cartographier les opérateurs de livraison](map-shipping-carriers.md)**-Avant traitement [!DNL Walmart Marketplace] commandes de [!DNL Commerce], assurez-vous de mapper les opérateurs de transport à partir de votre [!DNL Commerce] instance aux opérateurs correspondants sur [!DNL Walmart Marketplace].

- **Informations d’identification de l’API Walmart**: pendant la [!DNL Channel Manager] processus d’intégration, vous fournissez la variable [Informations d’identification de l’API Walmart](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de votre [!DNL Walmart Marketplace Seller] compte à connecter [!DNL Commerce] to [!DNL Walmart Marketplace] pour la communication et la synchronisation des données. Si nécessaire, vous pouvez [mettre à jour ces informations d’identification](manage-wmt-connection.md) de la _[!UICONTROL Channel Settings]_page.
