---
title: Actions des règles de prix standard
description: Utilisez les actions standard de règle de prix pour augmenter ou diminuer le prix d’une offre Amazon par rapport au prix du catalogue de commerce (ou à la source du prix).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Actions des règles de prix standard

Une action de règle de prix standard vous permet d’augmenter ou de diminuer un prix d’achat d’Amazon d’un pourcentage spécifique ou d’un montant fixe en dollars par rapport au [!DNL Commerce] prix du catalogue (ou source du prix).

Les sections d’une action standard de règle de prix incluent :

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configuration des actions de règle de prix

1. Pour **[!UICONTROL Rule Type]**, choisissez `Standard price rule`.

   Cette option désactive les autres champs de la variable _[!UICONTROL Select Rule Type]_.

1. Développez l’objet _[!UICONTROL Price Adjustment]_, le cas échéant.

1. Pour **[!UICONTROL Price Action]**, choisissez une option pour déterminer comment modifier la variable *[!UICONTROL Magento Price Source]* (défini dans votre [Prix d’énumération](./listing-price.md)).

   - `Decrease By` - Choisissez quand vous souhaitez que la valeur soit réduite avant de la répertorier sur Amazon.

   - `Increase By` - Choisissez quand vous souhaitez augmenter la valeur avant de l’ajouter à Amazon.

1. Pour **[!UICONTROL Apply]**, choisissez une option pour déterminer le mode de définition de la variable *[!UICONTROL Magento Price Source]* défini dans votre [Prix d’énumération](./listing-price.md) valeur à ajuster :

   - `Apply as percentage` - Choisissez quand vous souhaitez que la variable *[!UICONTROL Magento Price Source]* défini dans votre [Prix d’énumération](./listing-price.md) valeur ajustée en pourcentage

   - `Apply as fixed amount` - Choisissez quand vous souhaitez que la variable *[!UICONTROL Magento Price Source]* défini dans votre [Prix d’énumération](./listing-price.md) ajustée d’un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), saisissez la valeur numérique de l’ajustement de prix.

   - When *[!UICONTROL Apply]* est défini sur `Apply as percentage`, saisissez la valeur de pourcentage (exemple : enter `25` pour un ajustement de prix de 25 %).

   - When *[!UICONTROL Apply]* est défini sur `Apply as fixed amount`, saisissez la valeur numérique du montant fixe (exemple : enter `25` pour un ajustement de prix fixe de 25 $).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save pricing rule]**.

![Règle de prix standard](assets/ob-price-rule-action-standard-example.png)

| Champ | Description |
|---|---|
| [!UICONTROL Rule Type] | Sélectionner `Standard price rule`. |
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez que la variable [!DNL Commerce] valeur de la source de prix à diminuer avant d’être mise en vente dans Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez que la variable [!DNL Commerce] valeur de la source de prix à augmenter avant d’être mise en vente dans Amazon.</li></ul> |
| [!UICONTROL Apply] | Options :<ul><li>**[!UICONTROL Apply as percentage]** - Choisissez quand vous souhaitez que la variable [!DNL Commerce] valeur de la source du prix ajustée d’un pourcentage.</li><li>**[!UICONTROL Apply as fixed amount]** - Choisissez quand vous souhaitez que la variable [!DNL Commerce] valeur de la source du prix ajustée d’un montant fixe.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br><br>Si vous choisissez `Apply as percentage` pour *[!UICONTROL Apply]*, saisissez la valeur de pourcentage (exemple : enter `25` pour un ajustement de 25 %).<br><br>Si vous choisissez `Apply as fixed amount` pour *[!UICONTROL Apply]*, saisissez la valeur numérique du montant fixe (exemple : enter `25` pour un ajustement fixe de 25 $). |
