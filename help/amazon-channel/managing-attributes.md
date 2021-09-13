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

Amazon et [!DNL Commerce] utilisent tous deux un système de propriétés de produit, appelées attributs, utilisées pour définir un produit. Les attributs définissent la description, le contenu, les images, les prix et diverses données pour vos produits.

Une communication réussie entre Commerce et Amazon nécessite que les attributs [!DNL Commerce] soient correctement mappés (ou correspondants) à l’attribut Amazon correspondant. Lors de l’intégration à Amazon, vous mappez ces attributs avec les attributs Amazon. Une fois l’opération terminée, [!DNL Commerce] peut synchroniser et gérer vos listes Amazon avec votre catalogue de produits [!DNL Commerce].

Supposons, par exemple, que votre catalogue [!DNL Commerce] et vos listes Amazon contiennent le même élément. Un attribut du produit peut être le prix de l’article. Le nom du prix de l’offre dans [!DNL Commerce] peut être nommé `Price`, tandis que le prix de l’offre pour Amazon peut être nommé `ListingPrice`. Vous devez indiquer à [!DNL Commerce] que lors de la communication avec Amazon, l’attribut [!DNL Commerce] nommé `Price` est identique à l’attribut Amazon nommé `ListingPrice`. Ce processus s’appelle _gestion des attributs_ et comprend la création et la modification d’attributs existants. Assurez-vous que les attributs correspondent correctement pour assurer une communication correcte entre [!DNL Commerce] et Amazon.

Lorsque le mappage d’attributs est configuré, [!DNL Commerce] peut communiquer des informations sur les produits avec Amazon. Si vous disposez de listes de produits Amazon, [!DNL Commerce] peut importer vos produits et détails Amazon dans votre catalogue [!DNL Commerce], ce qui vous permet de gérer vos listes Amazon à partir d’un seul et même catalogue central de produits.

Le canal de vente Amazon vous permet d’accéder aux attributs, de les examiner, de les créer et de les gérer, selon les besoins, dans la [_[!UICONTROL Attributes]_vue](./attributes-view.md) de la page d’accueil du canal de vente Amazon. Si vous ajoutez un attribut à votre catalogue [!DNL Commerce], il peut nécessiter une mise à jour de ces valeurs pour tous les produits.

Pour plus d’informations sur [!DNL Commerce] et les ensembles d’attributs et valeurs Amazon, voir :

- [Gérer les attributs de base](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Création d’un attribut](./creating-attributes.md#create-an-attribute)
- [Modification d’un attribut existant](./creating-attributes.md#edit-an-attribute)
- [Affichage du mappage des attributs](./amazon-matching-attributes-values.md)
- [Modification ou création d’un mappage d’attribut](./amazon-manually-update-incomplete-listing.md)
