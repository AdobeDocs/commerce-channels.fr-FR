---
title: Création et modification de remplacements
description: Utilisez les remplacements de Sales Channel Amazon pour appliquer vos modifications à une seule annonce Amazon ou à plusieurs annonces.
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# Création et modification de remplacements

Vous pouvez créer et remplacer une annonce, modifier ou supprimer une modification qui a été appliquée à une annonce. Les remplacements définissent une valeur définie pour une annonce spécifique.

## Créer un remplacement pour une seule annonce

Le _[!UICONTROL Create Override]_est disponible lors de l’affichage des annonces sur le_[!UICONTROL Inactive]_, _[!UICONTROL Active]_et_[!UICONTROL Ineligible]_ onglets.

1. Afficher la liste sur un _[!UICONTROL Products Listings]_page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_et_[!UICONTROL Ineligible]_ ).

1. Dans la boîte de dialogue _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Create Override]**pour ouvrir la page Remplacements de la liste de produits.

   ![créer un remplacement de liste Amazon](assets/amazon-select-create-override.png)

1. Pour vous assurer que vous consultez la liste correcte, vérifiez le _[!UICONTROL Listing Details]_.

1. Déterminez le type de remplacement que vous créez.

   Vous pouvez définir un type de remplacement unique ou une combinaison de types pour la mise en vente (Prix, Heure de traitement, Condition, Informations sur le vendeur).

   - **Prix** - Cliquez sur **[!UICONTROL Change Listing Price]** et entrez votre valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Temps de traitement** - Cliquez sur **[!UICONTROL Change Handling Time]** et entrez la valeur temporelle définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour l’option **[!UICONTROL Condition Override]**.
   - **Informations sur le vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   Le _[!UICONTROL Product Listing Overrides]_se ferme. Le statut de la liste change en `Relist in Progress`. La modification sera publiée à Amazon avec votre prochaine synchronisation de données (comme configuré dans vos paramètres cron). La liste est également ajoutée au_[!UICONTROL Overrides]_ .

L’exemple suivant montre un remplacement qui définit un nouveau prix de `$55`, un nouveau délai de traitement de `1 day`, une nouvelle condition de `Used; Like New`, et nouveau texte de note du vendeur.

![Exemple de remplacement de la liste Amazon](assets/amazon-overrides-edit.png)

## Modification ou suppression d’un remplacement pour une seule annonce {#edit-override-single-listing}

Le _[!UICONTROL Edit Overrides]_est disponible lors de l’affichage des annonces sur le_[!UICONTROL Overrides]_ .

1. Affichez une liste dans le dossier _[!UICONTROL Product Listings]_page (_[!UICONTROL Overrides]_ ).

1. Dans la boîte de dialogue _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   Le _[!UICONTROL Product Listing Overrides]_s’ouvre.

   ![Sélectionner un remplacement de liste Amazon](assets/amazon-select-edit-overrides.png)

1. Pour vous assurer que vous remplacez la liste correcte, vérifiez le _[!UICONTROL Listing Details]_.

1. Pour modifier votre _[!UICONTROL Override]_, définissez les sections pour le type que vous souhaitez modifier (Prix, Heure de traitement, Condition, Informations sur le vendeur).

   Pour conserver un type de remplacement identique, sélectionnez `No Change To <override type>` (par défaut). Ce paramètre ne modifie pas la valeur de remplacement définie précédemment.

   - **Prix** - Cliquez sur **[!UICONTROL Change Listing Price]** et entrez votre valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Temps de traitement** - Cliquez sur **[!UICONTROL Change Handling Time]** et entrez la valeur temporelle définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour **[!UICONTROL Condition Override]**.
   - **Informations sur le vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Pour supprimer un type de remplacement, cliquez sur **Supprimer** pour chacun des types à supprimer. Si elle n’est pas supprimée, la valeur précédemment définie reste dans le remplacement.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   Le _[!UICONTROL Product Listing Overrides]_se ferme. Le statut de la liste change en `Relist in Progress`. La modification sera publiée à Amazon avec votre prochaine synchronisation de données (comme configuré dans vos paramètres cron). S’ils ne sont pas déjà répertoriés, les annonces sont également ajoutées au_[!UICONTROL Overrides]_ .

Piggyback sur _Créer un remplacement_ exemple. L’exemple suivant montre une modification du remplacement créé précédemment qui définit un nouveau prix de `$50`, supprime le paramètre Temps de traitement personnalisé et conserve les remplacements Condition et Notes du vendeur précédents.

![Modification ou suppression d’un remplacement](assets/amazon-overrides-edit-2.png)
__

## Modification ou suppression d’un remplacement pour plusieurs annonces {#edit-override-multiple-listings}

Le _[!UICONTROL Edit Listing Overrides]_est disponible sur la_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ et _[!UICONTROL Ineligible]_onglets.

>[!NOTE]
>
>Étant donné que vous modifiez les remplacements pour plusieurs annonces, la _[!UICONTROL Listing Details]_ne s’affiche pas comme lors de la modification d’une seule annonce.

1. Afficher la liste sur un _[!UICONTROL Products Listings]_page (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ et _[!UICONTROL Ineligible]_).

1. Cochez la case dans la colonne de gauche pour chacun des annonces à modifier.

1. Sous _[!UICONTROL Actions]_, cliquez sur **[!UICONTROL Edit Listing Overrides]**.

   Le _[!UICONTROL Product Listing Overrides]_s’ouvre.

   ![Sélectionner un remplacement de liste Amazon](assets/amazon-actions-edit-listing-overrides.png)

1. Pour modifier votre _[!UICONTROL Override]_, définissez les sections pour le type que vous souhaitez modifier (Prix, Heure de traitement, Condition, Informations sur le vendeur).

   Pour conserver un remplacement identique, sélectionnez `No Change To <override type>` (par défaut). Ce paramètre ne modifie pas la valeur de remplacement définie précédemment.

   - **Prix** - Cliquez sur **[!UICONTROL Change Listing Price]** et entrez votre valeur de prix définie pour **[!UICONTROL Price Override]**.
   - **Temps de traitement** - Cliquez sur **[!UICONTROL Change Handling Time]** et entrez la valeur temporelle définie (en jours) pour **[!UICONTROL Handling Time Override]**.
   - **Condition** - Cliquez sur **[!UICONTROL Change Condition]** et sélectionnez l’option appropriée pour **[!UICONTROL Condition Override]**.
   - **Informations sur le vendeur** - Cliquez sur **[!UICONTROL Change Seller Notes]** et saisissez le texte de vos notes pour **[!UICONTROL Seller Notes Override]**.

1. Pour supprimer un type de remplacement, cliquez sur **[!UICONTROL Remove]** pour chacun des types à supprimer. Si elle n’est pas supprimée, la valeur précédemment définie reste dans le remplacement.

1. Cliquez sur **[!UICONTROL Save Listing Override]**.

   Le _[!UICONTROL Product Listing Overrides]_se ferme. Le statut des annonces change en `Relist in Progress`. La modification sera publiée à Amazon avec votre prochaine synchronisation de données (comme configuré dans vos paramètres cron). S’ils ne sont pas déjà répertoriés, les annonces sont également ajoutées au_[!UICONTROL Overrides]_ .

### Remplacer les types

| Remplacer | Description |
|--- |--- |
| [!UICONTROL Price Override] | Un remplacement de prix définit le prix des annonces. Ce remplacement prend la priorité sur tous les paramètres automatisés jusqu’à ce que le remplacement soit supprimé.<br><br>Pour remplacer le prix de votre produit, sélectionnez **[!UICONTROL Change Listing Price]** et entrez le nouveau prix pour **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | Un délai de manutention personnalisé définit le temps nécessaire (en jours) pour traiter et expédier les produits. Un remplacement de temps de traitement prend la priorité sur tous les paramètres de temps de traitement automatisés et par défaut jusqu’à ce que le remplacement soit supprimé.<br><br>La valeur qui existe dans la propriété _[!UICONTROL Handling Time Override]_est soit votre temps de traitement par défaut défini dans votre [paramètres de liste](./listing-settings.md) ou votre temps de traitement de remplacement défini. Si vous supprimez un délai de traitement personnalisé, la liste prend par défaut le délai de traitement défini dans vos paramètres d&#39;annonce.<br><br>Pour définir un délai de traitement personnalisé, sélectionnez **[!UICONTROL Change Handling Time]**et entrez le nouveau délai de traitement (en jours) pour **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Pour remplacer la condition d’annonce, sélectionnez **[!UICONTROL Change Condition]** et sélectionnez la nouvelle condition dans **Remplacement de condition**. |
| [!UICONTROL Seller Notes Override] | Pour les produits de votre catalogue qui sont définis avec une condition autre que `New`, une note de vendeur peut être ajoutée afin de préciser votre produit et son état aux acheteurs potentiels. Vous pouvez saisir un remplacement de note de vendeur pour un `New` produit conditionnel, mais Amazon n’affiche pas la note.<br><br>Pour remplacer les notes du vendeur, sélectionnez **[!UICONTROL Change Seller Notes]** et saisissez la nouvelle note pour **[!UICONTROL Seller Notes Override]**. |
