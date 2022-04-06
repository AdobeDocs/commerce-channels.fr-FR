---
title: Remplacements
description: Amazon Sales Channel fournit l’onglet Remplacements pour vous aider à identifier et à gérer la manière dont vous appliquez les remplacements dans vos listes Amazon.
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Remplacements

Le _[!UICONTROL Overrides]_affiche vos listes Amazon auxquelles vous avez appliqué un remplacement. Un remplacement est un paramètre spécifique à une liste qui peut être utilisé pour définir une valeur définie sur une liste. Un remplacement appliqué à une liste définit le paramètre de la liste, indépendamment des autres paramètres ou règles de liste définis pour lesquels la liste est éligible. Lorsqu’un remplacement est appliqué à une liste, celle-ci s’affiche sur la liste_[!UICONTROL Overrides]_ . La valeur définie dans le remplacement apparaît dans la colonne appropriée pour la liste. Quatre types de remplacements peuvent être appliqués : Prix, heure de traitement, condition et notes de vente.

## Types de remplacements

| Type | Description |
|---|---|
| Prix | Un remplacement qui définit le prix de la liste, en ignorant tous les autres paramètres de prix de la liste. <br><br>**Exemple**: Vous avez défini une règle de prix de remise de 20 % qui s’applique à tous les produits d’une catégorie spécifique de votre catalogue. Vous avez un produit qui est nouveau sur le marché et la demande est élevée. Vous ne souhaitez donc pas que le prix escompté soit appliqué à la liste même si le produit se trouve dans cette catégorie. Vous pouvez sélectionner la liste, [créer un remplacement de prix ;](./creating-editing-overrides.md#edit-override-single-listing)et définir le prix de l’offre dans un remplacement de prix. |
| Traitement du temps | Remplacement qui définit le délai de gestion d’une liste, en ignorant le délai de gestion par défaut défini dans les paramètres de liste.<br><br>**Exemple**: Le temps de traitement par défaut de vos listes est défini sur 2 jours. Vous avez un produit fragile qui nécessite une journée supplémentaire pour assurer son emballage spécial pour la livraison. Vous pouvez afficher la liste, [création d’un remplacement de durée de gestion](./creating-editing-overrides.md#edit-override-single-listing)et définissez le délai de traitement sur trois jours.<br><br>**Remarque :** Non disponible pour les produits définis sur `Fulfilled by Amazon`. |
| Condition | Remplacement qui définit la valeur de condition d’une liste, quel que soit l’attribut de condition affecté à la liste.<br><br>**Exemple**: La plupart des produits de votre catalogue sont dans la condition Nouvelle, mais vous disposez d’un produit en état Réaménagé . Vous pouvez afficher la liste, [création d’un remplacement de condition](./creating-editing-overrides.md#edit-override-single-listing), puis définissez la condition Mise à jour de la liste.<br><br>**Remarque :** Non disponible pour les produits définis sur `Fulfilled by Amazon`. |
| Notes de vente | Un remplacement qui définit la variable _Notes de vente_ de la liste. Ce champ peut être utilisé pour ajouter des informations supplémentaires relatives au produit ou au remplacement appliqué, généralement utilisé pour décrire la condition des produits &quot;non nouveaux&quot;. Le texte de ce champ s’affiche avec la liste de l’acheteur. Les notes du vendeur ne peuvent pas être ajoutées pour une liste dont la valeur de condition est `New`. <br><br>**Exemple**: Vous disposez d’un produit qui se trouve dans `Refurbished` condition. Normalement, les produits dans cette condition n’incluent pas de manuels ou de documents, mais vous avez un autre fournisseur pour ce produit qui inclut un manuel. Vous pouvez afficher la liste, [créer un remplacement de notes de vendeur ;](./creating-editing-overrides.md#edit-override-single-listing), et ajoutez votre note texte propre à cette liste au sujet du manuel afin que l’acheteur sache qu’il est inclus.<br><br>**Remarque**: Si un produit a une condition définie de `New`, vous pouvez saisir un remplacement de notes de vendeur, mais Amazon n’affiche pas de notes de vendeur pour un événement `New` produit. |

Vous pouvez créer, modifier ou supprimer un remplacement pour une [liste unique](./creating-editing-overrides.md#edit-override-single-listing). Sur le _[!UICONTROL Inactive]_,_[!UICONTROL Active]_, et _[!UICONTROL Ineligible]_onglets, vous pouvez cliquer sur **[!UICONTROL Select]**dans le_[!UICONTROL Action]_ et choisissez **[!UICONTROL Create Override]**. Le _[!UICONTROL Edit Overrides]_Cette action n’est disponible que lorsqu’une liste est remplacée et qu’elle est affichée sur la variable_[!UICONTROL Overrides]_ .

Vous pouvez également créer, modifier ou supprimer un remplacement pour [listes multiples](./creating-editing-overrides.md#edit-override-multiple-listings). Sur le _[!UICONTROL Inactive]_,_[!UICONTROL Active]_, et _[!UICONTROL Ineligible]_onglets, vous pouvez cliquer sur **[!UICONTROL Select]**dans le_[!UICONTROL Action]_ et choisissez **[!UICONTROL Edit Listing Overrides]**.

La suppression d’un remplacement demande à la liste d’utiliser les valeurs définies par vos paramètres et règles de liste.

Lors de la définition d’un remplacement, vous pouvez également choisir de saisir un seul type de remplacement ou toute combinaison de types.

Voir [Créer et modifier des remplacements](./creating-editing-overrides.md).

>[!NOTE]
>
>Si des listes sont en cours de traitement, le nombre de listes est affiché dans un message au-dessus des onglets.

![Onglet Remplacements](assets/amazon-overrides.png)

Les pages d’accueil du canal de vente Amazon partagent certaines [contrôles workspace](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Amazon Seller SKU] | SKU (unité de gestion des stocks) affectée par Amazon à un produit pour identifier le produit, les options, le prix et le fabricant. |
| [!UICONTROL ASIN] | Un bloc unique de 10 lettres et/ou chiffres qui identifient les éléments.<br><br>ASIN est l’acronyme des numéros d’identification standard d’Amazon. Un ASIN est un bloc unique de 10 lettres et/ou nombres qui identifie les éléments. Pour les livres, l&#39;ASIN est le même que le numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l&#39;article est téléchargé dans son catalogue. Vous trouverez un ASIN d’articles sur la page des détails du produit dans Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL Condition Override] | Nouvelle condition définie dans le remplacement. Si le remplacement appliqué à la liste n’est pas un remplacement de condition, `Not Selected` apparaît dans cette colonne. |
| [!UICONTROL Product Listing Name] | Nom du produit. |
| [!UICONTROL Seller Notes Override] | Les nouvelles notes du vendeur définies dans le remplacement. Si le remplacement appliqué à la liste n’est pas ce type de remplacement, cette colonne est vide. |
| [!UICONTROL Handling Override] | Le nouveau délai de traitement défini dans le remplacement (en jours). Si le remplacement appliqué à la liste n’est pas un remplacement de temps de traitement, cette colonne est vide. |
| [!UICONTROL List Price Override] | Le nouveau prix de la liste défini dans le remplacement. Si le remplacement appliqué à la liste n’est pas un remplacement de prix, `N/A` apparaît dans cette colonne. |
| [!UICONTROL Action] | Liste des actions disponibles pouvant être appliquées à une liste spécifique. Pour appliquer une action, dans la variable _[!UICONTROL Action]_colonne, cliquez sur **[!UICONTROL Select]**et choisissez une option :<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
