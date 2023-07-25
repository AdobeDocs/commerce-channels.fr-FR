---
title: Affichage du mappage des attributs Amazon
description: Vérifiez les valeurs de vos attributs Commerce liés pour une synchronisation correcte entre Commerce et Amazon.
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Affichage du mappage des attributs Amazon

Lorsque vous mappez des attributs Amazon avec [!DNL Commerce] , le canal de vente Amazon effectue le suivi et fournit une liste filtrable de toutes les valeurs Amazon. Utilisez cette page pour vérifier les valeurs de votre lien [!DNL Commerce] les attributs correctement synchronisés entre [!DNL Commerce] et Amazon. Vous pouvez vérifier les valeurs synchronisées pour un attribut Amazon lié ou non à un [!DNL Commerce] attribut. Pour créer ou modifier vos attributs Amazon, voir [Création et modification d’attributs](./creating-attributes.md).

Le _Valeur Amazon_ varie selon le type d’attribut et l’attribut Amazon que vous affichez. Par exemple, une valeur Amazon répertoriée pour `Label` serait une valeur de texte tandis que `AmazonListPrice` serait un montant numérique. Le statut indique si la valeur Amazon a été importée.

## Affichage des valeurs d’attribut

1. Sur le _[!UICONTROL Admin]_barre latérale, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Create]** ou **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Cliquez sur le bouton **[!UICONTROL Matching Attribute Values]** .

   Les listes qui ont une [!DNL Commerce] le produit catalogue affiche une valeur liée dans la variable _[!UICONTROL Magento Product SKU]_colonne . Cliquez sur un lien pour ouvrir la page des détails du produit du catalogue correspondante. Les modifications apportées aux attributs Amazon sur la page des détails du produit ne sont pas synchronisées avec le canal de vente Amazon.

>[!TIP]
>Pour modifier ou affecter le mappage d’une liste à un produit de catalogue, voir [Mettre à jour les informations requises](./amazon-manually-update-incomplete-listing.md).

![Affichage des valeurs d’attribut](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Champ | Description |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | La région de l’activité de vente définie dans **[!DNL Amazon Marketplace]Pays** lors de l’intégration du magasin. |
| [!UICONTROL Magento Product SKU] | Indique la variable [!DNL Commerce] produits synchronisés avec la boutique Amazon. La valeur est un ID de produit attribué par [!DNL Commerce] et liés à un produit dans le catalogue. Pour ouvrir le produit dans [!DNL Commerce], cliquez sur le lien. |
| [!UICONTROL ASIN] | Indique l’identificateur unique alphanumérique de 10 caractères (ASIN) d’Amazon Standard Identification Number (Numéro d’identification standard d’) attribué au produit par Amazon pour l’identification du produit. |
| [!UICONTROL Amazon Value] | Indique la valeur de l’attribut sélectionné. La valeur Amazon varie en fonction du type d’attribut et de l’attribut Amazon que vous affichez. Par exemple, une valeur Amazon répertoriée pour `Label` serait une valeur de texte tandis que `AmazonListPrice` serait un montant numérique. Le statut indique si la valeur Amazon a été importée. |
| [!UICONTROL Status] | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et liés à un [!DNL Commerce] attribut. Options : `Not Imported` / `Imported` |
