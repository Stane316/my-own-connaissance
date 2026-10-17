# **DOCUMENT 03 — CARTOGRAPHIE DE LA CYBERSÉCURITÉ**

**Version : 1.0 — Document fondamental**

**Objectif : culture technique, conception sécurisée et contrôle des systèmes assistés par IA**

**Niveau visé : développeur / créateur de produits utilisant fortement l’IA, pas expert cybersécurité**

## **0\. Positionnement du document**

Ce document n’a pas pour objectif de faire de toi un pentester, un analyste SOC ou un cryptographe.

Son objectif est beaucoup plus stratégique :

**te donner suffisamment de culture en cybersécurité pour ne pas construire, déployer ou faire construire par une IA un système dangereusement vulnérable sans t’en rendre compte.**

À la fin de cette cartographie, tu dois pouvoir :

reconnaître les principales familles de menaces ;

identifier ce qui doit être protégé ;

comprendre pourquoi une vulnérabilité existe ;

estimer grossièrement son importance ;

savoir quelles protections existent ;

savoir **quand penser à une protection donnée** ;

choisir entre plusieurs approches ;

demander à une IA d'implémenter une fonctionnalité de manière sécurisée ;

vérifier si ce que l’IA a produit est réellement sécurisé ;

reconnaître les signaux d’une mauvaise implémentation ;

savoir quand une situation dépasse ton niveau et nécessite un spécialiste ;

intégrer la sécurité **dès la conception**, plutôt qu’après avoir construit le produit.

La logique générale sera :

**ACTIFS → MENACES → SURFACE D’ATTAQUE → VULNÉRABILITÉS → RISQUES → PROTECTIONS → DÉTECTION → RÉPONSE → AUDIT → AMÉLIORATION**

# **A — VUE GLOBALE : COMPRENDRE LE TERRITOIRE DE LA CYBERSÉCURITÉ**

## **A.1. La cybersécurité, c’est quoi ?**

La cybersécurité est l’ensemble des pratiques, technologies, processus et décisions permettant de protéger :

des données ;

des systèmes ;

des applications ;

des utilisateurs ;

des infrastructures ;

des identités ;

des services ;

des réseaux ;

contre :

l’accès non autorisé ;

la modification non autorisée ;

la destruction ;

la divulgation ;

l’interruption ;

l’abus ;

la compromission.

Mais cette définition reste insuffisante.

La cybersécurité est surtout une **gestion du risque numérique**.

On ne cherche pas à rendre un système absolument inviolable.

On cherche à réduire suffisamment :

**la probabilité qu’un événement dangereux arrive × son impact s’il arrive.**

# **A.2. Le modèle mental fondamental**

Lorsque tu regardes n’importe quel système, commence par poser cette chaîne :

QU'EST-CE QUE JE DOIS PROTÉGER ?  
↓  
CONTRE QUOI ?  
↓  
PAR QUELLE VOIE ?  
↓  
QU'EST-CE QUI POURRAIT MAL TOURNER ?  
↓  
QUEL SERAIT L'IMPACT ?  
↓  
COMMENT PRÉVENIR ?  
↓  
COMMENT DÉTECTER ?  
↓  
COMMENT RÉAGIR ?  
↓  
COMMENT VÉRIFIER ?

C'est le réflexe de base que tu dois développer.

# **A.3. Les grandes familles de la cybersécurité**

La cybersécurité n'est pas une seule discipline.

Elle contient plusieurs territoires.

### **1\. Sécurité des applications**

Protection :

sites web ;

APIs ;

applications mobiles ;

logiciels ;

backend ;

frontend ;

microservices.

Exemples :

XSS ;

SQL injection ;

contrôle d'accès défaillant ;

mauvaise gestion des sessions ;

upload dangereux.

### **2\. Sécurité des identités et des accès**

On cherche à répondre à :

**Qui es-tu ?**

et :

**Qu'as-tu le droit de faire ?**

Concepts :

authentification ;

autorisation ;

sessions ;

MFA ;

RBAC ;

OAuth ;

OpenID Connect ;

gestion des comptes ;

privilèges.

### **3\. Sécurité des données**

Protection :

données personnelles ;

mots de passe ;

tokens ;

clés API ;

documents ;

bases de données ;

sauvegardes.

Concepts :

chiffrement ;

hachage ;

secrets ;

contrôle d'accès ;

sauvegarde ;

confidentialité ;

intégrité.

### **4\. Sécurité réseau**

Protection des communications et infrastructures :

réseau ;

serveurs ;

ports ;

protocoles ;

connexions ;

trafic.

Concepts :

firewall ;

TLS ;

VPN ;

segmentation ;

DNS ;

réseau privé ;

monitoring.

### **5\. Sécurité de l'infrastructure**

Protection :

serveurs ;

systèmes d'exploitation ;

cloud ;

conteneurs ;

machines ;

environnements de déploiement.

### **6\. DevSecOps**

Intégration de la sécurité dans le cycle de développement :

Code  
↓  
Tests  
↓  
Analyse sécurité  
↓  
Build  
↓  
Déploiement  
↓  
Monitoring

La sécurité devient une partie du développement normal.

### **7\. Sécurité opérationnelle**

Une fois le système déployé :

logs ;

alertes ;

monitoring ;

détection ;

incidents ;

réponse ;

récupération.

### **8\. Gouvernance et gestion des risques**

On s'intéresse à :

politiques ;

responsabilités ;

conformité ;

risques ;

procédures ;

continuité ;

gestion des incidents.

### **9\. Sécurité humaine**

Une grande partie des attaques ne commencent pas par du code.

Elles peuvent commencer par :

phishing ;

ingénierie sociale ;

mot de passe réutilisé ;

erreur humaine ;

mauvaise configuration ;

partage accidentel d'informations.

# **A.4. Les trois propriétés fondamentales : CIA**

Un des modèles les plus importants est la triade :

**Confidentiality — Integrity — Availability**

En français :

**Confidentialité — Intégrité — Disponibilité**

### **Confidentialité**

Seules les personnes autorisées peuvent accéder aux informations.

Exemple :

Un utilisateur ne doit pas pouvoir lire les données privées d'un autre utilisateur.

### **Intégrité**

Les données ne doivent pas être modifiées de manière non autorisée.

Exemple :

Un utilisateur ne doit pas pouvoir modifier le prix d'une facture appartenant à quelqu'un d'autre.

### **Disponibilité**

Le service doit rester accessible lorsqu'il est nécessaire.

Exemple :

Une application de paiement doit rester disponible.

### **Réflexe**

Pour chaque fonctionnalité importante :

**Que se passe-t-il si la confidentialité est violée ?**

**Que se passe-t-il si l'intégrité est violée ?**

**Que se passe-t-il si la disponibilité est violée ?**

# **A.5. Actif, menace, vulnérabilité, risque**

Ces quatre notions doivent devenir automatiques.

## **Actif**

Quelque chose qui possède de la valeur.

Exemples :

compte utilisateur ;

mot de passe ;

base de données ;

clé API ;

argent ;

réputation ;

serveur ;

code source.

## **Menace**

Quelque chose susceptible de causer un dommage.

Exemples :

attaquant ;

malware ;

phishing ;

erreur humaine ;

insider malveillant ;

mauvaise configuration.

## **Vulnérabilité**

Une faiblesse exploitable.

Exemple :

API :  
GET /users/123  
<br/>L'application ne vérifie pas  
si l'utilisateur connecté possède le compte 123.

La faiblesse est un contrôle d'accès insuffisant.

## **Risque**

Combinaison :

**probabilité × impact**

Une vulnérabilité faible sur une donnée sans importance n'a pas le même risque qu'une vulnérabilité permettant d'accéder à tous les comptes clients.

# **A.6. Surface d'attaque**

La **surface d'attaque** représente les endroits par lesquels un système peut potentiellement être attaqué.

Exemple :

INTERNET  
│  
┌──────────────┼──────────────┐  
↓ ↓ ↓  
Web API Mobile  
│ │ │  
└──────────────┼──────────────┘  
↓  
Backend  
↓  
Database  
↓  
External Services

Chaque :

endpoint ;

formulaire ;

upload ;

API ;

port ;

intégration ;

compte ;

dépendance ;

peut devenir une partie de la surface d'attaque.

# **A.7. Défense en profondeur**

Ne jamais penser :

« J'ai un firewall donc je suis sécurisé. »

ou :

« J'ai HTTPS donc je suis sécurisé. »

La sécurité fonctionne mieux en couches.

Utilisateur  
↓  
MFA  
↓  
HTTPS  
↓  
Firewall / WAF  
↓  
Validation  
↓  
Authentification  
↓  
Autorisation  
↓  
Application sécurisée  
↓  
Base de données protégée  
↓  
Logs  
↓  
Monitoring  
↓  
Backup

Une couche peut échouer.

Les autres doivent limiter les dégâts.

# **B — CONCEPTS ESSENTIELS À ABSOLUMENT CONNAÎTRE****B.1. Authentification ≠ Autorisation**

C'est probablement l'une des distinctions les plus importantes.

### **Authentification**

**Qui es-tu ?**

Exemple :

email + mot de passe

Le système vérifie ton identité.

### **Autorisation**

**Qu'as-tu le droit de faire ?**

Exemple :

Stane est connecté.  
<br/>Mais Stane n'est pas administrateur.  
<br/>Donc :  
→ accès au profil : OUI  
→ modification de son profil : OUI  
→ suppression de tous les utilisateurs : NON

Une application peut avoir une excellente authentification et une très mauvaise autorisation.

# **B.2. Principe du moindre privilège**

Un utilisateur, service ou programme doit recevoir :

**uniquement les permissions dont il a réellement besoin.**

Exemple :

Une application qui doit uniquement lire une table ne devrait pas avoir des droits permettant de supprimer toute la base.

# **B.3. Zero Trust**

Le principe général :

**Ne jamais faire confiance automatiquement ; vérifier explicitement.**

Cela ne signifie pas :

« Personne n'est digne de confiance. »

Cela signifie :

**l'identité, le contexte et les permissions doivent être vérifiés au moment approprié.**

# **B.4. Hachage ≠ chiffrement ≠ encodage**

Erreur extrêmement fréquente.

## **Encodage**

Transformation destinée principalement à représenter/transporter une donnée.

Exemple :

Base64

Ce n'est **pas** une protection cryptographique.

## **Chiffrement**

Transformation réversible grâce à une clé.

Donnée  
↓  
Chiffrement + clé  
↓  
Donnée chiffrée  
↓  
Déchiffrement + clé  
↓  
Donnée originale

Utilisé lorsque l'on doit récupérer la donnée originale.

## **Hachage**

Transformation conçue pour produire une empreinte.

mot de passe  
↓  
hachage  
↓  
empreinte

On ne cherche normalement pas à récupérer le mot de passe original.

Pour les mots de passe, on utilise des fonctions spécialement conçues pour le stockage de mots de passe, avec notamment un mécanisme de sel et un coût de calcul approprié.

# **B.5. HTTPS et TLS**

HTTPS protège les communications HTTP grâce à TLS.

Il permet notamment de protéger :

la confidentialité du trafic ;

l'intégrité des communications ;

l'authentification du serveur via les certificats.

Réflexe :

**Une application web sérieuse doit fonctionner en HTTPS.**

Mais :

HTTPS ne rend pas automatiquement l'application sécurisée.

Il protège principalement **la communication**, pas les erreurs logiques de ton application.

# **B.6. Secret**

Un secret est une information dont la possession donne un accès ou un pouvoir particulier.

Exemples :

clé API ;

mot de passe ;

token ;

clé privée ;

secret de webhook ;

credentials de base de données.

Règle fondamentale :

**Un secret ne doit pas être exposé dans le code public, le frontend, Git ou les logs.**

# **B.7. Gestion des secrets**

Mauvais :

const API_KEY = "sk-xxxxxxxx";

dans un dépôt Git.

Meilleur principe :

Application  
↓  
Variable d'environnement / Secret Manager  
↓  
Secret

Mais attention :

une variable d'environnement n'est pas une solution magique à tous les problèmes de secrets.

Dans des environnements complexes, on peut utiliser un véritable **secret manager**.

# **B.8. Injection**

Une injection survient lorsqu'une donnée contrôlée par un utilisateur est interprétée comme une partie d'une commande ou d'un langage.

Exemples :

SQL injection ;

command injection ;

LDAP injection ;

NoSQL injection.

Principe général de défense :

**séparer les données des instructions.**

Par exemple, utiliser des requêtes paramétrées plutôt que construire une requête SQL par concaténation de chaînes contrôlées par l'utilisateur.

# **B.9. XSS**

Cross-Site Scripting.

Un attaquant parvient à faire exécuter du contenu JavaScript non fiable dans le contexte d'une page web.

Risques :

vol de données accessibles au navigateur ;

actions réalisées au nom de l'utilisateur ;

modification de l'interface ;

phishing ;

compromission de session dans certains scénarios.

Défenses :

escaping/output encoding approprié ;

sanitization lorsque du HTML est réellement autorisé ;

CSP ;

cookies correctement configurés ;

éviter les mécanismes dangereux d'injection HTML.

# **B.10. CSRF**

Cross-Site Request Forgery.

L'idée générale :

un utilisateur authentifié peut être amené à effectuer involontairement une action sur une application.

Les défenses dépendent de l'architecture, mais peuvent inclure :

tokens CSRF ;

cookies SameSite correctement configurés ;

vérification d'origine dans certains contextes ;

conception appropriée des APIs.

# **B.11. IDOR / BOLA**

Un utilisateur modifie simplement un identifiant :

/account/123

en :

/account/124

et découvre les données d'un autre utilisateur.

Le problème n'est pas forcément l'identifiant lui-même.

Le problème est :

**l'application vérifie-t-elle réellement que cet utilisateur est autorisé à accéder à cette ressource ?**

C'est une erreur d'autorisation.

# **B.12. Validation des entrées**

Ne jamais supposer :

« Le frontend vérifie donc c'est bon. »

Un attaquant peut appeler directement l'API.

La validation importante doit exister côté serveur lorsqu'elle concerne la sécurité ou l'intégrité des données.

Exemple :

Frontend  
↓  
Validation UX  
↓  
API  
↓  
Validation serveur  
↓  
Business logic

# **B.13. Rate limiting**

Le rate limiting limite le nombre de requêtes qu'un client peut effectuer dans une période donnée.

Utile notamment pour :

login ;

OTP ;

reset password ;

APIs coûteuses ;

endpoints sensibles ;

prévention de certains abus.

Exemple conceptuel :

100 tentatives / minute  
↓  
limite atteinte  
↓  
requêtes temporairement bloquées

# **B.14. Logging**

Les logs permettent de conserver des traces utiles.

Exemples :

connexion ;

échec d'authentification ;

changement de mot de passe ;

changement de privilège ;

action administrative ;

erreur critique.

Mais attention :

**ne jamais logger aveuglément les secrets, mots de passe ou tokens.**

# **B.15. Monitoring**

Logging :

« Voici ce qui s'est passé. »

Monitoring :

« Voici ce qui se passe et ce qui semble anormal. »

Exemple :

50 échecs de connexion  
↓  
détection  
↓  
alerte

# **B.16. Backup**

Un backup est une copie permettant notamment de récupérer des données après :

suppression accidentelle ;

panne ;

corruption ;

ransomware ;

erreur humaine.

Mais :

**avoir un backup ≠ avoir un backup fiable.**

Il faut également :

vérifier les sauvegardes ;

tester leur restauration ;

protéger les sauvegardes ;

définir leur fréquence ;

déterminer leur rétention.

# **B.17. Patch et dépendances**

Une application dépend souvent de dizaines ou centaines de bibliothèques.

Une dépendance vulnérable peut devenir une porte d'entrée.

Il faut donc :

connaître ses dépendances ;

surveiller les vulnérabilités ;

mettre à jour raisonnablement ;

éviter les dépendances inutiles ;

verrouiller les versions lorsque pertinent ;

auditer la supply chain.

# **B.18. Secure by design**

La sécurité ne doit pas être :

Produit terminé  
↓  
OH !  
↓  
Ajoutons la sécurité.

Mais :

Idée  
↓  
Architecture  
↓  
Threat modeling  
↓  
Conception  
↓  
Développement  
↓  
Tests  
↓  
Déploiement  
↓  
Monitoring

# **C — TECHNOLOGIES, MÉTHODES ET OUTILS**

L'objectif ici n'est pas de mémoriser chaque outil.

Tu dois savoir :

**ce que l'outil fait, quel problème il traite et quand il devient pertinent.**

# **C.1. HTTPS / TLS**

**Problème :** protéger les communications.

**À penser :**

dès qu'une application communique sur Internet.

# **C.2. Firewall**

Un firewall contrôle certains flux réseau selon des règles.

Il peut décider :

Autoriser  
Bloquer

selon :

IP ;

port ;

protocole ;

zone ;

règles spécifiques.

# **C.3. WAF**

Web Application Firewall.

Spécialisé dans la protection de trafic web.

Peut contribuer à détecter/bloquer certaines attaques web.

Mais :

**un WAF ne remplace jamais une application correctement développée.**

# **C.4. VPN**

Un VPN crée généralement un canal sécurisé entre des points.

Utile selon le contexte pour :

accès distant ;

connexion à un réseau privé ;

protection de certains flux.

VPN ≠ antivirus.

VPN ≠ sécurité totale.

VPN ≠ remplacement de TLS.

# **C.5. MFA**

Multi-Factor Authentication.

Au lieu de dépendre uniquement du mot de passe :

Mot de passe  
+  
Facteur supplémentaire

Exemples :

application d'authentification ;

clé de sécurité ;

passkey ;

facteur biométrique selon le système.

Pour les comptes sensibles, le MFA est souvent une protection extrêmement importante.

# **C.6. RBAC**

Role-Based Access Control.

Les permissions sont associées à des rôles.

USER  
↓  
role = editor  
↓  
permissions

Exemple :

Admin  
Editor  
User

# **C.7. ABAC**

Attribute-Based Access Control.

La décision dépend d'attributs.

Exemple conceptuel :

Utilisateur = Stane  
Rôle = Manager  
Département = Finance  
Ressource = Document Finance  
Heure = journée

La politique peut alors déterminer l'accès.

# **C.8. OAuth 2.0**

OAuth concerne principalement la **délégation d'autorisation**.

Exemple :

permettre à une application d'accéder à certaines ressources d'un utilisateur sans donner directement son mot de passe à cette application.

# **C.9. OpenID Connect**

OpenID Connect ajoute une couche d'identité au-dessus d'OAuth 2.0.

Simplification :

OAuth 2.0  
→ autorisation  
<br/>OpenID Connect  
→ authentification/identité

Cette distinction doit devenir automatique.

# **C.10. Sessions vs JWT**

Deux grandes approches.

### **Session**

Le serveur conserve l'état de session.

Client  
↓  
Cookie de session  
↓  
Serveur  
↓  
Session

### **JWT**

Le client reçoit un token signé contenant des informations structurées.

Client  
↓  
JWT  
↓  
API

Aucune approche n'est universellement meilleure.

Le choix dépend :

architecture ;

besoins ;

expiration ;

révocation ;

clients ;

infrastructure ;

niveau de complexité acceptable.

# **C.11. SAST**

Static Application Security Testing.

Analyse le code sans nécessairement exécuter l'application.

Peut détecter :

patterns dangereux ;

secrets ;

erreurs connues ;

constructions suspectes.

# **C.12. DAST**

Dynamic Application Security Testing.

Teste l'application en fonctionnement.

Différence simplifiée :

SAST → regarde le code  
DAST → regarde le comportement de l'application

Les deux sont complémentaires.

# **C.13. SCA**

Software Composition Analysis.

Analyse les dépendances utilisées par le projet.

Question :

« Est-ce que les bibliothèques que j'utilise comportent des vulnérabilités connues ? »

# **C.14. Secret scanning**

Cherche des secrets accidentellement exposés dans :

Git ;

code ;

commits ;

fichiers.

# **C.15. SIEM**

Security Information and Event Management.

Centralise et analyse des événements de sécurité provenant de différentes sources.

Conceptuellement :

Applications  
Servers  
Network  
Identity  
↓  
Logs  
↓  
SIEM  
↓  
Correlation / Alerts

# **C.16. EDR**

Endpoint Detection and Response.

Surveille des postes ou endpoints afin de détecter et répondre à certains comportements suspects.

# **C.17. Nmap, Wireshark, Burp Suite, etc.**

Ce sont des outils de cybersécurité connus, mais ils appartiennent à des catégories différentes.

**Nmap** : découverte et analyse réseau ;

**Wireshark** : analyse de trafic réseau ;

**Burp Suite** : analyse/test d'applications web ;

scanners de vulnérabilités : recherche automatisée de faiblesses connues ou suspectées.

Ces outils doivent être utilisés uniquement sur des systèmes que tu possèdes ou pour lesquels tu as une autorisation explicite.

Ton objectif ici est surtout de savoir :

**quel problème chaque catégorie d'outil permet d'investiguer.**

# **D — COMPARAISONS STRUCTURANTES**

## **D.1. Authentification vs Autorisation**

|     |     |     |
| --- | --- | --- |
|     | **Authentification** | **Autorisation** |
| Question | Qui es-tu ? | Que peux-tu faire ? |
| Exemple | Login | Accès admin |
| Moment | Identification | Contrôle d'accès |
| Erreur typique | mauvais mot de passe | accès à une ressource interdite |

# **D.2. Encodage vs chiffrement vs hachage**

|     |     |     |     |
| --- | --- | --- | --- |
|     | **Encodage** | **Chiffrement** | **Hachage** |
| Objectif | représentation | confidentialité | empreinte |
| Réversible | oui | oui avec clé | conçu pour être non réversible |
| Secret ? | non | oui | pas nécessairement |
| Exemple | Base64 | AES | Argon2id |

# **D.3. TLS vs VPN**

|     |     |
| --- | --- |
| **TLS** | **VPN** |
| protège certaines communications applicatives | crée généralement un tunnel sécurisé entre points |
| très courant sur le web | accès réseau / tunnel |
| HTTPS utilise TLS | HTTPS n'est pas un VPN |
| ne corrige pas les bugs applicatifs | ne corrige pas les bugs applicatifs |

# **D.4. Firewall vs WAF**

Firewall  
→ contrôle réseau  
<br/>WAF  
→ protection spécialisée du trafic web

Ils peuvent être complémentaires.

# **D.5. SAST vs DAST**

SAST  
→ code  
<br/>DAST  
→ application en fonctionnement

Un système mature peut utiliser les deux.

# **D.6. Backup vs réplication**

### **Réplication**

Copie synchronisée ou quasi synchronisée destinée notamment à améliorer disponibilité/continuité.

### **Backup**

Copie permettant notamment de revenir à un état antérieur.

Une réplication peut reproduire immédiatement une suppression accidentelle.

Donc :

**réplication ≠ backup.**

# **D.7. RBAC vs ABAC**

RBAC  
→ rôle  
<br/>ABAC  
→ attributs + politiques

RBAC est généralement plus simple.

ABAC peut être beaucoup plus flexible mais également plus complexe.

# **D.8. JWT vs session**

Ne demande jamais :

« Quel est le meilleur ? »

Demande :

« Lequel correspond le mieux à mon architecture et à mes contraintes ? »

C'est exactement le type de question que tu dois apprendre à poser à une IA.

# **E — DÉCISIONS : QUAND DOIS-JE PENSER À QUOI ?**

C'est probablement la partie la plus importante du document.

# **E.1. Je construis une application avec des comptes utilisateurs**

Pense immédiatement à :

Authentication  
Authorization  
Password storage  
Session management  
MFA  
Rate limiting  
Account recovery  
Logging

# **E.2. Je stocke des mots de passe**

Pense :

**hachage spécialisé pour mots de passe**

et non :

chiffrement maison.

Ne stocke jamais les mots de passe en clair.

# **E.3. Je stocke une information réellement confidentielle**

Pose :

Est-ce que cette donnée doit être récupérable ?

Si oui :

→ chiffrement potentiellement pertinent.

Si non et qu'il s'agit d'un secret d'authentification :

→ hachage approprié potentiellement pertinent.

# **E.4. Je construis une API**

Checklist mentale :

HTTPS  
Authentication  
Authorization  
Input validation  
Rate limiting  
Error handling  
Logging  
CORS  
Secrets  
Dependencies

# **E.5. Je construis un espace administrateur**

Le niveau de vigilance augmente.

Pense :

MFA ;

contrôle d'accès strict ;

sessions ;

journalisation ;

protection contre les tentatives répétées ;

séparation des privilèges ;

validation côté serveur ;

audit des actions sensibles.

# **E.6. Je permets l'upload de fichiers**

Danger potentiel important.

Questions :

quels types de fichiers ?

quelle taille ?

où sont-ils stockés ?

peuvent-ils être exécutés ?

comment sont-ils nommés ?

peuvent-ils écraser un fichier existant ?

sont-ils accessibles publiquement ?

faut-il les scanner ?

l'utilisateur peut-il contrôler leur chemin ?

# **E.7. Je connecte une API externe**

Pense :

API key  
Secret  
Permissions  
Rate limits  
Timeout  
Validation des réponses  
Gestion des erreurs  
Logs  
Rotation des clés

# **E.8. Je déploie une application**

Checklist minimale :

HTTPS  
Secrets protégés  
Debug désactivé  
Dependencies à jour  
Database sécurisée  
Backups  
Logs  
Monitoring  
Permissions minimales  
Headers de sécurité appropriés

# **E.9. Je construis un paiement**

Le niveau de vigilance doit être élevé.

Il faut notamment penser à :

ne jamais faire confiance au frontend pour confirmer un paiement ;

vérifier les événements côté serveur ;

authentifier les webhooks ;

empêcher les doubles traitements ;

vérifier les montants ;

vérifier les références ;

journaliser les événements importants ;

gérer les erreurs et les états intermédiaires.

# **E.10. Je construis un système avec des rôles**

Ne fais jamais :

if (user.role === "admin") {  
...  
}

et considère que c'est suffisant.

La vraie question est :

**où et comment le serveur impose-t-il les permissions ?**

# **E.11. Je travaille avec des données personnelles**

Pense :

minimisation ;

accès ;

stockage ;

suppression ;

chiffrement lorsque pertinent ;

logs ;

exposition frontend ;

sauvegardes ;

durée de conservation ;

obligations légales applicables.

# **F — INTERACTION AVEC L'IA**

C'est ici que ce document devient directement utile à ton mode de travail.

# **F.1. Le problème du prompt « fais-moi une application sécurisée »**

Il est trop vague.

Une IA peut répondre :

« J'ai ajouté JWT, bcrypt et CORS. »

Et pourtant ton application peut rester vulnérable.

Pourquoi ?

Parce que :

**sécurité ≠ présence de quelques technologies de sécurité.**

# **F.2. Le bon réflexe : donner un modèle de menace**

Au lieu de :

« Sécurise mon API. »

Demande :

« Analyse cette API en identifiant ses actifs, utilisateurs, privilèges, surface d'attaque, frontières de confiance, menaces principales et conséquences potentielles avant de proposer des protections. »

Tu forces l'IA à **raisonner avant de coder**.

# **F.3. Prompt de conception sécurisé**

Une bonne demande peut préciser :

Contexte :  
Application web SaaS.  
<br/>Utilisateurs :  
User / Admin.  
<br/>Données :  
Données personnelles + données métier.  
<br/>Architecture :  
React + API + PostgreSQL.  
<br/>Objectif :  
Construire l'authentification.  
<br/>Contraintes :  
\- secrets côté serveur ;  
\- HTTPS ;  
\- validation serveur ;  
\- contrôle d'autorisation serveur ;  
\- protection contre brute force ;  
\- gestion sécurisée des sessions ;  
\- logs sans secrets.  
<br/>Avant de coder :  
1\. identifier les menaces ;  
2\. identifier les erreurs classiques ;  
3\. proposer l'architecture ;  
4\. expliquer les compromis ;  
5\. seulement ensuite produire l'implémentation.

# **F.4. Demander à l'IA de chercher les scénarios négatifs**

Ne demande pas seulement :

« Fais fonctionner cette fonctionnalité. »

Demande :

« Maintenant, imagine comment cette fonctionnalité pourrait être mal utilisée ou attaquée et vérifie que l'implémentation résiste à ces scénarios. »

# **F.5. Demander une revue de sécurité séparée**

Une bonne pratique :

### **Étape 1**

IA construit.

### **Étape 2**

IA audite.

### **Étape 3**

Une autre analyse critique les résultats.

### **Étape 4**

Tu vérifies toi-même.

Cela évite de considérer le premier résultat de l'IA comme vérité.

# **F.6. Demander les hypothèses**

Toujours utile :

« Quelles hypothèses de sécurité fais-tu ? »

Exemple :

L'IA suppose peut-être :

que le frontend est fiable ;

que le token ne sera jamais volé ;

que l'utilisateur est honnête ;

que l'API externe est fiable.

Certaines hypothèses sont dangereuses.

# **F.7. Demander les limites**

Question extrêmement importante :

**« Qu'est-ce que cette protection ne protège PAS ? »**

Exemple :

HTTPS protège le transport.

Mais HTTPS ne protège pas :

une mauvaise autorisation ;

une SQL injection ;

une logique métier incorrecte ;

un secret exposé dans Git.

# **F.8. Ne jamais donner de vrais secrets à l'IA**

Évite de fournir à une IA :

clés API réelles ;

mots de passe ;

tokens actifs ;

credentials ;

secrets privés.

Utilise des placeholders :

YOUR_API_KEY  
YOUR_DATABASE_URL  
YOUR_SECRET

# **F.9. Demander des tests de sécurité**

Pour une fonctionnalité sensible :

« Génère également les tests qui doivent échouer si un utilisateur tente d'effectuer une action non autorisée. »

Exemple :

User A  
↓  
essaie d'accéder  
↓  
ressource de User B  
↓  
403 / refus

Le test négatif est essentiel.

# **F.10. Prompt d'audit générique**

Tu peux développer ton propre pattern :

Analyse cette fonctionnalité comme un reviewer sécurité.  
<br/>1\. Actifs à protéger  
2\. Menaces  
3\. Surface d'attaque  
4\. Vulnérabilités potentielles  
5\. Contrôles existants  
6\. Contrôles manquants  
7\. Mauvaises hypothèses  
8\. Scénarios d'abus  
9\. Tests négatifs  
10\. Risques critiques  
11\. Corrections prioritaires  
12\. Ce que cette analyse ne permet pas de garantir

# **G — CONTRÔLE ET AUDIT : COMMENT SAVOIR SI C'EST VRAIMENT SÉCURISÉ ?**

C'est ici que tu dois apprendre à **lire** une application.

# **G.1. Première règle**

Ne demande pas :

« Est-ce sécurisé ? »

Cette question est trop absolue.

Demande :

**« Quels risques avons-nous identifiés et quelles mesures les réduisent ? »**

# **G.2. Lire l'authentification**

Questions :

Où le mot de passe est-il vérifié ?

Où est-il stocké ?

Est-il haché correctement ?

Y a-t-il une limitation des tentatives ?

Comment fonctionne le reset password ?

Comment les sessions expirent-elles ?

Peut-on invalider une session ?

MFA disponible si nécessaire ?

Les cookies sensibles ont-ils les bons attributs ?

# **G.3. Lire l'autorisation**

C'est l'une des parties les plus importantes.

Pour chaque endpoint :

QUI appelle ?  
↓  
QUE demande-t-il ?  
↓  
A-T-IL LE DROIT ?  
↓  
SUR QUELLE RESSOURCE ?  
↓  
DANS QUEL CONTEXTE ?

# **G.4. Lire une API**

Pour chaque endpoint :

METHOD  
PATH  
AUTHENTICATION  
AUTHORIZATION  
INPUT  
VALIDATION  
BUSINESS LOGIC  
DATABASE  
OUTPUT  
ERROR  
LOGGING  
RATE LIMIT

Tu peux presque transformer cela en grille d'audit.

# **G.5. Lire les entrées utilisateur**

Cherche :

Formulaire  
URL  
Query parameter  
Path parameter  
Header  
Cookie  
JSON  
Upload  
Webhook

Chaque donnée externe doit être considérée comme :

**non fiable jusqu'à validation appropriée.**

# **G.6. Lire la base de données**

Questions :

les requêtes sont-elles paramétrées ?

les permissions sont-elles minimales ?

la base est-elle directement exposée à Internet ?

les credentials sont-ils protégés ?

les données sensibles sont-elles protégées ?

les sauvegardes sont-elles sécurisées ?

# **G.7. Lire les erreurs**

Mauvais :

Database connection failed:  
postgres://admin:password@server...

L'utilisateur ne doit pas recevoir :

stack trace inutile ;

credentials ;

détails internes ;

chemins système ;

informations permettant de cartographier l'infrastructure.

# **G.8. Lire les logs**

Demande :

« Si cette fonctionnalité est compromise, aurais-je une trace exploitable ? »

Et :

« Les logs contiennent-ils eux-mêmes des secrets ? »

# **G.9. Lire les dépendances**

Question :

« Quelles dépendances critiques mon application utilise-t-elle et comment leurs vulnérabilités sont-elles surveillées ? »

# **G.10. Lire la configuration de production**

Cherche notamment :

debug ;

CORS ;

cookies ;

HTTPS ;

headers ;

secrets ;

permissions ;

services exposés ;

ports ;

stockage ;

backups.

# **G.11. Lire les frontières de confiance**

C'est un concept très puissant.

Exemple :

Navigateur  
│  
│ NON FIABLE  
↓  
API  
│  
│  
↓  
Backend  
│  
↓  
Database

Le navigateur ne doit jamais être considéré comme une autorité de sécurité.

Même si tu contrôles ton frontend, l'utilisateur peut :

modifier les requêtes ;

appeler l'API directement ;

modifier le JavaScript ;

ignorer complètement ton interface.

# **G.12. Le frontend n'est jamais une frontière de sécurité**

C'est un principe à mémoriser.

Mauvais raisonnement :

« Le bouton Admin n'est pas affiché aux utilisateurs normaux, donc ils ne peuvent pas être admins. »

Faux.

La sécurité doit être imposée côté serveur.

# **H — MÉTHODOLOGIE DE CONCEPTION SÉCURISÉE**

Voici ton futur réflexe lorsque tu construiras un produit.

## **H.1. Étape 1 — Identifier les actifs**

Qu'est-ce qui possède de la valeur ?

## **H.2. Étape 2 — Identifier les utilisateurs**

Qui utilise le système ?

## **H.3. Étape 3 — Identifier les privilèges**

Qui peut faire quoi ?

## **H.4. Étape 4 — Cartographier les flux**

Client  
↓  
Frontend  
↓  
API  
↓  
Services  
↓  
Database

## **H.5. Étape 5 — Identifier les frontières de confiance**

À chaque frontière :

« Qui fait confiance à qui ? »

## **H.6. Étape 6 — Identifier les menaces**

Demander :

interception ?

vol d'identité ?

abus de privilèges ?

injection ?

fuite de données ?

modification ?

destruction ?

indisponibilité ?

abus de fonctionnalité ?

## **H.7. Étape 7 — Évaluer le risque**

Pour chaque menace :

Probabilité  
×  
Impact  
\=  
Priorité

## **H.8. Étape 8 — Choisir les contrôles**

Exemples :

Menace  
↓  
Protection  
↓  
Détection  
↓  
Réponse

## **H.9. Étape 9 — Tester**

Pas seulement :

« Est-ce que ça marche ? »

Mais :

« Est-ce que ça refuse correctement ce qui doit être refusé ? »

## **H.10. Étape 10 — Surveiller**

Après déploiement :

Logs  
Monitoring  
Alertes  
Backups  
Updates  
Audits

# **I — LES ERREURS QUE TU DOIS ABSOLUMENT SAVOIR RECONNAÎTRE**

## **Erreur 1**

« C'est caché dans le frontend donc c'est sécurisé. »

Faux.

## **Erreur 2**

« J'utilise HTTPS donc je suis sécurisé. »

Faux.

## **Erreur 3**

« J'utilise JWT donc mon authentification est sécurisée. »

Faux.

JWT est un mécanisme/format ; la sécurité dépend de son utilisation.

## **Erreur 4**

« J'ai bcrypt donc mon application est sécurisée. »

Faux.

Une application peut avoir un excellent stockage de mots de passe et une autorisation catastrophique.

## **Erreur 5**

« CORS protège mon API. »

Faux.

CORS est principalement une politique appliquée par les navigateurs. Ce n'est pas un mécanisme général d'autorisation d'API.

## **Erreur 6**

« J'ai un firewall donc mon application est protégée. »

Faux.

## **Erreur 7**

« L'utilisateur ne peut pas modifier le prix parce que le frontend l'affiche seulement. »

Faux.

Le serveur doit imposer la logique métier.

## **Erreur 8**

« J'ai testé avec mon compte admin donc tout fonctionne. »

Insuffisant.

Il faut tester :

utilisateur normal ;

utilisateur non authentifié ;

utilisateur avec mauvais rôle ;

utilisateur ciblant une ressource d'un autre utilisateur.

# **J — NIVEAU DE MATURITÉ : DE « JE SAIS QUE ÇA EXISTE » À « JE SAIS CONTRÔLER »**

Ton apprentissage doit suivre plusieurs niveaux.

## **Niveau 1 — Reconnaître**

Tu entends :

SQL injection

Tu sais :

c'est une famille de vulnérabilités liée à l'interprétation non sécurisée d'entrées dans des requêtes SQL.

## **Niveau 2 — Comprendre**

Tu peux expliquer :

pourquoi elle existe ;

ce qu'elle peut provoquer ;

comment elle est généralement évitée.

## **Niveau 3 — Identifier le besoin**

Tu construis une API et tu te demandes :

« Comment mes requêtes SQL sont-elles construites ? »

## **Niveau 4 — Choisir**

Tu sais qu'il faut privilégier :

requêtes paramétrées ;

ORM correctement utilisé ;

validation adaptée.

## **Niveau 5 — Diriger l'IA**

Tu peux demander :

« Implémente cette fonctionnalité avec des requêtes paramétrées et montre-moi où l'entrée utilisateur est séparée de la requête. »

## **Niveau 6 — Contrôler**

Tu peux regarder le code et demander :

« Est-ce réellement paramétré partout ? »

## **Niveau 7 — Approfondir**

Tu apprends :

mécanismes ;

variantes ;

limitations ;

techniques de détection ;

protections avancées.

## **Niveau 8 — Pratiquer**

Tu réalises des exercices dans des environnements contrôlés et autorisés.

## **Niveau 9 — Fiche STANE OS**

Une fois suffisamment maîtrisé :

Concept  
Définition  
Pourquoi  
Menaces  
Quand y penser  
Quand ne pas l'utiliser  
Fonctionnement  
Exemple  
Alternatives  
Avantages  
Limites  
Erreurs  
Prompt IA  
Audit  
Tests  
Ressources  
Niveau de maîtrise

# **K — TA CHECKLIST DE SÉCURITÉ MINIMALE POUR UN PRODUIT WEB**

Elle ne remplace évidemment pas un audit professionnel, mais elle constitue une excellente **barrière minimale**.

### **Identité**

authentification correctement conçue ;

mots de passe correctement protégés ;

récupération de compte sécurisée ;

MFA pour les comptes sensibles si pertinent ;

sessions correctement gérées.

### **Autorisation**

permissions vérifiées côté serveur ;

principe du moindre privilège ;

séparation des rôles ;

accès aux ressources vérifié individuellement.

### **Données**

HTTPS ;

secrets protégés ;

données sensibles correctement protégées ;

pas de secrets dans Git ;

backups.

### **API**

validation serveur ;

rate limiting lorsque pertinent ;

erreurs contrôlées ;

authentification ;

autorisation ;

CORS correctement configuré ;

endpoints sensibles identifiés.

### **Application**

protection contre les injections ;

XSS considéré ;

CSRF considéré si pertinent ;

uploads contrôlés ;

dépendances surveillées ;

logique métier protégée.

### **Production**

mode debug désactivé ;

secrets séparés du code ;

logs ;

monitoring approprié ;

sauvegardes testées ;

mises à jour de sécurité ;

permissions minimales.

# **L — LE MODÈLE MENTAL FINAL**

Lorsque tu découvriras n'importe quel nouveau concept de cybersécurité, ne cherche pas immédiatement à apprendre sa syntaxe.

Pose ces questions :

1\. QU'EST-CE QUE C'EST ?  
↓  
2\. QUEL PROBLÈME EST-IL CENSÉ RÉSOUDRE ?  
↓  
3\. QUELLE MENACE EST CONCERNÉE ?  
↓  
4\. QUEL ACTIF EST PROTÉGÉ ?  
↓  
5\. QUAND DOIS-JE Y PENSER ?  
↓  
6\. COMMENT ÇA FONCTIONNE ?  
↓  
7\. QUELLES SONT LES ALTERNATIVES ?  
↓  
8\. QUELS SONT LES COMPROMIS ?  
↓  
9\. COMMENT DEMANDER À L'IA DE L'UTILISER ?  
↓  
10\. COMMENT VÉRIFIER QUE L'IA L'A BIEN UTILISÉ ?

C'est exactement ce qui transforme la cybersécurité d'une collection de mots compliqués en **capacité de décision**.

# **M — CARTOGRAPHIE DE RÉFÉRENCE**

Voici maintenant la carte que tu dois progressivement avoir en tête :

CYBERSÉCURITÉ  
│  
┌───────────────────┼───────────────────┐  
↓ ↓ ↓  
MENACES ACTIFS RISQUES  
│ │ │  
↓ ↓ ↓  
Attaques Données Impact  
Erreurs Identités Probabilité  
Abus Systèmes Priorité  
│  
↓  
SURFACE D'ATTAQUE  
│  
↓  
VULNÉRABILITÉS  
│  
┌─────┼─────┬─────────┐  
↓ ↓ ↓ ↓  
Web API IAM Réseau  
│ │ │ │  
↓ ↓ ↓ ↓  
XSS IDOR Auth TLS  
SQLi CSRF MFA Firewall  
SSRF etc. RBAC VPN  
│  
└──────────┬─────────────┘  
↓  
PROTECTIONS  
│  
┌─────────┼─────────┐  
↓ ↓ ↓  
Prévention Détection Réponse  
│ │ │  
↓ ↓ ↓  
Validation Logs Incident  
Least Monitoring Recovery  
Privilege Alertes Backup  
│  
└─────────┬─────────┘  
↓  
AUDIT  
│  
┌───────┼────────┐  
↓ ↓ ↓  
Code Config Architecture  
│ │ │  
└───────┼────────┘  
↓  
AMÉLIORATION

# **N — CE QUE TU DOIS ÊTRE CAPABLE DE FAIRE APRÈS CETTE CARTOGRAPHIE**

Tu n'as pas besoin de savoir exploiter toutes les vulnérabilités.

Tu dois progressivement pouvoir regarder un produit et dire :

« Ici, il y a une authentification. »

« Ici, il y a une autorisation. »

« Cette donnée est sensible. »

« Ce endpoint est exposé. »

« Cette entrée vient directement de l'utilisateur. »

« Cette partie appartient à une frontière de confiance. »

« Ici, je dois penser au contrôle d'accès. »

« Ici, je dois penser à l'injection. »

« Ici, je dois penser aux secrets. »

« Ici, il faut du rate limiting. »

« Ici, un backup est nécessaire. »

« Cette protection ne résout pas le problème complet. »

« L'IA me propose une solution, mais je dois vérifier son hypothèse. »

Et surtout :

**« Je sais quelles questions poser avant de laisser l'IA construire. »**

C'est le niveau de cybersécurité que cette cartographie doit t'apporter.

# **O — LA CYBERSÉCURITÉ DANS TON MODE DE TRAVAIL AVEC L'IA**

Ton objectif final n'est donc pas :

**« Je connais la cybersécurité. »**

Mais :

**« Je sais intégrer une réflexion de sécurité dans chacune de mes décisions techniques. »**

Ton cycle de construction devient :

IDÉE  
↓  
BESOIN  
↓  
ARCHITECTURE  
↓  
ACTIFS  
↓  
MENACES  
↓  
RISQUES  
↓  
PROTECTIONS  
↓  
IMPLÉMENTATION  
↓  
TESTS  
↓  
AUDIT  
↓  
DÉPLOIEMENT  
↓  
MONITORING  
↓  
AMÉLIORATION

Et l'IA devient un **assistant de sécurité**, pas une autorité.

# **P — RÉSUMÉ OPÉRATIONNEL**

Si tu ne devais retenir que **15 réflexes** de ce document :

**Tout système possède des actifs à protéger.**

**Tout système possède une surface d'attaque.**

**Une menace n'est pas une vulnérabilité.**

**Une vulnérabilité n'est pas automatiquement un risque critique.**

**Authentification ≠ autorisation.**

**Frontend ≠ frontière de sécurité.**

**Encodage ≠ chiffrement ≠ hachage.**

**HTTPS ne sécurise pas toute l'application.**

**Les secrets ne doivent jamais être exposés dans le code.**

**Toute entrée utilisateur doit être considérée comme non fiable.**

**Le serveur doit imposer les règles importantes.**

**Le moindre privilège réduit l'impact d'une compromission.**

**La défense doit fonctionner en profondeur, pas avec une seule protection.**

**La sécurité doit être pensée avant le déploiement, pas après.**

**Une réponse générée par l'IA doit être auditée, surtout lorsqu'elle concerne la sécurité.**

# **Q — LA COMPÉTENCE CIBLE**

Le niveau recherché pour ton projet peut être résumé ainsi :

**Reconnaître → Comprendre → Identifier le risque → Savoir quand agir → Choisir une approche → Diriger l'IA → Contrôler l'implémentation → Tester → Approfondir si nécessaire.**

Tu n'as donc pas besoin de transformer chaque domaine en spécialisation.

Tu construis plutôt une **intelligence technique transversale**.

Pour la cybersécurité, cette intelligence doit te permettre de passer de :

« Je ne sais pas ce que c'est. »

à :

« Je sais pourquoi ça existe. »

puis :

« Je sais quand je dois y penser. »

puis :

« Je sais quelle solution est raisonnable. »

et enfin :

**« Je peux demander à l'IA de l'implémenter et vérifier qu'elle ne m'a pas donné une fausse impression de sécurité. »**

## **Fin du Document 03 — Cybersécurité**

**Document suivant : Document 04 — SEO & Web Performance.**

La logique changera alors de nouveau : **visibilité → découvrabilité → exploration → indexation → pertinence → performance → expérience → mesure → optimisation**, avec le même principe fondamental : comprendre suffisamment pour savoir **quoi demander à l'IA, pourquoi, quand et comment contrôler son travail**.