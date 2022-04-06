---
title: Création et attribution de produits
description: Amazon Sales Channel fournit les [!UICONTROL New Third Party] pour créer et attribuer des produits de catalogue Commerce correspondants aux listes Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Création et affectation de produits

Lors de l’affichage _[!UICONTROL New Third Party]_vous pouvez faire correspondre vos [!DNL Commerce] cataloguer les produits dans une liste Amazon existante. Il existe deux options pour cette correspondance. Vous pouvez affecter une liste à un produit de catalogue existant ou utiliser les informations de la liste pour créer des produits de catalogue. Ces options s’avèrent utiles lorsque vos listes Amazon ne correspondent pas automatiquement à vos [!DNL Commerce] catalogue.

La correspondance (ou l’affectation) de vos produits à vos listes Amazon est nécessaire pour utiliser l’ensemble des fonctionnalités du canal de vente Amazon.

Lorsque vous créez un produit de catalogue à partir d’une liste Amazon :

- Le **ASIN** devient la propriété [!DNL Commerce] SKU
- Le **Nom de la liste de produits** devient le nom de la liste du catalogue
- Le **Prix** et **Quantité** sont importées depuis la liste Amazon

Le reste des paramètres nécessaires est déterminé par la variable [!DNL Commerce] paramètres de produit que vous sélectionnez lors de la création.

Une fois créées et mises en correspondance, les listes sont supprimées de la propriété _[!UICONTROL New Third Party]_et s’affichent sur la_[!UICONTROL Active]_ .

## Attribuer un seul produit de catalogue à une liste Amazon

1. Affichez vos listes de produits sur la page [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Recherchez la liste que vous souhaitez affecter dans la liste, puis cliquez sur **[!UICONTROL Select]** dans le _[!UICONTROL Action]_, puis cliquez sur **[!UICONTROL Assign Catalog Product]**.

   Cette action ouvre la fenêtre _[!UICONTROL Assign Magento Catalog Product]_page.

1. Recherchez ou filtrez la liste à l’aide du [contrôles workspace](./workspace-controls.md) et recherchez le produit de catalogue approprié à la liste.

1. Lorsque le produit approprié apparaît dans la liste, cliquez sur **[!UICONTROL Assign Catalog Product]** dans le _[!UICONTROL Action]_colonne .

Votre produit et votre liste correspondent désormais. Le canal de vente Amazon peut désormais partager les données de produit et de liste avec Amazon et gérer votre liste et ses informations, notamment le prix de vente, le prix d’expédition, le stock/la quantité, les informations de commande et l’état, etc.

## Créer un produit de catalogue unique à l’aide des informations de liste Amazon

1. Affichez vos listes de produits sur la page [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Recherchez la liste que vous souhaitez créer dans votre [!DNL Commerce] catalogue, cliquez sur **[!UICONTROL Select]** dans le _[!UICONTROL Action]_, puis cliquez sur **[!UICONTROL Create New Catalog Product]**.

   Cette action ouvre la fenêtre _[!UICONTROL Create Magento Catalog Product]_page.

1. Définissez les paramètres du catalogue du produit.

   - Définir **[!UICONTROL Enable Product(s)]** bascule vers `Yes` ou `No` (obligatoire).

      |Oui|Choisissez de rendre le produit éligible pour votre [!DNL Commerce] ventes de storefront.| |Non|Choisissez de rendre le produit inéligible à votre [!DNL Commerce] ventes storefront.|

   - Pour **[!UICONTROL Categories]**, attribuez une catégorie au produit (facultatif).

      Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et cochez une case de catégorie. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

   - Pour **[!UICONTROL Website Ids]**, sélectionnez le site web (storefront) auquel le produit à associer.

      Les options de cette liste dépendent de vos [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;}.

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), choisissez une option.

      `Default` est la sélection par défaut. Les options de cette liste dépendent de vos [!DNL Commerce] [ensembles d’attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

      |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n’est pas inclus dans vos listes storefront, bien qu’il puisse être disponible sous la forme d’une variante d’un autre produit.| |**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.| |**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.| |**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

      Les options qui s’affichent dans cette liste dépendent du [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Create Catalog Products]**.

Le produit catalogue est créé dans votre [!DNL Commerce] catalogue et affecté à la liste Amazon à partir de laquelle il a été créé. La liste étant désormais associée à une liste Amazon existante, elle est supprimée de la variable _[!UICONTROL New Third Party]_et apparaissent dans la_[!UICONTROL Active]_ .

## Créer plusieurs produits de catalogue à l’aide de leurs informations de liste Amazon

1. Affichez vos listes de produits sur la page [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Sélectionnez les listes pour lesquelles créer des produits de catalogue.

   Vous pouvez sélectionner des cases à cocher individuelles dans la colonne de gauche ou cliquer sur la flèche vers le bas dans la colonne de haut à gauche et choisir **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create New Catalog Product(s)]**.

1. Pour accepter le message de confirmation et ouvrir le _[!UICONTROL Create Magento Catalog Product]_page, cliquez sur **[!UICONTROL OK]**.

1. Renseignez les paramètres du catalogue pour les produits.

   >[!NOTE]
   >Lors de la création de produits de catalogue pour plusieurs listes sélectionnées, les paramètres de produit saisis sont appliqués à toutes les listes.

   - Définir **[!UICONTROL Enable Product(s)]** bascule vers `Yes` ou `No` (obligatoire).

      |Oui|Choisissez de rendre le produit éligible pour votre [!DNL Commerce] ventes de storefront.| |Non|Choisissez de rendre le produit inéligible à votre [!DNL Commerce] ventes storefront.|

   - Pour **[!UICONTROL Categories]**, attribuez une catégorie au produit (facultatif).

      Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et cochez une case de catégorie. Cliquez sur **Terminé** lorsque vous avez terminé.

   - Pour **[!UICONTROL Website Ids]**, sélectionnez le site web (storefront) auquel le produit à associer.

      Les options de cette liste dépendent de vos [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;}.

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), choisissez une option.

      `Default` est la sélection par défaut. Les options de cette liste dépendent de vos [!DNL Commerce] [ensembles d’attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

      |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n’est pas inclus dans vos listes storefront, bien qu’il puisse être disponible sous la forme d’une variante d’un autre produit.| |**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.| |**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.| |**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

      Les options qui s’affichent dans cette liste dépendent du [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Create Catalog Products]**.

Les produits du catalogue sont créés dans votre [!DNL Commerce] catalogue et affecté à la liste Amazon à partir de laquelle il a été créé. Maintenant que les listes correspondent à leur liste Amazon respective, elles sont supprimées de la variable [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) et apparaissent dans la [_[!UICONTROL Active]_](./active-listings.md) .

![Créer un produit de catalogue de commerce](assets/amazon-magento-catalog-product.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatoire) Si cette option est activée, le produit est visible dans votre [!DNL Commerce] storefront. Si cette option est désactivée, le produit ne s’affiche pas dans votre [!DNL Commerce] storefront. |
| [!UICONTROL Categories] | Vous pouvez saisir le nom de la catégorie de votre nouveau produit ou sélectionner une catégorie en cliquant sur la flèche vers le bas pour afficher vos options. Les options dépendent de votre [categories](https://docs.magento.com/user-guide/catalog/category-create.html)Configuration de {target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obligatoire) Sélectionnez le site web (storefront) auquel le produit à associer. Les options dépendent de votre [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;} |
| Identifiant du jeu d’attributs | Sélectionnez un jeu d’attributs. Les options dépendent de votre configuration [!DNL Commerce] [ensembles d’attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Visibility] | Options :<ul><li>**[!UICONTROL Not Visible Individually]** - Le produit n’est pas visible dans votre [!DNL Commerce] storefront (le plus courant pour les variantes de produits).</li><li>**[!UICONTROL Catalog]** - Permet d’accéder au produit par le biais de la catégorie à laquelle il est associé dans le site web.</li><li>**Rechercher** - Permet de ne trouver le produit que par le biais de l’outil de recherche.</li><li>**[!UICONTROL Catalog and Search]** - Permet d&#39;accéder aux produits par le biais de la structure de catégories et à l&#39;aide de l&#39;outil de recherche.</li></ul> |
| [!UICONTROL Assign Tax Class] | Attribuez une classe de taxe au nouveau produit. Les options dépendent de votre configuration [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}. |
