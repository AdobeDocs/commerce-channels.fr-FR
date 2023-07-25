---
title: Canal de vente Amazon - [!UICONTROL Listing Price]
description: Utilisez les paramètres de prix d’énumération pour déterminer la source de prix et la valeur de prix de base (par défaut) de vos listes Amazon.
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] font partie des paramètres de liste des magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord de la boutique](./amazon-store-dashboard.md).

Ces paramètres définissent les [!DNL Commerce] l’attribut price à utiliser comme source de prix, qui est la valeur de prix de base (par défaut) de vos listes Amazon. Ces paramètres sont utilisés par vos [règles de tarification](./pricing-rule-general-settings.md) pour ajuster automatiquement le prix de votre offre Amazon par rapport à la valeur définie pour _[!UICONTROL Magento Price Source]_.

Vous pouvez configurer vos [portée des prix](./price-scope.md) comme global ou site web. Si la portée de votre tarification est définie sur `Global`, il existe une source de prix unique pour tous vos magasins/sites web. Si la portée de votre tarification est définie sur `Website`, la source de prix utilise une logique de secours du prix du site web (le cas échéant) suivie du prix par défaut (global).

Si une règle de liste est définie pour s’appliquer à plusieurs sites Web, l’ordre dans lequel le prix du site Web est utilisé est déterminé par le paramètre de priorité du site Web défini dans la variable [règle de liste](./listing-rules.md). Ces règles vous permettent de définir le prix des produits dans votre catalogue. Pour savoir si vous utilisez la fourchette de prix du site web, reportez-vous à la section [Portée du prix du catalogue](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

Les options répertoriées dans _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_, et _[!UICONTROL Strike Through Price (MSRP)]_incluez les attributs de tarification configurés. Les attributs de prix sont [!DNL Commerce] Attributs de produit avec la valeur Type d’entrée du catalogue pour le propriétaire du magasin définie sur `Price`. Voir [Types d’entrée d’attribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## Configuration des paramètres de prix d’énumération {#configure-listing-price-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord de la boutique.

1. Développez l’objet _[!UICONTROL Listing Price]_.

1. Pour **[!UICONTROL Magento Price Source]** (obligatoire), choisissez une option.

   La valeur par défaut est `Price`. Ce paramètre détermine la source de prix utilisée pour vos listes Amazon. Si vous créez [règles de tarification](./pricing-products.md), les règles sont appliquées à la valeur définie pour l’attribut sélectionné ici. Vous pouvez sélectionner n’importe quel attribut de prix configuré. Cependant, si l’attribut sélectionné n’est pas renseigné pour un produit, la source de prix du produit revient par défaut à `Price` lorsque des règles de tarification sont appliquées pour déterminer le prix de la mise en vente d’Amazon publiée.

1. Pour **[!UICONTROL Minimum Advertised Price (MAP)**], choisissez une option.

   La valeur par défaut n’est pas sélectionnée. Ce paramètre active un prix minimum de publicité (MAP) pour un produit. Lorsque vous définissez un attribut de prix et que le prix de vente d’un produit est inférieur au prix minimum déterminé (en fonction de votre source de prix et de vos règles), cette valeur devient le MAP de la liste. Ce paramètre vous permet d’implémenter des [règles de tarification](./pricing-products.md), tout en contrôlant le prix minimum d’un produit. Pour éviter qu’un prix de mise en vente ne soit trop bas, choisissez un attribut de prix à utiliser comme MAP. Cependant, si le champ de tarification sélectionné n’est pas défini pour un produit, le MAP n’est pas utilisé.

1. Pour **[!UICONTROL Strike Through Price (MSRP)]**, choisissez une option.

   La valeur par défaut n’est pas sélectionnée. Ce paramètre détermine quel attribut de prix est utilisé comme prix de détail suggéré par le fabricant (MSRP) pour un produit. Si le prix de votre offre est inférieur au MSRP défini, votre offre Amazon s’affiche avec une répercussion du prix MSRP avec le prix de la mise en vente le plus bas, ainsi que le montant et le pourcentage calculés &quot;Vous économisez&quot;. Cependant, si le champ de tarification sélectionné n&#39;est pas défini pour un produit, le MSRP n&#39;est pas calculé.

   >[!NOTE]
   >
   >Ce paramètre s’applique uniquement aux listes qui ont gagné le [Buy Box](./buy-box-competitor-pricing.md) position. Le Buy Box est attribué par Amazon au vendeur dont le produit est habituellement répertorié au meilleur prix, ainsi que d&#39;autres facteurs tels que l&#39;offre de livraison FBA/Prime, la disponibilité et la performance du vendeur.

1. Pour **Appliquer la taxe sur la valeur ajoutée (TVA)**, choisissez une option :

   - `Disabled` - (Par défaut) Choisissez les cas où vous ne souhaitez pas appliquer la TVA au prix de votre offre.

   - `Enabled` - Choisissez quand vous souhaitez appliquer la TVA au prix de votre offre. La TVA est généralement utilisée comme taxe de vente dans les pays européens et est ajoutée à votre prix final répertorié dans Amazon. La TVA ne s&#39;applique pas au prix final pour les listes utilisées dans une règle de prix intelligente, sauf si la variable [prix plancher](./floor-price.md) est atteint.

   >[!NOTE]
   >
   >Les entreprises de l’Union européenne (UE) sont tenues d’envoyer des factures à des acheteurs afin que le client puisse verser des taxes. Vous pouvez générer ces factures et calculer les impôts vous-même ou utiliser un service de calcul des impôts tel que Amazon Computing Service. Amazon recommande de s’abonner au [Service de calcul de la TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). Si vous choisissez une autre méthode, vous êtes responsable du respect de la TVA.>
   >
   >Il peut s’écouler entre 10 et 14 jours avant qu’Amazon ne vérifie et n’active votre compte de service de calcul de la TVA.

1. Pour **[!UICONTROL VAT Percentage]**, saisissez la valeur de votre taux de TVA.

   La valeur par défaut est `0.00`. Cette valeur est utilisée pour calculer le montant de la TVA à ajouter au prix de la mise en vente. If `10.2` est renseignée, une TVA de 10,20 % est appliquée au prix de votre offre. Ce champ est désactivé lorsque le champ Demander la taxe à valeur ajoutée (TVA) est défini sur `Disabled`.

1. **(Magasins britanniques uniquement)** Pour **[!UICONTROL Amazon Product Tax Code (PTC)]**, choisissez une option :

   - `Do Not Manage PTC` - (Par défaut) Choisissez si vous utilisez un service de calcul des impôts tiers ou si tous vos calculs sont déjà configurés dans votre [!DNL Amazon Seller Central] compte . Lorsque cette option est sélectionnée, le canal de vente Amazon n’envoie aucune information de code de taxe sur les produits à votre [!DNL Amazon Seller Central] compte .

   - `Set Default PTC` - Choisissez si vous avez un code de taxe sur les produits universels (PTC) que vous souhaitez utiliser pour tous vos produits. Lorsque cette option est sélectionnée, vous devez effectuer les opérations suivantes : _[!UICONTROL Default PTC]_.

      - Pour **[!UICONTROL Default PTC]**, saisissez le code PTC par défaut à utiliser pour toutes les listes Amazon éligibles. Si votre PTC par défaut est défini dans votre [!DNL Amazon Seller Central] , laissez ce champ vide. Les modifications apportées à ce champ n’ont aucune incidence sur les listes Amazon existantes. Pour modifier le PTC par défaut d’une liste existante, la liste doit être [completed](./end-listings-manually.md) et une nouvelle liste a été créée.

   >[!NOTE]
   >
   >Si vous utilisez le service de calcul de la TVA Amazon, vous devez connaître la catégorie de taxe de vos produits. Un PTC est le code d’ID de catégorie de taxe Amazon pour les achats B2B dans l’UE. Voir [Codes de taxe des produits Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. Pour **[!UICONTROL Currency Conversion]**, choisissez une option.

   La valeur par défaut est `Disabled`. Ces options dépendent de vos [!DNL Commerce] [currency](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) paramètres. Si aucune option n’est disponible, configurez vos paramètres de devise.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Prix d’énumération](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| Champ | Description |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Détermine la source de prix utilisée lors de la création de vos listes Amazon. La valeur par défaut est `Price`. Si vous choisissez un autre attribut, comme `Amazon Price` ou `Special Price`, la valeur définie pour l’attribut est utilisée pour votre liste Amazon. Cependant, si l’attribut sélectionné n’est pas défini, `Price` est utilisée. |
| [!UICONTROL Minimum Advertised Price (MAP)] | Le [!DNL Commerce] pour la tarification MAP. Le choix de l’option MAP définit automatiquement votre liste Amazon sur le prix MAP si le prix de la liste est inférieur au prix du MAP. |
| [!UICONTROL Strike Through Price (MSRP)] | Le [!DNL Commerce] qui représente le prix MSRP. Si le prix de votre offre Amazon est inférieur au MSRP, il affiche une répercussion sur le prix MSRP et le prix de la vente. Ce paramètre est également utilisé pour calculer le montant et le pourcentage &quot;Vous économisez&quot;, mais cette fonctionnalité ne s’applique qu’aux listes qui ont gagné le [Buy Box](./buy-box-competitor-pricing.md) position. |
| [!UICONTROL Apply Value Added Tax (VAT)] | La TVA est utilisée par les vendeurs dans l&#39;Union Européenne.<br><br>Choisir `Disabled` si vous ne souhaitez pas que la TVA soit ajoutée aux prix listés.<br><br>Choisir `Enabled` puis saisissez le pourcentage de TVA pour appliquer la TVA aux prix de vos listes. |
| [!UICONTROL VAT Percentage] | Définissez le pourcentage à utiliser pour calculer le montant de la TVA à ajouter au prix de la mise en vente de vos listes Amazon. <br><br>Si vous saisissez `5`, une TVA de 5 % sera appliquée au prix de vente final une fois toutes les règles de prix appliquées. La TVA ne s&#39;applique pas au prix final des inscriptions utilisées dans le cadre d&#39;une règle de tarification intelligente, sauf si la variable [floor](./floor-price.md) ou [ceiling](./optional-ceiling-price.md) est atteint. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Apparaît pour les magasins britanniques uniquement) Détermine si le canal de vente Amazon envoie des informations de code de taxe sur les produits à votre [!DNL Amazon Seller Central] compte . <br><br>Sélectionner **Ne pas gérer PTC** si vous utilisez un service de calcul des impôts tiers ou si tous vos calculs sont déjà configurés dans votre [!DNL Amazon Seller Central] compte . Lorsque cette option est définie, le canal de vente Amazon n’envoie aucune information de code de taxe sur les produits à votre [!DNL Amazon Seller Central] compte .<br><br>Sélectionner **Définir le PTC par défaut** si vous disposez d’un code de taxe sur les produits universels que vous souhaitez utiliser pour tous vos produits.<br><br>Voir [Codes de taxe des produits Amazon](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | S’affiche uniquement lorsque **Code de taxe sur les produits Amazon (PTC)** est défini sur `Set Default PTC`. Saisissez le code PTC par défaut à utiliser pour toutes les listes Amazon éligibles. Si votre PTC par défaut est défini dans votre [!DNL Amazon Seller Central] , laissez ce champ vide. <br><br>Les modifications apportées à ce champ n’ont aucune incidence sur les listes existantes. La liste doit être [completed](./end-listings-manually.md) et une nouvelle liste créée pour que la modification prenne effet. |
| [!UICONTROL Currency Conversion] | Permet à [!DNL Commerce] la devise par défaut storefront pour une conversion précise en votre devise Amazon par défaut afin de publier les prix de vos listes dans la devise appropriée. La conversion de devise est toujours basée sur votre [!DNL Commerce] devise par défaut.<br><br>Vous pouvez toujours afficher votre [!DNL Commerce] et les devises Amazon lorsque d’autres devises sont disponibles. Si la valeur par défaut [!DNL Commerce] Devise correspond à votre devise Amazon par défaut, laissez la conversion de devise désactivée.<br><br>Par exemple, si la variable [!DNL Commerce] la devise par défaut est CAD (dollars canadiens) et la devise par défaut d’Amazon est USD. Vous devez activer la conversion de devise et choisir la valeur CAD du taux de conversion en USD. Les options présentées reposent sur la fonction intégrée [!DNL Commerce] conversions de devises. Si vous ne voyez pas l’option que vous recherchez, [configurer la devise dans [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
