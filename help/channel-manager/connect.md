---
title: '''Se connecter à [!DNL Commerce] Services'
description: "Connectez le gestionnaire de canaux à [!DNL Commerce] des services permettant la synchronisation et la communication des données entre les [!DNL Commerce] , Channel Manager et d’autres services annexes."
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Se connecter à [!DNL Commerce] Services

Le [!DNL Commerce Services Connector] intègre le service Channel Manager aux instances Adobe Commerce et Magento Open Source. Le connecteur permet la synchronisation et la communication des données entre les [!DNL Commerce] instance, [!DNL Channel Manager], ainsi que d’autres services annexes.

[!DNL Commerce Services Connector] La configuration est un processus unique nécessaire à l’utilisation de [Services Adobe Commerce SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) par exemple [!DNL Channel Manager], [!DNL Live Search], et [!DNL Product Recommendations]. Si vous avez déjà configuré le connecteur pour un autre service, ignorez cette étape.

## Conditions

- **Compte Commerce**-Pour installer le logiciel sur [!DNL Commerce] , vous devez disposer d’un compte avec un accès propriétaire ou administrateur au [!DNL Commerce] plateforme.

  Les propriétaires de compte et les super utilisateurs peuvent créer des comptes d’administration à partir de la variable [!DNL Commerce] ou à partir de la ligne de commande à l’aide de la fonction [!DNL Commerce] Commande CLI `admin:user:create`.

- **Clé d’API de production Adobe Commerce**-This [key](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) permet l’accès aux API aux services requis par Channel Manager. Vous avez besoin des informations d’identification publiques et privées pour cette clé.

>[!TIP]
>
>Pour fournir les informations d’identification, une [!DNL Commerce] le détenteur de licence ou le propriétaire de compte a la possibilité de [accès au partage](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html), ou donnez à la variable [Clé API](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) informations d’identification à un développeur de confiance.

## Configurez la variable [!DNL Commerce Services Connector]

1. Ouvrez la configuration des services de magasin .

   - Dans l’onglet Admin, sélectionnez **[!UICONTROL Stores]**.

   - Sous *[!UICONTROL Settings]*, sélectionnez **[!UICONTROL Configuration]**.

   - Développer **[!UICONTROL Services]** et sélectionnez **[!UICONTROL Commerce Services Connector]**.

1. Ajoutez les informations d’identification de clé de l’API de production de votre compte Adobe Commerce.

   ![[!DNL Commerce Services Connector] dans le [!DNL Admin] view](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Si votre [!DNL Commerce] instance comporte une autre instance [!DNL Adobe Commerce] services tels que [!DNL Live Search] ou [!DNL Product Recommendations] installé, les informations d’identification s’affichent dans l’interface et aucune configuration supplémentaire n’est requise.

1. Configurez le projet SaaS et l’espace de données afin que Commerce Services puisse envoyer des données au service de gestionnaire de canaux.

   ![[!DNL Commerce Services Connector] Configuration de l’identifiant SaaS dans la variable [!DNL Admin] view](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

