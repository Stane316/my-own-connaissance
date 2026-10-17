# DOCUMENT F — COMBINATOIRE ET OPTIMISATION COMBINATOIRE

## Cartographie complète pour les mathématiques discrètes, l’algorithmique, les structures de données, les graphes, l’IA et les systèmes informatiques

# 0 — IDENTITÉ ET MISSION DU DOMAINE

## 0.1 Définition générale

La **combinatoire** est la branche des mathématiques discrètes qui étudie les structures finies ou dénombrables, notamment :

- comment les objets peuvent être construits ;
- combien de configurations existent ;
- comment les configurations se répartissent ;
- quelles contraintes elles satisfont ;
- comment générer ces configurations ;
- comment rechercher une configuration optimale ;
- comment compter sans énumérer explicitement toutes les possibilités.

Elle répond donc à des questions du type :

Combien de possibilités existe-t-il ?

De combien de façons peut-on organiser ces objets ?

Combien de configurations satisfont ces contraintes ?

Comment générer toutes les configurations ?

Comment trouver la meilleure configuration parmi un ensemble immense ?

# 1 — PLACE DE LA COMBINATOIRE DANS LA CARTOGRAPHIE

La progression des domaines précédents peut être prolongée ainsi :

A — LOGIQUE ET FONDEMENTS  
↓  
raisonner sur les propositions et les structures  
<br/>B — THÉORIE DES NOMBRES  
↓  
raisonner sur les structures arithmétiques  
<br/>C — ALGÈBRE LINÉAIRE / GÉOMÉTRIE LINÉAIRE  
↓  
représenter et transformer des espaces  
<br/>D — GÉOMÉTRIE COMPUTATIONNELLE  
↓  
raisonner sur les structures spatiales  
<br/>E — THÉORIE DES GRAPHES  
↓  
raisonner sur les relations discrètes  
<br/>F — COMBINATOIRE  
↓  
compter, construire, énumérer et optimiser  
les structures discrètes

La combinatoire constitue donc une sorte de **moteur de comptage et d’organisation du discret**.

# 2 — POURQUOI LA COMBINATOIRE EST FONDAMENTALE EN INFORMATIQUE

L’informatique manipule constamment des ensembles de possibilités.

Exemples :

Mots de passe  
↓  
combinaisons de caractères  
<br/>Ordonnancement  
↓  
permutations de tâches  
<br/>Réseaux  
↓  
configurations possibles  
<br/>Graphes  
↓  
sous-graphes / chemins / colorations  
<br/>Programmes  
↓  
chemins d'exécution  
<br/>IA  
↓  
espace de configurations  
<br/>Recherche  
↓  
espace d'états  
<br/>Tests  
↓  
combinaisons de paramètres  
<br/>Bases de données  
↓  
possibilités de requêtes / jointures  
<br/>Systèmes  
↓  
états et transitions

Une partie importante de la complexité algorithmique vient précisément de la taille de ces espaces.

# 3 — CARTOGRAPHIE GLOBALE DU DOMAINE

Le domaine F peut être organisé en grandes familles.

## Famille A — Principes fondamentaux de comptage

- principe additif ;
- principe multiplicatif ;
- complément ;
- partition ;
- bijection ;
- double comptage ;
- principe des tiroirs.

## Famille B — Factorielle

- factorielle ;
- notation (n!) ;
- propriétés ;
- récurrence ;
- croissance.

## Famille C — Permutations

- permutations simples ;
- permutations partielles ;
- permutations avec répétition ;
- permutations circulaires ;
- permutations avec contraintes.

## Famille D — Arrangements

- arrangements sans répétition ;
- arrangements avec répétition ;
- sélection ordonnée.

## Famille E — Combinaisons

- combinaisons simples ;
- combinaisons avec répétition ;
- coefficients binomiaux ;
- triangle de Pascal.

## Famille F — Binôme et coefficients

- coefficients binomiaux ;
- formule du binôme ;
- identités combinatoires ;
- récurrences binomiales.

## Famille G — Répétitions et distributions

- étoiles et barres ;
- distributions d’objets ;
- compositions ;
- partitions ;
- contraintes de capacité.

## Famille H — Récurrences

- récurrences linéaires ;
- récurrences non linéaires ;
- conditions initiales ;
- résolution ;
- récursivité algorithmique.

## Famille I — Fonctions génératrices

- fonctions génératrices ordinaires ;
- fonctions génératrices exponentielles ;
- encodage de suites ;
- résolution de récurrences ;
- dénombrement.

## Famille J — Inclusion-exclusion

- principe d’inclusion-exclusion ;
- intersections ;
- unions ;
- dérangements ;
- contraintes multiples.

## Famille K — Bijections

- correspondances ;
- preuves bijectives ;
- changements de représentation ;
- comptages indirects.

## Famille L — Structures discrètes

- ensembles ;
- suites ;
- mots ;
- arbres ;
- graphes ;
- partitions ;
- permutations ;
- familles de sous-ensembles.

## Famille M — Énumération algorithmique

- backtracking ;
- génération de permutations ;
- génération de combinaisons ;
- génération de sous-ensembles ;
- génération lexicographique ;
- pruning.

## Famille N — Programmation dynamique

- sous-problèmes ;
- états ;
- transitions ;
- mémoïsation ;
- tabulation ;
- comptage dynamique.

## Famille O — Optimisation combinatoire

- optimisation discrète ;
- recherche exhaustive ;
- glouton ;
- programmation dynamique ;
- branch and bound ;
- programmation entière ;
- approximation ;
- heuristiques.

## Famille P — Probabilités combinatoires

- espace fini ;
- dénombrement ;
- probabilités discrètes ;
- variables aléatoires discrètes ;
- espérance ;
- distributions classiques.

## Famille Q — Combinatoire sur les graphes

- colorations ;
- chemins ;
- arbres ;
- couplages ;
- sous-graphes ;
- clique ;
- couverture ;
- indépendance.

## Famille R — Applications informatiques

- cryptographie ;
- tests ;
- scheduling ;
- optimisation ;
- IA ;
- recherche ;
- sécurité ;
- bases de données ;
- réseaux ;
- jeux ;
- systèmes distribués.

# 4 — VOCABULAIRE FONDAMENTAL

## 4.1 Ensemble

Un ensemble est une collection d’objets distincts.

Exemple :

\[ A={1,2,3,4} \]

## 4.2 Cardinal

Le nombre d’éléments d’un ensemble (A) est :

\[ |A| \]

## 4.3 Sous-ensemble

Un ensemble (B) est un sous-ensemble de (A) si :

\[ BA \]

## 4.4 Configuration

Une configuration est une disposition particulière des objets considérés.

## 4.5 Arrangement

Une sélection où **l’ordre compte**.

## 4.6 Combinaison

Une sélection où **l’ordre ne compte pas**.

## 4.7 Permutation

Une organisation de tous les éléments d’un ensemble dans un ordre donné.

## 4.8 Partition

Une décomposition d’un ensemble en parties disjointes dont l’union donne l’ensemble initial.

## 4.9 Composition

Une décomposition ordonnée d’un entier.

Exemple :

\[ 5=2+1+2 \]

est une composition de 5.

# 5 — PRINCIPE ADDITIF

Si un choix peut être effectué de (a) façons dans un cas et de (b) façons dans un autre cas, avec des cas disjoints :

\[ N=a+b \]

## Exemple

Un système permet :

- 3 modes de connexion ;
- ou 2 modes hors connexion.

Si les deux catégories sont disjointes :

\[ 3+2=5 \]

possibilités.

# 6 — PRINCIPE MULTIPLICATIF

Si une procédure comporte :

- (a) possibilités pour la première étape ;
- (b) possibilités pour la deuxième ;

alors le nombre total est :

\[ ab \]

## Exemple

Un formulaire possède :

- 4 thèmes ;
- 3 niveaux.

Nombre de configurations :

\[ 4=12 \]

# 7 — RÈGLE GÉNÉRALE DU PRODUIT

Pour (k) étapes :

\[ N=n_1n_2n_k \]

Cette règle est l’une des bases de toute la combinatoire.

# 8 — FACTORIELLE

La factorielle est définie par :

\[ n!=n(n-1)(n-2) \]

avec :

\[ 0!=1 \]

## 8.1 Récurrence

\[ n!=n(n-1)! \]

## 8.2 Exemple

\[ 5!=5=120 \]

## 8.3 Importance algorithmique

La factorielle croît extrêmement rapidement.

Cela explique pourquoi les algorithmes qui explorent toutes les permutations deviennent rapidement impossibles à exécuter.

# 9 — PERMUTATIONS

## 9.1 Définition

Une permutation de (n) objets est un arrangement de tous les objets.

Nombre de permutations :

\[ P(n)=n! \]

## Exemple

Pour :

\[ {A,B,C} \]

les permutations sont :

ABC  
ACB  
BAC  
BCA  
CAB  
CBA

Donc :

\[ 3!=6 \]

# 10 — ARRANGEMENTS SANS RÉPÉTITION

On sélectionne (r) objets parmi (n), et **l’ordre compte**.

\[ A(n,r)= \]

## Exemple

Choisir :

- président ;
- vice-président ;
- secrétaire

parmi 10 personnes.

L’ordre des rôles compte.

Donc :

\[ A(10,3) = = 10 \]

# 11 — ARRANGEMENTS AVEC RÉPÉTITION

Si chaque position peut prendre l’une des (n) valeurs et qu’il y a (r) positions :

\[ n^r \]

## Exemple

Un code de 4 chiffres :

\[ 10^4 \]

possibilités si les chiffres peuvent être répétés.

# 12 — COMBINAISONS

Lorsqu’on sélectionne (r) objets parmi (n) et que l’ordre ne compte pas :

\[ nr = \]

## Exemple

Choisir 3 membres parmi 10 :

\[ \]

Les groupes :

ABC  
BAC  
CAB

représentent le même groupe.

# 13 — RELATION ENTRE ARRANGEMENT ET COMBINAISON

Une combinaison peut être transformée en arrangement en ordonnant les (r) éléments.

Ainsi :

\[ A(n,r)=nr r! \]

Donc :

\[ \]

# 14 — PERMUTATIONS ET COMBINAISONS : DISTINCTION ESSENTIELLE

| Question | Ordre compte ? | Objet |
| --- | --- | --- |
| Organiser tout le monde | Oui | permutation |
| Sélectionner des postes distincts | Oui | arrangement |
| Former une équipe | Non | combinaison |
| Former un code | Oui | arrangement |
| Choisir des éléments | Non | combinaison |

Question réflexe :

Si j’échange deux éléments, est-ce que j’obtiens une nouvelle configuration ?

Si oui :

**l’ordre compte.**

# 15 — COMBINAISONS AVEC RÉPÉTITION

Pour sélectionner (r) éléments parmi (n) types avec répétition :

\[ \]

Cette formule est notamment associée à la méthode :

**étoiles et barres**.

# 16 — ÉTOILES ET BARRES

On cherche à distribuer (r) objets identiques entre (n) catégories.

Exemple :

\[ x_1+x_2+x_3=5 \]

avec :

\[ x_i \]

Nombre de solutions :

\[ = \]

# 17 — CONTRAINTES DANS LES DISTRIBUTIONS

Les problèmes deviennent plus intéressants lorsqu’on impose :

\[ x_i \]

ou :

\[ x_ik \]

ou encore :

\[ x_1+x_2++x_n=r \]

avec des contraintes individuelles.

Techniques possibles :

- changement de variable ;
- complément ;
- inclusion-exclusion ;
- fonctions génératrices ;
- programmation dynamique.

# 18 — COEFFICIENTS BINOMIAUX

Le coefficient :

\[ nr \]

possède de nombreuses propriétés.

## Symétrie

\[ nr=n{n-r} \]

## Cas limites

\[ n0=1 \]

\[ nn=1 \]

## Récurrence de Pascal

\[ nr =

- \]

# 19 — TRIANGLE DE PASCAL

1  
1 1  
1 2 1  
1 3 3 1  
1 4 6 4 1

Chaque élément intérieur est la somme des deux éléments situés au-dessus.

# 20 — FORMULE DU BINÔME

\[ (a+b)^n = \_{k=0}^{n} nk a<sup>{n-k}b</sup>k \]

Cette formule relie directement :

- algèbre ;
- combinatoire ;
- coefficients binomiaux.

# 21 — PRINCIPE DES TIROIRS

Si (n+1) objets sont placés dans (n) catégories, alors au moins une catégorie contient au moins deux objets.

Formellement :

\[ n+1 \]

## Applications

- collisions de hash ;
- existence de doublons ;
- bornes ;
- informatique théorique ;
- algorithmes ;
- cryptographie.

# 22 — BIJECTIONS

Une bijection associe chaque élément d’un ensemble à exactement un élément d’un autre ensemble et réciproquement.

Si :

\[ AB \]

alors :

\[ |A|=|B| \]

## Pourquoi c’est puissant

Pour compter un ensemble difficile, on peut construire une bijection vers un ensemble dont le cardinal est connu.

C’est une méthode fondamentale de preuve combinatoire.

# 23 — DOUBLE COMPTAGE

Une même quantité peut être comptée de deux manières différentes.

Si :

\[ N_1=N_2 \]

on obtient une identité combinatoire.

Le double comptage est extrêmement utile pour démontrer des relations qui seraient difficiles à obtenir algébriquement.

# 24 — PRINCIPE D’INCLUSION-EXCLUSION

Pour deux ensembles :

\[ |AB| = |A|+|B|-|AB| \]

Pour trois ensembles :

\[ |ABC| = |A|+|B|+|C| -|AB| -|AC| -|BC| +|ABC| \]

Le principe général alterne :

\+ intersections simples  
− intersections doubles  
\+ intersections triples  
− ...

# 25 — APPLICATION : COMPTAGE AVEC CONTRAINTES

Lorsqu’une configuration peut violer plusieurs contraintes :

Configurations totales  
↓  
retirer celles violant A  
↓  
corriger celles violant A et B  
↓  
corriger les intersections supplémentaires

L’inclusion-exclusion permet d’éviter les doubles comptages.

# 26 — DÉRANGEMENTS

Un dérangement est une permutation dans laquelle aucun élément ne reste à sa position initiale.

Le nombre de dérangements de (n) objets est généralement noté :

\[ !n \]

ou :

\[ D_n \]

Il vérifie la récurrence :

\[ D_n=(n-1)(D_{n-1}+D_{n-2}) \]

avec :

\[ D_0=1,D_1=0 \]

# 27 — RÉCURRENCES

Une récurrence définit une suite à partir de termes précédents.

Exemple :

\[ a_n=a_{n-1}+a_{n-2} \]

avec des conditions initiales.

# 28 — SUITE DE FIBONACCI

\[ F_n=F_{n-1}+F_{n-2} \]

avec des conditions initiales selon la convention utilisée.

Cette suite constitue un exemple fondamental de :

- récurrence ;
- récursivité ;
- programmation dynamique ;
- croissance ;
- analyse algorithmique.

# 29 — RÉCURRENCES ALGORITHMIQUES

Un algorithme récursif peut produire une récurrence de temps.

Exemple conceptuel :

\[ T(n)=2T(n/2)+O(n) \]

Cette relation peut être analysée avec :

- arbre de récursion ;
- substitution ;
- théorème maître.

La combinatoire et l’analyse algorithmique se rejoignent ici.

# 30 — THÉORÈME MAÎTRE

Pour des récurrences de la forme :

\[ T(n)=aT(nb)+f(n) \]

le théorème maître permet d’obtenir des bornes asymptotiques dans plusieurs cas classiques.

Il relie :

- récursivité ;
- division pour régner ;
- complexité algorithmique.

# 31 — FONCTIONS GÉNÉRATRICES

Une fonction génératrice permet d’encoder une suite :

\[ a_0,a_1,a_2, \]

dans une expression formelle :

\[ A(x)=\_{n}a_nx^n \]

## Pourquoi les utiliser ?

Elles permettent notamment de :

- résoudre des récurrences ;
- compter des structures ;
- transformer des problèmes de comptage en problèmes algébriques ;
- extraire des coefficients.

# 32 — FONCTIONS GÉNÉRATRICES ET DISTRIBUTION

Pour une catégorie pouvant contenir :

\[ 0,1,2, \]

objets, une série comme :

\[ 1+x+x<sup>2+x</sup>3+ \]

encode les possibilités.

Pour plusieurs catégories, les produits de fonctions génératrices permettent de combiner les choix.

# 33 — COMPOSITIONS D’ENTIERS

Une composition de (n) est une écriture de (n) comme somme ordonnée d’entiers positifs.

Exemple :

\[ 5=2+1+2 \]

est différente de :

\[ 5=1+2+2 \]

car l’ordre compte.

# 34 — PARTITIONS D’ENTIERS

Une partition de (n) est une écriture de (n) comme somme où l’ordre ne compte pas.

Ainsi :

\[ 5=3+2 \]

et :

\[ 5=2+3 \]

représentent la même partition.

## Distinction essentielle

Composition  
→ ordre important  
<br/>Partition  
→ ordre ignoré

# 35 — NOMBRES DE CATALAN

Les nombres de Catalan apparaissent dans de nombreuses structures combinatoires.

Ils peuvent notamment compter :

- parenthésages valides ;
- arbres binaires ;
- triangulations de polygones ;
- certains chemins ;
- structures récursives.

Une forme classique est :

\[ C_n= \]

Ils constituent un excellent exemple de structure apparaissant dans plusieurs problèmes apparemment différents.

# 36 — STRUCTURES DISCRÈTES

La combinatoire étudie notamment :

### Ensembles

\[ {a,b,c} \]

### Suites

\[ (a_1,a_2,,a_n) \]

### Mots

Chaînes sur un alphabet.

### Arbres

Structures hiérarchiques.

### Graphes

Relations entre objets.

### Permutations

Ordonnancements.

### Partitions

Décompositions.

### Sous-ensembles

Familles de sélections.

# 37 — COMBINATOIRE DES GRAPHES

Le domaine E et le domaine F sont intimement liés.

La combinatoire peut étudier :

- nombre de chemins ;
- nombre de cycles ;
- nombre d’arbres ;
- nombre de colorations ;
- nombre de sous-graphes ;
- nombre de couplages ;
- nombre de configurations.

# 38 — NOMBRE D’ARBRES

Un résultat fondamental est le **théorème de Cayley** :

Le nombre d’arbres étiquetés sur (n) sommets est :

\[ n^{n-2} \]

pour :

\[ n \]

Ce résultat montre comment la combinatoire peut quantifier des structures issues directement de la théorie des graphes.

# 39 — ÉNUMÉRATION

L’énumération consiste à produire explicitement les objets d’un espace combinatoire.

Exemples :

Toutes les permutations  
Toutes les combinaisons  
Tous les sous-ensembles  
Tous les chemins  
Tous les arbres

# 40 — GÉNÉRATION DE SOUS-ENSEMBLES

Pour un ensemble de (n) éléments, le nombre de sous-ensembles est :

\[ 2^n \]

Chaque élément possède deux choix :

présent  
ou  
absent

## Représentation par masque binaire

10110

Chaque bit indique si l’élément correspondant est sélectionné.

C’est une connexion directe entre :

- combinatoire ;
- représentation binaire ;
- algorithmique.

# 41 — BITMASK ET COMBINATOIRE

Pour (n) éléments :

\[ 0mask<2^n \]

permet d’énumérer tous les sous-ensembles.

Applications :

- programmation dynamique ;
- recherche exhaustive ;
- TSP ;
- sélection de fonctionnalités ;
- configuration système ;
- optimisation.

# 42 — BACKTRACKING

Le backtracking construit progressivement une solution.

Schéma :

État initial  
↓  
choix  
↓  
nouvel état  
↓  
choix  
↓  
contrainte violée ?  
↙ ↘  
oui non  
↓ ↓  
retour continuer

## Structure conceptuelle

choose  
explore  
unchoose

# 43 — BACKTRACKING ET ESPACE DE RECHERCHE

Un problème combinatoire peut être représenté comme un arbre de recherche.

départ  
/ | \\  
A B C  
/ \\ ...  
...

Chaque niveau correspond à une décision.

# 44 — PRUNING

Le **pruning** consiste à abandonner une branche lorsqu’on sait qu’elle :

- viole une contrainte ;
- ne peut produire une solution valide ;
- ne peut produire une solution meilleure que la meilleure actuelle.

C’est une idée fondamentale pour rendre une recherche combinatoire praticable.

# 45 — N-QUEENS

Problème classique :

Placer (n) reines sur un échiquier (nn) sans qu’elles ne s’attaquent.

Il illustre :

- backtracking ;
- contraintes ;
- espace de recherche ;
- pruning ;
- représentation combinatoire.

# 46 — GÉNÉRATION DE PERMUTATIONS

Un algorithme récursif peut construire une permutation position par position :

choisir un élément  
↓  
le marquer utilisé  
↓  
choisir le suivant  
↓  
...

Nombre de solutions :

\[ n! \]

# 47 — GÉNÉRATION DE COMBINAISONS

Pour générer des combinaisons de taille (r) :

choisir  
↓  
continuer uniquement avec les éléments suivants

Cela évite de générer plusieurs fois le même ensemble dans des ordres différents.

# 48 — PROGRAMMATION DYNAMIQUE

La programmation dynamique apparaît lorsqu’un problème possède :

1.  des sous-problèmes réutilisables ;
2.  une structure permettant de construire la solution globale à partir de solutions plus petites.

Deux approches :

- mémoïsation ;
- tabulation.

# 49 — COMPTAGE PAR PROGRAMMATION DYNAMIQUE

La programmation dynamique ne sert pas uniquement à trouver une valeur optimale.

Elle peut également compter :

- nombre de chemins ;
- nombre de façons de rendre une somme ;
- nombre de séquences valides ;
- nombre de configurations.

# 50 — EXEMPLE : NOMBRE DE CHEMINS

Dans une grille, si l’on peut uniquement aller :

→  
↓

on peut définir :

\[ dp\[i\]\[j\] = dp\[i-1\]\[j\]+dp\[i\]\[j-1\] \]

Cette relation correspond à un principe de décomposition combinatoire.

# 51 — COIN CHANGE

Le problème du rendu de monnaie peut être posé comme :

De combien de façons peut-on obtenir une somme (S) avec certains types de pièces ?

On peut chercher :

- le nombre de façons ;
- le nombre minimal de pièces.

Le premier est combinatoire.

Le second est un problème d’optimisation.

# 52 — COMPTAGE VS OPTIMISATION

Cette distinction est essentielle.

### Comptage

Combien de solutions existent ?

### Décision

Existe-t-il une solution satisfaisant les contraintes ?

### Optimisation

Quelle est la meilleure solution ?

### Énumération

Quelles sont toutes les solutions ?

Un même problème peut être étudié selon ces quatre angles.

# 53 — OPTIMISATION COMBINATOIRE

L’optimisation combinatoire cherche une meilleure configuration dans un espace discret.

Exemples :

- sac à dos ;
- TSP ;
- scheduling ;
- affectation ;
- coloration ;
- couverture ;
- sélection ;
- routage.

# 54 — PROBLÈME DU SAC À DOS

On dispose d’objets :

\[ i=1,,n \]

avec :

- poids (w_i) ;
- valeur (v_i).

Capacité :

\[ W \]

Objectif :

\[ v_ix_i \]

sous :

\[ w_ix_iW \]

avec :

\[ x_i{0,1} \]

# 55 — PROGRAMMATION ENTIÈRE

Les problèmes combinatoires peuvent être formulés comme des problèmes d’optimisation avec variables entières :

\[ x_iZ \]

ou binaires :

\[ x_i{0,1} \]

Applications :

- planning ;
- affectation ;
- sélection ;
- logistique ;
- réseaux ;
- allocation de ressources.

# 56 — ALGORITHMES GLOUTONS

Un algorithme glouton choisit localement ce qui semble optimal.

Schéma :

choix local  
↓  
choix suivant  
↓  
choix suivant

Les méthodes gloutonnes sont rapides, mais elles ne garantissent pas toujours une solution globale optimale.

# 57 — QUAND LE GLOUTON FONCTIONNE

Pour certains problèmes, une propriété structurelle garantit qu’un choix local peut mener à une solution globale optimale.

Exemples classiques :

- certains problèmes de sélection ;
- arbres couvrants minimaux ;
- codage de Huffman.

# 58 — BRANCH AND BOUND

Branch and Bound combine :

- division de l’espace de recherche ;
- bornes ;
- élimination des branches impossibles ou inutiles.

Schéma :

problème  
/ \\  
P1 P2  
/ \\ / \\  
... ... ... ...

Une borne permet de décider si une branche mérite encore d’être explorée.

# 59 — RECHERCHE EXHAUSTIVE

On teste toutes les possibilités.

Si l’espace contient :

\[ 2^n \]

solutions, le coût peut devenir exponentiel.

Si l’espace contient :

\[ n! \]

solutions, la croissance est encore plus rapide.

# 60 — CROISSANCES COMBINATOIRES

Il faut savoir reconnaître :

\[ O(1) \]

\[ O(n) \]

\[ O(n) \]

\[ O(nn) \]

\[ O(n^2) \]

\[ O(2^n) \]

\[ O(n!) \]

La combinatoire explique pourquoi les dernières classes deviennent rapidement impraticables.

# 61 — EXPLOSION COMBINATOIRE

Un espace de recherche peut croître très rapidement :

n  
↓  
n²  
↓  
n³  
↓  
2ⁿ  
↓  
n!

C’est l’une des raisons fondamentales pour lesquelles l’informatique utilise :

- programmation dynamique ;
- glouton ;
- pruning ;
- approximation ;
- heuristiques ;
- branch and bound.

# 62 — TSP ET OPTIMISATION

Le problème du voyageur de commerce cherche une tournée minimale visitant tous les sommets.

Une approche exhaustive doit considérer un nombre énorme de permutations.

La combinatoire permet de comprendre :

pourquoi l’espace de recherche explose.

Les graphes fournissent la structure.

L’optimisation fournit les méthodes de recherche.

# 63 — COMBINATOIRE ET NP-COMPLÉTUDE

Plusieurs problèmes combinatoires sont difficiles au sens de la théorie de la complexité.

Exemples :

- TSP ;
- clique ;
- coloration ;
- subset sum ;
- vertex cover ;
- SAT.

Il faut alors étudier :

- algorithmes exacts ;
- approximation ;
- heuristiques ;
- paramétrisation ;
- programmation entière.

# 64 — COMBINATOIRE ET PROBABILITÉS

La probabilité discrète repose souvent sur :

\[ P(E)= {} \]

lorsque les cas élémentaires sont équiprobables.

La combinatoire fournit donc directement les outils de comptage nécessaires.

# 65 — VARIABLES ALÉATOIRES DISCRÈTES

Une variable aléatoire discrète peut prendre un ensemble fini ou dénombrable de valeurs.

Exemples :

- nombre de succès ;
- nombre de collisions ;
- nombre de requêtes ;
- nombre de défauts ;
- nombre de sommets visités.

# 66 — DISTRIBUTION BINOMIALE

Pour (n) essais indépendants avec probabilité de succès (p) :

\[ P(X=k) = nk p<sup>k(1-p)</sup>{n-k} \]

La combinaison apparaît parce qu’il faut choisir quelles positions correspondent aux succès.

# 67 — ESPÉRANCE

Pour une variable discrète :

\[ E\[X\] = \_x xP(X=x) \]

L’analyse combinatoire permet souvent de calculer cette somme.

# 68 — COMBINATOIRE ET CRYPTOGRAPHIE

La combinatoire intervient notamment dans :

- espaces de clés ;
- nombre de configurations ;
- sécurité par recherche exhaustive ;
- collisions ;
- structures combinatoires.

Exemple :

Un code de longueur (n) avec (k) symboles possède, si les répétitions sont autorisées :

\[ k^n \]

possibilités.

# 69 — COMBINATOIRE ET SÉCURITÉ

Une question fondamentale peut être :

Combien d’essais sont nécessaires dans le pire cas ?

ou :

Combien de configurations possibles existe-t-il ?

Cela permet d’évaluer la taille d’un espace de recherche.

# 70 — COMBINATOIRE ET TESTS LOGICIELS

Si une application possède :

- 5 navigateurs ;
- 3 systèmes ;
- 4 tailles d’écran ;

le nombre de combinaisons naïves est :

\[ 5=60 \]

La combinatoire aide donc à mesurer l’explosion des cas de test.

# 71 — COMBINATOIRE ET TESTING AVANCÉ

Pour réduire les tests :

- pairwise testing ;
- covering arrays ;
- sélection représentative ;
- contraintes ;
- génération combinatoire.

Objectif :

couvrir un grand nombre d’interactions avec moins de tests que l’énumération exhaustive.

# 72 — COMBINATOIRE ET IA

L’IA explore fréquemment des espaces combinatoires.

Exemples :

Architecture  
↓  
hyperparamètres  
<br/>Planification  
↓  
séquences d'actions  
<br/>Agent  
↓  
séquences d'outils  
<br/>Recherche  
↓  
états possibles  
<br/>Génération  
↓  
séquences possibles

# 73 — RECHERCHE DANS UN ESPACE D’ÉTATS

Un problème peut être représenté comme :

État initial  
↓  
actions possibles  
↓  
nouveaux états  
↓  
actions  
↓  
...

Cela crée un arbre ou un graphe de recherche.

La combinatoire mesure la taille potentielle de cet espace.

# 74 — IA AGENTIQUE ET PLANIFICATION

Un agent peut devoir choisir une séquence :

Action A  
Action B  
Action C  
...

Le nombre de séquences possibles peut exploser.

Les techniques combinatoires permettent de raisonner sur :

- profondeur ;
- branchement ;
- contraintes ;
- pruning ;
- recherche ;
- optimisation.

# 75 — COMBINATOIRE ET GÉNÉRATION

La génération de contenu peut également être vue comme une exploration d’un espace combinatoire.

Exemple :

Sujet  
├── ton  
├── format  
├── structure  
├── vocabulaire  
└── style

Le nombre de configurations possibles peut rapidement devenir très élevé.

# 76 — COMBINATOIRE ET STRUCTURES DE DONNÉES

Les structures de données sont souvent choisies en fonction de la taille de l’espace à explorer.

Exemples :

- bitmask pour sous-ensembles ;
- heap pour choix prioritaires ;
- hash table pour mémoïsation ;
- trie pour espaces de mots ;
- arbre de recherche pour exploration ;
- graphe pour espaces d’états.

# 77 — COMBINATOIRE ET PROGRAMMATION DYNAMIQUE

Une intuition importante :

Si plusieurs branches recalculent les mêmes sous-problèmes, l’arbre combinatoire peut être compressé en graphe de dépendances.

Recherche récursive  
↓  
beaucoup de répétitions  
↓  
mémoïsation  
↓  
sous-problèmes partagés  
↓  
programmation dynamique

C’est une connexion fondamentale entre combinatoire et algorithmique.

# 78 — INVARIANTS COMBINATOIRES

Un invariant est une propriété qui reste vraie pendant une transformation ou une construction.

Exemples :

- nombre de sommets traités ;
- parité ;
- cardinalité ;
- capacité restante ;
- nombre d’éléments sélectionnés.

Les invariants permettent :

- de prouver la correction ;
- de réduire les états ;
- de contrôler une recherche.

# 79 — PARITÉ

La parité est un outil combinatoire extrêmement puissant.

Un entier est :

- pair s’il est divisible par 2 ;
- impair sinon.

Des arguments de parité permettent de prouver l’impossibilité de certaines configurations.

# 80 — INVARIANTS ET IMPOSSIBILITÉ

Une stratégie classique :

supposer qu'une configuration existe  
↓  
identifier un invariant  
↓  
montrer qu'il est incompatible avec la configuration  
↓  
conclure à l'impossibilité

# 81 — COMBINATOIRE ET RÉSEAUX

La combinatoire peut étudier :

- nombre de chemins ;
- nombre de routes ;
- nombre de configurations ;
- nombre de sous-réseaux ;
- nombre de topologies.

Elle complète donc naturellement la théorie des graphes.

# 82 — COMBINATOIRE ET GRAPHES : CARTE

GRAPHE  
│  
┌───────────┼────────────┐  
│ │ │  
chemins cycles arbres  
│ │ │  
└───────────┼────────────┘  
↓  
COMBINATOIRE  
│  
┌──────────┼─────────┐  
│ │ │  
compter générer optimiser

# 83 — COMBINATOIRE ET GÉOMÉTRIE

La géométrie computationnelle produit également des problèmes combinatoires :

- nombre de triangulations ;
- configurations de points ;
- arrangements ;
- intersections ;
- partitions spatiales.

Les structures géométriques peuvent donc être étudiées comme des objets combinatoires.

# 84 — COMBINATOIRE ET GÉOMÉTRIE 3D

Dans un mesh 3D :

vertices  
edges  
faces

on peut étudier :

- nombre de configurations ;
- connectivité ;
- topologie ;
- subdivisions ;
- maillages possibles.

# 85 — OPTIMISATION : MODÈLE GÉNÉRAL

Un problème combinatoire d’optimisation peut être formalisé par :

\[ f(x) \]

sous :

\[ xS \]

où (S) est un ensemble discret de solutions admissibles.

# 86 — ESPACE DES SOLUTIONS

Il faut distinguer :

Espace de recherche  
↓  
toutes les configurations possibles  
<br/>Espace admissible  
↓  
configurations satisfaisant les contraintes  
<br/>Solution optimale  
↓  
meilleure configuration selon l'objectif

Cette distinction est fondamentale.

# 87 — CONTRAINTES

Les contraintes peuvent être :

- binaires ;
- cardinales ;
- temporelles ;
- spatiales ;
- logiques ;
- budgétaires ;
- de capacité ;
- de dépendance.

# 88 — PROGRAMMATION PAR CONTRAINTES

Un problème peut être formulé comme :

Variables  
+  
Domaines  
+  
Contraintes  
+  
Objectif éventuel

Exemple :

x1 ∈ {A,B,C}  
x2 ∈ {A,B,C}  
<br/>contrainte :  
x1 ≠ x2

La combinatoire étudie alors l’espace des affectations possibles.

# 89 — SAT ET COMBINATOIRE

SAT demande si une formule booléenne possède une affectation satisfaisante.

Pour (n) variables booléennes, il existe :

\[ 2^n \]

affectations possibles.

La combinatoire explique directement la taille de l’espace de recherche.

# 90 — CSP

Un **Constraint Satisfaction Problem** comporte :

- variables ;
- domaines ;
- contraintes.

Applications :

- planning ;
- Sudoku ;
- configuration ;
- allocation ;
- scheduling ;
- configuration logicielle.

# 91 — SUDOKU COMME PROBLÈME COMBINATOIRE

Chaque case possède un domaine de valeurs.

variable  
↓  
domaine  
↓  
contraintes

Une recherche naïve explore un grand espace.

Le pruning et les contraintes réduisent drastiquement cet espace.

# 92 — COLORATION COMME CSP

Pour chaque sommet :

\[ color(v){1,,k} \]

avec :

\[ color(u)color(v) \]

pour toute arête ((u,v)).

La coloration est donc également un problème combinatoire de satisfaction de contraintes.

# 93 — ORDRE DES CHOIX

Dans les algorithmes de recherche combinatoire, l’ordre des décisions peut avoir un impact majeur.

Heuristiques classiques :

- choisir la variable la plus contrainte ;
- choisir la valeur la plus prometteuse ;
- explorer d’abord les branches les plus prometteuses.

# 94 — BRANCHEMENT

Si chaque étape possède en moyenne (b) choix et qu’une recherche possède une profondeur (d), le nombre de nœuds peut être de l’ordre de :

\[ O(b^d) \]

Cette relation est fondamentale pour comprendre :

- recherche ;
- IA ;
- jeux ;
- planification ;
- backtracking.

# 95 — COMBINATOIRE ET JEUX

Dans un jeu :

État  
↓  
coups possibles  
↓  
nouveaux états  
↓  
coups possibles

On obtient un arbre de recherche.

Applications :

- minimax ;
- alpha-beta pruning ;
- recherche de coups ;
- planification.

# 96 — ALPHA-BETA ET PRUNING

Dans un arbre de jeu, alpha-beta permet de ne pas explorer certaines branches qui ne peuvent modifier la décision finale.

C’est une application directe du principe :

ne pas explorer ce qui ne peut plus améliorer le résultat.

# 97 — COMBINATOIRE ET BASES DE DONNÉES

Les opérations de jointure peuvent produire de nombreux couples ou tuples.

Pour plusieurs relations :

A JOIN B JOIN C

le nombre de combinaisons potentielles peut devenir très important.

L’optimisation des requêtes consiste notamment à contrôler cet espace.

# 98 — COMBINATOIRE ET SQL

Les concepts utiles comprennent :

- cardinalité ;
- produit cartésien ;
- sélection ;
- projection ;
- jointure ;
- filtrage.

Le produit cartésien correspond directement au principe multiplicatif.

# 99 — COMBINATOIRE ET SYSTÈMES DISTRIBUÉS

Dans un système distribué, les configurations possibles peuvent dépendre de :

- ordre des événements ;
- retards ;
- pannes ;
- messages ;
- états.

Le nombre de scénarios possibles peut rapidement devenir énorme.

La combinatoire aide à raisonner sur ces espaces.

# 100 — COMBINATOIRE ET CONCURRENCE

Deux opérations :

A  
B

peuvent avoir plusieurs ordres d’exécution :

A puis B  
B puis A

Avec davantage d’opérations, le nombre d’ordonnancements augmente rapidement.

Les problèmes de concurrence ont donc une dimension combinatoire forte.

# 101 — SCHEDULING

Le scheduling consiste notamment à affecter :

Tâches  
↓  
machines  
↓  
créneaux

L’espace de solutions peut être combinatoire.

Applications :

- CPU ;
- cloud ;
- CI/CD ;
- production ;
- universités ;
- réseaux.

# 102 — COMBINATOIRE ET CLOUD

Exemples :

- placement de conteneurs ;
- allocation de ressources ;
- répartition de charges ;
- ordonnancement de jobs ;
- sélection de machines.

Les variables sont souvent discrètes.

# 103 — COMBINATOIRE ET ARCHITECTURE LOGICIELLE

Choisir une architecture peut parfois être formulé comme une sélection parmi plusieurs configurations :

services  
+  
technologies  
+  
réplication  
+  
placement  
+  
dépendances

La combinatoire permet d’évaluer la taille de l’espace des configurations.

# 104 — COMBINATOIRE ET IA : HYPERPARAMÈTRES

Si :

learning rate : 5 choix  
batch size : 4 choix  
optimizer : 3 choix  
architecture : 6 choix

alors une recherche exhaustive peut comporter :

\[ 5 \]

configurations.

C’est une forme simple d’espace combinatoire.

# 105 — GRID SEARCH

La recherche en grille teste systématiquement des combinaisons de paramètres.

Avantage :

- simple ;
- exhaustive sur la grille choisie.

Inconvénient :

- nombre de configurations pouvant exploser.

# 106 — RANDOM SEARCH

Au lieu d’explorer toutes les configurations, on en échantillonne certaines.

Cela réduit le coût au prix d’une couverture différente de l’espace.

# 107 — COMBINATOIRE ET RECHERCHE D’ARCHITECTURE

Dans Neural Architecture Search, les architectures possibles peuvent former un immense espace combinatoire.

On peut rechercher :

- nombre de couches ;
- types de couches ;
- connexions ;
- tailles ;
- hyperparamètres.

# 108 — COMBINATOIRE ET GÉNÉRATION DE DONNÉES

La génération de données synthétiques peut utiliser :

- permutations ;
- combinaisons ;
- contraintes ;
- distributions ;
- échantillonnage.

# 109 — COMPLEXITÉ DES ESPACES COMBINATOIRES

| Structure | Taille typique |
| --- | --- |
| Sous-ensembles de (n) éléments | (2^n) |
| Permutations de (n) éléments | (n!) |
| Combinaisons de (r) parmi (n) | (nr) |
| Chaînes de longueur (n) sur alphabet (k) | (k^n) |
| Affectations booléennes de (n) variables | (2^n) |
| Arbres étiquetés sur (n) sommets | (n^{n-2}) |

Cette table doit devenir un réflexe de reconnaissance.

# 110 — ALGORITHMES COMBINATOIRES À CONNAÎTRE

## Fondamentaux

- génération de sous-ensembles ;
- génération de permutations ;
- génération de combinaisons ;
- backtracking ;
- récursion.

## Intermédiaires

- programmation dynamique ;
- mémoïsation ;
- bitmask DP ;
- branch and bound ;
- glouton.

## Avancés

- programmation entière ;
- algorithmes d’approximation ;
- recherche locale ;
- métaheuristiques ;
- algorithmes paramétrés.

# 111 — STRUCTURES DE DONNÉES ASSOCIÉES

- tableaux ;
- piles ;
- files ;
- arbres ;
- graphes ;
- heaps ;
- hash tables ;
- bitsets ;
- bitmasks ;
- Union-Find ;
- structures de mémoïsation.

# 112 — COMPLEXITÉS À RECONNAÎTRE

La combinatoire exige de savoir identifier immédiatement :

\[ O(n!) \]

\[ O(2^n) \]

\[ O(n^k) \]

\[ O(nr) \]

ainsi que les différences entre :

- polynomial ;
- exponentiel ;
- factoriel.

# 113 — APPROCHES POUR RÉDUIRE L’EXPLOSION COMBINATOIRE

Face à un espace énorme :

### 1\. Éliminer les solutions impossibles

→ contraintes.

### 2\. Fusionner les sous-problèmes identiques

→ programmation dynamique.

### 3\. Éviter les branches inutiles

→ pruning.

### 4\. Utiliser une borne

→ branch and bound.

### 5\. Exploiter une propriété structurelle

→ glouton.

### 6\. Accepter une approximation

→ approximation.

### 7\. Échantillonner

→ randomisation.

### 8\. Exploiter le parallélisme

→ calcul distribué / GPU lorsque pertinent.

# 114 — PROPRIÉTÉS ET THÉORÈMES À RETENIR

## Propriété 1 — Produit

\[ n_1n_2n_k \]

## Propriété 2 — Somme

Pour des cas disjoints :

\[ n_1+n_2++n_k \]

## Propriété 3 — Factorielle

\[ n!=n(n-1)! \]

## Propriété 4 — Arrangement

\[ A(n,r)= \]

## Propriété 5 — Combinaison

\[ nr = \]

## Propriété 6 — Symétrie

\[ nr=n{n-r} \]

## Propriété 7 — Pascal

\[ nr =

- \]

## Propriété 8 — Sous-ensembles

\[ |P(A)|=2^{|A|} \]

## Propriété 9 — Cayley

\[ n^{n-2} \]

arbres étiquetés sur (n) sommets.

## Propriété 10 — Catalan

\[ C_n= \]

# 115 — DISTINCTIONS CONCEPTUELLES À MAÎTRISER

Il faut absolument distinguer :

Permutation  
vs  
Arrangement

Arrangement  
vs  
Combinaison

Composition  
vs  
Partition

Comptage  
vs  
Énumération

Énumération  
vs  
Optimisation

Recherche exhaustive  
vs  
Backtracking

Backtracking  
vs  
Programmation dynamique

Glouton  
vs  
Optimisation exacte

Maximum  
vs  
Maximal

# 116 — ERREURS CLASSIQUES

## Erreur 1

Utiliser une combinaison alors que l’ordre compte.

## Erreur 2

Utiliser un arrangement alors que l’ordre ne compte pas.

## Erreur 3

Oublier les répétitions.

## Erreur 4

Compter deux fois la même configuration.

## Erreur 5

Ne pas traiter les cas d’intersection.

## Erreur 6

Confondre partition et composition.

## Erreur 7

Explorer tout un espace (2^n) ou (n!) sans analyser sa taille.

## Erreur 8

Utiliser un algorithme glouton sans preuve de sa validité.

## Erreur 9

Confondre :

nombre de solutions

et :

meilleure solution

# 117 — MÉTHODE DE RÉSOLUTION D’UN PROBLÈME COMBINATOIRE

Face à un problème :

## Étape 1 — Identifier les objets

Que manipule-t-on ?

## Étape 2 — Identifier les choix

Quelles décisions sont possibles ?

## Étape 3 — Déterminer si l’ordre compte

Question centrale.

## Étape 4 — Déterminer les répétitions

Peut-on réutiliser un élément ?

## Étape 5 — Identifier les contraintes

Que doit respecter une solution ?

## Étape 6 — Déterminer l’objectif

Cherche-t-on :

- un nombre ?
- toutes les solutions ?
- une solution quelconque ?
- une solution optimale ?

## Étape 7 — Estimer la taille de l’espace

Calculer ou approximer :

\[ |S| \]

## Étape 8 — Choisir une stratégie

- formule ;
- récurrence ;
- backtracking ;
- DP ;
- glouton ;
- branch and bound ;
- approximation.

# 118 — FICHES INDIVIDUELLES À DÉVELOPPER ULTÉRIEUREMENT

Le document F constitue la cartographie générale.

Il peut être décliné en fiches spécialisées :

### F1 — Principes fondamentaux de comptage

### F2 — Principe additif

### F3 — Principe multiplicatif

### F4 — Factorielle

### F5 — Permutations

### F6 — Arrangements

### F7 — Arrangements avec répétition

### F8 — Combinaisons

### F9 — Combinaisons avec répétition

### F10 — Triangle de Pascal

### F11 — Coefficients binomiaux

### F12 — Binôme de Newton

### F13 — Principe des tiroirs

### F14 — Bijections

### F15 — Double comptage

### F16 — Inclusion-exclusion

### F17 — Dérangements

### F18 — Étoiles et barres

### F19 — Compositions d’entiers

### F20 — Partitions d’entiers

### F21 — Récurrences

### F22 — Résolution des récurrences

### F23 — Théorème maître

### F24 — Fonctions génératrices

### F25 — Fonctions génératrices exponentielles

### F26 — Nombres de Catalan

### F27 — Nombres de Stirling

### F28 — Nombres de Bell

### F29 — Énumération combinatoire

### F30 — Génération de sous-ensembles

### F31 — Bitmask

### F32 — Génération de permutations

### F33 — Génération de combinaisons

### F34 — Backtracking

### F35 — Pruning

### F36 — N-Queens

### F37 — Programmation dynamique

### F38 — DP de comptage

### F39 — Bitmask DP

### F40 — Branch and Bound

### F41 — Algorithmes gloutons

### F42 — Optimisation combinatoire

### F43 — Programmation entière

### F44 — CSP

### F45 — SAT et combinatoire

### F46 — Probabilités combinatoires

### F47 — Distribution binomiale

### F48 — Espérance et dénombrement

### F49 — Combinatoire des graphes

### F50 — Théorème de Cayley

### F51 — Coloration et combinatoire

### F52 — Couplages et dénombrement

### F53 — Flots et structures combinatoires

### F54 — TSP

### F55 — Knapsack

### F56 — Scheduling

### F57 — Combinatoire des systèmes distribués

### F58 — Combinatoire des bases de données

### F59 — Combinatoire pour le testing

### F60 — Combinatoire pour l’IA

### F61 — Espaces d’états

### F62 — Planification combinatoire

### F63 — Recherche dans les espaces combinatoires

### F64 — Hyperparamètres et recherche de configurations

### F65 — Neural Architecture Search

### F66 — Combinatoire et IA agentique

### F67 — Combinatoire et jeux

### F68 — Minimax et recherche

### F69 — Alpha-beta pruning

### F70 — Approximation combinatoire

### F71 — Recherche locale

### F72 — Métaheuristiques

### F73 — Randomisation

### F74 — Algorithmes paramétrés

### F75 — Complexité des espaces combinatoires

# 119 — PROJETS PRATIQUES DE MAÎTRISE

## Projet F1 — Combinatorial Explorer

Créer une interface permettant de générer :

- permutations ;
- combinaisons ;
- sous-ensembles ;
- arrangements.

Afficher :

- nombre total ;
- objets générés ;
- temps ;
- mémoire.

## Projet F2 — Backtracking Visualizer

Créer un visualiseur montrant l’arbre de recherche.

Afficher :

exploration  
↓  
contrainte  
↓  
pruning  
↓  
retour

## Projet F3 — N-Queens Solver

Comparer :

- recherche exhaustive ;
- backtracking ;
- pruning ;
- heuristiques.

## Projet F4 — Scheduling Optimizer

Créer un problème d’affectation :

Tâches  
↓  
Machines  
↓  
Créneaux

Comparer plusieurs stratégies.

## Projet F5 — Knapsack Lab

Comparer :

- force brute ;
- glouton ;
- programmation dynamique ;
- branch and bound.

## Projet F6 — TSP Explorer

Comparer :

- brute force ;
- nearest neighbor ;
- recherche locale ;
- programmation dynamique sur petit (n).

## Projet F7 — Constraint Solver

Construire un petit moteur CSP :

Variables  
+  
Domaines  
+  
Contraintes

avec :

- backtracking ;
- propagation ;
- heuristique de sélection.

## Projet F8 — Combinatorial Testing Generator

Créer un outil générant des jeux de tests couvrant certaines interactions entre paramètres.

## Projet F9 — Hyperparameter Search

Construire une interface permettant de comparer :

- grid search ;
- random search ;
- recherche guidée.

## Projet F10 — Agent Planning Lab

Créer un petit agent explorant un espace d’états et comparer :

- recherche exhaustive ;
- BFS ;
- DFS ;
- A\* ;
- pruning.

# 120 — EXERCICES PROGRESSIFS

## Niveau 1 — Comptage

Calculer :

- sommes ;
- produits ;
- factorielles ;
- arrangements ;
- combinaisons.

## Niveau 2 — Reconnaissance

Pour chaque problème :

ordre important ou non ?

répétition ou non ?

## Niveau 3 — Preuves

Démontrer :

\[ nr=n{n-r} \]

par plusieurs méthodes.

## Niveau 4 — Récurrences

Construire une récurrence pour un problème de comptage.

## Niveau 5 — Génération

Implémenter :

- permutations ;
- combinaisons ;
- sous-ensembles.

## Niveau 6 — Recherche

Implémenter :

- backtracking ;
- pruning.

## Niveau 7 — Optimisation

Comparer :

- exhaustive ;
- glouton ;
- DP ;
- branch and bound.

## Niveau 8 — Modélisation

Transformer un problème réel en :

espace de solutions  
+  
contraintes  
+  
fonction objectif

# 121 — CHALLENGES SANS IA

## Challenge 1

Expliquer sans formule la différence entre permutation, arrangement et combinaison.

## Challenge 2

Retrouver les formules à partir du principe multiplicatif.

## Challenge 3

Démontrer une identité binomiale par bijection.

## Challenge 4

Construire une récurrence de comptage.

## Challenge 5

Écrire un générateur de permutations.

## Challenge 6

Écrire un générateur de combinaisons.

## Challenge 7

Résoudre N-Queens avec backtracking.

## Challenge 8

Ajouter du pruning.

## Challenge 9

Mesurer l’explosion du nombre d’états.

## Challenge 10

Choisir une méthode d’optimisation sans assistance.

# 122 — CHALLENGES AVEC IA

L’IA peut être utilisée comme :

- vérificateur ;
- générateur de cas limites ;
- critique ;
- générateur de problèmes ;
- comparateur d’approches.

Exemple :

« Voici mon raisonnement combinatoire. Trouve uniquement les hypothèses non justifiées. »

Puis :

« Donne-moi cinq problèmes similaires mais plus difficiles. »

Puis :

« Compare ma solution exhaustive avec une approche dynamique sans réécrire mon code. »

L’objectif reste de conserver la capacité de résoudre le problème sans l’IA.

# 123 — CONNEXIONS AVEC LES DOMAINES PRÉCÉDENTS

## Domaine A — Logique

La combinatoire utilise :

- propositions ;
- quantificateurs ;
- contraintes ;
- preuves ;
- implications.

## Domaine B — Théorie des nombres

Connexions avec :

- coefficients binomiaux ;
- divisibilité ;
- congruences ;
- arithmétique modulaire ;
- fonctions arithmétiques.

## Domaine C — Algèbre linéaire

Connexions avec :

- matrices ;
- systèmes ;
- graphes ;
- programmation linéaire ;
- optimisation.

## Domaine D — Géométrie computationnelle

Connexions avec :

- triangulations ;
- arrangements ;
- configurations ;
- meshes ;
- structures spatiales.

## Domaine E — Théorie des graphes

Connexion particulièrement forte :

Graphes  
↓  
structures  
↓  
comptage  
↓  
énumération  
↓  
optimisation

# 124 — CARTE DES RELATIONS ENTRE E ET F

THÉORIE DES GRAPHES  
│  
┌────────────┼────────────┐  
│ │ │  
chemins arbres colorations  
│ │ │  
└────────────┼────────────┘  
↓  
COMBINATOIRE  
│  
┌───────────────┼────────────────┐  
│ │ │  
compter générer optimiser  
│ │ │  
↓ ↓ ↓  
formules backtracking DP / greedy  
récurrences pruning B&B  
bijections énumération approximation

# 125 — CARTE MENTALE GLOBALE DU DOMAINE F

COMBINATOIRE  
│  
┌──────────────────────┼──────────────────────┐  
│ │ │  
COMPTER CONSTRUIRE OPTIMISER  
│ │ │  
┌─────┼─────┐ ┌─────┼─────┐ ┌─────┼─────┐  
│ │ │ │ │ │ │ │ │  
Somme Produit Binôme Perm. Comb. Sous-Ens. DP Greedy B&B  
│ │ │ │ │ │ │ │ │  
└─────┴─────┴──────────┴─────┴─────┴─────────┴─────┴─────┘  
│  
STRUCTURES  
│  
┌─────────────────┼────────────────┐  
│ │ │  
Graphes Arbres Partitions  
│ │ │  
└─────────────────┼────────────────┘  
↓  
ALGORITHMIQUE  
│  
┌─────────────────┼─────────────────┐  
│ │ │  
IA Systèmes Web  
│ │ │  
recherche scheduling testing  
planning allocation config  
agents optimisation données

# 126 — CRITÈRE DE MAÎTRISE DU DOMAINE F

La maîtrise de la combinatoire ne consiste pas à mémoriser une liste de formules.

Elle consiste à reconnaître la structure cachée derrière un problème.

Face à une question :

Combien ?

il faut être capable de rechercher :

Addition ?  
Multiplication ?  
Permutation ?  
Arrangement ?  
Combinaison ?  
Répétition ?  
Complément ?  
Inclusion-exclusion ?  
Bijection ?  
Récurrence ?  
Fonction génératrice ?

Face à une question :

Comment générer ?

penser :

récursion  
backtracking  
pruning  
énumération

Face à :

Quelle est la meilleure ?

penser :

optimisation  
DP  
glouton  
branch and bound  
approximation  
heuristique

Face à :

Combien de possibilités ?

penser immédiatement :

taille de l'espace  
↓  
complexité  
↓  
explosion combinatoire

# 127 — CHECKLIST FINALE DE MAÎTRISE

## Comptage

- principe additif ;
- principe multiplicatif ;
- complément ;
- partition ;
- double comptage ;
- bijection ;
- principe des tiroirs.

## Formules

- factorielle ;
- permutation ;
- arrangement ;
- combinaison ;
- répétition ;
- coefficient binomial ;
- triangle de Pascal ;
- binôme de Newton.

## Structures

- ensembles ;
- sous-ensembles ;
- suites ;
- mots ;
- permutations ;
- partitions ;
- compositions ;
- arbres ;
- graphes.

## Récurrences

- construire une récurrence ;
- résoudre une récurrence simple ;
- reconnaître une récursivité algorithmique ;
- utiliser le théorème maître lorsque pertinent.

## Énumération

- générer les sous-ensembles ;
- générer les permutations ;
- générer les combinaisons ;
- utiliser les bitmasks ;
- backtracking ;
- pruning.

## Optimisation

- programmation dynamique ;
- glouton ;
- branch and bound ;
- programmation entière ;
- approximation ;
- heuristiques.

## Contraintes

- CSP ;
- SAT ;
- N-Queens ;
- coloration ;
- scheduling.

## Complexité

- (n!) ;
- (2^n) ;
- (n^k) ;
- (nr) ;
- explosion combinatoire.

## Applications

- graphes ;
- systèmes ;
- réseaux ;
- bases de données ;
- Web ;
- testing ;
- cryptographie ;
- IA ;
- agents ;
- jeux ;
- optimisation.

# 128 — SYNTHÈSE ULTIME

Le domaine F peut être résumé par cette chaîne :

ENSEMBLES  
↓  
CHOIX  
↓  
COMPTAGE  
↓  
CONFIGURATIONS  
↓  
STRUCTURES DISCRÈTES  
↓  
RÉCURRENCES  
↓  
ÉNUMÉRATION  
↓  
ESPACE DE RECHERCHE  
↓  
CONTRAINTES  
↓  
OPTIMISATION  
↓  
ALGORITHMES  
↓  
SYSTÈMES  
↓  
IA

La combinatoire fournit ainsi le langage mathématique permettant de comprendre **combien de possibilités existent, comment elles sont structurées, comment les générer et comment chercher efficacement parmi elles**.

Elle est donc directement reliée à :

- l’algorithmique ;
- la théorie de la complexité ;
- la théorie des graphes ;
- la programmation dynamique ;
- l’optimisation ;
- les probabilités discrètes ;
- la recherche ;
- les systèmes ;
- l’IA ;
- les jeux ;
- les bases de données ;
- la sécurité informatique.

# 129 — POSITION DANS LA CARTOGRAPHIE GLOBALE

A — Logique et fondements  
B — Théorie des nombres  
C — Algèbre linéaire / géométrie linéaire  
D — Géométrie computationnelle  
E — Théorie des graphes et algorithmes sur les graphes  
F — Combinatoire et optimisation combinatoire  
↓  
G — \[Domaine mathématique suivant\]

## DOMAINE F — IDÉE CENTRALE

**La combinatoire étudie les possibilités discrètes : les compter, les construire, les organiser, les contraindre et, lorsque leur nombre devient immense, trouver efficacement une solution sans avoir à toutes les parcourir.**

Cette idée constitue le lien naturel entre les mathématiques discrètes et l’algorithmique moderne.