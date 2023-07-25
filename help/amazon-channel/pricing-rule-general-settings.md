---
title: Sales Channel Amazon - Paramètres généraux des règles de tarification
description: Utilisez les paramètres généraux de la règle de prix pour définir les Principales caractéristiques d’une règle de prix de vente.
feature: Sales Channels, Price Rules, Configuration
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Paramètres généraux des règles de tarifs

Définissez le nom, la description, les dates principales et la priorité de la règle.

## Renseignez la section Paramètres généraux de la règle de prix .

1. Pour **[!UICONTROL Rule Name]** (obligatoire), saisissez le nom de la règle.

   Ce nom est fourni à des fins d’identification interne uniquement. Plus le nom de la règle est descriptif, mieux c’est.

1. Pour **[!UICONTROL Description]**, saisissez une description détaillée de votre règle.

   Cette description peut inclure des informations sur les produits à qualifier, les dates principales, la formule de calcul de votre prix ajusté, ou toute autre information utile si vous souhaitez modifier la règle.

1. Pour **[!UICONTROL Status]**, choisissez une option :

   - `Active` - Sélectionnez cette option lorsque vous souhaitez que la règle de tarification s’applique à vos produits éligibles et ajustez les tarifs de votre liste avant de les publier sur Amazon.

   - `Inactive` - Sélectionnez cette option lorsque vous ne souhaitez pas que la règle de tarification s’applique à vos produits éligibles. Cette option sera probablement utilisée lors de la modification d’une règle de tarification ou de sa désactivation après une promotion limitée.

1. Pour **[!UICONTROL From]** et **[!UICONTROL To]**, saisissez les dates de début et de fin de la règle de tarification.

   Vous pouvez également cliquer sur l&#39;icône Calendrier pour sélectionner une date dans le calendrier dynamique. Cette option de début et d’arrêt automatique est bénéfique lors de la configuration de promotions à temps limité ou saisonnières avec des dates de début et de fin définies.

1. Pour **[!UICONTROL Priority]**, saisissez une valeur numérique pour la priorité de la règle.

   Valeur de priorité égale à `1` est la priorité la plus élevée. Lorsque vous disposez de plusieurs règles de tarification principales, vous pouvez utiliser cette valeur de priorité pour déterminer la règle qui est appliquée en premier. Ce champ est nécessaire pour utiliser la variable _[!UICONTROL Discard Subsequent Rules]_fonction .

1. Pour **[!UICONTROL Discard Subsequent Rules]**, choisissez une option :

   - `Yes` - Sélectionnez cette option lorsque vous ne souhaitez pas que d’autres règles de tarification puissent s’appliquer à un produit. Ignorer les règles suivantes signifie que, si plusieurs règles de tarification s’appliquent au même produit, seule la règle de tarification avec la valeur de priorité définie la plus élevée est appliquée au produit. Cette option empêche plusieurs règles de tarification de s’empiler et de fournir des remises supplémentaires non prévues.

   - `No` - Sélectionnez cette option lorsque vous souhaitez autoriser l’application de plusieurs règles de tarification au même produit. Cette option peut entraîner l’empilement et fournir plusieurs remises à appliquer.

>[!NOTE]
>
>Pour ignorer les règles suivantes, une règle de tarification doit avoir une définition **Priorité** .

![Paramètres généraux des règles de tarifs](assets/amazon-pricing-rule-general.png){width="600" zoomable="yes"}

| Champ | Description |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Name] | (Obligatoire) Saisissez un nom pour la règle, utilisé à des fins d’identification interne. Plus le nom de la règle est descriptif, mieux c’est. Par exemple, &quot;25 % de remise sur la vente de livres en fin d’année&quot;. |
| [!UICONTROL Description] | Saisissez une description détaillée qui explique la règle (également utilisée à des fins internes). Par exemple, &quot;soldes de fin d’année, 25 % de tous les articles de la catégorie Livres&quot;. |
| [!UICONTROL Status] | Options :<ul><li>**[!UICONTROL Inactive]** - La règle de tarification ne s’applique pas à vos listes. Cette option peut être utilisée lors de la modification d’une règle de tarification ou de sa désactivation après une promotion limitée.</li><li>**[!UICONTROL Active]** - La règle de tarification s’applique à vos listes et ajustez le prix de vos listes avant de les publier dans Amazon.</li></ul> |
| [!UICONTROL From] | Saisissez la date de début de la règle de tarification. Par exemple, pour qu’une vente ait lieu au cours du dernier mois de l’année, vous devez définir la variable `From` date du 1er décembre afin que la règle de tarification s’applique automatiquement à vos listes Amazon à partir du 1er décembre. |
| [!UICONTROL To] | Entrez la date de fin à laquelle la règle de tarification se termine. Dans l’exemple précédent, pour limiter la vente au dernier mois de l’année, vous devez définir la variable `To` date du 31 décembre, de sorte que la règle de tarification expire le 31 décembre. |
| [!UICONTROL Priority] | Saisissez une valeur pour la priorité de la règle de tarification. Une valeur de priorité égale à `1` est la priorité la plus élevée. Lorsque vous disposez de plusieurs règles de tarification, vous pouvez utiliser la valeur de priorité pour déterminer la règle qui est appliquée en premier. Ce champ est nécessaire pour utiliser la variable **Ignorer les règles suivantes** fonction . |
| [!UICONTROL Discard Subsequent Rules] | Permet d’autoriser ou d’empêcher l’empilement de plusieurs règles de tarification et de fournir des remises supplémentaires. Pour ignorer les règles suivantes, une règle de tarification doit avoir une valeur définie pour **[!UICONTROL Priority]**. Options :<ul><li>**[!UICONTROL Yes]** - Sélectionnez cette option lorsque vous ne souhaitez pas que d’autres règles de tarification puissent s’appliquer à un produit. Ignorer les règles suivantes signifie que, lorsque plusieurs règles de tarification s’appliquent au même produit, seule la règle de tarification avec la valeur de priorité définie la plus élevée est appliquée.</li><li>**[!UICONTROL No]** - Choisissez quand vous souhaitez autoriser l’application de plusieurs règles de tarification au même produit. Cette option peut entraîner l’empilement et plusieurs remises s’appliquer au prix de votre offre.</li></ul> |
