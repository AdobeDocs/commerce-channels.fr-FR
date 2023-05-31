---
title: Intégration de magasin avec une [!DNL Amazon Seller Account]
description: Avant de démarrer le processus d’intégration, vous devez créer (ajouter) une boutique de Sales Channel Amazon et la connecter à votre compte de vendeur Amazon.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Intégration de magasin avec une [!DNL Amazon Seller Account]

Pour commencer à utiliser le canal de vente Amazon, vous devez créer (ajouter) une boutique de canaux de vente Amazon et la connecter à votre [!DNL Amazon Seller Account]. Ces deux étapes intègrent votre [!DNL Commerce] et comptes Amazon pour partager des données, synchroniser des produits, etc.

_Vous avez besoin des Principales informations d’identification pour votre [!DNL Amazon Seller Central] compte (adresse électronique ou téléphone utilisée pour créer le compte du vendeur) pour connecter votre boutique._

>[!NOTE]
>
>Après votre première intégration de magasin, vous serez invité chaque année à renouveler votre connexion au canal de vente Amazon à Amazon en accordant de nouveau l’accès. Vous pouvez renouveler ou révoquer cette autorisation dans le _Autorisations actuelles_ dans le _Autorisations des développeurs MWS Amazon_ de la section **Paramètres** > **Autorisations utilisateur** de votre compte central de vendeur.

## Ajout d’un magasin Amazon

1. Sur le _Administration_ barre latérale, accédez à **Marketing** > _Canaux_ > **Amazon Sales Channel**.

   Lors de l’ajout de votre première boutique de canaux de vente Amazon, la variable _Tâches préalables à la configuration_ modale s’affiche. Une fois votre premier magasin ajouté, vous pouvez accéder aux tâches préconfigurées sur la page [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) page sous _Formation et préparation_ dans le menu de gauche.

1. Cliquez sur **[!UICONTROL Add Amazon Store]**.

   Le _[!UICONTROL Add Amazon sales channel]_s’ouvre.

   ![Ajout de la boutique de canaux de vente Amazon](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. Pour **[!UICONTROL Magento Website to use for Amazon Listing]**, choisissez laquelle parmi vos [!DNL Commerce] sites web pour se connecter à cette boutique de canaux de vente Amazon.

   Ce paramètre définit également la valeur par défaut [!DNL Commerce] boutique pour [import de commandes Amazon](./order-settings.md).

1. Pour **[!UICONTROL Email Address]**, saisissez l’adresse électronique de contact préférée.

1. Pour **[!UICONTROL New Store Name]**, saisissez un nom explicite pour votre nouvelle boutique de canaux de vente Amazon.

   >[!NOTE]
   >
   >Ce nom est utilisé comme [!DNL Commerce] référencez uniquement et identifie le magasin sur la variable [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) page. Vous voulez en faire quelque chose que votre équipe peut facilement identifier. Par exemple, votre boutique Amazon qui vend dans la région des États-Unis peut être nommée `Amazon Store USA`.

1. Pour **[!UICONTROL Amazon Marketplace Country]**, sélectionnez la région/le pays dans lequel cette boutique de canaux de vente Amazon vend des produits. Options :

   - États-Unis
   - Canada
   - Mexique
   - Royaume-Uni

1. Dans le _[!UICONTROL Map your Magento attributes to Amazon]_, procédez comme suit :

   - Pour **[!UICONTROL Product ID on the Amazon market]**, sélectionnez l’attribut Amazon à mapper à la propriété [!DNL Commerce] est sélectionné ci-dessous.

      Cet identifiant permet de faire correspondre correctement les produits correspondants dans votre [!DNL Commerce] catalogue.

   - Pour **[!UICONTROL Map a Magento attribute]**, choisissez la variable [!DNL Commerce] attribut de produit à mapper à l’attribut Amazon sélectionné ci-dessus.

      [Mappage des attributs](./ob-creating-magento-attributes.md) vous aide à vous assurer que votre liste Amazon correspond correctement au produit correspondant dans votre [!DNL Commerce] catalogue.

1. Cliquez sur **[!UICONTROL Connect]**.

   La boîte de dialogue se ferme et le nouveau magasin s’affiche sur la [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) avec un message de confirmation.

## Connexion d’un magasin à [!DNL Amazon Seller Central]

1. Dans le tableau de bord de la boutique, cliquez sur **[!UICONTROL Connect store]** sur la carte de magasin à lancer [!DNL Amazon Seller Central] dans un nouvel onglet.

1. Saisissez votre [!DNL Amazon Seller Central] informations d’identification du compte et cliquez sur **[!UICONTROL Sign in]**.

   Pour terminer cette connexion, vous devez vous connecter à votre [!DNL Amazon Seller Central] compte utilisant les informations de connexion de l’utilisateur Principal (l’adresse électronique ou le téléphone utilisé pour créer le compte de vendeur).

1. Si vous y êtes invité, remplissez l’autorisation à deux facteurs d’Amazon (2FA) en saisissant le code que vous recevez d’Amazon et cliquez sur **[!UICONTROL Sign in]**.

1. Sur le _[!UICONTROL Amazon Marketplace Web Service]_page de confirmation, sélectionnez le[!UICONTROL I understand...]&quot; , puis cliquez sur **[!UICONTROL Next]**.

1. Sur le _[!UICONTROL You are almost done]_message, cliquez sur **[!UICONTROL Continue]**.

   Vous avez autorisé le canal de vente Amazon à accéder aux données et à les partager avec votre [!DNL Amazon Seller Central] compte . La page Amazon se ferme et un message de confirmation s’affiche.

   Le [Accueil du canal de vente Amazon](./amazon-sales-channel-home.md) s’ouvre, affichant vos cartes de magasin Amazon.

   Pour afficher le tableau de bord de la boutique, cliquez sur **[!UICONTROL View Store]** sur la carte du magasin.

![Accueil du canal de vente Amazon avec nouvelle carte de boutique](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

Votre nouvelle boutique de canaux de vente Amazon est maintenant connectée à votre [!DNL Amazon Seller Central] compte .

![Icône Suivant](assets/btn-next.png) [**Continuer à créer une règle de liste**](./ob-create-listing-rule.md)
