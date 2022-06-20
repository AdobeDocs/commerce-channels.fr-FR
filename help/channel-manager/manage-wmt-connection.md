---
title: Gérer la connexion à Walmart Marketplace
description: Mettez à jour les informations d’identification de l’API pour autoriser la connexion entre un [DNL! Commerce] vue de magasin et la variable [!DNL Walmart Marketplace]. La connexion est requise pour connecter les listes de produits Commerce et synchroniser les données d’inventaire, de prix, de commande et d’expédition entre Commerce et Walmart.
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Mappage des opérateurs de navigation

Avant [traiter les envois de commande](process-orders.md#ship-an-order) pour [!DNL Walmart Marketplace] commandes, mapper Walmart à des compagnies de transport préférées à l&#39;opérateur correspondant dans [!DNL Commerce] afin que les données d’expédition puissent être synchronisées entre [!DNL Walmart] et [!DNL Commerce].

Les opérateurs de commerce qui ne correspondent pas à un opérateur préféré sont étiquetés comme *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**Conditions préalables**

Réviser [Exigences de Walmart](walmart-requirements.md) pour le [!DNL Marketplace Seller account].

## Mise à jour des informations d’identification de connexion

1. Sur le [!UICONTROL Listings] pour la boutique de canaux de vente, sélectionnez **[!UICONTROL Channel Settings]**.

1. Activé **[!UICONTROL Channel Settings]**, sélectionnez **[!UICONTROL Walmart Connection]**.

1. Pour modifier les informations d’identification, sélectionnez **[!UICONTROL Change Credentials]**

   ![Mise à jour des informations d’identification de l’API Walmart pour autoriser la connexion](assets/update-connection-credentials.png)

1. Saisissez le **[!UICONTROL Walmart Client ID]** et **[!UICONTROL Walmart Client Secret]**.

1. Sélectionner **[!UICONTROL Save]** pour appliquer la configuration.
