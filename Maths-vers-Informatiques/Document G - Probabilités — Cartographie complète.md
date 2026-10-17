# DOCUMENT G — PROBABILITÉS

## Cartographie complète pour les mathématiques, l’algorithmique, le machine learning, l’IA et les systèmes probabilistes

# 0\. IDENTITÉ DU DOMAINE

## 0.1 Nom

**Domaine G — Probabilités**

## 0.2 Mission du domaine

Les probabilités fournissent un cadre mathématique permettant de :

- représenter l’incertitude ;
- quantifier le hasard ;
- modéliser des événements incertains ;
- raisonner à partir d’informations incomplètes ;
- estimer des quantités inconnues ;
- prédire des résultats ;
- simuler des phénomènes aléatoires ;
- mesurer la variabilité ;
- comparer des hypothèses ;
- mettre à jour des croyances à partir d’observations ;
- construire des modèles probabilistes ;
- prendre des décisions sous incertitude.

En informatique, elles constituent l’un des fondements mathématiques majeurs de :

- l’intelligence artificielle ;
- le machine learning ;
- les statistiques ;
- la classification ;
- la détection d’anomalies ;
- le traitement automatique du langage ;
- les modèles génératifs ;
- les réseaux bayésiens ;
- les systèmes de recommandation ;
- les simulations ;
- les systèmes distribués ;
- les files d’attente ;
- les chaînes de Markov ;
- les processus stochastiques ;
- les algorithmes randomisés ;
- le reinforcement learning ;
- l’analyse de risques ;
- la cryptographie ;
- les systèmes de décision.

# 1\. PLACE DU DOMAINE G DANS LA CARTE MATHÉMATIQUE

Les probabilités sont directement connectées à plusieurs domaines précédents.

### Domaine A — Logique et fondements

Permet notamment de formaliser :

- événements ;
- propositions ;
- ensembles ;
- implication ;
- négation ;
- raisonnement.

### Domaine B — Théorie des nombres

Intervient notamment dans :

- cryptographie probabiliste ;
- algorithmes randomisés ;
- tests de primalité probabilistes ;
- générateurs pseudo-aléatoires.

### Domaine C — Algèbre linéaire

Fondamental pour :

- variables aléatoires vectorielles ;
- covariance ;
- matrices de covariance ;
- modèles gaussiens ;
- PCA ;
- modèles probabilistes multivariés ;
- Kalman ;
- machine learning.

### Domaine D — Géométrie computationnelle

Intervient dans :

- distributions spatiales ;
- processus géométriques aléatoires ;
- Monte Carlo géométrique ;
- estimation dans l’espace ;
- simulation 2D/3D.

### Domaine E — Théorie des graphes

Intervient dans :

- réseaux probabilistes ;
- graphes bayésiens ;
- chaînes de Markov ;
- random walks ;
- modèles graphiques.

### Domaine F — Combinatoire

Fournit les outils de :

- dénombrement ;
- calcul de probabilités discrètes ;
- espace des configurations ;
- comptage des cas favorables ;
- analyse des espaces combinatoires.

### Domaine G — Probabilités

Ajoute une nouvelle dimension :

**Comment raisonner mathématiquement lorsque le résultat n’est pas déterministe ?**

# 2\. POURQUOI LES PROBABILITÉS SONT CRITIQUES EN INFORMATIQUE

Un programme classique peut être vu comme :

\[ entrée traitement sortie \]

Un système probabiliste peut plutôt être vu comme :

\[ entrée + incertitude distribution de résultats \]

Un modèle d’IA ne dit pas nécessairement :

« Cette image est un chat. »

Il peut produire :

\[ P(x)=0.93 \]

et :

\[ P(x)=0.05 \]

\[ P(x)=0.02 \]

La probabilité devient donc un langage permettant au système de représenter son **degré d’incertitude**.

# 3\. CARTOGRAPHIE GLOBALE DU DOMAINE

Le domaine peut être organisé en grandes familles.

## G1 — Fondements probabilistes

- expérience aléatoire ;
- univers ;
- événements ;
- espace probabilisé ;
- axiomes ;
- probabilité.

## G2 — Probabilités conditionnelles

- probabilité conditionnelle ;
- indépendance ;
- dépendance ;
- formule des probabilités totales ;
- Bayes.

## G3 — Variables aléatoires

- variables discrètes ;
- variables continues ;
- fonctions de répartition ;
- densités ;
- lois.

## G4 — Moments

- espérance ;
- variance ;
- écart-type ;
- covariance ;
- corrélation ;
- moments supérieurs.

## G5 — Lois de probabilité

### Discrètes

- Bernoulli ;
- binomiale ;
- géométrique ;
- binomiale négative ;
- hypergéométrique ;
- Poisson.

### Continues

- uniforme ;
- exponentielle ;
- normale ;
- gamma ;
- bêta ;
- khi-deux ;
- Student ;

## G6 — Variables aléatoires multiples

- distributions conjointes ;
- distributions marginales ;
- distributions conditionnelles ;
- covariance ;
- corrélation ;
- indépendance.

## G7 — Convergence probabiliste

- loi des grands nombres ;
- convergence en probabilité ;
- convergence presque sûre ;
- convergence en loi ;
- théorème central limite.

## G8 — Espérance conditionnelle

- information ;
- filtrage ;
- projection ;
- martingales ;
- applications ML.

## G9 — Processus stochastiques

- chaînes de Markov ;
- marches aléatoires ;
- processus de Poisson ;
- processus de renouvellement ;
- martingales ;
- processus de diffusion.

## G10 — Simulation

- Monte Carlo ;
- échantillonnage ;
- génération pseudo-aléatoire ;
- importance sampling ;

## G11 — Probabilités et IA

- Bayes ;
- classification ;
- Naive Bayes ;
- réseaux bayésiens ;
- modèles graphiques ;
- modèles génératifs ;
- HMM ;
- modèles séquentiels ;
- reinforcement learning.

## G12 — Probabilités et systèmes

- files d’attente ;
- réseaux ;
- fiabilité ;
- systèmes distribués ;
- tolérance aux pannes ;
- disponibilité ;
- performance.

# 4\. VOCABULAIRE FONDAMENTAL

## 4.1 Expérience aléatoire

Une expérience dont le résultat n’est pas déterministe avant son observation.

Exemples :

- lancer un dé ;
- lancer une pièce ;
- recevoir une requête réseau ;
- observer le temps de réponse d’un serveur ;
- sélectionner un utilisateur ;
- générer un échantillon.

## 4.2 Univers

L’ensemble des résultats possibles.

Notation :

\[ \]

Exemple :

\[ ={1,2,3,4,5,6} \]

pour un dé.

## 4.3 Événement

Un sous-ensemble de l’univers.

Exemple :

\[ A={2,4,6} \]

représente l’événement « obtenir un nombre pair ».

## 4.4 Événement certain

\[ P()=1 \]

## 4.5 Événement impossible

\[ P()=0 \]

# 5\. AXIOMES DE KOLMOGOROV

Une probabilité respecte trois principes fondamentaux.

## Axiome 1 — Positivité

\[ P(A) \]

## Axiome 2 — Normalisation

\[ P()=1 \]

## Axiome 3 — Additivité

Pour des événements disjoints :

\[ P(AB)=P(A)+P(B) \]

plus généralement :

\[ P(\_i A_i) = \_i P(A_i) \]

lorsque les événements sont deux à deux disjoints.

# 6\. PROPRIÉTÉS FONDAMENTALES

## Complément

\[ P(A^c)=1-P(A) \]

## Union

\[ P(AB) = P(A)+P(B)-P(AB) \]

## Inclusion

Si :

\[ AB \]

alors :

\[ P(A)P(B) \]

# 7\. PROBABILITÉ CONDITIONNELLE

La probabilité conditionnelle mesure la probabilité d’un événement sachant qu’une information est déjà connue.

Pour :

\[ P(B)>0 \]

on définit :

\[ P(AB) = \]

genui{“learning_viz”:{“type_id”:“CONDITIONAL_PROBABILITY_DEFINITION”,“initial_values”:{“pB”:0.65,“pIntersection”:0.3},“locale_override”:“fr-FR”}}

## Interprétation

La condition (B) réduit l’espace des possibilités.

Au lieu de considérer tout (), on raisonne essentiellement à l’intérieur de (B).

# 8\. RÈGLE DU PRODUIT

À partir de la probabilité conditionnelle :

\[ P(AB) = P(AB)P(B) \]

ou :

\[ P(AB) = P(BA)P(A) \]

Cette formule est fondamentale pour les modèles probabilistes.

# 9\. INDÉPENDANCE

Deux événements sont indépendants si la connaissance de l’un ne modifie pas la probabilité de l’autre.

\[ P(AB)=P(A)P(B) \]

Équivalent, lorsque les probabilités conditionnelles sont définies :

\[ P(AB)=P(A) \]

## Attention

**Indépendance ≠ incompatibilité.**

Deux événements incompatibles vérifient :

\[ AB= \]

Deux événements indépendants vérifient :

\[ P(AB)=P(A)P(B) \]

Ce sont deux concepts très différents.

# 10\. PROBABILITÉS TOTALES

Si :

\[ B_1,,B_n \]

forment une partition de (), alors :

\[ P(A) = \_{i=1}^{n} P(AB_i)P(B_i) \]

Cette formule est particulièrement importante dans :

- diagnostic ;
- classification ;
- réseaux bayésiens ;
- systèmes experts ;
- détection d’anomalies.

# 11\. THÉORÈME DE BAYES

Le théorème de Bayes permet de renverser une condition.

\[ P(AB) = \]

genui{“learning_viz”:{“type_id”:“BAYES_THEOREM”,“initial_values”:{“pA”:0.2,“pBGivenA”:0.85,“pBGivenNotA”:0.1},“locale_override”:“fr-FR”}}

## Interprétation

Bayes permet de passer de :

\[ P() \]

à :

\[ P() \]

C’est l’un des mécanismes fondamentaux de l’inférence probabiliste.

# 12\. INTERPRÉTATION BAYÉSIENNE

On distingue :

### Prior

\[ P(H) \]

Croyance avant l’observation.

### Likelihood

\[ P(DH) \]

Probabilité d’observer les données (D) sous l’hypothèse (H).

### Posterior

\[ P(HD) \]

Croyance mise à jour après observation.

### Evidence

\[ P(D) \]

Probabilité globale des données.

Ainsi :

\[ Posterior LikelihoodPrior \]

# 13\. VARIABLES ALÉATOIRES

Une variable aléatoire associe une valeur numérique à chaque résultat d’une expérience aléatoire.

Notation :

\[ X: \]

Exemple :

(X) = nombre de requêtes reçues pendant une minute.

# 14\. VARIABLE ALÉATOIRE DISCRÈTE

Une variable discrète prend un ensemble fini ou dénombrable de valeurs.

Exemples :

- nombre de clients ;
- nombre de défauts ;
- nombre de succès ;
- nombre de paquets perdus.

Sa loi est donnée par :

\[ P(X=x) \]

# 15\. VARIABLE ALÉATOIRE CONTINUE

Une variable continue peut prendre une infinité non dénombrable de valeurs.

Exemples :

- temps ;
- température ;
- distance ;
- durée d’une requête ;
- poids.

Pour une variable continue :

\[ P(X=x)=0 \]

pour une valeur individuelle.

On raisonne plutôt sur des intervalles :

\[ P(aXb) \]

# 16\. FONCTION DE RÉPARTITION

Pour toute variable aléatoire (X) :

\[ F_X(x)=P(Xx) \]

Elle existe pour les variables :

- discrètes ;
- continues.

Elle permet de représenter la distribution cumulative.

# 17\. DENSITÉ DE PROBABILITÉ

Pour une variable continue possédant une densité :

\[ f_X(x) \]

on a :

\[ P(aXb) = \_a^b f_X(x),dx \]

et :

\[ \_{-}^{+}f_X(x),dx=1 \]

# 18\. ESPÉRANCE

L’espérance représente la moyenne théorique d’une variable aléatoire.

Pour une variable discrète :

\[ E\[X\] = \_x xP(X=x) \]

Pour une variable continue :

\[ E\[X\] = \_{-}^{+}x f_X(x),dx \]

genui{“learning_viz”:{“type_id”:“EXPECTED_VALUE_WEIGHTED_AVERAGE”,“locale_override”:“fr-FR”}}

L’espérance est fondamentale pour :

- estimation ;
- décision ;
- optimisation ;
- reinforcement learning ;
- théorie de l’information ;
- analyse des performances.

# 19\. LINÉARITÉ DE L’ESPÉRANCE

Pour des variables (X,Y) et des constantes (a,b) :

\[ E\[aX+bY\] = aE\[X\]+bE\[Y\] \]

Cette propriété est valable même lorsque (X) et (Y) ne sont pas indépendantes.

C’est une propriété extrêmement importante en algorithmique probabiliste et en machine learning.

# 20\. VARIANCE

La variance mesure la dispersion autour de l’espérance.

\[ Var(X) = E\[(X-E\[X\])^2\] \]

Forme équivalente :

\[ Var(X) = E\[X^2\]-E\[X\]^2 \]

genui{“learning_viz”:{“type_id”:“VARIANCE”,“locale_override”:“fr-FR”}}

# 21\. ÉCART-TYPE

\[ \_X= \]

Contrairement à la variance, l’écart-type possède les mêmes unités que (X).

# 22\. PROPRIÉTÉS DE LA VARIANCE

Pour une constante (a) :

\[ Var(aX)=a^2Var(X) \]

Pour deux variables indépendantes :

\[ Var(X+Y) = Var(X)+Var(Y) \]

Plus généralement :

\[ Var(X+Y) = Var(X)+Var(Y)+2Cov(X,Y) \]

# 23\. COVARIANCE

La covariance mesure la variation conjointe de deux variables.

\[ Cov(X,Y) = E\[(X-E\[X\])(Y-E\[Y\])\] \]

Forme équivalente :

\[ Cov(X,Y) = E\[XY\]-E\[X\]E\[Y\] \]

# 24\. CORRÉLATION

La corrélation normalise la covariance :

\[ \_{X,Y} = {\_X_Y} \]

avec :

\[ -1 \]

Attention :

corrélation n’implique pas causalité.

# 25\. VARIABLES ALÉATOIRES MULTIPLES

Pour deux variables (X,Y), on peut étudier :

- loi conjointe ;
- lois marginales ;
- lois conditionnelles ;
- indépendance ;
- covariance ;
- corrélation.

On peut avoir :

\[ P(X=x,Y=y) \]

et obtenir une marginale :

\[ P(X=x) = \_y P(X=x,Y=y) \]

dans le cas discret.

# 26\. INDÉPENDANCE DES VARIABLES ALÉATOIRES

(X) et (Y) sont indépendantes si :

\[ P(XA,YB) = P(XA)P(YB) \]

pour les ensembles appropriés (A,B).

Dans le cas discret :

\[ P(X=x,Y=y) = P(X=x)P(Y=y) \]

# 27\. LOI DE BERNOULLI

Une expérience avec deux résultats :

- succès ;
- échec.

On note :

\[ XBernoulli(p) \]

avec :

\[ P(X=1)=p \]

\[ P(X=0)=1-p \]

Espérance :

\[ E\[X\]=p \]

Variance :

\[ Var(X)=p(1-p) \]

# 28\. LOI BINOMIALE

Si :

- (n) essais indépendants ;
- même probabilité de succès (p) ;

alors :

\[ XBinomial(n,p) \]

et :

\[ P(X=k) = nk p<sup>k(1-p)</sup>{n-k} \]

Espérance :

\[ E\[X\]=np \]

Variance :

\[ Var(X)=np(1-p) \]

Applications :

- classification binaire ;
- tests ;
- conversion ;
- fiabilité ;
- A/B testing ;
- nombre de succès dans une série d’essais.

# 29\. LOI GÉOMÉTRIQUE

Elle modélise le nombre d’essais nécessaires avant le premier succès.

\[ P(X=k) = (1-p)^{k-1}p \]

Propriété importante :

**absence de mémoire**.

\[ P(X>m+nX>m) = P(X>n) \]

# 30\. LOI BINOMIALE NÉGATIVE

Elle généralise la logique de la loi géométrique en considérant le nombre d’essais nécessaires pour obtenir un nombre donné de succès.

Applications :

- comptage ;
- modélisation de surdispersion ;
- événements répétés.

# 31\. LOI HYPERGÉOMÉTRIQUE

Utilisée lorsque l’on effectue des tirages **sans remise**.

Elle est donc différente de la binomiale, qui suppose généralement des essais indépendants.

# 32\. LOI DE POISSON

Elle modélise souvent le nombre d’événements rares apparaissant pendant une durée ou une région donnée.

\[ XPoisson() \]

avec :

\[ P(X=k) = e<sup>{-}\\frac{</sup>k}{k!} \]

Espérance :

\[ E\[X\]= \]

Variance :

\[ Var(X)= \]

Applications :

- requêtes serveur ;
- appels ;
- défauts ;
- événements réseau ;
- arrivées ;
- incidents.

# 33\. LOI UNIFORME

### Discrète

Chaque valeur possède la même probabilité.

### Continue

Sur (\[a,b\]) :

\[ f(x)= \]

pour :

\[ axb \]

# 34\. LOI EXPONENTIELLE

Elle modélise fréquemment un temps d’attente.

\[ f(x)=e^{-x} \]

pour :

\[ x \]

Espérance :

\[ E\[X\]= \]

Variance :

\[ Var(X)= \]

Elle possède également la propriété d’absence de mémoire.

# 35\. LOI NORMALE

La loi normale est l’une des distributions continues fondamentales.

\[ X(,^2) \]

Sa densité est :

\[ f(x) = e<sup>{-\\frac{(x-)</sup>2}{2^2}} \]

Elle apparaît notamment grâce au théorème central limite.

# 36\. STANDARDISATION

Si :

\[ XN(,^2) \]

alors :

\[ Z= \]

suit une loi normale centrée réduite :

\[ ZN(0,1) \]

genui{“learning_viz”:{“type_id”:“STANDARD_SCORE_Z”,“initial_values”:{“x”:1.2,“mu”:0,“sigma”:1},“locale_override”:“fr-FR”}}

# 37\. AUTRES LOIS CONTINUES IMPORTANTES

À connaître au niveau de reconnaissance :

### Loi Gamma

Très importante pour :

- temps d’attente ;
- modèles bayésiens ;
- processus de Poisson.

### Loi Beta

Très importante pour :

- probabilités ;
- modèles bayésiens ;
- proportions ;
- paramètres (p).

### Loi du Khi-deux

Utilisée notamment pour :

- tests statistiques ;
- estimation de variance ;
- statistiques inférentielles.

### Loi de Student

Utilisée notamment lorsque :

- l’échantillon est petit ;
- la variance de population est inconnue.

### Loi de Fisher-Snedecor

Utilisée notamment pour :

- comparaison de variances ;
- ANOVA ;
- modèles statistiques.

# 38\. TRANSFORMATIONS DE VARIABLES ALÉATOIRES

Si :

\[ Y=g(X) \]

on peut chercher la distribution de (Y) à partir de celle de (X).

Cela est particulièrement important pour :

- simulation ;
- statistiques ;
- changement de variables ;
- modèles génératifs ;
- probabilités continues.

# 39\. MOMENTS

Le premier moment :

\[ E\[X\] \]

Le second moment :

\[ E\[X^2\] \]

La variance :

\[ E\[X^2\]-E\[X\]^2 \]

Les moments d’ordre supérieur permettent de caractériser plus finement une distribution.

# 40\. ASYMÉTRIE ET APLATISSEMENT

Deux notions statistiques avancées :

### Skewness

Mesure l’asymétrie.

### Kurtosis

Mesure certains aspects de la concentration et des queues de distribution.

Elles deviennent pertinentes dans :

- analyse exploratoire ;
- détection d’anomalies ;
- analyse de distributions ;
- modélisation des erreurs.

# 41\. ESPÉRANCE CONDITIONNELLE

L’espérance conditionnelle :

\[ E\[XY\] \]

représente l’espérance de (X) lorsque l’information concernant (Y) est connue.

C’est une notion centrale pour :

- prédiction ;
- filtrage ;
- processus stochastiques ;
- statistiques ;
- machine learning ;
- théorie de la décision.

# 42\. PROPRIÉTÉS DE L’ESPÉRANCE CONDITIONNELLE

### Linéarité

\[ E\[aX+bYZ\] = aE\[XZ\]+bE\[YZ\] \]

### Tower property

\[ E\[E\[XY\]\] = E\[X\] \]

Plus généralement :

\[ E\[E\[XY,Z\]Y\] = E\[XY\] \]

Cette propriété est fondamentale dans les systèmes probabilistes hiérarchiques.

# 43\. LOI DES ESPÉRANCES TOTALES

\[ E\[X\] = E\[E\[XY\]\] \]

Dans le cas discret :

\[ E\[X\] = \_y E\[XY=y\]P(Y=y) \]

Cette formule généralise le raisonnement par décomposition.

# 44\. LOI DE LA VARIANCE TOTALE

\[ Var(X) = E\[Var(XY)\]

- Var(E\[XY\]) \]

Cette identité sépare :

- la variabilité interne ;
- la variabilité entre groupes.

# 45\. THÉORÈME CENTRAL LIMITE

Le théorème central limite explique pourquoi la loi normale apparaît si fréquemment.

Sous des conditions appropriées, la somme ou moyenne d’un grand nombre de variables aléatoires indépendantes et suffisamment régulières tend vers une distribution normale après standardisation.

Pour une moyenne :

\[ \]

tend vers :

\[ N(0,1) \]

lorsque (n) devient grand.

Applications :

- statistiques ;
- estimation ;
- intervalles de confiance ;
- analyse de données ;
- machine learning ;
- approximation probabiliste.

# 46\. LOI DES GRANDS NOMBRES

La loi des grands nombres explique que la moyenne empirique se rapproche de l’espérance lorsque le nombre d’observations augmente, sous des conditions appropriées.

Schématiquement :

\[ 1n_{i=1}^n X_i E\[X\] \]

# 47\. DIFFÉRENCE ENTRE LGN ET TCL

### Loi des grands nombres

Répond principalement à :

« Vers quoi converge la moyenne ? »

### Théorème central limite

Répond principalement à :

« Quelle est la forme de la fluctuation autour de cette moyenne ? »

C’est une distinction fondamentale.

# 48\. CONVERGENCES PROBABILISTES

À niveau avancé, il faut distinguer :

- convergence presque sûre ;
- convergence en probabilité ;
- convergence en moyenne (L^p) ;
- convergence en distribution.

Ces notions ne sont pas interchangeables.

# 49\. PROCESSUS STOCHASTIQUE

Un processus stochastique est une famille de variables aléatoires indexées par le temps ou un autre paramètre.

On peut écrire :

\[ {X_t}\_{tT} \]

Exemples :

- trafic réseau ;
- prix ;
- nombre de requêtes ;
- position d’un agent ;
- état d’un système.

# 50\. CHAÎNES DE MARKOV

Une chaîne de Markov possède la propriété suivante :

l’état futur dépend du présent, mais pas du passé au-delà de l’information contenue dans l’état actuel.

Formellement :

\[ P(X_{t+1}X_t,X_{t-1},…,X_0) = P(X_{t+1}X_t) \]

# 51\. MATRICE DE TRANSITION

Une chaîne de Markov finie peut être représentée par :

\[ P=

\]

avec :

\[ p_{ij}=P(X_{t+1}=jX_t=i) \]

Chaque ligne doit sommer à 1.

# 52\. DISTRIBUTION STATIONNAIRE

Une distribution () est stationnaire si :

\[ P= \]

avec :

\[ \_i_i=1 \]

Cette notion intervient dans :

- PageRank ;
- systèmes de recommandation ;
- modélisation séquentielle ;
- files d’attente ;
- processus de décision.

# 53\. MARCHE ALÉATOIRE

Une marche aléatoire décrit un déplacement soumis au hasard.

Exemple simple :

\[ X_{t+1}=X_t+\_t \]

avec :

\[ \_t{-1,+1} \]

selon certaines probabilités.

Applications :

- réseaux ;
- graphes ;
- exploration ;
- recherche ;
- algorithmes randomisés ;
- systèmes physiques simulés ;
- PageRank.

# 54\. PROCESSUS DE POISSON

Il modélise souvent des événements arrivant au cours du temps avec un taux moyen donné et certaines hypothèses d’indépendance et de stationnarité.

Il est fortement connecté à :

- loi de Poisson ;
- loi exponentielle ;
- files d’attente ;
- réseaux ;
- télécommunications.

# 55\. MARTINGALES

Une martingale modélise, de manière simplifiée, un processus dont l’espérance future conditionnelle, sachant l’information présente, est égale à la valeur actuelle.

\[ E\[X_{t+1}F_t\] = X_t \]

Les martingales sont importantes en :

- probabilités avancées ;
- finance mathématique ;
- théorie des jeux ;
- processus stochastiques ;
- théorie du reinforcement learning.

# 56\. MONTE CARLO

Les méthodes Monte Carlo utilisent des échantillons aléatoires pour approximer des quantités mathématiques.

Principe :

\[ \]

Par exemple :

\[ E\[f(X)\] 1N \_{i=1}^{N}f(X_i) \]

# 57\. CONVERGENCE MONTE CARLO

Sous des conditions appropriées, lorsque :

\[ N \]

la moyenne empirique converge vers l’espérance.

L’erreur typique de Monte Carlo décroît de l’ordre de :

\[ O() \]

Ce point explique pourquoi doubler simplement la précision peut coûter très cher en nombre d’échantillons.

# 58\. IMPORTANCE SAMPLING

Lorsque certaines régions contribuent beaucoup plus à l’espérance que d’autres, on peut échantillonner davantage les régions importantes et corriger le biais par pondération.

Principe :

\[ E_p\[f(X)\] = E_q \]

où (q) est la distribution de proposition.

Applications :

- simulation ;
- finance ;
- robotique ;
- IA ;
- estimation de probabilités rares.

# 59\. MCMC

Les méthodes Markov Chain Monte Carlo utilisent une chaîne de Markov pour produire des échantillons approximativement distribués selon une distribution cible.

Familles importantes :

- Metropolis-Hastings ;
- Gibbs sampling.

Applications :

- inférence bayésienne ;
- modèles probabilistes ;
- posterior distributions ;
- recherche dans des espaces complexes.

# 60\. MÉTHODE DE REJET

Technique d’échantillonnage consistant à :

1.  générer un candidat ;
2.  calculer une probabilité d’acceptation ;
3.  accepter ou rejeter ;
4.  répéter.

Elle constitue une autre méthode fondamentale de génération d’échantillons.

# 61\. PROBABILITÉS ET MACHINE LEARNING

Le machine learning manipule constamment l’incertitude.

Exemples :

\[ P(YX) \]

\[ P(XY) \]

\[ P(X,Y) \]

\[ E\[L(Y,Y)\] \]

\[ Var() \]

# 62\. CLASSIFICATION PROBABILISTE

Un classifieur peut produire :

\[ P(Y=kX=x) \]

pour chaque classe (k).

Exemple :

| Classe | Probabilité |
| --- | --- |
| Chat | 0,80 |
| Chien | 0,15 |
| Autre | 0,05 |

La décision peut ensuite être :

\[ y=\_y P(Y=yX) \]

# 63\. NAIVE BAYES

Le classifieur Naive Bayes repose sur Bayes et une hypothèse simplificatrice d’indépendance conditionnelle entre certaines variables.

\[ P(YX_1,,X_n) P(Y) \_iP(X_iY) \]

Applications :

- classification de texte ;
- spam detection ;
- sentiment analysis ;
- catégorisation.

# 64\. RÉSEAUX BAYÉSIENS

Un réseau bayésien représente des dépendances conditionnelles sous la forme d’un graphe orienté acyclique.

Il combine :

- graphe ;
- probabilités conditionnelles ;
- inférence.

Cela relie directement :

**Domaine E + Domaine G.**

# 65\. MODÈLES DE MARKOV CACHÉS

Un Hidden Markov Model possède :

- des états cachés ;
- des observations ;
- des transitions ;
- des probabilités d’émission.

Applications historiques et conceptuelles :

- reconnaissance de séquences ;
- parole ;
- NLP ;
- bioinformatique ;
- séries temporelles.

# 66\. MODÈLES GÉNÉRATIFS

Un modèle génératif cherche notamment à représenter une distribution :

\[ P(X) \]

ou :

\[ P(X,Y) \]

ou encore :

\[ P(XZ) \]

selon l’architecture.

Cela permet de :

- générer ;
- échantillonner ;
- compléter ;
- prédire ;
- simuler.

# 67\. PROBABILITÉS ET NLP

Le langage peut être modélisé probabilistiquement.

Exemple :

\[ P(w_tw_1,,w_{t-1}) \]

Un modèle autoregressif factorise :

\[ P(w_1,,w_n) = _{t=1}^{n} P(w_tw_1,,w_{t-1}) \]

Cette idée est fondamentale pour comprendre de nombreux modèles de langage.

# 68\. LOG-PROBABILITÉ

Au lieu de multiplier de nombreuses probabilités :

\[ \_i p_i \]

on utilise souvent :

\[ P = \_ip_i \]

Avantages :

- stabilité numérique ;
- simplification des produits en sommes ;
- optimisation plus pratique.

# 69\. VRAISEMBLANCE

Pour des données observées (D) et un paramètre () :

\[ L(;D) = P(D) \]

La vraisemblance considère les données comme observées et examine comment elles soutiennent différents paramètres.

# 70\. MAXIMUM DE VRAISEMBLANCE

On cherche :

\[ = \_L(;D) \]

ou de façon équivalente :

\[ = \_L(;D) \]

Cette idée est fondamentale en apprentissage statistique.

# 71\. APPROCHE BAYÉSIENNE

Dans l’approche bayésienne, le paramètre lui-même est modélisé comme aléatoire :

\[ P(D) P(D)P() \]

On obtient une distribution a posteriori plutôt qu’une simple estimation ponctuelle.

# 72\. BIAS-VARIANCE

La décomposition biais-variance permet d’analyser l’erreur de prédiction.

De manière conceptuelle :

\[ Erreur = Biais^2

- Variance
- Bruit \]

Elle permet de comprendre le compromis entre :

- modèle trop simple ;
- modèle trop sensible aux données ;
- bruit irréductible.

# 73\. DÉTECTION D’ANOMALIES

Une observation peut être considérée comme inhabituelle si :

\[ P(X=x) \]

ou une mesure apparentée est très faible.

On peut rechercher :

\[ -P(X) \]

comme score d’anomalie.

Applications :

- fraude ;
- cybersécurité ;
- monitoring ;
- détection d’incidents ;
- systèmes industriels.

# 74\. PROBABILITÉS ET REINFORCEMENT LEARNING

Dans un système de reinforcement learning :

- état (S) ;
- action (A) ;
- récompense (R) ;
- état suivant (S’).

La dynamique peut être :

\[ P(S’S,A) \]

La politique peut être déterministe ou probabiliste :

\[ (as) \]

# 75\. VALEUR ESPÉRÉE D’UNE POLITIQUE

Une politique peut être évaluée par son retour espéré :

\[ V^(s) = E_ \]

La probabilité devient donc directement liée à l’apprentissage par renforcement.

# 76\. EXPLORATION PROBABILISTE

Des politiques probabilistes permettent d’équilibrer :

- exploration ;
- exploitation.

Exemples :

- epsilon-greedy ;
- softmax ;
- distributions sur les actions ;
- politiques stochastiques.

# 77\. PROBABILITÉS ET ALGORITHMES RANDOMISÉS

Un algorithme randomisé utilise le hasard pendant son exécution.

On peut distinguer :

### Las Vegas

Toujours correct, mais temps d’exécution aléatoire.

### Monte Carlo

Temps contrôlé, mais résultat potentiellement probabiliste.

Cette distinction est importante en algorithmique.

# 78\. COMPLEXITÉ PROBABILISTE

On peut étudier :

\[ E\[T(n)\] \]

où (T(n)) est le temps d’exécution aléatoire.

On peut aussi étudier :

\[ P(T(n)>t) \]

ou des bornes probabilistes.

# 79\. INÉGALITÉS PROBABILISTES

À connaître au niveau de reconnaissance :

## Markov

Pour (X) :

\[ P(Xa) \]

## Chebyshev

\[ P(|X-|k) \]

## Chernoff

Fournit des bornes exponentielles particulièrement utiles pour les sommes de variables aléatoires indépendantes.

Applications :

- algorithmique ;
- théorie de l’information ;
- machine learning ;
- randomized algorithms.

# 80\. CONCENTRATION DES MESURES

Une grande famille de résultats permet de montrer qu’une variable aléatoire reste proche de son espérance avec forte probabilité.

Conceptuellement :

\[ P(|X-E\[X\]|) \]

devient très petit lorsque certaines conditions sont satisfaites.

Ces résultats sont fondamentaux pour :

- généralisation ML ;
- algorithmes randomisés ;
- statistiques ;
- apprentissage théorique.

# 81\. PROBABILITÉS ET INFORMATION

Les probabilités sont directement liées à la théorie de l’information.

Pour une variable discrète :

\[ H(X) = -\_xP(x)P(x) \]

est l’entropie.

Elle mesure l’incertitude moyenne.

# 82\. ENTROPIE CONDITIONNELLE

\[ H(XY) \]

mesure l’incertitude restante sur (X) lorsque (Y) est connu.

# 83\. INFORMATION MUTUELLE

\[ I(X;Y) = \_{x,y} P(x,y) \]

Elle mesure la quantité d’information partagée entre (X) et (Y).

Applications :

- feature selection ;
- NLP ;
- compression ;
- représentation ;
- apprentissage.

# 84\. KULLBACK-LEIBLER

La divergence KL est :

\[ D_{KL}(PQ) = \_xP(x) \]

Elle mesure une forme d’écart entre distributions.

Attention :

\[ D_{KL}(PQ) D_{KL}(QP) \]

en général.

Applications :

- machine learning ;
- modèles génératifs ;
- variational inference ;
- distillation ;
- optimisation.

# 85\. DISTRIBUTIONS JOINTES ET MODÈLES GRAPHIQUES

Une distribution complexe peut être factorisée selon les dépendances représentées par un graphe.

Exemple conceptuel :

\[ P(A,B,C) = P(A)P(BA)P(CB) \]

Cette factorisation réduit parfois considérablement la complexité de représentation.

# 86\. MONTE CARLO DANS LES SYSTÈMES 2D/3D

Monte Carlo peut servir à :

- intégration numérique ;
- rendu ;
- estimation d’aires ;
- simulation physique ;
- propagation d’incertitude ;
- génération procédurale.

Exemple :

estimer une aire en tirant des points aléatoires.

# 87\. PROBABILITÉS ET GRAPHES

Dans un graphe, les probabilités peuvent représenter :

- probabilité de transition ;
- probabilité d’activation ;
- probabilité de défaillance ;
- probabilité de visite ;
- probabilité d’une classe ;
- probabilité d’un chemin.

Cela crée une connexion directe entre :

\[ + \]

# 88\. RANDOM WALK SUR UN GRAPHE

Un agent choisit aléatoirement son prochain sommet.

On peut alors étudier :

- distribution des positions ;
- temps de retour ;
- distribution stationnaire ;
- temps de mélange ;
- propriétés spectrales.

# 89\. PAGERANK

PageRank peut être interprété à travers une marche aléatoire sur le Web.

L’idée fondamentale consiste à modéliser la probabilité de présence d’un surfeur aléatoire sur les pages.

Cela relie :

- graphes ;
- matrices ;
- probabilités ;
- chaînes de Markov.

# 90\. PROBABILITÉS ET SYSTÈMES DISTRIBUÉS

Les probabilités peuvent modéliser :

- panne ;
- latence ;
- perte de paquets ;
- arrivée de requêtes ;
- charge ;
- temps de réponse.

On peut ainsi analyser :

\[ P() \]

\[ E\[\] \]

\[ P(>T) \]

# 91\. FIABILITÉ

Si plusieurs composants ont des probabilités de défaillance, on peut calculer :

- fiabilité globale ;
- disponibilité ;
- probabilité de panne ;
- redondance.

Pour des composants indépendants en série, une panne d’un composant peut suffire à provoquer la panne globale.

Pour des systèmes redondants, plusieurs composants peuvent être nécessaires à la panne.

# 92\. FILES D’ATTENTE

Les systèmes de files d’attente étudient :

- arrivées ;
- services ;
- files ;
- temps d’attente ;
- occupation.

Modèles classiques :

- M/M/1 ;
- M/M/c ;
- M/G/1.

Ils sont importants pour :

- serveurs ;
- réseaux ;
- cloud ;
- systèmes distribués.

# 93\. PROBABILITÉS ET BASES DE DONNÉES

Les probabilités peuvent être utilisées pour :

- estimation de cardinalité ;
- optimisation de requêtes ;
- statistiques de tables ;
- échantillonnage ;
- systèmes probabilistes.

# 94\. PROBABILITÉS ET CYBERSÉCURITÉ

Applications :

- détection d’anomalies ;
- scoring de risque ;
- détection de fraude ;
- comportement utilisateur ;
- génération aléatoire ;
- analyse statistique des événements.

# 95\. PROBABILITÉS ET TESTS LOGICIELS

Les tests probabilistes peuvent permettre :

- génération aléatoire de cas ;
- fuzzing ;
- property-based testing ;
- estimation de couverture ;
- recherche de cas rares.

# 96\. GÉNÉRATION ALÉATOIRE

Il faut distinguer :

### Hasard physique

Source physique d’entropie.

### Générateur pseudo-aléatoire

Algorithme déterministe produisant une séquence ressemblant à une séquence aléatoire.

### CSPRNG

Générateur pseudo-aléatoire conçu pour des usages cryptographiques.

Cette distinction est essentielle en cybersécurité.

# 97\. ÉCHANTILLONNAGE

L’échantillonnage consiste à sélectionner des observations selon une procédure donnée.

Types à reconnaître :

- aléatoire simple ;
- stratifié ;
- systématique ;
- par grappes ;
- avec ou sans remise.

# 98\. BIAIS D’ÉCHANTILLONNAGE

Une procédure d’échantillonnage peut produire un échantillon non représentatif.

Il faut distinguer :

- hasard ;
- biais ;
- variance d’échantillonnage ;
- erreur de mesure.

Un grand échantillon biaisé ne devient pas automatiquement représentatif.

# 99\. ESTIMATION

On cherche à estimer un paramètre inconnu :

\[ \]

à partir des données.

On obtient un estimateur :

\[ \]

# 100\. BIAIS D’UN ESTIMATEUR

\[ Bias() = E\[\]- \]

Un estimateur est sans biais si :

\[ E\[\]= \]

# 101\. CONSISTANCE

Un estimateur est consistant lorsqu’il converge vers la vraie valeur lorsque la taille de l’échantillon augmente, sous les conditions appropriées.

# 102\. INTERVALLES DE CONFIANCE

Un intervalle de confiance fournit une procédure permettant d’encadrer un paramètre avec un niveau de couverture donné.

Attention :

un intervalle de confiance à 95 % n’est pas, dans l’interprétation fréquentiste standard, une affirmation directe que le paramètre fixe possède 95 % de probabilité d’être dans cet intervalle particulier.

Cette distinction conceptuelle est importante.

# 103\. TESTS D’HYPOTHÈSES

On distingue notamment :

- hypothèse nulle ;
- hypothèse alternative ;
- statistique de test ;
- région critique ;
- p-value ;
- niveau de signification.

Il faut éviter de confondre :

\[ P(DH_0) \]

avec :

\[ P(H_0D) \]

Cette confusion est particulièrement importante lorsqu’on passe à Bayes.

# 104\. APPROCHE FRÉQUENTISTE ET BAYÉSIENNE

### Fréquentiste

Le paramètre est généralement considéré comme fixe et les données comme aléatoires.

### Bayésienne

Le paramètre peut être représenté par une variable aléatoire et recevoir un prior.

Les deux cadres ont des interprétations différentes et ne doivent pas être mélangés sans précaution.

# 105\. PROCESSUS DE DÉCISION

Une décision probabiliste peut être modélisée avec :

- états du monde ;
- actions ;
- probabilités ;
- utilités ;
- pertes.

On cherche alors souvent :

\[ E\[U(a)\] \]

ou :

\[ E\[L(a)\] \]

selon l’objectif.

# 106\. RISQUE

En statistique décisionnelle, le risque d’un estimateur ou d’une décision peut être défini comme une espérance de perte.

\[ R(,) = E_\]

Cela relie directement :

**probabilités + optimisation + machine learning.**

# 107\. PROBABILITÉS ET IA AGENTIQUE

Un agent évoluant dans un environnement incertain peut devoir estimer :

\[ P(s’s,a) \]

et :

\[ P(rs,a) \]

Il peut maintenir une croyance :

\[ P(sobservations) \]

puis choisir une action selon :

\[ (as) \]

Cela constitue une base mathématique importante pour :

- agents ;
- planification sous incertitude ;
- POMDP ;
- reinforcement learning ;
- robotique.

# 108\. ESPACE D’ÉTATS ET INCERTITUDE

Un système peut posséder un état caché.

On observe seulement :

\[ O_t \]

et cherche à estimer :

\[ P(S_tO_1,,O_t) \]

Ce mécanisme est au cœur de nombreux systèmes de filtrage et d’inférence.

# 109\. FILTRAGE

Le filtrage consiste à estimer l’état courant à partir des observations passées.

Exemples :

- Kalman filter ;
- Bayesian filtering ;
- HMM filtering ;
- localisation robotique.

# 110\. PRÉDICTION

La prédiction cherche à estimer :

\[ P(S_{t+k}observations) \]

C’est une extension naturelle du raisonnement temporel probabiliste.

# 111\. MODÈLES MARKOVIENS ET AI

Les chaînes de Markov constituent une base conceptuelle pour comprendre :

- HMM ;
- modèles séquentiels ;
- systèmes dynamiques probabilistes ;
- MDP ;
- reinforcement learning.

# 112\. PROCESSUS DE DÉCISION MARKOVIEN

Un MDP contient généralement :

\[ (S,A,P,R,) \]

où :

- (S) = états ;
- (A) = actions ;
- (P) = transitions ;
- (R) = récompenses ;
- () = facteur d’actualisation.

C’est un pont majeur entre probabilités, graphes et reinforcement learning.

# 113\. MONTE CARLO ET REINFORCEMENT LEARNING

Les méthodes Monte Carlo en RL estiment des valeurs à partir de trajectoires complètes.

Conceptuellement :

\[ V(s) 1N \_{i=1}^{N} G_i \]

où (G_i) est un retour observé.

# 114\. TEMPORAL-DIFFERENCE

Les méthodes TD estiment des valeurs à partir d’observations partielles du futur et utilisent notamment :

\[ V(S_t) V(S_t)

- \[ R_{t+1}
- V(S_{t+1})
- V(S_t) \] \]

Cela relie :

- espérance ;
- processus stochastiques ;
- apprentissage ;
- estimation.

# 115\. PROBABILITÉS ET MODÈLES GÉNÉRATIFS MODERNES

Une grande partie des modèles génératifs peut être comprise à travers :

- distributions ;
- échantillonnage ;
- vraisemblance ;
- entropie ;
- divergence KL ;
- probabilités conditionnelles ;
- variables latentes ;
- transformations probabilistes.

Il faut donc considérer les probabilités comme une infrastructure mathématique de l’IA générative.

# 116\. VARIABLE LATENTE

Une variable latente est une variable non directement observée mais utilisée pour expliquer les observations.

On peut chercher :

\[ P(ZX) \]

où :

- (X) = données observées ;
- (Z) = variable latente.

# 117\. MODÈLES MÉLANGE

Un modèle de mélange représente une distribution comme combinaison de plusieurs distributions.

Par exemple :

\[ P(X) = \_k_kP(XZ=k) \]

Applications :

- clustering probabiliste ;
- segmentation ;
- détection de sous-populations ;
- modèles génératifs.

# 118\. ESPÉRANCE-MAXIMISATION

L’algorithme EM est utilisé dans certains modèles à variables latentes.

Il alterne conceptuellement :

### E-step

Estimer les variables latentes conditionnellement aux paramètres.

### M-step

Mettre à jour les paramètres.

Il constitue un exemple important d’utilisation de l’espérance conditionnelle dans l’apprentissage.

# 119\. PROBABILITÉS ET OPTIMISATION

De nombreuses fonctions d’apprentissage sont liées à des quantités probabilistes.

Exemples :

\[ -P(YX) \]

\[ D_{KL}(PQ) \]

\[ E\[L\] \]

Ainsi :

\[ probabilités fonction objectif optimisation modèle appris \]

# 120\. ESPACES PROBABILISTES ET COMPLEXITÉ

Il faut distinguer :

### Probabilité d’un événement

\[ P(A) \]

### Nombre de configurations

\[ || \]

### Distribution sur les configurations

\[ P(X=x) \]

### Espérance

\[ E\[X\] \]

### Variance

\[ Var(X) \]

### Optimisation

\[ / \]

Ces notions sont liées mais ne sont pas interchangeables.

# 121\. ERREURS CLASSIQUES

## Confondre :

\[ P(AB) \]

et :

\[ P(BA) \]

## Confondre indépendance et incompatibilité

## Croire que corrélation implique causalité

## Confondre moyenne et médiane

## Confondre variance et écart-type

## Oublier les hypothèses d’une loi

## Utiliser une binomiale lorsque les tirages ne sont pas indépendants

## Utiliser une hypergéométrique comme si les tirages étaient avec remise

## Interpréter incorrectement une p-value

## Confondre probabilité et vraisemblance

## Confondre prior et posterior

## Croire que Monte Carlo donne exactement le résultat avec peu d’échantillons

## Ignorer la variance d’un estimateur

# 122\. ALGORITHMES ET TECHNIQUES À CONNAÎTRE

## Fondamentaux

- calcul probabiliste ;
- Bayes ;
- probabilités totales ;
- simulation ;
- échantillonnage.

## Algorithmiques

- génération pseudo-aléatoire ;
- Monte Carlo ;
- Las Vegas ;
- rejection sampling ;
- importance sampling.

## Inférence

- Bayes ;
- Naive Bayes ;
- MCMC ;
- Metropolis-Hastings ;
- Gibbs.

## Séquentiel

- chaînes de Markov ;
- forward algorithm ;
- backward algorithm ;
- Viterbi ;
- filtrage.

## Machine learning

- maximum likelihood ;
- maximum a posteriori ;
- EM ;
- estimation bayésienne.

# 123\. STRUCTURES DE DONNÉES ASSOCIÉES

Les probabilités peuvent être représentées avec :

- tableaux de probabilités ;
- vecteurs ;
- matrices de transition ;
- histogrammes ;
- distributions discrètes ;
- arbres probabilistes ;
- graphes bayésiens ;
- tables de contingence ;
- tenseurs ;
- structures de simulation.

# 124\. COMPLEXITÉ

Une opération probabiliste peut être :

- (O(1)) ;
- (O(n)) ;
- (O(n^2)) ;
- (O(nn)) ;
- exponentielle ;
- dépendante du nombre d’états ;
- dépendante du nombre d’échantillons.

Pour Monte Carlo :

\[ N \]

échantillons impliquent généralement un coût croissant avec (N).

Dans les modèles graphiques, l’inférence exacte peut devenir très coûteuse selon la structure du graphe.

# 125\. DIMENSION ET EXPLOSION COMBINATOIRE

Un modèle comportant :

\[ n \]

variables binaires possède potentiellement :

\[ 2^n \]

configurations.

Les probabilités peuvent permettre de raisonner sur cet espace sans l’énumérer complètement.

C’est une connexion directe avec le Domaine F.

# 126\. #P ET COMPTAGE PROBABILISTE

Il faut distinguer :

- décision ;
- optimisation ;
- comptage ;
- estimation probabiliste.

Le comptage exact de solutions peut être beaucoup plus difficile que la simple question :

« Existe-t-il une solution ? »

Cette distinction devient importante dans :

- SAT ;
- CSP ;
- probabilistic inference ;
- modèles graphiques.

# 127\. PROBABILITÉS ET #SAT

#SAT demande :

combien d’affectations satisfont une formule logique ?

Cela constitue un pont entre :

- logique ;
- combinatoire ;
- complexité ;
- probabilités ;
- IA.

# 128\. MÉTHODE GÉNÉRALE DE RÉSOLUTION D’UN PROBLÈME PROBABILISTE

## Étape 1 — Définir l’expérience

Qu’est-ce qui est aléatoire ?

## Étape 2 — Définir l’espace

Quels sont les résultats possibles ?

## Étape 3 — Définir les événements

Que cherche-t-on ?

## Étape 4 — Identifier les dépendances

Les événements sont-ils indépendants ?

## Étape 5 — Choisir la représentation

- événements ;
- variable aléatoire ;
- loi ;
- distribution conditionnelle ;
- processus.

## Étape 6 — Identifier la loi

Bernoulli ?

Binomiale ?

Poisson ?

Normale ?

Exponentielle ?

Autre ?

## Étape 7 — Calculer

Probabilité ?

Espérance ?

Variance ?

Covariance ?

Posterior ?

## Étape 8 — Vérifier

Les probabilités sont-elles dans (\[0,1\]) ?

La distribution somme-t-elle à 1 ?

Les hypothèses sont-elles satisfaites ?

## Étape 9 — Interpréter

Que signifie le résultat dans le système réel ?

# 129\. FICHE DE RECONNAISSANCE RAPIDE DES LOIS

| Situation | Loi à envisager |
| --- | --- |
| Un seul succès/échec | Bernoulli |
| Nombre de succès sur (n) essais indépendants | Binomiale |
| Nombre d’essais avant succès | Géométrique |
| Tirages sans remise | Hypergéométrique |
| Nombre d’événements sur une période | Poisson |
| Temps entre événements | Exponentielle |
| Variable bornée uniforme | Uniforme |
| Somme de nombreux effets indépendants | Normale / TCL |
| Proportion ou paramètre (p) bayésien | Beta |
| Temps d’attente de plusieurs événements | Gamma |

# 130\. CATALOGUE DES FICHES INDIVIDUELLES À MAÎTRISER

Le document global doit pouvoir être décomposé en fiches spécialisées.

### Fiche G01

Espace probabilisé.

### Fiche G02

Axiomes de Kolmogorov.

### Fiche G03

Événements et opérations.

### Fiche G04

Probabilité conditionnelle.

### Fiche G05

Indépendance.

### Fiche G06

Probabilités totales.

### Fiche G07

Bayes.

### Fiche G08

Variables aléatoires.

### Fiche G09

Fonction de répartition.

### Fiche G10

Variables discrètes.

### Fiche G11

Variables continues.

### Fiche G12

Espérance.

### Fiche G13

Variance.

### Fiche G14

Covariance.

### Fiche G15

Corrélation.

### Fiche G16

Lois de Bernoulli et binomiale.

### Fiche G17

Lois géométrique et binomiale négative.

### Fiche G18

Loi hypergéométrique.

### Fiche G19

Loi de Poisson.

### Fiche G20

Lois uniforme et exponentielle.

### Fiche G21

Loi normale.

### Fiche G22

Lois Gamma et Beta.

### Fiche G23

Lois Khi-deux, Student et Fisher.

### Fiche G24

Variables aléatoires conjointes.

### Fiche G25

Espérance conditionnelle.

### Fiche G26

Variance conditionnelle.

### Fiche G27

Loi des grands nombres.

### Fiche G28

Théorème central limite.

### Fiche G29

Convergences probabilistes.

### Fiche G30

Chaînes de Markov.

### Fiche G31

Distributions stationnaires.

### Fiche G32

Marches aléatoires.

### Fiche G33

Processus de Poisson.

### Fiche G34

Martingales.

### Fiche G35

Monte Carlo.

### Fiche G36

Importance sampling.

### Fiche G37

### Fiche G38

Bayesian inference.

### Fiche G39

Naive Bayes.

### Fiche G40

Réseaux bayésiens.

### Fiche G41

Hidden Markov Models.

### Fiche G42

MDP.

### Fiche G43

Probabilités en reinforcement learning.

### Fiche G44

Maximum likelihood.

### Fiche G45

MAP.

### Fiche G46

EM.

### Fiche G47

Entropie.

### Fiche G48

Information mutuelle.

### Fiche G49

Divergence KL.

### Fiche G50

Inégalités de concentration.

### Fiche G51

Algorithmes randomisés.

### Fiche G52

Probabilités et systèmes distribués.

### Fiche G53

Files d’attente.

### Fiche G54

Fiabilité.

### Fiche G55

Détection d’anomalies.

### Fiche G56

Simulation probabiliste.

# 131\. PROJETS PRATIQUES PROGRESSIFS

## Projet 1 — Simulateur de dés

Construire un programme simulant :

- 1 lancer ;
- 100 lancers ;
- 10 000 lancers ;
- 1 000 000 lancers.

Comparer :

\[ fréquence empirique \]

et :

\[ probabilité théorique \]

## Projet 2 — Simulateur binomial

Permettre à l’utilisateur de choisir :

\[ n,p \]

et observer la distribution des succès.

## Projet 3 — Simulateur de Poisson

Simuler des arrivées de requêtes sur un serveur.

Analyser :

- moyenne ;
- variance ;
- histogramme ;
- événements rares.

## Projet 4 — Monte Carlo

Estimer () par tirage de points aléatoires.

## Projet 5 — Détection d’anomalies

Créer un système simple calculant un score probabiliste.

## Projet 6 — Naive Bayes

Construire un classifieur de texte.

Applications possibles :

- spam ;
- sentiment ;
- catégories.

## Projet 7 — Chaîne de Markov

Créer un système de navigation entre états.

## Projet 8 — Random Walk

Simuler un agent se déplaçant aléatoirement dans :

- une ligne ;
- une grille ;
- un graphe.

## Projet 9 — Réseau bayésien

Construire un petit réseau permettant d’effectuer des inférences.

## Projet 10 — Monte Carlo en 2D

Estimer :

- aire ;
- intégrale ;
- probabilité de collision.

## Projet 11 — MCMC

Implémenter une chaîne de Markov simple et observer sa convergence.

## Projet 12 — Agent probabiliste

Créer un agent dont les actions sont échantillonnées selon :

\[ (as) \]

# 132\. EXERCICES DE MAÎTRISE

## Niveau 1 — Reconnaissance

Identifier :

- expérience ;
- univers ;
- événement ;
- variable ;
- loi.

## Niveau 2 — Calcul

Calculer :

- probabilités ;
- Bayes ;
- espérance ;
- variance ;
- covariance.

## Niveau 3 — Modélisation

Choisir correctement une loi.

## Niveau 4 — Simulation

Vérifier expérimentalement un résultat théorique.

## Niveau 5 — Inférence

Construire un modèle conditionnel.

## Niveau 6 — Processus

Analyser une chaîne de Markov.

## Niveau 7 — IA

Construire un classifieur probabiliste.

## Niveau 8 — Recherche

Comparer :

- Monte Carlo ;
- MCMC ;
- importance sampling ;
- inférence exacte.

# 133\. DÉFIS SANS IA

Pour vérifier la compréhension réelle :

### Défi 1

Démontrer Bayes à partir de la définition de la probabilité conditionnelle.

### Défi 2

Dériver l’espérance d’une binomiale.

### Défi 3

Dériver sa variance.

### Défi 4

Expliquer pourquoi l’exponentielle est sans mémoire.

### Défi 5

Simuler une loi sans utiliser directement une fonction spécialisée.

### Défi 6

Expliquer le TCL sans réciter sa définition.

### Défi 7

Construire une chaîne de Markov à la main.

### Défi 8

Expliquer la différence entre :

\[ P(AB) \]

et :

\[ P(BA) \]

avec un exemple concret.

# 134\. DÉFIS AVEC IA

L’IA peut être utilisée comme :

- professeur ;
- générateur d’exercices ;
- vérificateur ;
- simulateur ;
- adversaire pédagogique ;
- analyste d’erreurs.

Mais le raisonnement probabiliste doit rester maîtrisé par l’étudiant.

Exemple de défi :

Demander à une IA de générer un problème Bayésien, résoudre seul, puis utiliser l’IA uniquement pour auditer le raisonnement.

# 135\. CONNEXIONS AVEC LES DOMAINES PRÉCÉDENTS

## F → G

La combinatoire permet de calculer :

\[ || \]

Les probabilités permettent ensuite de calculer :

\[ P(A) \]

sur cet espace.

## E → G

Les graphes deviennent :

- probabilistes ;
- markoviens ;
- bayésiens ;
- stochastiques.

## C → G

Les matrices deviennent :

- matrices de covariance ;
- matrices de transition ;
- opérateurs probabilistes.

## D → G

La géométrie peut devenir aléatoire :

- points aléatoires ;
- trajectoires ;
- Monte Carlo ;
- simulation.

# 136\. CARTE CONCEPTUELLE GLOBALE

On peut résumer le domaine par :

\[ \]

puis :

\[ \]

puis :

\[ \]

puis :

\[ \]

et enfin :

\[ \]

# 137\. CRITÈRE DE MAÎTRISE

La maîtrise du Domaine G ne signifie pas connaître par cœur toutes les distributions.

Elle signifie pouvoir :

1.  reconnaître l’incertitude ;
2.  formaliser l’expérience ;
3.  définir les événements ;
4.  choisir une variable aléatoire ;
5.  identifier une loi adaptée ;
6.  calculer une probabilité ;
7.  utiliser une condition ;
8.  appliquer Bayes ;
9.  calculer une espérance ;
10. mesurer une variance ;
11. comprendre covariance et corrélation ;
12. manipuler des distributions conjointes ;
13. raisonner avec l’espérance conditionnelle ;
14. comprendre LGN et TCL ;
15. modéliser un processus temporel ;
16. comprendre une chaîne de Markov ;
17. simuler un phénomène ;
18. utiliser Monte Carlo ;
19. comprendre l’inférence bayésienne ;
20. relier les probabilités au machine learning ;
21. reconnaître les hypothèses d’un modèle ;
22. identifier les limites d’une interprétation probabiliste.

# 138\. CHECKLIST FINALE DE MAÎTRISE

## Fondements

- Univers
- Événement
- Axiomes
- Probabilité
- Complément
- Union
- Intersection

## Conditionnement

- Probabilité conditionnelle
- Produit
- Indépendance
- Probabilités totales
- Bayes

## Variables

- Variable aléatoire
- Discrète
- Continue
- Fonction de répartition
- Densité
- Distribution conjointe

## Moments

- Espérance
- Variance
- Écart-type
- Covariance
- Corrélation
- Moments supérieurs

## Lois

- Bernoulli
- Binomiale
- Géométrique
- Hypergéométrique
- Poisson
- Uniforme
- Exponentielle
- Normale
- Gamma
- Beta
- Khi-deux
- Student

## Convergence

- Loi des grands nombres
- TCL
- Convergence en probabilité
- Convergence en loi
- Convergence presque sûre

## Processus

- Markov
- Matrice de transition
- Distribution stationnaire
- Random walk
- Processus de Poisson
- Martingales

## Simulation

- Génération aléatoire
- Monte Carlo
- Rejection sampling
- Importance sampling
- MCMC

## IA

- Naive Bayes
- Réseaux bayésiens
- HMM
- MDP
- RL probabiliste
- Maximum likelihood
- MAP
- EM
- Modèles génératifs

## Information

- Entropie
- Entropie conditionnelle
- Information mutuelle
- KL divergence

## Systèmes

- Files d’attente
- Fiabilité
- Disponibilité
- Détection d’anomalies
- Simulation
- Algorithmes randomisés

# 139\. SYNTHÈSE ULTIME

Le Domaine G peut être résumé par cinq questions fondamentales :

### 1\. Qu’est-ce qui peut arriver ?

\[ \]

### 2\. Avec quelle probabilité ?

\[ P(A) \]

### 3\. Que devient cette probabilité lorsqu’une information est connue ?

\[ P(AB) \]

### 4\. Que peut-on attendre en moyenne ?

\[ E\[X\] \]

### 5\. Comment évolue l’incertitude dans le temps ?

\[ {X_t}\_{tT} \]

À partir de ces questions se construisent :

\[ \]

# 140\. POSITION DU DOMAINE G DANS LA CARTOGRAPHIE GLOBALE

La progression des domaines peut maintenant être comprise comme :

\[ A: \]

\[ B: \]

\[ C: \]

\[ D: \]

\[ E: \]

\[ F: \]

\[ G: \]

Le Domaine G apporte donc une nouvelle capacité fondamentale :

**ne plus seulement demander ce qui est possible ou optimal, mais quantifier ce qui est probable, ce qui est incertain, ce qui est attendu et ce qui peut être inféré à partir d’informations incomplètes.**

C’est cette capacité qui permet ensuite de construire une grande partie de la mathématique moderne de l’intelligence artificielle.

# CONCLUSION DU DOMAINE G

La probabilité n’est pas simplement une collection de formules sur les dés, les pièces ou les tirages.

Dans l’informatique moderne, elle constitue un **langage mathématique de l’incertitude**.

Elle permet de passer :

\[ \]

et :

\[ \]

Elle fournit ainsi une infrastructure commune à :

- l’inférence statistique ;
- le machine learning ;
- les réseaux bayésiens ;
- le NLP ;
- les modèles génératifs ;
- la simulation ;
- les systèmes distribués ;
- les algorithmes randomisés ;
- les processus stochastiques ;
- le reinforcement learning ;
- la décision sous incertitude.

**Idée centrale du Domaine G :**

\[ \]

**Domaine suivant : Domaine H — à définir selon la cartographie mathématique globale du projet.**