---
title: Gérer les listes
description: Gestion des listes de canaux de vente pour un [!DNL Commerce] stockez avec le Gestionnaire de canaux pour Adobe Commerce et Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: ee103895e1035e04a4601857032caa172d493a31
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Gestion des listes

Gestion des listes de produits pour le [!DNL Walmart Marketplace] canal de vente à partir de [!UICONTROL Listings] dans la vue de magasin de canaux. L’état d’une liste individuelle indique où se trouve le produit dans la variable [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs.

L’état d’une liste individuelle indique où se trouve le produit dans la variable [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs.

![Page Listes d’un canal de vente connecté](assets/product-listing-landing.png)

Vous pouvez effectuer les tâches suivantes depuis la vue Liste.

* Afficher les listes actuelles
* Tri et filtrage des listes
* Ajout de produits
* Correspondance de produits
* Suivi de l’état de liste

## Afficher les listes de produits

1. Depuis l’administrateur, accédez à [!UICONTROL **Marketing** > Canaux > **Gestionnaire de canaux**].

1. Dans la liste Boutique de canaux , sélectionnez l’icône en forme de crayon dans une ligne d’entrée de magasin pour ouvrir la vue de magasin.

1. Sélectionner [!UICONTROL **Listes**].

1. Triez les *Liste* en sélectionnant un en-tête de colonne dans la *Liste* table.

1. Filtrez les *Liste* en sélectionnant l’une des cartes de comptage d’état.

1. Réinitialisez l’ordre de tri et supprimez les filtres en sélectionnant **Actualiser les produits**.

## Ajout de produits Commerce à Channel Manager

Créez l’assortiment de produits pour le canal Walmart Marketplace en procédant comme suit :

* [Ajout de produits de votre catalogue de produits Commerce à Channel Manager](add-products-to-channel-store.md)

* [Mise en correspondance des attributs de catalogue](map-catalog-attributes.md#configure-product-attribute-settings)

## Publier des produits sur Walmart

Vous pouvez créer des offres de produits sur Walmart Marketplace à l’aide de la correspondance de produits ou en chargeant manuellement les listes de produits pour les nouveaux produits. Pour obtenir des instructions, voir [Publier les listes sur Walmart Marketplace](publish-listings-to-marketplace.md) comme décrit dans les rubriques suivantes :

* **[Faire correspondre des produits sur Walmart](publish-listings-to-marketplace.md)**-Publier les listes de produits de votre canal vers [!DNL Walmart Marketplace] en mettant à jour les listes existantes qui vendent le même produit. Les critères de correspondance sont déterminés par la variable [configuration du mapping des attributs](map-catalog-attributes.md) pour votre canal.

* **[Chargement manuel de nouvelles listes](publish-listings-to-marketplace.md#upload-new-product-listings)-**- Pour les produits qui ne correspondent pas à une liste existante sur Walmart Marketplace, utilisez un modèle Excel de catégorie de produits Walmart pour charger en masse des listes de produits.

## Commandes de liste et descriptions de colonnes

Les tableaux suivants décrivent les contrôles et les colonnes disponibles pour [!UICONTROL Listings].

**Contrôles pour[!UICONTROL Listings]**

| **Contrôle** | **Description** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Ouvre la [!UICONTROL Admin Product Catalog] pour sélectionner les produits à ajouter à votre [!DNL Walmart Marketplace] ou pour mettre à jour les attributs de produit afin de répondre aux exigences de liste de Walmart Marketplace. |
| [!UICONTROL Match products on Walmart] | Après avoir sélectionné un ou plusieurs produits à l’état En création, sélectionnez Match products sur Walmart pour rechercher des offres de produits qui peuvent être ajoutées à un produit existant. [!DNL Walmart Marketplace] Liste. |
| [!UICONTROL Refresh products] | Mettez à jour l’affichage avec la liste et l’état les plus récents. Ce contrôle réinitialise également la vue Liste à l’ordre de tri par défaut et supprime les filtres. |
| [!UICONTROL Filter by *État*] | Affichez uniquement les listes ayant un état spécifique en sélectionnant une carte de comptage de l’état au-dessus du tableau Listes . Utilisez la variable *Actualiser les produits* pour supprimer le filtre. |
| [!UICONTROL Sort products] | Modifiez l’ordre de tri des listes en sélectionnant un en-tête de colonne. |


**Descriptions des colonnes**

| **Champ** | **Description** |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Nom du produit de la [!DNL Commerce] catalogue de magasin. |
| [!UICONTROL SKU (Unique ID)] | Attribut mappé utilisé pour faire correspondre les produits sur le marché. Ce nom de champ varie en fonction de la configuration de l’attribut mappé pour [!DNL Channel Manager] des listes. Dans ce cas, l’opération de mise en correspondance de produit utilise le SKU du produit provenant de la variable [!DNL Commerce] catalogue pour trouver un [!DNL Walmart Marketplace]  Liste avec une valeur de SKU correspondant à la valeur de SKU de la variable [!DNL Commerce] attributs de produit. |
| [!UICONTROL  Quantity] | Quantité d’inventaire disponible dans Adobe Commerce ou Magento Open Source. |
| [!UICONTROL Price] | Le prix du produit de la variable [!DNL Commerce] catalogue de magasin. Les mises à jour des prix du catalogue sont synchronisées avec Channel Manager, puis envoyées à [!DNL Walmart Marketplace]  afin que les éléments répertoriés affichent le prix actuel. |
| [!UICONTROL Status] | Indique l’état actuel de la commande dans la variable [!DNL Commerce] workflow de commande. L’état est mis à jour lorsque vous ajoutez des produits à [!DNL Channel Manager] et lorsque vous faites correspondre des produits sur le marché. Si une opération échoue, la liste affiche un état d’erreur. Après avoir corrigé l’erreur, [!DNL Channel Manager] tente à nouveau l’opération et met à jour l’état. |
| [!UICONTROL Status Detail] | Fournit des informations supplémentaires sur les produits avec *Erreur* ou *Correspondance* statut. |

### À propos de l’état de liste

Dans l’espace de travail Liste, le libellé État indique où se trouve un produit dans la variable [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs. Les listes peuvent avoir les libellés d’état suivants :

* **[!UICONTROL Draft]**-Identifie les produits qui n’ont pas été [envoyé à [!DNL Walmart] pour la correspondance](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**- Identifie les produits envoyés pour correspondance dans le [!DNL Walmart Marketplace]. Les produits restent dans *Traitement* jusqu’à ce que la variable [!DNL Walmart] renvoie un message d’état HTTP indiquant si la correspondance a réussi ou si une erreur s’est produite. Cela peut prendre jusqu’à 30 minutes pour que l’opération de correspondance se termine sur la variable [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**- Identifie les produits qui ont fait l’objet d’une correspondance réussie sur [!DNL Walmart].

   Une correspondance se produit lorsque l’attribut de produit value-UPC code par exemple, correspond à la valeur UPC dans un[!DNL Walmart Marketplace] Liste. Lorsqu’un produit correspond, l’offre de produit Commerce est ajoutée à la liste Walmart existante.

   Vérifiez les [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) tableau de bord pour examiner la mise à jour de la liste de produits et vérifier les détails du produit, le prix et la quantité d’inventaire.

* **[!UICONTROL Match - Match in Stage]**- Identifie les produits correspondants sur [!DNL Walmart] qui ne peut pas être publié tant que la variable [!DNL Walmart Marketplace] Le magasin est en ligne. Les produits avec ce statut sont publiés automatiquement lorsque la variable [!DNL Walmart Marketplace] le magasin est actif.

* **[!UICONTROL Error]**- Identifie les produits qui n’ont pas été mis en correspondance avec un [!DNL Walmart Marketplace] Liste.

* **[!UICONTROL Error description]**- Fournit des informations détaillées sur l’erreur de liste.

   Après avoir résolu l’erreur, soumettez de nouveau le produit pour qu’il corresponde. Voir [Dépannage des erreurs de correspondance de produit](publish-listings-to-marketplace.md#troubleshoot-product-match-errors).
