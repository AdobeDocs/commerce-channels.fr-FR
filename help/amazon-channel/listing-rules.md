---
title: Canal de vente Amazon - [!UICONTROL Listing Rules]
description: Les règles d’utilisation des listes déterminent les produits du catalogue Commerce publiés en tant que listes Amazon Marketplace.
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

Vous pouvez accéder aux règles de liste pour le magasin dans le [tableau de bord du magasin](./amazon-store-dashboard.md).

Les règles d’énumération définissent les règles à appliquer pour déterminer les produits que le canal de vente Amazon publie sur Amazon. Ces règles offrent de nombreuses options pour créer des règles simples à complexes afin d’inclure ou d’exclure des produits en tant que listes. Chaque règle se compose de conditions qui définissent les exigences d’éligibilité à la liste de produits.

Les règles de liste sont continuellement synchronisées avec votre catalogue [!DNL Commerce]. Lorsque vous ajoutez de nouveaux produits [!DNL Commerce] qui répondent aux exigences d’éligibilité définies par vos règles de mise en liste, les produits sont automatiquement traités pour être répertoriés sur Amazon.

- Si vous souhaitez que tous vos produits soient publiés dans une liste Amazon, ne définissez aucune condition pour vos règles de liste.

- Si vous souhaitez limiter les produits de votre catalogue publiés sur Amazon, vous définissez les conditions de votre règle de liste. La définition des conditions de vos règles de liste Amazon suit la même logique et le même processus que la définition des conditions des [règles de prix du panier](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- Si vos règles de liste excluent un produit, l’état d’éligibilité de ce produit passe à `Ineligible`. Les produits non éligibles ne sont pas publiés sur Amazon.

- Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre produit de catalogue [!DNL Commerce], la quantité de la liste Amazon passe à `0` pour empêcher les ventes du produit. Les listes Amazon peuvent être [supprimées manuellement](./end-listings-manually.md).

Les modifications apportées à la quantité et à l’état d’éligibilité ont un impact sur toutes les listes qui partagent le SKU du vendeur Amazon sur les marchés qui existent pour les magasins qui vendent dans la même région (comme défini dans _[!UICONTROL Amazon Marketplace Country]_lors de l’ [intégration de magasin](./store-integration.md)). Cependant, une modification apportée à un [!DNL Amazon Seller SKU] partagé dans une région n’a aucune incidence sur les listes Amazon du produit dans un autre pays.

![Règles de liste](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## Configuration des paramètres des règles de liste

1. Cliquez sur **[!UICONTROL Listing Rules]** dans le tableau de bord du magasin.

1. Définissez les conditions d&#39;éligibilité des produits à lister sur Amazon.

Voir [Exemple : définition d’une condition](./ob-define-condition-example.md).

| Champ | Description |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | Les options disponibles dépendent des [sites web](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) que vous avez configurés dans votre configuration [!DNL Commerce]. Sélectionnez le site web correspondant aux produits éligibles répertoriés dans Amazon. Un seul site web peut être sélectionné, car chaque site web nécessite un magasin Amazon unique créé dans le canal de vente Amazon. |
| [!UICONTROL Conditions] | Utilisé pour définir les attributs [!DNL Commerce] pour l’éligibilité de produit dans votre région Amazon. Voir [Exemple : définition d’une condition](./ob-define-condition-example.md). |

## Espace de travail des conditions

Vous pouvez cliquer sur n’importe quelle zone des conditions en gras pour afficher les différentes options.

- N’ajoutez pas de conditions si tous les produits des sites web sélectionnés sont éligibles.
- Il existe un ensemble complexe de processus principaux pour communiquer directement avec les systèmes Amazon. En fonction du nombre d’éléments que vous tentez de répertorier et de l’occupation des systèmes Amazon (Noël, par exemple), la liste de vos éléments dans Amazon peut prendre du temps.

Pour plus d’informations sur les conditions, voir [Description des conditions](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## Aperçu des règles de liste

Lorsque vous modifiez les définitions de conditions pour vos règles de liste, vous pouvez cliquer sur **[!UICONTROL Preview Changes]** pour appliquer les modifications de vos règles et afficher l’impact de vos listes. Vérifiez vos listes dans cette fonction d’aperçu de liste avant d’enregistrer les modifications apportées à vos règles de liste.

Vos listes Amazon sont comparées à vos règles et conditions définies. Vous pouvez ensuite consulter :

- Les produits qui passent à un état non éligible en fonction de votre compte [!DNL Amazon Seller Central] actuel
- Les produits qui passent d’un état inéligible à un état éligible
- Quels produits sont de nouvelles listes Amazon et ajoutés à votre liste Amazon à partir de vos produits [!DNL Commerce] éligibles ?

L’aperçu de la liste vous permet de prévisualiser vos listes Amazon potentielles et d’apporter les modifications nécessaires à vos règles de liste.

Vos listes Amazon potentielles sont renseignées sur la page _[!UICONTROL Listing Preview]_dans l’un des trois onglets suivants :

- **[!UICONTROL Ineligible Listings]** - Les produits répertoriés ne sont pas éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles.

  Les produits non éligibles ne sont pas publiés sur Amazon. Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre produit de catalogue [!DNL Commerce], la quantité de la liste Amazon passe à `0` pour empêcher les ventes du produit. Pour supprimer manuellement une liste, reportez-vous à la section [Fin de la liste Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles selon les exigences d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés dans l’onglet [Listes inactives](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Les produits répertoriés sont éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles et sont également éligibles en fonction des exigences d’Amazon. Cette liste inclut vos listes Amazon existantes qui sont importées (si **Importer des listes tierces** est défini sur `Import Listing` dans [Paramètres de liste](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Les produits répertoriés incluent vos [!DNL Commerce] produits de catalogue qui sont nouvellement éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles, ainsi que pour créer et publier de nouvelles listes Amazon.

### Afficher l&#39;aperçu de votre liste

1. Cliquez sur **[!UICONTROL Listing Rules]** dans le tableau de bord du magasin.

1. Affichez ou ajoutez vos [règles de liste](./listing-rules.md).

1. Modifiez les [conditions des règles de liste](./ob-define-condition-example.md).

1. Cliquez sur **[!UICONTROL Preview Changes]**.

1. Vérifiez et confirmez vos listes dans les onglets _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ et _[!UICONTROL New Listings]_.

1. Si vos listes correspondent à vos attentes, cliquez sur **[!UICONTROL Save and close]**.

   Si vos listes ne s&#39;affichent pas comme prévu, cliquez sur **[!UICONTROL Back]** et modifiez vos règles et conditions jusqu&#39;à ce que vos listes correspondent à vos attentes.

![Aperçu des règles de liste](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### Listage des enregistrements d’aperçu

| Champ | Description |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | Numéro séquentiel unique attribué à un produit de catalogue [!DNL Commerce] lors de son ajout. |
| [!UICONTROL Thumbnail] | Affiche une miniature de l’image du produit principal. |
| [!UICONTROL Name] | Le nom du produit, géré dans la [!DNL Commerce] [grille de produits](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | Le type de produit, géré dans la grille de produits [!DNL Commerce]. |
| [!UICONTROL Attribute Set] | Nom de l’ensemble d’attributs utilisé comme modèle pour le produit, géré dans la grille de produits [!DNL Commerce]. |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit, gérée dans la grille de produits [!DNL Commerce]. |
| [!UICONTROL Visibility] | Indique l’endroit où le produit est visible, géré dans la grille de produits [!DNL Commerce]. Options :<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| État | Indique l’état du produit, géré dans la grille de produits [!DNL Commerce]. Options : `Enabled` / `Disabled` |

![Workflow d&#39;aperçu de liste](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
