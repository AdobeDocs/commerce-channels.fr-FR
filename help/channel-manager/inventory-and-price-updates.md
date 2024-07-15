---
title: Mises à jour du stock et du prix
description: '"[!DNL Channel Manager]" synchronise les mises à jour de stock et de prix entre le  [!DNL Commerce] magasin et  [!DNL Walmart Marketplace] afin que vous puissiez gérer les opérations de vos canaux de vente à partir de l’ [!DNL Commerce] administrateur"'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Mise à jour de l’inventaire et des tarifs

[!DNL Channel Manager] effectue le suivi de l’inventaire et de la tarification des produits du catalogue de produits [!DNL Commerce] et synchronise les mises à jour du canal de vente connecté et de [!DNL Walmart Marketplace]. L’opération de synchronisation permet de s’assurer que les listes de produits reflètent la quantité et le prix actuels du stock.


>[!IMPORTANT]
>
>Une fois [!DNL Channel Manager] installé et configuré, toutes les mises à jour de stock, de prix et de commande sont synchronisées automatiquement. Si vous vendez déjà sur Walmart Marketplace, veillez à désactiver toutes les autres intégrations qui mettent à jour les données de produit et de commande. Ensuite, vérifiez que les niveaux de stock et les prix du stock dans le storefront [!DNL Commerce] sont précis et correspondent aux données dans [!DNL Walmart Marketplace] avant de connecter [!DNL Channel Manager] à la boutique en ligne.


## Mises à jour du stock

Lorsque les niveaux d’inventaire des produits changent dans [!DNL Commerce], [!DNL Channel Manager] synchronise les mises à jour dans [!DNL Walmart Marketplace]. La synchronisation des mises à jour d’inventaire sur le canal des ventes avec [!DNL Walmart marketplace] peut prendre jusqu’à 10 minutes.

* **Mises à jour de la quantité en stock dans le catalogue de produits**—Lorsque [!DNL Commerce] la quantité en stock change en raison de [ changements manuels de quantité en stock ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), remboursements ou annulations, [!DNL Channel Manager] synchronise la modification sur les canaux connectés et [!DNL Walmart Marketplace].

* **Réduire la quantité de stock pour refléter [!DNL Walmart Marketplace] commandes** : après la synchronisation d’une commande [!DNL Walmart Marketplace] vers [!DNL Channel Manager], [!DNL Channel Manager] envoie la mise à jour au système de commande [!DNL Commerce]. [!DNL Commerce] ajuste les quantités de stock en fonction de la commande. Ensuite, la quantité mise à jour est synchronisée avec [!DNL Walmart Marketplace]. Tant que les opérations de synchronisation ne sont pas terminées, vous pouvez voir différentes quantités dans les listes de canaux de vente et [!DNL Walmart].

>[!IMPORTANT]
>
>Après la synchronisation d&#39;une commande [!DNL Walmart Marketplace] vers [!DNL Channel Manager], les quantités de stock et les informations de commande sont mises à jour uniquement pour les remboursements et annulations lancés à partir de [!DNL Commerce]. Si une commande est remboursée ou annulée à partir de [!DNL Walmart marketplace], traitez la modification de [!DNL Commerce] pour garantir l’exactitude des [!DNL Commerce] quantités d’inventaire et des informations de commande.

## Mises à jour des prix

Lorsque le prix du produit change dans [!DNL Commerce], [!DNL Channel Manager] synchronise la mise à jour vers [!DNL Walmart Marketplace]. Cela peut prendre jusqu’à cinq minutes pour que le changement de prix s’affiche dans la liste [!DNL Walmart Marketplace].

### Gestion des tarifs d’un produit connecté

1. Dans [!UICONTROL Admin], sélectionnez **[!UICONTROL Catalog > Products]**.
1. Dans la grille de produit, recherchez le produit à mettre à jour et sélectionnez **[!UICONTROL Edit]**.
1. Passez en revue et mettez à jour le prix suivant vos besoins.
1. **[!UICONTROL Save]** de la modification.

Pour obtenir de l’aide sur la gestion de la configuration des prix des produits dans [!DNL Commerce], voir [Gestion des prix](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
