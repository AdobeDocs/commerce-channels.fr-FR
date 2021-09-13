---
title: '"Intégration : Créer une règle de liste"'
description: Lors de l’achèvement du processus d’intégration du canal de vente Amazon, créez les règles de liste initiales pour générer des listes Amazon pour vos  [!DNL Commerce] produits.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Intégration : Créer une règle de liste

Les règles de liste peuvent être définies lors de l’intégration, mais peuvent également être modifiées à tout moment. Après l’intégration, vous pouvez accéder aux [règles de liste](./listing-rules.md) sur le [tableau de bord](./amazon-store-dashboard.md) du magasin.

## Création d’une règle de liste lors de l’intégration

1. Une fois votre magasin connecté, cliquez sur **[!UICONTROL View Store]** pour le magasin ajouté.

   Le [tableau de bord](./amazon-store-dashboard.md) du magasin s’affiche avec le message `No products listed to Amazon`.

1. Cliquez sur **[!UICONTROL Preview and List Eligible Products]**.

   La page _[!UICONTROL Listing Rules]_s’affiche.

1. Définissez les conditions d&#39;éligibilité des produits à lister sur Amazon et cliquez sur **[!UICONTROL Preview changes]**, ou cliquez sur **[!UICONTROL Preview changes]** pour ignorer cette étape.

   Voir [Exemple : Définissez une condition ](./ob-define-condition-example.md).

1. Vérifiez vos listes dans l’aperçu de la liste :

   ![Aperçu de la liste](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Les produits répertoriés sur cet onglet ne sont pas éligibles à la liste Amazon en fonction des paramètres actuels de votre règle de liste.

      Les produits non éligibles ne sont pas publiés sur Amazon. Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit catalogue, la quantité de la liste Amazon passe à `0` pour empêcher les ventes du produit. Pour supprimer manuellement une liste d’Amazon, voir [Fin de la liste d’Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles selon les exigences d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés dans l’onglet [[!UICONTROL Inactive Listings]](./inactive-listings.md).

      Pour transformer une liste `Ineligible` en liste `Eligible`, répétez cette procédure et modifiez les règles de votre liste.

   - **[!UICONTROL Eligible Listings]** - Les produits répertoriés sur cet onglet sont éligibles à la liste Amazon en fonction de votre configuration actuelle des règles de liste et sont éligibles selon les exigences d’Amazon. Cet onglet inclut vos listes Amazon existantes qui sont importées (si **[!UICONTROL Import Third Party Listings]** est défini sur `Import Listing` dans vos [Paramètres de liste](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Les produits répertoriés dans cet onglet incluent vos produits  [!DNL Commerce] de catalogue qui sont nouvellement éligibles à la liste Amazon en fonction de votre configuration actuelle de règles de liste et créez des listes Amazon.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save and Close]**.

   Le [tableau de bord](./amazon-store-dashboard.md) du magasin s’ouvre.

Une fois l’intégration à un magasin terminée, la synchronisation des informations entre [!DNL Commerce] et Amazon est lancée. Vos listes Amazon sont importées dans [!DNL Commerce] et tentent de correspondre aux produits de votre [!DNL Commerce] catalogue.

Vous pouvez afficher les informations de commande Amazon dans la section _[!UICONTROL Recent Orders]_du tableau de bord de la boutique. Voir [Tableau de bord du magasin](./amazon-store-dashboard.md) ou [Gestion des commandes](./managing-orders.md).

>[!IMPORTANT]
>
>Certains paramètres de magasin importants (listes, prix, règles, exécution, etc.) possèdent des valeurs par défaut pour un nouveau magasin. Pour vous assurer que votre magasin est configuré en fonction de vos besoins spécifiques, consultez vos [paramètres de magasin](./default-store-settings.md) .

![Icône suivante ](assets/btn-next.png) [**: Accédez aux paramètres de magasin par défaut**](./default-store-settings.md)
