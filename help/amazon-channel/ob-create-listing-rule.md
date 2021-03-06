---
title: '"Intégration : Créer une règle de liste"'
description: Lors de l’achèvement du processus d’intégration du canal de vente Amazon, créez les règles de liste initiales pour générer des listes Amazon pour vos [!DNL Commerce] produits.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Intégration : Créer une règle de liste

Les règles de liste peuvent être définies lors de l’intégration, mais peuvent également être modifiées à tout moment. Après l’intégration, vous pouvez accéder au [règles de liste](./listing-rules.md) sur le magasin [tableau de bord](./amazon-store-dashboard.md).

## Création d’une règle de liste lors de l’intégration

1. Une fois votre magasin connecté, cliquez sur **[!UICONTROL View Store]** pour le magasin ajouté.

   Le magasin [tableau de bord](./amazon-store-dashboard.md) apparaît avec la fonction `No products listed to Amazon` message.

1. Cliquez sur **[!UICONTROL Preview and List Eligible Products]**.

   Le _[!UICONTROL Listing Rules]_s’affiche.

1. Définissez les conditions d&#39;éligibilité des produits à lister sur Amazon et cliquez sur **[!UICONTROL Preview changes]** ou cliquez sur **[!UICONTROL Preview changes]** pour ignorer cette étape.

   Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md).

1. Vérifiez vos listes dans l’aperçu de la liste :

   ![Aperçu de la liste](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Les produits répertoriés sur cet onglet ne sont pas éligibles à la liste Amazon en fonction des paramètres actuels de votre règle de liste.

      Les produits non éligibles ne sont pas publiés sur Amazon. Si un produit non éligible est déjà répertorié dans Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit de catalogue, la quantité pour laquelle la liste Amazon est modifiée en `0` pour empêcher les ventes du produit. Pour supprimer manuellement une liste d’Amazon, reportez-vous à la section [Fin d’une liste Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles selon les exigences d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés dans la [[!UICONTROL Inactive Listings] tab](./inactive-listings.md).

      Pour modifier un `Ineligible` à `Eligible` listez, répétez cette procédure et modifiez vos règles de liste.

   - **[!UICONTROL Eligible Listings]** - Les produits répertoriés sur cet onglet sont éligibles à la liste Amazon en fonction de votre configuration actuelle des règles de liste et sont éligibles selon les exigences d’Amazon. Cet onglet comprend vos listes Amazon existantes qui sont importées (si vous avez **[!UICONTROL Import Third Party Listings]** défini sur `Import Listing` dans votre [Paramètres de liste](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Les produits répertoriés dans cet onglet incluent votre [!DNL Commerce] cataloguer les produits nouvellement éligibles à la liste Amazon en fonction de la configuration actuelle de votre règle de liste et créer des listes Amazon.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save and Close]**.

   Le magasin [tableau de bord](./amazon-store-dashboard.md) s’ouvre.

Une fois l’intégration à un magasin terminée, la synchronisation des informations entre [!DNL Commerce] et Amazon est lancé. Vos listes Amazon sont importées dans [!DNL Commerce] et essayer de correspondre aux produits de votre [!DNL Commerce] Catalogue.

Vous pouvez afficher les informations de commande Amazon dans la _[!UICONTROL Recent Orders]_du tableau de bord de la boutique. Voir [Tableau de bord de la boutique](./amazon-store-dashboard.md) ou [Gestion des commandes](./managing-orders.md).

>[!IMPORTANT]
>
>Certains paramètres de magasin importants (listes, prix, règles, exécution, etc.) possèdent des valeurs par défaut pour un nouveau magasin. Pour vous assurer que votre boutique est configurée en fonction de vos besoins spécifiques, consultez votre [paramètres de magasin](./default-store-settings.md) .

![Icône Suivant](assets/btn-next.png) [**Continuer vers les paramètres de magasin par défaut**](./default-store-settings.md)
