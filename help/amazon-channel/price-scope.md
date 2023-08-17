---
title: Canal de vente Amazon - Étendue du prix
description: Utilisez la portée de la tarification de Commerce pour gérer les tarifs en fonction de plusieurs sites web ou à l’échelle mondiale.
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Étendue du prix

[!DNL Commerce] fournit une configuration pour votre [portée des prix](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) à définir sur `Global` ou `Website`. Si la tarification est définie sur `Global`, il existe une source de prix unique pour tous les sites web. Si la tarification est définie sur `Website`, vos sites web peuvent varier leurs tarifs et ont également une valeur de prix par défaut de secours (voir [Étendue du prix](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Si vous modifiez la portée du prix de votre catalogue à partir de `Global` to `Website`, tous les attributs de type de prix changent également en `Website`. Voir [Ajout de sites web](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Lorsqu’un prix est sélectionné, il existe deux sources de prix :

- Prix du site web
- Le prix par défaut (diminuer)

Pour l’intégration du canal de vente Amazon, en fonction de votre [règles de liste](./listing-rules.md), vous pouvez mapper les produits de plusieurs sites web en une seule [!DNL Amazon Marketplace] Pays (défini lors de la [intégration de magasin](./store-integration.md)). Cependant, ce mappage introduit la question de savoir quel prix doit être publié si le produit existe sur plusieurs sites web avec des prix différents.
