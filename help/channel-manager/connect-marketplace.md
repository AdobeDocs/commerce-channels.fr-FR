---
title: Connexion du canal de vente à [!DNL Walmart Marketplace]
description: Configurez le canal des ventes et connectez-vous à Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 06affb78c30086e11dd9ead70e6538ef3d1ff95b
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Connexion du canal de vente à [!DNL Walmart Marketplace]

Après avoir installé Channel Manager sur votre [!DNL Commerce] Connectez un magasin Commerce à Walmart Marketplace, par exemple.

1. [Création du canal de vente](#create-the-sales-channel) en sélectionnant Commerce store pour les listes de produits.

1. [Connectez le canal à [!DNL Walmart Marketplace] en ajoutant les informations d’identification de l’API Walmart](#connect-the-channel-to-walmart-marketplace).

1. [Finalisation de la configuration du canal de vente](#complete-store-setup) pour gérer les listes, les stocks, les prix et les commandes de votre gamme de produits Walmart Marketplace.

## Création du canal de vente

1. Ouvrir [!DNL Channel Manager].

   - Dans Admin, sélectionnez **[!UICONTROL Marketing** > _Canaux _> **Gestionnaire de canaux]**.

   - Sélectionner **[!UICONTROL Connect New Store]**.

      ![Connecter Commerce Store à [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)

1. Sur la page d’accueil du Gestionnaire de canaux dans la [!UICONTROL Marketplaces available to connect] , sélectionnez [!UICONTROL Get Started].

   ![Connectez le nouveau magasin Walmart à [!DNL Channel Manager]](assets/channel-manager-home.png)

1. Si nécessaire, configurez votre compte Walmart Marketplace Seller.

1. Configurez le magasin et la connexion :

   - Sélectionner **[!UICONTROL Add Credentials]**.

      ![Configurer la connexion entre Commerce et [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - Sélectionnez la vue Commerce store pour vous connecter au marketplace.

   - Saisissez un **[!UICONTROL store name]**.

   - Sélectionnez la **[!UICONTROL Adobe Commerce site]** pour les listes de produits.

   - Ajoutez un **[!UICONTROL email address]** pour recevoir des notifications relatives au service [!DNL Channel Manager].

1. Connectez le canal à [!DNL Walmart Marketplace].

   - Ajoutez les informations d’identification de la variable [[!DNL Walmart Marketplace Adobe Production API key]](walmart-prerequisites.md#generate-a-walmart-marketplace-production-api-key) de votre [!DNL Walmart Marketplace Seller] compte .

   - Si vous ne disposez pas des informations d’identification, sélectionnez **[!UICONTROL Get API credentials]** pour les obtenir à partir de la fonction [!DNL Walmart Marketplace Developer Portal].

      Si vous y êtes invité, sélectionnez votre région (États-Unis et Canada), puis connectez-vous.

      ![[!DNL Walmart Marketplace] connexion au compte](assets/walmart-marketplace-login-page.png)

   - Sur le formulaire de clé API, copiez et enregistrez le **[!UICONTROL Client ID]** et **[!UICONTROL Client Secret]** des valeurs de [!UICONTROL Adobe Inc Production API key] vers un emplacement sécurisé.

      ![[!DNL Walmart Marketplace API key] page de configuration](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Si la variable [!DNL Adobe Inc] La clé n’est pas répertoriée dans Developer Portal, sélectionnez **[!UICONTROL Add New Key for a Solution Provider]** pour configurer les autorisations et générer la clé. Pour plus d’informations sur la configuration, voir [Générer une [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - Revenir à [!DNL Channel Manager] pour ajouter les informations d’identification à la variable **[!UICONTROL Walmart Connection]** informations.

      Lorsque vous ajoutez des informations d’identification à [!DNL Channel Manager], Adobe masque le secret client et stocke la valeur dans un coffre sécurisé.

1. Sélectionner **[!UICONTROL Save Store]** pour appliquer la configuration et vous connecter à la fonction [!DNL Walmart marketplace].

Une fois la connexion établie, gérez le canal à partir de **[!UICONTROL Channel Manager > Marketplace Stores]**.

![Configuration du premier magasin](assets/channel-manager-setup-first-store.png)

### Résolution des problèmes de connexion

Si la connexion à Walmart échoue, reportez-vous à la section [FAQ sur Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} pour obtenir des conseils de dépannage.

- Dans la [!DNL Walmart Developer Portal], vérifiez que vous avez copié les informations d’identification correctes pour la clé d’API de production pour [!UICONTROL Adobe Inc.]

- Vérifiez que la configuration d’accès de la clé de l’API Walmart Adobe dispose des autorisations appropriées. Voir [Conditions préalables de Walmart](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Confirmez que la variable [!DNL Walmart API] est disponible à partir de la fonction [Page d’état de l’API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.

## Configuration complète du magasin

Une fois que vous avez connecté une boutique Commerce à [!DNL Walmart Marketplace], vous pouvez terminer la configuration du magasin à partir de la fonction [!DNL Channel Manager Stores] vue.

Pour terminer la configuration du magasin :

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing** > **Gestionnaire de canaux**].

   ![Configuration du premier magasin](assets/channel-manager-setup-first-store.png)

1. Ouvrez le magasin en cliquant sur l’icône représentant un oeil dans la colonne située à l’extrême droite.

1. Lancer les opérations du canal de vente.

   - [Ajout de produits de votre catalogue de commerce au Gestionnaire de canaux](add-products-to-connected-channel.md)

   - [Publication de produits sur Walmart à l’aide de la correspondance de produits](publish-listings-to-marketplace.md)

   - [Affichage et gestion des stocks et des prix](inventory-and-price-updates.md)

   - [Afficher et gérer les commandes Walmart depuis l’administrateur Commerce](manage-orders.md)
