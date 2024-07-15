---
title: Ajout ou vérification de la clé API Amazon
description: Dans votre configuration Commerce, la clé d’API Amazon validée vous permet d’intégrer vos magasins à votre compte de vendeur Amazon.
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Ajout ou vérification de la clé API Amazon

Lors de l’accès au canal de vente Amazon, [!DNL Commerce] vérifie et valide automatiquement la clé d’API Amazon que vous avez ajoutée dans la configuration de votre magasin. S’il est validé, vous pouvez passer à l’étape suivante, [Intégration de magasin](./store-integration.md).

Si la clé de l’API Amazon est manquante, non valide ou expirée, vous devez mettre à jour votre clé. Un message s’affiche vous invitant à obtenir une clé d’API et à l’ajouter à la configuration de votre canal de vente Amazon.

## Obtenez et ajoutez la clé d’API Amazon suivant les instructions.

La clé API est validée chaque fois que vous accédez à votre canal de vente Amazon.

1. Connectez-vous à l’administrateur [!DNL Commerce].

1. Sur la barre latérale _[!UICONTROL Admin]_, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Si vous accédez au canal de vente Amazon pour la première fois ou si votre clé d’API doit être mise à jour, le système vous invite à passer par ce processus.

   ![Obtenir et ajouter l’invite de clé API Amazon](assets/amazon-api-verification-prompt.png){width="500"}

1. Cliquez sur **[!UICONTROL Sign in]** pour accéder à votre compte web [!DNL Commerce].

   La page Comptes Commerce s’ouvre dans un nouvel onglet du navigateur.

   - Si vous êtes connecté à votre compte [!DNL Commerce], la section _[!UICONTROL API Portal]_de la page_[!UICONTROL My Account]_ s’affiche automatiquement.

   - Si vous n’êtes pas connecté, vous êtes invité à saisir le nom d’utilisateur et le mot de passe de votre compte [!DNL Commerce] avant que l’onglet _[!UICONTROL API Portal]_ne s’affiche.

   - Si vous n&#39;avez pas de compte, visitez [la  [!DNL Commerce] page de compte](https://account.magento.com/customer/account/login/){target="_blank"} et inscrivez-vous. Ce compte doit faire partie de votre entreprise ou de votre entreprise.

1. Si nécessaire, vous pouvez afficher et générer des clés d’API sur l’onglet _[!UICONTROL API Portal]_de votre compte [!DNL Commerce].

   Pour créer une clé API, saisissez une description du type `Amazon Sales Channel` et cliquez sur **[!UICONTROL Add New]**. La nouvelle clé est générée et affichée avec le nom que vous avez saisi. Cliquez sur **[!UICONTROL Copy]** pour copier la nouvelle clé.

   ![Générer ou copier une clé API](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. Une fois la nouvelle clé générée et copiée, revenez à l’onglet _[!UICONTROL Amazon Sales Channel]_dans le navigateur.

1. Sur la page _[!UICONTROL Welcome to Amazon Sales Channel]_, cliquez sur **[!UICONTROL Add the key]**.

   Le navigateur quitte le canal de vente Amazon et une page de configuration de magasin ouvre la page _[!UICONTROL Api Keys]_dans l’administrateur [!DNL Commerce]. Vous pouvez ouvrir cette page manuellement lorsque vous accédez à&#x200B;**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, développez **[!UICONTROL Services]** dans le panneau de gauche, puis sélectionnez **[!UICONTROL Magento Services]**.

1. Collez la clé copiée pour **[!UICONTROL Production Api key]**.

1. Cliquez sur **[!UICONTROL Save Config]**. Vous pouvez désormais revenir au canal de vente Amazon.

   ![Ajout de votre clé API dans la configuration de votre magasin](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. Sur la barre latérale _[!UICONTROL Admin]_, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   La réaccès aux déclencheurs de canal de vente Amazon [!DNL Commerce] vérifie et valide votre clé API et vous permet de continuer.

   Si vous êtes invité à vérifier à nouveau la clé, répétez ce processus _Ajouter et vérifier_.

![Icône suivante](assets/btn-next.png) [**Continuer vers l’intégration de magasin**](./store-integration.md)
