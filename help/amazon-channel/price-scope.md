---
title: Étendue du prix
description: Utilisez la portée de la tarification de Commerce pour gérer les tarifs en fonction de plusieurs sites web ou à l’échelle mondiale.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Étendue du prix

[!DNL Commerce] fournit une configuration pour que le périmètre de votre  [tarification](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} soit défini sur  `Global` ou  `Website`. Si le prix est défini sur `Global`, il existe une source de prix unique pour tous les sites Web. Si le prix est défini sur `Website`, vos sites web peuvent varier le prix de leur site et ont également une valeur de prix par défaut de secours. Voir [Prix du catalogue](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} dans le guide d’utilisation de base de Commerce.

Si vous remplacez la portée de prix de votre catalogue de `Global` par `Website`, tous les attributs de type de prix sont également modifiés en `Website`. Voir [Ajout de sites web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target=&quot;_blank&quot;}.

Lorsqu’un prix est sélectionné, il existe deux sources de prix :

- Prix du site web
- Prix par défaut (de la baisse)

Pour l’intégration du canal de vente Amazon, en fonction de vos [règles de liste](./listing-rules.md), vous pouvez mapper les produits de plusieurs sites web dans un seul [!DNL Amazon Marketplace] pays (défini lors de l’[intégration de magasin](./store-integration.md)). Cependant, ce mappage introduit la question de savoir quel prix doit être publié si le produit existe sur plusieurs sites web avec des prix différents.
