---
title: À propos d'Amazon et du catalogue Commerce
description: Le canal de vente Amazon importe vos annonces Amazon dans votre back-end Commerce, et synchronise en permanence avec les produits et les ventes.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# À propos d’Amazon et de [!DNL Commerce] catalogue

Votre serveur principal Adobe Commerce ou Magento Open Source comprend un catalogue avec tous les produits et les paramètres et informations associés (images, options, prix, etc.) et les configurations de commande et d’expédition. Votre [!DNL Amazon Seller Central] compte dispose également d’un catalogue et de configurations de commande, assurant un suivi strict de vos ventes via le [!DNL Amazon Marketplace].

Pour mieux gérer et examiner votre catalogue de produits et vos ventes via un seul emplacement, Amazon Sales Channel importe vos annonces Amazon dans votre [!DNL Commerce] back end, synchronise continuellement avec les produits et les ventes, et signale les problèmes et les tendances. Il prend en charge les intégrations avec plusieurs [!DNL Amazon Seller Central] , en effectuant le suivi de toutes les données via l&#39;interface unique pour plusieurs fronts.

## Attributs de produit

Adobe Commerce et le Magento Open Source gèrent les synchronisations de catalogue avec l’utilisation du produit [attributs](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} pour définir les paramètres et les données du produit. Amazon utilise également des attributs, à mapper via l’intégration. Pendant [tâches de préconfiguration](./amazon-pre-setup-tasks.md) pour le canal de vente Amazon, vous définissez des attributs Amazon supplémentaires (si nécessaire) pour vous assurer que les mises en correspondance de produits lors de l’importation de vos annonces Amazon dans votre [!DNL Commerce] catalogue. Ces attributs incluent UPC, EAN, ISBN et ASIN ([!DNL Amazon Standard Identification Number]). Grâce à l’intégration, les produits sont synchronisés entre Amazon et [!DNL Commerce] à l’aide de vos attributs. Mappage approprié de votre [!DNL Commerce] et les produits Amazon assurent une synchronisation continue des informations sur les produits, des commandes et du stock.

Si ces attributs ne sont pas créés ou configurés pour votre catalogue, vous devez ajouter un [!DNL Commerce] [Attribut de produit](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} et les valeurs de vos produits avant l&#39;intégration. Lorsqu’un attribut Amazon est importé, il peut être utilisé pour la recherche, la navigation, les règles de prix, etc. Pour plus d’informations sur ces attributs, voir [Amazon : Que sont les CUP, les EAN, les ISBN et les ASIN ?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Après l’intégration, vous pouvez gérer et mettre à jour vos attributs de produit et vos mappages Amazon à tout moment.

## Listes de produits

Une annonce Amazon est une page de produits pour chaque produit que vous vendez par l’intermédiaire de la [!DNL Amazon Marketplace], affichant les descriptions de produit, les prix, les images et plus encore mappés par le biais d’attributs. Lors de l’intégration, vous pouvez configurer votre [!DNL Commerce] les produits peuvent être automatiquement publiés dans les annonces Amazon. Vous pouvez également importer vos annonces Amazon existantes en les mappant sur votre [!DNL Commerce] produits.

Lorsque vous avez créé une annonce [!DNL Commerce] produits, ils sont soumis à l&#39;approbation d&#39;Amazon. La plupart des annonces réussies sont approuvées en quelques heures. Si votre annonce est approuvée, elle apparaît dans le fichier [!DNL Amazon Marketplace] pour les commandes immédiates des clients. Le [!DNL Amazon Sales Channel] fournit un ensemble d’onglets pour consulter les annonces Amazon. En fonction du problème ou des données requises, vous devez vérifier votre [!DNL Amazon Seller Central] pour des détails spécifiques sur ces annonces.

- [Actif](./active-listings.md): Répertorie les annonces de produits approuvées disponibles sur le marché.

- [Prêt pour la liste](./ready-to-list.md): Répertorie les produits répondant aux exigences de la réglementation de mise en vente et prêts à être publiés sur Amazon.

- [Inactif](./inactive-listings.md): Répertorie les produits qui ne sont pas disponibles sur le marché en raison d’un blocage pour une raison spécifique (par exemple un problème de marque), d’une fermeture et d’une remise en vente obligatoire, etc.

- [Inéligible](./ineligible-listings.md): En raison des règles de mise en vente, répertorie les produits qui ne peuvent pas être activement répertoriés sur le marché (tels que `0` dates de quantité ou de vente).

- [Incomplet](./incomplete-listings.md): Répertorie les informations requises manquantes pour les produits. Mettez à jour les données du produit pour une autre révision.

- [Terminé](./ended-listings.md): Répertorie les annonces de produits éligibles à la mise en vente mais manuellement supprimées d’Amazon. Vous pouvez remettre ces produits en vente.

## Synchronisation des données

Adobe Commerce et Magento Open Source communiquent les données de produit et de commande entre vos [!DNL Amazon Seller Central] et [!DNL Commerce] backend. Les mises à jour continues fournissent une source unique via [!DNL Commerce] pour gérer et gérer vos stocks, exécuter vos commandes, suivre les ventes et réduire les frais généraux et les doubles emplois. La création de rapports capture les données les plus récentes pour suivre les tendances et résoudre les problèmes de communication entre les deux systèmes.

Toute synchronisation est gérée par une [travail de cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, défini pour une mise à jour toutes les cinq minutes dans votre [Tâches de préconfiguration](./amazon-pre-setup-tasks.md).
