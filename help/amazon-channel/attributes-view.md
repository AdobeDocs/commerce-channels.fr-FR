---
title: Attributs des listes Amazon
description: Amazon Sales Channel fournit les [!UICONTROL Attributes] pour surveiller la liste des attributs Amazon et Commerce et leur mappage pour la correspondance des produits.
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Attributs des listes Amazon

Le _[!UICONTROL Attributes]_affiche votre liste d’Amazon et [!DNL Commerce] attributs. La liste indique également les attributs qui ont été mappés pour la correspondance des produits. Pour plus d’informations, voir [Gestion des attributs](./managing-attributes.md).

![Vue Attributs](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

Dans la _[!UICONTROL Attributes]_visualisez, vous et vérifiez vos paramètres d’attribut dans le tableau et [créer ou modifier](./creating-attributes.md) un attribut .

## Afficher votre liste d’attributs

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon et consultez votre liste d’attributs.

1. Créez ou modifiez un attribut, selon les besoins :

   - À [create](./creating-attributes.md#create-an-attribute) et définissez les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Create]**.

   - Pour désactiver ou [modifier les paramètres ;](./creating-attributes.md#edit-an-attribute) ou Correspondance de valeurs d’attribut pour l’attribut, cliquez sur **[!UICONTROL Edit]**.

     La modification d’un attribut inclut la modification du mappage d’attributs pour la correspondance des produits.

| Champ | Description |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | Le pays pour l’activité de vente définie dans  **[!DNL Amazon Marketplace]Pays** during [intégration de magasin](./store-integration.md). |
| [!UICONTROL ID] | Valeur d’attribut générique générée par [!DNL Commerce] lors de la création de l’attribut. |
| [!UICONTROL Amazon Attribute Name] | Nom de l’attribut importé à partir d’Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Si elle est mappée, la variable [!DNL Commerce] Attribut affecté à la mise en correspondance avec la propriété _[!UICONTROL Amazon Attribute Name]_pour faire correspondre les produits du catalogue et de la liste. |
| [!UICONTROL Overwrite Magento Values] | Si l’attribut est défini sur `Overwrite Existing Magento Values` Dans les paramètres d’attribut, le tableau affiche `Enabled`. Activé signifie que lorsque les informations de produit mises à jour pour l’attribut sont reçues d’Amazon, les nouvelles informations sont mises à jour (remplacent) les informations correspondantes pour le produit dans votre [!DNL Commerce] catalogue. Cela peut également affecter vos produits répertoriés dans votre [!DNL Commerce] magasins. |
| État | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et mappés à un [!DNL Commerce] attribut. Options : `Enabled` / `Disabled` |
| Action | Indique les options de tâche disponibles pour l’attribut . Options : `Create` / `Edit` |
