---
title: Afficher les commandes Amazon
description: Affichez vos commandes Amazon Marketplace dans l’administrateur Adobe Commerce ou Magento Open Source.
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Afficher les commandes Amazon

Vous pouvez afficher vos commandes Amazon de deux manières différentes : _[!UICONTROL Recent Orders]_et_[!UICONTROL All Orders]_.

Les deux options vous présentent des informations de commande de base, telles qu’elles sont reçues d’Amazon, notamment :

- Date d’achat
- Numéro de commande
- État
- Nom de l’acheteur
- Total général
- Notes de commande

_[!UICONTROL All Orders]_vue ajoute des options de filtrage pour les recherches de commande.

>[!NOTE]
>
>Sauf pour le _[!UICONTROL Order Notes]_, la variable_[!UICONTROL Amazon orders]_ est renseigné avec les informations de commande reçues d’Amazon. Le _Notes de commande_ est mise à jour par [!DNL Commerce] pendant le traitement de la commande.

## Commandes récentes

Vous pouvez afficher vos commandes les plus récentes dans la _[!UICONTROL Recent Orders]_de la section [tableau de bord de la boutique](./amazon-store-dashboard.md).

![Commandes récentes](assets/amazon-recent-orders-imported.png)

### Afficher les commandes Amazon récentes

1. Cliquez sur **[!UICONTROL View Store]** sur une carte de magasin.

1. Affichez vos commandes dans le _[!UICONTROL Recent Orders]_.

1. Pour afficher les détails de la commande, cliquez sur le numéro de la commande Amazon dans la _[!UICONTROL Order Number]_colonne .

   Le _[!UICONTROL Amazon Order Details]_pour la commande qui s’ouvre.

## Afficher toutes les commandes

Vous pouvez afficher toutes vos commandes Amazon sur la page _[!UICONTROL Amazon orders]_(également appelée_[!UICONTROL All Orders]_ ). Le tableau Commandes d’Amazon est semblable au tableau _[!UICONTROL Recent Orders]_du tableau de bord de la boutique, mais vous permet de visualiser toutes vos commandes Amazon et de limiter la liste de vos commandes à l’aide des options de filtrage suivantes :

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Commandes Amazon](assets/amazon-orders-list-all.png)

### Afficher toutes les commandes Amazon

1. Cliquez sur **[!UICONTROL View Store]** sur une carte de magasin.

1. Cliquez sur **[!UICONTROL All Orders]** dans le _[!UICONTROL Recent Orders]_.

1. Pour réduire la liste ou rechercher un numéro de commande spécifique, renseignez la variable **[!UICONTROL Filter by]** paramètres et cliquez sur **[!UICONTROL Apply filters]**.

1. Pour afficher les détails de la commande, cliquez sur le numéro de la commande Amazon dans la _[!UICONTROL Order Number]_colonne .

   Le _[!UICONTROL Amazon Order Details]_pour la commande qui s’ouvre.

## Utilisation des filtres

Vous pouvez appliquer des filtres à votre liste de commandes dans la variable _[!UICONTROL Filter by]_. Effectuez vos sélections et cliquez sur **[!UICONTROL Apply filters]**. Les filtres appliqués s’affichent au-dessus de la grille des commandes.

![Filtres pour l’affichage des commandes Amazon](assets/amazon-orders-filter-view.png)

### Modification des filtres appliqués

- Vous pouvez ajouter ou modifier vos filtres dans la variable _[!UICONTROL Filter by]_. Cliquez sur **[!UICONTROL Apply filters]**pour mettre à jour la liste des commandes et les options de filtrage qui apparaissent au-dessus de la grille des commandes.

- Vous pouvez supprimer des filtres un par un en cliquant sur l’icône `x` pour le filtre ou tout à la fois en cliquant sur **[!UICONTROL Clear all filters]**. La suppression d’un filtre met à jour la liste des commandes et les options de filtrage qui apparaissent au-dessus de la grille des commandes.

- Si votre liste de commandes est longue, vous pouvez utiliser les commandes de pagination situées sous la grille pour afficher davantage de commandes.

>[!TIP]
>
>Quelques conseils sur la vue des commandes :
>
>- Si vous disposez de plusieurs intégrations de magasin Amazon, une actualisation de la page vue lors du basculement entre les vues de magasin peut s’avérer nécessaire pour mettre à jour la liste des commandes et les vues de pagination du magasin actuel.
>- Lors du tri par colonne, le tri ne s’applique qu’au mode Liste actuel. Il est recommandé de filtrer votre liste, puis de trier la page que vous affichez.
>- Selon la largeur de la fenêtre d’affichage, le texte des colonnes peut se chevaucher. Pour agrandir les colonnes pour que le texte soit renvoyé à la ligne, élargissez la vue de la fenêtre.
>- Lors du filtrage par _[!UICONTROL Total]_, filtrez par nombres entiers. La saisie d’un nombre décimal peut entraîner des erreurs dans les résultats.


### Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Filter by] | Disponible uniquement dans le _[!UICONTROL All Orders]_vue.<br>Limitez la liste des commandes en fonction des éléments suivants :<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Date de l’achat, telle qu’elle a été reçue d’Amazon. |
| [!UICONTROL Order Number] | Numéro de commande généré par et reçu d’Amazon. Pour afficher l’écran Détails de la commande Amazon, cliquez sur le lien. |
| [!UICONTROL Status] | État de la commande, tel qu’il est reçu par Amazon. Options : `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Nom de la personne qui a passé la commande, tel qu’il a été reçu d’Amazon. |
| [!UICONTROL Grand Total] | Valeur monétaire totale de la commande, telle qu’elle est reçue d’Amazon. |
| [!UICONTROL Order Notes] | Action la plus récente enregistrée pour la commande lors de son traitement dans [!DNL Commerce]. Les informations incluent, sans s’y limiter, les erreurs d’importation de commande et les mises à jour de traitement des commandes.<br>**Remarque**: Ce champ est mis à jour par [!DNL Commerce] pendant le traitement de la commande. |
