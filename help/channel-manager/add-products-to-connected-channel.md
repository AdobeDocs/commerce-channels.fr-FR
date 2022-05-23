---
title: Ajout de produits à la boutique de canaux de vente
description: Créer un assortiment de produits pour [!DNL Walmart Marketplace] ventes en ajoutant des produits du catalogue au canal de vente
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 76aa7451c9df83fbb7ea808fc14ef2d306235da2
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Ajout de produits à la boutique de canaux de vente

Pour synchroniser les produits avec le canal de vente Walmart Marketplace, vous sélectionnez les produits dans la variable [!DNL Commerce] Catalogue de produits et importez-les dans Channel Manager. Les produits sélectionnés doivent avoir la configuration d’attribut suivante :

- **[!UICONTROL Publish to Channel Manager]** est activé

- Au moins un attribut de produit doit correspondre à l’un des attributs [Attributs requis de Walmart Marketplace](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

Processus d’importation de produits à partir de [!DNL Commerce] jusqu’à 30 minutes ou plus peuvent s’écouler entre le Gestionnaire de canaux en fonction du nombre de produits sélectionnés.

## Ajout de produits

1. Dans une boutique de canaux de vente connectée, sélectionnez **Ajout de produits** pour ouvrir le catalogue de produits.

   ![Ajout de produits à la boutique de canaux de vente](assets/add-initial-products-to-connected-channel.png)

   Le catalogue s’ouvre dans un nouvel onglet.

1. Dans la grille de produits du catalogue, sélectionnez les produits sur lesquels vendre. [!DNL Walmart Marketplace].

   ![Envoi de produits à la boutique de canaux de vente](assets/select-products-from-catalog.png)

1. Activez la variable **[!UICONTROL Publish to Channel Manager]** pour les éléments sélectionnés.

   - De **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Update attributes]**.

   - Faites défiler l’écran jusqu’à **[!UICONTROL Publish to Channel Manager]** et activez-la.

   - Vérifiez que les attributs de produit incluent au moins un des ID de produit Walmart requis.

   - Sélectionner **[!UICONTROL Save]**.

      Un message de confirmation s’affiche.

      ![Message de confirmation d’importation de produit du catalogue au canal de vente](assets/product-import-from-catalog-confirmation.png)

      Si le message indique que la mise à jour est planifiée, utilisez la variable [queue:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] pour traiter immédiatement la mise à jour.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. Une fois l’opération d’importation terminée, vérifiez les produits ajoutés en revenant à [!DNL Channel Manager] et sélection **[!UICONTROL Listings]**.

   ![Produits importés sur le canal de vente connecté](assets/products-in-marketplace-sales-channel.png)

   Au départ, les produits sont *Version préliminaire* statut. Sélectionner **[!UICONTROL Refresh products]** pour mettre à jour le tableau.

