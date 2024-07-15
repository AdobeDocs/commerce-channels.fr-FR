---
title: Gestion des attributs des listes Amazon
description: Vous pouvez gérer le mappage des attributs de produit Commerce avec les attributs Amazon afin d’assurer la précision des informations sur les produits entre les systèmes.
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Gestion des attributs des listes Amazon

Amazon et [!DNL Commerce] utilisent tous deux un système de propriétés de produit, appelées attributs, utilisées pour définir un produit. Les attributs définissent la description, le contenu, les images, les prix et diverses données pour vos produits.

Une communication réussie entre Commerce et Amazon nécessite que les attributs [!DNL Commerce] soient correctement mappés (ou correspondants) à l’attribut Amazon correspondant. Lors de l’intégration à Amazon, vous mappez ces attributs avec les attributs Amazon. Une fois terminé, [!DNL Commerce] peut synchroniser et gérer vos listes Amazon avec votre catalogue de produits [!DNL Commerce].

Supposons, par exemple, que votre catalogue [!DNL Commerce] et vos listes Amazon contiennent le même élément. Un attribut du produit peut être le prix de l’article. Le nom du prix de la liste dans [!DNL Commerce] peut être appelé `Price`, tandis que le prix de la liste pour Amazon peut être appelé `ListingPrice`. Vous devez indiquer à [!DNL Commerce] que, lors de la communication avec Amazon, l’attribut [!DNL Commerce] nommé `Price` est identique à l’attribut Amazon nommé `ListingPrice`. Ce processus, appelé _gestion des attributs_, comprend la création et la modification d’attributs existants. Assurez-vous que les attributs correspondent correctement pour assurer une communication correcte entre [!DNL Commerce] et Amazon.

Lorsque le mappage d’attributs est configuré, [!DNL Commerce] peut communiquer des informations sur les produits avec Amazon. Si vous avez des listes de produits Amazon, [!DNL Commerce] peut importer vos produits et détails Amazon dans votre catalogue [!DNL Commerce], ce qui vous permet de gérer vos listes Amazon à partir d’un seul catalogue central de produits.

Le canal de vente Amazon vous permet d’accéder aux attributs, de les examiner, de les créer et de les gérer, selon les besoins, dans la vue [_[!UICONTROL Attributes]_](./attributes-view.md) de la page d’accueil du canal de vente Amazon. Si vous ajoutez un attribut à votre catalogue [!DNL Commerce], il peut nécessiter une mise à jour de ces valeurs pour tous les produits.

Pour plus d’informations sur [!DNL Commerce] et les ensembles d’attributs et valeurs Amazon, voir :

- [Gérer les bases des attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Création d’un attribut](./creating-attributes.md#create-an-attribute)
- [Modifier un attribut existant](./creating-attributes.md#edit-an-attribute)
- [Affichage du mappage des attributs](./amazon-matching-attributes-values.md)
- [Modification ou création d’un mappage d’attribut](./amazon-manually-update-incomplete-listing.md)
