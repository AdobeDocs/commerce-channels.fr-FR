---
title: Portée du prix
description: Utilisez l’étendue de tarification Commerce pour gérer les tarifs en fonction de plusieurs sites Web ou à l’échelle mondiale.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Portée du prix

[!DNL Commerce] fournit la configuration pour votre [étendue des prix](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} à définir sur `Global` ou `Website`. Si la tarification est définie sur `Global`, il existe une source de prix unique pour tous les sites Web. Si la tarification est définie sur `Website`, vos sites Web peuvent varier leurs tarifs et ont également une valeur de prix par défaut de secours. Voir [Prix catalogue](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} dans le guide de l&#39;utilisateur commercial de base.

Si vous modifiez la fourchette de prix du catalogue de `Global` à `Website`, tous les attributs de type de prix changent également en `Website`. Voir [Ajout de sites web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target=&quot;_blank&quot;}.

Lorsque le prix d&#39;un site web est choisi, il existe deux sources de prix :

- Prix du site web
- Le prix par défaut (baisse)

Pour l’intégration du canal de vente Amazon, en fonction de votre [règles d&#39;inscription](./listing-rules.md), vous pouvez mapper des produits de plusieurs sites web en une seule [!DNL Amazon Marketplace] Pays (défini au [intégration de magasin](./store-integration.md)). Toutefois, cette cartographie introduit la question de savoir quel prix doit être publié si le produit existe sur plusieurs sites Web avec des prix différents.
