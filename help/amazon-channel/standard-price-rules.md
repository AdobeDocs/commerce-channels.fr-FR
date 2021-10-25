---
title: Actions sur les règles de prix standard
description: Utilisez les actions de règle de prix standard pour augmenter ou diminuer le prix d'une annonce Amazon par rapport au prix du catalogue Commerce (ou à la source de prix).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Actions de règle de prix standard

Une action de règle de prix standard vous permet d&#39;augmenter ou de diminuer le prix d&#39;une annonce Amazon d&#39;un pourcentage spécifique ou d&#39;un montant fixe en dollars par rapport au [!DNL Commerce] prix du catalogue (ou source du prix).

Les sections d&#39;une action de règle de prix standard comprennent :

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Configuration des actions de règle de prix

1. Pour **[!UICONTROL Rule Type]**, sélectionnez `Standard price rule`.

   Cette option désactive les autres champs de la _[!UICONTROL Select Rule Type]_.

1. Développez la _[!UICONTROL Price Adjustment]_si nécessaire.

1. Pour **[!UICONTROL Price Action]**, choisissez une option pour déterminer la manière dont vous souhaitez modifier la *[!UICONTROL Magento Price Source]* (défini dans votre [Prix d&#39;annonce](./listing-price.md)).

   - `Decrease By` - Choisissez quand vous souhaitez que la valeur soit réduite avant d&#39;être ajoutée à Amazon.

   - `Increase By` - Choisissez quand vous souhaitez augmenter la valeur avant d&#39;inscrire sur Amazon.

1. Pour **[!UICONTROL Apply]**, choisissez une option pour déterminer la manière dont vous souhaitez définir *[!UICONTROL Magento Price Source]* défini dans votre [Prix d&#39;annonce](./listing-price.md) valeur à ajuster :

   - `Apply as percentage` - Choisissez quand vous souhaitez définir *[!UICONTROL Magento Price Source]* défini dans votre [Prix d&#39;annonce](./listing-price.md) valeur ajustée d&#39;un pourcentage

   - `Apply as fixed amount` - Choisissez quand vous souhaitez définir *[!UICONTROL Magento Price Source]* défini dans votre [Prix d&#39;annonce](./listing-price.md) valeur ajustée d&#39;un montant fixe.

1. Pour **[!UICONTROL Adjustment Amount]** (obligatoire), entrez la valeur numérique de l’ajustement de prix.

   - Lorsque *[!UICONTROL Apply]* est défini sur `Apply as percentage`, entrez la valeur de pourcentage (exemple : entrer `25` pour un ajustement de prix de 25 %).

   - Lorsque *[!UICONTROL Apply]* est défini sur `Apply as fixed amount`, entrez la valeur numérique du montant fixe (exemple : entrer `25` pour un ajustement de prix fixe de 25 $).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save pricing rule]**.

![Règle de prix standard](assets/ob-price-rule-action-standard-example.png)

| Champ | Description |
|---|---|
| [!UICONTROL Rule Type] | Sélectionner `Standard price rule`. |
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Choisissez quand vous souhaitez définir [!DNL Commerce] valeur de la source de prix à diminuer avant d&#39;être cotée en Amazon.</li><li>**[!UICONTROL Increase By]** - Choisissez quand vous souhaitez définir [!DNL Commerce] valeur de la source de prix à augmenter avant l&#39;inscription à Amazon.</li></ul> |
| [!UICONTROL Apply] | Options :<ul><li>**[!UICONTROL Apply as percentage]** - Choisissez quand vous souhaitez définir [!DNL Commerce] valeur de la source du prix ajustée d&#39;un pourcentage.</li><li>**[!UICONTROL Apply as fixed amount]** - Choisissez quand vous souhaitez définir [!DNL Commerce] valeur de la source du prix ajustée d&#39;un montant fixe.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoire.<br><br>Si vous choisissez `Apply as percentage` pour *[!UICONTROL Apply]*, entrez la valeur de pourcentage (exemple : entrer `25` pour un réglage de 25 %).<br><br>Si vous avez choisi `Apply as fixed amount` pour *[!UICONTROL Apply]*, entrez la valeur numérique du montant fixe (exemple : entrer `25` pour un ajustement fixe de 25 $). |
