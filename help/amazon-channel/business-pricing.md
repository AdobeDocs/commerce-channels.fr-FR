---
title: "[!DNL (B2B) Business Price] pour les listes Amazon"
description: Vous pouvez répertorier vos  [!DNL Commerce] produits de magasin sur le site Amazon Business (B2B) en activant les activités dans votre compte Amazon [!DNL Seller Central] .
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] pour les listes Amazon

(B2B) Les paramètres de prix pour l’entreprise font partie de vos paramètres de liste de magasins. Les paramètres de liste sont accessibles à partir du [tableau de bord du magasin Amazon](./amazon-store-dashboard.md).

[!DNL Amazon Business] est une marketplace réservée aux comptes commerciaux enregistrés Amazon et n’est disponible qu’aux États-Unis, en France, en Allemagne et au Royaume-Uni. Si le marketplace autorise la tarification commerciale B2B, elle est modifiable dans les paramètres de vos listes.

[!DNL B2B Business Pricing] permet aux commerçants disposant de comptes professionnels de s’acheter les uns des autres avec les performances attendues de l’expérience d’achat d’Amazon. Grâce aux prix d’entreprise B2B, les entreprises peuvent proposer des prix différenciés en fonction de la quantité achetée.

Pour que vos produits soient répertoriés sur le site [!DNL Amazon Business (B2B)], vous devez d’abord activer les activités dans votre compte [!DNL Amazon Seller Central]. Pour plus d’informations sur la fonctionnalité B2B, voir [Amazon : B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} (nécessite une connexion Seller Central).

## Configuration des paramètres [!DNL (B2B) Business Price]

1. Cliquez sur **[!UICONTROL Listing Settings]** dans le tableau de bord du magasin.

1. Développez la section _[!UICONTROL (B2B) Business Price]_.

1. Pour **[!UICONTROL Enable Business Pricing]**, choisissez une option.

   - `Disabled` - (Par défaut) Choisissez les cas où vous ne souhaitez pas activer les ventes entre entreprises. Lorsque vous le souhaitez, tous les autres champs de cette section sont désactivés.

   - `Enabled` - Choisissez le moment où vous souhaitez activer vos ventes entre entreprises. Lorsque cette option est activée, le prix de l’entreprise est défini sur le prix de la liste une fois toutes les règles de prix appliquées. Le prix de l’entreprise respecte la portée du prix du site web, si cette option est activée. Le prix d’une entreprise ne peut pas être inférieur à 1 $.

1. Pour **[!UICONTROL Enable Tiered Pricing]**, choisissez une option.

   - `Disabled` - (Par défaut) Choisissez quand vous souhaitez obtenir le même prix d’inscription pour toutes les quantités commandées. Lorsque cette option est sélectionnée, tous les champs _[!UICONTROL Pricing Level]_de cette section sont désactivés.

   - `Enabled` - Choisissez le moment où vous souhaitez activer les ajustements de prix en fonction de la quantité de commande. Lorsque cette option est sélectionnée, les champs _[!UICONTROL Pricing Level]_sont activés.

1. Renseignez les paramètres **[!UICONTROL Pricing Level]**.

   Vous pouvez définir jusqu’à cinq paramètres de quantité/remise qui définissent le niveau de prix pour vos listes commerciales. Dans chaque ligne, saisissez la valeur du seuil de quantité et le pourcentage de remise à appliquer. Par exemple, si vous saisissez `5` dans le premier champ de la première ligne et `5` dans le deuxième champ, le prix applique une remise de 5 % lorsqu’une autre entreprise achète une quantité de 5 ou plus.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save listing settings]**.

![ Tarifs professionnels Amazon (B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| Champ | Description |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | Options : <ul><li>**[!UICONTROL Disabled]** - (Par défaut) Choisissez les cas où vous ne souhaitez pas activer les ventes entre entreprises. Lorsque cette option est sélectionnée, tous les autres champs de cette section sont désactivés.</li><li>**[!UICONTROL Enabled]** - Choisissez le moment où vous souhaitez activer les ventes de votre entreprise. Lorsqu’il est sélectionné, le prix de l’entreprise est défini sur le prix de la liste après l’application de toutes les règles de prix. Le prix de l’entreprise respecte la portée du prix du site web, si cette option est activée. Le prix d’une entreprise ne peut pas être inférieur à 1 $.</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | (Obligatoire) Options : <ul><li>**[!UICONTROL Disabled]** - (Par défaut) Choisissez quand vous souhaitez obtenir le même prix d’inscription pour toutes les quantités commandées. Lorsque cette option est sélectionnée, tous les champs _[!UICONTROL Pricing Level]_de cette section sont désactivés.</li><li>**[!UICONTROL Enabled]** - Choisissez le moment où vous souhaitez activer la tarification qui s’ajuste en fonction de la quantité de la commande. Lorsque cette option est sélectionnée, les champs _[!UICONTROL Pricing Level]_sont activés.</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | Lorsque la fonction Tarification par niveaux est activée, vous pouvez définir jusqu’à cinq paramètres de quantité/remise qui définissent le niveau de prix pour vos listes commerciales. Dans chaque ligne, saisissez la valeur du seuil de quantité et le pourcentage de remise à appliquer. Par exemple, si vous saisissez `5` dans le premier champ de la première ligne et `5` dans le deuxième champ, le prix applique une remise de 5 % lorsqu’une autre entreprise achète une quantité de cinq ou plus. |

**Accès rapide** - [!UICONTROL Listing Settings] sections

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
