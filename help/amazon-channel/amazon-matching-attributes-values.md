---
title: Affichage du mappage des attributs Amazon
description: Vérifiez les valeurs de vos attributs de commerce liés afin de synchroniser correctement Commerce et Amazon.
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Affichage du mappage d’attributs Amazon

Lorsque vous mappez des attributs Amazon vers [!DNL Commerce] , le canal de vente Amazon assure le suivi et fournit une liste filtrable de toutes les valeurs Amazon. Utilisez cette page pour vérifier les valeurs de votre lien [!DNL Commerce] attributs synchronisation correcte entre [!DNL Commerce] et Amazon. Vous pouvez consulter les valeurs synchronisées pour l’attribut Amazon lié ou non à un [!DNL Commerce] . Pour créer ou modifier vos attributs Amazon, voir [Création et modification d’attributs](./creating-attributes.md).

Le _Valeur Amazon_ diffère selon le type d’attribut et l’attribut Amazon que vous affichez. Par exemple, une valeur Amazon répertoriée pour `Label` serait une valeur de texte tandis que `AmazonListPrice` serait un montant numérique. L’état indique si la valeur Amazon a été importée.

## Affichage des valeurs d’attribut

1. Sur la _[!UICONTROL Admin]_barre latérale, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur l’une des options suivantes : **[!UICONTROL Create]** ou **[!UICONTROL Edit]** dans la _[!UICONTROL Action]_colonne.

1. Cliquez sur le bouton **[!UICONTROL Matching Attribute Values]** .

   Annonces ayant un [!DNL Commerce] le produit de catalogue affiche une valeur liée dans la propriété _SKU de produit Magento_ colonne. Cliquez sur un lien pour ouvrir la page de détails du produit du catalogue correspondant. Les modifications apportées aux attributs Amazon sur la page de détails du produit ne sont pas synchronisées avec le canal de vente Amazon.

>[!TIP]
>Pour modifier ou affecter le mappage d’une annonce à un produit de catalogue, voir [Mettre à jour les informations requises](./amazon-manually-update-incomplete-listing.md).

![Affichage des valeurs d’attribut](assets/amazon-managing-attribute-values.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Region] | La région pour l&#39;activité de vente définie dans **[!DNL Amazon Marketplace]Pays** lors de l’intégration du magasin. |
| [!UICONTROL Magento Product SKU] | Indique que [!DNL Commerce] produits synchronisés avec le magasin Amazon. La valeur est un ID de produit attribué par [!DNL Commerce] et lié à un produit dans le catalogue. Pour ouvrir le produit dans [!DNL Commerce], cliquez sur le lien. |
| [!UICONTROL ASIN] | Indique l’identificateur unique alphanumérique de 10 caractères ASIN (Amazon Standard Identification Number) attribué au produit par Amazon pour l’identification du produit. |
| [!UICONTROL Amazon Value] | Indique la valeur de l’attribut sélectionné. La valeur Amazon varie en fonction du type d’attribut et de l’attribut Amazon que vous affichez. Par exemple, une valeur Amazon répertoriée pour `Label` serait une valeur de texte tandis que `AmazonListPrice` serait un montant numérique. L’état indique si la valeur Amazon a été importée. |
| [!UICONTROL Status] | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et lié à un [!DNL Commerce] . Options : `Not Imported` / `Imported` |
