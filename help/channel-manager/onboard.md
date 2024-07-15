---
title: Onboard [!DNL Channel Manager]
description: 'Connectez votre instance au service [!DNL Channel Manager] en suivant quelques étapes d’intégration.'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Onboard [!DNL Channel Manager]

Une fois le processus d’intégration du Gestionnaire de canaux terminé, vous pouvez accéder aux opérations de vente de canaux Walmart Marketplace, les configurer et les gérer à partir d’Adobe Commerce. Le gestionnaire de canaux est disponible à partir de l’option [!UICONTROL Channel Manager] du menu [!UICONTROL Commerce Admin Marketing].

Option ![[!DNL Channel Manager] dans la vue d’administration ](assets/channel-manager-admin-view.png){width="500"}

## Conditions

Passez en revue les conditions requises pour utiliser le gestionnaire de canaux et collectez les informations de compte et les informations d’identification requises pour télécharger, installer et configurer l’extension.

- **[Exigences de Walmart Marketplace](walmart-requirements.md)** - Vérifiez que vous remplissez les conditions requises pour l’intégration à Channel Manager, y compris [ la configuration de votre compte Seller](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) et la génération de la clé API pour activer l’intégration.

- **Informations sur le compte Commerce**-Le téléchargement et l’installation de [!DNL Channel Manager] nécessitent un [compte Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Vous avez besoin d’un identifiant de compte et d’informations d’identification avec accès propriétaire ou administrateur à l’instance [!DNL Adobe Commerce] ou [!DNL Magento Open Source].

   - **MAGE ID**-[Connectez-vous](https://account.magento.com/customer/account/login/) au compte [!DNL Commerce] pour obtenir l’identifiant de **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] sur [!DNL Commerce] paramètres de compte ](assets/mageid-my-commerce-account.png){width="250"}

   - **Accéder aux clés-** Obtenez des clés d’authentification pour télécharger les [!DNL Commerce] extensions à partir du [!DNL Commerce] référentiel du compositeur `([!DNL repo.magento.com]`).

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     Sur les projets Adobe Commerce et Magento Open Source, le propriétaire peut configurer l’[accès partagé](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) pour permettre aux employés et aux fournisseurs de services de confiance de télécharger des extensions à l’aide des informations d’identification du compte du propriétaire ou du détenteur de licence.

     Pour [!DNL Adobe Commerce] sur les projets d’infrastructure cloud, les programmes d’installation doivent avoir l’accès suivant à l’instance [!DNL Commerce] :

      - Accès des super utilisateurs au projet Cloud
      - Accès de l’administrateur à un environnement spécifique
      - un compte [!DNL Adobe Commerce] avec des autorisations d’accès au référentiel du compositeur

     Voir [Gestion de l’accès des utilisateurs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) dans le *Guide de l’infrastructure de Commerce on Cloud*.

- **Expérience avec le compositeur et le[!DNL Commerce CLI]**-Voir [Installation d’une extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) dans le *Guide d’installation* pour plus d’informations sur l’utilisation de ces outils pour installer et gérer des extensions sur des plateformes [!DNL Adobe Commerce] ou [!DNL Magento Open Source].

- **[[!DNL Amazon Sales Channel] version 4.4.2 ou ultérieure](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** - Si vous avez activé [!DNL Amazon Sales Channel] pour vos [!DNL Commerce] sites, vérifiez que la version 4.4.2 ou ultérieure de votre plateforme [!DNL Commerce] est installée avant d’installer [!DNL Channel Manager].

- Extension **[!DNL Inventory Management]pour Adobe Commerce et Magento Open Source**

  Si vous prévoyez d’utiliser le gestionnaire de canaux pour la gestion des stocks et des commandes, l’extension Inventory management doit être installée et activée sur vos instances Adobe Commerce et Magento Open Source. En règle générale, cette extension est installée et activée par défaut sur Adobe Commerce et [!DNL Magento Open Source] 2.3.x et versions ultérieures.

  Si vous avez mis à niveau Commerce à partir de la version 2.2.x ou si vous avez désactivé Inventory management, mettez à jour votre installation afin d’inclure les modules requis. Voir [Installation d’Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) dans le *Guide d’Inventory management*.

### Configuration requise

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Compositeur 1.x ou ultérieur](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] version 4.4.2 ou ultérieure](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) - Si vous avez activé [!DNL Amazon Sales Channel] pour vos [!DNL Commerce] sites, vérifiez que la version 4.4.2 de votre plateforme [!DNL Commerce] est installée avant d’installer [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plateformes prises en charge

- Adobe Commerce on Cloud (CEE) : 2.4.x
- Adobe Commerce sur site (EE) : 2.4.x
- Magento Open Source 2.4.x

## Étapes d’intégration

1. [ Configurez votre compte Walmart ](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Installez l&#39; [!DNL Channel Manager] extension](install.md).

1. [Connectez-vous aux services Commerce](connect.md) pour intégrer le gestionnaire de canaux à l’instance Commerce et à d’autres services de prise en charge.

1. [Connectez votre  [!DNL Commerce] boutique à [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Installation de magasin terminée](complete-sales-channel-store-setup.md).
