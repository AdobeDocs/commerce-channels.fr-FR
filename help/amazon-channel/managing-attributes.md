---
title: Gestion des attributs
description: Vous pouvez gérer le mappage des attributs de produit Commerce avec les attributs Amazon pour garantir des informations de produit précises entre les systèmes.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Gestion des attributs

Amazon et [!DNL Commerce] tous deux utilisent un système de propriétés de produit, appelées attributs, utilisé pour définir un produit. Les attributs définissent la description, le contenu, les images, les prix et diverses données pour vos produits.

Une communication réussie entre Commerce et Amazon requiert que [!DNL Commerce] Les attributs doivent être correctement mappés (ou mis en correspondance) avec l’attribut Amazon correspondant. Lors de l’intégration à Amazon, vous mappez ces attributs avec les attributs Amazon. Une fois terminé, [!DNL Commerce] peut synchroniser et gérer vos listes Amazon avec votre [!DNL Commerce] catalogue de produits.

Imaginez, par exemple, que vous ayez le même élément dans votre [!DNL Commerce] catalogue et listes Amazon. Un attribut du produit peut être le prix de l’article. Nom du prix de la liste dans [!DNL Commerce] peut être nommé `Price`, tandis que le prix d’inscription d’Amazon peut être nommé `ListingPrice`. Vous devez indiquer [!DNL Commerce] que lors de la communication avec Amazon, la variable [!DNL Commerce] attribut nommé `Price` est identique à l’attribut Amazon nommé `ListingPrice`. Ce processus s’appelle _gestion des attributs_, et comprend la création et la modification d’attributs existants. S’assurer que les attributs sont correctement mis en correspondance garantit une communication correcte entre les [!DNL Commerce] et Amazon.

Lorsque le mappage des attributs est configuré, [!DNL Commerce] peut communiquer des informations sur les produits avec Amazon. Si vous disposez de listes de produits Amazon, [!DNL Commerce] Vous pouvez importer vos produits et détails Amazon dans votre [!DNL Commerce] catalogue, ce qui vous permet de gérer vos listes Amazon à partir d’un seul et même catalogue central de produits.

Le canal de vente Amazon vous permet d’accéder aux attributs, de les examiner, de les créer et de les gérer, selon vos besoins, dans le [_[!UICONTROL Attributes]_view](./attributes-view.md) sur la page d’accueil du canal de vente Amazon. Si vous ajoutez un attribut à votre [!DNL Commerce] catalogue, il peut nécessiter une mise à jour de ces valeurs pour tous les produits.

Pour plus d’informations sur [!DNL Commerce] et les ensembles d’attributs et valeurs Amazon, voir :

- [Gestion des bases d’attributs](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Création d’un attribut](./creating-attributes.md#create-an-attribute)
- [Modification d’un attribut existant](./creating-attributes.md#edit-an-attribute)
- [Affichage du mappage des attributs](./amazon-matching-attributes-values.md)
- [Modification ou création d’un mappage d’attribut](./amazon-manually-update-incomplete-listing.md)
