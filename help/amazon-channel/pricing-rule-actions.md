---
title: Canal vente Amazon - Actions de règle de prix
description: Utilisez les actions de règle de prix pour définir les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la mise en vente d’Amazon.
feature: Sales Channels, Price Rules
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Actions de règle de prix

Règle de prix Les actions définissent les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la mise en vente.

## Règle de prix standard

A [règle de prix standard](./standard-price-rules.md) vous permet d’augmenter ou de diminuer le prix d’une offre Amazon d’un pourcentage spécifique ou d’un montant fixe en dollars par rapport à la valeur [!DNL Commerce] prix du catalogue (ou source du prix).

| Section | Description |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | Définissez le type de règle sur `Standard price rule`. |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | Définissez les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la vente. |

## Règle de retarification intelligente

Un [règle de retarification intelligente](./intelligent-repricing-rules.md) utilise les tarifs des concurrents d’Amazon pour déterminer le prix de votre offre. Les concurrents sont d’autres vendeurs qui répertorient les mêmes produits que ceux répertoriés sur Amazon.

| Section | Description |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | Définissez le type de règle sur `Intelligent repricing rule` ainsi que vos exigences en matière de source de prix et de retour des concurrents. |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | Définissez des écarts pour les conditions du même produit vendu par des concurrents. |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | Définissez les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la vente. |
| [[!UICONTROL Floor Price]](./floor-price.md) | Définissez le prix le plus bas pour un produit afin d’empêcher plusieurs règles de tarification de définir un prix de vente trop bas. |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | Définissez le prix le plus élevé d’un produit pour vous assurer que vos prix restent compétitifs. |
