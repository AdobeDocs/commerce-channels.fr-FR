---
title: Ajout ou vérification de la clé API Amazon
description: Dans votre configuration Commerce, la clé API Amazon validée vous permet d’intégrer vos magasins à votre compte de vendeur Amazon.
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Ajout ou vérification de la clé API Amazon

Lorsque vous accédez au canal de vente Amazon, [!DNL Commerce] vérifie et valide automatiquement la clé d’API Amazon que vous avez ajoutée dans votre configuration de magasin. Si elle est validée, vous pouvez passer à l’étape suivante, [Intégration de Boutique](./store-integration.md).

Si la clé API Amazon est manquante, non valide ou a expiré, vous devez mettre à jour votre clé. Un message s’affiche vous invitant à obtenir une clé d’API et à ajouter cette clé à votre configuration de canal de vente Amazon.

## Obtention et ajout de la clé API Amazon à l’invite

La clé d’API est validée chaque fois que vous accédez à votre canal de vente Amazon.

1. Connectez-vous au [!DNL Commerce] Administrateur.

1. Sur la _[!UICONTROL Admin]_barre latérale, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Si vous accédez pour la première fois au canal de vente Amazon ou si votre clé d’API nécessite une mise à jour, le système vous invite tout au long du processus.

   ![Obtenir et ajouter l’invite de clé d’API Amazon](assets/amazon-api-verification-prompt.png)

1. Cliquez sur **[!UICONTROL Sign in]** pour accéder à [!DNL Commerce] compte Web.

   La page des comptes Commerce s’ouvre dans un nouvel onglet de navigateur.

   - Si vous êtes connecté à votre [!DNL Commerce] , le _[!UICONTROL API Portal]_de la section_[!UICONTROL My Account]_ s’affiche automatiquement.

   - Si vous n’êtes pas connecté, vous êtes invité à saisir votre [!DNL Commerce] nom d’utilisateur et mot de passe du compte avant _[!UICONTROL API Portal]_s’affiche.

   - Si vous n’avez pas de compte, rendez-vous sur la page [le [!DNL Commerce] page de compte](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;} et enregistrez. Ce compte doit faire partie de votre entreprise ou de votre entreprise.

1. Si nécessaire, vous pouvez afficher et générer des clés d’API sur le _[!UICONTROL API Portal]_dans votre [!DNL Commerce] compte.

   Pour créer une clé d’API, entrez une description comme `Amazon Sales Channel` et cliquez sur **[!UICONTROL Add New]**. La nouvelle clé est générée et affichée avec le nom que vous avez entré. Cliquez sur **[!UICONTROL Copy]** pour copier la nouvelle clé.

   ![Génération ou copie d’une clé d’API](assets/amazon-add-api-key.png)

1. Une fois la nouvelle clé générée et copiée, revenez à la _[!UICONTROL Amazon Sales Channel]_dans le navigateur.

1. Sur la _[!UICONTROL Welcome to Amazon Sales Channel]_, cliquez sur **[!UICONTROL Add the key]**.

   Le navigateur quitte le canal de vente Amazon et une page de configuration de magasin ouvre le _[!UICONTROL Api Keys]_dans la [!DNL Commerce] Administrateur. Vous pouvez ouvrir cette page manuellement lorsque vous accédez à&#x200B;**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, développez **[!UICONTROL Services]** dans le panneau de gauche, puis sélectionnez **[!UICONTROL Magento Services]**.

1. Collez la clé copiée pour **[!UICONTROL Production Api key]**.

1. Cliquez sur **[!UICONTROL Save Config]**. Vous pouvez maintenant revenir au canal de vente Amazon.

   ![Ajout de votre clé d’API dans la configuration de votre magasin](assets/config-magento-services-api-screen.png)

1. Sur la _[!UICONTROL Admin]_barre latérale, accédez à&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Réaccès aux déclencheurs du canal de vente Amazon [!DNL Commerce] vérifiez et validez votre clé d’API et vous permet de continuer.

   Si vous êtes invité à confirmer à nouveau la clé, répétez cette opération. _Ajouter et vérifier_ processus.

![Icône suivante](assets/btn-next.png) [**Continuer vers l’intégration de stockage**](./store-integration.md)
