---
title: Publier les listes vers Walmart
description: Publiez des listes de produits Commerce sur Walmart Marketplace pour commencer à vendre.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Publier les listes vers Walmart

Comme d&#39;autres marchés, Walmart permet aux vendeurs tiers de répertorier les articles vendus par d&#39;autres personnes.

La plateforme utilise des identifiants de produit comme UPC et GTIN pour faire correspondre des articles déjà en vente.
Pour les produits correspondants, la liste existante de Walmart Marketplace est mise à jour afin d’inclure l’offre du produit Commerce.
En règle générale, les produits dont les prix sont les plus bas apparaissent en premier dans les résultats. Mais d&#39;autres facteurs comme les révisions affectent également le placement.

## Processus de correspondance

Lorsque vous faites correspondre des produits, Channel Manager envoie les données de produit à Walmart Marketplace pour rechercher des listes existantes avec des valeurs d’attribut correspondant à l’attribut de produit Commerce mappé.

Si une correspondance est trouvée, la liste de produits existante est mise à jour pour ajouter votre offre.

## Conditions préalables

Avant de faire correspondre des produits, vérifiez que les valeurs d’attribut de votre catalogue de produits répondent aux exigences de Walmart et configurez les paramètres d’attribut. Voir [Configuration de la correspondance des produits](map-product-attributes-for-matching.md)

## Sélection et mise en correspondance de produits

1. Ouvrez un canal de vente connecté.

1. De **[!UICONTROL Listings]**, sélectionnez les produits qui correspondent à *[!UICONTROL Draft]* statut.

   ![Sélection de produits dans les listes et envoi pour correspondance](assets/products-in-marketplace-sales-channel.png)

1. Sélectionner **[!UICONTROL Match Products]**.

   Un message indique le nombre de produits envoyés pour la correspondance.

   ![Envoi de produits au canal de vente connecté](assets/products-submit-for-matching.png)

   Cela peut prendre jusqu’à 30 minutes pour que Walmart Marketplace termine l’opération de match.

   L’état des produits sélectionnés passe à *[!UICONTROL Processing]* jusqu’à ce que les opérations de correspondance se terminent. Cela peut prendre jusqu’à 30 minutes pour que Walmart Marketplace termine l’opération de match.

## Vérifier l’état de correspondance

1. Sélectionner **Actualiser les produits** pour mettre à jour l’état le plus récent du produit.

1. Vérifiez l’état du produit.

   Une fois la correspondance terminée, l’état peut être *Correspondance* ou *Erreur*.

   * **[!UICONTROL Match]** indique que la correspondance du produit a été établie. Votre offre de produit a été publiée dans une liste Walmart Marketplace existante.

   * **[!UICONTROL Error]** indique l’un des éléments suivants :

      * Une erreur s’est produite et l’opération de correspondance a échoué.

      * Aucune correspondance n’a été trouvée.

      * Correspondance trouvée, mais produit publié en tant qu’évaluation car la variable [Le magasin Marketplace n’est pas principal](walmart-prerequisites.md#walmart-marketplace-store-status).

## Dépannage des erreurs de correspondance de produit

Si l’opération de correspondance de produit échoue, Walmart Marketplace renvoie un code d’erreur et Channel Manager affiche l’état d’erreur dans les informations de liste de produits.

Pour afficher le détail des messages d’erreur, survolez le **Erreur** libellé d’état. Les erreurs courantes renvoyées sont des valeurs d’ID de produit mal formatées ou des attributs obligatoires manquants.

## Correction des valeurs d’ID de produit

| Type | Description | Exemple |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, nombre à 12 chiffres comprenant un chiffre de contrôle.</br></br>Si votre CUP comporte moins de 12 chiffres, comme UPC-E qui est de 8 chiffres, ajoutez</br>des zéros de début pour répondre aux exigences. | Modifier à partir de `45678912345` to `045678912345` |
| GTIN | GTIN-14, nombre à 14 chiffres incluant un chiffre de contrôle.</br></br>Si votre GTIN comporte moins de 14 chiffres, ajoutez des zéros de début. </br>pour répondre aux exigences. | Modifier `456789123456` to `0045678912345` |
| EAN | GTIN-13, nombre à 13 chiffres incluant un chiffre à cocher.</br></br>Si votre EAN comporte moins de 13 chiffres, ajoutez au début</br>zéros pour répondre aux exigences. | Modifier à partir de `4567891234` to `0004567891234` |

Pour plus d’informations sur les codes d’erreur de Walmart Marketplace, reportez-vous à la section [Aide de Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).
