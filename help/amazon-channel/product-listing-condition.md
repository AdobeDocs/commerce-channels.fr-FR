---
title: Canal commercial Amazon - Condition de liste de produits
description: Utilisez les paramètres de condition de liste de produits pour mapper vos produits Commerce à une condition de produit Amazon, telle que "Nouveau" ou "Mise à jour".
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Condition de liste de produits

Les paramètres de condition de liste de produits font partie des paramètres de liste de magasins. Vous pouvez accéder aux paramètres de liste sur le [tableau de bord du magasin](./amazon-store-dashboard.md).

Amazon nécessite qu’une liste de produits ait une condition définie. Si tous vos produits sont la même condition, vous pouvez sélectionner l’une des options de condition Amazon pour représenter tous vos produits comme valeur de condition globale. Les conditions Amazon standard incluent :

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>Si vous vendez des produits renouvelés (rénovés), vous devez vous inscrire à l’ [!DNL Amazon Renewed Program]. Voir [Produits renouvelés](./renewed-products.md).

Cependant, si votre catalogue contient des produits dans différentes conditions (nouveaux, utilisés et mis à jour, par exemple), vous devez choisir **[!UICONTROL Assign Condition Using Product Attribute]**. Ce paramètre vous permet de mapper votre attribut de condition [!DNL Commerce] et vos valeurs aux conditions de votre liste Amazon.

Pendant les [tâches préalables à la configuration](./amazon-pre-setup-tasks.md), vous êtes invité à créer un attribut de produit [!DNL Commerce] pour la condition d’un produit. Si vous proposez des produits dans différentes conditions et que vous n’avez pas créé d’attribut de condition, voir [Création d’un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md). Une fois l’attribut de condition créé, vous pouvez attribuer une valeur de condition à chacun de vos produits dans votre catalogue [!DNL Commerce].

## Configuration des paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord du magasin.

1. Développez la section **[!UICONTROL Product Listing Condition]** .

1. Pour **[!UICONTROL Listing Product Condition]**, choisissez une option.

   Sélectionnez l’une des conditions Amazon standard pour votre valeur de condition globale pour toutes vos listes. Le paramètre par défaut est `New`.

   Si des produits/listes ont des conditions différentes, choisissez `Assign Condition Using Product Attribute` pour définir vos paramètres de condition de produit dans les champs supplémentaires qui s’affichent.

1. Pour **Attribut de condition**, choisissez l’attribut [!DNL Commerce] pour mapper les valeurs de chacun des attributs de condition Amazon standard.

   Si vous avez des produits dans la condition `Used` ou `Collectible` mais que vous ne faites pas d’autres différences, vous pouvez les mapper à une seule condition Amazon `Used` ou `Collectible` et laisser les autres vides. Cette méthode mappe toutes vos conditions `Used` ou `Collectible` à la condition unique Amazon Utilisé ou Collection.

   Par exemple, vous avez une seule condition `Used` pour vos produits. Lors du mappage, vous choisissez si vous souhaitez mapper à la condition Amazon `Used; Like New`, `Used; Very Good`, `Used; Good` ou `Used; Acceptable`. Renseignez uniquement le champ correspondant à la condition Amazon que vous souhaitez, en laissant les autres options `Used` définies sur `--Select Option--`. Dans l’exemple d’image, tous les produits [!DNL Commerce] de la condition `Used` sont mappés à la condition Amazon `Used; Very Good` .

   Vous pouvez également saisir un texte descriptif pour vos conditions, à l’exception de `New`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Condition de liste de produits](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Champ | Description |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | La condition de vos listes de produits. Options : `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vous vendez une seule condition de produit, choisissez l’une des conditions Amazon standard. Si votre catalogue [!DNL Commerce] contient des produits dans différentes conditions, choisissez `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | L’attribut [!DNL Commerce] qui définit la condition de vos produits. Sélectionnez l’attribut Magneto que vous avez créé pour mapper l’attribut de condition Amazon. Dans l’ [exemple de tâches préalables à la configuration](./ob-creating-magento-attributes.md) , vous pouvez lui donner le nom `Amazon Condition`. Lorsque cette option est sélectionnée, des champs supplémentaires s’affichent pour le mappage des conditions Amazon standard. |
| [!UICONTROL Additional Condition fields] | Pour chacune des conditions Amazon standard, choisissez la condition correspondante. Les options sont les étiquettes de condition que vous avez ajoutées lorsque vous [avez créé votre attribut de condition Amazon](./ob-creating-magento-attributes.md).<br><br>Si vous avez des produits dans la condition `Used` ou `Collectible` mais que vous ne faites pas d’autres différences, vous pouvez les mapper à une seule condition Amazon `Used` ou `Collectible` et laisser les autres vides. Cette méthode mappe toutes les conditions `Used` ou `Collectible` à la condition unique Amazon Utilisé ou Collection. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
