---
title: Se connecter à [!DNL Commerce] services
description: Connectez le Gestionnaire de canaux à [!DNL Commerce] des services permettant la synchronisation et la communication des données entre les [!DNL Commerce] , Channel Manager et d’autres services annexes.
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 30495c4e47f15c821206f7b0252b868b4e27d62d
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# Se connecter à [!DNL Commerce] services

Commerce Services Connector intègre le service Channel Manager aux instances Adobe Commerce et Magento Open Source. Le connecteur permet la synchronisation et la communication des données entre les [!DNL Commerce] instance, [!DNL Channel Manager], ainsi que d’autres services annexes.

La configuration du connecteur de Commerce Services est un processus unique requis pour utiliser Adobe. [Services SaaS de commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} comme [!DNL Channel Manager], [!DNL Live Search], et [!DNL Product Recommendations]. Si vous avez déjà configuré le connecteur pour un autre service, ignorez cette étape.

## Conditions préalables

- **Compte Commerce**- Pour installer un logiciel sur les instances de Commerce, vous devez disposer d’un compte avec un accès propriétaire ou administrateur à la plateforme Commerce.

   Les propriétaires de compte et les utilisateurs administrateurs peuvent créer des comptes d’administrateur à partir de l’instance Commerce ou de la ligne de commande à l’aide de la fonction [!DNL Commerce] Commande CLI `admin:user:create`.

- **Clé d’API de production Adobe Commerce**-This [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} permet l’accès à l’API aux services requis par le gestionnaire de canaux. Vous avez besoin des informations d’identification publiques et privées pour cette clé.

>[!TIP]
>
>Pour fournir les informations d’identification, un détenteur de licence Commerce ou un propriétaire de compte a la possibilité de [accès au partage](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} ou indiquez la variable [Clé API](https://docs.magento.com/user-guide/system/saas.html#apikey)Informations d’identification {target=&quot;_blank&quot;} à un développeur approuvé.

## Configuration du connecteur Commerce Services

1. Ouvrez la configuration des services de magasin .

   - Dans l’onglet Admin, sélectionnez **[!UICONTROL Stores]**.

   - Sous *[!UICONTROL Settings]*, sélectionnez **[!UICONTROL Configuration]**.

   - Développer **[!UICONTROL Services]** et sélectionnez **[!UICONTROL Commerce Services Connector]**.

1. Ajoutez les informations d’identification de clé de l’API de production de votre compte Adobe Commerce.

   ![[!DNL Commerce Service Connector] dans le [!DNL Admin] view](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Si votre [!DNL Commerce] instance comporte une autre instance [!DNL Adobe Commerce] services tels que [!DNL Live Search] ou [!DNL Product Recommendations] installé, les informations d’identification s’affichent dans l’interface et aucune configuration supplémentaire n’est requise.

1. Configurez le projet SaaS et l’espace de données afin que Commerce Services puisse envoyer des données au service de gestionnaire de canaux.

   ![[!DNL Commerce Service Connector] Configuration de l’identifiant SaaS dans la variable [!DNL Admin] view](assets/commerce-services-connector-saas-config.png)

