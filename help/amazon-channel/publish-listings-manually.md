---
title: Publier manuellement les listes Amazon
description: Si nécessaire, vous pouvez publier manuellement vos listes Amazon terminées à partir de votre administrateur Commerce.
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publier manuellement les listes Amazon

Vous pouvez publier manuellement une ou plusieurs listes Amazon terminées.

1. Affichez une ou plusieurs listes dans l’onglet _[!UICONTROL Ended]_de la page [Listes de produits](./managing-product-listings.md) (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_ou_[!UICONTROL Ineligible]_ ).

1. Dans la colonne de gauche, cliquez pour vérifier chacune des listes que vous souhaitez republier.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Publish Product to Amazon]**.

1. Cliquez sur **[!UICONTROL OK]** dans le message de confirmation.

   Un message s’affiche pour confirmer que les listes sélectionnées sont en cours de traitement pour publication sur Amazon.

   Les informations de liste sont publiées dans Amazon en fonction de vos paramètres cron. Les informations de liste sont envoyées à Amazon lors de la prochaine synchronisation des données. Jusqu’à ce qu’Amazon réponde avec la confirmation de liste, les listes publiées manuellement restent sur l’onglet _Prêt à lister_ avec le statut `List in Progress`. Lorsque la confirmation de la liste est reçue d’Amazon, les listes se déplacent vers l’onglet _Actif_ avec l’état `Active`.
