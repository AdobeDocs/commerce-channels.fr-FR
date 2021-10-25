---
title: Publication manuelle des annonces Amazon
description: Si nécessaire, vous pouvez publier manuellement vos annonces Amazon terminées à partir de votre administrateur Commerce.
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Publication manuelle des annonces Amazon

Vous pouvez publier manuellement une ou plusieurs annonces Amazon terminées.

1. Afficher une ou plusieurs annonces sur le _[!UICONTROL Ended]_dans le menu [Listes de produits](./managing-product-listings.md) page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_, ou_[!UICONTROL Ineligible]_ ).

1. Dans la colonne de gauche, cliquez sur pour vérifier chaque annonce que vous souhaitez republier.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Publish Product to Amazon]**.

1. Cliquez sur **[!UICONTROL OK]** dans le message de confirmation.

   Un message s’affiche pour confirmer que les annonces sélectionnées sont en cours de traitement pour publication vers Amazon.

   Les informations de liste sont publiées vers Amazon en fonction de vos paramètres cron. Les informations de liste sont envoyées à Amazon lors de la prochaine synchronisation des données. Tant qu’Amazon n’aura pas répondu à la confirmation d’inscription, les annonces publiées manuellement resteront sur le _Prêt pour la liste_ avec un `List in Progress` statut. Lorsque la confirmation d’inscription est reçue d’Amazon, les annonces sont placées dans le dossier _Actif_ avec un `Active` statut.
