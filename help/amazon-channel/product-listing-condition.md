---
title: Condition de liste de produits
description: Utilisez les paramètres Condition de la liste de produits pour mapper vos produits Commerce à une condition de produit Amazon, telle que "Nouveau" ou "Rénové".
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Condition de mise en vente de produits

Les paramètres de condition de la mise en vente des produits font partie des paramètres de mise en vente de votre boutique. Vous pouvez accéder aux paramètres de mise en vente sur la page [tableau de bord de magasin](./amazon-store-dashboard.md).

Pour qu’une condition soit définie, Amazon doit disposer d’une liste de produits. Si tous vos produits sont dans la même condition, vous pouvez sélectionner l’une des options de condition Amazon pour représenter tous vos produits comme valeur de condition globale. Les conditions Amazon standard comprennent :

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
>Si vous vendez des produits renouvelés (remis à neuf), vous devez vous inscrire au [!DNL Amazon Renewed Program]. Voir [Produits renouvelés](./renewed-products.md).

Toutefois, si votre catalogue contient des produits dans des conditions différentes (Nouveau, Utilisé et Rénové, par exemple), vous devez choisir **[!UICONTROL Assign Condition Using Product Attribute]**. Ce paramètre vous permet de mapper votre [!DNL Commerce] attributs et valeurs de condition aux conditions de votre liste Amazon.

Pendant [Tâches de préconfiguration](./amazon-pre-setup-tasks.md), vous êtes invité à créer une [!DNL Commerce] attribut de produit pour la condition d’un produit. Si vous proposez des produits dans différentes conditions et que vous n’avez pas créé d’attribut de condition, consultez [Créer un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md). Une fois l’attribut de condition créé, vous pouvez attribuer une valeur de condition à chacun de vos produits dans votre [!DNL Commerce] catalogue.

## Configuration des paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la **[!UICONTROL Product Listing Condition]** .

1. Pour **[!UICONTROL Listing Product Condition]**, choisissez une option.

   Sélectionnez l’une des conditions Amazon standard pour votre valeur de condition globale pour toutes vos annonces. Le paramètre par défaut est `New`.

   Si vous avez des produits/annonces qui ont des conditions différentes, sélectionnez `Assign Condition Using Product Attribute` pour définir vos paramètres de condition de produit dans les champs supplémentaires qui s’affichent.

1. Pour **Attribut de condition**, sélectionnez l’option [!DNL Commerce] pour mapper des valeurs pour chacun des attributs de condition Amazon standard.

   Si vous avez des produits dans la `Used` ou `Collectible` mais vous ne pouvez pas distinguer plus loin, vous pouvez mapper sur un `Used` ou `Collectible` Amazon et laissez les autres vides. Cette méthode met en correspondance tous les `Used` ou `Collectible` à la condition unique Amazon utilisée ou Collectible.

   Par exemple, vous n’avez qu’une seule `Used` pour vos produits. Lors du mappage, vous indiquez si vous souhaitez mapper à la condition Amazon. `Used; Like New`, `Used; Very Good`, `Used; Good`, ou `Used; Acceptable`. Remplissez uniquement le champ correspondant à la condition Amazon souhaitée, en laissant l’autre `Used` options définies sur `--Select Option--`. Dans l’image d’exemple, tous [!DNL Commerce] produits dans `Used` sont mappées vers l’Amazon `Used; Very Good` condition.

   Vous pouvez également saisir un texte descriptif pour vos conditions, sauf `New`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Condition de mise en vente de produits](assets/amazon-product-listing-condition.png)

| Champ | Description |
|---|---|
| [!UICONTROL Listing Product Condition] | État de vos annonces de produits. Options : `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Si vous vendez une seule condition de produit, choisissez l’une des conditions Amazon standard. Si [!DNL Commerce] catalogue contient des produits dans différentes conditions, sélectionnez `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | Le [!DNL Commerce] qui définit la condition de vos produits. Sélectionnez l’attribut Magneto que vous avez créé pour mapper à l’attribut de condition Amazon. Dans la boîte de dialogue [Exemple de tâches de préconfiguration](./ob-creating-magento-attributes.md) recommande de le nommer comme `Amazon Condition`. Lorsque cette option est sélectionnée, des champs supplémentaires s’affichent pour le mappage des conditions Amazon standard. |
| [!UICONTROL Additional Condition fields] | Pour chacune des conditions Amazon standard, sélectionnez la condition correspondante. Les options sont les libellés de condition que vous avez ajoutés lorsque vous [a créé votre attribut de condition Amazon](./ob-creating-magento-attributes.md).<br><br>Si vous avez des produits dans la `Used` ou `Collectible` mais vous ne pouvez pas distinguer plus loin, vous pouvez mapper sur un `Used` ou `Collectible` Amazon et laissez les autres vides. Cette méthode mappe tous les `Used` ou `Collectible` à la condition unique Amazon utilisée ou Collectible. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
