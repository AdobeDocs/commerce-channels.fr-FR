---
title: 'Connect [!DNL Channel Manager] to [!DNL Walmart Marketplace]'
description: "Connectez une vue de magasin Commerce à  [!DNL Walmart Marketplace] pour créer le canal de vente afin de gérer les listes de produits, les stocks, les prix et les commandes Commerce pour les ventes de Walmart Marketplace."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Connectez [!DNL Channel Manager] à [!DNL Walmart Marketplace]

Après avoir installé le gestionnaire de canaux sur votre instance [!DNL Commerce], créez un canal de vente dans le gestionnaire de canaux et configurez les informations d’identification pour connecter [!DNL Channel Manager] à [!DNL Walmart Marketplace].

1. [Créez le canal de vente](#create-the-sales-channel) en sélectionnant le magasin [!DNL Commerce] pour les listes de produits.

1. [Connectez le canal à  [!DNL Walmart Marketplace]  en ajoutant [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [ Configurez le canal de vente ](#complete-sales-channel-store-setup) pour gérer les listes, les stocks, les prix et les commandes de votre gamme de produits [!DNL Walmart Marketplace].

>[!NOTE]
>
>Le gestionnaire de canaux nécessite une connexion un-à-un entre un compte Walmart et une vue de magasin [!DNL Commerce]. Vous ne pouvez pas connecter la même vue de magasin à plusieurs comptes Walmart.

## Création du canal de vente

1. Depuis l’administrateur, ouvrez [!DNL Channel Manager] en sélectionnant **[!UICONTROL Marketing** > _Canaux _> **Gestionnaire de canaux]**.

1. Dans la section **[!UICONTROL Marketplaces available to connect]**, sélectionnez **[!UICONTROL Get Started]**.

   ![ Connecter le nouveau [!DNL Walmart] magasin à [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Si nécessaire, configurez votre compte [!DNL Walmart Marketplace Seller].

1. Configurez le magasin et la connexion :

   - Sélectionnez **[!UICONTROL Add Credentials]**.

   - Sélectionnez la vue de magasin [!DNL Commerce] qui offre les produits que vous souhaitez vendre sur la marketplace.

     ![Configurer la connexion entre [!DNL Commerce] et [!DNL Walmart Marketplace] à partir de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Saisissez un **[!UICONTROL store name]** unique.

   - Sélectionnez le **[!UICONTROL Adobe [!DNL Commerce] site]** pour les listes de produits et le traitement des commandes.

   - Pour recevoir des notifications relatives à [!DNL Channel Manager], ajoutez un **[!UICONTROL email address]**.

1. Connectez le canal à [!DNL Walmart Marketplace].

   - Ajoutez les informations d’identification pour [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) de votre compte [!DNL Walmart Marketplace Seller].

   - Si vous ne disposez pas des informations d’identification, obtenez-les de l’ [!DNL Walmart Marketplace Developer Portal] en sélectionnant **[!UICONTROL Get API credentials]**.

     Sur Developer Portal, sélectionnez votre région (États-Unis et Canada), puis connectez-vous.

     ![[!DNL Walmart Marketplace] connexion au compte ](assets/walmart-marketplace-login-page.png){width="600"}

   - Sur le formulaire de clé d’API, copiez et enregistrez les valeurs **[!UICONTROL Client ID]** et **[!UICONTROL Client Secret]** pour le [!UICONTROL Adobe Inc Production API key] à un emplacement sécurisé.

     ![[!DNL Walmart Marketplace API key] page de configuration](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Si la clé [!DNL Adobe Inc] n’est pas répertoriée dans Developer Portal, sélectionnez **[!UICONTROL Add New Key for a Solution Provider]** pour configurer les autorisations et générer la clé. Pour plus d’informations sur la configuration, voir [Générer un [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Revenez à [!DNL Channel Manager] pour ajouter les informations d’identification à **[!UICONTROL Walmart Connection]**.

     Lorsque vous ajoutez des informations d’identification, Adobe masque le secret client et stocke la valeur dans un coffre sécurisé.

1. Sélectionnez **[!UICONTROL Save Store]** pour appliquer la configuration et vous connecter à [!DNL Walmart marketplace].

1. Une fois la connexion établie, [effectuez la configuration du magasin](complete-sales-channel-store-setup.md) à partir de la page de magasin **[!UICONTROL Channel Manager]**.

![Configurer le premier magasin](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Résolution des problèmes de connexion

Si la connexion à [!DNL Walmart] échoue, consultez la [FAQ Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} pour obtenir des conseils de dépannage.

- Depuis [!DNL Walmart Developer Portal], vérifiez que vous avez copié les informations d’identification correctes pour la clé API de production pour [!UICONTROL Adobe Inc.].

- Vérifiez que la configuration d’accès pour [!UICONTROL Walmart Adobe API key] dispose des autorisations appropriées. Voir [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Vérifiez que le service [!DNL Walmart API] est disponible à partir de la [page d&#39;état de l&#39;API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
