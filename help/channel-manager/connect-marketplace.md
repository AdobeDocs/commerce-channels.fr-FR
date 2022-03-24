---
title: 'Connecter Sales Channel à [!DNL Walmart Marketplace] '
description: Configurez le canal des ventes et connectez-vous à Walmart Marketplace.
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Se connecter à [!DNL Walmart Marketplace]

Après avoir installé Channel Manager sur votre [!DNL Commerce] Connectez un magasin Commerce à Walmart Marketplace, par exemple.

1. Créez le canal de vente par [sélection de la boutique Commerce pour les listes de produits](#select-the-commerce-store-for-the-sales-channel).

1. [Connectez le canal à [!DNL Walmart Marketplace] en ajoutant les informations d’identification de l’API Walmart](#connect-the-channel-to-walmart-marketplace).

1. [Finalisation de la configuration du canal de vente](#complete-store-setup) vous pouvez ainsi gérer les listes, les stocks, les prix et les ventes à partir de Channel Manager.

## Création du canal de vente

1. Ouvrez le Gestionnaire de canaux.

   - Dans Admin, sélectionnez **[!UICONTROL Marketing** > _Canaux _> **Gestionnaire de canaux]**.

   - Sélectionner **[!UICONTROL Connect New Store]**.

      ![Connecter Commerce Store à [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Configurez le magasin et la connexion :

   - Saisissez un **[!UICONTROL store name]**.

   - Sélectionnez la **[!UICONTROL Adobe Commerce site]** pour les listes de produits.

   - Ajoutez un **[!UICONTROL email address]** pour recevoir des notifications relatives au service [!DNL Channel Manager].

      ![Configurer la connexion entre Commerce et [!DNL Walmart Marketplace] de [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## Connexion du canal à Walmart Marketplace

1. Ajoutez les informations d’identification de la variable [!DNL Walmart Marketplace Adobe Production API key] de votre [!DNL Walmart Marketplace Seller] compte .

   - Si vous ne disposez pas des informations d’identification, sélectionnez **[!UICONTROL Get API credentials]** pour les obtenir à partir de la fonction [!DNL Walmart Marketplace Developer Portal].

      Si vous y êtes invité, sélectionnez votre région (États-Unis et Canada), puis connectez-vous.

      ![[!DNL Walmart Marketplace] connexion au compte](assets/walmart-marketplace-login-page.png)

   - Sur le formulaire de clé API, copiez et enregistrez le **[!UICONTROL Client ID]** et **[!UICONTROL Client Secret]** des valeurs de [!UICONTROL Adobe Inc Production API key] vers un emplacement sécurisé.

      ![[!DNL Walmart Marketplace API key] page de configuration](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Si vous ne voyez pas de [!DNL Adobe Inc] dans Developer Portal, sélectionnez **[!UICONTROL Add New Key for a Solution Provider]** pour configurer les autorisations et générer la clé. Pour plus d’informations sur la configuration, voir [Générer une [!DNL Walmart Marketplace API Key]](overview.md#generate-a-walmart-marketplace-api-key).

   - Revenir à [!DNL Channel Manager] pour ajouter les informations d’identification à la variable **[!UICONTROL Walmart Connection]** informations.

      Lorsque vous ajoutez des informations d’identification à [!DNL Channel Manager], Adobe masque le secret client et stocke la valeur dans un coffre sécurisé.

1. [!UICONTROL Save] la configuration pour établir la connexion.

   Une fois la connexion établie, gérez le canal à partir de **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] page de configuration](assets/manage-connected-stores.png)


### Résolution des problèmes de connexion

Si la connexion à Walmart échoue, reportez-vous à la section [FAQ sur Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} pour obtenir des conseils de dépannage.

- Dans la [!DNL Walmart Developer Portal], vérifiez que vous avez copié les informations d’identification correctes pour la clé d’API de production pour [!UICONTROL Adobe Inc.]

- Vérifiez que la configuration d’accès de la clé de l’API Walmart Adobe dispose des autorisations appropriées. Voir [Conditions préalables de Walmart](overview.md#walmart-prerequisites).

- Vérifiez que le service d’API Walmart est disponible à l’aide de la fonction [Page d’état de l’API Walmart](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.


## Configuration complète du magasin

Une fois que vous avez connecté une boutique Commerce à [!DNL Walmart Marketplace], vous pouvez terminer la configuration du magasin à partir de la fonction [!DNL Channel Manager Stores] vue.

Pour terminer la configuration du magasin :

1. Dans l’onglet Admin, sélectionnez **[!UICONTROL Marketing** > **Gestionnaire de canaux**].

   ![[!DNL Walmart Marketplace API key] page de configuration](assets/connect-commerce-store-config.png)

1. Ouvrez un canal de vente connecté en sélectionnant l’icône en forme de crayon dans une ligne d’entrée de magasin.

1. Lancer les opérations du canal de vente.

   - Ajout de produits de votre catalogue de commerce au Gestionnaire de canaux

   - Publication de produits sur Walmart à l’aide de la correspondance de produits

   - Affichage et gestion des stocks et des prix

   - Afficher et gérer les commandes Walmart depuis l’administrateur Commerce
