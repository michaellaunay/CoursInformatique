L'Ingénierie logicielle repose sur l'art de concevoir des logiciels et
d'améliorer la façon de les concevoir (l'ingénieur cherche à optimiser
ses processus de travail).

Depuis près de 10 000 ans (c.f mégalithes de [Gobekli
Tepe](https://fr.wikipedia.org/wiki/Göbekli_Tepe) ) les très grands
projets témoignent d'un sens de l'organisation, d'abord pour la
construction des bâtiments et des navires (voir les découvertes de 2013
de l'équipe de [Pierre
Tallet](https://fr.wikipedia.org/wiki/Pierre_Tallet) décrite dans « Les
papyrus de la Mer Rouge I, le journal de Merer (papyrus Jarf A et B) »
), et maintenant pour les œuvres immatérielles comme les films ou les
logiciels . Ces activités soulignent ce que l'on sait depuis fort
longtemps :

Il n'y a pas de grand projet sans une organisation rigoureuse des
processus et des équipes.

Pourtant une majorité des projets informatiques sont en échec à savoir
que soit les budgets sont dépassés, soit ce sont les délais, et très
souvent les deux.

L'une des premières causes est la mauvaise compréhension du besoin.

Le « client » vient avec une envie et il est du devoir de l'ingénieur de
détecter le besoin pour d'abord satisfaire celui-ci.

On peut illustrer cette obligation par la métaphore suivante :

Une personne rentre dans une concession automobile, le commercial qui
l'aborde lui demande s'il a besoin d'une information. La personne perçue
comme un prospect aux yeux du commercial annonce qu'il souhaiterait
s'offrir la dernière sportive de la marque. Il énonce ici une envie. Le
commercial lui demande alors de lui décrire l'usage qu'il en fera, et
lui fait formuler différents scénarios. En l'interrogeant, il arrive à
détermine son besoin, qui dans cet exemple sont de se transporter de
chez lui à son travail lors des heures de pointe et de temps à autre de
sortir le weekend à la plage avec sa famille de deux enfants, d'ailleurs
sa femme prendra le véhicule au moins trois fois par semaine, car ils
n'auront qu'une voiture. Après avoir sollicité habilement son prospect,
le commercial dirige son presque client vers une familiale hybride,
automatique et élégante de façon à satisfaire le besoin et ménager
l'envie. Il y gagne un client qui reviendra, car celui-ci aura
l'impression d'avoir été écouté, puisque son besoin aura été satisfait
tout autant que son envie. Si le commercial n'avait su identifier le
besoin, la vente se serait conclue, mais peu de temps après le client
aurait été insatisfait et ne serait jamais revenu.

Il est du rôle de l'ingénieur d'interroger ses clients pour trouver le
besoin derrière l'envie, mais également de rapidement comprendre le
contexte et pour cela d'interroger un échantillon représentatif des
différents rôles tenus par les futurs utilisateurs, car comme dans le
film « [Répétition
d'orchestre](https://fr.wikipedia.org/wiki/Répétition_d%27orchestre) »
de Fellini, chaque protagoniste ne voit que son travail et n'a pas la
vue d'ensemble permettant de comprendre le processus que viendra aider
le logiciel développé.

[L'élicitation](https://hal.inria.fr/inria-00098954/) des besoins est
l'art de faire dire au client toutes les informations nécessaires au
projet.

Projet exemple
==============

L\'association CultureDiffusion souhaite réaliser une bibliothèque
numérique à gestion décentralisée.

Le principe est de permettre à chaque membre de numériser les œuvres et
aux bibliothécaires de les proposer à l\'emprunt selon deux modalités.

Toutes les œuvres du domaine public sont accessibles gratuitement,
toutes les œuvres sous droits sont proposées en location pour une
période de 2 semaines.

Lorsqu\'une œuvre passe dans le domaine public, elle devient accessible
gratuitement et est diffusée aux membres ayant accordé à l\'application
suffisamment d\'espace disque.

Chaque membre de la bibliothèque peut emprunter ou louer une œuvre.

Chaque membre peut proposer une œuvre et ainsi enrichir la bibliothèque.

Chaque œuvre est constituée d\'un fichier contenant l\'œuvre et d\'un
fichier au format json contenant les informations sur l\'œuvre.

L\'application bibliothèque possède un index des œuvres qui est mis à
jour à chaque ajout ou suppression d\'œuvre.

L\'application possède quatre rubriques proposées sous forme de
répertoires.

Un répertoire \"fond\_commun\" avec une partie des œuvres libres de
droits de l\'association.

Un répertoire \"emprunts\" avec les œuvres sous droit empruntées par le
membre qui sont chiffrées avec sa clé.

Un répertoire \"séquestre\" avec une partie des œuvres sous droit gérée
par l\'association, tous les fichiers y sont chiffrés, l\'index n\'y est
pas accessible de façon directe.

Un répertoire \"à modérer\" avec les œuvres que le membre a proposées.

Lorsqu\'une œuvre est proposée par un membre, elle est soumise à
modération.

Les bibliothécaires voient les œuvres soumises, vérifient et complètent
les données telles que les auteurs, éditeur, langue, pays d\'origine,
date de publication, droits, catégorie de l\'œuvre, format du support,
puis ils décident du statut de l\'œuvre et donc si elle est dans le
domaine public ou non, ou si elle est rejetée.

Selon le statut de l\'œuvre modérée, l\'application range dans la bonne
rubrique et gère les droits d\'accès.

Si l\'œuvre est dans le domaine public il peut y en avoir autant de
copie qu\'il y a de membre.

Si l\'œuvre est protégée alors il ne peut y avoir que 3 fois plus de
copies que de licence d\'exploitation, et chaque œuvre est chiffrée par
une clé différente ayant une date de validité.

À la fin de la validité d\'un emprunt, l\'application bibliothèque
supprime automatiquement l\'œuvre du répertoire du membre.

Les œuvres sont classées selon les types et sous-types suivants :

Article

Livre :

BD

Enfants

Romans

Livre technique

Education

Loisir

Culture

Sante

etc

Musique :

Classique

Jazz/Funk/Soul

Pop

Metal

etc

Vidéos :

SF

Histoire

Série

Documentaire

etc

Certaines œuvres appartiennent à plusieurs catégories en même temps.

On utilisera PlantUML.

Réalisez le glossaire.

Réalisez le diagramme de cas d\'utilisations.

Listez les scénarios de l\'application, ajouter ceux fondamentaux
n\'apparaissant pas dans le cahier des charges.

Triez les scénarios par ordre d\'importance.

Réalisez les 4 diagrammes de séquence système les plus importants.

Réalisez les 5 diagrammes de classes des scénarios les plus importants.

Faites un choix d\'architecture et justifiez le.

Quels design pattern utilisez vous et pourquoi ?

Réalisez le diagramme de classe détaillant les associations et leur
cardinalité.

Repérage des mots clés
----------------------

### Légende des couleurs

Concept : Mot portant une signification pour le projet ;

Nom propre : Identifiant unique d'une chose ou d'une personne ;

Action : transformation de l'état ;

Propriété : qualité, durée etc.

### Repérage

*L\'association* *CultureDiffusion* souhaite réaliser une *bibliothèque
numérique* à *gestion décentralisée*.

Le principe est de permettre à chaque *membre* de *numériser* les
*œuvres* et aux *bibliothécaires* de les *proposer à l\'emprunt* selon
deux modalités :

Toutes les *œuvres du domaine public* sont *accessibles gratuitement*,
toutes les *œuvres sous droits* sont proposées en *location* pour une
période de *2 semaines*.

Lorsqu\'une œuvre *passe dans le domaine public*, elle devient
*accessible gratuitement* et *est diffusée aux membres* *ayant accordé*
à *l\'application* *suffisamment d\'espace disque*.

Chaque *membre* de la *bibliothèque* peut *emprunter* ou *louer* une
*œuvre*.

Chaque *membre* peut *proposer* une œuvre et ainsi *enrichir* la
*bibliothèque*.

Chaque *œuvre* est constituée d\'un *fichier* contenant l\'œuvre et
d\'un fichier au *format json* contenant *les informations sur
l\'œuvre*.

L\'application bibliothèque possède un *index* des œuvres qui est *mis à
jour* à chaque *ajout* ou *suppression* d\'œuvre.

L\'application possède quatre *rubriques* proposées sous forme de
*répertoires*.

Un répertoire \"*fond\_commun*\" avec une partie des œuvres *libres de
droits* de *l\'association*.

Un répertoire \"*emprunts*\" avec les *œuvres* sous droit empruntées par
le *membre* qui sont *chiffrées* avec sa *clé*.

Un *répertoire \"séquestre\"* avec une partie des *œuvres* sous *droit*
gérée par *l\'association*, *tous les fichiers y sont chiffrés*,
*l\'index* n\'y est pas *accessible de façon directe*.

Un *répertoire \"à modérer\" *avec les *œuvres* que le *membre* a
*proposées*.

Lorsqu\'une *œuvre* est *proposée* par un membre, elle est *soumise à
modération*.

Les *bibliothécaires* *voient les œuvres soumises*, vérifient et
complètent les *données* telles que les *auteurs*, *éditeur*, *langue*,
*pays d\'origine*, *date de publication*, *droits*, *catégorie de
l\'œuvre*, *format du support*, puis ils décident du *statut de
l\'œuvre* et donc si elle est dans le domaine public ou non, ou si elle
est *rejetée*.

Selon le statut de l\'*œuvre modérée*, l\'application *range* dans la
bonne *rubrique* et *gère* les *droits d\'accès*.

Si l\'*œuvre* est dans le *domaine public* il peut y en avoir autant de
*copie* qu\'il y a de membre.

Si l\'*œuvre* est *protégée* alors il ne peut y avoir que *3 fois plus
de copies* que de *licence d\'exploitation*, et chaque œuvre est
*chiffrée* par une *clé différente* ayant une *date de validité*.

À la *fin de la validité d\'un emprunt*, l\'application bibliothèque
supprime automatiquement l\'œuvre du répertoire du membre.

Les œuvres sont classées selon les types et sous-types suivants :

Article

Livre :

BD

Enfants

Romans

Livre technique

Education

Loisir

Culture

Sante

etc

Musique :

Classique

Jazz/Funk/Soul

Pop

Metal

etc

Vidéos :

SF

Histoire

Série

Documentaire

etc

Certaines œuvres appartiennent à plusieurs catégories en même temps.

Glossaire
---------

1^er^ étape identifier les concepts, mots clés et phrases clés et créer
une entrée dans un tableau ;

2me étape trouver une définitions pour chaque entrées créée ;

3me étape classer les entrées alphabétiquement.

Exemple à l'étape deux nous avons :

*Association* :Personne morale au sens loi 1901.

*CultureDiffusion*:Nom de l'application.

*Bibliothèque numérique* : Application informatique qui fonctionne
métaphoriquement comme une bibliothèque/médiathèque physique.

*Gestion décentralisée* : Les administrateurs ainsi que les
bibliothécaires accèdes à l'application depuis des lieux et des moments
différents, en plus après discussion avec le client, celui-ci veut que
les œuvres numériques soient stockées sur les terminaux des membres et
seulement sauvegardées sur un serveur du client ainsi il souhaite
utiliser des protocoles de partage pair à pair et de contrôle de
version.

*Membre* : Toute personne ayant un compte sur l'application.

*Numériser* : Consiste à créer ne projection de l'œuvre dans un fichier,
par exemple à scanner un livre.

*Œuvres* : Création ou réalisation humaine ayant généralement un intérêt
artistique .

*Bibliothécaires* : Membre de l'application en charge de classer les
œuvres et de vérifier leur nature.

*Proposer à l\'emprunt* : Action des bibliothécaires permettant de
partager les œuvres.

*Œuvres du domaine public *: Création ou réalisation dont les droits
moraux permettent leur usage par tous gratuitement généralement par ce
que l'auteur est mort depuis plus de 70 ans.

*Accessibles gratuitement* : L'accès à l'œuvre est permis au membre sans
contrepartie financière.

*Œuvres sous droits*: œuvres pour lesquelles ils existent encore des
ayant droits et qui imposent de respecter des règles strictes de mise à
disposition.

*Location d'une œuvre*

Délai de deux semaines de location : Contrainte sur la durée
d'utilisation d'une œuvre

Œuvre passant dans le domaine public

*Œuvre accessible gratuitement*

Œuvre diffusée aux membres

Membre accordant de l'espace disque au partage

*Application*

*Teste et validation de l\'espace disque*

*Emprunter une œuvre libre de droits*

*Œuvre Libre de droits* : synonyme de « *Œuvres du domaine public »*,

Œuvre orpheline : œuvre sous droits mais dont on ne connaît pas l'auter

Œuvre sous « creative common » : certaine permettent le partage d'autre
non selon la licence.

Louer une œuvre sous droits

*Enrichir* la *bibliothèque*.

Fichier

Format json

*Informations sur une œuvre*

*Index*

Index mis à jour

Mise à jour de l'index

*Ajout d'une œuvre*

Suppression d'une œuvre

*Rubriques*

*Répertoires*

Fond\_commun

Fichier chiffré

*Clé*

*Répertoire \"séquestre\"*

*Fichiers chiffrés*

*Index*

*Accessible de façon directe*

*Répertoire \"à modérer\" *

*Soumise à modération*

*Voire les œuvres soumises*

*Données :*

*Auteurs* : ,

*éditeur* : ,

*langue* : ,

*pays d\'origine* : ,

*date de publication* : ,

*droits* : ,

*catégorie de l\'œuvre* : ,

*format du support* :

*Statut de l\'œuvre* : Ensemble des informations permettant de savoir si
l'œuvre est dans le domaine public ou non.

*Fichier rejeté* : fichier dont le partage a été refusé par les
bibliothécaires.

*Œuvre modérée*

*Range dans la bonne rubrique* :

*Gère les droits d\'accès*

*Domaine public*

*Copie* :

*Œuvre protégée* :

3 fois plus de copies :

*Licence d\'exploitation* :

*Date de validité* :

### Glossaire technique et concepts introduits par les scénarios :

Anonyme : Utilisateur non encore authentifié ou n'ayant pas de compte.

Téléchargement de l'application :

Installation de l'application :

Utilisateur : Anonyme ou Membre ou Bibliothécaire utilisant
l'application.

Média : Support permettant d'exécuté l'application de la bibliothèque
décentralisée.

Membre authentifié:Membre dont la connexion s'est faite avec
FranceConnect.

Numéro de transaction : Identification unique de toute opération
réalisée.

Fichier journal local : Fichier contenant un historique de toutes les
opérations ayant été effectuées par le membre.

Filtre : Permet de cacher des éléments d'une liste lorsque ces éléments
ne sont pas voulus.

Tri : Permet d'ordonner les éléments d'une liste selon les critères
souhaités.

Liste des scénarios
-------------------

La transcription du cahier des charges en scénario donne lieu à des
échanges avec le client à la fois pour préciser les hypothèses, mais
également par ce qu'elle fait apparaître de nouveau concept et décrire
dans le glossaire.

Pour chaque scénario on donne un nom, une description, la liste des
acteurs, les préconditions, puis la liste des étapes du cas nominal sous
forme d'une liste de phrase au présent construite avec un sujet un verbe
et un complément. On peut fournir les scénarios alternatifs et ceux
d'erreurs.

Il faut détailler en premier les étapes des scénarios les plus
importants.

### Installer l'application

**Description **: Décrit le processus d'installation de l'application
sur différents médias

**Acteurs **: L'utilisateur, le serveur de mis à disposition de
l'application.

**Précondition **: Le téléchargement de l'application doit être possible
depuis le média (ordinateur ou smartphone) de l'utilisateur

**Étapes **:

1.  Le futur utilisateur ouvre son navigateur ou le market store de son
    système d'exploitation.
2.  Le futur utilisateur saisit le nom de l'application.
3.  La page de sélection affiche la description de l'application et ses
    informations légales, notamment celles correspondant aux partages
    des œuvres et à leurs droits d'auteurs.
4.  Le futur utilisateur sélectionne l'application et l'installe.

### Devenir Membre

**Description **: Un anonyme

**Acteurs **: un utilisateur Anonyme, FranceConnect, les différents
mandataires de FranceConnecte.

**Prérequis **: le scénario « Installer l'application » a été exécuté
sans erreur.

**Étapes **:

1.  L'utilisateur anonyme lance l'application.
2.  L'application détecte que c'est son premier lancement sur le média.
3.  L'application affiche une page d'information.
4.  L'application propose à l'utilisateur de se connecter via
    > FranceConnect.

5.  L'application propose de créer un compte ne pouvant déposer ou louer
    des œuvres.
6.  L'utilisateur choisit de se connecter via FranceConnect.
7.  L'application propose les différents sites d'identification.
8.  L'utilisateur choisit l'un des sites.
9.  L'utilisateur s'authentifie.
10. L'application reçoit les informations de connexion.
11. L'application affiche toutes les actions, dont celles de dépôt.

**Scénario alternatif**:

branchement à l'étape 6

1.  L'utilisateur choisit de créer un nouvel identifiant.
2.  L'application demande le nom , prénom et date de naissance de
    l'utilisateur.
3.  L'utilisateur saisit les informations.
4.  À partir de ces informations, l'application crée

-   un identifiant unique garantissant l'anonymat,
-   une paire de clés, publique et privée, pour enregistrer les
    opérations qui seront faites.

1.  L'application transmet l'identifiant et la clé publique au serveur
    de l'association.
2.  L'application affiche les actions permises.
3.  L'application affiche la liste des œuvres dans le domaine public.

**Documents **:

Page d'information affichée : pour expliquer l'objectif de
l'application, ses possibilités et précise que l'utilisateur devra
utiliser un compte FranceConnect s'il veut pouvoir louer des œuvres sous
droits ou déposer des œuvres.

### Devenir Bibliothécaire

**Description **: Un membre demande à devenir bibliothécaire.

**Acteurs **: Membre, Bibliothécaire

**Prérequis **: Il existe au moins un Bibliothécaire actif.

**Étapes **:

1.  Un membre demande à l'application à devenir bibliothécaires.
2.  L'application enregistre la demande et soumet la demande aux
    bibliothécaires.
3.  L'application sur le média d'un autre bibliothécaire transmet à son
    utilisateur la demande pour modération.
4.  L'application demande au bibliothécaire s'il :

-   accepte,
-   rejette,
-   n'a pas d'avis,
-   ou souhaite ignorer la candidature.

1.  Le bibliothécaire indique à l'application quel est son choix.
2.  L'application partage de façon anonyme et unique ce choix avec les
    autres applications sur les médias des autres Bibliothécaires.
3.  Le Bibliothécaire peut modifier son choix tant que le délai imparti
    n'est pas écoulé.
4.  Une fois le délai écoulé, les applications des bibliothécaires
    propagent aux autres applications la décision automatique prise
    ainsi :

-   Si la majorité des bibliothécaires ont accepté la candidature du
    membre alors celui-ci devient bibliothécaire.

1.  Le membre consulte la décision depuis l'application sur son média.
2.  Si l'application du futur bibliothécaire constate qu'il est promu
    bibliothécaire alors il reçoit les droits lui permettant d'accéder à
    l'ensemble des contenus et de pouvoir accepter ou refuser les
    modérations.
3.  Sinon l'application indique le refus de sa promotion.

**Scénarios alternatifs** :

La majorité des bibliothécaires refuse la promotion.

**Scénarios erreurs** :

**Données, documents, écrans** :

### Se connecter

\@TODO

### Accéder à la liste des œuvres

**Description **: L'utilisateur demande à voir la liste des œuvres

**Acteurs **: Utilisateur

**Prérequis **:

**Étapes **:

**Scénarios alternatifs** :

**Scénarios erreurs** :

**Données, documents, écrans** :

### Déposer une œuvre numérisée

**Description **: Un membre a numérisé une œuvre et souhaite la partager
avec la bibliothèque pour enrichir son fond.

**Acteurs **: Membre authentifié

**Prérequis **: Le membre est authentifié sur l'application par
FranceConnect

**Étapes **:

1.  Le membre authentifié demande à l'application à partager une œuvre.
2.  L'application affiche un formulaire de saisie d'information
    concernant l'œuvre.
3.  Le membre authentifié saisit les informations, et joint le fichier
    de l'œuvre numérisée.
4.  L'application demande confirmation de l'envoi.
5.  Le membre authentifié confirme l'envoi.
6.  L'application enregistre le fichier dans le répertoire « à
    modérer ».
7.  L'application créer un numéro de transaction et l'enregistre dans le
    fichier journal local.
8.  L'application transmet le fichier, ses informations et les numéros
    de transaction au dépôt sur le serveur de l'association.
9.  Les serveurs de l'association notifient les bibliothécaires qu'une
    nouvelle œuvre est en attente de modération.
10. L'application indique au membre que son partage est en attente de
    modération.

**Scénarios alternatifs :**

**Scénarios erreurs :**

Erreur de connexion avec le serveur.

**Données, documents, écrans :**

\@TODO

### Modérer une œuvre numérisée

**Description **: Les bibliothécaires sont avertis des numérisations
œuvres à modérer.

**Acteurs **: Bibliothécaire, serveur de la Bibliothèque Nationale de
France

**Prérequis **:Le fichier d'une œuvre numérisée doit avoir été déposé et
soumis en modération

**Étapes **:

1.  L'un des bibliothécaires se connecte à l'application.
2.  L'application lui affiche la liste des fichiers d'œuvres numérisées
    soumises.
3.  Le bibliothécaire positionne ses filtres pour ne voir que les œuvres
    susceptibles de l'intéresser.
4.  L'application n'affiche que les résultats correspondant aux filtres.
5.  Le bibliothécaire positionne les tris pour les afficher dans l'ordre
    voulu.
6.  L'application affiche les résultats dans l'ordre souhaité.
7.  Le bibliothécaire sélectionne un fichier d'une œuvre.
8.  L'application affiche les informations saisies par le membre ayant
    soumis l'œuvre.
9.  L'application affiche un lecteur spécifique au type de fichier.
10. Le bibliothécaire parcourt l'œuvre.
11. Le bibliothécaire complète les informations sur l'œuvre.
12. Le bibliothécaire accepte l'œuvre en précisant sa nature.
13. \@TODO

**Scénarios alternatifs** :

**Scénarios erreurs** :

**Données, documents, écrans** :

### Consulter une œuvre du domaine public

\@TODO

### Remplir les informations concernant une œuvre

\@TODO

### Consulter les informations concernant une œuvre

\@TODO

### Modifier les informations concernant une œuvre

\@TODO

### Louer une œuvre sous droits d'auteur

\@TODO

### Passage d'une œuvre dans le domaine public

\@TODO

### Diffusion d'une œuvre libre de droits

\@TODO

### Mise à jour de l'index des œuvres

\@TODO

### Consultation des rubriques

\@TODO

### Consultation de la rubrique « Fond commun »

\@TODO
