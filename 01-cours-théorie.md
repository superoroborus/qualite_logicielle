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

### Rappel
L'origine des bugs : Il sagit d'une erreur humaine qui entraine un défaut (ou bug) qui cause une défaillance. 

### Qu'est ce qu'un testeur

Le testeur, dans un projet, à la charge d'assurer de la fiabilité du logiciel, pour cela plusieurs tâches lui incombe : travail de préparation, implémentation et exécution des tests puis evaluation et reporting. Nous allons détailler ces étapes un peu plus loin. Selon les tailles d'équipe il peut aussi avoir la charge de planification des campagnes de tests, un contrôle sur l'avancement des tests et une cloture pour valider (ou non) qu'un logiciel est suffisamment fiable pour être déployé. 

Il peut s'agir d'un membre identifié d'une équipe, d'un développeur, d'un service tiers ou du client...

#### Être un testeur certifié 

Il existe, et ceci afin que les différentes entreprises informatiques voulant parler le même langage puisse, un organisme de certification international : ISTQB.

### Les travaux du testeur

#### Analyse et conception 
 
Il s'agit d'un travail d'analyse bien souvent. A partir du matériel mis à disposition (specifications, user story, code existant) le testeur va établir des oracles de test, c'est à dire des éléments pour déterminer ce qui fait que les tests passent ou échouent. Cette phase permet déjà de relever des éventuels incohérences ou imprécisions.

**Exemple** : 

*Je veux que mon application de calcul de taux d'intérêt applique un pourcentage de 2% si le solde est supérieur à 100€ et de 1% si le solde est inférieur à 100 €* : Quel est la question que le testeur doit poser pour lever une éventuel imprécision ?

#### Implémentation et execution 

Il s'agit là de la partie effective, qui consiste a automatiser les tests, les arranger sous forme de suite et les exécuter en fonction de priroités définies à l'étape précédente. Pour ça on découpe souvent ceci en campagne. Nous verrons dans le chapitre suivant un focus sur les différents niveaux de test. Il arrive 

#### Evaluation et Reporting 

Le but de cette phase est de fournir un retour et une visibilité sur les activités de test. Ce reporting peut-être fait de manière manuelle mais aussi automatique. Elle permet de savoir ce qui s'est passé lors d'une campagne de test :

* Le nombre de tests excutés.
* Le nombre d'échecs et de réussites.
* Les informations sur les défauts.
* La couverture, par les tests des exigences, des risques ou du code.

#### Exercices 

Dans l'exemple suivant, quel est le nombre minimu de cas de test nécessaires pour obtenir une couverture de 100% de couverture?

```
   Reduction = 0
   Quantite = 0
   Read Quantite
   If Quantite >= 20 then
      Reduction = 0.05
      If Quantite >= 100
         Reduction = 0.1
      End If
   End If
```

### Les niveaux de tests

On compte quatre niveaux de test (je me réfère ici aux définitions de l'ISTQB)

* Composant
* Intégration
* Système
* Acceptance

Si on détaille ces différents niveaux : 

#### Composant 

Traditionnellement on parle de test unitaire. Il s'agit des tests du développeur. Cette partie permet de tester le fonctionnement interne des composant.

#### Intégration

Les tests d'intégration permettent de tester les interfaces entre les composants. Pour cela on fait appel, bien souvent, à des mocks. Cette partie permet d'isoler les défauts liés à un compoant en particulier.

#### Système

Les tests système vont valider le fonctionnement du logiciel dans son ensemble. 

#### Acceptation

Les tests d'acceptation dont des tests de haut niveau permettant de vérifier si les fonctionnalités du logiciel correspondent aux attentes du client et si le système est utilisable.

#### A retenir

* Plus un bug est trouvé tôt, moins il est couteux à corriger.
* Les tests sont automatisable à tout niveau
* Un test non executé ne sert à rien
* Les bons tests échouent

### En complément : 

#### Les principes du test

* Les tests montrent la présence de défauts
* Les tests exhaustifs sont impossibles
* Tester tôt
* Regroupement des défauts
* Paradoxe du pesticide
* Les tests dépendent du contexte
* L'illusion de l'absence d'erreurs

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

Avant toute chose, il convient de rappeler ce qu'est le test unitaire : le test unitaire  est une procédure permettant de vérifier le bon fonctionnement d'un composant (voir plus haut). Adopter le pilotage par les tests consiste à travailler de la manière suivante : 

* Démarrer sa tache de développement par l'écriture d'un test qui échoue
* Écrivez le code pour que le test passe
* Vérifier que le code passe
* Restructurer votre code et automatisez le trest

Pour s'entrainer à ça, je conseille de faire régulièrement des katas (ce sera fait dans la suite de votre formation). Adopter le développement piloter par les tests (TDD) permet d'obtenir, très rapidement, une bonne couverture des composants. L'automatisation et l'execution des tests permettra de détecter rapidement des régression dans votre code.

### Automatiser l'exécution des tests

Comme indiquer dans le chapitre précédent, une bonne pratique consiste à automatiser l'exécution des tests. Je rappelle qu'un test non joué est un test inutile qui, en plus risque de ne plus être pertinent quand il sera rejoué.

Il existe plusieurs possibilités en matière d'automatisation selon le niveau de test ou la criticité de l'application ou de la durée d'execution des tests. Il est possible d'executer les tests soit de manière régulière, soit lors d'un événement comme par exemple un commit sur le dépot.

### Livrer réguliérement

Pour ces deux points, nous verrons plus loin que ces bonnes pratiques sont facilités par la mise en place d'une plateforme d'intégration continue.

## Outils

Il est important ici d'identifier quelques familles d'outils que l'on va retrouver quelque soit le langage que l'on utilise.

### Système de gestion de version

* git (à ne pas confondre avec github).
* github (à ne pas confondre avec git)

### Les VMs et Conteneurs 

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
