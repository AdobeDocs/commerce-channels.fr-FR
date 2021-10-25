---
title: Paramètres du Sales Channel
description: Pour gérer la journalisation, la source cron et la synchronisation des fonctions de canal de vente Amazon, mettez à jour la configuration Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Paramètres de Sales Channel

Lorsque [!DNL Amazon Sales Channel] est installée, les valeurs par défaut sont définies dans le canal de vente Admin for Amazon. Ces paramètres peuvent être modifiés dans vos paramètres de configuration pour votre banque Amazon. Ces paramètres sont les suivants :

- Intervalles pour effacer l&#39;historique du journal d&#39;activité
- Sélection de source Cron
- Options de synchronisation du journal

## Modification des paramètres des canaux de commerce

1. Sur la _Administrateur_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales Channels]** et sélectionnez **[!UICONTROL Global Settings]**.

1. Pour **[!UICONTROL Clear Log History]**, choisissez une option :

   - `Once Daily` - Choisissez de effacer l&#39;historique de vos activités de magasin une fois par jour.

   - `Once Weekly` - Choisissez de effacer votre historique d&#39;activité de magasin une fois par semaine.

   - `Once Monthly` - (Par défaut) Choisissez d’effacer votre historique d’activité de magasin une fois par mois.

1. Pour **[!UICONTROL Background Tasks (CRON) Source]**, sélectionnez `Magento CRON`.

   Cette option permet à Amazon Sales Channel d’utiliser votre [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) paramètres permettant de déterminer les intervalles de communication et de synchronisation des données avec [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Enable Debug Logging]**, sélectionnez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque le dépannage est nécessaire.

   La journalisation du canal de vente Amazon est écrite dans `{Commerce Root}/var/log/channel_amazon.log` et peut être affiché dans [mode développeur](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}. La journalisation ne doit être effectuée que `Enabled` pendant le dépannage et doit `Disabled` lorsque le dépannage est terminé.

1. Cliquez sur **[!UICONTROL Save Config]**.

![Paramètres de configuration Sales Channel](assets/config-sales-channel-global-settings.png)
