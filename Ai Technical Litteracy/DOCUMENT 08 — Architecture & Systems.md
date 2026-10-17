# DOCUMENT 08 — ARCHITECTURE & SYSTEMS

## Référentiel fondamental de culture technique

**Version 1.0**

# 0\. FINALITÉ DU DOCUMENT

L’architecture est le domaine qui permet de répondre à une question fondamentale :

**Comment organiser plusieurs éléments pour construire un système cohérent, fiable, maintenable et adapté à ses contraintes ?**

Un développeur peut savoir écrire du code sans savoir concevoir correctement un système.

Une équipe peut savoir utiliser React, Python, PostgreSQL, Docker ou AWS sans savoir :

- où placer chaque responsabilité ;
- comment les composants doivent communiquer ;
- comment gérer les erreurs ;
- comment sécuriser les flux ;
- comment faire évoluer le système ;
- comment éviter les dépendances inutiles ;
- comment choisir entre plusieurs architectures ;
- comment prévoir les contraintes de performance ;
- comment raisonner sur les compromis.

L’objectif de ce document est donc de construire une **culture d’architecture et de systèmes**.

Il ne s’agit pas de devenir immédiatement architecte logiciel, ingénieur systèmes ou DevOps.

Il s’agit de pouvoir :

1.  reconnaître les concepts architecturaux ;
2.  comprendre leur raison d’être ;
3.  identifier les problèmes qu’ils résolvent ;
4.  savoir quand penser à eux ;
5.  comprendre les relations entre les composants ;
6.  distinguer les différentes architectures ;
7.  choisir une approche adaptée à un contexte ;
8.  comprendre les compromis ;
9.  dialoguer avec des développeurs et ingénieurs spécialisés ;
10. demander correctement à une IA de concevoir un système ;
11. vérifier une architecture générée par l’IA ;
12. détecter les architectures inutilement complexes ;
13. identifier les risques techniques ;
14. comprendre les implications de sécurité, performance, coût et maintenance ;
15. construire progressivement une vision système.

# 1\. LE PROBLÈME CENTRAL

Un système logiciel n’est pas simplement :

frontend + backend + base de données.

Un système réel peut contenir :

- utilisateurs ;
- interfaces ;
- applications ;
- API ;
- services ;
- bases de données ;
- fichiers ;
- authentification ;
- autorisation ;
- cache ;
- files de messages ;
- tâches asynchrones ;
- services externes ;
- systèmes de paiement ;
- emails ;
- notifications ;
- logs ;
- métriques ;
- monitoring ;
- infrastructure ;
- sauvegardes ;
- CI/CD ;
- secrets ;
- DNS ;
- CDN ;
- sécurité ;
- équipes ;
- procédures.

Le problème architectural est donc :

**Comment faire fonctionner toutes ces parties ensemble sans créer un système incohérent ?**

# 2\. LE MODÈLE MENTAL GLOBAL

Une manière utile de lire un système :

UTILISATEURS  
↓  
INTERFACE / CLIENT  
↓  
RÉSEAU  
↓  
API / SERVICES  
↓  
LOGIQUE MÉTIER  
↓  
DONNÉES  
↓  
INFRASTRUCTURE

Mais un système réel doit également être traversé par :

SÉCURITÉ  
OBSERVABILITÉ  
PERFORMANCE  
FIABILITÉ  
DÉPLOIEMENT  
GOUVERNANCE

Une architecture complète peut donc être pensée comme :

**COMPOSANTS + RESPONSABILITÉS + RELATIONS + DONNÉES + FLUX + CONTRAINTES + OPÉRATIONS**

# 3\. ARCHITECTURE ≠ TECHNOLOGIE

Choisir :

React + Node + PostgreSQL

n’est pas encore une architecture complète.

L’architecture concerne également :

- les responsabilités ;
- les frontières ;
- les dépendances ;
- les flux ;
- les données ;
- les décisions ;
- les contraintes ;
- les propriétés du système.

La technologie est un moyen.

L’architecture est une organisation.

# NIVEAU A — CARTOGRAPHIE DU DOMAINE

# 4\. LES GRANDES FAMILLES

Le domaine peut être organisé autour de douze grandes familles.

## 4.1 Architecture logicielle

- composants ;
- modules ;
- couches ;
- dépendances ;
- interfaces ;
- services ;
- patterns.

## 4.2 Architecture applicative

- frontend ;
- backend ;
- API ;
- logique métier ;
- persistance ;
- intégrations.

## 4.3 Architecture des données

- bases de données ;
- schémas ;
- relations ;
- index ;
- transactions ;
- réplication ;
- cache ;
- stockage.

## 4.4 Architecture distribuée

- services ;
- réseau ;
- communication ;
- messages ;
- événements ;
- synchronisation ;
- cohérence.

## 4.5 Infrastructure

- serveurs ;
- cloud ;
- conteneurs ;
- réseau ;
- DNS ;
- CDN ;
- stockage ;
- compute.

## 4.6 DevOps

- CI/CD ;
- environnements ;
- automatisation ;
- déploiement ;
- infrastructure as code ;
- rollback.

## 4.7 Fiabilité

- disponibilité ;
- résilience ;
- tolérance aux pannes ;
- sauvegarde ;
- reprise ;
- disaster recovery.

## 4.8 Performance

- latence ;
- débit ;
- concurrence ;
- cache ;
- compression ;
- scaling.

## 4.9 Sécurité architecturale

- authentification ;
- autorisation ;
- isolation ;
- chiffrement ;
- secrets ;
- trust boundaries ;
- défense en profondeur.

## 4.10 Observabilité

- logs ;
- métriques ;
- traces ;
- alertes ;
- monitoring ;
- diagnostics.

## 4.11 Gouvernance technique

- standards ;
- conventions ;
- ADR ;
- documentation ;
- dette technique ;
- ownership ;
- évolution.

## 4.12 Architecture organisationnelle

- équipes ;
- responsabilités ;
- ownership ;
- communication ;
- dépendances ;
- structure de décision.

# 5\. SYSTÈME

## Qu’est-ce qu’un système ?

Un système est un ensemble d’éléments reliés entre eux pour produire un comportement ou un résultat.

Un système logiciel peut comprendre :

Entrées  
↓  
Traitement  
↓  
Données  
↓  
Décisions  
↓  
Sorties

Mais les systèmes modernes sont souvent dynamiques :

INPUT  
↓  
PROCESSING  
↓  
STATE  
↓  
OUTPUT  
↓  
FEEDBACK  
↓  
ADAPTATION

# 6\. ARCHITECTURE

L’architecture décrit notamment :

- les composants ;
- leurs responsabilités ;
- leurs relations ;
- leurs frontières ;
- leurs dépendances ;
- leurs interactions.

Une architecture cherche à rendre le système :

- compréhensible ;
- évolutif ;
- fiable ;
- sécurisé ;
- maintenable.

# 7\. COMPOSANT

Un composant est une partie identifiable du système ayant une responsabilité donnée.

Exemples :

- frontend ;
- service d’authentification ;
- service de paiement ;
- module de facturation ;
- base de données ;
- moteur de recherche.

# 8\. MODULE

Un module regroupe du code autour d’une responsabilité.

Un module bien défini possède idéalement :

- une responsabilité claire ;
- une interface claire ;
- peu de dépendances inutiles ;
- un faible couplage avec les autres modules.

# 9\. INTERFACE

Une interface définit comment une partie du système peut communiquer avec une autre.

Elle peut être :

- API HTTP ;
- fonction ;
- classe ;
- événement ;
- message ;
- protocole.

# 10\. DÉPENDANCE

A dépend de B lorsque A a besoin de B pour fonctionner.

Une architecture devient problématique lorsque les dépendances sont :

- nombreuses ;
- circulaires ;
- cachées ;
- difficiles à remplacer.

# 11\. COUPLAGE

Le couplage mesure le degré de dépendance entre différentes parties.

### Couplage fort

Modifier A oblige fréquemment à modifier B.

### Couplage faible

Les composants peuvent évoluer avec davantage d’indépendance.

Objectif général :

réduire les dépendances inutiles.

# 12\. COHÉSION

La cohésion décrit à quel point les responsabilités regroupées dans un composant sont liées.

Bonne cohésion :

une responsabilité cohérente.

Mauvaise cohésion :

un composant qui fait « un peu de tout ».

# 13\. COUPLAGE VS COHÉSION

Une règle classique :

**couplage faible + cohésion forte**

Cela ne signifie pas :

zéro dépendance.

Les systèmes ont nécessairement des dépendances.

L’objectif est de les rendre :

- intentionnelles ;
- compréhensibles ;
- contrôlables.

# NIVEAU B — COMMENT LIRE UN SYSTÈME

# 14\. FRONTEND

Partie généralement exécutée côté client et responsable notamment :

- interface ;
- interactions ;
- état local ;
- affichage ;
- expérience utilisateur.

Technologies possibles :

- HTML ;
- CSS ;
- JavaScript ;
- React ;
- Vue ;
- Angular ;
- Svelte.

# 15\. BACKEND

Partie responsable notamment :

- logique métier ;
- accès aux données ;
- authentification ;
- autorisation ;
- traitements ;
- intégrations.

Technologies possibles :

- Node.js ;
- Python ;
- Java ;
- Go ;
- C# ;
- PHP ;
- Ruby.

# 16\. BASE DE DONNÉES

Système permettant de stocker et récupérer des données.

Grandes familles :

### Relationnelles

- PostgreSQL ;
- MySQL ;
- MariaDB ;
- SQL Server.

### NoSQL

- MongoDB ;
- Redis ;
- DynamoDB ;
- autres systèmes spécialisés.

Le choix dépend du problème.

# 17\. API

Une API définit un moyen permettant à des systèmes de communiquer.

Exemple :

Frontend  
↓  
GET /users  
↓  
Backend  
↓  
Database

# 18\. REST

REST est un style architectural couramment utilisé pour concevoir des API HTTP.

Concepts fréquents :

- ressources ;
- méthodes HTTP ;
- statelessness ;
- représentations ;
- codes HTTP.

REST n’est donc pas synonyme d’API.

# 19\. GRAPHQL

GraphQL permet notamment au client de demander les données dont il a besoin selon un schéma défini.

Avantages possibles :

- flexibilité ;
- réduction de certains overfetching/underfetching.

Coûts possibles :

- complexité ;
- cache ;
- sécurité ;
- gouvernance ;
- monitoring.

# 20\. gRPC

gRPC est un framework de communication RPC particulièrement utilisé pour certaines communications service-à-service.

Il peut être intéressant lorsque :

- performance ;
- contrats fortement typés ;
- communication interne ;

sont importants.

Ce n’est pas automatiquement meilleur que REST.

# 21\. SYNCHRONE VS ASYNCHRONE

### Synchrone

Le composant attend généralement une réponse.

A → B  
A ← réponse

### Asynchrone

A peut continuer son travail sans attendre immédiatement B.

A → message  
↓  
B traite plus tard

L’asynchrone devient intéressant pour :

- tâches longues ;
- notifications ;
- traitement lourd ;
- événements ;
- files d’attente.

# 22\. QUEUE

Une queue stocke temporairement des tâches/messages à traiter.

Exemple :

Utilisateur  
↓  
API  
↓  
Queue  
↓  
Worker  
↓  
Traitement

Avantages :

- découplage ;
- absorption des pics ;
- traitement différé.

Risques :

- complexité ;
- messages dupliqués ;
- ordre ;
- échec ;
- monitoring.

# 23\. EVENT

Un événement décrit quelque chose qui s’est produit.

Exemple :

PaymentCompleted

L’événement peut être consommé par plusieurs composants.

# 24\. EVENT-DRIVEN ARCHITECTURE

Architecture dans laquelle les composants réagissent à des événements.

Exemple :

Commande créée  
↓  
OrderCreated  
┌────┼────┐  
↓ ↓ ↓  
Email Stock Analytics

Avantages :

- découplage ;
- extensibilité ;
- réactivité.

Coûts :

- débogage ;
- cohérence ;
- observabilité ;
- gestion des doublons ;
- complexité mentale.

# NIVEAU C — ARCHITECTURES LOGICIELLES

# 25\. MONOLITHE

Une application dont les principales fonctionnalités sont regroupées dans une même unité déployable.

Cela ne signifie pas nécessairement :

mauvais design.

Un monolithe peut être :

- simple ;
- rapide à développer ;
- facile à déployer ;
- très performant pour certains usages.

# 26\. MONOLITHE MODULAIRE

Un monolithe peut être organisé en modules bien séparés :

Application  
├── Auth  
├── Users  
├── Billing  
├── Orders  
└── Notifications

Il peut offrir une partie des avantages organisationnels d’une architecture plus distribuée sans introduire immédiatement les coûts du réseau.

# 27\. MICROSERVICES

Architecture où une application est divisée en plusieurs services relativement indépendants.

Exemple :

API Gateway  
│  
┌──┼─────────────┐  
↓ ↓ ↓  
Auth Billing Orders  
↓  
Stock

Avantages possibles :

- indépendance de déploiement ;
- scaling indépendant ;
- ownership par équipe ;
- isolation de certaines responsabilités.

Coûts :

- réseau ;
- observabilité ;
- déploiement ;
- données distribuées ;
- cohérence ;
- debugging ;
- infrastructure.

# 28\. MONOLITHE VS MICROSERVICES

Ne pas demander :

« Quelle architecture est la plus moderne ? »

Demander :

« Quelle architecture correspond aux contraintes actuelles ? »

### Monolithe souvent pertinent lorsque :

- petite équipe ;
- produit jeune ;
- domaine encore incertain ;
- faible complexité opérationnelle ;
- vitesse de développement prioritaire.

### Microservices potentiellement pertinents lorsque :

- organisation suffisamment grande ;
- domaines clairement séparés ;
- besoins de scaling différents ;
- équipes autonomes ;
- contraintes opérationnelles justifiant la complexité.

# 29\. SERVERLESS

Architecture dans laquelle certaines fonctions d’exécution sont gérées par un fournisseur.

Exemples conceptuels :

Request  
↓  
Function  
↓  
Database

Avantages :

- infrastructure réduite à gérer ;
- scaling automatique dans certains cas ;
- paiement à l’usage selon le service.

Contraintes :

- cold starts selon plateforme ;
- limites d’exécution ;
- observabilité ;
- dépendance fournisseur ;
- architecture parfois distribuée.

# 30\. LAYERED ARCHITECTURE

Organisation en couches.

Exemple :

Presentation  
↓  
Application  
↓  
Domain  
↓  
Infrastructure

L’objectif est notamment de séparer les responsabilités.

# 31\. CLEAN ARCHITECTURE

Approche visant notamment à isoler la logique métier des détails externes.

Principe général :

les éléments centraux du domaine ne devraient pas dépendre inutilement des détails techniques externes.

# 32\. HEXAGONAL ARCHITECTURE

Aussi appelée Ports and Adapters.

Idée :

API  
↓  
┌─────────────┐  
DB → │ DOMAIN │ ← External Service  
└─────────────┘  
↑  
CLI

Le domaine communique avec le monde extérieur via des interfaces/ports.

# 33\. DOMAIN-DRIVEN DESIGN

DDD cherche à organiser le logiciel autour du domaine métier.

Concepts importants :

- domain ;
- subdomain ;
- bounded context ;
- entity ;
- value object ;
- aggregate ;
- repository ;
- domain service ;
- ubiquitous language.

Il devient particulièrement pertinent lorsque le domaine métier est complexe.

# NIVEAU D — FRONTIÈRES ET RESPONSABILITÉS

# 34\. SEPARATION OF CONCERNS

Principe :

ne pas mélanger inutilement des responsabilités différentes.

Exemple :

Éviter qu’un même module gère simultanément :

- interface ;
- paiement ;
- accès base ;
- email ;
- authentification ;
- logique métier.

# 35\. SINGLE RESPONSIBILITY

Une unité devrait avoir une responsabilité cohérente et une raison claire d’évoluer.

Attention :

Cela ne signifie pas :

une fonction = une seule ligne de code.

# 36\. ABSTRACTION

Une abstraction masque des détails inutiles derrière une interface plus simple.

Exemple :

PaymentService  
↓  
Stripe / FedaPay / autre

Le reste du système peut dépendre du concept :

PaymentService

plutôt que d’être directement dépendant de chaque détail du fournisseur.

# 37\. ENCAPSULATION

Une partie du système contrôle l’accès à son état interne.

Objectif :

éviter que n’importe quel composant modifie directement n’importe quoi.

# 38\. DEPENDENCY INVERSION

L’idée générale :

les politiques métier ne devraient pas dépendre directement des détails techniques.

Cela permet notamment de remplacer :

- base ;
- fournisseur ;
- API ;
- infrastructure.

avec moins de modifications centrales.

# 39\. BOUNDARY

Une boundary est une frontière architecturale.

Exemples :

- frontend / backend ;
- service / service ;
- domaine / infrastructure ;
- système / fournisseur externe ;
- tenant / tenant.

Une bonne architecture rend les frontières explicites.

# 40\. TRUST BOUNDARY

Frontière au-delà de laquelle le niveau de confiance change.

Exemple :

Utilisateur  
↓  
Internet  
↓  
API publique  
↓  
Réseau interne  
↓  
Database

Chaque frontière nécessite une réflexion de sécurité.

# NIVEAU E — ARCHITECTURE DES DONNÉES

# 41\. DATA MODEL

Le modèle de données définit notamment :

- entités ;
- attributs ;
- relations ;
- contraintes.

Exemple :

User  
↓  
Organization  
↓  
Project  
↓  
Task

# 42\. NORMALISATION

Technique de conception des bases relationnelles visant notamment à réduire :

- duplication ;
- incohérences ;
- anomalies de mise à jour.

Mais une normalisation excessive peut aussi avoir des coûts pratiques.

# 43\. INDEX

Un index aide la base à retrouver certaines données plus efficacement.

Mais :

index ≠ optimisation gratuite.

Les index ont des coûts :

- stockage ;
- écriture ;
- maintenance.

# 44\. TRANSACTION

Une transaction regroupe des opérations qui doivent respecter certaines garanties de cohérence.

Concepts classiques :

ACID

- Atomicity
- Consistency
- Isolation
- Durability

# 45\. CONSISTENCY

La cohérence décrit si les différents composants observent des données compatibles selon les garanties du système.

Dans les systèmes distribués, il faut parfois choisir entre :

- cohérence immédiate ;
- cohérence éventuelle ;
- disponibilité ;
- performance.

# 46\. CACHE

Un cache stocke temporairement des données pour accélérer l’accès.

Request  
↓  
Cache ?  
├── Oui → réponse  
└── Non → Database

Problème classique :

**cache invalidation**

Les données en cache peuvent devenir obsolètes.

# 47\. STOCKAGE OBJET

Utilisé notamment pour :

- images ;
- vidéos ;
- documents ;
- fichiers volumineux.

Il faut distinguer :

base de données

et :

stockage de fichiers.

# 48\. RÉPLICATION

La réplication consiste à maintenir plusieurs copies de données ou d’un système.

Objectifs possibles :

- disponibilité ;
- lecture ;
- tolérance aux pannes.

Elle introduit aussi :

- latence ;
- synchronisation ;
- complexité.

# 49\. SHARDING

Le sharding divise les données entre plusieurs partitions/nœuds.

Utile dans certaines situations de très grande échelle.

Mais :

ce n’est pas une optimisation à introduire par défaut.

# NIVEAU F — RÉSEAU ET COMMUNICATION

# 50\. DNS

Le DNS traduit notamment des noms de domaine en informations permettant d’atteindre les services correspondants.

Exemple :

example.com  
↓  
DNS  
↓  
IP / service

# 51\. IP

Une adresse IP identifie une interface réseau dans un contexte donné.

Il faut distinguer :

- IPv4 ;
- IPv6 ;
- adresse publique ;
- adresse privée.

# 52\. HTTP

Protocole fondamental du Web.

Concepts :

- request ;
- response ;
- method ;
- headers ;
- body ;
- status code ;
- cookies ;
- cache.

# 53\. HTTPS

HTTP protégé par TLS.

Il permet notamment :

- chiffrement en transit ;
- authentification du serveur ;
- intégrité des communications.

# 54\. LOAD BALANCER

Distribue les requêtes entre plusieurs instances.

Load Balancer  
/ | \\  
↓ ↓ ↓  
Server Server Server

# 55\. CDN

Un CDN distribue des contenus depuis des points de présence proches des utilisateurs.

Utile notamment pour :

- images ;
- CSS ;
- JavaScript ;
- vidéos ;
- fichiers statiques.

# 56\. LATENCE

Temps nécessaire pour obtenir une réponse.

Une architecture peut être techniquement correcte tout en étant mauvaise du point de vue utilisateur si la latence est excessive.

# 57\. THROUGHPUT

Quantité de travail qu’un système peut traiter pendant une période donnée.

Exemples :

- requêtes/seconde ;
- transactions/seconde ;
- événements/seconde.

# 58\. BOTTLENECK

Point limitant la performance globale.

Exemples :

- CPU ;
- mémoire ;
- disque ;
- réseau ;
- database ;
- API externe.

Optimiser ailleurs que sur le bottleneck peut avoir peu d’effet.

# NIVEAU G — SCALABILITÉ

# 59\. SCALABILITÉ

Capacité d’un système à supporter une augmentation de charge.

La charge peut augmenter par :

- utilisateurs ;
- requêtes ;
- données ;
- transactions ;
- fichiers ;
- traitements.

# 60\. SCALE UP

Ajouter davantage de ressources à une machine.

Server  
↓  
More CPU / RAM

# 61\. SCALE OUT

Ajouter davantage d’instances.

Server 1  
Server 2  
Server 3

# 62\. AUTO-SCALING

Adapter automatiquement les ressources selon la charge ou d’autres métriques.

# 63\. STATEFUL VS STATELESS

### Stateful

Le serveur conserve un état nécessaire entre plusieurs requêtes.

### Stateless

Chaque requête peut être traitée sans dépendre d’un état local conservé sur une instance particulière.

Les architectures distribuées favorisent souvent le stateless lorsque possible.

# 64\. BACKPRESSURE

Mécanisme permettant d’empêcher un producteur de surcharger un consommateur.

Important dans :

- streams ;
- queues ;
- pipelines ;
- systèmes asynchrones.

# NIVEAU H — FIABILITÉ ET RÉSILIENCE

# 65\. AVAILABILITY

Proportion de temps pendant laquelle un service est disponible selon une définition donnée.

# 66\. RELIABILITY

Capacité d’un système à fonctionner correctement sur la durée.

Disponibilité et fiabilité sont liées mais différentes.

# 67\. RESILIENCE

Capacité à continuer à fonctionner ou à récupérer après une perturbation.

# 68\. FAULT TOLERANCE

Capacité à continuer malgré certaines défaillances.

# 69\. SINGLE POINT OF FAILURE

Composant dont la panne peut provoquer une panne importante du système.

Exemple :

Everything  
↓  
One Server

Si ce serveur tombe :

tout tombe.

# 70\. REDUNDANCY

Posséder plusieurs éléments capables d’assurer une même fonction.

Objectif :

éviter qu’une panne unique provoque une interruption.

# 71\. RETRY

Réessayer une opération après un échec.

Mais :

retry ≠ toujours bonne solution.

Il faut gérer :

- nombre de tentatives ;
- délai ;
- type d’erreur ;
- idempotence.

# 72\. EXPONENTIAL BACKOFF

Augmenter progressivement le délai entre les tentatives.

Utile pour éviter :

surcharge → erreur → retry immédiat → surcharge supplémentaire.

# 73\. CIRCUIT BREAKER

Mécanisme qui peut temporairement empêcher les appels vers un service défaillant afin de protéger le reste du système.

# 74\. TIMEOUT

Un système ne doit pas nécessairement attendre indéfiniment une réponse.

Les timeouts protègent contre :

- services bloqués ;
- connexions lentes ;
- ressources immobilisées.

# 75\. IDEMPOTENCE

Une opération idempotente peut être répétée sans produire plusieurs effets indésirables.

Particulièrement important pour :

- paiements ;
- commandes ;
- webhooks ;
- retries.

# NIVEAU I — SÉCURITÉ ARCHITECTURALE

# 76\. SECURITY BY DESIGN

La sécurité doit être intégrée dans l’architecture dès la conception.

Pas :

« on sécurisera à la fin ».

# 77\. AUTHENTICATION

Répond :

**Qui es-tu ?**

# 78\. AUTHORIZATION

Répond :

**As-tu le droit de faire cela ?**

# 79\. LEAST PRIVILEGE

Chaque utilisateur, service ou composant doit avoir uniquement les permissions nécessaires.

# 80\. ZERO TRUST

Ne pas considérer automatiquement qu’un composant est fiable simplement parce qu’il se trouve « à l’intérieur » du système.

# 81\. SECRETS

Exemples :

- clés API ;
- tokens ;
- mots de passe ;
- credentials.

Ils ne doivent pas être exposés dans :

- Git ;
- frontend public ;
- logs ;
- documentation publique.

# 82\. CHIFFREMENT

Deux grandes situations :

### En transit

Protection des données pendant la communication.

### Au repos

Protection des données stockées.

# 83\. ISOLATION

Dans un système multi-utilisateur, il faut empêcher qu’un utilisateur accède aux données d’un autre.

Cela devient particulièrement critique dans un SaaS multi-tenant.

# NIVEAU J — OBSERVABILITÉ

# 84\. OBSERVABILITY

L’observabilité permet de comprendre ce qui se passe à l’intérieur d’un système à partir de ses sorties observables.

Trois piliers classiques :

- logs ;
- metrics ;
- traces.

# 85\. LOGS

Événements enregistrés.

Exemple :

2026-09-12  
payment_failed  
user_id=...  
reason=...

Les logs doivent être :

- utiles ;
- structurés ;
- exploitables ;
- suffisamment détaillés.

Mais éviter :

- secrets ;
- données personnelles inutiles ;
- bruit excessif.

# 86\. METRICS

Valeurs numériques mesurées dans le temps.

Exemples :

- CPU ;
- mémoire ;
- latence ;
- erreurs ;
- requêtes/seconde ;
- taux de succès.

# 87\. TRACES

Permettent de suivre une requête à travers plusieurs composants.

Request  
↓  
API  
↓  
Service  
↓  
Database  
↓  
External API

Très utiles dans les architectures distribuées.

# 88\. MONITORING

Surveillance de l’état du système.

# 89\. ALERTING

Notification lorsqu’une condition importante est détectée.

Une mauvaise stratégie d’alerting produit :

trop d’alertes → fatigue → alertes ignorées.

# NIVEAU K — DEVOPS ET CYCLE DE VIE

# 90\. ENVIRONNEMENTS

Typiquement :

Development  
↓  
Staging  
↓  
Production

Chaque environnement peut avoir :

- configuration ;
- données ;
- secrets ;
- contraintes.

# 91\. CI

**Continuous Integration**

Automatiser notamment :

- tests ;
- lint ;
- build ;
- vérifications.

# 92\. CD

Selon le contexte :

- Continuous Delivery ;
- Continuous Deployment.

Objectif général :

rendre la livraison logicielle plus fiable et répétable.

# 93\. PIPELINE

Chaîne automatisée :

Git Push  
↓  
Tests  
↓  
Build  
↓  
Security checks  
↓  
Deploy  
↓  
Verification

# 94\. ROLLBACK

Retour à une version précédente après un problème.

Une architecture de déploiement mature prévoit :

comment revenir en arrière ?

# 95\. BLUE-GREEN DEPLOYMENT

Deux environnements permettent notamment de basculer entre ancienne et nouvelle version.

# 96\. CANARY DEPLOYMENT

Déployer progressivement une nouvelle version sur une partie des utilisateurs avant généralisation.

# 97\. FEATURE FLAG

Permet d’activer ou désactiver une fonctionnalité indépendamment du déploiement du code.

Utile pour :

- tests ;
- lancement progressif ;
- rollback fonctionnel ;
- expérimentation.

# NIVEAU L — CLOUD ET INFRASTRUCTURE

# 98\. CLOUD

Le cloud fournit des ressources informatiques via des infrastructures distantes.

Catégories courantes :

- compute ;
- storage ;
- database ;
- networking ;
- managed services.

# 99\. IaaS

Infrastructure as a Service.

Tu gères davantage de composants.

# 100\. PaaS

Platform as a Service.

Le fournisseur gère davantage d’infrastructure.

# 101\. SaaS

Software as a Service.

L’utilisateur consomme directement le logiciel.

À ne pas confondre :

SaaS = modèle de distribution/service.

Architecture SaaS = manière dont le logiciel est conçu pour servir ses clients.

# 102\. CONTAINER

Un conteneur encapsule une application et son environnement d’exécution.

Docker est un outil majeur de cet écosystème.

# 103\. VIRTUAL MACHINE

Une machine virtuelle émule un environnement informatique isolé au-dessus d’un hyperviseur.

# 104\. CONTAINER VS VM

### Container

- plus léger ;
- partage le kernel de l’hôte ;
- démarrage généralement rapide.

### VM

- isolation différente ;
- système invité complet ;
- plus lourde généralement.

# 105\. KUBERNETES

Système d’orchestration de conteneurs.

Il peut gérer notamment :

- déploiement ;
- scaling ;
- service discovery ;
- remplacement d’instances ;
- configuration.

Mais :

Kubernetes n’est pas nécessaire pour tous les projets.

# 106\. INFRASTRUCTURE AS CODE

Décrire l’infrastructure avec du code ou des fichiers déclaratifs.

Avantages :

- reproductibilité ;
- versioning ;
- automatisation ;
- audit.

# NIVEAU M — ARCHITECTURE D’UN PRODUIT MODERNE

# 107\. ARCHITECTURE TYPE

Une application web moderne peut ressembler à :

USERS  
↓  
DNS / CDN / WAF  
↓  
FRONTEND  
↓  
API / BFF  
↓  
┌───────────┼───────────┐  
↓ ↓ ↓  
AUTH BUSINESS PAYMENTS  
↓  
DATABASE  
/ \\  
↓ ↓  
CACHE STORAGE  
↓  
QUEUES  
↓  
WORKERS  
↓  
EMAIL / EXTERNAL APIs

Transversalement :

SECURITY  
OBSERVABILITY  
CI/CD  
BACKUPS  
MONITORING

# 108\. BFF — BACKEND FOR FRONTEND

Backend spécialisé pour les besoins d’un frontend particulier.

Utile lorsque :

- plusieurs clients ont des besoins différents ;
- l’API générale n’est pas adaptée ;
- aggregation de données nécessaire.

# 109\. API GATEWAY

Point d’entrée pouvant gérer :

- routage ;
- authentification ;
- rate limiting ;
- transformation ;
- observabilité.

Mais il peut aussi devenir :

un point de complexité ou un bottleneck.

# 110\. RATE LIMITING

Limiter le nombre de requêtes autorisées sur une période.

Objectifs :

- protection ;
- équité ;
- maîtrise des coûts ;
- prévention d’abus.

# NIVEAU N — SaaS ET ARCHITECTURE MULTI-TENANT

# 111\. TENANT

Un tenant représente généralement un client organisationnel ou un espace isolé dans un SaaS.

Exemple :

SaaS  
├── Tenant A  
│ ├── User 1  
│ └── User 2  
│  
├── Tenant B  
│ ├── User 3  
│ └── User 4

# 112\. MULTI-TENANCY

Architecture permettant à plusieurs clients de partager une infrastructure tout en maintenant leur isolation logique.

# 113\. MODÈLES DE MULTI-TENANCY

### Shared database / shared schema

Tous les tenants partagent :

- base ;
- tables.

Le tenant est identifié dans les lignes.

### Shared database / separate schema

Chaque tenant dispose d’un schéma distinct.

### Separate database

Chaque tenant possède une base séparée.

# 114\. COMPROMIS MULTI-TENANT

### Partagé

Avantages :

- coût ;
- simplicité opérationnelle.

Risques :

- isolation ;
- blast radius ;
- complexité des requêtes.

### Séparé

Avantages :

- isolation ;
- personnalisation.

Coûts :

- infrastructure ;
- migrations ;
- maintenance.

# 115\. RBAC

**Role-Based Access Control**

Permissions associées à des rôles.

Exemple :

Admin  
Manager  
Member  
Viewer

# 116\. ABAC

**Attribute-Based Access Control**

Décisions basées sur des attributs :

- utilisateur ;
- ressource ;
- contexte ;
- organisation ;
- localisation ;
- heure.

# 117\. ENTITLEMENTS

Définissent ce qu’un client a le droit d’utiliser selon :

- plan ;
- abonnement ;
- rôle ;
- licence.

Exemple :

Free → 3 projets  
Pro → 50 projets  
Enterprise → illimité

# NIVEAU O — ARCHITECTURE DES INTÉGRATIONS

# 118\. THIRD-PARTY SERVICE

Service externe utilisé par ton système.

Exemples :

- paiement ;
- email ;
- SMS ;
- stockage ;
- analytics ;
- IA.

# 119\. LE PROBLÈME DE LA DÉPENDANCE EXTERNE

Si ton système dépend d’un fournisseur :

- il peut tomber ;
- changer son API ;
- augmenter ses prix ;
- limiter l’usage ;
- modifier ses conditions.

Il faut donc réfléchir à :

- abstraction ;
- timeout ;
- retry ;
- fallback ;
- monitoring ;
- migration.

# 120\. WEBHOOK

Une application externe informe ton système qu’un événement s’est produit.

Exemple :

Payment Provider  
↓  
POST /webhook  
↓  
Your Backend

# 121\. WEBHOOK ≠ API POLLING

### Polling

Ton système demande régulièrement :

« Est-ce que quelque chose a changé ? »

### Webhook

Le fournisseur dit :

« Quelque chose vient de changer. »

# 122\. IDEMPOTENCE DES WEBHOOKS

Un webhook peut être envoyé plusieurs fois.

Le système doit donc éviter :

même événement → paiement traité deux fois.

# NIVEAU P — ARCHITECTURE DES APPLICATIONS IA

# 123\. APPLICATION IA

Une application IA n’est pas nécessairement :

modèle IA seul.

Elle peut être :

User  
↓  
Frontend  
↓  
Backend  
↓  
Prompt / Orchestration  
↓  
Model  
↓  
Tools / Retrieval  
↓  
Validation  
↓  
Response

# 124\. RAG

**Retrieval-Augmented Generation**

Architecture dans laquelle le système récupère des informations avant de les fournir au modèle.

Question  
↓  
Retrieval  
↓  
Documents  
↓  
Context  
↓  
Model  
↓  
Answer

# 125\. VECTOR DATABASE

Stocke notamment des représentations vectorielles permettant des recherches par similarité.

Mais :

une vector database n’est pas automatiquement nécessaire pour toute application IA.

# 126\. AGENT

Système capable de :

- raisonner sur une tâche ;
- utiliser des outils ;
- observer des résultats ;
- poursuivre plusieurs étapes.

Plus l’autonomie augmente :

plus les risques et besoins de contrôle augmentent.

# 127\. AI GATEWAY / MODEL ROUTER

Dans certaines architectures, une couche peut gérer :

- sélection du modèle ;
- quotas ;
- coûts ;
- fallback ;
- logs ;
- sécurité ;
- routage.

# 128\. MODEL FALLBACK

Si un modèle échoue ou devient indisponible :

Model A  
↓ échec  
Model B  
↓  
Response

Mais cela peut entraîner :

- différences de qualité ;
- différences de coûts ;
- différences de comportement.

# NIVEAU Q — ARCHITECTURE ET PERFORMANCE

# 129\. PERFORMANCE BUDGET

Définir des limites avant de construire.

Exemples :

- temps de réponse ;
- taille JavaScript ;
- mémoire ;
- coût ;
- nombre de requêtes.

# 130\. N+1 QUERY

Problème où une requête principale déclenche ensuite de nombreuses requêtes supplémentaires.

Exemple :

1 query users  
+  
100 queries projects  
\=  
101 queries

# 131\. DATABASE BOTTLENECK

Une base peut devenir le facteur limitant à cause de :

- mauvaises requêtes ;
- absence d’index ;
- trop de connexions ;
- volume ;
- contention ;
- architecture de données.

# 132\. CACHE STRATEGY

Il faut déterminer :

- quoi mettre en cache ;
- combien de temps ;
- qui invalide ;
- que faire en cas de cache miss ;
- comment éviter les données obsolètes.

# NIVEAU R — ARCHITECTURE ET COÛT

# 133\. TECHNICAL COST

Une architecture doit être évaluée selon :

- infrastructure ;
- stockage ;
- compute ;
- réseau ;
- services externes ;
- maintenance ;
- temps développeur ;
- monitoring ;
- sécurité.

# 134\. PREMATURE OPTIMIZATION

Construire une architecture complexe pour un problème qui n’existe pas encore.

Exemple :

10 utilisateurs → Kubernetes + 15 microservices + Kafka + service mesh.

Ce n’est pas nécessairement mauvais techniquement.

Mais cela peut être disproportionné.

# 135\. ARCHITECTURAL FIT

Une bonne architecture est :

adaptée au contexte.

Pas :

technologiquement impressionnante.

# NIVEAU S — ARCHITECTURAL DECISION MAKING

# 136\. LES 8 QUESTIONS

Avant de choisir une architecture :

1.  Quel problème doit-elle résoudre ?
2.  Quelle charge ?
3.  Quelle équipe ?
4.  Quelles compétences ?
5.  Quelles contraintes ?
6.  Quel niveau de disponibilité ?
7.  Quel niveau de sécurité ?
8.  Quelle évolution probable ?

# 137\. BUILD VS BUY

### Build

Construire soi-même.

Avantages :

- contrôle ;
- personnalisation.

Coûts :

- temps ;
- maintenance ;
- expertise.

### Buy / Use

Utiliser une solution existante.

Avantages :

- rapidité ;
- expertise fournisseur.

Risques :

- dépendance ;
- coût ;
- limitation.

# 138\. MONOLITH VS MICROSERVICES

Décider selon :

- taille équipe ;
- complexité ;
- indépendance des domaines ;
- scaling ;
- déploiement ;
- maturité opérationnelle.

# 139\. SQL VS NOSQL

Question incorrecte :

« Quel est le meilleur ? »

Bonne question :

« Quel type de données et quelles opérations avons-nous ? »

SQL peut être privilégié lorsque :

- relations importantes ;
- transactions ;
- intégrité ;
- requêtes structurées.

NoSQL peut être intéressant lorsque :

- modèle spécifique ;
- flexibilité ;
- échelle ;
- patterns d’accès particuliers.

# 140\. SYNCHRONE VS ASYNCHRONE

Choisir l’asynchrone lorsque :

- l’utilisateur n’a pas besoin de réponse immédiate ;
- traitement long ;
- pics de charge ;
- découplage utile.

Éviter l’asynchrone lorsqu’il ajoute une complexité inutile.

# 141\. CACHE OU DATABASE ?

Le cache est utile lorsque :

- lecture répétée ;
- données relativement stables ;
- latence importante.

Ne pas utiliser un cache simplement parce que :

« le système doit être rapide ».

Il faut identifier le problème réel.

# NIVEAU T — DOCUMENTER L’ARCHITECTURE

# 142\. ARCHITECTURE DIAGRAM

Un diagramme peut représenter :

- composants ;
- flux ;
- frontières ;
- dépendances.

# 143\. C4 MODEL

Le modèle C4 propose plusieurs niveaux de représentation :

- Context ;
- Container ;
- Component ;
- Code.

L’intérêt est de ne pas mettre tous les détails dans un seul diagramme illisible.

# 144\. ADR

**Architecture Decision Record**

Document court expliquant une décision architecturale.

Structure :

Decision  
Context  
Options  
Decision  
Consequences

Exemple :

Pourquoi PostgreSQL plutôt que MongoDB ?

L’ADR permet de conserver :

pourquoi cette décision a été prise.

# 145\. ARCHITECTURAL PRINCIPLES

Une équipe peut définir des principes comme :

- security by default ;
- API versioning ;
- least privilege ;
- observability obligatoire ;
- migrations versionnées ;
- pas de secrets dans Git.

# 146\. TECHNICAL DEBT

Dette technique = coût futur créé par certains compromis techniques.

Elle peut provenir de :

- solution temporaire ;
- architecture inadéquate ;
- absence de tests ;
- documentation insuffisante ;
- dépendances obsolètes.

Attention :

dette technique ≠ code mauvais.

Certaines dettes sont intentionnelles et rationnelles.

# NIVEAU U — SYSTÈMES DISTRIBUÉS

# 147\. DISTRIBUTED SYSTEM

Un système distribué comporte plusieurs composants qui communiquent via un réseau.

Exemples :

- microservices ;
- systèmes cloud ;
- plateformes globales.

# 148\. LE RÉSEAU EST NON FIABLE

Dans un système distribué :

un appel réseau peut échouer.

Il peut :

- être lent ;
- être perdu ;
- être dupliqué ;
- arriver dans le désordre ;
- revenir après un délai.

Il faut donc concevoir avec ces possibilités.

# 149\. PARTITION

Une partie du système peut devenir temporairement incapable de communiquer avec une autre.

# 150\. CAP THEOREM

Dans certaines conditions de partition réseau, un système distribué doit faire des compromis entre certaines garanties de cohérence et de disponibilité.

Il ne faut pas réduire CAP à :

« on ne peut avoir que deux des trois ».

Le théorème concerne spécifiquement le comportement en présence de partition.

# 151\. EVENTUAL CONSISTENCY

Les différentes répliques peuvent temporairement avoir des états différents avant convergence.

Utile dans certains systèmes où :

disponibilité et performance sont prioritaires.

# NIVEAU V — OPÉRATIONS ET INCIDENTS

# 152\. INCIDENT

Événement qui dégrade ou interrompt un service.

# 153\. INCIDENT RESPONSE

Processus permettant de :

1.  détecter ;
2.  qualifier ;
3.  contenir ;
4.  corriger ;
5.  communiquer ;
6.  récupérer ;
7.  analyser.

# 154\. POSTMORTEM

Analyse après incident.

Une bonne culture cherche :

pourquoi le système a permis que cela arrive ?

plutôt que simplement :

qui a fait l’erreur ?

# 155\. BLAST RADIUS

Étendue des conséquences d’une panne ou d’une erreur.

Une bonne architecture cherche parfois à réduire le blast radius.

# 156\. DISASTER RECOVERY

Plan permettant de restaurer un système après une catastrophe importante.

# 157\. RTO

**Recovery Time Objective**

Temps cible pour restaurer le service.

# 158\. RPO

**Recovery Point Objective**

Quantité maximale de données que l’on accepte potentiellement de perdre selon le scénario.

# NIVEAU W — TESTER UNE ARCHITECTURE

# 159\. UNIT TEST

Teste une unité isolée.

# 160\. INTEGRATION TEST

Teste l’interaction entre plusieurs composants.

# 161\. END-TO-END

Teste un parcours proche de celui d’un utilisateur réel.

# 162\. LOAD TEST

Teste le comportement sous charge.

# 163\. STRESS TEST

Cherche notamment les limites du système en augmentant fortement la charge.

# 164\. CHAOS ENGINEERING

Introduire volontairement certaines défaillances pour vérifier la résilience.

À réserver à des environnements et organisations capables de le faire correctement.

# NIVEAU X — ARCHITECTURE ET ORGANISATION

# 165\. OWNERSHIP

Chaque composant important devrait avoir une responsabilité claire.

Question :

Qui est responsable de ce système ?

# 166\. BOUNDARIES ORGANISATIONNELLES

La manière dont une organisation est structurée influence parfois l’architecture.

Une architecture avec 20 services indépendants nécessite généralement davantage de coordination qu’un monolithe.

# 167\. TEAM TOPOLOGIES

Les équipes peuvent être organisées autour :

- d’un produit ;
- d’un domaine ;
- d’une plateforme ;
- d’une capacité.

L’objectif est de réduire les dépendances de coordination inutiles.

# 168\. TECH LEAD

Le Tech Lead guide notamment :

- décisions techniques ;
- cohérence du code ;
- architecture ;
- pratiques ;
- arbitrages techniques.

Il n’est pas nécessairement :

le chef hiérarchique de tous les développeurs.

# 169\. CTO

Le CTO porte généralement une responsabilité plus large sur :

- stratégie technologique ;
- organisation technique ;
- architecture ;
- recrutement ;
- risques ;
- direction technologique.

Dans une petite startup, une même personne peut être :

Founder + CTO + Tech Lead + Developer.

# NIVEAU Y — ARCHITECTURE ET IA

# 170\. L’IA COMME ARCHITECTE ASSISTANT

Une IA peut aider à :

- proposer des architectures ;
- comparer des options ;
- générer des diagrammes ;
- identifier des dépendances ;
- produire des ADR ;
- analyser les risques ;
- proposer des schémas ;
- générer du code ;
- produire des tests ;
- simuler des charges ;
- auditer une architecture.

Mais :

**une architecture générée par IA n’est pas automatiquement une architecture correcte.**

# 171\. LE DANGER DE L’ARCHITECTURE GÉNÉRIQUE

Prompt faible :

« Conçois l’architecture d’un SaaS moderne scalable. »

L’IA peut produire :

React  
Node  
Microservices  
Kubernetes  
Kafka  
Redis  
PostgreSQL  
Docker  
AWS  
CI/CD

Cela peut sembler professionnel.

Mais la vraie question est :

**Pourquoi chacun de ces composants est-il nécessaire ?**

# 172\. PROMPT ARCHITECTURAL STRUCTURÉ

Un bon brief doit préciser :

### CONTEXTE

Quel système ?

### UTILISATEURS

Combien ?

### TRAFIC

Quelle charge actuelle et prévue ?

### FONCTIONNALITÉS

Quelles fonctions principales ?

### DONNÉES

Quel volume ?

### DISPONIBILITÉ

Quel niveau attendu ?

### SÉCURITÉ

Quelles contraintes ?

### BUDGET

Quelle limite ?

### ÉQUIPE

Combien de développeurs ?

### COMPÉTENCES

Quelles technologies maîtrisées ?

### DÉLAI

Quelle échéance ?

### CONTRAINTES

Réglementation, fournisseur, localisation, etc.

### OBJECTIF

Rapidité ? coût ? scalabilité ? simplicité ?

# 173\. DEMANDER DES ALTERNATIVES

Ne pas demander seulement :

« Donne-moi l’architecture. »

Demander :

« Propose trois architectures : simple, intermédiaire et scalable. Compare-les selon coût, complexité, performance, sécurité, maintenance et capacité d’évolution. »

Cela transforme l’IA :

générateur de réponse

en :

assistant de décision.

# 174\. DEMANDER LES HYPOTHÈSES

Toujours demander :

« Liste explicitement toutes les hypothèses sur lesquelles tu bases cette architecture. »

Puis :

« Indique lesquelles sont vérifiées et lesquelles sont seulement supposées. »

# 175\. DEMANDER LES NON-GOALS

Exemple :

« Qu’est-ce que cette architecture ne cherche volontairement pas à optimiser ? »

Cette question permet d’éviter :

optimisation inutile.

# 176\. DEMANDER LE FAILURE MODE ANALYSIS

Demander :

« Pour chaque composant critique, que se passe-t-il s’il tombe, ralentit ou renvoie des données incorrectes ? »

# 177\. DEMANDER LE PLAN D’ÉVOLUTION

Une architecture doit répondre :

« Que se passe-t-il lorsque le système passe de 100 à 100 000 utilisateurs ? »

Mais également :

« Qu’est-ce qui n’a pas besoin d’être construit maintenant ? »

# NIVEAU Z — AUDIT D’UNE ARCHITECTURE

# 178\. AUDIT FONCTIONNEL

Demander :

- toutes les exigences sont-elles couvertes ?
- les flux principaux existent-ils ?
- les cas d’erreur sont-ils prévus ?

# 179\. AUDIT DE COMPLEXITÉ

Pour chaque composant :

Pourquoi existe-t-il ?

Si la réponse est :

« parce que c’est une bonne pratique »

ce n’est pas suffisant.

# 180\. AUDIT DES DÉPENDANCES

Identifier :

- dépendances externes ;
- dépendances internes ;
- dépendances circulaires ;
- fournisseurs critiques.

# 181\. AUDIT DE SÉCURITÉ

Vérifier :

- auth ;
- permissions ;
- secrets ;
- chiffrement ;
- isolation ;
- validation ;
- rate limiting ;
- logs ;
- surface d’attaque.

# 182\. AUDIT DE PERFORMANCE

Identifier :

- bottlenecks ;
- appels réseau ;
- requêtes ;
- cache ;
- taille des payloads ;
- traitements lourds.

# 183\. AUDIT DE FIABILITÉ

Vérifier :

- single points of failure ;
- retries ;
- timeouts ;
- backups ;
- recovery ;
- monitoring ;
- rollback.

# 184\. AUDIT DES COÛTS

Calculer ou estimer :

- infrastructure ;
- services externes ;
- stockage ;
- réseau ;
- maintenance ;
- temps humain.

# 185\. AUDIT D’ÉVOLUTIVITÉ

Question centrale :

« Si les besoins changent, quelle partie du système sera la plus difficile à modifier ? »

# 186\. AUDIT OPÉRATIONNEL

Question :

« Peut-on réellement exploiter cette architecture avec l’équipe disponible ? »

Une architecture peut être excellente sur le papier et impossible à maintenir par l’équipe.

# 187\. AUDIT IA FINAL

Lorsqu’une IA propose une architecture, vérifier :

PROBLÈME  
↓  
HYPOTHÈSES  
↓  
CONTRAINTES  
↓  
ARCHITECTURE  
↓  
ALTERNATIVES  
↓  
COMPROMIS  
↓  
RISQUES  
↓  
COÛTS  
↓  
PLAN DE TEST  
↓  
PLAN D'ÉVOLUTION

# NIVEAU AA — GRANDES CONFUSIONS À ÉLIMINER

## Architecture ≠ Stack

La stack = technologies choisies.

L’architecture = organisation du système.

## Backend ≠ Architecture

Le backend est une partie du système.

## API ≠ Backend

Une API est une interface de communication.

## REST ≠ API

REST est un style architectural utilisé pour concevoir certaines API.

## Database ≠ Storage

Une base de données et un stockage de fichiers répondent à des besoins différents.

## Docker ≠ Virtual Machine

Les deux isolent des environnements mais fonctionnent différemment.

## Docker ≠ Kubernetes

Docker sert notamment à construire/exécuter des conteneurs.

Kubernetes orchestre des workloads conteneurisés.

## Cloud ≠ Internet

Le cloud fournit des ressources/services informatiques.

Internet est un réseau mondial interconnecté.

## Scalability ≠ Performance

Performance :

à quelle vitesse fonctionne le système ?

Scalabilité :

comment se comporte-t-il lorsque la charge augmente ?

## Availability ≠ Reliability

Availability :

le service est-il disponible ?

Reliability :

fonctionne-t-il correctement de manière durable ?

## Authentication ≠ Authorization

Authentication :

qui es-tu ?

Authorization :

qu’as-tu le droit de faire ?

## Cache ≠ Database

Le cache accélère l’accès.

La base constitue généralement une source de données persistante selon le système.

## Microservices ≠ Scalabilité automatique

Les microservices peuvent faciliter certains types de scaling mais n’apportent pas automatiquement de meilleure scalabilité.

## Serverless ≠ Sans serveur

Le serveur existe toujours.

Le fournisseur prend simplement davantage de responsabilités d’infrastructure.

## Monolithe ≠ Mauvaise architecture

Un monolithe bien conçu peut être excellent.

## Distributed ≠ Better

Distribuer un système ajoute :

réseau + latence + pannes + complexité.

# NIVEAU AB — ARCHITECTURE MINIMALE D’UN PROJET

# 188\. PETIT PROJET WEB

Une architecture simple peut être :

User  
↓  
Frontend  
↓  
Backend/API  
↓  
PostgreSQL

Et éventuellement :

┌── Auth  
├── Storage  
├── Email  
└── Payment

Pas besoin automatiquement de :

- Kubernetes ;
- microservices ;
- Kafka ;
- service mesh ;
- event bus complexe.

# 189\. PROJET SAAS

Architecture possible :

Users  
↓  
Frontend  
↓  
API  
├── Auth  
├── Users  
├── Billing  
├── Product  
└── Notifications  
↓  
PostgreSQL  
↓  
Queue/Workers  
↓  
External Services

Transversalement :

Logging  
Monitoring  
Security  
Backups  
CI/CD

# 190\. APPLICATION IA

Architecture possible :

User  
↓  
Frontend  
↓  
Backend  
↓  
Orchestrator  
├── Model  
├── Retrieval  
├── Tools  
└── Guardrails  
↓  
Response

# NIVEAU AC — LE SYSTÈME COMME ENSEMBLE

# 191\. LA VISION EN COUCHES

Pour analyser n’importe quel système, regarder successivement :

### 1\. Business

Pourquoi le système existe-t-il ?

### 2\. User

Qui l’utilise ?

### 3\. Functional

Que doit-il faire ?

### 4\. Domain

Quelles sont les règles métier ?

### 5\. Application

Comment les fonctionnalités sont-elles organisées ?

### 6\. Data

Quelles données existent ?

### 7\. Integration

Avec quels systèmes communique-t-il ?

### 8\. Infrastructure

Où s’exécute-t-il ?

### 9\. Security

Qui peut accéder à quoi ?

### 10\. Operations

Comment le système est-il déployé et surveillé ?

### 11\. Evolution

Comment changera-t-il ?

# 192\. LE MODÈLE « FLUX »

Pour chaque fonctionnalité importante, suivre :

USER ACTION  
↓  
REQUEST  
↓  
NETWORK  
↓  
API  
↓  
AUTHORIZATION  
↓  
BUSINESS LOGIC  
↓  
DATABASE / SERVICE  
↓  
RESPONSE  
↓  
USER

Puis demander :

Que se passe-t-il si chaque étape échoue ?

# 193\. LE MODÈLE « DONNÉE »

Pour chaque donnée importante :

CREATION  
↓  
VALIDATION  
↓  
STORAGE  
↓  
ACCESS  
↓  
TRANSFORMATION  
↓  
TRANSMISSION  
↓  
BACKUP  
↓  
DELETION

Questions :

- Qui peut la créer ?
- Qui peut la lire ?
- Qui peut la modifier ?
- Où est-elle stockée ?
- Combien de temps ?
- Est-elle sensible ?
- Peut-elle être supprimée ?
- Peut-elle être exportée ?

# 194\. LE MODÈLE « PANNE »

Pour chaque composant critique :

COMPONENT  
↓  
FAILURE  
↓  
DETECTION  
↓  
IMPACT  
↓  
CONTAINMENT  
↓  
RECOVERY  
↓  
LEARNING

# NIVEAU AD — PRINCIPES ARCHITECTURAUX À RETENIR

# 195\. SIMPLICITÉ

La meilleure architecture n’est pas celle qui contient le plus de technologies.

# 196\. EXPLICITE

Les responsabilités et dépendances importantes doivent être compréhensibles.

# 197\. MODULARITÉ

Les parties doivent pouvoir évoluer avec un minimum de perturbation.

# 198\. AUTOMATISATION

Tout processus répétitif et fiable peut progressivement être automatisé.

# 199\. OBSERVABILITÉ

Un système que l’on ne peut pas comprendre lorsqu’il tombe est difficile à exploiter.

# 200\. SÉCURITÉ

La sécurité doit être considérée comme une propriété architecturale.

# 201\. RÉSILIENCE

Prévoir les échecs, pas uniquement le scénario idéal.

# 202\. MESURE

Ne pas optimiser sans mesurer.

# 203\. CONTEXTE

Une architecture doit être jugée par rapport à :

- problème ;
- équipe ;
- budget ;
- charge ;
- risques ;
- évolution.

# 204\. ÉVOLUTION

Une architecture doit pouvoir évoluer sans exiger systématiquement une reconstruction complète.

# NIVEAU AE — MASTER MENTAL MODEL

# 205\. LA FORMULE FINALE

Pour analyser un système :

**POURQUOI ?**

Pourquoi existe-t-il ?

↓

**QUI ?**

Qui l’utilise ?

↓

**QUOI ?**

Que doit-il faire ?

↓

**QUELLES RÈGLES ?**

Quelle logique métier ?

↓

**QUELLES DONNÉES ?**

Que doit-on stocker ?

↓

**QUELS COMPOSANTS ?**

Quelles responsabilités ?

↓

**QUELLES FRONTIÈRES ?**

Où séparer ?

↓

**QUELS FLUX ?**

Comment les composants communiquent-ils ?

↓

**QUELLES DÉPENDANCES ?**

De quoi dépend chaque partie ?

↓

**QUELLES PANNES ?**

Que se passe-t-il lorsque quelque chose échoue ?

↓

**QUELLE SÉCURITÉ ?**

Qui peut faire quoi ?

↓

**QUELLE PERFORMANCE ?**

Quelle charge et quelle latence ?

↓

**QUELLE ÉVOLUTIVITÉ ?**

Comment le système grandira-t-il ?

↓

**QUELLE EXPLOITATION ?**

Comment le déployer, surveiller et réparer ?

↓

**QUEL COÛT ?**

Combien coûte cette architecture à construire et maintenir ?

↓

**QUEL COMPROMIS ?**

Qu’est-ce qu’on gagne et qu’est-ce qu’on sacrifie ?

# 206\. ARCHITECTURE COMME SYSTÈME DE COMPROMIS

Il n’existe presque jamais de solution parfaite.

Une décision peut améliorer :

performance

mais augmenter :

coût.

Une autre peut améliorer :

simplicité

mais limiter :

flexibilité.

Une autre peut améliorer :

disponibilité

mais augmenter :

complexité.

Une autre peut améliorer :

sécurité

mais ajouter :

friction utilisateur.

La compétence architecturale consiste donc moins à mémoriser des technologies qu’à comprendre :

**les compromis.**

# 207\. MATRICE DE DÉCISION ARCHITECTURALE

Pour comparer deux solutions :

| Critère | Solution A | Solution B |
| --- | --- | --- |
| Complexité |     |     |
| Coût |     |     |
| Performance |     |     |
| Scalabilité |     |     |
| Sécurité |     |     |
| Fiabilité |     |     |
| Maintenance |     |     |
| Compétences nécessaires |     |     |
| Vitesse de développement |     |     |
| Dépendance fournisseur |     |     |
| Évolutivité |     |     |
| Observabilité |     |     |
| Risque |     |     |

La meilleure solution n’est pas celle qui obtient :

« 10/10 partout ».

Elle est celle qui correspond le mieux au contexte.

# 208\. CHECKLIST ARCHITECTURALE

Avant de considérer une architecture comme prête :

## Compréhension

- objectif clair
- utilisateurs identifiés
- exigences fonctionnelles
- exigences non fonctionnelles

## Structure

- composants identifiés
- responsabilités claires
- frontières claires
- dépendances comprises

## Données

- modèle défini
- stockage choisi
- intégrité
- sauvegarde
- rétention

## Sécurité

- authentication
- authorization
- isolation
- secrets
- chiffrement
- rate limiting

## Performance

- latence
- charge
- bottlenecks
- cache si nécessaire
- database

## Fiabilité

- timeouts
- retries
- idempotence
- monitoring
- backups
- recovery
- rollback

## Déploiement

- environnements
- CI
- CD
- configuration
- secrets
- migrations

## Observabilité

- logs
- metrics
- traces si nécessaire
- alertes
- dashboards

## Évolution

- scaling prévu
- dépendances identifiées
- dette technique
- décisions documentées

## Économie

- infrastructure
- services externes
- coût d’exploitation
- coût humain

# 209\. VOCABULAIRE ESSENTIEL À SAVOIR RECONNAÎTRE

## Architecture

- architecture
- system
- component
- module
- service
- interface
- dependency
- coupling
- cohesion
- abstraction
- encapsulation
- boundary
- separation of concerns

## Application

- frontend
- backend
- API
- REST
- GraphQL
- gRPC
- BFF
- API Gateway
- middleware

## Architecture

- monolith
- modular monolith
- microservices
- serverless
- layered architecture
- clean architecture
- hexagonal architecture
- DDD
- event-driven architecture

## Data

- SQL
- NoSQL
- schema
- index
- transaction
- ACID
- replication
- sharding
- cache
- object storage
- consistency

## Distributed Systems

- queue
- event
- message broker
- asynchronous
- synchronous
- retry
- timeout
- idempotency
- circuit breaker
- backpressure
- eventual consistency
- CAP

## Infrastructure

- server
- VM
- container
- Docker
- Kubernetes
- cloud
- IaaS
- PaaS
- SaaS
- IaC

## Network

- DNS
- IP
- HTTP
- HTTPS
- TLS
- CDN
- load balancer
- latency
- throughput
- bandwidth

## Reliability

- availability
- reliability
- resilience
- redundancy
- fault tolerance
- SPOF
- RTO
- RPO
- disaster recovery
- incident
- postmortem
- blast radius

## DevOps

- Git
- CI
- CD
- pipeline
- deployment
- rollback
- canary
- blue-green
- feature flag
- environment

## Observability

- log
- metric
- trace
- monitoring
- alert
- dashboard
- telemetry

## Security

- authentication
- authorization
- least privilege
- zero trust
- secret
- encryption
- isolation
- trust boundary
- WAF
- rate limiting

## SaaS

- tenant
- multi-tenancy
- RBAC
- ABAC
- entitlement
- subscription
- billing
- isolation

## AI Systems

- model
- inference
- prompt
- embedding
- vector database
- RAG
- agent
- tool calling
- orchestration
- model routing
- guardrail
- evaluation

# 210\. PROGRESSION DE MAÎTRISE

## Niveau 1 — RECONNAÎTRE

Tu sais que :

« microservices », « API Gateway », « queue », « cache », « CDN », « Kubernetes », « RAG » existent.

## Niveau 2 — EXPLIQUER

Tu peux dire :

ce qu’ils sont.

## Niveau 3 — IDENTIFIER LE BESOIN

Tu peux reconnaître :

« ici, une queue pourrait résoudre ce problème. »

## Niveau 4 — COMPARER

Tu peux expliquer :

monolithe vs microservices.

## Niveau 5 — CHOISIR

Tu peux justifier :

« pour ce contexte, je choisirais le monolithe. »

## Niveau 6 — CONCEVOIR AVEC ASSISTANCE

Tu peux demander à l’IA :

« propose une architecture adaptée à ces contraintes. »

## Niveau 7 — AUDITER

Tu peux repérer :

complexité inutile, risques, dépendances, failles et hypothèses.

## Niveau 8 — IMPLÉMENTER

Tu peux construire progressivement certaines parties.

## Niveau 9 — APPROFONDIR

Tu peux étudier :

- systèmes distribués ;
- cloud ;
- réseaux ;
- bases avancées ;
- fiabilité ;
- sécurité ;
- architecture logicielle.

# 211\. CARTE DE MAÎTRISE

PROBLÈME  
↓  
BESOIN  
↓  
EXIGENCES  
↓  
CONTRAINTES  
↓  
ARCHITECTURE  
↓  
┌────────────┼────────────┐  
↓ ↓ ↓  
DONNÉES SERVICES RÉSEAU  
│ │ │  
└────────────┼────────────┘  
↓  
INFRASTRUCTURE  
↓  
DÉPLOIEMENT  
↓  
OBSERVABILITÉ  
↓  
SÉCURITÉ  
↓  
PERFORMANCE  
↓  
FIABILITÉ  
↓  
ÉVOLUTION  
↓  
AUDIT

# 212\. INTÉGRATION AVEC LES SEPT AUTRES DOMAINES

Architecture & Systems constitue une couche transversale.

## Web & Software Engineering

Architecture organise la manière dont le logiciel est structuré.

Architecture  
↓  
Software  
↓  
Code

## UX/UI & Design

L’architecture technique doit soutenir l’expérience utilisateur.

Exemple :

une excellente interface qui dépend d’une API extrêmement lente produit une mauvaise expérience.

## Cybersécurité

La sécurité dépend profondément de l’architecture :

frontières → permissions → flux → données → isolation → secrets.

## SEO & Performance

Architecture influence :

- rendu ;
- temps de réponse ;
- cache ;
- CDN ;
- disponibilité ;
- crawlabilité.

## AI / ML / Intelligent Systems

Les modèles sont seulement une partie d’une application IA.

Product  
↓  
Application  
↓  
AI Architecture  
↓  
Model

## Product / SaaS / Startup

Les décisions produit imposent des contraintes architecturales.

Exemple :

SaaS multi-tenant → isolation → permissions → billing → entitlements → données.

## Branding / Marketing / Personal Branding

Architecture peut soutenir :

- disponibilité ;
- vitesse ;
- analytics ;
- formulaires ;
- CRM ;
- automatisation ;
- intégrations.

# 213\. LE MODÈLE FINAL DES HUIT DOMAINES

Les huit documents peuvent maintenant être compris comme un système.

PROBLÈME / OBJECTIF  
↓  
┌────────────┴────────────┐  
↓ ↓  
UTILISATEUR BUSINESS  
↓ ↓  
UX / UI PRODUCT  
↓ ↓  
WEB / SOFTWARE MARKETING  
↓ ↓  
ARCHITECTURE ←──────────────→ BRANDING  
↓  
CYBERSÉCURITÉ  
↓  
PERFORMANCE / SEO  
↓  
IA  
↓  
SYSTÈME

Une autre lecture :

COMPRENDRE LE BESOIN  
↓  
CONCEVOIR L'EXPÉRIENCE  
↓  
DÉFINIR LE PRODUIT  
↓  
CONSTRUIRE LE LOGICIEL  
↓  
ORGANISER LE SYSTÈME  
↓  
SÉCURISER  
↓  
RENDRE VISIBLE  
↓  
ATTIRER / CONVERTIR  
↓  
MESURER / APPRENDRE  
↓  
ÉVOLUER

# 214\. CE QUE TU DOIS ÊTRE CAPABLE DE FAIRE APRÈS LES 8 DOCUMENTS

L’objectif final n’est pas :

connaître toutes les technologies.

Il est de pouvoir regarder un projet et demander :

### Produit

Quel problème résout-il ?

### Utilisateur

Pour qui ?

### UX

Comment cette personne interagit-elle avec lui ?

### Business

Comment crée-t-il et capture-t-il de la valeur ?

### Branding

Comment est-il perçu ?

### Marketing

Comment les utilisateurs le découvrent-ils ?

### Software

Comment est-il construit ?

### Architecture

Comment ses composants sont-ils organisés ?

### Data

Quelles informations circulent et où sont-elles stockées ?

### Security

Qui peut accéder à quoi ?

### Performance

Où sont les bottlenecks ?

### Reliability

Que se passe-t-il lorsqu’une partie tombe ?

### AI

Où l’intelligence artificielle apporte-t-elle réellement de la valeur ?

### Operations

Comment déployer, surveiller et maintenir le système ?

# 215\. LA COMPÉTENCE SUPÉRIEURE : PENSER EN SYSTÈMES

La véritable compétence recherchée par cette série de documents est la suivante :

**ne plus regarder une technologie isolément.**

Ne plus penser :

« Je connais React. »

Mais :

« React est une technologie de présentation dans un système plus large. »

Ne plus penser :

« Je veux utiliser Redis. »

Mais :

« Quel problème de lecture, de latence ou de synchronisation justifierait Redis ? »

Ne plus penser :

« Je veux des microservices. »

Mais :

« Quelles frontières de domaine, contraintes de déploiement ou besoins de scaling justifieraient cette distribution ? »

Ne plus penser :

« Je veux utiliser Kubernetes. »

Mais :

« Quelle complexité opérationnelle avons-nous réellement besoin de résoudre ? »

Ne plus penser :

« L’IA m’a donné une architecture professionnelle. »

Mais :

« Quelles hypothèses, contraintes, preuves et compromis justifient cette architecture ? »

# 216\. FORMULE FINALE

Pour toute architecture :

**PROBLÈME → EXIGENCES → CONTRAINTES → COMPOSANTS → RESPONSABILITÉS → FRONTIÈRES → FLUX → DONNÉES → DÉPENDANCES → SÉCURITÉ → PERFORMANCE → FIABILITÉ → OBSERVABILITÉ → COÛT → ÉVOLUTION → COMPROMIS**

Et pour toute décision architecturale :

**POURQUOI ?**

avant :

**COMMENT ?**

et surtout avant :

**QUELLE TECHNOLOGIE ?**

# 217\. CONCLUSION

L’architecture n’est pas l’art de rendre un projet complexe.

C’est l’art de **structurer la complexité nécessaire tout en évitant la complexité inutile**.

Un bon architecte ne cherche donc pas systématiquement :

- le framework le plus moderne ;
- le cloud le plus puissant ;
- le plus grand nombre de services ;
- la meilleure base de données ;
- le plus grand niveau de scalabilité.

Il cherche :

**la solution la plus adaptée aux contraintes du système.**

La compétence fondamentale devient alors :

**comprendre le système avant de choisir les outils.**

Et dans un environnement où l’IA peut désormais générer une grande quantité de code et proposer des architectures en quelques secondes, cette compétence devient encore plus importante.

L’humain doit pouvoir dire :

« Cette architecture répond à mon problème. »

ou :

« Cette architecture est inutilement complexe. »

ou :

« Cette dépendance crée un risque. »

ou :

« Cette partie n’est pas suffisamment sécurisée. »

ou :

« Ce choix ne correspond pas à notre charge actuelle. »

ou :

« Cette décision sera difficile à inverser. »

ou :

« L’IA suppose quelque chose que nous n’avons jamais vérifié. »

La maîtrise recherchée n’est donc pas la mémorisation de centaines de technologies.

C’est la capacité à :

**LIRE → MODÉLISER → QUESTIONNER → COMPARER → DÉCIDER → CONCEVOIR → CONSTRUIRE → MESURER → AUDITER → FAIRE ÉVOLUER.**

C’est cette capacité qui transforme progressivement une personne qui **utilise des technologies** en une personne capable de **comprendre, concevoir et piloter des systèmes technologiques.**