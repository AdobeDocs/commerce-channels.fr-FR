---
title: Publier manuellement les listes Amazon
description: Si nécessaire, vous pouvez publier manuellement vos listes Amazon terminées à partir de votre administrateur Commerce.
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publier manuellement les listes Amazon

Vous pouvez publier manuellement une ou plusieurs listes Amazon qui ont été terminées.

1. Afficher une ou plusieurs listes sur le _[!UICONTROL Ended]_sur l’onglet [Listes de produits](./managing-product-listings.md) page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_ou_[!UICONTROL Ineligible]_ ).

1. Dans la colonne de gauche, cliquez pour vérifier chacune des listes que vous souhaitez republier.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Publish Product to Amazon]**.

1. Cliquez sur **[!UICONTROL OK]** dans le message de confirmation.

   Un message s’affiche pour confirmer que les listes sélectionnées sont en cours de traitement pour publication sur Amazon.

   Les informations de liste sont publiées dans Amazon en fonction de vos paramètres cron. Les informations de liste sont envoyées à Amazon lors de la prochaine synchronisation des données. Tant qu’Amazon n’a pas répondu avec la confirmation de liste, les listes publiées manuellement restent sur la page _Prêt à répertorier_ avec un `List in Progress` statut. Lorsque la confirmation de la liste est reçue d’Amazon, les listes se déplacent vers le _Principal_ avec un `Active` statut.
