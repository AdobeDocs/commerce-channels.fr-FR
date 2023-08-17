---
title: Afficher les détails de la liste Amazon
description: Pour comprendre les mesures de concurrence sur vos listes Amazon et les modifications individuelles des SKU/produits, consultez la page Détails de la liste de produits .
feature: Sales Channels, Products, Merchandising
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Afficher les détails de la liste Amazon

La variable _[!UICONTROL Product Listing Details]_La page affiche des informations supplémentaires sur vos listes de produits actives, y compris le journal d’activité d’énumération qui affiche les modifications sur un SKU/produit individuel. Ces informations peuvent vous aider à comprendre les mesures de compétitivité de vos produits et des modifications individuelles des SKU/produits. Informations supplémentaires sur cette page :

- **[!UICONTROL Listing Details]** - Détails du produit, notamment le SKU Nom et Vendeur Amazon
- **[!UICONTROL Listing Activity Log]** - Historique de toutes les modifications apportées à cette liste, telles que les modifications de prix et de quantité/stock. Aucune autre action n’est requise. Ce journal peut être consulté pour comprendre l’historique des modifications.
- **[!UICONTROL Buy Box Competitor Pricing]** - Données pour Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) tarification du statut et des concurrents
- **[!UICONTROL Lowest Competitor Pricing]** - Informations sur le prix du concurrent Amazon le plus bas et informations de retour

Les pages d’accueil du canal de vente Amazon partagent certaines [contrôles workspace](./workspace-controls.md) qui vous permettent de personnaliser les données affichées.

## Détails de la liste

Les informations sur les produits affichées incluent :

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![Détails de la liste](assets/amazon-product-listing-details.png){width="600" zoomable="yes"}

## Journal des activités d’énumération {#listing-activity-log}

Affiche toutes les activités récentes de la liste Amazon. Les informations affichées sont les suivantes :

- SKU du vendeur Amazon : identifie l’unité de gestion des stocks (SKU) définie pour la liste.
- ASIN : identifie l’identifiant de produit Amazon à 10 chiffres.
- Action de liste : identifie le type d’action survenue pour la liste.
- Commentaires : fournit des détails supplémentaires relatifs au type d’action de liste qui s’est produite.
- Exécuté à : identifie la date et l’heure auxquelles l’action a eu lieu.

![Détails de la liste de produits - Journal d’activité de liste](assets/amazon-listing-activity-log.png){width="600" zoomable="yes"}
__

## Prix des concurrents Buy Box {#buy-box-competitor-pricing}

Cet onglet affiche des informations sur le commerçant Amazon qui détient le [[!DNL Buy Box]](./buy-box-competitor-pricing.md) position de la liste. Ces informations peuvent être utilisées pour comprendre le positionnement des prix de vos concurrents sur Amazon. Les informations affichées sont les suivantes :

- ASIN : identifiant de produit Amazon à 10 chiffres.
- Est-ce que le vendeur : indique si vous êtes le [!DNL Buy Box] vendeur. Options Oui / Non.
- Condition : identifie la condition définie pour la liste.
- Prix d’énumération : indique le prix auquel la liste a été publiée.
- Prix de livraison : indique le prix de livraison ajouté à la liste.
- Prix d’entrée : indique le prix d’entrée plus le prix d’expédition pour la liste.
- Dernière mise à jour : identifie la date et l’heure de mise à jour des informations de tarification à partir d’Amazon.

![Détails de la liste de produits : prix des concurrents Buy Box](assets/amazon-listing-details-buy-box-2.png){width="600" zoomable="yes"}

## Prix du concurrent le plus bas {#lowest-competitor-pricing}

Cet onglet affiche des informations sur les concurrents Amazon pour la même liste. Ces informations peuvent être utilisées pour comprendre le positionnement des prix et [prix concurrentiel le plus bas](./lowest-competitor-pricing.md). Les informations affichées sont les suivantes :

- ASIN : identifiant de produit Amazon à 10 chiffres.
- Condition : identifie la condition définie pour la liste.
- Canal d’exécution : identifie le responsable de l’exécution. Options : marchand/Amazon.
- Prix d’énumération : indique le prix auquel la liste a été publiée.
- Prix de livraison : indique le prix de livraison ajouté à la liste.
- Prix d’entrée : indique le prix d’entrée plus le prix d’expédition pour la liste.
- Note de retour : identifie la note de retour Amazon pour le marchand au prix le plus bas.
- Décompte de commentaires : identifie le nombre de commentaires Amazon pour le marchand au prix le plus bas.
- Dernière mise à jour : identifie la date et l’heure de mise à jour des informations de tarification à partir d’Amazon.

![Détails des listes de produits - prix de concurrent le plus bas](assets/amazon-listing-details-lowest-comp.png){width="600" zoomable="yes"}
