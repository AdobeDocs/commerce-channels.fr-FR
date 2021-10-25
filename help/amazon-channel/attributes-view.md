---
title: Attributs
description: Le Sales Channel Amazon fournit la [!UICONTROL Attributes] pour contrôler la liste des attributs Amazon et Commerce et la manière dont ils sont mappés pour la mise en correspondance des produits.
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Attributs

Le _[!UICONTROL Attributes]_affiche votre liste d’Amazon et [!DNL Commerce] attributs. La liste indique également les attributs qui ont été mappés pour la mise en correspondance des produits. Pour plus d’informations, voir [Gérer les attributs](./managing-attributes.md).

![Vue Attributs](assets/amazon-attributes-view.png)

De _[!UICONTROL Attributes]_afficher, vous et examiner vos paramètres d’attribut dans le tableau et [création ou modification](./creating-attributes.md) un attribut.

## Affichage de votre liste d’attributs

1. Sur la _Administrateur_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis passez en revue votre liste d’attributs.

1. Créez ou modifiez un attribut, selon les besoins :

   - À [créer](./creating-attributes.md#create-an-attribute) et définissez les valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Create]**.

   - Pour désactiver ou [modification des paramètres](./creating-attributes.md#edit-an-attribute) ou Valeurs d’attribut correspondantes pour l’attribut, cliquez sur **[!UICONTROL Edit]**.

      La modification d’un attribut comprend la modification du mappage d’attributs pour la correspondance de produit.

| Champ | Description |
|--- |--- |
| [!UICONTROL Country] | Pays pour l&#39;activité de vente définie dans  **[!DNL Amazon Marketplace]Pays** pendant [intégration de magasin](./store-integration.md). |
| [!UICONTROL ID] | Valeur d’attribut générique générée par [!DNL Commerce] lorsque l’attribut est créé. |
| [!UICONTROL Amazon Attribute Name] | Nom de l’attribut importé d’Amazon. |
| [!UICONTROL Product Catalog Attribute Code] | Si elle est mappée, la propriété [!DNL Commerce] Attribut affecté au mappage à _[!UICONTROL Amazon Attribute Name]_pour rechercher des produits de catalogue et de liste correspondants. |
| [!UICONTROL Overwrite Magento Values] | Si l’attribut est défini sur `Overwrite Existing Magento Values` dans les paramètres d’attribut, le tableau affiche `Enabled`. Lorsque cette option est activée, lorsque des informations de produit mises à jour pour l’attribut sont reçues d’Amazon, les nouvelles informations sont mises à jour (remplacent) les informations correspondantes pour le produit dans votre [!DNL Commerce] catalogue. Cela peut également affecter vos produits répertoriés dans votre [!DNL Commerce] magasins. |
| Statut | Indique si les valeurs d’attribut ont été importées dans [!DNL Commerce] et mappé sur un [!DNL Commerce] . Options : `Enabled` / `Disabled` |
| Action | Indique les options de tâche disponibles pour l’attribut. Options : `Create` / `Edit` |
