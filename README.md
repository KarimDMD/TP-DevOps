# Tic-Tac-Toe

Ce repository contient le projet Tic-Tac-Toe, qui a été cloné depuis un repository existant dans le cadre d'un travail pratique. L'objectif principal de ce TP était de mettre en place un environnement de développement à l'aide d'un docker-compose et de créer une pipeline d'intégration et de déploiement avec Jenkins.

## Objectif du TP

Le TP avait pour objectif de mettre en pratique les connaissances en gestion de projet logiciel, en CI/CD et en tests automatisés en réalisant les tâches suivantes :

- Préparer son environnement en utilisant le docker-compose disponible sur le repository docker-gitlab-jenkins.
- Récupérer le projet en local et le cloner depuis un repository existant.
- Mettre en place le projet sur le GitLab local avec un nom formaté selon les consignes données.
- Créer une pipeline d'intégration et de déploiement avec Jenkins, en respectant un schéma spécifique.
- S'assurer que la pipeline puisse être exécutée manuellement et à chaque action de push et de merge request.
- Configurer la pipeline pour exécuter les tests automatiques et fournir un rapport de couverture Clover.
- Produire les artefacts de distribution nécessaires au déploiement.
- Corriger les tests non-validés par la pipeline afin qu'ils soient valides.

## Technologies utilisées

- Jest : Framework de test utilisé pour écrire et exécuter des tests unitaires.
- Docker : Utilisé pour la gestion des conteneurs et la mise en place de l'environnement de développement.
- Jenkins : Utilisé comme plateforme d'intégration continue pour automatiser les tests et le déploiement.

## Environnement de développement

Le projet est basé sur un docker-compose disponible sur le repository docker-gitlab-jenkins. Cet environnement permet de créer un environnement isolé et reproductible pour le développement du jeu.

## Pipeline d'intégration et de déploiement (CI/CD)

Une pipeline d'intégration et de déploiement a été mise en place avec Jenkins. Cette pipeline est configurée pour être exécutée manuellement et à chaque action de push et de merge request sur le repository.

### Contenu de la pipeline

- La pipeline exécute les tests automatiques pour garantir la qualité du code.
- Un rapport de couverture Clover est généré pour évaluer la couverture des tests.
- Les artefacts de distribution nécessaires au déploiement sont produits.

## Workflow Git

Le workflow Git utilisé pour ce projet suit un modèle de feature branching. Chaque nouvelle fonctionnalité est développée dans une branche dédiée, puis fusionnée dans la branche principale (main) via une pull request après validation.

