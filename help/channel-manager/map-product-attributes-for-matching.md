---
title: Configuration de la correspondance de produits
description: Mappez les attributs pour faire correspondre les produits Commerce aux listes Walmart Marketplace existantes.
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 97b8ace717ace2a81cb39b9b7b09ff3fe06ef5e4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Configuration de la correspondance de produits

Avant de publier la liste sur Walmart Marketplace, vous devez associer au moins un identifiant unique des attributs de votre catalogue de produits à l’un des identifiants de produits Walmart Marketplace requis. Cette étape est requise pour faire correspondre les produits sur le marché Walmart.

Pour la correspondance des produits, le produit Commerce doit avoir au moins un des identifiants de produit (ID de produit) suivants dans les attributs de catalogue.

**Identifiants de produit Walmart requis**

| **Type accepté** | **Nom** | **Objectif** | **Chiffres acceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Élément commercial mondial | Objectif général, utilisé dans le monde entier | 14 chiffres |
| ISBN | Numéro de livre standard international | Papier, livre relié et livre électronique | 10 ou 13 chiffres |
| ISSN | Numéro de série standard international | Numéro de série à 8 chiffres qui permet d&#39;identifier les magazines, les revues, les journaux et les périodiques de toutes sortes diffusés sur tous supports et supports | 8 chiffres |
| ISBN | Numéro de livre standard international | Paperback, Hardcover et Electronic | 12 chiffres |

Si votre catalogue contient un type d’attribut ID de produit différent, convertissez-le en l’un des types requis. Ensuite, mappez-le à l’attribut Walmart Marketplace correspondant dans la configuration de liste de la boutique Channel Manager.

## Configuration des paramètres d’attribut de produit

1. Sur la page de liste de produits du canal de vente connecté, sélectionnez un ou plusieurs produits dans *Version préliminaire* statut.

1. Sélectionner **[!UICONTROL Settings]**.

   - Recherchez l’attribut Walmart Marketplace à mapper.

   - Sélectionnez l’attribut correspondant dans le catalogue du magasin.

      L’exemple suivant mappe l’attribut UPC de Walmart Marketplace à l’attribut UPC du catalogue de produits.
   ![Mise en correspondance des attributs pour les critères de correspondance de produit](assets/products-map-attributes-for--match.png)

   - Sélectionner **[!UICONTROL Save]**.


## Mise à jour de la configuration des attributs mappés

Modifiez l’identifiant du produit Commerce pour les produits correspondants en mettant à jour les paramètres d’attribut mappés.

Par exemple, au lieu de faire correspondre des produits en fonction du code d’attribut de produit UPC de Commerce, vous pouvez établir une correspondance en fonction du SKU. Vous pouvez également mapper des attributs supplémentaires pour améliorer la correspondance.

1. Dans la **[!UICONTROL Listings]**, sélectionnez **[!UICONTROL Settings]**.

1. Sur le formulaire d’attribut Map , modifiez la configuration d’attribut mappé selon les besoins.
