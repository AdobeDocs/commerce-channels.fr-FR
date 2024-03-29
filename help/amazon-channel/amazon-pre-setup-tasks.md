---
title: Tâches préalables à la configuration pour [!DNL Amazon sales channel]
description: Passez en revue les tâches à effectuer avant d’intégrer votre boutique Adobe Commerce ou Magento Open Source dans Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Tâches préalables à la configuration pour [!DNL Amazon sales channel]

Avant [Intégration de magasin](./store-integration.md), vous devez vous assurer que la variable [!DNL Amazon Seller Central] et votre compte [!DNL Commerce] sont prêts pour l’intégration. Pour réussir l’intégration, certaines tâches préalables à la configuration sont requises.

Lorsque vous configurez votre premier magasin Amazon dans le canal de vente Amazon, une liste des tâches de configuration s’affiche. Il est recommandé de passer en revue ces tâches avant de [ajouter un magasin Amazon](./store-integration.md). Après avoir ajouté votre premier magasin, vous pouvez passer en revue ces tâches dans la vue Formation et préparation du canal de vente Amazon. [page d&#39;accueil](./amazon-sales-channel-home.md).

## 1. Activez les tâches en arrière-plan dans [!DNL Commerce]

Tous les produits et données synchronisés entre [!DNL Commerce] et Amazon est géré par une [tâche cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). Lorsque vous effectuez des tâches telles que l’ajout ou la mise à jour de listes et que vous recevez des commandes, une tâche cron envoie et reçoit des données entre vos [!DNL Commerce] et votre serveur principal [!DNL Amazon Seller Central] compte .

- [Activer [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- Pour des performances maximales, [set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) pour qu’il s’exécute toutes les cinq minutes.

## 2. Créez votre [!DNL Amazon Seller Central] account

Avant de commencer à configurer votre canal de vente Amazon, vous devez disposer d’un [!DNL Amazon Seller Central] compte . Si vous ne disposez pas d’un compte de vendeur Amazon dans la variable [Amérique du Nord (États-Unis, Californie, MX)](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} région, vous pouvez terminer le processus de configuration du compte vendeur Amazon.

Le canal de vente Amazon nécessite une [!DNL Professional Seller] compte sur [!DNL Amazon Seller Central]. Amazon facture un abonnement mensuel et des frais pour la vente. Voir [Amazon : choisissez votre plan de vente](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Assurez-vous d’être un vendeur Amazon approuvé

Pour intégrer , vous devez disposer d’un [!DNL Amazon Seller Central] compte . Votre compte ne doit comporter aucune restriction pour les produits ou les catégories. Certains produits et catégories doivent être approuvés avant de créer des listes. Vérifiez les stratégies Amazon pour l’approbation des catégories et des produits afin de vous assurer que vos produits sont approuvés. Voir [Amazon : catégories et produits nécessitant une validation](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (Connexion à Seller Central requise).

Il est également important de vous assurer que vous avez configuré les éléments suivants dans votre [!DNL Amazon Seller Central] compte :

- Assurez-vous que votre stratégie de retour est aussi bonne ou meilleure que la stratégie de retour Amazon. Voir [Amazon : stratégie de retour](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Vérifiez que vos paramètres de taxe sont configurés. Voir [Amazon : politiques fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (Connexion à Seller Central requise).

- Assurez-vous que vos méthodes d’expédition sont configurées avec précision. Pour configurer les méthodes d’expédition qui [!DNL Commerce] sont proposées aux clients pour répondre à vos commandes Amazon, mettre à jour la variable [Amazon : paramètres de livraison](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} dans votre [!DNL Amazon Seller Central] compte .

## 4. Assurez-vous que votre TVA est configurée pour vos magasins

(Utilisé principalement par les vendeurs britanniques.) Amazon recommande de s’abonner au [Service de calcul de la TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Si vous choisissez une autre méthode, vous êtes responsable de la conformité à la TVA.

>[!NOTE]
>
>Il peut s’écouler entre 10 et 14 jours avant qu’Amazon ne vérifie et n’active votre compte de service de calcul de la TVA.

## 5. Augmentation du nombre de correspondances automatiques du catalogue

Lors de l’intégration, le canal de vente Amazon utilise les attributs de produit pour faire correspondre vos listes Amazon existantes (le cas échéant) aux produits existants dans votre [!DNL Commerce] catalogue. Après l’intégration, ces attributs de produit sont utilisés pour publier votre [!DNL Commerce] cataloguer des éléments dans une liste Amazon et synchroniser vos données de produit entre [!DNL Commerce] et Amazon.

Pour avoir le nombre maximal de [!DNL Commerce] les produits correspondent automatiquement aux listes Amazon. Vous devez créer un ensemble d’attributs de produit pour vos [!DNL Commerce] catalogue. Avant de configurer votre boutique de canaux de vente Amazon, vous devez ajouter [!DNL Commerce] attributs de produit pour correspondre à ces attributs Amazon, par exemple : ASIN, EAN, ISBN, UPC ou GCID. Voir [Créez un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configurez votre devise et votre conversion (si nécessaire).

Si votre boutique Amazon utilise une devise différente de celle configurée pour votre [!DNL Commerce] magasin, [activer la devise](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) et définissez la variable [taux de conversion des devises](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Créez un attribut de condition de produit (selon les besoins).

Si vos listes Amazon contiennent plusieurs conditions de produit (telles que _new_, _used_, ou _apprécier les nouveaux_), créez une [!DNL Commerce] Attribuez et attribuez des valeurs de condition. Vous devez mapper cet attribut lors de l’intégration à l’attribut de produit Condition Amazon. Voir [Création d’attributs pour Amazon](./ob-creating-magento-attributes.md).

## 8. Configurez votre [!DNL Amazon Seller Central] méthode d&#39;expédition

Pour configurer les méthodes de livraison que vous souhaitez proposer pour répondre à vos commandes Amazon, reportez-vous à la section _Paramètres et paramètres d’expédition_ dans votre [!DNL Amazon Seller Central] compte .

## Paramétrages supplémentaires

Lorsque votre compte Amazon est configuré et actif, plusieurs [!DNL Commerce] recommandations qui permettent de rationaliser le processus d’intégration du canal de vente Amazon.

### Examinez et notez tous les produits que vous souhaitez exclure.

Il se peut que vous ne souhaitiez pas que certains produits soient répertoriés dans Amazon. Le canal de vente Amazon dispose d’un moteur de règles de liste utilisé pour déterminer les produits pouvant être publiés sur Amazon. [Règles de liste](./listing-rules.md) vous permettent de sélectionner des sous-ensembles de produits à publier (ou à ne pas publier) sur votre [!DNL Amazon Seller Central] par exemple par sélection de catégorie ou en définissant un ou plusieurs attributs de produit. Comme [!DNL Commerce] [catalogue](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) ou [panier](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) règles de prix, les attributs de produit utilisés pour l’éligibilité à la liste Amazon doivent avoir **[!UICONTROL Use for Promo Rule Conditions]** défini sur `Yes`. Voir **[!UICONTROL Use for Promo Rule Conditions]** in [Attributs de produit](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Définissez vos [!DNL Amazon Seller Central] région à inactif

Pour faciliter la transition des données sans erreur lors de l’intégration, il est recommandé de définir la région Amazon sur `Inactive` dans Paramètres > Informations du compte > Paramètres de déplacement. Une fois la configuration terminée, redéfinissez l’état sur `Active` dans Amazon.

![Icône Suivant](assets/btn-next.png) [**Passez à la section Création [!DNL Commerce] Attributs**](./ob-creating-magento-attributes.md)
