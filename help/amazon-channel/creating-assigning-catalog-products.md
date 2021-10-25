---
title: Création et attribution de produits
description: Le Sales Channel Amazon fournit la [!UICONTROL New Third Party] pour aider à créer et à affecter des produits de catalogue Commerce correspondants à des annonces Amazon.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Création et attribution de produits

Lors de l’affichage _[!UICONTROL New Third Party]_, vous pouvez [!DNL Commerce] catalogue des produits vers une liste Amazon existante. Il existe deux options pour cette correspondance. Vous pouvez affecter une annonce à un produit de catalogue existant, ou vous pouvez utiliser les informations de cette annonce pour créer des produits de catalogue. Ces options sont utiles lorsque vos annonces Amazon ne correspondent pas automatiquement à votre [!DNL Commerce] catalogue.

L’association (ou l’affectation) de vos produits à vos annonces Amazon est nécessaire pour utiliser l’ensemble des fonctionnalités du canal de vente Amazon.

Lorsque vous créez un produit de catalogue à partir d’une liste Amazon :

- Le **ASIN** devient la [!DNL Commerce] SKU
- Le **Nom de la liste de produits** devient le nom de la liste de catalogues
- Le **Prix** et **Quantité** sont importés à partir de la liste Amazon

Les autres paramètres nécessaires sont déterminés par la [!DNL Commerce] paramètres de produit que vous sélectionnez lors de la création.

Une fois créés et mis en correspondance, les annonces sont supprimées de la _[!UICONTROL New Third Party]_et s’affiche sur la_[!UICONTROL Active]_ .

## Attribution d’un produit de catalogue unique à une liste Amazon

1. Afficher vos annonces de produits sur le [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Recherchez la liste que vous souhaitez affecter dans la liste, puis cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_, puis cliquez sur **[!UICONTROL Assign Catalog Product]**.

   Cette action ouvre la boîte de dialogue _[!UICONTROL Assign Magento Catalog Product]_.

1. Recherchez ou filtrez la liste à l’aide de l’option [commandes de l’espace de travail](./workspace-controls.md) et localisez le produit de catalogue approprié pour correspondre à la liste.

1. Lorsque le produit approprié apparaît dans la liste, cliquez sur **[!UICONTROL Assign Catalog Product]** dans la _[!UICONTROL Action]_colonne.

Votre produit et votre annonce sont maintenant mis en correspondance. Le canal de vente Amazon peut désormais partager des données de produits et de listes avec Amazon et gérer votre annonce et ses informations, y compris le prix de vente, le prix d&#39;expédition, la quantité/stock, les informations de commande et le statut, et bien plus encore.

## Création d’un produit de catalogue unique à l’aide des informations de liste Amazon

1. Afficher vos annonces de produits sur le [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Trouvez la liste que vous souhaitez créer dans votre [!DNL Commerce] catalogue, cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_, puis cliquez sur **[!UICONTROL Create New Catalog Product]**.

   Cette action ouvre la boîte de dialogue _[!UICONTROL Create Magento Catalog Product]_.

1. Complétez les paramètres de catalogue du produit.

   - Définir **[!UICONTROL Enable Product(s)]** activer/désactiver `Yes` ou `No` (requis).

      |Oui|Choisissez de rendre le produit éligible pour votre [!DNL Commerce] ventes au magasin.| |Non|Choisissez de rendre le produit non éligible pour votre [!DNL Commerce] ventes de vitrine.|

   - Pour **[!UICONTROL Categories]**, attribuez une catégorie au produit (facultatif).

      Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et sélectionnez une case à cocher de catégorie. Cliquez sur **[!UICONTROL Done]** une fois terminé.

   - Pour **[!UICONTROL Website Ids]**, sélectionnez le site web (storefront) pour lequel le produit à associer.

      Les options de cette liste dépendent de votre [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;}.

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), sélectionnez une option.

      `Default` est la sélection par défaut. Les options de cette liste dépendent de votre [!DNL Commerce] [ensembles d&#39;attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

      |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n&#39;est pas inclus dans vos annonces de vitrine, bien qu&#39;il puisse être disponible en tant que variante d&#39;un autre produit.| |**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.| |**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.| |**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

      Les options qui s’affichent dans cette liste dépendent de la [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Lorsque vous avez terminé, cliquez sur **[!UICONTROL Create Catalog Products]**.

Le produit du catalogue est créé dans votre [!DNL Commerce] et affecté à la liste Amazon à partir de laquelle il a été créé. La mise en vente étant maintenant mise en correspondance avec une mise en vente Amazon existante, la mise en vente est supprimée de la liste _[!UICONTROL New Third Party]_et s’affiche dans la_[!UICONTROL Active]_ .

## Création de plusieurs produits de catalogue à l’aide de leurs informations de liste Amazon

1. Afficher vos annonces de produits sur le [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) .

1. Sélectionnez les annonces pour lesquelles créer des produits de catalogue.

   Vous pouvez sélectionner des cases à cocher individuelles dans la colonne de gauche ou cliquer sur la flèche vers le bas dans la colonne de haut à gauche et choisir **[!UICONTROL Select All]** ou **[!UICONTROL Select All on this Page]**.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Create New Catalog Product(s)]**.

1. Pour accepter le message de confirmation et ouvrir le _[!UICONTROL Create Magento Catalog Product]_, cliquez sur **[!UICONTROL OK]**.

1. Complétez les paramètres de catalogue pour les produits.

   >[!NOTE]
   >Lors de la création de produits de catalogue pour plusieurs annonces sélectionnées, les paramètres de produit saisis sont appliqués à toutes les annonces.

   - Définir **[!UICONTROL Enable Product(s)]** activer/désactiver `Yes` ou `No` (requis).

      |Oui|Choisissez de rendre le produit éligible pour votre [!DNL Commerce] ventes au magasin.| |Non|Choisissez de rendre le produit non éligible pour votre [!DNL Commerce] ventes de vitrine.|

   - Pour **[!UICONTROL Categories]**, attribuez une catégorie au produit (facultatif).

      Pour sélectionner la catégorie du produit, cliquez sur la flèche vers le bas et sélectionnez une case à cocher de catégorie. Cliquez sur **Terminé** une fois terminé.

   - Pour **[!UICONTROL Website Ids]**, sélectionnez le site web (storefront) pour lequel le produit à associer.

      Les options de cette liste dépendent de votre [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;}.

   - Pour **[!UICONTROL Attribute Set Id]** (obligatoire), sélectionnez une option.

      `Default` est la sélection par défaut. Les options de cette liste dépendent de votre [!DNL Commerce] [ensembles d&#39;attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Pour **[!UICONTROL Visibility]**, choisissez une option pour le nouveau produit.

      |**[!UICONTROL Not Visible Individually]** (par défaut)|Le produit n&#39;est pas inclus dans vos annonces de vitrine, bien qu&#39;il puisse être disponible en tant que variante d&#39;un autre produit.| |**[!UICONTROL Catalog]**|Le produit apparaît dans vos listes de catalogues.| |**[!UICONTROL Search]**|Le produit est disponible pour les opérations de recherche.| |**[!UICONTROL Catalog and Search]**|Le produit est inclus dans les listes de catalogues et disponible pour les opérations de recherche.|

   - Pour **[!UICONTROL Assign Tax Class]**, choisissez une option pour le produit.

      Les options qui s’affichent dans cette liste dépendent de la [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} que vous avez configuré.

   - Lorsque vous avez terminé, cliquez sur **[!UICONTROL Create Catalog Products]**.

Les produits du catalogue sont créés dans votre [!DNL Commerce] et affecté à la liste Amazon à partir de laquelle il a été créé. Les annonces étant désormais associées à leur liste Amazon respective, les annonces sont supprimées de la liste [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) et s’affiche dans la [_[!UICONTROL Active]_](./active-listings.md) .

![Créer un produit de catalogue Commerce](assets/amazon-magento-catalog-product.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatoire) Si cette option est activée, le produit est visible dans votre [!DNL Commerce] vitrine. Si cette option est désactivée, le produit ne s’affiche pas dans votre [!DNL Commerce] vitrine. |
| [!UICONTROL Categories] | Vous pouvez entrer le nom de la catégorie de votre nouveau produit ou sélectionner une catégorie en cliquant sur la flèche vers le bas pour afficher vos options. Les options dépendent de votre [catégories](https://docs.magento.com/user-guide/catalog/category-create.html)Configuration de {target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obligatoire) Sélectionnez le site Web (storefront) pour lequel le produit à associer. Les options dépendent de votre [!DNL Commerce] [configuration du magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html)Paramètres {target=&quot;_blank&quot;} |
| ID jeu d’attributs | Sélectionnez un jeu d’attributs. Les options dépendent de votre configuration [!DNL Commerce] [ensembles d&#39;attributs](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Visibility] | Options :<ul><li>**[!UICONTROL Not Visible Individually]** - Le produit n’est pas visible dans votre [!DNL Commerce] storefront (le plus courant pour les variantes de produits).</li><li>**[!UICONTROL Catalog]** - Permet d’accéder au produit via la catégorie à laquelle il est associé sur le site web.</li><li>**Rechercher** - Permet de ne trouver le produit qu’à l’aide de l’outil de recherche.</li><li>**[!UICONTROL Catalog and Search]** - Permet d’accéder aux produits via la structure de catégories et à l’aide de l’outil de recherche.</li></ul> |
| [!UICONTROL Assign Tax Class] | Attribuez une classe de taxe au nouveau produit. Les options dépendent de votre configuration [classes fiscales](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}. |
