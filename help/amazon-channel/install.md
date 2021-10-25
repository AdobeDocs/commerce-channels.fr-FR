---
title: Installation de l’extension
description: Pour intégrer votre [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] et vendre par l'intermédiaire du [!DNL Amazon Marketplace], téléchargez et installez l’extension Sales Channel Amazon.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Installation de l’extension

>[!IMPORTANT]
>
>Seulement [!DNL Amazon Sales Channel] les versions 4.0 et ultérieures sont prises en charge pour les versions Adobe Commerce et Magento Open Source 2.4.x. Si vous exécutez une version 2.3.x, reportez-vous à la documentation du fichier [autorisation de canal de vente Amazon compatible](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Pour plus d’informations sur la compatibilité des versions, consultez la section [Disponibilité](https://devdocs.magento.com/release/availability.html)Page {target=&quot;_blank&quot;} dans la documentation du développeur.

Le [!UICONTROL Amazon Sales Channel] installe et ajoute des fonctionnalités pour intégrer votre catalogue Commerce à [!DNL Amazon Seller Accounts] pour vendre par l&#39;intermédiaire du [!DNL Amazon Marketplace]. Pour consulter des informations supplémentaires, consultez la section [Sales Channel Amazon](https://marketplace.magento.com/magento-module-amazon.html) page [!DNL Commerce Marketplace] et [notes de mise à jour](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) dans la documentation du développeur.

## Exigences

- **Instance Commerce**: Le [!DNL Amazon Sales Channel] peut être installé sur des instances avec Magento Open Source, Adobe Commerce et Adobe Commerce et sur les infrastructures cloud 2.3.x ou version ultérieure. Il n’est plus pris en charge dans les versions 2.1, 2.2 ou 1.x.
- **Compte Web Commerce**: Vous devez disposer d’un compte Web Commerce, qui est utilisé pour créer et suivre une clé d’API.
- **Clé d’API**: Créez une clé d&#39;API de canal de vente Amazon via votre compte Web Commerce. Les instructions suivantes incluent ces étapes.

## Installer

Pour plus d’informations sur l’utilisation du compositeur pour ce processus, consultez la section [installation d&#39;extension](https://devdocs.magento.com/extensions/install/)Instructions {target=&quot;_blank&quot;} dans la documentation du développeur.

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Cliquez sur le bouton **[!UICONTROL Marketplace]** , puis cliquez sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page d’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Utilisez les informations de nom et de version pour mettre à jour l’entrée du connecteur de services dans votre `composer.json` fichier.

   - Ajoutez le nom et la version de l’extension à votre `composer.json` fichier.

   - Accédez à votre [!DNL Commerce] répertoire de projets et mettez à jour votre `composer.json` fichier.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Saisissez votre [clés d&#39;authentification](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

   - Attendez que Composer termine la mise à jour des dépendances de votre projet et assurez-vous qu’il n’y a aucune erreur.


1. [Vérification de l’extension](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Ajout de la clé d&#39;API du canal de vente Amazon

Après l’installation, entrez un [Clé d’API](./amazon-verify-api-key.md) pour terminer la configuration.

## Définition des options de configuration du canal Amazon

Vous disposez des options suivantes pour configurer le canal de vente Amazon. Vous n’avez pas besoin de modifier ces paramètres pour commencer l’intégration et la vente sur Amazon. Il est recommandé aux administrateurs avancés d’examiner ces options.

1. Connectez-vous à l’administrateur.

1. Sur la _Administrateur_ barre latérale, accédez à **Magasins** > _Paramètres_ > **Configuration**.

1. Cliquez sur **Sales Channel**, puis **Paramètres généraux**.

1. Pour **Effacer l&#39;historique des journaux**, définissez l&#39;intervalle d&#39;effacement des journaux collectés.

   Les options incluent `Once Daily`, `Once Weekly`et `Once Monthly` (par défaut).

1. (Facultatif) Pour **Source des tâches en arrière-plan (CRON)**, définissez le paramètre sur `Command Line (CLI) CRON`.

   Ce paramètre est recommandé pour **_utilisateurs/administrateurs avancés_**.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Mettre à jour l’extension

1. Connectez-vous au [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Cliquez sur le bouton **[!UICONTROL Marketplace]** , puis cliquez sur **[!UICONTROL My Purchases]**.

1. Recherchez et sélectionnez **[!UICONTROL Amazon Sales Channel]**.

1. Sur la page d’extension, sélectionnez la version.

1. Pour le nom et la version du composant, cliquez sur **[!UICONTROL Technical Details]**.

1. Renseignez la [instructions de mise à niveau d&#39;extension](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} dans la documentation du développeur.
