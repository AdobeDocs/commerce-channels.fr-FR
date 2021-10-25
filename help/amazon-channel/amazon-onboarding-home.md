---
title: Sales Channel Amazon à bord
description: Découvrez les tâches de préconfiguration, les étapes d’intégration et la façon dont Amazon fonctionne avec l’Sales Channel Amazon dans Adobe Commerce et l’Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Canal de vente Amazon intégré

Cette section décrit les tâches de préconfiguration, les étapes d&#39;intégration et quelques concepts clés de la façon dont Amazon fonctionne avec le canal de vente Amazon dans Adobe Commerce et Magento Open Source.

Le [!DNL Amazon Sales Channel] prend en charge plusieurs magasins Amazon. Pour une [!DNL Amazon Seller Central] qui opère dans la région Amazon États-Unis/Canada/Mexique, créer trois magasins Amazon (un pour les ventes aux États-Unis, les ventes au Mexique et les ventes au Canada). Chacun des trois magasins définit le pays du marché au cours de sa création. Si vous en avez plusieurs [!DNL Amazon Seller Central] , vous pourriez avoir jusqu’à trois magasins Amazon pour chacun de vos [!DNL Amazon Seller Central] comptes. Si vous vendez aussi au Royaume-Uni, vous auriez un quatrième magasin Amazon.

>[!TIP]
>
>A [Compte de vendeur professionnel](https://sell.amazon.com/){target=&quot;_blank&quot;} le [!DNL Amazon Seller Central] en Amérique du Nord ou en Europe (Royaume-Uni) est nécessaire. Amazon facture un abonnement mensuel et des frais de vente. Voir [Amazon : Choix de votre formule de vente](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>L’intégration est simple : créez votre boutique, puis connectez-la à votre [!DNL Amazon Seller Central] compte.
>Lorsque votre magasin est connecté, le canal Amazon tente d’importer vos annonces Amazon et de les faire correspondre à votre catalogue, en fonction de votre [mappage d&#39;attributs](./attributes-view.md).<br><br>
>Vos paramètres de canal de vente Amazon affectent vos annonces Amazon. Votre annonce initiale, vos tarifs et vos paramètres de produit sont par défaut pour vous. Vous pouvez modifier votre [paramètres de stockage](./ob-store-review.md) (annonce, tarification, commande et reporting) une fois que votre magasin est connecté à votre [!DNL Amazon Seller Central] compte.

| Étapes | Ce qui se passe |
|--- |--- |
| [Tâches de préconfiguration](./amazon-pre-setup-tasks.md) | Avant d’embarquer, vous devez vous assurer que vous disposez d’un [!DNL Amazon Seller Central] compte. Il y en a aussi quelques-uns [!DNL Commerce] exigences et recommandations à remplir avant l’intégration. |
| [Vérification de la clé d’API Amazon](./amazon-verify-api-key.md) | Lorsque vous accédez au canal de vente Amazon, [!DNL Commerce] vérifie et valide automatiquement la clé d’API Amazon que vous avez ajoutée dans votre configuration de magasin. Si votre clé d’API n’a pas été ajoutée ou n’est pas valide, vous êtes invité à [ajouter ou mettre à jour votre clé d’API Amazon](./amazon-verify-api-key.md). |
| [Intégration de Boutique](./store-integration.md) | Cette étape comprend la création d&#39;un magasin de canaux de vente Amazon, puis la connexion à votre [!DNL Amazon Seller Central] compte. Vous avez besoin des informations d’identification de connexion principales pour votre [!DNL Amazon Seller Central] (adresse électronique ou téléphone utilisée pour créer le compte vendeur) pour cette étape. |
| [Créer une règle d&#39;annonce](./ob-create-listing-rule.md) | Une fois que vous avez connecté votre magasin de canaux de vente Amazon, vous êtes invité à créer une règle de mise en vente. Cette étape est encouragée, mais vous pouvez également l’ignorer pour lancer le processus d’importation de la liste. Vous pouvez également accéder à [paramètres de magasin et de liste](./ob-store-review.md) sur le magasin [tableau de bord](./amazon-store-dashboard.md). |
