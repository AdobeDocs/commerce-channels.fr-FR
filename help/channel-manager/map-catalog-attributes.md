---
title: Mappage des attributs de catalogue
description: 'Mappez les attributs pour correspondre à [DNL! [Commerce] produits aux  [!DNL Walmart Marketplace] listes existantes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].'
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Mappage des attributs de catalogue

Avant de connecter les listes de [!DNL Commerce] à [!DNL Walmart Marketplace], vous devez mapper au moins un identifiant unique de votre catalogue [!DNL Commerce] à l’identifiant correspondant de Walmart.

Cette étape est nécessaire pour faire correspondre [!DNL Commerce] produits aux listes [!DNL Walmart] existantes et pour synchroniser les données de produit entre [!DNL Commerce] et [!DNL Walmart]. Le produit [!DNL Commerce] doit comporter au moins un attribut de produit qui correspond à l’un des identifiants de produit (ID de produit) suivants requis par [!DNL Walmart].

**ID de produit [!DNL Walmart] requis**

| **Type accepté** | **Nom** | **Objectif** | **Chiffres acceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Élément commercial mondial | Objectif général, utilisé dans le monde entier | 14 chiffres |
| ISBN | Numéro de livre standard international | Papier, livre relié et livre électronique | 10 ou 13 chiffres |
| ISSN | Numéro de série standard international | Numéro de série à 8 chiffres qui permet d&#39;identifier les magazines, les revues, les journaux et les périodiques de toutes sortes diffusés sur tous supports et supports | 8 chiffres |
| UPC | Code de produit universel | Code de suivi de vente au détail standard | 12 chiffres |

Si votre catalogue ne comporte pas d’attribut correspondant, [ajoutez ou convertissez un attribut de catalogue existant](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

## Mapper les identifiants uniques

1. Sur la page **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** de la boutique de canaux de vente, sélectionnez **[!UICONTROL Channel Settings]**.

1. Sur **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Map Attributes]**.

   - Recherchez l’attribut [!DNL Walmart Marketplace] à mapper.

   - Sélectionnez l’attribut correspondant dans le catalogue du magasin [!DNL Commerce].

     L’exemple suivant mappe l’attribut [!UICONTROL Walmart Marketplace UPC] à l’attribut UPC dans le catalogue de produits.

     ![ Attributs de mappage pour les critères de correspondance de produit ](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - Sélectionnez **[!UICONTROL Save]**.
