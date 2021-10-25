---
title: Conditions de la règle de prix
description: Utilisez les conditions de la règle de prix pour déterminer quels produits sont éligibles à la règle de prix d'annonce.
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Conditions de règle de prix

Les conditions déterminent quels produits sont éligibles à la règle de prix. La définition des conditions pour vos règles de tarification Amazon suit la même logique et le même processus que la définition des conditions pour [Règles de prix du panier](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;} dans [!DNL Commerce].

>[!IMPORTANT]
>
>Si votre règle de prix s’applique à tous les produits de votre [!DNL Commerce] , puis laissez cette section vide.

Vous pouvez cliquer sur n’importe quelle zone en gras pour afficher les différentes options.

## Exemple : créer une condition de règle de prix

Ce processus peut être simple ou détaillé, en fonction de la configuration de votre catalogue. Vous pouvez définir vos conditions de sorte que lorsque `ALL` ou `ANY` de ces conditions sont `TRUE` ou `FALSE` pour un produit, le produit est éligible à l’application de la règle de tarification.

Les conditions sont basées sur votre [attributs de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}. Pour appliquer la règle à tous les produits, laissez la section conditions vide.

>[!NOTE]
>
>Si vous souhaitez définir une condition basée sur un attribut de produit spécifique, **Utiliser pour les conditions des règles de promo** pour l’attribut doit être défini sur `Yes` dans votre [Propriétés de la vitrine](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target=&quot;_blank&quot;} pour l&#39;attribut.

![Condition de règle de prix - ligne 1](assets/ob-price-rules-condition-1.png)

Cet exemple définit une règle qui applique une remise de 25 % à tous les produits définis dans la `Books` catégorie.

L&#39;instruction de règle comporte deux liens en gras qui, lorsque l&#39;utilisateur clique dessus, affichent les options de cette partie de l&#39;instruction de condition. Si vous enregistrez la condition sans modifier une option en gras, la règle s’applique à tous vos produits.

- Cliquez sur **[!UICONTROL ALL]** et choisissez `ALL` ou `ANY`.
- Cliquez sur **[!UICONTROL TRUE]**, puis choisissez `TRUE` ou `FALSE`.
- Pour appliquer la règle à tous les produits, ne modifiez pas la condition.

Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Pour cet exemple, la condition suivante est utilisée :

`If ALL of these conditions are TRUE:`

1. Pour afficher les attributs disponibles auxquels la condition s’applique, cliquez sur le bouton Ajouter (![Icône Ajouter](assets/btn-add-grn.png)) au début de la ligne de condition et sélectionnez un attribut sur lequel baser la condition.

   **[!UICONTROL Conditions Combination]** - Choisissez de créer un autre jeu de `All/Any` et `True/False` dans la condition existante.

   ![Combinaison de conditions de règle de prix](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]** - Les attributs de produit disponibles dépendent de la [configuration de l’attribut](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target=&quot;_blank&quot;}. Pour qu’un attribut s’affiche dans la liste, *[!UICONTROL Use for Promo Rule Conditions]* pour l’attribut doit être défini sur `Yes` dans votre [propriétés storefront](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target=&quot;_blank&quot;}.

   - Pour **[!UICONTROL Product Attribute]**, sélectionnez l’attribut que vous souhaitez définir comme base de la condition. Pour cet exemple, la condition sélectionnée est `Category`.

      ![Condition de règle de prix - ligne 2, partie 2](assets/ob-price-rule-condition-2.png)

      La condition sélectionnée apparaît dans l’instruction, suivie de deux autres liens en gras. Les options varient en fonction de l’attribut de produit sélectionné.

      Une fois l’attribut défini, il ne peut pas être modifié. Pour modifier l’attribut, vous devez supprimer la ligne et ajouter le nouvel attribut. Vous pouvez supprimer une ligne de condition en cliquant sur Supprimer (![Icône Supprimer](assets/btn-del-red.png) à la fin de la ligne.

   - Cliquez sur **[!UICONTROL is]** et choisissez l&#39;opérateur de comparaison qui décrit la condition à respecter pour les produits.

      Pour cet exemple, l’opérateur de comparaison est `is`. Les options disponibles dépendent de l’attribut sélectionné à l’étape précédente et peuvent inclure différentes options de comparaison. Les options peuvent inclure des valeurs correspondantes, à l’exclusion ou à l’inclusion d’au moins une valeur, et supérieures à, égales à et inférieures à un montant numérique. Dans cet exemple, les options sont les suivantes : `is` et `is not`.

   - Cliquez sur **[!UICONTROL ...]** et sélectionnez la valeur d’attribut sur laquelle la condition est basée. Les options dépendent de la configuration de l’attribut.

      Vous pouvez être invité à sélectionner une option ou à saisir une valeur pour la condition. Dans cet exemple, le champ apparaît vide. Pour sélectionner votre ou vos catégories pour la règle, cliquez sur l’icône de sélecteur (![Icône Sélecteur](assets/btn-chooser.png)) pour afficher vos options de sélection. Cette règle est _Livres_, sélectionnez l’option **[!UICONTROL Books]** case à cocher. Le numéro de catégorie est renseigné. Pour accepter vos sélections de catégorie, cliquez sur la coche verte (![Icône de coche](assets/btn-check-mark-green.png)).

      ![Condition de règle de prix - ligne 2, partie 3](assets/ob-price-rule-condition-3.png)

      L&#39;élément sélectionné apparaît dans l&#39;instruction pour remplir la condition.

      ![Condition de règle de prix - ligne 2, partie 4](assets/ob-price-rule-condition-4.png)

      Cet exemple de condition est terminé. Comme indiqué ci-dessus, cette condition signifie que tout produit dans votre [!DNL Commerce] catalogue qui possède une catégorie définie de livres (`4`) est éligible à cette règle de tarification. Vous pouvez ajouter d’autres lignes de condition pour affiner davantage vos produits admissibles.

1. Pour ajouter une autre ligne de condition à l’instruction, revenez à l’étape 1 et répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

   Vous pouvez supprimer une ligne de l’instruction de condition à tout moment en cliquant sur le bouton Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.
