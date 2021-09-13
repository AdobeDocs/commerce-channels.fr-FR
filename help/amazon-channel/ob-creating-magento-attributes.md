---
title: Création d’attributs [!DNL Commerce] pour Amazon
description: Avant de terminer le processus d’intégration du canal de vente Amazon, assurez-vous de disposer des attributs de produit [!UICONTROL Commerce] nécessaires.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Créer des attributs [!DNL Commerce] pour Amazon

Avant d’intégrer vos comptes [!DNL Amazon Seller Central], il est recommandé d’ajouter [!DNL Commerce] [attributs de produit](https://docs.magento.com/user-guide/stores/attributes-product.html){:target=&quot;_blank&quot;} pour mapper vos listes de produits. Une fois l’intégration terminée, vous pouvez gérer les attributs de vos produits à l’aide de l’onglet [Attributs](./managing-attributes.md) de la [page d’accueil du canal de vente Amazon](./amazon-sales-channel-home.md).

Ces instructions expliquent comment créer des attributs [!DNL Commerce] pour Amazon ASIN et la condition Amazon. Il est recommandé de créer des attributs supplémentaires, notamment Amazon EAN, Amazon ISBN et Amazon UPC. Vous pouvez également créer un attribut de prix Amazon si vous souhaitez utiliser le prix de votre offre Amazon comme source de prix pour les règles de tarification. Ces attributs sont utilisés lors de la configuration de vos paramètres de liste et de tarification lors de l’intégration. Utilisez également ces attributs lors de la création de listes Amazon et lors de la mise à jour et de la synchronisation de votre catalogue [!DNL Commerce] avec vos listes Amazon.

Les paramètres de recherche catalogue vous permettent de définir des paramètres de recherche correspondants qui permettent de mapper des produits [!DNL Commerce] éligibles avec des listes Amazon. Lorsqu’il est mappé, Amazon active des actions liées à la tarification, à la quantité, aux remplacements et à la synchronisation des commandes et des produits.

La définition de ces valeurs augmente le risque de correspondances exactes, ce qui réduit le besoin de faire correspondre manuellement les listes de produits ultérieurement. En ajoutant les attributs dans le cadre de vos [tâches préalables à la configuration](./amazon-pre-setup-tasks.md), le canal de vente Amazon a un potentiel plus élevé pour faire correspondre automatiquement vos produits lors de l’intégration et synchroniser les données de produit entre Amazon et [!DNL Commerce] après l’intégration.

Si vous créez uniquement l’attribut Amazon ASIN (sans ajouter de valeurs ASIN par produit), vos produits [!DNL Commerce] peuvent ne pas correspondre automatiquement à vos listes Amazon. Vous pouvez faire correspondre manuellement vos produits par l’intermédiaire de _Store Review_. Toutefois, la correspondance manuelle ne crée pas les éléments de données nécessaires pour partager et synchroniser les données de vos produits.

>[!IMPORTANT]
>
>Si vous mettez à jour un élément de données ASIN, UPC ou autre pour un produit correspondant manuellement, vous devez mettre à jour les données aux deux emplacements : votre catalogue [!DNL Commerce] et la liste de votre compte [!DNL Amazon Seller Central].

## Création de l’attribut de produit Amazon ASIN

1. Connectez-vous à votre administrateur [!DNL Commerce].

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans la section _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attributs, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, saisissez `Amazon ASIN` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, choisissez `Text Field`.

1. Pour **[!UICONTROL Values Required]**, choisissez `No`.

   Bien qu’un ASIN Amazon soit requis pour répertorier un produit sur Amazon, certains de vos produits de catalogue peuvent ne pas être répertoriés sur Amazon.

1. Développez la section _[!UICONTROL Advanced Attribute Properties]_et définissez les options suivantes :

   - Pour **[!UICONTROL Attribute Code]**, saisissez `amazon_asin`.

   - Pour **[!UICONTROL Scope]**, choisissez `Global`.

   - Pour **[!UICONTROL Unique Value]**, choisissez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, choisissez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, choisissez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, choisissez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut Amazon ASIN](assets/creating-asin-attribute.png)

## Création de l’attribut de produit Condition Amazon

1. Connectez-vous à votre administrateur [!DNL Commerce].

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans la section _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attribut, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, saisissez `Amazon Condition` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, choisissez `Dropdown`.

   La section _[!UICONTROL Manage Options (Values of your Attribute)]_s’affiche.

1. Pour **[!UICONTROL Values Required]**, choisissez `No`.

1. Pour **[!UICONTROL Manage Options (Values for your Attribute)]**, ajoutez chacune de vos options de condition.

   Les conditions Amazon standard incluent :

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Cliquez sur **[!UICONTROL Add Option]**.

1. Sélectionnez l&#39;option **[!UICONTROL Is Default]** pour la condition que vous souhaitez être la sélection par défaut.

1. Dans la colonne _[!UICONTROL Admin]_, saisissez le texte du libellé de la condition que vous ajoutez (par exemple `New`, `Used` et `Used-Like New`).

1. Cliquez sur **[!UICONTROL Add Option]** pour ajouter d’autres options, si nécessaire.

1. Développez la section _[!UICONTROL Advanced Attribute Properties]_et définissez les options.

   - Pour **[!UICONTROL Attribute Code]**, saisissez `amazon_condition`.

   - Pour **[!UICONTROL Scope]**, choisissez `Global`.

   - Pour **[!UICONTROL Unique Value]**, choisissez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, choisissez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, choisissez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, choisissez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut de condition Amazon](assets/creating-amazon-condition-attribute.png)

![Icône suivante ](assets/btn-next.png) [**: Ajoutez ou vérifiez la clé API.**](./amazon-verify-api-key.md)
