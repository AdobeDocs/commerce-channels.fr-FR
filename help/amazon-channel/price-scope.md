---
title: Étendue du prix
description: Utilisez la portée de la tarification de Commerce pour gérer les tarifs en fonction de plusieurs sites web ou à l’échelle mondiale.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Étendue du prix

[!DNL Commerce] fournit une configuration pour votre [portée des prix](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} à définir sur `Global` ou `Website`. Si la tarification est définie sur `Global`, il existe une source de prix unique pour tous les sites web. Si la tarification est définie sur `Website`, vos sites web peuvent varier leurs tarifs et ont également une valeur de prix par défaut de secours. Voir [Prix du catalogue](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} dans le guide de l’utilisateur Commerce principal.

Si vous modifiez la portée du prix de votre catalogue à partir de `Global` to `Website`, tous les attributs de type de prix changent également en `Website`. Voir [Ajout de sites web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target=&quot;_blank&quot;}.

Lorsqu’un prix est sélectionné, il existe deux sources de prix :

- Prix du site web
- Le prix par défaut (diminuer)

Pour l’intégration du canal de vente Amazon, en fonction de votre [règles de liste](./listing-rules.md), vous pouvez mapper les produits de plusieurs sites web en une seule [!DNL Amazon Marketplace] Pays (défini lors de la [intégration de magasin](./store-integration.md)). Cependant, ce mappage introduit la question de savoir quel prix doit être publié si le produit existe sur plusieurs sites web avec des prix différents.
