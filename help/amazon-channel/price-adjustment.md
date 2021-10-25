---
title: Ajustement du prix
description: Configurez les ajustements de prix pour définir le calcul de prix lorsque vous avez identifié la source de prix du concurrent Amazon.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Ajustement de prix

>[!NOTE]
>
>La section Ajustement de prix diffère légèrement pour les règles de tarification standard et intelligente. **[!UICONTROL Match Competitor Price]** est uniquement disponible sous _[!UICONTROL Price Action]_lorsque **[!UICONTROL Rule Type]**est défini sur `Intelligent repricing rule`.

Les sections d&#39;une règle de réévaluation intelligente comprennent :

- [Sélectionner le type de règle](./intelligent-repricing-rules.md)
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- Ajustement du prix
- [Prix plancher](./floor-price.md)
- [Prix plafond facultatif](./optional-ceiling-price.md)

L&#39;ajustement de prix définit le calcul du prix lorsque vous avez identifié la source de prix du concurrent.

## Configurer l&#39;ajustement de prix

Définissez votre ajustement de tarification dans la section _[!UICONTROL Price Adjustment]_.

1. Pour **[!UICONTROL Price Action]**, choisissez une option :

   - `Decrease By` - Choisissez quand vous voulez que la valeur de la source de prix définie soit ajustée à la baisse, créant ainsi un prix plus bas pour la règle, avant d&#39;inscrire sur Amazon.

   - `Increase By` - Choisissez quand vous souhaitez ajuster la valeur de la source de prix définie, créant ainsi un prix plus élevé pour la règle, avant d&#39;inscrire sur Amazon.

   - `Match Competitor Price` - (Règle de tarification intelligente uniquement) Choisissez quand vous souhaitez modifier le prix de votre annonce Amazon pour qu’il corresponde au [concurrent le plus bas](./lowest-competitor-pricing.md) prix, en fonction des commentaires de vos concurrents et des paramètres d’écart. Lorsque la valeur est définie sur `Match Competitor Price`, le _[!UICONTROL Apply]_et_[!UICONTROL Adjustment Amount]_ sont supprimés.

1. Pour **[!UICONTROL Apply]**, choisissez une option :

   - `Apply as percentage` - Choisissez quand vous souhaitez définir **[!UICONTROL Magento Price Source]** défini dans votre [Prix d&#39;annonce](./listing-price.md) ajusté d&#39;un pourcentage.

   - `Apply as fixed amount` - Choisissez quand vous souhaitez définir **[!UICONTROL Magento Price Source]** défini dans votre [Prix d&#39;annonce](./listing-price.md) rajusté d&#39;un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), entrez la valeur numérique de l’ajustement de prix.

   - Lorsque **[!UICONTROL Apply]** est défini sur `Apply as percentage`, entrez la valeur de pourcentage (exemple : entrer `25` pour un réglage de 25 %).

   - Lorsque **[!UICONTROL Apply]** est défini sur `Apply as fixed amount`, entrez la valeur numérique du montant fixe (exemple : entrer `25` pour un ajustement fixe de 25 $).

![Règle de réévaluation intelligente - ajustement des prix](assets/amazon-price-adjustment.png)

| Champ | Description |
|---|---|
| [!UICONTROL Price Action] | Sélectionnez une action d&#39;ajustement de tarification. Options :<br>**[!UICONTROL Decrease By]**- Choisissez quand vous souhaitez définir _[!UICONTROL Magento Price Source]_défini dans votre [Prix d&#39;annonce](./listing-price.md) à ajuster à la baisse, créant un prix plus bas pour la règle, avant d&#39;inscrire à Amazon.<br>**[!UICONTROL Increase By]**- Choisissez quand vous souhaitez définir_[!UICONTROL Magento Price Source]_ défini dans votre [Prix d&#39;annonce](./listing-price.md) à ajuster, créant un prix plus élevé pour la règle, avant d&#39;être coté en Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Règle de tarification intelligente uniquement) Choisissez quand vous souhaitez modifier le prix de votre annonce Amazon pour qu’il corresponde au [concurrent le plus bas](./lowest-competitor-pricing.md) prix, en fonction des commentaires de vos concurrents et des paramètres d’écart. Lorsque cette option est sélectionnée, la _Appliquer_ et _Montant de réglage_ sont supprimés. |
| [!UICONTROL Apply] | Options :<br>**[!UICONTROL Apply as percentage]**- Choisissez quand vous souhaitez définir _[!UICONTROL Magento Price Source]_défini dans votre [Prix d&#39;annonce](./listing-price.md) ajusté d&#39;un pourcentage.<br>**[!UICONTROL Apply as fixed amount]**- Choisissez quand vous souhaitez définir_[!UICONTROL Magento Price Source]_ défini dans votre [Prix d&#39;annonce](./listing-price.md) rajusté d&#39;un montant fixe. |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br>Si vous avez choisi `Apply as percentage` pour **[!UICONTROL Apply]**, entrez la valeur de pourcentage (exemple : entrer `25` pour un réglage de 25 %).<br>Si vous avez choisi `Apply as fixed amount` pour **[!UICONTROL Apply]**, entrez la valeur numérique du montant fixe (exemple : entrer `25` pour un ajustement fixe de 25 $). |
