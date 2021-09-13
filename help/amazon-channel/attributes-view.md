---
title: Attributs
description: Amazon Sales Channel fournit l’onglet [!UICONTROL Attributes] pour surveiller la liste des attributs Amazon et Commerce et leur mappage pour la correspondance des produits.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Attributs

La vue _[!UICONTROL Attributes]_affiche votre liste d’attributs Amazon et [!DNL Commerce]. La liste indique également les attributs qui ont été mappés pour la correspondance des produits. Pour plus d’informations, voir [Gestion des attributs](./managing-attributes.md).

![Vue Attributs](assets/amazon-attributes-view.png)

Dans la vue _[!UICONTROL Attributes]_, vous et passez en revue vos paramètres d’attribut dans le tableau et [créez ou modifiez ](./creating-attributes.md) un attribut.

## Afficher votre liste d’attributs

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon et consultez votre liste d’attributs.

1. Créez ou modifiez un attribut, selon les besoins :

   - Pour [créer](./creating-attributes.md#create-an-attribute) et définir les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Create]**.

   - Pour désactiver ou [modifier les paramètres](./creating-attributes.md#edit-an-attribute) ou les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Edit]**.

      La modification d’un attribut inclut la modification du mappage d’attributs pour la correspondance des produits.

| Champ | Description |
|--- |--- |
| [!UICONTROL Country] | Pays pour l’activité de vente définie dans **[!DNL Amazon Marketplace]Pays** au cours de l’[intégration de magasin](./store-integration.md). |
| [!UICONTROL ID] | Valeur d’attribut générique générée par [!DNL Commerce] lors de la création de l’attribut. |
| [!UICONTROL Amazon Attribute Name] | Nom de l’attribut importé à partir d’Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | S’il est mappé, l’attribut [!DNL Commerce] attribué à la correspondance avec _[!UICONTROL Amazon Attribute Name]_pour les produits de catalogue et de liste correspondants. |
| [!UICONTROL Overwrite Magento Values] | Si l’attribut est défini sur `Overwrite Existing Magento Values` dans les paramètres d’attribut, le tableau affiche `Enabled`. L’option activée signifie que lorsque des informations de produit mises à jour pour l’attribut sont reçues d’Amazon, les nouvelles informations sont mises à jour (remplacent) les informations correspondantes pour le produit dans votre catalogue [!DNL Commerce]. Elle peut également affecter vos produits répertoriés dans vos [!DNL Commerce] magasins. |
| État | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et mappées à un attribut [!DNL Commerce]. Options : `Enabled` / `Disabled` |
| Action | Indique les options de tâche disponibles pour l’attribut . Options : `Create` / `Edit` |
