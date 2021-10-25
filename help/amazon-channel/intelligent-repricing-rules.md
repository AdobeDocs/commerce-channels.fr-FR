---
title: '''Règle de tarification intelligente : Sélectionner le type de règle"'
description: Déterminez le prix de votre annonce Amazon en fonction des prix pratiqués par les concurrents en créant une règle de tarification intelligente.
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# Règle de revalorisation intelligente : sélectionner le type de règle

>[!IMPORTANT]
>
>Les règles de tarification intelligentes ne fonctionnent pas correctement si la région Amazon est définie sur `Inactive` , comme c’est le cas lors de l’intégration. Vos tarifs dépendent de vos tarifs d’expédition et votre région doit se trouver dans `Active` statut de vos tarifs d&#39;expédition à synchroniser à partir d&#39;Amazon.<br><br>
>
>Pour mettre à jour l’état de votre région dans votre compte Amazon, accédez à Paramètres > Informations de compte > Paramètres de vacances. Reportez-vous à [Amazon : Statut de la liste pour les vacances](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

Une règle de tarification intelligente utilise la tarification des concurrents Amazon pour déterminer le prix de votre annonce. Les concurrents sont d&#39;autres vendeurs qui listent les mêmes produits que les vôtres sur Amazon.

Les sections d&#39;une règle de réévaluation intelligente comprennent :

- Sélectionner le type de règle
- [Écarts conditionnels des concurrents](./competitor-conditional-variances.md)
- [Ajustement du prix](./price-adjustment.md)
- [Prix plancher](./floor-price.md)
- [Prix plafond facultatif](./optional-ceiling-price.md)

## Configuration du type de règle

Définissez le type de règle dans la propriété _[!UICONTROL Select Rule Type]_.

1. Pour **[!UICONTROL Rule Type]**, sélectionnez `Intelligent repricing rule`.

   Ce paramètre active la _[!UICONTROL Competitor Price Source]_et [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)et [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) sections.

1. Pour **[!UICONTROL Competitor Price Source]**, choisissez une option :

   - **[!UICONTROL Use "Buy Box" Price]** - Choisissez quand vous souhaitez ajuster vos tarifs Amazon en fonction de l&#39;Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix vendeur. A [!DNL Buy Box] existe lorsque plusieurs vendeurs sur Amazon proposent le même produit. Amazon définit la [!DNL Buy Box] vendeur en fonction des exigences de performances. Les commerçants cherchent à gagner [!DNL Buy Box] statut de vendeur et offre une visibilité maximale de leurs annonces de produits.

   - **[!UICONTROL Use Lowest Competitor Price]** - Choisissez quand vous souhaitez comparer et ajuster le prix de votre annonce à celui d&#39;un concurrent pour le même produit. Lorsque cette option est sélectionnée, la _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.

1. Si cette option est activée, sélectionnez une option pour **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Choisissez quand vous souhaitez comparer et ajuster votre prix en fonction de tous les prix de concurrent pour le même produit.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Choisissez quand vous souhaitez limiter les concurrents auxquels le prix est comparé pour le même produit. Ce paramètre limite davantage les concurrents en exigeant que leur annonce présente un minimum du pourcentage de commentaires positifs choisi avant d&#39;appliquer la règle du prix le plus bas.

1. Si cette option est activée, entrez une valeur numérique pour **[!UICONTROL Minimum Feedback Count]**.

   Cette valeur numérique facultative réduit davantage les prix concurrentiels. Par exemple, si un commerçant a une cote de rétroaction positive de 95 %, mais a seulement un compte de rétroaction de `20`, il se peut que vous ne souhaitiez pas modifier votre prix par rapport à un concurrent. Toutefois, si vous entrez une valeur de `1000`, il faudrait que le commerçant ait 95 p. 100 de commentaires positifs et qu&#39;il ait un minimum de 1 000 commentaires commerciaux.

>[!NOTE]
>
>Vous pouvez utiliser ces options de tarification et de rétroaction des concurrents pour éviter de baser votre tarification sur un concurrent qui a de faibles retours et vend un produit de qualité inférieure.

![Règle de revalorisation intelligente - sélectionnez le type de règle](assets/ob-intelligent-price-rule-type.png)

| Champ | Description |
|--- |--- |
| [!UICONTROL Rule Type] | Sélectionnez un type de règle. Options :<ul><li>**[!UICONTROL Standard price rule]** - Ce type de règle vous permet d&#39;augmenter ou de diminuer le prix d&#39;inscription Amazon d&#39;un pourcentage spécifique ou d&#39;un montant fixe en dollars par rapport au _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Ce type de règle vous permet d&#39;ajuster le prix de votre annonce Amazon, en fonction de la tarification du concurrent. Lorsque cette option est sélectionnée, la _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.</li></ul> |
| [!UICONTROL Competitor Price Source] | Sélectionnez la source de prix souhaitée. Options :<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Sélectionnez cette option lorsque vous souhaitez ajuster vos tarifs Amazon en fonction de l’Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix vendeur. A [!DNL Buy Box] existe lorsque plusieurs vendeurs sur Amazon proposent le même produit. Amazon définit la [!DNL Buy Box] vendeur en fonction des exigences de performances. Les commerçants cherchent à gagner [!DNL Buy Box] statut de vendeur et offre une visibilité maximale de leurs annonces de produits.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Sélectionnez cette option lorsque vous souhaitez comparer et ajuster le prix de votre annonce au [prix compétitif le plus bas](./lowest-competitor-pricing.md) pour le même produit. Lorsque cette option est sélectionnée, la _[!UICONTROL Minimum Positive Feedback]_et_[!UICONTROL Minimum Feedback Count]_ sont activés.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Uniquement actif si `Use Lowest Competitor Price` est sélectionné. Options :<ul><li>**[!UICONTROL All Competitor's Prices]** - Choisissez quand vous souhaitez comparer et ajuster votre prix en fonction de tous les prix de concurrent pour le même produit.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Choisissez quand vous souhaitez limiter les concurrents auxquels vous comparez et ajustez votre prix. Ce paramètre réduit davantage vos concurrents en exigeant que leur annonce présente un minimum du pourcentage de rétroaction positive choisi, puis utilise le prix le plus bas de ce sous-ensemble de concurrents.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Uniquement actif si `Use Lowest Competitor Price` est sélectionné. Cette valeur numérique facultative réduit davantage la comparaison des prix concurrentiels. Par exemple, si un commerçant a une cote de rétroaction positive de 95 % mais a seulement un compte de rétroaction de `20`, il se peut que vous ne souhaitiez pas modifier votre prix par rapport à un concurrent. Toutefois, si vous entrez une valeur de `1000`, il faudrait que le commerçant ait 95 p. 100 de commentaires positifs et qu&#39;il ait un minimum de 1 000 commentaires commerciaux. |
