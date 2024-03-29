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

Les paramètres de condition de liste de produits font partie des paramètres de liste de magasins. Vous pouvez accéder aux paramètres de la liste sur la page [tableau de bord de la boutique](./amazon-store-dashboard.md).

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
>Si vous vendez des produits renouvelés (actualisés), vous devez vous inscrire à la variable [!DNL Amazon Renewed Program]. Voir [Produits renouvelés](./renewed-products.md).

Cependant, si votre catalogue contient des produits dans différentes conditions (nouveaux, utilisés et mis à jour, par exemple), vous devez choisir **[!UICONTROL Assign Condition Using Product Attribute]**. Ce paramètre vous permet de mapper votre [!DNL Commerce] attribut de condition et valeurs aux conditions de votre liste Amazon.

Durant [Tâches préalables à la configuration](./amazon-pre-setup-tasks.md), vous êtes invité à créer une [!DNL Commerce] attribut de produit pour la condition d’un produit. Si vous proposez des produits dans différentes conditions et que vous n’avez pas créé d’attribut de condition, voir [Créez un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md). Une fois l’attribut de condition créé, vous pouvez attribuer une valeur de condition à chacun de vos produits dans votre [!DNL Commerce] catalogue.

## Configuration des paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord de la boutique.

1. Développez l’objet **[!UICONTROL Product Listing Condition]** .

1. Pour **[!UICONTROL Listing Product Condition]**, choisissez une option.

   Sélectionnez l’une des conditions Amazon standard pour votre valeur de condition globale pour toutes vos listes. Le paramètre par défaut est `New`.

   Si des produits/listes ont des conditions différentes, choisissez `Assign Condition Using Product Attribute` pour définir vos paramètres de condition de produit dans les champs supplémentaires qui s’affichent.

1. Pour **Attribut de condition**, choisissez la variable [!DNL Commerce] pour mapper des valeurs pour chacun des attributs de condition Amazon standard.

   Si vous avez des produits dans la variable `Used` ou `Collectible` mais vous ne pouvez pas distinguer davantage, vous pouvez mapper sur une seule condition `Used` ou `Collectible` condition Amazon et laissez les autres vides. Cette méthode mappe tous les `Used` ou `Collectible` conditions d’utilisation ou de collection d’Amazon unique.

   Par exemple, vous disposez d’une `Used` condition de vos produits. Lors du mappage, vous choisissez si vous souhaitez mapper à la condition Amazon. `Used; Like New`, `Used; Very Good`, `Used; Good`, ou `Used; Acceptable`. Renseignez uniquement le champ correspondant à la condition Amazon souhaitée, en laissant l’autre `Used` options définies sur `--Select Option--`. Dans l’exemple d’image, toutes les [!DNL Commerce] produits dans `Used` sont mappées à la condition Amazon. `Used; Very Good` condition.

   Vous pouvez également saisir un texte descriptif pour vos conditions, à l’exception des `New`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Condition de liste de produits](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Champ | Description |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | La condition de vos listes de produits. Options : `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vous vendez une seule condition de produit, sélectionnez l’une des conditions Amazon standard. Si votre [!DNL Commerce] Le catalogue contient des produits sous diverses conditions, sélectionnez `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | La variable [!DNL Commerce] qui définit la condition de vos produits. Sélectionnez l’attribut Magneto que vous avez créé pour mapper l’attribut de condition Amazon. Dans le [Exemple de tâches préalables à la configuration](./ob-creating-magento-attributes.md) recommande de le nommer comme `Amazon Condition`. Lorsque cette option est sélectionnée, des champs supplémentaires s’affichent pour le mappage des conditions Amazon standard. |
| [!UICONTROL Additional Condition fields] | Pour chacune des conditions Amazon standard, choisissez la condition correspondante. Les options sont les étiquettes de condition que vous avez ajoutées lorsque vous [création de votre attribut de condition Amazon](./ob-creating-magento-attributes.md).<br><br>Si vous avez des produits dans la variable `Used` ou `Collectible` mais vous ne pouvez pas distinguer davantage, vous pouvez mapper sur une seule condition `Used` ou `Collectible` condition Amazon et laissez les autres vides. Cette méthode mappe tous les `Used` ou `Collectible` conditions d’utilisation ou de collection d’Amazon unique. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
