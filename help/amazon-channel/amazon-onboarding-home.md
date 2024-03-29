---
title: "Onboard [!DNL Amazon Sales Channel]"
description: Découvrez les tâches préconfigurées, les étapes d’intégration et le fonctionnement d’Amazon avec Amazon Sales Channel dans Adobe Commerce et Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Onboard [!DNL Amazon Sales Channel]

Cette section décrit les tâches préalables à la configuration, les étapes à suivre pour l’intégration et quelques concepts clés du fonctionnement d’Amazon avec le canal de vente Amazon dans Adobe Commerce et Magento Open Source.

La variable [!DNL Amazon Sales Channel] prend en charge plusieurs magasins Amazon. Pour un seul [!DNL Amazon Seller Central] qui opère dans la région États-Unis/Canada/Mexique d’Amazon, créez trois boutiques Amazon (une pour les ventes aux États-Unis, les ventes au Mexique et les ventes au Canada). Chacune des trois boutiques définit le pays du marché lors de sa création. Si vous en avez plusieurs [!DNL Amazon Seller Central] compte, vous pouvez avoir jusqu’à trois boutiques Amazon pour chacune de vos [!DNL Amazon Seller Central] comptes. Si vous vendez aussi au Royaume-Uni, vous avez un quatrième magasin Amazon.

>[!TIP]
>
>A [Compte de vendeur professionnel](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>L’intégration est simple : créez votre boutique, puis connectez-la à votre [!DNL Amazon Seller Central] compte .
>Lorsque votre boutique est connectée, le canal Amazon tente d’importer vos listes Amazon et de les faire correspondre à votre catalogue, en fonction de vos [mappage d’attributs](./attributes-view.md).<br><br>
>Les paramètres de canal de vente Amazon affectent vos listes Amazon. Les paramètres initiaux de mise en liste, de tarification et de produit sont par défaut pour vous. Vous pouvez modifier votre [paramètres de magasin](./ob-store-review.md) (mise en liste, tarification, commande et création de rapports) une fois votre boutique connectée à votre [!DNL Amazon Seller Central] compte .

| Étapes | Ce qui se passe |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tâches préalables à la configuration](./amazon-pre-setup-tasks.md) | Avant d’embarquer, vous devez vous assurer que vous disposez d’un [!DNL Amazon Seller Central] compte . Il y en a aussi quelques [!DNL Commerce] conditions requises et recommandations à remplir avant l’intégration. |
| [Vérification de la clé API Amazon](./amazon-verify-api-key.md) | Lors de l’accès au canal de vente Amazon, [!DNL Commerce] vérifie et valide automatiquement la clé d’API Amazon que vous avez ajoutée dans la configuration de votre magasin. Si votre clé API n’a pas été ajoutée ou n’est pas valide, vous êtes invité à [Ajout ou mise à jour de votre clé API Amazon](./amazon-verify-api-key.md). |
| [Intégration de magasin](./store-integration.md) | Cette étape comprend la création d’une boutique de canaux de vente Amazon, puis sa connexion à votre [!DNL Amazon Seller Central] compte . Vous avez besoin des informations d’identification de connexion principales pour votre [!DNL Amazon Seller Central] compte (adresse électronique ou téléphone utilisée pour créer le compte de vendeur) pour cette étape. |
| [Créer une règle de liste](./ob-create-listing-rule.md) | Une fois que vous avez connecté votre boutique de canaux de vente Amazon, vous êtes invité à créer une règle de mise en vente. Cette étape est recommandée, mais vous pouvez également l’ignorer pour lancer le processus d’importation des listes. Vous pouvez également accéder à [paramètres de magasin et de liste](./ob-store-review.md) sur le magasin [tableau de bord](./amazon-store-dashboard.md). |
