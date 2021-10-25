---
title: Paramètres de stockage par défaut
description: Modifiez les paramètres Commerce par défaut pour personnaliser le Sales Channel Amazon pour votre boutique.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Paramètres de magasin par défaut

Une fois que votre magasin est connecté et que vous avez configuré votre première règle d&#39;annonce, la synchronisation des données entre Amazon et [!DNL Commerce] commence. Il existe plusieurs types de paramètres de magasin qui vous permettent de personnaliser votre magasin en fonction de vos besoins. Les paramètres de la boutique sont accessibles dans la boutique. [tableau de bord](./amazon-store-dashboard.md).

Les paramètres de la Boutique sont les suivants :

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Contrôler l’interaction de votre catalogue de produits avec le [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Contrôler la gestion des commandes Amazon.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Définissez les produits de catalogue pouvant être répertoriés sur Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Définissez la manière dont le prix de la liste Amazon est modifié pour les annonces qualifiées.

- **[!UICONTROL Store reports]** - [Analyse concurrentielle des prix](./competitive-price-analysis.md) et [amélioration de la liste](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Modifications de la liste](./listing-changes-log.md) et [erreurs de communication](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Vérifiez les paramètres de nom de magasin de canaux de vente Amazon et de courrier électronique dans la section [!DNL Commerce] Administrateur.

## Quelques paramètres par défaut importants

| Paramètre | Par défaut | Description | Emplacement |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Crée le [!DNL Commerce] commandes lorsque de nouvelles commandes sont reçues d’Amazon, ce qui permet de gérer les commandes dans le [[!DNL Commerce] Commandes](https://docs.magento.com/user-guide/sales/orders.html)Workflow {target=&quot;_blank&quot;}. Lorsque `Disabled`, Amazon commande importer des informations de commande pour révision, mais les commandes doivent être gérées dans votre [!DNL Amazon Seller Central] compte. | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Les données client des commandes Amazon ne sont pas importées dans votre [!DNL Commerce] base de données. Les commandes Amazon importées sont traitées en tant qu&#39;extraction invitée. Si vous souhaitez créer votre [!DNL Commerce] base de données client, vous devez modifier ce paramètre en `Build New Customer Account`. | [Paramètres de commande](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] les produits de catalogue (qui répondent aux exigences d’éligibilité d’Amazon) à publier automatiquement sur Amazon et à créer des listes Amazon. Si vous souhaitez réviser et publier manuellement vos produits, vous devez modifier ce paramètre en `Do Not Automatically List Eligible Products`. Les produits en attente d’une publication manuelle s’affichent sur la page [_Prêt pour la liste_](./ready-to-list.md) . | [Actions de liste de produits](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Définit l’attribut de source de prix utilisé comme base pour vos annonces Amazon. Si vous ne souhaitez pas utiliser la [!DNL Commerce] `Price` comme prix de base sur lequel vos règles de tarification sont basées, vous devez modifier ce paramètre en un attribut différent. | [Prix d&#39;annonce](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | Le marchand remplit toutes les commandes. Si vous utilisez l’exécution par Amazon ou une combinaison de méthodes d’exécution, vous devez modifier ce paramètre. | [Rempli par](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Si tous vos produits sont dans la même condition, vous pouvez sélectionner l’une des options de condition Amazon pour représenter tous vos produits. Si votre catalogue contient des produits dans des conditions différentes (Nouveau, Utilisé et Rénové, par exemple), vous devez modifier ce paramètre pour `Assign Condition Using Product Attribute` et mappez votre [!DNL Commerce] attributs de condition pour vos conditions de mise en vente Amazon. | [Condition de liste de produits](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | aucune | Définissez les règles utilisées pour déterminer quels produits Amazon Sales Channel publie sur Amazon. Ces règles offrent de nombreuses options pour créer des règles simples ou complexes pour inclure ou exclure des produits en tant qu’annonces. | [Règles d&#39;annonce](./listing-rules.md) |
| Règles de tarification | aucune | Définissez votre attribut de prix de vente Amazon différent de celui défini _[!UICONTROL Magento Price Source]_dans votre [Prix d&#39;annonce](./listing-price.md). Pour ajuster le prix de votre annonce (à la hausse ou à la baisse) par rapport à votre_[!UICONTROL Magento Price Source]_ , créez des règles. | [Règles de tarification](./pricing-products.md) |

Pour plus d’informations, voir [Paramètres de stockage](./ob-store-review.md).
