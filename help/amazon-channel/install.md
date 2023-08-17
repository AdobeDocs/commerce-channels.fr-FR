---
title: "Installez le [!DNL Amazon Sales Channel] extension"
description: Pour intégrer votre [!DNL Commerce] catalogue avec [!DNL Amazon Seller Accounts] et vendre par l’intermédiaire de la variable [!DNL Amazon Marketplace], téléchargez et installez l’extension Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Installez le [!DNL Amazon Sales Channel] extension

>[!IMPORTANT]
>
>Uniquement [!DNL Amazon Sales Channel] les versions d’extension 4.0+ sont prises en charge pour Adobe Commerce et Magento Open Source 2.4.x. Si vous exécutez une version 2.3.x, reportez-vous à la documentation de la variable [version compatible du canal de vente Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Pour plus d’informations sur la compatibilité des versions, voir [Disponibilité](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) dans la documentation destinée aux développeurs.

La variable [!UICONTROL Amazon Sales Channel] l’extension installe et ajoute des fonctionnalités pour intégrer votre catalogue Commerce à [!DNL Amazon Seller Accounts] pour vendre par l’intermédiaire de la variable [!DNL Amazon Marketplace]. Pour consulter d’autres informations, voir [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) page [!DNL Commerce Marketplace] et la variable [notes de mise à jour](release-notes.md).

## Conditions

- **Instance de commerce**: la variable [!DNL Amazon Sales Channel] l’extension peut être installée sur les instances avec Magento Open Source, Adobe Commerce et Adobe Commerce sur les versions 2.3.x ou ultérieures de l’infrastructure cloud. Il n’est plus pris en charge dans les versions 2.1, 2.2 ou 1.x.
- **Compte web Commerce**: vous devez disposer d’un compte Web Commerce, qui est utilisé pour créer et suivre une clé API.
- **Clé API**: créez une clé d’API de canal de vente Amazon via votre compte web Commerce. Les instructions suivantes comprennent ces étapes.

## Installer

Pour plus d’informations sur l’utilisation du compositeur pour ce processus, voir [installation d’extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) instructions dans la documentation destinée aux développeurs.

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Cliquez sur le bouton **[!UICONTROL Marketplace]** puis cliquez sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page de l’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Utilisez les informations de nom et de version pour mettre à jour l’entrée du connecteur de services dans votre `composer.json` fichier .

   - Ajoutez le nom et la version de l’extension à votre `composer.json` fichier .

   - Accédez à [!DNL Commerce] répertoire du projet et mettez à jour votre `composer.json` fichier .

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Saisissez votre [clés d’authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

   - Attendez que le compositeur termine la mise à jour des dépendances de votre projet et assurez-vous qu’il n’y a aucune erreur.

1. [Vérification de l’extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Ajout de la clé API du canal de vente Amazon

Après l’installation, saisissez une [Clé API](./amazon-verify-api-key.md) pour terminer la configuration.

## Définition des options de configuration du canal Amazon

Vous disposez des options suivantes pour configurer le canal de vente Amazon. Vous n’avez pas besoin de modifier ces paramètres pour commencer l’intégration et la vente sur Amazon. Il est recommandé que les administrateurs avancés prennent en compte ces options.

1. Connectez-vous à l’administrateur.

1. Sur le _Administration_ barre latérale, accédez à **Magasins** > _Paramètres_ > **Configuration**.

1. Cliquez sur **Sales Channel**, puis **Paramètres globaux**.

1. Pour **Effacer l’historique du journal**, définissez l’intervalle d’effacement des journaux collectés.

   Les options incluent `Once Daily`, `Once Weekly`, et `Once Monthly` (par défaut).

1. (Facultatif) Pour **Source des tâches en arrière-plan (CRON)**, définissez le paramètre sur `Command Line (CLI) CRON`.

   Ce paramètre est recommandé pour **_utilisateurs/administrateurs avancés_**.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Mettre à jour l’extension

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Cliquez sur le bouton **[!UICONTROL Marketplace]** puis cliquez sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page de l’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Procédez comme suit : [instructions de mise à niveau d’extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) dans le _Guide d’installation_.
