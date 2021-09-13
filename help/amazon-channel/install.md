---
title: Installation de l’extension
description: Pour intégrer votre  [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] et le vendre par l’intermédiaire de la [!DNL Amazon Marketplace], téléchargez et installez l’extension du Sales Channel Amazon.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Installation de l’extension

>[!IMPORTANT]
>
>Seules les versions [!DNL Amazon Sales Channel] de l’extension 4.0+ sont prises en charge pour les versions Adobe Commerce et Magento Open Source 2.4.x. Si vous exécutez une version 2.3.x, reportez-vous à la documentation de la [version compatible du canal de vente Amazon](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Pour plus d’informations sur la compatibilité des versions, consultez la page [Disponibilité](https://devdocs.magento.com/release/availability.html){target=&quot;_blank&quot;} de la documentation destinée aux développeurs.

L’extension [!UICONTROL Amazon Sales Channel] installe et ajoute des fonctionnalités pour intégrer votre catalogue Commerce à [!DNL Amazon Seller Accounts] afin de le vendre par le biais de [!DNL Amazon Marketplace]. Pour consulter des informations supplémentaires, reportez-vous à la page [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) dans [!DNL Commerce Marketplace] et aux [notes de mise à jour](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) de la documentation destinée aux développeurs.

## Conditions

- **Instance** de commerce : L’ [!DNL Amazon Sales Channel] extension peut être installée sur les instances avec Magento Open Source, Adobe Commerce et Adobe Commerce sur les versions 2.3.x ou ultérieures de l’infrastructure cloud. Il n’est plus pris en charge dans les versions 2.1, 2.2 ou 1.x.
- **Compte** web Commerce : Vous devez disposer d’un compte Web Commerce, qui est utilisé pour créer et suivre une clé API.
- **Clé** API : Créez une clé d’API de canal de vente Amazon via votre compte web Commerce. Les instructions suivantes comprennent ces étapes.

## Installer

Pour plus d’informations sur l’utilisation du compositeur pour ce processus, voir les instructions d’[installation de l’extension](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} dans la documentation destinée aux développeurs.

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

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

   - Saisissez vos [clés d’authentification](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

   - Attendez que le compositeur termine la mise à jour des dépendances de votre projet et assurez-vous qu’il n’y a aucune erreur.


1. [Vérifiez l’extension](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Ajout de la clé API du canal de vente Amazon

Après l’installation, saisissez une [clé API](./amazon-verify-api-key.md) pour terminer la configuration.

## Définition des options de configuration du canal Amazon

Vous disposez des options suivantes pour configurer le canal de vente Amazon. Vous n’avez pas besoin de modifier ces paramètres pour commencer l’intégration et la vente sur Amazon. Il est recommandé que les administrateurs avancés prennent en compte ces options.

1. Connectez-vous à l’administrateur.

1. Dans la barre latérale _Admin_, accédez à **Magasins** > _Paramètres_ > **Configuration**.

1. Cliquez sur **Sales Channel**, puis sur **Paramètres globaux**.

1. Pour **Effacer l’historique du journal**, définissez l’intervalle d’effacement des journaux collectés.

   `Once Daily`, `Once Weekly` et `Once Monthly` (valeur par défaut).

1. (Facultatif) Pour **Source** des tâches en arrière-plan (CRON), remplacez le paramètre par `Command Line (CLI) CRON`.

   Ce paramètre est recommandé pour les **_utilisateurs/administrateurs avancés_**.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Mettre à jour l’extension

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Cliquez sur l’onglet **[!UICONTROL Marketplace]**, puis sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page de l’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Suivez les [instructions de mise à niveau de l’extension](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} dans la documentation destinée aux développeurs.
