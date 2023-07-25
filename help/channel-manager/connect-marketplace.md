---
title: 'Connect [!DNL Channel Manager] to [!DNL Walmart Marketplace]'
description: "Connexion d’une vue Commerce Store à [!DNL Walmart Marketplace] pour créer le canal des ventes afin de gérer les listes de produits Commerce, l’inventaire, le prix et les commandes pour les ventes de Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Connexion [!DNL Channel Manager] to [!DNL Walmart Marketplace]

Après avoir installé Channel Manager sur votre [!DNL Commerce] créez un canal de vente dans le Gestionnaire de canaux et configurez les informations d’identification pour vous connecter. [!DNL Channel Manager] to [!DNL Walmart Marketplace].

1. [Création du canal de vente](#create-the-sales-channel) en sélectionnant l’option [!DNL Commerce] magasin pour les listes de produits.

1. [Connectez le canal à [!DNL Walmart Marketplace] en ajoutant [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Finalisation de la configuration du canal de vente](#complete-sales-channel-store-setup) pour gérer les listes, les stocks, les prix et les commandes pour vos [!DNL Walmart Marketplace] assortiment de produits.

>[!NOTE]
>
>Le gestionnaire de canaux requiert une connexion un-à-un entre un compte Walmart et un [!DNL Commerce] vue de magasin. Vous ne pouvez pas connecter la même vue de magasin à plusieurs comptes Walmart.

## Création du canal de vente

1. Depuis l’administrateur, ouvrez [!DNL Channel Manager] en sélectionnant **[!UICONTROL Marketing** > _Canaux _> **Gestionnaire de canaux]**.

1. Dans le **[!UICONTROL Marketplaces available to connect]** , sélectionnez **[!UICONTROL Get Started]**.

   ![Se connecter à nouveau [!DNL Walmart] stocker dans [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Si nécessaire, configurez votre [!DNL Walmart Marketplace Seller] compte .

1. Configurez le magasin et la connexion :

   - Sélectionner **[!UICONTROL Add Credentials]**.

   - Sélectionnez la [!DNL Commerce] vue de magasin qui offre les produits que vous souhaitez vendre sur le marché.

     ![Configurer la connexion entre [!DNL Commerce] et [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Saisissez un **[!UICONTROL store name]**.

   - Sélectionnez la **[!UICONTROL Adobe [!DNL Commerce] site]** pour les listes de produits et le traitement des commandes.

   - Pour recevoir des notifications relatives à [!DNL Channel Manager], ajoutez une **[!UICONTROL email address]**.

1. Connectez le canal à [!DNL Walmart Marketplace].

   - Ajoutez les informations d’identification de la variable [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de votre [!DNL Walmart Marketplace Seller] compte .

   - Si vous ne disposez pas des informations d’identification, récupérez-les à partir de la [!DNL Walmart Marketplace Developer Portal] en sélectionnant **[!UICONTROL Get API credentials]**.

     Sur Developer Portal, sélectionnez votre région (États-Unis et Canada), puis connectez-vous.

     ![[!DNL Walmart Marketplace] connexion au compte](assets/walmart-marketplace-login-page.png){width="600"}

   - Sur le formulaire de clé API, copiez et enregistrez le **[!UICONTROL Client ID]** et **[!UICONTROL Client Secret]** des valeurs de [!UICONTROL Adobe Inc Production API key] vers un emplacement sécurisé.

     ![[!DNL Walmart Marketplace API key] page de configuration](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Si la variable [!DNL Adobe Inc] La clé n’est pas répertoriée dans Developer Portal, sélectionnez **[!UICONTROL Add New Key for a Solution Provider]** pour configurer les autorisations et générer la clé. Pour plus d’informations sur la configuration, voir [Générer une [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Revenir à [!DNL Channel Manager] pour ajouter les informations d’identification à la variable **[!UICONTROL Walmart Connection]** informations.

     Lorsque vous ajoutez des informations d’identification, Adobe masque le secret client et stocke la valeur dans un coffre sécurisé.

1. Sélectionner **[!UICONTROL Save Store]** pour appliquer la configuration et vous connecter à la fonction [!DNL Walmart marketplace].

1. Une fois la connexion établie, [configuration complète du magasin](complete-sales-channel-store-setup.md) de la **[!UICONTROL Channel Manager]** page de stockage.

![Configuration du premier magasin](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Résolution des problèmes de connexion

Si la connexion à [!DNL Walmart] échec, voir [FAQ sur Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} pour obtenir des conseils de dépannage.

- Dans la [!DNL Walmart Developer Portal], vérifiez que vous avez copié les informations d’identification correctes pour la clé d’API de production pour [!UICONTROL Adobe Inc.]

- Vérifiez que la configuration d’accès pour la variable [!UICONTROL Walmart Adobe API key] dispose des autorisations appropriées. Voir [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Confirmez que la variable [!DNL Walmart API] est disponible à partir de la fonction [Page d’état de l’API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
