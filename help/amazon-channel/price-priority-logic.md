---
title: Logique de priorité des prix
description: Le canal de vente Amazon applique la hiérarchisation pour déterminer le prix publié d'une annonce Amazon.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Logique de priorité des prix

Dans l’exemple suivant, comment le système détermine-t-il si vous devez publier 31,99 $, 24,99 $ ou 27,99 $ ?

![Portée du prix du commerce](assets/amazon-price-scope.png)

Pour déterminer quel prix est utilisé si un produit se trouve sur deux sites Web et a un prix variable par site Web, utilisez la logique de priorité de prix (déterminée par [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valeur).

Pour afficher l’ordre de tri de vos magasins, accédez à la section **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** dans la _Administrateur_ barre latérale. Dans la boîte de dialogue _[!UICONTROL Web Site]_, cliquez sur le nom du site web. Le_[!UICONTROL Web Site Information]_ affiche la _[!UICONTROL Sort Order]_pour le site web, qui détermine la priorité du site web. Une valeur de `1` indique la priorité la plus élevée.

Si le prix du produit est défini sur `Use Default`, il revient à la valeur de prix par défaut au lieu de la valeur de prix du site web.

## Exemple 1

|  | Priorité du site Web | Prix (Site Web) | Utiliser par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | — |
| Boutique 1 | 1 | 24,99 $ | Non |
| Store 2 | 2 | 27,99 $ | Oui |

- Le **[!UICONTROL Magento Price Source]** (défini dans votre [Prix d&#39;annonce](./listing-price.md) est défini sur `Price` .
- Regardez le site web ayant la priorité la plus élevée, qui est Store 1 (défini par le [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valeur).
- Puisque la Boutique 1 est configurée pour utiliser le prix du site Web (Utiliser la valeur par défaut = Non), le prix publié est de 24,99 $.

## Exemple 2

|  | Priorité du site Web | Site Web Prix | Utiliser par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | — |
| Boutique 1 | 1 | 24,99 $ | Oui |
| Store 2 | 2 | 27,99 $ | Non |

- Le **[!UICONTROL Magento Price Source]** (défini dans votre [Prix d&#39;annonce](./listing-price.md) est défini sur `Price` .
- Regardez le site web ayant la priorité la plus élevée, qui est Store 1 (défini par le [ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valeur).
- Depuis la Boutique 1 **n&#39;est pas** pour utiliser le prix du site web (Utiliser la valeur par défaut = Oui), consultez le site web suivant dans l’ordre de tri.
- Depuis la boutique 2 **est** défini pour utiliser le prix du site web (Utiliser la valeur par défaut = Non), le prix publié est de 27,99 $.

## Exemple 3

|  | Priorité du site Web | Site Web Prix | Utiliser par défaut |
|---|---|---|---|
| Par défaut | 0 | 31,99 $ | 30,00 $ |
| Boutique 1 | 1 | 24,99 $ | — |
| Store 2 | 2 | 27,99 $ | 20,00 $ |

Cet exemple montre comment ajouter la valeur hors prix, qui est utilisée si vous sélectionnez une autre valeur pour le _[!UICONTROL Magento Price Source_] (défini dans votre [Prix d&#39;annonce](./listing-price.md) ). La valeur hors prix utilise toujours le prix comme prix de secours.

- Le **[!UICONTROL Magento Price Source]** (défini dans votre [[!UICONTROL Listing Price]](./listing-price.md) ) est défini sur `Non-Price`.
- Regardez le site web ayant la priorité la plus élevée, qui est `Store 1`(défini par la propriété [Ordre de tri](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} valeur).
- Depuis la Boutique 1 **n&#39;est pas** pour utiliser la `Non-Price` , regardez le site web suivant dans l’ordre de tri.
- Depuis la boutique 2 **est** pour utiliser la `Non-Price` attribut (Non-Price [Site] = 20,00 $), le prix publié est de 20,00 $.
