---
title: Recherche de catalogue
description: Pour définir la correspondance d’attributs qui permet de mapper les produits de catalogue Commerce éligibles avec les annonces Amazon, mettez à jour les paramètres de recherche de catalogue.
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# Recherche de catalogue

_Recherche de catalogue_ font partie des paramètres de votre liste de magasins. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres vous permettent de définir la correspondance d’attributs qui aide à mapper les éléments éligibles [!DNL Commerce] produits avec annonces Amazon. Lorsqu’il est mappé, Amazon active des actions liées à la tarification, à la quantité, aux remplacements et à la synchronisation des commandes et des produits.

La définition de ces valeurs de mappage augmente le risque de correspondances exactes, ce qui réduit la nécessité de faire correspondre manuellement les listes de produits. Ajout des attributs dans le cadre de votre [Tâches de préconfiguration](./amazon-pre-setup-tasks.md), Amazon Sales Channel a un potentiel plus élevé pour faire correspondre automatiquement vos produits lors de l’intégration et de la synchronisation des données de produit entre Amazon et [!DNL Commerce].

Si vous créez uniquement l’attribut ASIN Amazon (sans ajouter de valeurs ASIN par produit), votre [!DNL Commerce] les produits peuvent ne pas correspondre automatiquement à vos annonces Amazon. Vous pouvez [assigner](./creating-assigning-catalog-products.md) vos produits. Toutefois, la correspondance manuelle ne crée pas les éléments de données nécessaires pour partager et synchroniser vos données de produit.

>[!IMPORTANT]
>
>Si vous avez fait correspondre manuellement un produit et que vous souhaitez mettre à jour un élément de données ASIN, UPC ou autre pour le produit, vous devez mettre à jour les données à deux endroits. Mettez-le à jour dans votre [!DNL Commerce] et dans votre liste Amazon dans votre [!DNL Amazon Seller Central] compte.

Il est recommandé de mettre en correspondance ces attributs et valeurs, le cas échéant. L’achèvement de ce mappage n’est pas nécessaire, mais est bénéfique pour la mise en correspondance des produits et nécessaire pour une synchronisation de catalogue correcte entre Amazon et [!DNL Commerce].

Si vous souhaitez ajouter des attributs, consultez [Créer des attributs de produit pour les correspondances Amazon](./ob-creating-magento-attributes.md).

## Configurer [!UICONTROL Catalog Search] paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la _[!UICONTROL Catalog Search]_.

1. Pour **[!UICONTROL ASIN]**, sélectionnez l’attribut de produit que vous avez créé pour la valeur ASIN Amazon.

   Un ASIN ([!DNL Amazon Standard Identification Number]) est un bloc unique de dix lettres et/ou chiffres qui identifient les éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article.

1. Pour **[!UICONTROL EAN]**, sélectionnez l’attribut de produit que vous avez créé pour la valeur Amazon EAN.

   Le numéro d&#39;article européen (EAN) est une norme de code à barres, un code d&#39;identification de produit à 12 ou 13 chiffres. Chaque EAN identifie de manière unique le produit, le fabricant et ses attributs ; généralement, l&#39;EAN est imprimé sur une étiquette de produit ou sur un emballage sous forme de code à barres. Amazon a besoin de codes EAN pour améliorer la qualité des résultats de recherche et la qualité du catalogue. Vous pouvez obtenir des EAN auprès du fabricant.

1. Pour **[!UICONTROL GCID]**, sélectionnez l’attribut de produit que vous avez créé pour la valeur Amazon GCIN.

   L’identifiant de catalogue global (GCID) est un ID pour les produits qui ne possèdent pas de code UPC ou d’ISBN. Le registre des marques Amazon vous permet de vous enregistrer en tant que propriétaire de marque et de créer un ID unique pour les produits.

1. Pour **[!UICONTROL ISBN]**, sélectionnez l’attribut de produit que vous avez créé pour la valeur ISBN Amazon.

   Le numéro international normalisé du livre (ISBN) est un code à barres d&#39;identification du livre commercial unique. Chaque code ISBN identifie de manière unique un livre. Un ISBN a dix ou treize chiffres. Tous les ISBN attribués après le 1er janvier 2007 ont 13 chiffres.

1. Pour **[!UICONTROL UPC]**, sélectionnez l’attribut de produit que vous avez créé pour la valeur Amazon UPC.

   Le code universel de produit (UPC) est un code à barres à 12 chiffres utilisé de façon intensive pour les emballages de détail aux États-Unis.

1. Pour **[!UICONTROL General Search]**, sélectionnez l’attribut de produit que vous souhaitez utiliser pour une correspondance de recherche générale.

   Cet attribut est un attribut que vous pouvez sélectionner pour qu’il corresponde [!DNL Commerce] produits vers la liste Amazon appropriée. La recherche générale utilise les recherches par mot-clé de votre catalogue. Il est donc recommandé d’utiliser un [!DNL Commerce] qui contient des mots-clés pertinents, tels que la référence SKU du produit ou le nom du produit. La recherche générale peut renvoyer de nombreuses correspondances possibles, et dans ce cas, vous pouvez sélectionner la liste Amazon appropriée parmi les correspondances possibles. Une sélection courante pour ce champ est `Product Name`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Recherche de catalogue](assets/amazon-catalog-search.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL ASIN] | Bloc unique de 10 lettres et/ou chiffres identifiant des éléments.<br><br>ASIN signifie [!DNL Amazon Standard Identification Number]. Un ASIN est un bloc unique de 10 lettres et/ou chiffres qui identifie des éléments. Pour les livres, l’ASIN est identique au numéro ISBN, mais pour tous les autres produits, un nouvel ASIN est créé lorsque l’élément est chargé dans leur catalogue. Vous pouvez trouver un ASIN articles sur la page de détails du produit sur Amazon, ainsi que d’autres détails relatifs à l’article. |
| [!UICONTROL EAN (European Article Number)] | Code d&#39;identification de produit à 12 ou 13 chiffres. Le numéro d&#39;article européen (EAN) est une norme de code à barres, un code d&#39;identification de produit à 12 ou 13 chiffres. Chaque EAN identifie de manière unique le produit, le fabricant et ses attributs ; généralement, l&#39;EAN est imprimé sur une étiquette de produit ou sur un emballage sous forme de code à barres. Amazon a besoin de codes EAN pour améliorer la qualité des résultats de recherche et la qualité du catalogue. Vous pouvez obtenir des EAN auprès du fabricant. |
| [!UICONTROL GCID (Global Catalog Identifier)] | L’identifiant de catalogue global (GCID) est un ID pour les produits qui ne possèdent pas de code UPC ou d’ISBN. Le registre des marques Amazon vous permet de vous enregistrer en tant que propriétaire de marque et de créer un ID unique pour les produits qui ne possèdent pas d’UPC ou d’ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | Un code à barres d&#39;identificateur de livre commercial unique à 10 ou 13 chiffres. Le numéro international normalisé du livre (ISBN) est un code à barres d&#39;identification du livre commercial unique. Chaque code ISBN identifie de manière unique un livre. Un ISBN a dix ou treize chiffres. Tous les ISBN attribués après le 1er janvier 2007 ont 13 chiffres. |
| UPC (Universal Product Code) | Code à barres à 12 chiffres. Le code universel de produit (UPC) est un code à barres à 12 chiffres utilisé de façon intensive pour les emballages de détail aux États-Unis. |
| [!UICONTROL General Search] | Sélectionnez un attribut. Cet attribut est un attribut que vous pouvez sélectionner pour qu’il corresponde [!DNL Commerce] produits vers la liste Amazon appropriée. La recherche générale utilise les recherches par mot-clé de votre catalogue. Il est donc recommandé d’utiliser un [!DNL Commerce] qui contient des mots-clés pertinents, tels que la référence SKU du produit ou le nom du produit. La recherche générale peut renvoyer de nombreuses correspondances possibles, et dans ce cas, vous pouvez sélectionner la liste Amazon appropriée parmi les correspondances possibles. Une sélection courante pour ce champ est `Product Name`. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
