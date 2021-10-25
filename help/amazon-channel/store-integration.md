---
title: Intégration de Boutique
description: Avant de commencer le processus d’intégration, vous devez créer (ajouter) une boutique de Sales Channel Amazon et la connecter à votre compte de vendeur Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Intégration de la boutique

Pour commencer avec le canal de vente Amazon, vous devez créer (ajouter) un magasin de canaux de vente Amazon et le connecter à votre compte de vendeur Amazon. Ces deux étapes intègrent votre [!DNL Commerce] et Amazon pour partager des données, synchroniser des produits, etc.

_Vous avez besoin des informations d’identification de connexion principales pour votre [!DNL Amazon Seller Central] (l’adresse e-mail ou le téléphone utilisé pour créer le compte vendeur) pour connecter votre boutique._

>[!NOTE]
>
>Après votre première intégration de magasin, vous serez invité à renouveler chaque année votre connexion de canal de vente Amazon à Amazon en accordant à nouveau l’accès. Vous pouvez renouveler ou révoquer cette autorisation dans le dossier _Autorisations actuelles_ dans le noeud _Autorisations de développeur Amazon MWS_ de la section **Paramètres** > **Autorisations utilisateur** de votre compte de centre de ventes.

## Ajout d&#39;un magasin Amazon

1. Sur la _Administrateur_ barre latérale, accédez à **Marketing** > _Canaux_ > **Sales Channel Amazon**.

   Lors de l’ajout de votre premier magasin de canaux de vente Amazon, le _Tâches de préconfiguration_ modale s’affiche. Une fois votre premier magasin ajouté, vous pouvez accéder aux tâches de préconfiguration sur le [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) page sous _Formation et préparation_ dans le menu de gauche.

1. Cliquez sur **[!UICONTROL Add Amazon Store]**.

   Le _[!UICONTROL Add Amazon sales channel]_s’ouvre.

   ![Ajout de la boutique de canaux de vente Amazon](assets/amazon-store-integration.png)

1. Pour **[!UICONTROL Magento Website to use for Amazon Listing]**, choisissez lequel de vos [!DNL Commerce] sites pour se connecter à cette boutique de canaux de vente Amazon.

   Ce paramètre définit également la valeur par défaut [!DNL Commerce] magasin pour [importation de commandes Amazon](./order-settings.md).

1. Pour **[!UICONTROL Email Address]**, entrez votre adresse e-mail de contact préférée.

1. Pour **[!UICONTROL New Store Name]**, entrez un nom descriptif pour votre nouvelle boutique de canaux de vente Amazon.

   >[!NOTE]
   >
   >Ce nom est utilisé comme [!DNL Commerce] référencez uniquement et identifie le magasin sur le [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) . Vous voulez en faire un élément que votre équipe peut facilement identifier. Par exemple, votre magasin Amazon qui vend dans la région des États-Unis peut être nommé `Amazon Store USA`.

1. Pour **[!UICONTROL Amazon Marketplace Country]**, choisissez la région/le pays dans lequel ce magasin de distribution Amazon vend des produits. Options :

   - États-Unis
   - Canada
   - Mexique
   - Royaume-Uni

1. Dans la boîte de dialogue _[!UICONTROL Map your Magento attributes to Amazon]_, procédez comme suit :

   - Pour **[!UICONTROL Product ID on the Amazon market]**, sélectionnez l’attribut Amazon à mapper au [!DNL Commerce] sélectionné ci-dessous.

      Cet ID permet de faire correspondre correctement les produits correspondants dans votre [!DNL Commerce] catalogue.

   - Pour **[!UICONTROL Map a Magento attribute]**, sélectionnez l’option [!DNL Commerce] Attribut de produit à mapper avec l’attribut Amazon sélectionné ci-dessus.

      [Attributs de mappage](./ob-creating-magento-attributes.md) veille à ce que votre annonce Amazon corresponde correctement au produit correspondant dans votre [!DNL Commerce] catalogue.

1. Cliquez sur **[!UICONTROL Connect]**.

   La boîte de dialogue se ferme et le nouveau magasin s’affiche sur le [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) avec un message de confirmation.

## Connexion d’un magasin à [!DNL Amazon Seller Central]

1. Dans le tableau de bord de stockage, cliquez sur **[!UICONTROL Connect store]** sur la carte de magasin à lancer [!DNL Amazon Seller Central] dans un nouvel onglet.

1. Saisissez votre [!DNL Amazon Seller Central] informations d’identification du compte et cliquez sur **[!UICONTROL Sign in]**.

   Pour terminer cette connexion, vous devez vous connecter à votre [!DNL Amazon Seller Central] à l’aide des identifiants de connexion de l’utilisateur principal (adresse électronique ou téléphone utilisée pour créer le compte vendeur).

1. Si vous y êtes invité, complétez l’autorisation à deux facteurs Amazon (2FA) en entrant le code que vous recevez d’Amazon et cliquez sur **[!UICONTROL Sign in]**.

1. Sur la _[!UICONTROL Amazon Marketplace Web Service]_page de confirmation, sélectionnez le[!UICONTROL I understand...]&quot; et cliquez sur **[!UICONTROL Next]**.

1. Sur la _[!UICONTROL You are almost done]_message, cliquez sur **[!UICONTROL Continue]**.

   Vous avez autorisé Amazon Sales Channel à accéder aux données et à les partager avec votre [!DNL Amazon Seller Central] compte. La page Amazon se ferme et un message de confirmation s’affiche.

   Le [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) s’ouvre et affiche vos cartes Amazon Store.

   Pour afficher le tableau de bord de la boutique, cliquez sur **[!UICONTROL View Store]** sur la carte de magasin.

![Entrée du canal de vente Amazon avec une nouvelle carte de magasin](assets/asc-dashboard-after-2fa.png)

Votre nouvelle boutique de canaux de vente Amazon est maintenant connectée à votre [!DNL Amazon Seller Central] compte.

![Icône suivante](assets/btn-next.png) [**Continuer à créer une règle d&#39;annonce**](./ob-create-listing-rule.md)
