---
title: Canal vente Amazon - Conditions des règles de prix
description: Utilisez les conditions de la règle de prix pour déterminer les produits éligibles à la règle de prix de la liste.
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Conditions des règles de prix

Les conditions déterminent quels produits sont éligibles à la règle de prix. La définition des conditions de vos règles de tarification Amazon suit la même logique et le même processus que la définition des conditions des [ Règles de prix du panier](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) dans [!DNL Commerce].

>[!IMPORTANT]
>
>Si votre règle de prix s’applique à tous les produits de votre catalogue [!DNL Commerce], laissez cette section vide.

Vous pouvez cliquer sur n’importe quelle zone des conditions en gras pour afficher les différentes options.

## Exemple : créer une condition de règle de prix

Ce processus peut être simple ou détaillé, en fonction de la configuration de votre catalogue. Vous pouvez définir vos conditions de sorte que lorsque `ALL` ou `ANY` des conditions sont `TRUE` ou `FALSE` pour un produit, le produit soit éligible à la règle de prix à appliquer.

Les conditions sont basées sur vos [attributs de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Pour appliquer la règle à tous les produits, laissez la section conditions vide.

>[!NOTE]
>
>Si vous souhaitez définir une condition basée sur un attribut de produit spécifique, **Utiliser pour les conditions de règle promotionnelle** pour l’attribut doit être défini sur `Yes` dans vos [Propriétés Storefront](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) pour l’attribut.

![Condition de règle de prix - ligne 1](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

Cet exemple définit une règle qui applique une remise de 25 % à tous les produits définis dans la catégorie `Books`.

L’instruction de règle comporte deux liens en gras qui, lorsque vous cliquez dessus, affichent les options de cette partie de l’instruction de condition. Si vous enregistrez la condition sans modifier une option en gras, la règle s’applique à tous vos produits.

- Cliquez sur **[!UICONTROL ALL]** et choisissez `ALL` ou `ANY`.
- Cliquez sur **[!UICONTROL TRUE]** et choisissez `TRUE` ou `FALSE`.
- Pour appliquer la règle à tous les produits, laissez la condition inchangée.

Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Dans cet exemple, la condition suivante est utilisée :

`If ALL of these conditions are TRUE:`

1. Pour afficher les attributs disponibles pour lesquels la condition s’applique, cliquez sur l’icône Ajouter (![Icône Ajouter](assets/btn-add-grn.png)) au début de la ligne de condition et sélectionnez un attribut sur lequel baser la condition.

   **[!UICONTROL Conditions Combination]** - Choisissez de créer un autre ensemble de conditions `All/Any` et `True/False` dans la condition existante.

   ![Combinaison des conditions de règle de prix](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]** - Les attributs de produit disponibles dépendent de la [configuration de l’attribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html). Pour qu’un attribut s’affiche dans la liste, *[!UICONTROL Use for Promo Rule Conditions]* pour l’attribut doit être défini sur `Yes` dans vos propriétés storefront.

   - Pour **[!UICONTROL Product Attribute]**, choisissez l’attribut que vous souhaitez définir comme base de la condition. Pour cet exemple, la condition sélectionnée est `Category`.

     ![Condition de règle de prix - ligne 2, partie 2](assets/ob-price-rule-condition-2.png){width="500"}

     La condition sélectionnée s’affiche dans l’instruction, suivie de deux autres liens en gras. Les options diffèrent selon l’attribut de produit que vous sélectionnez.

     Une fois l’attribut défini, il ne peut pas être modifié. Pour modifier l’attribut, vous devez supprimer la ligne et ajouter le nouvel attribut. Vous pouvez supprimer une ligne de condition en cliquant sur l’icône Supprimer (![Icône Supprimer](assets/btn-del-red.png) à la fin de la ligne.

   - Cliquez sur **[!UICONTROL is]** et sélectionnez l’opérateur de comparaison qui décrit la condition à remplir pour les produits.

     Pour cet exemple, l’opérateur de comparaison est `is`. Les options disponibles dépendent de l’attribut sélectionné à l’étape précédente et peuvent inclure différentes options de comparaison. Les options peuvent inclure des valeurs correspondantes, sans inclure ou inclure au moins une valeur, et un montant supérieur, égal ou inférieur à un montant numérique. Dans cet exemple, les options sont `is` et `is not`.

   - Cliquez sur **[!UICONTROL ...]** et sélectionnez la valeur d’attribut sur laquelle repose la condition. Les options dépendent de la configuration de l’attribut.

     Vous pouvez être invité à sélectionner une option ou à saisir une valeur pour la condition. Dans cet exemple, le champ apparaît vide. Pour sélectionner votre ou vos catégories pour la règle, cliquez sur l’icône de sélection (![Icône de sélecteur](assets/btn-chooser.png)) pour afficher vos options de sélection. Cette règle est pour _Books_, cochez la case **[!UICONTROL Books]** . Le numéro de catégorie est renseigné. Pour accepter vos sélections de catégorie, cliquez sur l’icône en forme de coche verte (![Icône de coche](assets/btn-check-mark-green.png)).

     ![Condition de règle de prix - ligne 2, partie 3](assets/ob-price-rule-condition-3.png){width="500"}

     L’élément sélectionné apparaît dans l’instruction pour remplir la condition.

     ![Condition de règle de prix - ligne 2, partie 4](assets/ob-price-rule-condition-4.png){width="500"}

     Cet exemple de condition est terminé. Comme indiqué, cette condition signifie que tout produit de votre catalogue [!DNL Commerce] qui possède une catégorie définie de livres (`4`) est éligible à cette règle de tarification. Vous pouvez ajouter d’autres lignes de condition pour affiner davantage vos produits éligibles.

1. Pour ajouter une autre ligne de condition à l’instruction, revenez à l’étape 1 et répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

   Vous pouvez supprimer une ligne de l’instruction de condition à tout moment en cliquant sur l’icône Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.
