---
title: "Exemple : définir une condition pour les règles de liste Amazon"
description: Lors de la création de vos règles de liste, définissez les conditions d’identification des produits du catalogue Commerce à répertorier sur Amazon Marketplace.
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Exemple : définir une condition

## Conditions

Vous pouvez cliquer sur n’importe quelle zone des conditions en gras pour afficher les différentes options.

**N&#39;ajoutez pas de conditions si tous les produits du site web sélectionné sont éligibles.**

>[!NOTE]
>
>Il existe un ensemble complexe de processus principaux pour communiquer directement avec les systèmes Amazon. En fonction du nombre d’éléments que vous tentez de répertorier et de l’occupation des systèmes Amazon (Noël, par exemple), la liste de vos éléments dans Amazon peut prendre du temps.

Voir la section Conditions de la [création d’une règle de prix de panier](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## Définition d’une condition

Ce processus peut être simple ou détaillé, en fonction de la configuration de votre catalogue. Vous pouvez configurer vos conditions de sorte que lorsque `ALL` ou `ANY` des conditions définies sont `TRUE` ou `FALSE` pour un produit, le produit puisse être répertorié dans Amazon.

Les conditions sont basées sur des valeurs d’attribut de produit existantes. Pour appliquer la règle à tous les produits, laissez la section conditions vide.

>[!NOTE]
>
>Si vous souhaitez définir une condition basée sur un attribut de produit spécifique, définissez le paramètre **[!UICONTROL Use for Promo Rule Conditions]** pour l’attribut sur `Yes`. Vous pouvez accéder à ce paramètre sur la page [Propriétés Storefront](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) pour l’attribut .

![Condition - ligne 1](assets/ob-listing-rule-conditions-start.png){width="500"}

La règle de cet exemple définit une règle qui définit l’éligibilité Amazon pour tous les produits de catalogue dont l’attribut _Amazon FBA_ est défini sur `Yes`.

L’instruction de règle comporte deux liens en gras qui, lorsque vous cliquez dessus, affichent les options correspondant à cette partie de l’instruction. Si vous enregistrez la condition sans modifier une option en gras, la règle s’applique à tous vos produits.

- Cliquez sur **[!UICONTROL ALL]** et choisissez `ALL` ou `ANY`.
- Cliquez sur **[!UICONTROL TRUE]** et choisissez `TRUE` ou `FALSE`.
- Pour appliquer la règle à tous les produits, laissez la condition inchangée.

Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Dans cet exemple, la condition suivante est utilisée :

`If ALL of these conditions are TRUE:`

1. Cliquez sur l’icône Ajouter (![Icône Ajouter](assets/btn-add-grn.png)) au début de la ligne de condition et sélectionnez un attribut sur lequel baser la condition, tel qu’une combinaison de conditions ou un attribut de produit.

   - **[!UICONTROL Conditions Combination]** - Choisissez de vous permettre de créer un autre ensemble de conditions `All/Any` et `True/False` à l’intérieur de l’ensemble existant.

     ![Combinaison de conditions](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]** - Les attributs de produit dépendent de la configuration de l’attribut . Pour qu’un attribut apparaisse dans la liste, il doit être configuré pour être utilisé dans les conditions des règles promotionnelles. Reportez-vous à la section _Utilisation pour les conditions de règle promotionnelle_ dans [Attributs de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     Dans la liste sous **[!UICONTROL Product Attribute]**, sélectionnez l’attribut que vous souhaitez utiliser comme base de la condition. Pour cet exemple, la condition sélectionnée est `Amazon FBA`.

     ![Condition line 2, partie 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     La condition sélectionnée s’affiche dans l’instruction, suivie de deux autres liens en gras. Les options diffèrent selon l’attribut de produit que vous sélectionnez.

     Une fois l’attribut défini, il ne peut pas être modifié. Pour modifier l’attribut, vous devez supprimer la ligne et ajouter le nouvel attribut. Vous pouvez supprimer une ligne de condition en cliquant sur l’icône Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.

      1. Cliquez sur **[!UICONTROL is]** et sélectionnez l’opérateur de comparaison qui décrit la condition à remplir pour les produits.

         Pour cet exemple, l’opérateur de comparaison est `is`. Les options disponibles dépendent de l’attribut sélectionné à l’étape précédente. Les options peuvent inclure différentes options de comparaison, telles que des valeurs correspondantes, sans inclure ou inclure au moins une valeur et un montant supérieur, égal ou inférieur à un montant numérique. Dans cet exemple, les options sont `is` et `is not`.

      1. Cliquez sur **[!UICONTROL ...]** et sélectionnez la valeur d’attribut sur laquelle repose la condition.

         Les options dépendent de la configuration de l’attribut. Vous pouvez être invité à sélectionner une option ou à saisir du texte ou des valeurs numériques pour la condition. Pour cet exemple, la sélection est `Yes`.

         L’élément sélectionné apparaît dans l’instruction pour remplir la condition.

         ![Condition line 2, partie 3](assets/ob-listing-rule-condition-is.png){width="500"}

   Cette condition est terminée. Comme indiqué, cette condition signifie que tout produit de votre catalogue [!DNL Commerce] dont l’attribut Amazon FBA est défini sur une valeur `Yes` peut être répertorié dans Amazon pour la région et le magasin. Vous pouvez ajouter d’autres lignes de condition pour affiner davantage vos produits éligibles.

1, pour ajouter une autre ligne de condition à l’instruction, revenez à l’étape 1 et répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

Vous pouvez supprimer une ligne de l’instruction de condition à tout moment en cliquant sur l’icône Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.
