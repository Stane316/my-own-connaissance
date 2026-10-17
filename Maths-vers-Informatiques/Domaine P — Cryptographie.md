# DOMAINE P — CRYPTOGRAPHIE

## Une intersection extraordinaire entre mathématiques et informatique

**Question centrale :**

**Comment permettre à des personnes ou des machines de communiquer, stocker des données ou prouver leur identité dans un environnement où l’on suppose que l’adversaire peut observer, modifier, intercepter, rejouer ou fabriquer des informations ?**

La cryptographie transforme cette question en problèmes mathématiques et algorithmiques.

Elle cherche notamment à construire des mécanismes permettant de garantir :

- la **confidentialité** ;
- l’**intégrité** ;
- l’**authenticité** ;
- l’**authentification** ;
- la **non-répudiation** dans certains modèles ;
- la **preuve de possession d’un secret** ;
- l’**établissement de clés secrètes** ;
- la **résistance à certaines classes d’attaques** ;
- la **sécurité des communications** ;
- la **protection des données au repos et en transit** ;
- la **confiance distribuée**.

La cryptographie moderne est donc beaucoup plus vaste que :

« chiffrer un message ».

Elle constitue une véritable **couche mathématique de confiance pour les systèmes informatiques**.

# 0\. PRÉDISPOSITION D’INTÉGRATION

Ce document doit être utilisé comme une **base de raisonnement cryptographique** dans les projets logiciels, réseaux, systèmes distribués, IA, cybersécurité, blockchain et architectures sécurisées.

Lorsqu’un projet implique :

- des mots de passe ;
- des comptes utilisateurs ;
- des sessions ;
- des API ;
- des tokens ;
- des données sensibles ;
- des communications réseau ;
- des paiements ;
- des signatures ;
- des certificats ;
- des clés ;
- du stockage sécurisé ;
- une blockchain ;
- des systèmes distribués ;
- de l’authentification ;
- de l’identité numérique ;
- des secrets ;
- de la confidentialité ;
- de la vérification d’intégrité ;
- des échanges entre machines ;
- des agents autonomes ;

l’IA doit se demander :

1.  **Quel actif doit être protégé ?**
2.  **Contre quel adversaire ?**
3.  **Quelle propriété de sécurité est nécessaire ?**
4.  **Quelle primitive cryptographique correspond à cette propriété ?**
5.  **Comment les clés sont-elles générées ?**
6.  **Où sont-elles stockées ?**
7.  **Comment sont-elles distribuées ?**
8.  **Comment sont-elles renouvelées ?**
9.  **Que se passe-t-il lorsqu’une clé est compromise ?**
10. **Quel protocole assemble correctement les primitives ?**
11. **Quel modèle de menace est supposé ?**
12. **Quel niveau de sécurité est réellement nécessaire ?**
13. **L’implémentation est-elle résistante aux attaques pratiques ?**
14. **Existe-t-il une dépendance à une hypothèse mathématique précise ?**
15. **Le système reste-t-il sécurisé lorsque l’échelle augmente ?**
16. **Existe-t-il un risque quantique futur ?**

Le document ne doit jamais conduire à :

« J’ai utilisé du chiffrement, donc mon système est sécurisé. »

La cryptographie protège **certaines propriétés dans certaines hypothèses**.

La sécurité réelle dépend également :

- de l’implémentation ;
- des clés ;
- des protocoles ;
- de l’architecture ;
- du stockage ;
- de l’authentification ;
- de la gestion des erreurs ;
- des permissions ;
- du matériel ;
- des utilisateurs ;
- du modèle de menace.

# 1\. IDENTITÉ DU DOMAINE

## Nom

**Cryptographie**

## Domaine

Mathématiques appliquées + informatique + cybersécurité.

## Nature

La cryptographie étudie la conception et l’analyse de mécanismes permettant de sécuriser l’information et les communications face à des adversaires.

Elle s’appuie notamment sur :

### Mathématiques

- théorie des nombres ;
- arithmétique modulaire ;
- algèbre ;
- groupes ;
- anneaux ;
- corps finis ;
- théorie des probabilités ;
- combinatoire ;
- théorie de l’information ;
- géométrie algébrique dans certains domaines ;
- algèbre linéaire ;
- théorie de la complexité.

### Informatique

- algorithmes ;
- structures de données ;
- réseaux ;
- systèmes distribués ;
- programmation ;
- architecture logicielle ;
- cybersécurité ;
- systèmes embarqués ;
- bases de données ;
- blockchain.

# 2\. LA GRANDE QUESTION DE LA CRYPTOGRAPHIE

La cryptographie répond à une famille de problèmes fondamentaux.

Alice veut communiquer avec Bob.

Mais Eve peut :

- écouter ;
- copier ;
- modifier ;
- supprimer ;
- injecter ;
- rejouer ;
- fabriquer ;
- observer les métadonnées ;
- tenter de deviner des secrets.

Comment Alice et Bob peuvent-ils malgré cela construire une communication fiable ?

On obtient alors plusieurs problèmes différents.

### Confidentialité

Eve ne doit pas pouvoir comprendre le message.

### Intégrité

Eve ne doit pas pouvoir modifier le message sans que cela soit détecté.

### Authentification

Bob doit pouvoir déterminer qu’il communique réellement avec Alice.

### Non-répudiation

Dans certains systèmes, on veut pouvoir démontrer qu’une signature a été produite par une certaine clé.

### Établissement de secret

Alice et Bob doivent pouvoir obtenir un secret partagé même si le canal est public.

### Preuve

Une partie doit pouvoir démontrer qu’elle connaît quelque chose sans nécessairement révéler ce secret.

Cette dernière idée mène notamment à la cryptographie **zero-knowledge**.

# 3\. PLACE DANS LA PILE MATHÉMATIQUE

La cryptographie est une intersection particulièrement riche.

THÉORIE DES NOMBRES  
↓  
arithmétique modulaire  
↓  
groupes / corps finis  
↓  
problèmes difficiles  
↓  
PRIMITIVES CRYPTOGRAPHIQUES  
↓  
chiffrement / hash / signatures / MAC / KDF  
↓  
PROTOCOLES CRYPTOGRAPHIQUES  
↓  
TLS / PKI / authentification / échanges sécurisés  
↓  
SYSTÈMES  
↓  
web / cloud / paiements / blockchain / identité

Elle se connecte directement aux domaines précédents :

- **B — Théorie des nombres** ;
- **C — Algèbre linéaire** ;
- **G — Probabilités** ;
- **M — Théorie de l’information** ;
- **O — Théorie de la complexité**.

Et aux domaines informatiques :

- cybersécurité ;
- réseaux ;
- systèmes distribués ;
- bases de données ;
- IA ;
- blockchain ;
- architecture logicielle.

# 4\. CRYPTOGRAPHIE VS CRYPTANALYSE

Deux disciplines complémentaires.

## Cryptographie

Cherche à construire des mécanismes sécurisés.

## Cryptanalyse

Cherche à casser ou affaiblir ces mécanismes.

Exemples :

- retrouver une clé ;
- trouver une collision ;
- récupérer un message ;
- distinguer une sortie cryptographique d’un hasard idéal ;
- exploiter une mauvaise implémentation ;
- exploiter une faiblesse protocolaire.

La cryptologie englobe traditionnellement :

CRYPTOGRAPHIE  
+  
CRYPTANALYSE  
\=  
CRYPTOLOGIE

# 5\. MODÈLE DE MENACE

Avant de choisir un algorithme, il faut définir l’adversaire.

Questions :

- Que peut-il observer ?
- Peut-il modifier les messages ?
- Peut-il injecter des messages ?
- Peut-il choisir certains messages ?
- Peut-il interroger le système ?
- Peut-il obtenir des sorties répétées ?
- Peut-il contrôler une machine ?
- Peut-il mesurer le temps d’exécution ?
- Peut-il observer la consommation électrique ?
- Peut-il disposer d’un ordinateur quantique ?
- Peut-il voler une clé ?

# 6\. TYPES D’ATTAQUANTS

## Passive adversary

Observe uniquement.

Exemple :

écoute d’un trafic réseau.

## Active adversary

Peut modifier ou injecter.

Exemple :

attaque man-in-the-middle.

## Chosen-plaintext adversary

L’adversaire peut faire chiffrer certains messages de son choix.

## Chosen-ciphertext adversary

L’adversaire peut soumettre certains chiffrés au système de déchiffrement.

## Adaptive adversary

L’adversaire adapte ses requêtes selon les réponses précédentes.

Cette distinction est fondamentale dans les notions modernes de sécurité cryptographique.

# 7\. PRINCIPALES PROPRIÉTÉS DE SÉCURITÉ

## Confidentialité

Empêcher la divulgation.

## Intégrité

Détecter la modification.

## Authenticité

Vérifier l’origine ou l’identité.

## Disponibilité

La cryptographie seule ne garantit pas la disponibilité.

Un attaquant peut toujours :

- couper le réseau ;
- bloquer un serveur ;
- saturer une API.

## Non-répudiation

Propriété associée notamment aux signatures numériques dans certains modèles.

# 8\. CRYPTOGRAPHIE SYMÉTRIQUE

Même secret pour les opérations principales.

Alice  
|  
| clé K  
↓  
Encrypt(M, K)  
|  
↓  
C  
|  
↓  
Decrypt(C, K)  
|  
↓  
M  
Bob

On utilise une clé secrète partagée.

## Avantages

- rapide ;
- efficace ;
- adaptée aux gros volumes ;
- adaptée au stockage ;
- adaptée au chiffrement réseau.

## Problème

Comment Alice et Bob obtiennent-ils initialement la même clé sans qu’Eve l’intercepte ?

C’est le problème de **l’établissement de clés**.

# 9\. CRYPTOGRAPHIE ASYMÉTRIQUE

Deux clés :

- clé publique ;
- clé privée.

La clé publique peut être diffusée.

La clé privée doit rester secrète.

Applications :

- chiffrement asymétrique ;
- signatures ;
- échange de clés ;
- authentification ;
- PKI.

Principales familles :

- RSA ;
- Diffie-Hellman ;
- ECC ;
- EdDSA ;
- cryptographie post-quantique.

# 10\. SYMÉTRIQUE VS ASYMÉTRIQUE

| Propriété | Symétrique | Asymétrique |
| --- | --- | --- |
| Clés | secrètes partagées | publique + privée |
| Vitesse | très élevée | généralement plus coûteuse |
| Gros fichiers | excellente | peu adaptée directement |
| Signature | non | oui |
| Établissement de clés | problème initial | excellent outil |
| Exemple | AES | RSA / ECC |
| Usage typique | données | identité / échange / signature |

Architecture moderne :

ASYMÉTRIQUE  
↓  
établir / authentifier  
↓  
clé symétrique  
↓  
AES-GCM / ChaCha20-Poly1305  
↓  
données

# 11\. ARITHMÉTIQUE MODULAIRE

Fondation de nombreuses constructions.

On travaille avec :

\[ a b n \]

si :

\[ n (a-b) \]

Exemple :

\[ 17 \]

car :

\[ 17-5=12 \]

# 12\. GROUPE

Un groupe est un ensemble muni d’une opération satisfaisant notamment :

1.  fermeture ;
2.  associativité ;
3.  élément neutre ;
4.  inverse.

En cryptographie, les groupes permettent de construire des problèmes mathématiques faciles à calculer dans un sens mais difficiles à inverser.

# 13\. GROUPES CYCLIQUES

Un élément (g) peut générer un groupe.

On écrit :

\[ G=g \]

Les puissances :

\[ g<sup>0,g</sup>1,g^2, \]

peuvent parcourir le groupe.

Cette structure est fondamentale dans :

- Diffie-Hellman ;
- DSA ;
- ECC ;
- certains systèmes de preuve.

# 14\. CORPS FINIS

Un corps fini est un ensemble fini dans lequel on peut effectuer :

- addition ;
- soustraction ;
- multiplication ;
- division par tout élément non nul.

On note souvent :

\[ \_p \]

pour un corps de (p) éléments lorsque (p) est premier.

On utilise également :

\[ \_{2^n} \]

dans certaines constructions.

Les corps finis interviennent notamment dans :

- AES ;
- ECC ;
- cryptographie à clé publique ;
- codes ;
- protocoles.

# 15\. NOMBRES PREMIERS

Les nombres premiers sont essentiels notamment dans RSA.

Un nombre premier (p) possède seulement :

\[ 1 \]

et :

\[ p \]

comme diviseurs positifs.

La factorisation d’un grand entier en facteurs premiers joue un rôle central dans la sécurité de RSA.

# 16\. PGCD

Le plus grand commun diviseur :

\[ (a,b) \]

est fondamental pour :

- inverses modulaires ;
- RSA ;
- génération de clés ;
- algorithme d’Euclide étendu.

# 17\. ALGORITHME D’EUCLIDE

Pour calculer :

\[ (a,b) \]

on utilise :

\[ (a,b)=(b,ab) \]

jusqu’à obtenir un reste nul.

# 18\. EUCLIDE ÉTENDU

Il permet de trouver (x,y) tels que :

\[ ax+by=(a,b) \]

Si :

\[ (a,n)=1 \]

alors :

\[ axn \]

et (x) est l’inverse modulaire de (a).

Cette opération est fondamentale dans RSA et de nombreuses constructions.

# 19\. EXPONENTIATION MODULAIRE

Calculer efficacement :

\[ a^en \]

est fondamental.

L’exponentiation naïve serait trop coûteuse.

On utilise notamment l’exponentiation rapide par carré successif.

Complexité approximative :

\[ O(e) \]

multiplications modulaires.

# 20\. ALGORITHMES PROBABILISTES

La cryptographie utilise massivement le hasard.

Exemples :

- génération de clés ;
- génération de nonces ;
- génération de sels ;
- génération de nombres premiers candidats ;
- padding ;
- protocoles.

Il faut distinguer :

PRNG  
pseudo-random number generator

et :

CSPRNG  
cryptographically secure pseudo-random number generator

Un générateur aléatoire ordinaire n’est pas nécessairement adapté à la cryptographie.

# 21\. ENTROPIE ET HASARD

La sécurité dépend souvent de l’imprévisibilité.

Si une clé de 128 bits est réellement uniforme :

\[ 2^{128} \]

possibilités existent.

Mais si seulement une petite partie de ces possibilités est effectivement utilisée, la sécurité réelle chute.

La qualité du hasard est donc une propriété cryptographique.

# 22\. PRIMITIVES CRYPTOGRAPHIQUES

Une primitive est une brique cryptographique fondamentale.

Principales familles :

- chiffrement symétrique ;
- chiffrement asymétrique ;
- hash ;
- MAC ;
- signature ;
- KDF ;
- PRF ;
- KEM ;
- générateurs aléatoires.

Un protocole sécurisé est généralement une **composition de primitives**.

# 23\. FONCTION DE HASH CRYPTOGRAPHIQUE

Une fonction :

\[ H:{0,1}<sup>{\*}</sup>{n} \]

transforme une entrée de taille variable en sortie de taille fixe.

Exemple :

message  
↓  
SHA-256  
↓  
256 bits

Une fonction de hash cryptographique cherche notamment à fournir :

- résistance à la préimage ;
- seconde préimage ;
- collisions difficiles.

NIST décrit les fonctions de hash comme produisant une représentation condensée de taille fixe et leur utilisation dans les signatures, MAC, dérivation de clés et autres mécanismes.

# 24\. PRÉIMAGE

Étant donné :

\[ y=H(x) \]

il doit être difficile de retrouver (x).

# 25\. SECONDE PRÉIMAGE

Étant donné (x), il doit être difficile de trouver :

\[ x’x \]

tel que :

\[ H(x’)=H(x) \]

# 26\. COLLISION

Trouver deux messages :

\[ xy \]

tels que :

\[ H(x)=H(y) \]

Une collision est différente d’une préimage.

# 27\. PARADOXE DES ANNIVERSAIRES

Pour un hash de (n) bits, les collisions génériques deviennent pertinentes autour de :

\[ 2^{n/2} \]

essais.

C’est pourquoi la résistance aux collisions d’un hash de 256 bits est approximativement associée à une sécurité générique de l’ordre de :

\[ 2^{128} \]

contre les collisions.

# 28\. SHA-2 ET SHA-3

Familles importantes :

- SHA-224 ;
- SHA-256 ;
- SHA-384 ;
- SHA-512 ;
- SHA-3 ;
- SHAKE.

Il faut distinguer :

hash général

de :

hash utilisé correctement dans un protocole cryptographique.

# 29\. HASH ≠ CHIFFREMENT

Erreur fondamentale.

Un hash :

\[ MH(M) \]

n’est pas conçu pour être inversé.

Un chiffrement :

\[ MC \]

est conçu pour être déchiffrable avec une clé appropriée.

# 30\. STOCKAGE DES MOTS DE PASSE

Il ne faut généralement pas stocker :

password = "123456"

ni simplement :

SHA256(password)

On utilise des fonctions de dérivation adaptées aux mots de passe.

Conceptuellement :

\[ K=KDF(password,salt,cost) \]

Exemples de familles :

- Argon2 ;
- scrypt ;
- PBKDF2.

Le **sel** doit être unique et non secret.

Le coût doit rendre les attaques massives plus difficiles.

# 31\. SEL

Un sel est une valeur aléatoire ou unique ajoutée au secret avant dérivation.

Conceptuellement :

\[ H(passwordsalt) \]

Objectifs :

- empêcher l’utilisation directe de tables pré-calculées ;
- distinguer deux mots de passe identiques ;
- augmenter le coût des attaques à grande échelle.

# 32\. HMAC

HMAC combine une fonction de hash avec une clé secrète.

Conceptuellement :

\[ HMAC(K,M) \]

permet de fournir une forme d’authentification et d’intégrité du message.

Applications :

- API ;
- tokens ;
- protocoles ;
- dérivation ;
- authentification réseau.

# 33\. MAC

Un MAC — Message Authentication Code — produit un authentificateur à partir :

- d’un message ;
- d’une clé secrète.

K + M  
↓  
MAC  
↓  
tag

Le destinataire possédant la clé peut vérifier le tag.

# 34\. HASH VS MAC VS SIGNATURE

| Primitive | Clé ? | Confidentialité ? | Intégrité ? | Authentification ? |
| --- | --- | --- | --- | --- |
| Hash | non | non | indirectement | non |
| MAC | oui | non | oui | oui, entre détenteurs de clé |
| Signature | clé privée/publique | non | oui | oui |

# 35\. CHIFFREMENT SYMÉTRIQUE

Deux grandes familles :

- chiffrements par blocs ;
- chiffrements par flot.

Exemples :

- AES ;
- ChaCha20.

# 36\. AES

AES signifie **Advanced Encryption Standard**.

AES est un chiffrement symétrique par blocs.

Il utilise :

- blocs de 128 bits ;
- clés de 128 bits ;
- clés de 192 bits ;
- clés de 256 bits.

Les trois variantes sont :

- AES-128 ;
- AES-192 ;
- AES-256.

Ces paramètres sont spécifiés dans FIPS 197.

# 37\. STRUCTURE D’AES

AES repose notamment sur :

- substitution ;
- permutation ;
- transformations linéaires ;
- addition de clé.

Pour AES-128 :

- 10 tours.

Pour AES-192 :

- 12 tours.

Pour AES-256 :

- 14 tours.

# 38\. CORPS FINI DANS AES

AES utilise une structure basée sur :

\[ GF(2^8) \]

Les octets sont traités comme des éléments d’un corps fini.

C’est un excellent exemple de connexion directe entre :

algèbre abstraite  
↓  
corps finis  
↓  
algorithme cryptographique  
↓  
implémentation logicielle

# 39\. MODES DE FONCTIONNEMENT

Un chiffrement par blocs n’est pas nécessairement utilisé directement.

Modes historiques :

- ECB ;
- CBC ;
- CTR ;
- CFB ;
- OFB.

Modes modernes importants :

- GCM ;
- CCM ;
- XTS selon le contexte.

# 40\. ECB

ECB chiffre chaque bloc indépendamment.

C’est dangereux pour certaines données structurées car les motifs peuvent rester visibles.

Le problème fondamental :

\[ M_1=M_2 C_1=C_2 \]

dans le même contexte de clé.

# 41\. CBC

CBC introduit une dépendance entre blocs.

Il nécessite notamment un IV.

Une mauvaise gestion de l’IV peut compromettre la sécurité.

# 42\. CTR

CTR transforme un chiffrement par blocs en mécanisme proche d’un chiffrement par flot.

Il est crucial de ne jamais réutiliser dangereusement un nonce/compteur avec la même clé.

# 43\. AEAD

Une notion centrale de la cryptographie moderne :

**Authenticated Encryption with Associated Data**

AEAD permet simultanément :

- confidentialité ;
- intégrité ;
- authentification du ciphertext ;
- protection de données associées non chiffrées.

Exemples :

- AES-GCM ;
- ChaCha20-Poly1305.

Architecture :

clé  
+  
nonce  
+  
plaintext  
+  
associated data  
↓  
AEAD  
↓  
ciphertext + tag

# 44\. NONCE

Nonce :

Number used once.

Ce n’est pas nécessairement secret.

Mais certaines constructions imposent des contraintes très fortes sur sa réutilisation.

Exemple critique :

même clé  
+  
même nonce  
+  
AES-GCM

peut conduire à une compromission grave.

# 45\. CRYPTOGRAPHIE ASYMÉTRIQUE : RSA

RSA repose sur l’arithmétique modulaire et la difficulté pratique de certains problèmes liés à la factorisation.

Génération simplifiée :

Choisir deux grands nombres premiers :

\[ p,q \]

Puis :

\[ n=pq \]

et choisir un exposant public (e) compatible avec la structure mathématique.

L’exposant privé (d) satisfait une relation d’inversion modulaire.

# 46\. RSA : CLÉ PUBLIQUE ET PRIVÉE

Clé publique :

\[ (n,e) \]

Clé privée :

\[ (n,d) \]

L’opération mathématique fondamentale repose sur l’exponentiation modulaire.

# 47\. RSA N’EST PAS « JUSTE (m^en) »

Une erreur fréquente consiste à implémenter RSA brut.

Les constructions modernes utilisent des schémas d’encodage/padding adaptés.

Pour RSA, on rencontre notamment :

- RSAES-OAEP pour le chiffrement ;
- RSASSA-PSS pour les signatures.

PKCS #1 v2.2 documente ces constructions ainsi que les représentations de clés et mécanismes associés.

# 48\. RSA ET CRT

Le théorème des restes chinois peut accélérer les opérations privées RSA.

On peut travailler séparément modulo :

\[ p \]

et :

\[ q \]

puis recombiner.

C’est une illustration de :

même résultat mathématique, architecture de calcul différente.

# 49\. DIFFIE-HELLMAN

Diffie-Hellman résout un problème fondamental :

établir un secret partagé sur un canal public.

Alice choisit :

\[ a \]

Bob choisit :

\[ b \]

Ils échangent certaines valeurs publiques.

Alice calcule un secret à partir de (a).

Bob calcule le même secret à partir de (b).

Le mécanisme repose sur la difficulté d’inverser certaines opérations dans un groupe.

NIST documente notamment les mécanismes d’établissement de clés basés sur le logarithme discret dans des corps finis et sur les courbes elliptiques.

# 50\. PROBLÈME DU MAN-IN-THE-MIDDLE

Diffie-Hellman seul ne prouve pas nécessairement l’identité des participants.

Un attaquant peut s’interposer :

Alice ←→ Eve ←→ Bob

Il peut établir :

Alice ↔ Eve

et :

Eve ↔ Bob

C’est pourquoi l’échange de clés doit être combiné avec une authentification.

# 51\. DIFFIE-HELLMAN ÉPHÉMÈRE

On utilise souvent des clés éphémères.

Concept :

nouvelle clé temporaire  
↓  
échange  
↓  
secret partagé  
↓  
clé de session  
↓  
destruction des secrets temporaires

Cela peut contribuer à la **forward secrecy**.

# 52\. FORWARD SECRECY

Objectif :

la compromission future d’une clé à long terme ne doit pas permettre de déchiffrer automatiquement toutes les anciennes sessions enregistrées.

C’est une propriété architecturale très importante des protocoles modernes.

# 53\. COURBES ELLIPTIQUES

Une courbe elliptique peut être représentée sous une forme telle que :

\[ y<sup>2=x</sup>3+ax+b \]

sur un corps approprié.

En cryptographie, on travaille avec les points de la courbe et une opération de groupe.

# 54\. ECC

**Elliptic Curve Cryptography**

L’idée centrale :

remplacer certains problèmes algébriques classiques par des problèmes liés aux groupes de points sur courbes elliptiques.

Applications :

- ECDH ;
- ECDSA ;
- EdDSA ;
- signatures ;
- établissement de clés.

# 55\. ADDITION DE POINTS

Les points d’une courbe elliptique peuvent être munis d’une opération d’addition.

On obtient conceptuellement :

\[ P+Q \]

et :

\[ kP \]

pour un entier (k).

Le calcul de :

\[ kP \]

peut être efficace.

L’inversion générale du problème :

\[ Q=kP \]

est supposée difficile dans les paramètres appropriés.

# 56\. ECDH

Elliptic Curve Diffie-Hellman.

Alice possède une clé privée :

\[ a \]

et une clé publique :

\[ A=aG \]

Bob possède :

\[ b \]

et :

\[ B=bG \]

Alice calcule :

\[ aB=abG \]

Bob calcule :

\[ bA=abG \]

Ils obtiennent donc le même point partagé.

# 57\. ECDSA

**Elliptic Curve Digital Signature Algorithm**

Permet de créer des signatures numériques basées sur ECC.

Conceptuellement :

message  
↓  
hash  
↓  
signature avec clé privée  
↓  
signature

Puis :

message + signature + clé publique  
↓  
vérification

# 58\. EdDSA

EdDSA est une famille moderne de signatures basée sur des courbes d’Edwards.

Exemple très connu :

- Ed25519.

NIST FIPS 186-5 spécifie notamment RSA, ECDSA et EdDSA comme techniques de génération et de vérification de signatures.

# 59\. RSA VS ECC

Pour une architecture moderne, le choix ne consiste pas simplement à demander :

« lequel est le plus sécurisé ? »

Il faut considérer :

- niveau de sécurité ;
- taille des clés ;
- taille des signatures ;
- performance ;
- bibliothèque ;
- protocole ;
- compatibilité ;
- matériel ;
- modèle de menace ;
- migration future.

# 60\. SIGNATURE NUMÉRIQUE

Une signature permet notamment de vérifier :

1.  que le message n’a pas été modifié ;
2.  qu’il correspond à une clé privée donnée.

Schéma :

Message  
↓  
Hash  
↓  
Signature avec clé privée  
↓  
Signature

Vérification :

Message  
+  
Signature  
+  
Clé publique  
↓  
Verification  
↓  
VALID / INVALID

# 61\. SIGNATURE ≠ CHIFFREMENT

Une signature n’est pas principalement destinée à cacher le contenu.

Elle sert principalement à :

- authentifier ;
- vérifier l’intégrité ;
- établir une preuve cryptographique liée à une clé.

Le chiffrement sert principalement à :

- protéger la confidentialité.

# 62\. AUTHENTIFICATION

L’authentification répond à :

« Qui es-tu ? »

La cryptographie permet plusieurs mécanismes :

- mot de passe ;
- secret partagé ;
- certificat ;
- signature ;
- preuve de possession ;
- challenge-response ;
- clés matérielles.

# 63\. AUTHENTIFICATION VS AUTORISATION

Très important.

### Authentification

Qui es-tu ?

### Autorisation

Qu’as-tu le droit de faire ?

Un système peut authentifier correctement un utilisateur et avoir malgré tout une mauvaise autorisation.

# 64\. CHALLENGE-RESPONSE

Principe :

Serveur → challenge aléatoire  
Client → réponse cryptographique  
Serveur → vérification

Le secret n’a pas besoin d’être directement transmis.

# 65\. TOKENS

La cryptographie intervient dans les systèmes de tokens.

Exemples conceptuels :

payload  
+  
signature  
\=  
token vérifiable

Attention :

encoder n’est pas chiffrer.

Un token Base64 n’est pas automatiquement secret.

# 66\. JWT

JWT peut être utilisé pour transporter des claims structurés.

On distingue :

- JWS : signature ;
- JWE : chiffrement.

Un JWT signé n’est donc pas nécessairement confidentiel.

# 67\. PKI

**Public Key Infrastructure**

Infrastructure permettant notamment de gérer :

- certificats ;
- autorités de certification ;
- clés publiques ;
- chaînes de confiance ;
- révocation ;
- renouvellement.

# 68\. CERTIFICAT

Un certificat associe notamment une identité à une clé publique selon un cadre de confiance.

Conceptuellement :

Identité  
+  
Clé publique  
+  
métadonnées  
+  
signature de CA  
↓  
Certificat

# 69\. AUTORITÉ DE CERTIFICATION

Une CA — Certificate Authority — signe des certificats.

Elle constitue une racine de confiance dans certaines architectures.

Le navigateur ou système possède des ancres de confiance.

# 70\. X.509

X.509 définit un format largement utilisé pour les certificats.

Applications :

- HTTPS ;
- TLS ;
- VPN ;
- authentification machine ;
- infrastructure d’entreprise.

# 71\. TLS

TLS permet de sécuriser les communications réseau.

TLS cherche notamment à empêcher :

- écoute ;
- modification ;
- falsification.

TLS 1.3 est spécifié par l’IETF dans RFC 8446, avec une architecture de handshake et de protection des données conçue pour ces objectifs.

# 72\. ARCHITECTURE CRYPTOGRAPHIQUE DE TLS

Schéma conceptuel :

Client  
↓  
Handshake  
↓  
Authentification  
↓  
Établissement de clés  
↓  
Clés de session  
↓  
AEAD  
↓  
Données sécurisées

Cela montre une idée fondamentale :

un protocole moderne ne repose presque jamais sur une seule primitive.

# 73\. KDF

**Key Derivation Function**

Une KDF transforme un secret en une ou plusieurs clés adaptées à des usages différents.

Conceptuellement :

\[ K_1,K_2,,K_n=KDF(secret,context) \]

Applications :

- clés de session ;
- séparation des usages ;
- dérivation de clés ;
- protocoles réseau ;
- stockage sécurisé.

# 74\. KEY SEPARATION

Une bonne architecture évite de réutiliser exactement la même clé pour plusieurs usages.

Exemple :

master secret  
↓  
KDF  
↙ ↓ ↘  
Kenc Kmac Kauth

Ainsi :

- une clé chiffre ;
- une autre authentifie ;
- une autre sert à un autre sous-système.

# 75\. GESTION DES CLÉS

La sécurité d’un système cryptographique dépend énormément de la gestion des clés.

Cycle :

Génération  
↓  
Distribution  
↓  
Stockage  
↓  
Utilisation  
↓  
Rotation  
↓  
Révocation  
↓  
Destruction

NIST traite explicitement la génération, protection, utilisation, renouvellement et gestion du matériel cryptographique comme une discipline à part entière.

# 76\. KEY ROTATION

Une clé ne devrait pas nécessairement rester valide indéfiniment.

Rotation :

ancienne clé  
↓  
nouvelle clé  
↓  
migration  
↓  
ancienne clé retirée

# 77\. KEY COMPROMISE

Question fondamentale :

Que se passe-t-il si une clé privée fuit ?

Un système robuste doit prévoir :

- détection ;
- révocation ;
- rotation ;
- invalidation ;
- récupération ;
- limitation des dégâts.

# 78\. HSM

**Hardware Security Module**

Matériel spécialisé permettant notamment de protéger des clés et d’effectuer certaines opérations cryptographiques dans un environnement contrôlé.

Applications :

- banques ;
- PKI ;
- paiements ;
- cloud ;
- infrastructures critiques.

# 79\. SECRET MANAGEMENT

Les clés et secrets ne doivent pas être placés naïvement dans :

source code

ou :

Git repository

ou :

frontend JavaScript

Exemples de solutions architecturales :

- secret manager ;
- HSM ;
- KMS ;
- variables d’environnement selon le contexte ;
- coffre-fort de secrets.

# 80\. CRYPTOGRAPHIE ET BASE DE DONNÉES

Il faut distinguer :

### Chiffrement au repos

Données stockées chiffrées.

### Chiffrement en transit

Données chiffrées pendant le transport.

### Chiffrement applicatif

L’application chiffre elle-même certaines données avant stockage.

# 81\. ENCRYPTION AT REST

Exemple :

Application  
↓  
AEAD  
↓  
ciphertext  
↓  
Database

La base ne contient pas nécessairement le plaintext.

# 82\. ENCRYPTION IN TRANSIT

Exemple :

Client  
↓  
TLS  
↓  
Internet  
↓  
TLS  
↓  
Serveur

# 83\. END-TO-END ENCRYPTION

Dans une architecture E2EE :

Alice  
↓  
chiffrement  
↓  
serveurs intermédiaires  
↓  
ciphertext  
↓  
Bob  
↓  
déchiffrement

Les intermédiaires ne disposent pas nécessairement des clés permettant de lire le contenu.

# 84\. ATTAQUES CRYPTOGRAPHIQUES

Il faut reconnaître plusieurs familles.

### Brute force

Tester les clés possibles.

### Dictionary attack

Tester des secrets issus d’une liste.

### Replay attack

Réutiliser un message valide.

### Man-in-the-middle

Intercepter et manipuler la communication.

### Chosen plaintext

Choisir des messages à faire chiffrer.

### Chosen ciphertext

Soumettre des chiffrés choisis.

### Side-channel

Exploiter des informations indirectes.

### Fault injection

Provoquer des erreurs pour révéler des informations.

# 85\. SIDE-CHANNELS

Une implémentation peut fuir de l’information sans que l’algorithme mathématique soit cassé.

Sources :

- temps ;
- consommation électrique ;
- cache CPU ;
- branches ;
- mémoire ;
- émissions électromagnétiques.

Exemple :

if secret_bit == 1:  
opération coûteuse

Une différence de temps peut devenir une fuite.

# 86\. CONSTANT-TIME

Pour certaines opérations sensibles, on cherche à éviter que le temps d’exécution dépende de secrets.

Concept :

secret  
↓  
opération à temps indépendant du secret  
↓  
résultat

Il s’agit d’un problème d’implémentation, pas uniquement de mathématiques.

# 87\. RANDOMNESS FAILURE

Une excellente primitive avec un mauvais générateur aléatoire peut devenir vulnérable.

Cela est particulièrement critique pour :

- clés privées ;
- nonces ;
- signatures ;
- protocoles.

# 88\. NONCE REUSE

Erreur extrêmement dangereuse dans certaines constructions.

Exemple conceptuel :

clé K  
nonce N  
message A

puis :

clé K  
nonce N  
message B

Selon l’algorithme, cela peut révéler des informations critiques.

# 89\. BLOCKCHAIN

La blockchain utilise plusieurs briques cryptographiques :

- hash ;
- signatures ;
- clés publiques ;
- arbres de Merkle ;
- fonctions de dérivation ;
- parfois preuves cryptographiques avancées.

# 90\. HASH CHAIN

Un bloc peut référencer le hash du bloc précédent :

Bloc 1  
↓ hash  
Bloc 2  
↓ hash  
Bloc 3  
↓ hash  
Bloc 4

Une modification du bloc 1 change son hash et invalide les références suivantes.

# 91\. MERKLE TREE

Arbre où les nœuds parents sont construits à partir des hash des enfants.

Root  
/ \\  
H12 H34  
/ \\ / \\  
H1 H2 H3 H4

Applications :

- blockchain ;
- systèmes distribués ;
- vérification efficace de données ;
- structures authentifiées.

# 92\. SIGNATURES ET BLOCKCHAIN

Une transaction peut être :

transaction  
↓  
hash / encodage  
↓  
signature avec clé privée  
↓  
réseau  
↓  
vérification avec clé publique

La blockchain n’est donc pas « du chiffrement ».

Elle repose principalement sur :

- intégrité ;
- signatures ;
- consensus ;
- structures distribuées.

# 93\. BLOCKCHAIN ≠ BASE DE DONNÉES CHIFFRÉE

Une blockchain vise principalement à fournir une forme de registre distribué avec des mécanismes cryptographiques et de consensus.

Le contenu peut même être publiquement lisible.

La cryptographie ne signifie donc pas nécessairement confidentialité.

# 94\. ZERO-KNOWLEDGE PROOFS

Une preuve zero-knowledge permet conceptuellement de convaincre un vérificateur :

« Je connais un secret satisfaisant une propriété »

sans révéler nécessairement le secret.

On distingue notamment :

- prover ;
- verifier ;
- statement ;
- witness.

Applications :

- identité ;
- blockchain ;
- confidentialité ;
- systèmes de preuve.

# 95\. PROPRIÉTÉS D’UNE PREUVE ZERO-KNOWLEDGE

Trois notions classiques :

### Completeness

Un prover honnête peut convaincre.

### Soundness

Un prover malhonnête ne peut pas facilement convaincre pour une affirmation fausse.

### Zero-knowledge

Le vérificateur n’apprend pas le secret lui-même, au-delà de ce qui est nécessaire pour établir l’affirmation.

# 96\. MULTI-PARTY COMPUTATION

MPC :

plusieurs parties calculent conjointement une fonction sans révéler nécessairement leurs entrées privées.

Conceptuellement :

Secret A ─┐  
├→ MPC → résultat  
Secret B ─┘

Applications :

- finance ;
- identité ;
- données sensibles ;
- infrastructures distribuées.

# 97\. HOMOMORPHIC ENCRYPTION

Une idée plus avancée :

effectuer certaines opérations directement sur des données chiffrées.

Conceptuellement :

\[ Enc(x)Enc(y) \]

peut correspondre à une opération sur :

\[ x+y \]

selon le schéma.

On distingue :

- partially homomorphic ;
- somewhat homomorphic ;
- fully homomorphic encryption.

# 98\. CRYPTOGRAPHIE POST-QUANTIQUE

Les systèmes classiques à clé publique basés notamment sur :

- factorisation ;
- logarithme discret ;

sont menacés par des ordinateurs quantiques suffisamment puissants.

L’algorithme de Shor est central dans cette problématique.

# 99\. POURQUOI LE QUANTIQUE CHANGE LE PROBLÈME

Conceptuellement :

RSA  
↓  
factorisation  
↓  
Shor  
↓  
menace quantique

et :

ECC / DH  
↓  
logarithme discret  
↓  
Shor  
↓  
menace quantique

# 100\. POST-QUANTUM ≠ QUANTUM CRYPTOGRAPHY

Deux concepts différents.

### Cryptographie post-quantique

Algorithmes classiques exécutés sur des ordinateurs classiques mais conçus pour résister à des adversaires quantiques.

### Cryptographie quantique

Utilise des phénomènes quantiques dans le protocole lui-même.

Ne pas confondre.

# 101\. ML-KEM

NIST a standardisé **ML-KEM** dans FIPS 203 comme mécanisme de key encapsulation basé sur les réseaux euclidiens/module lattices.

Il sert notamment à établir un secret partagé destiné ensuite à être utilisé par des algorithmes symétriques.

Paramètres :

- ML-KEM-512 ;
- ML-KEM-768 ;
- ML-KEM-1024.

# 102\. ML-DSA

NIST a également standardisé **ML-DSA** dans FIPS 204 comme mécanisme de signature numérique post-quantique basé sur les réseaux.

# 103\. SLH-DSA

SLH-DSA est une famille de signatures post-quantiques basée sur les hash, standardisée par NIST dans FIPS 205.

# 104\. MIGRATION POST-QUANTIQUE

Une architecture moderne doit réfléchir à :

algorithme actuel  
↓  
inventaire cryptographique  
↓  
identification des dépendances  
↓  
algorithmes remplaçables  
↓  
hybridation éventuelle  
↓  
migration  
↓  
validation

La cryptographie post-quantique devient donc également un problème d’architecture et de gestion du cycle de vie.

# 105\. CRYPTOAGILITY

Une propriété architecturale importante :

pouvoir remplacer un algorithme cryptographique sans reconstruire tout le système.

Mauvaise architecture :

AES partout  
RSA partout  
algorithmes codés en dur

Meilleure architecture :

CryptoProvider  
↓  
algorithme configurable  
↓  
implémentation

# 106\. ALGORITHMIC AGILITY

Une architecture peut permettre de passer :

RSA → ECC → PQC

ou :

AES-GCM → autre AEAD

sans modifier toute la logique métier.

# 107\. SÉCURITÉ PAR COMPOSITION

Une erreur fréquente :

prendre plusieurs primitives sécurisées et les assembler arbitrairement.

Deux primitives sûres ne garantissent pas automatiquement un protocole sûr.

Exemple conceptuel :

hash sécurisé  
+  
chiffrement sécurisé  
+  
signature sécurisée

peut néanmoins produire :

protocole vulnérable

si l’ordre ou le contexte sont incorrects.

# 108\. CRYPTOGRAPHIC PROTOCOL

Un protocole décrit :

- qui parle ;
- à qui ;
- quand ;
- quelles données sont envoyées ;
- quelles clés sont utilisées ;
- comment elles sont obtenues ;
- comment les erreurs sont gérées ;
- comment les messages sont authentifiés ;
- comment les sessions sont terminées.

# 109\. STATE MACHINE D’UN PROTOCOLE

Un protocole sécurisé peut être modélisé comme une machine à états.

INIT  
↓  
AUTHENTICATION  
↓  
KEY_ESTABLISHMENT  
↓  
SESSION  
↓  
REKEY  
↓  
CLOSE

Chaque transition doit être analysée.

# 110\. REPLAY PROTECTION

Un protocole doit parfois empêcher :

message valide  
↓  
intercepté  
↓  
réutilisé plus tard

Mécanismes possibles :

- nonce ;
- compteur ;
- timestamp ;
- numéro de séquence ;
- état de session.

# 111\. DOMAIN SEPARATION

Une clé ou une fonction cryptographique peut être utilisée dans différents contextes.

Il faut éviter qu’un résultat valide dans un contexte soit réutilisable dans un autre.

On introduit des contextes explicites :

KDF(secret, "authentication")  
KDF(secret, "encryption")  
KDF(secret, "export")

# 112\. CRYPTOGRAPHIC DOMAIN SEPARATION

Idée générale :

\[ H(contextdata) \]

plutôt que :

\[ H(data) \]

dans les constructions où la séparation de contexte est nécessaire.

# 113\. CRYPTOGRAPHIE ET API

Une API sécurisée peut combiner :

TLS  
+  
authentification  
+  
tokens  
+  
hash / MAC  
+  
gestion de secrets  
+  
autorisation  
+  
rate limiting

La cryptographie n’est qu’une partie du système.

# 114\. CRYPTOGRAPHIE ET WEB

Un système web moderne peut utiliser :

HTTPS  
↓  
TLS  
↓  
certificat  
↓  
échange de clés  
↓  
clé de session  
↓  
AEAD

Puis au niveau applicatif :

password  
↓  
password KDF  
↓  
base de données

et :

session  
↓  
token  
↓  
authentification  
↓  
autorisation

# 115\. CRYPTOGRAPHIE ET IA

Applications :

- confidentialité des données d’entraînement ;
- fédération ;
- secure aggregation ;
- confidentialité des prompts ;
- agents sécurisés ;
- identité d’agents ;
- signatures de sorties ;
- provenance ;
- protection des secrets API ;
- RAG privé ;
- calcul confidentiel.

# 116\. AGENTS IA ET IDENTITÉ CRYPTOGRAPHIQUE

Un agent peut posséder :

Agent ID  
↓  
clé publique  
+  
clé privée

Il peut alors signer :

- actions ;
- messages ;
- décisions ;
- appels ;
- artefacts.

Architecture :

Agent  
↓  
action  
↓  
signature  
↓  
orchestrateur  
↓  
vérification  
↓  
exécution

Cela ouvre des architectures d’agents **auditables et authentifiables**.

# 117\. PROVENANCE DES SORTIES IA

On peut imaginer :

modèle  
↓  
réponse  
↓  
hash  
↓  
signature  
↓  
artefact signé

Le système peut alors vérifier que l’artefact n’a pas été modifié.

# 118\. CRYPTOGRAPHIE ET DATA PROVENANCE

Une donnée peut être associée à :

- hash ;
- timestamp ;
- signature ;
- identité ;
- chaîne de provenance.

Applications :

- documents ;
- modèles ;
- datasets ;
- logiciels ;
- images ;
- contenus générés par IA.

# 119\. SIGNED ARTIFACTS

Un logiciel peut être distribué avec une signature.

binary  
↓  
hash  
↓  
signature développeur  
↓  
distribution  
↓  
verification

Applications :

- logiciels ;
- packages ;
- firmware ;
- mises à jour ;
- modèles IA.

# 120\. SUPPLY CHAIN SECURITY

La cryptographie peut aider à vérifier :

- origine ;
- intégrité ;
- provenance ;
- authenticité.

Mais :

signature valide ≠ logiciel intrinsèquement sûr.

Elle prouve seulement certaines propriétés sur l’artefact signé.

# 121\. CRYPTOGRAPHIE ET MOBILE

Applications :

- stockage sécurisé ;
- clés matérielles ;
- authentification biométrique indirecte ;
- chiffrement de fichiers ;
- sessions ;
- paiements.

# 122\. CRYPTOGRAPHIE ET IoT

Contraintes :

- faible puissance ;
- faible mémoire ;
- réseau instable ;
- matériel limité ;
- longue durée de vie.

Il faut donc considérer :

- taille des clés ;
- coût CPU ;
- consommation ;
- stockage ;
- rotation ;
- provisioning.

# 123\. CRYPTOGRAPHIE EMBARQUÉE

Un microcontrôleur peut nécessiter :

RNG  
+  
AES  
+  
hash  
+  
secure boot  
+  
clé matérielle

La sécurité devient alors fortement dépendante du matériel.

# 124\. SECURE BOOT

Concept :

Firmware  
↓  
hash  
↓  
signature  
↓  
Bootloader vérifie  
↓  
exécution

Si la signature est invalide :

STOP

# 125\. REMOTE ATTESTATION

Une machine peut tenter de prouver cryptographiquement :

« voici l’état logiciel que j’exécute ».

Applications :

- cloud ;
- enclaves ;
- IoT ;
- systèmes critiques ;
- confidential computing.

# 126\. CHIFFREMENT HOMOMORPHE ET IA

Une application avancée :

données sensibles  
↓  
chiffrement  
↓  
modèle  
↓  
calcul sur données chiffrées  
↓  
résultat chiffré

Potentiel :

- santé ;
- finance ;
- données personnelles ;
- IA privée.

Limite majeure :

coût computationnel souvent beaucoup plus élevé que le calcul classique.

# 127\. SECURE MULTI-PARTY COMPUTATION ET IA

Plusieurs organisations pourraient vouloir entraîner ou calculer sur des données communes sans partager directement les données brutes.

Concept :

Entreprise A  
\\  
\\  
MPC / secure aggregation  
/  
/  
Entreprise B

# 128\. FEDERATED LEARNING ET CRYPTOGRAPHIE

La cryptographie peut être utilisée pour :

- masquer les contributions ;
- sécuriser les agrégations ;
- protéger certaines mises à jour ;
- authentifier les participants.

Mais :

apprentissage fédéré ≠ automatiquement privé.

# 129\. CRYPTOGRAPHIE ET BLOCKCHAIN : STACK

BLOCKCHAIN  
│  
┌─────────┼─────────┐  
│ │ │  
HASH SIGNATURE MERKLE  
│ │ │  
└─────────┼─────────┘  
│  
CONSENSUS  
│  
DISTRIBUTION

La cryptographie est donc une composante, pas l’ensemble de la blockchain.

# 130\. THÉORIE DE L’INFORMATION ET CRYPTOGRAPHIE

Connexion directe avec le domaine M.

La théorie de l’information apporte :

- entropie ;
- incertitude ;
- quantité d’information ;
- capacité de canal.

La cryptographie s’intéresse notamment à :

- imprévisibilité ;
- secrets ;
- distributions ;
- fuite d’information ;
- sécurité informationnelle.

# 131\. ONE-TIME PAD

Le one-time pad possède une propriété théorique extraordinaire.

Si la clé est :

- parfaitement aléatoire ;
- aussi longue que le message ;
- utilisée une seule fois ;
- gardée secrète ;

alors le chiffrement peut atteindre la confidentialité parfaite au sens informationnel.

Conceptuellement :

\[ C=MK \]

# 132\. POURQUOI LE ONE-TIME PAD N’EST PAS LA SOLUTION UNIVERSELLE

Le problème est la gestion de la clé :

message de 1 Go  
↓  
clé secrète de 1 Go

Il faut :

- générer ;
- distribuer ;
- stocker ;
- protéger ;
- synchroniser ;

une clé aussi grande que les données.

La cryptographie moderne cherche donc des solutions beaucoup plus pratiques.

# 133\. SÉCURITÉ COMPUTATIONNELLE VS INFORMATIONNELLE

### Informationnelle

Même avec une puissance de calcul illimitée, l’adversaire ne peut pas obtenir l’information.

### Computationnelle

La sécurité repose sur le fait que l’attaque est suffisamment coûteuse.

RSA, ECC et de nombreuses constructions modernes reposent sur cette seconde logique.

# 134\. HYPOTHÈSES DE SÉCURITÉ

Une construction cryptographique repose sur une hypothèse.

Exemples :

- factorisation difficile ;
- logarithme discret difficile ;
- problème sur courbes elliptiques difficile ;
- collision difficile ;
- problème sur réseaux difficile.

Une primitive n’est donc pas :

« magiquement sûre ».

Elle est sûre **dans un modèle donné sous certaines hypothèses**.

# 135\. PREUVE DE SÉCURITÉ

Une preuve cryptographique peut chercher à montrer :

si un adversaire casse le protocole, alors il peut résoudre un problème réputé difficile.

Conceptuellement :

attaquer protocole  
↓  
convertir attaque  
↓  
résoudre problème difficile  
↓  
contradiction avec hypothèse

# 136\. REDUCTION CRYPTOGRAPHIQUE

Connexion directe avec le domaine O.

On peut montrer :

\[ A B \]

au sens où une capacité à résoudre (A) permettrait de résoudre (B), ou inversement selon la réduction.

La notion de réduction permet de relier :

- sécurité ;
- difficulté ;
- hypothèses ;
- problèmes mathématiques.

# 137\. COMPLEXITÉ D’UNE ATTAQUE

Une question centrale :

combien coûte l’attaque ?

Exemples :

\[ O(2^{128}) \]

peut être considéré comme hors de portée dans de nombreux contextes classiques.

Mais :

\[ O(2^{40}) \]

est complètement différent.

La taille des clés doit donc être pensée en termes de **niveau de sécurité**, pas seulement en nombre de bits.

# 138\. KEY LENGTH ≠ SECURITY LEVEL

Une clé de 256 bits n’implique pas automatiquement :

\[ 256 \]

Le niveau réel dépend de l’algorithme.

Exemple :

- clé symétrique ;
- RSA ;
- ECC ;

ne se comparent pas directement par leur longueur brute.

# 139\. CRYPTOGRAPHIC AGILITY ET FUTUR

Une bonne architecture doit pouvoir évoluer lorsque :

- une vulnérabilité apparaît ;
- un standard change ;
- un algorithme devient obsolète ;
- une nouvelle attaque apparaît ;
- les capacités matérielles augmentent ;
- la menace quantique progresse.

# 140\. CRYPTOGRAPHIE ET COMPLEXITÉ

Connexion :

problème mathématique  
↓  
complexité d’attaque  
↓  
niveau de sécurité  
↓  
paramètres cryptographiques  
↓  
coût système

La cryptographie transforme donc une notion mathématique de difficulté en une contrainte d’ingénierie.

# 141\. CRYPTOGRAPHIE ET PERFORMANCE

Un système cryptographique doit considérer :

- CPU ;
- mémoire ;
- latence ;
- débit ;
- taille des clés ;
- taille des signatures ;
- taille des ciphertexts ;
- génération aléatoire ;
- accès matériel.

# 142\. LATENCE VS DÉBIT

Un algorithme peut être :

- rapide pour un gros volume ;
- mais coûteux au démarrage.

Ou :

- léger par opération ;
- mais coûteux lorsqu’il est répété des millions de fois.

# 143\. HYBRID CRYPTOGRAPHY

Architecture typique :

Asymétrique  
↓  
établissement de clé  
↓  
clé symétrique  
↓  
AES-GCM / ChaCha20-Poly1305  
↓  
données

C’est l’un des concepts architecturaux les plus importants à reconnaître.

# 144\. ENVELOPE ENCRYPTION

Concept :

data  
↓  
clé de données  
↓  
ciphertext

Puis :

clé de données  
↓  
clé maître  
↓  
wrapped key

On peut ainsi séparer :

- chiffrement des données ;
- gestion des clés.

# 145\. KMS

**Key Management Service**

Un KMS peut gérer :

- génération ;
- stockage ;
- rotation ;
- permissions ;
- utilisation ;
- audit.

# 146\. TRUST BOUNDARY

Dans une architecture cryptographique, il faut identifier :

zone de confiance  
\--------------------  
clé privée  
secret  
HSM  
\--------------------  
zone non fiable  
Internet  
client  
base

La question fondamentale :

qui possède réellement le secret ?

# 147\. CRYPTOGRAPHIE CÔTÉ CLIENT

Si un secret est présent dans un frontend public :

JavaScript  
↓  
clé secrète  
↓  
attaquant

la clé doit être considérée comme compromise.

La cryptographie ne peut pas transformer un secret distribué publiquement en secret.

# 148\. RECONNAISSANCE DES PROBLÈMES

Lorsqu’un problème contient :

| Signal | Concept à suspecter |
| --- | --- |
| « cacher les données » | chiffrement |
| « vérifier modification » | hash / MAC / signature |
| « vérifier l’auteur » | signature / authentification |
| « mot de passe » | password KDF |
| « secret partagé » | Diffie-Hellman / KEM |
| « clé publique » | cryptographie asymétrique |
| « HTTPS » | TLS |
| « certificat » | PKI / X.509 |
| « blockchain » | hash / signature / Merkle |
| « preuve sans révéler » | zero-knowledge |
| « données chiffrées mais calculables » | homomorphic encryption |
| « plusieurs parties sans partager les données » | MPC |
| « ordinateur quantique » | post-quantum cryptography |
| « intégrité d’un logiciel » | hash + signature |
| « clé compromise » | rotation / révocation |
| « token signé » | MAC / signature |
| « secret dans Git » | secret management |

# 149\. WORKFLOW D’ANALYSE CRYPTOGRAPHIQUE

Lorsqu’un nouveau système doit être sécurisé :

## Étape 1 — Identifier les actifs

Exemples :

- mot de passe ;
- clé API ;
- données personnelles ;
- paiement ;
- document ;
- identité.

## Étape 2 — Identifier les adversaires

- utilisateur malveillant ;
- attaquant réseau ;
- serveur compromis ;
- insider ;
- attaquant physique.

## Étape 3 — Définir les propriétés

- confidentialité ;
- intégrité ;
- authenticité ;
- disponibilité ;
- confidentialité à long terme.

## Étape 4 — Choisir les primitives

- hash ;
- MAC ;
- AEAD ;
- signature ;
- KDF ;
- KEM.

## Étape 5 — Concevoir le protocole

Définir :

- messages ;
- états ;
- clés ;
- nonces ;
- erreurs ;
- rotation.

## Étape 6 — Gérer les clés

- génération ;
- stockage ;
- rotation ;
- révocation.

## Étape 7 — Analyser les implémentations

- bibliothèque ;
- configuration ;
- constant-time ;
- RNG ;
- logs ;
- mémoire.

## Étape 8 — Tester

- tests fonctionnels ;
- tests négatifs ;
- tests d’interopérabilité ;
- tests de protocole ;
- tests de sécurité.

## Étape 9 — Préparer l’évolution

- rotation ;
- migration ;
- crypto-agility ;
- post-quantum.

# 150\. ERREURS CRYPTOGRAPHIQUES CLASSIQUES

## Erreur 1

Inventer son propre algorithme.

« Je vais créer mon propre chiffrement. »

À éviter dans les systèmes réels.

## Erreur 2

Utiliser Base64 comme chiffrement.

Base64 est un encodage.

## Erreur 3

Utiliser SHA-256 pour chiffrer.

SHA-256 est un hash.

## Erreur 4

Stocker les mots de passe en clair.

## Erreur 5

Stocker simplement SHA-256(password).

## Erreur 6

Réutiliser un nonce là où cela est interdit.

## Erreur 7

Mettre une clé secrète dans le frontend.

## Erreur 8

Utiliser RSA « brut ».

## Erreur 9

Utiliser Diffie-Hellman sans authentification.

## Erreur 10

Créer soi-même un protocole cryptographique.

## Erreur 11

Loguer les secrets.

## Erreur 12

Ne jamais faire tourner les clés.

## Erreur 13

Confondre authentification et autorisation.

## Erreur 14

Croire que HTTPS protège automatiquement toute la logique applicative.

## Erreur 15

Croire qu’un hash garantit la confidentialité.

# 151\. BIBLIOTHÈQUES CRYPTOGRAPHIQUES

En production, il faut généralement privilégier des bibliothèques reconnues.

Exemples d’écosystèmes :

- OpenSSL ;
- libsodium ;
- BoringSSL ;
- Web Crypto API ;
- bibliothèques cryptographiques natives des langages.

Le principe :

**ne pas réimplémenter une primitive cryptographique lorsque le problème a déjà une implémentation robuste et auditée.**

# 152\. API CRYPTOGRAPHIQUE

Une bonne API doit réduire les erreurs.

Mauvaise abstraction :

encrypt(data, key, iv, mode, padding, ...)

où l’utilisateur doit choisir lui-même de nombreux paramètres dangereux.

Meilleure abstraction :

seal(plaintext, key)  
open(ciphertext, key)

avec des paramètres sûrs par défaut lorsque le contexte le permet.

# 153\. CRYPTOGRAPHIE ET ARCHITECTURE LOGICIELLE

On peut isoler une couche :

Application  
↓  
Security Service  
↓  
Crypto Abstraction  
↓  
Crypto Library  
↓  
OS / Hardware

Avantages :

- remplacement d’algorithme ;
- tests ;
- audit ;
- centralisation ;
- crypto-agility.

# 154\. MODÈLE DE DONNÉES CRYPTOGRAPHIQUE

Un système réel peut avoir :

Key  
├── id  
├── algorithm  
├── purpose  
├── version  
├── created_at  
├── expires_at  
├── status  
└── metadata

Important :

ne pas traiter une clé cryptographique comme une simple chaîne de caractères sans contexte.

# 155\. ÉTAT D’UNE CLÉ

Une clé peut être :

GENERATED  
↓  
ACTIVE  
↓  
ROTATING  
↓  
DEPRECATED  
↓  
REVOKED  
↓  
DESTROYED

Cette modélisation est extrêmement utile dans les architectures réelles.

# 156\. CRYPTOGRAPHIE ET AUDIT

Un système auditable doit pouvoir répondre :

- quelle clé a été utilisée ?
- pour quel usage ?
- quand ?
- par quel service ?
- quelle version de l’algorithme ?
- la clé était-elle active ?
- quelle politique s’appliquait ?

Attention cependant :

les logs eux-mêmes ne doivent pas révéler les secrets.

# 157\. FICHES D’APPROFONDISSEMENT

## P01 — Arithmétique modulaire

À maîtriser :

- congruence ;
- PGCD ;
- Euclide ;
- Euclide étendu ;
- inverse modulaire ;
- exponentiation modulaire.

## P02 — Groupes

À maîtriser :

- groupe ;
- sous-groupe ;
- ordre ;
- générateur ;
- groupe cyclique ;
- homomorphisme.

## P03 — Corps finis

À maîtriser :

- (\_p) ;
- (\_{2^n}) ;
- polynômes ;
- opérations ;
- inverse.

## P04 — RSA

À maîtriser :

- génération ;
- (p,q) ;
- (n) ;
- (e) ;
- (d) ;
- Euler / Carmichael ;
- exponentiation ;
- OAEP ;
- PSS ;
- CRT.

## P05 — Diffie-Hellman

À maîtriser :

- groupe ;
- générateur ;
- clé privée ;
- clé publique ;
- secret partagé ;
- MITM ;
- authentification ;
- forward secrecy.

## P06 — ECC

À maîtriser :

- courbes ;
- points ;
- addition ;
- multiplication scalaire ;
- ECDH ;
- ECDSA ;
- EdDSA.

## P07 — Hash

À maîtriser :

- préimage ;
- seconde préimage ;
- collision ;
- avalanche ;
- résistance ;
- SHA-2 ;
- SHA-3.

## P08 — MAC

À maîtriser :

- secret partagé ;
- intégrité ;
- authentification ;
- HMAC ;
- comparaison constante.

## P09 — AEAD

À maîtriser :

- plaintext ;
- ciphertext ;
- nonce ;
- tag ;
- associated data ;
- AES-GCM ;
- ChaCha20-Poly1305.

## P10 — KDF

À maîtriser :

- dérivation ;
- salt ;
- context ;
- séparation de clés ;
- PBKDF2 ;
- scrypt ;
- Argon2 ;
- HKDF.

## P11 — Signatures

À maîtriser :

- clé privée ;
- clé publique ;
- hash ;
- signature ;
- vérification ;
- RSA-PSS ;
- ECDSA ;
- EdDSA.

## P12 — PKI

À maîtriser :

- certificat ;
- CA ;
- chaîne de confiance ;
- X.509 ;
- révocation ;
- renouvellement ;
- trust store.

## P13 — TLS

À maîtriser :

- handshake ;
- authentification ;
- key establishment ;
- clés de session ;
- AEAD ;
- certificats ;
- forward secrecy.

## P14 — Blockchain

À maîtriser :

- hash chain ;
- Merkle tree ;
- signatures ;
- clés ;
- transaction ;
- preuve ;
- consensus.

## P15 — Zero-Knowledge

À maîtriser :

- prover ;
- verifier ;
- witness ;
- statement ;
- completeness ;
- soundness ;
- zero-knowledge.

## P16 — MPC

À maîtriser :

- secret sharing ;
- parties ;
- protocole ;
- calcul distribué ;
- confidentialité.

## P17 — Homomorphic Encryption

À maîtriser :

- opération sur ciphertext ;
- correspondance avec opération sur plaintext ;
- FHE ;
- coût computationnel.

## P18 — Side Channels

À maîtriser :

- timing ;
- cache ;
- power analysis ;
- constant-time ;
- fault injection.

## P19 — Post-Quantum

À maîtriser :

- Shor ;
- Grover ;
- lattices ;
- KEM ;
- ML-KEM ;
- ML-DSA ;
- SLH-DSA ;
- migration.

## P20 — Key Management

À maîtriser :

- génération ;
- stockage ;
- rotation ;
- révocation ;
- destruction ;
- KMS ;
- HSM ;
- crypto-agility.

# 158\. PROJETS D’APPRENTISSAGE

## Projet 1 — Mini coffre-fort chiffré

Construire un petit système permettant :

- création d’un mot de passe maître ;
- dérivation de clé ;
- chiffrement AEAD ;
- stockage ;
- déchiffrement.

Objectif :

comprendre la chaîne :

password  
↓  
KDF  
↓  
key  
↓  
AEAD  
↓  
ciphertext

# 159\. PROJET 2 — Implémentation pédagogique de RSA

Implémenter uniquement à des fins pédagogiques :

- génération de petits nombres premiers ;
- PGCD ;
- inverse modulaire ;
- génération RSA ;
- chiffrement ;
- déchiffrement.

Puis comparer avec une bibliothèque réelle.

Objectif :

comprendre la mathématique sans confondre cela avec une implémentation de production.

# 160\. PROJET 3 — Diffie-Hellman pédagogique

Construire :

Alice  
↘  
public channel  
↗  
Bob

et vérifier que :

\[ K_A=K_B \]

Puis simuler :

Alice ↔ Eve ↔ Bob

pour observer le problème MITM.

# 161\. PROJET 4 — Mini TLS pédagogique

Construire une simulation :

Client  
↓  
server identity  
↓  
key exchange  
↓  
session key  
↓  
AEAD  
↓  
secure messages

Sans prétendre remplacer TLS.

# 162\. PROJET 5 — Système de fichiers signé

Créer :

file  
↓  
hash  
↓  
signature  
↓  
manifest

Puis :

file  
+  
signature  
+  
public key  
↓  
verify

# 163\. PROJET 6 — Blockchain minimale

Construire :

Block  
├── index  
├── timestamp  
├── transactions  
├── previous_hash  
└── hash

Puis simuler une modification.

genui{“learning_viz”:{“type_id”:“BLOCKCHAIN_HASH_CHAIN”,“initial_values”:{“chainState”:“original”},“locale_override”:“fr-FR”}}

# 164\. PROJET 7 — Merkle Tree

Construire un arbre de Merkle permettant :

- calcul de root ;
- génération d’une preuve ;
- vérification d’une preuve.

Objectif :

comprendre comment vérifier efficacement l’appartenance d’une donnée.

# 165\. PROJET 8 — Password Vault

Construire un gestionnaire de secrets pédagogique avec :

- KDF ;
- salt ;
- AEAD ;
- rotation de clé ;
- verrouillage ;
- audit.

# 166\. PROJET 9 — Agent IA signé

Construire un agent qui possède une paire :

private key  
public key

L’agent signe chaque action.

Le serveur vérifie :

action  
+  
signature  
+  
public key

Objectif :

explorer l’identité cryptographique des agents.

# 167\. PROJET 10 — Provenance de modèles IA

Construire un système :

model.bin  
↓  
hash  
↓  
signature  
↓  
registry

Puis vérifier l’authenticité avant chargement.

# 168\. CHALLENGES SANS IA

## Challenge 1

Calculer manuellement :

\[ 17^{-1} \]

avec Euclide étendu.

## Challenge 2

Construire un petit RSA pédagogique.

## Challenge 3

Démontrer pourquoi :

\[ ECDH \]

produit le même secret des deux côtés.

## Challenge 4

Construire une collision volontaire avec un hash jouet.

## Challenge 5

Démontrer une attaque par réutilisation de nonce sur une construction jouet.

## Challenge 6

Construire une chaîne de hash.

## Challenge 7

Construire un Merkle tree.

## Challenge 8

Modéliser une attaque MITM.

## Challenge 9

Concevoir un protocole challenge-response.

## Challenge 10

Concevoir un système de rotation de clés.

# 169\. CHALLENGES AVEC IA

## Challenge IA 1 — Crypto Code Reviewer

Donner un code volontairement vulnérable à l’IA.

Lui demander :

identifie toutes les erreurs cryptographiques sans proposer immédiatement de correction.

Puis vérifier humainement.

## Challenge IA 2 — Protocol Designer

Demander à l’IA de concevoir un protocole.

Puis chercher :

- replay ;
- MITM ;
- mauvaise gestion des nonces ;
- key reuse ;
- downgrade ;
- confusion de contexte.

## Challenge IA 3 — Threat Model Generator

Donner une architecture.

Demander :

actifs  
adversaires  
capacités  
objectifs  
attaques  
contre-mesures

## Challenge IA 4 — Crypto Migration Agent

Construire un agent capable d’inventorier :

RSA  
ECC  
SHA  
AES  
TLS  
certificats

puis d’identifier les dépendances et proposer une stratégie de migration.

# 170\. APPLICATIONS CRÉATIVES

La cryptographie devient particulièrement intéressante lorsqu’on cesse de la considérer uniquement comme :

« cacher des données ».

## 170.1 Cryptographic Identity for AI Agents

Chaque agent possède une identité cryptographique.

Agent  
↓  
public/private key  
↓  
signed actions  
↓  
verifiable identity

Possibilités :

- agents authentifiables ;
- réputation ;
- audit ;
- délégation ;
- permissions.

## 170.2 Agent Capability Tokens

Un agent reçoit un token signé représentant certaines capacités.

Agent  
↓  
capability token  
↓  
service  
↓  
verification  
↓  
action allowed

## 170.3 Verifiable AI Outputs

Une sortie d’IA peut être accompagnée de :

hash  
+  
signature  
+  
model identifier  
+  
timestamp

Permettant de construire une couche de provenance.

## 170.4 Complexity-Aware Cryptographic Systems

Connexion avec le domaine O :

security level  
↓  
algorithm  
↓  
computational cost  
↓  
latency  
↓  
scalability

Un système peut alors calculer un **budget cryptographique**.

## 170.5 Privacy-Aware RAG

Architecture :

private documents  
↓  
access control  
↓  
encryption  
↓  
retrieval  
↓  
authorized context  
↓  
LLM

La cryptographie devient une composante de la confidentialité du RAG.

## 170.6 Verifiable RAG

Associer aux documents :

- hash ;
- signature ;
- provenance ;
- version.

L’agent peut vérifier l’origine des documents avant utilisation.

## 170.7 Cryptographic Supply Chain

Chaque composant logiciel possède :

artifact  
↓  
hash  
↓  
signature  
↓  
dependency graph  
↓  
verification

Cela permet de construire une supply chain plus vérifiable.

## 170.8 Personal Data Vault

Architecture :

Utilisateur  
↓  
Personal Vault  
↓  
données chiffrées  
↓  
permissions cryptographiques

L’utilisateur contrôle quelles applications peuvent accéder à quelles données.

## 170.9 Portable Digital Identity

Construire une identité composée de :

- clés ;
- credentials ;
- signatures ;
- preuves ;
- attestations.

Cela peut se connecter aux systèmes d’identité décentralisée.

## 170.10 Cryptographic Access Layer

Une application pourrait abstraire :

WHO  
↓  
WHAT  
↓  
WHICH KEY  
↓  
WHICH OPERATION  
↓  
WHICH DATA

pour construire une couche d’accès cryptographique unifiée.

# 171\. MATRICE DE RECONNAISSANCE

| Problème | Outil |
| --- | --- |
| cacher une donnée | chiffrement |
| chiffrer beaucoup de données | AES / ChaCha20 |
| vérifier une modification | hash / MAC / signature |
| authentifier avec secret partagé | MAC |
| authentifier avec clé publique | signature |
| établir une clé | DH / ECDH / KEM |
| protéger une session | AEAD |
| protéger un mot de passe | KDF |
| protéger une clé | KMS / HSM |
| authentifier un serveur | certificat / PKI |
| sécuriser HTTP | TLS |
| prouver une provenance | signature |
| construire un registre vérifiable | hash + Merkle + signatures |
| prouver sans révéler | zero-knowledge |
| calculer sur données privées | homomorphic / MPC |
| préparer l’ère quantique | PQC |
| protéger un firmware | signature |
| authentifier un agent | clé + signature |
| rendre les algorithmes remplaçables | crypto-agility |

# 172\. CONNEXIONS AVEC LES AUTRES DOMAINES

## B — Théorie des nombres

Fondations :

- nombres premiers ;
- factorisation ;
- congruences ;
- PGCD ;
- inverses ;
- exponentiation modulaire.

## C — Algèbre linéaire

Intervient notamment dans :

- constructions algébriques ;
- cryptographie sur réseaux ;
- certaines constructions post-quantiques.

## G — Probabilités

Fondamentales pour :

- hasard ;
- sécurité probabiliste ;
- distributions ;
- génération de clés ;
- analyse d’attaques.

## M — Théorie de l’information

Connexion :

- entropie ;
- information ;
- secret ;
- fuite ;
- sécurité informationnelle.

## O — Complexité

Connexion :

- difficulté des problèmes ;
- coût des attaques ;
- niveau de sécurité ;
- réduction ;
- menace quantique.

## E — Graphes

Applications :

- réseaux ;
- blockchain ;
- arbres de Merkle ;
- structures distribuées ;
- protocoles.

## L — Analyse numérique

Pertinente pour :

- implémentations numériques ;
- calculs à haute précision ;
- erreurs ;
- optimisation de certaines primitives.

# 173\. CRYPTOGRAPHIE ET SÉCURITÉ SYSTÈME

La sécurité peut être vue comme une chaîne :

Mathématiques  
↓  
Primitive  
↓  
Construction  
↓  
Protocole  
↓  
Bibliothèque  
↓  
Implémentation  
↓  
Architecture  
↓  
Déploiement  
↓  
Opérations

Une faiblesse à n’importe quel niveau peut compromettre le système.

# 174\. CRYPTOGRAPHIE ET DÉFENSE EN PROFONDEUR

Une architecture robuste peut combiner :

TLS  
+  
authentification  
+  
autorisation  
+  
AEAD  
+  
key management  
+  
logging  
+  
rate limiting  
+  
monitoring

La cryptographie ne remplace pas les autres couches.

# 175\. CRYPTOGRAPHIE ET ZERO TRUST

Dans une architecture Zero Trust :

ne pas supposer qu’un composant est fiable simplement parce qu’il est à l’intérieur du réseau.

La cryptographie permet notamment :

- authentification forte ;
- identité machine ;
- certificats ;
- signatures ;
- canaux sécurisés ;
- attestation.

# 176\. MENTAL MODEL GLOBAL

Le modèle mental fondamental du domaine P est :

MENACE  
↓  
MODÈLE DE MENACE  
↓  
PROPRIÉTÉ À GARANTIR  
↓  
PRIMITIVE  
↓  
PROTOCOLE / CONSTRUCTION  
↓  
GESTION DES CLÉS  
↓  
IMPLÉMENTATION  
↓  
ARCHITECTURE  
↓  
SYSTÈME  
↓  
ÉVOLUTION

# 177\. LES CINQ GRANDES QUESTIONS

Lorsqu’un système utilise de la cryptographie, toujours demander :

### 1\. Qu’est-ce que je protège ?

Donnée, identité, clé, transaction, communication ?

### 2\. Contre qui ?

Attaquant réseau, utilisateur, serveur compromis, attaquant physique ?

### 3\. Quelle propriété ?

Confidentialité, intégrité, authenticité, preuve ?

### 4\. Quelle primitive ?

AES, hash, MAC, signature, KDF, KEM ?

### 5\. Comment les clés vivent-elles ?

Génération, stockage, rotation, révocation, destruction ?

# 178\. LES DISTINCTIONS À NE JAMAIS OUBLIER

HASH ≠ CHIFFREMENT  
<br/>ENCODAGE ≠ CHIFFREMENT  
<br/>AUTHENTIFICATION ≠ AUTORISATION  
<br/>SIGNATURE ≠ CHIFFREMENT  
<br/>DIFFIE-HELLMAN ≠ AUTHENTIFICATION  
<br/>BLOCKCHAIN ≠ CHIFFREMENT  
<br/>TLS ≠ SÉCURITÉ TOTALE  
<br/>CLÉ PUBLIQUE ≠ SECRET  
<br/>SECRET ≠ HASH  
<br/>AES ≠ AES-GCM  
<br/>RSA BRUT ≠ RSA-OAEP / RSA-PSS  
<br/>PQC ≠ CRYPTOGRAPHIE QUANTIQUE

# 179\. CHECKLIST DE MAÎTRISE

Tu maîtrises le domaine P lorsque tu peux expliquer sans aide :

### Fondements

- arithmétique modulaire ;
- PGCD ;
- Euclide étendu ;
- inverse modulaire ;
- exponentiation modulaire ;
- groupes ;
- groupes cycliques ;
- corps finis ;
- hasard cryptographique.

### Primitives

- hash ;
- collision ;
- préimage ;
- MAC ;
- HMAC ;
- KDF ;
- chiffrement symétrique ;
- AEAD ;
- signature ;
- KEM.

### Algorithmes

- AES ;
- RSA ;
- Diffie-Hellman ;
- ECDH ;
- ECDSA ;
- EdDSA ;
- SHA-2 ;
- SHA-3.

### Protocoles

- TLS ;
- PKI ;
- certificats ;
- X.509 ;
- challenge-response ;
- replay protection.

### Sécurité

- MITM ;
- brute force ;
- nonce reuse ;
- side-channel ;
- constant-time ;
- key compromise ;
- rotation ;
- révocation.

### Technologies avancées

- blockchain ;
- Merkle tree ;
- zero-knowledge ;
- MPC ;
- homomorphic encryption ;
- secure aggregation ;
- post-quantum cryptography.

### Architecture

- KMS ;
- HSM ;
- secret management ;
- crypto-agility ;
- secure boot ;
- provenance ;
- signed artifacts.

# 180\. TEST ULTIME

Pour vérifier une véritable compréhension, prendre un système réel :

**application web avec comptes utilisateurs, paiements, API, données personnelles et agents IA.**

Puis répondre :

1.  Quelles données doivent être chiffrées ?
2.  Quelles données doivent seulement être hashées ?
3.  Quels secrets doivent être stockés ?
4.  Où doivent-ils être stockés ?
5.  Comment les mots de passe sont-ils protégés ?
6.  Comment le serveur est-il authentifié ?
7.  Comment le client est-il authentifié ?
8.  Comment les clés de session sont-elles établies ?
9.  Pourquoi utiliser AEAD ?
10. Comment éviter les attaques replay ?
11. Comment faire tourner les clés ?
12. Que faire si une clé fuit ?
13. Comment signer les artefacts ?
14. Comment vérifier la provenance ?
15. Quelle architecture permettrait une migration post-quantique ?
16. Quels éléments sont cryptographiques ?
17. Quels éléments relèvent de l’autorisation ?
18. Quels éléments relèvent de la sécurité système ?
19. Quelles hypothèses mathématiques soutiennent les mécanismes choisis ?
20. Quel est le coût computationnel des opérations ?

Si tu peux répondre précisément à ces questions, tu ne connais plus seulement des algorithmes cryptographiques.

Tu commences à **raisonner comme un architecte cryptographique**.

# 181\. SYNTHÈSE FINALE

La cryptographie peut être comprise comme une chaîne :

MATHÉMATIQUES  
↓  
arithmétique  
groupes  
corps finis  
probabilités  
↓  
PROBLÈMES DIFFICILES  
↓  
PRIMITIVES  
↓  
hash  
MAC  
AES  
RSA  
ECC  
KDF  
signatures  
KEM  
↓  
PROTOCOLES  
↓  
TLS  
PKI  
authentification  
échange de clés  
↓  
ARCHITECTURES  
↓  
web  
cloud  
paiements  
blockchain  
IoT  
IA  
↓  
SÉCURITÉ  
↓  
confidentialité  
intégrité  
authenticité  
identité  
provenance  
↓  
ÉVOLUTION  
↓  
crypto-agility  
post-quantum

Le point fondamental est le suivant :

**La cryptographie transforme des problèmes mathématiques difficiles en mécanismes informatiques permettant de créer de la confiance dans des environnements où la confiance directe n’existe pas.**

Elle ne consiste donc pas simplement à chiffrer.

Elle permet de répondre à des questions beaucoup plus profondes :

**Comment prouver que cette donnée n’a pas changé ?**

**Comment savoir qui a produit cette information ?**

**Comment établir un secret sur un canal public ?**

**Comment communiquer sans faire confiance au réseau ?**

**Comment permettre à plusieurs parties de calculer sans révéler leurs données ?**

**Comment prouver quelque chose sans révéler le secret qui le démontre ?**

**Comment construire une identité numérique vérifiable ?**

**Comment construire des agents logiciels capables de s’authentifier et de signer leurs actions ?**

**Comment maintenir cette confiance lorsque les algorithmes actuels deviennent obsolètes ?**

C’est cette dernière dimension qui fait de la cryptographie une discipline particulièrement importante pour l’ingénierie logicielle moderne.

# 182\. FORMULE MENTALE ULTIME

CRYPTOGRAPHIE  
│  
┌────────────┼────────────┐  
↓ ↓ ↓  
CONFIDENTIALITÉ INTÉGRITÉ AUTHENTICITÉ  
│ │ │  
AES HASH SIGNATURE  
│ │ │  
└────────────┼────────────┘  
↓  
ÉTABLISSEMENT  
DE CLÉS  
↓  
DIFFIE-HELLMAN  
/ ECC / KEM  
↓  
PROTOCOLES  
↓  
TLS / PKI  
↓  
ARCHITECTURES  
↓  
WEB / CLOUD / IA / BLOCKCHAIN  
↓  
CONFIANCE  
↓  
POST-QUANTIQUE

### L’idée à retenir

**Ne demande pas seulement : « Quel algorithme dois-je utiliser ? »**

Demande :

**« Quelle propriété de sécurité dois-je garantir, contre quel adversaire, sous quelles hypothèses, avec quelles clés, dans quel protocole, et comment cette sécurité évoluera-t-elle lorsque le système grandira ou que les hypothèses changeront ? »**

C’est à ce niveau que la cryptographie passe d’une collection d’algorithmes à une **discipline d’ingénierie de la confiance**.