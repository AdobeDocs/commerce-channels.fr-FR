---
title: Journaux et rapports de magasin
description: Utilisez les journaux et les rapports de magasin pour voir ce qui se passe dans votre boutique Adobe Commerce ou Magento Open Source et vos listes Amazon Marketplace.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Journaux et rapports de magasin

L’extension du canal de vente Amazon comprend des journaux et des rapports de magasin de valeur qui vous permettent de visualiser les modifications qui affectent vos commandes et listes Amazon. Vous pouvez utiliser ces rapports pour voir ce qui se passe dans votre boutique et pour comprendre les différents statuts de liste.

Aucune action n’est disponible pour les journaux ou les rapports de magasin, car il s’agit de fonctionnalités de révision uniquement.

Les journaux suivants sont accessibles à partir du [tableau de bord de la boutique](./amazon-store-dashboard.md).

- Le [Journal des modifications de liste](./listing-changes-log.md) affiche les modifications apportées à votre compte de vendeur Amazon en tant que reflet des paramètres de votre canal de vente Amazon.

- Le [Journal des erreurs de communication](./communication-errors-log.md) affiche les erreurs de communication signalées avec Amazon.

Les rapports suivants spécifiques au magasin sont accessibles à partir de la [tableau de bord de la boutique](./amazon-store-dashboard.md).

- Le [Analyse des prix compétitifs](./competitive-price-analysis.md) Le rapport indique que votre Amazon _prix au rabais_ (prix d’inscription plus prix d’expédition) par rapport à [Buy Box](./buy-box-competitor-pricing.md) prix et [concurrent le plus faible](./lowest-competitor-pricing.md) prix.

- Le [Améliorations de la liste](./listing-improvements.md) Le rapport affiche toutes les améliorations de liste proposées par Amazon pour le magasin sélectionné.

>[!TIP]
>
>Vous pouvez également consulter le fichier journal pour plus d’informations lorsque la résolution des problèmes est nécessaire. Voir [paramètres d’administration du canal de vente](./sales-channel-settings.md). La journalisation de la synchronisation du canal de vente Amazon est écrite dans la variable `{Commerce Root}/var/log/channel_amazon.log` et peuvent être affichés dans [mode développeur](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}.
