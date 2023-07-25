---
title: Création et modification d’attributs pour le canal de vente Amazon
description: Amazon Sales Channel fournit la vue Attributs pour vous aider à passer en revue les attributs Amazon actuels et les attributs Commerce liés.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 0%

---

# Création et modification d’attributs

Créer ou mettre à jour [!DNL Commerce] attributs tels que vous vendez par le biais d’Amazon et mettez à jour vos magasins. Vérifier les attributs Amazon actuels et liés [!DNL Commerce] Attributs par l’intermédiaire de la variable [_[!UICONTROL Attributes]_view](./attributes-view.md) de la page d’accueil du canal de vente Amazon. Le_[!UICONTROL Action]_ affiche les actions disponibles pour l’attribut . Vous pouvez créer et mapper une nouvelle [!DNL Commerce] pour un attribut Amazon non lié, ou vous pouvez modifier un attribut existant [!DNL Commerce] et son mappage à un attribut Amazon.

Lorsque vous créez et mettez à jour des attributs, vous pouvez vérifier les valeurs d’attribut pour [!DNL Commerce] et les produits Amazon. Ces valeurs peuvent différer si vous ne synchronisez pas et n’importez pas de valeurs à partir d’Amazon. Pour consulter les valeurs Amazon de ces attributs, voir [Vérification du mappage des attributs Amazon](./amazon-matching-attributes-values.md). Si vous souhaitez modifier ces valeurs, vous pouvez [modification ou création d’un mappage](./amazon-manually-update-incomplete-listing.md) entre Amazon et [!DNL Commerce].

## Création d’un attribut {#create-an-attribute}

Ces étapes créent une [!DNL Commerce] et le mapper à un attribut Amazon. Selon les configurations, les valeurs peuvent commencer à synchroniser les catalogues.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Create Attribute]** dans le _[!UICONTROL Action]_colonne .

1. Pour permettre la synchronisation des valeurs Amazon avec le lien [!DNL Commerce] attribute, set **[!UICONTROL Is Active]** to `Yes`.

   Lorsque la variable est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Choisir `Create New Magento Attribute` pour **[!UICONTROL Select Magento Product Attribute]**.

   L’attribut correspond à la valeur choisie pour **[!UICONTROL Amazon Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Code]**.

   Cette valeur doit être entièrement en minuscules, sans espaces.

1. Pour **[!UICONTROL Attribute Set Ids]**, choisissez un jeu d’attributs à affecter.

   En règle générale, les attributs font partie d’un jeu d’attributs, tel qu’un jeu de couleurs avec des attributs pour le bleu, le vert, le jaune et le rouge.

1. Pour **[!UICONTROL Type]**, choisissez le type de la valeur d’attribut, comme le texte et les nombres.

   Cette option affecte la valeur autorisée pour l’attribut .

1. Pour **[!UICONTROL Use for Promo Rule Conditions]**, définissez sur `Yes` pour permettre à l’attribut d’être disponible pour un paramètre dans vos conditions promotionnelles.

1. Pour **[!UICONTROL Used in Search]**, définissez sur `Yes` si l’attribut et la valeur peuvent être utilisés dans les recherches de produits.

1. Pour **[!UICONTROL Comparable on Storefront]**, définissez sur `Yes` si la valeur d’attribut peut être utilisée dans la fonctionnalité &quot;Comparer par&quot; d’Amazon.

1. Choisissez la [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) pour l’attribut , puis sélectionnez une ou plusieurs vues de magasin dans lesquelles importer les valeurs Amazon.

   Si la portée est définie sur `Global`, la variable _[!UICONTROL Store View]_ne peut pas être modifié une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes vos vues de magasin Amazon. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute Settings]**.

Après l’enregistrement, vous pouvez modifier l’attribut pour vérifier les paramètres et faire correspondre Amazon et [!DNL Commerce] pour l’attribut . Vous pouvez également indiquer si les valeurs Amazon doivent être remplacées. [!DNL Commerce] valeurs.

![créer des paramètres d’attribut](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Champ | Description |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronise activement entre Amazon et [!DNL Commerce]. Définissez sur . `Yes` pour garantir les valeurs d’attribut d’Amazon et [!DNL Commerce] rester synchronisé pour l’attribut sélectionné. |
| Sélectionner un attribut de produit Magento | Indique l’attribut sélectionné que vous souhaitez lier au nom d’attribut Amazon répertorié. Lors de la création d’un attribut, choisissez `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon que vous avez choisi. L’attribut sélectionné est lié à cet attribut Amazon. Vous ne pouvez pas modifier cette valeur via [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indique le nom de l’attribut ou &quot;label&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indique le code d’attribut, le tout en minuscules, sans espaces. |
| [!UICONTROL Attribute Set Ids] | Indique le jeu d’attributs auquel attribuer l’attribut. Les attributs font généralement partie d’un jeu d’attributs, comme un jeu de couleurs avec des attributs pour le bleu, le vert, le jaune et le rouge. |
| [!UICONTROL Type] | Indique le type de valeur de la valeur d’attribut, comme le texte et les nombres. La sélection affecte la valeur autorisée pour l’attribut. |
| [!UICONTROL Use for Promo Rule Conditions] | Basculer vers `Yes` pour permettre à l’attribut d’être disponible pour un paramètre dans vos conditions promotionnelles. |
| [!UICONTROL Used in Search] | Indique si l’attribut et la valeur peuvent être utilisés dans les recherches de produits. |
| [!UICONTROL Comparable on Storefront] | Indique si la valeur d’attribut peut être utilisée dans la fonctionnalité &quot;Comparer par&quot; d’Amazon. |
| [!UICONTROL Magento Product Attribute Scope] | Indique la variable [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) pour l’attribut . Options : Vue globale/magasin<br>Lorsque la variable est définie sur `Global`, il n’est pas possible de modifier la vue de magasin une fois l’attribut créé. |
| [!UICONTROL Store Views (to import values into to)] | S’affiche uniquement lorsque la portée est définie sur `Store View`. Choisissez la [vue de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) à laquelle les valeurs d’attribut Amazon sont synchronisées. Choix `All Store Views (Global)` met à jour la valeur dans tous les [!DNL Commerce] vues des magasins. |

## Modification d’un attribut {#edit-an-attribute}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Pour activer ou désactiver la synchronisation des valeurs Amazon avec le lien [!DNL Commerce] attribute, set **Est Principal** to `Yes` ou `No`.

   Lorsque la variable est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Pour **[!UICONTROL Select Magento Product Attribute]**, vérifiez ou mettez à jour l’attribut pour le mappage au choix. **[!UICONTROL Amazon Attribute Name]**.

1. Indiquez si vous souhaitez que la valeur d’attribut Amazon entrante remplace la valeur d’attribut existante.

   Par exemple, vous pouvez ne pas remplacer les prix d’Amazon dans [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserve la valeur, en conservant des valeurs différentes pour votre [!DNL Commerce] et les magasins Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Remplace la valeur de la variable [!DNL Commerce] catalogue de produits avec la valeur Amazon entrante.

1. Si vous pouvez le modifier, choisissez une ou plusieurs **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si l’attribut a été créé avec une `Global` la portée, _Affichage en magasin_ ne peut pas être modifié une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes les vues de magasin. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute Settings]**.

![modification des paramètres d’attribut](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Champ | Description |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronise activement entre Amazon et [!DNL Commerce]. Définissez sur . `Yes` pour garantir les valeurs d’attribut d’Amazon et [!DNL Commerce] rester synchronisé pour l’attribut sélectionné. |
| [!UICONTROL Select Magento Product Attribute] | Indique le [!DNL Commerce] que vous souhaitez lier au nom d’attribut Amazon répertorié. Si vous souhaitez modifier le lien [!DNL Commerce] , choisissez un autre attribut dans la liste déroulante. Les valeurs sont synchronisées selon les configurations. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon tel que défini dans [!DNL Amazon Seller Central]. Le [!DNL Commerce] des liens vers cet attribut Amazon. Vous ne pouvez pas modifier cette valeur via [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indique si les valeurs d’attribut Amazon remplacent les valeurs existantes. [!DNL Commerce] , affectant tous les produits avec cette variable [!DNL Commerce] attribut.<ul><li>**Ne pas remplacer les valeurs de Magento existantes** - (Par défaut) conserve la variable [!DNL Commerce] , en conservant différentes valeurs pour [!DNL Commerce] et les magasins Amazon.</li><li>**Remplacer les valeurs de Magento existantes** - Enregistre la valeur Amazon au-dessus de la variable [!DNL Commerce] dans la variable [!DNL Commerce] catalogue de produits.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | N’apparaît pas lors de la modification d’un attribut si l’attribut a été créé avec la propriété `Global` portée. Indique que la variable [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) a été créé et défini sur `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Choisissez votre [!DNL Commerce] [vue de magasin](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) à laquelle synchroniser les valeurs d’attribut Amazon. Choix `All Store Views (Global)` met à jour la valeur pour toutes les vues de magasin. |
