---
title: Remplacements
description: Amazon Sales Channel fournit l’onglet Remplacements pour vous aider à identifier et à gérer la façon dont vous appliquez des remplacements dans vos annonces Amazon.
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Remplacements

Le _[!UICONTROL Overrides]_affiche vos annonces Amazon auxquelles vous avez appliqué un remplacement. Un remplacement est un paramètre spécifique à la mise en vente qui peut être utilisé pour définir une valeur définie pour une mise en vente. Un remplacement appliqué à une liste définit le paramètre de la liste, indépendamment des autres paramètres ou règles de liste définis pour lesquels la liste est éligible. Lorsqu’un remplacement est appliqué à une liste, la liste apparaît sur la_[!UICONTROL Overrides]_ . La valeur définie dans le remplacement s’affiche dans la colonne appropriée pour la liste. Il existe quatre types de remplacements qui peuvent être appliqués : Prix, Heure de traitement, Condition et Informations sur le vendeur.

## Types de remplacements

| Type | Description |
|---|---|
| Prix | Remplacement qui définit le prix de la mise en vente, en ignorant tous les autres paramètres de prix de la mise en vente. <br><br>**Exemple**: Vous avez défini une règle de prix de remise de 20 % qui s’applique à tous les produits d’une catégorie spécifique de votre catalogue. Vous avez un produit qui est nouveau sur le marché et la demande est élevée, donc vous ne voulez pas que le prix réduit appliqué à l&#39;annonce même si le produit est dans cette catégorie. Vous pouvez sélectionner la liste, [création d’un remplacement de prix](./creating-editing-overrides.md#edit-override-single-listing), et définissez le prix d’annonce dans un remplacement de prix. |
| Temps de traitement | Remplacement qui définit le délai de traitement d&#39;une annonce, en ignorant le délai de traitement par défaut défini dans les paramètres d&#39;annonce.<br><br>**Exemple**: Votre délai de traitement par défaut pour vos annonces est défini sur 2 jours. Vous avez un produit fragile et qui nécessite une journée supplémentaire pour assurer son emballage spécial pour l&#39;expédition. Vous pouvez afficher la liste, [création d’un délai de traitement personnalisé](./creating-editing-overrides.md#edit-override-single-listing)et définir le délai de traitement à trois jours.<br><br>**Remarque :** Non disponible pour les produits définis sur `Fulfilled by Amazon`. |
| Condition | Remplacement qui définit la valeur de condition d’une liste, quel que soit l’attribut de condition affecté à la liste.<br><br>**Exemple**: La plupart des produits de votre catalogue sont de type Nouvelle condition, mais vous disposez d’un produit en état de rénovation. Vous pouvez afficher la liste, [création d’un remplacement de condition](./creating-editing-overrides.md#edit-override-single-listing), et définissez la condition de remise à neuf pour la mise en vente.<br><br>**Remarque :** Non disponible pour les produits définis sur `Fulfilled by Amazon`. |
| Informations sur le vendeur | Un remplacement qui définit la propriété _Informations sur le vendeur_ de la liste. Ce champ peut être utilisé pour ajouter des informations supplémentaires relatives au produit ou au remplacement appliqué, généralement utilisé pour décrire la condition des produits &quot;non nouveaux&quot;. Le texte de ce champ s’affiche avec la liste de l’acheteur. Les notes du vendeur ne peuvent pas être ajoutées pour une annonce dont la valeur de condition est `New`. <br><br>**Exemple**: Vous disposez d’un produit qui est `Refurbished` condition. Normalement, les produits dans cette condition n&#39;incluent pas de manuels ou de documents, mais vous avez un fournisseur différent pour ce produit qui inclut un manuel. Vous pouvez afficher la liste, [créer un remplacement de notes de vendeur](./creating-editing-overrides.md#edit-override-single-listing)et ajoutez votre note de texte propre à cette liste au sujet du manuel pour que le commerçant sache qu&#39;elle est incluse.<br><br>**Note**: Si un produit a une condition définie de `New`, vous pouvez saisir un remplacement de notes de vendeur, mais Amazon n’affiche pas les notes de vendeur pour un `New` produit. |

Vous pouvez créer, modifier ou supprimer un remplacement pour un [liste unique](./creating-editing-overrides.md#edit-override-single-listing). Sur la _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ et _[!UICONTROL Ineligible]_, vous pouvez cliquer sur **[!UICONTROL Select]**dans la_[!UICONTROL Action]_ , puis choisissez **[!UICONTROL Create Override]**. Le _[!UICONTROL Edit Overrides]_n’est disponible que lorsqu’un remplacement a été appliqué à une annonce et est affiché sur le_[!UICONTROL Overrides]_ .

Vous pouvez également créer, modifier ou supprimer un remplacement pour [annonces multiples](./creating-editing-overrides.md#edit-override-multiple-listings). Sur la _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ et _[!UICONTROL Ineligible]_, vous pouvez cliquer sur **[!UICONTROL Select]**dans la_[!UICONTROL Action]_ , puis choisissez **[!UICONTROL Edit Listing Overrides]**.

La suppression d’un remplacement indique à la liste d’utiliser les valeurs définies par vos paramètres et règles d’inscription.

Lors de la définition d’un remplacement, vous pouvez également choisir de saisir un seul type de remplacement ou une combinaison des types.

Voir [Création et modification de remplacements](./creating-editing-overrides.md).

>[!NOTE]
>
>Si vous avez des annonces en cours de traitement, le nombre d’annonces s’affiche dans un message au-dessus des onglets.

![Onglet Remplacements](assets/amazon-overrides.png)

Les pages d&#39;accueil du canal de vente Amazon partagent certaines parties communes [commandes de l’espace de travail](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Amazon Seller SKU] | La référence SKU (Stock Keeping Unit) attribuée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Bloc unique de 10 lettres et/ou chiffres identifiant des éléments.<br><br>ASIN est l&#39;acronyme d&#39;Amazon Standard Identification Numbers. Un ASIN est un bloc unique de 10 lettres et/ou chiffres qui identifie des éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Condition Override] | Nouvelle condition définie dans le remplacement. Si le remplacement appliqué à la liste n’est pas un remplacement de condition, `Not Selected` apparaît dans cette colonne. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Seller Notes Override] | Les nouvelles notes de vendeur définies dans le remplacement. Si le remplacement appliqué à la liste n’est pas de ce type, cette colonne est vide. |
| [!UICONTROL Handling Override] | Le nouveau délai de traitement défini dans le remplacement (en jours). Si le remplacement appliqué à la liste n&#39;est pas un remplacement de délai de traitement, cette colonne est vide. |
| [!UICONTROL List Price Override] | Le nouveau prix d&#39;annonce défini dans le remplacement. Si le remplacement appliqué à la mise en vente n&#39;est pas un remplacement de prix, `N/A` apparaît dans cette colonne. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, dans le noeud _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**et choisissez une option :<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
