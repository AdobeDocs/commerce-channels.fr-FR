---
title: '"Intégration : Créer une règle d''annonce"'
description: Lors de l'exécution du processus d'intégration du canal de vente Amazon, créez les règles de mise en vente initiale pour générer des annonces Amazon pour votre [!DNL Commerce] produits.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Intégration : Créer une règle de mise en vente

Les règles de liste peuvent être définies lors de l’intégration, mais peuvent également être modifiées à tout moment. Une fois l’intégration effectuée, vous pouvez accéder à la [règles d&#39;inscription](./listing-rules.md) sur le magasin [tableau de bord](./amazon-store-dashboard.md).

## Création d’une règle de mise en vente lors de l’intégration

1. Une fois votre boutique connectée, cliquez sur **[!UICONTROL View Store]** pour le magasin ajouté.

   Le magasin [tableau de bord](./amazon-store-dashboard.md) apparaît avec la `No products listed to Amazon` message.

1. Cliquez sur **[!UICONTROL Preview and List Eligible Products]**.

   Le _[!UICONTROL Listing Rules]_s’affiche.

1. Définissez les conditions d’éligibilité des produits à inscrire sur Amazon et cliquez sur **[!UICONTROL Preview changes]** ou cliquez sur **[!UICONTROL Preview changes]** pour ignorer cette étape.

   Voir [Exemple : Définition d’une condition](./ob-define-condition-example.md).

1. Passez en revue vos annonces dans l’aperçu de la liste :

   ![Aperçu de la liste](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Les produits répertoriés dans cet onglet ne sont pas éligibles pour l’inscription Amazon en fonction des paramètres de règle d’inscription actuels.

      Les produits non éligibles ne sont pas publiés à Amazon. Si un produit non éligible est déjà répertorié sur Amazon et que vous faites correspondre la liste Amazon à votre [!DNL Commerce] produit catalogue, la quantité pour la liste Amazon change en `0` pour empêcher la vente du produit. Pour supprimer manuellement une annonce d’Amazon, voir [Fin d&#39;une liste Amazon](./end-listings-manually.md). Les produits qui ne sont pas éligibles aux conditions d’Amazon ne sont pas répertoriés ici. Ces produits sont répertoriés sur la [[!UICONTROL Inactive Listings] onglet](./inactive-listings.md).

      Pour modifier un `Ineligible` vers un `Eligible` lister, répéter ce processus et modifier vos règles d&#39;inscription.

   - **[!UICONTROL Eligible Listings]** - Les produits répertoriés dans cet onglet sont éligibles pour la mise en vente Amazon en fonction de votre configuration actuelle de règles de mise en vente et sont éligibles en vertu des exigences du Amazon. Cet onglet inclut vos annonces Amazon existantes qui sont importées (si vous avez **[!UICONTROL Import Third Party Listings]** défini sur `Import Listing` dans votre [Paramètres de liste](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Les produits répertoriés dans cet onglet incluent votre [!DNL Commerce] les produits de catalogue qui sont nouvellement éligibles pour l&#39;inscription Amazon en fonction de la configuration actuelle de la règle d&#39;inscription et de créer des annonces Amazon.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save and Close]**.

   Le magasin [tableau de bord](./amazon-store-dashboard.md) s’ouvre.

Une fois l’intégration d’une boutique terminée, les informations sont synchronisées entre [!DNL Commerce] et Amazon est initié. Vos annonces Amazon sont importées dans [!DNL Commerce] et tenter de faire correspondre les produits de votre [!DNL Commerce] Catalogue.

Vous pouvez afficher vos informations de commande Amazon dans le dossier _[!UICONTROL Recent Orders]_du tableau de bord de la boutique. Voir [Tableau de bord Store](./amazon-store-dashboard.md) ou [Gérer les commandes](./managing-orders.md).

>[!IMPORTANT]
>
>Certains paramètres de magasin importants (annonces, tarifs, règles, exécution, etc.) ont des valeurs par défaut pour un nouveau magasin. Pour vous assurer que votre magasin est configuré pour vos besoins spécifiques, consultez votre [paramètres de stockage](./default-store-settings.md) .

![Icône suivante](assets/btn-next.png) [**Continuer vers les paramètres de magasin par défaut**](./default-store-settings.md)
