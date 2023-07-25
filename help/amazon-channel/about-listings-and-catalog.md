---
title: Amazon et le catalogue de commerce
description: Le canal de vente Amazon importe vos listes Amazon dans votre serveur principal Commerce et se synchronise en permanence avec les produits et les ventes.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalogs
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Amazon et la variable [!DNL Commerce] Catalogue

Votre serveur principal Adobe Commerce ou Magento Open Source comprend un catalogue contenant tous les produits, ainsi que les paramètres et informations associés (images, options, prix, etc.) et les configurations de commande et d’expédition. Votre [!DNL Amazon Seller Central] Ce compte comporte également des configurations de catalogue et de commande, qui effectuent un suivi strict de vos ventes par le biais de la variable [!DNL Amazon Marketplace].

Pour mieux gérer et revoir votre catalogue de produits et vos ventes au moyen d’un seul emplacement, le canal de vente Amazon importe vos listes Amazon dans votre [!DNL Commerce] back-end, se synchronise en permanence avec les produits et les ventes, et consigne les problèmes et tendances. Il prend en charge les intégrations avec plusieurs [!DNL Amazon Seller Central] comptes, suivi de toutes les données par le biais de l’interface unique pour plusieurs storefronts.

## Attributs de produit

Adobe Commerce et Magento Open Source gèrent les synchronisations des catalogues avec l’utilisation du produit [Attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) pour définir les paramètres et les données du produit. Amazon utilise également des attributs qui peuvent être mappés par le biais de l’intégration. Durant [tâches de préconfiguration](./amazon-pre-setup-tasks.md) pour le canal de vente Amazon, vous définissez des attributs Amazon supplémentaires (si nécessaire) pour vous assurer que les mappages de produits lors de l’importation de vos listes Amazon dans votre [!DNL Commerce] catalogue. Ces attributs incluent CUP, EAN, ISBN et ASIN ([!DNL Amazon Standard Identification Number]). Grâce à l’intégration, la synchronisation des produits entre Amazon et [!DNL Commerce] catalogues utilisant vos attributs. Mappage approprié de votre [!DNL Commerce] et les produits Amazon assurent une synchronisation continue des informations sur les produits, des commandes et des stocks.

Si ces attributs ne sont pas créés ou configurés pour votre catalogue, vous devez ajouter une [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) et de vos produits avant l’intégration. Lorsqu’un attribut Amazon est importé, il peut être utilisé pour la recherche, la navigation, les règles de prix, etc. Voir [Que signifient ASIN, UPC, EAN, ISBN, SKU et autres codes à barres ?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Après l’intégration, vous pouvez gérer et mettre à jour vos attributs de produit et vos mappages Amazon à tout moment.

## Listes de produits

Une liste Amazon est une page de produits pour chaque produit que vous vendez par l’intermédiaire de la variable [!DNL Amazon Marketplace], affichant les descriptions de produits, les prix, les images, etc. mappés à l’aide d’attributs . Lors de l’intégration, vous pouvez configurer votre [!DNL Commerce] les produits peuvent être automatiquement publiés dans les listes Amazon. Vous pouvez également importer vos listes Amazon existantes en les mappant sur vos [!DNL Commerce] produits.

Lorsque vous avez créé une liste [!DNL Commerce] produits, ils sont envoyés à Amazon pour approbation. La plupart des listes réussies sont approuvées dans les quelques heures qui suivent. Si votre liste est approuvée, elle apparaît dans la variable [!DNL Amazon Marketplace] pour les commandes immédiates des clients. Le [!DNL Amazon Sales Channel] L’extension fournit un ensemble d’onglets permettant de consulter les listes Amazon. En fonction du problème ou des données requises, vous devez consulter [!DNL Amazon Seller Central] pour obtenir des détails spécifiques sur ces listes.

- [Principal](./active-listings.md): Répertorie les listes de produits approuvées disponibles sur le marché.

- [Prêt à répertorier](./ready-to-list.md): Répertorie les produits répondant aux exigences des règles de liste et prêts à être publiés dans Amazon.

- [Inactif](./inactive-listings.md): Répertorie les produits qui ne sont pas disponibles sur le marché en raison d’un blocage pour une raison spécifique (comme un problème de marque), d’une fermeture et d’une réinscription obligatoire, etc.

- [Inéligible](./ineligible-listings.md): En raison des règles de liste, répertorie les produits qui ne peuvent pas être activement répertoriés sur le marché (tels que `0` dates de vente ou de quantité).

- [Incomplet](./incomplete-listings.md): Répertorie les produits sans les informations requises. Mettez à jour les données de produit pour une autre révision.

- [Terminé](./ended-listings.md): Répertorie les listes de produits éligibles à la liste, mais supprimées manuellement d’Amazon. Vous pouvez remettre ces produits en liste.

## Synchronisation des données

Adobe Commerce et Magento Open Source communiquent les données de produit et de commande entre vos [!DNL Amazon Seller Central] et la variable [!DNL Commerce] back-end. Les mises à jour continues fournissent une source unique via [!DNL Commerce] pour gérer et gérer vos stocks, répondre aux commandes, suivre les ventes et réduire les frais généraux et la duplication du travail. La création de rapports capture les dernières données permettant de suivre les tendances et de résoudre les problèmes de communication détectés entre les deux systèmes.

Toute la synchronisation est gérée par une [tâche cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html), définissez sur mettre à jour toutes les cinq minutes dans votre [Tâches préalables à la configuration](./amazon-pre-setup-tasks.md).
