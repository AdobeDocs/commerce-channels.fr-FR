---
title: Gestion des tarifs Amazon
description: Vous pouvez définir le prix de vos listes Amazon en fonction des règles de prix de votre boutique en ligne.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Gestion des tarifs Amazon

Le canal de vente d’Amazon vous permet de définir des règles de prix, ce qui vous permet de définir le prix de votre offre Amazon différent du prix défini. **[!UICONTROL Magento Price Source]** dans votre [tarif lisliste](./listing-price.md). Vous pouvez également empiler plusieurs règles et même utiliser la tarification intelligente pour ajuster le prix de votre offre Amazon en fonction de celui des concurrents. [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix ou [prix compétitif le plus bas](./lowest-competitor-pricing.md).

Il existe deux types de règles de tarification :

- [Règle de tarification standard](./standard-price-rules.md)
- [Règle de retarification intelligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Les règles de tarification intelligente ne fonctionnent pas correctement si la région Amazon est définie sur `Inactive` , comme c’est le cas lors de l’intégration. Vos calculs de prix dépendent de vos tarifs d’expédition. Votre région doit se trouver dans `Active` statut de synchronisation de vos tarifs d’expédition depuis Amazon.
   >
   >Pour mettre à jour l’état de votre région dans votre compte Amazon, accédez à Paramètres > Informations du compte > Paramètres de déplacement. Voir [Amazon : État de la liste des vacances](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) (Connexion à Seller Central requise).

Cette fonctionnalité vous permet de manipuler les prix Amazon d’une manière similaire au [!DNL Commerce] [règles de prix du catalogue](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). Vous pouvez créer des règles complexes qui vous permettent de modifier les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou même avec des attributs spécifiques.

Vous pouvez ajouter des règles de tarification pour vos listes Amazon. Les règles de prix peuvent être utilisées pour ajuster automatiquement les prix de votre offre, en fonction d’un ensemble de conditions définies. Les règles de prix sont déclenchées et calculent le prix ajusté avant que votre produit ne soit répertorié dans Amazon.

>[!NOTE]
>
>La source de prix de vos listes Amazon est définie pour **[!UICONTROL Magento Price Source]** dans votre [tarif lisliste](./listing-price.md) paramètres. Tout calcul d’ajustement défini dans la règle de prix utilise la source de prix comme valeur de départ.

Les règles de tarification vous permettent de définir le prix de votre offre Amazon en liste différent de votre **[!UICONTROL Magento Price Source]** dans votre [tarif lisliste](./listing-price.md) paramètres. Vous pouvez également empiler plusieurs règles qui fonctionnent ensemble pour ajuster votre prix.

Une règle de tarification/retarification nécessite trois ensembles d’informations lors de sa configuration :

- [Paramètres généraux](./pricing-rule-general-settings.md): Définit le nom, la description, les dates principales, la priorité d’une règle et définit le comportement des règles suivantes, en fonction de son paramètre de priorité.
- [Conditions](./pricing-rule-conditions.md): Déterminez les produits éligibles à la règle de prix.
- [Actions](./pricing-rule-actions.md): Définissez les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la mise en vente.

Vous pouvez créer des [règles de tarification standard](./standard-price-rules.md) qui ajustent automatiquement le prix de votre offre Amazon par rapport au **[!UICONTROL Magento Price Source]** dans votre [tarif lisliste](./listing-price.md) paramètres. Cette fonctionnalité vous permet de manipuler les prix Amazon d’une manière similaire au [!DNL Commerce] [règles de prix du catalogue](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). Vous pouvez créer des règles complexes qui modifient automatiquement les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou de produits avec des attributs spécifiques. Vous pouvez compléter les paramètres traditionnels et retarifer vos produits pour augmenter ou diminuer en fonction d’un montant fixe ou d’un pourcentage.

Un autre outil puissant est le suivant : [Optimisation intelligente des prix](./intelligent-repricing-rules.md) qui ajuste le prix de votre offre Amazon en fonction de votre concurrent [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix ou [Prix de concurrent le plus bas](./lowest-competitor-pricing.md). Semblable au [!DNL Commerce] [règles de prix du catalogue](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html), cette fonctionnalité avancée vous permet de manipuler les prix Amazon en créant des règles complexes. Les règles peuvent définir la portée d’un changement de prix pour des produits spécifiques, des produits appartenant à des catégories spécifiques ou même avec des attributs de produit spécifiques.

Utiliser des prix intelligents pour ajuster les prix de vos listes Amazon en fonction des prix de vos concurrents. Le canal de vente Amazon dispose de protections intégrées que vous pouvez configurer afin de protéger les marges ou d’éviter de faire correspondre les prix d’un commerçant avec un retour faible. Utilisation [règles de retarification intelligente](./intelligent-repricing-rules.md), les prix des listes Amazon peuvent être automatiquement manipulés sous la forme d’un montant fixe ou d’un pourcentage (en hausse ou en baisse) ou même synchronisés avec la variable [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix ou [Prix de concurrent le plus bas](./lowest-competitor-pricing.md) par élément. Les règles peuvent même être empilées pour offrir une flexibilité illimitée.

Vous pouvez contrôler des aspects importants des règles, tels que l’état principal/inactif, l’éligibilité au site web, les plages de dates facultatives et les niveaux de priorité facultatifs (utilisés pour l’empilement des règles).

Par exemple, vous pouvez définir et définir les conditions d’une règle de prix qui, lorsque les conditions sont remplies, ajustera automatiquement le prix de votre offre avant de l’envoyer à Amazon.

Une autre option de tarification est une [remplacement du prix](./overrides.md), qui est défini au niveau de la liste individuelle. A [remplacement du prix](./overrides.md) peut être défini et un remplacement ignore/a la priorité sur tous les autres paramètres, paramètres et règles par défaut. Un [override](./overrides.md) peut être défini pour le prix, le temps de traitement, la condition et les notes de vendeur (à quelques exceptions près).

![Règles de tarifs](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Name] | Nom de la règle de tarification, tel que défini dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | Le type de règle, tel que défini dans [Actions des règles de tarification](./pricing-rule-actions.md) (règle de prix standard ou règle de retarification intelligente) |
| [!UICONTROL Is Active] | Si la règle est principale, comme défini dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La priorité par rapport aux autres conditions de tarification, telles que définies dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indique si d’autres règles de prix sont traitées sur les produits éligibles pour cette règle, comme défini dans [paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Début de la période pendant laquelle la règle est principale |
| [!UICONTROL To Date] | Fin de la période pendant laquelle la règle est principale |
| [!UICONTROL Action] | Répertorie toutes les actions qui peuvent être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans le _[!UICONTROL Action]_colonne . Options : `Edit Price Rule` / `Delete Price Rule` |
