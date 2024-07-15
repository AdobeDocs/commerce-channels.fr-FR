---
title: Canal vente Amazon - Exemples de règles de prix
description: Pour vous aider à concevoir vos règles de tarification pour les listes Amazon, passez en revue ces exemples en fonction de scénarios courants.
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# Exemples de règles de prix

## Exemples de règles de prix standard

### Ignorer les règles suivantes

La possibilité d’ignorer les règles suivantes est une fonctionnalité formidable au sein des règles de tarification, qui empêche plusieurs règles de tarification de s’empiler et qui fournit des remises supplémentaires inattendues. Pour ignorer les règles suivantes, une règle de tarification doit utiliser les priorités définies dans la section _[!UICONTROL Priority]_des [Paramètres généraux de la règle de tarification](./pricing-rule-general-settings.md).

Si **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`, les règles ayant une priorité plus faible (nombre plus élevé) ne s’appliquent pas aux produits éligibles.

Par exemple, supposons qu’il existe trois règles de prix :

| Exemple | Nom de la règle | Priorité | Ignorer la règle suivante |
|---------|-----------------------|----------|-------------------------|
| 1 | 10 % de réduction sur les produits de vente | 1 | Non |
| 2 | 2 $ de produits de vente | 2 | Oui |
| 3 | 5 % de réduction sur tous les produits | 3 | Non |

Dans ce scénario, les règles #1 et #2 s’appliquent aux produits éligibles. La règle #3 s’applique uniquement aux produits éligibles non contenus dans la #2 de règles, car elle a une priorité inférieure à l’exemple #2 et **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`. Ainsi, les produits éligibles dans la catégorie de vente recevront une remise de 10 % et 2 $ sur le prix de vente d’Amazon.

### Appliquer deux règles de prix standard

| Champ | Paramètre - Règle 1 | Paramètre - Règle 2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | Règle 1 | Règle 2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Règle de prix standard | Règle de prix standard |
| [!UICONTROL Price action] | Réduire de | Réduire de |
| [!UICONTROL Apply] | Appliquer en pourcentage | Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### Produit 1

Prix : 45,49 $

Règle 1 appliquée : 45,49 $ x (0,9) = 40,94 $

Règle 2 appliquée : 40,94 $ - 10,00 $ = 30,94 $

Le prix final après la règle 1 et la règle 2 est appliqué : 30,94 $

#### Product 2

Prix : 47,76 $

Règle 1 appliquée : 47,76 $ x (0,9) = 42,98 $

Règle 2 appliquée : 42,98 $ - 10,00 $ = 32,98 $

Le prix final après la règle 1 et la règle 2 est appliqué : 32,98 $

## Exemples de règles de réévaluation intelligentes

### Prix Buy Box avec Prix du plancher Source = Prix

| Champ | Paramètre |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Correspondance avec le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

#### Produit 1

Prix : 15 $

Prix [Buy Box](./buy-box-competitor-pricing.md) d’Amazon : 10 $

Comme le prix de [Buy Box](./buy-box-competitor-pricing.md) est inférieur au prix d’origine, le produit est répertorié au prix d’origine.

Prix final après application de la règle : 15 $

#### Product 2

Prix : 5 $

Prix [Buy Box](./buy-box-competitor-pricing.md) d’Amazon : 10 $

Comme le prix de [Buy Box](./buy-box-competitor-pricing.md) est supérieur au prix d’origine, le produit est répertorié au prix de [Buy Box](./buy-box-competitor-pricing.md).

Prix final après application de la règle : 10 $

### Prix Buy Box avec Prix du plancher Source = Prix et une baisse de prix de 20 %

| Champ | Paramètre |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Correspondance avec le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Réduire de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Produit 1

Prix : 20 $

Prix de base calculé : 16 $

Prix [Buy Box](./buy-box-competitor-pricing.md) d’Amazon : 15 $

Comme le prix de [Buy Box](./buy-box-competitor-pricing.md) est inférieur au [Prix du sol](./floor-price.md) calculé, le produit est répertorié dans le [Prix du sol](./floor-price.md) calculé.

Prix final après application de la règle : 16 $

#### Product 2

Prix : 15 $

Calculé [Floor Price](./floor-price.md) : $12

Prix [Buy Box](./buy-box-competitor-pricing.md) d’Amazon : 15 $

Comme le prix de [Buy Box](./buy-box-competitor-pricing.md) est supérieur au [Prix du sol](./floor-price.md) calculé, le produit est répertorié au prix de [Buy Box](./buy-box-competitor-pricing.md).

Prix final après application de la règle : 15 $

#### Product 3

Prix : 17 $

Prix de base calculé : 13,60 $

Prix [Buy Box](./buy-box-competitor-pricing.md) d’Amazon : 15 $

Comme le prix de [Buy Box](./buy-box-competitor-pricing.md) est supérieur au [Prix du sol](./floor-price.md) calculé, le produit est répertorié au prix de [Buy Box](./buy-box-competitor-pricing.md).

Prix final après application de la règle : 15 $

### Prix le plus bas avec tous les prix du concurrent et utiliser toutes les conditions de produit du concurrent

| Champ | Paramètre |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix de concurrent le plus bas |
| [!UICONTROL Minimum Positive Feedback] | Tous les prix des concurrents |
| [!UICONTROL Conditional Variance] | Utiliser toutes les conditions de produit du concurrent |
| [!UICONTROL Price Action] | Correspondance avec le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

| Prix | Condition |
|-------|-----------------|
| 17 $ | Nouveau |
| 15 $ | Nouveau |
| 14 $ | Utilisé ; Très bon |
| 13 $ | Utilisé ; Bon |

#### Produit 1

Prix : 10 $

Condition : Nouveau

Comme le prix concurrent le plus bas pour la nouvelle condition est de 15 $, le produit est répertorié à 15 $.

Prix final après application de la règle : 15 $

#### Product 2

Prix : 10 $

Condition : utilisé ; acceptable

Comme le [prix concurrent le plus bas](./lowest-competitor-pricing.md) pour la condition Utilisé est de 13 $, le produit est répertorié à 13 $.

Prix final après application de la règle : 13 $

### Règle de retarification intelligente combinant le prix plafond, la conversion de devise et la TVA

| Champ | Paramètre |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10 % |
| [!UICONTROL Ceiling price source] | 10 $ |
| [!UICONTROL Currency conversion] | 1,25 Euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 = 12,50 $

Lorsque le [prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) est atteint, la TVA est calculée et ajoutée.

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

### Combiner plusieurs règles de tarification, prix plafond, conversion de devise et TVA

#### Règle de tarification intelligente (à partir de l’exemple précédent)

| Champ | Paramètre |
|----------------------|---------------|
| Priorité | 1 |
| TVA | 10 % |
| Source des prix du plafond | 10 $ |
| Conversion des devises | 1,25 Euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 = 12,50 $

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

#### Règle de prix standard

| Champ | Paramètre |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | 5 $ |

Lorsque le [prix plafond](./optional-ceiling-price.md) est atteint, la règle de tarification standard est appliquée en plus de la règle de tarification intelligente.

Prix final après application de la règle de tarification standard : 13,75 $ + 5,00 $ = 18,75 $

### Ajustement des prix

Dans cet exemple, le prix le plus compétitif est défini en examinant le [prix le plus bas du concurrent](./lowest-competitor-pricing.md) Amazon avec un retour positif de 95 % et un nombre minimum de commentaires de 1 000 commentaires du marché.

![Exemple d’ajustement de prix](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

Après avoir effectué cette recherche en fonction de ces paramètres, le prix concurrentiel revient à 25 $.

À partir de là, il existe trois options différentes [action de règle de prix](./pricing-rule-actions.md) basées sur ce prix le plus bas.

| Champ | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Cette option réduit le prix de votre offre par rapport au [prix du concurrent le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** - Cette option augmente le prix de votre offre par rapport au [prix du concurrent le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** - Cette option modifie le prix de votre offre Amazon pour qu’il corresponde au prix le plus bas en fonction des paramètres. Dans cet exemple, le prix de la mise en vente d’Amazon est de 25 $.</li></ul> |
| [!UICONTROL Apply] | Options : Appliquer en pourcentage / Appliquer en montant fixe |
| [!UICONTROL Adjustment Amount] | Valeur numérique pour définir le pourcentage ou le montant fixe de la remise à appliquer. <br>Ces sélections entraînent la prise du prix le plus bas et sa définition à 0,01 $ de moins. |

### Prix plancher

| Champ | Paramètre |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | Coût = 5 $ |
| [!UICONTROL Floor Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Prix du plancher](./floor-price.md) calcul = Prix du plancher Source `$5` x Montant d’ajustement du plancher `5%` = 5,25 $

Lorsque la règle de tarification intelligente est appliquée, elle permet que le prix de la mise en vente soit inférieur à 5,25 $ pour ce produit spécifique lorsque le coût est de 5 $.
