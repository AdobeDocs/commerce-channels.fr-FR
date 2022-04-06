---
title: Créer [!DNL Commerce] Attributs pour Amazon
description: Avant de terminer le processus d’intégration du canal de vente Amazon, assurez-vous que vous disposez des [!UICONTROL Commerce] attributs de produit.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Créer [!DNL Commerce] Attributs pour Amazon

Avant d’intégrer votre [!DNL Amazon Seller Central] comptes, il est recommandé d’ajouter [!DNL Commerce] [attributs de produit](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;} pour mapper vos listes de produits. Une fois l’intégration terminée, vous pouvez gérer les attributs de vos produits par le biais de l’ [Attributs](./managing-attributes.md) de l’onglet [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) page.

Ces instructions expliquent comment créer des [!DNL Commerce] attributs pour Amazon ASIN et la condition Amazon. Il est recommandé de créer des attributs supplémentaires, notamment Amazon EAN, Amazon ISBN et Amazon UPC. Vous pouvez également créer un attribut de prix Amazon si vous souhaitez utiliser le prix de votre offre Amazon comme source de prix pour les règles de tarification. Ces attributs sont utilisés lors de la configuration de vos paramètres de liste et de tarification lors de l’intégration. Utilisez également ces attributs lors de la création de listes Amazon et lors de la mise à jour et de la synchronisation de vos [!DNL Commerce] catalogue avec vos listes Amazon.

Les paramètres de recherche catalogue vous permettent de définir les paramètres de recherche correspondants qui aident à mapper les éléments éligibles [!DNL Commerce] produits avec des listes Amazon. Lorsqu’il est mappé, Amazon active des actions liées à la tarification, à la quantité, aux remplacements et à la synchronisation des commandes et des produits.

La définition de ces valeurs augmente le risque de correspondances exactes, ce qui réduit le besoin de faire correspondre manuellement les listes de produits ultérieurement. Ajout des attributs dans le cadre de votre intégration [tâches de préconfiguration](./amazon-pre-setup-tasks.md), le canal de vente Amazon présente un potentiel plus élevé de mise en correspondance automatique de vos produits lors de l’intégration et de la synchronisation des données de produit entre Amazon et [!DNL Commerce] après l’intégration.

Si vous créez uniquement l’attribut Amazon ASIN (sans ajouter de valeurs ASIN par produit), votre [!DNL Commerce] les produits peuvent ne pas correspondre automatiquement à vos listes Amazon. Vous pouvez faire correspondre manuellement vos produits par le biais de _Critique du magasin_. Toutefois, la correspondance manuelle ne crée pas les éléments de données nécessaires pour partager et synchroniser les données de vos produits.

>[!IMPORTANT]
>
>Si vous mettez à jour un élément de données ASIN, UPC ou autre pour un produit correspondant manuellement, vous devez mettre à jour les données aux deux emplacements : your [!DNL Commerce] et la liste dans votre [!DNL Amazon Seller Central] compte .

## Création de l’attribut de produit Amazon ASIN

1. Connectez-vous à votre [!DNL Commerce] Administrateur.

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans le _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attributs, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, saisissez `Amazon ASIN` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, choisissez `Text Field`.

1. Pour **[!UICONTROL Values Required]**, choisissez `No`.

   Bien qu’un ASIN Amazon soit requis pour répertorier un produit sur Amazon, certains de vos produits de catalogue peuvent ne pas être répertoriés sur Amazon.

1. Développez l’objet _[!UICONTROL Advanced Attribute Properties]_et définissez les options suivantes :

   - Pour **[!UICONTROL Attribute Code]**, saisissez `amazon_asin`.

   - Pour **[!UICONTROL Scope]**, choisissez `Global`.

   - Pour **[!UICONTROL Unique Value]**, choisissez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, choisissez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, choisissez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, choisissez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut Amazon ASIN](assets/creating-asin-attribute.png)

## Création de l’attribut de produit Condition Amazon

1. Connectez-vous à votre [!DNL Commerce] Administrateur.

1. Cliquez sur **[!UICONTROL Stores]** dans le menu de gauche.

1. Dans le _[!UICONTROL Attributes]_, cliquez sur **[!UICONTROL Product]**.

1. Pour ouvrir les propriétés d’attribut, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Pour **[!UICONTROL Default Label]**, saisissez `Amazon Condition` (nom de votre attribut).

1. Pour **[!UICONTROL Catalog Input Type for Store Owner]**, choisissez `Dropdown`.

   Le _[!UICONTROL Manage Options (Values of your Attribute)]_s’affiche.

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

1. Sélectionnez la **[!UICONTROL Is Default]** pour la condition que vous souhaitez être la sélection par défaut.

1. Dans le _[!UICONTROL Admin]_, saisissez le texte du libellé de la condition que vous ajoutez (par exemple `New`, `Used`, et `Used-Like New`)

1. Cliquez sur **[!UICONTROL Add Option]** pour ajouter d’autres options, si nécessaire.

1. Développer _[!UICONTROL Advanced Attribute Properties]_et définissez les options.

   - Pour **[!UICONTROL Attribute Code]**, saisissez `amazon_condition`.

   - Pour **[!UICONTROL Scope]**, choisissez `Global`.

   - Pour **[!UICONTROL Unique Value]**, choisissez `No`.

   - Pour **[!UICONTROL Input Validation for Store Owner]**, choisissez `None`.

   - Pour **[!UICONTROL Add to Column Options]**, choisissez `Yes`.

   - Pour **[!UICONTROL Use in Filter Options]**, choisissez `Yes`.

1. Cliquez sur **[!UICONTROL Save Attribute]**.

![Attribut de condition Amazon](assets/creating-amazon-condition-attribute.png)

![Icône Suivant](assets/btn-next.png) [**Continuer à ajouter ou vérifier la clé API**](./amazon-verify-api-key.md)
