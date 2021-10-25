---
title: Meilleures pratiques et limites pour le canal de vente Amazon
description: Examinez les meilleures pratiques et les limites lors de l’utilisation du canal de vente Amazon pour Adobe Commerce et Magento Open Source.
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Meilleures pratiques et limites pour le canal de vente Amazon

Les meilleures pratiques sont les suivantes :

- Le canal de vente Amazon peut affecter vos annonces Amazon en augmentant ou en diminuant les prix, en synchronisant les informations sur les produits (y compris le stock disponible) et en ajoutant, mettant à jour et en finissant (supprimant) les annonces. Passez en revue vos annonces par statut lors de votre configuration et ajustez vos paramètres ([paramètres de liste](./listing-settings.md), [règles d&#39;inscription](./listing-rules.md), [règles de tarification](./pricing-products.md), [remplacements](./overrides.md), etc.) avant de terminer la configuration de votre magasin. Ces paramètres peuvent également être modifiés après la configuration, si nécessaire.

- Le canal de vente Amazon peut définir vos règles de tarification pour ajuster automatiquement le prix de votre annonce. Les garanties de tarification automatisées comprennent : [prix plancher](./floor-price.md) et [prix plafond facultatif](./optional-ceiling-price.md) caractéristiques [Règles de réévaluation intelligentes](./intelligent-repricing-rules.md). L’utilisation de ces mesures de protection permet de s’assurer que les prix de votre annonce ne sont pas inférieurs à votre coût ou supérieurs à un prix défini.

- La synchronisation des données entre le canal de vente Amazon et Amazon est contrôlée par votre [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html)Paramètres {target=&quot;_blank&quot;}. Limitation intégrée entre [!DNL Commerce] et Amazon contribue à assurer une transmission de données fluide et efficace, mais pendant les temps de trafic élevés du commerce électronique (comme le Black Friday), les systèmes Amazon pourraient prendre plus de temps que d’habitude pour se mettre à jour. Définir [!DNL Commerce] cron à courir toutes les cinq minutes.

- Le canal de vente Amazon importe vos informations de commande Amazon. Pour gérer vos commandes Amazon dans le canal de vente Amazon, vous devez vous assurer que votre [paramètres de commande](./order-settings.md) sont définis pour importer et créer un [!DNL Commerce] pour chaque commande Amazon. Si elle n’est pas définie, vous pouvez uniquement afficher les informations de commande Amazon. Toutes les taxes pour les ventes via Amazon sont toujours gérées et remises via votre [!DNL Amazon Seller Central] compte. Dans certains États, Amazon est tenue de percevoir et de remettre automatiquement les impôts. Pour les autres États, les vendeurs ont la possibilité de calculer les taxes manuellement ou automatiquement. Voir [Amazon : Politiques fiscales](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}. Vous devrez peut-être vous connecter à votre [!DNL Amazon Seller Central] pour afficher la documentation de la stratégie fiscale Amazon.

- Pour les régions du Royaume-Uni, il est recommandé de s’inscrire au [Service de calcul de TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;} avant d&#39;intégrer le canal de vente Amazon.


   >[!NOTE]
   >
   >Il peut prendre entre 10 et 14 jours pour qu’Amazon vérifie et active votre compte de service de calcul de la TVA.

Les restrictions sont les suivantes :

- Offre groupée, carte cadeau et types de produits groupés faisant partie de votre [!DNL Commerce] ne sont pas pris en charge par le canal de vente Amazon pour la mise en vente vers Amazon.

- Le canal de vente Amazon ne peut pas créer une annonce pour un produit qui n&#39;a pas de liste Amazon existante ou précédente. Si un produit n’existe pas dans [!DNL Amazon Seller Central] avec un ASIN, il doit être ajouté dans [!DNL Amazon Seller Central] pour qu’Amazon puisse affecter un ASIN au produit. Une fois qu’un produit est ajouté dans Amazon et qu’une annonce est créée, la mise en vente peut être mise en correspondance avec votre catalogue dans le canal de vente Amazon et synchronisée.
