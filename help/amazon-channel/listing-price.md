---
title: Prix d'annonce
description: Utilisez les paramètres Prix d'annonce pour déterminer la source de prix et la valeur de prix de base (par défaut) de vos annonces Amazon.
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# Prix d&#39;annonce

[!UICONTROL Listing Price] font partie des paramètres de votre liste de magasins. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres définissent [!DNL Commerce] attribut de tarification à utiliser comme source de prix, qui est la valeur de prix de base (par défaut) pour vos annonces Amazon. Ces paramètres sont utilisés par votre [règles de tarification](./pricing-rule-general-settings.md) pour ajuster automatiquement le prix de votre annonce Amazon par rapport à la valeur définie pour _[!UICONTROL Magento Price Source]_.

Vous pouvez configurer votre [étendue des prix](./price-scope.md) comme global ou site web. Si votre étendue de tarification est définie sur `Global`, il existe une source de prix unique pour tous vos magasins/sites web. Si votre étendue de tarification est définie sur `Website`, la source de prix utilise une logique de repli du prix du site web (si disponible) suivie du prix par défaut (global).

Si une règle de mise en vente est définie pour s’appliquer à plusieurs sites Web, l’ordre dans lequel le prix du site Web est utilisé est déterminé par le paramètre de priorité du site Web défini dans la propriété [règle de liste](./listing-rules.md). Ces règles vous permettent de définir la tarification du produit dans l’ensemble de votre catalogue. Pour savoir si vous utilisez l’étendue de prix du site web, voir [Portée du prix du catalogue](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

Les options répertoriées dans _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ et _[!UICONTROL Strike Through Price (MSRP)]_inclure vos attributs de tarification configurés. Les attributs de tarification sont [!DNL Commerce] attributs de produit avec le type d’entrée de catalogue pour la valeur Propriétaire du magasin défini sur `Price`. Voir [Types d’entrée d’attribut](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Configurer les paramètres de prix d&#39;annonce {#configure-listing-price-settings}

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la _[!UICONTROL Listing Price]_.

1. Pour **[!UICONTROL Magento Price Source]** (obligatoire), sélectionnez une option.

   La valeur par défaut est `Price`. Ce paramètre détermine la source de prix utilisée pour vos annonces Amazon. Si vous créez [règles de tarification](./pricing-products.md), les règles sont appliquées à la valeur définie pour l’attribut sélectionné ici. Vous pouvez sélectionner n’importe quel attribut de tarification configuré. Toutefois, si l’attribut sélectionné n’est pas rempli pour un produit, la source de prix du produit revient par défaut à `Price` lorsque des règles de tarification sont appliquées pour déterminer le prix d&#39;annonce Amazon publié.

1. Pour **[!UICONTROL Minimum Advertised Price (MAP)**], choisissez une option.

   La valeur par défaut n’est pas une sélection. Ce paramètre active un prix minimal annoncé (MAP) pour un produit. Lorsque vous définissez un attribut de tarification et que le prix d’annonce d’un produit tombe en dessous du prix minimum déterminé (en fonction de votre source de tarification et de vos règles), cette valeur devient le MAP de la mise en vente. Ce paramètre vous permet de mettre en oeuvre [règles de tarification](./pricing-products.md), tout en contrôlant le prix minimum d’un produit. Pour éviter qu&#39;un prix de vente ne soit trop bas, choisissez un attribut de prix à utiliser comme MAP. Toutefois, si le champ de tarification sélectionné n’est pas défini pour un produit, le MAP n’est pas utilisé.

1. Pour **[!UICONTROL Strike Through Price (MSRP)]**, choisissez une option.

   La valeur par défaut n’est pas une sélection. Ce paramètre détermine quel attribut de tarification est utilisé comme prix au détail suggéré par le fabricant (MSRP) pour un produit. Si votre prix d&#39;inscription est inférieur au MSRP défini, votre annonce Amazon s&#39;affiche avec une barré du prix MSRP avec le prix d&#39;inscription le plus bas, ainsi que le montant et le pourcentage &quot;Vous économisez&quot; calculés. Toutefois, si le champ de tarification sélectionné n’est pas défini pour un produit, le MSRP n’est pas calculé.

   >[!NOTE]
   >
   >Ce paramètre s’applique uniquement aux annonces qui ont remporté le [Buy Box](./buy-box-competitor-pricing.md) position. Le Buy Box est attribué par Amazon au vendeur qui a le produit listé habituellement au meilleur prix, ainsi que d&#39;autres facteurs tels que l&#39;offre d&#39;expédition FBA/Prime, la disponibilité et la performance du vendeur.

1. Pour **Appliquer la taxe sur la valeur ajoutée (TVA)**, choisissez une option :

   - `Disabled` - (Par défaut) Choisissez si vous ne souhaitez pas appliquer la TVA au prix de votre annonce.

   - `Enabled` - Choisissez quand vous souhaitez appliquer la TVA au prix de votre annonce. La TVA est généralement utilisée comme taxe de vente dans les pays européens et est ajoutée à votre prix final inscrit dans Amazon. La TVA ne s’applique pas au prix final pour les annonces utilisées dans le cadre d’une règle de tarification intelligente, à moins que la [prix plancher](./floor-price.md) est touché.
   >[!NOTE]
   >
   >Les entreprises de l’Union européenne (UE) sont tenues d’envoyer des factures à des acheteurs d’entreprise, afin que le client puisse verser la taxe. Vous pouvez générer ces factures et calculer les taxes vous-même ou utiliser un service de calcul de taxe tel que Amazon Tax Calculation Service. Amazon recommande de s&#39;inscrire pour le [Service de calcul de TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Si vous choisissez une autre méthode, vous êtes responsable du respect de la TVA.>
   >
   >Il peut prendre entre 10 et 14 jours pour qu’Amazon vérifie et active votre compte de service de calcul de la TVA.

1. Pour **[!UICONTROL VAT Percentage]**, entrez la valeur de votre taux de TVA.

   La valeur par défaut est `0.00`. Cette valeur est utilisée pour calculer le montant de TVA à ajouter au prix d&#39;annonce. Si `10.2` est saisi, une TVA de 10,20% est appliquée au prix de votre annonce. Ce champ est désactivé lorsque le champ Appliquer la taxe sur la valeur ajoutée (TVA) est défini sur `Disabled`.

1. **(Boutiques Royaume-Uni uniquement)** Pour **[!UICONTROL Amazon Product Tax Code (PTC)]**, choisissez une option :

   - `Do Not Manage PTC` - (Par défaut) Indiquez si vous utilisez un service de calcul fiscal tiers ou si tous vos calculs fiscaux sont déjà configurés dans votre [!DNL Amazon Seller Central] compte. Lorsque cette option est sélectionnée, le canal de vente Amazon n’envoie aucune information de code de taxe de produit à votre [!DNL Amazon Seller Central] compte.

   - `Set Default PTC` - Choisissez si vous avez un code de taxe sur les produits (PTC) universel que vous souhaitez utiliser pour tous vos produits. Lorsque cette option est sélectionnée, vous devez remplir _[!UICONTROL Default PTC]_.

      - Pour **[!UICONTROL Default PTC]**, entrez le code PTC par défaut à utiliser pour toutes les annonces Amazon éligibles. Si votre code PTC par défaut est défini dans votre [!DNL Amazon Seller Central] , laissez ce champ vide. Les modifications apportées à ce champ n’affectent pas les listes Amazon existantes. Pour modifier le PTC par défaut d&#39;une annonce existante, la liste doit être [terminé](./end-listings-manually.md) et une nouvelle annonce a été créée.
   >[!NOTE]
   >
   >Si vous utilisez le service de calcul de TVA Amazon, vous devez connaître la catégorie de taxe de vos produits. Un code PTC est en train d&#39;Amazon à le code de catégorie de taxe pour les achats B2B dans l&#39;UE. Voir [Amazon - Codes de taxe sur les produits](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}.

1. Pour **[!UICONTROL Currency Conversion]**, choisissez une option.

   La valeur par défaut est `Disabled`. Ces options dépendent de votre [!DNL Commerce] [devise](https://docs.magento.com/user-guide/configuration/general/currency-setup.html)Paramètres {target=&quot;_blank&quot;}. Si aucune option n’est disponible, configurez vos paramètres de devise.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Prix d&#39;annonce](assets/amazon-listing-price.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Magento Price Source] | Détermine la source de prix utilisée lors de la création de vos annonces Amazon. La valeur par défaut est `Price`. Si vous choisissez un attribut différent, tel que `Amazon Price` ou `Special Price`, la valeur définie pour l’attribut est utilisée pour votre liste Amazon. Toutefois, si l’attribut sélectionné n’est pas défini, `Price` est utilisé. |
| [!UICONTROL Minimum Advertised Price (MAP)] | Le [!DNL Commerce] pour la tarification MAP. Si vous choisissez l’option MAP, votre annonce Amazon est automatiquement réglée sur le prix MAP si le prix d’inscription est inférieur au prix MAP. |
| [!UICONTROL Strike Through Price (MSRP)] | Le [!DNL Commerce] qui représente la tarification MSRP. Si votre prix d&#39;inscription Amazon est inférieur au MSRP, il affiche une annulation du prix MSRP et du prix d&#39;inscription. Ce paramètre est également utilisé pour calculer le montant et le pourcentage &quot;Vous économisez&quot;, mais cette fonction s’applique uniquement aux annonces qui ont remporté la [Buy Box](./buy-box-competitor-pricing.md) position. |
| [!UICONTROL Apply Value Added Tax (VAT)] | La TVA est utilisée par les vendeurs dans l&#39;Union européenne.<br><br>Choisir `Disabled` si vous ne souhaitez pas que la TVA soit ajoutée aux prix d&#39;annonce.<br><br>Choisir `Enabled` puis entrez le pourcentage de TVA pour appliquer la TVA aux prix de votre annonce. |
| [!UICONTROL VAT Percentage] | Définissez le pourcentage à utiliser pour calculer le montant de TVA à ajouter au prix d&#39;annonce pour vos annonces Amazon. <br><br>Si vous entrez `5`, une TVA de 5% sera appliquée au prix final de la cotation après application de toutes les règles de prix. La taxe sur la TVA ne s’applique pas au prix final pour les annonces utilisées dans le cadre d’une règle de tarification intelligente, à moins que la [étage](./floor-price.md) ou [plafond](./optional-ceiling-price.md) est touché. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (S’affiche pour les magasins britanniques uniquement) Détermine si le canal de vente Amazon envoie des informations de code de taxe de produit à votre [!DNL Amazon Seller Central] compte. <br><br>Sélectionner **Ne pas gérer PTC** si vous utilisez un service de calcul fiscal tiers ou si tous vos calculs fiscaux sont déjà configurés dans votre [!DNL Amazon Seller Central] compte. Lorsque cette option est définie sur cette option, Amazon Sales Channel n’envoie aucune information de code de taxe de produit à votre [!DNL Amazon Seller Central] compte.<br><br>Sélectionner **Définir le code PTC par défaut** si vous avez un code de taxe sur les produits universels que vous souhaitez utiliser pour tous vos produits.<br><br>Voir [Amazon - Codes de taxe sur les produits](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | N’apparaît que lorsque **Code de taxe sur les produits Amazon (PTC)** est défini sur `Set Default PTC`. Entrez le code PTC par défaut à utiliser pour toutes les annonces Amazon éligibles. Si votre code PTC par défaut est défini dans votre [!DNL Amazon Seller Central] , laissez ce champ vide. <br><br>Les modifications apportées à ce champ n’affectent pas les annonces existantes. La liste doit être [terminé](./end-listings-manually.md) et une nouvelle annonce créée pour que la modification entre en vigueur. |
| [!UICONTROL Currency Conversion] | Permet à [!DNL Commerce] la devise par défaut de storefront pour convertir avec précision votre devise Amazon par défaut afin de publier vos prix de vente dans la devise appropriée. La conversion de devise est toujours basée sur votre [!DNL Commerce] devise par défaut.<br><br>Vous pouvez toujours afficher votre [!DNL Commerce] et Amazon lorsque d&#39;autres devises sont disponibles. Si votre [!DNL Commerce] devise correspond à votre devise Amazon par défaut, laissez la conversion de devise désactivée.<br><br>Par exemple, si [!DNL Commerce] la devise par défaut est CAD (dollars canadiens) et la devise par défaut Amazon est USD, vous devez activer Conversion de devise et choisir CAD Taux de conversion en USD. Les options présentées sont basées sur la [!DNL Commerce] conversions de devises. Si vous ne voyez pas l’option que vous recherchez, [configurer la devise dans [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
