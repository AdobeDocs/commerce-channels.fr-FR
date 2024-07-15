---
title: Créer et attribuer des produits pour le canal de vente Amazon
description: Amazon Sales Channel fournit l’onglet [!UICONTROL New Third Party] pour vous aider à créer et à attribuer des produits de catalogue Commerce correspondants aux listes Amazon.
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Création et affectation de produits

Lors de l’affichage de l’onglet _[!UICONTROL New Third Party]_, vous pouvez faire correspondre vos produits de catalogue [!DNL Commerce] à une liste Amazon existante. Il existe deux options pour cette correspondance. Vous pouvez affecter une liste à un produit de catalogue existant ou utiliser les informations de la liste pour créer des produits de catalogue. Ces options s’avèrent utiles lorsque vos listes Amazon ne correspondent pas automatiquement à votre catalogue [!DNL Commerce].

La correspondance (ou l’affectation) de vos produits à vos listes Amazon est nécessaire pour utiliser l’ensemble des fonctionnalités du canal de vente Amazon.

Lorsque vous créez un produit de catalogue à partir d’une liste Amazon :

- Le **ASIN** devient le SKU [!DNL Commerce]
- Le **nom de liste de produits** devient le nom de liste de catalogue
- Les **Price** et **Quantity** sont importés depuis la liste Amazon

Le reste des paramètres nécessaires est déterminé par les paramètres de produit [!DNL Commerce] que vous sélectionnez lors de la création.

Une fois créées et mises en correspondance, les listes sont supprimées de l’onglet _[!UICONTROL New Third Party]_et apparaissent dans l’onglet_[!UICONTROL Active]_.

## Attribuer un seul produit de catalogue à une liste Amazon

1. Affichez vos listes de produits dans l’onglet [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Recherchez la liste que vous souhaitez attribuer dans la liste, cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_et cliquez sur **[!UICONTROL Assign Catalog Product]**.

   Cette action ouvre la page _[!UICONTROL Assign Magento Catalog Product]_.

1. Recherchez ou filtrez la liste à l’aide des [commandes de l’espace de travail](./workspace-controls.md) et recherchez le produit de catalogue approprié à la liste.

1. Lorsque le produit correct apparaît dans la liste, cliquez sur **[!UICONTROL Assign Catalog Product]** dans la colonne _[!UICONTROL Action]_.

Votre produit et votre liste correspondent désormais. Le canal de vente Amazon peut désormais partager les données de produit et de liste avec Amazon et gérer votre liste et ses informations, notamment le prix de vente, le prix d’expédition, le stock/la quantité, les informations de commande et l’état, etc.

## Créer un produit de catalogue unique à l’aide des informations de liste Amazon

1. Affichez vos listes de produits dans l’onglet [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Recherchez la liste que vous souhaitez créer dans votre catalogue [!DNL Commerce], cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_et cliquez sur **[!UICONTROL Create New Catalog Product]**.

   Cette action ouvre la page _[!UICONTROL Create Magento Catalog Product]_.

1. Définissez les paramètres du catalogue du produit.

   - Définissez la bascule **[!UICONTROL Enable Product(s)]** sur `Yes` ou `No` (obligatoire).

     |Oui|Choisissez de rendre le produit éligible à vos ventes [!DNL Commerce] storefront.|
|Non|Sélectionnez cette option pour que le produit ne soit pas éligible à vos ventes [!DNL Commerce] de vitrine.|

   - Pour **[!UICONTROL Categories]**, affectez une catégorie au produit (facultatif).

     Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et cochez une case de catégorie. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

   - Pour **[!UICONTROL Website Ids]**, choisissez le site web (storefront) auquel le produit à associer.

     Les options de cette liste dépendent de vos paramètres [!DNL Commerce] [configuration de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), choisissez une option.

     `Default` est la sélection par défaut. Les options de cette liste dépendent des [!DNL Commerce] [ensembles d’attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que vous avez configurés.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

     |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n’est pas inclus dans vos listes storefront, bien qu’il puisse être disponible sous la forme d’une variante d’un autre produit.|
|**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.|
|**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.|
|**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

     Les options qui s’affichent dans cette liste dépendent des [classes d’impôts](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que vous avez configurées.

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Create Catalog Products]**.

Le produit du catalogue est créé dans votre catalogue [!DNL Commerce] et affecté à la liste Amazon à partir de laquelle il a été créé. Maintenant que la liste correspond à une liste Amazon existante, elle est supprimée de l’onglet _[!UICONTROL New Third Party]_et apparaît dans l’onglet_[!UICONTROL Active]_.

## Créer plusieurs produits de catalogue à l’aide de leurs informations de liste Amazon

1. Affichez vos listes de produits dans l’onglet [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Sélectionnez les listes pour lesquelles créer des produits de catalogue.

   Vous pouvez sélectionner des cases à cocher individuelles dans la colonne de gauche ou cliquer sur la flèche vers le bas dans la colonne de haut à gauche et choisir **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create New Catalog Product(s)]**.

1. Pour accepter le message de confirmation et ouvrir la page _[!UICONTROL Create Magento Catalog Product]_, cliquez sur **[!UICONTROL OK]**.

1. Renseignez les paramètres du catalogue pour les produits.

   >[!NOTE]
   >Lors de la création de produits de catalogue pour plusieurs listes sélectionnées, les paramètres de produit saisis sont appliqués à toutes les listes.

   - Définissez la bascule **[!UICONTROL Enable Product(s)]** sur `Yes` ou `No` (obligatoire).

     |Oui|Choisissez de rendre le produit éligible à vos ventes [!DNL Commerce] storefront.|
|Non|Sélectionnez cette option pour que le produit ne soit pas éligible à vos ventes [!DNL Commerce] de vitrine.|

   - Pour **[!UICONTROL Categories]**, affectez une catégorie au produit (facultatif).

     Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et cochez une case de catégorie. Lorsque vous avez terminé, cliquez sur **Terminé**.

   - Pour **[!UICONTROL Website Ids]**, choisissez le site web (storefront) auquel le produit à associer.

     Les options de cette liste dépendent de vos paramètres [!DNL Commerce] [configuration de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), choisissez une option.

     `Default` est la sélection par défaut. Les options de cette liste dépendent des [!DNL Commerce] [ensembles d’attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) que vous avez configurés.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

     |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n’est pas inclus dans vos listes storefront, bien qu’il puisse être disponible sous la forme d’une variante d’un autre produit.|
|**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.|
|**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.|
|**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

     Les options qui s’affichent dans cette liste dépendent des [classes d’impôts](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) que vous avez configurées.

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Create Catalog Products]**.

Les produits du catalogue sont créés dans votre catalogue [!DNL Commerce] et affectés à la liste Amazon à partir de laquelle ils ont été créés. Maintenant que les listes correspondent à leur liste Amazon respective, les listes sont supprimées de l’onglet [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) et apparaissent dans l’onglet [_[!UICONTROL Active]_](./active-listings.md).

![Créer un produit de catalogue Commerce](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Champ | Description |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | (Obligatoire) Si cette option est activée, le produit est visible dans votre vitrine [!DNL Commerce]. Si cette option est désactivée, le produit ne s’affiche pas dans votre vitrine [!DNL Commerce]. |
| [!UICONTROL Categories] | Vous pouvez saisir le nom de la catégorie de votre nouveau produit ou sélectionner une catégorie en cliquant sur la flèche vers le bas pour afficher vos options. Les options dépendent de votre configuration [categories](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html). |
| [!UICONTROL Website Ids] | (Obligatoire) Sélectionnez le site web (storefront) auquel le produit à associer. Les options dépendent de vos paramètres de [!DNL Commerce] [configuration de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) |
| Identifiant du jeu d’attributs | Sélectionnez un jeu d’attributs. Les options dépendent de vos [!DNL Commerce] [ensembles d&#39;attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) configurés. |
| [!UICONTROL Visibility] | Options :<ul><li>**[!UICONTROL Not Visible Individually]** - Le produit n’est pas visible dans votre vitrine [!DNL Commerce] (le plus courant pour les variantes de produits).</li><li>**[!UICONTROL Catalog]** - Permet d’accéder au produit par le biais de la catégorie à laquelle il est associé dans le site web.</li><li>**Recherche** - Permet de ne trouver le produit que par le biais de l’outil de recherche.</li><li>**[!UICONTROL Catalog and Search]** - Permet d’accéder aux produits par le biais de la structure de catégories et à l’aide de l’outil de recherche.</li></ul> |
| [!UICONTROL Assign Tax Class] | Attribuez une classe de taxe au nouveau produit. Les options dépendent de vos [classes d’impôts](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) configurées. |
