---
title: Tâches de préconfiguration
description: Passez en revue les tâches requises à effectuer avant d’intégrer votre Adobe Commerce ou votre Magento Open Source store dans Amazon Sales Channel.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Tâches de préconfiguration

Avant [Intégration de Boutique](./store-integration.md), vous devez vous assurer que [!DNL Amazon Seller Central] et votre [!DNL Commerce] sont prêts pour l’intégration. Pour réussir l’intégration, certaines tâches de préconfiguration sont requises.

Lorsque vous configurez votre premier magasin Amazon dans le canal de vente Amazon, une liste des tâches de configuration s’affiche. Il est recommandé de passer en revue ces tâches avant de [ajouter un magasin Amazon](./store-integration.md). Après avoir ajouté votre premier magasin, vous pouvez passer en revue ces tâches dans la vue Formation et préparation du canal de vente Amazon. [page d&#39;accueil](./amazon-sales-channel-home.md).

## 1. Activez les tâches en arrière-plan dans [!DNL Commerce]

Tous les produits et données synchronisés entre [!DNL Commerce] et Amazon est géré par un [travail de cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. Lorsque vous effectuez des tâches telles que l&#39;ajout ou la mise à jour d&#39;annonces et la réception de commandes, une tâche de création envoie et reçoit des données entre [!DNL Commerce] et votre [!DNL Amazon Seller Central] compte.

- [Activer [!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- Pour des performances maximales, [définir [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} à exécuter une fois toutes les cinq minutes.

## 2. Créez votre [!DNL Amazon Seller Central] compte

Avant de commencer à configurer votre canal de vente Amazon, vous devez disposer d’un [!DNL Amazon Seller Central] compte. Si vous ne disposez pas d’un compte vendeur Amazon existant dans le fichier [Amérique du Nord (États-Unis, Californie, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} ou [Européen (Royaume-Uni)](https://sell.amazon.co.uk/sell-online/beginners-guide)Région {target=&quot;_blank&quot;}, vous pouvez terminer le processus de configuration du compte vendeur Amazon.

Le canal de vente Amazon nécessite un [!DNL Professional Seller] compte sur [!DNL Amazon Seller Central]. Amazon facture un abonnement mensuel et des frais de vente. Voir [Amazon : Choix de votre formule de vente](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Assurez-vous d’être un vendeur Amazon agréé.

Pour intégrer, vous devez disposer d’un [!DNL Amazon Seller Central] compte. Votre compte ne doit pas avoir de restrictions pour les produits ou catégories. Certains produits et catégories doivent être approuvés avant de créer des annonces. Consultez les stratégies Amazon pour connaître la catégorie et l’approbation des produits afin de vous assurer que vos produits sont approuvés. Voir [Amazon : Catégories et produits nécessitant une approbation](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (Connexion au centre du vendeur requise).

Il est également important de s’assurer que vous avez configuré les éléments suivants dans votre [!DNL Amazon Seller Central] compte :

- Assurez-vous que votre politique de retour est aussi bonne ou meilleure que la politique de retour Amazon. Voir [Amazon : Politique de retour](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Assurez-vous que vos paramètres fiscaux sont configurés. Voir [Amazon : Politiques fiscales](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (Connexion au centre du vendeur requise).

- Assurez-vous que vos méthodes d’expédition sont configurées avec précision. Pour configurer les méthodes d&#39;expédition qui [!DNL Commerce] sont proposés aux clients pour répondre à vos commandes Amazon, mettre à jour le [Amazon : Paramètres d&#39;expédition](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} dans votre [!DNL Amazon Seller Central] compte.

## 4. Assurez-vous que votre TVA est configurée pour vos magasins.

(Principalement utilisé par les vendeurs britanniques.) Amazon recommande de s&#39;inscrire pour le [Service de calcul de TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Si vous choisissez une autre méthode, vous êtes responsable du respect de la TVA.

>[!NOTE]
>
>Il peut prendre entre 10 et 14 jours pour qu’Amazon vérifie et active votre compte de service de calcul de la TVA.

## 5. Augmenter le nombre de correspondances automatiques de catalogue

Lors de l’intégration, Amazon Sales Channel utilise des attributs de produit pour correspondre à vos listes Amazon existantes (le cas échéant) aux produits existants dans votre [!DNL Commerce] catalogue. Après l’intégration, ces attributs de produit sont utilisés pour publier votre [!DNL Commerce] Eléments de catalogue vers une liste Amazon et synchronisation des données de votre produit entre [!DNL Commerce] et Amazon.

Pour avoir le plus grand nombre de [!DNL Commerce] les produits correspondent automatiquement aux annonces Amazon, vous devez créer un ensemble d’attributs de produit pour vos [!DNL Commerce] catalogue. Avant de configurer votre magasin de canaux de vente Amazon, vous devez ajouter [!DNL Commerce] attributs de produit correspondant à ces attributs Amazon, par exemple : ASIN, EAN, ISBN, UPC ou GCID. Voir [Créer un attribut de produit dans [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Configurez votre devise et votre conversion (si nécessaire).

Si votre Amazon Store utilise une devise différente de celle configurée pour votre [!DNL Commerce] magasin [activer la devise](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} et définissez la propriété [taux de conversion des devises](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Créez un attribut Condition de produit (si nécessaire).

Si vos annonces Amazon contiennent plusieurs conditions de produit (telles que _nouveau_, _utilisé_, ou _comme nouveau_), créez un [!DNL Commerce] et attribuez des valeurs de condition. Vous devez mapper cet attribut lors de l’intégration à l’attribut de produit Condition Amazon. Voir [Création d&#39;attributs pour Amazon](./ob-creating-magento-attributes.md).

## 8. Configurez votre [!DNL Amazon Seller Central] mode d&#39;expédition

Pour configurer les méthodes d&#39;expédition que vous souhaitez proposer pour exécuter vos commandes Amazon, reportez-vous à la section [Paramètres et paramètres d’expédition][10] dans votre [!DNL Amazon Seller Central] compte.

## Configurations supplémentaires

Lorsque votre compte Amazon est configuré et actif, plusieurs [!DNL Commerce] recommandations qui aident à rationaliser le processus d&#39;intégration du canal de vente Amazon.

### Examinez et notez tous les produits que vous souhaitez exclure.

Vous pouvez ne pas vouloir que certains produits soient répertoriés sur Amazon. Le canal de vente Amazon dispose d&#39;un moteur de règles de mise en vente qui est utilisé pour déterminer quels produits peuvent être publiés sur Amazon. [Règles d&#39;annonce](./listing-rules.md) vous permettent de sélectionner des sous-ensembles de produits à publier (ou à ne pas publier) dans votre [!DNL Amazon Seller Central] , par exemple par sélection de catégorie ou en définissant un ou plusieurs attributs de produit. Comme [!DNL Commerce] [catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} ou [panier](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;} règles de prix, les attributs de produit utilisés pour l&#39;éligibilité aux listes Amazon doivent avoir **[!UICONTROL Use for Promo Rule Conditions]** défini sur `Yes`. Voir la section **[!UICONTROL Use for Promo Rule Conditions]** dans [Attributs de produit](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Définir [!DNL Amazon Seller Central] région à inactif

Pour faciliter la transition des données sans erreur pendant l’intégration, il est recommandé de définir votre région Amazon sur `Inactive` dans Paramètres > Informations de compte > Paramètres de vacances. Reportez-vous à [Amazon : Statut de la liste pour les vacances][11]. Une fois votre configuration terminée, repassez à l’état `Active` en Amazon.

![Icône suivante](assets/btn-next.png) [**Continuer à créer [!DNL Commerce] Attributs**](./ob-creating-magento-attributes.md)
