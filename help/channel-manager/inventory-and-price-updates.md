---
title: Mises à jour du stock et du prix
description: '''[!DNL Channel Manager] synchronise les mises à jour de stock et de prix entre la boutique Commerce et [!DNL Walmart Marketplace] afin que vous puissiez gérer vos opérations de canal de vente à partir de votre administrateur Commerce'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Mises à jour du stock et du prix

[!DNL Channel Manager] effectue le suivi de l’inventaire et de la tarification des produits de la boutique de canaux. Lorsque le stock ou la tarification change, les mises à jour sont synchronisées avec les deux [!DNL Channel Manager] et [!DNL Walmart Marketplace] afin de refléter la quantité et le prix actuels des stocks dans les listes de produits.

## Mises à jour du stock

Lorsque les niveaux d’inventaire changent, Channel Manager synchronise les mises à jour entre Commerce et Walmart Marketplace pour s’assurer que Channel Manager et Walmart Marketplace disposent de la quantité de stock appropriée.

La synchronisation entre le Gestionnaire de canaux et le marketplace peut prendre jusqu’à 10 minutes.

* **Mises à jour de la quantité en stock dans le catalogue de produits**- Lorsque la quantité de stock Commerce change en raison de [modifications manuelles de la quantité de stock](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), les remboursements ou les annulations, Channel Manager synchronise la modification avec les canaux connectés et [!DNL Walmart Marketplace].

* **Réduire la quantité de stock pour refléter les commandes de Walmart Marketplace**- Une fois qu’une commande Walmart Marketplace est synchronisée dans Channel Manager, Channel Manager envoie la mise à jour au système de commandes Commerce. Le commerce ajuste les quantités de stock en fonction de la commande. Ensuite, la quantité mise à jour est synchronisée avec Walmart Marketplace. Tant que les opérations de synchronisation ne sont pas terminées, il se peut que le Gestionnaire de canaux et Marketplace présentent des différences de quantité.

>[!IMPORTANT]
>
> Une fois qu’une commande Walmart Marketplace est synchronisée dans Channel Manager, les quantités de stock et les informations de commande sont mises à jour uniquement pour les remboursements et les annulations lancés à partir de Commerce. Si une commande est remboursée ou annulée à partir de Walmart Marketplace, traitez le changement de Commerce pour garantir l’exactitude des quantités d’inventaire et des informations de commande du Commerce.

## Mises à jour des prix

Lorsque le prix du produit change dans Commerce, Channel Manager synchronise la mise à jour à partir de la variable [!DNL Commerce] catalogue de produits vers [!DNL Walmart Marketplace]. Il peut s’écouler jusqu’à cinq minutes avant que la marketplace affiche les changements de prix.

### Gestion des tarifs d’un produit publié

1. Dans la [!UICONTROL Admin], sélectionnez **[!UICONTROL Catalog > Products]**.
1. Dans la grille de produit, recherchez le produit à mettre à jour et sélectionnez **[!UICONTROL Edit]**.
1. Passez en revue et mettez à jour le prix suivant vos besoins.
1. **[!UICONTROL Save]** la modification.

Pour plus d’informations sur la gestion de la configuration des prix des produits dans Commerce, voir [Gérer les tarifs](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
