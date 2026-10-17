# DOCUMENT K — FRACTALES, CHAOS & SYSTÈMES DYNAMIQUES

**Référence mathématique, algorithmique et informatique pour la génération procédurale, les simulations, les systèmes dynamiques, le rendu graphique et les expériences interactives**

**Version : 1.0**

# 00 — PRÉDISPOSITION D’INTÉGRATION

Ce document constitue la référence du **Domaine K — Fractales, Chaos & Systèmes Dynamiques**.

Il doit être consulté lorsqu’un problème implique notamment :

- des formes auto-similaires ;
- des structures récursives ;
- des motifs générés par répétition ;
- des systèmes qui évoluent dans le temps ;
- des comportements émergents ;
- des attracteurs ;
- des bifurcations ;
- une forte sensibilité aux conditions initiales ;
- des phénomènes pseudo-aléatoires ou chaotiques ;
- du bruit procédural ;
- de la génération procédurale ;
- des terrains ;
- des nuages ;
- des textures ;
- de la végétation ;
- des particules ;
- des simulations ;
- des effets graphiques ;
- des visualisations scientifiques ;
- des environnements virtuels ;
- des systèmes interactifs évolutifs.

L’objectif n’est pas seulement de connaître le vocabulaire.

Le système doit pouvoir suivre la chaîne :

PHÉNOMÈNE / BESOIN  
↓  
CONCEPT MATHÉMATIQUE  
↓  
RÈGLE OU ÉQUATION  
↓  
PROCESSUS ITÉRATIF / PROCÉDURAL  
↓  
REPRÉSENTATION NUMÉRIQUE  
↓  
ALGORITHME  
↓  
PARAMÈTRES  
↓  
VISUALISATION / SIMULATION  
↓  
APPLICATION LOGICIELLE

Lorsqu’un besoin créatif apparaît, l’IA doit également rechercher si plusieurs familles peuvent être combinées.

Par exemple :

Fractale  
+  
Bruit procédural  
+  
Système dynamique  
+  
Particules  
+  
Shader  
\=  
Environnement visuel génératif

ou :

Système dynamique  
+  
Contrôle utilisateur  
+  
Visualisation temps réel  
\=  
Expérience interactive

Le document doit donc être utilisé comme une **base de raisonnement et de conception**, et non comme une simple liste de définitions.

# 01 — IDENTITÉ DU DOMAINE

Le Domaine K étudie principalement trois grandes familles :

FRACTALES  
│  
├── structures auto-similaires  
├── récursivité  
├── itérations  
├── dimensions non entières  
└── géométrie complexe  
<br/>CHAOS  
│  
├── déterminisme  
├── sensibilité aux conditions initiales  
├── instabilité  
├── bifurcations  
├── attracteurs étranges  
└── comportement apparemment aléatoire  
<br/>SYSTÈMES DYNAMIQUES  
│  
├── état  
├── évolution temporelle  
├── équations différentielles  
├── systèmes discrets  
├── stabilité  
├── trajectoires  
└── attracteurs

À cela s’ajoute une quatrième couche particulièrement importante pour l’informatique :

GÉNÉRATION PROCÉDURALE  
│  
├── bruit  
├── fonctions déterministes  
├── champs scalaires  
├── règles locales  
├── récursivité  
├── interpolation  
└── composition multi-échelle

Ces familles sont liées mais doivent être distinguées.

# 02 — DISTINCTION FONDAMENTALE : FRACTALE ≠ BRUIT PROCÉDURAL

Cette distinction est essentielle pour éviter une confusion fréquente dans les projets graphiques.

## 02.1 — Fractale

Une fractale désigne généralement une structure caractérisée par une complexité produite par des règles souvent itératives, récursives ou auto-similaires.

Exemples :

- ensemble de Mandelbrot ;
- ensembles de Julia ;
- triangle de Sierpiński ;
- courbe de Koch ;
- flocon de Koch ;
- courbe du dragon ;
- courbe de Hilbert ;
- courbe de Peano ;
- arbres fractals.

La fractale répond principalement à une logique de :

RÈGLE  
↓  
RÉPÉTITION  
↓  
TRANSFORMATION  
↓  
STRUCTURE

## 02.2 — Bruit procédural

Un bruit procédural est une fonction ou un champ numérique permettant de produire une variation contrôlée, généralement continue ou suffisamment régulière pour générer :

- relief ;
- texture ;
- nuages ;
- déformation ;
- turbulence visuelle ;
- végétation ;
- déplacement ;
- animation ;
- variation de couleur.

Le bruit répond plutôt à une logique de :

COORDONNÉES  
↓  
FONCTION  
↓  
VALEUR  
↓  
INTERPOLATION / COMPOSITION  
↓  
STRUCTURE VISUELLE

## 02.3 — Ils peuvent être combinés

Une fractale peut utiliser du bruit.

Un bruit peut produire une structure visuellement fractale.

Mais :

**tout bruit n’est pas une fractale, et toute fractale n’est pas du bruit.**

Exemple :

Perlin Noise

est un procédé de génération de variation spatiale.

Mandelbrot

est un ensemble fractal défini par une dynamique itérative complexe.

Ils peuvent produire tous deux des images complexes, mais leur fondement mathématique n’est pas le même.

# 03 — PLACE DU DOMAINE K DANS LA PILE MATHÉMATIQUE

Les domaines précédents apportent les outils fondamentaux nécessaires.

A — Logique  
↓  
B — Nombres  
↓  
C — Algèbre linéaire  
↓  
D — Géométrie  
↓  
E — Graphes  
↓  
F — Combinatoire  
↓  
G — Probabilités  
↓  
H — Statistiques  
↓  
I — Calcul différentiel  
↓  
J — Optimisation  
↓  
K — Fractales, Chaos & Systèmes dynamiques

Le Domaine K utilise particulièrement :

- les nombres complexes ;
- les fonctions ;
- les vecteurs ;
- les matrices ;
- les transformations géométriques ;
- les dérivées ;
- les équations différentielles ;
- l’itération ;
- les probabilités et le bruit ;
- les méthodes numériques ;
- l’optimisation.

# 04 — CARTOGRAPHIE GÉNÉRALE

Le domaine peut être organisé en neuf familles.

## Famille A — Géométrie fractale

- auto-similarité ;
- récursivité ;
- fractales déterministes ;
- fractales aléatoires ;
- dimension fractale ;
- fractales géométriques ;
- fractales complexes.

## Famille B — Systèmes itératifs

- suites ;
- fonctions itérées ;
- systèmes dynamiques discrets ;
- IFS ;
- L-systems.

## Famille C — Fractales complexes

- nombres complexes ;
- Mandelbrot ;
- Julia ;
- dynamique complexe ;
- ensembles de points bornés ;
- orbites.

## Famille D — Systèmes dynamiques

- états ;
- trajectoires ;
- équations différentielles ;
- systèmes discrets ;
- stabilité ;
- attracteurs.

## Famille E — Chaos

- sensibilité ;
- mélange ;
- bifurcation ;
- exposant de Lyapunov ;
- attracteurs étranges ;
- chaos déterministe.

## Famille F — Bruit procédural

- bruit ;
- interpolation ;
- gradients ;
- Perlin ;
- Simplex ;
- Value Noise ;
- Worley / Cellular Noise ;
- FBM ;
- turbulence ;
- domain warping.

## Famille G — Génération procédurale

- terrains ;
- végétation ;
- structures ;
- environnements ;
- textures ;
- nuages ;
- systèmes naturels.

## Famille H — Simulation

- physique ;
- particules ;
- fluides ;
- systèmes biologiques ;
- phénomènes dynamiques.

## Famille I — Rendu et interaction

- shaders ;
- GPU ;
- WebGL ;
- Three.js ;
- visualisation ;
- animation ;
- expériences interactives.

# 05 — VOCABULAIRE ESSENTIEL

## 05.1 — Itération

Application répétée d’une fonction.

\[ x_{n+1}=f(x_n) \]

## 05.2 — Orbite

Suite des états successifs :

\[ x_0, x_1, x_2, \]

avec :

\[ x_{n+1}=f(x_n) \]

## 05.3 — État

Information suffisante pour décrire le système à un instant donné.

On peut représenter l’état par :

\[ x(t) \]

ou, dans un système discret :

\[ x_n \]

## 05.4 — Trajectoire

Évolution de l’état au cours du temps.

État initial  
↓  
État 1  
↓  
État 2  
↓  
État 3  
↓  
...

## 05.5 — Attracteur

Ensemble vers lequel certaines trajectoires convergent ou restent confinées.

## 05.6 — Bifurcation

Modification qualitative du comportement d’un système lorsque l’on fait varier un paramètre.

## 05.7 — Chaos déterministe

Comportement complexe produit par des règles déterministes.

Il n’est donc pas nécessaire d’avoir une source aléatoire pour obtenir un comportement apparemment imprévisible.

## 05.8 — Auto-similarité

Propriété selon laquelle une structure présente des motifs similaires à différentes échelles.

## 05.9 — Dimension fractale

Mesure permettant de caractériser la complexité ou la manière dont un objet occupe l’espace.

Elle peut ne pas être entière.

## 05.10 — Bruit

Fonction ou processus produisant une variation structurée ou aléatoire selon le modèle utilisé.

# 06 — FRACTALES : CONCEPT FONDAMENTAL

Une fractale peut être comprise comme une structure dont la complexité est générée par une règle relativement simple.

Le principe général est :

STRUCTURE INITIALE  
↓  
RÈGLE  
↓  
TRANSFORMATION  
↓  
RÉPÉTITION  
↓  
COMPLEXITÉ

La puissance informatique des fractales vient précisément de cette propriété :

une description extrêmement compacte peut générer une structure visuelle extrêmement riche.

Cela permet :

- génération à la demande ;
- absence de stockage d’un modèle complet ;
- variation paramétrique ;
- génération infinie ou quasi infinie ;
- niveaux de détail ;
- zoom ;
- exploration interactive.

# 07 — AUTO-SIMILARITÉ

## 07.1 — Définition intuitive

Une structure est auto-similaire lorsqu’une partie ressemble au tout, au moins approximativement ou statistiquement.

Exemple conceptuel :

Objet  
├── motif  
│ ├── motif  
│ │ └── motif  
│ └── motif  
└── motif

## 07.2 — Auto-similarité exacte

Une transformation reproduit exactement une structure réduite de l’ensemble.

Exemple :

- triangle de Sierpiński ;
- certaines constructions de Koch.

## 07.3 — Auto-similarité approximative

La structure présente des caractéristiques similaires sans être strictement identique.

Elle est fréquente dans :

- terrains naturels ;
- nuages ;
- végétation ;
- montagnes ;
- phénomènes naturels.

## 07.4 — Auto-similarité statistique

La structure possède des propriétés statistiques similaires à plusieurs échelles.

Cette idée est particulièrement importante pour :

- bruit fractal ;
- terrain procédural ;
- textures ;
- phénomènes naturels.

# 08 — FRACTALES DÉTERMINISTES ET ALÉATOIRES

## 08.1 — Fractale déterministe

La règle produit toujours exactement la même structure pour les mêmes paramètres.

Exemple :

\[ Mandelbrot(c) \]

ou une construction récursive de Sierpiński.

## 08.2 — Fractale stochastique

Une composante aléatoire intervient.

Deux générations peuvent donc être différentes tout en conservant les mêmes propriétés statistiques.

Cette approche est très utile pour :

- paysages ;
- nuages ;
- végétation ;
- textures ;
- environnements.

# 09 — FRACTALE DE MANDELBROT

L’ensemble de Mandelbrot est défini à partir de l’itération :

\[ z_{n+1}=z_n^2+c \]

avec :

\[ z_0=0 \]

où (z) et (c) sont des nombres complexes.

Pour chaque valeur de (c), on observe le comportement de l’orbite.

Si :

\[ |z_n| \]

reste borné, le point est associé à l’ensemble.

Si la valeur diverge, le point est considéré comme extérieur.

## 09.1 — Principe informatique

Pour chaque pixel :

pixel  
↓  
coordonnée complexe c  
↓  
z = 0  
↓  
itération  
↓  
test de divergence  
↓  
nombre d'itérations  
↓  
couleur

## 09.2 — Pseudocode conceptuel

pour chaque pixel :  
convertir pixel → c  
<br/>z = 0  
iteration = 0  
<br/>tant que |z| ≤ seuil  
et iteration < maxIterations :  
<br/>z = z² + c  
iteration += 1  
<br/>attribuer une couleur

## 09.3 — Applications

- visualisation mathématique ;
- art génératif ;
- exploration interactive ;
- zoom fractal ;
- shaders ;
- expériences WebGL ;
- génération de textures ;
- démonstration de systèmes dynamiques complexes.

# 10 — ENSEMBLES DE JULIA

Les ensembles de Julia utilisent une dynamique similaire :

\[ z_{n+1}=z_n^2+c \]

mais (c) est fixé tandis que la valeur initiale (z_0) varie.

Ainsi :

Mandelbrot  
→ on explore c  
<br/>Julia  
→ on fixe c et on explore z₀

Cette relation est fondamentale.

## 10.1 — Génération

Pour chaque point initial :

\[ z_0=x+iy \]

on applique :

\[ z_{n+1}=z_n^2+c \]

puis on étudie l’orbite.

## 10.2 — Applications

- art génératif ;
- visualisation ;
- animation paramétrique ;
- exploration de l’espace des paramètres ;
- shaders ;
- génération de motifs.

# 11 — TRIANGLE DE SIERPIŃSKI

Le triangle de Sierpiński est obtenu par subdivision récursive.

Principe :

Triangle  
↓  
division en 4 triangles  
↓  
suppression du triangle central  
↓  
répétition sur les triangles restants

La structure peut être générée récursivement.

## 11.1 — Algorithme conceptuel

fonction sierpinski(A, B, C, profondeur):  
<br/>si profondeur = 0 :  
dessiner triangle  
retourner  
<br/>calculer AB  
calculer AC  
calculer BC  
<br/>sierpinski(A, AB, AC, profondeur - 1)  
sierpinski(AB, B, BC, profondeur - 1)  
sierpinski(AC, BC, C, profondeur - 1)

## 11.2 — Complexité

Le nombre de triangles croît exponentiellement avec la profondeur.

Il faut donc contrôler :

- profondeur ;
- nombre de primitives ;
- mémoire ;
- temps de rendu.

# 12 — COURBE ET FLOCON DE KOCH

La courbe de Koch est construite en remplaçant chaque segment par une séquence de segments.

Règle conceptuelle :

────  
↓  
─╱╲─

Plus précisément, un segment est divisé en trois parties puis la partie centrale est remplacée par deux segments formant un triangle.

La transformation est répétée récursivement.

## 12.1 — Flocon de Koch

Trois courbes de Koch peuvent être combinées pour former le flocon.

## 12.2 — Intérêt informatique

La construction illustre parfaitement :

géométrie  
+  
récursivité  
+  
transformation  
+  
génération procédurale

Elle peut servir de base à :

- génération de motifs ;
- géométrie procédurale ;
- visualisation ;
- apprentissage algorithmique.

# 13 — DRAGON CURVE

La courbe du dragon est une fractale construite par une règle récursive ou par des substitutions.

Elle est particulièrement intéressante pour étudier :

- récursivité ;
- systèmes de réécriture ;
- auto-similarité ;
- géométrie discrète ;
- L-systems.

Elle constitue également un exemple utile de transformation d’une chaîne de règles en géométrie.

# 14 — COURBES DE HILBERT ET DE PEANO

Les courbes de Hilbert et de Peano sont particulièrement importantes car elles explorent une idée surprenante :

construire une courbe unidimensionnelle capable de remplir progressivement une région bidimensionnelle.

Elles sont utiles pour comprendre :

- espace ;
- parcours ;
- récursivité ;
- subdivision ;
- indexation spatiale ;
- locality-preserving curves.

## 14.1 — Applications informatiques

Elles peuvent être utilisées ou étudiées pour :

- parcours de grilles ;
- indexation spatiale ;
- cache locality ;
- visualisation ;
- compression ;
- génération procédurale ;
- organisation de données spatiales.

# 15 — L-SYSTEMS

Les **L-systems**, ou systèmes de Lindenmayer, sont des systèmes formels de réécriture.

Ils sont particulièrement importants pour la génération procédurale de structures naturelles.

## 15.1 — Principe

Un système contient :

- un alphabet ;
- un axiome ;
- des règles de production.

Exemple :

Axiome :  
F  
<br/>Règle :  
F → F+F−F−F+F

Chaque itération remplace les symboles selon les règles.

## 15.2 — Passage de symboles à géométrie

On peut interpréter :

F → avancer  
\+ → tourner  
− → tourner dans l'autre sens  
\[ → sauvegarder l'état  
\] → restaurer l'état

On obtient alors une géométrie.

## 15.3 — Applications

Les L-systems sont particulièrement puissants pour :

- arbres ;
- plantes ;
- branches ;
- racines ;
- feuilles ;
- structures organiques ;
- architecture procédurale ;
- mondes virtuels.

# 16 — IFS — ITERATED FUNCTION SYSTEMS

Un **Iterated Function System** repose sur plusieurs transformations appliquées de manière répétée.

Une transformation affine peut être représentée par :

\[ T(x)=Ax+b \]

où :

- (A) est une matrice ;
- (b) est un vecteur de translation.

Un IFS combine plusieurs transformations :

\[ T_1,T_2,,T_n \]

## 16.1 — Principe

forme initiale  
↓  
transformations  
↓  
copies transformées  
↓  
répétition  
↓  
structure fractale

## 16.2 — Exemples

Les IFS permettent notamment de construire :

- fougères fractales ;
- triangles ;
- tapis fractals ;
- structures auto-similaires.

# 17 — DIMENSION FRACTALE

La dimension fractale mesure la manière dont une structure occupe l’espace.

Elle peut être non entière.

## 17.1 — Dimension de similarité

Si une structure est composée de (N) copies réduites d’un facteur (r), alors :

\[ N=r^{-D} \]

d’où :

\[ D= \]

## 17.2 — Exemple

Pour le triangle de Sierpiński :

- (N=3)
- (r=1/2)

donc :

\[ D= \]

La dimension est comprise entre 1 et 2.

## 17.3 — Pourquoi cette notion est importante

Elle permet de caractériser quantitativement :

- complexité géométrique ;
- occupation de l’espace ;
- rugosité ;
- structures naturelles ;
- frontières complexes.

# 18 — DIMENSION BOX-COUNTING

Pour des objets plus complexes, on peut utiliser le principe du comptage par boîtes.

On recouvre l’objet avec des boîtes de taille ().

On observe le nombre :

\[ N() \]

de boîtes nécessaires.

La dimension peut être estimée par :

\[ D {(1/)} \]

lorsque le comportement asymptotique est approprié.

# 19 — FRACTALES ET RÉCURSIVITÉ

La récursivité constitue un mécanisme naturel de génération fractale.

Architecture conceptuelle :

PROBLÈME  
↓  
SOUS-PROBLÈMES SIMILAIRES  
↓  
SOUS-SOUS-PROBLÈMES  
↓  
...  
↓  
CAS DE BASE

Cependant, toutes les fractales ne nécessitent pas une récursion logicielle explicite.

Elles peuvent être générées par :

- boucles ;
- systèmes de réécriture ;
- transformations matricielles ;
- shaders ;
- calcul GPU ;
- systèmes itératifs.

# 20 — SYSTÈMES DYNAMIQUES

Un système dynamique décrit l’évolution d’un état.

Deux grandes familles sont fondamentales.

## 20.1 — Système discret

\[ x_{n+1}=f(x_n) \]

Le temps évolue par étapes.

## 20.2 — Système continu

\[ =f(x,t) \]

Le temps est continu.

## 20.3 — Système multidimensionnel

\[ =F(,t) \]

où :

\[ =

\]

# 21 — ESPACE DES PHASES

L’espace des phases représente les états possibles d’un système.

Une trajectoire dans cet espace permet d’observer :

- convergence ;
- oscillation ;
- stabilité ;
- divergence ;
- cycle ;
- chaos.

Exemple :

État  
│  
│ •  
│ • •  
│ • •  
│ • •  
└──────────────── Temps

Dans un système multidimensionnel, l’espace des phases devient particulièrement utile pour visualiser les trajectoires.

# 22 — POINTS FIXES

Un point fixe (x^\*) vérifie :

\[ f(x<sup>\*)=x</sup>\* \]

Pour un système discret :

\[ x_{n+1}=f(x_n) \]

un point fixe reste donc inchangé.

## 22.1 — Stabilité

Un point fixe peut être :

- stable ;
- instable ;
- asymptotiquement stable.

Pour une application scalaire, une condition classique locale utilise :

\[ |f’(x^\*)|<1 \]

pour la stabilité locale.

# 23 — CYCLES ET ORBITES PÉRIODIQUES

Un cycle de période (p) vérifie :

\[ f^p(x)=x \]

sans nécessairement avoir :

\[ f(x)=x \]

Cela signifie que le système revient à son état initial après (p) étapes.

Les cycles sont fondamentaux dans l’étude des systèmes dynamiques et des bifurcations.

# 24 — ATTRACTEURS

Un attracteur est une région ou un ensemble d’états vers lequel des trajectoires peuvent évoluer.

On distingue notamment :

- point fixe ;
- cycle limite ;
- tore ;
- attracteur étrange.

## 24.1 — Attracteur étrange

Un attracteur étrange combine généralement :

- structure complexe ;
- dynamique déterministe ;
- sensibilité ;
- géométrie non triviale.

L’attracteur de Lorenz est l’un des exemples les plus célèbres.

# 25 — SENSIBILITÉ AUX CONDITIONS INITIALES

Deux états initiaux extrêmement proches peuvent produire des trajectoires qui deviennent rapidement très différentes.

Conceptuellement :

x₀  
x₀ + ε

peuvent évoluer vers :

trajectoire A  
trajectoire B

avec une divergence croissante.

Cette propriété est souvent appelée :

effet papillon.

Elle constitue une caractéristique importante du chaos déterministe.

# 26 — CHAOS DÉTERMINISTE

Un système chaotique peut être :

- déterministe ;
- non linéaire ;
- sensible aux conditions initiales ;
- apériodique ;
- complexe.

Il ne faut donc pas confondre :

aléatoire

et :

chaotique

Un système aléatoire utilise une composante probabiliste.

Un système chaotique peut être entièrement déterministe.

# 27 — APPLICATION LOGISTIQUE

L’équation logistique discrète est :

\[ x_{n+1}=r x_n(1-x_n) \]

où :

- (x_n) est l’état ;
- (r) est un paramètre.

Cette équation simple présente des régimes de comportement très différents selon (r).

On peut observer :

convergence  
↓  
cycle  
↓  
doublement de période  
↓  
chaos

# 28 — DIAGRAMME DE BIFURCATION

Le diagramme de bifurcation permet d’observer les changements qualitatifs du comportement lorsqu’un paramètre varie.

Pour l’équation logistique, on peut :

faire varier r  
↓  
simuler le système  
↓  
ignorer le régime transitoire  
↓  
enregistrer les états finaux  
↓  
tracer x en fonction de r

On obtient une visualisation de la structure dynamique.

# 29 — ROUTE VERS LE CHAOS

Une route classique vers le chaos passe par le doublement de période.

Schéma :

point fixe  
↓  
cycle de période 2  
↓  
cycle de période 4  
↓  
cycle de période 8  
↓  
...  
↓  
chaos

Cette structure permet d’étudier comment un système relativement simple peut devenir extrêmement complexe.

# 30 — EXPOSANT DE LYAPUNOV

L’exposant de Lyapunov mesure le taux moyen de divergence ou de convergence de trajectoires initialement proches.

Conceptuellement :

\[ _{n}_ {i=0}^{n-1} |f’(x_i)| \]

dans le cas scalaire approprié.

Interprétation simplifiée :

- (<0) : convergence ;
- () : régime critique ;
- (>0) : divergence exponentielle locale compatible avec un comportement chaotique.

Il s’agit d’un outil important pour l’analyse des systèmes dynamiques.

# 31 — ATTRACTEUR DE LORENZ

Le système de Lorenz est donné par :

\[ =(y-x) \]

\[ =x(-z)-y \]

\[ =xy-z \]

où :

- () ;
- () ;
- ()

sont des paramètres.

Le système produit, pour certains paramètres, une trajectoire complexe présentant une structure caractéristique en deux lobes.

# 32 — INTÉGRATION NUMÉRIQUE

Les équations différentielles doivent généralement être résolues numériquement dans un logiciel.

La méthode la plus simple est Euler :

\[ x_{n+1}=x_n+h f(x_n,t_n) \]

où (h) est le pas temporel.

## 32.1 — Limites d’Euler

Un pas trop grand peut produire :

- instabilité ;
- divergence artificielle ;
- perte de précision ;
- comportement qualitativement faux.

## 32.2 — Méthodes plus avancées

Selon le besoin :

- Euler ;
- Runge-Kutta ;
- RK4 ;
- méthodes adaptatives ;
- intégrateurs spécialisés.

Pour une simulation sérieuse, le choix du solveur devient une décision d’ingénierie.

# 33 — STABILITÉ NUMÉRIQUE

Un système mathématique stable peut devenir numériquement instable si :

- le pas temporel est mauvais ;
- les erreurs d’arrondi s’accumulent ;
- l’intégrateur est inadapté ;
- les valeurs deviennent trop grandes ;
- la précision numérique est insuffisante.

Une simulation correcte doit donc distinguer :

DYNAMIQUE RÉELLE  
vs  
ARTEFACT NUMÉRIQUE

# 34 — BRUIT PROCÉDURAL

Le bruit procédural permet de générer une variation contrôlée sans stocker explicitement chaque valeur.

Une fonction de bruit peut être vue comme :

\[ N:^n \]

ou :

\[ N(x,y)v \]

pour une surface 2D.

# 35 — PROPRIÉTÉS D’UN BON BRUIT PROCÉDURAL

Selon l’application, on recherche :

- continuité ;
- cohérence spatiale ;
- déterminisme ;
- contrôle de l’échelle ;
- absence de motifs indésirables ;
- bonne distribution ;
- performance ;
- répétabilité.

# 36 — VALUE NOISE

Le Value Noise repose généralement sur des valeurs définies sur une grille puis interpolées.

Concept :

grille de valeurs  
↓  
sélection des voisins  
↓  
interpolation  
↓  
champ continu

L’interpolation peut utiliser :

- linéaire ;
- smoothstep ;
- interpolation cubique ;
- autres fonctions de lissage.

# 37 — PERLIN NOISE

Le Perlin Noise est un bruit gradient.

Il utilise une structure de grille et des gradients pseudo-aléatoires.

Conceptuellement :

coordonnée  
↓  
cellule  
↓  
gradients locaux  
↓  
produits avec vecteurs de distance  
↓  
interpolation  
↓  
valeur finale

Il est particulièrement connu pour :

- textures ;
- terrains ;
- nuages ;
- déformations ;
- effets graphiques.

# 38 — SIMPLEX NOISE

Le Simplex Noise constitue une famille de méthodes conçues pour produire un bruit cohérent dans plusieurs dimensions avec certaines propriétés géométriques et computationnelles intéressantes.

Il est particulièrement utile pour :

- 2D ;
- 3D ;
- 4D ;
- animations ;
- textures ;
- environnements procéduraux.

# 39 — WORLEY / CELLULAR NOISE

Le bruit de Worley repose sur la distance à des points caractéristiques.

Concept :

points  
↓  
distance vers les points  
↓  
plus proche voisin  
↓  
champ de distance

Il est particulièrement adapté à :

- cellules ;
- surfaces organiques ;
- pierre ;
- peau ;
- écailles ;
- motifs biologiques ;
- structures cellulaires.

# 40 — FRACTIONAL BROWNIAN MOTION — FBM

Le FBM consiste à additionner plusieurs couches de bruit à différentes échelles.

Forme générale :

\[ F(x)= \_{i=0}^{n-1} a_i N(f_i x) \]

où :

- (a_i) contrôle l’amplitude ;
- (f_i) contrôle la fréquence.

Chaque couche correspond à une octave.

## 40.1 — Principe

Bruit grande échelle  
+  
Bruit moyenne échelle  
+  
Bruit petite échelle  
+  
...  
\=  
structure riche

Cette technique est fondamentale pour les environnements naturels.

# 41 — LACUNARITÉ

Dans les constructions fractales et les bruits multi-échelles, la relation entre amplitude et fréquence influence fortement le caractère visuel du résultat.

Les paramètres doivent permettre de contrôler :

- rugosité ;
- détail ;
- contraste ;
- échelle ;
- fréquence.

# 42 — TURBULENCE

Une construction fréquente consiste à utiliser la valeur absolue du bruit :

\[ T(x)=\_i a_i |N(f_i x)| \]

Cela produit des structures visuelles plus agressives et plus riches.

Applications :

- fumée stylisée ;
- feu ;
- turbulence ;
- énergie ;
- déformation ;
- effets abstraits.

# 43 — DOMAIN WARPING

Le domain warping consiste à modifier les coordonnées avant d’évaluer le bruit.

Au lieu de :

\[ N(x) \]

on utilise :

\[ N(x+w(x)) \]

où (w(x)) est un champ de déplacement.

Cette technique peut produire :

- marbrures ;
- structures organiques ;
- turbulence ;
- distorsions ;
- formes complexes.

Elle est particulièrement puissante dans les shaders.

# 44 — BRUIT MULTI-ÉCHELLE

Un bon environnement naturel nécessite rarement une seule fréquence.

Exemple :

Macro structure  
↓  
forme générale du terrain  
<br/>Meso structure  
↓  
collines / vallées  
<br/>Micro structure  
↓  
rugosité / détails

Cette hiérarchie doit être conservée lors de la génération.

# 45 — FRACTALES ET BRUITS : DEUX APPROCHES COMPLÉMENTAIRES

### Fractale

Règle structurelle  
↓  
itération  
↓  
géométrie

### Bruit

Champ de variation  
↓  
échantillonnage  
↓  
déformation / texture

### Système dynamique

État  
↓  
règle d'évolution  
↓  
nouvel état  
↓  
répétition

Ces trois mécanismes peuvent être combinés.

# 46 — TERRAIN PROCÉDURAL

Un terrain peut être généré par un champ :

\[ h(x,y) \]

où (h) représente l’altitude.

Exemple :

\[ h(x,y)= a_1N(x,y) +a_2N(2x,2y) +a_3N(4x,4y) \]

On obtient un terrain multi-échelle.

## 46.1 — Pipeline

SEED  
↓  
PARAMÈTRES  
↓  
BRUIT  
↓  
FBM  
↓  
HEIGHTMAP  
↓  
NORMALS  
↓  
MESH  
↓  
MATERIAL  
↓  
LIGHTING  
↓  
RENDER

# 47 — NUAGES PROCÉDURAUX

Les nuages peuvent être représentés par des champs de densité.

On peut utiliser :

- bruit 3D ;
- FBM ;
- turbulence ;
- domain warping ;
- ray marching.

Concept :

position 3D  
↓  
densité  
↓  
absorption / diffusion  
↓  
accumulation le long du rayon  
↓  
couleur finale

# 48 — VÉGÉTATION PROCÉDURALE

La végétation peut combiner :

L-system  
+  
IFS  
+  
règles biologiques  
+  
bruit  
+  
géométrie procédurale

Exemple :

tronc  
↓  
branche principale  
↓  
branches secondaires  
↓  
ramifications  
↓  
feuilles

Les paramètres peuvent contrôler :

- angle ;
- longueur ;
- profondeur ;
- densité ;
- variation ;
- courbure ;
- gravité simulée ;
- lumière.

# 49 — GÉNÉRATION PROCÉDURALE

La génération procédurale consiste à produire du contenu par règles plutôt qu’à stocker chaque élément manuellement.

Elle peut générer :

- terrain ;
- végétation ;
- bâtiments ;
- textures ;
- routes ;
- rivières ;
- grottes ;
- environnements ;
- particules ;
- motifs ;
- animations.

# 50 — SEED ET REPRODUCTIBILITÉ

Un générateur procédural doit idéalement accepter une graine :

seed

La même graine doit produire le même résultat.

Cela permet :

- debugging ;
- partage ;
- sauvegarde ;
- reproductibilité ;
- génération déterministe ;
- synchronisation.

Exemple :

seed = 4217  
<br/>→ terrain A  
→ même terrain lors d'une nouvelle génération

# 51 — GÉNÉRATION PROCÉDURALE DÉTERMINISTE

Un générateur doit distinguer :

ALÉATOIRE RÉEL

et :

PSEUDO-ALÉATOIRE DÉTERMINISTE

Pour un logiciel, la seconde approche est souvent plus utile.

Elle permet :

seed  
+  
paramètres  
+  
algorithme  
\=  
résultat reproductible

# 52 — SYSTÈMES À AGENTS

Un système dynamique peut être composé de plusieurs agents.

Chaque agent possède :

- état ;
- position ;
- vitesse ;
- règles ;
- perception ;
- interaction.

Le comportement global peut émerger des règles locales.

Applications :

- foules ;
- trafic ;
- essaims ;
- végétation ;
- comportements artificiels ;
- simulations sociales.

# 53 — AUTOMATES CELLULAIRES

Un automate cellulaire représente l’espace comme une grille d’états.

Chaque cellule évolue selon une règle locale.

grille  
↓  
voisinage  
↓  
règle locale  
↓  
nouvelle grille  
↓  
répétition

Les automates cellulaires sont proches conceptuellement des systèmes dynamiques discrets.

Applications :

- simulation ;
- génération de mondes ;
- propagation ;
- croissance ;
- phénomènes biologiques ;
- jeux ;
- recherche computationnelle.

# 54 — SYSTÈMES DYNAMIQUES ET ÉMERGENCE

Une propriété importante est l’émergence.

Des règles simples peuvent produire un comportement global complexe.

Règles locales simples  
↓  
interaction répétée  
↓  
structure globale  
↓  
comportement émergent

Cette idée est fondamentale pour :

- simulations ;
- IA ;
- vie artificielle ;
- systèmes multi-agents ;
- jeux ;
- génération procédurale.

# 55 — FRACTALES DANS LES GRAPHISMES

Les fractales peuvent être utilisées pour générer :

- motifs ;
- textures ;
- arrière-plans ;
- formes organiques ;
- structures abstraites ;
- particules ;
- paysages ;
- environnements.

# 56 — SHADERS ET FRACTALES

Les fractales sont particulièrement adaptées aux shaders car leur calcul peut être exécuté indépendamment pour de nombreux pixels.

Architecture :

UV  
↓  
transformation  
↓  
fonction fractale  
↓  
itérations  
↓  
valeur  
↓  
palette  
↓  
pixel

# 57 — SHADERS ET BRUIT

Architecture typique :

UV / Position  
↓  
Noise  
↓  
FBM  
↓  
Domain Warping  
↓  
Mask  
↓  
Color  
↓  
Lighting  
↓  
Pixel

Les paramètres importants doivent être exposés :

- scale ;
- frequency ;
- amplitude ;
- octaves ;
- lacunarity ;
- gain ;
- warp strength ;
- seed ;
- animation speed.

# 58 — PARTICULES ET SYSTÈMES DYNAMIQUES

Une particule peut être représentée par :

\[ x(t),v(t) \]

avec :

\[ =v \]

et :

\[ =a \]

Le système peut ensuite ajouter :

- gravité ;
- attraction ;
- répulsion ;
- turbulence ;
- bruit ;
- collisions ;
- contraintes.

# 59 — CHAMPS DE VECTEURS

Un champ de vecteurs associe un vecteur à chaque point :

\[ F(x,y,z) \]

Les particules peuvent suivre ce champ.

position  
↓  
champ de vecteurs  
↓  
direction  
↓  
vitesse  
↓  
nouvelle position

Applications :

- fumée stylisée ;
- flux ;
- vent ;
- particules ;
- visualisation scientifique ;
- animation abstraite.

# 60 — SYSTÈMES DE FLUIDES

Les fluides peuvent être modélisés par des équations physiques plus complexes.

Une référence fondamentale est Navier-Stokes.

Conceptuellement :

vitesse  
+  
pression  
+  
viscosité  
+  
forces  
\=  
évolution du fluide

Dans un logiciel graphique, on peut également utiliser des modèles simplifiés ou stylisés.

Il faut donc distinguer :

simulation physiquement fidèle

de :

simulation visuellement plausible

Cette distinction est importante en production.

# 61 — GÉNÉRATION PROCÉDURALE D’EAU

On peut combiner :

- bruit ;
- vagues sinusoïdales ;
- champs de déplacement ;
- simulation ;
- shaders.

Une surface peut être définie par :

\[ z=h(x,y,t) \]

où le temps (t) permet de faire évoluer la surface.

# 62 — ANIMATION PROCÉDURALE

Un système dynamique constitue naturellement un moteur d’animation.

temps  
↓  
état  
↓  
règle  
↓  
nouvel état  
↓  
rendu

Cela peut produire :

- mouvement organique ;
- oscillation ;
- turbulence ;
- comportement émergent ;
- systèmes interactifs.

# 63 — CHAOS COMME OUTIL CRÉATIF

Le chaos peut être utilisé volontairement pour produire :

- trajectoires complexes ;
- variation ;
- animation imprévisible ;
- compositions génératives ;
- particules ;
- mouvements organiques.

Mais un système chaotique doit être paramétré avec soin.

Une petite variation peut entraîner une différence importante.

# 64 — CONTRÔLE D’UN SYSTÈME CHAOTIQUE

Pour rendre un système utilisable dans une application, il faut exposer des paramètres contrôlables.

Exemples :

initialState  
parameter  
timeStep  
iterationCount  
noiseStrength  
damping  
interactionStrength

Le développeur doit également pouvoir limiter :

- énergie ;
- amplitude ;
- vitesse ;
- espace ;
- nombre d’itérations.

# 65 — FRACTALES ET COMPRESSION CONCEPTUELLE

Une fractale est intéressante en informatique parce qu’elle peut représenter une structure complexe avec relativement peu de paramètres.

petite description  
↓  
règle  
↓  
itération  
↓  
structure complexe

Cette propriété peut être exploitée pour :

- génération ;
- représentation ;
- compression spécialisée ;
- visualisation ;
- stockage paramétrique.

# 66 — FRACTALES ET NIVEAUX DE DÉTAIL

Une fractale peut naturellement produire différents niveaux de détail.

niveau 0  
↓  
niveau 1  
↓  
niveau 2  
↓  
niveau 3  
↓  
...

Cela peut être exploité pour :

- zoom ;
- LOD ;
- génération progressive ;
- streaming ;
- terrain ;
- visualisation.

# 67 — PERFORMANCE

La génération fractale peut devenir coûteuse.

Les principaux paramètres sont :

- résolution ;
- profondeur ;
- nombre d’itérations ;
- nombre d’octaves ;
- taille du domaine ;
- nombre de particules ;
- fréquence de mise à jour.

Il faut donc mesurer :

qualité  
vs  
coût

# 68 — CPU VS GPU

Certaines opérations sont naturellement adaptées au GPU :

- calcul par pixel ;
- bruit ;
- fractales ;
- particules ;
- transformations parallèles ;
- simulation locale.

Architecture :

CPU  
→ logique  
→ paramètres  
→ état global  
<br/>GPU  
→ calcul parallèle  
→ génération  
→ rendu

Mais le transfert CPU ↔ GPU doit être maîtrisé.

# 69 — PRÉCALCUL VS TEMPS RÉEL

Un système peut :

### Pré-calculer

génération  
↓  
stockage  
↓  
rendu

ou :

### Calculer en temps réel

paramètres  
↓  
calcul  
↓  
rendu

Le choix dépend de :

- complexité ;
- interactivité ;
- mémoire ;
- fréquence de variation ;
- matériel cible.

# 70 — ARCHITECTURE D’UN GÉNÉRATEUR PROCÉDURAL

Une architecture générique peut être :

Generator  
│  
├── Seed  
├── Parameters  
├── Noise  
├── Fractal / Rule System  
├── Transformations  
├── Sampling  
├── Post Processing  
├── Output  
└── Cache

Les responsabilités doivent rester séparées.

# 71 — PARAMÉTRISATION

Les générateurs doivent éviter les constantes dispersées.

Exemple :

terrainScale  
octaves  
persistence  
lacunarity  
heightMultiplier  
warpStrength  
seed

Les paramètres doivent être :

- documentés ;
- contrôlables ;
- testables ;
- bornés lorsque nécessaire.

# 72 — VALIDATION D’UN GÉNÉRATEUR

Un générateur doit être testé sur :

- plusieurs seeds ;
- plusieurs résolutions ;
- plusieurs paramètres ;
- cas extrêmes ;
- appareils différents ;
- tailles différentes.

Vérifier :

- stabilité ;
- répétabilité ;
- absence d’artefacts ;
- performance ;
- qualité visuelle.

# 73 — DÉTERMINISME ET DEBUGGING

Une seed fixe permet :

Bug  
↓  
seed  
↓  
reproduction exacte  
↓  
analyse  
↓  
correction

Sans reproductibilité, les bugs procéduraux peuvent être particulièrement difficiles à diagnostiquer.

# 74 — VISUALISATION SCIENTIFIQUE

Les systèmes dynamiques peuvent être visualisés sous forme de :

- courbes temporelles ;
- trajectoires ;
- portraits de phase ;
- diagrammes de bifurcation ;
- cartes de chaleur ;
- attracteurs ;
- champs vectoriels.

# 75 — ART GÉNÉRATIF

Les fractales et systèmes dynamiques peuvent alimenter un moteur artistique.

Architecture :

PARAMÈTRES  
↓  
MOTEUR MATHÉMATIQUE  
↓  
STRUCTURE  
↓  
COULEUR  
↓  
COMPOSITION  
↓  
ANIMATION  
↓  
INTERACTION

Les paramètres peuvent être pilotés par :

- temps ;
- musique ;
- utilisateur ;
- données ;
- événements ;
- capteurs.

# 76 — JEUX VIDÉO

Applications possibles :

- génération de mondes ;
- terrains ;
- grottes ;
- végétation ;
- nuages ;
- textures ;
- effets ;
- particules ;
- météo ;
- environnements ;
- animation procédurale.

# 77 — GÉNÉRATION DE GROTTES

Une approche peut combiner :

bruit  
+  
threshold  
+  
automate cellulaire  
+  
smoothing

pour obtenir une structure de cavernes.

# 78 — MÉTÉO PROCÉDURALE

Une simulation stylisée peut combiner :

champs de bruit  
+  
systèmes dynamiques  
+  
particules  
+  
vent  
+  
densité

pour générer :

- nuages ;
- pluie ;
- brouillard ;
- poussière ;
- tempêtes.

# 79 — SIMULATION DE FUMÉE

Une approche simplifiée peut utiliser :

- champ de vitesse ;
- diffusion ;
- advection ;
- bruit ;
- particules.

Architecture :

velocity field  
↓  
advection  
↓  
density  
↓  
diffusion  
↓  
rendering

# 80 — EFFETS VISUELS

Le Domaine K peut alimenter :

- distorsion ;
- glitch organique ;
- liquide abstrait ;
- feu ;
- fumée ;
- énergie ;
- turbulence ;
- apparition/disparition ;
- transitions.

# 81 — TRANSITIONS PROCÉDURALES

Une transition peut être construite à partir d’un champ :

\[ M(x,y) \]

puis d’un seuil contrôlé par (t).

mask  
+  
progress  
↓  
threshold  
↓  
reveal

Cette technique permet des transitions organiques.

# 82 — FRACTALES ET UI

Les fractales peuvent également servir à créer :

- backgrounds ;
- illustrations ;
- visualisations ;
- loaders ;
- états de chargement ;
- transitions ;
- éléments décoratifs.

Mais elles ne doivent pas nuire :

- à la lisibilité ;
- à la performance ;
- à l’accessibilité ;
- à la hiérarchie visuelle.

# 83 — ACCESSIBILITÉ DES EXPÉRIENCES PROCÉDURALES

Une visualisation dynamique doit prévoir :

- réduction du mouvement ;
- possibilité d’arrêt ;
- alternative textuelle si nécessaire ;
- contraste suffisant ;
- absence de dépendance exclusive aux animations.

Une expérience mathématiquement intéressante ne doit pas devenir une barrière fonctionnelle.

# 84 — PARAMÈTRES DE RÉFÉRENCE POUR UN MOTEUR FRACTAL

Un moteur générique peut exposer :

type  
depth  
scale  
rotation  
translation  
iterations  
threshold  
seed  
colorMode  
palette  
zoom  
center  
escapeRadius

Pour Mandelbrot/Julia :

complexConstant  
maxIterations  
escapeRadius  
zoom  
center  
colorMapping

# 85 — PARAMÈTRES DE RÉFÉRENCE POUR UN MOTEUR DE BRUIT

seed  
frequency  
amplitude  
octaves  
lacunarity  
persistence  
gain  
warpStrength  
warpFrequency  
normalization

# 86 — PARAMÈTRES DE RÉFÉRENCE POUR UN SYSTÈME DYNAMIQUE

initialState  
timeStep  
duration  
parameters  
integrator  
damping  
force  
boundary  
precision

# 87 — RÈGLE DE RECONNAISSANCE : QUAND UTILISER QUOI ?

## Besoin : motif auto-similaire

→ Fractale.

## Besoin : structure récursive

→ Fractale / L-system / IFS.

## Besoin : arbre ou végétation

→ L-system + règles procédurales.

## Besoin : terrain

→ bruit + FBM + éventuellement érosion.

## Besoin : texture organique

→ bruit + FBM + domain warping.

## Besoin : cellules

→ Worley / cellular noise.

## Besoin : comportement évolutif

→ système dynamique.

## Besoin : mouvement complexe déterministe

→ système dynamique / chaos.

## Besoin : trajectoires étranges

→ attracteur / système chaotique.

## Besoin : nuages

→ bruit 3D + FBM + densité.

## Besoin : simulation physique

→ équations différentielles + intégration numérique.

## Besoin : effet visuel extrêmement rapide par pixel

→ shader / GPU.

# 88 — ERREURS CONCEPTUELLES À ÉVITER

## Erreur 1 — Appeler tout bruit « fractal »

Incorrect.

Le bruit et la fractale sont des concepts différents.

## Erreur 2 — Confondre hasard et chaos

Un système chaotique peut être déterministe.

## Erreur 3 — Croire qu’une fractale doit être récursive dans le code

La structure peut être calculée autrement.

## Erreur 4 — Croire que plus d’itérations signifie toujours meilleur résultat

Plus d’itérations signifie surtout :

- plus de coût ;
- plus de détail ;
- parfois plus de bruit visuel.

## Erreur 5 — Simuler sans contrôler le pas temporel

Une mauvaise discrétisation peut créer des artefacts.

## Erreur 6 — Utiliser du WebGL pour tout

La technologie doit suivre le besoin.

## Erreur 7 — Ajouter du bruit sans structure

Le bruit seul peut produire une image sans organisation.

## Erreur 8 — Mélanger trop de fréquences sans contrôle

Un résultat procédural peut devenir visuellement incohérent.

# 89 — WORKFLOW DE CONCEPTION D’UNE APPLICATION PROCÉDURALE

1\. Définir le phénomène  
↓  
2\. Identifier le modèle mathématique  
↓  
3\. Choisir la représentation  
↓  
4\. Définir les paramètres  
↓  
5\. Construire une version minimale  
↓  
6\. Vérifier la stabilité  
↓  
7\. Vérifier la reproductibilité  
↓  
8\. Ajouter les détails  
↓  
9\. Optimiser  
↓  
10\. Visualiser  
↓  
11\. Ajouter l'interaction  
↓  
12\. Tester les limites  
↓  
13\. Documenter le générateur

# 90 — ARCHITECTURE LOGICIELLE RECOMMANDÉE

Pour une application complexe :

APPLICATION  
│  
├── Mathematical Model  
│ ├── Fractal  
│ ├── Noise  
│ └── Dynamic System  
│  
├── Simulation  
│ ├── State  
│ ├── Integrator  
│ └── Update  
│  
├── Procedural Generator  
│ ├── Seed  
│ ├── Parameters  
│ └── Generation  
│  
├── Rendering  
│ ├── Canvas  
│ ├── WebGL  
│ ├── Shader  
│ └── Three.js  
│  
├── Interaction  
│ ├── Input  
│ ├── Camera  
│ └── Controls  
│  
└── Debug  
├── Metrics  
├── State  
└── Parameters

# 91 — MOTEUR DE GÉNÉRATION GÉNÉRIQUE

Un moteur procédural peut être conceptualisé comme :

Seed  
+  
Parameters  
+  
Generator  
+  
Transform  
+  
PostProcess  
\=  
Output

Cette architecture permet de remplacer le générateur sans réécrire tout le système.

# 92 — CACHE

Le cache peut stocker :

- bruit ;
- heightmaps ;
- meshes ;
- textures ;
- résultats intermédiaires ;
- chunks générés.

Architecture :

Request  
↓  
Cache lookup  
↓  
Hit → return  
↓  
Miss  
↓  
Generate  
↓  
Cache  
↓  
Return

# 93 — GÉNÉRATION PAR CHUNKS

Pour un monde procédural :

World  
├── Chunk 0  
├── Chunk 1  
├── Chunk 2  
└── ...

Chaque chunk peut être généré à partir de :

\[ seed + coordonnées \]

Cela permet une génération cohérente à grande échelle.

# 94 — LOD ET PROCÉDURAL

Les systèmes fractals permettent naturellement plusieurs niveaux de détail.

distance faible  
→ haute résolution  
<br/>distance moyenne  
→ résolution moyenne  
<br/>distance élevée  
→ faible résolution

Cela peut réduire fortement le coût de rendu.

# 95 — CONTINUITÉ ENTRE CHUNKS

Un problème important des mondes procéduraux est la jonction entre zones.

Il faut éviter :

chunk A  
██████  
██████  
chunk B

avec une rupture visible.

Les coordonnées globales ou les fonctions déterministes permettent de produire une continuité.

# 96 — NORMALISATION

Les générateurs peuvent produire des valeurs dans différents intervalles.

Il est souvent utile de normaliser :

\[ x’= \]

afin d’obtenir :

\[ x’\]

Cette étape facilite :

- couleurs ;
- hauteur ;
- masques ;
- seuils ;
- paramètres de matériaux.

# 97 — SAMPLING

Un modèle continu doit être échantillonné pour devenir numérique.

fonction continue  
↓  
grille  
↓  
échantillons  
↓  
image / mesh / volume

La résolution du sampling influence :

- détail ;
- aliasing ;
- mémoire ;
- performance.

# 98 — ALIASING ET DÉTAIL PROCÉDURAL

Une structure contenant des détails trop fins par rapport à la résolution peut produire :

- aliasing ;
- scintillement ;
- motifs instables.

Il faut donc adapter le niveau de détail à :

- résolution ;
- distance ;
- fréquence d’affichage ;
- taille du pixel.

# 99 — ANIMATION DU BRUIT

Un bruit peut être animé en ajoutant une dimension temporelle :

\[ N(x,y,t) \]

ou :

\[ N(x,y,z) \]

avec :

\[ z=vt \]

Cette technique permet de produire une variation temporelle cohérente.

# 100 — COHÉRENCE TEMPORELLE

Un mauvais bruit animé peut produire :

frame 1 → structure A  
frame 2 → structure B totalement différente

ce qui crée du scintillement.

Une bonne animation procédurale doit conserver une cohérence entre les frames.

# 101 — SYSTÈMES DYNAMIQUES INTERACTIFS

L’utilisateur peut modifier le système en temps réel :

Input  
↓  
Parameter  
↓  
Dynamic System  
↓  
New State  
↓  
Render

Exemples :

- modifier un attracteur ;
- changer (r) dans la logistique ;
- déplacer une constante complexe ;
- modifier le vent ;
- changer la force d’un champ.

# 102 — FRACTALES INTERACTIVES

Un explorateur fractal peut permettre :

- zoom ;
- déplacement ;
- changement de palette ;
- modification des paramètres ;
- augmentation du nombre d’itérations ;
- export.

Architecture :

Camera State  
↓  
Fractal Parameters  
↓  
GPU Computation  
↓  
Render

# 103 — VISUALISATEUR DE SYSTÈMES DYNAMIQUES

Un outil pédagogique peut afficher simultanément :

Équation  
+  
Paramètres  
+  
État actuel  
+  
Trajectoire  
+  
Portrait de phase  
+  
Statistiques

Cela transforme une formule abstraite en système observable.

# 104 — GÉNÉRATION DE CONTENU POUR JEUX

Pipeline :

Seed  
↓  
World Parameters  
↓  
Terrain  
↓  
Biomes  
↓  
Vegetation  
↓  
Structures  
↓  
Weather  
↓  
Entities  
↓  
World

Le système peut être déterministe.

# 105 — BIOMES PROCÉDURAUX

Les biomes peuvent dépendre de champs :

\[ temperature(x,y) \]

\[ humidity(x,y) \]

\[ elevation(x,y) \]

Puis une règle :

temperature  
+  
humidity  
+  
elevation  
↓  
biome

Exemple :

température élevée  
+  
humidité faible  
+  
altitude faible  
→ désert

# 106 — COMBINAISON AVANCÉE : FRACTALE + BRUIT + DYNAMIQUE

Un système très puissant peut combiner les trois familles :

Fractale  
→ structure  
<br/>Bruit  
→ variation  
<br/>Dynamique  
→ évolution

Exemple :

Terrain fractal  
+  
bruit local  
+  
vent dynamique  
\=  
environnement vivant

# 107 — CHAOS + PARTICULES

Une trajectoire chaotique peut piloter un système de particules.

Attracteur  
↓  
Trajectoire  
↓  
Emitter  
↓  
Particles  
↓  
Rendering

Cela permet de créer des mouvements impossibles à obtenir avec une simple animation linéaire.

# 108 — FRACTALE + 3D

Une fractale 2D peut être transformée en :

- heightmap ;
- mesh ;
- volume ;
- texture ;
- champ de déplacement.

Exemple :

Fractal / Noise  
↓  
Heightmap  
↓  
Displacement  
↓  
Mesh  
↓  
Material  
↓  
Lighting

# 109 — FRACTALES VOLUMÉTRIQUES

Le concept peut être étendu à :

\[ F(x,y,z) \]

permettant de générer :

- volumes ;
- nuages ;
- fumée ;
- cavités ;
- structures organiques.

# 110 — RAY MARCHING ET FRACTALES

Certaines fractales 3D peuvent être rendues par des techniques de ray marching.

Concept :

camera ray  
↓  
distance estimation  
↓  
march  
↓  
surface hit  
↓  
normal  
↓  
lighting

Cette approche est particulièrement intéressante pour :

- Mandelbulb ;
- fractales 3D ;
- objets mathématiques ;
- scènes volumétriques.

# 111 — MANDELBULB

Le Mandelbulb est une extension tridimensionnelle inspirée de la dynamique complexe.

Il ne constitue pas simplement une transposition triviale du Mandelbrot en 3D.

Il illustre plutôt comment des règles mathématiques complexes peuvent produire une géométrie tridimensionnelle riche.

Applications :

- art génératif ;
- visualisation ;
- ray marching ;
- exploration mathématique.

# 112 — DIMENSION FRACTALE ET DONNÉES RÉELLES

La dimension fractale peut également être utilisée pour analyser des structures observées :

- contours ;
- réseaux ;
- terrains ;
- textures ;
- phénomènes naturels.

Elle peut alors passer du rôle de générateur à celui d’outil d’analyse.

# 113 — FRACTALES ET ANALYSE D’IMAGES

Pipeline possible :

Image  
↓  
Segmentation  
↓  
Contour / structure  
↓  
Box Counting  
↓  
Dimension estimée  
↓  
Analyse

Applications potentielles :

- caractérisation de textures ;
- analyse de formes ;
- recherche scientifique ;
- classification.

# 114 — CHAOS ET SÉRIES TEMPORELLES

Une série temporelle peut être analysée pour rechercher :

- périodicité ;
- instabilité ;
- corrélation ;
- structure ;
- comportement chaotique.

Il faut cependant éviter de conclure au chaos uniquement parce qu’une série paraît irrégulière.

L’analyse doit reposer sur des critères appropriés.

# 115 — SYSTÈMES DYNAMIQUES ET IA

Les systèmes dynamiques peuvent servir à :

- modéliser des états ;
- simuler des environnements ;
- générer des données ;
- construire des représentations temporelles ;
- modéliser des phénomènes physiques ;
- produire des comportements émergents.

Ils peuvent être combinés avec :

- apprentissage automatique ;
- réseaux neuronaux ;
- reinforcement learning ;
- optimisation ;
- contrôle.

# 116 — NEURAL ODE ET SYSTÈMES DYNAMIQUES

Une connexion avancée consiste à représenter l’évolution d’un modèle neuronal sous la forme :

\[ =f_(h,t) \]

où (f_) est paramétré par un réseau neuronal.

Cette approche rapproche :

réseaux neuronaux  
+  
équations différentielles  
+  
apprentissage

# 117 — SYSTÈMES DYNAMIQUES ET ROBOTIQUE

Un robot peut être décrit par :

état  
↓  
dynamique  
↓  
action  
↓  
nouvel état

Exemple :

\[ x_{t+1}=f(x_t,u_t) \]

où :

- (x_t) est l’état ;
- (u_t) est la commande.

Cette structure relie naturellement :

- dynamique ;
- contrôle ;
- optimisation ;
- planification.

# 118 — CONTRÔLE

Un système de contrôle cherche à faire évoluer un système vers un comportement désiré.

État actuel  
↓  
Observation  
↓  
Erreur  
↓  
Contrôleur  
↓  
Commande  
↓  
Système  
↓  
Nouvel état

Cette architecture est fondamentale en robotique et systèmes embarqués.

# 119 — SYSTÈMES DYNAMIQUES ET JEUX

Un jeu peut être considéré comme un système dynamique :

player input  
+  
world state  
+  
physics  
+  
AI  
↓  
new world state

Cela permet d’utiliser les concepts du Domaine K pour :

- physique ;
- comportements ;
- météo ;
- monde vivant ;
- animation ;
- événements émergents.

# 120 — CRÉATION D’EXPÉRIENCES GÉNÉRATIVES

Une expérience générative avancée peut utiliser :

USER  
↓  
PARAMETERS  
↓  
MATHEMATICAL SYSTEM  
↓  
PROCEDURAL GENERATION  
↓  
VISUAL OUTPUT  
↓  
FEEDBACK  
↓  
NEW PARAMETERS

Le système devient alors interactif et non simplement décoratif.

# 121 — RÈGLE DE CONCEPTION : MODÈLE AVANT EFFET

Ne pas commencer par :

« Quel effet visuel puis-je créer ? »

Commencer par :

« Quel comportement ou quelle structure veux-je représenter ? »

Puis :

Intention  
↓  
Modèle  
↓  
Mathématiques  
↓  
Algorithme  
↓  
Représentation  
↓  
Effet

Cette règle évite l’utilisation superficielle des mathématiques.

# 122 — RÈGLE DE CONCEPTION : SIMPLE RÈGLE, COMPLEXE RÉSULTAT

Une architecture particulièrement intéressante consiste à chercher :

règle locale simple  
+  
répétition  
+  
interaction  
\=  
complexité émergente

C’est l’une des idées les plus importantes du Domaine K.

# 123 — MOTEUR D’ORIGINALITÉ

Pour chercher des applications originales, l’IA peut croiser plusieurs axes.

### Axe 1 — Structure

- fractale ;
- arbre ;
- attracteur ;
- champ ;
- réseau.

### Axe 2 — Variation

- bruit ;
- hasard contrôlé ;
- paramètres ;
- données.

### Axe 3 — Temps

- statique ;
- animé ;
- interactif ;
- évolutif.

### Axe 4 — Représentation

- 2D ;
- 3D ;
- particules ;
- volume ;
- shader ;
- audio.

### Axe 5 — Interaction

- souris ;
- clavier ;
- tactile ;
- données ;
- musique ;
- environnement.

# 124 — MATRICE D’IDÉATION

| Mathématique | Variation | Temps | Rendu | Application potentielle |
| --- | --- | --- | --- | --- |
| Mandelbrot | palette | statique | shader | explorateur fractal |
| Julia | paramètre (c) | animé | WebGL | art génératif |
| L-system | seed | dynamique | 3D  | forêt procédurale |
| FBM | seed | animé | shader | nuages |
| Lorenz | paramètres | temps réel | particules | sculpture dynamique |
| Worley | seed | animé | texture | matière organique |
| champ vectoriel | données | dynamique | particules | visualisation |
| automate cellulaire | état initial | évolution | grille | simulation |
| bruit 3D | paramètres | temps | volume | fumée |
| fractale 3D | caméra | interactif | ray marching | sculpture mathématique |

# 125 — COMBINAISONS À EXPLORER

Le domaine devient particulièrement puissant lorsqu’on combine plusieurs techniques.

## Fractale + L-system

→ végétation complexe.

## L-system + bruit

→ végétation moins régulière.

## Bruit + système dynamique

→ environnement évolutif.

## Attracteur + particules

→ art génératif dynamique.

## Bruit + ray marching

→ nuages et volumes.

## Fractale + shader

→ visualisation interactive.

## Chaos + audio

→ visualisation musicale non linéaire.

## Données + système dynamique

→ visualisation de données vivante.

## Optimisation + génération procédurale

→ recherche automatique de formes ou environnements.

# 126 — CONNEXION AVEC LE DOMAINE J — OPTIMISATION

Une connexion particulièrement importante est :

Générateur procédural  
↓  
Paramètres  
↓  
Fonction de qualité  
↓  
Optimisation  
↓  
Meilleure génération

Exemple :

Chercher automatiquement les paramètres produisant :

- une forme souhaitée ;
- une densité donnée ;
- une distribution donnée ;
- une esthétique particulière.

Le générateur devient alors un espace de recherche.

# 127 — CONNEXION AVEC LE DOMAINE G — PROBABILITÉS

Le bruit peut être :

- pseudo-aléatoire ;
- probabiliste ;
- stochastique.

Les probabilités permettent de modéliser :

incertitude  
+  
variation  
+  
distribution

alors que le Domaine K utilise ces mécanismes pour générer ou faire évoluer des structures.

# 128 — CONNEXION AVEC LE DOMAINE H — STATISTIQUES

Les statistiques peuvent mesurer :

- distribution du bruit ;
- propriétés d’un générateur ;
- dimension estimée ;
- comportement d’un système ;
- qualité d’une génération.

# 129 — CONNEXION AVEC LE DOMAINE I — CALCUL DIFFÉRENTIEL

Les systèmes dynamiques continus utilisent directement :

\[ =f(x,t) \]

Le calcul différentiel fournit donc les outils nécessaires pour comprendre leur évolution.

# 130 — CONNEXION AVEC LE DOMAINE C — ALGÈBRE LINÉAIRE

Les matrices servent notamment à :

- transformations ;
- rotations ;
- systèmes dynamiques ;
- IFS ;
- géométrie ;
- simulation ;
- représentation d’état.

# 131 — CONNEXION AVEC LE DOMAINE D — GÉOMÉTRIE

La géométrie permet de transformer les structures mathématiques en :

- points ;
- lignes ;
- surfaces ;
- volumes ;
- transformations.

# 132 — CONNEXION AVEC LE DOMAINE E — GRAPHES

Les systèmes dynamiques peuvent être représentés par des graphes d’états :

État A  
↓  
État B  
↓  
État C  
↘  
État D

Les graphes peuvent également représenter :

- structures fractales ;
- systèmes de réécriture ;
- arbres ;
- dépendances.

# 133 — CONNEXION AVEC LE DOMAINE F — COMBINATOIRE

La génération procédurale peut nécessiter :

- recherche de configurations ;
- arrangements ;
- structures ;
- règles combinatoires.

# 134 — CONNEXION AVEC L’INGÉNIERIE LOGICIELLE

Un système procédural doit être :

- modulaire ;
- déterministe lorsque nécessaire ;
- paramétrable ;
- testable ;
- observable ;
- performant ;
- documenté.

La beauté mathématique ne dispense pas de l’ingénierie.

# 135 — TESTS UNITAIRES POUR UN GÉNÉRATEUR

Tester notamment :

same seed  
→ same result  
<br/>different seed  
→ different result  
<br/>invalid parameter  
→ controlled failure  
<br/>boundary parameter  
→ stable result

# 136 — TESTS DE STABILITÉ

Pour un système dynamique :

petite perturbation  
↓  
simulation  
↓  
comparaison

Cela permet d’étudier :

- sensibilité ;
- stabilité ;
- divergence ;
- robustesse.

# 137 — TESTS DE PERFORMANCE

Mesurer :

- temps de génération ;
- FPS ;
- mémoire ;
- nombre d’itérations ;
- coût GPU ;
- coût CPU ;
- temps de chargement.

# 138 — DOCUMENTATION D’UN GÉNÉRATEUR

Chaque générateur devrait documenter :

Nom  
Objectif  
Modèle mathématique  
Entrées  
Paramètres  
Plages recommandées  
Seed  
Sortie  
Complexité  
Limites  
Dépendances  
Méthode de rendu  
Exemples

# 139 — FICHE DE RÉFÉRENCE : FRACTALE

Pour toute fractale étudiée :

### 1\. Nom

### 2\. Définition mathématique

### 3\. Règle de génération

### 4\. Paramètres

### 5\. Algorithme

### 6\. Structure obtenue

### 7\. Dimension éventuelle

### 8\. Complexité

### 9\. Représentation

### 10\. Applications

### 11\. Optimisations

### 12\. Variantes

# 140 — FICHE DE RÉFÉRENCE : SYSTÈME DYNAMIQUE

Documenter :

### 1\. Variables d’état

### 2\. Équations

### 3\. Conditions initiales

### 4\. Paramètres

### 5\. Méthode d’intégration

### 6\. Pas temporel

### 7\. Stabilité

### 8\. Attracteurs

### 9\. Bifurcations

### 10\. Visualisation

### 11\. Applications

# 141 — FICHE DE RÉFÉRENCE : BRUIT

Documenter :

### 1\. Type de bruit

### 2\. Dimension

### 3\. Seed

### 4\. Domaine d’entrée

### 5\. Domaine de sortie

### 6\. Continuité

### 7\. Interpolation

### 8\. Fréquence

### 9\. Amplitude

### 10\. Octaves

### 11\. Composition

### 12\. Coût

### 13\. GPU/CPU

### 14\. Applications

# 142 — CATALOGUE DE FICHES D’APPROFONDISSEMENT

Le Domaine K peut être approfondi à travers les fiches suivantes.

K01 — Auto-similarité  
K02 — Récursivité fractale  
K03 — Mandelbrot  
K04 — Julia  
K05 — Sierpiński  
K06 — Koch  
K07 — Dragon Curve  
K08 — Hilbert  
K09 — Peano  
K10 — L-systems  
K11 — IFS  
K12 — Dimension fractale  
K13 — Box Counting  
K14 — Fractales aléatoires  
K15 — Systèmes dynamiques discrets  
K16 — Systèmes dynamiques continus  
K17 — Points fixes  
K18 — Stabilité  
K19 — Cycles  
K20 — Attracteurs  
K21 — Attracteurs étranges  
K22 — Bifurcations  
K23 — Chaos déterministe  
K24 — Sensibilité aux conditions initiales  
K25 — Exposants de Lyapunov  
K26 — Équation logistique  
K27 — Attracteur de Lorenz  
K28 — Intégration numérique  
K29 — Automates cellulaires  
K30 — Systèmes multi-agents  
K31 — Value Noise  
K32 — Perlin Noise  
K33 — Simplex Noise  
K34 — Worley Noise  
K35 — FBM  
K36 — Turbulence  
K37 — Domain Warping  
K38 — Bruit 3D  
K39 — Terrain procédural  
K40 — Végétation procédurale  
K41 — Nuages procéduraux  
K42 — Fluides procéduraux  
K43 — Particules  
K44 — Champs vectoriels  
K45 — Shaders procéduraux  
K46 — Ray Marching  
K47 — Fractales 3D  
K48 — Mandelbulb  
K49 — Génération procédurale de mondes  
K50 — Seed et reproductibilité  
K51 — Chunking  
K52 — LOD procédural  
K53 — Optimisation de générateurs  
K54 — Fractales et GPU  
K55 — Systèmes dynamiques interactifs  
K56 — Art génératif  
K57 — Visualisation scientifique  
K58 — Chaos et audio  
K59 — Systèmes dynamiques pour IA  
K60 — Systèmes dynamiques pour robotique

# 143 — PROJETS PRATIQUES PROGRESSIFS

## Projet K01 — Générateur de Sierpiński

Objectif :

- récursion ;
- géométrie ;
- profondeur ;
- rendu.

## Projet K02 — Explorateur de Mandelbrot

Fonctions :

- zoom ;
- déplacement ;
- palette ;
- nombre d’itérations.

## Projet K03 — Explorateur de Julia

Permettre de modifier :

\[ c=a+bi \]

en temps réel.

## Projet K04 — Générateur de Koch

Paramètres :

- profondeur ;
- longueur ;
- angle ;
- couleur.

## Projet K05 — Générateur de plantes L-system

Paramètres :

- profondeur ;
- angle ;
- longueur ;
- variation ;
- seed.

## Projet K06 — Générateur de terrain

Pipeline :

Seed  
↓  
Noise  
↓  
FBM  
↓  
Heightmap  
↓  
Mesh  
↓  
Material  
↓  
3D

## Projet K07 — Visualiseur de Lorenz

Afficher :

- trajectoire 3D ;
- paramètres ;
- vitesse ;
- zoom ;
- caméra.

## Projet K08 — Diagramme de bifurcation

Utiliser l’équation logistique.

## Projet K09 — Attracteur + particules

Transformer la trajectoire du système dynamique en système de particules.

## Projet K10 — Générateur de nuages

Utiliser :

Noise 3D  
+  
FBM  
+  
Density  
+  
Ray Marching

## Projet K11 — Monde procédural

Combiner :

terrain  
+  
biomes  
+  
végétation  
+  
structures  
+  
météo

## Projet K12 — Studio d’art génératif

Interface permettant de combiner :

fractale  
+  
noise  
+  
dynamique  
+  
palette  
+  
animation

# 144 — EXERCICES DE COMPRÉHENSION

### Exercice 1

Expliquer pourquoi Mandelbrot et Julia utilisent une équation similaire mais explorent des paramètres différents.

### Exercice 2

Construire un triangle de Sierpiński récursif.

### Exercice 3

Calculer la dimension de similarité d’une fractale simple.

### Exercice 4

Simuler l’équation logistique pour plusieurs valeurs de (r).

### Exercice 5

Construire un diagramme de bifurcation.

### Exercice 6

Implémenter Euler pour Lorenz.

### Exercice 7

Comparer plusieurs pas temporels.

### Exercice 8

Implémenter un bruit 2D.

### Exercice 9

Construire un FBM.

### Exercice 10

Ajouter un domain warp.

### Exercice 11

Transformer un bruit en heightmap.

### Exercice 12

Générer un terrain 3D.

### Exercice 13

Créer une végétation L-system.

### Exercice 14

Piloter des particules par un champ vectoriel.

### Exercice 15

Créer une expérience interactive combinant fractale et système dynamique.

# 145 — MAÎTRISE CONCEPTUELLE

À la fin de l’étude du Domaine K, il faut pouvoir expliquer clairement la différence entre :

- fractale ;
- récursion ;
- auto-similarité ;
- bruit ;
- pseudo-aléatoire ;
- système dynamique ;
- chaos ;
- attracteur ;
- bifurcation ;
- stabilité ;
- système discret ;
- système continu.

# 146 — MAÎTRISE ALGORITHMIQUE

Il faut savoir reconnaître les architectures :

Récursion  
→ fractale  
<br/>Réécriture  
→ L-system  
<br/>Transformations  
→ IFS  
<br/>Itération complexe  
→ Mandelbrot / Julia  
<br/>Évolution temporelle  
→ système dynamique  
<br/>Champ scalaire  
→ bruit  
<br/>Champ multi-échelle  
→ FBM  
<br/>Champ vectoriel  
→ particules / flux  
<br/>Équation différentielle  
→ simulation

# 147 — MAÎTRISE D’INGÉNIERIE

Il faut également savoir décider :

- CPU ou GPU ;
- pré-calcul ou temps réel ;
- résolution ;
- précision ;
- cache ;
- seed ;
- LOD ;
- chunking ;
- nombre d’itérations ;
- intégrateur ;
- niveau de détail.

# 148 — MAÎTRISE CRÉATIVE

Le niveau avancé consiste à ne plus demander :

« Quelle fractale puis-je dessiner ? »

mais :

« Quel phénomène ou quelle expérience puis-je construire à partir d’une règle mathématique ? »

Cette différence est importante.

# 149 — MOTEUR DE CRÉATIVITÉ POUR UNE IA

Lorsqu’une IA rencontre un besoin logiciel, elle peut suivre :

BESOIN  
↓  
Quelle structure ?  
↓  
Quelle évolution ?  
↓  
Quelle variation ?  
↓  
Quelle échelle ?  
↓  
Quelle interaction ?  
↓  
Quelle représentation ?

Puis tester :

Fractale ?  
Bruit ?  
Dynamique ?  
Chaos ?  
Automate ?  
Champ ?  
L-system ?  
IFS ?  
Combinaison ?

# 150 — EXEMPLE DE RAISONNEMENT CRÉATIF

Besoin :

« Je veux une forêt qui ne ressemble jamais exactement à une autre. »

Analyse :

Structure  
→ L-system  
<br/>Variation  
→ bruit / seed  
<br/>Échelle  
→ récursivité  
<br/>Placement  
→ bruit spatial  
<br/>Croissance  
→ règles dynamiques  
<br/>Rendu  
→ instancing / GPU

Résultat :

Forêt procédurale déterministe  
+  
variation contrôlée  
+  
croissance simulée

# 151 — AUTRE EXEMPLE

Besoin :

« Je veux un fond animé organique qui réagisse à la souris. »

Analyse :

Structure  
→ champ de bruit  
<br/>Complexité  
→ FBM  
<br/>Déformation  
→ domain warping  
<br/>Temps  
→ bruit animé  
<br/>Interaction  
→ perturbation par pointeur  
<br/>Rendu  
→ shader GPU

# 152 — AUTRE EXEMPLE

Besoin :

« Je veux une visualisation qui semble vivante mais qui reste mathématiquement déterministe. »

Analyse :

Système dynamique  
+  
seed  
+  
paramètres  
+  
particules  
+  
rendu GPU

Le système peut paraître organique tout en étant parfaitement reproductible.

# 153 — AUTRE EXEMPLE

Besoin :

« Je veux générer automatiquement des environnements différents à partir d’un seul identifiant. »

Solution conceptuelle :

World Seed  
↓  
Terrain Seed  
↓  
Biome Seed  
↓  
Vegetation Seed  
↓  
Structure Seed  
↓  
Weather Seed

Une même seed globale permet de reconstruire le monde.

# 154 — PRINCIPES DE QUALITÉ

Un système procédural de qualité doit être :

### Déterministe

lorsque la reproductibilité est nécessaire.

### Paramétrable

les variables importantes doivent être contrôlables.

### Stable

les paramètres ne doivent pas provoquer de comportements incontrôlés.

### Performant

le coût doit être compatible avec la plateforme.

### Lisible

les résultats doivent rester compréhensibles.

### Extensible

de nouveaux générateurs doivent pouvoir être ajoutés.

### Testable

les résultats doivent pouvoir être reproduits.

# 155 — PRINCIPES DE RECHERCHE

Lorsqu’une technique avancée est nécessaire, la recherche externe doit partir du concept mathématique précis.

Exemple :

Besoin :  
nuages réalistes  
↓  
bruit volumétrique  
↓  
FBM  
↓  
ray marching  
↓  
density field  
↓  
recherche technique spécialisée

et non :

"comment faire de beaux nuages"

Le modèle mathématique permet d’obtenir des recherches beaucoup plus précises.

# 156 — STRATÉGIE DE RECHERCHE POUR UNE IA

Une IA utilisant ce document doit pouvoir produire :

1\. Concept identifié  
2\. Définition mathématique  
3\. Algorithme  
4\. Paramètres  
5\. Représentation numérique  
6\. Technique informatique  
7\. Technologie possible  
8\. Contraintes  
9\. Optimisations  
10\. Recherche externe ciblée

# 157 — RELATION AVEC LES TECHNOLOGIES

Les mathématiques peuvent être implémentées avec :

- Python ;
- NumPy ;
- JavaScript ;
- TypeScript ;
- Canvas ;
- SVG ;
- WebGL ;
- GLSL ;
- Three.js ;
- React Three Fiber ;
- moteurs de jeu ;
- compute shaders ;
- systèmes GPU.

Le choix dépend du problème.

# 158 — TECHNOLOGIE AU SERVICE DU MODÈLE

La séquence recommandée reste :

MATHÉMATIQUES  
↓  
ALGORITHME  
↓  
REPRÉSENTATION  
↓  
CONTRAINTES  
↓  
TECHNOLOGIE

et non :

TECHNOLOGIE  
↓  
EFFET  
↓  
JUSTIFICATION MATHÉMATIQUE

# 159 — RÉSUMÉ DES TROIS PILIERS

## FRACTALES

Répondent principalement à :

Comment générer une structure complexe à partir d’une règle répétée ou auto-similaire ?

## SYSTÈMES DYNAMIQUES

Répondent principalement à :

Comment un état évolue-t-il au cours du temps ?

## CHAOS

Répond principalement à :

Comment des règles déterministes peuvent-elles produire des comportements extrêmement complexes et sensibles ?

# 160 — RÉSUMÉ DU BRUIT PROCÉDURAL

Le bruit répond principalement à :

Comment produire une variation structurée, contrôlable et souvent cohérente spatialement ou temporellement ?

Il constitue un outil fondamental de génération.

# 161 — SYNTHÈSE GÉNÉRALE

Le Domaine K peut être résumé par quatre chaînes fondamentales.

### Fractales

Règle  
↓  
Itération  
↓  
Auto-similarité  
↓  
Complexité

### Dynamique

État  
↓  
Règle d’évolution  
↓  
Nouvel état  
↓  
Trajectoire

### Chaos

Règle déterministe  
↓  
Non-linéarité  
↓  
Sensibilité  
↓  
Complexité

### Génération procédurale

Seed  
+  
Fonction  
+  
Paramètres  
↓  
Structure

# 162 — CARTE MENTALE FINALE

DOMAINE K  
│  
├── FRACTALES  
│ ├── Mandelbrot  
│ ├── Julia  
│ ├── Sierpiński  
│ ├── Koch  
│ ├── Dragon  
│ ├── Hilbert  
│ ├── Peano  
│ ├── L-system  
│ ├── IFS  
│ └── Dimension fractale  
│  
├── SYSTÈMES DYNAMIQUES  
│ ├── État  
│ ├── Trajectoire  
│ ├── Point fixe  
│ ├── Cycle  
│ ├── Stabilité  
│ ├── Attracteur  
│ └── Équations différentielles  
│  
├── CHAOS  
│ ├── Logistique  
│ ├── Bifurcation  
│ ├── Sensibilité  
│ ├── Lyapunov  
│ └── Lorenz  
│  
├── BRUIT  
│ ├── Value  
│ ├── Perlin  
│ ├── Simplex  
│ ├── Worley  
│ ├── FBM  
│ ├── Turbulence  
│ └── Domain Warping  
│  
└── INFORMATIQUE  
├── Génération procédurale  
├── Terrains  
├── Nuages  
├── Végétation  
├── Textures  
├── Particules  
├── Fluides  
├── Shaders  
├── 3D  
├── Jeux  
├── Simulation  
└── Art génératif

# 163 — CHECKLIST DE MAÎTRISE DU DOMAINE K

Avant de considérer le domaine comme maîtrisé, il faut être capable de :

- expliquer ce qu’est une fractale ;
- expliquer l’auto-similarité ;
- expliquer la récursivité fractale ;
- générer Sierpiński ;
- générer Koch ;
- expliquer Mandelbrot ;
- expliquer Julia ;
- comprendre les nombres complexes utilisés dans ces systèmes ;
- expliquer L-systems ;
- comprendre IFS ;
- calculer une dimension de similarité simple ;
- comprendre le box-counting ;
- définir un système dynamique ;
- distinguer discret et continu ;
- expliquer un point fixe ;
- expliquer stabilité et instabilité ;
- comprendre un attracteur ;
- expliquer une bifurcation ;
- expliquer le chaos déterministe ;
- comprendre la sensibilité aux conditions initiales ;
- simuler l’équation logistique ;
- construire un diagramme de bifurcation ;
- comprendre Lorenz ;
- utiliser une intégration numérique élémentaire ;
- comprendre les limites d’Euler ;
- expliquer le bruit procédural ;
- distinguer bruit et fractale ;
- comprendre Perlin Noise ;
- comprendre Simplex Noise ;
- comprendre Worley Noise ;
- construire du FBM ;
- comprendre le domain warping ;
- générer une heightmap ;
- construire un terrain procédural ;
- comprendre la génération végétale par L-system ;
- comprendre les champs vectoriels ;
- piloter des particules avec un champ ;
- comprendre le rôle des shaders ;
- distinguer CPU et GPU ;
- utiliser une seed ;
- assurer la reproductibilité ;
- contrôler la complexité ;
- utiliser le LOD ;
- comprendre le chunking ;
- concevoir un générateur modulaire ;
- transformer une équation en algorithme ;
- transformer un algorithme en visualisation ;
- transformer une visualisation en système interactif.

# 164 — SYNTHÈSE FINALE

Le Domaine K introduit une idée extrêmement importante pour l’informatique :

**La complexité visuelle ou comportementale n’exige pas nécessairement une description complexe.**

Une règle simple peut produire :

forme complexe

Une règle locale peut produire :

structure émergente

Une équation simple peut produire :

comportement chaotique

Une fonction de bruit peut produire :

environnement crédible

Un système dynamique peut produire :

animation vivante

Et la combinaison de plusieurs mécanismes peut produire :

MATHÉMATIQUES  
+  
ALGORITHMES  
+  
GÉNÉRATION PROCÉDURALE  
+  
SIMULATION  
+  
GPU  
+  
INTERACTION  
\=  
EXPÉRIENCES NUMÉRIQUES COMPLEXES

Le domaine ne doit donc pas être étudié uniquement comme une branche de mathématiques visuelles.

Il constitue également une boîte à outils pour concevoir :

- des mondes ;
- des environnements ;
- des simulations ;
- des systèmes émergents ;
- des visualisations ;
- des expériences interactives ;
- des œuvres génératives ;
- des moteurs procéduraux ;
- des comportements artificiels ;
- des interfaces dynamiques.

La règle fondamentale à retenir est :

PHÉNOMÈNE  
↓  
MODÈLE  
↓  
MATHÉMATIQUES  
↓  
RÈGLE  
↓  
ITÉRATION / ÉVOLUTION  
↓  
ALGORITHME  
↓  
REPRÉSENTATION  
↓  
INTERACTION  
↓  
APPLICATION

Et lorsqu’une idée logicielle paraît difficile à concevoir directement, il faut se demander :

**« Puis-je la décrire comme une règle, un champ, une transformation, une itération ou un système qui évolue ? »**

C’est précisément à cet endroit que le Domaine K devient une source d’innovation.

# 165 — POSITION DU DOMAINE K DANS L’ENSEMBLE

Le Domaine K complète les domaines précédents en ajoutant une dimension essentielle :

A — LOGIQUE  
→ raisonner  
<br/>B — NOMBRES  
→ calculer  
<br/>C — ALGÈBRE LINÉAIRE  
→ représenter et transformer  
<br/>D — GÉOMÉTRIE  
→ représenter l’espace  
<br/>E — GRAPHES  
→ connecter et parcourir  
<br/>F — COMBINATOIRE  
→ construire et compter  
<br/>G — PROBABILITÉS  
→ modéliser l’incertitude  
<br/>H — STATISTIQUES  
→ apprendre à partir des données  
<br/>I — CALCUL DIFFÉRENTIEL  
→ mesurer les variations  
<br/>J — OPTIMISATION  
→ rechercher le meilleur choix  
<br/>K — FRACTALES, CHAOS & SYSTÈMES DYNAMIQUES  
→ générer, évoluer, émerger et simuler

Le Domaine K devient ainsi le domaine où les mathématiques cessent d’être uniquement une description statique d’un objet et deviennent un **moteur de génération, d’évolution et de comportement**.

# 166 — FORMULE DE RÉFÉRENCE

Pour toute future application utilisant ce domaine :

\[ \]

Cette chaîne constitue la référence opérationnelle du **Domaine K**.