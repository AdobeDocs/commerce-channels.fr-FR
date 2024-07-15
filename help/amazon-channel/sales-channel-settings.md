---
title: Paramètres du canal de vente
description: Pour gérer la journalisation, la source cron et la synchronisation des fonctions de canal de vente Amazon, mettez à jour la configuration Commerce.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Paramètres du canal de vente

Lorsque l’extension [!DNL Amazon Sales Channel] est installée, les valeurs par défaut sont définies dans le canal de vente Admin for Amazon. Ces paramètres peuvent être modifiés dans les paramètres de configuration de votre boutique Amazon. Ces paramètres incluent :

- Intervalles pour effacer l’historique des logs d’activité
- Sélection de la source cron
- Options de synchronisation des logs

## Modification des paramètres des canaux Commerce

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales Channels]** et choisissez **[!UICONTROL Global Settings]**.

1. Pour **[!UICONTROL Clear Log History]**, choisissez une option :

   - `Once Daily` - Choisissez d’effacer l’historique de vos activités de magasin une fois par jour.

   - `Once Weekly` - Choisissez d’effacer l’historique de vos activités de magasin une fois par semaine.

   - `Once Monthly` - (Par défaut) Choisissez d’effacer l’historique de vos activités de magasin une fois par mois.

1. Pour **[!UICONTROL Background Tasks (CRON) Source]**, choisissez `Magento CRON`.

   Cette option permet au canal de vente Amazon d’utiliser vos paramètres [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) pour déterminer les intervalles de communication et de synchronisation des données avec [!DNL Amazon Seller Central].

1. Pour **[!UICONTROL Enable Debug Logging]**, choisissez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque la résolution des problèmes est nécessaire.

   La journalisation du canal de vente Amazon est écrite dans le fichier `{Commerce Root}/var/log/channel_amazon.log` et peut être visualisée en [mode développeur](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). La journalisation ne doit être que `Enabled` au cours de la résolution des problèmes et doit être `Disabled` une fois le dépannage terminé.

1. Pour **[!UICONTROL Read-Only Mode]**, sélectionnez `Enabled` pour bloquer toutes les demandes d’API qui changent l’état sortant.

   Avec ce paramètre, les modifications potentielles sont enregistrées, mais ne sont pas envoyées, jusqu’à ce que [!UICONTROL Read-Only Mode] soit désactivé. Le cache de configuration doit être effacé pour que le mode lecture seule soit activé. Pour redémarrer les transferts de données, sélectionnez `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] est conçu pour les copies de l’instance de production, telles que l’évaluation ou l’assurance qualité, et ne doit pas être utilisé sur l’instance de production.
   >
   >Lorsqu&#39;une base de données est migrée vers une nouvelle copie de l&#39;instance (détectée lorsque l&#39;URL d&#39;un magasin change dans la configuration), [!UICONTROL Read-Only Mode] est automatiquement activé.

1. Cliquez sur **[!UICONTROL Save Config]**.

![Paramètres de configuration du Sales Channel](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
