---
user-guide-title: Guide de l’utilisateur d’Amazon Sales Channel
user-guide-description: Générez des ventes via Amazon en intégrant Adobe Commerce ou Magento Open Source à votre [!DNL Amazon Seller Central] compte .
breadcrumb-title: Canal de vente Amazon
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# Canal de vente Amazon - [!DNL channel manager] pour Adobe Commerce {#amazon}

- [Guide de l’utilisateur d’Amazon Sales Channel](guide-overview.md)
- [Présentation du canal de vente Amazon](overview.md)
- Prise en main {#getting-started}
   - [À propos d’Amazon Marketplace](about-amazon-marketplace.md)
   - [Amazon et le catalogue de commerce](about-listings-and-catalog.md)
   - [Bonnes pratiques et limites](amazon-best-practices.md)
   - [Installation de l’extension](install.md)
- Intégration {#onboarding}
   - [Canal de vente Amazon intégré](amazon-onboarding-home.md)
   - [Tâches préalables à la configuration](amazon-pre-setup-tasks.md)
   - [Créer [!DNL Commerce] Attributs pour Amazon](ob-creating-magento-attributes.md)
   - [Vérification de la clé d’API Amazon](amazon-verify-api-key.md)
   - [Intégration de magasin](store-integration.md)
   - [Créer une règle de liste](ob-create-listing-rule.md)
   - [Paramètres de magasin par défaut](default-store-settings.md)
- Gestion du canal de vente {#manage}
   - [Page d’accueil](amazon-sales-channel-home.md)
   - [Magasins Amazon](managing-stores.md)
   - [Contrôles Workspace](workspace-controls.md)
   - [Formation et préparation](learning-preparation.md)
   - Attributs {#attributes}
      - [Affichage des attributs](attributes-view.md)
      - [Gestion des attributs](managing-attributes.md)
      - [Création et modification d’attributs](creating-attributes.md)
      - [Affichage du mappage des attributs](amazon-matching-attributes-values.md)
   - [Paramètres d’administration des canaux de vente](sales-channel-settings.md)
   - [Tableau de bord de la boutique Amazon](amazon-store-dashboard.md)
   - [Paramètres de magasin](ob-store-review.md)
- Paramètres de liste {#listing-settings}
   - [Afficher les paramètres de liste](listing-settings.md)
   - [Actions de liste de produits](product-listing-actions.md)
   - [Listes tierces](third-party-listing-settings.md)
   - [Prix d&#39;inscription](listing-price.md)
   - [Prix d’entreprise (B2B)](business-pricing.md)
   - [Stock/quantité](stock-quantity.md)
   - [Renseigné par](fulfilled-by.md)
   - [Recherche catalogue](catalog-search.md)
   - [Condition de liste de produits](product-listing-condition.md)
   - [Produits renouvelés](renewed-products.md)
- [Paramètres de commande](order-settings.md)
- [Paramètres d’intégration de magasin](store-integration-settings.md)
- Règles d&#39;énumération et de tarification {#rules}
   - [Règles d&#39;énumération](listing-rules.md)
   - Règles de tarifs {#pricing-rules}
      - [Gérer les tarifs](pricing-products.md)
      - [Ajouter une nouvelle règle de tarification](add-pricing-rule.md)
      - [Paramètres généraux des règles de prix](pricing-rule-general-settings.md)
      - [Conditions des règles de prix](pricing-rule-conditions.md)
      - [Actions de règle de prix](pricing-rule-actions.md)
      - [Règle de prix standard](standard-price-rules.md)
      - [Règle de retarification intelligente](intelligent-repricing-rules.md)
      - [Écarts conditionnels des concurrents](competitor-conditional-variances.md)
      - [Ajustement des prix](price-adjustment.md)
      - [Prix plancher](floor-price.md)
      - [Prix plafond facultatif](optional-ceiling-price.md)
      - [Étendue du prix](price-scope.md)
      - [Logique de priorité des prix](price-priority-logic.md)
      - [Prix des concurrents Buy Box](buy-box-competitor-pricing.md)
      - [Prix du concurrent le plus bas](lowest-competitor-pricing.md)
   - Exemples {#rules-examples}
      - [Définition d’une condition](ob-define-condition-example.md)
      - [Exemples de règles de prix](price-rule-examples.md)
- Rapports et logs {#reports-logs}
   - [Journaux et rapports de magasin](amazon-logs-reports.md)
   - Rapports de magasin {#store-reports}
      - [Analyse des prix compétitifs](competitive-price-analysis.md)
      - [Améliorations des listes](listing-improvements.md)
   - Journaux {#logs}
      - [Journal des modifications de la liste](listing-changes-log.md)
      - [Journal des erreurs de communication](communication-errors-log.md)
- Gestion des listes {#admin-listings}
   - [Gestion des listes Amazon](managing-product-listings.md)
   - Par statut/onglet {#status-tab}
      - [Gérer par statut/onglet](managing-listings-by-tab.md)
      - [Listes incomplètes](incomplete-listings.md)
      - [Nouvelles listes tierces](new-third-party-listings.md)
      - [Prêt à répertorier](ready-to-list.md)
      - [Listes inactives](inactive-listings.md)
      - [Principales listes](active-listings.md)
      - [Remplacements](overrides.md)
      - [Listes non éligibles](ineligible-listings.md)
      - [Listes terminées](ended-listings.md)
   - Par actions {#actions}
      - [Gérer par des actions](managing-listings-by-action.md)
      - [Création et affectation de produits de catalogue](creating-assigning-catalog-products.md)
      - [Créer et modifier des remplacements](creating-editing-overrides.md)
      - [Créer un SKU de fournisseur d’alias](create-alias-seller-sku.md)
      - [Modification d’un ASIN affecté](edit-assigned-asin.md)
      - [Fin d’une liste Amazon](end-listings-manually.md)
      - [Publication d’une liste Amazon](publish-listings-manually.md)
      - [Mise à jour des informations requises](amazon-manually-update-incomplete-listing.md)
      - [Afficher les détails](product-listing-details.md)
- Gestion des commandes {#admin-orders}
   - [Gestion des commandes](managing-orders.md)
   - [Afficher les commandes Amazon](amazon-orders-all.md)
   - [Affichage des détails de commande Amazon](amazon-order-details.md)
   - [Tâches de traitement de l’ordre commun](common-order-processing.md)
   - [Workflows d’exécution](fulfillment-workflows.md)
   - [Annuler les commandes non expédiées](cancel-unshipped-order.md)
- [Notes de mise à jour](release-notes.md)
