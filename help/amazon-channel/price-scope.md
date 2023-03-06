---
title: Étendue du prix
description: Utilisez la portée de la tarification de Commerce pour gérer les tarifs en fonction de plusieurs sites web ou à l’échelle mondiale.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Étendue du prix

[!DNL Commerce] fournit une configuration pour votre [portée des prix](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} dans le guide d’utilisation de Commerce principal.

Si vous modifiez la portée du prix de votre catalogue à partir de `Global` to `Website`, tous les attributs de type de prix changent également en `Website`. Voir [Ajout de sites web](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

Lorsqu’un prix est sélectionné, il existe deux sources de prix :

- Prix du site web
- Le prix par défaut (diminuer)

Pour l’intégration du canal de vente Amazon, en fonction de votre [règles de liste](./listing-rules.md), vous pouvez mapper les produits de plusieurs sites web en une seule [!DNL Amazon Marketplace] Pays (défini lors de la [intégration de magasin](./store-integration.md)). Cependant, ce mappage introduit la question de savoir quel prix doit être publié si le produit existe sur plusieurs sites web avec des prix différents.
