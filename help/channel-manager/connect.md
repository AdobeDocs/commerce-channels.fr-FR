---
title: Connexion à Commerce Services
description: Connectez l’instance du gestionnaire de canaux à [!DNL Commerce services] pour activer la synchronisation et la communication des données entre l’instance Commerce, le gestionnaire de canaux et d’autres services annexes.
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Connexion à Commerce Services

Commerce Services Connector intègre le service Channel Manager aux instances Adobe Commerce et Magento Open Source. Le connecteur permet la synchronisation et la communication des données entre les [!DNL Commerce] instance, [!DNL Channel Manager], ainsi que d’autres services annexes.

La configuration de Commerce Services Connector est un processus unique requis pour utiliser Adobe. [Services SaaS de commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} comme [!DNL Channel Manager], [!DNL Live Search], et [!DNL Product Recommendations]. Si vous avez déjà configuré le connecteur pour un autre service, vous pouvez ignorer cette étape.

## Conditions préalables

- **Compte Commerce avec [Accès administrateur](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** à votre instance de commerce** - Les propriétaires de compte et les utilisateurs administrateurs peuvent configurer des comptes d’utilisateurs à partir de l’instance de commerce ou à partir de la ligne de commande à l’aide de la fonction [!DNL Commerce] Commande CLI `admin:user:create`.

- **Adobe Commerce [Clés d’API de production](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}**- Activation de l’accès aux API pour les services requis par Channel Manager

   Pour fournir les informations d’identification, un détenteur de licence Commerce ou un propriétaire de compte a la possibilité de
   [accès au partage](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} ou indiquez la variable [Clé API](https://docs.magento.com/user-guide/system/saas.html#apikey)Informations d’identification {target=&quot;_blank&quot;} à un développeur approuvé.

## Configuration du connecteur Commerce Services

1. Ouvrez la configuration des services de magasin .

   - Dans l’onglet Admin, sélectionnez [!UICONTROL Stores].

   - Sous *Paramètres*, sélectionnez [!UICONTROL Configuration].

   - Sur le [!UICONTROL Configuration] page, développer [!UICONTROL Services] et sélectionnez [!UICONTROL Commerce Services Connector].

1. Ajoutez des clés d’API de production à partir de votre compte Adobe Commerce.

   ![[!DNL Commerce Service Connector] dans le [!DNL Admin] view](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Si votre [!DNL Commerce] instance comporte une autre instance [!DNL Adobe Commerce] services tels que [!DNL Live Search] ou [!DNL Product Recommendations] installé, les informations d’identification s’affichent dans l’interface et aucune configuration supplémentaire n’est requise.

1. Configurez le projet SaaS et l’espace de données afin que Commerce Services puisse envoyer des données au service de gestionnaire de canaux.

   ![[!DNL Commerce Service Connector] Configuration de l’identifiant SaaS dans la variable [!DNL Admin] view](assets/commerce-services-connector-saas-config.png)

