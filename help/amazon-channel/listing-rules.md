---
title: Règles d’énumération
description: Les règles d’utilisation des listes déterminent les produits du catalogue de commerce publiés en tant que listes Amazon Marketplace.
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Règles d&#39;énumération

Vous pouvez accéder aux règles de liste pour le magasin dans la variable [tableau de bord de la boutique](./amazon-store-dashboard.md).

Les règles d’énumération définissent les règles à appliquer pour déterminer les produits que le canal de vente Amazon publie sur Amazon. Ces règles offrent de nombreuses options pour créer des règles simples à complexes afin d’inclure ou d’exclure des produits en tant que listes. Chaque règle se compose de conditions qui définissent les exigences d’éligibilité à la liste de produits.

Les règles de liste sont synchronisées en permanence avec vos [!DNL Commerce] catalogue. Lorsque vous ajoutez de nouveaux [!DNL Commerce] produits qui répondent aux critères d’éligibilité définis par vos règles de mise en liste, les produits sont automatiquement traités pour être répertoriés sur Amazon.

- Si vous souhaitez que tous vos produits soient publiés dans une liste Amazon, ne définissez aucune condition pour vos règles de liste.

- Si vous souhaitez limiter les produits de votre catalogue publiés sur Amazon, vous définissez les conditions de votre règle de liste. La définition des conditions de vos règles de liste Amazon suit la même logique et le même processus que la définition des conditions pour [Règles de prix du panier](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

- Si vos règles d’inscription excluent un produit, l’état d’éligibilité de ce produit est défini sur `Ineligible`. Les produits non éligibles ne sont pas publiés sur Amazon.

- Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit de catalogue, la quantité pour laquelle la liste Amazon est modifiée en `0` pour empêcher les ventes du produit. Les listes Amazon peuvent être [supprimé manuellement](./end-listings-manually.md).

Les modifications apportées à la quantité et à l’état d’éligibilité ont un impact sur toutes les listes qui partagent le SKU du vendeur Amazon sur les marchés qui existent pour les magasins qui vendent dans la même région (tel que défini dans _[!UICONTROL Amazon Marketplace Country]_during [intégration de magasin](./store-integration.md)). Cependant, une modification apportée à un partage [!DNL Amazon Seller SKU] dans une région n’affecte pas les listes Amazon du produit dans un autre pays.

![Règles d&#39;énumération](assets/ob-listing-rules.png)

## Configuration des paramètres des règles de liste

1. Cliquez sur **[!UICONTROL Listing Rules]** dans le tableau de bord de la boutique.

1. Définissez les conditions d&#39;éligibilité des produits à lister sur Amazon.

Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md).

| Champ | Description |
|---|---|
| [!UICONTROL Websites] | Les options disponibles dépendent de la variable [sites web](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} que vous avez configuré dans votre [!DNL Commerce] configuration. Sélectionnez le site web correspondant aux produits éligibles répertoriés dans Amazon. Un seul site web peut être sélectionné, car chaque site web nécessite un magasin Amazon unique créé dans le canal de vente Amazon. |
| [!UICONTROL Conditions] | Utilisé pour définir la variable [!DNL Commerce] attributs pour l’éligibilité de produit dans votre région Amazon. Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md). |

## Espace de travail des conditions

Vous pouvez cliquer sur n’importe quelle zone des conditions en gras pour afficher les différentes options.

- N’ajoutez pas de conditions si tous les produits des sites web sélectionnés sont éligibles.
- Il existe un ensemble complexe de processus principaux pour communiquer directement avec les systèmes Amazon. En fonction du nombre d’éléments que vous tentez de répertorier et de l’occupation des systèmes Amazon (Noël, par exemple), la liste de vos éléments dans Amazon peut prendre du temps.

Pour plus d’informations sur les conditions, voir [Description des conditions](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

## Aperçu des règles de liste

Lorsque vous modifiez vos définitions de condition pour vos règles de liste, vous pouvez cliquer sur **[!UICONTROL Preview Changes]** pour appliquer les modifications apportées aux règles et visualiser l’impact sur vos listes. Vérifiez vos listes dans cette fonction d’aperçu de liste avant d’enregistrer les modifications apportées à vos règles de liste.

Vos listes Amazon sont comparées à vos règles et conditions définies. Vous pouvez ensuite consulter :

- Les produits qui passent à un état non éligible en fonction de votre état actuel [!DNL Amazon Seller Central] account
- Les produits qui passent d’un état inéligible à un état éligible
- Quels produits sont de nouvelles listes Amazon et ajoutés à votre liste Amazon à partir de votre [!DNL Commerce] products

L’aperçu de la liste vous permet de prévisualiser vos listes Amazon potentielles et d’apporter les modifications nécessaires à vos règles de liste.

Vos listes Amazon potentielles sont renseignées dans la variable _[!UICONTROL Listing Preview]_dans l’un des trois onglets suivants :

- **[!UICONTROL Ineligible Listings]** - Les produits répertoriés ne sont pas éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles.

   Les produits non éligibles ne sont pas publiés sur Amazon. Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit de catalogue, la quantité pour laquelle la liste Amazon est modifiée en `0` pour empêcher les ventes du produit. Pour supprimer manuellement une liste, reportez-vous à la section [Fin d’une liste Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles selon les exigences d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés dans la [Onglet Listes inactives](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Les produits répertoriés sont éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles et sont également éligibles en fonction des exigences d’Amazon. Cette liste comprend vos listes Amazon existantes qui sont importées (si vous avez **Importer des listes tierces** défini sur `Import Listing` in [Paramètres de liste](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Les produits répertoriés incluent votre [!DNL Commerce] cataloguer les produits qui sont nouvellement éligibles à la liste Amazon en fonction de vos règles et conditions de liste actuelles, et créer et publier de nouvelles listes Amazon.

### Afficher l&#39;aperçu de votre liste

1. Cliquez sur **[!UICONTROL Listing Rules]** dans le tableau de bord de la boutique.

1. Affichez ou ajoutez vos [règles de liste](./listing-rules.md).

1. Modifiez votre [Conditions des règles de liste](./ob-define-condition-example.md).

1. Cliquez sur **[!UICONTROL Preview Changes]**.

1. Vérifiez et confirmez vos listes dans le _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_, et _[!UICONTROL New Listings]_onglets.

1. Si vos listes correspondent à vos attentes, cliquez sur **[!UICONTROL Save and close]**.

   Si vos listes ne s’affichent pas comme prévu, cliquez sur **[!UICONTROL Back]** et modifiez vos règles et conditions jusqu’à ce que vos listes correspondent à vos attentes.

![Aperçu des règles de liste](assets/amazon-listing-rule-preview.png)

### Listage des enregistrements d’aperçu

| Champ | Description |
|--- |--- |
| [!UICONTROL Product ID] | Le numéro séquentiel unique attribué à une [!DNL Commerce] catalogue de produits lorsqu’il est ajouté. |
| [!UICONTROL Thumbnail] | Affiche une miniature de l’image du produit principal. |
| [!UICONTROL Name] | Nom du produit, géré dans la variable [!DNL Commerce] [grille de produits](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Type] | Le type de produit, géré dans la variable [!DNL Commerce] grille de produits. |
| [!UICONTROL Attribute Set] | Nom du jeu d’attributs utilisé comme modèle pour le produit, géré dans la variable [!DNL Commerce] grille de produits. |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit, gérée dans la variable [!DNL Commerce] grille de produits. |
| [!UICONTROL Visibility] | Indique l’emplacement de visibilité du produit, géré dans la variable [!DNL Commerce] grille de produits. Options :<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| État | Indique le statut du produit, géré dans la variable [!DNL Commerce] grille de produits. Options : `Enabled` / `Disabled` |

![Workflow d&#39;aperçu de liste](assets/listing-preview-flowchart.png)
