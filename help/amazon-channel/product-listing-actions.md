---
title: Canal commercial Amazon - Actions de liste de produits
description: Utilisez les paramètres Actions de liste de produits pour définir la manière dont votre catalogue Commerce interagit avec Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Actions de liste de produits

Les paramètres d’actions de liste de produits font partie des paramètres de liste de magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord du magasin](./amazon-store-dashboard.md).

Ces paramètres définissent la manière dont votre catalogue interagit avec Amazon. Ces paramètres :

- Indiquez si vos produits de catalogue [!DNL Commerce] répondant aux critères d’éligibilité d’Amazon sont automatiquement envoyés à votre compte [!DNL Amazon Seller Central] pour créer des listes.

- Définissez le délai de traitement par défaut d’une commande. Cette valeur définit le nombre de jours nécessaires au traitement et à l’envoi d’une commande. Par exemple, si quelqu’un sélectionne une livraison de 2 jours, ce délai ne commence pas tant que le traitement n’est pas terminé et les packages ne sont pas remis à un opérateur. Le temps de livraison total est (temps de traitement + temps de transit + jours fériés).

## Configuration des paramètres

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord du magasin.

1. Développez la section _[!UICONTROL Product Listing Actions]_.

1. Pour **[!UICONTROL Automatic List Action]** (obligatoire), choisissez une option :

   - `Automatically List Eligible Products` - (Par défaut) Choisissez le moment où vous souhaitez que vos produits de catalogue [!DNL Commerce] (qui répondent aux exigences d’éligibilité d’Amazon) soient automatiquement publiés dans Amazon et créent des listes Amazon.

   - `Do Not Automatically List Eligible Products` - Choisissez quand vous souhaitez sélectionner manuellement vos produits de catalogue [!DNL Commerce] éligibles et créer des listes Amazon. Une fois sélectionnés, les produits du catalogue qui répondent aux critères de votre liste et contiennent toutes les informations requises s’affichent sur l’onglet [_[!UICONTROL Ready to List]_](./ready-to-list.md) pour une publication manuelle sur Amazon.

1. Pour **[!UICONTROL Default Handling Time]** (obligatoire), saisissez le nombre de jours requis pour le délai d’avance avant l’expédition.

   La valeur par défaut est de `2` jours.

   >[!NOTE]
   >
   >Cette valeur de délai d’exécution par défaut n’est effective que pour les listes Amazon créées via le canal de vente Amazon. Toutes les listes Amazon créées dans votre compte [!DNL Amazon Seller Central] utilisent le délai de gestion par défaut défini dans Amazon.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![Actions de liste de produits](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| Champ | Description |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | Options :<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Recommandé) Choisissez quand vous souhaitez que vos produits de catalogue [!DNL Commerce] (qui répondent aux critères d’éligibilité d’Amazon) soient automatiquement publiés dans Amazon et créent des listes Amazon. Lorsque cette option est sélectionnée, l’onglet [_[!UICONTROL Ready to List]_](./ready-to-list.md) ne s’affiche pas. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Choisissez quand vous souhaitez sélectionner manuellement les produits de catalogue éligibles [!DNL Commerce] et créer des listes Amazon. Une fois sélectionnés, les produits du catalogue qui répondent aux critères de votre liste et contiennent toutes les informations requises s’affichent sur l’onglet [_[!UICONTROL Ready to List]_](./ready-to-list.md) pour la publication manuelle.</li></ul> |
| [!UICONTROL Default Handling Time] | Valeur numérique qui représente le nombre de jours, en général, nécessaire au traitement et à l’envoi des commandes. La valeur par défaut est `2`. Cette valeur est utilisée pour les listes Amazon créées dans [!DNL Commerce] et publiées dans Amazon. Le temps de traitement par défaut des listes Amazon avant l’intégration à [!DNL Commerce] n’est pas affecté par ce paramètre.<br><br>La valeur définie dans le canal de vente Amazon ne remplace pas le temps de traitement par défaut défini dans une liste Amazon existante. Lorsqu’un **[!UICONTROL Handling Time Override]** est activé, puis supprimé, l’ heure de traitement d’une commande revient à la valeur définie ici.<br><br>Si des produits ont des temps de traitement différents, vous pouvez créer un remplacement de temps de gestion au niveau spécifique au produit. Vous pouvez gérer les remplacements de temps dans l’onglet [_[!UICONTROL Overrides]_](./overrides.md), ce qui vous donne la possibilité de gérer l’exécution de votre produit. En l’absence de remplacement du temps de gestion dans [!DNL Commerce] pour un produit, la valeur par défaut du temps de gestion est la valeur définie dans la liste Amazon.<br><br>Handling Time est un attribut régional. Lorsque la valeur est modifiée pour une liste, la modification affecte toutes les listes qui partagent le [!DNL Amazon Seller SKU] dans tous les magasins Amazon qui existent pour la même région (défini à l’ [intégration de magasin](./store-integration.md)). Cependant, la modification de la valeur d&#39;un [!DNL Amazon Seller SKU] partagé dans la région Amérique du Nord n&#39;affecte pas les mêmes produits répertoriés dans un magasin avec une région définie différente. Le magasin de la région avec la date de création la plus ancienne contrôle la priorité des paramètres d’heure de gestion par défaut. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
