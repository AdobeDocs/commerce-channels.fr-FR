---
title: Création et modification des remplacements de canal de vente Amazon
description: Utilisez les remplacements de Sales Channel Amazon pour appliquer vos modifications à une seule liste Amazon ou à plusieurs listes.
feature: Sales Channels, Products, Configuration
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---

# Créer et modifier des remplacements

Vous pouvez créer et remplacer une liste, modifier ou supprimer un remplacement qui a été appliqué à une liste. Permet de remplacer une valeur définie pour une liste spécifique.

## Créer un remplacement pour une seule liste

L’action _[!UICONTROL Create Override]_est disponible lors de l’affichage de listes sur les onglets_[!UICONTROL Inactive]_, _[!UICONTROL Active]_et_[!UICONTROL Ineligible]_.

1. Affichez une liste sur une page _[!UICONTROL Products Listings]_(onglet_[!UICONTROL Inactive]_, _[!UICONTROL Active]_et_[!UICONTROL Ineligible]_).

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Create Override]**pour ouvrir la page Remplacements de la liste de produits .

   ![créer un remplacement de liste Amazon](assets/amazon-select-create-override.png){width="220"}

1. Pour vous assurer que vous consultez la liste correcte, vérifiez le _[!UICONTROL Listing Details]_.

1. Déterminez le type de remplacement que vous créez.

   Vous pouvez définir un seul type de remplacement ou toute combinaison de types pour la liste (prix, heure de traitement, condition, notes de vente).

   - **Price** - Cliquez sur **[!UICONTROL Change Listing Price]** et saisissez la valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Handling Time** - Cliquez sur **[!UICONTROL Change Handling Time]** et saisissez la valeur de temps définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour **[!UICONTROL Condition Override]**.
   - **Notes du vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   La page _[!UICONTROL Product Listing Overrides]_se ferme. L’état de la liste passe à `Relist in Progress`. La modification sera publiée sur Amazon avec votre prochaine synchronisation des données (telle que configurée dans vos paramètres cron). La liste est également ajoutée à l’onglet_[!UICONTROL Overrides]_ .

L’exemple suivant illustre un remplacement qui définit un nouveau prix de `$55`, une nouvelle période de traitement de `1 day`, une nouvelle condition de `Used; Like New` et un nouveau texte de note du vendeur.

![Exemple de remplacement de liste Amazon](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## Modification ou suppression d’un remplacement pour une seule liste {#edit-override-single-listing}

L’action _[!UICONTROL Edit Overrides]_est disponible lors de l’affichage de listes sur l’onglet_[!UICONTROL Overrides]_.

1. Affichez une liste sur la page _[!UICONTROL Product Listings]_(onglet_[!UICONTROL Overrides]_).

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   La page _[!UICONTROL Product Listing Overrides]_s’ouvre.

   ![Sélectionner un remplacement de liste Amazon](assets/amazon-select-edit-overrides.png){width="125"}

1. Pour vous assurer que vous remplacez la liste correcte, vérifiez le _[!UICONTROL Listing Details]_.

1. Pour modifier vos paramètres _[!UICONTROL Override]_, définissez les sections correspondant au type que vous souhaitez modifier (Prix, Heure de traitement, Condition, Notes de vente).

   Pour conserver un type de remplacement identique, sélectionnez `No Change To <override type>` (valeur par défaut). Ce paramètre laisse la valeur de remplacement définie précédemment inchangée.

   - **Price** - Cliquez sur **[!UICONTROL Change Listing Price]** et saisissez la valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Handling Time** - Cliquez sur **[!UICONTROL Change Handling Time]** et saisissez la valeur de temps définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour **[!UICONTROL Condition Override]**.
   - **Notes du vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Pour supprimer un type de remplacement, cliquez sur **Supprimer** pour chacun des types à supprimer. Si elle n’est pas supprimée, la valeur précédemment définie reste dans le remplacement.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   La page _[!UICONTROL Product Listing Overrides]_se ferme. L’état de la liste passe à `Relist in Progress`. La modification sera publiée sur Amazon avec votre prochaine synchronisation des données (telle que configurée dans vos paramètres cron). Si elles ne sont pas déjà répertoriées, les listes sont également ajoutées à l’onglet_[!UICONTROL Overrides]_ .

Traitement ping sur l&#39;exemple _Create an Override_ . L’exemple suivant montre une modification du remplacement créé précédemment qui définit un nouveau prix de `$50`, supprime le remplacement de l’heure de gestion et conserve les remplacements de conditions et de notes de vente précédents.

![Modification ou suppression d’un remplacement](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## Modifier ou supprimer un remplacement pour plusieurs listes {#edit-override-multiple-listings}

L’action _[!UICONTROL Edit Listing Overrides]_est disponible sur les onglets_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ et _[!UICONTROL Ineligible]_.

>[!NOTE]
>
>Puisque vous modifiez les remplacements pour plusieurs listes, la section _[!UICONTROL Listing Details]_ne s’affiche pas comme elle le fait lors de la modification d’une seule liste.

1. Affichez la liste sur une page _[!UICONTROL Products Listings]_(onglet_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ et _[!UICONTROL Ineligible]_).

1. Cochez la case dans la colonne de gauche pour chacune des listes que vous souhaitez modifier.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Edit Listing Overrides]**.

   La page _[!UICONTROL Product Listing Overrides]_s’ouvre.

   ![Sélectionner un remplacement de liste Amazon](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. Pour modifier vos paramètres _[!UICONTROL Override]_, définissez les sections correspondant au type que vous souhaitez modifier (Prix, Heure de traitement, Condition, Notes de vente).

   Pour conserver un remplacement identique, sélectionnez `No Change To <override type>` (par défaut). Ce paramètre laisse la valeur de remplacement définie précédemment inchangée.

   - **Price** - Cliquez sur **[!UICONTROL Change Listing Price]** et saisissez la valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Handling Time** - Cliquez sur **[!UICONTROL Change Handling Time]** et saisissez la valeur de temps définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour **[!UICONTROL Condition Override]**.
   - **Notes du vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Pour supprimer un type de remplacement, cliquez sur **[!UICONTROL Remove]** pour chacun des types à supprimer. Si elle n’est pas supprimée, la valeur précédemment définie reste dans le remplacement.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   La page _[!UICONTROL Product Listing Overrides]_se ferme. L’état des listes passe à `Relist in Progress`. La modification sera publiée sur Amazon avec votre prochaine synchronisation des données (telle que configurée dans vos paramètres cron). Si elles ne sont pas déjà répertoriées, les listes sont également ajoutées à l’onglet_[!UICONTROL Overrides]_ .

### Types de remplacement

| Remplacement | Description |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | Un remplacement de prix définit le prix des listes. Ce remplacement a la priorité sur tous les paramètres automatisés jusqu’à ce qu’il soit supprimé.<br><br>Pour remplacer le prix de votre produit, choisissez **[!UICONTROL Change Listing Price]** et saisissez le nouveau prix de **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Un remplacement de durée de gestion définit le temps (en jours) nécessaire au traitement et à l’envoi des produits. Un remplacement de temps de traitement a la priorité sur tous les paramètres de temps de traitement automatisés et par défaut jusqu’à ce que le remplacement soit supprimé.<br><br>La valeur qui existe dans la zone _[!UICONTROL Handling Time Override]_est soit le temps de gestion par défaut défini dans vos [paramètres de liste](./listing-settings.md), soit le temps de traitement de remplacement défini. Si vous supprimez un remplacement de délai de gestion, la liste utilise par défaut le délai de gestion défini dans vos paramètres de liste.<br><br>Pour définir un remplacement de délai de gestion, choisissez **[!UICONTROL Change Handling Time]**et saisissez le nouveau délai de traitement (en jours) pour **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Pour remplacer la condition de liste, choisissez **[!UICONTROL Change Condition]** et choisissez la nouvelle condition dans **Condition Override**. |
| [!UICONTROL Seller Notes Override] | Pour les produits de votre catalogue définis avec une condition autre que `New`, une note de vendeur peut être ajoutée pour détailler davantage votre produit et son état pour les acheteurs potentiels. Vous pouvez saisir un remplacement de note de vendeur pour un produit de condition `New`, mais Amazon n’affiche pas la note.<br><br>Pour remplacer les notes du vendeur, choisissez **[!UICONTROL Change Seller Notes]** et saisissez la nouvelle note pour **[!UICONTROL Seller Notes Override]**. |
