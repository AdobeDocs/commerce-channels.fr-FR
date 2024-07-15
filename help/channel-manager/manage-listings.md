---
title: Gérer les listes
description: "Gérez les listes de canaux de vente pour un magasin  [!DNL Commerce] avec le gestionnaire de canaux pour Adobe Commerce et Magento Open Source."
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Gérer les listes

Gérez les listes de produits pour le canal de vente [!DNL Walmart Marketplace] à partir de l’interface utilisateur du Gestionnaire de canaux.

L’état d’une liste individuelle indique où se trouve le produit dans le workflow [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs.

![Page de listes pour un canal de vente connecté](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

Vous pouvez effectuer les tâches suivantes depuis la vue Liste.

* Afficher les listes actuelles
* Tri et filtrage des listes
* Ajout de produits
* Correspondance de produits
* Suivi de l’état de liste
* Vérification de la description d’erreur des listes ayant un état d’erreur

## Afficher les listes de produits

1. Depuis l’administrateur, accédez à [!UICONTROL **Marketing** > **Gestionnaire de canaux**].

1. Dans la liste Boutique, sélectionnez l’icône en forme d’oeil dans une ligne d’entrée de magasin pour ouvrir la vue de magasin.

1. Sélectionnez [!UICONTROL **Listes**].

1. Triez la vue *Liste* en sélectionnant un en-tête de colonne dans la table *Liste*.

1. Filtrez la vue *Liste* en sélectionnant l’une des cartes de comptage d’état.

1. Réinitialisez l’ordre de tri et supprimez les filtres en sélectionnant **Actualiser les produits**.

## Ajout de [!DNL Commerce] produits à Channel Manager

Créez l’assortiment de produits pour le canal [!DNL Walmart Marketplace] en effectuant les tâches suivantes :

* [Ajoutez des produits de votre  [!DNL Commerce] catalogue de produits à [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Mise en correspondance des attributs de catalogue](map-catalog-attributes.md#configure-product-attribute-settings)

## Correspondance de produits sur [!DNL Walmart]

Vous pouvez créer des offres de produits sur le [!DNL Walmart Marketplace] à l’aide de la correspondance de produits ou en chargeant manuellement les listes de produits pour les nouveaux produits.

* **[Faire correspondre des produits sur Walmart](connect-listings-to-marketplace.md)** : connectez les listes de produits de votre canal à [!DNL Walmart Marketplace] en mettant à jour les listes existantes qui vendent le même produit. Les critères de correspondance sont déterminés par la [configuration de mappage d’attribut](map-catalog-attributes.md) pour votre canal.

* **[Chargement manuel de nouvelles listes](connect-listings-to-marketplace.md#upload-new-product-listings)** : pour les produits qui ne correspondent pas à une liste existante sur [!DNL Walmart Marketplace], utilisez un modèle Excel de catégorie de produits [!DNL Walmart] pour charger en masse des listes de produits.

## Commandes de liste et descriptions de colonnes

Les tableaux suivants décrivent les contrôles et les colonnes disponibles pour [!UICONTROL Listings].

**Contrôles pour[!UICONTROL Listings]**

| **Control** | **Description** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Ouvre la page [!UICONTROL Admin Product Catalog] pour sélectionner les produits à ajouter à votre assortiment [!DNL Walmart Marketplace] ou pour mettre à jour les attributs de produit afin de répondre aux exigences de liste de Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Après avoir sélectionné un ou plusieurs produits avec l’état [!UICONTROL Draft], sélectionnez [!UICONTROL Match products on Walmart] pour rechercher des offres de produits qui peuvent être ajoutées à une liste [!DNL Walmart Marketplace] existante. |
| [!UICONTROL Refresh products] | Mettez à jour l’affichage avec la liste et l’état les plus récents. Ce contrôle réinitialise également la vue Liste à l’ordre de tri par défaut et supprime les filtres. |
| [!UICONTROL Filter by *Status*] | Afficher uniquement les listes ayant un statut spécifique en sélectionnant une carte d’état au-dessus du tableau Listes . Supprimez le filtre en sélectionnant **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | Modifiez l’ordre de tri des listes en sélectionnant un en-tête de colonne. |


**Descriptions des colonnes**

| **Field** | **Description** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nom du produit du catalogue du magasin [!DNL Commerce]. |
| [!UICONTROL SKU (Unique ID)] | SKU affecté au produit dans le catalogue [!DNL Commerce]. |
| [!UICONTROL  Quantity] | Quantité d’inventaire disponible dans Adobe Commerce ou Magento Open Source. |
| [!UICONTROL Price] | Prix du produit du catalogue du magasin [!DNL Commerce]. Les mises à jour des prix du catalogue sont synchronisées avec Channel Manager, puis envoyées à [!DNL Walmart Marketplace] afin que les articles répertoriés affichent le prix actuel. |
| [!UICONTROL Status] | Indique l’état actuel de la commande dans le workflow de commande [!DNL Commerce]. L’état est mis à jour lorsque vous ajoutez des produits à [!DNL Channel Manager] et lorsque vous faites correspondre des produits sur la marketplace. Si une opération échoue, la liste affiche un état d’erreur. Après avoir corrigé l’erreur, [!DNL Channel Manager] tente de relancer l’opération et met à jour l’état. |
| [!UICONTROL Error Description] | Fournit des informations d’erreur supplémentaires pour les produits dont l’état est `[!DNL Error]`. |

### À propos de l’état de liste

Dans l’espace de travail Liste, le libellé État indique où se trouve un produit dans le workflow [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs. Les listes peuvent avoir les libellés d’état suivants :

* **[!UICONTROL Draft]**-Identifie les produits qui n’ont pas été [envoyés vers [!DNL Walmart] pour la correspondance](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** : identifie les produits envoyés pour correspondance sur le [!DNL Walmart Marketplace]. Les produits restent à l’état *Processing* jusqu’à ce que [!DNL Walmart] renvoie un message d’état HTTP indiquant si la correspondance a réussi ou si une erreur s’est produite. Cela peut prendre jusqu’à 30 minutes pour que l’opération de correspondance se termine sur [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifie les produits qui ont été mis en correspondance avec succès sur [!DNL Walmart].

  Une correspondance se produit lorsque la valeur d’attribut de produit (par exemple, le code UPC) correspond à la valeur UPC dans une liste [!DNL Walmart Marketplace] existante. Lorsqu’un produit correspond, l’offre de produit Commerce est ajoutée à la liste existante.

  Consultez le tableau de bord [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) pour examiner la liste mise à jour des produits et vérifier les détails, le prix et la quantité de stock du produit.

* **[!UICONTROL Match - Match in Stage]** : identifie les produits correspondants sur [!DNL Walmart] qui ne peuvent pas être connectés tant que le magasin [!DNL Walmart Marketplace] n’est pas actif. Les produits avec ce statut se connectent automatiquement lorsque le magasin [!DNL Walmart Marketplace] est en ligne.

* **[!UICONTROL Error]** : identifie les produits qui n’ont pas été associés à une liste [!DNL Walmart Marketplace] existante.

* **[!UICONTROL Error description]** : fournit des informations détaillées sur l’erreur de liste.

  Après avoir résolu l’erreur, soumettez de nouveau le produit pour qu’il corresponde. Voir [Résolution des problèmes de correspondance de produit](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
