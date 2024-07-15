---
title: Installation de l’extension  [!DNL Amazon Sales Channel]
description: Pour intégrer votre  [!DNL Commerce] catalogue à  [!DNL Amazon Seller Accounts] et le vendre par l’intermédiaire de [!DNL Amazon Marketplace], téléchargez et installez l’extension Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Installation de l’extension [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
>Seules les versions [!DNL Amazon Sales Channel] de l’extension 4.0+ sont prises en charge pour les versions Adobe Commerce et Magento Open Source 2.4.x. Si vous exécutez une version 2.3.x, reportez-vous à la documentation de la [version compatible du canal de vente Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Pour plus d’informations sur la compatibilité des versions, consultez la page [Disponibilité](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) de la documentation destinée aux développeurs.

L’extension [!UICONTROL Amazon Sales Channel] installe et ajoute des fonctionnalités pour intégrer votre catalogue Commerce à [!DNL Amazon Seller Accounts] afin de le vendre via [!DNL Amazon Marketplace]. Pour consulter des informations supplémentaires, consultez la page [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) dans [!DNL Commerce Marketplace] et les [ notes de mise à jour](release-notes.md).

## Conditions

- **Instance Commerce** : l’extension [!DNL Amazon Sales Channel] peut être installée sur les instances avec Magento Open Source, Adobe Commerce et Adobe Commerce sur les versions 2.3.x ou ultérieures de l’infrastructure cloud. Il n’est plus pris en charge dans les versions 2.1, 2.2 ou 1.x.
- **Compte web Commerce** : vous devez disposer d’un compte web Commerce, qui est utilisé pour créer et suivre une clé API.
- **Clé API** : créez une clé API de canal de vente Amazon via votre compte web Commerce. Les instructions suivantes comprennent ces étapes.

## Installer

Pour plus d’informations sur l’utilisation du compositeur pour ce processus, voir les instructions [installation de l’extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) dans la documentation destinée aux développeurs.

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Cliquez sur l’onglet **[!UICONTROL Marketplace]**, puis sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page de l’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Utilisez les informations de nom et de version pour mettre à jour l’entrée du connecteur de services dans votre fichier `composer.json`.

   - Ajoutez le nom et la version de l’extension à votre fichier `composer.json`.

   - Accédez au répertoire de votre projet [!DNL Commerce] et mettez à jour votre fichier `composer.json`.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Saisissez vos [clés d&#39;authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

   - Attendez que le compositeur termine la mise à jour des dépendances de votre projet et assurez-vous qu’il n’y a aucune erreur.

1. [Vérifiez l’extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Ajout de la clé API du canal de vente Amazon

Après l’installation, saisissez une [clé API](./amazon-verify-api-key.md) pour terminer la configuration.

## Définition des options de configuration du canal Amazon

Vous disposez des options suivantes pour configurer le canal de vente Amazon. Vous n’avez pas besoin de modifier ces paramètres pour commencer l’intégration et la vente sur Amazon. Il est recommandé que les administrateurs avancés prennent en compte ces options.

1. Connectez-vous à l’administrateur.

1. Sur la barre latérale _Admin_, accédez à **Magasins** > _Paramètres_ > **Configuration**.

1. Cliquez sur **Sales Channel**, puis sur **Paramètres globaux**.

1. Pour **Effacer l’historique du journal**, définissez l’intervalle d’effacement des journaux collectés.

   Les options incluent `Once Daily`, `Once Weekly` et `Once Monthly` (par défaut).

1. (Facultatif) Pour **Tâches en arrière-plan (CRON) Source**, remplacez le paramètre par `Command Line (CLI) CRON`.

   Ce paramètre est recommandé pour les **_utilisateurs/administrateurs avancés_**.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Mettre à jour l’extension

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Cliquez sur l’onglet **[!UICONTROL Marketplace]**, puis sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page de l’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Suivez les [instructions de mise à niveau de l&#39;extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) du _Guide d&#39;installation_.
