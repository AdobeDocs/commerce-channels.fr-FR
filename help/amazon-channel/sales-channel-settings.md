---
title: Paramètres du Sales Channel
description: Pour gérer la journalisation, la source cron et la synchronisation des fonctions de canal de vente Amazon, mettez à jour la configuration Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Paramètres du Sales Channel

Lorsque la variable [!DNL Amazon Sales Channel] est installée, les valeurs par défaut sont définies dans le canal de vente Admin for Amazon. Ces paramètres peuvent être modifiés dans les paramètres de configuration de votre boutique Amazon. Ces paramètres incluent :

- Intervalles pour effacer l’historique des logs d’activité
- Sélection de la source cron
- Options de synchronisation des logs

## Modification des paramètres des canaux de commerce

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales Channels]** et choisissez **[!UICONTROL Global Settings]**.

1. Pour **[!UICONTROL Clear Log History]**, choisissez une option :

   - `Once Daily` - Choisissez d’effacer l’historique de vos activités de magasin une fois par jour.

   - `Once Weekly` - Choisissez d’effacer l’historique de vos activités de magasin une fois par semaine.

   - `Once Monthly` - (Par défaut) Choisissez d’effacer l’historique de vos activités de magasin une fois par mois.

1. Pour **[!UICONTROL Background Tasks (CRON) Source]**, choisissez `Magento CRON`.

   Cette option permet au canal de vente Amazon d’utiliser votre [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) paramètres permettant de déterminer les intervalles de communication et de synchronisation des données avec [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Enable Debug Logging]**, choisissez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque la résolution des problèmes est nécessaire.

   La journalisation du canal de vente Amazon est écrite dans la variable `{Commerce Root}/var/log/channel_amazon.log` et peuvent être affichés dans [mode développeur](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}. La journalisation doit uniquement être `Enabled` lors du dépannage et doit être `Disabled` lorsque le dépannage est terminé.

1. Pour **[!UICONTROL Read-Only Mode]**, sélectionnez `Enabled` pour bloquer toutes les demandes d’API qui changent l’état sortantes.

   Avec ce paramètre, les modifications potentielles sont enregistrées, mais pas envoyées, jusqu’à ce que [!UICONTROL Read-Only Mode] est désactivée. Le cache de configuration doit être effacé pour que le mode lecture seule soit activé. Pour redémarrer les transferts de données, sélectionnez `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] est conçu pour les copies de l’instance de production, telles que l’évaluation ou l’assurance qualité, et ne doit pas être utilisé sur l’instance de production.
   >
   >Lorsqu&#39;une base de données est migrée vers une nouvelle copie de l&#39;instance (détectée lorsque l&#39;URL d&#39;un magasin change dans la configuration), [!UICONTROL Read-Only Mode] est activé automatiquement.

1. Cliquez sur **[!UICONTROL Save Config]**.

![Paramètres de configuration du Sales Channel](assets/config-sales-channel-global-settings.png)
