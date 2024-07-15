---
title: Attributs des listes Amazon
description: Amazon Sales Channel fournit l’onglet [!UICONTROL Attributes] pour surveiller la liste des attributs Amazon et Commerce et leur mappage pour la correspondance des produits.
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Attributs des listes Amazon

La vue _[!UICONTROL Attributes]_affiche votre liste d’attributs Amazon et [!DNL Commerce]. La liste indique également les attributs qui ont été mappés pour la correspondance des produits. Pour plus d’informations, voir [Gestion des attributs](./managing-attributes.md).

![Vue Attributs](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

Dans la vue _[!UICONTROL Attributes]_, vous et passez en revue vos paramètres d’attribut dans le tableau et [créez ou modifiez](./creating-attributes.md) un attribut.

## Afficher votre liste d’attributs

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon et consultez votre liste d’attributs.

1. Créez ou modifiez un attribut, selon les besoins :

   - Pour [créer](./creating-attributes.md#create-an-attribute) et définir les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Create]**.

   - Pour désactiver ou [modifier les paramètres](./creating-attributes.md#edit-an-attribute) ou les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Edit]**.

     La modification d’un attribut inclut la modification du mappage d’attributs pour la correspondance des produits.

| Champ | Description |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | Le pays pour l’activité de vente définie dans **[!DNL Amazon Marketplace]Country** lors de l’ [intégration de magasin](./store-integration.md). |
| [!UICONTROL ID] | Valeur d’attribut générique générée par [!DNL Commerce] lors de la création de l’attribut. |
| [!UICONTROL Amazon Attribute Name] | Nom de l’attribut importé à partir d’Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | S’il est mappé, l’attribut [!DNL Commerce] attribué à la mise en correspondance avec _[!UICONTROL Amazon Attribute Name]_pour les produits de catalogue et de liste correspondants. |
| [!UICONTROL Overwrite Magento Values] | Si l’attribut est défini sur `Overwrite Existing Magento Values` dans les paramètres d’attribut, le tableau affiche `Enabled`. Activé signifie que lorsque des informations de produit mises à jour pour l’attribut sont reçues d’Amazon, les nouvelles informations sont mises à jour (remplacent) les informations correspondantes pour le produit de votre catalogue [!DNL Commerce]. Elle peut également affecter vos produits répertoriés dans vos magasins [!DNL Commerce]. |
| État | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et mappées à un attribut [!DNL Commerce]. Options : `Enabled` / `Disabled` |
| Action | Indique les options de tâche disponibles pour l’attribut . Options : `Create` / `Edit` |
