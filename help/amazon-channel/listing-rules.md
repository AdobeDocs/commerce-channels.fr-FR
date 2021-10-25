---
title: Règles d'annonce
description: Les règles d’utilisation déterminent les produits du catalogue Commerce qui sont publiés en tant que listes Amazon Marketplace.
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Règles d&#39;annonce

Vous pouvez accéder aux règles de mise en vente pour le magasin dans le dossier [tableau de bord de magasin](./amazon-store-dashboard.md).

Les règles d&#39;énumération définissent les règles permettant de déterminer quels produits Amazon Sales Channel publie sur Amazon. Ces règles offrent de nombreuses options pour créer des règles simples ou complexes pour inclure ou exclure des produits en tant qu’annonces. Chaque règle comprend des conditions qui définissent les conditions d’éligibilité à la liste de produits.

Vos règles de mise en vente sont continuellement synchronisées avec votre [!DNL Commerce] catalogue. Lorsque vous ajoutez un nouveau [!DNL Commerce] les produits qui répondent aux critères d’éligibilité définis par vos règles d’inscription sont automatiquement traités pour être inclus dans l’inscription sur Amazon.

- Si vous souhaitez que tous vos produits soient publiés dans une annonce Amazon, ne définissez aucune condition pour vos règles de mise en vente.

- Si vous souhaitez limiter les produits de votre catalogue qui sont publiés sur Amazon, vous devez définir les conditions de votre règle d’annonce. La définition des conditions pour vos règles d&#39;inscription Amazon suit la même logique et le même processus que la définition des conditions pour [Règles de prix du panier](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

- Si vos règles de mise en vente excluent un produit, le statut d’éligibilité de ce produit devient `Ineligible`. Les produits non éligibles ne sont pas publiés à Amazon.

- Si un produit non éligible est déjà répertorié sur Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit catalogue, la quantité pour la liste Amazon change en `0` pour empêcher la vente du produit. Les annonces Amazon peuvent être [supprimé manuellement](./end-listings-manually.md).

Les modifications apportées à la quantité et au statut d’éligibilité ont une incidence sur toutes les annonces qui partagent la référence SKU du vendeur Amazon sur les marchés qui existent pour les magasins qui vendent dans la même région (telle que définie dans _[!UICONTROL Amazon Marketplace Country]_pendant [intégration de magasin](./store-integration.md)). Cependant, une modification d’un partage [!DNL Amazon Seller SKU] dans une région n&#39;affecte pas les annonces Amazon du produit dans un autre pays.

![Règles d&#39;annonce](assets/ob-listing-rules.png)

## Configuration des paramètres de règles de liste

1. Cliquez sur **[!UICONTROL Listing Rules]** sur le tableau de bord de la boutique.

1. Définissez les conditions d’éligibilité des produits à inscrire sur Amazon.

Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md).

| Champ | Description |
|---|---|
| [!UICONTROL Websites] | Les options disponibles dépendent de la [sites web](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} que vous avez configuré dans votre [!DNL Commerce] configuration. Sélectionnez le site web pour les produits éligibles répertoriés sur Amazon. Un seul site web peut être sélectionné, car chaque site nécessite un magasin Amazon unique créé dans le canal de vente Amazon. |
| [!UICONTROL Conditions] | Utilisé pour définir la propriété [!DNL Commerce] pour l’éligibilité des produits dans votre région Amazon. Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md). |

## Espace de travail Conditions

Vous pouvez cliquer sur n’importe quelle zone en gras pour afficher les différentes options.

- Ne pas ajouter de conditions si tous les produits des sites web sélectionnés sont éligibles.
- Il existe un ensemble complexe de processus back-end pour communiquer directement avec les systèmes Amazon. En fonction du nombre d’éléments que vous tentez d’énumérer et de l’afflux des systèmes d’Amazon (tel que Black Friday), il peut s’avérer nécessaire de temps pour que vos éléments soient répertoriés sur Amazon.

Pour plus d’informations sur les conditions, voir [Décrire les conditions](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}.

## Aperçu des règles de liste

Lorsque vous modifiez vos définitions de condition pour vos règles de mise en vente, vous pouvez cliquer sur **[!UICONTROL Preview Changes]** pour appliquer vos modifications de règles et voir comment vos annonces sont affectées. Vérifiez vos annonces dans cette fonction d&#39;aperçu avant d&#39;enregistrer vos modifications de règle d&#39;annonce.

Vos annonces Amazon sont comparées à vos règles et conditions définies. Vous pouvez ensuite passer en revue :

- Quels produits passent à un statut non éligible en fonction de votre [!DNL Amazon Seller Central] compte
- Quels produits passent d’un état non éligible à un statut éligible ?
- Quels produits sont des annonces New Amazon et ajoutés à votre annonce Amazon à partir de votre liste éligible ? [!DNL Commerce] produits

L’aperçu des annonces vous permet de prévisualiser vos annonces Amazon potentielles et d’apporter les modifications nécessaires à vos règles d’annonce.

Vos annonces Amazon potentielles sont renseignées sur le _[!UICONTROL Listing Preview]_dans l’un des trois onglets suivants :

- **[!UICONTROL Ineligible Listings]** - Les produits répertoriés ne sont pas éligibles à l&#39;inscription Amazon en fonction de vos règles et conditions d&#39;inscription actuelles.

   Les produits non éligibles ne sont pas publiés à Amazon. Si un produit non éligible est déjà répertorié sur Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit catalogue, la quantité pour la liste Amazon change en `0` pour empêcher la vente du produit. Pour supprimer manuellement une annonce, voir [Fin d&#39;une liste Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles aux conditions d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés sur la [Onglet Annonces inactives](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - Les produits listés sont admissibles à l&#39;inscription sur Amazon en fonction de vos règles et conditions d&#39;inscription actuelles et sont également admissibles aux exigences du Amazon. Cette liste inclut vos listes Amazon existantes qui sont importées (si vous avez **Importer des annonces tierces** défini sur `Import Listing` dans [Paramètres de liste](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Les produits répertoriés incluent votre [!DNL Commerce] les produits de catalogue qui sont nouvellement éligibles à l’inscription Amazon en fonction de vos règles et conditions d’inscription actuelles, ainsi que la création et la publication de nouvelles annonces Amazon.

### Afficher l&#39;aperçu de votre annonce

1. Cliquez sur **[!UICONTROL Listing Rules]** sur le tableau de bord de la boutique.

1. Afficher ou ajouter votre [règles d&#39;inscription](./listing-rules.md).

1. Modifier votre [Conditions des règles d&#39;annonce](./ob-define-condition-example.md).

1. Cliquez sur **[!UICONTROL Preview Changes]**.

1. Vérifiez et confirmez vos annonces dans le fichier _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ et _[!UICONTROL New Listings]_onglets.

1. Si vos annonces correspondent à vos attentes, cliquez sur **[!UICONTROL Save and close]**.

   Si vos annonces n’apparaissent pas comme prévu, cliquez sur **[!UICONTROL Back]** et modifiez vos règles et conditions jusqu’à ce que vos annonces correspondent à vos attentes.

![Aperçu des règles de liste](assets/amazon-listing-rule-preview.png)

### Liste des enregistrements d’aperçu

| Champ | Description |
|--- |--- |
| [!UICONTROL Product ID] | Numéro séquentiel unique attribué à un [!DNL Commerce] produit catalogue lorsqu’il est ajouté. |
| [!UICONTROL Thumbnail] | Affiche une vignette de l’image principale du produit. |
| [!UICONTROL Name] | Le nom du produit, géré dans le dossier [!DNL Commerce] [grille de produits](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Type] | Le type de produit, géré dans le dossier [!DNL Commerce] grille de produits. |
| [!UICONTROL Attribute Set] | Le nom du jeu d’attributs utilisé comme modèle pour le produit, géré dans le noeud [!DNL Commerce] grille de produits. |
| [!UICONTROL SKU] | Unité de conservation d’images unique affectée au produit, gérée dans le dossier [!DNL Commerce] grille de produits. |
| [!UICONTROL Visibility] | Indique où le produit est visible, géré dans le dossier [!DNL Commerce] grille de produits. Options :<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Statut | Indique l’état du produit, géré dans le dossier [!DNL Commerce] grille de produits. Options : `Enabled` / `Disabled` |

![Workflow d’aperçu de la liste](assets/listing-preview-flowchart.png)
