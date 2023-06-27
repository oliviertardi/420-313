---
title: "Ce qu'on protège"
date: 2023-06-21T20:24:05-04:00
draft: false
weight: 11
---

La cybersécurité a pour but de protéger les _informations_, peu importe leur forme, autant lorsqu'elles sont stockées que lorsqu'elles circulent à travers les réseaux de communication.

Les informations dont disposent les systèmes informatiques des organisations (comme une entreprise, un hôpital, une association, etc.) sont essentielles à leur fonctionnement et doivent donc être protégées. On peut penser aux informations personnelles des personnes (employés, clients), aux données bancaires ou financières de ceux-ci, à tout ce qui touche la propriété intellectuelle (inventions, recherche et développement), en plus des données privées comme les courriels ou autres systèmes de messagerie. Dans certains cas même, la loi oblige les orgqnisations à protéger les données, comme les données médicales ou judiciaires. 

Cette protection touche à trois aspects des informations: 
+ la confidentialité
+ l'intégrité
+ la disponibilité

On nomme souvent ces trois axes la "triade de cybersécurité", regroupés sous l'acronyme _CIA_ (de l'anglais _Confidentiality, Integrity, Availability_). Dans cette section nous allons voir en quoi cela consiste, comment chacun peut être attaqué et comment on les protège.

## Confidentialité
> L’information doit être protégée afin d’être accessible uniquement à ceux qui y sont autorisés.  

Les informations n'ont pas toutes la même valeur: certaines peuvent être diffusées sans risque, mais d'autres doivent demeurer secrètes. Les informations contenues dans une page web qui décrit la recette d'un gâteau aux carottes ont moins besoin d'être protégées que celles qui se trouvent dans un échange de courriels entre un comptable et ses clients.

Les données utilisées par les entreprises peuvent être de nature publique ou privée. Parmi les données privées, celles qui requièrent d’être protégées par la confidentialité se divisent globalement en deux catégories : les données personnelles, qui regroupent toutes les informations permettant d’identifier de manière unique les individus, et les données sur l’entreprise qui révèlent ses opérations ou ses actifs. Quelques exemples : 

##### Données personnelles:
+ Numéro d’assurance sociale, d’employé, ou autre identifiant unique 
+ Données médicales 
+ Dossier judiciaire 
+ Données fiscales 
+ Numéros de carte de crédit 

##### Données d'entreprise
+ Projets de développement ou secrets industriels 
+ Données financières 
+ Informations sur les clients ou les fournisseurs 
+ Actifs matériels 

#### Niveaux de confidentialité
Ces données ont différents _niveaux de confidentialité_: certains sont accessibles par un grand nombre de personnes (par exemple, tous les employés de l'entreprise), d'autre par très peu d'individus. Pour s'assurer de respecter ces niveaux de confidentialité, des mesures de base doivent être appliquées. Ces mesures sont:

##### Authentification 
Chacun des utilisateurs d’un système informatique peut être identifié de manière unique et doit prouver son identité pour accéder au système. On utilise généralement _l'identifiant utilisateur_ à cette fin, et les _mots de passe_ servent à l'utilisateur pour prouver qu'il est bien celui qu'il prétend.

##### Autorisation 
Il faut déterminer quels utilisateurs ont accès à quelles informations, et la nature de ces permissions. Les systèmes de privilèges présents dans la plupart des systèmes informatiques servent à associer les utilisateurs aux informations qu'ils peuvent consulter. Par exemple, les permissions d'un système d'exploitation donnent à des utilisateurs et des groupes d'utilisateurs des droits de lecture, écriture ou exécution sur less fichiers du système.

##### Imputabilité 
On doit pouvoir savoir à quelles données un utilisateur a accédé, pour combien de temps et quelles modifications il y a apportées. Les logiciels et systèmes informatiques qui contiennent des données sensibles disposent souvent de mécanismes de journalisation ("logs") qui permettent de retracer les accès à ces données.

#### Chiffrement 
Le *chiffrement* est une mesure de protection supplémentaire pour la confidentialité. Lorsqu'on chiffre des données, celles-ci deviennent impossibles à lire à moins de disposer de la *clé* qui permet de les déchiffrer. 

_BitLocker_ est un outil dans Windows qui permet de chiffrer les partitions d'un disque dur; _LUKS_ est un équivalent pour linux.

Des protocoles de communication comme TLS ou SSH utilisent le chiffement pour préserver la confidentialité des données qui circulent sur les réseaux.

#### Valeur des informations
En règle générale, la confidentialité d'une information va de pair avec sa valeur: par exemple, une entreprise qui développe un logiciel qui lui rapporte beaucoup d'argent essaiera d'en garder le code source secret. Un grand nombre d'attaques informatiques ont ainsi pour objectif de se procurer des données confidentielles car celles-ci peuvent rapporter beaucoup d'argent en étant utilisées ou vendues à des tiers.

Lorsque la confidentialité des données est brisée, il n’y a pas de retour en arrière possible : les informations ne sont plus secrètes, on peut uniquement se protéger contre les attaques futures. C’est pourquoi les fuites de données relatives aux clients de grandes entreprises, sans nécessairement affecter directement les entreprises elles-mêmes, peuvent porter un coup important sur la confiance envers celles-ci. 

#### Exemple d'une attaque sur la confidentialité
En cliquant sur le fichier _.docx_ attaché à un courriel, un employé a déclenché à son insu l’installation d’un « keylogger » sur son poste de travail qui enregistre tous les identifiants et mots de passe des sites qu’il visite. Cette liste d'identifiants de connexion est ensuite récupérée par l'attaquant qui peut accéder à tous les comptes en ligne de l'employé.


## Intégrité
> L’information doit être authentique et fiable : on peut attester avec certitude de sa provenance, et elle n’a pas été modifiée de façon non-autorisée.


## Disponibilité
> L’information doit être accessible aux utilisateurs autorisés au moment où ils en ont besoin.

