---
title: Canal de vente Amazon - [!UICONTROL Price Adjustment]
description: Configurez les ajustements de prix pour définir le calcul des prix lorsque vous avez identifié la source de prix du concurrent Amazon.
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>La section Ajustement des prix diffère légèrement pour les règles de tarification standard et intelligente. **[!UICONTROL Match Competitor Price]** n’est disponible que sous _[!UICONTROL Price Action]_lorsque **[!UICONTROL Rule Type]**est défini sur `Intelligent repricing rule`.

Les sections d’une règle de retarification intelligente incluent :

- [Sélectionner le type de règle](./intelligent-repricing-rules.md)
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- Ajustement des prix
- [Prix plancher](./floor-price.md)
- [Prix de plafond facultatif](./optional-ceiling-price.md)

L&#39;ajustement de prix définit le calcul du prix lorsque vous avez identifié la source de prix du concurrent.

## Configuration de l’ajustement des prix

Définissez votre ajustement de tarification dans la section _[!UICONTROL Price Adjustment]_.

1. Pour **[!UICONTROL Price Action]**, choisissez une option :

   - `Decrease By` - Choisissez le moment où vous souhaitez que la valeur de la source de prix définie soit ajustée, créant ainsi un prix inférieur pour la règle, avant d’être répertoriée dans Amazon.

   - `Increase By` - Choisissez le moment où vous souhaitez ajuster la valeur de la source de prix définie, créant ainsi un prix plus élevé pour la règle, avant de l’ajouter à Amazon.

   - `Match Competitor Price` - (Règle de tarification intelligente uniquement) Choisissez le moment où vous souhaitez modifier le prix de votre offre Amazon pour qu’il corresponde au prix [du concurrent le plus bas](./lowest-competitor-pricing.md), en fonction des commentaires de votre concurrent et des paramètres d’écart. Lorsqu&#39;ils sont définis sur `Match Competitor Price`, les champs _[!UICONTROL Apply]_et_[!UICONTROL Adjustment Amount]_ sont supprimés.

1. Pour **[!UICONTROL Apply]**, choisissez une option :

   - `Apply as percentage` - Choisissez le moment où vous souhaitez que le **[!UICONTROL Magento Price Source]** défini dans votre [Prix de liste](./listing-price.md) ajusté d&#39;un pourcentage.

   - `Apply as fixed amount` - Choisissez le moment où vous souhaitez que le **[!UICONTROL Magento Price Source]** défini dans votre [Prix de liste](./listing-price.md) ajusté d&#39;un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), saisissez la valeur numérique de l’ajustement de prix.

   - Lorsque **[!UICONTROL Apply]** est défini sur `Apply as percentage`, entrez la valeur de pourcentage (exemple : saisissez `25` pour un ajustement de 25 %).

   - Lorsque **[!UICONTROL Apply]** est défini sur `Apply as fixed amount`, saisissez la valeur numérique du montant fixe (par exemple : saisissez `25` pour un ajustement fixe de 25 $).

![Règle de réévaluation intelligente - ajustement de prix](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| Champ | Description |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Choisissez une action d’ajustement des prix. Options : <br>**[!UICONTROL Decrease By]**- Choisissez le moment où vous souhaitez que le _[!UICONTROL Magento Price Source]_défini dans votre [Prix de liste](./listing-price.md) soit ajusté, ce qui crée un prix inférieur pour la règle, avant de l’ajouter à Amazon.<br>**[!UICONTROL Increase By]**- Choisissez le moment où vous souhaitez que le_[!UICONTROL Magento Price Source]_ défini dans votre [Prix de liste](./listing-price.md) soit ajusté, ce qui crée un prix plus élevé pour la règle, avant de le mettre en vente dans Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Règle de tarification intelligente uniquement) Choisissez le moment où vous souhaitez modifier le prix de votre offre Amazon pour qu’il corresponde au prix [du concurrent le plus bas](./lowest-competitor-pricing.md), en fonction des commentaires de votre concurrent et des paramètres d’écart. Lorsque cette option est sélectionnée, les champs _Apply_ et _Ajustement Amount_ sont supprimés. |
| [!UICONTROL Apply] | Options : <br>**[!UICONTROL Apply as percentage]**- Choisissez quand vous souhaitez que le _[!UICONTROL Magento Price Source]_défini dans votre [Prix de liste](./listing-price.md) ajusté d&#39;un pourcentage.<br>**[!UICONTROL Apply as fixed amount]**- Choisissez le moment où vous souhaitez que le_[!UICONTROL Magento Price Source]_ défini dans votre [Prix de liste](./listing-price.md) ajusté d&#39;un montant fixe. |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br>Si vous choisissez `Apply as percentage` pour **[!UICONTROL Apply]**, saisissez la valeur de pourcentage (par exemple : saisissez `25` pour un ajustement de 25 %).<br>Si vous choisissez `Apply as fixed amount` pour **[!UICONTROL Apply]**, saisissez la valeur numérique du montant fixe (par exemple : saisissez `25` pour un ajustement fixe de 25 $). |
