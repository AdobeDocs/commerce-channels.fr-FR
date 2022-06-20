---
title: Mise en correspondance des attributs de catalogue
description: Mappez les attributs pour correspondre à [DNL! Commerce] de produits existants [!DNL Walmart Marketplace] listes et synchronisation des données entre [!DNL Channel Manager] et [!DNL Walmart].
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Mise en correspondance des attributs de catalogue

Avant de connecter des listes depuis [!DNL Commerce] to [!DNL Walmart Marketplace], vous devez mapper au moins un identifiant unique à partir de [!DNL Commerce] Catalogue à l’identifiant correspondant de Walmart.

Cette étape doit correspondre à [!DNL Commerce] produits existants [!DNL Walmart] listes et pour synchroniser les données de produit entre [!DNL Commerce] et [!DNL Walmart]. Le [!DNL Commerce] Le produit doit avoir au moins un attribut de produit qui correspond à l’un des identifiants de produit (ID de produit) suivants requis par [!DNL Walmart].

**Obligatoire [!DNL Walmart] ID de produit**

| **Type accepté** | **Nom** | **Objectif** | **Chiffres acceptables** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Élément commercial mondial | Objectif général, utilisé dans le monde entier | 14 chiffres |
| ISBN | Numéro de livre standard international | Papier, livre relié et livre électronique | 10 ou 13 chiffres |
| ISSN | Numéro de série standard international | Numéro de série à 8 chiffres qui permet d&#39;identifier les magazines, les revues, les journaux et les périodiques de toutes sortes diffusés sur tous supports et supports | 8 chiffres |
| UPC | Code de produit universel | Code de suivi de vente au détail standard | 12 chiffres |

Si votre catalogue ne comporte pas d’attribut correspondant, [ajout ou conversion d’un attribut de catalogue existant](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mapper les identifiants uniques

1. Dans la **[!UICONTROL Listings]** ou **[!UICONTROL Orders]** pour la boutique de canaux de vente, sélectionnez **[!UICONTROL Channel Settings]**.

1. Activé **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Shipping Carriers]**.

   - Recherchez le [!DNL Walmart Marketplace] à mapper.

   - Sélectionnez l’attribut correspondant dans la [!DNL Commerce] catalogue de magasin.

      L’exemple suivant mappe la variable [!UICONTROL Walmart Marketplace UPC] à l’attribut UPC dans le catalogue de produits.
   ![Mise en correspondance des attributs pour les critères de correspondance de produit](assets/products-map-attributes-for-match.png)

   - Sélectionner **[!UICONTROL Save]**.


