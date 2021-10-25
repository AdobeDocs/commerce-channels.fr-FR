---
title: Paramètres généraux des règles de tarification
description: Utilisez les paramètres généraux de la règle de prix pour définir les caractéristiques principales d'une règle de prix d'annonce.
redirect_from: /sales-channels/asc/ob-pricing-rules-general-settings.html
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Paramètres généraux de la règle de tarification

Définissez le nom, la description, les dates actives et la priorité de la règle.

## Compléter la section Paramètres généraux de règle de prix

1. Pour **[!UICONTROL Rule Name]** (obligatoire), entrez le nom de la règle.

   Ce nom n&#39;est utilisé qu&#39;à des fins d&#39;identification interne. Plus le nom de la règle est descriptif, mieux c&#39;est.

1. Pour **[!UICONTROL Description]**, entrez une description détaillée de votre règle.

   Cette description peut inclure des informations sur les produits qui répondent aux critères, les dates d&#39;activation, la formule de calcul de votre prix ajusté ou toute autre information que vous trouverez utile si vous souhaitez modifier la règle.

1. Pour **[!UICONTROL Status]**, choisissez une option :

   - `Active` - Sélectionnez cette option lorsque vous souhaitez que la règle de tarification s’applique à vos produits éligibles et ajustez la tarification de votre annonce avant de publier sur Amazon.

   - `Inactive` - Sélectionnez cette option lorsque vous ne souhaitez pas que la règle de tarification s’applique à vos produits éligibles. Cette option sera probablement utilisée lors de la modification d&#39;une règle de tarification ou de sa désactivation après une promotion limitée.

1. Pour **[!UICONTROL From]** et **[!UICONTROL To]**, entrez une date de début et de fin pour la règle de tarification.

   Vous pouvez également cliquer sur l’icône de calendrier pour sélectionner une date dans le calendrier dynamique. Cette option de début et d’arrêt automatique est utile lors de la configuration de promotions à temps limité ou saisonnières avec des dates de début et de fin définies.

1. Pour **[!UICONTROL Priority]**, entrez une valeur numérique pour la priorité de la règle.

   Valeur de priorité égale à `1` est la plus haute priorité. Lorsque vous avez plusieurs règles de tarification actives, vous pouvez utiliser cette valeur de priorité pour déterminer quelle règle est appliquée en premier. Ce champ est nécessaire pour utiliser la propriété _[!UICONTROL Discard Subsequent Rules]_fonction.

1. Pour **[!UICONTROL Discard Subsequent Rules]**, choisissez une option :

   - `Yes` - Sélectionnez cette option lorsque vous ne souhaitez pas appliquer d’autres règles de tarification applicables à un produit. L’abandon des règles suivantes signifie que, si plusieurs règles de tarification s’appliquent au même produit, seule la règle de tarification ayant la valeur de priorité définie la plus élevée est appliquée au produit. Cette option empêche plusieurs règles de tarification d’empiler et d’offrir des remises supplémentaires imprévues.

   - `No` - Sélectionnez cette option lorsque vous souhaitez autoriser l’application de plusieurs règles de tarification au même produit. Cette option peut entraîner l’empilement et fournir plusieurs remises à appliquer.

>[!NOTE]
>
>Pour annuler les règles suivantes, une règle de tarification doit avoir une définition **Priorité** valeur.

![Paramètres généraux de la règle de tarification](assets/amazon-pricing-rule-general.png)

| Champ | Description |
|---|---|
| [!UICONTROL Rule Name] | (Obligatoire) Saisissez un nom pour la règle, utilisé à des fins d’identification interne. Plus le nom de la règle est descriptif, mieux c&#39;est. Par exemple, &quot;25 % de remise sur la vente de livres à la fin de l’année&quot;. |
| [!UICONTROL Description] | Entrez une description détaillée expliquant la règle (également utilisée à des fins internes). Par exemple, &quot;Vente de fin d’année, 25 % sur tous les articles de la catégorie Livres&quot;. |
| [!UICONTROL Status] | Options :<ul><li>**[!UICONTROL Inactive]** - La règle de tarification ne s&#39;applique pas à vos annonces. Cette option peut être utilisée lors de la modification d’une règle de tarification ou de sa désactivation après une promotion limitée.</li><li>**[!UICONTROL Active]** - La règle de tarification s&#39;applique à vos annonces et réglez votre tarification avant de les publier sur Amazon.</li></ul> |
| [!UICONTROL From] | Entrez la date de début du début de la règle de tarification. Par exemple, pour avoir une vente au cours du dernier mois de l’année, vous devez définir l’option `From` date du 1er décembre, de sorte que la règle de tarification s’applique automatiquement à vos annonces Amazon à partir du 1er décembre. |
| [!UICONTROL To] | Entrez la date de fin à la fin de la règle de tarification. En continuant l’exemple précédent, pour limiter la vente au dernier mois de l’année, vous définissez l’attribut `To` date du 31 décembre, de sorte que la règle de tarification expire le 31 décembre. |
| [!UICONTROL Priority] | Entrez une valeur pour la priorité de la règle de tarification. Une valeur de priorité égale à `1` est la plus haute priorité. Lorsque vous disposez de plusieurs règles de tarification, vous pouvez utiliser la valeur de priorité pour déterminer quelle règle est appliquée en premier. Ce champ est nécessaire pour utiliser la propriété **Ignorer les règles suivantes** fonction. |
| [!UICONTROL Discard Subsequent Rules] | Permet d’autoriser ou d’empêcher plusieurs règles de tarification d’empiler et de fournir des remises supplémentaires. Pour ignorer les règles suivantes, une règle de tarification doit avoir une valeur définie pour **[!UICONTROL Priority]**. Options :<ul><li>**[!UICONTROL Yes]** - Choisissez quand vous ne souhaitez pas appliquer d&#39;autres règles de tarification applicables à un produit. L’abandon des règles suivantes signifie que, lorsque plusieurs règles de tarification s’appliquent au même produit, seule la règle de tarification ayant la valeur de priorité définie la plus élevée est appliquée.</li><li>**[!UICONTROL No]** - Choisissez quand vous souhaitez autoriser l&#39;application de plusieurs règles de tarification au même produit. Cette option peut entraîner l’empilement et plusieurs remises appliquées au prix de votre annonce.</li></ul> |
