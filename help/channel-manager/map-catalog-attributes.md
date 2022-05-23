---
title: Mise en correspondance des attributs de catalogue
description: Mappez les attributs pour correspondre à [DNL! Commerce] de produits existants [!DNL Walmart Marketplace] listes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].
source-git-commit: dfe56db25bb569ad70fb1036d539797bbb126dd5
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Mise en correspondance des attributs de catalogue

Avant de publier des listes à partir de [!DNL Commerce] to [!DNL Walmart Marketplace], vous devez mapper au moins un identifiant unique à partir de [!DNL Commerce] Catalogue à l’identifiant correspondant de Walmart.
Cette étape doit correspondre à [!DNL Commerce] produits existants [!DNL Walmart] listes et pour synchroniser les données de produit entre [!DNL Commerce] et [!DNL Walmart].

Pour la correspondance de produit, le produit Commerce doit avoir au moins un attribut de produit correspondant à l’un des identifiants de produit (ID de produit) suivants requis par [!DNL Walmart].

**Identifiants de produit Walmart requis**

| **Type accepté** | **Nom** | **Objectif** | **Chiffres acceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Élément commercial mondial | Objectif général, utilisé dans le monde entier | 14 chiffres |
| ISBN | Numéro de livre standard international | Papier, livre relié et livre électronique | 10 ou 13 chiffres |
| ISSN | Numéro de série standard international | Numéro de série à 8 chiffres qui permet d&#39;identifier les magazines, les revues, les journaux et les périodiques de toutes sortes diffusés sur tous supports et supports | 8 chiffres |
| UPC | Code de produit universel | Code de suivi de vente au détail standard | 12 chiffres |

Si votre catalogue ne comporte pas d’attribut correspondant à l’un de ces types, [ajout ou conversion d’un attribut de catalogue existant](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mapper les identifiants uniques

1. Sur le [!UICONTROL Listings] pour la boutique de canaux de vente, sélectionnez **[!UICONTROL Settings]**.

   - Recherchez l’attribut Walmart Marketplace à mapper.

   - Sélectionnez l’attribut correspondant dans la [!DNL Commerce] catalogue de magasin.

      L’exemple suivant mappe l’attribut UPC de Walmart Marketplace à l’attribut UPC du catalogue de produits.
   ![Mise en correspondance des attributs pour les critères de correspondance de produit](assets/products-map-attributes-for-match.png)

   - Sélectionner **[!UICONTROL Save]**.


## Mise à jour de la configuration des attributs mappés

Modifiez l’identifiant du produit Commerce pour les produits correspondants en mettant à jour les paramètres d’attribut mappés.

Par exemple, au lieu de faire correspondre des produits en fonction du code d’attribut de produit UPC de Commerce, vous pouvez établir une correspondance en fonction du SKU. Vous pouvez également mapper des attributs supplémentaires pour améliorer la correspondance.

1. Dans la **[!UICONTROL Listings]**, sélectionnez **[!UICONTROL Settings]**.

1. Sur le formulaire d’attribut Map , modifiez la configuration d’attribut mappé selon les besoins.
