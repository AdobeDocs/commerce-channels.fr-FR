---
title: Paramètres de magasin par défaut pour les listes Amazon
description: Modifiez les paramètres Commerce par défaut pour personnaliser le Sales Channel Amazon de votre magasin.
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Paramètres de magasin par défaut pour les listes Amazon

Une fois que votre magasin est connecté et que vous avez configuré votre première règle de liste, la synchronisation des données entre Amazon et [!DNL Commerce] démarre. Plusieurs types de paramètres de magasin vous permettent de personnaliser votre magasin en fonction de vos besoins. Les paramètres de magasin sont accessibles sur le [tableau de bord](./amazon-store-dashboard.md) du magasin.

Les paramètres de magasin incluent :

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Contrôlez la manière dont votre catalogue de produits interagit avec [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Contrôle de la gestion des commandes Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Définissez les produits du catalogue qui peuvent être répertoriés dans Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Définissez la manière dont le prix de la liste Amazon est modifié pour les listes qualifiées.

- **[!UICONTROL Store reports]** - [Analyse des prix compétitifs](./competitive-price-analysis.md) et [améliorations des listes](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Modifications de liste](./listing-changes-log.md) et [erreurs de communication](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Vérifiez les paramètres de nom de la boutique de canaux de vente Amazon et d’e-mail dans l’administrateur [!DNL Commerce].

## Certains paramètres par défaut importants

| Paramètre | Par défaut | Description | Emplacement |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crée les [!DNL Commerce] commandes correspondantes lors de la réception de nouvelles commandes d’Amazon, ce qui permet de gérer les commandes dans le workflow [[!DNL Commerce] Commandes](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Lorsque `Disabled`, Amazon commande des informations de commande d’importation pour révision, mais les commandes doivent être gérées dans votre compte [!DNL Amazon Seller Central]. | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Les données client des commandes Amazon ne sont pas importées dans votre base de données [!DNL Commerce]. Les commandes Amazon importées sont traitées comme un passage en caisse invité. Si vous souhaitez créer votre base de données client [!DNL Commerce], vous devez définir ce paramètre sur `Build New Customer Account`. | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] produits de catalogue (qui répondent aux critères d’éligibilité d’Amazon) pour publier automatiquement sur Amazon et créer des listes Amazon. Si vous souhaitez passer manuellement en revue et publier vos produits, vous devez modifier ce paramètre en `Do Not Automatically List Eligible Products`. Les produits en attente d’une publication manuelle s’affichent dans l’onglet [_Prêt à lister_](./ready-to-list.md) . | [Actions de liste de produits](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Définit l’attribut price source utilisé comme base de vos listes Amazon. Si vous ne souhaitez pas utiliser l’attribut [!DNL Commerce] `Price` comme prix de base sur lequel vos règles de tarification sont basées, vous devez définir ce paramètre sur un attribut différent. | [Prix d’énumération](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | Le marchand répond à toutes les commandes. Si vous utilisez l’exécution par Amazon ou un mélange de méthodes d’exécution, vous devez modifier ce paramètre. | [Complété par](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si tous vos produits sont la même condition, vous pouvez sélectionner l’une des options de condition Amazon pour représenter tous vos produits. Si votre catalogue contient des produits dans différentes conditions (nouveaux, utilisés et mis à jour, par exemple), vous devez modifier ce paramètre en `Assign Condition Using Product Attribute` et mapper vos attributs de condition [!DNL Commerce] aux conditions de liste Amazon. | [Condition de liste de produits](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | none | Définissez les règles utilisées pour déterminer les produits que le canal de vente Amazon publie dans Amazon. Ces règles offrent de nombreuses options pour créer des règles simples à complexes afin d’inclure ou d’exclure des produits en tant que listes. | [Règles de liste](./listing-rules.md) |
| Règles de tarifs | none | Définissez l&#39;attribut de prix de la liste Amazon différent de l&#39;attribut _[!UICONTROL Magento Price Source]_défini dans votre [Prix de la liste](./listing-price.md). Pour ajuster le prix de votre liste (haut ou bas) en fonction de votre paramètre_[!UICONTROL Magento Price Source]_, créez des règles. | [Règles de tarification](./pricing-products.md) |

Pour plus d’informations, voir [Paramètres de magasin](./ob-store-review.md).
