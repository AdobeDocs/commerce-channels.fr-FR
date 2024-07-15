---
title: 'Se connecter à [!DNL Commerce] Services'
description: Connectez le gestionnaire de canaux aux services  [!DNL Commerce] pour activer la synchronisation et la communication des données entre l’instance  [!DNL Commerce] , le gestionnaire de canaux et d’autres services annexes.'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Connexion à [!DNL Commerce] Services

[!DNL Commerce Services Connector] intègre le service Channel Manager aux instances Adobe Commerce et Magento Open Source. Le connecteur permet la synchronisation et la communication des données entre l’instance [!DNL Commerce], [!DNL Channel Manager] et d’autres services annexes.

[!DNL Commerce Services Connector] La configuration est un processus unique requis pour utiliser les [services Adobe Commerce SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) tels que [!DNL Channel Manager], [!DNL Live Search] et [!DNL Product Recommendations]. Si vous avez déjà configuré le connecteur pour un autre service, ignorez cette étape.

## Conditions

- **Compte Commerce** - Pour installer un logiciel sur des instances [!DNL Commerce], vous devez disposer d’un compte avec un accès propriétaire ou administrateur à la plateforme [!DNL Commerce].

  Les propriétaires de compte et les super utilisateurs peuvent créer des comptes d&#39;administrateur à partir de l&#39;instance [!DNL Commerce] ou de la ligne de commande à l&#39;aide de la commande [!DNL Commerce] CLI `admin:user:create`.

- **Clé d’API de production Adobe Commerce**-Cette [clé](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) permet à l’API d’accéder aux services requis par Channel Manager. Vous avez besoin des informations d’identification publiques et privées pour cette clé.

>[!TIP]
>
>Pour fournir les informations d’identification, un détenteur de licence ou propriétaire de compte [!DNL Commerce] a des options pour [partager l’accès](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html), ou donner les [clé API](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) à un développeur approuvé.

## Configurez le [!DNL Commerce Services Connector]

1. Ouvrez la configuration des services de magasin .

   - Dans l&#39;Admin, sélectionnez **[!UICONTROL Stores]**.

   - Sous *[!UICONTROL Settings]*, sélectionnez **[!UICONTROL Configuration]**.

   - Développez **[!UICONTROL Services]** et sélectionnez **[!UICONTROL Commerce Services Connector]**.

1. Ajoutez les informations d’identification de clé de l’API de production de votre compte Adobe Commerce.

   Service ![[!DNL Commerce Services Connector] dans la vue [!DNL Admin]](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Si d’autres services [!DNL Adobe Commerce] tels que [!DNL Live Search] ou [!DNL Product Recommendations] sont installés sur votre instance [!DNL Commerce], les informations d’identification s’affichent dans l’interface et aucune configuration supplémentaire n’est requise.

1. Configurez le projet SaaS et l’espace de données afin que les services Commerce puissent envoyer des données au service de gestionnaire de canaux.

   ![[!DNL Commerce Services Connector] Configuration de l’identifiant SaaS dans la vue [!DNL Admin]](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

