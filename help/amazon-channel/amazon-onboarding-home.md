---
title: Amazon Sales Channel intégré
description: 'Découvrez les tâches préconfigurées, les étapes d’intégration et le fonctionnement d’Amazon avec Amazon Sales Channel dans Adobe Commerce et Magento Open Source.'
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html: 
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# Canal de vente Amazon intégré

Cette section décrit les tâches préconfigurées, les étapes d’intégration et quelques concepts clés du fonctionnement d’Amazon avec le canal de vente Amazon dans Adobe Commerce et Magento Open Source.

L’extension [!DNL Amazon Sales Channel] prend en charge plusieurs magasins Amazon. Pour un seul compte [!DNL Amazon Seller Central] qui fonctionne dans la région Amazon États-Unis/Canada/Mexique, créez trois magasins Amazon (un pour les ventes aux États-Unis, les ventes au Mexique et les ventes au Canada). Chacune des trois boutiques définit le pays du marché lors de sa création. Si vous disposez de plusieurs comptes [!DNL Amazon Seller Central], vous pouvez avoir jusqu’à trois boutiques Amazon pour chacun de vos comptes [!DNL Amazon Seller Central]. Si vous vendez aussi au Royaume-Uni, vous avez un quatrième magasin Amazon.

>[!TIP]
>
>Un [compte de vendeur professionnel](https://sell.amazon.com/){target=&quot;_blank&quot;} sur [!DNL Amazon Seller Central] dans la région Amérique du Nord ou Europe (Royaume-Uni) est requis. Amazon facture un abonnement mensuel et des frais pour la vente. Voir [Amazon : Choisissez votre plan de vente](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>L’intégration est simple : créez votre boutique, puis connectez-la à votre compte [!DNL Amazon Seller Central].
>Lorsque votre magasin est connecté, le canal Amazon tente d’importer vos listes Amazon et de les faire correspondre à votre catalogue, en fonction de votre [mappage d’attributs](./attributes-view.md).<br><br>
>Les paramètres de canal de vente Amazon affectent vos listes Amazon. Les paramètres initiaux de mise en liste, de tarification et de produit sont par défaut pour vous. Vous pouvez modifier les [paramètres de magasin](./ob-store-review.md) (liste, prix, commande et création de rapports) une fois que votre magasin est connecté à votre compte [!DNL Amazon Seller Central].

| Étapes | Ce qui se passe |
|--- |--- |
| [Tâches préalables à la configuration](./amazon-pre-setup-tasks.md) | Avant d’embarquer, vous devez vous assurer que vous disposez d’un compte [!DNL Amazon Seller Central] principal et approuvé. Il existe également quelques [!DNL Commerce] exigences et recommandations à remplir avant l’intégration. |
| [Vérification de la clé API Amazon](./amazon-verify-api-key.md) | Lors de l’accès au canal de vente Amazon, [!DNL Commerce] vérifie et valide automatiquement la clé d’API Amazon que vous avez ajoutée dans votre configuration de magasin. Si votre clé API n’a pas été ajoutée ou n’est pas valide, vous êtes invité à [ajouter ou mettre à jour votre clé API Amazon](./amazon-verify-api-key.md). |
| [Intégration de magasin](./store-integration.md) | Cette étape comprend la création d’une boutique de canaux de vente Amazon, puis sa connexion à votre compte [!DNL Amazon Seller Central]. Pour cette étape, vous avez besoin des Principales informations d’identification de connexion pour votre compte [!DNL Amazon Seller Central] (l’adresse électronique ou le téléphone utilisé pour créer le compte de vendeur). |
| [Créer une règle de liste](./ob-create-listing-rule.md) | Une fois que vous avez connecté votre boutique de canaux de vente Amazon, vous êtes invité à créer une règle de mise en vente. Cette étape est recommandée, mais vous pouvez également l’ignorer pour lancer le processus d’importation des listes. Vous pouvez également accéder à vos [paramètres de magasin et de liste](./ob-store-review.md) dans le [tableau de bord](./amazon-store-dashboard.md) du magasin. |
