---
title: Actions des règles de prix standard
description: Utilisez les actions standard de règle de prix pour augmenter ou diminuer le prix d’une offre Amazon par rapport au prix du catalogue de commerce (ou à la source du prix).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Actions de règle de prix standard

Une action de règle de prix standard vous permet d’augmenter ou de diminuer le prix d’une offre Amazon d’un pourcentage spécifique ou d’un montant fixe en dollars par rapport au prix du catalogue [!DNL Commerce] (ou source de prix).

Les sections d’une action standard de règle de prix incluent :

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configuration des actions de règle de prix

1. Pour **[!UICONTROL Rule Type]**, choisissez `Standard price rule`.

   Cette option désactive les autres champs de la section _[!UICONTROL Select Rule Type]_.

1. Développez la section _[!UICONTROL Price Adjustment]_, si nécessaire.

1. Pour **[!UICONTROL Price Action]**, choisissez une option afin de déterminer comment modifier la valeur *[!UICONTROL Magento Price Source]* (définie dans votre valeur [Prix d’énumération](./listing-price.md)).

   - `Decrease By` - Choisissez quand vous souhaitez que la valeur soit réduite avant de la répertorier sur Amazon.

   - `Increase By` - Choisissez quand vous souhaitez augmenter la valeur avant de l’ajouter à Amazon.

1. Pour **[!UICONTROL Apply]**, choisissez une option afin de déterminer la façon dont vous souhaitez ajuster le *[!UICONTROL Magento Price Source]* défini dans votre valeur [Prix d’énumération](./listing-price.md) :

   - `Apply as percentage` - Choisissez quand vous souhaitez que la valeur définie  *[!UICONTROL Magento Price Source]* dans votre  [prix de ](./listing-price.md) liste soit ajustée d&#39;un pourcentage

   - `Apply as fixed amount` - Sélectionnez cette option lorsque vous souhaitez que la valeur définie  *[!UICONTROL Magento Price Source]* dans votre  [prix de ](./listing-price.md) liste soit ajustée d’un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), saisissez la valeur numérique de l’ajustement de prix.

   - Lorsque *[!UICONTROL Apply]* est défini sur `Apply as percentage`, saisissez la valeur de pourcentage (exemple : saisissez `25` pour un ajustement de prix de 25 %).

   - Si *[!UICONTROL Apply]* est défini sur `Apply as fixed amount`, saisissez la valeur numérique de la valeur fixe (exemple : saisissez `25` pour un ajustement de prix fixe de 25 $).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save pricing rule]**.

![Règle de prix standard](assets/ob-price-rule-action-standard-example.png)

| Champ | Description |
|---|---|
| [!UICONTROL Rule Type] | Sélectionnez `Standard price rule`. |
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez le moment où vous souhaitez que la valeur de source de  [!DNL Commerce] prix définie soit réduite avant d’être cotée à Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez que la valeur de source de  [!DNL Commerce] prix définie soit augmentée avant d’être mise en vente dans Amazon.</li></ul> |
| [!UICONTROL Apply] | Options :<ul><li>**[!UICONTROL Apply as percentage]** - Sélectionnez cette option lorsque vous souhaitez que la valeur de  [!DNL Commerce] prix source définie soit ajustée d’un pourcentage.</li><li>**[!UICONTROL Apply as fixed amount]** - Sélectionnez cette option lorsque vous souhaitez que la valeur source de  [!DNL Commerce] prix définie soit ajustée d’un montant fixe.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br><br>Si vous choisissez  `Apply as percentage` pour  *[!UICONTROL Apply]*, saisissez la valeur de pourcentage (exemple : saisissez  `25` un ajustement de 25 %).<br><br>Si vous choisissez  `Apply as fixed amount` pour  *[!UICONTROL Apply]*, saisissez la valeur numérique du montant fixe (exemple : saisissez  `25` un ajustement fixe de 25 $). |
