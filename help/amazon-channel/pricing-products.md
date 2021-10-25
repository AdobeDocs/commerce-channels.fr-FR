---
title: Gestion des tarifs Amazon
description: Vous pouvez définir la tarification de vos annonces Amazon pour qu’elle diffère de celle de votre boutique en ligne en utilisant les règles de tarification.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Gestion des tarifs Amazon

Le canal de vente Amazon vous permet de définir des règles de tarification, ce qui vous permet de définir votre prix de vente Amazon différent du prix défini **[!UICONTROL Magento Price Source]** dans votre [prix de vente](./listing-price.md). Vous pouvez également empiler plusieurs règles et même utiliser la tarification intelligente pour ajuster le prix de votre annonce Amazon en fonction de la concurrence. [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ou [prix compétitif le plus bas](./lowest-competitor-pricing.md).

Il existe deux types de règles de tarification :

- [Règle de tarification standard](./standard-price-rules.md)
- [Règle de tarification intelligente](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Les règles de tarification intelligentes ne fonctionnent pas correctement si la région Amazon est définie sur `Inactive` , comme c’est le cas lors de l’intégration. Vos tarifs dépendent de vos tarifs d’expédition et votre région doit se trouver dans `Active` statut de vos tarifs d&#39;expédition à synchroniser à partir d&#39;Amazon.
   >
   >Pour mettre à jour l’état de votre région dans votre compte Amazon, accédez à Paramètres > Informations de compte > Paramètres de vacances. Reportez-vous à [Amazon : Statut de la liste pour les vacances](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target=&quot;_blank&quot;} (Connexion au centre du vendeur requise).

Cette fonctionnalité vous permet de manipuler vos prix Amazon d’une manière similaire à la [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}. Vous pouvez créer des règles complexes qui vous permettent de modifier les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou même avec des attributs spécifiques.

Vous pouvez ajouter des règles de tarification pour vos annonces Amazon. Les règles de prix peuvent être utilisées pour ajuster automatiquement les prix de votre annonce, en fonction d&#39;un ensemble de conditions définies. Les règles de prix sont déclenchées et calculent votre prix ajusté avant que votre produit ne soit répertorié sur Amazon.

>[!NOTE]
>
>La source de prix de vos annonces Amazon est définie pour **[!UICONTROL Magento Price Source]** dans votre [prix de vente](./listing-price.md) paramètres. Tout calcul d&#39;ajustement défini dans la règle de tarification utilise la source de prix comme valeur de départ.

Les règles de tarification vous permettent de définir le prix de votre annonce Amazon différent de celui de votre **[!UICONTROL Magento Price Source]** dans votre [prix de vente](./listing-price.md) paramètres. Vous pouvez également empiler plusieurs règles qui fonctionnent ensemble pour ajuster votre prix.

Une règle de tarification/retarification nécessite trois ensembles d&#39;informations lors de sa configuration :

- [Paramètres généraux](./pricing-rule-general-settings.md): Définit le nom, la description, les dates actives, la priorité d’une règle et définit le comportement des règles suivantes, en fonction de son paramètre de priorité.
- [Conditions](./pricing-rule-conditions.md): Déterminez quels produits sont admissibles à la règle de prix.
- [Actions](./pricing-rule-actions.md): Définissez les calculs d&#39;ajustement appliqués à la source de prix pour déterminer le prix d&#39;annonce.

Vous pouvez créer des [règles de tarification standard](./standard-price-rules.md) qui ajustent automatiquement le prix de votre annonce Amazon par rapport au **[!UICONTROL Magento Price Source]** dans votre [prix de vente](./listing-price.md) paramètres. Cette fonctionnalité vous permet de manipuler vos prix Amazon d’une manière similaire à la [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}. Vous pouvez créer des règles complexes qui modifient automatiquement les prix de produits spécifiques, de produits appartenant à des catégories spécifiques ou de produits ayant des attributs spécifiques. Vous pouvez compléter les paramètres traditionnels et réévaluer vos produits pour les augmenter ou les diminuer en fonction d’un montant ou d’un pourcentage fixe.

Un autre outil puissant est [Réévaluation intelligente](./intelligent-repricing-rules.md) qui ajuste le prix de votre annonce Amazon en fonction de votre concurrent [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix ou [Prix compétitif le plus bas](./lowest-competitor-pricing.md). Similaire à la propriété [!DNL Commerce] [règles de prix du catalogue](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}, cette fonctionnalité avancée vous permet de manipuler vos prix Amazon en créant des règles complexes. Les règles peuvent définir la portée d’une modification de prix pour des produits spécifiques, des produits appartenant à des catégories spécifiques ou même avec des attributs de produit spécifiques.

Utiliser des prix intelligents pour ajuster vos prix d&#39;achat Amazon, en fonction des prix pratiqués par les concurrents. Le canal de vente Amazon a intégré des sauvegardes que vous pouvez configurer pour protéger les marges ou éviter de faire correspondre les prix d&#39;un commerçant avec un retour d&#39;information faible. Utilisation [règles de tarification intelligente](./intelligent-repricing-rules.md), les prix de vente Amazon peuvent être automatiquement manipulés sous la forme d&#39;un montant fixe ou d&#39;un pourcentage (à la hausse ou à la baisse) ou même synchronisés avec le [[!DNL Buy Box]](./buy-box-competitor-pricing.md) prix ou [Prix compétitif le plus bas](./lowest-competitor-pricing.md) par article. Les règles peuvent même être empilées pour offrir une flexibilité illimitée.

Vous pouvez contrôler des aspects importants des règles, tels que l’état actif/inactif, l’éligibilité au site web, les plages de dates facultatives et les niveaux de priorité facultatifs (utilisés pour l’empilement de règles).

Par exemple, vous pouvez définir et définir les conditions d’une règle de prix qui, lorsque les conditions sont remplies, ajuste automatiquement le prix de votre annonce avant qu’elle ne soit envoyée à Amazon.

Une autre option de tarification est [remplacement de prix](./overrides.md), qui est défini au niveau de la liste individuelle. A [remplacement de prix](./overrides.md) peut être définie, et un remplacement ignore/prend la priorité sur tous les autres paramètres, paramètres et règles par défaut. An [remplacer](./overrides.md) peut être défini pour le prix, le délai de traitement, l’état et les notes du vendeur (à quelques exceptions près).

![Règles de tarification](assets/amazon-pricing-rules.png)

## Colonnes par défaut

| Colonne | Description |
|---|---|
| [!UICONTROL Name] | Nom de la règle de tarification, tel que défini dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | Le type de règle, tel que défini dans [Actions des règles de tarification](./pricing-rule-actions.md) (règle de prix standard ou règle de retarification intelligente) |
| [!UICONTROL Is Active] | Si la règle est active, comme défini dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | La priorité par rapport aux autres conditions de tarification, telles que définies dans [Paramètres généraux des règles de tarification](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Indique si d’autres règles de prix sont traitées sur les produits éligibles à cette règle, comme indiqué dans [règle de tarification paramètres généraux](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Début de la période dans laquelle la règle est active |
| [!UICONTROL To Date] | Fin de la période pendant laquelle la règle est active |
| [!UICONTROL Action] | Répertorie toutes les actions pouvant être appliquées à une liste spécifique. Pour appliquer une action, cliquez sur **[!UICONTROL Select]** dans la _[!UICONTROL Action]_colonne. Options : `Edit Price Rule` / `Delete Price Rule` |
