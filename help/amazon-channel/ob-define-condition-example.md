---
title: '''Exemple : Définir une condition"'
description: Lors de la création de vos règles de mise en vente, définissez les conditions d’identification des produits du catalogue Commerce qui doivent être répertoriés sur le Marché Amazon.
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Exemple : Définition d’une condition

## Conditions

Vous pouvez cliquer sur n’importe quelle zone en gras pour afficher les différentes options.

**Ne pas ajouter de conditions si tous les produits du site web sélectionné sont éligibles.**

>[!NOTE]
>
>Il existe un ensemble complexe de processus back-end pour communiquer directement avec les systèmes Amazon. En fonction du nombre d’éléments que vous tentez d’énumérer et de l’afflux des systèmes d’Amazon (tel que Black Friday), il peut s’avérer nécessaire de temps pour que vos éléments soient répertoriés sur Amazon.

Consultez la section Conditions de [Création d&#39;une règle de prix de panier](https://docs.magento.com/user-guide/marketing/price-rules-catalog-create.html){target=&quot;_blank&quot;}.

## Définition d’une condition

Ce processus peut être simple ou détaillé, en fonction de la configuration de votre catalogue. Vous pouvez configurer vos conditions de sorte que lorsque `ALL` ou `ANY` des conditions définies sont `TRUE` ou `FALSE` pour un produit, le produit peut alors être inscrit sur Amazon.

Les conditions sont basées sur les valeurs d’attribut de produit existantes. Pour appliquer la règle à tous les produits, laissez la section conditions vide.

>[!NOTE]
>
>Si vous souhaitez définir une condition basée sur un attribut de produit spécifique, définissez l’attribut **[!UICONTROL Use for Promo Rule Conditions]** paramètre pour l’attribut à `Yes`. Vous pouvez accéder à ce paramètre sur le noeud [Propriétés de la vitrine](https://docs.magento.com/user-guide/catalog/product-attributes-add.html)Page {target=&quot;_blank&quot;} pour l&#39;attribut.

![Condition - ligne 1](assets/ob-listing-rule-conditions-start.png)

La règle de cet exemple définit une règle qui définit l’éligibilité Amazon pour tous les produits de catalogue qui ont le _Amazon FBA_ attribut défini sur `Yes`.

L&#39;instruction de règle comporte deux liens en gras qui, lorsque l&#39;utilisateur clique dessus, affichent les options de cette partie de l&#39;instruction. Si vous enregistrez la condition sans modifier une option en gras, la règle s’applique à tous vos produits.

- Cliquez sur **[!UICONTROL ALL]** et choisissez soit `ALL` ou `ANY`.
- Cliquez sur **[!UICONTROL TRUE]** et choisissez `TRUE` ou `FALSE`.
- Pour appliquer la règle à tous les produits, ne modifiez pas la condition.

Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Pour cet exemple, la condition suivante est utilisée :

`If ALL of these conditions are TRUE:`

1. Cliquez sur Ajouter (![Icône Ajouter](assets/btn-add-grn.png)) au début de la ligne de condition et sélectionnez un attribut sur lequel baser la condition, tel qu’une combinaison de conditions ou un attribut de produit.

   - **[!UICONTROL Conditions Combination]** - Choisissez de vous autoriser à créer un autre jeu de `All/Any` et `True/False` dans le jeu existant.

      ![Combinaison de conditions](assets/ob-conditions-combinations.png)

   - **[!UICONTROL Product Attribute]** - Les attributs de produit dépendent de la configuration de l’attribut. Pour qu’un attribut apparaisse dans la liste, il doit être configuré pour une utilisation dans les conditions de règle promotionnelle. Voir la section _Utiliser pour les conditions des règles de promo_ dans [Attributs de produit](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

      Dans la liste sous **[!UICONTROL Product Attribute]**, sélectionnez l’attribut que vous souhaitez utiliser comme base de la condition. Pour cet exemple, la condition sélectionnée est `Amazon FBA`.

      ![Ligne de condition 2, partie 2](assets/ob-condition-attribute-dropdown.png)

      La condition sélectionnée apparaît dans l’instruction, suivie de deux autres liens en gras. Les options varient en fonction de l’attribut de produit sélectionné.

      Une fois l’attribut défini, il ne peut pas être modifié. Pour modifier l’attribut, vous devez supprimer la ligne et ajouter le nouvel attribut. Vous pouvez supprimer une ligne de condition en cliquant sur Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.

      1. Cliquez sur **[!UICONTROL is]** et choisissez l&#39;opérateur de comparaison qui décrit la condition à respecter pour les produits.

         Pour cet exemple, l’opérateur de comparaison est `is`. Les options disponibles dépendent de l’attribut sélectionné à l’étape précédente. Les options peuvent inclure différentes options de comparaison, telles que des valeurs correspondantes, sans inclure ou inclure au moins une valeur et supérieur à, égal à et inférieur à un montant numérique. Dans cet exemple, les options sont les suivantes : `is` et `is not`.

      1. Cliquez sur **[!UICONTROL ...]** et sélectionnez la valeur d’attribut sur laquelle la condition est basée.

         Les options dépendent de la configuration de l’attribut. Vous pouvez être invité à sélectionner une option ou à saisir du texte ou des valeurs numériques pour la condition. Pour cet exemple, la sélection est `Yes`.

         L&#39;élément sélectionné apparaît dans l&#39;instruction pour remplir la condition.

         ![Ligne de condition 2, partie 3](assets/ob-listing-rule-condition-is.png)
   Cette condition est terminée. Comme indiqué ci-dessus, cette condition signifie que tout produit dans votre [!DNL Commerce] catalogue dont l’attribut FBA Amazon est défini sur une valeur de `Yes` est admissible à l&#39;inscription à Amazon pour la région et le magasin. Vous pouvez ajouter d’autres lignes de condition pour affiner davantage vos produits admissibles.

1, Pour ajouter une autre ligne de condition à l’instruction, revenez à l’étape 1 et répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

Vous pouvez supprimer une ligne de l’instruction de condition à tout moment en cliquant sur le bouton Supprimer (![Icône Supprimer](assets/btn-del-red.png)) à la fin de la ligne.
