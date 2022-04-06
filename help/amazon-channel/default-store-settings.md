---
title: Paramètres de magasin par défaut
description: Modifiez les paramètres Commerce par défaut pour personnaliser le Sales Channel Amazon de votre boutique.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Paramètres de magasin par défaut

Une fois votre boutique connectée et que vous avez configuré votre première règle de liste, la synchronisation des données entre Amazon et [!DNL Commerce] commence. Plusieurs types de paramètres de magasin vous permettent de personnaliser votre magasin en fonction de vos besoins. Les paramètres de magasin sont accessibles sur le magasin [tableau de bord](./amazon-store-dashboard.md).

Les paramètres de magasin incluent :

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Contrôler la manière dont votre catalogue de produits interagit avec la variable [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Contrôle de la gestion des commandes Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Définissez les produits du catalogue qui peuvent être répertoriés dans Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Définissez la manière dont le prix de la liste Amazon est modifié pour les listes qualifiées.

- **[!UICONTROL Store reports]** - [Analyse des prix compétitifs](./competitive-price-analysis.md) et [améliorations des listes](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Modifications de la liste](./listing-changes-log.md) et [erreurs de communication](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Vérifiez les paramètres de nom de la boutique de canaux de vente Amazon et d’e-mail dans le [!DNL Commerce] Administrateur.

## Certains paramètres par défaut importants

| Paramètre | Par défaut | Description | Emplacement |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crée la [!DNL Commerce] commandes lors de la réception de nouvelles commandes d’Amazon, ce qui permet de gérer les commandes dans la variable [[!DNL Commerce] Commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}. When `Disabled`, Amazon commande des informations de commande d’importation à des fins de révision, mais les commandes doivent être gérées dans votre [!DNL Amazon Seller Central] compte . | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Les données client des commandes Amazon ne sont pas importées dans votre [!DNL Commerce] base de données. Les commandes Amazon importées sont traitées comme un passage en caisse invité. Si vous souhaitez créer votre [!DNL Commerce] base de données client, vous devez définir ce paramètre sur `Build New Customer Account`. | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] cataloguer des produits (qui répondent aux critères d’éligibilité d’Amazon) pour les publier automatiquement dans Amazon et créer des listes Amazon. Si vous souhaitez passer manuellement en revue et publier vos produits, vous devez modifier ce paramètre en `Do Not Automatically List Eligible Products`. Les produits en attente d’une publication manuelle s’affichent sur la page [_Prêt à répertorier_](./ready-to-list.md) . | [Actions de liste de produits](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Définit l’attribut price source utilisé comme base de vos listes Amazon. Si vous ne souhaitez pas utiliser la variable [!DNL Commerce] `Price` comme prix de base sur lequel vos règles de tarification sont basées, vous devez définir ce paramètre sur un attribut différent. | [Prix d’énumération](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | Le marchand remplit toutes les commandes. Si vous utilisez l’exécution par Amazon ou un mélange de méthodes d’exécution, vous devez modifier ce paramètre. | [Renseigné par](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si tous vos produits sont la même condition, vous pouvez sélectionner l’une des options de condition Amazon pour représenter tous vos produits. Si votre catalogue contient des produits dans différentes conditions (nouveaux, utilisés et mis à jour, par exemple), vous devez définir ce paramètre sur `Assign Condition Using Product Attribute` et mappez vos [!DNL Commerce] attributs de condition à vos conditions de liste Amazon. | [Condition de liste de produits](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | none | Définissez les règles utilisées pour déterminer les produits que le canal de vente Amazon publie dans Amazon. Ces règles offrent de nombreuses options pour créer des règles simples à complexes afin d’inclure ou d’exclure des produits en tant que listes. | [Règles d’énumération](./listing-rules.md) |
| Règles de tarifs | none | Définissez votre attribut de prix de mise en vente Amazon différent de celui défini _[!UICONTROL Magento Price Source]_dans votre [Prix d’énumération](./listing-price.md). Pour ajuster le prix de votre offre (élevé ou négatif) par rapport à votre_[!UICONTROL Magento Price Source]_ , créez des règles. | [Règles de tarifs](./pricing-products.md) |

Pour plus d’informations, voir [Paramètres de magasin](./ob-store-review.md).
