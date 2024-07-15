---
title: Intégration de magasin avec un  [!DNL Amazon Seller Account]
description: Avant de démarrer le processus d’intégration, vous devez créer (ajouter) une boutique de Sales Channel Amazon et la connecter à votre compte de vendeur Amazon.
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Intégration de magasin avec un [!DNL Amazon Seller Account]

Pour commencer à utiliser le canal de vente Amazon, vous devez créer (ajouter) une boutique de canaux de vente Amazon et la connecter à votre [!DNL Amazon Seller Account]. Ces deux étapes intègrent vos comptes [!DNL Commerce] et Amazon pour partager des données, synchroniser des produits, etc.

_Vous avez besoin des informations d’identification de connexion principales pour votre compte [!DNL Amazon Seller Central] (l’adresse électronique ou le téléphone utilisé pour créer le compte de vendeur) pour connecter votre boutique._

>[!NOTE]
>
>Après votre première intégration de magasin, vous serez invité chaque année à renouveler votre connexion au canal de vente Amazon à Amazon en accordant de nouveau l’accès. Vous pouvez renouveler ou révoquer cette autorisation dans le tableau _Autorisations actuelles_ de la section _Autorisations des développeurs MWS Amazon_ de la page **Paramètres** > **Autorisations des utilisateurs** de votre compte central Seller.

## Ajout d’un magasin Amazon

1. Sur la barre latérale _Admin_, accédez à **Marketing** > _Canaux_ > **Sales Channel Amazon**.

   Lors de l’ajout de votre première boutique de canaux de vente Amazon, le modal _Tâches préalables à la configuration_ s’affiche. Une fois votre premier magasin ajouté, vous pouvez accéder aux tâches de préconfiguration sur la page d’accueil [ du canal de vente Amazon](./amazon-sales-channel-home.md) sous _Formation et préparation_ dans le menu de gauche.

1. Cliquez sur **[!UICONTROL Add Amazon Store]**.

   La page _[!UICONTROL Add Amazon sales channel]_s’ouvre.

   ![Ajout de la boutique de canaux de vente Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Pour **[!UICONTROL Magento Website to use for Amazon Listing]**, choisissez l’un de vos [!DNL Commerce] sites web à connecter pour cette boutique de canaux de vente Amazon.

   Ce paramètre définit également le [!DNL Commerce] magasin par défaut pour [ importer des commandes Amazon](./order-settings.md).

1. Pour **[!UICONTROL Email Address]**, saisissez l’adresse électronique de contact préférée.

1. Pour **[!UICONTROL New Store Name]**, saisissez un nom explicite pour votre nouvelle boutique de canaux de vente Amazon.

   >[!NOTE]
   >
   >Ce nom est utilisé comme référence [!DNL Commerce] uniquement et identifie le magasin sur la page [accueil du canal de vente Amazon](./amazon-sales-channel-home.md). Vous voulez en faire quelque chose que votre équipe peut facilement identifier. Par exemple, votre boutique Amazon qui se vend dans la région des États-Unis peut être nommée `Amazon Store USA`.

1. Pour **[!UICONTROL Amazon Marketplace Country]**, choisissez la région/le pays dans lequel cette boutique de canaux de vente Amazon vend des produits. Options :

   - États-Unis
   - Canada
   - Mexique
   - Royaume-Uni

1. Dans la section _[!UICONTROL Map your Magento attributes to Amazon]_, procédez comme suit :

   - Pour **[!UICONTROL Product ID on the Amazon market]**, choisissez l’attribut Amazon à mapper à l’attribut [!DNL Commerce] sélectionné ci-dessous.

     Cet identifiant permet de faire correspondre correctement les produits correspondants dans votre catalogue [!DNL Commerce].

   - Pour **[!UICONTROL Map a Magento attribute]**, choisissez l’attribut de produit [!DNL Commerce] à mapper à l’attribut Amazon sélectionné ci-dessus.

     [Le mappage des attributs](./ob-creating-magento-attributes.md) permet de s’assurer que votre liste Amazon correspond correctement au produit correspondant dans votre catalogue [!DNL Commerce].

1. Cliquez sur **[!UICONTROL Connect]**.

   La boîte de dialogue se ferme et le nouveau magasin s’affiche sur la page d’accueil [ du canal de vente Amazon](./amazon-sales-channel-home.md) avec un message de confirmation.

## Connexion d’un magasin à [!DNL Amazon Seller Central]

1. Dans le tableau de bord du magasin, cliquez sur **[!UICONTROL Connect store]** sur la carte du magasin pour lancer [!DNL Amazon Seller Central] dans un nouvel onglet.

1. Saisissez vos informations d’identification de compte [!DNL Amazon Seller Central] et cliquez sur **[!UICONTROL Sign in]**.

   Pour terminer cette connexion, vous devez vous connecter à votre compte [!DNL Amazon Seller Central] à l’aide des informations d’identification de connexion de l’utilisateur principal (adresse électronique ou téléphone utilisé pour créer le compte de vendeur).

1. Si vous y êtes invité, complétez l’autorisation à deux facteurs d’Amazon (2FA) en saisissant le code que vous recevez d’Amazon et cliquez sur **[!UICONTROL Sign in]**.

1. Sur la page de confirmation _[!UICONTROL Amazon Marketplace Web Service]_, cochez la case &quot;[!UICONTROL I understand...]&quot; et cliquez sur **[!UICONTROL Next]**.

1. Sur le message _[!UICONTROL You are almost done]_, cliquez sur **[!UICONTROL Continue]**.

   Vous avez autorisé le canal de vente Amazon à accéder aux données et à les partager avec votre compte [!DNL Amazon Seller Central]. La page Amazon se ferme et un message de confirmation s’affiche.

   La page [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) s’ouvre et affiche vos cartes de boutique Amazon.

   Pour afficher le tableau de bord du magasin, cliquez sur **[!UICONTROL View Store]** sur la carte du magasin.

![Page d’accueil du canal de vente Amazon avec une nouvelle carte de boutique](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

Votre nouvelle boutique de canaux de vente Amazon est maintenant connectée à votre compte [!DNL Amazon Seller Central].

![Icône suivante](assets/btn-next.png) [**Continuer à créer une règle de liste**](./ob-create-listing-rule.md)
