# AI-AUGMENTED TECHNICAL LITERACY

# DOCUMENT 01 — WEB & SOFTWARE ENGINEERING

**Version : 1.0 — Document de référence**

## 0\. Positionnement du document

### Objectif

Ce document constitue une **carte générale du Web et du Software Engineering**.

Il ne cherche pas à transformer immédiatement le lecteur en expert de chaque technologie, langage, framework ou architecture.

Son objectif est différent :

**Comprendre suffisamment le territoire du développement logiciel pour reconnaître les concepts, comprendre les problèmes qu’ils résolvent, identifier quand ils deviennent pertinents, comparer les solutions possibles, choisir une direction cohérente, demander à une IA de l’implémenter correctement et contrôler son résultat.**

La compétence recherchée est donc une forme de **littératie technique augmentée par l’IA**.

# 1\. La compétence cible

Pour chaque concept rencontré, l’objectif final est de pouvoir passer progressivement par cette chaîne :

**Reconnaître → Comprendre → Identifier le besoin → Choisir → Diriger l’IA → Contrôler → Approfondir → Pratiquer**

### 1.1 Reconnaître

Je vois le terme et je sais au moins dans quelle famille il se situe.

Exemple :

« PWA »

Je sais que cela concerne le Web, les applications web et certaines capacités proches du natif.

### 1.2 Comprendre

Je peux expliquer simplement :

- ce que c’est ;
- pourquoi cela existe ;
- quel problème cela résout ;
- ce que cela permet ;
- ce que cela ne permet pas bien.

### 1.3 Identifier le besoin

Je peux reconnaître une situation dans laquelle le concept devient pertinent.

Exemple :

« L’application doit pouvoir fonctionner avec une connexion intermittente et être installable depuis le Web. »

Je commence à penser :

PWA / stratégies offline / service worker / cache.

### 1.4 Choisir

Je peux comparer plusieurs solutions.

Exemple :

Site classique ? PWA ? application mobile native ? Flutter ? React Native ?

Je ne choisis plus uniquement parce que :

« C’est la technologie que j’utilise habituellement. »

Je choisis en fonction des contraintes.

### 1.5 Diriger l’IA

Je peux donner à l’IA :

- le contexte ;
- les contraintes ;
- l’architecture souhaitée ;
- les exigences fonctionnelles ;
- les exigences non fonctionnelles ;
- les technologies imposées ou interdites ;
- les critères de qualité ;
- les critères de vérification.

### 1.6 Contrôler

Je peux demander :

« Pourquoi as-tu choisi cette architecture ? »

« Quels sont les risques ? »

« Comment puis-je tester cette implémentation ? »

« Quelle hypothèse technique pourrais-tu avoir mal comprise ? »

« Comment vérifier que cette authentification est réellement sécurisée ? »

L’IA cesse alors d’être une autorité.

Elle devient un **collaborateur technique qu’il faut superviser**.

# 2\. Niveaux de lecture du document

Le document est organisé autour de plusieurs niveaux.

## Niveau A — Vue globale

Comprendre les grandes familles du Web et du Software Engineering.

## Niveau B — Concepts essentiels

Connaître les notions fondamentales qu’un développeur ou un responsable technique doit reconnaître.

## Niveau C — Technologies et outils

Savoir situer les technologies et comprendre leur rôle.

## Niveau D — Comparaisons

Comprendre pourquoi plusieurs technologies existent et dans quelles situations elles diffèrent.

## Niveau E — Décisions

Savoir répondre à :

« Dans cette situation, quelle solution est raisonnable ? »

## Niveau F — Interaction avec l’IA

Savoir demander, cadrer et faire produire du logiciel par une IA.

## Niveau G — Contrôle et audit

Savoir vérifier le résultat produit par l’IA.

# PARTIE I — NIVEAU A

# CARTOGRAPHIE DU WEB & DU SOFTWARE ENGINEERING

# 3\. Qu’est-ce que le Software Engineering ?

Le **Software Engineering**, ou ingénierie logicielle, désigne l’ensemble des pratiques permettant de concevoir, construire, tester, déployer, maintenir et faire évoluer des logiciels de manière organisée et fiable.

Il ne s’agit donc pas simplement de :

« savoir programmer ».

La programmation est une partie du travail.

L’ingénierie logicielle ajoute notamment :

- l’analyse des besoins ;
- la conception ;
- l’architecture ;
- la gestion du code ;
- les tests ;
- la sécurité ;
- la performance ;
- le déploiement ;
- la maintenance ;
- la documentation ;
- la collaboration ;
- l’observabilité ;
- la gestion des versions ;
- la gestion des dépendances ;
- la qualité ;
- les compromis techniques.

# 4\. Les grandes familles

Le territoire peut être représenté ainsi :

WEB & SOFTWARE ENGINEERING  
│  
├── 1. Fondations informatiques  
│ ├── Algorithmes  
│ ├── Structures de données  
│ ├── Logique  
│ ├── Complexité  
│ └── Programmation  
│  
├── 2. Web  
│ ├── HTTP  
│ ├── DNS  
│ ├── URL  
│ ├── Navigateurs  
│ ├── HTML  
│ ├── CSS  
│ ├── JavaScript  
│ └── Web APIs  
│  
├── 3. Frontend  
│ ├── UI  
│ ├── DOM  
│ ├── State  
│ ├── Routing  
│ ├── Components  
│ ├── Frameworks  
│ └── Performance  
│  
├── 4. Backend  
│ ├── Serveurs  
│ ├── APIs  
│ ├── Business logic  
│ ├── Authentification  
│ ├── Autorisation  
│ └── Background jobs  
│  
├── 5. Données  
│ ├── SQL  
│ ├── NoSQL  
│ ├── PostgreSQL  
│ ├── MySQL  
│ ├── Redis  
│ ├── Cache  
│ └── Migrations  
│  
├── 6. Architecture  
│ ├── Monolithe  
│ ├── Modular monolith  
│ ├── Microservices  
│ ├── Serverless  
│ ├── Event-driven  
│ └── Distributed systems  
│  
├── 7. Mobile / multiplateforme  
│ ├── Native  
│ ├── Flutter  
│ ├── React Native  
│ └── PWA  
│  
├── 8. Qualité  
│ ├── Tests  
│ ├── Linting  
│ ├── Formatting  
│ ├── Code review  
│ └── CI/CD  
│  
├── 9. Déploiement  
│ ├── Hosting  
│ ├── Cloud  
│ ├── Containers  
│ ├── Docker  
│ └── Infrastructure  
│  
└── 10. Maintenance  
├── Monitoring  
├── Logging  
├── Observability  
├── Updates  
├── Refactoring  
└── Technical debt

Cette carte est plus importante que la mémorisation de dizaines de noms de technologies.

# 5\. La distinction fondamentale : langage, framework, bibliothèque, outil

Cette distinction est indispensable.

## 5.1 Langage de programmation

Un langage permet d’exprimer des instructions et des algorithmes.

Exemples :

- JavaScript ;
- TypeScript ;
- Python ;
- Java ;
- C ;
- C++ ;
- C# ;
- Go ;
- Rust ;
- Dart ;
- PHP ;
- Kotlin ;
- Swift.

## 5.2 Langage de balisage

HTML n’est pas un langage de programmation.

HTML décrit la structure et la sémantique d’un document.

Exemple :

&lt;h1&gt;Titre&lt;/h1&gt;  
&lt;p&gt;Paragraphe&lt;/p&gt;

## 5.3 Langage de style

CSS décrit principalement la présentation d’une interface.

Exemple :

button {  
padding: 12px;  
}

## 5.4 Bibliothèque

Une bibliothèque fournit du code réutilisable que ton application appelle.

Exemple :

React est principalement une bibliothèque pour construire des interfaces utilisateur.

La logique générale de ton application reste sous ton contrôle.

## 5.5 Framework

Un framework fournit davantage de structure et impose généralement davantage de conventions.

Il peut prendre en charge :

- routing ;
- architecture ;
- rendu ;
- serveur ;
- gestion des données ;
- conventions de projet ;
- outils de développement.

Le terme « framework » n’est toutefois pas toujours utilisé de manière parfaitement uniforme dans l’industrie.

## 5.6 Runtime

Un runtime fournit l’environnement permettant d’exécuter du code.

Exemples :

- navigateur pour JavaScript côté client ;
- Node.js pour JavaScript côté serveur ;
- Deno ;
- Bun ;
- JVM pour certains langages comme Java.

## 5.7 Package / dépendance

Une dépendance est un logiciel dont ton projet dépend.

Exemple :

Mon application  
│  
├── React  
├── Zod  
├── TanStack Query  
└── bibliothèque d'icônes

Chaque dépendance ajoute :

- une capacité ;
- mais aussi une maintenance ;
- une surface de risque ;
- une dette potentielle ;
- des mises à jour.

# PARTIE II — NIVEAU B

# FONDATIONS DU WEB

# 6\. Comment fonctionne le Web ?

Une simplification utile :

Utilisateur  
↓  
Navigateur  
↓  
DNS  
↓  
Serveur / CDN / infrastructure  
↓  
Application  
↓  
API / logique métier  
↓  
Base de données

Le chemin réel peut être beaucoup plus complexe.

# 7\. Client et serveur

## Client

Le client est généralement le navigateur ou une application qui demande une ressource ou un service.

Exemple :

Chrome demande une page Web.

## Serveur

Le serveur reçoit une requête et produit ou transmet une réponse.

Il peut :

- servir une page ;
- retourner des données ;
- authentifier un utilisateur ;
- exécuter une logique métier ;
- communiquer avec une base de données ;
- traiter un fichier ;
- déclencher un traitement.

# 8\. HTTP

HTTP est l’un des protocoles fondamentaux du Web.

Une requête possède notamment :

- une méthode ;
- une URL ;
- des headers ;
- éventuellement un body.

Exemple conceptuel :

GET /users/42

Réponse :

200 OK  
Content-Type: application/json

Puis :

{  
"id": 42,  
"name": "Stane"  
}

# 9\. Méthodes HTTP essentielles

## GET

Récupérer une ressource.

## POST

Créer ou déclencher une opération.

## PUT

Remplacer une ressource.

## PATCH

Modifier partiellement une ressource.

## DELETE

Supprimer une ressource.

Ces méthodes ne doivent pas être choisies au hasard : elles expriment une intention.

# 10\. Codes HTTP essentiels

## 2xx — succès

- 200 : OK
- 201 : Created
- 204 : No Content

## 3xx — redirection

- 301
- 302
- 304

## 4xx — problème côté requête/client

- 400 : Bad Request
- 401 : Unauthorized
- 403 : Forbidden
- 404 : Not Found
- 409 : Conflict
- 422 : Unprocessable Content
- 429 : Too Many Requests

## 5xx — problème côté serveur

- 500 : Internal Server Error
- 502 : Bad Gateway
- 503 : Service Unavailable

# 11\. URL

Une URL identifie une ressource ou une destination.

Exemple :

https://example.com/products/42?sort=price

On peut distinguer :

- protocole : https
- domaine : example.com
- chemin : /products/42
- query parameter : sort=price

# 12\. DNS

Le DNS permet notamment de traduire un nom de domaine en information permettant de trouver le serveur correspondant.

Conceptuellement :

example.com  
↓  
DNS  
↓  
adresse IP  
↓  
serveur

Il ne faut pas confondre :

- domaine ;
- hébergement ;
- serveur ;
- DNS.

# 13\. HTTPS

HTTPS protège les communications HTTP grâce à TLS.

Il permet notamment :

- le chiffrement ;
- l’authentification du serveur ;
- l’intégrité des communications.

À retenir :

HTTP décrit le protocole applicatif ; HTTPS correspond à HTTP transporté de manière sécurisée via TLS.

# 14\. Navigateur

Le navigateur n’est pas simplement « une fenêtre qui affiche un site ».

Il contient notamment :

- moteur HTML ;
- moteur CSS ;
- moteur JavaScript ;
- DOM ;
- gestion réseau ;
- stockage ;
- cache ;
- APIs Web ;
- sécurité ;
- gestion des permissions.

Exemples d’APIs Web :

- Fetch API ;
- Web Storage ;
- IndexedDB ;
- Geolocation API ;
- Notifications API ;
- Service Workers ;
- WebSockets ;
- WebRTC.

# 15\. HTML

HTML décrit la structure du contenu.

Concepts importants :

- éléments ;
- attributs ;
- sémantique ;
- formulaires ;
- liens ;
- images ;
- tableaux ;
- structure du document ;
- accessibilité.

Exemples :

&lt;header&gt;  
&lt;nav&gt;  
&lt;main&gt;  
&lt;section&gt;  
&lt;article&gt;  
&lt;footer&gt;

# 16\. CSS

CSS contrôle notamment :

- couleurs ;
- typographie ;
- espacement ;
- dimensions ;
- positionnement ;
- responsive design ;
- animations ;
- transitions ;
- layout.

Concepts à reconnaître :

- cascade ;
- spécificité ;
- héritage ;
- box model ;
- Flexbox ;
- Grid ;
- media queries ;
- responsive design ;
- variables CSS ;
- pseudo-classes ;
- pseudo-éléments.

# 17\. JavaScript

JavaScript permet d’ajouter du comportement et de la logique aux applications Web.

Concepts fondamentaux :

- variables ;
- types ;
- fonctions ;
- objets ;
- tableaux ;
- conditions ;
- boucles ;
- modules ;
- événements ;
- DOM ;
- Promises ;
- async/await ;
- fetch ;
- gestion des erreurs.

# 18\. Java ≠ JavaScript

C’est une confusion classique.

**Java** et **JavaScript** sont deux langages distincts.

Java est notamment utilisé dans :

- backend ;
- systèmes d’entreprise ;
- Android historiquement ;
- applications distribuées.

JavaScript est central dans :

- Web frontend ;
- Web backend ;
- applications multiplateformes ;
- outils de développement.

Le nom similaire est historique ; il ne signifie pas qu’il s’agit du même langage.

# 19\. TypeScript

TypeScript est un sur-ensemble de JavaScript qui ajoute notamment un système de typage statique.

Exemple :

function add(a: number, b: number): number {  
return a + b;  
}

Intérêt :

- détecter certaines erreurs plus tôt ;
- améliorer l’autocomplétion ;
- rendre les grandes bases de code plus explicites ;
- faciliter certaines refactorisations.

TypeScript n’élimine cependant pas toutes les erreurs.

# 20\. DOM

Le DOM représente le document HTML sous forme d’une structure manipulable par JavaScript.

Exemple :

Document  
│  
├── html  
│ ├── head  
│ └── body  
│ ├── header  
│ └── main

Les frameworks frontend travaillent généralement avec des abstractions autour de cette mécanique.

# 21\. Frontend et backend

## Frontend

Ce que l’utilisateur utilise directement.

Responsabilités possibles :

- interface ;
- interactions ;
- navigation ;
- validation immédiate ;
- affichage ;
- état local ;
- communication avec les APIs.

## Backend

Ce qui s’exécute côté serveur.

Responsabilités possibles :

- logique métier ;
- authentification ;
- autorisation ;
- accès aux données ;
- calculs ;
- traitement ;
- intégrations externes ;
- APIs.

# 22\. Full-stack

Un développeur full-stack travaille sur plusieurs couches :

Frontend  
↕  
API  
↕  
Backend  
↕  
Base de données  
↕  
Infrastructure

« Full-stack » ne signifie pas nécessairement être expert de toutes les couches.

# PARTIE III — CONSTRUIRE UNE APPLICATION

# 23\. Les couches d’une application

Une application moderne peut être conceptualisée ainsi :

┌────────────────────────────┐  
│ Interface │  
│ Frontend │  
└──────────────┬─────────────┘  
│  
↓  
┌────────────────────────────┐  
│ API / transport │  
└──────────────┬─────────────┘  
│  
↓  
┌────────────────────────────┐  
│ Business Logic │  
│ Backend │  
└──────────────┬─────────────┘  
│  
┌───────┴────────┐  
↓ ↓  
┌──────────────┐ ┌──────────────┐  
│ Database │ │ External API │  
└──────────────┘ └──────────────┘

Cette séparation permet de raisonner.

# 24\. Fonctionnalité vs exigence non fonctionnelle

Une fonctionnalité décrit ce que le système fait.

Exemple :

L’utilisateur peut créer une facture.

Une exigence non fonctionnelle décrit comment le système doit fonctionner.

Exemples :

- rapide ;
- sécurisé ;
- accessible ;
- disponible ;
- maintenable ;
- scalable ;
- observable.

Une application peut être fonctionnellement correcte et techniquement mauvaise.

# 25\. Architecture

L’architecture décrit l’organisation globale du logiciel.

Elle répond à des questions comme :

- Où se trouve la logique ?
- Où sont stockées les données ?
- Comment les composants communiquent-ils ?
- Quelles sont les frontières du système ?
- Que se passe-t-il si un service tombe ?
- Comment le système évolue-t-il ?

# 26\. Monolithe

Une application monolithique regroupe généralement plusieurs fonctionnalités dans une même unité déployable.

Exemple :

Application  
├── Auth  
├── Users  
├── Payments  
├── Orders  
├── Admin  
└── Reports

### Avantages

- simple à commencer ;
- déploiement relativement simple ;
- développement rapide ;
- moins de communication réseau interne ;
- plus facile pour une petite équipe.

### Inconvénients

- peut devenir difficile à maintenir ;
- déploiement global ;
- couplage potentiel ;
- scaling moins fin.

# 27\. Modular Monolith

Le modular monolith garde une application déployable unique mais organise fortement le code en modules.

Exemple :

Application  
├── Auth  
├── Billing  
├── Orders  
├── Users  
└── Notifications

Chaque module possède ses responsabilités.

C’est souvent une excellente solution intermédiaire.

# 28\. Microservices

L’application est divisée en services indépendants.

Auth Service  
│  
├── Users Service  
│  
├── Payment Service  
│  
└── Notification Service

### Avantages

- déploiements indépendants ;
- scaling indépendant ;
- équipes séparées ;
- isolation de certaines responsabilités.

### Inconvénients

- réseau ;
- monitoring ;
- déploiement ;
- observabilité ;
- gestion des erreurs distribuées ;
- cohérence des données ;
- complexité opérationnelle.

### Règle importante

**Microservices ne signifie pas automatiquement meilleure architecture.**

Pour une petite application, ils peuvent créer plus de problèmes qu’ils n’en résolvent.

# 29\. Serverless

Le développeur déploie des fonctions ou services sans gérer directement toute l’infrastructure serveur sous-jacente.

Exemples de cas :

- API ;
- webhook ;
- traitement événementiel ;
- tâche ponctuelle.

Avantages :

- démarrage rapide ;
- infrastructure simplifiée ;
- scaling géré par la plateforme.

Limites :

- dépendance fournisseur ;
- contraintes d’exécution ;
- cold starts selon plateforme ;
- debugging parfois plus complexe ;
- coût pouvant devenir imprévisible selon usage.

# 30\. Architecture événementielle

Au lieu d’appeler directement un composant, un système peut publier un événement.

Exemple :

Commande créée  
↓  
Event: OrderCreated  
↓  
├── Email  
├── Stock  
├── Analytics  
└── Notification

Très utile lorsque plusieurs composants doivent réagir à un même événement.

Mais cela introduit aussi :

- asynchronisme ;
- complexité de débogage ;
- gestion des doublons ;
- cohérence éventuelle ;
- files et brokers.

# PARTIE IV — DONNÉES ET BASES DE DONNÉES

# 31\. Pourquoi une base de données ?

Une base de données permet notamment de :

- stocker ;
- rechercher ;
- modifier ;
- supprimer ;
- organiser ;
- sécuriser ;
- indexer ;
- maintenir des données.

# 32\. SQL

SQL est un langage permettant notamment d’interagir avec des bases relationnelles.

Exemple :

SELECT \*  
FROM users  
WHERE id = 42;

Concepts importants :

- tables ;
- colonnes ;
- lignes ;
- relations ;
- clés primaires ;
- clés étrangères ;
- contraintes ;
- index ;
- transactions ;
- jointures.

# 33\. Bases relationnelles

Exemples :

- PostgreSQL ;
- MySQL ;
- MariaDB ;
- SQLite ;
- SQL Server ;
- Oracle Database.

Elles représentent généralement les données sous forme structurée avec des relations.

# 34\. NoSQL

NoSQL désigne plusieurs familles de bases qui ne reposent pas nécessairement sur le modèle relationnel classique.

Exemples :

- document ;
- clé-valeur ;
- colonne ;
- graphe.

Une base NoSQL n’est pas « une base SQL meilleure ».

Elle répond à d’autres besoins.

# 35\. PostgreSQL

PostgreSQL est une base relationnelle très complète.

Elle convient notamment à :

- applications Web ;
- SaaS ;
- systèmes métier ;
- données relationnelles complexes ;
- transactions ;
- applications nécessitant une base solide et extensible.

# 36\. SQLite

SQLite est une base embarquée et légère.

Très utile pour :

- petits projets ;
- applications locales ;
- prototypes ;
- tests ;
- outils embarqués.

Elle ne remplace pas systématiquement PostgreSQL pour une application Web multi-utilisateur à forte charge.

# 37\. Index

Un index accélère certaines recherches.

Mais un index a un coût :

- espace ;
- maintenance lors des écritures ;
- complexité.

Donc :

« Ajouter des index partout » n’est pas une stratégie de performance.

# 38\. Transactions

Une transaction permet de regrouper plusieurs opérations qui doivent respecter certaines garanties.

Exemple bancaire :

Débiter A  
+  
Créditer B

On ne veut pas que seulement une des deux opérations réussisse.

# 39\. Migrations

Une migration permet de faire évoluer la structure d’une base de données de manière contrôlée.

Exemple :

Version 1  
users(id, name)  
<br/>↓ migration  
<br/>Version 2  
users(id, name, email)

Les migrations sont essentielles pour les projets qui évoluent.

# 40\. ORM

Un ORM permet de manipuler certaines bases de données à travers des abstractions de programmation.

Exemples :

- Prisma ;
- SQLAlchemy ;
- Hibernate ;
- Entity Framework.

### Avantages

- productivité ;
- abstraction ;
- typage selon outil ;
- réduction de SQL répétitif.

### Inconvénients

- abstraction imparfaite ;
- requêtes inefficaces possibles ;
- difficulté à comprendre les performances si le SQL sous-jacent est ignoré.

Règle :

Utiliser un ORM ne dispense pas de comprendre SQL.

# PARTIE V — API ET COMMUNICATION

# 41\. Qu’est-ce qu’une API ?

Une API est une interface permettant à des logiciels de communiquer.

Elle définit notamment :

- ce qu’on peut demander ;
- comment le demander ;
- quelles données envoyer ;
- quelles données recevoir ;
- quelles erreurs peuvent survenir.

# 42\. REST

REST est un style architectural couramment utilisé pour les APIs Web.

Exemple :

GET /users  
GET /users/42  
POST /users  
PATCH /users/42  
DELETE /users/42

Avantages :

- relativement simple ;
- standard familier ;
- outils nombreux ;
- adapté à beaucoup d’applications.

Limites :

- certaines données nécessitent plusieurs requêtes ;
- certaines APIs REST deviennent incohérentes ;
- le style n’est pas une garantie automatique de qualité.

# 43\. GraphQL

GraphQL permet notamment au client de demander précisément les données souhaitées.

Intéressant lorsque :

- les besoins de données sont complexes ;
- plusieurs clients ont des besoins différents ;
- les relations de données sont importantes.

Mais cela ajoute :

- complexité ;
- gestion du caching ;
- sécurité ;
- contrôle de la profondeur des requêtes ;
- infrastructure spécifique.

# 44\. WebSockets

Les WebSockets permettent une communication bidirectionnelle persistante entre client et serveur.

Cas typiques :

- chat ;
- collaboration temps réel ;
- notifications ;
- tableaux de bord live ;
- jeux.

Pour une simple page qui récupère des données une fois, WebSocket serait généralement inutile.

# 45\. Webhooks

Un webhook permet à un système d’informer automatiquement un autre système lorsqu’un événement survient.

Exemple :

Paiement effectué  
↓  
FedaPay  
↓  
Webhook  
↓  
Backend  
↓  
Commande marquée "payée"

Le webhook est particulièrement important dans les systèmes de paiement et d’intégration.

# 46\. API externe

Une application peut dépendre de services externes :

- paiement ;
- SMS ;
- email ;
- cartographie ;
- IA ;
- authentification ;
- stockage ;
- analytics.

Chaque dépendance externe représente une contrainte supplémentaire :

- disponibilité ;
- coût ;
- limites ;
- changements d’API ;
- sécurité ;
- confidentialité ;
- dépendance fournisseur.

# PARTIE VI — FRONTEND

# 47\. Pourquoi utiliser un framework frontend ?

Un site simple peut parfaitement fonctionner avec :

HTML + CSS + JavaScript

Un framework devient intéressant lorsque l’interface possède davantage de complexité :

- composants réutilisables ;
- état complexe ;
- routing ;
- interactions nombreuses ;
- données dynamiques ;
- grandes équipes ;
- besoin de conventions.

# 48\. React

React est une bibliothèque centrée sur la construction d’interfaces utilisateur avec des composants.

Concepts essentiels :

- composants ;
- props ;
- state ;
- hooks ;
- rendu ;
- composition.

React n’est pas :

- une base de données ;
- un backend ;
- un hébergeur ;
- une solution complète obligatoire pour tous les sites.

# 49\. React Native

React Native vise la création d’interfaces d’applications mobiles avec React et JavaScript/TypeScript.

Il ne faut pas confondre :

React → interfaces principalement Web.

React Native → applications natives/mobiles avec une architecture différente.

# 50\. Vue

Vue est un framework progressif pour construire des interfaces Web.

Il vise notamment :

- simplicité ;
- composants ;
- réactivité ;
- intégration progressive.

# 51\. Angular

Angular est un framework Web complet avec une structure plus opinionated.

Il convient notamment à :

- grandes applications ;
- équipes structurées ;
- environnements où les conventions fortes sont utiles.

# 52\. Svelte

Svelte propose une approche différente du développement frontend en déplaçant une partie du travail vers la compilation.

Il est intéressant pour comprendre qu’il existe plusieurs modèles de construction d’UI.

# 53\. CSS frameworks

## Bootstrap

Bootstrap fournit notamment :

- composants ;
- système de grille ;
- styles ;
- conventions.

Avantage :

productivité rapide.

Inconvénient :

risque d’interfaces très reconnaissables si fortement utilisé sans personnalisation.

## Tailwind CSS

Tailwind repose sur des classes utilitaires.

Exemple :

&lt;div class="flex items-center gap-4"&gt;

Avantages :

- rapidité ;
- cohérence ;
- contrôle ;
- système de design personnalisable.

Inconvénients :

- HTML parfois très chargé ;
- nécessite de comprendre CSS ;
- peut devenir difficile sans conventions.

# 54\. CSS pur

CSS natif reste parfaitement valable.

Il ne faut pas adopter un framework simplement parce qu’il existe.

# 55\. State management

L’état représente des informations qui évoluent pendant l’utilisation de l’application.

Exemples :

- utilisateur connecté ;
- panier ;
- filtre ;
- modal ouverte ;
- formulaire ;
- données serveur.

Outils possibles :

- state natif du framework ;
- Context ;
- Redux ;
- Zustand ;
- autres solutions.

Il faut distinguer :

### UI state

État de l’interface.

### Server state

Données provenant du serveur.

Ces deux problèmes ne nécessitent pas nécessairement le même outil.

# 56\. Client state vs server state

Exemple :

Client state  
→ modal ouverte  
→ thème  
→ onglet sélectionné  
<br/>Server state  
→ produits  
→ commandes  
→ profil utilisateur

Des outils comme TanStack Query répondent principalement aux problèmes liés au server state.

# 57\. Routing

Le routing permet d’associer des URLs à des vues ou ressources.

Exemple :

/  
/about  
/products  
/products/42  
/admin

Il peut être :

- côté client ;
- côté serveur ;
- hybride.

# PARTIE VII — RENDU ET PERFORMANCE

# 58\. CSR

**Client-Side Rendering**

Le navigateur reçoit principalement une application JavaScript qui construit l’interface côté client.

Avantages :

- applications interactives ;
- transitions rapides après chargement ;
- architecture SPA fréquente.

Limites :

- premier chargement ;
- SEO selon implémentation ;
- JavaScript requis pour certaines expériences.

# 59\. SSR

**Server-Side Rendering**

Le serveur génère HTML pour la requête.

Avantages :

- HTML initial disponible rapidement ;
- utile pour SEO ;
- bon pour certains contenus dynamiques.

Coûts :

- architecture plus complexe ;
- charge serveur ;
- gestion du rendu hybride.

# 60\. SSG

**Static Site Generation**

Les pages sont générées à l’avance.

Excellent pour :

- documentation ;
- blog ;
- pages marketing ;
- contenu relativement stable.

# 61\. ISR et approches hybrides

Certaines architectures permettent de combiner :

- contenu statique ;
- rendu serveur ;
- génération à la demande ;
- revalidation.

Le choix dépend du type de contenu et des exigences.

# 62\. PWA

Une Progressive Web App peut rapprocher une application Web de certaines caractéristiques d’une application installable.

Concepts associés :

- service worker ;
- cache ;
- offline ;
- installation ;
- manifest ;
- notifications selon contexte.

À envisager lorsque :

le Web doit offrir une expérience applicative renforcée sans nécessiter immédiatement une application native distincte.

# 63\. Cache

Le cache conserve temporairement des données pour éviter un travail inutile.

On peut rencontrer :

- cache navigateur ;
- cache HTTP ;
- CDN cache ;
- cache applicatif ;
- Redis ;
- cache de données ;
- cache de requêtes.

Le cache améliore potentiellement :

- vitesse ;
- charge serveur ;
- coût.

Mais il introduit un problème fondamental :

**La fraîcheur des données.**

Phrase à retenir :

« There are only two hard things in Computer Science: cache invalidation and naming things. »

La citation est surtout célèbre comme aphorisme : dans la pratique, l’invalidation du cache est effectivement un problème complexe.

# 64\. CDN

Un CDN distribue des ressources depuis des emplacements géographiques plus proches des utilisateurs.

Excellent pour :

- images ;
- CSS ;
- JavaScript ;
- vidéos ;
- ressources statiques ;
- parfois HTML et réponses cacheables.

# PARTIE VIII — MOBILE ET MULTIPLATEFORME

# 65\. Développement natif

Chaque plateforme est développée avec ses technologies privilégiées.

Exemples :

- Swift pour iOS ;
- Kotlin pour Android.

Avantages :

- intégration plateforme ;
- performances ;
- accès aux APIs natives ;
- expérience spécifique.

Inconvénient :

- davantage de code à maintenir si plusieurs plateformes.

# 66\. Flutter

Flutter permet de construire des applications pour plusieurs plateformes à partir d’une base de code en Dart.

Il est intéressant lorsqu’on veut :

- mobile ;
- éventuellement Web ;
- desktop ;
- expérience UI cohérente ;
- développement multiplateforme.

Mais Flutter n’est pas automatiquement supérieur au natif ou à React Native.

# 67\. React Native

Intéressant lorsque l’équipe maîtrise déjà :

- JavaScript ;
- TypeScript ;
- React.

Il permet de réutiliser certaines compétences et une partie de la logique entre plateformes.

# 68\. PWA vs Flutter vs React Native vs natif

### PWA

Choisir plutôt si :

- le Web est prioritaire ;
- distribution simple souhaitée ;
- installation sans store importante ;
- besoins natifs limités.

### React Native

Choisir plutôt si :

- compétences React ;
- applications mobiles ;
- besoin d’écosystème JavaScript/TypeScript ;
- partage de logique souhaité.

### Flutter

Choisir plutôt si :

- multiplateforme forte ;
- UI contrôlée ;
- équipe acceptant Dart ;
- besoin d’une base de code commune.

### Natif

Choisir plutôt si :

- intégration profonde avec la plateforme ;
- performances spécifiques ;
- fonctionnalités natives avancées ;
- expérience plateforme prioritaire.

# PARTIE IX — CMS ET DÉVELOPPEMENT SUR MESURE

# 69\. WordPress

WordPress est un CMS.

Il permet notamment :

- publication ;
- gestion de contenu ;
- thèmes ;
- extensions ;
- administration.

Excellent pour :

- sites institutionnels ;
- blogs ;
- sites vitrines ;
- certains sites e-commerce ;
- projets où le client doit administrer facilement le contenu.

# 70\. Développement sur mesure

Une application React/backend ou autre approche custom offre davantage de contrôle.

Pertinent lorsque :

- logique métier spécifique ;
- workflows complexes ;
- intégrations particulières ;
- exigences techniques fortes ;
- expérience utilisateur spécifique.

Mais le coût de développement et de maintenance augmente.

# 71\. WordPress vs développement custom

| Besoin | WordPress | Custom |
| --- | --- | --- |
| Blog | Excellent | Possible |
| Site vitrine simple | Excellent | Possible |
| Administration simple | Excellent | À construire |
| Logique métier complexe | Limité selon besoin | Excellent |
| Contrôle technique | Moyen à élevé | Très élevé |
| Développement initial | Rapide | Plus long |
| Maintenance | Plugins/thème | Code propriétaire |
| Fonctionnalités très spécifiques | Peut devenir complexe | Très adapté |

Règle :

**Ne pas développer sur mesure ce qu’un CMS peut résoudre proprement.**

Mais inversement :

**Ne pas forcer un CMS à devenir une application métier complexe.**

# PARTIE X — QUALITÉ DU CODE

# 72\. Lisibilité

Un bon code doit être compréhensible.

Critères :

- noms explicites ;
- fonctions raisonnablement petites ;
- responsabilités claires ;
- structure cohérente.

# 73\. DRY

**Don’t Repeat Yourself**

Éviter les duplications inutiles.

Attention :

DRY ne signifie pas créer une abstraction complexe dès qu’une ligne apparaît deux fois.

Une abstraction prématurée peut être pire qu’une petite duplication.

# 74\. KISS

**Keep It Simple, Stupid**

Chercher une solution simple lorsque le problème est simple.

# 75\. YAGNI

**You Aren’t Gonna Need It**

Ne pas construire aujourd’hui une fonctionnalité hypothétique sans besoin réel.

# 76\. SOLID

Ensemble de principes de conception orientée objet.

À connaître au niveau culturel :

- Single Responsibility;
- Open/Closed;
- Liskov Substitution;
- Interface Segregation;
- Dependency Inversion.

Objectif :

reconnaître les problèmes de conception qu’ils cherchent à éviter.

Il n’est pas nécessaire d’appliquer mécaniquement SOLID partout.

# 77\. Refactoring

Le refactoring consiste à améliorer la structure interne du code sans modifier intentionnellement son comportement externe.

Exemples :

- réduire duplication ;
- séparer responsabilités ;
- renommer ;
- simplifier ;
- extraire une fonction.

# 78\. Dette technique

La dette technique représente les compromis techniques qui rendent les évolutions futures plus coûteuses.

Exemple :

Prototype rapide  
↓  
fonctionne  
↓  
clients arrivent  
↓  
code difficile à maintenir  
↓  
chaque modification devient coûteuse

La dette technique n’est pas toujours mauvaise.

Une dette peut être volontaire.

Le problème est la dette :

non identifiée, non suivie et jamais remboursée.

# PARTIE XI — TESTS

# 79\. Pourquoi tester ?

Un test répond à :

« Le logiciel fait-il ce que nous pensons qu’il doit faire ? »

Il ne garantit pas que le logiciel est parfait.

# 80\. Tests unitaires

Tester une petite unité isolée.

Exemple :

calculateTotal()

# 81\. Tests d’intégration

Tester plusieurs composants ensemble.

Exemple :

API  
+  
Database

# 82\. Tests end-to-end

Tester un scénario proche de l’utilisateur réel.

Exemple :

Utilisateur  
→ connexion  
→ ajoute produit  
→ paiement  
→ confirmation

# 83\. Pyramide de tests

Conceptuellement :

E2E  
/ \\  
Integration  
/ \\  
Unit

Les tests unitaires sont généralement nombreux et rapides.

Les E2E sont plus coûteux mais testent davantage le système réel.

# 84\. Tests manuels

Ils restent utiles.

Particulièrement pour :

- UX ;
- apparence ;
- comportements difficiles à automatiser ;
- exploration ;
- validation finale.

# PARTIE XII — GIT, GITHUB ET COLLABORATION

# 85\. Git

Git est un système de contrôle de versions.

Il permet notamment :

- historique ;
- branches ;
- commits ;
- comparaison ;
- retour en arrière ;
- collaboration.

# 86\. GitHub

GitHub est une plateforme qui héberge notamment des dépôts Git et ajoute :

- Pull Requests ;
- Issues ;
- Actions ;
- discussions ;
- collaboration ;
- revue de code.

Donc :

Git ≠ GitHub.

# 87\. Commit

Un commit représente un état enregistré du projet.

Un bon commit devrait généralement représenter une modification cohérente.

# 88\. Branches

Une branche permet notamment de travailler sur une évolution sans modifier directement la branche principale.

# 89\. Pull Request

Une Pull Request permet de proposer une modification pour :

- revue ;
- discussion ;
- tests ;
- fusion.

# PARTIE XIII — DÉPENDANCES ET GESTIONNAIRES DE PACKAGES

# 90\. Package manager

Il permet notamment de :

- installer ;
- mettre à jour ;
- supprimer ;
- verrouiller des dépendances.

Exemples :

- npm ;
- pnpm ;
- yarn ;
- pip ;
- Composer ;
- Maven ;
- Gradle ;
- Cargo.

# 91\. Lockfile

Un lockfile enregistre précisément certaines versions des dépendances utilisées.

Objectif :

éviter qu’une installation différente récupère involontairement des versions différentes.

# 92\. Risque des dépendances

Chaque dépendance ajoute :

- code externe ;
- risque de vulnérabilité ;
- maintenance ;
- compatibilité ;
- potentiel de rupture.

Donc :

**Installer une bibliothèque n’est jamais totalement gratuit.**

# PARTIE XIV — CONTENEURS ET DÉPLOIEMENT

# 93\. Docker

Docker permet notamment d’emballer une application et son environnement dans une image exécutable dans un conteneur.

Conceptuellement :

Application  
+  
Runtime  
+  
Dépendances  
+  
Configuration  
↓  
Image  
↓  
Container

# 94\. Container vs machine virtuelle

Une machine virtuelle émule généralement une machine complète avec son propre système d’exploitation.

Un conteneur partage davantage les ressources du système hôte tout en isolant l’application.

Les deux répondent à des besoins différents.

# 95\. CI/CD

CI = Continuous Integration.

CD peut signifier Continuous Delivery ou Continuous Deployment selon le contexte.

Pipeline typique :

Push  
↓  
Tests  
↓  
Lint  
↓  
Build  
↓  
Security checks  
↓  
Deploy

# 96\. Environnements

Un projet peut avoir :

- development ;
- testing ;
- staging ;
- production.

Objectif :

éviter de tester directement sur la production.

# 97\. Variables d’environnement

Elles permettent notamment de séparer la configuration du code.

Exemple :

DATABASE_URL  
API_KEY  
JWT_SECRET

Attention :

Une variable d’environnement n’est pas automatiquement secrète.

Si une valeur est envoyée au frontend, elle peut généralement être récupérée par l’utilisateur.

# PARTIE XV — OBSERVABILITÉ

# 98\. Logging

Les logs enregistrent des événements.

Exemple :

Payment failed  
order_id=123  
reason=timeout

# 99\. Monitoring

Le monitoring permet de surveiller notamment :

- disponibilité ;
- erreurs ;
- CPU ;
- mémoire ;
- latence ;
- trafic.

# 100\. Tracing

Le tracing suit une requête à travers plusieurs composants.

Très utile dans les systèmes distribués.

# 101\. Observabilité

L’observabilité regroupe notamment :

- logs ;
- métriques ;
- traces.

Elle permet de comprendre ce qui se passe dans un système à partir de ses signaux observables.

# PARTIE XVI — NIVEAU C

# TECHNOLOGIES ET OUTILS À SAVOIR SITUER

# 102\. Carte rapide

| Technologie | Catégorie | À retenir |
| --- | --- | --- |
| HTML | Balisage | Structure |
| CSS | Style | Présentation |
| JavaScript | Langage | Logique Web |
| TypeScript | Langage | JavaScript typé |
| Java | Langage | Backend/entreprise/etc. |
| Python | Langage | Backend, data, IA, scripts |
| PHP | Langage | Web/backend |
| C#  | Langage | .NET |
| Go  | Langage | Backend/systèmes |
| Rust | Langage | Systèmes/performance/sécurité mémoire |
| React | Bibliothèque UI | Interfaces |
| Vue | Framework UI | Interfaces |
| Angular | Framework | Applications Web structurées |
| Svelte | Framework/compiler | UI  |
| Next.js | Framework React | Web full-stack/hybride |
| Node.js | Runtime | JS côté serveur |
| Django | Framework Python | Backend |
| FastAPI | Framework Python | APIs |
| Spring | Framework Java | Backend |
| Laravel | Framework PHP | Backend/Web |
| Tailwind | CSS framework | Utilitaires CSS |
| Bootstrap | CSS/component framework | UI rapide |
| WordPress | CMS | Gestion de contenu |
| PostgreSQL | Base SQL | Base relationnelle |
| MySQL | Base SQL | Base relationnelle |
| SQLite | Base SQL embarquée | Petit/local |
| MongoDB | Base NoSQL document | Documents |
| Redis | Clé-valeur/in-memory | Cache, données rapides |
| GraphQL | API/query language | Requêtes flexibles |
| REST | Style API | APIs Web |
| WebSocket | Protocole communication | Temps réel |
| Docker | Conteneurisation | Environnements reproductibles |
| Git | VCS | Historique |
| GitHub | Plateforme | Collaboration |
| Flutter | Framework multiplateforme | Dart/mobile/Web/desktop |
| React Native | Framework mobile | React/mobile |
| Kubernetes | Orchestration | Conteneurs à grande échelle |
| Vite | Build/dev tool | Frontend moderne |
| npm | Package manager | Dépendances JS |
| pnpm | Package manager | Dépendances JS |
| Vitest | Test runner | Tests JS/TS |
| Playwright | E2E/browser automation | Tests navigateur |

# PARTIE XVII — NIVEAU D

# COMPARAISONS STRUCTURANTES

# 103\. HTML vs CSS vs JavaScript

| Technologie | Question principale |
| --- | --- |
| HTML | Qu’est-ce qui existe ? |
| CSS | À quoi cela ressemble ? |
| JavaScript | Que fait-il ? |

Simplification :

HTML → structure  
CSS → présentation  
JS → comportement

# 104\. Java vs JavaScript

Ils sont différents.

| Java | JavaScript |
| --- | --- |
| Langage | Langage |
| JVM | Navigateur/Node/etc. |
| Backend/entreprise | Web/frontend/backend |
| Typage statique traditionnel | Dynamique, TypeScript possible |
| Écosystème Java | Écosystème JS/TS |

# 105\. React vs Vue vs Angular

### React

Bon choix lorsque :

- équipe React ;
- écosystème important ;
- flexibilité souhaitée.

### Vue

Bon choix lorsque :

- simplicité ;
- intégration progressive ;
- équipe appréciant son modèle.

### Angular

Bon choix lorsque :

- structure forte ;
- grande application ;
- conventions d’équipe importantes.

Aucun n’est universellement « meilleur ».

# 106\. React vs vanilla JavaScript

### Vanilla

Excellent lorsque :

- site simple ;
- peu d’état ;
- interactions limitées ;
- dépendances minimales souhaitées.

### React

Excellent lorsque :

- UI complexe ;
- composants nombreux ;
- état important ;
- application interactive.

# 107\. Tailwind vs Bootstrap

### Bootstrap

Choisir si :

- besoin de composants rapidement ;
- équipe voulant des conventions préfabriquées ;
- prototypage rapide.

### Tailwind

Choisir si :

- contrôle visuel ;
- design system personnalisé ;
- workflow utility-first.

### CSS natif

Choisir si :

- projet simple ;
- besoin de dépendances minimales ;
- équipe compétente en CSS.

# 108\. SQL vs NoSQL

Choisir SQL lorsque :

- relations importantes ;
- transactions ;
- structure claire ;
- intégrité forte ;
- requêtes relationnelles.

Choisir NoSQL lorsque :

- modèle document pertinent ;
- besoins spécifiques de scaling ;
- structure flexible ;
- cas d’utilisation adaptés.

Ne jamais choisir NoSQL uniquement parce que :

« C’est moderne. »

# 109\. PostgreSQL vs MySQL

Les deux sont de solides bases relationnelles.

Le choix dépend de :

- compétences ;
- fonctionnalités ;
- écosystème ;
- hébergement ;
- contraintes du projet.

Pour beaucoup de projets modernes, PostgreSQL est une excellente option par défaut.

Mais :

« PostgreSQL partout » n’est pas une règle universelle.

# 110\. REST vs GraphQL

### REST

Préférer souvent si :

- API classique ;
- CRUD ;
- simplicité ;
- architecture facilement compréhensible.

### GraphQL

Envisager si :

- données complexes ;
- nombreux clients ;
- besoins de requêtes flexibles.

# 111\. Monolithe vs microservices

### Monolithe

Souvent préférable :

- petit projet ;
- petite équipe ;
- MVP ;
- domaine encore incertain.

### Modular monolith

Très intéressant lorsque :

- projet grandissant ;
- besoin de séparation ;
- mais microservices prématurés.

### Microservices

Pertinent lorsque :

- frontières métier claires ;
- équipes multiples ;
- scaling indépendant ;
- besoins opérationnels réels.

# 112\. REST vs WebSocket

### REST

Pour :

- CRUD ;
- consultation ;
- opérations classiques.

### WebSocket

Pour :

- temps réel ;
- communication persistante ;
- événements instantanés.

# 113\. WordPress vs React

Ce sont des catégories différentes.

WordPress :

CMS.

React :

bibliothèque UI.

Comparer directement les deux est souvent une erreur de catégorie.

Une meilleure comparaison serait :

WordPress vs développement custom.

Ou :

React vs Vue.

# 114\. React vs Flutter

React :

principalement Web.

Flutter :

multiplateforme avec Dart.

Le choix dépend notamment :

- plateforme cible ;
- compétences ;
- UI ;
- écosystème ;
- contraintes natives ;
- stratégie de distribution.

# 115\. Git vs GitHub

Git :

technologie de contrôle de version.

GitHub :

plateforme de collaboration et d’hébergement autour de Git.

# 116\. SQL vs PostgreSQL

Encore une distinction importante :

SQL = langage / famille de concepts.

PostgreSQL = système de gestion de base de données.

Même logique :

JavaScript ≠ React.

HTML ≠ WordPress.

Git ≠ GitHub.

# PARTIE XVIII — NIVEAU E

# ORIENTATION ET ARBRES DE DÉCISION

# 117\. Première question : quel problème dois-je résoudre ?

Avant de choisir une technologie :

Quel est le produit ?  
↓  
Qui l'utilise ?  
↓  
Quelles fonctionnalités ?  
↓  
Quelles contraintes ?  
↓  
Quel niveau de trafic ?  
↓  
Quelles données ?  
↓  
Quel besoin de temps réel ?  
↓  
Quel besoin mobile ?  
↓  
Quel budget ?  
↓  
Quelles compétences disponibles ?  
↓  
Quelle technologie ?

# 118\. Site vitrine simple

Si :

- contenu principalement statique ;
- quelques formulaires ;
- SEO important ;
- peu de logique ;

considérer :

- HTML/CSS/JS ;
- générateur statique ;
- CMS ;
- framework léger.

Ne pas commencer automatiquement avec :

React + backend + PostgreSQL + Docker + Kubernetes.

# 119\. Blog / contenu

Considérer :

- WordPress ;
- CMS headless ;
- générateur statique ;
- framework avec CMS.

La question centrale :

Qui doit gérer le contenu ?

# 120\. Application SaaS

Besoin typique :

- comptes ;
- authentification ;
- dashboard ;
- base de données ;
- paiements ;
- rôles ;
- API.

Architecture possible :

Frontend  
↓  
Backend/API  
↓  
Database  
↓  
External services

# 121\. Application métier

Exemples :

- gestion de stock ;
- facturation ;
- RH ;
- CRM.

Priorités :

- intégrité des données ;
- permissions ;
- workflows ;
- audit ;
- fiabilité ;
- sauvegardes.

# 122\. Application temps réel

Si besoin :

- chat ;
- collaboration ;
- données live.

Envisager :

- WebSockets ;
- Server-Sent Events ;
- architecture événementielle.

Mais vérifier d’abord :

Est-ce réellement du temps réel ?

# 123\. Application mobile

Questions :

1.  Android seulement ?
2.  iOS également ?
3.  Web également ?
4.  Besoin de fonctions natives ?
5.  Équipe JavaScript/React ?
6.  Équipe Dart ?
7.  Performance critique ?

Puis comparer :

- natif ;
- Flutter ;
- React Native ;
- PWA.

# 124\. Besoin d’un CMS

Demander :

Le client doit-il modifier lui-même du contenu régulièrement ?

Si oui :

CMS ou architecture headless à envisager.

# 125\. Besoin de backend

Demander :

Le navigateur peut-il fonctionner uniquement avec des ressources statiques ?

Si oui :

Backend potentiellement inutile.

Si non :

API/backend/serverless/BaaS à considérer.

# 126\. Besoin de base de données

Demander :

L’application doit-elle conserver des données structurées persistantes ?

Si oui :

Base de données probablement nécessaire.

Mais attention :

Tous les projets n’ont pas besoin d’une base de données.

# 127\. Besoin de cache

Penser au cache lorsque :

- mêmes données demandées souvent ;
- calcul coûteux ;
- données peu fréquemment modifiées ;
- latence réseau importante.

Ne pas ajouter un cache avant de comprendre :

quel problème de performance existe réellement ?

# 128\. Besoin de microservices

Question :

Quelle contrainte réelle le monolithe ne peut-il pas résoudre correctement ?

Si aucune réponse claire :

microservices probablement prématurés.

# 129\. Besoin de Docker

Envisager Docker lorsque :

- environnement complexe ;
- reproductibilité ;
- plusieurs services ;
- déploiement cohérent ;
- équipe.

Pour une petite page statique :

Docker peut être inutile.

# 130\. Besoin de Kubernetes

Kubernetes est une technologie d’orchestration puissante.

Mais elle introduit une complexité importante.

Pour un petit projet :

probablement inutile.

Pour une infrastructure importante :

potentiellement pertinent.

# 131\. Besoin de Redis

Envisager Redis pour :

- cache ;
- sessions ;
- compteurs ;
- files simples ;
- données temporaires ;
- certaines architectures temps réel.

Ne pas l’ajouter simplement parce que :

« Redis est rapide. »

# PARTIE XIX — LE DÉVELOPPEMENT AUGMENTÉ PAR IA

# 132\. Nouveau rôle du développeur

Avec l’IA, le développeur ne disparaît pas.

Une partie du travail se déplace.

Avant :

Comprendre  
→ concevoir  
→ coder  
→ tester

Avec IA :

Comprendre  
→ spécifier  
→ concevoir  
→ déléguer  
→ inspecter  
→ tester  
→ corriger  
→ auditer

Le risque principal devient :

produire beaucoup de code que personne ne comprend réellement.

# 133\. Ce que l’IA fait bien

L’IA peut être excellente pour :

- boilerplate ;
- génération de composants ;
- refactoring ;
- tests ;
- documentation ;
- exploration ;
- conversion de code ;
- debugging ;
- recherche d’alternatives ;
- génération de SQL ;
- scripts ;
- configuration ;
- explications.

# 134\. Ce qu’il ne faut pas déléguer aveuglément

Ne pas déléguer sans contrôle :

- architecture ;
- sécurité ;
- choix de données ;
- secrets ;
- conformité ;
- logique métier critique ;
- paiements ;
- permissions ;
- migrations destructrices ;
- décisions irréversibles.

# 135\. Prompt technique faible

Fais-moi un dashboard React.

Problème :

L’IA doit inventer :

- architecture ;
- design ;
- état ;
- API ;
- données ;
- sécurité ;
- composants ;
- conventions.

# 136\. Prompt technique meilleur

Contexte :  
Je construis une application SaaS de facturation.  
<br/>Stack :  
React + TypeScript + Vite  
Tailwind CSS  
Supabase/PostgreSQL  
TanStack Query  
Zod  
<br/>Objectif :  
Créer la page de liste des factures.  
<br/>Contraintes :  
\- mobile-first  
\- accessible au clavier  
\- pagination serveur  
\- états loading/error/empty  
\- validation des données  
\- aucune donnée sensible dans le frontend  
\- composants réutilisables  
\- pas de nouvelle dépendance sans justification  
<br/>Avant de coder :  
1\. propose l'architecture ;  
2\. liste les fichiers à modifier ;  
3\. explique les choix ;  
4\. identifie les risques ;  
5\. attends validation avant implémentation.

# 137\. Le contexte est une spécification

Plus l’IA possède un contexte précis, moins elle doit inventer.

Le contexte devrait inclure si nécessaire :

- objectif ;
- utilisateurs ;
- contraintes ;
- stack ;
- architecture ;
- conventions ;
- données ;
- sécurité ;
- performance ;
- accessibilité ;
- compatibilité ;
- critères d’acceptation.

# 138\. Toujours demander les hypothèses

Demander :

« Quelles hypothèses as-tu faites ? »

Cette question est extrêmement importante.

L’IA peut avoir supposé :

- qu’un utilisateur est toujours authentifié ;
- qu’une donnée existe ;
- qu’un endpoint est fiable ;
- qu’un champ est unique ;
- qu’une action est autorisée ;
- que le trafic est faible.

Une hypothèse fausse peut provoquer une mauvaise architecture.

# 139\. Demander plusieurs options

Au lieu de :

« Fais X. »

Demander :

« Propose trois architectures raisonnables, avec avantages, inconvénients, complexité, coût et risques. Puis recommande-en une. »

Cela transforme l’IA en assistant de décision.

# 140\. Demander les compromis

Question fondamentale :

« Quel compromis introduit ton choix ? »

Chaque décision technique possède généralement un coût.

Exemples :

Simplicité ↔ Flexibilité  
Performance ↔ Complexité  
Contrôle ↔ Productivité  
Coût ↔ Disponibilité  
Rapiditié ↔ Robustesse

# 141\. Développement par étapes

Workflow recommandé :

1\. Comprendre le besoin  
2\. Clarifier les contraintes  
3\. Définir les critères de réussite  
4\. Proposer architecture  
5\. Valider architecture  
6\. Découper en tâches  
7\. Implémenter  
8\. Tester  
9\. Auditer  
10\. Documenter

Éviter :

"Construis-moi toute l'application."

# PARTIE XX — NIVEAU G

# CONTRÔLE ET AUDIT DU CODE PRODUIT PAR L’IA

# 142\. Première règle

**Le fait que le code fonctionne ne signifie pas qu’il est bon.**

Un code peut :

- fonctionner ;
- être lent ;
- être vulnérable ;
- être difficile à maintenir ;
- mal gérer les erreurs ;
- exposer des données ;
- être impossible à faire évoluer.

# 143\. Audit fonctionnel

Question :

Le logiciel fait-il réellement ce qui est demandé ?

Tester :

- happy path ;
- cas limites ;
- erreurs ;
- données invalides ;
- absence de données ;
- utilisateurs différents.

# 144\. Audit architectural

Demander :

- Les responsabilités sont-elles bien séparées ?
- Le frontend contient-il une logique qui devrait être serveur ?
- Le backend fait-il trop de choses ?
- Les modules sont-ils couplés ?
- La base est-elle correctement structurée ?
- L’architecture est-elle inutilement complexe ?

# 145\. Audit sécurité

Vérifier notamment :

- authentification ;
- autorisation ;
- validation des entrées ;
- gestion des secrets ;
- injections ;
- XSS ;
- CSRF selon architecture ;
- contrôle d’accès ;
- exposition des données ;
- fichiers uploadés ;
- rate limiting ;
- dépendances vulnérables.

# 146\. Audit des permissions

Question critique :

« Est-ce que l’interface empêche l’utilisateur, ou est-ce réellement le serveur qui l’empêche ? »

Cacher un bouton n’est pas une autorisation.

Exemple incorrect :

Admin button hidden  
→ donc sécurité

Correct :

Backend vérifie le rôle  
→ autorisation  
→ opération

# 147\. Audit des données

Vérifier :

- validation ;
- contraintes ;
- types ;
- relations ;
- transactions ;
- doublons ;
- nullabilité ;
- intégrité.

# 148\. Audit performance

Vérifier :

- nombre de requêtes ;
- taille des bundles ;
- images ;
- appels réseau ;
- requêtes SQL ;
- index ;
- cache ;
- rendu ;
- mémoire.

Ne jamais affirmer :

« C’est optimisé »

sans mesure.

# 149\. Audit UX

Même dans un document technique, le développeur doit vérifier :

- loading ;
- erreur ;
- vide ;
- succès ;
- mobile ;
- clavier ;
- accessibilité ;
- feedback utilisateur.

Une interface qui fonctionne techniquement mais laisse l’utilisateur sans indication pendant 8 secondes est une mauvaise expérience.

# 150\. Audit des dépendances

Pour chaque dépendance :

- est-elle nécessaire ?
- est-elle maintenue ?
- est-elle fiable ?
- existe-t-il une solution native ?
- apporte-t-elle suffisamment de valeur ?
- introduit-elle un risque ?

# 151\. Audit des tests

Demander :

« Quels tests prouvent que cette fonctionnalité fonctionne ? »

Puis :

« Quels scénarios ne sont pas couverts ? »

Et :

« Quel bug pourrait passer malgré ces tests ? »

# 152\. Audit de l’IA elle-même

Une technique très utile :

Demander à l’IA de critiquer son propre travail.

Exemple :

Analyse l'implémentation que tu viens de produire.  
<br/>Ne cherche pas à la défendre.  
<br/>Cherche au contraire :  
\- bugs potentiels ;  
\- failles de sécurité ;  
\- mauvaises hypothèses ;  
\- problèmes de performance ;  
\- problèmes de maintenabilité ;  
\- dépendances inutiles ;  
\- cas limites ;  
\- erreurs de concurrence ;  
\- problèmes d'accessibilité.  
<br/>Classe chaque problème par gravité.

Puis demander à une autre IA ou à une autre session de réaliser un audit indépendant.

# PART XXI — CHECKLIST DE CONTRÔLE AVANT PRODUCTION

# 153\. Fonctionnel

- Toutes les fonctionnalités demandées existent.
- Les cas normaux fonctionnent.
- Les cas limites ont été testés.
- Les erreurs sont gérées.
- Les états vides sont gérés.
- Les états de chargement sont gérés.

# 154\. Sécurité

- Authentification correctement implémentée.
- Autorisation vérifiée côté serveur.
- Secrets non exposés.
- Entrées validées.
- Données sensibles protégées.
- Dépendances vérifiées.
- Uploads contrôlés.
- Rate limiting considéré si nécessaire.

# 155\. Performance

- Images optimisées.
- Requêtes raisonnables.
- Pas de requêtes inutiles.
- Bundle analysé si nécessaire.
- Cache utilisé uniquement lorsque pertinent.
- Performance mesurée.

# 156\. Qualité

- Code lisible.
- Architecture compréhensible.
- Duplication raisonnablement contrôlée.
- Pas d’abstraction inutile.
- Tests présents.
- Erreurs compréhensibles.
- Documentation suffisante.

# 157\. Déploiement

- Variables d’environnement configurées.
- Build reproductible.
- CI/CD vérifié.
- Logs disponibles.
- Monitoring disponible si nécessaire.
- Rollback possible.
- Sauvegardes configurées si nécessaire.

# PART XXII — ERREURS DE RAISONNEMENT À ÉVITER

# 158\. « Cette technologie est populaire donc elle est meilleure »

Faux.

Popularité ≠ adéquation.

# 159\. « React est obligatoire pour un site moderne »

Faux.

HTML/CSS/JS peuvent suffire.

# 160\. « Les microservices sont plus professionnels »

Faux.

Une architecture professionnelle est une architecture adaptée au problème.

# 161\. « Il faut utiliser l’IA partout »

Faux.

Une solution simple sans IA est parfois meilleure.

# 162\. « Plus de dépendances = plus de fonctionnalités »

Faux.

Chaque dépendance augmente aussi la complexité.

# 163\. « Si les tests passent, le logiciel est correct »

Faux.

Les tests ne peuvent couvrir que les comportements qu’ils vérifient.

# 164\. « Le frontend peut gérer la sécurité »

Faux.

Le frontend est contrôlé par l’utilisateur.

Les décisions de sécurité critiques doivent être imposées côté serveur.

# 165\. « Une technologie plus complexe est plus scalable »

Pas nécessairement.

La scalabilité dépend notamment :

- architecture ;
- données ;
- réseau ;
- infrastructure ;
- charge ;
- conception.

# 166\. « Tout doit être optimisé dès le départ »

Faux.

Il faut distinguer :

- bonnes fondations ;
- optimisation prématurée.

Une bonne règle :

mesurer → identifier le problème → optimiser → mesurer à nouveau.

# PART XXIII — CARTE MENTALE D’UNE APPLICATION MODERNE

# 167\. Vue synthétique

UTILISATEUR  
│  
↓  
INTERFACE  
HTML/CSS/JS/UI  
│  
↓  
FRONTEND / CLIENT  
React / Vue / Angular  
│  
↓  
NETWORK  
HTTP / HTTPS  
│  
↓  
API / BACKEND  
REST / GraphQL / WebSocket  
│  
┌───────────┼───────────┐  
↓ ↓ ↓  
AUTH LOGIQUE SERVICES  
│  
↓  
DATABASE  
PostgreSQL / MySQL  
│  
┌───────────┼───────────┐  
↓ ↓ ↓  
CACHE FILES SEARCH  
Redis Storage Index  
│  
↓  
INFRASTRUCTURE  
Cloud / Docker / CDN  
│  
↓  
OBSERVABILITY  
Logs / Metrics / Traces

Cette carte doit devenir progressivement familière.

# PART XXIV — CE QU’IL FAUT SAVOIR RECONNAÎTRE

# 168\. Niveau de reconnaissance minimal

À la fin de cette première lecture, les termes suivants doivent au moins être familiers :

### Web

- HTTP
- HTTPS
- DNS
- URL
- browser
- client/server
- API
- request
- response
- cookie
- cache
- CDN

### Frontend

- HTML
- CSS
- JavaScript
- TypeScript
- DOM
- component
- state
- routing
- React
- Vue
- Angular
- Tailwind
- Bootstrap

### Backend

- server
- API
- REST
- GraphQL
- WebSocket
- authentication
- authorization
- middleware
- runtime
- Node.js

### Data

- SQL
- NoSQL
- PostgreSQL
- MySQL
- SQLite
- MongoDB
- Redis
- ORM
- index
- transaction
- migration

### Architecture

- monolith
- modular monolith
- microservices
- serverless
- event-driven
- queue
- cache

### Delivery

- Git
- GitHub
- package manager
- Docker
- CI/CD
- staging
- production
- environment variables

### Quality

- unit test
- integration test
- E2E
- lint
- formatter
- refactoring
- technical debt
- logging
- monitoring
- tracing

### Mobile

- native
- PWA
- React Native
- Flutter
- iOS
- Android

# PART XXV — CE QUE TU DOIS SAVOIR FAIRE AVEC CETTE CARTE

# 169\. Scénario 1 — On te parle de PWA

Tu dois pouvoir penser :

PWA  
→ Web  
→ expérience applicative  
→ installation  
→ offline/cache  
→ service worker  
→ alternative partielle au natif

Puis demander :

« Pourquoi aurais-je besoin d’une PWA dans ce projet ? »

# 170\. Scénario 2 — On te parle de SQL injection

Tu dois immédiatement situer :

Cybersécurité  
→ application Web  
→ entrée utilisateur  
→ requête SQL  
→ backend/database  
→ validation/paramétrage

Tu n’as pas besoin d’être pentester pour reconnaître le problème.

# 171\. Scénario 3 — On te parle de Redis

Tu dois penser :

Infrastructure / Data  
→ mémoire rapide  
→ cache  
→ sessions  
→ données temporaires  
→ performance

Puis :

« Avons-nous réellement besoin d’un cache ? »

# 172\. Scénario 4 — On te propose Kubernetes

Tu dois penser :

Infrastructure  
→ containers  
→ orchestration  
→ scaling  
→ complexité opérationnelle

Puis demander :

« Quel problème actuel nécessite Kubernetes ? »

# 173\. Scénario 5 — On te propose React pour un site vitrine

Tu dois demander :

- Le site est-il interactif ?
- Quelle complexité ?
- SEO ?
- contenu dynamique ?
- besoin de composants ?
- équipe déjà React ?
- alternative statique/CMS ?

# 174\. Scénario 6 — On te propose WordPress pour un SaaS métier

Tu dois demander :

- logique métier ?
- authentification ?
- workflows ?
- permissions ?
- intégrations ?
- volume ?
- personnalisation ?

Puis comparer sérieusement avec une architecture custom.

# PART XXVI — COMMENT PRENDRE UNE DÉCISION TECHNIQUE

# 175\. La matrice de décision

Pour comparer deux technologies, utiliser :

| Critère | Question |
| --- | --- |
| Besoin | Résout-elle réellement le problème ? |
| Complexité | Combien de complexité ajoute-t-elle ? |
| Performance | Répond-elle aux contraintes ? |
| Sécurité | Quel est son profil de risque ? |
| Coût | Combien coûte-t-elle à utiliser ? |
| Équipe | Quelles compétences faut-il ? |
| Maintenance | Est-elle facile à maintenir ? |
| Écosystème | Existe-t-il de bons outils ? |
| Documentation | Peut-on trouver de l’aide ? |
| Scalabilité | Peut-elle évoluer suffisamment ? |
| Vendor lock-in | Sommes-nous fortement dépendants ? |
| Réversibilité | Peut-on changer plus tard ? |

# 176\. La règle des contraintes

Une technologie doit être choisie à partir des contraintes.

Exemple :

Projet  
│  
├── Budget faible  
├── Petite équipe  
├── Délais courts  
├── SEO important  
├── Contenu éditorial  
└── Peu de logique métier

La solution optimale sera probablement différente de :

Projet  
│  
├── 1 million d'utilisateurs  
├── Temps réel  
├── Paiements  
├── Haute disponibilité  
├── Équipes multiples  
└── Données critiques

Même problème apparent :

« Construire un site »

Mais problèmes techniques radicalement différents.

# PART XXVII — LA PLACE DE L’IA DANS TON PROCESSUS

# 177\. Avant de demander du code

Demander à l’IA :

1\. Reformule le problème.  
2\. Identifie les contraintes.  
3\. Liste les inconnues.  
4\. Propose les architectures possibles.  
5\. Compare-les.  
6\. Recommande une solution.  
7\. Explique les risques.  
8\. Définis les critères de validation.

# 178\. Pendant l’implémentation

Demander :

Implémente uniquement l'étape X.  
<br/>Ne modifie pas :  
\- Y  
\- Z  
<br/>Respecte :  
\- architecture  
\- conventions  
\- sécurité  
\- accessibilité  
\- tests  
<br/>À la fin :  
\- liste les fichiers modifiés ;  
\- explique les choix ;  
\- indique les risques ;  
\- indique comment tester.

# 179\. Après l’implémentation

Demander :

Audite ton implémentation.  
<br/>Cherche activement :  
\- bugs ;  
\- sécurité ;  
\- performance ;  
\- maintenabilité ;  
\- accessibilité ;  
\- edge cases ;  
\- dette technique.  
<br/>Ne présume pas que ton code est correct.

# 180\. Avant production

Demander :

Fais un pre-production review.  
<br/>Classe les problèmes :  
P0 = bloquant  
P1 = critique  
P2 = important  
P3 = amélioration  
<br/>Pour chaque problème :  
\- localisation ;  
\- impact ;  
\- scénario ;  
\- correction ;  
\- méthode de vérification.

# PART XXVIII — LA LIMITE DE CETTE CULTURE TECHNIQUE

# 181\. Ce document n’est pas une fin

Connaître :

« Redis = cache »

ne signifie pas savoir concevoir un système de cache.

Connaître :

« WebSocket = temps réel »

ne signifie pas savoir gérer :

- reconnexion ;
- authentification ;
- concurrence ;
- présence ;
- scaling.

Connaître :

« PostgreSQL = base relationnelle »

ne signifie pas savoir :

- concevoir un schéma ;
- optimiser une requête ;
- gérer les transactions ;
- administrer une base.

C’est précisément pour cela que ce document constitue le **niveau cartographique**, et non le niveau expert.

# PART XXIX — CE QUI DOIT ÊTRE APPROFONDI PLUS TARD

# 182\. Concepts prioritaires pour approfondissement

Après la lecture de la carte, les concepts qui méritent probablement des sessions approfondies sont :

### Priorité 1 — Fondations

- HTTP ;
- DNS ;
- navigateur ;
- JavaScript ;
- TypeScript ;
- DOM ;
- API ;
- SQL ;
- Git.

### Priorité 2 — Construction d’applications

- architecture frontend ;
- architecture backend ;
- authentification ;
- autorisation ;
- API REST ;
- bases relationnelles ;
- ORM ;
- migrations ;
- gestion d’état ;
- caching.

### Priorité 3 — Architecture

- monolithes ;
- modular monolith ;
- microservices ;
- serverless ;
- événements ;
- queues ;
- systèmes distribués.

### Priorité 4 — Production

- Docker ;
- CI/CD ;
- monitoring ;
- logging ;
- observabilité ;
- déploiement ;
- gestion des secrets.

### Priorité 5 — Performance

- rendering ;
- caching ;
- CDN ;
- optimisation réseau ;
- bases de données ;
- Core Web Vitals ;
- profiling.

# PART XXX — TEST DE MAÎTRISE DU TERRITOIRE

Avant de considérer la culture générale Web comme suffisamment solide, tu devrais progressivement être capable de répondre à ces questions.

## Question 1

Quelle est la différence entre :

HTML, CSS et JavaScript ?

## Question 2

Quelle est la différence entre :

Java et JavaScript ?

## Question 3

Quelle est la différence entre :

React, React Native et Flutter ?

## Question 4

Pourquoi utiliser :

WordPress plutôt qu’une application custom ?

## Question 5

Pourquoi utiliser :

PostgreSQL plutôt que MongoDB ?

## Question 6

Pourquoi utiliser :

REST plutôt que GraphQL ?

## Question 7

Quand un WebSocket est-il réellement nécessaire ?

## Question 8

Pourquoi ne pas utiliser des microservices dès le début ?

## Question 9

Quelle différence entre :

authentification et autorisation ?

## Question 10

Pourquoi cacher un bouton « Admin » n’est-il pas une mesure de sécurité ?

## Question 11

Pourquoi utiliser un cache ?

## Question 12

Pourquoi un cache peut-il aussi créer des problèmes ?

## Question 13

Quelle différence entre :

Git et GitHub ?

## Question 14

Pourquoi utiliser Docker ?

## Question 15

Pourquoi écrire des tests ?

## Question 16

Quelle différence entre :

unit test, integration test et E2E ?

## Question 17

Pourquoi le code généré par une IA doit-il être audité ?

## Question 18

Comment choisir une technologie lorsque plusieurs sont raisonnables ?

# PART XXXI — RÈGLES DIRECTRICES

# 183\. Les 20 règles à retenir

### 1.

**Une technologie existe généralement parce qu’elle résout un problème.**

Cherche d’abord le problème.

### 2.

**La popularité n’est pas un critère suffisant.**

### 3.

**Plus complexe ne signifie pas plus professionnel.**

### 4.

**Le bon outil dépend du contexte.**

### 5.

**Comprendre le problème avant de choisir la technologie.**

### 6.

**Ne pas confondre langage, bibliothèque, framework, runtime et outil.**

### 7.

**Ne pas confondre Git et GitHub.**

### 8.

**Ne pas confondre Java et JavaScript.**

### 9.

**Ne pas confondre SQL et PostgreSQL.**

### 10.

**Ne pas confondre authentification et autorisation.**

### 11.

**Ne pas mettre la sécurité uniquement dans le frontend.**

### 12.

**Ne pas ajouter une base de données sans besoin réel.**

### 13.

**Ne pas ajouter un cache sans problème de performance identifié.**

### 14.

**Ne pas ajouter des microservices sans problème justifiant leur complexité.**

### 15.

**Ne pas ajouter une dépendance sans raison.**

### 16.

**Mesurer avant d’optimiser.**

### 17.

**Tester les comportements importants.**

### 18.

**Documenter les décisions techniques importantes.**

### 19.

**Faire expliquer les choix à l’IA.**

### 20.

**Ne jamais considérer l’IA comme l’autorité finale.**

# PART XXXII — CARTE FINALE

Le territoire Web & Software Engineering peut finalement être résumé ainsi :

WEB & SOFTWARE ENGINEERING  
│  
┌───────────────────────────┼───────────────────────────┐  
│ │ │  
FONDATIONS WEB LOGICIEL  
│ │ │  
Algorithmes HTTP/DNS Architecture  
Programmation Browser Design  
Structures HTML Tests  
Complexité CSS Git  
JS CI/CD  
│ │ │  
└───────────────────────────┼───────────────────────────┘  
│  
CONSTRUCTION  
│  
┌──────────────────┼──────────────────┐  
↓ ↓ ↓  
Frontend Backend Data  
│ │ │  
React/Vue APIs/Logic SQL/NoSQL  
TypeScript Auth PostgreSQL  
State Services Redis  
│ │ │  
└──────────────────┼──────────────────┘  
│  
DELIVERY  
│  
Docker / Cloud / CI/CD  
│  
↓  
PRODUCTION  
│  
Logs / Metrics / Traces  
│  
↓  
EVOLUTION  
│  
Maintenance / Refactoring / Scaling

# PART XXXIII — LA COMPÉTENCE FINALE RECHERCHÉE

Le but de ce document n’est pas que tu puisses réciter 150 définitions.

Le but est qu’un jour, lorsqu’on te dit :

« On veut construire une plateforme de réservation avec paiement, comptes utilisateurs, tableau de bord administrateur, notifications et application mobile. »

Tu ne répondes plus immédiatement :

« On va utiliser React, Supabase et Flutter. »

Tu dois commencer à raisonner :

Plateforme de réservation  
↓  
Quel type de produit ?  
↓  
Quels utilisateurs ?  
↓  
Quels rôles ?  
↓  
Quelles données ?  
↓  
Quelles relations ?  
↓  
Quelle authentification ?  
↓  
Quelle autorisation ?  
↓  
Quel paiement ?  
↓  
Quels webhooks ?  
↓  
Quelles notifications ?  
↓  
Besoin de temps réel ?  
↓  
Web + mobile ?  
↓  
PWA / React Native / Flutter / natif ?  
↓  
Quel backend ?  
↓  
Quelle base ?  
↓  
Quelle architecture ?  
↓  
Quel niveau de trafic ?  
↓  
Quels besoins de sécurité ?  
↓  
Quels besoins de performance ?  
↓  
Quels tests ?  
↓  
Quel déploiement ?

Puis seulement :

**Quelles technologies sont les plus adaptées ?**

C’est exactement cette transformation du raisonnement que ce projet cherche à produire.

# CONCLUSION

Le Web & Software Engineering n’est pas une collection de frameworks.

C’est un ensemble de problèmes récurrents :

- représenter de l’information ;
- faire communiquer des systèmes ;
- construire des interfaces ;
- traiter des données ;
- gérer des utilisateurs ;
- organiser de la logique métier ;
- assurer la sécurité ;
- maintenir la performance ;
- tester ;
- déployer ;
- observer ;
- faire évoluer.

Les technologies sont des **réponses différentes à ces problèmes**.

Ainsi, la compétence technique recherchée n’est pas :

« Je connais React. »

Mais plutôt :

« Je comprends le problème, je connais les familles de solutions disponibles, je peux comparer leurs compromis, choisir une direction raisonnable, demander à l’IA de l’implémenter avec des contraintes précises et vérifier que le résultat respecte réellement les exigences. »

C’est cette capacité qui permet de devenir **AI-augmented** sans devenir **AI-dependent**.

# FICHE DE RÉFÉRENCE RAPIDE

## Quand je rencontre un nouveau terme

Je me pose :

1.  **Dans quel domaine se situe-t-il ?**
2.  **De quelle famille est-il ?**
3.  **Quel problème résout-il ?**
4.  **Pourquoi a-t-il été créé ?**
5.  **Quand dois-je penser à lui ?**
6.  **Quelles sont ses alternatives ?**
7.  **Quels sont ses avantages ?**
8.  **Quels sont ses inconvénients ?**
9.  **Quelles contraintes impose-t-il ?**
10. **Comment demander à une IA de l’utiliser correctement ?**
11. **Comment vérifier que l’IA l’a correctement utilisé ?**
12. **Est-ce un concept que je dois approfondir ou simplement savoir reconnaître ?**

# FORMULE CENTRALE DU PROJET

**Je ne cherche pas à tout savoir faire.**

**Je cherche à savoir suffisamment pour comprendre ce que je vois, reconnaître ce dont j’ai besoin, choisir intelligemment, diriger l’IA et contrôler son travail.**

**Document 01 — Web & Software Engineering — Version 1.0**