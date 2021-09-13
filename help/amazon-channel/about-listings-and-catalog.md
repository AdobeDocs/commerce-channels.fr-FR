---
title: À propos d’Amazon et du catalogue de commerce
description: Le canal de vente Amazon importe vos listes Amazon dans votre serveur principal Commerce et se synchronise en permanence avec les produits et les ventes.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# À propos d’Amazon et du catalogue [!DNL Commerce]

Votre serveur principal Commerce ou Magento Open Source Adobe comprend un catalogue contenant tous les produits et les paramètres et informations associés (images, options, prix, etc.), ainsi que les configurations de commande et d’expédition. Votre compte [!DNL Amazon Seller Central] comporte également un catalogue et des configurations de commande, qui effectuent un suivi strict de vos ventes par le biais de [!DNL Amazon Marketplace].

Pour mieux gérer et passer en revue votre catalogue de produits et vos ventes au moyen d’un seul emplacement, le canal de vente Amazon importe vos listes Amazon dans votre [!DNL Commerce] serveur principal, se synchronise en permanence avec les produits et les ventes et signale les problèmes et tendances. Il prend en charge les intégrations avec plusieurs comptes [!DNL Amazon Seller Central], assurant le suivi de toutes les données par le biais d’une seule interface pour plusieurs storefronts.

## Attributs de produit

Adobe Commerce et Magento Open Source gèrent les synchronisations des catalogues avec l’utilisation des [attributs](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} du produit pour définir les paramètres et les données du produit. Amazon utilise également des attributs qui peuvent être mappés par le biais de l’intégration. Lors des [tâches préalables à la configuration](./amazon-pre-setup-tasks.md) pour le canal de vente Amazon, vous définissez des attributs Amazon supplémentaires (si nécessaire) pour vous assurer que les mappages de produits lors de l’importation de vos listes Amazon dans votre catalogue [!DNL Commerce] sont corrects. Ces attributs incluent CUP, EAN, ISBN et ASIN ([!DNL Amazon Standard Identification Number]). Grâce à l’intégration, les produits sont synchronisés entre Amazon et les catalogues [!DNL Commerce] à l’aide de vos attributs. Un mappage correct de vos produits [!DNL Commerce] et Amazon garantit une synchronisation continue des informations sur les produits, des commandes et de l’inventaire.

Si ces attributs ne sont pas créés ou configurés pour votre catalogue, vous devez ajouter un [!DNL Commerce] [attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} et des valeurs à vos produits avant l’intégration. Lorsqu’un attribut Amazon est importé, il peut être utilisé pour la recherche, la navigation, les règles de prix, etc. Pour plus d’informations sur ces attributs, voir [Amazon : Que sont les CUP, EAN, ISBN et ASIN ?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Après l’intégration, vous pouvez gérer et mettre à jour vos attributs de produit et vos mappages Amazon à tout moment.

## Listes de produits

Une liste Amazon est une page de produits pour chaque produit que vous vendez par l’intermédiaire de [!DNL Amazon Marketplace], qui affiche les descriptions, les prix, les images et d’autres éléments mappés par le biais d’attributs. Lors de l’intégration, vous pouvez configurer vos [!DNL Commerce] produits qui peuvent être automatiquement publiés dans les listes Amazon. Vous pouvez également importer vos listes Amazon existantes en les mappant à vos produits [!DNL Commerce].

Lorsque vous avez créé une liste de produits [!DNL Commerce], ils sont envoyés à Amazon pour approbation. La plupart des listes réussies sont approuvées dans les quelques heures qui suivent. Si votre liste est approuvée, elle apparaît dans la section [!DNL Amazon Marketplace] pour les commandes immédiates des clients. L’extension [!DNL Amazon Sales Channel] fournit un ensemble d’onglets permettant de passer en revue les listes Amazon. Selon le problème ou les données requises, vous devez consulter votre compte [!DNL Amazon Seller Central] pour obtenir des détails spécifiques sur ces listes.

- [Principal](./active-listings.md) : Répertorie les listes de produits approuvées disponibles sur le marché.

- [Ready to List](./ready-to-list.md) : Répertorie les produits répondant aux exigences des règles de liste et prêts à être publiés dans Amazon.

- [Inactif](./inactive-listings.md) : Répertorie les produits qui ne sont pas disponibles sur le marché en raison d’un blocage pour une raison spécifique (comme un problème de marque), d’une fermeture et d’une réinscription obligatoire, etc.

- [Inéligible](./ineligible-listings.md) : En raison des règles de liste, répertorie les produits qui ne peuvent pas être activement répertoriés sur le marché (dates de  `0` vente ou de quantité, par exemple).

- [Incomplet](./incomplete-listings.md) : Répertorie les produits sans les informations requises. Mettez à jour les données de produit pour une autre révision.

- [Fin](./ended-listings.md) : Répertorie les listes de produits éligibles à la liste, mais supprimées manuellement d’Amazon. Vous pouvez remettre ces produits en liste.

## Synchronisation des données

Adobe Commerce et Magento Open Source communiquent les données de produit et de commande entre votre compte [!DNL Amazon Seller Central] et le serveur principal [!DNL Commerce]. Les mises à jour continues fournissent une source unique par le biais de [!DNL Commerce] pour gérer et gérer vos stocks, respecter les commandes, suivre les ventes et réduire les frais généraux et les doublons de travail. La création de rapports capture les dernières données permettant de suivre les tendances et de résoudre les problèmes de communication détectés entre les deux systèmes.

Toute synchronisation est gérée par une [tâche cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, définie pour mettre à jour toutes les cinq minutes dans vos [tâches préalables à la configuration](./amazon-pre-setup-tasks.md).
