---
title: '"Onboard [!DNL Channel Manager]"'
description: Connectez votre instance à la fonction [!DNL Channel Manager] en suivant quelques étapes d’intégration.
role: User
level: Intermediate
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Onboard [!DNL Channel Manager]

Gestionnaire de canaux intégré en installant l’extension Channel Manager sur votre [!DNL Commerce] et configuration des connexions API pour activer la communication et la synchronisation des données entre votre instance Commerce et Walmart Marketplace.

Une fois l’intégration terminée, vous pouvez configurer et gérer les opérations du canal de vente à partir du [!UICONTROL Channel Manager] sur l’option [!UICONTROL Commerce Admin Marketing] .

![[!DNL Channel Manager] dans la vue Admin](assets/channel-manager-admin-view.png)

## Présentation de l’intégration

1. [Installez le [!DNL Channel Manager] extension](install.md).

1. [Configurez la variable [!DNL Commerce Services Connector]](connect.md) pour intégrer Channel Manager à l’instance Commerce et à d’autres services de prise en charge.

1. [Connectez-vous à [!DNL Commerce] stocker dans [!DNL Walmart Marketplace]](connect.md).

## Conditions préalables

- Vérifiez que vous disposez des conditions requises de Walmart Marketplace Seller AccountWalmart pour la vente sur Walmart Marketplace.

- **Informations de compte Commerce**-Téléchargement et installation [!DNL Channel Manager] nécessite un identifiant et des informations d’identification d’un [Compte Commerce](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;} avec accès propriétaire au [!DNL Adobe Commerce] ou [!DNL Magento Open Source] instance.

   - **MAGE ID**-[Connexion](https://account.magento.com/customer/account/login/) au compte Commerce pour obtenir l’ID à partir de [!UICONTROL My Account - Magento settings]. Vous avez besoin de cet identifiant pour vous inscrire au [!DNL Channel Manager] le service bêta.

      ![[!DNL MAGEID] dans les paramètres du compte Commerce ;](assets/mageid-my-commerce-account.png)

   - **Access keys-** Obtenez des clés d’authentification pour télécharger des extensions Commerce à partir du référentiel Commerce Composer ([!DNL repo.magento.com]).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Sur les projets Adobe Commerce et Magento Open Source, le propriétaire peut configurer [Accès partagé](https://docs.magento.com/user-guide/magento/magento-account-share.html) pour permettre aux employés et aux fournisseurs de services de confiance de télécharger des extensions à l’aide des informations d’identification du compte du propriétaire ou du détenteur de licence.

      Activé [!DNL Adobe Commerce] sur les projets d’infrastructure cloud, les utilisateurs doivent disposer des autorisations suivantes pour installer le logiciel sur le [!DNL Commerce] instance :

      - Accès des super utilisateurs au projet Cloud
      - Accès de l’administrateur à un environnement spécifique
      - an [!DNL Adobe Commerce] ou [!DNL Magento Open Source] compte avec les autorisations d’accès au référentiel du compositeur. Voir [Gestion de l’accès des utilisateurs](https://devdocs.magento.com/cloud/project/user-admin.html).

- **Autorisation de téléchargement du package du compositeur du Gestionnaire de canaux**-Indiquez l’ID MAGE du compte Commerce utilisé pour gérer le service au représentant de l’Adobe qui coordonne le programme bêta de votre entreprise.
- **Expérience à l’aide du compositeur et de la variable[!DNL Commerce CLI]** -Voir [Installation de l’interface de ligne de commande générale](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} pour plus d’informations sur l’utilisation de ces outils pour installer et gérer des extensions sur A[!DNL Adobe Commerce] ou [!DNL Magento Open Source] plateformes.
- Pour les instances de Commerce sur lesquelles Amazon Sales Channel est installé, vérifiez que [Amazon Sales Channel version 4.4.2 ou ultérieure](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) est installé avant d’installer Channel Manager.


### Conditions

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Compositeur 1.x ou version ultérieure](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plateformes prises en charge

- Adobe Commerce on Cloud (CEE) : 2.4.x
- Adobe Commerce On-Premise (EE) : 2.4.x
- Magento Open Source 2.4.x
