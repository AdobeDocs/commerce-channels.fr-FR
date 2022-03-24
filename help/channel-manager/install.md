---
title: Installer [!DNL Channel Manager]
description: Installez l’extension Channel Manager.
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Installation du gestionnaire de canaux

Consultez la section [conditions préalables](onboard.md#prerequisites) et collectez les informations requises avant d’installer le Gestionnaire de canaux.

## Mise à jour du paramètre de stabilité minimale

Avant d’installer l’extension, mettez à jour la variable `minimum-stability` dans votre `composer.json` afin que vous puissiez installer les versions antérieures du Gestionnaire de canaux à l’aide du compositeur.

Pour mettre à jour la configuration, ajoutez les lignes suivantes au `composer.json` fichier .

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## Installation de l’extension

Les instructions d’installation de Channel Manager dépendent si Adobe Commerce ou Magento Open Source est déployé sur site ou sur l’infrastructure cloud.

- Installez sur un [Instance locale](#install-on-an-on-premises-instance).

- Installez sur un [[!DNL Adobe Commerce] sur l’instance d’infrastructure cloud](#install-adobe-commerce-on-cloud-infrastructure)

Les deux méthodes nécessitent l’utilisation de l’interface de ligne de commande.

>[!NOTE]
>
>Pour obtenir de l’aide sur l’installation [!DNL Commerce] à l’aide de l’interface en ligne de commande, voir [Installation de l’interface de ligne de commande générale](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}.

### Installation sur une instance sur site

Suivez ces instructions pour installer sur les plateformes Adobe Commerce et Magento Open Source.

1. Connectez-vous au [!DNL Commerce] server as a [utilisateur avec autorisations](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target=&quot;_blank&quot;} pour écrire dans le [!DNL Commerce] système de fichiers.

1. Insérer votre site web dans [mode de maintenance](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target=&quot;_blank&quot;}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Dans la [!DNL Commerce] répertoire racine du projet, ajoutez Channel Manager à `composer.json`.

   ```bash
    $ composer require magento/channel-manager --no-update
   ```

1. Si vous y êtes invité, saisissez les clés d’accès de votre [!DNL Commerce] compte .

   Votre clé publique est votre nom d’utilisateur ; votre clé privée est votre mot de passe.

1. Mettez à jour les dépendances et installez l’extension.

   ```bash
   $ composer update
   ```

   Le `composer update` met à jour toutes les dépendances. Pour mettre à jour uniquement les dépendances liées au Gestionnaire de canaux, utilisez plutôt cette commande : `composer update magento/channel-manager`.

1. Attendez que le compositeur termine la mise à jour des dépendances du projet et résolve les erreurs.

1. Vérification de l’installation

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exemple de réponse :

   ```terminal
   Module is disabled
   ```

1. Enregistrez l’extension.

   ```bash
   $ bin/magento setup:upgrade
   ```

1. Si vous y êtes invité, recompilez votre [!DNL Commerce] projet.

   ```bash
   $ bin/magento setup:di:compile
   ```

1. Vérifiez que l’extension est activée :

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exemple de réponse :

   ```bash
   Module is enabled
   ```

1. Nettoyez le cache.

   ```bash
   $ bin/magento cache:clean
   ```

1. Désactivez le mode de maintenance.

   ```bash
    $ bin/magento maintenance:disable
   ```

### Installation sur une instance Adobe Commerce sur une infrastructure cloud

Travaillez dans une branche de développement lors de l’ajout d’une extension à votre instance cloud.

Pour obtenir de l’aide sur l’utilisation des branches, voir [Prise en main de la création de branches](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;} dans la documentation destinée aux développeurs Adobe Commerce.

Pendant l’installation, le nom de l’extension (`&lt;VendorName>\_&lt;ComponentName>`) est automatiquement insérée dans la variable [app/etc/config.php](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html)fichier {target=&quot;_blank&quot;}. Vous n’avez pas besoin de modifier directement le fichier.

1. Sur votre poste de travail local, accédez au répertoire racine du projet Cloud.

1. Création ou extraction d’un développement [branche](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;}.

1. À l’aide du nom du compositeur, ajoutez l’extension au `require` de la section `composer.json` fichier .

   ```bash
   $ composer require magento/channel-manager --no-update
   ```

1. Ajout, validation et transmission de modifications de code - Incluez les modifications apportées aux `composer.lock` et `composer.json` fichier .

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. Une fois la création et le déploiement terminés, utilisez SSH pour vous connecter à l’environnement distant et vérifier que l’extension est installée correctement.

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exemple de réponse :

   ```terminal
   Module is enabled
   ```

1. Une fois l’installation terminée, connectez-vous au [!UICONTROL Admin] to [configuration du connecteur Commerce Services](connect.md).

   >[!NOTE]
   >
   >Pour obtenir des instructions sur la mise à jour de Channel Manager vers une nouvelle version, voir [Mise à niveau des modules et des extensions](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target=&quot;_blank&quot;}.


## Dépannage

Utilisez les informations suivantes pour résoudre les erreurs qui se produisent pendant le processus d’installation de Channel Manager.

### Clés de compositeur incorrectes

Si la variable [touches d&#39;accès](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} utilisé pour s’authentifier dans le référentiel du compositeur ne sont pas valides ou ne sont pas liés à la variable [!DNL MAGE ID] utilisé pour s’inscrire au [!DNL Channel Manager] , l’erreur suivante s’affiche.


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

1. Vérification de la correspondance des informations d’identification dans le fichier auth.json [les clés associées à l’ID MAGE ;](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} utilisé pour s’enregistrer pour le service Channel Manager.

### Mémoire insuffisante pour PHP

L’erreur suivante s’affiche si le système ne dispose pas de suffisamment de mémoire pour PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Utilisez l’une des méthodes suivantes pour résoudre le problème de mémoire :

- [Augmentation de la limite de mémoire pour PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target=&quot;_blank&quot;} dans l’environnement `php.ini` fichier . Vérifiez également que l’instance Commerce possède la variable [valeurs recommandées](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target=&quot;_blank&quot;} pour les autres paramètres PHP.

- Spécifiez la limite de mémoire à partir de la ligne de commande.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Par exemple :

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Vue manquante

Si vous obtenez une erreur à propos d’un objet manquant `process_catalog_exporter_view` lors de l’installation de Channel Manager, essayez [actualisation des indexeurs](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target=&quot;_blank&quot;}.

```bash
php bin/magento indexer:refresh
```

### Erreurs de déploiement dans le cloud

Pour les problèmes de déploiement de l’extension sur le cloud, voir [échec du déploiement de l’extension](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target=&quot;_blank&quot;}.
