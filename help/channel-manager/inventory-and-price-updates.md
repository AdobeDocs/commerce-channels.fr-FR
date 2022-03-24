---
title: Mises à jour du stock et du prix
description: '"[!DNL Channel Manager] synchronise les mises à jour de stock et de prix entre la boutique Commerce et [!DNL Walmart Marketplace] afin que vous puissiez gérer les opérations de vos canaux de vente à partir de votre administrateur Commerce."'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# Mises à jour du stock et du prix

Channel Manager effectue le suivi de l’inventaire et des prix des produits publiés et synchronise les modifications dans Channel Manager et Walmart Marketplace afin de refléter la quantité et la tarification actuelles des stocks dans les listes de produits.**

## Mises à jour du stock

Lorsque les niveaux d’inventaire changent, Channel Manager synchronise les mises à jour entre le catalogue de produits Commerce et Walmart Marketplace afin que Channel Manager et Walmart Marketplace affichent la quantité actuelle de stock.

Cela peut prendre jusqu’à 5 minutes pour que les modifications d’inventaire s’affichent dans Channel Manager et Walmart Marketplace.

* **Mises à jour de la quantité en stock dans le catalogue de produits**- Si la quantité en stock de Commerce change pour un produit vendu sur Walmart en raison d’une [modification manuelle de la quantité du stock](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) Pour un remboursement ou une annulation de commande, Channel Manager synchronise la modification avec le canal de vente connecté et la variable [!DNL Walmart Marketplace].

* **Réduire la quantité de stock pour refléter les commandes de Walmart Marketplace**- Une fois qu’une commande Walmart Marketplace est synchronisée dans Channel Manager, Channel Manager envoie la mise à jour au système de commandes Commerce. Le commerce ajuste les quantités de stock en fonction de la commande. Ensuite, la quantité mise à jour est synchronisée avec Walmart Marketplace. Il peut s’agir de différences dans la quantité de stock affichée dans le Gestionnaire de canaux et dans Marketplace jusqu’à la fin des opérations de synchronisation.

>[!IMPORTANT]
>
> Une fois qu’une commande Walmart Marketplace est synchronisée dans Channel Manager, les quantités de stock et les autres informations de traitement des commandes sont mises à jour uniquement pour les remboursements et les annulations lancés à partir de Commerce. Si une commande est remboursée ou annulée à partir de Walmart Marketplace, traitez la modification provenant de Commerce pour vous assurer que les quantités d’inventaire et les informations de commande du Commerce sont exactes.

## Mises à jour des prix

Lorsque le prix du produit change dans Commerce, Channel Manager synchronise la mise à jour du catalogue de produits Commerce vers Walmart Marketplace. L’affichage des modifications de stock peut prendre jusqu’à 5 minutes.

### Gestion des tarifs d’un produit publié

1. Dans la [!UICONTROL Admin], sélectionnez **[!UICONTROL Catalog > Products]**.
1. Dans la grille de produit, recherchez le produit à mettre à jour et sélectionnez **[!UICONTROL Edit]**.
1. Passez en revue et mettez à jour le prix suivant vos besoins.
1. **[!UICONTROL Save]** la modification.

Channel Manager synchronise toutes les mises à jour de prix dans la boutique de canaux et [!DNL Walmart Marketplace]. Cette opération peut prendre jusqu’à 5 minutes.

Pour plus d’informations sur la gestion de la configuration des prix des produits dans Commerce, voir [Gérer les tarifs](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
