---
title: Commandes de l’espace de travail
description: Amazon Sales Channel fournit des commandes d’espace de travail qui vous permettent de localiser des annonces, d’afficher des informations et d’appliquer facilement des actions.
exl-id: 4f76b1d0-ae58-435b-bd6d-50155a023421
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# Contrôles de l’espace de travail

Canal de vente Amazon [page d&#39;accueil](./amazon-sales-channel-home.md) dispose de commandes d’espace de travail courantes, notamment Filtres, Affichage par défaut, Colonnes et Exporter. Toutes les pages ne disposent pas des mêmes options de contrôle.

![Exemples de contrôle de l’espace de travail Sales Channel Amazon](assets/amazon-workspace-controls.png)

## Actions

Le _[!UICONTROL Actions]_sélecteur fournit une liste d’actions disponibles pour un utilisateur pour une page. Lorsque cette option est sélectionnée, l’action est appliquée à tous les éléments sélectionnés. Pour appliquer une action à un élément spécifique, cochez la case dans la première colonne de chaque élément et choisissez une option sous_[!UICONTROL Actions]_.

Par exemple, lorsque le sélecteur s’affiche sur la _[!UICONTROL Attributes]_, il inclut_[!UICONTROL Re-import Product Attribute Values]_ action. Si vous sélectionnez cette action, les calques correspondants sont [!DNL Amazon Seller Central] et actualise la [!DNL Commerce] pour chacun des éléments du magasin Amazon archivés dans la colonne de gauche.

![Exemple de menu Actions](assets/amazon-sales-channel-home-actions-option.png)

## Filtres

Le _[!UICONTROL Filters]_affiche les options permettant de réduire les données affichées dans le tableau. Les options de filtre sont basées sur les colonnes sélectionnées dans le contrôle Colonnes. Les options de filtre s’affichent uniquement pour les colonnes activées dans le contrôle Colonnes.

Les contrôles de filtres peuvent inclure des calendriers dynamiques pour limiter les données pour les dates spécifiées, des menus déroulants pour les colonnes ayant des sélections prédéfinies et des champs de texte libre pouvant contenir des données personnalisées.

L&#39;exemple suivant montre les paramètres de filtrage de la liste des commandes pour afficher uniquement les commandes qui répondent aux critères suivants :

- Commandes effectuées entre le 01/02/2019 et le 07/2019, et
- Commandes avec un acheteur nommé de `Smith`et
- Commandes ayant le statut `Shipped`.

Lorsque vos options de filtrage sont définies, cliquez sur **[!UICONTROL Apply Filters]** pour filtrer les données répertoriées. Cliquez sur Annuler pour quitter le contrôle Filtres sans appliquer.

![Exemple de contrôle Filtres](assets/workspace-controls-filters.png)

Après avoir appliqué des filtres à vos données, **[!UICONTROL Active Filters]** des informations s&#39;affichent. Vous pouvez cliquer sur le bouton ![Icône Effacer les filtres](assets/x-icon-clear-filters.png) pour effacer une option de filtre spécifique ou cliquez sur **[!UICONTROL Clear All]** pour effacer tous les filtres appliqués.

![Exemple de filtres actifs](assets/applied-filters-line.png)

## Affichage

Le contrôle Affichage est basé sur les colonnes par défaut de la page, il est donc nommé Vue par défaut. Vous pouvez ajouter ou supprimer des colonnes disponibles à l’aide du contrôle Colonnes. Lorsque vous personnalisez vos colonnes, vous pouvez ensuite enregistrer la vue en tant que vue personnalisée dans le contrôle Affichage.

Lorsque vos colonnes sont ajoutées ou supprimées de l’affichage de la page :

1. Cliquez sur **[!UICONTROL Default View]** > **[!UICONTROL Save View As...]**.

1. Saisissez un nom pour la vue.

1. Pour enregistrer la vue personnalisée, cliquez sur l’icône de flèche.

![Afficher l’exemple de contrôle](assets/workspace-controls-view.png)

Dans cet exemple, la propriété _ID de commande_ est ajoutée dans le contrôle Colonne et enregistrée en tant qu’affichage personnalisé. Une fois le nom de la vue personnalisée enregistré, le nom de la vue a changé. _Affichage par défaut_ au nom saisi.

Vous pouvez basculer entre les vues en sélectionnant la vue souhaitée dans le menu _[!UICONTROL View]_.

Si vous souhaitez supprimer ou modifier le nom de votre vue personnalisée, cliquez sur l’icône de crayon. Vous pouvez ensuite entrer un autre nom ou cliquer sur l’icône de corbeille pour supprimer la vue personnalisée. Impossible de supprimer la vue par défaut.

## Colonnes

Le contrôle Colonnes vous permet d’ajouter ou de supprimer des colonnes de données de l’affichage de la page. Chaque page du canal de vente Amazon comporte une combinaison prédéfinie de colonnes de données, mais la plupart des pages disposent de colonnes supplémentaires. Si aucune colonne supplémentaire n’est disponible, vous pouvez toujours supprimer les colonnes par défaut de l’affichage.

L&#39;exemple suivant montre un contrôle Columns. Les options cochées correspondent aux en-têtes de colonne affichés sur la page.

- Pour ajouter une colonne de données à votre page, cochez la case correspondante.
- Pour supprimer une colonne de données de votre page, ne cochez pas la case.

![Exemple de contrôle Colonnes](assets/workspace-controls-columns.png)

Les modifications apportées à la case à cocher s’affichent immédiatement. Si vous apportez des modifications et que vous quittez la page, celle-ci revient à l’affichage de colonne par défaut. Pour les modifications que vous apportez régulièrement, vous pouvez enregistrer les modifications apportées aux colonnes en tant qu’affichage personnalisé dans le contrôle Affichage. Vous pouvez ensuite activer ou désactiver le contrôle Affichage sans avoir à ajouter ou supprimer des colonnes manuellement.

Vous pouvez cliquer sur **[!UICONTROL Reset]** pour rétablir les paramètres par défaut des options, ou vous pouvez cliquer sur **[!UICONTROL Cancel]** pour quitter sans vos modifications.

## Exporter

L’option Exporter vous permet d’exporter les données vers un fichier de données qui peut être importé dans un logiciel tiers ou une base de données distincte. Les données exportées sont limitées aux données affichées. Si nécessaire, assurez-vous d’ajouter ou de supprimer des colonnes avant d’utiliser le contrôle Exporter.

Lorsque vous êtes prêt à exporter vos données, sélectionnez une option de format d’exportation et cliquez sur **[!UICONTROL Export]**.

- CSV : fichier de valeurs séparé par des virgules contenant des données de texte brut
- Excel XML : format de données de feuille de calcul basé sur XML (généralement utilisé pour les utilisateurs d’Excel)

Le fichier de données généré s’enregistre automatiquement dans le dossier désigné pour les téléchargements.

![Contrôle d’exportation](assets/workspace-controls-export.png)
