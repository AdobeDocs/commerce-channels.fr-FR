---
title: Mises à jour du stock et du prix
description: '[!DNL Channel Manager] synchronise les mises à jour de stock et de prix entre les [!DNL Commerce] stocker et [!DNL Walmart Marketplace] afin que vous puissiez gérer vos opérations de canal de vente à partir de la variable [!DNL Commerce] Admin'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Mise à jour de l’inventaire et des tarifs

[!DNL Channel Manager] effectue le suivi du stock et de la tarification des produits dans la variable [!DNL Commerce] catalogue de produits et synchronise les mises à jour sur le canal de vente connecté et [!DNL Walmart Marketplace]. L’opération de synchronisation permet de s’assurer que les listes de produits reflètent la quantité et le prix actuels du stock.


>[!IMPORTANT]
>
>Après [!DNL Channel Manager] est installé et configuré, toutes les mises à jour de stock, de prix et de commande sont synchronisées automatiquement. Si vous vendez déjà sur Walmart Marketplace, veillez à désactiver toutes les autres intégrations qui mettent à jour les données de produit et de commande. Ensuite, vérifiez les niveaux et les prix des stocks dans la variable [!DNL Commerce] storefront est précis et correspond aux données de [!DNL Walmart Marketplace] avant de vous connecter [!DNL Channel Manager] à la boutique en ligne.


## Mises à jour du stock

Lorsque les niveaux d’inventaire des produits changent [!DNL Commerce], [!DNL Channel Manager] synchronise les mises à jour de la variable [!DNL Walmart Marketplace]. La synchronisation des mises à jour d’inventaire sur le canal des ventes peut prendre jusqu’à 10 minutes. [!DNL Walmart marketplace].

* **Mises à jour de la quantité en stock dans le catalogue de produits**—When [!DNL Commerce] la quantité de stock change en raison de [modifications manuelles de la quantité de stock](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), les remboursements ou les annulations, [!DNL Channel Manager] synchronise la modification avec les canaux connectés et [!DNL Walmart Marketplace].

* **Réduire la quantité de stock pour refléter [!DNL Walmart Marketplace] commandes**—Après un [!DNL Walmart Marketplace] synchroniser les synchronisations avec [!DNL Channel Manager], [!DNL Channel Manager] envoie la mise à jour au [!DNL Commerce] système de commande. [!DNL Commerce] ajuste les quantités en stock en fonction de la commande. Ensuite, la quantité mise à jour est synchronisée avec [!DNL Walmart Marketplace]. Tant que les opérations de synchronisation ne sont pas terminées, les quantités des listes de canaux de vente peuvent différer et [!DNL Walmart].

>[!IMPORTANT]
>
>Après une [!DNL Walmart Marketplace] synchroniser les synchronisations avec [!DNL Channel Manager], les informations sur les stocks et les commandes ne sont mises à jour que pour les remboursements et les annulations lancés à partir de [!DNL Commerce]. Si une commande est remboursée ou annulée à partir de la variable [!DNL Walmart marketplace], traitez la modification à partir de [!DNL Commerce] pour garantir l’exactitude des [!DNL Commerce] quantité de stock et informations sur la commande.

## Mises à jour des prix

Lorsque le prix du produit change dans [!DNL Commerce], [!DNL Channel Manager] synchronise la mise à jour avec la variable [!DNL Walmart Marketplace]. Le changement de prix peut prendre jusqu’à cinq minutes pour s’afficher dans la variable [!DNL Walmart Marketplace] Liste.

### Gestion des tarifs d’un produit connecté

1. Dans la [!UICONTROL Admin], sélectionnez **[!UICONTROL Catalog > Products]**.
1. Dans la grille de produit, recherchez le produit à mettre à jour et sélectionnez **[!UICONTROL Edit]**.
1. Passez en revue et mettez à jour le prix suivant vos besoins.
1. **[!UICONTROL Save]** la modification.

Pour obtenir de l’aide sur la gestion de la configuration des prix des produits dans [!DNL Commerce], voir [Gérer les tarifs](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
