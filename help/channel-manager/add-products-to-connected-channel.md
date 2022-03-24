---
title: Ajout de produits à la boutique de canaux
description: Créez un assortiment de produits pour les ventes Marketplace en ajoutant des produits du catalogue au canal de vente.
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# Ajout de produits à la boutique de canaux

Dans le Gestionnaire de canaux, sélectionnez des produits dans le [!DNL Commerce] catalogue pour les ventes de Walmart Marketplace.

Pour synchroniser les produits avec le canal de vente, les produits sélectionnés doivent avoir la configuration d’attribut suivante :

- **[!UICONTROL Publish to Channel Manager]** est activé

- Au moins un attribut de produit doit correspondre à l’un des attributs [Attributs requis de Walmart Marketplace](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

Une fois les sélections enregistrées, le Gestionnaire de canaux importe les données de produit dans le canal. Ce processus peut prendre jusqu’à 30 minutes.

## Ajout de produits au canal de vente

1. Ouvrez le catalogue de produits associé à votre boutique Channel Manager.

   Dans une boutique de canaux de vente connectée, sélectionnez **Ajout de produits**.

   ![Ajout de produits au canal connecté](assets/add-initial-products-to-connected-channel.png)

   Le catalogue s’ouvre dans un nouvel onglet.

1. Dans la grille de produits du catalogue, sélectionnez les produits à vendre sur Walmart Marketplace.

   ![Envoyer les produits au canal connecté](assets/select-products-from-catalog.png)

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

1. Revenez au canal de vente connecté dans [!DNL Channel Manager].

   Une fois l’opération d’importation terminée, affichez les produits à partir de **[!UICONTROL Listings]**. Au départ, les produits sont *Version préliminaire* statut. Sélectionner [!UICONTROL Refresh products]** pour mettre à jour le tableau.

   ![Produits importés sur le canal de vente connecté](assets/products-in-marketplace-sales-channel.png)
