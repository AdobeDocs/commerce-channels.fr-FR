---
title: 'Installer [!DNL Channel Manager]'
description: 'Installez le[!DNL Channel Manager] extension.'
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# Installer [!DNL Channel Manager]

Consultez la section [conditions requises](onboard.md#requirements) et collectez les informations requises avant d’installer le Gestionnaire de canaux.

## Installation de l’extension

Les instructions d’installation de Channel Manager dépendent si Adobe Commerce ou Magento Open Source est déployé sur site ou sur l’infrastructure cloud.

- Installez sur un [Instance locale](#install-on-an-on-premises-instance).

- Installez sur un [[!DNL Adobe Commerce] sur l’instance d’infrastructure cloud](#install-adobe-commerce-on-cloud-infrastructure)

Les deux méthodes nécessitent l’utilisation de l’interface de ligne de commande.

>[!NOTE]
>
>Pour obtenir de l’aide sur l’installation [!DNL Commerce] à l’aide de l’interface en ligne de commande, voir [Installer une extension](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### Installation sur une instance sur site

Suivez ces instructions pour installer [!DNL Channel Manager] sur Adobe Commerce et Magento Open Source à une instance sur site.

1. Connectez-vous au [!DNL Commerce] server as a [utilisateur avec autorisations](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) pour écrire dans le [!DNL Commerce] système de fichiers.

1. Insérer votre site web dans [mode de maintenance](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Dans la [!DNL Commerce] répertoire racine du projet, ajoutez Channel Manager à `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Si vous y êtes invité, saisissez les clés d’accès de votre [!DNL Commerce] compte .

   Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

1. Mettez à jour les dépendances et installez l’extension.

   ```bash
   composer update magento/channel-manager
   ```

   Le `composer update` ne met à jour que les dépendances requises pour [!DNL Channel Manager]. Pour mettre à jour toutes les dépendances, utilisez plutôt la commande suivante : `composer update`.

1. Attendez que le compositeur termine la mise à jour des dépendances du projet et résolve les erreurs.

1. Vérifiez l’installation du module :

   - Vérifiez le statut du module.

      ```bash
      bin/magento module:status Magento_SalesChannels
      ```

      Exemple de réponse :

      ```terminal
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

1. Si vous y êtes invité, recompilez votre [!DNL Commerce] projet.

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

Pour obtenir de l’aide sur l’utilisation des branches, voir [Prise en main de la création de branches](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) dans le _Guide d’infrastructure de Commerce on Cloud_.

Pendant l’installation, le nom de l’extension (`magento\channel-manager`) est automatiquement insérée dans la variable [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) fichier . Vous n’avez pas besoin de modifier directement le fichier.

1. Sur votre poste de travail local, accédez au répertoire racine du projet Cloud.

1. Création ou extraction d’un développement [branche](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html).

1. À l’aide du nom du compositeur, ajoutez l’extension au `require` de la section `composer.json` fichier .

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Mettez à jour les dépendances et installez l’extension.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   Le `composer update` ne met à jour que les dépendances requises pour [!DNL Channel Manager]. Pour mettre à jour toutes les dépendances, utilisez plutôt la commande suivante : `composer update`.

1. Ajout, validation et transmission de modifications de code - Incluez les modifications apportées aux `composer.lock` et `composer.json` fichier .

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

```terminal
Module is enabled
```

Si le module est désactivé, [l’activer dans votre environnement local ;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) et déployez vos modifications.


1. Une fois l’extension installée, connectez-vous au [!UICONTROL Admin] to [configuration du connecteur Commerce Services](connect.md).

   >[!NOTE]
   >
   >Pour obtenir des instructions sur la mise à jour de Channel Manager vers une nouvelle version, voir [Mise à niveau des modules et des extensions](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## Dépannage

Utilisez les informations suivantes pour résoudre les erreurs qui se produisent pendant le processus d’installation de Channel Manager.

### Clés de compositeur incorrectes

Si la variable [touches d&#39;accès](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilisé pour s’authentifier dans le référentiel du compositeur ne sont pas valides ou ne sont pas liés à la variable [!DNL MAGE ID] utilisé pour s’inscrire au [!DNL Channel Manager] , l’erreur suivante s’affiche.

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Vérifiez la configuration de la clé :

1. Recherchez l’emplacement du `auth.json` fichier :

   ```bash
   $ composer config –global home
   ```

1. Afficher la variable `auth.json` fichier .

   ```bash
   $ cat /path/to/auth.json
   ```

1. Vérification de la correspondance des informations d’identification dans le fichier auth.json [les clés associées à l’ID MAGE ;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) utilisé pour s’enregistrer pour le service Channel Manager.

### Mémoire insuffisante pour PHP

L’erreur suivante s’affiche si le système ne dispose pas de suffisamment de mémoire pour PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilisez l’une des méthodes suivantes pour résoudre le problème de mémoire :

- [Augmentation de la limite de mémoire pour PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) dans l’environnement `php.ini` fichier . Vérifiez également que l’instance Commerce possède la variable [valeurs recommandées](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) pour d’autres paramètres PHP.

- Spécifiez la limite de mémoire à partir de la ligne de commande.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Par exemple :

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Vue manquante

Si vous obtenez une erreur à propos d’un objet manquant `process_catalog_exporter_view` lors de l’installation de Channel Manager, essayez [actualisation des indexeurs](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### Erreurs de déploiement dans le cloud

Pour les problèmes de déploiement de l’extension sur le cloud, voir [échec du déploiement de l’extension](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
