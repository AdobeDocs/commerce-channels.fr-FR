---
title: Création et modification d’attributs
description: Le Sales Channel Amazon fournit la vue Attributs pour vous aider à passer en revue les attributs Amazon actuels et les attributs Commerce liés.
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Création et modification d’attributs

Créer ou mettre à jour [!DNL Commerce] comme vous vendez via Amazon et mettez à jour vos magasins. Passer en revue les attributs Amazon actuels et les liens [!DNL Commerce] via le [_[!UICONTROL Attributes]_affichage](./attributes-view.md) de la page d&#39;accueil du canal de vente Amazon. Le_[!UICONTROL Action]_ affiche les actions disponibles pour l’attribut. Vous pouvez créer et mapper un nouveau [!DNL Commerce] pour un attribut Amazon non lié ou vous pouvez modifier un attribut existant [!DNL Commerce] et son mappage vers un attribut Amazon.

Lorsque vous créez et mettez à jour des attributs, vous pouvez vérifier les valeurs d’attribut pour [!DNL Commerce] et les produits Amazon. Ces valeurs peuvent différer si vous ne synchronisez pas et n’importez pas les valeurs d’Amazon. Pour vérifier les valeurs Amazon pour ces attributs, voir [Révision du mappage des attributs Amazon](./amazon-matching-attributes-values.md). Si vous souhaitez modifier ces valeurs, vous pouvez [modification ou création d’un mappage](./amazon-manually-update-incomplete-listing.md) entre Amazon et [!DNL Commerce].

## Création d’un attribut {#create-an-attribute}

Ces étapes créent un [!DNL Commerce] et mappez-le à un attribut Amazon. Selon les configurations, les valeurs peuvent commencer à synchroniser entre les catalogues.

1. Sur la _Administrateur_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Create Attribute]** dans la _[!UICONTROL Action]_colonne.

1. Pour activer la synchronisation des valeurs Amazon avec le lien [!DNL Commerce] attribut, set **[!UICONTROL Is Active]** à `Yes`.

   Lorsque la valeur est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Choisir `Create New Magento Attribute` pour **[!UICONTROL Select Magento Product Attribute]**.

   L’attribut est mappé sur le **[!UICONTROL Amazon Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Name]**.

1. Saisissez un **[!UICONTROL Magento Product Attribute Code]**.

   Cette valeur doit être toute en minuscules sans espaces.

1. Pour **[!UICONTROL Attribute Set Ids]**, sélectionnez un jeu d’attributs à affecter.

   En règle générale, les attributs font partie d’un ensemble d’attributs, tel qu’un ensemble de couleurs ayant des attributs pour le bleu, le vert, le jaune et le rouge.

1. Pour **[!UICONTROL Type]**, sélectionnez le type de la valeur d’attribut, par exemple le texte et les nombres.

   Cette option affecte la valeur autorisée pour l’attribut.

1. Pour **[!UICONTROL Use for Promo Rule Conditions]**, définissez sur `Yes` pour permettre à l’attribut d’être disponible pour un paramètre dans vos conditions promotionnelles.

1. Pour **[!UICONTROL Used in Search]**, définissez sur `Yes` si l’attribut et la valeur peuvent être utilisés dans les recherches de produit.

1. Pour **[!UICONTROL Comparable on Storefront]**, définissez sur `Yes` si la valeur d’attribut peut être utilisée dans Amazon en  la fonctionnalité &quot;Comparer par&quot;.

1. Sélectionnez l’option [!DNL Commerce] [étendue](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} pour l&#39;attribut, puis sélectionnez une ou plusieurs vues de magasin dans lesquelles importer les valeurs Amazon.

   Si la portée est définie sur `Global`, le _[!UICONTROL Store View]_ne peut pas être modifié une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes les vues de votre magasin Amazon. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute Settings]**.

Après l’enregistrement, vous pouvez modifier l’attribut pour vérifier les paramètres et les Amazon correspondants et [!DNL Commerce] pour l’attribut. Vous pouvez également indiquer si les valeurs Amazon doivent être remplacées. [!DNL Commerce] valeurs.

![créer des paramètres d’attribut](assets/amazon-attribute-settings-create.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronisé activement entre Amazon et [!DNL Commerce]. Définir sur `Yes` pour garantir les valeurs d’attribut d’Amazon et [!DNL Commerce] reste synchronisé pour l’attribut sélectionné. |
| Sélectionner un attribut de produit Magento | Indique l’attribut sélectionné que vous souhaitez lier au nom de l’attribut Amazon répertorié. Lors de la création d’un attribut, sélectionnez `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon que vous avez choisi. L’attribut sélectionné est lié à cet attribut Amazon. Vous ne pouvez pas modifier cette valeur via [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Indique le nom d’attribut ou &quot;label&quot;. |
| [!UICONTROL Magento Product Attribute Code] | Indique le code d’attribut, le tout en caractères minuscules sans espaces. |
| [!UICONTROL Attribute Set Ids] | Indique le jeu d’attributs auquel affecter l’attribut. Les attributs ont tendance à faire partie d’un ensemble d’attributs, par exemple un ensemble de couleurs ayant des attributs pour le bleu, le vert, le jaune et le rouge. |
| [!UICONTROL Type] | Indique le type de valeur de la valeur d’attribut, tel que le texte et les nombres. La sélection affecte la valeur autorisée pour l’attribut. |
| [!UICONTROL Use for Promo Rule Conditions] | Basculer vers `Yes` pour permettre à l’attribut d’être disponible pour un paramètre dans vos conditions promotionnelles. |
| [!UICONTROL Used in Search] | Indique si l’attribut et la valeur peuvent être utilisés dans les recherches de produit. |
| [!UICONTROL Comparable on Storefront] | Indique si la valeur de l’attribut peut être utilisée dans l’Amazon de la fonctionnalité &quot;Comparer par&quot; de. |
| [!UICONTROL Magento Product Attribute Scope] | Indique que [étendue](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} pour l&#39;attribut. Options : Vue Global/Store<br>Lorsque la valeur est définie sur `Global`, la vue Boutique ne peut pas être modifiée une fois l’attribut créé. |
| [!UICONTROL Store Views (to import values into to)] | S’affiche uniquement lorsque la portée est définie sur `Store View`. Sélectionnez l’option [vue magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} vers lequel les valeurs d&#39;attribut Amazon sont synchronisées. Choix `All Store Views (Global)` met à jour la valeur dans l’ensemble [!DNL Commerce] vues de magasin. |

## Modification d’un attribut {#edit-an-attribute}

1. Sur la _Administrateur_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Cliquez sur **[!UICONTROL Attributes]** dans le menu de gauche, recherchez un attribut Amazon, puis cliquez sur **[!UICONTROL Edit]** dans la _[!UICONTROL Action]_colonne.

1. Pour activer ou désactiver la synchronisation des valeurs Amazon avec le lien [!DNL Commerce] attribut, set **Est actif** à `Yes` ou `No`.

   Lorsque la valeur est définie sur `Yes`, les valeurs sont synchronisées en fonction de votre configuration.

1. Pour **[!UICONTROL Select Magento Product Attribute]**, vérifiez ou mettez à jour l’attribut à mapper avec le **[!UICONTROL Amazon Attribute Name]**.

1. Indiquez si vous souhaitez que la valeur d’attribut Amazon entrante remplace la valeur d’attribut existante.

   Par exemple, vous pouvez ne pas vouloir remplacer les prix d’Amazon dans [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Conserve la valeur, en conservant des valeurs différentes pour votre [!DNL Commerce] et les magasins Amazon.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Remplace la valeur dans la propriété [!DNL Commerce] catalogue de produits avec la valeur Amazon entrante.

1. Si cette option est disponible pour modification, choisissez une ou plusieurs options **[!UICONTROL Store Views (to import Amazon values into)]**.

   Si l’attribut a été créé avec un `Global` , _Mode Boutique_ ne peut pas être modifié une fois l’attribut créé.

   Si vous choisissez `All Store Views (Global)`, il synchronise et enregistre les valeurs dans toutes les vues du magasin. Vous pouvez uniquement synchroniser les valeurs avec des vues de magasin spécifiques.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute Settings]**.

![modifier les paramètres d’attribut](assets/amazon-attribute-settings-edit.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Is Active] | Indique si cet attribut est actif et synchronisé activement entre Amazon et [!DNL Commerce]. Définir sur `Yes` pour garantir les valeurs d’attribut d’Amazon et [!DNL Commerce] reste synchronisé pour l’attribut sélectionné. |
| [!UICONTROL Select Magento Product Attribute] | Indique le [!DNL Commerce] que vous souhaitez lier au nom d’attribut Amazon répertorié. Si vous souhaitez modifier le lien [!DNL Commerce] , choisissez un attribut différent dans la liste déroulante. Les valeurs sont synchronisées en fonction des configurations. |
| [!UICONTROL Amazon Attribute Name] | Affiche le nom de l’attribut Amazon tel que défini dans [!DNL Amazon Seller Central]. La [!DNL Commerce] est lié à cet attribut Amazon. Vous ne pouvez pas modifier cette valeur via [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Indique si les valeurs d’attribut Amazon remplacent les valeurs existantes [!DNL Commerce] valeurs, affectant tous les produits avec cette [!DNL Commerce] .<ul><li>**Ne pas écraser les valeurs de Magento existantes** - (Par défaut) Conserve la [!DNL Commerce] valeur, en conservant différentes valeurs pour [!DNL Commerce] et les magasins Amazon.</li><li>**Remplacer les valeurs de Magento existantes** - Enregistre la valeur Amazon sur la propriété [!DNL Commerce] dans la propriété [!DNL Commerce] catalogue de produits.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | N’apparaît pas lors de la modification d’un attribut si l’attribut a été créé avec l’attribut `Global` portée. Indique que [!DNL Commerce] [étendue](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;} a été créé et défini sur `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Sélectionnez votre [!DNL Commerce] [vue magasin](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;} vers lequel synchroniser les valeurs d&#39;attribut Amazon. Choix `All Store Views (Global)` met à jour la valeur dans toutes les vues de magasin. |
