---
title: Journaux et rapports de magasin
description: Utilisez les journaux et les rapports de magasin pour voir ce qui se passe dans votre magasin Adobe Commerce ou Magento Open Source et dans vos annonces de place de marché Amazon.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Journaux et rapports de magasin

L&#39;extension du canal de vente Amazon comprend des journaux et des rapports de magasin de valeur qui vous permettent de visualiser les modifications qui affectent vos annonces et commandes Amazon. Vous pouvez utiliser ces rapports pour voir ce qui se passe dans votre magasin et pour comprendre les différents statuts de mise en vente.

Aucune action n’est disponible pour les journaux ou les rapports de magasin, car il s’agit de fonctions de révision uniquement.

Les journaux suivants sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

- Le [Journal des modifications de la liste](./listing-changes-log.md) affiche les modifications qui se sont produites dans votre compte de vendeur Amazon en tant que reflet de vos paramètres de canal de vente Amazon.

- Le [Journal des erreurs de communication](./communication-errors-log.md) affiche toutes les erreurs de communication signalées avec Amazon.

Les rapports spécifiques au magasin suivants sont accessibles à partir de la [tableau de bord de magasin](./amazon-store-dashboard.md).

- Le [Analyse des prix concurrentiels](./competitive-price-analysis.md) indique que votre Amazon _prix à payer_ (prix d&#39;annonce plus prix d&#39;expédition) en ce qui concerne [Buy Box](./buy-box-competitor-pricing.md) prix et [concurrent le plus bas](./lowest-competitor-pricing.md) prix.

- Le [Améliorations de la liste](./listing-improvements.md) affiche toutes les améliorations de listes suggérées fournies par Amazon pour le magasin sélectionné.

>[!TIP]
>
>Vous pouvez également consulter le fichier journal pour obtenir des informations supplémentaires lorsque le dépannage est nécessaire. Voir [paramètres d’administration du canal de vente](./sales-channel-settings.md). La journalisation de la synchronisation des canaux de vente Amazon est écrite dans `{Commerce Root}/var/log/channel_amazon.log` et peut être affiché dans [mode développeur](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}.
