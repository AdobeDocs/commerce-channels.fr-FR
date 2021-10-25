---
title: Exemples de règles de prix
description: Pour vous aider à concevoir vos règles de tarification pour les annonces Amazon, consultez ces exemples en fonction de scénarios courants.
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# Exemples de règles de prix

## Exemples de règles de prix standard

### Ignorer les règles suivantes

La possibilité de rejeter les règles suivantes est une caractéristique importante des règles de tarification qui empêche plusieurs règles de tarification de cumuler et de fournir des remises supplémentaires involontaires. Pour ignorer les règles suivantes, une règle de tarification doit utiliser les priorités définies dans la propriété _[!UICONTROL Priority]_section [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md).

Si **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`, les règles ayant une priorité moindre (nombre plus élevé) ne s&#39;appliquent pas aux produits éligibles.

Par exemple, supposons qu’il existe trois règles de tarification :

| Exemple | Nom de la règle | Priorité | Ignorer la règle suivante |
|----------|----|----|----|
| 1 | 10 % de réduction sur les produits de vente | 1 | Non |
| 2 | 2 $ de produits hors vente | 2 | Oui |
| 3 | 5 % de tous les produits | 3 | Non |

Dans ce scénario, les règles 1 et 2 s&#39;appliquent aux produits admissibles. La règle #3 ne s&#39;applique qu&#39;aux produits admissibles non visés par la règle #2 parce qu&#39;elle a une priorité inférieure à l&#39;exemple #2 et **[!UICONTROL Discard Subsequent Rules]** est défini sur `Yes`. Ainsi, les produits admissibles de la catégorie de vente bénéficieraient d&#39;une remise de 10 % et de 2 $ sur le prix d&#39;inscription Amazon.

### Application de deux règles de prix standard

| Champ | Définition - Règle 1 | Cadre - Article 2 |
|----------|----|----|
| [!UICONTROL Rule Name] | Règle 1 | Article 2 |
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

#### Produit 2

Prix : 47,76 $

Règle 1 appliquée : 47,76 $ x (0,9) = 42,98 $

Règle 2 appliquée : 42,98 $ - 10,00 $ = 32,98 $

Le prix final après la règle 1 et la règle 2 est appliqué : 32,98 $

## Exemples de règles de tarification intelligente

### Prix Buy Box avec Prix plancher Source = Prix

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de réévaluation intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Ajuster le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

#### Produit 1

Prix : 15 $

[Buy Box](./buy-box-competitor-pricing.md) prix de Amazon : 10 $

Parce que [Buy Box](./buy-box-competitor-pricing.md) est inférieur au prix d&#39;origine, le produit est indiqué au prix d&#39;origine.

Le prix final après application de la règle : 15 $

#### Produit 2

Prix : $5

[Buy Box](./buy-box-competitor-pricing.md) prix de Amazon : 10 $

Parce que [Buy Box](./buy-box-competitor-pricing.md) le prix est supérieur au prix d’origine, le produit est répertorié au [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 10 $

### Prix Buy Box avec Prix plancher Source = Prix et une baisse de prix de 20%

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de réévaluation intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix &quot;Buy Box&quot; |
| [!UICONTROL Price Action] | Ajuster le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Réduire de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Produit 1

Prix : 20 $

Prix plancher calculé : 16 $

[Buy Box](./buy-box-competitor-pricing.md) prix de Amazon : 15 $

Parce que [Buy Box](./buy-box-competitor-pricing.md) le prix est inférieur au montant calculé [Prix plancher](./floor-price.md), le produit est répertorié dans la section Calculé [Prix plancher](./floor-price.md).

Le prix final après application de la règle : 16 $

#### Produit 2

Prix : 15 $

Calculé [Prix plancher](./floor-price.md): 12 $

[Buy Box](./buy-box-competitor-pricing.md) prix de Amazon : 15 $

Parce que [Buy Box](./buy-box-competitor-pricing.md) le prix est supérieur au montant calculé [Prix plancher](./floor-price.md), le produit est répertorié dans la section [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 15 $

#### Produit 3

Prix : 17 $

Prix plancher calculé : 13,60 $

[Buy Box](./buy-box-competitor-pricing.md) prix de Amazon : 15 $

Parce que [Buy Box](./buy-box-competitor-pricing.md) le prix est supérieur au montant calculé [Prix plancher](./floor-price.md), le produit est répertorié dans la section [Buy Box](./buy-box-competitor-pricing.md) prix.

Le prix final après application de la règle : 15 $

### Prix le plus bas avec tous les prix du concurrent et utiliser toutes les conditions de produit du concurrent

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL Rule Name] | Règle 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Règle de réévaluation intelligente |
| [!UICONTROL Competitor Price Source] | Utiliser le prix concurrent le plus bas |
| [!UICONTROL Minimum Positive Feedback] | Tous les prix compétitifs |
| [!UICONTROL Conditional Variance] | Utiliser toutes les conditions de produit du concurrent |
| [!UICONTROL Price Action] | Ajuster le prix du concurrent |
| [!UICONTROL Floor Price Source] | Prix |
| [!UICONTROL Floor Price Action] | Correspondance |

| Prix | Condition |
|----------|----|
| 17 $ | Nouveau |
| 15 $ | Nouveau |
| 14 $ | Utilisé ; Très bon |
| 13 $ | Utilisé ; Bon |

#### Produit 1

Prix : 10 $

Condition : Nouveau

Comme le prix concurrent le plus bas pour la nouvelle condition est de 15 $, le produit est indiqué à 15 $.

Le prix final après application de la règle : 15 $

#### Produit 2

Prix : 10 $

Condition : Utilisé ; Acceptable

Parce que [prix compétitif le plus bas](./lowest-competitor-pricing.md) pour la condition Utilisé est de 13 $, le produit est indiqué à 13 $.

Le prix final après application de la règle : 13 $

### Règle de réévaluation intelligente combinant prix plafond, conversion de devise et TVA

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | 10 $ |
| [!UICONTROL Currency conversion] | 1,25 euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 $ = 12,50 $

Lorsque [prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) est touché, la TVA est calculée et ajoutée.

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

### Combinaison de plusieurs règles de tarification, prix plafond, conversion de devise et TVA

#### Règle de tarification intelligente (exemple précédent)

| Champ | Paramètre |
|----------|----|
| Priorité | 1 |
| TVA | 10% |
| Source de prix plafond | 10 $ |
| Conversion des devises | 1,25 euro : 1 USD |

[Prix plafond](./optional-ceiling-price.md) sur le marché européen (TVA) : 10 $ x 1,25 $ = 12,50 $

Prix final après TVA : 12,50 $ x (1,1) = 13,75 $

#### Règle de tarification standard

| Champ | Paramètre |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | 5,00 $ |

Lorsque [prix plafond](./optional-ceiling-price.md) est activée, la règle de tarification standard est appliquée en plus de la règle de tarification intelligente.

Prix final après application de la règle de tarification standard : 13,75 $ + 5,00 $ = 18,75 $

### Ajustement de prix

Dans cet exemple, le prix le plus compétitif est défini en regardant l’Amazon [prix le plus bas du concurrent](./lowest-competitor-pricing.md) avec une rétroaction positive de 95 % et un nombre minimal de commentaires de 1 000 revues commerciales.

![Exemple d’ajustement de prix](assets/amazon-price-adjustment-example.png)

Après avoir effectué cette recherche basée sur ces paramètres, le prix concurrentiel revient à 25 $.

D&#39;ici, il y a trois différences [action de règle de prix](./pricing-rule-actions.md) choix basés sur ce prix le plus bas.

| Champ | Description |
|--- |--- |
| [!UICONTROL Price Action] | Options :<ul><li>**[!UICONTROL Decrease By]** - Cette option réduit le prix de votre annonce par rapport au [prix compétitif le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** - Cette option augmente le prix de votre annonce par rapport au [prix compétitif le plus bas](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** - Cette option modifie le prix de votre annonce Amazon pour qu’il corresponde au prix le plus bas en fonction des paramètres. Dans l&#39;exemple, le prix d&#39;inscription de l&#39;Amazon est de 25 $.</li></ul> |
| [!UICONTROL Apply] | Options : Appliquer comme pourcentage / Appliquer comme montant fixe |
| [!UICONTROL Adjustment Amount] | Valeur numérique pour définir le pourcentage ou le montant fixe de la remise à appliquer. <br>Ces sélections se traduisent par la prise du prix le plus bas et la fixation à 0,01 $ de moins. |

### Prix plancher

| Champ | Paramètre |
|----------|----|
| [!UICONTROL Floor Price Source] | Coût = 5 $ |
| [!UICONTROL Floor Price Action] | Augmenter de |
| [!UICONTROL Apply] | Appliquer en pourcentage |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Prix plancher](./floor-price.md) calcul = Source du prix plancher `$5` x Montant de réglage du plancher `5%` = 5,25 $

Lorsque la règle de tarification intelligente est appliquée, elle permet que le prix d&#39;annonce soit inférieur à 5,25 $ pour ce produit spécifique lorsque le coût est de 5 $.
