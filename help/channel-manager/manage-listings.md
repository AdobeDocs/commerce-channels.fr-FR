---
title: Gestion des commandes
description: Gestion des listes de canaux de vente pour un [!DNL Commerce] stockez avec le Gestionnaire de canaux pour Adobe Commerce et Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: f1a42dab1dbbc629ba01a4fcd8ade1052697d5a5
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Gérer les listes

Gérer les listes de produits pour un canal connecté à partir de[!UICONTROL Listings] dans la vue de magasin de canaux.

L’espace de travail Listes comprend les produits pour les listes sur Walmart Marketplace et fournit les outils pour gérer les listes. L’état d’une liste individuelle indique où se trouve le produit dans la variable [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs.

![Page Listes d’un canal de vente connecté](assets/products-submit-for-matching.png)

## Afficher les listes

1. Depuis l’administrateur, accédez à [!UICONTROL **Marketing** > Canaux > **Gestionnaire de canaux**].

1. Dans la liste Boutique de canaux , sélectionnez l’icône en forme de crayon dans une ligne d’entrée de magasin pour ouvrir la vue de magasin.

1. Sélectionner [!UICONTROL **Listes**].


## Publier des produits sur Walmart

Vous pouvez créer des offres de produits sur Walmart Marketplace à l’aide de la correspondance de produits ou en chargeant manuellement les listes de produits pour les nouveaux produits. Pour obtenir des instructions, voir [Publier les listes sur Walmart Marketplace](publish-listings-to-marketplace.md) comme décrit dans les rubriques suivantes :

* **[Faire correspondre des produits sur Walmart](publish-listings-to-marketplace.md)**-Publier les listes de produits de votre canal vers [!DNL Walmart Marketplace] en mettant à jour les listes existantes qui vendent le même produit. Les critères de correspondance sont déterminés par la variable [configuration du mappage d’attributs](map-product-attributes-for-matching.md) pour votre canal.

* **Chargement manuel de nouvelles listes**- Pour les produits qui ne correspondent pas à une liste existante sur Walmart Marketplace, utilisez un modèle Excel de catégorie de produits Walmart pour charger en masse des listes de produits.

## A propos des commandes d&#39;énumération et des informations

**Contrôles pour[!UICONTROL Listings]**

| **Attribut** | **Niveau d’exigence** |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actualiser les produits | Met à jour l’affichage avec les données de statut et de liste les plus récentes. |
| Ajouter des produits | Ouvre la [!UICONTROL  Admin Product Catalog] pour sélectionner les produits à ajouter à votre [!DNL Walmart Marketplace] ou pour mettre à jour les attributs de produit afin de répondre aux exigences de liste de Walmart Marketplace. |
| Faire correspondre des produits sur Walmart | Après avoir sélectionné un ou plusieurs produits à l’état En création, sélectionnez Match products sur Walmart pour rechercher des offres de produits qui peuvent être ajoutées à un produit existant.[!DNL Walmart Marketplace] Liste. |


**Descriptions des colonnes**

| **Champ** | **Description** |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom du produit | Nom du produit de la [!DNL Commerce] catalogue de magasin. |
| SKU (identifiant unique) | Attribut mappé utilisé pour faire correspondre les produits sur le marché. Ce nom de champ varie en fonction de la configuration de l’attribut mappé pour [!DNL Channel Manager] des listes. Dans ce cas, l’opération de mise en correspondance de produit utilise le SKU du produit provenant de la variable [!DNL Commerce] catalogue pour trouver un [!DNL Walmart Marketplace]  Listage avec une valeur de SKU qui correspond à la valeur de SKU des attributs de produit Commerce. |
| Quantité | Quantité d’inventaire disponible dans Adobe Commerce ou Magento Open Source. |
| Prix | Le prix du produit de la variable [!DNL Commerce] catalogue de magasin. Les mises à jour des prix du catalogue sont synchronisées avec Channel Manager, puis envoyées à [!DNL Walmart Marketplace]  afin que les éléments répertoriés affichent le prix actuel. |
| État | Indique l’état actuel de la commande dans la variable [!DNL Commerce] workflow de commande. L’état est mis à jour lorsque vous ajoutez des produits à [!DNL Channel Manager] et lorsque vous faites correspondre des produits sur le marché. Si une opération échoue, la liste affiche le statut Erreur . Après avoir corrigé l’erreur, [!DNL Channel Manager] tente à nouveau l’opération et met à jour l’état. |


### À propos de l’état de liste

Dans l’espace de travail Liste, le libellé État indique où se trouve un produit dans la variable [!DNL Channel Manager] afin que vous puissiez déterminer les étapes suivantes et résoudre les erreurs. Etat du produit*.

* **[!UICONTROL Draft]**-Identifie les produits qui n’ont pas été [envoyé à [!DNL Walmart] pour la correspondance](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**- Identifie les produits envoyés pour correspondance dans le [!DNL Walmart Marketplace]. Les produits restent dans *Traitement* jusqu’à ce que la variable [!DNL Walmart Marketplace] renvoie un message d’état HTTP indiquant si la correspondance a réussi ou si une erreur s’est produite. Cela peut prendre jusqu’à 30 minutes pour que l’opération de correspondance se termine sur la variable [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**- Identifie les produits qui ont été mis en correspondance avec succès sur Walmart.

   Une correspondance se produit lorsque l’attribut de produit value-UPC code par exemple, correspond à la valeur UPC dans un[!DNL Walmart Marketplace] Liste. Lorsqu’un produit correspond, l’offre de produit Commerce est ajoutée à la liste Walmart existante.

   Vérifiez les [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) tableau de bord pour examiner la mise à jour de la liste de produits et vérifier les détails du produit, le prix et la quantité d’inventaire.


* **[!UICONTROL Error]**- Identifie les produits qui n’ont pas été mis en correspondance avec un [!DNL Walmart Marketplace] Liste. Pour afficher les détails des erreurs, survolez le *Erreur* libellé d’état.

   Après avoir résolu l’erreur, soumettez de nouveau le produit pour qu’il corresponde. Voir [Dépannage des erreurs de correspondance de produit](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]**- Identifie les produits correspondants sur [!DNL Walmart] qui ne peut pas être publié tant que la variable [!DNL Walmart Marketplace] Le magasin est en ligne. Les produits avec ce statut sont publiés automatiquement lorsque la variable [!DNL Walmart Marketplace] le magasin est actif.
