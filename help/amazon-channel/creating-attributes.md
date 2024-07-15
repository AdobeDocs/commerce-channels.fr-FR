---
title: Création et modification d’attributs pour le canal de vente Amazon
description: Amazon Sales Channel fournit la vue Attributs pour vous aider à passer en revue les attributs Amazon actuels et les attributs Commerce liés.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Création et modification d’attributs

Créez ou mettez à jour des attributs [!DNL Commerce] au fur et à mesure que vous vendez via Amazon et mettez à jour vos magasins. Passez en revue les attributs Amazon actuels et les attributs [!DNL Commerce] liés via la [_[!UICONTROL Attributes]_vue](./attributes-view.md) de la page d’accueil du canal de vente Amazon. La colonne_[!UICONTROL Action]_ affiche les actions disponibles pour l’attribut . Vous pouvez soit créer et mapper un nouvel attribut [!DNL Commerce] pour un attribut Amazon non lié, soit modifier un attribut [!DNL Commerce] existant et son mappage à un attribut Amazon.

Lorsque vous créez et mettez à jour des attributs, vous pouvez vérifier les valeurs d’attribut pour les produits [!DNL Commerce] et Amazon. Ces valeurs peuvent différer si vous ne synchronisez pas et n’importez pas de valeurs à partir d’Amazon. Pour consulter les valeurs Amazon de ces attributs, voir [Vérification du mappage des attributs Amazon](./amazon-matching-attributes-values.md). Si vous souhaitez modifier ces valeurs, vous pouvez [modifier ou créer un mappage](./amazon-manually-update-incomplete-listing.md) entre Amazon et [!DNL Commerce].

## Création d’un attribut {#create-an-attribute}

Ces étapes créent un attribut [!DNL Commerce] et le mappent à un attribut Amazon. Selon les configurations, les valeurs peuvent commencer à synchroniser les catalogues.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Create Attribute]** dans la colonne _[!UICONTROL Action]_.

1. Pour activer la synchronisation des valeurs Amazon avec l’attribut [!DNL Commerce] lié, définissez **[!UICONTROL Is Active]** sur `Yes`.

   Lorsque la valeur est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Sélectionnez `Create New Magento Attribute` pour **[!UICONTROL Select Magento Product Attribute]**.

   L’attribut correspond au choix pour **[!UICONTROL Amazon Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Code]**.

   Cette valeur doit être entièrement en minuscules, sans espaces.

1. Pour **[!UICONTROL Attribute Set Ids]**, choisissez un jeu d’attributs à affecter.

   En règle générale, les attributs font partie d’un jeu d’attributs, tel qu’un jeu de couleurs avec des attributs pour le bleu, le vert, le jaune et le rouge.

1. Pour **[!UICONTROL Type]**, choisissez le type de la valeur d’attribut, comme le texte et les nombres.

   Cette option affecte la valeur autorisée pour l’attribut .

1. Pour **[!UICONTROL Use for Promo Rule Conditions]**, définissez sur `Yes` pour autoriser l’attribut à être disponible pour un paramètre dans vos conditions promotionnelles.

1. Pour **[!UICONTROL Used in Search]**, définissez sur `Yes` si l’attribut et la valeur peuvent être utilisés dans les recherches de produits.

1. Pour **[!UICONTROL Comparable on Storefront]**, définissez sur `Yes` si la valeur d’attribut peut être utilisée dans la fonctionnalité &quot;Comparer par&quot; d’Amazon.

1. Sélectionnez l’attribut [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings), puis une ou plusieurs vues de magasin pour importer les valeurs Amazon dans.

   Si la portée est définie sur `Global`, _[!UICONTROL Store View]_ne peut pas être modifié une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes vos vues de magasin Amazon. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute Settings]**.

Après l’enregistrement, vous pouvez modifier l’attribut pour vérifier les paramètres et faire correspondre les valeurs Amazon et [!DNL Commerce] pour l’attribut. Vous pouvez également indiquer si les valeurs Amazon doivent remplacer les valeurs [!DNL Commerce].

![créer des paramètres d’attribut](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Champ | Description |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronise activement entre Amazon et [!DNL Commerce]. Définissez cette variable sur `Yes` pour vous assurer que les valeurs d’attribut d’Amazon et de [!DNL Commerce] restent synchronisées pour l’attribut sélectionné. |
| Sélectionner un attribut de produit Magento | Indique l’attribut sélectionné que vous souhaitez lier au nom d’attribut Amazon répertorié. Lors de la création d’un attribut, choisissez `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon que vous avez choisi. L’attribut sélectionné est lié à cet attribut Amazon. Vous ne pouvez pas modifier cette valeur par l’intermédiaire de [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indique le nom de l’attribut ou &quot;label&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indique le code d’attribut, le tout en minuscules, sans espaces. |
| [!UICONTROL Attribute Set Ids] | Indique le jeu d’attributs auquel attribuer l’attribut. Les attributs font généralement partie d’un jeu d’attributs, comme un jeu de couleurs avec des attributs pour le bleu, le vert, le jaune et le rouge. |
| [!UICONTROL Type] | Indique le type de valeur de la valeur d’attribut, comme le texte et les nombres. La sélection affecte la valeur autorisée pour l’attribut. |
| [!UICONTROL Use for Promo Rule Conditions] | Passez à `Yes` pour que l’attribut soit disponible pour un paramètre dans vos conditions promotionnelles. |
| [!UICONTROL Used in Search] | Indique si l’attribut et la valeur peuvent être utilisés dans les recherches de produits. |
| [!UICONTROL Comparable on Storefront] | Indique si la valeur d’attribut peut être utilisée dans la fonctionnalité &quot;Comparer par&quot; d’Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indique la [portée](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) pour l’attribut. Options : vue globale/magasin<br>Lorsqu’elle est définie sur `Global`, la vue magasin ne peut pas être modifiée une fois l’attribut créé. |
| [!UICONTROL Store Views (to import values into to)] | S’affiche uniquement lorsque la portée est définie sur `Store View`. Sélectionnez la [vue de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) vers laquelle les valeurs d’attribut Amazon sont synchronisées. Le choix de `All Store Views (Global)` met à jour la valeur sur toutes les [!DNL Commerce] vues de magasin. |

## Modification d’un attribut {#edit-an-attribute}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Pour activer ou désactiver la synchronisation des valeurs Amazon avec l’attribut [!DNL Commerce] lié, définissez **Is Active** sur `Yes` ou `No`.

   Lorsque la valeur est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Pour **[!UICONTROL Select Magento Product Attribute]**, vérifiez ou mettez à jour l’attribut pour le mappage sur le **[!UICONTROL Amazon Attribute Name]** sélectionné.

1. Indiquez si vous souhaitez que la valeur d’attribut Amazon entrante remplace la valeur d’attribut existante.

   Par exemple, vous pouvez ne pas remplacer les prix d’Amazon par [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserve la valeur, en conservant des valeurs différentes pour vos magasins [!DNL Commerce] et Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Remplace la valeur du catalogue de produits [!DNL Commerce] par la valeur Amazon entrante.

1. Si vous pouvez le modifier, choisissez un ou plusieurs **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si l’attribut a été créé avec une portée `Global`, la _vue de magasin_ ne peut pas être modifiée une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes les vues de magasin. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute Settings]**.

![Modifier les paramètres d’attribut](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Champ | Description |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronise activement entre Amazon et [!DNL Commerce]. Définissez cette variable sur `Yes` pour vous assurer que les valeurs d’attribut d’Amazon et de [!DNL Commerce] restent synchronisées pour l’attribut sélectionné. |
| [!UICONTROL Select Magento Product Attribute] | Indique l’attribut [!DNL Commerce] sélectionné à lier au nom d’attribut Amazon répertorié. Si vous souhaitez modifier l’attribut [!DNL Commerce] lié, choisissez un autre attribut dans la liste déroulante. Les valeurs sont synchronisées selon les configurations. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon tel que défini dans [!DNL Amazon Seller Central]. L’attribut [!DNL Commerce] sélectionné est lié à cet attribut Amazon. Vous ne pouvez pas modifier cette valeur par l’intermédiaire de [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indique si les valeurs d’attribut Amazon remplacent les valeurs [!DNL Commerce] existantes, ce qui affecte tous les produits avec cet attribut [!DNL Commerce].<ul><li>**Ne pas remplacer les valeurs de Magento existantes** - (par défaut) Conserve la valeur [!DNL Commerce], en conservant différentes valeurs pour les magasins [!DNL Commerce] et Amazon.</li><li>**Remplacer les valeurs de Magento existantes** - Enregistre la valeur Amazon sur la valeur [!DNL Commerce] dans le catalogue de produits [!DNL Commerce].</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | N’apparaît pas lors de la modification d’un attribut si l’attribut a été créé avec la portée `Global`. Indique que la [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) a été créée et définie sur `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Sélectionnez la [!DNL Commerce] [vue de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) vers laquelle synchroniser les valeurs d’attribut Amazon. Le choix de `All Store Views (Global)` met à jour la valeur sur toutes les vues de magasin. |
