---
title: Amazon et le catalogue Commerce
description: Le canal de vente Amazon importe vos listes Amazon dans votre serveur principal Commerce et se synchronise en permanence avec les produits et les ventes.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazon et le catalogue [!DNL Commerce]

Votre serveur principal Adobe Commerce ou Magento Open Source comprend un catalogue contenant tous les produits, ainsi que les paramètres et informations associés (images, options, prix, etc.) et les configurations de commande et d’expédition. Votre compte [!DNL Amazon Seller Central] possède également un catalogue et des configurations de commande, qui effectuent un suivi strict de vos ventes par le biais de [!DNL Amazon Marketplace].

Pour mieux gérer et passer en revue votre catalogue de produits et vos ventes au travers d’un emplacement unique, le canal de vente Amazon importe vos listes Amazon dans votre serveur principal [!DNL Commerce], se synchronise en permanence avec les produits et les ventes, et signale les problèmes et tendances. Il prend en charge les intégrations avec plusieurs comptes [!DNL Amazon Seller Central], le suivi de toutes les données par le biais d’une seule interface pour plusieurs storefronts.

## Attributs de produit

Adobe Commerce et Magento Open Source gèrent les synchronisations des catalogues avec l’utilisation des [attributs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) du produit pour définir les paramètres et les données du produit. Amazon utilise également des attributs qui peuvent être mappés par le biais de l’intégration. Lors des [ tâches préalables à la configuration](./amazon-pre-setup-tasks.md) pour le canal de vente Amazon, vous définissez des attributs Amazon supplémentaires (si nécessaire) pour vous assurer que les mappages de produits lors de l’importation de vos listes Amazon dans votre catalogue [!DNL Commerce] sont corrects. Ces attributs incluent CUP, EAN, ISBN et ASIN ([!DNL Amazon Standard Identification Number]). Grâce à l’intégration, les produits sont synchronisés entre les catalogues Amazon et [!DNL Commerce] à l’aide de vos attributs. Un mappage correct de vos produits [!DNL Commerce] et Amazon garantit une synchronisation continue des informations sur les produits, des commandes et de l’inventaire.

Si ces attributs ne sont pas créés ou configurés pour votre catalogue, vous devez ajouter un [!DNL Commerce] [attribut de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) et des valeurs à vos produits avant l’intégration. Lorsqu’un attribut Amazon est importé, il peut être utilisé pour la recherche, la navigation, les règles de prix, etc. Voir [Que signifient ASIN, UPC, EAN, ISBN, SKU et autres codes à barres ?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Après l’intégration, vous pouvez gérer et mettre à jour vos attributs de produit et vos mappages Amazon à tout moment.

## Listes de produits

Une liste Amazon est une page de produits pour chaque produit que vous vendez par le biais de [!DNL Amazon Marketplace], affichant les descriptions de produit, les prix, les images, et d’autres mappés par le biais d’attributs. Lors de l’intégration, vous pouvez configurer vos produits [!DNL Commerce] pour qu’ils soient automatiquement publiés dans les listes Amazon. Vous pouvez également importer vos listes Amazon existantes en les mappant à vos produits [!DNL Commerce].

Lorsque vous avez créé une liste de produits [!DNL Commerce], ils sont envoyés à Amazon pour approbation. La plupart des listes réussies sont approuvées dans les quelques heures qui suivent. Si votre liste est approuvée, elle apparaît dans le [!DNL Amazon Marketplace] pour les commandes immédiates des clients. L’extension [!DNL Amazon Sales Channel] fournit un ensemble d’onglets pour examiner les listes Amazon. En fonction du problème ou des données requises, vous devez consulter votre compte [!DNL Amazon Seller Central] pour obtenir des détails spécifiques sur ces listes.

- [Actif](./active-listings.md) : répertorie les listes de produits approuvées disponibles sur le marché.

- [Prêt à répertorier](./ready-to-list.md) : répertorie les produits qui répondent aux exigences des règles et qui sont prêts à être publiés sur Amazon.

- [Inactif](./inactive-listings.md) : répertorie les produits qui ne sont pas disponibles sur le marché en raison d’un blocage pour une raison spécifique (par exemple, un problème de marque), qui sont fermés et nécessitent une remise en liste, etc.

- [Inéligible](./ineligible-listings.md) : en raison des règles de liste, répertorie les produits qui ne peuvent pas être activement répertoriés sur le marché (par exemple, la quantité `0` ou les dates de vente).

- [Incomplete](./incomplete-listings.md) : répertorie les produits sans les informations requises. Mettez à jour les données de produit pour une autre révision.

- [Ended](./ended-listings.md) : répertorie les listes de produits éligibles à la liste, mais supprimées manuellement d’Amazon. Vous pouvez remettre ces produits en liste.

## Synchronisation des données

Adobe Commerce et Magento Open Source communiquent les données de produit et de commande entre votre compte [!DNL Amazon Seller Central] et le serveur principal [!DNL Commerce]. Les mises à jour constantes fournissent une source unique jusqu’à [!DNL Commerce] pour gérer et gérer vos stocks, respecter les commandes, suivre les ventes et réduire les frais généraux et la duplication du travail. La création de rapports capture les dernières données permettant de suivre les tendances et de résoudre les problèmes de communication détectés entre les deux systèmes.

Toutes les synchronisations sont gérées par une [tâche cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html), définie pour se mettre à jour toutes les cinq minutes dans vos [tâches préalables à la configuration](./amazon-pre-setup-tasks.md).
