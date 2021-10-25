---
title: Actions de liste de produits
description: Utilisez les paramètres Actions de liste de produits pour définir la manière dont votre catalogue Commerce interagit avec Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Actions de mise en vente de produits

Les paramètres d’actions Liste des produits font partie de vos paramètres d’annonce de magasin. Les paramètres de liste sont accessibles à partir de l’onglet [tableau de bord de magasin](./amazon-store-dashboard.md).

Ces paramètres définissent l’interaction de votre catalogue avec Amazon. Ces paramètres :

- Indiquez si [!DNL Commerce] les produits de catalogue répondant aux exigences d’éligibilité Amazon sont automatiquement envoyés à votre [!DNL Amazon Seller Central] pour créer des annonces.

- Définissez le délai de traitement par défaut pour une commande. Cette valeur définit le nombre de jours requis pour traiter et expédier une commande. Par exemple, si quelqu&#39;un choisit l&#39;expédition de 2 jours, ce délai de transit ne commence pas tant que le traitement n&#39;est pas terminé et que les colis ne sont pas remis à un transporteur. Le délai total de livraison est (temps de manutention + temps de transit + jours fériés).

## Configuration des paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** sur le tableau de bord de la boutique.

1. Développez la _[!UICONTROL Product Listing Actions]_.

1. Pour **[!UICONTROL Automatic List Action]** (obligatoire), choisissez une option :

   - `Automatically List Eligible Products` - (Par défaut) Choisissez quand vous souhaitez [!DNL Commerce] les produits de catalogue (qui répondent aux exigences d’éligibilité d’Amazon) à publier automatiquement sur Amazon et à créer des listes Amazon.

   - `Do Not Automatically List Eligible Products` - Choisissez quand vous souhaitez sélectionner manuellement votre éligible [!DNL Commerce] cataloguez les produits et créez des annonces Amazon. Lorsque cette option est sélectionnée, les produits de catalogue qui répondent aux critères de votre annonce et contiennent toutes les informations requises s’affichent sur la [_[!UICONTROL Ready to List]_](./ready-to-list.md) pour la publication manuelle vers Amazon.

1. Pour **[!UICONTROL Default Handling Time]** (requis), indiquez le nombre de jours requis pour le délai de livraison avant expédition.

   La valeur par défaut est `2` jours.

   >[!NOTE]
   >
   >Cette valeur de temps de traitement par défaut ne s&#39;applique qu&#39;aux annonces Amazon créées via le canal de vente Amazon. Toute annonce Amazon créée dans votre [!DNL Amazon Seller Central] utilisent le délai de traitement par défaut défini dans Amazon.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save listing settings]**.

![Actions de mise en vente de produits](assets/amazon-product-listing-actions.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Automatic List Action] | Options :<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recommandé) Choisissez quand vous souhaitez [!DNL Commerce] les produits de catalogue (qui répondent aux exigences d’éligibilité d’Amazon) à publier automatiquement sur Amazon et à créer des listes Amazon. Lorsque cette option est sélectionnée, la [_[!UICONTROL Ready to List]_](./ready-to-list.md) n’est pas affiché. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Choisissez quand vous souhaitez sélectionner manuellement les éléments éligibles [!DNL Commerce] cataloguez les produits et créez des annonces Amazon. Lorsque cette option est sélectionnée, les produits de catalogue qui répondent aux critères de votre annonce et contiennent toutes les informations requises s’affichent sur la [_[!UICONTROL Ready to List]_](./ready-to-list.md) pour la publication manuelle.</li></ul> |
| [!UICONTROL Default Handling Time] | Valeur numérique qui représente le nombre de jours, en général, nécessaire au traitement et à l&#39;expédition de vos commandes. La valeur par défaut est `2`. Cette valeur est utilisée pour les annonces Amazon créées dans [!DNL Commerce] et publié sur Amazon. Temps de traitement par défaut pour les annonces Amazon avant l’intégration avec [!DNL Commerce] ne sont pas affectés par ce paramètre.<br><br>La valeur définie dans le canal de vente Amazon ne remplace pas le temps de traitement par défaut défini dans une liste Amazon existante. Lorsque **[!UICONTROL Handling Time Override]** est activée, puis supprimée, le délai de traitement d’une commande revient à la valeur définie ici.<br><br>Si vous disposez de produits dont les délais de traitement sont différents, vous pouvez créer un remplacement du temps de traitement au niveau spécifique au produit. Vous pouvez gérer les remplacements de temps de traitement dans le dossier [_[!UICONTROL Overrides]_](./overrides.md) , ce qui vous donne la souplesse nécessaire pour gérer la réalisation de votre produit. S’il n’y a pas de délai de traitement personnalisé dans [!DNL Commerce] pour un produit, la valeur par défaut du délai de traitement est la valeur définie dans la liste Amazon.<br><br>La gestion du temps est un attribut régional. Lorsque la valeur d’une annonce est modifiée, la modification affecte toutes les annonces qui partagent la propriété [!DNL Amazon Seller SKU] dans tous les magasins Amazon qui existent pour la même région (définie à [intégration de magasin](./store-integration.md)). Toutefois, la modification de la valeur d’un partage [!DNL Amazon Seller SKU] dans la région de l’Amérique du Nord n’affecte pas les mêmes produits répertoriés dans un magasin avec une région définie différente. Le magasin de la région avec la date de création la plus ancienne contrôle la priorité des paramètres Temps de gestion par défaut. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
