# Documentation du Code C

Ce document vise à décrire les fonctionnalités, la structure et l'objectif du code C fourni.

## Aperçu

Le code C est une application simple conçue pour gérer un système de réservation de bus. Il comprend des fonctionnalités à la fois pour les clients et les administrateurs.

## Fonctionnalités

### Pour les Clients

1. **Créer un Compte** : Permet aux clients de créer un nouveau compte utilisateur en fournissant leur numéro de téléphone, leur nom et leur prénom.
2. **Réserver un Voyage** : Permet aux utilisateurs de faire une réservation pour un voyage en sélectionnant parmi les voyages disponibles.
3. **Voir les Réservations** : Affiche les réservations effectuées par l'utilisateur.
4. **Annuler une Réservation** : Permet aux utilisateurs d'annuler une réservation précédemment effectuée.

### Pour les Administrateurs

1. **Ajouter un Bus** : Permet aux administrateurs d'ajouter de nouveaux bus au système avec des détails tels que l'ID, la capacité et l'emplacement.
2. **Afficher les Bus** : Affiche une liste des bus disponibles, leurs détails et les voyages associés.
3. **Organiser un Voyage** : Permet aux administrateurs d'organiser un nouveau voyage, en allouant un bus et en spécifiant des détails tels que la destination, la date et le tarif.
4. **Afficher les Voyages** : Affiche une liste des voyages planifiés avec leurs détails.
5. **Afficher les Voyageurs** : Liste tous les voyageurs enregistrés.
6. **Déclarer le Retour d'un Bus** : Les administrateurs peuvent déclarer le retour d'un bus après son voyage.

## Structure du Code

### Structures de Données

Le code utilise plusieurs structures :
- `voyageur` pour stocker les détails des voyageurs.
- `bus` pour les informations sur les bus.
- `noeud` pour une structure de liste chaînée pour gérer les voyageurs.
- `voyage` pour stocker les détails du voyage.
- `reservation` pour contenir les détails de la réservation.

### Manipulation de Fichiers

1. **Entrée/Sortie de Fichiers** : Le code utilise la manipulation de fichiers pour lire et écrire dans des fichiers `.bin` afin de stocker les données sur les bus, les voyages et les réservations.

### Fonctions

Le code définit diverses fonctions, notamment :
- Création de compte (`creer_compte()`) et ajout de bus (`ajouter_bus()`).
- Fonctionnalités d'affichage (`affiche_bus()`, `affiche_voyages()`, `affiche_reservation()`, etc.).
- Gestion des réservations (`reserver()`, `annule_reservation()`).

## Utilisation

La fonction principale pilote le programme. Elle présente une interface basée sur un menu permettant aux clients et aux administrateurs de naviguer à travers les fonctionnalités disponibles.

### Gestion des Erreurs

Le code comprend des vérifications d'erreur de base pour l'ouverture de fichiers, la validation de l'entrée utilisateur et la gestion de la disponibilité des réservations.

## Conclusion

Ce programme C offre un système simple de réservation de bus avec des fonctionnalités distinctes pour les clients et les administrateurs. Son interface basée sur un menu permet une interaction facile pour effectuer diverses opérations liées aux réservations de bus.

## note
- pour acceder les fonctions d'administrateur utiliser le mot (admin) comme nom d'utilisateur et mot de passe.
- l'affichage des voyageurs s'effectue pour chaque session d'ouverture de programme c'est t'a dire que toute les 
  reservations effectuer dans une session leur voageur sera ajouter a la liste des voyageurs de cette session 
  stockee dans le memoire et non le disque donc ce liste sera vide chaque fois le programme est fermee.