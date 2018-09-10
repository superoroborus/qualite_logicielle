# Qualité logicielle

## Objectif du cours : 

* Fournir une culture générale autour de la qualité et du test
* Identifier quels sont les critères qualités d'un logiciel.
* Identifier les différents types de tests et d'action à mettre en place pour amélirer la qualité d'un logiciel.
* Pouvoir mettre en place des processus de qualité sur ses projets

## Introduction

Nous allons détailler les raisons pour lesquelles la qualité est au coeur du développement logiciel et a induit un certain nombre de processus, de méthodes mais également de certifications.

**Le logiciel est partout**

Ce n'est pas nouveau, le logiciel prend une part de plus en plus importante dans nos vie que ce soit pour réserver un billet de train, faire décoller une fusée ou permettre d'envoyer Yo à ses potes, on développe du logiciel. Des pans entiers de nos vies dépendent donc du bon fonctionnement de ceux ci.

**Le logiciel est développé par des humains...**

Et les humains sont faillibles, donc le logiciel est faillible. Les failles d'un développeur peuvent être de différentes nature :

* Manque de connaissance 
* Confusion dans la lecture du code
* Pression du temps
* Pression de l'argent (souvent lié)

**D'où un rôle de plus en plus important de la qualité dans le logiciel**

### Quelles sont les raisons qui nous pousse à tester... ou pas.

Si on se réfère à ce que l'on vient de dire, il apparait donc important d'investir sur la qualité d'un logiciel. Alors pourquoi ne fait on pas que ça?

Il faut néanmoins se rappeler que la qualité à un cout, faire des tests prend du temps et ce coût est, bien entendu, à mettre en rapport à le coût de la non-qualité. 

Quand on investi trop dans la qualité par rapport à ce que l'on devrait on parle alors de surqualité. 

### La qualité en tant que métier.

Au cours de votre carrière, vous serez amener à faire vous même du test, à participer, en tant que développeur, à la qualité. Il faut savoir aussi qu'il s'agit d'un métier, d'une carrière que vous pouvez embrasser.

Nous allons voir, dans le chapitre suivant, quelques compléments sur le test et le métier de testeur.

## Le test et le testeur

### Qu'est ce qu'un testeur

Son rôle est de trouver des bugs, un bug étant un défaut produit dans un logiciel, un système ou un document, par l'erreur d'un être humain qui peut entrainer une défaillance. Le testeur a aussi pour rôle de préparer et d'écire des cas de test à partir deséléments dont il dispose. Le plus important, pour lui, est de savoir ce qui fait qu'un test passe ou échoue. 

Il peut s'agir d'un membre identifié d'une équipe, d'un développeur, d'un service tiers ou du client...

Il existe, et ceci afin que les différentes entreprises informatiques voulant parler le même langage puisse, un organisme de certification international : ISTQB.

### Les principes du test

* Les tests montrent la présence de défauts
* Les tests exhaustifs sont impossibles
* Tester tôt
* Regroupement des défauts
* Paradoxe du pesticide
* Les tests dépendent du contexte
* L'illusion de l'absence d'erreurs

### Les niveaux de tests

L'ISTQB en définit 4 :
* Composant
* Intégration
* Système
* Acceptance



## Quoi faire pour améliorer la qualité de développement

### Suivre une méthodologie agile (et la suivre bien)

* Scrum
* eXtreme Programming

Cf. Annexe pour les détails

### Adopter des standards

Pour de nombreuses raisons, il est utile d'adopter et de suivre des standards de développement. quelque soit le langage que vous utilisiez, des normes ont été émises pour définir les crtières d'écriture de code, de formatage des commentaires, de définition des interfaces. En PHP on a, par exemple, les PSR : PHP Standards Recommendations.

Suivre des standards ou en définir pour son équipe permet à tout le monde d'écrire les choses de la même manière. Cela permet de faciliter la lecture du code. 

Il est important, quand on intégre une équipe, de se renseigner sur les standards adoptés. 

A noter qu'il existe aussi des standards ou des référentiels sur des sujets qui nne sont pas lié au code particuliérement comme des stadards d'accessibilité ou d'ergonomie qu'il est bon de connaitre quand on fait, par exemple, du développement front.

### Pratiquer la Revue 

La revue est un processus mis en place au sein des équipes de développement qui consiste à faire relire son code par un autre membre de l'équipe. Le processus peut-être plus ou moins formel et intégré dans le processus de développement.

A noter qu'on peut faire des revues sur tout : 
* Du code (bien entendu)
* De la documentation (maquette, spécfications, documentation client et développeur)
* Des éléments de développement (User Story)
* De la base de données (Schéma)

Exemple : la pull request 

Conseil pour les développeurs solitaires : Si vous n'avez pas de relecteur sous la main, vous pouvez vous même être votre propre relecteur. Je vous conseille de laisser un peu de temps entre votre dernier commit et votre relecture (Par exemple : une nuit). De même pensez à l'option -p (patch) de git quand vous faites un git add qui vous permet de choisir quoi ajouter à votre commit, ligne par ligne.

### Programmer en binôme

Le pair programming (ou programmation en binôme) consiste à executer une tâche de développement à deux. Les deux développeurs travaillent en même temps sur la tâche, partagent les connaissances et produisent du code à travers une conversation entre eux. 

Il existe des méthodes plus ou moins formel de pair programming. On peut définir un *pilote* (celui qui est aux commandes, donc au clavier) et un *navigateur* (celui qui détient la vision plus large, qui s'assure que le développement rentre dans le contexte plus large de l'application.

L'inconvénient de cette méthode est qu'elle va impliquer le temps de deux personnes, mais les gains en connaissance compensent la perte de temps potentielle. Souvent, dans les entreprises, on réserve cette pratique à des cas bien particulier dans le développement (démarrage d'un projet, mise en place d'un POC...)

### Adopter le pilotage du développement par les tests 

*J'aimerais bien vivre en Théorie, car en Théorie tout se passe bien.*

Avant toute chose, il convient de rappeler ce qu'est le test unitaire : le test unitaire  est une procédure permettant de vérifier le bon fonctionnement d'un composant (voir plus haut)


### Automatiser l'exécution des tests

### Livrer réguliérement

Pour ces deux points, nous verrons plus loin que ces bonnes pratiques sont facilités par la mise en place d'une plateforme d'intégration continue.


## Outils

Il est important ici d'identifier quelques familles d'outils que l'on va retrouver quelque soit le langage que l'on utilise.

### Système de gestion de version

* git (à ne pas confondre avec github).
* github (à ne pas confondre avec git)

### Les linters

### Les outils de statistiques

### Les framework de test

### Les outils de déploiement

### Les plateformes d'intégration continue

## Exercices :

### Le jeu des sept erreurs : 

Repérer, dans un listing, des erreurs courantes. Cet exercice à pour but d'affiner vos compétences lors des revues. 

Les erreurs peuvent être les suivantes :

* [ ] Problème d'indentation
* [ ] Erreur de code
* [ ] Assignation incorrecte
* [ ] Code mort

Il est aussi possible de trouver des améliorations : 

* [ ] Suppression de code
* [ ] Optimisation

### 99 luftballons


## Ouverture sur le prochain cours
