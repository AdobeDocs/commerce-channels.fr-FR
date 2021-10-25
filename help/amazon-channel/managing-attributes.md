---
title: Gérer les attributs
description: Vous pouvez gérer le mappage des attributs de produit Commerce avec les attributs Amazon pour garantir l’exactitude des informations sur les produits entre les systèmes.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Gestion des attributs

Amazon et [!DNL Commerce] tous deux utilisent un système de propriétés de produit, appelées attributs, utilisé pour définir un produit. Les attributs définissent la description, le contenu, les images, les prix et les diverses données de vos produits.

Une communication réussie entre le Commerce et Amazon exige que [!DNL Commerce] doit être mappé (ou mis en correspondance) correctement avec l’attribut Amazon correspondant. Lors de l’intégration avec Amazon, vous mappez ces attributs aux attributs Amazon. Une fois terminé, [!DNL Commerce] peut synchroniser et gérer vos annonces Amazon avec votre [!DNL Commerce] catalogue de produits.

Par exemple, imaginez que vous ayez le même élément dans votre [!DNL Commerce] catalogue et annonces Amazon. Un attribut du produit peut être le prix de vente de l&#39;article. Nom du prix d&#39;annonce dans [!DNL Commerce] peut être nommé `Price`, tandis que le prix d&#39;inscription pour Amazon peut être nommé `ListingPrice`. Vous devez indiquer [!DNL Commerce] que lors de la communication avec Amazon, [!DNL Commerce] attribut nommé `Price` est identique à l’attribut Amazon nommé `ListingPrice`. Ce processus est appelé _gestion des attributs_, et inclut la création et la modification d’attributs existants. Veiller à ce que les attributs soient correctement mis en correspondance garantit une communication correcte entre les [!DNL Commerce] et Amazon.

Lorsque le mappage d’attributs est configuré, [!DNL Commerce] peut communiquer des informations sur les produits entre les deux pays avec Amazon. Si vous avez des annonces de produits Amazon, [!DNL Commerce] Vous pouvez importer vos produits Amazon et les détails dans votre [!DNL Commerce] , ce qui vous permet de gérer vos annonces Amazon à partir d’un catalogue central de produits unique.

Le canal de vente Amazon vous permet d’accéder, de réviser, de créer et de gérer des attributs, selon vos besoins, dans le dossier [_[!UICONTROL Attributes]_affichage](./attributes-view.md) sur la page d&#39;accueil du canal de vente Amazon. Si vous ajoutez un attribut à votre [!DNL Commerce] , il peut nécessiter une mise à jour de ces valeurs pour tous les produits.

Pour plus d’informations sur [!DNL Commerce] et Amazon attribute sets and values, voir :

- [Principes de base de la gestion des attributs](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Création d’un attribut](./creating-attributes.md#create-an-attribute)
- [Modification d’un attribut existant](./creating-attributes.md#edit-an-attribute)
- [Afficher le mappage d’attributs](./amazon-matching-attributes-values.md)
- [Modification ou création d’un mappage d’attributs](./amazon-manually-update-incomplete-listing.md)
