---
title: Gestion des tarifs Amazon
description: Vous pouvez définir le prix de vos listes Amazon en fonction des règles de prix de votre boutique en ligne.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Gestion des tarifs Amazon

Le canal de vente Amazon vous permet de définir des règles de prix, ce qui vous permet de définir le prix de votre offre Amazon différent du **[!UICONTROL Magento Price Source]** défini dans votre [prix de vente](./listing-price.md). Vous pouvez également empiler plusieurs règles et même utiliser la tarification intelligente pour ajuster le prix de votre offre Amazon en fonction du [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix des concurrents ou du [prix du concurrent le plus bas](./lowest-competitor-pricing.md).

Il existe deux types de règles de tarification :

- [Règle de tarification standard](./standard-price-rules.md)
- [Règle de retarification intelligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Les règles de tarification intelligente ne fonctionnent pas correctement si la région Amazon est définie sur l’état `Inactive`, comme c’est le cas lors de l’intégration. Vos calculs de prix dépendent de vos tarifs d’expédition. Votre région doit être à l’état `Active` pour que vos taux d’expédition soient synchronisés à partir d’Amazon.
   >
   >Pour mettre à jour l’état de votre région dans votre compte Amazon, accédez à Paramètres > Informations du compte > Paramètres de déplacement. Voir [Amazon : État d’affichage de la liste pour les vacances](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){:target=&quot;_blank&quot;} (connexion à Seller Central requise).

Cette fonctionnalité vous permet de manipuler les prix Amazon d’une manière similaire aux [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/catalog/pricing.html){:target=&quot;_blank&quot;}. Vous pouvez créer des règles complexes qui vous permettent de modifier les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou même avec des attributs spécifiques.

Vous pouvez ajouter des règles de tarification pour vos listes Amazon. Les règles de prix peuvent être utilisées pour ajuster automatiquement les prix de votre offre, en fonction d’un ensemble de conditions définies. Les règles de prix sont déclenchées et calculent le prix ajusté avant que votre produit ne soit répertorié dans Amazon.

>[!NOTE]
>
>La source de prix de vos listes Amazon est définie pour **[!UICONTROL Magento Price Source]** dans vos paramètres [Prix de la liste](./listing-price.md). Tout calcul d’ajustement défini dans la règle de prix utilise la source de prix comme valeur de départ.

Les règles de tarification vous permettent de définir le prix de votre offre Amazon différent de celui de votre **[!UICONTROL Magento Price Source]** dans vos paramètres [prix de la mise en vente](./listing-price.md). Vous pouvez également empiler plusieurs règles qui fonctionnent ensemble pour ajuster votre prix.

Une règle de tarification/retarification nécessite trois ensembles d’informations lors de sa configuration :

- [Paramètres généraux](./pricing-rule-general-settings.md) : Définit le nom, la description, les dates principales, la priorité d’une règle et définit le comportement des règles suivantes, en fonction de son paramètre de priorité.
- [Conditions](./pricing-rule-conditions.md) : Déterminez les produits éligibles à la règle de prix.
- [Actions](./pricing-rule-actions.md) : Définissez les calculs d’ajustement appliqués à la source de prix pour déterminer le prix de la mise en vente.

Vous pouvez créer des [règles de tarification standard](./standard-price-rules.md) qui ajustent automatiquement le prix de votre offre Amazon par rapport au **[!UICONTROL Magento Price Source]** sélectionné dans vos paramètres [Prix du référencement](./listing-price.md). Cette fonctionnalité vous permet de manipuler les prix Amazon d’une manière similaire aux [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}. Vous pouvez créer des règles complexes qui modifient automatiquement les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou de produits avec des attributs spécifiques. Vous pouvez compléter les paramètres traditionnels et retarifer vos produits pour augmenter ou diminuer en fonction d’un montant fixe ou d’un pourcentage.

Un autre outil puissant est la fonction de [réévaluation intelligente](./intelligent-repricing-rules.md) qui ajuste le prix de votre offre Amazon en fonction du prix du concurrent [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou [Prix du concurrent le plus bas](./lowest-competitor-pricing.md). Tout comme les [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}, cette fonctionnalité avancée vous permet de manipuler les prix Amazon en créant des règles complexes. Les règles peuvent définir la portée d’un changement de prix pour des produits spécifiques, des produits appartenant à des catégories spécifiques ou même avec des attributs de produit spécifiques.

Utiliser des prix intelligents pour ajuster les prix de vos listes Amazon en fonction des prix de vos concurrents. Le canal de vente Amazon dispose de protections intégrées que vous pouvez configurer afin de protéger les marges ou d’éviter de faire correspondre les prix d’un commerçant avec un retour faible. En utilisant des [règles intelligentes de réévaluation des prix](./intelligent-repricing-rules.md), les prix d’inscription d’Amazon peuvent être automatiquement manipulés sous la forme d’un montant fixe ou en pourcentage (en hausse ou en baisse) ou même synchronisés avec le prix [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou le [prix le plus bas des concurrents](./lowest-competitor-pricing.md) sur une base par article. Les règles peuvent même être empilées pour offrir une flexibilité illimitée.

Vous pouvez contrôler des aspects importants des règles, tels que l’état principal/inactif, l’éligibilité au site web, les plages de dates facultatives et les niveaux de priorité facultatifs (utilisés pour l’empilement des règles).

Par exemple, vous pouvez définir et définir les conditions d’une règle de prix qui, lorsque les conditions sont remplies, ajustera automatiquement le prix de votre offre avant de l’envoyer à Amazon.

Une autre option de tarification est un [remplacement de prix](./overrides.md), qui est défini au niveau de la liste individuelle. Un [remplacement de prix](./overrides.md) peut être défini, et un remplacement ignore/a la priorité sur tous les autres paramètres, paramètres et règles par défaut. Un [remplacement](./overrides.md) peut être défini pour le prix, le temps de traitement, la condition et les notes du vendeur (à quelques exceptions près).

![Règles de tarifs](assets/amazon-pricing-rules.png)

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Name] | Nom de la règle de tarification, tel que défini dans [Paramètres généraux de la règle de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | Type de règle, tel que défini dans [Actions de règle de tarification](./pricing-rule-actions.md) (règle de prix standard ou règle de retarification intelligente) |
| [!UICONTROL Is Active] | Si la règle est principale, comme défini dans [Paramètres généraux de la règle de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La priorité par rapport aux autres conditions de prix, comme défini dans [Paramètres généraux de la règle de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indique si d’autres règles de prix sont traitées sur les produits éligibles pour cette règle, comme défini dans [paramètres généraux des règles de prix](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Début de la période pendant laquelle la règle est principale |
| [!UICONTROL To Date] | Fin de la période pendant laquelle la règle est principale |
| [!UICONTROL Action] | Répertorie toutes les actions qui peuvent être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la colonne _[!UICONTROL Action]_. Options : `Edit Price Rule` / `Delete Price Rule` |
