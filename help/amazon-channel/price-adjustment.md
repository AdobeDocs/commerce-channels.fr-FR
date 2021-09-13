---
title: Ajustement des prix
description: Configurez les ajustements de prix pour définir le calcul des prix lorsque vous avez identifié la source de prix du concurrent Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Ajustement des prix

>[!NOTE]
>
>La section Ajustement des prix diffère légèrement pour les règles de tarification standard et intelligente. **[!UICONTROL Match Competitor Price]** n’est disponible que sous  _[!UICONTROL Price Action]_lorsque **[!UICONTROL Rule Type]**est défini sur  `Intelligent repricing rule`.

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

   - `Decrease By` - Choisissez le moment où vous souhaitez que la valeur de la source de prix définie soit ajustée, créant ainsi un prix inférieur pour la règle, avant d’être mise en vente dans Amazon.

   - `Increase By` - Choisissez le moment où vous souhaitez ajuster la valeur de la source de prix définie, créant ainsi un prix plus élevé pour la règle, avant de l’attribuer à Amazon.

   - `Match Competitor Price` - (Règle de tarification intelligente uniquement) Choisissez le moment où vous souhaitez modifier le prix de votre offre Amazon pour qu’il corresponde au  [prix ](./lowest-competitor-pricing.md) le plus bas, en fonction des commentaires de votre concurrent et des paramètres d’écart. Lorsqu’ils sont définis sur `Match Competitor Price`, les champs _[!UICONTROL Apply]_et_[!UICONTROL Adjustment Amount]_ sont supprimés.

1. Pour **[!UICONTROL Apply]**, choisissez une option :

   - `Apply as percentage` - Choisissez le moment où vous souhaitez que le soit  **[!UICONTROL Magento Price Source]** défini dans votre  [prix de ](./listing-price.md) liste ajusté d’un pourcentage.

   - `Apply as fixed amount` - Sélectionnez cette option lorsque vous souhaitez que la valeur définie  **[!UICONTROL Magento Price Source]** dans votre  [prix de ](./listing-price.md) liste soit ajustée d’un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), saisissez la valeur numérique de l’ajustement de prix.

   - Lorsque **[!UICONTROL Apply]** est défini sur `Apply as percentage`, saisissez la valeur de pourcentage (exemple : saisissez `25` pour un ajustement de 25 %).

   - Si **[!UICONTROL Apply]** est défini sur `Apply as fixed amount`, saisissez la valeur numérique de la valeur fixe (exemple : saisissez `25` pour un ajustement fixe de 25 $).

![Règle de retarification intelligente - ajustement des prix](assets/amazon-price-adjustment.png)

| Champ | Description |
|---|---|
| [!UICONTROL Price Action] | Choisissez une action d’ajustement des prix. Options :<br>**[!UICONTROL Decrease By]**- Choisissez le moment où vous souhaitez que la valeur _[!UICONTROL Magento Price Source]_définie dans votre [Prix d’énumération](./listing-price.md) soit ajustée, ce qui crée un prix inférieur pour la règle, avant d’être cotée à Amazon.<br>**[!UICONTROL Increase By]**- Choisissez le moment où vous souhaitez que la_[!UICONTROL Magento Price Source]_ définition de votre  [prix de ](./listing-price.md) liste soit ajustée, ce qui crée un prix plus élevé pour la règle, avant de l’ajouter à Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Règle de tarification intelligente uniquement) Choisissez le moment où vous souhaitez modifier le prix de votre offre Amazon pour qu’il corresponde au  [prix ](./lowest-competitor-pricing.md) le plus bas, en fonction des commentaires de votre concurrent et des paramètres d’écart. Une fois sélectionnés, les champs _Appliquer_ et _Montant d’ajustement_ sont supprimés. |
| [!UICONTROL Apply] | Options :<br>**[!UICONTROL Apply as percentage]**- Choisissez quand vous souhaitez que la valeur _[!UICONTROL Magento Price Source]_définie dans votre [Prix de liste](./listing-price.md) ajusté d’un pourcentage.<br>**[!UICONTROL Apply as fixed amount]**- Sélectionnez cette option lorsque vous souhaitez que la valeur définie_[!UICONTROL Magento Price Source]_ dans votre  [prix de ](./listing-price.md) liste soit ajustée d’un montant fixe. |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br>Si vous choisissez  `Apply as percentage` pour  **[!UICONTROL Apply]**, saisissez la valeur de pourcentage (exemple : saisissez  `25` un ajustement de 25 %).<br>Si vous choisissez  `Apply as fixed amount` pour  **[!UICONTROL Apply]**, saisissez la valeur numérique du montant fixe (exemple : saisissez  `25` un ajustement fixe de 25 $). |