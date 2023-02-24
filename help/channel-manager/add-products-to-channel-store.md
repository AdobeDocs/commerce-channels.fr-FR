---
title: Ajout de produits au Gestionnaire de canaux
description: "Créer un assortiment de produits pour [!DNL Walmart Marketplace] ventes en ajoutant les produits du catalogue au canal de vente configuré dans le Gestionnaire de canaux."
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Ajouter des produits à [!DNL Channel Manager]

Pour ajouter des produits au [!DNL Walmart Marketplace] canal de vente, sélectionnez-les dans la [!DNL Commerce] catalogue de produits et les importer dans [!DNL Channel Manager].
Le processus d’importation peut prendre jusqu’à 30 minutes ou plus en fonction du nombre de produits que vous sélectionnez.

## Condition requise

**[Mise en correspondance des attributs de catalogue](map-catalog-attributes.md)**: dans le [!DNL Channel Settings] configuration, mappez au moins un attribut de la propriété [!DNL Commerce] catalogue de produits à l’un des identifiants de produits Walmart requis : -GTIN, ISBN, ISSN, UPC, EAN.

## Exigences d’énumération

[!DNL Commerce] les listes de produits doivent avoir la configuration d’attribut requise suivante :

- **[!UICONTROL Connect to Channel Manager]** est activé

- Spécifiez des valeurs valides pour les attributs Walmart requis.

   - Au moins un attribut de produit qui correspond à l’un des attributs requis [!DNL Walmart Marketplace] identifiants de produit - GTIN, ISBN, ISSN, UPC, EAN.

   - Prix du produit spécifié à un maximum de deux décimales, par exemple `9.99`

   - Poids du produit spécifié à un maximum de deux décimales, par exemple `1.25`

>[!TIP]
>
>Pour plus d’informations sur l’optimisation des listes pour votre canal de vente, voir [Guide d’optimisation de la qualité de la liste Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Ajout de produits

1. Dans une boutique de canaux de vente connectée, sélectionnez **Ajout de produits** pour ouvrir le catalogue de produits.

   ![Ajout de produits à la boutique de canaux de vente](assets/add-initial-products-to-connected-channel.png)

   Le catalogue s’ouvre dans un nouvel onglet.

1. Dans la grille de produits du catalogue, sélectionnez les produits sur lesquels vendre. [!DNL Walmart Marketplace].

   ![Envoi de produits à la boutique de canaux de vente](assets/select-products-from-catalog.png)

1. Activez la variable **[!UICONTROL Connect to Channel Manager]** pour les éléments sélectionnés.

   - De **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Update attributes]**.

   - Faites défiler l’écran jusqu’à **[!UICONTROL Connect to Channel Manager]** et activez-la.

   - Vérifiez que les attributs de produit incluent au moins l’un des attributs requis [!DNL Walmart Product IDs].

   - Sélectionner **[!UICONTROL Save]**.

      Un message de confirmation s’affiche.

      ![Message de confirmation d’importation de produit du catalogue au canal de vente](assets/product-import-from-catalog-confirmation.png)

      Si le message indique que la mise à jour est planifiée, utilisez la variable [queue:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] pour traiter immédiatement la mise à jour.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. Une fois l’opération d’importation terminée, vérifiez les produits que vous avez ajoutés en revenant à [!DNL Channel Manager] et sélection **[!UICONTROL Listings]**.

   Au départ, les produits sont *Version préliminaire* statut. Sélectionner **[!UICONTROL Refresh products]** pour mettre à jour le tableau.

1. Mettez à jour la vue pour afficher les nouveaux produits ajoutés au Gestionnaire de canaux en sélectionnant le **[!UICONTROL Draft]** carte d’état.

   ![Produits importés sur le canal de vente connecté](assets/products-in-marketplace-sales-channel.png)


