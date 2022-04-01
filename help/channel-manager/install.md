---
title: ' [!DNL Channel Manager]'
description: Install the Channel Manager extension.
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 4509528d1b084c9a91fd6be0d0a863782edb3bdd
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Install Channel Manager

[](onboard.md#prerequisites)

## Update minimum-stability setting

`minimum-stability``composer.json`

`composer.json`

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## Install the extension

The Channel Manager installation instructions depend on whether Adobe Commerce or Magento Open Source is deployed on-premises or on cloud infrastructure.

- [](#install-on-an-on-premises-instance)

- [[!DNL Adobe Commerce] ](#install-adobe-commerce-on-cloud-infrastructure)

Both methods require you to use the Command Line Interface (CLI).

>[!NOTE]
>
>[!DNL Commerce][](https://devdocs.magento.com/extensions/install/)

### Install on an on-premises instance

Use these instructions to install on Adobe Commerce and Magento Open Source platforms.

1. [!DNL Commerce][](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html)[!DNL Commerce]

1. [](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html)

   ```bash
   $ bin/magento maintenance:enable
   ```

1. [!DNL Commerce]`composer.json`

   ```bash
    $ composer require magento/channel-manager --no-update
   ```

1. [!DNL Commerce]

   Your public key is your username; your private key is your password.

1. Update the dependencies and install the extension.

   ```bash
   $ composer update
   ```

   `composer update` `composer update magento/channel-manager`

1. Wait for Composer to finish updating project dependencies and resolve any errors.

1. Verify the installation

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:

   ```terminal
   Module is disabled
   ```

1. Register the extension.

   ```bash
   $ bin/magento setup:upgrade
   ```

1. [!DNL Commerce]

   ```bash
   $ bin/magento setup:di:compile
   ```

1. Verify that the extension is enabled:

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:

   ```bash
   Module is enabled
   ```

1. Clean the cache.

   ```bash
   $ bin/magento cache:clean
   ```

1. Disable maintenance mode.

   ```bash
    $ bin/magento maintenance:disable
   ```

### Install on an Adobe Commerce on Cloud Infrastructure Instance

Work in a development branch when adding an extension to your cloud instance.

[](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted)

`&lt;VendorName>\_&lt;ComponentName>`[](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html) You do not need to edit the file directly.

1. On your local workstation, change to the Cloud project root directory.

1. [](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted)

1. `require``composer.json`

   ```bash
   $ composer require magento/channel-manager --no-update
   ```

1. `composer.lock``composer.json`

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. After build and deploy completes, use SSH to log in to the remote environment and verify that the extension installed correctly.

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Sample response:

   ```terminal
   Module is enabled
   ```

1. [!UICONTROL Admin][](connect.md)

   >[!NOTE]
   >
   >[](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)


## Troubleshooting

Use the following information to resolve errors that occur during the Channel Manager installation process.

### Incorrect Composer keys

[](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html)[!DNL MAGE ID][!DNL Channel Manager]

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Check the key configuration:

1. `auth.json`

   ```bash
   $ composer config –global home
   ```

1. `auth.json`

   ```bash
   $ cat /path/to/auth.json
   ```

1. [](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html)

### Insufficient memory for PHP

The following error displays if the system does not have enough memory allocated for PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Use either of the following methods to resolve the memory issue:

- [](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit)`php.ini` [](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)

- Specify the memory limit from the command line.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Par exemple :

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Missing view

`process_catalog_exporter_view`[](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex)

```bash
php bin/magento indexer:refresh
```

### Cloud deployment errors

[](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html)
