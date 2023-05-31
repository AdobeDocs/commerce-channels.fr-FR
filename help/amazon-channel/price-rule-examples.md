---
title: Canal vente Amazon - Exemples de règles de prix
description: Pour vous aider à concevoir vos règles de tarification pour les listes Amazon, passez en revue ces exemples en fonction de scénarios courants.
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 2%

---

# Exemples de règles de prix

## Exemples de règles de prix standard

### Ignorer les règles suivantes

La possibilité d’ignorer les règles suivantes est une fonctionnalité formidable au sein des règles de tarification, qui empêche plusieurs règles de tarification de s’empiler et qui fournit des remises supplémentaires inattendues. Pour ignorer les règles suivantes, une règle de tarification doit utiliser les priorités définies dans la variable _[!UICONTROL Priority]_section [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md).

If **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`, les règles avec une priorité plus faible (nombres plus élevés) ne s’appliquent pas aux produits éligibles.

Par exemple, supposons qu’il existe trois règles de prix :

| Exemple | Nom de la règle | Priorité | Ignorer la règle suivante |
|----------|----|----|----|
| 1 | 10 % de réduction sur les produits de vente | 1 | Non |
| 2 | 2 $ de produits de vente | 2 | Oui |
| 3 | 5 % de réduction sur tous les produits | 3 | Non |

Dans ce scénario, les règles #1 et #2 s’appliquent aux produits éligibles. La règle #3 s’applique uniquement aux produits éligibles non contenus dans #2 de règles, car elle a une priorité inférieure à l’exemple #2 et **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`. Ainsi, les produits éligibles dans la catégorie de vente recevront une remise de 10 % et 2 $ sur le prix de vente d’Amazon.

### Appliquer deux règles de prix standard

| Champ | Paramètre - Règle 1 | Paramètre - Règle 2 |
|----------|----|----|
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

Le prix final après la règle 1 et la règle 2 sont appliqués : 32,98 $

## Exemples de règles de réévaluation intelligentes

### Prix Buy Box avec Prix plancher source = Prix

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Correspondance du prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

#### Produit 1

Prix : 15 $

[Buy Box](./buy-box-competitor-pricing.md) price d’Amazon : 10 $

Parce que la variable [Buy Box](./buy-box-competitor-pricing.md) Le prix est inférieur au prix d&#39;origine, le produit est présenté au prix d&#39;origine.

Le prix final après application de la règle : 15 $

#### Product 2

Prix : $5

[Buy Box](./buy-box-competitor-pricing.md) price d’Amazon : 10 $

Parce que la variable [Buy Box](./buy-box-competitor-pricing.md) Le prix est supérieur au prix d’origine, le produit est répertorié à l’adresse [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 10 $

### Prix Buy Box avec source du prix de base = prix et une baisse de prix de 20 %

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Correspondance du prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Réduire de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Produit 1

Prix : 20 $

Prix de base calculé : 16 $

[Buy Box](./buy-box-competitor-pricing.md) price d’Amazon : 15 $

Parce que la variable [Buy Box](./buy-box-competitor-pricing.md) Le prix est inférieur au calculé [Prix plancher](./floor-price.md), le produit est répertorié dans la section Calculé . [Prix plancher](./floor-price.md).

Le prix final après application de la règle : 16 $

#### Product 2

Prix : 15 $

Calculé [Prix plancher](./floor-price.md): 12 $

[Buy Box](./buy-box-competitor-pricing.md) price d’Amazon : 15 $

Parce que la variable [Buy Box](./buy-box-competitor-pricing.md) Le prix est supérieur au montant calculé [Prix plancher](./floor-price.md), le produit est répertorié à l’adresse [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 15 $

#### Product 3

Prix : 17 $

Prix de base calculé : 13,60 $

[Buy Box](./buy-box-competitor-pricing.md) price d’Amazon : 15 $

Parce que la variable [Buy Box](./buy-box-competitor-pricing.md) Le prix est supérieur au montant calculé [Prix plancher](./floor-price.md), le produit est répertorié à l’adresse [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 15 $

### Prix le plus bas avec tous les prix du concurrent et utiliser toutes les conditions de produit du concurrent

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de retarification intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix de concurrent le plus bas |
| [!UICONTROL Minimum Positive Feedback] | Tous les prix des concurrents |
| [!UICONTROL Conditional Variance] | Utiliser toutes les conditions de produit du concurrent |
| [!UICONTROL Price Action] | Correspondance du prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

| Prix | Condition |
|----------|----|
| $17 | Nouveau |
| $15 | Nouveau |
| $14 | Utilisé ; Très bon |
| $13 | Utilisé ; Bon |

#### Produit 1

Prix : 10 $

Condition : Nouveau

Comme le prix concurrent le plus bas pour la nouvelle condition est de 15 $, le produit est répertorié à 15 $.

Le prix final après application de la règle : 15 $

#### Product 2

Prix : 10 $

Condition : Utilisé ; Acceptable

Parce que la variable [prix compétitif le plus bas](./lowest-competitor-pricing.md) pour la condition Utilisé, la somme de 13 $ est indiquée, le produit est indiqué à 13 $.

Le prix final après application de la règle : 13 $

### Règle de retarification intelligente combinant le prix plafond, la conversion de devise et la TVA

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1,25 Euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 = 12,50 $

Lorsque la variable [prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA), la TVA est calculée et ajoutée.

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

### Combiner plusieurs règles de tarification, prix plafond, conversion de devise et TVA

#### Règle de tarification intelligente (de l’exemple précédent)

| Champ | Paramètre |
|----------|----|
| Priorité | 1 |
| TVA | 10% |
| Source des prix du plafond | $10 |
| Conversion des devises | 1,25 Euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 = 12,50 $

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

#### Règle de prix standard

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | $5.00 |

Lorsque la variable [prix plafond](./optional-ceiling-price.md) est atteint, la règle de tarification standard est appliquée en plus de la règle de tarification intelligente.

Prix final après application de la règle de prix standard : 13,75 $ + 5,00 $ = 18,75 $

### Ajustement des prix

Dans cet exemple, le prix le plus compétitif est défini en regardant Amazon [le prix le plus bas du concurrent](./lowest-competitor-pricing.md) avec 95 % de commentaires positifs et un nombre minimum de commentaires de 1 000 commentaires de marchands.

![Exemple d&#39;ajustement de prix](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

Après avoir effectué cette recherche en fonction de ces paramètres, le prix concurrentiel revient à 25 $.

D&#39;ici, il y a trois [action de règle de prix](./pricing-rule-actions.md) choix basés sur ce prix le plus bas.

| Champ | Description |
|--- |--- |
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Cette option réduit le prix de votre offre par rapport à la valeur [prix compétitif le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** - Cette option augmente le prix de votre offre par rapport à la valeur [prix compétitif le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** - Cette option modifie le prix de votre offre Amazon pour qu’il corresponde au prix le plus bas en fonction des paramètres. Dans cet exemple, le prix de la mise en vente d’Amazon est de 25 $.</li></ul> |
| [!UICONTROL Apply] | Options : Appliquer comme pourcentage/Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | Valeur numérique pour définir le pourcentage ou le montant fixe de la remise à appliquer. <br>Ces sélections se traduisent par le prix le plus bas et par une réduction de 0,01 $. |

### Prix plancher

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Floor Price Source] | Coût = 5 $ |
| [!UICONTROL Floor Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Prix plancher](./floor-price.md) calcul = source du prix plancher `$5` x Montant d’ajustement du plancher `5%` = 5,25 $

Lorsque la règle de tarification intelligente est appliquée, elle permet que le prix de la mise en vente soit inférieur à 5,25 $ pour ce produit spécifique lorsque le coût est de 5 $.
