---
layout: default
title: Article – Mon stage à la mairie
date: 2026-06-21
---

# Mon stage à la mairie : découverte de Publik

**Publié :** 21 juin 2026 | **Temps de lecture :** 5 min

---

## Introduction

Durant mon stage à la mairie, j’ai travaillé avec le gestionnaire de la plateforme informatique. Mon rôle a principalement consisté à créer, modifier et améliorer différents formulaires utilisés par les usagers et les agents.  
J’ai passé plusieurs semaines à découvrir Publik, à comprendre son fonctionnement, et à répondre aux demandes des services en adaptant les formulaires existants ou en en créant de nouveaux.

Ce stage m’a permis d’apprendre énormément, autant sur l’outil que sur la logique derrière les workflows, les sources de données, les conditions et tout ce qui permet de rendre un service en ligne réellement fonctionnel.

---

## Mes missions principales

### Création et modification de formulaires

Dès la première semaine, j’ai travaillé sur plusieurs formulaires, comme :

- un formulaire de prise de rendez‑vous pour différentes permanences ;
- un questionnaire destiné à recueillir des retours d’établissements sur des activités nautiques ;
- un formulaire permettant aux entreprises de faire des pré‑demandes pour un évènement ;
- la numérisation complète d’un cahier de transmission ;
- des formulaires pour les abonnements piscines, la relance de factures ou le signalement d’anomalies.

Chaque formulaire avait ses particularités, et j’ai dû apprendre à utiliser les champs, les blocs, les sources de données, les conditions en JSON, les workflows, et tout ce qui permet de structurer une démarche en ligne.

### Utilisation de Publik

Publik était un outil totalement nouveau pour moi. J’ai appris à :

- créer des champs (texte, listes, numériques, fichiers, etc.) ;
- construire des blocs réutilisables ;
- manipuler des sources de données ressemblant à des dictionnaires JSON ;
- écrire des conditions pour afficher ou masquer des champs ;
- utiliser des filtres comme |multiply, |subtract, |is_working_day, |safe, etc. ;
- créer ou modifier des workflows pour gérer les statuts, les courriels, les documents générés, ou encore les actions automatiques.

J’ai aussi découvert la syntaxe particulière de Publik, qui ne fonctionne pas comme Python ou d’autres langages que j’avais déjà utilisés. Il fallait donc être très précis, surtout pour les blocs {% raw %}{% if %}{% endraw %} et {% raw %}{% with %}{% endraw %}.

---

## Quelques réalisations marquantes

### Le cahier de transmission

J’ai entièrement numérisé un cahier de transmission utilisé par les professionnels.  
Il permet maintenant :

- d’écrire un message via un formulaire
- de créer automatiquement une fiche associée
- d’ajouter des fichiers
- de trier et filtrer les messages
- de modifier ou supprimer une fiche existante
- de gérer l’expiration automatique grâce à un workflow qui vérifie toutes les 10 minutes si une fiche doit être supprimée.

### Le formulaire de réservation de contenants réemployables

Ce formulaire a été l’un des plus complexes.  
J’ai dû :

- rendre la liste des contenants extensible
- afficher les images et descriptions
- remplacer un champ numérique par une liste « nombre d’unités – prix »
- créer une deuxième page affichant le total calculé automatiquement
- gérer les dates avec la condition |is_working_day
- permettre la duplication du bloc pour réserver plusieurs contenants

### Les abonnements piscines

J’ai créé un formulaire complet permettant aux usagers de s’abonner aux piscines communautaires.  
Il inclut :

- des champs préremplis si l’usager est connecté
- une adresse en autocomplétion
- un choix d’abonnement avec description affichée via |safe
- des données calculées selon la date, le type d’engagement et le prix
- la création d’un panier pour permettre le paiement en ligne

---

## Difficultés rencontrées

J’ai rencontré plusieurs difficultés, notamment :

- la syntaxe stricte de Publik
- la découverte du JSON
- les liaisons dans les workflows
- la recherche des bonnes sources de données
- la création de documents automatiques (comme les conventions)
- les conditions complexes pour les calculs ou les validations

Pour les surmonter, je me suis appuyé sur :

- la documentation officielle
- les projets déjà existants
- les conseils de mon tuteur
- beaucoup de tests et d’essais

---

## Ce que j’ai appris

Ce stage m’a permis de :

- comprendre en profondeur le fonctionnement de Publik
- apprendre à structurer des formulaires complexes
- manipuler des workflows et des données dynamiques
- améliorer ma logique et ma rigueur
- travailler en autonomie tout en répondant à des demandes réelles
- participer à l’évolution d’un service en ligne utilisé quotidiennement

---

## Conclusion

Ce stage a été très formateur. J’ai pu découvrir un outil complet, apprendre à gérer des formulaires avancés, comprendre les workflows, et surtout répondre à des besoins concrets de la mairie.  
Chaque semaine m’a permis de progresser, de comprendre de nouvelles choses et de gagner en autonomie.

---

[← Retour aux articles](./articles.md)
