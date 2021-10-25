---
title: Mettre à jour les informations requises (liste incomplète)
description: Le canal de vente Amazon fournit l'onglet Incomplet pour surveiller les produits de catalogue Commerce qui manquent des informations requises par Amazon.
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Mettre à jour les informations requises (liste incomplète)

Les annonces affichées sur le _[!UICONTROL Incomplete]_, incluez votre [!DNL Commerce] les produits de catalogue qui répondent aux critères d’éligibilité d’Amazon tels que définis dans vos règles d’inscription mais qui sont des informations manquantes requises par Amazon avant l’inscription.

## Mettre à jour les informations requises (impossible d’affecter à la liste Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Affichez les annonces dans le menu _[!UICONTROL Incomplete]_dans [Gérer les annonces](./managing-product-listings.md).

1. Dans la boîte de dialogue _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Consultez les informations sur le produit du catalogue (UGS et Nom du produit) pour lequel vous tentez de faire correspondre une mise en vente Amazon.

1. Pour **[!UICONTROL Assign ASIN]**, entrez l’ASIN assigné par Amazon pour la liste que vous souhaitez faire correspondre au produit du catalogue.

1. Pour enregistrer la correspondance de produit, cliquez sur **[!UICONTROL Save Listing Update]**.

La mise en vente est maintenant mise en correspondance avec votre catalogue, et la mise en vente est ensuite mise à jour et publiée sur Amazon en fonction de vos paramètres de mise en vente et de cron. Il est également supprimé de la _[!UICONTROL Incomplete]_.

![Attribuer manuellement ASIN pour qu’aucune correspondance d’annonce ne soit trouvée](assets/amazon-listing-update-assign-asin.png)

## Mettre à jour les informations requises (plusieurs correspondances trouvées) {#update-required-info-multiple-matches-found}

1. Affichez les annonces dans le menu _[!UICONTROL Incomplete]_dans [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Dans la boîte de dialogue _Action_ , cliquez sur **Sélectionner** > **Mettre à jour les informations requises** pour la liste que vous souhaitez mettre à jour.

1. Consultez les informations sur le produit du catalogue (UGS et Nom du produit) pour lequel vous tentez de faire correspondre une mise en vente Amazon.

1. Pour **[!UICONTROL Select Correct Amazon Listing]**, choisissez l’ASIN correct pour la liste que vous souhaitez faire correspondre à ce produit.

   Les options répertoriées ici incluent des produits de catalogue identifiés comme correspondances possibles. Si aucune des options n’est correcte, vous pouvez choisir `Manually Enter Correct ASIN` et entrez manuellement l’ASIN du produit.

1. Si vous entrez l’ASIN manuellement, entrez l’ASIN correct pour **[!UICONTROL Manually Assign ASIN]**.

1. Pour enregistrer la correspondance de produit, cliquez sur **[!UICONTROL Save Listing Update]**.

![Sélectionner manuellement ASIN à partir de plusieurs correspondances possibles](assets/amazon-listing-update-multiple-matches.png)

## Mettre à jour les informations requises (avec variantes) {#update-required-info-has-variants}

1. Affichez les annonces dans le menu _[!UICONTROL Incomplete]_dans [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Dans la boîte de dialogue _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Consultez les informations sur le produit du catalogue (UGS et Nom du produit) pour lequel vous tentez de faire correspondre une mise en vente Amazon.

1. Pour **[!UICONTROL Select Correct Amazon Listing]**, choisissez l’ASIN correct pour la liste que vous souhaitez faire correspondre à ce produit.

   Les options répertoriées ici incluent des produits de catalogue identifiés comme correspondances possibles. Si aucune des options n’est correcte, vous pouvez sélectionner `Manually Enter Correct ASIN` et entrez manuellement l’ASIN du produit.

1. Si vous entrez l’ASIN manuellement, entrez l’ASIN correct pour **[!UICONTROL Manually Assign ASIN]**.

1. Pour enregistrer la correspondance de produit, cliquez sur **[!UICONTROL Save Listing Update]**.

![Sélection manuelle d’ASIN à partir de variantes de correspondance possibles](assets/amazon-listing-update-multiple-matches.png)

## Mettre à jour les informations requises (condition manquante) {#update-required-info-missing-condition}

1. Affichez les annonces dans le menu _[!UICONTROL Incomplete]_dans [Gérer les annonces](./managing-product-listings.md).

1. Dans la boîte de dialogue _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Consultez les informations sur le produit du catalogue (UGS et Nom du produit) pour lequel vous tentez de faire correspondre une mise en vente Amazon.

1. Pour **[!UICONTROL Condition]**, sélectionnez la condition appropriée.

   La liste des options disponibles dépend de votre [Condition de liste de produits](./product-listing-condition.md) paramètres.

1. Pour enregistrer la correspondance de produit, cliquez sur **[!UICONTROL Save Listing Update]** .

![Mise à jour manuelle de la condition manquante](assets/amazon-update-listing-missing-condition.png)
