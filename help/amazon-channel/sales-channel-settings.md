---
title: Paramètres du Sales Channel
description: Pour gérer la journalisation, la source cron et la synchronisation des fonctions de canal de vente Amazon, mettez à jour la configuration Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Paramètres du Sales Channel

Lorsque l’extension [!DNL Amazon Sales Channel] est installée, les valeurs par défaut sont définies dans le canal de vente Admin for Amazon. Ces paramètres peuvent être modifiés dans les paramètres de configuration de votre boutique Amazon. Ces paramètres incluent :

- Intervalles pour effacer l’historique des logs d’activité
- Sélection de la source cron
- Options de synchronisation des logs

## Modification des paramètres des canaux de commerce

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales Channels]** et choisissez **[!UICONTROL Global Settings]**.

1. Pour **[!UICONTROL Clear Log History]**, choisissez une option :

   - `Once Daily` - Choisissez d’effacer l’historique de vos activités de magasin une fois par jour.

   - `Once Weekly` - Choisissez d’effacer l’historique de vos activités de magasin une fois par semaine.

   - `Once Monthly` - (Par défaut) Choisissez d’effacer l’historique de vos activités de magasin une fois par mois.

1. Pour **[!UICONTROL Background Tasks (CRON) Source]**, choisissez `Magento CRON`.

   Cette option permet au canal de vente Amazon d’utiliser vos paramètres [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) pour déterminer les intervalles de communication et de synchronisation des données avec [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Enable Debug Logging]**, choisissez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque le dépannage est nécessaire.

   La journalisation du canal de vente Amazon est écrite dans le fichier `{Commerce Root}/var/log/channel_amazon.log` et peut être visualisée en [mode développeur](https://docs.magento.com/user-guide/magento/installation-modes.html){:target=&quot;_blank&quot;}. La journalisation ne doit être `Enabled` que lors du dépannage et doit être `Disabled` une fois le dépannage terminé.

1. Cliquez sur **[!UICONTROL Save Config]**.

![Paramètres de configuration du Sales Channel](assets/config-sales-channel-global-settings.png)
