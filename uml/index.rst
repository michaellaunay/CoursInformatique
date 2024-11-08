.. -*- coding: utf-8 -*-

================
Modélisation UML
================

Objectifs
=========

Connaitre les bases de la notation UML.

Savoir
======

- Les différents diagrammes,
- La représentation des classes, attributs, méthodes, associations,
- La représentation des objets, des composants, des collaborations, des flux
  d'informations.

Pour réaliser l'analyse et générer les composants nécessaires à Plone nous
allons utiliser l'outil ArchGenXML en version 2.

Nous réaliserons dans un premier temps un diagramme de classes, qui permettra
de décrire le plan documentaire de notre application, puis nous associerons à
nos documents des "workflows" sous forme de diagramme d'états transitions.

Mais avant cela nous allons réaliser un bref rappel des notions UML utilisées
dans la suite.

Qu'est ce qu'UML
================

.. glossary::

  UML
    UML (Unified Modeling Language) est une notation graphique qui permet de
    traduire sous forme de vues l'architecture d'un logiciel ou d'une
    application orientée objet.

UML est la fusion de différentes notations issues des méthodes de génie
logiciel orienté objet antérieures aux années 1995. La version 1.0 a
officiellement été publiée en 1997 par l'OMG (Object Management Group) qui est
l'organisme responsable de sa standardisation. Depuis 2007, la version
officielle est la 2.5.

Historiquement, son usage intervenait dans la phase de conception pour permettre
de "visualiser" ce que sera et fera le logiciel. Comme les feuillets des plans
d'un architecte en bâtiment, différents diagrammes composent une vue spécifique
de la solution apportée au problème.

Le lecteur doit parcourir plusieurs vues et donc lire plusieurs diagrammes pour
se créer son image mentale du logiciel.

Cette abstraction n'est malheureusement pas évitable, puisque un logiciel est
composé à la fois de parties statiques, telle que le code exécutable, de données
dynamiques telles que les entrées sorties, et de comportements.

Les vues sont des regroupements abstraits des diagrammes qui sont eux les
"dessins" représentant les interactions entre les éléments constitutifs du
logiciel. Ces diagrammes permettent de visualiser l'interaction entre les
éléments de l'architecture qui sont regroupés dans un "modèles d'éléments" et
constitués des cas d'utilisations, classes, associations, attributs, etc.

Actuellement, les courants de l'IDM (Ingénierie Dirigée par les Modèles), font
que son usage est présent tout au long du cycle de vie du logiciel, et l'on met
à jour le logiciel en modifiant le modèle puis en générant à nouveau
l'application. Les outils de génération se chargent de fusionner l'existant avec
les nouvelles fonctionnalités.

Initialement, la conception orientée objet cherchait à résoudre un problème en le
découpant non pas en un ensemble de fonctionnalités dont le tout forme un arbre
ayant pour racine une fonction "main", mais en boites travaillant ensemble par
l'échange de messages et dont le comportement global réalise la tâche attendue.

La description de ces boites forme un tout homogène de données et de fonctions
appelée interface, c'est une abstraction.

La définition d'un type de boite respectant une interface donnée est nommée
"classe" si elle est simple, et composant si pour respecter le contrat de
l'interface elle encapsule la collaboration de plusieurs classes et peut à elle
seule être considérée comme une application.

L'exécution d'une classe est appelée instance, elle possède alors ses propres
valeurs d'attributs à commencer par son occupation mémoire ce qui la distingue
des autres instances de la même classe.

Mais revenons à UML.

UML se base sur trois types de briques pour permettre la modélisation d'une
architecture :

- Les éléments, qui sont un peu le vocabulaire de UML ;
- Les relations, qui représentent la syntaxe du projet ;
- Les diagrammes, qui contiennent la sémantique du projet.

Les éléments
============

Nous n'allons détailler ici que les éléments d'UML que nous utiliserons.

Les éléments structurels
************************

La classe
+++++++++

C'est un types d'éléments qui partagent les mêmes propriétés (attributs,
méthodes, relations, sémantique).

Si les propriétés définies par la classe sont immuables et ne dépendent pas des
éléments, on parle d'attributs ou de variables de classe et de méthodes de
classes, inversement si leur contenu dépend de l'élément on parle d'attribut ou de
variable d'instances et de méthodes.

Les propriétés d'une classe ont une visibilité, c'est-à-dire que l'accès aux
propriétés d'une classe par une autre est contrôlé.

.. figure:: uml_repr_classe.jpg
    :align: center

    Représentation des classes

L'interface
+++++++++++

C'est un ensemble de méthodes qui définissent le comportement attendu d'une
classe en laissant aux classes issues de cette interface de choisir
l'implémentation.

.. figure:: uml_repr_interface.jpg
    :align: center

    Représentation des interfaces

L'objet
+++++++

C'est un élément concret actif ou passif appartenant à une classe.
Si la classe de l'objet est connue, on parle alors d'instance de cette classe.
L'objet possède toutes les propriétés de sa classe et définie les valeurs des
attributs d'instances.

.. figure:: uml_repr_objet.jpg
    :align: center

    Représentation des objets

L'acteur
++++++++

C'est une classe externe au système agissant ou réagissant au système.

Ainsi tous les intervenants sur le système sont des acteurs.

.. figure:: uml_repr_acteur.jpg
    :align: center

    Représentation des acteurs

Le composant
++++++++++++

C'est une classe formant un tout cohérent et suffisant permettant de réaliser
un ensemble de fonctionnalités, c'est la boite noire par excellence.

.. figure:: uml_repr_composant.jpg
    :align: center

    Représentation des composants

La collaboration
++++++++++++++++

Lorsque plusieurs instances de classes réalisent un comportement global par
échange de messages, on dit qu'ils forment une collaboration et que les objets y
remplissent un rôle.

La collaboration permet donc de visualiser la réalisation des exigences
fonctionnelles.

.. figure:: uml_repr_collaboration.jpg
    :align: center

    Représentation des collaborations

Le cas d'utilisation
++++++++++++++++++++

C'est un comportement du système dont est témoin un acteur, il est réalisé par
des collaborations.

.. figure:: uml_repr_cas_d_utilisation.jpg
    :align: center

    Représentation des cas d'utilisations

Les éléments comportementaux
****************************

Les interactions
++++++++++++++++

Elles sont constituées par l'envoi de messages ou d'événements provoquant des
actions chez le récepteur.

L'appel d'une méthode de classe correspond à l'envoi d'un message dont le nom
est suivi de parenthèses.

.. figure:: uml_repr_messages.jpg
    :align: center

    Représentation des messages

Les états
+++++++++

Ils permettent de constituer des automates décrivant le comportement d'une
classe ou d'une méthode.

.. figure:: uml_repr_etat.jpg
    :align: center

    Représentation des états dans un diagramme d'états

Les activités
+++++++++++++

Les activités sont des comportements exécutables séquentiellement ou
parallèlement.

.. figure:: uml_repr_activites.jpg
    :align: center

    Représentation des activités dans un diagramme d'activités


Les éléments de regroupement
****************************

Les paquetages
++++++++++++++

Ils permettent de ranger les classes et diagrammes de façon à rendre plus clair
le modèle.

.. figure:: uml_repr_paquetages.jpg
    :align: center

    Représentation des paquetages

Les éléments d'annotation
+++++++++++++++++++++++++

Les notes permettent de donner des informations.

.. figure:: uml_repr_notes.jpg
    :align: center

    Représentation des notes

Les relations
=============

La dépendance
*************

C'est une relation sémantique indiquant que tout changement de l'élément
indépendant peut affecter l'élément dépendant.

.. figure:: uml_repr_dependance.jpg
    :align: center

    Représentation des dépendances

L'association
*************

Elle permet d'indiquer une relation entre deux éléments.

La nature de la relation est donnée par le texte situé dessus. Un lien peut être
précisé aux extrémités par le nombre et le rôle de chacun des éléments.

Un lien de contenance est symbolisé par l'agrégation.

.. figure:: uml_repr_associations.jpg
    :align: center

    Représentation des associations


La généralisation
*****************

Cette relation permet de définir des niveaux d'abstraction entre les classes, le
but est de permettre de manipuler de façon homogène des ensembles d'objets qui
partagent les mêmes propriétés. Cette factorisation des traitements s'appelle le
polymorphisme.

.. figure:: uml_repr_generalisation.jpg
    :align: center

    Représentation des généralisations

La réalisation
**************

Cette relation indique que la classe implémente les comportements définis dans
l'interface qu'elle réalise.

.. figure:: uml_repr_realisations.jpg
    :align: center

    Représentation des réalisations

La transition
*************

Cette relation joint deux états et permet d'expliciter les conditions à
respecter et les traitements à réaliser lors des changements d'états.

Les diagrammes que nous utiliserons
===================================

Alors que UML permet de créer 13 types de diagrammes nous n'allons n'en utiliser
que trois pour la génération de notre produit. Les autres diagrammes servirons à
la documentation de notre architecture.

Les diagrammes qui servirons à la génération sont :

 - Le diagramme de classes
 - Le diagramme d'états transitions
 - Le diagramme d'activités

Le diagramme de classes
***********************

Ce diagramme permet de mettre en évidence la structure des classes c'est-à-dire
les attributs et méthodes présents dans les classes, les relations entre classes.

Ainsi, il fait apparaitre les hiérarchies de classes (héritage, abstraction,
interface), les compositions et agrégations (un instance d'une classe contenant
des instances d'autres classes), les dépendances, les "packages".

Par convention on limite le nombre de classes visibles dans un diagramme de
classes. On va alors réaliser différents diagrammes de classes qui chacun doit
montrer un aspect du problème en n'affichant que les attributs, méthodes et
associations concernés par cet aspect.

.. figure:: uml_repr_diagramme_classes.jpg
    :align: center

    Diagramme de classes

Le diagramme d'objets
*********************

Il regroupe les objets et permet de les représenter avec leur liens à un moment
donné.

.. figure:: uml_repr_diagramme_objets.jpg
    :align: center

    Diagramme d'objets


Le diagramme de cas d'utilisation
*********************************

Il regroupe les cas d'utilisations et les acteurs concernés.

.. figure:: uml_repr_diagramme_cas_utilisations.jpg
    :align: center

    Diagramme de cas d'utilisations

Le diagramme de séquence
************************

Il permet de visualiser l'enchainement des messages entre objets. L'ordre de
lecture est de haut en bas.

.. figure:: uml_repr_diagramme_sequences.jpg
    :align: center

    Diagramme de séquences

Le diagramme de collaboration
*****************************

C'est une représentation symétrique du diagramme de séquence.

Le diagramme d'états transitions
********************************

Il est utilisé pour modéliser les changements d'états d'un élément.

Nous l'utiliserons pour modéliser les workflows de nos types de contenu.

Le diagramme d'activités
************************

Il permet de voir l'enchainement des tâches du système ou des traitements
déclenchés par les acteurs.

Le diagramme de composants
**************************

Il montre les liens entre composants.

Le diagramme de déploiement
***************************

Il permet de voir l'intégration.
