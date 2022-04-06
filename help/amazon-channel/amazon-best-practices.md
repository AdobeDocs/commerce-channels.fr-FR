---
title: Bonnes pratiques et limites du canal de vente Amazon
description: Examinez les bonnes pratiques et les limites lors de l’utilisation du canal de vente Amazon pour Adobe Commerce et Magento Open Source.
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Bonnes pratiques et limites du canal de vente Amazon

Les bonnes pratiques sont les suivantes :

- Le canal de vente Amazon peut affecter vos listes Amazon en augmentant ou en diminuant les prix, en synchronisant les informations sur les produits (y compris les stocks disponibles) et en ajoutant, mettant à jour et en supprimant des listes. Vérifiez vos listes par statut lors de la configuration et ajustez vos paramètres ([paramètres de liste](./listing-settings.md), [règles de liste](./listing-rules.md), [règles de tarification](./pricing-products.md), [overrides](./overrides.md), etc.) avant de terminer la configuration du magasin. Ces paramètres peuvent également être modifiés après la configuration, si nécessaire.

- Le canal de vente Amazon peut définir vos règles de prix afin d’ajuster automatiquement le prix de votre offre. Les protections de prix automatisées incluent : [prix plancher](./floor-price.md) et [prix plafond facultatif](./optional-ceiling-price.md) fonctions de [Règles de retarification intelligentes](./intelligent-repricing-rules.md). L’utilisation de ces protections permet de s’assurer que les prix de vos listes ne vont pas en dessous de votre coût ou au-dessus d’un prix défini.

- La synchronisation des données entre le canal de vente Amazon et Amazon est contrôlée par votre [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html)Paramètres {target=&quot;_blank&quot;}. Ralentissement intégré entre [!DNL Commerce] et Amazon permet d’assurer une transmission des données fluide et efficace, mais pendant les temps de trafic élevés d’e-commerce (Noël, par exemple), les systèmes d’Amazon peuvent prendre plus de temps que d’habitude pour se mettre à jour. Définissez vos [!DNL Commerce] cron à exécuter toutes les cinq minutes.

- Le canal de vente Amazon importe les informations de commande Amazon. Pour gérer vos commandes Amazon dans le canal de vente Amazon, vous devez vous assurer que votre [paramètres de commande](./order-settings.md) sont définies pour importer et créer un [!DNL Commerce] commande pour chaque commande Amazon. Si elle n’est pas définie, vous pouvez uniquement afficher les informations de commande Amazon. Toutes les taxes pour les ventes via Amazon sont toujours gérées et remises via votre [!DNL Amazon Seller Central] compte . Dans certains États, Amazon est tenu de collecter et de transférer automatiquement les impôts. Pour les autres états, les vendeurs ont la possibilité de calculer les taxes manuellement ou automatiquement. Voir [Amazon : Stratégies fiscales](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}. Vous devrez peut-être vous connecter à votre [!DNL Amazon Seller Central] pour afficher la documentation sur la politique fiscale d’Amazon.

- Pour les régions du Royaume-Uni, il est recommandé de s’inscrire au [Service de calcul de la TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;} avant d’intégrer le canal de vente Amazon.


   >[!NOTE]
   >
   >Il peut s’écouler entre 10 et 14 jours avant qu’Amazon ne vérifie et n’active votre compte de service de calcul de la TVA.

Les restrictions incluent :

- Les types de produits regroupés, les cartes de cadeaux et les lots qui font partie de votre [!DNL Commerce] Les catalogues ne sont pas pris en charge par le canal de vente Amazon pour être répertoriés dans Amazon.

- Le canal de vente Amazon ne peut pas créer de liste pour un produit qui n’a pas de liste Amazon existante ou précédente. Si un produit n’existe pas dans [!DNL Amazon Seller Central] avec un ASIN, il doit être ajouté dans [!DNL Amazon Seller Central] afin qu’Amazon puisse attribuer un ASIN au produit. Une fois qu’un produit est ajouté dans Amazon et qu’une liste est créée, la liste peut être mise en correspondance avec votre catalogue dans le canal de vente Amazon et synchronisée.
