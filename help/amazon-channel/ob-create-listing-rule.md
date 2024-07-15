---
title: Création d’une règle de liste Amazon
description: Lors de l’achèvement du processus d’intégration du canal de vente Amazon, créez les règles de liste initiales pour générer des listes Amazon pour vos produits  [!DNL Commerce] .
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Création d’une règle de liste Amazon

Les règles de liste peuvent être définies lors de l’intégration, mais peuvent également être modifiées à tout moment. Après l’intégration, vous pouvez accéder aux [règles de liste](./listing-rules.md) sur le [tableau de bord](./amazon-store-dashboard.md) du magasin.

## Création d’une règle de liste lors de l’intégration

1. Une fois votre magasin connecté, cliquez sur **[!UICONTROL View Store]** pour le magasin ajouté.

   Le magasin [dashboard](./amazon-store-dashboard.md) apparaît avec le message `No products listed to Amazon`.

1. Cliquez sur **[!UICONTROL Preview and List Eligible Products]**.

   La page _[!UICONTROL Listing Rules]_s’affiche.

1. Définissez les conditions souhaitées pour l’éligibilité des produits à lister sur Amazon et cliquez sur **[!UICONTROL Preview changes]**, ou cliquez sur **[!UICONTROL Preview changes]** pour ignorer cette étape.

   Voir [Exemple : définition d’une condition](./ob-define-condition-example.md).

1. Vérifiez vos listes dans l’aperçu de la liste :

   ![Aperçu de la liste](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** - Les produits répertoriés sur cet onglet ne sont pas éligibles à la liste Amazon en fonction des paramètres actuels de votre règle de liste.

     Les produits non éligibles ne sont pas publiés sur Amazon. Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre produit de catalogue [!DNL Commerce], la quantité de la liste Amazon passe à `0` pour empêcher les ventes du produit. Pour supprimer manuellement une liste d’Amazon, reportez-vous à la section [Fin de la liste d’Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles selon les exigences d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés dans l’onglet [[!UICONTROL Inactive Listings]](./inactive-listings.md).

     Pour transformer une liste `Ineligible` en liste `Eligible`, répétez cette procédure et modifiez les règles de votre liste.

   - **[!UICONTROL Eligible Listings]** - Les produits répertoriés dans cet onglet sont éligibles à la liste Amazon en fonction de votre configuration actuelle de règle de liste et sont éligibles selon les exigences d’Amazon. Cet onglet inclut vos listes Amazon existantes qui sont importées (si **[!UICONTROL Import Third Party Listings]** est défini sur `Import Listing` dans vos [ ](./listing-settings.md) paramètres de liste).

   - **[!UICONTROL New Listings]** - Les produits répertoriés dans cet onglet incluent vos [!DNL Commerce] produits de catalogue qui sont nouvellement éligibles à la liste Amazon en fonction de votre configuration de règle de liste actuelle et créez des listes Amazon.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save and Close]**.

   Le magasin [dashboard](./amazon-store-dashboard.md) s’ouvre.

Une fois l’intégration d’un magasin terminée, la synchronisation des informations entre [!DNL Commerce] et Amazon est lancée. Vos listes Amazon sont importées dans [!DNL Commerce] et tentent de correspondre aux produits de votre catalogue [!DNL Commerce].

Vous pouvez afficher les informations de commande Amazon dans la section _[!UICONTROL Recent Orders]_du tableau de bord du magasin. Voir [Tableau de bord de magasin](./amazon-store-dashboard.md) ou [Gérer les commandes](./managing-orders.md).

>[!IMPORTANT]
>
>Certains paramètres de magasin importants (listes, prix, règles, exécution, etc.) possèdent des valeurs par défaut pour un nouveau magasin. Pour vous assurer que votre magasin est configuré en fonction de vos besoins spécifiques, consultez vos [paramètres de magasin](./default-store-settings.md) .

![Icône suivante](assets/btn-next.png) [**Continuer vers les paramètres de magasin par défaut**](./default-store-settings.md)
