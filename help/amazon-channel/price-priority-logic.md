---
title: Canal vente Amazon - Logique de priorité des prix
description: Le canal de vente Amazon applique la hiérarchisation pour déterminer le prix publié pour une liste Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# Logique de priorité des prix

Dans l’exemple suivant, comment le système détermine-t-il si vous souhaitez publier pour 31,99 $, 24,99 $ ou 27,99 $ ?

![Étendue des prix du commerce](assets/amazon-price-scope.png){width="400"}

Pour déterminer le prix utilisé si un produit se trouve sur deux sites web et a un prix variable par site web, utilisez la logique de priorité du prix (déterminée par [Ordre de tri](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) ).

Pour consulter l’ordre de tri de vos magasins, accédez à **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** dans le _Administration_ barre latérale. Dans le _[!UICONTROL Web Site]_, cliquez sur le nom du site web. Le_[!UICONTROL Web Site Information]_ affiche la page _[!UICONTROL Sort Order]_pour le site web, qui détermine la priorité du site web. Une valeur de `1` indique la priorité la plus élevée.

Si le prix du produit est défini sur `Use Default`, il revient à la valeur de prix par défaut au lieu de la valeur de prix du site web.

## Exemple 1

|  | Priorité du site web | Prix (site web) | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | $31.99 | -- |
| Magasin 1 | 1 | $24.99 | Non |
| Magasin 2 | 2 | $27.99 | Oui |

- Le **[!UICONTROL Magento Price Source]** (défini dans votre [Prix d’énumération](./listing-price.md) est défini sur la valeur `Price` attribut.
- Examinez le site web ayant la priorité la plus élevée, qui est Magasin 1 (défini par la variable [Ordre de tri](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) ).
- Puisque le magasin 1 est configuré pour utiliser le prix du site web (Utiliser par défaut = Non), le prix publié est de 24,99 $.

## Exemple 2

|  | Priorité du site web | Prix du site | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | $31.99 | -- |
| Magasin 1 | 1 | $24.99 | Oui |
| Magasin 2 | 2 | $27.99 | Non |

- Le **[!UICONTROL Magento Price Source]** (défini dans votre [Prix d’énumération](./listing-price.md) est défini sur la valeur `Price` attribut.
- Examinez le site web ayant la priorité la plus élevée, qui est Magasin 1 (défini par la variable [ordre de tri](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) ).
- Depuis le magasin 1 **n’est pas** Pour utiliser le prix du site web (Utiliser par défaut = Oui), consultez le site web suivant dans l’ordre de tri.
- Depuis le magasin 2 **is** définie pour utiliser le prix du site web (Utiliser par défaut = Non), le prix publié est de 27,99 €.

## Exemple 3

|  | Priorité du site web | Prix du site | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | $31.99 | $30.00 |
| Magasin 1 | 1 | $24.99 | -- |
| Magasin 2 | 2 | $27.99 | $20.00 |

Cet exemple ajoute la valeur non-price, qui est utilisée si vous sélectionnez une autre valeur pour le _[!UICONTROL Magento Price Source_] (défini dans votre [Prix d’énumération](./listing-price.md) ). La valeur non-prix utilise toujours le prix comme prix de rechange.

- Le **[!UICONTROL Magento Price Source]** (défini dans [[!UICONTROL Listing Price]](./listing-price.md) ) est défini sur `Non-Price`.
- Examinez le site web ayant la priorité la plus élevée, à savoir : `Store 1`(défini par la variable [Ordre de tri](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) ).
- Depuis le magasin 1 **n’est pas** pour utiliser la variable `Non-Price` , consultez le site web suivant dans l’ordre de tri.
- Depuis le magasin 2 **is** pour utiliser la variable `Non-Price` Attribut (non-prix) [Site Web] = 20,00 $), le prix publié est de 20,00 $.
