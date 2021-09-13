---
title: Tâches préalables à la configuration
description: Passez en revue les tâches à effectuer avant d’intégrer votre boutique Adobe Commerce ou Magento Open Source dans Amazon Sales Channel.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Tâches préalables à la configuration

Avant [Intégration de magasin](./store-integration.md), vous devez vous assurer que votre compte [!DNL Amazon Seller Central] et votre compte [!DNL Commerce] sont prêts pour l’intégration. Pour réussir l’intégration, certaines tâches préalables à la configuration sont requises.

Lorsque vous configurez votre premier magasin Amazon dans le canal de vente Amazon, une liste des tâches de configuration s’affiche. Il est recommandé de passer en revue ces tâches avant [d’ajouter un magasin Amazon](./store-integration.md). Après avoir ajouté votre première boutique, vous pouvez passer en revue ces tâches dans la vue Formation et préparation du canal de vente Amazon [page d’accueil](./amazon-sales-channel-home.md).

## 1. Activez les tâches en arrière-plan dans [!DNL Commerce]

Tous les produits et données synchronisés entre [!DNL Commerce] et Amazon sont gérés par une [tâche cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Lorsque vous effectuez des tâches telles que l’ajout ou la mise à jour de listes et que vous recevez des commandes, une tâche cron envoie et reçoit des données entre votre serveur principal [!DNL Commerce] et votre compte [!DNL Amazon Seller Central].

- [ [!DNL Commerce] Activez](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Pour des performances maximales, [définissez [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} pour une exécution toutes les cinq minutes.

## 2. Créez votre compte [!DNL Amazon Seller Central]

Avant de commencer à configurer votre canal de vente Amazon, vous devez disposer d’un principal compte [!DNL Amazon Seller Central]. Si vous ne disposez pas d’un compte de vendeur Amazon existant dans la région [Amérique du Nord (États-Unis, Californie, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} ou [européenne (Royaume-Uni)](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;}, vous pouvez terminer le processus de configuration du compte de vendeur Amazon.

Le canal de vente Amazon nécessite un compte [!DNL Professional Seller] sur [!DNL Amazon Seller Central]. Amazon facture un abonnement mensuel et des frais pour la vente. Voir [Amazon : Choisissez votre plan de vente](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Assurez-vous d’être un vendeur Amazon approuvé

Pour intégrer , vous devez disposer d’un compte [!DNL Amazon Seller Central] approuvé. Votre compte ne doit comporter aucune restriction pour les produits ou les catégories. Certains produits et catégories doivent être approuvés avant de créer des listes. Vérifiez les stratégies Amazon pour la validation des catégories et des produits afin de vous assurer que vos produits sont approuvés. Voir [Amazon : Catégories et produits nécessitant une approbation](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (connexion au centre du vendeur requise).

Il est également important de vous assurer que vous avez configuré les éléments suivants dans votre compte [!DNL Amazon Seller Central] :

- Assurez-vous que votre stratégie de retour est aussi bonne ou meilleure que la stratégie de retour Amazon. Voir [Amazon : Stratégie de retour](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Assurez-vous que vos paramètres de taxe sont configurés. Voir [Amazon : Stratégies fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (connexion centrale du vendeur requise).

- Assurez-vous que vos méthodes d’expédition sont configurées avec précision. Pour configurer les méthodes de livraison que [!DNL Commerce] sont proposées aux clients pour exécuter vos commandes Amazon, mettez à jour l’[Amazon : Paramètres d’expédition](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} dans votre compte [!DNL Amazon Seller Central].

## 4. Assurez-vous que votre TVA est configurée pour vos magasins

(Utilisé principalement par les vendeurs britanniques.) Amazon recommande de s’abonner au [service de calcul de la TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Si vous choisissez une autre méthode, vous êtes responsable de la conformité à la TVA.

>[!NOTE]
>
>Il peut s’écouler entre 10 et 14 jours avant qu’Amazon ne vérifie et n’active votre compte de service de calcul de la TVA.

## 5. Augmentation du nombre de correspondances automatiques du catalogue

Lors de l’intégration, le canal de vente Amazon utilise les attributs de produit pour faire correspondre vos listes Amazon existantes (le cas échéant) aux produits existants dans votre catalogue [!DNL Commerce]. Après l’intégration, ces attributs de produit sont utilisés pour publier vos [!DNL Commerce] éléments de catalogue dans une liste Amazon et pour synchroniser vos données de produit entre [!DNL Commerce] et Amazon.

Pour que le nombre de produits [!DNL Commerce] le plus élevé corresponde automatiquement aux listes Amazon, vous devez créer un ensemble d’attributs de produit pour votre catalogue [!DNL Commerce]. Avant de configurer votre boutique de canaux de vente Amazon, vous devez ajouter des attributs de produit [!DNL Commerce] correspondant à ces attributs Amazon, par exemple : ASIN, EAN, ISBN, UPC ou GCID. Voir [Création d’un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configurez votre devise et votre conversion (si nécessaire).

Si votre boutique Amazon utilise une devise différente de celle configurée pour votre magasin [!DNL Commerce], [activez la devise](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} et définissez le [taux de conversion de devise](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Création d’un attribut de condition de produit (selon les besoins)

Si vos listes Amazon contiennent plusieurs conditions de produit (telles que _new_, _used_ ou _comme new_), créez un attribut [!DNL Commerce] et affectez des valeurs de condition. Vous devez mapper cet attribut lors de l’intégration à l’attribut de produit Condition Amazon. Voir [Création d’attributs pour Amazon](./ob-creating-magento-attributes.md).

## 8. Configuration de votre méthode de livraison [!DNL Amazon Seller Central]

Pour configurer les méthodes de livraison que vous souhaitez proposer pour répondre à vos commandes Amazon, reportez-vous à la section [Paramètres et paramètres d’expédition][10] de votre compte [!DNL Amazon Seller Central].

## Paramétrages supplémentaires

Lorsque votre compte Amazon est configuré et principal, plusieurs [!DNL Commerce] recommandations permettent de rationaliser le processus d’intégration du canal de vente Amazon.

### Examinez et notez tous les produits que vous souhaitez exclure.

Il se peut que vous ne souhaitiez pas que certains produits soient répertoriés dans Amazon. Le canal de vente Amazon dispose d’un moteur de règles de liste utilisé pour déterminer les produits pouvant être publiés sur Amazon. [Les ](./listing-rules.md) règles d’énumération vous permettent de sélectionner des sous-ensembles de produits à publier (ou non publié) sur votre  [!DNL Amazon Seller Central] compte, par exemple par sélection de catégorie ou en définissant un ou plusieurs attributs de produit. Comme [!DNL Commerce] [catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} ou [panier](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}, les attributs de produit utilisés pour l’éligibilité aux listes Amazon doivent être **[!UICONTROL Use for Promo Rule Conditions]** définis sur `Yes`. Voir **[!UICONTROL Use for Promo Rule Conditions]** dans [Attributs du produit](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Définissez votre région [!DNL Amazon Seller Central] inactive.

Pour faciliter la transition de données sans erreur lors de l’intégration, il est recommandé de définir la région Amazon sur `Inactive` état dans Paramètres > Informations du compte > Paramètres de déplacement. Voir [Amazon : État de liste des déplacements][11]. Une fois la configuration terminée, redéfinissez l’état sur `Active` dans Amazon.

![Icône suivante ](assets/btn-next.png) [**: Passez à la création d’ [!DNL Commerce] attributs**](./ob-creating-magento-attributes.md)
