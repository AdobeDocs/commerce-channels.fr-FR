---
title: '[!DNL Amazon Sales Channel] notes de mise à jour'
description: Consultez les notes de mise à jour pour plus d’informations sur toutes les versions de  [!DNL Amazon Sales Channel]  .
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# Notes de mise à jour de [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] peut être installé sur des instances avec Magento Open Source, Adobe Commerce et Adobe Commerce sur les versions 2.3.x et 2.4.x de l’infrastructure cloud. L’extension n’est plus prise en charge sur Adobe Commerce 2.1, Magento Open Source 2.2 ou Magento 1.
> <br>La prise en charge est disponible pour [!DNL Amazon sales channel] versions 4.0.0 et 4.1.0 sur les versions Adobe Commerce 2.3.x uniquement.
> <br>[!DNL Amazon sales channel] La version 4.2.0+ est compatible avec les versions Adobe Commerce 2.3.x, mais la prise en charge est disponible uniquement pour les versions Adobe Commerce 2.4.x.
>

Ces notes de mise à jour décrivent la version initiale de [!DNL Amazon sales channel] et incluent :

![New](../assets/new.svg) Nouvelles fonctionnalités
![Problème corrigé](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

Voir [Versions à venir](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) pour en savoir plus sur le contrôle de version, la prise en charge et la compatibilité.

Voir [Disponibilité du produit](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) pour savoir quelles versions d’Adobe Commerce prennent en charge cette extension.

## v4.5.0

*30 août 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la passerelle API Adobe.IO, qui change depuis MAGI, pour une sécurité d’authentification améliorée. `ServicesId` fournit une nouvelle interface utilisateur pour gérer vos informations d’identification Adobe.IO, comme pour les autres [services Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Les commerçants doivent s’assurer que les [clés d’API privée et publique](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) sont mises à jour pour production.


![ Correction d’un problème ](../assets/fix.svg) Identifiant un problème de paramètre de configuration et correction du flux de création de commande.

## v4.4.4

*7 mars 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![ Correction d’un problème ](../assets/fix.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.6 et de PHP 8.2.

![Correction d’un problème](../assets/fix.svg) : réduction du bruit dans les journaux.

![Correction d’un problème](../assets/fix.svg) Amélioration de la stabilité de l’extraction des mises à jour.

![ Correction d’un problème ](../assets/fix.svg) : simplification du processus d’exécution d’une extraction unique de type action ou d’application à partir de l’interface de ligne de commande.

![ Correction d’un problème ](../assets/fix.svg) Mise à niveau de la dépendance pour `magento/services-connector`.

![ Correction d’un problème ](../assets/fix.svg) Correction de problèmes de synchronisation dans les comptes britanniques avec un code de pays non valide.

![Correction d’un problème](../assets/fix.svg) Le codage en dur de l’entité entity_type_id pour l’entité de produit catalogue entraîne des problèmes avec le Source de prix Magento.

![Correction d’un problème ](../assets/fix.svg) Correction d’un problème qui empêchait également la suppression de comptes supprimés sur un serveur principal à partir d’une autre instance dans l’interface utilisateur.

![ Correction d’un problème en raison duquel certaines règles de panier endommageaient l’importation de l’ordre.](../assets/fix.svg)

## v4.4.3

*7 mars 2023*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Correctif](../assets/fix.svg) Ajout de la prise en charge d’Adobe Commerce 2.4.4.

## v4.4.2

*11 novembre 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Correctif](../assets/fix.svg) Mise à jour des dépendances pour la prise en charge d’autres extensions mises à jour.
![Fix](../assets/fix.svg) Ajout de la prise en charge de PHP 8.1.

## v4.4.1

*11 novembre 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Correctif](../assets/fix.svg) Modification de la manière dont Adobe Commerce reçoit le champ _User Name_ d’Amazon. Auparavant, une erreur se produisait lors de la création de la commande lorsque le champ _Nom d’utilisateur_ contenait des caractères spéciaux. Adobe Commerce reçoit désormais les données _Nom d’utilisateur_ et filtre les caractères spéciaux afin que la commande puisse être créée.

## v4.4.0

*9 avril 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) Ajout de la prise en charge du mode Lecture seule à la configuration. Voir [Paramètres du canal de vente](sales-channel-settings.md).

![Correctif](../assets/fix.svg) Modification du flux de données afin que plusieurs copies de la même instance puissent récupérer les mises à jour simultanément.

![Correctif](../assets/fix.svg) Modification du processus de synchronisation des informations de compte. Ajout d’une tâche cron pour la synchronisation avec un compte distant et ajout de la même fonctionnalité aux commandes de l’interface de ligne de commande.

![Fix](../assets/fix.svg) Ajout d’arguments de commande CLI et de indicateurs pour un contrôle plus précis.

![Fix](../assets/fix.svg) Correction du Source Tâches en arrière-plan (cron) dans la configuration du système.

![Fix](../assets/fix.svg) Correction du problème empêchant la création de commandes lorsque le code de pays était défini sur Porto Rico (PR).

## v4.3.0

*3 mars 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Correctif](../assets/fix.svg) <!--CHAN-xxxx-->La fonctionnalité _Détails de la commande_ a été repensée et ne repose plus sur le paramètre _Importer des commandes_. Les détails de la commande s’affichent désormais dans l’interface du Sales Channel Amazon pour toutes les commandes.

![Correctif](../assets/fix.svg) Dans le menu _[!UICONTROL Marketing]_de l’Admin, le nom a été remplacé par_[!UICONTROL Amazon]_._[!UICONTROL Amazon Sales Channel]_

![Problème connu](../assets/bug.svg) **Important** : les problèmes connus de compatibilité avec Adobe Commerce 2.4.0 sont résolus dans la version Adobe Commerce 2.4.1.

- Processus Amazon cron à l’état `error`
- Échec de l’installation avec Commerce 2.4.0 lors de la création de magasins dans la base de données
- La création du produit échoue lorsque MSI est installé

## v4.2.0

*3 mars 2021*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

Si une version précédente de [!DNL Amazon sales channel] est installée et que vous tentez de mettre à jour votre Adobe Commerce vers la version 2.4.0, vous êtes invité à mettre à jour l’extension avant de pouvoir terminer la mise à jour d’Adobe Commerce.

![Problème connu](../assets/bug.svg) Lorsque [!DNL Amazon sales channel] 4.2.0 est intégré à la version 2.4.0 et que [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) est activé, un problème connu empêche l’ajout de produits dans votre catalogue Commerce. Ce problème sera résolu dans une prochaine version de Commerce.

![New](../assets/new.svg) [!DNL Amazon sales channel] a été amélioré afin d’accepter les données d’adresse textuelles et de les faire correspondre à des formats d’adresse normalisés, y compris la ville, l’état et le code postal. Cette mise à jour permet aux données de commande et d’expédition de se synchroniser (synchroniser) avec Amazon sans erreur d’adresse.<br/>Par exemple, un acheteur saisit la ville, l’état, le code postal comme `Escondido, californiA 92025-1501`. Amazon Sales Channel importe et fait correspondre les données au format standard `Escondido, CA 92025`, puis les resynchronise sur Amazon dans ce format normalisé.

![Nouveau](../assets/new.svg) Ajout de la prise en charge de PHP 7.4.

![Nouveau](../assets/new.svg) <!--CHAN-4334-->Ajout de la prise en charge d’Adobe Commerce 2.4.x. Les versions précédentes peuvent être compatibles avec Commerce 2.4.x, mais ne sont pas prises en charge. Voir [Versions à venir](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) pour connaître la compatibilité des versions. Amazon Sales Channel doit être mis à jour vers la version 4.2.0 avant que la mise à jour d’Adobe Commerce 2.4.0 ne puisse être terminée.

![Correctif](../assets/fix.svg) <!--CHAN-4431--> Correction d’un problème qui provoquait une erreur _Accès refusé_ pour les clients britanniques.

![Correction](../assets/fix.svg) <!--CHAN-4394--> Correction d’un problème qui empêchait la synchronisation de l’état d’expédition d’Amazon avec la commande Commerce correspondante, &quot;verrouillant&quot; ainsi l’état d’expédition de la commande sur `Pending` dans Commerce et `Unshipped` dans Amazon. Grâce à la nouvelle fonctionnalité d’adresse normalisée, ces erreurs d’état de livraison ont été résolues.

![Correctif](../assets/fix.svg) <!--ticket#--> Mise à jour de la synchronisation des commandes pour ignorer les importations de commandes ayant échoué, ce qui réduit les tentatives de synchronisation multiples et permet aux importations suivantes de traiter, avec les demandes de synchronisation de commande envoyées toutes les cinq minutes. Les erreurs de synchronisation sont toujours enregistrées dans le journal des erreurs, mais marquées comme &quot;traitées&quot; pour permettre d’autres fonctions de journalisation. En outre, [!DNL Amazon sales channel] supprime désormais automatiquement les données excédentaires collectées pour les commandes qui ne sont pas créées dans Commerce.

![Correctif](../assets/fix.svg) Mise à jour de la journalisation des erreurs pour collecter plus d’informations sur les erreurs d’exception non interceptées et de mise à jour d’extension.

![Correction](../assets/fix.svg) <!--ticket#--> Correction d’un problème qui entraînait l’échec de la synchronisation initiale des données _le prix le plus bas_ en raison d’une valeur _price_ manquante.

![Correction](../assets/fix.svg) <!--CHAN-4410--> Correction de problèmes qui provoquaient des erreurs de filtrage dans la vue _Commandes Amazon_ lorsque le champ de période n’est pas renseigné.

![Correction](../assets/fix.svg) <!--CHAN-4439--> Correction d’un problème qui provoquait des erreurs de synchronisation de stock et d’exécution liées à la quantité. L’extension arrondit désormais les valeurs de quantité saisies sous forme de décimale avant synchronisation avec Amazon.<br/> Par exemple, lorsqu’un commerçant entre manuellement une quantité de `2.5`, l’extension arrondit la valeur à `2`, puis synchronise la quantité mise à jour avec Amazon.

## v4.1.0

*7 mai 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) <!--4247, 4230-->Modification du processus d’importation de commandes afin de l’aligner sur les exigences de commande Commerce. Ces modifications corrigent les problèmes qui empêchaient Commerce de créer la commande correspondante pour une commande importée. Pour plus d’informations sur les programmes de blocage des commandes et les solutions, voir [Gestion des commandes](managing-orders.md) .

![Nouveau](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Mise à jour de la section _Commandes récentes_ du tableau de bord du magasin et ajout d’une nouvelle vue _Toutes les commandes_ qui affiche toutes vos commandes Amazon, y compris les options de filtre et la pagination pour afficher davantage de commandes. Voir [Tableau de bord de la boutique Amazon](amazon-store-dashboard.md) et [Afficher les commandes Amazon](amazon-orders-all.md).

![New](../assets/new.svg) Ajout de la colonne _[!UICONTROL Order Notes]_de la table_[!UICONTROL Amazon Orders]_ repensée dans les vues _[!UICONTROL Recent Orders]_et_[!UICONTROL All Orders]_. _[!UICONTROL Order Notes]_pour informer le commerçant qu’il existe un problème avec l’importation de la commande. Voir [Affichage des commandes Amazon](amazon-orders-all.md).

![Nouveau](../assets/new.svg) <!--CHAN-4013-->Mise à jour des paramètres de condition du produit pour s’aligner sur le programme [Amazon Renewed](https://sell.amazon.com/programs/renewed). Voir [Produits renouvelés](renewed-products.md).

![Nouveau](../assets/new.svg) <!--CHAN-3680-->Mise à jour de [Amazon Order Details](amazon-order-details.md) pour inclure des &quot;données génériques&quot; pour les commandes qui sont exécutées par Amazon. Voir [Complété par](fulfilled-by.md).

![Correctif](../assets/fix.svg) <!--CHAN-4069-->Correction d’un problème qui entraînait la distorsion des icônes sur la carte du magasin.

![Correctif](../assets/fix.svg) <!--CHAN-4165--> Correction d’une erreur qui empêchait l’affichage de l’écran _Connexion_ après l’expiration de la session.

![Correctif](../assets/fix.svg) <!--CHAN-4211--> Correction d’un problème qui empêchait l’importation du montant de la taxe de la commande Amazon dans la nouvelle commande Commerce.

![Correction](../assets/fix.svg) <!--CHAN-4234--> Correction d’un problème en raison duquel les totaux des recettes affichés sur le tableau de bord du magasin incluaient des commandes à l’état `Canceled` ou `Error`.

![Correction](../assets/fix.svg) <!--CHAN-4326--> Correction d’un problème qui provoquait des erreurs d’importation de commande associées à des extensions tierces qui utilisaient les méthodes _Magento Shipping_ pour créer des commandes.

![Fix](../assets/fix.svg) <!--CHAN-4357--> Correction d’un problème qui provoquait des erreurs lors de l’exécution de la synchronisation cron. Un verrouillage a été ajouté sur la commande d’interface de ligne de commande afin d’empêcher la synchronisation simultanée de deux tâches cron.

![Correctif](../assets/fix.svg) Mise à jour de la stratégie de sécurité du contenu pour la prise en charge de Commerce version 2.3.5.

## v4.0.0

*25 mars 2020*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

>[!IMPORTANT]
>
>Amazon Sales Channel 4.0.0 n’est pas pris en charge pour Adobe Commerce 2.3.5. Pour la prise en charge d’Adobe Commerce 2.3.5, effectuez une mise à niveau vers Amazon Sales Channel 4.1.0.

![Nouveau](../assets/new.svg) a introduit une nouvelle page d’accueil [Amazon Sales Channel](amazon-sales-channel-home.md) avec un &quot;affichage de carte&quot; amélioré pour les informations de votre boutique.

![Nouveau](../assets/new.svg) a introduit un nouveau [ tableau de bord de magasin ](amazon-store-dashboard.md) avec liste, commandes récentes et informations de paramètre de magasin.

![Nouveau](../assets/new.svg) a introduit un [processus d&#39;intégration](amazon-onboarding-home.md) et [paramètres de magasin par défaut](default-store-settings.md) plus simples et simplifiés pour que vos magasins s&#39;intègrent plus rapidement.

![Problème connu](../assets/bug.svg) <!--CHAN-4102--> Lorsque [ la création d’attributs](managing-attributes.md) pour l’importation d’images à partir de listes et que l’option **Vues de magasin** est définie sur `All Store Views (Global)`, un problème connu empêche l’importation d’images vers toutes les vues de magasin. Si vous modifiez le paramètre **Vues de magasin (pour importer des valeurs dans)** vers un magasin spécifique, les images sont importées pour ce magasin.

## v3.0.1

*11 novembre 2019*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Correctif](../assets/fix.svg) **Paramètres de champ numérique** : <!--CHAN-3779-->Les champs qui nécessitent une valeur numérique ont été mis à jour afin de n’accepter que les caractères numériques. Exemple : Paramètres des règles de tarification > champ Montant de l’ajustement

![Correctif](../assets/fix.svg) **Liens du guide de l’utilisateur** : <!--CHAN-3778-->Les liens _Guide de l’utilisateur_ incorrects ont été corrigés.

![Correctif](../assets/fix.svg) **Dupliquer les listes Amazon** : <!--CHAN-3593-->Un problème précédemment signalé qui entraîne la duplication de listes Amazon est maintenant corrigé. Avant cette version, l’extension ajoutait le code pays de la région Amazon aux valeurs de SKU lors de l’importation de listes. La liste correspondait à l’élément de catalogue, mais l’extension a créé une nouvelle liste en double avec le SKU ajouté. Avec cette version, l’extension ne modifie pas le SKU des listes importées et aucune modification n’est apportée aux listes existantes. Vous pouvez utiliser l’option [!UICONTROL End Listing(s)] sur Amazon pour supprimer les listes en double.

## v3.0.0

*7 octobre 2019*

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

![Nouveau](../assets/new.svg) **Amazon UK Marketplace Now Available** : les utilisateurs peuvent choisir la marketplace du Royaume-Uni lors de la création et de l’intégration d’un magasin Commerce. Cette mise à niveau vers le Royaume-Uni inclut une prise en charge supplémentaire pour :

- [Service de calcul de la TVA Amazon](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Code de taxe sur les produits](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

![Nouveau](../assets/new.svg) **Journalisation améliorée** : <!--CHAN-3642, 3672-->Mise en oeuvre de la fonction **Activer la journalisation de débogage** pour collecter des données de synchronisation supplémentaires lorsque le dépannage est nécessaire. Reportez-vous à la rubrique [Paramètres de Sales Channel](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) dans la référence de configuration.

![Correctif](../assets/fix.svg) **Catalogue de produits** : <!--CHAN-3687-->Correction d’un problème qui empêchait l’application des images importées avec une liste Amazon au produit de catalogue Commerce correspondant.

![Correctif](../assets/fix.svg) **Création de commande** : <!--CHAN-3708-->Correction d’un problème qui empêchait Commerce de créer des commandes pour une commande Amazon qui ne correspond pas à un produit de catalogue Commerce.

![Problème connu](../assets/bug.svg) **Dupliquer les listes Amazon** : <!--CHAN-3593-->Ce problème entraîne la création par le catalogue d’un élément pour une liste importée, à l’aide du même SKU, mais avec un code de région ajouté à la fin. Amazon traite ensuite le SKU modifié en tant que nouvel élément et crée une liste. Ce problème sera résolu dans une version ultérieure.

## v2.0.0

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"}

>[!NOTE]
>
>La version 1.0.0 était disponible en version limitée uniquement.

![Nouveau](../assets/new.svg) **Intégration et maintenance simplifiées** : ajoutez et intégrez votre compte Seller Amazon par le biais d’un processus détaillé avec des instructions détaillées disponibles via l’administration. Gérez vos magasins, comptes et produits répertoriés par le biais d’un seul tableau de bord.

![Nouveau](../assets/new.svg) **Prise en charge de plusieurs comptes** : gérez et surveillez plusieurs marques Amazon et régions du marché par l’intermédiaire de l’administrateur.

![Nouveau](../assets/new.svg) **Indice intelligent** : définissez des règles de tarification automatisée afin d’augmenter vos chances pour le Buy Box convoité. Paramétrez les prix pour qu&#39;ils s&#39;ajustent dynamiquement au prix Buy Box actuel, ou au prix concurrentiel le plus bas. Définissez des limites à la réévaluation des prix pour protéger vos marges.

![Nouveau](../assets/new.svg) **Gestion des listes** : automatisez les listes de produits et synchronisez votre catalogue Commerce avec Amazon Marketplace à l’aide des règles de liste. Ajoutez des remplacements spécifiques pour contrôler précisément vos offres. Surveillez et gérez toutes vos listes directement depuis l’administrateur.

![Nouveau](../assets/new.svg) **Inventory management cohérente** : maintenez les quantités d’inventaire de Commerce et Amazon constamment synchronisées.

![Nouveau](../assets/new.svg) **Gestion des commandes et des exécutions** : effectuez le suivi des commandes Amazon par le biais du tableau de bord, avec une communication transparente et des mises à jour d’inventaire. Effectuez le suivi et le suivi des envois de commande tels qu’ils ont été réalisés par Amazon, par le marchand rempli ou par une combinaison de méthodes.

![Problème connu](../assets/bug.svg) Vous pouvez rencontrer des temps d’attente plus longs pour mettre à jour les quantités de produits. La synchronisation des mises à jour de la quantité de produits peut prendre ~deux heures.

![Problème connu](../assets/bug.svg) Les commandes importées peuvent avoir un type de _Prime_ ou _Premium_ commandes. Vous devez vérifier ces commandes dans votre compte de vendeur Amazon.

![Problème connu](../assets/bug.svg) Les produits groupés non admissibles peuvent s’afficher comme étant éligibles pour une inscription sur Amazon. L’un des produits du produit regroupé peut ne pas être éligible. Si vous rencontrez des problèmes, vérifiez le statut d’éligibilité pour les éléments de produits regroupés.

![Problème connu](../assets/bug.svg) Lors de l’utilisation d’Inventory management pour Commerce 2.3.x, une réindexation partielle du stock peut ne pas se déclencher lors de la création d’une commande. La quantité vendable est recalculée toutes les heures, ce qui peut entraîner un ventes abusif pendant cet intervalle de mise à jour.
