# DOCUMENT L — ANALYSE NUMÉRIQUE

## Référence complète pour transformer les mathématiques en calculs fiables sur ordinateur

# 0\. PRÉDISPOSITION D’INTÉGRATION — COMMENT UTILISER CE DOCUMENT

**Domaine : Analyse numérique**

Ce document décrit les méthodes permettant de **représenter, approximer, calculer et résoudre numériquement des problèmes mathématiques sur ordinateur**.

Il doit être considéré comme une référence lorsqu’un problème contient une tension entre :

\[ \]

et

\[ . \]

L’analyse numérique répond notamment aux questions suivantes :

- Comment représenter un nombre réel sur une machine ?
- Quelle erreur est introduite par cette représentation ?
- Comment calculer une solution lorsqu’aucune formule exacte exploitable n’existe ?
- Comment approcher une fonction à partir de quelques valeurs ?
- Comment résoudre numériquement une équation ?
- Comment résoudre un système linéaire ?
- Comment calculer une intégrale ?
- Comment approximer une dérivée ?
- Comment simuler une équation différentielle ?
- Comment savoir si une méthode converge ?
- À quelle vitesse converge-t-elle ?
- Une méthode convergente peut-elle être numériquement instable ?
- Comment mesurer et contrôler l’erreur ?
- Quel compromis choisir entre précision, stabilité, mémoire et temps de calcul ?

### Règle d’utilisation par une IA ou un système

Lorsqu’une demande concerne un calcul mathématique destiné à être exécuté par un logiciel, le système doit considérer ce document comme une **couche de traduction entre le modèle mathématique et son implémentation numérique**.

Il doit identifier :

1.  le problème mathématique exact ;
2.  la représentation informatique utilisée ;
3.  la source potentielle d’erreur ;
4.  la méthode numérique appropriée ;
5.  les conditions de convergence ;
6.  la stabilité de la méthode ;
7.  le coût algorithmique ;
8.  le critère d’arrêt ;
9.  la précision recherchée ;
10. la manière de vérifier le résultat.

Le système ne doit donc jamais considérer :

\[ \]

sans analyser les conditions du calcul.

### Principe directeur

\[ \]

Ce domaine constitue notamment une base pour :

- la simulation scientifique ;
- l’intelligence artificielle ;
- la robotique ;
- la finance quantitative ;
- les jeux vidéo ;
- la 2D/3D ;
- les moteurs physiques ;
- le traitement du signal ;
- les systèmes embarqués ;
- la météo et les simulations environnementales ;
- les systèmes de contrôle ;
- l’ingénierie ;
- la visualisation scientifique ;
- les logiciels scientifiques ;
- le calcul haute performance.

# 1\. IDENTITÉ DU DOMAINE

L’analyse numérique est la branche des mathématiques et de l’informatique qui étudie les méthodes permettant de **résoudre approximativement des problèmes mathématiques à l’aide d’algorithmes numériques**.

Elle se situe à l’intersection de :

- l’analyse mathématique ;
- l’algèbre ;
- l’optimisation ;
- les probabilités ;
- les équations différentielles ;
- l’informatique ;
- l’algorithmique ;
- l’architecture des ordinateurs.

Son objectif n’est pas simplement de produire une approximation.

Il faut produire une approximation :

- suffisamment précise ;
- calculable ;
- stable ;
- convergente ;
- efficace ;
- vérifiable.

# 2\. PLACE DANS LA CARTOGRAPHIE MATHÉMATIQUE

Les domaines précédents fournissent les objets mathématiques.

L’analyse numérique explique comment les faire fonctionner sur une machine.

On peut représenter la chaîne :

\[ \]

avec notamment :

- A : logique et fondements ;
- B : théorie des nombres ;
- C : algèbre linéaire ;
- D : géométrie computationnelle ;
- E : graphes et algorithmes sur graphes ;
- F : combinatoire et optimisation combinatoire ;
- G : probabilités ;
- H : statistiques ;
- I : calcul différentiel ;
- J : optimisation ;
- K : fractales, chaos et systèmes dynamiques ;
- L : analyse numérique.

### Fonction spécifique du domaine L

Les domaines précédents peuvent produire :

\[ f(x),Ax=b,f,\_a^b f(x),dx,=f(t,y) \]

mais L pose la question :

**Comment calculer ces objets réellement sur une machine avec des ressources finies et une précision finie ?**

# 3\. LE PRINCIPE FONDAMENTAL : L’ORDINATEUR CALCULE DES APPROXIMATIONS

Sur papier, on peut écrire :

\[ \]

exactement.

Un ordinateur utilisant une représentation binaire à précision finie ne peut généralement pas représenter exactement ce réel.

Il stocke une approximation :

\[ x. \]

Cette différence est fondamentale.

\[ \]

dans la plupart des cas.

# 4\. ERREUR ABSOLUE ET ERREUR RELATIVE

## 4.1 Erreur absolue

Si (x) est la valeur exacte et () la valeur calculée :

\[ E_a=|x-|. \]

Exemple :

\[ x=10 \]

et

\[ =9.99. \]

Alors :

\[ E_a=0.01. \]

## 4.2 Erreur relative

Lorsque (x) :

\[ E_r=. \]

Elle permet de comparer l’erreur à l’échelle du résultat.

## 4.3 Erreur relative en pourcentage

\[ E_r(%)= 100. \]

# 5\. SOURCES D’ERREUR NUMÉRIQUE

Il faut distinguer plusieurs erreurs.

## 5.1 Erreur de modèle

Le modèle mathématique lui-même peut être une approximation du phénomène réel.

\[ . \]

## 5.2 Erreur de données

Les données initiales peuvent être mesurées ou enregistrées avec une précision limitée.

## 5.3 Erreur de représentation

La machine représente les nombres avec une précision finie.

## 5.4 Erreur d’arrondi

Une opération produit un résultat qui doit être arrondi.

## 5.5 Erreur de troncature

Une expression infinie ou continue est remplacée par une approximation finie.

Exemple :

\[ e^x = \_{k=0}<sup>{}\\frac{x</sup>k}{k!} \]

est approximée par :

\[ e^x \_{k=0}<sup>{N}\\frac{x</sup>k}{k!}. \]

Le terme restant constitue une erreur de troncature.

## 5.6 Erreur algorithmique

Une méthode numérique peut produire une approximation imparfaite même avec des calculs individuellement exacts.

# 6\. ARITHMÉTIQUE EN VIRGULE FLOTTANTE

La représentation informatique classique d’un réel utilise une structure proche de :

\[ x=mb^e. \]

Dans les systèmes binaires :

\[ x=m^e. \]

Une représentation flottante possède notamment :

- un signe ;
- un exposant ;
- une mantisse/significande ;
- une précision finie.

# 7\. PRÉCISION FINIE

Il existe une différence fondamentale entre :

\[ \]

et l’ensemble fini des nombres représentables par une machine.

Ainsi :

\[ \]

est continu et infini tandis que les nombres flottants disponibles sont finis.

# 8\. MACHINE EPSILON

La **machine epsilon** caractérise approximativement la résolution relative de l’arithmétique flottante autour de (1).

Pour une représentation de précision (p), on rencontre des quantités de l’ordre de :

\[ \_{}^{-p} \]

selon la convention utilisée.

Elle permet d’estimer le niveau de précision relatif de la machine.

# 9\. PROBLÈMES CLASSIQUES DE VIRGULE FLOTTANTE

## 9.1 Addition de nombres d’échelles différentes

Additionner :

\[ 10^{20}+1 \]

peut conduire à perdre l’information portée par (1).

## 9.2 Soustraction catastrophique

Lorsque deux nombres presque égaux sont soustraits :

\[ x-y \]

les chiffres significatifs communs peuvent s’annuler.

On parle de :

\[ \]

ou **catastrophic cancellation**.

## 9.3 Associativité non garantie

En arithmétique exacte :

\[ (a+b)+c=a+(b+c). \]

En flottant :

\[ ((a+b)+c) \]

peut être différent de :

\[ (a+(b+c)). \]

## 9.4 Overflow

Une valeur dépasse la plage représentable.

## 9.5 Underflow

Une valeur devient trop petite pour être représentée normalement.

# 10\. STABILITÉ NUMÉRIQUE

Une méthode est numériquement stable lorsque les petites perturbations introduites par le calcul ne provoquent pas une amplification incontrôlée des erreurs.

Il faut distinguer :

### Stabilité

Comportement des erreurs introduites par l’algorithme.

### Conditionnement

Sensibilité intrinsèque du problème aux perturbations des données.

### Convergence

Capacité de l’approximation à tendre vers la solution recherchée.

Ces trois notions sont différentes.

\[ \]

# 11\. CONDITIONNEMENT

Un problème est bien conditionné lorsque de petites perturbations des données provoquent de petites variations du résultat.

Il est mal conditionné lorsque :

\[ . \]

L’analyse numérique doit donc toujours distinguer :

problème difficile intrinsèquement

de

algorithme mauvais pour un problème donné.

# 12\. CONVERGENCE

Une méthode produit une suite :

\[ x_0,x_1,x_2, \]

qui doit idéalement vérifier :

\[ x_kx^. \]

On étudie :

- si elle converge ;
- vers quelle solution ;
- sous quelles conditions ;
- à quelle vitesse.

# 13\. ORDRE DE CONVERGENCE

Si :

\[ e_k=|x_k-x^| \]

et :

\[ e_{k+1}C e_k^p, \]

alors (p) représente l’ordre de convergence.

### Convergence linéaire

\[ p=1. \]

### Convergence quadratique

\[ p=2. \]

### Convergence superlinéaire

La vitesse devient supérieure à une convergence linéaire classique sans nécessairement être quadratique.

# 14\. CRITÈRES D’ARRÊT

Une méthode itérative doit savoir quand s’arrêter.

Critères possibles :

\[ |x_{k+1}-x_k|< \]

ou :

\[ |F(x_k)|< \]

ou :

\[ {(1,|x_k|)} <. \]

Il est généralement préférable d’utiliser des critères combinant :

- tolérance absolue ;
- tolérance relative ;
- résidu ;
- nombre maximal d’itérations.

# 15\. RÉSOLUTION NUMÉRIQUE D’ÉQUATIONS

Le problème fondamental est :

\[ f(x)=0. \]

Une solution peut être impossible à exprimer simplement analytiquement.

On cherche donc :

\[ x^x. \]

# 16\. MÉTHODE DE BISSECTION

Supposons :

\[ f(a)f(b)<0. \]

Si (f) est continue, il existe au moins une racine dans :

\[ \[a,b\]. \]

On calcule :

\[ m=. \]

Puis on conserve le sous-intervalle dans lequel le changement de signe subsiste.

### Avantage

Méthode très robuste.

### Inconvénient

Convergence relativement lente.

# 17\. MÉTHODE DE NEWTON-RAPHSON

La méthode de Newton utilise :

\[ \]

Elle repose sur l’approximation locale de (f) par sa tangente.

## 17.1 Interprétation géométrique

On part de :

\[ x_n. \]

On trace la tangente au graphe de (f).

L’intersection de cette tangente avec l’axe (x) donne :

\[ x_{n+1}. \]

## 17.2 Avantage

Près d’une racine simple et sous des conditions favorables :

\[ . \]

## 17.3 Risques

Newton peut :

- diverger ;
- osciller ;
- converger vers une autre racine ;
- devenir instable lorsque (f’(x)) est proche de zéro ;
- être très dépendante de l’initialisation.

# 18\. MÉTHODE DE LA SÉCANTE

La dérivée est approximée par une pente :

\[ f’(x_n) {x_n-x_{n-1}}. \]

On obtient une méthode ne nécessitant pas explicitement (f’).

Elle est utile lorsque la dérivée est difficile ou coûteuse à calculer.

# 19\. MÉTHODES HYBRIDES

Les méthodes modernes peuvent combiner :

- robustesse de la bissection ;
- rapidité de Newton ;
- comportement de la sécante.

Une stratégie robuste consiste à utiliser une méthode de type Newton lorsque son pas est sûr, puis à revenir à une méthode de bracketing lorsqu’il ne l’est pas.

# 20\. RÉSOLUTION DE SYSTÈMES LINÉAIRES

Un problème fondamental est :

\[ Ax=b. \]

Il apparaît partout :

- simulation ;
- optimisation ;
- graphisme ;
- physique ;
- machine learning ;
- statistiques ;
- ingénierie ;
- systèmes de contrôle.

# 21\. ÉLIMINATION DE GAUSS

L’élimination de Gauss transforme progressivement :

\[ Ax=b \]

en un système triangulaire.

On résout ensuite par substitution arrière.

# 22\. FACTORISATION LU

On écrit :

\[ A=LU. \]

où :

- (L) est triangulaire inférieure ;
- (U) est triangulaire supérieure.

La résolution devient :

\[ Ly=b \]

puis :

\[ Ux=y. \]

# 23\. PIVOTAGE

Pour améliorer la stabilité numérique, on utilise souvent le pivotage.

Une factorisation peut alors être représentée :

\[ PA=LU. \]

où (P) représente une permutation.

Le pivotage réduit notamment certains risques liés aux petits pivots.

# 24\. FACTORISATION DE CHOLESKY

Pour une matrice symétrique définie positive :

\[ A=LL^T. \]

Cette factorisation est efficace et numériquement intéressante dans les problèmes appropriés.

# 25\. QR

On peut écrire :

\[ A=QR \]

avec :

- (Q) orthogonale ;
- (R) triangulaire supérieure.

La factorisation QR est particulièrement importante pour :

- les moindres carrés ;
- les problèmes de valeurs propres ;
- certaines méthodes numériques robustes.

# 26\. SYSTÈMES LINÉAIRES CREUX

Une matrice creuse possède beaucoup de zéros.

Il serait inutile de stocker explicitement tous ces zéros.

Structures courantes :

- COO ;
- CSR ;
- CSC.

Cette représentation devient essentielle pour les grands systèmes scientifiques.

# 27\. MÉTHODES DIRECTES ET ITÉRATIVES

### Méthodes directes

Cherchent une solution en un nombre fini d’opérations idéalement exactes en arithmétique exacte.

Exemples :

- Gauss ;
- LU ;
- Cholesky ;
- QR.

### Méthodes itératives

Produisent :

\[ x_0,x_1,x_2, \]

jusqu’à atteindre une précision acceptable.

Exemples :

- Jacobi ;
- Gauss-Seidel ;
- gradient ;
- gradient conjugué ;
- GMRES.

# 28\. MÉTHODE DE JACOBI

Pour :

\[ Ax=b, \]

on isole chaque variable puis on utilise les valeurs de l’itération précédente.

Sous certaines conditions, notamment de domination diagonale, la méthode converge.

# 29\. GAUSS-SEIDEL

Contrairement à Jacobi, les nouvelles valeurs calculées sont immédiatement réutilisées.

Cela peut accélérer la convergence.

# 30\. GRADIENT CONJUGUÉ

Pour les systèmes :

\[ Ax=b \]

avec (A) symétrique définie positive, le gradient conjugué est particulièrement important.

Il transforme le problème linéaire en problème d’optimisation :

\[ \_x 12x<sup>TAx-b</sup>Tx. \]

# 31\. PRÉCONDITIONNEMENT

Si un système converge lentement, on peut transformer le problème grâce à une matrice (M) qui rend le système plus facile à résoudre.

L’objectif est d’obtenir un système équivalent mieux conditionné.

Le préconditionnement est crucial pour :

- grandes matrices ;
- matrices creuses ;
- simulations physiques ;
- éléments finis ;
- calcul scientifique.

# 32\. INTERPOLATION

L’interpolation consiste à construire une fonction passant exactement par des données connues.

On dispose de :

\[ (x_0,y_0),,(x_n,y_n). \]

On cherche (p(x)) tel que :

\[ p(x_i)=y_i. \]

# 33\. INTERPOLATION POLYNOMIALE

### Forme de Lagrange

\[ p(x)= \_{i=0}^{n} y_iL_i(x) \]

avec :

\[ L_i(x)= \_{ji} . \]

# 34\. FORMULE DE NEWTON

On peut utiliser les différences divisées :

\[ p(x) = a_0+ a_1(x-x_0)

- a_2(x-x_0)(x-x_1) + \]

Cette forme est pratique pour ajouter progressivement de nouveaux points.

# 35\. PROBLÈME DE RUNGE

Une interpolation polynomiale de haut degré sur des points mal choisis peut présenter de fortes oscillations.

Cela montre que :

\[ . \]

# 36\. SPLINES

Une spline construit plusieurs polynômes de faible degré raccordés avec certaines conditions de continuité.

Les splines cubiques sont particulièrement utilisées.

Elles sont importantes pour :

- courbes graphiques ;
- animation ;
- interpolation de trajectoires ;
- CAD ;
- visualisation ;
- traitement de données.

# 37\. APPROXIMATION

L’interpolation impose :

\[ p(x_i)=f(x_i). \]

L’approximation cherche plutôt :

\[ p(x)f(x) \]

selon un critère donné.

# 38\. MOINDRES CARRÉS

On cherche à minimiser :

\[ \_i (y_i-f(x_i))^2. \]

Sous forme matricielle :

\[ \_x|Ax-b|\_2^2. \]

Cette méthode est fondamentale en :

- régression ;
- calibration ;
- traitement du signal ;
- machine learning ;
- estimation de paramètres.

# 39\. APPROXIMATION ET RÉGULARISATION

Une approximation peut être stabilisée par une pénalisation.

Exemple :

\[ \_x |Ax-b|\_2^2+ |x|\_2^2. \]

C’est une forme de régularisation de Tikhonov.

Elle limite notamment les solutions excessivement sensibles au bruit.

# 40\. INTÉGRATION NUMÉRIQUE

On cherche :

\[ I= \_a^b f(x),dx. \]

Lorsque l’intégrale exacte est impossible ou trop coûteuse, on l’approxime numériquement.

# 41\. RÈGLE DES RECTANGLES

Approximation :

\[ \_a^b f(x),dx \_i f(x_i)x. \]

# 42\. RÈGLE DU MILIEU

On évalue la fonction au milieu de chaque intervalle.

Cette méthode peut être plus précise que l’évaluation systématique aux extrémités.

# 43\. RÈGLE DES TRAPÈZES

\[ \_a^b f(x),dx \[f(a)+f(b)\]. \]

Pour plusieurs subdivisions :

\[ I h . \]

# 44\. MÉTHODE DE SIMPSON

Pour des subdivisions adaptées :

\[ \_a^b f(x),dx . \]

Elle utilise une approximation quadratique locale.

# 45\. QUADRATURE GAUSSIENNE

Au lieu de choisir uniformément les points, on choisit :

- des nœuds ;
- des poids ;

afin d’obtenir une précision élevée avec relativement peu d’évaluations.

La quadrature de Gauss est particulièrement utile lorsque l’évaluation de (f) est coûteuse.

# 46\. INTÉGRATION ADAPTATIVE

Toutes les régions d’une fonction ne nécessitent pas la même précision.

Une méthode adaptative subdivise davantage les zones où :

- la fonction varie rapidement ;
- la courbure est forte ;
- l’erreur estimée est élevée.

Cette idée est extrêmement importante en calcul scientifique.

# 47\. DIFFÉRENCES FINIES

Les dérivées peuvent être approximées à partir de valeurs discrètes.

## 47.1 Différence avant

\[ f’(x) . \]

## 47.2 Différence arrière

\[ f’(x) . \]

## 47.3 Différence centrée

\[ f’(x) . \]

La différence centrée offre généralement une meilleure précision.

# 48\. ORDRE D’APPROXIMATION

Une méthode peut avoir une erreur :

\[ O(h) \]

ou :

\[ O(h^2) \]

ou :

\[ O(h^4). \]

Plus l’ordre est élevé, plus l’erreur de discrétisation diminue rapidement lorsque :

\[ h. \]

# 49\. COMPROMIS ENTRE DISCRÉTISATION ET ARRONDI

Réduire (h) n’améliore pas toujours le résultat.

En diminuant (h) :

\[ \]

mais :

\[ \]

et les erreurs d’arrondi peuvent devenir dominantes.

On peut donc avoir une courbe d’erreur en forme de compromis :

\[ \]

approximativement.

# 50\. ÉQUATIONS DIFFÉRENTIELLES ORDINAIRES

Une EDO peut s’écrire :

\[ =f(t,y). \]

Avec :

\[ y(t_0)=y_0. \]

# 51\. MÉTHODE D’EULER

\[ y_{n+1} = y_n+ hf(t_n,y_n). \]

Elle est simple mais relativement peu précise.

# 52\. RUNGE-KUTTA

Les méthodes Runge-Kutta utilisent plusieurs évaluations de la dérivée par pas.

La méthode RK4 classique possède un ordre élevé tout en restant relativement simple.

Elle est largement utilisée pour :

- physique ;
- robotique ;
- jeux ;
- simulation ;
- animation ;
- dynamique de systèmes.

# 53\. STABILITÉ DES MÉTHODES D’EDO

Une méthode peut avoir une bonne précision locale tout en étant instable sur certaines équations.

La stabilité devient critique lorsque les systèmes possèdent des échelles temporelles très différentes.

On parle notamment de :

\[ \]

ou **stiff problems**.

Ils nécessitent parfois des méthodes implicites.

# 54\. ÉQUATIONS DIFFÉRENTIELLES PARTIELLES

Les EDP peuvent être discrétisées avec :

- différences finies ;
- éléments finis ;
- volumes finis ;
- méthodes spectrales.

Elles permettent de simuler :

- chaleur ;
- fluides ;
- élasticité ;
- électromagnétisme ;
- diffusion ;
- propagation d’ondes.

# 55\. MÉTHODE DES ÉLÉMENTS FINIS

Le domaine spatial est divisé en éléments.

La solution continue est approximée par des fonctions de base locales.

Le problème devient généralement un système :

\[ K u=f. \]

Cette méthode est centrale en ingénierie numérique.

# 56\. MÉTHODE DES VOLUMES FINIS

Les équations sont intégrées sur des volumes de contrôle.

Cette méthode est particulièrement adaptée aux lois de conservation et à la mécanique des fluides.

# 57\. MÉTHODES SPECTRALES

Une fonction est représentée à l’aide de fonctions globales, souvent :

- polynômes ;
- séries de Fourier.

Elles peuvent fournir une très haute précision pour les problèmes suffisamment réguliers.

# 58\. MÉTHODES DE MONTE-CARLO

Monte-Carlo utilise l’échantillonnage aléatoire pour approximer une quantité.

Pour une espérance :

\[ I=E\[f(X)\], \]

on peut utiliser :

\[ I_N = 1N \_{i=1}^{N}f(X_i). \]

Sous des conditions classiques :

\[ I_NI. \]

# 59\. ERREUR MONTE-CARLO

L’erreur statistique classique décroît approximativement comme :

\[ O(). \]

Cela signifie qu’obtenir beaucoup plus de précision peut nécessiter énormément plus d’échantillons.

# 60\. AVANTAGE DE MONTE-CARLO

L’une de ses grandes forces est sa capacité à traiter des intégrales ou problèmes de grande dimension.

Dans certaines situations :

\[ \]

rend les méthodes déterministes classiques très coûteuses, tandis que Monte-Carlo reste exploitable.

# 61\. RÉDUCTION DE VARIANCE

Techniques importantes :

- importance sampling ;
- stratification ;
- variables antithétiques ;
- contrôle de variance ;
- échantillonnage préférentiel.

# 62\. APPLICATION À LA FINANCE

Monte-Carlo est notamment utilisé pour :

- évaluer des produits financiers ;
- simuler des trajectoires ;
- estimer des risques ;
- calculer des espérances conditionnelles.

# 63\. VALEURS PROPRES ET VECTEURS PROPRES

On cherche :

\[ Av=v. \]

Les valeurs propres interviennent dans :

- stabilité ;
- systèmes dynamiques ;
- PCA ;
- compression ;
- mécanique ;
- analyse de matrices ;
- simulation ;
- systèmes de contrôle.

# 64\. MÉTHODE DE LA PUISSANCE

Pour certaines matrices, on peut approximer la valeur propre dominante par :

\[ x_{k+1}= . \]

# 65\. ALGORITHME QR

Les méthodes QR constituent une famille importante pour calculer les valeurs propres.

# 66\. ANALYSE NUMÉRIQUE ET OPTIMISATION

Le domaine J définit le problème :

\[ \_x f(x). \]

Le domaine L explique comment le résoudre réellement.

On rencontre notamment :

- descente de gradient ;
- Newton ;
- quasi-Newton ;
- gradient conjugué ;
- méthodes proximal ;
- méthodes sous contraintes ;
- solveurs numériques.

# 67\. NEWTON POUR L’OPTIMISATION

Pour :

\[ f(x), \]

on utilise :

\[ x_{k+1} = x_k- H_f(x_k)^{-1}f(x_k). \]

En pratique, on évite généralement de calculer explicitement :

\[ H^{-1}. \]

On résout plutôt :

\[ H=-f \]

puis :

\[ x_{k+1}=x_k+. \]

# 68\. DIFFÉRENCIATION AUTOMATIQUE

Il faut distinguer :

### Différentiation symbolique

Manipulation exacte d’expressions mathématiques.

### Différences finies

Approximation numérique des dérivées.

### Différentiation automatique

Calcul systématique des dérivées en appliquant la règle de chaîne aux opérations exécutées.

Elle est fondamentale en :

- deep learning ;
- optimisation ;
- simulation ;
- calcul scientifique.

# 69\. DIFFÉRENCIATION AUTOMATIQUE : IDÉE CENTRALE

Si :

\[ z=f(x) \]

puis :

\[ y=g(z), \]

alors :

\[ = . \]

Un programme peut construire cette chaîne de dérivations automatiquement.

C’est l’un des ponts fondamentaux entre :

\[ . \]

# 70\. MÉTHODES ITÉRATIVES : STRUCTURE GÉNÉRALE

Une méthode itérative suit généralement :

\[ x_{k+1}=(x_k). \]

On cherche un point fixe :

\[ x<sup>\=(x</sup>). \]

# 71\. POINT FIXE

Résoudre :

\[ x=(x) \]

peut être équivalent à résoudre une équation.

Si :

\[ |’(x^)|<1, \]

la méthode peut converger localement dans le cas scalaire approprié.

# 72\. ACCÉLÉRATION DE CONVERGENCE

On peut parfois accélérer une suite avec :

- extrapolation ;
- relaxation ;
- accélération d’Aitken ;
- méthode de Richardson ;
- techniques de préconditionnement ;
- multigrille.

# 73\. MULTIGRILLE

Les méthodes multigrilles exploitent différentes échelles de résolution pour éliminer efficacement les erreurs.

Elles sont extrêmement puissantes pour certains problèmes issus des EDP.

Idée :

\[ \]

peuvent devenir :

\[ . \]

# 74\. ANALYSE DE L’ERREUR

Pour une méthode numérique, on cherche à séparer :

\[ E_{} E_{}

- E_{}
- E_{}
- E_{}
- E_{}. \]

Cette décomposition permet de comprendre pourquoi un résultat est mauvais.

# 75\. RÉSILIENCE NUMÉRIQUE

Un logiciel scientifique doit prévoir :

- valeurs NaN ;
- infinis ;
- divisions proches de zéro ;
- overflow ;
- underflow ;
- systèmes mal conditionnés ;
- absence de convergence ;
- oscillations ;
- explosion numérique.

Une implémentation robuste doit détecter ces situations plutôt que simplement retourner un nombre.

# 76\. VALIDATION D’UN CALCUL NUMÉRIQUE

Un résultat numérique ne doit pas être considéré comme fiable uniquement parce que le programme s’est exécuté sans erreur.

Il faut vérifier :

### 1\. Résidu

\[ r=Ax-b. \]

### 2\. Erreur estimée

Comparer à une tolérance.

### 3\. Conservation

Vérifier les invariants physiques ou mathématiques.

### 4\. Cas limites

Tester :

- (0) ;
- valeurs très grandes ;
- valeurs très petites ;
- paramètres extrêmes.

### 5\. Comparaison analytique

Lorsque la solution exacte est connue.

### 6\. Raffinement

Augmenter la précision ou diminuer le pas et vérifier la stabilité du résultat.

# 77\. TEST DE CONVERGENCE PRATIQUE

Une technique fondamentale consiste à comparer :

\[ x_h,x_{h/2},x_{h/4}. \]

Si les résultats convergent :

\[ x_hx^, \]

on obtient une indication expérimentale de convergence.

# 78\. ANALYSE DE SENSIBILITÉ

Il faut étudier comment le résultat varie lorsque les entrées changent.

On peut examiner :

\[ . \]

ou expérimentalement :

\[ . \]

Cette analyse permet de détecter les paramètres critiques.

# 79\. NORMALISATION ET MISE À L’ÉCHELLE

Les différences d’échelle peuvent dégrader les calculs.

Si :

\[ x_110^{-10} \]

et :

\[ x_210^{10}, \]

une méthode naïve peut être mal conditionnée.

La mise à l’échelle cherche à rapprocher les ordres de grandeur.

# 80\. COMPLEXITÉ DU CALCUL NUMÉRIQUE

L’analyse numérique ne concerne pas uniquement la précision.

Il faut également étudier :

- temps ;
- mémoire ;
- nombre d’itérations ;
- coût d’une évaluation de fonction ;
- coût d’une dérivée ;
- parallélisation ;
- accès mémoire ;
- sparsité.

Une méthode légèrement moins précise peut être préférable si elle est considérablement plus rapide.

# 81\. DENSE VS CREUX

Un système dense :

\[ AR^{nn} \]

peut nécessiter :

\[ O(n^2) \]

mémoire.

Une matrice creuse peut être stockée proportionnellement au nombre de coefficients non nuls :

\[ O((A)). \]

Pour les grands problèmes, cette différence est déterminante.

# 82\. PARALLÉLISATION

De nombreuses opérations numériques sont parallélisables :

- produits matriciels ;
- Monte-Carlo ;
- calculs sur grilles ;
- intégration ;
- simulation de particules ;
- entraînement ML.

Les architectures GPU sont particulièrement adaptées à certains motifs de calcul massivement parallèles.

# 83\. PRÉCISION MIXTE

Un système peut utiliser plusieurs niveaux de précision.

Par exemple :

- calcul rapide en précision inférieure ;
- accumulation ou correction en précision supérieure.

La précision mixte permet parfois d’améliorer le compromis :

\[ . \]

Elle est particulièrement importante dans :

- deep learning ;
- HPC ;
- GPU computing.

# 84\. CALCUL SCIENTIFIQUE REPRODUCTIBLE

Un calcul numérique sérieux doit idéalement conserver :

- paramètres ;
- données ;
- méthode ;
- tolérance ;
- précision ;
- graine aléatoire ;
- version du logiciel ;
- environnement ;
- résultats intermédiaires importants.

La reproductibilité est une propriété du système numérique, pas seulement du code.

# 85\. APPLICATIONS EN INTELLIGENCE ARTIFICIELLE

L’analyse numérique est omniprésente dans l’IA.

### Entraînement

\[ \_L(). \]

### Gradient

\[ \_L. \]

### Mise à jour

\[ \_{t+1} = \_t-L. \]

### Calcul matriciel

\[ Y=WX+b. \]

### Propagation avant

enchaînement d’opérations numériques.

### Rétropropagation

calcul numérique de gradients.

### Optimisation

recherche des paramètres.

# 86\. ERREURS NUMÉRIQUES EN DEEP LEARNING

On rencontre :

- gradients trop petits ;
- gradients trop grands ;
- overflow ;
- underflow ;
- perte de précision ;
- mauvaise échelle des activations ;
- conditionnement ;
- instabilité d’entraînement.

Des mécanismes comme :

- normalisation ;
- clipping ;
- initialisation adaptée ;
- précision mixte ;
- optimisateurs robustes

contribuent à contrôler ces problèmes.

# 87\. APPLICATIONS EN GRAPHISME 2D/3D

L’analyse numérique intervient dans :

- interpolation de trajectoires ;
- simulation physique ;
- intégration temporelle ;
- collisions ;
- dynamique ;
- déformation ;
- animation ;
- ray tracing ;
- calcul de normales ;
- reconstruction de surfaces ;
- splines ;
- géométrie numérique.

# 88\. PHYSIQUE DES JEUX VIDÉO

Une simulation peut suivre :

\[ =a. \]

Avec Euler :

\[ v_{n+1}=v_n+ha_n \]

et :

\[ x_{n+1}=x_n+hv_n. \]

Le choix de l’intégrateur influence :

- stabilité ;
- conservation de l’énergie ;
- sensation physique ;
- comportement à long terme.

# 89\. INTÉGRATEURS SYMPLECTIQUES

Pour certains systèmes mécaniques, des méthodes spécifiques préservent mieux certaines structures géométriques.

Elles peuvent produire des simulations à long terme plus réalistes que des méthodes génériques.

# 90\. APPLICATIONS EN ROBOTIQUE

L’analyse numérique intervient dans :

- cinématique ;
- dynamique ;
- trajectoires ;
- contrôle ;
- estimation d’état ;
- optimisation ;
- simulation ;
- résolution de systèmes ;
- filtrage.

# 91\. APPLICATIONS EN FINANCE

Applications :

- Monte-Carlo ;
- équations différentielles ;
- calibration ;
- optimisation de portefeuille ;
- calcul de risques ;
- pricing ;
- résolution d’équations.

# 92\. APPLICATIONS EN TRAITEMENT DU SIGNAL

On rencontre :

- interpolation ;
- filtrage ;
- transformées numériques ;
- approximation ;
- optimisation ;
- résolution de systèmes ;
- estimation.

# 93\. APPLICATIONS EN CYBERSÉCURITÉ

L’analyse numérique peut intervenir dans :

- détection d’anomalies ;
- optimisation de modèles ;
- traitement de signaux ;
- analyse statistique ;
- simulation d’attaques ;
- estimation de paramètres ;
- systèmes de détection.

# 94\. APPLICATIONS WEB ET LOGICIELLES

Même une application Web peut nécessiter de l’analyse numérique :

- calculs scientifiques dans le navigateur ;
- visualisations interactives ;
- simulation ;
- traitement d’images ;
- interpolation ;
- animation ;
- graphiques ;
- optimisation ;
- modèles ML côté client.

# 95\. APPLICATIONS EN UI/UX ET ANIMATION

Les méthodes numériques permettent notamment :

- interpolation de mouvement ;
- easing ;
- spring animations ;
- trajectoires ;
- physique interactive ;
- transitions continues ;
- simulation de particules.

Une animation de ressort peut être modélisée par une EDO puis intégrée numériquement.

# 96\. APPLICATIONS EN GÉNÉRATION PROCÉDURALE

Le domaine K peut produire des structures mathématiques.

Le domaine L permet ensuite de :

- discrétiser ;
- simuler ;
- interpoler ;
- résoudre ;
- échantillonner ;
- calculer.

Ainsi :

\[ KL \]

peut produire des systèmes procéduraux beaucoup plus riches.

# 97\. APPLICATIONS EN SIMULATION DE FLUIDES

Les équations de fluides sont discrétisées sur une grille ou un maillage.

On peut alors résoudre numériquement les équations correspondantes.

Cela permet :

- fumée ;
- eau ;
- feu ;
- vent ;
- turbulence ;
- effets spéciaux ;
- simulation scientifique.

# 98\. ARCHITECTURE D’UN SOLVEUR NUMÉRIQUE

Un solveur sérieux peut être structuré ainsi :

\[ \]

# 99\. PARAMÈTRES D’UN SOLVEUR

Un solveur peut exposer :

- tolérance ;
- nombre maximal d’itérations ;
- taille de pas ;
- méthode ;
- précision ;
- préconditionneur ;
- critère d’arrêt ;
- stratégie adaptative.

# 100\. ARCHITECTURE LOGICIELLE RECOMMANDÉE

Un moteur numérique peut séparer :

### Modèle

Définition du problème.

### Discrétisation

Transformation du problème continu en problème discret.

### Solveur

Algorithme numérique.

### Contrôle

Convergence et stabilité.

### Validation

Tests et vérification.

### Visualisation

Interprétation du résultat.

Cette séparation permet de remplacer un solveur sans réécrire le modèle.

# 101\. PATTERNS DE RECONNAISSANCE

Lorsqu’un problème contient :

### « trouver une racine »

→ résolution numérique d’équation.

### « résoudre (Ax=b) »

→ algèbre linéaire numérique.

### « approximer une dérivée »

→ différences finies ou différentiation automatique.

### « calculer une intégrale »

→ quadrature numérique ou Monte-Carlo.

### « approximer une fonction à partir de points »

→ interpolation.

### « trouver une approximation optimale »

→ moindres carrés / optimisation.

### « simuler une dynamique »

→ intégration d’EDO/EDP.

### « données très nombreuses et matrice creuse »

→ méthodes itératives / solveurs creux.

### « résultat instable »

→ analyser conditionnement, stabilité et précision.

### « simulation lente »

→ analyser complexité, discrétisation, parallélisation et structure de données.

# 102\. DISTINCTION FONDAMENTALE : EXACT, APPROCHÉ, NUMÉRIQUE

Il faut distinguer :

\[ \]

\[ \]

\[ \]

Une solution exacte peut ne pas avoir de forme analytique simple.

Une solution numérique peut être extrêmement précise sans être symboliquement exacte.

# 103\. CHAÎNE DE CONCEPTION D’UNE SOLUTION NUMÉRIQUE

## Étape 1 — Formuler

Quel est le problème mathématique ?

## Étape 2 — Identifier

Quelle quantité cherche-t-on ?

## Étape 3 — Choisir une représentation

Dense ? Creuse ? Grille ? Maillage ? Échantillons ?

## Étape 4 — Discrétiser

Comment transformer le problème continu ?

## Étape 5 — Choisir une méthode

Quel algorithme ?

## Étape 6 — Analyser

Convergence ? Stabilité ? Conditionnement ?

## Étape 7 — Implémenter

Quel langage ? Quelle précision ? Quelles structures ?

## Étape 8 — Tester

Cas connus et cas limites.

## Étape 9 — Valider

Résidu, erreur, conservation, convergence.

## Étape 10 — Optimiser

Temps, mémoire, parallélisation.

# 104\. ERREURS DE CONCEPTION À ÉVITER

Ne jamais :

- choisir une méthode uniquement parce qu’elle est célèbre ;
- confondre précision et stabilité ;
- ignorer le conditionnement ;
- utiliser une tolérance arbitraire ;
- calculer explicitement une inverse de matrice sans raison ;
- supposer que réduire le pas améliore toujours le résultat ;
- ignorer les unités ;
- ignorer les échelles ;
- oublier les cas limites ;
- accepter silencieusement NaN ou inf ;
- comparer uniquement les sorties sans comparer les résidus ;
- mesurer la précision sans mesurer le coût.

# 105\. CRITÈRE DE QUALITÉ D’UN ALGORITHME NUMÉRIQUE

On peut évaluer une méthode selon :

\[ \]

Il n’existe généralement pas de méthode universellement optimale.

# 106\. MÉTHODES ADAPTATIVES

Une méthode adaptative ajuste dynamiquement :

- pas ;
- précision ;
- maillage ;
- nombre d’échantillons ;
- tolérance.

L’objectif est de concentrer les ressources là où elles sont nécessaires.

Cette idée est extrêmement importante pour créer des systèmes efficaces.

# 107\. CALCUL NUMÉRIQUE ET TEMPS RÉEL

Dans un système temps réel, la précision n’est pas le seul objectif.

Il faut parfois respecter :

\[ T_{}<T_{}. \]

Une méthode légèrement moins précise mais suffisamment rapide peut être préférable.

Applications :

- robotique ;
- jeux ;
- réalité virtuelle ;
- contrôle industriel ;
- interfaces interactives.

# 108\. ANALYSE NUMÉRIQUE POUR L’INNOVATION

L’analyse numérique devient particulièrement intéressante lorsqu’elle est combinée avec d’autres domaines.

### L + K

\[

- \]

→ mondes procéduraux dynamiques.

### L + J

\[

- \]

→ systèmes de décision numériques.

### L + I

\[

- \]

→ apprentissage et simulation.

### L + C

\[

- \]

→ calcul scientifique et IA.

### L + G

\[

- \]

→ simulation sous incertitude.

### L + D

\[

- \]

→ reconstruction et animation 3D.

### L + E/F

\[

- \]

→ planification et systèmes complexes.

# 109\. MOTEUR DE CRÉATIVITÉ POUR LES APPLICATIONS

Lorsqu’un système doit inventer une application, il peut appliquer :

\[ \]

Exemple :

\[ \]

Autre exemple :

\[ . \]

# 110\. QUESTIONS À POSER AVANT TOUTE IMPLÉMENTATION

1.  Quel est le problème mathématique ?
2.  Existe-t-il une solution exacte ?
3.  Si oui, est-elle calculable efficacement ?
4.  Sinon, quelle approximation est acceptable ?
5.  Quelle erreur est tolérable ?
6.  Quelle est la source dominante d’erreur ?
7.  Le problème est-il bien conditionné ?
8.  La méthode converge-t-elle ?
9.  Est-elle stable ?
10. À quelle vitesse converge-t-elle ?
11. Quel est son coût ?
12. Peut-elle être parallélisée ?
13. Existe-t-il une méthode plus robuste ?
14. Comment vérifier le résultat ?
15. Comment gérer l’échec du solveur ?

# 111\. CATALOGUE DES FICHES DE DEEP-DIVE

Le document L peut être prolongé par des fiches spécialisées.

## L01 — Arithmétique flottante

- représentation ;
- IEEE 754 ;
- précision ;
- epsilon ;
- overflow ;
- underflow ;
- NaN ;
- infinis ;
- arrondi.

## L02 — Erreurs numériques

- erreur absolue ;
- relative ;
- propagation ;
- troncature ;
- accumulation ;
- cancellation.

## L03 — Conditionnement et stabilité

- conditionnement ;
- stabilité absolue ;
- stabilité relative ;
- backward error ;
- forward error.

## L04 — Résolution d’équations

- bissection ;
- Newton ;
- sécante ;
- méthodes hybrides.

## L05 — Systèmes linéaires

- Gauss ;
- LU ;
- Cholesky ;
- QR ;
- pivotage ;
- systèmes creux.

## L06 — Méthodes itératives

- Jacobi ;
- Gauss-Seidel ;
- gradient ;
- gradient conjugué ;
- GMRES ;
- préconditionnement.

## L07 — Interpolation

- Lagrange ;
- Newton ;
- splines ;
- interpolation multidimensionnelle.

## L08 — Approximation

- moindres carrés ;
- approximation polynomiale ;
- régularisation ;
- bases fonctionnelles.

## L09 — Intégration numérique

- rectangles ;
- trapèzes ;
- Simpson ;
- Gauss ;
- adaptatif.

## L10 — Différences finies

- dérivées ;
- gradients ;
- Laplacien ;
- discrétisation.

## L11 — EDO

- Euler ;
- Runge-Kutta ;
- méthodes implicites ;
- stabilité.

## L12 — EDP

- différences finies ;
- éléments finis ;
- volumes finis ;
- méthodes spectrales.

## L13 — Monte-Carlo

- échantillonnage ;
- convergence ;
- variance ;
- importance sampling.

## L14 — Valeurs propres

- puissance ;
- QR ;
- Lanczos ;
- applications.

## L15 — Différentiation automatique

- forward mode ;
- reverse mode ;
- graphes computationnels ;
- backpropagation.

## L16 — Calcul scientifique haute performance

- parallélisation ;
- GPU ;
- mémoire ;
- précision mixte ;
- calcul distribué.

## L17 — Solveurs robustes

- tolérances ;
- diagnostics ;
- résidus ;
- fallback ;
- monitoring.

## L18 — Analyse numérique pour l’IA

- optimisation ;
- gradients ;
- stabilité ;
- précision ;
- entraînement.

## L19 — Analyse numérique pour la 3D

- interpolation ;
- simulation ;
- intégration temporelle ;
- géométrie ;
- physique.

## L20 — Simulation temps réel

- pas de temps ;
- stabilité ;
- performance ;
- approximation contrôlée.

# 112\. PROJETS D’APPRENTISSAGE

## Projet 1 — Visualiseur d’erreur flottante

Créer une interface montrant :

\[ x,,|x-|. \]

Comparer différentes opérations.

## Projet 2 — Comparateur de solveurs

Comparer :

- bissection ;
- Newton ;
- sécante.

Afficher :

- nombre d’itérations ;
- erreur ;
- convergence ;
- temps.

## Projet 3 — Interpolation interactive

Permettre à l’utilisateur de déplacer des points et observer :

- Lagrange ;
- Newton ;
- spline.

## Projet 4 — Solveur d’EDO visuel

Créer une simulation avec :

- Euler ;
- RK4 ;
- différents pas.

Visualiser l’erreur.

## Projet 5 — Simulateur Monte-Carlo

Estimer :

\[ \]

par échantillonnage aléatoire.

Puis visualiser la convergence.

## Projet 6 — Solveur linéaire

Implémenter :

- Gauss ;
- LU ;
- Jacobi ;
- Gauss-Seidel.

Comparer :

- précision ;
- temps ;
- nombre d’itérations.

## Projet 7 — Simulation physique

Créer un système :

\[ x(t),v(t) \]

avec différents intégrateurs.

Comparer leur stabilité.

## Projet 8 — Terrain numérique

Combiner :

- génération procédurale ;
- interpolation ;
- discrétisation ;
- visualisation 3D.

# 113\. CHALLENGES SANS IA

### Niveau 1

Implémenter Newton-Raphson.

### Niveau 2

Ajouter une détection de divergence.

### Niveau 3

Comparer Newton, sécante et bissection.

### Niveau 4

Construire un solveur générique.

### Niveau 5

Ajouter contrôle de tolérance et résidu.

### Niveau 6

Gérer automatiquement les cas pathologiques.

### Niveau 7

Créer un système adaptatif choisissant automatiquement la méthode.

# 114\. CHALLENGES AVEC IA

L’IA peut aider à :

- analyser une méthode ;
- comparer des solveurs ;
- générer des tests ;
- expliquer une divergence ;
- rechercher des méthodes spécialisées ;
- optimiser une implémentation ;
- comparer des bibliothèques ;
- analyser la littérature scientifique.

Mais le développeur doit conserver la capacité de vérifier :

\[ \]

sans dépendre aveuglément de l’IA.

# 115\. CE QU’IL FAUT ABSOLUMENT RETENIR

Un niveau de maîtrise opérationnelle du domaine L doit permettre de reconnaître immédiatement :

### Représentation

\[ \]

### Erreur

\[ \]

### Résolution

\[ f(x)=0 \]

→ solveur numérique.

### Système

\[ Ax=b \]

→ solveur linéaire.

### Interpolation

\[ (x_i,y_i) f(x) \]

### Intégration

\[ f(x),dx . \]

### Différentiation

\[ f’(x) . \]

### Dynamique

\[ =f(t,y) . \]

### Incertitude

\[ E\[f(X)\] . \]

### Fiabilité

\[ \]

# 116\. CHECKLIST DE MAÎTRISE

Je dois savoir :

- définir une erreur absolue ;
- définir une erreur relative ;
- expliquer la virgule flottante ;
- expliquer pourquoi les nombres réels ne sont pas tous représentables ;
- reconnaître une annulation catastrophique ;
- distinguer précision et exactitude ;
- distinguer stabilité et conditionnement ;
- expliquer la convergence ;
- comparer les ordres de convergence ;
- utiliser un critère d’arrêt ;
- résoudre une équation numériquement ;
- expliquer Newton-Raphson ;
- utiliser une méthode de bracketing ;
- résoudre un système linéaire ;
- expliquer LU ;
- comprendre les méthodes itératives ;
- comprendre les matrices creuses ;
- interpoler une fonction ;
- utiliser une spline ;
- approximer une fonction ;
- calculer une intégrale numériquement ;
- approximer une dérivée ;
- résoudre une EDO simple ;
- comprendre la stabilité temporelle ;
- comprendre Monte-Carlo ;
- analyser une erreur numérique ;
- valider un résultat ;
- choisir une méthode selon le problème ;
- prendre en compte le coût computationnel ;
- reconnaître les situations nécessitant une méthode adaptative.

# 117\. RELATIONS AVEC LES AUTRES DOMAINES

## Avec le domaine I — Calcul différentiel

\[ \]

## Avec le domaine J — Optimisation

\[ \]

## Avec le domaine K — Fractales, chaos et systèmes dynamiques

\[ . \]

## Avec le domaine C — Algèbre linéaire

\[ Ax=b . \]

## Avec le domaine G — Probabilités

\[ E\[X\] . \]

## Avec le domaine H — Statistiques

\[ . \]

# 118\. SYNTHÈSE FINALE

Le domaine L enseigne une idée fondamentale :

\[ \]

Entre le modèle et le résultat existe toute une chaîne :

\[ \]

Chaque étape peut introduire :

- erreur ;
- instabilité ;
- coût ;
- approximation ;
- biais numérique.

L’analyse numérique fournit donc les outils permettant de contrôler cette chaîne.

# 119\. LA GRANDE IDÉE DU DOMAINE L

Les mathématiques classiques demandent :

Quelle est la solution ?

L’analyse numérique demande une question supplémentaire :

**Comment obtenir cette solution de manière suffisamment précise, stable, convergente, efficace et vérifiable sur une machine réelle ?**

C’est cette seconde question qui transforme une formule mathématique en **système informatique exploitable**.

# 120\. FORMULE MENTALE À CONSERVER

Pour tout problème numérique :

\[ \]

Et lorsqu’une IA doit transformer un concept mathématique en logiciel :

\[ \]

Le domaine L constitue ainsi la **couche d’exécution numérique** de l’ensemble de la cartographie mathématique.

Il permet de passer de :

\[ \]

à :

\[ . \]

Et c’est précisément ce qui en fait un domaine central pour le calcul scientifique, l’IA, les simulations, la robotique, la 3D, les jeux vidéo, la finance, les systèmes physiques et les logiciels mathématiques.