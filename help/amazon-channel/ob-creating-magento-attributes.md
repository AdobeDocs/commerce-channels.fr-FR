---
title: Créer [!DNL Commerce] Attributs pour Amazon
description: Avant de terminer le processus d'intégration du canal de vente Amazon, assurez-vous que vous disposez des [!UICONTROL Commerce] attributs de produit.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Créer [!DNL Commerce] attributs pour Amazon

Avant d’intégrer votre [!DNL Amazon Seller Central] comptes, il est recommandé d&#39;ajouter [!DNL Commerce] [attributs de produit](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;} pour mapper vos listes de produits. Une fois l’intégration terminée, vous pouvez gérer vos attributs de produit via l’onglet [Attributs](./managing-attributes.md) de la [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) .

Ces instructions détaillent comment créer des [!DNL Commerce] pour Amazon ASIN et Amazon Condition. Il est recommandé de créer des attributs supplémentaires, notamment Amazon EAN, Amazon ISBN et Amazon UPC. Vous pouvez également créer un attribut de prix Amazon si vous souhaitez utiliser le prix de vente Amazon comme source de prix pour les règles de tarification. Ces attributs sont utilisés lors de la configuration de vos paramètres d’annonce et de tarification lors de l’intégration. Utilisez également ces attributs lors de la création d’annonces Amazon et lors de la mise à jour et de la synchronisation de vos [!DNL Commerce] avec vos annonces Amazon.

Les paramètres de recherche de catalogue vous permettent de définir des paramètres de recherche correspondants qui aident à mapper les éléments éligibles [!DNL Commerce] produits avec annonces Amazon. Lorsqu’il est mappé, Amazon active des actions liées à la tarification, à la quantité, aux remplacements et à la synchronisation des commandes et des produits.

La définition de ces valeurs augmente le risque de correspondances exactes, ce qui réduit le besoin de faire correspondre manuellement les listes de produits ultérieurement. Ajout des attributs dans le cadre de votre intégration [tâches de préconfiguration](./amazon-pre-setup-tasks.md), Amazon Sales Channel a un potentiel plus élevé pour faire correspondre automatiquement vos produits lors de l’intégration et de la synchronisation des données de produit entre Amazon et [!DNL Commerce] après l’intégration.

Si vous créez uniquement l’attribut ASIN Amazon (sans ajouter de valeurs ASIN par produit), votre [!DNL Commerce] les produits peuvent ne pas correspondre automatiquement à vos annonces Amazon. Vous pouvez faire correspondre manuellement vos produits via _Révision du magasin_. Toutefois, la correspondance manuelle ne crée pas les éléments de données nécessaires pour partager et synchroniser vos données de produit.

>[!IMPORTANT]
>
>Si vous mettez à jour un élément de données ASIN, UPC ou autre pour un produit correspondant manuellement, vous devez mettre à jour les données dans les deux emplacements : votre [!DNL Commerce] et la liste dans votre [!DNL Amazon Seller Central] compte.

## Création de l’attribut de produit Amazon ASIN

1. Connectez-vous à votre [!DNL Commerce] Administrateur.

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans la boîte de dialogue _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attributs, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, entrez `Amazon ASIN` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, sélectionnez `Text Field`.

1. Pour **[!UICONTROL Values Required]**, sélectionnez `No`.

   Bien qu’un ASIN Amazon soit nécessaire pour répertorier un produit sur Amazon, certains de vos produits de catalogue peuvent ne pas être répertoriés sur Amazon.

1. Développez la _[!UICONTROL Advanced Attribute Properties]_et définissez les options suivantes :

   - Pour **[!UICONTROL Attribute Code]**, entrez `amazon_asin`.

   - Pour **[!UICONTROL Scope]**, sélectionnez `Global`.

   - Pour **[!UICONTROL Unique Value]**, sélectionnez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, sélectionnez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, sélectionnez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, sélectionnez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut ASIN Amazon](assets/creating-asin-attribute.png)

## Création de l’attribut de produit Condition Amazon

1. Connectez-vous à votre [!DNL Commerce] Administrateur.

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans la boîte de dialogue _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attribut, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, entrez `Amazon Condition` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, sélectionnez `Dropdown`.

   Le _[!UICONTROL Manage Options (Values of your Attribute)]_s’affiche.

1. Pour **[!UICONTROL Values Required]**, sélectionnez `No`.

1. Pour **[!UICONTROL Manage Options (Values for your Attribute)]**, ajoutez chacune de vos options de condition.

   Les conditions Amazon standard comprennent :

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Cliquez sur **[!UICONTROL Add Option]**.

1. Sélectionnez l’option **[!UICONTROL Is Default]** pour la condition que vous souhaitez être la sélection par défaut.

1. Dans la boîte de dialogue _[!UICONTROL Admin]_, entrez le texte de l’étiquette de la condition que vous ajoutez (par exemple, `New`, `Used`et `Used-Like New`)

1. Cliquez sur **[!UICONTROL Add Option]** pour ajouter d’autres options, si nécessaire.

1. Développer _[!UICONTROL Advanced Attribute Properties]_et définissez les options.

   - Pour **[!UICONTROL Attribute Code]**, entrez `amazon_condition`.

   - Pour **[!UICONTROL Scope]**, sélectionnez `Global`.

   - Pour **[!UICONTROL Unique Value]**, sélectionnez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, sélectionnez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, sélectionnez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, sélectionnez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut de condition Amazon](assets/creating-amazon-condition-attribute.png)

![Icône suivante](assets/btn-next.png) [**Continuer à ajouter ou vérifier la clé d’API**](./amazon-verify-api-key.md)
