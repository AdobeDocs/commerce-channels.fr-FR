---
title: Mise à jour des informations requises sur Amazon
description: Le canal de vente Amazon fournit l’onglet Incomplet pour surveiller les produits du catalogue Commerce qui ne contiennent pas les informations requises par Amazon.
feature: Sales Channels, Merchandising, Catalog Management, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Mettre à jour les informations requises (liste incomplète)

Les listes affichées dans l’onglet _[!UICONTROL Incomplete]_incluent vos produits de catalogue [!DNL Commerce] qui répondent à vos exigences d’éligibilité Amazon telles que définies dans vos règles de liste, mais qui ne contiennent pas les informations requises par Amazon avant la mise en liste.

## Mise à jour des informations requises (impossible d’affecter à la liste Amazon) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Affichez les listes dans l’onglet _[!UICONTROL Incomplete]_de [Gérer les listes](./managing-product-listings.md).

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Passez en revue les informations sur les produits du catalogue (SKU et nom du produit) pour lesquelles vous essayez de créer une correspondance avec une liste Amazon.

1. Pour **[!UICONTROL Assign ASIN]**, saisissez l’ASIN attribué par Amazon pour la liste que vous souhaitez faire correspondre au produit du catalogue.

1. Pour enregistrer la correspondance du produit, cliquez sur **[!UICONTROL Save Listing Update]**.

La liste est maintenant mise en correspondance avec votre catalogue. La liste est alors mise à jour et publiée dans Amazon en fonction de vos paramètres cron et de liste. Il est également supprimé de l’onglet _[!UICONTROL Incomplete]_.

![Attribuez manuellement ASIN pour qu’il n’y ait aucune correspondance de liste](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## Mise à jour des informations requises (plusieurs correspondances trouvées) {#update-required-info-multiple-matches-found}

1. Affichez les listes dans l’onglet _[!UICONTROL Incomplete]_de [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Dans la colonne _Action_, cliquez sur **Sélectionner** > **Mettre à jour les informations requises** pour la liste que vous souhaitez mettre à jour.

1. Passez en revue les informations sur les produits du catalogue (SKU et nom du produit) pour lesquelles vous essayez de créer une correspondance avec une liste Amazon.

1. Pour **[!UICONTROL Select Correct Amazon Listing]**, choisissez l’ASIN correct pour la liste que vous souhaitez faire correspondre à ce produit.

   Les options répertoriées ici incluent des produits de catalogue identifiés comme pouvant correspondre. Si aucune des options n’est correcte, vous pouvez choisir `Manually Enter Correct ASIN` et saisir manuellement l’ASIN du produit.

1. Si vous saisissez l’ASIN manuellement, saisissez l’ASIN correct pour **[!UICONTROL Manually Assign ASIN]**.

1. Pour enregistrer la correspondance du produit, cliquez sur **[!UICONTROL Save Listing Update]**.

![Sélectionner manuellement ASIN parmi plusieurs correspondances possibles](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## Mettre à jour les informations requises (avec des variantes) {#update-required-info-has-variants}

1. Affichez les listes dans l’onglet _[!UICONTROL Incomplete]_de [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Passez en revue les informations sur les produits du catalogue (SKU et nom du produit) pour lesquelles vous essayez de créer une correspondance avec une liste Amazon.

1. Pour **[!UICONTROL Select Correct Amazon Listing]**, choisissez l’ASIN correct pour la liste que vous souhaitez faire correspondre à ce produit.

   Les options répertoriées ici incluent des produits de catalogue identifiés comme pouvant correspondre. Si aucune des options n’est correcte, vous pouvez sélectionner `Manually Enter Correct ASIN` et saisir manuellement l’ASIN du produit.

1. Si vous saisissez l’ASIN manuellement, saisissez l’ASIN correct pour **[!UICONTROL Manually Assign ASIN]**.

1. Pour enregistrer la correspondance du produit, cliquez sur **[!UICONTROL Save Listing Update]**.

## Mise à jour des informations requises (condition manquante) {#update-required-info-missing-condition}

1. Affichez les listes dans l’onglet _[!UICONTROL Incomplete]_de [Gérer les listes](./managing-product-listings.md).

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**pour la liste que vous souhaitez mettre à jour.

1. Passez en revue les informations sur les produits du catalogue (SKU et nom du produit) pour lesquelles vous essayez de créer une correspondance avec une liste Amazon.

1. Pour **[!UICONTROL Condition]**, choisissez la condition appropriée.

   La liste des options disponibles dépend de vos paramètres [ Condition de liste de produits](./product-listing-condition.md) .

1. Pour enregistrer la correspondance du produit, cliquez sur **[!UICONTROL Save Listing Update]** .

![Mettre à jour manuellement la condition manquante](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
