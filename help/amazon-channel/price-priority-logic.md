---
title: Logique de priorité des prix
description: Le canal de vente Amazon applique la hiérarchisation pour déterminer le prix publié pour une liste Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Logique de priorité des prix

Dans l’exemple suivant, comment le système détermine-t-il si vous souhaitez publier pour 31,99 $, 24,99 $ ou 27,99 $ ?

![Étendue des prix du commerce](assets/amazon-price-scope.png)

Pour déterminer le prix utilisé si un produit se trouve sur deux sites web et a un prix variable par site web, utilisez la logique de priorité du prix (déterminée par la valeur [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).

Pour afficher l’ordre de tri de vos magasins, accédez à **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** dans la barre latérale _Admin_. Dans la colonne _[!UICONTROL Web Site]_, cliquez sur le nom du site Web. La page_[!UICONTROL Web Site Information]_ affiche le paramètre _[!UICONTROL Sort Order]_du site web, qui détermine la priorité du site web. Une valeur `1` indique la priorité la plus élevée.

Si le prix du produit est défini sur `Use Default`, il revient à la valeur de prix par défaut au lieu de la valeur de prix du site web.

## Exemple 1

|  | Priorité du site web | Prix (site web) | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | — |
| Magasin 1 | 1 | 24,99 $ | Non |
| Magasin 2 | 2 | 27,99 $ | Oui |

- La valeur **[!UICONTROL Magento Price Source]** (définie dans votre [Prix de la liste](./listing-price.md) est définie sur l’attribut `Price`.
- Examinez le site web ayant la priorité la plus élevée sur le site web, qui est Store 1 (défini par la valeur [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} ).
- Puisque le magasin 1 est configuré pour utiliser le prix du site web (Utiliser par défaut = Non), le prix publié est de 24,99 $.

## Exemple 2

|  | Priorité du site web | Prix du site | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | — |
| Magasin 1 | 1 | 24,99 $ | Oui |
| Magasin 2 | 2 | 27,99 $ | Non |

- La valeur **[!UICONTROL Magento Price Source]** (définie dans votre [Prix de la liste](./listing-price.md) est définie sur l’attribut `Price`.
- Examinez le site web ayant la priorité la plus élevée sur le site web, qui est Store 1 (défini par la valeur [sort order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} ).
- Comme le magasin 1 **n’est pas** défini pour utiliser le prix du site web (Utiliser par défaut = Oui), consultez le site web suivant dans l’ordre de tri.
- Comme Magasin 2 **est** défini pour utiliser le prix du site web (Utiliser la valeur par défaut = Non), le prix publié est de 27,99 $.

## Exemple 3

|  | Priorité du site web | Prix du site | Utiliser la valeur par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | 30,00 $ |
| Magasin 1 | 1 | 24,99 $ | — |
| Magasin 2 | 2 | 27,99 $ | 20,00 $ |

Cet exemple ajoute la valeur non-price, qui est utilisée si vous sélectionnez une autre valeur pour le _[!UICONTROL Magento Price Source_] (définie dans vos paramètres [Prix d’énumération](./listing-price.md)). La valeur non-prix utilise toujours le prix comme prix de rechange.

- **[!UICONTROL Magento Price Source]** (défini dans vos paramètres [[!UICONTROL Listing Price]](./listing-price.md)) est défini sur `Non-Price`.
- Examinez le site web ayant la priorité la plus élevée sur le site web, qui est `Store 1` (défini par la valeur [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Comme le magasin 1 **n’est pas** défini pour utiliser l’attribut `Non-Price`, consultez le site web suivant dans l’ordre de tri.
- Puisque le magasin 2 **est** défini pour utiliser l’attribut `Non-Price` (Non-Price [Website] = 20,00 $), le prix publié est de 20,00 $.
