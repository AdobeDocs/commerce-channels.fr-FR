---
title: Onboard [!DNL Channel Manager]
description: Connectez votre instance au [!DNL Channel Manager] en suivant quelques étapes d’intégration."
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Onboard [!DNL Channel Manager]

Une fois le processus d’intégration du Gestionnaire de canaux terminé, vous pouvez accéder aux opérations de vente de canaux Walmart Marketplace, les configurer et les gérer à partir d’Adobe Commerce. Le gestionnaire de canaux est disponible dans la [!UICONTROL Channel Manager] sur l’option [!UICONTROL Commerce Admin Marketing] .

![[!DNL Channel Manager] dans la vue Admin](assets/channel-manager-admin-view.png)

## Conditions

Passez en revue les conditions requises pour utiliser le gestionnaire de canaux et collectez les informations de compte et les informations d’identification requises pour télécharger, installer et configurer l’extension.

- **[Exigences de Walmart Marketplace](walmart-requirements.md)**- Vérifiez que vous remplissez les conditions requises pour l’intégration à Channel Manager, notamment : [configuration de votre compte de vendeur](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) et de générer la clé API pour activer l’intégration.

- **Informations de compte Commerce**-Téléchargement et installation [!DNL Channel Manager] nécessite une [Compte Commerce](https://docs.magento.com/user-guide/magento/magento-account.html){target="_blank"}. Vous avez besoin d’un identifiant de compte et d’informations d’identification avec un accès Propriétaire ou Administrateur à la variable [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instance.

   - **MAGE ID**-[Connexion](https://account.magento.com/customer/account/login/) au [!DNL Commerce] pour obtenir l’identifiant à partir de **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] on [!DNL Commerce] paramètres du compte](assets/mageid-my-commerce-account.png)

   - **Access keys-** Obtention des clés d’authentification à télécharger [!DNL Commerce] des extensions de [!DNL Commerce] Référentiel de compositeur `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Sur les projets Adobe Commerce et Magento Open Source, le propriétaire peut configurer [Accès partagé](https://docs.magento.com/user-guide/magento/magento-account-share.html) pour permettre aux employés et aux fournisseurs de services de confiance de télécharger des extensions à l’aide des informations d’identification du compte du propriétaire ou du détenteur de licence.

      Pour [!DNL Adobe Commerce] sur les projets d’infrastructure cloud, les programmes d’installation logicielle doivent disposer des droits d’accès suivants au [!DNL Commerce] instance :

      - Accès des super utilisateurs au projet Cloud
      - Accès de l’administrateur à un environnement spécifique
      - an [!DNL Adobe Commerce] compte avec autorisations d’accès au référentiel du compositeur

      Voir [Gestion de l’accès des utilisateurs](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Expérience à l’aide du compositeur et de la variable[!DNL Commerce CLI]**-Voir [Installation de l’interface de ligne de commande générale](https://devdocs.magento.com/extensions/install/){target="_blank"} pour plus d’informations sur l’utilisation de ces outils pour installer et gérer des extensions sur [!DNL Adobe Commerce] ou [!DNL Magento Open Source] plateformes.

- **[[!DNL Amazon Sales Channel] version 4.4.2 ou ultérieure](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Si vous avez activé [!DNL Amazon Sales Channel] pour votre [!DNL Commerce] , vérifiez que la variable [!DNL Commerce] La version 4.4.2 ou ultérieure de la plateforme est installée avant l’installation. [!DNL Channel Manager].

- **[!DNL Inventory Management]extension pour Adobe Commerce et Magento Open Source**

   Si vous prévoyez d’utiliser le gestionnaire de canaux pour la gestion des stocks et des commandes, l’extension Inventory management doit être installée et activée sur vos instances Adobe Commerce et Magento Open Source. En règle générale, cette extension est installée et activée par défaut sur Adobe Commerce et [!DNL Magento Open Source] 2.3.x et versions ultérieures.

   Si vous avez mis à niveau Commerce à partir de la version 2.2.x ou si vous avez désactivé Inventory management, mettez à jour votre installation afin d’inclure les modules requis. Voir [Installation d’Inventory management](https://devdocs.magento.com/extensions/inventory-management/) dans la documentation destinée aux développeurs Adobe Commerce.

### Configuration requise

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Compositeur 1.x ou version ultérieure](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] version 4.4.2 ou ultérieure](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Si vous avez activé [!DNL Amazon Sales Channel] pour votre [!DNL Commerce] , vérifiez que la variable [!DNL Commerce] La version 4.4.2 de Platform est installée avant l’installation. [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

### Plateformes prises en charge

- Adobe Commerce on Cloud (CEE) : 2.4.x
- Adobe Commerce On-Premise (EE) : 2.4.x
- Magento Open Source 2.4.x

## Étapes d’intégration

1. [Configuration de votre compte Walmart Seller](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Installez le [!DNL Channel Manager] extension](install.md).

1. [Connexion à Commerce Services](connect.md) pour intégrer Channel Manager à l’instance Commerce et à d’autres services de prise en charge.

1. [Connectez-vous à [!DNL Commerce] stocker dans [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Configuration complète du magasin](complete-sales-channel-store-setup.md).
