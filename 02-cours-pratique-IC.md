# Mise en place d'une intégration continue dans un projet

# L'évolution du logiciel

Par le passé, des développeurs ont estimés que le traditionnel développement en cascade n'était plus adapté aux contraintes de développement actuelle. On retrouve ce constat dans plusieurs méthodes et manifeste

## Le Manifeste agile

* Les individus et leurs interactions plus que les processus et les outils
* Des logiciels opérationnels plus qu’une documentation exhaustive
* La collaboration avec les clients plus que la négociation contractuelle
* L’adaptation au changement plus que le suivi d’un plan

## L'eXtreme Programming :

### Valeurs : 

* Communication
* Simplicité
* Feedback
* Courage
* Respect

### Pratiques

* Client sur site
* Planning Poker
* Intégration continue
* Petites livraisons
* Rythme soutenable
* Tests de recettes (ou tests fonctionnels)
* Tests unitaires
* Conception Simple
* Utilisation de métaphores
* Refactoring
* Appropriation collective du code
* Convention de nommage
* Programmation en binôme

# Description de l'intégration continue

L'intégration continue permet à la fois de vérifier qu'un code fonctionne, correspond à des standards définis et peut également permettre de déployer le code. 

L'objectif d'une plateforme d'intégration continue est, au quotidien, de détecter les défauts d'intégration tôt et rapidement.

Mettre en place un outil d'intégration continuer est une bonne pratique à adopter quelque soit la taille de votre projet. 


## Activitées d'une plateforme d'intégration continue

Une plateforme d'intégration continue permet les activités suivantes : 

* Analyse statique du code
* Compilation du code 
* Éxecution des tests unitaires
* Déploiement du build dans un environnement de tests
* Publication du statut des activités dans un endroit visible par l'équipe.

## Liste d'outils 

* Jenkins : Un grand classique de l'intégration continue.

* Circle CI.

## A ne pas confondre 

Des outils de de QA tels qu'une framework de tests unitaire ou un linter. L'outil d'intégration continue utilise ces outils.

Avec un outil de déploiement (exemple codeship)

# Votre premier déploiement


