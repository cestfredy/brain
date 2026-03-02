# The Software Architecture Handbook
by German Cocca

## What is software architecture ?

L'architecture logiciel d'un système represente l'ensemble des décision de conception fondamentales qui définissent sa structure organisationnelle, ses comportements dynamiques et ses propriétés non fonctionnelles.

Elle décrit :

- la structure : les composants, leurs reponsabilités, leurs interfaces et les relations qui les relient.

- Le comportement : la maniere dont ces composants interagissent, communiquent et évoluent au cours de l'exécution.

- Les contraintes et qualité : exigences non fonctionnelles notamment 
    * performance
    * sécurité
    * maintenabilité
    * évolutivité
    * fiabilité

- Les choix technologiques et principes directeurs : langages, framework, protocoles, styles architecturaux (microservices, monolithes, couches, evenements, ...)

- Les compromis et justification : Le plus important !!!
pourquoi certaines décisions ont été prises, en tenant compte du contexte, des objectifs et des contraintes.


## Achitecture concepts to know

### C'est quoi le model Client-serveur ?
La chose a retenir ici c'est simplement que le client demande des ressources ou services et le serveur éffectuer toutes les opérations autour pour répondre.

Il est également important de toujours prendre en compte que le client et le serveur peuvent être developé, hebergé et exécuté séparement.


