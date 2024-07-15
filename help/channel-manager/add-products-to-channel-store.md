---
title: Ajout de produits au Gestionnaire de canaux
description: "Créez un assortiment de produits pour les  [!DNL Walmart Marketplace] ventes en ajoutant des produits du catalogue au canal de vente configuré dans le Gestionnaire de canaux."
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Ajout de produits à [!DNL Channel Manager]

Pour ajouter des produits au canal de vente [!DNL Walmart Marketplace], sélectionnez-les dans le catalogue de produits [!DNL Commerce] et importez-les dans [!DNL Channel Manager].
Le processus d’importation peut prendre jusqu’à 30 minutes ou plus en fonction du nombre de produits que vous sélectionnez.

## Condition requise

**[Mapper les attributs de catalogue](map-catalog-attributes.md)** : dans la configuration [!DNL Channel Settings], mappez au moins un attribut du catalogue de produits [!DNL Commerce] à l’un des identifiants de produit Walmart requis : -GTIN, ISBN, ISSN, UPC, EAN.

## Exigences d’énumération

Les listes de produits [!DNL Commerce] doivent avoir la configuration d’attribut requise suivante :

- L’attribut **[!UICONTROL Connect to Channel Manager]** est activé

- Spécifiez des valeurs valides pour les attributs Walmart requis.

   - Au moins un attribut de produit qui correspond à l’un des identifiants de produit [!DNL Walmart Marketplace] requis : GTIN, ISBN, ISSN, UPC, EAN.

   - Prix du produit spécifié à un maximum de deux décimales, par exemple `9.99`

   - Poids du produit spécifié à un maximum de deux décimales, par exemple `1.25`

>[!TIP]
>
>Pour plus d’informations sur l’optimisation des listes pour votre canal de vente, consultez le [Guide d’optimisation de la qualité pour les listes Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Ajout de produits

1. Dans une boutique de canaux de vente connectée, sélectionnez **Ajouter des produits** pour ouvrir le catalogue de produits.

   ![Ajouter des produits à la boutique de canaux de vente](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   Le catalogue s’ouvre dans un nouvel onglet.

1. Dans la grille de produits du catalogue, sélectionnez les produits à vendre sur [!DNL Walmart Marketplace].

   ![Envoyer des produits à la boutique de canaux de vente](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Activez l’attribut **[!UICONTROL Connect to Channel Manager]** pour les éléments sélectionnés.

   - Depuis **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Update attributes]**.

   - Accédez à l’attribut **[!UICONTROL Connect to Channel Manager]** et activez-le.

   - Vérifiez que les attributs de produit incluent au moins l’un des [!DNL Walmart Product IDs] requis.

   - Sélectionnez **[!UICONTROL Save]**.

     Un message de confirmation s’affiche.

     ![ Message de confirmation d’importation de produit du catalogue au canal de vente](assets/product-import-from-catalog-confirmation.png){width="400"}

     Si le message indique que la mise à jour est planifiée, utilisez la commande [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] pour traiter la mise à jour immédiatement.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. Une fois l’opération d’importation terminée, vérifiez les produits que vous avez ajoutés en revenant à [!DNL Channel Manager] et en sélectionnant **[!UICONTROL Listings]**.

   Au départ, les produits sont à l’état *Brouillon*. Sélectionnez **[!UICONTROL Refresh products]** pour mettre à jour la table.

1. Mettez à jour la vue pour afficher les nouveaux produits ajoutés au Gestionnaire de canaux en sélectionnant la carte d’état **[!UICONTROL Draft]**.

   ![Produits importés sur le canal de vente connecté](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


