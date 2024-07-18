---
title: 'Install [!DNL Channel Manager]'
description: 'Installez l’extension[!DNL Channel Manager].'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 1e74150e6ac88dbabb2e4bbb2fa2f243072eb03f
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# Installer [!DNL Channel Manager]

Passez en revue les [exigences](onboard.md#requirements) et rassemblez les informations requises avant d’installer le Gestionnaire de canaux.

## Installation de l’extension

Les instructions d’installation de Channel Manager dépendent si Adobe Commerce ou Magento Open Source est déployé sur site ou sur l’infrastructure cloud.

- Installez-le sur une [instance sur site](#install-on-an-on-premises-instance).

- Installation sur une [[!DNL Adobe Commerce]  sur une instance d’infrastructure cloud ](#install-adobe-commerce-on-cloud-infrastructure)

Les deux méthodes nécessitent l’utilisation de l’interface de ligne de commande.

>[!NOTE]
>
>Pour obtenir de l’aide sur l’installation du logiciel [!DNL Commerce] à l’aide de l’interface en ligne de commande, voir [Installation d’une extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### Installation sur une instance sur site

Suivez ces instructions pour installer [!DNL Channel Manager] sur Adobe Commerce et Magento Open Source sur une instance sur site.

1. Connectez-vous au serveur [!DNL Commerce] en tant qu&#39;utilisateur [ disposant d&#39;autorisations](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) pour écrire sur le système de fichiers [!DNL Commerce].

1. Placez votre site web en [mode de maintenance](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Depuis le répertoire racine du projet [!DNL Commerce], ajoutez Channel Manager à `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Si vous y êtes invité, saisissez les clés d’accès de votre compte [!DNL Commerce].

   Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

1. Mettez à jour les dépendances et installez l’extension.

   ```bash
   composer update magento/channel-manager
   ```

   La commande `composer update` ne met à jour que les dépendances requises pour [!DNL Channel Manager]. Pour mettre à jour toutes les dépendances, utilisez plutôt cette commande : `composer update`.

1. Attendez que le compositeur termine la mise à jour des dépendances du projet et résolve les erreurs.

1. Vérifiez l’installation du module :

   - Vérifiez le statut du module.

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     Exemple de réponse :

     ```
     Module is enabled
     ```

   - Si le module n’est pas activé, activez-le.

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. Enregistrez l’extension.

   ```bash
   bin/magento setup:upgrade
   ```

1. Si vous y êtes invité, recompilez votre projet [!DNL Commerce].

   ```bash
   bin/magento setup:di:compile
   ```

1. Nettoyez le cache.

   ```bash
   bin/magento cache:clean
   ```

1. Désactivez le mode de maintenance.

   ```bash
   bin/magento maintenance:disable
   ```

### Installation sur une instance Adobe Commerce sur une infrastructure cloud

Travaillez dans une branche de développement lors de l’ajout d’une extension à votre instance cloud.

Pour obtenir de l’aide sur l’utilisation des branches, reportez-vous à la section [Prise en main de la création de branches](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) du _Guide d’infrastructure de Commerce on Cloud_.

Pendant l’installation, le nom de l’extension (`magento\channel-manager`) est automatiquement inséré dans le fichier [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html). Vous n’avez pas besoin de modifier directement le fichier.

1. Sur votre poste de travail local, accédez au répertoire racine du projet Cloud.

1. Créez ou extrayez une [branche](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) de développement.

1. À l’aide du nom du compositeur, ajoutez l’extension à la section `require` du fichier `composer.json`.

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Mettez à jour les dépendances et installez l’extension.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   La commande `composer update` ne met à jour que les dépendances requises pour [!DNL Channel Manager]. Pour mettre à jour toutes les dépendances, utilisez plutôt cette commande : `composer update`.

1. Ajoutez, validez et poussez les modifications de code - incluez les modifications au fichier `composer.lock` et `composer.json`.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Une fois le processus de création et de déploiement terminé, utilisez SSH pour vous connecter à l’environnement distant et vérifier que l’extension est installée correctement.

```bash
   bin/magento module:status Magento_SalesChannels
```

Exemple de réponse :

```
Module is enabled
```

Si le module est désactivé, [activez-le dans votre environnement local](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) et déployez vos modifications.


1. Une fois l’extension installée, connectez-vous à [!UICONTROL Admin] pour [configurer Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >Pour obtenir des instructions sur la mise à jour de Channel Manager vers une nouvelle version, reportez-vous à la section [Mise à niveau des modules et extensions](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## Dépannage

Utilisez les informations suivantes pour résoudre les erreurs qui se produisent pendant le processus d’installation de Channel Manager.

### Clés de compositeur incorrectes

Si les [clés d’accès](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilisées pour s’authentifier dans le référentiel du compositeur ne sont pas valides ou ne sont pas liées à [!DNL MAGE ID] utilisées pour s’inscrire au service [!DNL Channel Manager], l’erreur suivante s’affiche.

```
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Vérifiez la configuration de la clé :

1. Recherchez l’emplacement du fichier `auth.json` :

   ```bash
   $ composer config –global home
   ```

1. Affichez le fichier `auth.json`.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Vérifiez que les informations d’identification dans le fichier auth.json correspondent à [les clés associées à l’ID MAGE](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilisé pour s’enregistrer pour le service Channel Manager.

### Mémoire insuffisante pour PHP

L’erreur suivante s’affiche si le système ne dispose pas de suffisamment de mémoire pour PHP.

```
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilisez l’une des méthodes suivantes pour résoudre le problème de mémoire :

- [Augmentez la limite de mémoire pour PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) dans le fichier d&#39;environnement `php.ini`. Vérifiez également que l’instance Commerce possède les [valeurs recommandées](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) pour d’autres paramètres PHP.

- Spécifiez la limite de mémoire à partir de la ligne de commande.

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  Par exemple :

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### Vue manquante

Si vous obtenez une erreur au sujet d’un `process_catalog_exporter_view` manquant lors de l’installation du Gestionnaire de canaux, essayez d’ [actualiser les indexeurs](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### Erreurs de déploiement dans le cloud

Pour les problèmes de déploiement de l’extension sur le cloud, voir [échec du déploiement de l’extension](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
