# DOCUMENT J — OPTIMISATION

## Cartographie complète pour l’intelligence artificielle, le machine learning, les systèmes et l’ingénierie

# 0\. IDENTITÉ DU DOMAINE

## Nom

**Domaine J — Optimisation**

## Définition générale

L’optimisation est l’ensemble des méthodes mathématiques et algorithmiques permettant de **chercher la meilleure solution possible selon un objectif donné, sous un ensemble éventuel de contraintes**.

De manière abstraite, un problème d’optimisation cherche une variable (x) qui minimise ou maximise une fonction objectif :

\[ \]

ou

\[ \]

où :

- (x) représente la solution recherchée ;
- (f(x)) représente le coût, l’erreur, la perte, le risque, le temps ou tout autre critère à optimiser ;
- () représente l’ensemble des solutions admissibles.

L’optimisation ne consiste donc pas simplement à « trouver une valeur ».

Elle consiste à répondre à une question beaucoup plus générale :

**Parmi toutes les solutions possibles, laquelle satisfait le mieux notre objectif tout en respectant les contraintes du problème ?**

# 1\. PLACE DE L’OPTIMISATION DANS LA CARTOGRAPHIE MATHÉMATIQUE

L’optimisation constitue l’un des points de convergence majeurs des domaines précédents.

On peut représenter une partie de la chaîne ainsi :

\[ \]

Mais l’optimisation utilise également :

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

Ainsi, le Domaine J n’est pas isolé.

Il constitue un **carrefour mathématique et algorithmique**.

# 2\. POURQUOI L’OPTIMISATION EST CENTRALE EN INFORMATIQUE

Une immense partie de l’informatique peut être formulée comme un problème d’optimisation.

Exemples :

### Machine learning

Chercher les paramètres d’un modèle qui minimisent l’erreur :

\[ ^\* = _ L() \]

### Réseaux

Chercher le chemin minimisant le coût :

\[ P^\* = \_P (P) \]

### Logistique

Minimiser :

\[

- \]

### Scheduling

Minimiser :

\[ \]

ou :

\[ \]

### Robotique

Chercher une trajectoire :

\[ ^\* = _ J() \]

### Allocation de ressources

Répartir des ressources limitées pour maximiser une utilité.

### Finance

Optimiser un portefeuille sous contraintes de risque et de rendement.

### Computer graphics

Choisir des paramètres permettant de minimiser une erreur de reconstruction, une énergie ou une fonction de coût géométrique.

# 3\. VOCABULAIRE FONDAMENTAL

## 3.1 Variable de décision

La variable que l’algorithme cherche à déterminer.

Exemple :

\[ x=(x_1,x_2,,x_n) \]

## 3.2 Fonction objectif

Fonction représentant ce que l’on souhaite minimiser ou maximiser.

Exemple :

\[ f(x)=x^2+3x+2 \]

## 3.3 Fonction de coût

Terme souvent utilisé lorsque l’on cherche une valeur minimale.

\[ \_x C(x) \]

## 3.4 Fonction de perte

En machine learning :

\[ L() \]

mesure l’écart entre les prédictions du modèle et les observations.

## 3.5 Contrainte

Condition que la solution doit respecter.

Exemple :

\[ x_1+x_2 \]

## 3.6 Domaine admissible

Ensemble des solutions satisfaisant toutes les contraintes.

\[ = {x : g_i(x), h_j(x)=0} \]

## 3.7 Solution admissible

Solution appartenant au domaine faisable.

## 3.8 Optimum

Solution atteignant une valeur optimale de la fonction objectif.

## 3.9 Optimum local

Solution meilleure que toutes les solutions suffisamment proches.

## 3.10 Optimum global

Solution meilleure que toutes les solutions admissibles.

## 3.11 Fonction convexe

Fonction ayant une géométrie particulièrement favorable à l’optimisation.

Pour une fonction convexe :

\[ f(x+(1-)y) f(x)+(1-)f(y) \]

pour :

\[ 0 \]

## 3.12 Paysage d’optimisation

On peut imaginer la fonction objectif comme un paysage :

- sommets → maxima ;
- vallées → minima ;
- plateaux → régions de faible variation ;
- cols → points selles ;
- vallées profondes → minima potentiellement attractifs.

Cette représentation devient particulièrement importante en machine learning.

# 4\. FORMULATION GÉNÉRALE D’UN PROBLÈME D’OPTIMISATION

La forme générale peut être écrite :

\[ \]

sous :

\[ g_i(x) \]

et :

\[ h_j(x)=0 \]

On peut donc avoir :

\[ \]

Cette formulation est fondamentale.

Elle permet de reconnaître immédiatement qu’un problème informatique possède une structure d’optimisation.

# 5\. MINIMUM ET MAXIMUM

## 5.1 Minimum

Un point (x^\*) est un minimum global si :

\[ f(x^\*)f(x) \]

pour tout (x) admissible.

## 5.2 Maximum

Un point (x^\*) est un maximum global si :

\[ f(x^\*)f(x) \]

pour tout (x) admissible.

## 5.3 Transformer un maximum en minimum

Un problème :

\[ \_x f(x) \]

peut être transformé en :

\[ \_x -f(x) \]

Cette transformation est extrêmement fréquente dans les bibliothèques d’optimisation.

# 6\. OPTIMUM LOCAL ET GLOBAL

## 6.1 Minimum local

(x^_) est un minimum local s’il existe un voisinage autour de (x^_) tel que :

\[ f(x^\*)f(x) \]

dans ce voisinage.

## 6.2 Minimum global

\[ f(x^\*)f(x) \]

pour tout (x) admissible.

## 6.3 Pourquoi cette distinction est fondamentale

Une méthode peut trouver :

\[ x_{}^\* \]

sans trouver :

\[ x_{}^\* \]

Dans les problèmes non convexes, le paysage peut contenir :

- plusieurs minima ;
- maxima ;
- points selles ;
- plateaux ;
- régions très plates ;
- vallées étroites.

C’est une difficulté majeure du machine learning moderne.

# 7\. CONDITIONS DU PREMIER ORDRE

Pour une fonction différentiable :

\[ f:^n \]

un optimum intérieur peut satisfaire :

\[ \]

Cela signifie que toutes les dérivées partielles sont nulles :

\[ =0, , =0 \]

Attention :

\[ f(x)=0 \]

ne signifie pas nécessairement que (x) est un minimum.

Cela peut être :

- un minimum ;
- un maximum ;
- un point selle ;
- un point stationnaire dégénéré.

# 8\. CONDITIONS DU SECOND ORDRE

La Hessienne :

\[ H_f(x) = ^2 f(x) \]

permet d’étudier la courbure locale.

Pour un point stationnaire (x^\*) :

### Hessienne définie positive

\[ H_f(x^\*) \]

→ minimum local strict.

### Hessienne définie négative

\[ H_f(x^\*) \]

→ maximum local strict.

### Hessienne indéfinie

→ point selle.

Cette relation constitue l’un des ponts fondamentaux entre :

**calcul différentiel → optimisation.**

# 9\. CONVEXITÉ

La convexité est l’un des concepts les plus importants de tout le domaine.

Une fonction convexe satisfait :

\[ f(x+(1-)y) f(x)+(1-)f(y) \]

## 9.1 Pourquoi la convexité est si importante

Dans un problème de minimisation convexe :

\[ \_x f(x) \]

tout minimum local est également un minimum global.

C’est une propriété extrêmement puissante.

Elle simplifie considérablement l’optimisation.

# 10\. CONVEXITÉ ET HESSIENNE

Pour une fonction deux fois différentiable :

\[ f:^n \]

une condition classique de convexité est :

\[ \]

pour tout (x).

Autrement dit, la Hessienne est semi-définie positive partout.

Pour une convexité stricte, on recherche des conditions plus fortes, typiquement :

\[ ^2 f(x) \]

dans les contextes appropriés.

# 11\. PROBLÈMES CONVEXES ET NON CONVEXES

## Problème convexe

Structure favorable :

\[ f(x) \]

avec :

- (f) convexe ;
- domaine admissible convexe ;
- contraintes appropriées.

## Problème non convexe

Le paysage peut contenir :

\[

- \]

Les réseaux neuronaux profonds sont généralement associés à des problèmes d’optimisation non convexes.

# 12\. OPTIMISATION SANS CONTRAINTES

Forme :

\[ \]

sans restriction supplémentaire.

Exemple :

\[ f(x)=x^2 \]

Le minimum est :

\[ x^\*=0 \]

# 13\. OPTIMISATION SOUS CONTRAINTES

Forme :

\[ \_x f(x) \]

sous :

\[ g_i(x) \]

et :

\[ h_j(x)=0 \]

Cette formulation est omniprésente dans :

- robotique ;
- finance ;
- logistique ;
- allocation ;
- planification ;
- ingénierie ;
- ML contraint.

# 14\. CONTRAINTES D’ÉGALITÉ

Exemple :

\[ x+y=10 \]

On ne peut pas choisir librement (x) et (y).

La solution doit appartenir à l’ensemble :

\[ {(x,y):x+y=10} \]

# 15\. CONTRAINTES D’INÉGALITÉ

Exemple :

\[ x+y \]

ou :

\[ x \]

ou :

\[ 0x \]

Ces contraintes permettent de représenter des limites physiques, économiques ou techniques.

# 16\. MULTIPLICATEURS DE LAGRANGE

Pour :

\[ \_x f(x) \]

sous :

\[ g(x)=0 \]

on construit le Lagrangien :

\[ \]

Les conditions stationnaires sont :

\[ \_x=0 \]

et :

\[ g(x)=0 \]

## 16.1 Interprétation

Le multiplicateur () peut être interprété comme une mesure de la sensibilité de l’optimum à la contrainte dans certains cadres réguliers.

Cette interprétation devient très importante en économie, finance et optimisation des ressources.

# 17\. CONDITIONS KKT

Les conditions de Karush-Kuhn-Tucker généralisent les multiplicateurs de Lagrange aux problèmes comportant notamment des contraintes d’inégalité.

Pour :

\[ \_x f(x) \]

sous :

\[ g_i(x) \]

et :

\[ h_j(x)=0 \]

on introduit des multiplicateurs :

\[ \_i \]

et (\_j).

Le Lagrangien devient :

\[ (x,,) = f(x)

- \_i_i g_i(x)
- \_j_j h_j(x) \]

Les KKT comprennent notamment :

### Stationnarité

\[ \_x=0 \]

### Faisabilité primale

\[ g_i(x) \]

\[ h_j(x)=0 \]

### Faisabilité duale

\[ \_i \]

### Complémentarité

\[ \]

Ces conditions sont fondamentales en optimisation sous contraintes.

# 18\. DUALITÉ

À un problème primal peut être associé un problème dual.

On peut avoir :

\[ \]

La dualité permet notamment :

- de produire des bornes ;
- d’analyser les contraintes ;
- de transformer certains problèmes ;
- de concevoir des algorithmes ;
- d’étudier les conditions d’optimalité.

Dans certains problèmes convexes, sous des hypothèses appropriées, la dualité forte donne :

\[ \]

où (p^_) et (d^_) représentent les valeurs optimales primal et dual.

# 19\. PROGRAMMATION LINÉAIRE

La programmation linéaire, ou LP, optimise une fonction linéaire sous contraintes linéaires.

Forme générale :

\[ \]

sous :

\[ Axb \]

et éventuellement :

\[ x \]

## Applications

- transport ;
- production ;
- allocation ;
- planification ;
- réseaux ;
- gestion des ressources ;
- supply chain.

# 20\. GÉOMÉTRIE DE LA PROGRAMMATION LINÉAIRE

Les contraintes définissent un polyèdre admissible.

L’optimum, lorsqu’il existe et dans les conditions usuelles, peut être recherché parmi les points extrêmes du domaine faisable.

Cette observation est fondamentale pour comprendre les algorithmes de programmation linéaire.

# 21\. ALGORITHME DU SIMPLEXE

Le simplexe explore les sommets du polyèdre admissible.

Conceptuellement :

\[ \]

jusqu’à atteindre une solution optimale ou détecter certaines situations particulières.

# 22\. MÉTHODES DE POINT INTÉRIEUR

Les méthodes de point intérieur cherchent à progresser à l’intérieur du domaine admissible plutôt qu’à suivre nécessairement les sommets.

Elles constituent une famille majeure d’algorithmes modernes de programmation convexe et linéaire.

# 23\. PROGRAMMATION ENTIÈRE

Dans une programmation entière, certaines variables doivent être entières :

\[ x_i \]

Exemple :

\[ x_i{0,1} \]

pour représenter :

- choisir/ne pas choisir ;
- ouvrir/fermer ;
- affecter/ne pas affecter ;
- activer/désactiver.

# 24\. PROGRAMMATION BINAIRE

Cas particulier :

\[ x_i{0,1} \]

Elle est extrêmement utile pour modéliser des décisions discrètes.

Exemples :

### Sélection de projets

\[ x_i=1 \]

si le projet (i) est sélectionné.

### Affectation

\[ x_{ij}=1 \]

si la tâche (i) est affectée à la ressource (j).

# 25\. MIXED-INTEGER PROGRAMMING

Un problème peut mélanger :

- variables continues ;
- variables entières ;
- variables binaires.

On obtient alors un problème de programmation mixte en nombres entiers, souvent appelé **MILP/MIP** selon le cadre.

Applications :

- scheduling ;
- logistique ;
- production ;
- allocation ;
- énergie ;
- réseaux.

# 26\. OPTIMISATION COMBINATOIRE

Lorsque les solutions sont discrètes et nombreuses :

\[ x \]

avec (||) potentiellement énorme.

Exemples :

- voyageur de commerce ;
- sac à dos ;
- coloration ;
- ordonnancement ;
- affectation ;
- couverture ;
- sélection.

Cela relie directement le Domaine J au **Domaine F — Combinatoire** et au **Domaine E — Graphes**.

# 27\. PROGRAMMATION DYNAMIQUE

La programmation dynamique exploite une structure de sous-problèmes.

Une formulation typique :

\[ DP\[s\] = s \]

avec une relation de récurrence :

\[ DP\[s\] = \_{a} { (s,a)+DP\[s’\] } \]

## Conditions favorables

La programmation dynamique devient particulièrement utile lorsqu’un problème possède :

1.  une structure de sous-problèmes ;
2.  des sous-problèmes qui se recouvrent ;
3.  une propriété de sous-structure optimale.

# 28\. EXEMPLES DE PROGRAMMATION DYNAMIQUE

- sac à dos ;
- plus court chemin dans certains contextes ;
- distance d’édition ;
- alignement de séquences ;
- segmentation ;
- planification ;
- contrôle ;
- problèmes de décision.

# 29\. OPTIMISATION DIFFÉRENTIABLE

Pour :

\[ f:^n \]

on peut utiliser :

\[ f(x) \]

pour déterminer la direction de croissance maximale locale.

Pour minimiser (f), on se déplace généralement dans la direction opposée :

\[ -f(x) \]

C’est le fondement du gradient descent.

# 30\. GRADIENT DESCENT

L’algorithme fondamental :

\[ \]

où :

- (x_t) est la solution actuelle ;
- () est le learning rate ;
- (f(x_t)) est le gradient.

# 31\. INTERPRÉTATION DU LEARNING RATE

Le learning rate contrôle la taille du déplacement.

### Trop petit

\[ \]

→ convergence potentiellement très lente.

### Trop grand

\[ \]

→ oscillations ou divergence possibles.

### Adapté

→ progression efficace vers une région optimale.

Le choix de () est donc une question d’optimisation à part entière.

# 32\. DESCENTE DE GRADIENT STOCHASTIQUE

En machine learning, au lieu de calculer le gradient sur tout le dataset :

\[ L() \]

on peut utiliser un mini-batch (B) :

\[ \]

C’est la base du **Stochastic Gradient Descent — SGD** et de nombreuses variantes.

# 33\. BATCH, STOCHASTIC ET MINI-BATCH

### Batch Gradient Descent

Utilise toutes les données.

### SGD

Utilise un exemple ou une très petite quantité de données.

### Mini-batch Gradient Descent

Utilise un sous-ensemble :

\[ BD \]

Le mini-batch est devenu une stratégie centrale dans l’entraînement des réseaux neuronaux.

# 34\. MOMENTUM

Le momentum introduit une mémoire de la direction précédente.

Une forme classique :

\[ v_t = v_{t-1}

- f(x_t) \]

puis :

\[ x_{t+1} = x_t-v_t \]

L’objectif est notamment de réduire certaines oscillations et d’accélérer la progression dans des directions cohérentes.

# 35\. ADAGRAD

Adagrad adapte le learning rate aux paramètres.

L’idée générale est de diminuer progressivement le pas pour les paramètres ayant accumulé beaucoup de gradient.

Cela peut être utile pour certaines données clairsemées.

# 36\. RMSPROP

RMSProp utilise une moyenne mobile des carrés des gradients afin d’adapter l’échelle des mises à jour.

# 37\. ADAM

Adam combine des idées proches du momentum et d’une adaptation de l’échelle des gradients.

Il maintient notamment des estimations de :

\[ m_t \]

et :

\[ v_t \]

puis construit une mise à jour adaptative.

Adam est très utilisé pour l’entraînement de réseaux neuronaux.

# 38\. SCHEDULES DU LEARNING RATE

Le learning rate peut être modifié pendant l’entraînement.

Exemples :

- décroissance ;
- step decay ;
- cosine decay ;
- warmup ;
- réduction selon une métrique ;
- schedules cycliques.

Le choix de la trajectoire du learning rate peut fortement influencer l’apprentissage.

# 39\. CRITÈRES D’ARRÊT

Une optimisation doit généralement savoir quand s’arrêter.

Critères possibles :

\[ |f(x)|< \]

ou :

\[ |f(x_{t+1})-f(x_t)|< \]

ou :

\[ |x_{t+1}-x_t|< \]

ou simplement :

\[ tT_{} \]

En ML, on peut également utiliser la validation et l’early stopping.

# 40\. NEWTON

La méthode de Newton utilise la dérivée seconde.

En dimension 1 :

\[ \]

En dimension (n) :

\[ \]

lorsque la Hessienne est inversible.

# 41\. INTERPRÉTATION DE NEWTON

Gradient descent utilise principalement :

\[ \]

Newton utilise :

\[

- \]

Cela peut permettre une convergence beaucoup plus rapide près de l’optimum.

Mais le coût de calcul de la Hessienne et de sa résolution peut être important.

# 42\. QUASI-NEWTON

Les méthodes quasi-Newton cherchent à obtenir les avantages de Newton sans calculer explicitement toute la Hessienne.

Elles construisent une approximation :

\[ B_tH_f(x_t) \]

ou de son inverse.

Exemples :

- BFGS ;
- L-BFGS.

## L-BFGS

L-BFGS est particulièrement intéressant lorsque le nombre de paramètres est élevé, car il évite de stocker une Hessienne complète.

# 43\. COMPARAISON DES MÉTHODES DIFFÉRENTIELLES

| Méthode | Information principale | Coût par étape | Usage typique |
| --- | --- | --- | --- |
| Gradient descent | Gradient | Faible | ML  |
| SGD | Gradient estimé | Très faible | Deep learning |
| Momentum | Gradient + mémoire | Faible | ML  |
| Adam | Gradient adaptatif | Faible | Deep learning |
| Newton | Gradient + Hessienne | Élevé | optimisation avancée |
| BFGS | approximation Hessienne | Moyen | optimisation numérique |
| L-BFGS | approximation compacte | Moyen | grands problèmes |

Il ne faut pas interpréter ce tableau comme un classement universel.

Le meilleur algorithme dépend de :

- dimension ;
- structure ;
- convexité ;
- bruit ;
- contraintes ;
- coût des gradients ;
- précision souhaitée ;
- architecture du problème.

# 44\. BACKPROPAGATION ET OPTIMISATION

Le calcul différentiel permet de calculer :

\[ \]

La backpropagation permet de calculer efficacement ces dérivées dans un réseau.

L’optimiseur utilise ensuite ces gradients :

\[ \_{t+1} = \_t

- \_L \]

Ainsi :

\[ \]

# 45\. CHAÎNE FONDAMENTALE POUR LE MACHINE LEARNING

La chaîne du Domaine I devient ici :

\[ f(x) f’(x) f(x) ^\* \]

Cette chaîne constitue l’un des mécanismes fondamentaux de l’apprentissage supervisé moderne.

# 46\. FONCTION DE PERTE

Le problème d’apprentissage peut être écrit :

\[ \]

Exemples :

### Régression

Erreur quadratique :

\[ MSE = 1n \_{i=1}^{n} (y_i-y_i)^2 \]

### Classification

Cross-entropy :

\[ L = -\_i y_i(y_i) \]

Le choix de la fonction de perte définit ce que signifie « faire une bonne prédiction » pour le modèle.

# 47\. RÉGULARISATION COMME PROBLÈME D’OPTIMISATION

On peut ajouter une pénalité :

\[ \]

Exemples :

### L2

\[ R()=||\_2^2 \]

### L1

\[ R()=||\_1 \]

La régularisation modifie donc directement le problème d’optimisation.

# 48\. OPTIMISATION ET GÉNÉRALISATION

Minimiser parfaitement la perte d’entraînement ne garantit pas une bonne généralisation.

On distingue :

\[ L_{} \]

et :

\[ L_{} \]

Un modèle peut avoir :

\[ L_{} \]

mais :

\[ L_{} \]

Le problème n’est donc pas uniquement :

« trouver le minimum ».

Il faut également considérer :

**quel minimum, avec quelle régularisation, quelle stabilité et quelle généralisation ?**

# 49\. PAYSAGE DE PERTE DES RÉSEAUX NEURONAUX

Pour un réseau :

\[ L() \]

où () peut contenir des millions ou milliards de paramètres, l’espace d’optimisation est extrêmement dimensionnel.

On rencontre :

- vallées ;
- plateaux ;
- points selles ;
- directions de forte courbure ;
- directions de faible courbure ;
- symétries ;
- minima multiples.

La visualisation classique en 2D ou 3D est donc une représentation simplifiée d’un phénomène beaucoup plus complexe.

# 50\. OPTIMISATION STOCHASTIQUE

Lorsque le gradient est bruité :

\[ g_t = f(x_t)

- \_t \]

l’algorithme travaille avec une estimation du gradient.

Cette stochasticité peut être :

- une difficulté ;
- une source d’instabilité ;
- mais également une propriété utile permettant d’explorer le paysage.

# 51\. BATCH ET BRUIT DU GRADIENT

La taille du batch influence :

- le coût computationnel ;
- le bruit du gradient ;
- l’utilisation du GPU ;
- la stabilité des mises à jour ;
- parfois la dynamique de généralisation.

Il existe donc un compromis entre :

\[ \]

et :

\[ \]

# 52\. OPTIMISATION GLOBALE

Lorsque le problème est non convexe ou discret, trouver le meilleur optimum global peut être difficile.

On peut utiliser :

- recherche exhaustive ;
- branch and bound ;
- programmation dynamique ;
- relaxation ;
- recherche locale ;
- recuit simulé ;
- algorithmes génétiques ;
- recherche tabou ;
- méthodes évolutionnaires ;
- optimisation bayésienne ;
- méthodes multi-start.

# 53\. RECHERCHE LOCALE

Une recherche locale commence à partir d’une solution et explore son voisinage.

Schéma :

\[ x N(x) x’ N(x’) \]

Elle est souvent efficace mais peut rester bloquée dans un optimum local.

# 54\. RECHERCHE MULTI-START

On lance une recherche locale depuis plusieurs points initiaux :

\[ x_0^{(1)}, x_0^{(2)}, , x_0^{(k)} \]

Puis on conserve la meilleure solution obtenue.

Cela permet de réduire la dépendance à l’initialisation.

# 55\. RECUIT SIMULÉ

Le recuit simulé s’inspire métaphoriquement du refroidissement progressif d’un matériau.

Il peut accepter temporairement une solution moins bonne afin d’échapper à un optimum local.

Une probabilité typique d’acceptation est :

\[ P = ( - ) \]

où :

- (E) est l’augmentation de coût ;
- (T) est la température.

Lorsque (T) diminue, les détours deviennent progressivement moins probables.

# 56\. ALGORITHMES GÉNÉTIQUES

Les algorithmes génétiques représentent des solutions comme des individus.

Une population :

\[ P={x_1,x_2,,x_n} \]

évolue grâce notamment à :

- sélection ;
- croisement ;
- mutation ;
- évaluation de fitness.

Schéma :

\[ \]

# 57\. FITNESS

La fonction de fitness mesure la qualité d’une solution.

Selon le problème :

\[ (x) \]

peut être :

- une récompense ;
- une performance ;
- l’inverse d’un coût ;
- une combinaison de plusieurs critères.

# 58\. RECHERCHE TABOU

La recherche tabou mémorise certaines solutions ou transformations récemment utilisées afin d’éviter de revenir immédiatement vers les mêmes régions de l’espace de recherche.

Elle appartient aux méthodes de **métaheuristique**.

# 59\. MÉTAHEURISTIQUES

Une métaheuristique fournit une stratégie générale pour explorer des espaces de recherche complexes.

Exemples :

- recuit simulé ;
- algorithmes génétiques ;
- recherche tabou ;
- colonies de fourmis ;
- essaims particulaires ;
- évolution différentielle.

Elles sont particulièrement intéressantes lorsque :

- le problème est non convexe ;
- l’espace est discret ;
- le gradient est indisponible ;
- l’évaluation est possible mais la structure mathématique est difficile à exploiter.

# 60\. OPTIMISATION SANS GRADIENT

Certaines fonctions ne sont :

- pas différentiables ;
- pas continues ;
- trop coûteuses à différencier ;
- accessibles uniquement comme boîte noire.

On peut alors utiliser :

- Nelder-Mead ;
- recherche locale ;
- évolution ;
- recuit ;
- optimisation bayésienne ;
- méthodes par échantillonnage.

# 61\. OPTIMISATION BAYÉSIENNE

L’optimisation bayésienne est particulièrement adaptée aux fonctions coûteuses à évaluer.

On construit un modèle probabiliste approximatif de la fonction objectif.

Puis on choisit intelligemment le prochain point à tester.

Principe :

\[ \]

Applications :

- hyperparamètres ML ;
- expérimentation coûteuse ;
- ingénierie ;
- simulation ;
- conception.

# 62\. EXPLORATION ET EXPLOITATION

Un problème central de nombreuses méthodes :

### Exploration

Chercher de nouvelles régions.

### Exploitation

Améliorer une région déjà prometteuse.

Ce compromis apparaît dans :

- optimisation globale ;
- recherche ;
- reinforcement learning ;
- bandits ;
- métaheuristiques.

# 63\. OPTIMISATION MULTI-OBJECTIFS

Certains problèmes possèdent plusieurs objectifs :

\[ f_1(x),f_2(x),,f_k(x) \]

Par exemple :

\[ \]

tout en :

\[ \]

et :

\[ \]

Ces objectifs peuvent être contradictoires.

# 64\. FRONT DE PARETO

Une solution est dite non dominée lorsqu’aucune autre solution n’est au moins aussi bonne sur tous les objectifs et strictement meilleure sur l’un d’eux.

L’ensemble des solutions non dominées constitue le **front de Pareto**.

C’est fondamental pour :

- ingénierie ;
- architecture système ;
- design ;
- logistique ;
- finance ;
- IA multi-critères.

# 65\. SCALARISATION

On peut combiner plusieurs objectifs :

\[ F(x) = \_1 f_1(x)

- \_2 f_2(x)

- \_k f_k(x) \]

avec des poids :

\[ \_i \]

Cette méthode transforme un problème multi-objectifs en un problème scalaire, mais elle impose des choix sur l’importance relative des objectifs.

# 66\. OPTIMISATION ROBUSTE

On peut chercher une solution qui reste performante lorsque les données ou paramètres changent.

Au lieu de :

\[ \_x f(x) \]

on peut considérer :

\[ _x_ {} f(x,) \]

où () représente une incertitude.

Applications :

- ingénierie ;
- réseaux ;
- finance ;
- contrôle ;
- systèmes critiques.

# 67\. OPTIMISATION STOCHASTIQUE

Lorsque les paramètres ou observations sont aléatoires :

\[ P \]

on peut chercher :

\[ \]

Cette formulation est extrêmement importante en machine learning.

# 68\. EMPIRICAL RISK MINIMIZATION

En apprentissage supervisé :

\[ R() = 1n _{i=1}^{n} L(f_(x_i),y_i) \]

On cherche :

\[ \]

C’est une formulation centrale du machine learning statistique.

# 69\. CONTRAINTE DE NORME ET OPTIMISATION

On peut imposer :

\[ ||C \]

ou ajouter :

\[ || \]

Cette idée relie :

- optimisation ;
- régularisation ;
- généralisation ;
- géométrie ;
- statistiques.

# 70\. OPTIMISATION ET CLASSIFICATION

Un classifieur peut être entraîné par minimisation d’une fonction de perte.

Exemple conceptuel :

\[ _ 1n _i L(y_i,f_(x_i)) \]

Les différents modèles peuvent donc être vus comme différentes familles de problèmes d’optimisation.

# 71\. OPTIMISATION ET RÉSEAUX NEURONAUX

Un réseau neuronal possède des paramètres :

\[ \]

et produit :

\[ y=f_(x) \]

L’entraînement cherche :

\[ ^\* = _L(f_(x),y) \]

La chaîne complète est :

\[ \]

# 72\. OPTIMISATION ET HYPERPARAMÈTRES

Il faut distinguer :

### Paramètres

Appris pendant l’entraînement.

Exemple :

\[ W,b \]

### Hyperparamètres

Choisis par le concepteur.

Exemples :

- learning rate ;
- batch size ;
- nombre de couches ;
- régularisation ;
- architecture ;
- nombre d’arbres ;
- profondeur.

La recherche d’hyperparamètres constitue elle-même un problème d’optimisation.

# 73\. GRID SEARCH

On définit une grille :

\[ = H_1H_2H_k \]

Puis on évalue chaque combinaison.

Simple, mais coûteux lorsque le nombre de dimensions augmente.

# 74\. RANDOM SEARCH

On échantillonne aléatoirement des configurations.

Cela permet souvent d’explorer efficacement un espace d’hyperparamètres de grande dimension.

# 75\. OPTIMISATION BAYÉSIENNE DES HYPERPARAMÈTRES

On peut modéliser :

\[ h \]

et sélectionner progressivement les hyperparamètres les plus prometteurs.

Cela est particulièrement intéressant lorsque chaque entraînement coûte cher.

# 76\. OPTIMISATION ET REINFORCEMENT LEARNING

En reinforcement learning, l’agent cherche à maximiser une récompense cumulée :

\[ J() = \]

L’objectif devient :

\[ \]

Les méthodes de policy gradient transforment notamment ce problème en optimisation différentielle.

# 77\. OPTIMISATION ET ROBOTIQUE

Une trajectoire peut être représentée par :

\[ (t) \]

On peut minimiser :

\[ J() = J_{}

- J_{}
- J_{}
- J_{} \]

sous des contraintes :

- obstacles ;
- vitesse ;
- accélération ;
- articulation ;
- énergie.

On obtient :

\[ \]

# 78\. OPTIMISATION ET LOGISTIQUE

Exemple :

\[ (

- ) \]

sous :

- capacité des véhicules ;
- disponibilité ;
- demandes ;
- horaires ;
- contraintes géographiques.

Cela peut conduire à des problèmes LP, MILP, graphes ou combinatoires.

# 79\. OPTIMISATION ET SCHEDULING

Supposons :

\[ T_1,T_2,,T_n \]

à affecter à :

\[ M_1,M_2,,M_k \]

On peut chercher à minimiser :

\[ C_{} \]

où (C_{}) représente le temps de fin global.

Autres objectifs :

- temps d’attente ;
- retards ;
- énergie ;
- coûts ;
- équilibrage de charge.

# 80\. OPTIMISATION ET ALLOCATION DE RESSOURCES

On dispose d’une ressource limitée :

\[ R \]

et de plusieurs activités :

\[ A_1,,A_n \]

On cherche la répartition maximisant :

\[ U(x) \]

sous :

\[ \_i x_iR \]

C’est un schéma fondamental en :

- cloud computing ;
- systèmes distribués ;
- télécommunications ;
- finance ;
- production ;
- gestion énergétique.

# 81\. OPTIMISATION ET RÉSEAUX

Les réseaux peuvent être optimisés pour :

- débit ;
- latence ;
- coût ;
- fiabilité ;
- congestion ;
- énergie.

Exemples :

### Routage

\[ \_P (P) \]

### Allocation de bande passante

\[ \_x \_i U_i(x_i) \]

sous :

\[ \_i x_iC \]

où (C) représente une capacité réseau.

# 82\. OPTIMISATION ET FINANCE

Un portefeuille peut être représenté par :

\[ w=(w_1,,w_n) \]

On peut chercher à optimiser :

\[

- \]

sous :

\[ \_i w_i=1 \]

et éventuellement :

\[ w_i \]

L’optimisation permet donc de formaliser les compromis entre rendement, risque et contraintes.

# 83\. OPTIMISATION ET COMPUTER GRAPHICS

L’optimisation apparaît notamment dans :

- reconstruction de formes ;
- ajustement de paramètres ;
- animation ;
- simulation ;
- inverse rendering ;
- reconstruction 3D ;
- calibration de caméra ;
- estimation de pose ;
- déformation de maillages.

Exemple :

\[ ^\* = _ |R()-I|^2 \]

où (R()) représente un rendu et (I) une image cible.

# 84\. OPTIMISATION ET SIMULATION PHYSIQUE

On peut chercher une configuration minimisant une énergie :

\[ E(x) \]

Exemple conceptuel :

\[ x^\* = \_x E(x) \]

Cette idée intervient dans :

- systèmes physiques ;
- déformation ;
- géométrie ;
- animation ;
- simulation ;
- reconstruction.

# 85\. OPTIMISATION ET COMPUTER VISION

Exemples :

- calibration ;
- estimation de profondeur ;
- pose estimation ;
- optical flow ;
- reconstruction 3D ;
- bundle adjustment ;
- segmentation ;
- registration.

Une grande partie de ces problèmes peut être formulée sous forme :

\[ _ \_i L_i() \]

# 86\. OPTIMISATION ET TRAITEMENT DU SIGNAL

On cherche fréquemment à reconstruire un signal (x) à partir d’observations bruitées :

\[ y=Ax+ \]

Puis :

\[ x^\* = \_x |Ax-y|^2

- R(x) \]

Cette formulation apparaît notamment dans :

- débruitage ;
- reconstruction ;
- compression ;
- inverse problems ;
- signal processing.

# 87\. OPTIMISATION ET CYBERSÉCURITÉ

L’optimisation peut intervenir dans :

- allocation de ressources de défense ;
- détection d’anomalies ;
- classification ;
- sélection de caractéristiques ;
- analyse de réseaux ;
- réponse aux incidents ;
- optimisation de politiques de sécurité.

Elle peut également être utilisée pour modéliser des problèmes adversariaux.

# 88\. OPTIMISATION ADVERSARIALE

En machine learning, on peut chercher une perturbation :

\[ \]

maximisant la perte :

\[ \_{} L(x+,y) \]

sous :

\[ || \]

On obtient un problème d’optimisation sous contrainte.

Cela permet d’étudier notamment la robustesse des modèles.

# 89\. OPTIMISATION DISTRIBUÉE

Lorsque les données ou calculs sont répartis entre plusieurs machines :

\[ _x_ {i=1}^{N} f_i(x) \]

Chaque nœud possède :

\[ f_i(x) \]

et le système cherche à obtenir une solution commune.

Applications :

- federated learning ;
- systèmes distribués ;
- edge AI ;
- calcul scientifique.

# 90\. FEDERATED LEARNING ET OPTIMISATION

Chaque client possède des données locales.

On cherche :

\[ {k=1}^{K} p_k F_k() \]

où :

- (F_k) est la fonction de perte locale ;
- (p_k) représente le poids du client.

Cela introduit des problèmes supplémentaires :

- communication ;
- données non IID ;
- clients hétérogènes ;
- contraintes de calcul ;
- confidentialité.

# 91\. OPTIMISATION ONLINE

Les données arrivent progressivement.

Au lieu de disposer d’un dataset fixe :

\[ D \]

on reçoit :

\[ x_1,x_2,x_3, \]

L’algorithme doit mettre à jour sa solution continuellement.

Applications :

- recommandation ;
- trading ;
- réseaux ;
- systèmes temps réel ;
- apprentissage continu.

# 92\. OPTIMISATION SOUS CONTRAINTE TEMPORELLE

Dans un système temps réel, une solution mathématiquement optimale mais calculée trop tard peut être inutilisable.

Il faut donc parfois optimiser :

\[ \]

sous :

\[ T \]

Cela introduit un compromis entre :

\[ \]

# 93\. EXACTITUDE VS APPROXIMATION

Un algorithme peut chercher :

### Solution exacte

\[ x^\* \]

### Solution approximative

\[ x \]

avec une garantie :

\[ f(x) f(x^\*) \]

dans certains problèmes de minimisation.

Cette distinction est fondamentale lorsque l’optimum exact est trop coûteux à calculer.

# 94\. OPTIMISATION ET COMPLEXITÉ

Un problème peut être facile à formuler mais difficile à résoudre.

Il faut donc distinguer :

\[ \]

Certains problèmes combinatoires sont NP-difficiles.

Dans ces situations, on peut chercher :

- approximation ;
- heuristique ;
- métaheuristique ;
- relaxation ;
- programmation dynamique ;
- recherche paramétrée ;
- branch and bound.

# 95\. BRANCH AND BOUND

Branch and Bound divise l’espace des solutions :

\[ \_1,\_2, \]

et calcule des bornes permettant d’éliminer des sous-espaces qui ne peuvent pas produire une meilleure solution.

Schéma :

\[ \]

# 96\. RELAXATION

On peut simplifier un problème difficile en supprimant temporairement certaines contraintes.

Exemple :

\[ x_i{0,1} \]

devient :

\[ 0x_i \]

On obtient une relaxation continue.

Elle peut fournir :

- une borne ;
- une approximation ;
- une information utile pour branch and bound.

# 97\. OPTIMISATION ET STRUCTURES DE DONNÉES

L’optimisation n’est pas seulement mathématique.

La représentation des données influence directement les performances.

Exemples :

- heaps pour certaines recherches ;
- arbres ;
- graphes ;
- matrices creuses ;
- structures spatiales ;
- index ;
- tables de hachage ;
- structures de priorité.

Une bonne formulation peut être ruinée par une mauvaise structure de données.

# 98\. MATRICES CREUSES

Dans de grands problèmes, la matrice Hessienne ou la matrice des contraintes peut être creuse.

Au lieu de stocker :

\[ n^2 \]

éléments, on peut exploiter le fait que seuls certains éléments sont non nuls.

Cela permet de réduire :

- mémoire ;
- temps ;
- communication.

# 99\. STABILITÉ NUMÉRIQUE

Les algorithmes d’optimisation utilisent des calculs flottants.

Des problèmes peuvent apparaître à cause :

- du sous-débordement ;
- du surdébordement ;
- de mauvaises échelles ;
- de matrices mal conditionnées ;
- de gradients très petits ;
- de gradients très grands.

L’optimisation numérique doit donc être distinguée de l’optimisation purement théorique.

# 100\. CONDITIONNEMENT

Deux problèmes peuvent avoir des difficultés très différentes selon leur conditionnement.

Un problème mal conditionné peut être très sensible à de petites perturbations.

En ML, certaines géométries de fonctions de perte peuvent présenter :

- directions raides ;
- directions plates.

Cela explique notamment certaines oscillations de gradient descent.

# 101\. NORMALISATION ET OPTIMISATION

Le prétraitement des données peut modifier considérablement le paysage d’optimisation.

Si une caractéristique varie entre :

\[ 01 \]

et une autre entre :

\[ 010^6 \]

les dimensions n’ont pas la même échelle.

La standardisation peut améliorer la dynamique de certaines méthodes.

# 102\. INITIALISATION

Le point de départ :

\[ x_0 \]

peut influencer la trajectoire d’optimisation.

Dans les réseaux neuronaux, l’initialisation des poids peut influencer :

- propagation des activations ;
- propagation des gradients ;
- symétries ;
- vitesse d’apprentissage.

# 103\. CONVERGENCE

On dit qu’une méthode converge lorsqu’elle se rapproche d’une solution selon une définition appropriée.

Exemple :

\[ x_tx^\* \]

ou :

\[ f(x_t)f(x^\*) \]

Il faut distinguer :

- convergence de la suite des paramètres ;
- convergence de la fonction objectif ;
- convergence vers un optimum global ;
- convergence vers un point stationnaire.

# 104\. TAUX DE CONVERGENCE

On peut étudier la vitesse à laquelle :

\[ f(x_t)-f(x^\*) \]

diminue.

On distingue notamment :

- convergence linéaire ;
- superlinéaire ;
- quadratique.

Newton peut présenter une convergence quadratique locale sous des hypothèses appropriées.

# 105\. COMPLEXITÉ DES OPTIMISEURS

Le coût d’un optimiseur dépend notamment de :

\[

- \]

Pour les modèles modernes, le coût total est souvent dominé par l’évaluation répétée du modèle et des gradients.

# 106\. MÉTHODES DU PREMIER ORDRE VS SECOND ORDRE

### Premier ordre

Utilisent principalement :

\[ f \]

Exemples :

- gradient descent ;
- SGD ;
- Adam ;
- momentum.

### Second ordre

Utilisent :

\[ ^2f \]

ou une approximation.

Exemples :

- Newton ;
- BFGS ;
- L-BFGS.

# 107\. QUAND UTILISER QUOI ?

### Gradient descent / SGD

Approprié lorsque :

- dimension élevée ;
- gradients accessibles ;
- dataset important ;
- calcul distribué/GPU.

### Newton

Intéressant lorsque :

- dimension raisonnable ;
- Hessienne exploitable ;
- grande précision recherchée.

### L-BFGS

Intéressant lorsque :

- fonction différentiable ;
- dimension importante ;
- problème déterministe ou relativement stable.

### Programmation linéaire

Lorsque :

- objectif linéaire ;
- contraintes linéaires.

### Programmation entière

Lorsque :

- décisions discrètes.

### Programmation dynamique

Lorsque :

- sous-structure optimale ;
- états gérables ;
- sous-problèmes réutilisables.

### Métaheuristiques

Lorsque :

- paysage complexe ;
- gradients indisponibles ;
- recherche globale souhaitée ;
- solution exacte trop coûteuse.

# 108\. ERREURS CLASSIQUES EN OPTIMISATION

## Erreur 1 — Confondre minimum local et global

\[ f(x)=0 \]

ne garantit pas l’optimalité globale.

## Erreur 2 — Penser que plus d’itérations signifie toujours mieux

Une optimisation peut :

- surajuster ;
- diverger ;
- perdre du temps ;
- accumuler des erreurs numériques.

## Erreur 3 — Ignorer l’échelle

Des variables mal normalisées peuvent ralentir fortement certaines méthodes.

## Erreur 4 — Utiliser un learning rate arbitraire

Le learning rate influence directement la dynamique d’apprentissage.

## Erreur 5 — Ignorer les contraintes

Une solution mathématiquement excellente mais physiquement impossible n’est pas une solution utile.

## Erreur 6 — Confondre perte d’entraînement et performance réelle

\[ L_{} \]

n’implique pas nécessairement :

\[ L_{} \]

# 109\. OPTIMISATION COMME PROBLÈME D’INGÉNIERIE

Résoudre un problème d’optimisation ne signifie pas simplement choisir un algorithme.

Il faut suivre une chaîne :

\[ \]

C’est cette chaîne qui transforme les mathématiques en système exploitable.

# 110\. MODÉLISATION AVANT ALGORITHME

Une mauvaise modélisation ne devient pas correcte simplement parce qu’on utilise un algorithme sophistiqué.

Il faut d’abord déterminer :

1.  Que veut-on optimiser ?
2.  Quelles sont les variables ?
3.  Quelles sont les contraintes ?
4.  Quelles solutions sont admissibles ?
5.  La fonction est-elle différentiable ?
6.  Est-elle convexe ?
7.  Le problème est-il continu ou discret ?
8.  L’évaluation est-elle coûteuse ?
9.  Une solution exacte est-elle nécessaire ?
10. Quel compromis entre qualité et temps de calcul est acceptable ?

# 111\. TAXONOMIE GLOBALE DES PROBLÈMES

## Selon les variables

- continues ;
- discrètes ;
- entières ;
- binaires ;
- mixtes.

## Selon les contraintes

- sans contraintes ;
- égalités ;
- inégalités ;
- contraintes mixtes.

## Selon la fonction

- linéaire ;
- quadratique ;
- convexe ;
- non convexe ;
- différentiable ;
- non différentiable ;
- boîte noire.

## Selon l’information

- déterministe ;
- stochastique ;
- partiellement observée.

## Selon les objectifs

- mono-objectifs ;
- multi-objectifs.

# 112\. FORMES IMPORTANTES À RECONNAÎTRE

### Forme 1

\[ \_x f(x) \]

→ optimisation générale.

### Forme 2

\[ \_x c^Tx \]

sous :

\[ Axb \]

→ programmation linéaire.

### Forme 3

\[ \_x f(x) \]

sous :

\[ g(x)=0 \]

→ optimisation contrainte / Lagrangien.

### Forme 4

\[ \_x f(x)+R(x) \]

→ régularisation.

### Forme 5

\[ x_{t+1}=x_t-f(x_t) \]

→ gradient descent.

### Forme 6

\[ x_{t+1} = x_t-H^{-1}f \]

→ Newton.

### Forme 7

\[ \_x \[f(x,)\] \]

→ optimisation stochastique.

### Forme 8

\[ \_J() \]

→ optimisation de politique en reinforcement learning.

# 113\. ALGORITHMES À CONNAÎTRE

## Fondamentaux

- recherche locale ;
- gradient descent ;
- SGD ;
- momentum ;
- Adam ;
- Newton ;
- quasi-Newton ;
- BFGS ;
- L-BFGS.

## Optimisation sous contraintes

- multiplicateurs de Lagrange ;
- KKT ;
- méthodes de pénalité ;
- méthodes de barrière ;
- projected gradient ;
- méthodes de point intérieur.

## Optimisation combinatoire

- programmation dynamique ;
- branch and bound ;
- backtracking ;
- recherche locale ;
- approximation.

## Métaheuristiques

- recuit simulé ;
- génétiques ;
- recherche tabou ;
- essaim particulaire ;
- colonies de fourmis.

## Optimisation coûteuse

- optimisation bayésienne ;
- surrogate models.

# 114\. STRUCTURES MATHÉMATIQUES À MAÎTRISER

Pour être autonome dans ce domaine, il faut reconnaître :

\[ f \]

\[ ^2f \]

\[ J_f \]

\[ (x,) \]

\[ Axb \]

\[ x \]

\[ x{0,1} \]

\[ ||\_1 \]

\[ ||\_2 \]

\[ \]

\[ \]

\[ \[f(x,)\] \]

\[ (f_1,,f_k) \]

# 115\. RELATION AVEC LE DOMAINE I — CALCUL DIFFÉRENTIEL

La relation doit être parfaitement claire.

Le Domaine I répond notamment à :

Comment une fonction varie-t-elle ?

Le Domaine J demande :

Comment exploiter cette variation pour trouver une solution optimale ?

Ainsi :

\[ \]

Et :

\[ \]

# 116\. RELATION AVEC LE DOMAINE G — PROBABILITÉS

L’optimisation peut porter sur une espérance :

\[ \_x \[f(x,)\] \]

Les probabilités permettent alors de modéliser l’incertitude.

# 117\. RELATION AVEC LE DOMAINE H — STATISTIQUES

L’estimation statistique peut devenir :

\[ ^\* = _ L() \]

ou :

\[ ^\* = _ () \]

Le maximum de vraisemblance est donc naturellement relié à l’optimisation.

# 118\. RELATION AVEC LE DOMAINE F — COMBINATOIRE

Lorsque l’espace de solutions est discret :

\[ x \]

l’optimisation combinatoire devient centrale.

Exemples :

- sélection ;
- ordonnancement ;
- affectation ;
- voyageur de commerce.

# 119\. RELATION AVEC LE DOMAINE E — GRAPHES

De nombreux problèmes de graphes sont des problèmes d’optimisation :

- plus court chemin ;
- arbre couvrant minimal ;
- flot maximal ;
- matching ;
- routage ;
- coloration.

# 120\. RELATION AVEC LE DOMAINE C — ALGÈBRE LINÉAIRE

L’optimisation numérique utilise massivement :

- matrices ;
- vecteurs ;
- produits matriciels ;
- systèmes linéaires ;
- valeurs propres ;
- factorisations.

Newton, par exemple, nécessite de résoudre :

\[ H(x)p=-f(x) \]

plutôt que nécessairement de calculer explicitement (H^{-1}).

# 121\. RELATION AVEC LE DOMAINE D — GÉOMÉTRIE COMPUTATIONNELLE

L’optimisation géométrique apparaît dans :

- positionnement ;
- collision ;
- reconstruction ;
- trajectoire ;
- maillage ;
- rendu inverse ;
- computer vision.

# 122\. ARCHITECTURE LOGIQUE D’UN SYSTÈME D’OPTIMISATION

Un moteur générique peut être pensé ainsi :

Problem  
↓  
Variables  
↓  
Objective  
↓  
Constraints  
↓  
Model  
↓  
Optimizer  
↓  
Iteration  
↓  
Evaluation  
↓  
Stopping criterion  
↓  
Solution  
↓  
Validation

Dans un système réel, on peut ajouter :

Data  
↓  
Preprocessing  
↓  
Optimization Problem  
↓  
Solver  
↓  
Monitoring  
↓  
Validation  
↓  
Deployment

# 123\. SYSTÈME D’OPTIMISATION POUR LE MACHINE LEARNING

Architecture conceptuelle :

Dataset  
↓  
Model  
↓  
Prediction  
↓  
Loss  
↓  
Backpropagation  
↓  
Gradient  
↓  
Optimizer  
↓  
Parameter Update  
↓  
New Model  
↓  
Validation  
↓  
Repeat

Cette boucle est au cœur de l’entraînement des réseaux neuronaux.

# 124\. BOUCLE D’OPTIMISATION

Une implémentation abstraite peut être représentée :

initialiser x  
<br/>tant que non convergé :  
<br/>calculer f(x)  
<br/>calculer gradient  
<br/>déterminer direction  
<br/>déterminer taille du pas  
<br/>appliquer mise à jour  
<br/>vérifier contraintes  
<br/>évaluer convergence  
<br/>retourner x

Ce schéma est plus important à comprendre que la syntaxe particulière d’un framework.

# 125\. MÉTRIQUES DE DIAGNOSTIC

Lors d’une optimisation, il faut observer :

- valeur de la fonction objectif ;
- norme du gradient ;
- norme du déplacement ;
- nombre d’itérations ;
- temps ;
- contraintes violées ;
- convergence ;
- validation ;
- stabilité.

En ML :

- training loss ;
- validation loss ;
- métriques métier ;
- généralisation ;
- stabilité entre runs.

# 126\. EXPÉRIMENTATION D’OPTIMISATION

Une bonne expérimentation compare :

\[

- \]

et mesure :

\[

- \]

Il faut éviter de conclure sur une seule exécution lorsqu’un algorithme possède une composante stochastique importante.

# 127\. ROBUSTESSE DES SOLUTIONS

Une solution optimale peut être fragile.

Il faut parfois demander :

\[ f(x^\*) \]

mais aussi :

\[ f(x^\*+) \]

pour de petites perturbations ().

Une solution légèrement moins optimale mais beaucoup plus robuste peut être préférable dans un système réel.

# 128\. OPTIMISATION ET TRADE-OFFS

L’ingénierie implique souvent plusieurs critères.

Par exemple :

\[ \]

\[ \]

\[ \]

\[ \]

Comprendre l’optimisation signifie donc aussi comprendre les **compromis**.

# 129\. OPTIMISATION ET SYSTÈMES INTELLIGENTS

Un système intelligent peut être considéré comme un système qui cherche continuellement à améliorer une fonction objectif.

Exemples :

### Recommandation

Maximiser l’utilité attendue.

### Agent

Maximiser la récompense.

### Robot

Minimiser le coût d’une trajectoire.

### Modèle ML

Minimiser la perte.

### Planificateur

Minimiser le temps ou le coût.

### Réseau

Minimiser la latence ou maximiser le débit.

Ainsi :

\[ \]

Cette formule est volontairement conceptuelle, mais elle constitue une excellente grille de lecture.

# 130\. APPLICATIONS WEB

L’optimisation intervient notamment dans :

- recommandations ;
- recherche ;
- ranking ;
- personnalisation ;
- cache ;
- allocation de ressources ;
- optimisation de requêtes ;
- routage ;
- compression ;
- livraison de contenu ;
- A/B testing ;
- tuning de systèmes.

Même lorsqu’un système ne « ressemble » pas à un problème mathématique, ses décisions peuvent souvent être reformulées en problème d’optimisation.

# 131\. APPLICATIONS SOFTWARE ENGINEERING

On peut optimiser :

- temps d’exécution ;
- mémoire ;
- coût cloud ;
- latence ;
- consommation énergétique ;
- taille des bundles ;
- requêtes ;
- parallélisme ;
- allocation des ressources.

Exemple conceptuel :

\[ (

- ) \]

# 132\. APPLICATIONS CLOUD ET DISTRIBUTED SYSTEMS

Un orchestrateur peut chercher à répartir :

\[ N \]

tâches sur :

\[ M \]

machines.

Objectifs :

- minimiser temps ;
- équilibrer charge ;
- minimiser coût ;
- respecter capacité ;
- maximiser disponibilité.

Cela devient un problème d’optimisation combinatoire ou continue selon le modèle.

# 133\. APPLICATIONS IA AGENTIQUE

Dans un système agentique, l’optimisation peut apparaître à plusieurs niveaux :

### Planification

Choisir une séquence d’actions :

\[ a_1,a_2,,a_T \]

### Allocation

Choisir quel outil utiliser.

### Coût

Minimiser :

\[

- \]

### Qualité

Maximiser la qualité du résultat.

### Fiabilité

Pénaliser les erreurs.

On peut donc construire :

\[ J() = Q

- C
- T
- E \]

où :

- (Q) = qualité ;
- (C) = coût ;
- (T) = temps ;
- (E) = erreurs.

Cela transforme une stratégie agentique en problème d’optimisation multi-critères.

# 134\. APPLICATIONS À L’ORCHESTRATION D’AGENTS

Supposons plusieurs agents :

\[ A_1,A_2,,A_n \]

et plusieurs tâches.

Le système doit déterminer :

\[ \]

tout en minimisant :

- temps ;
- coût ;
- redondance ;

et maximisant :

- qualité ;
- fiabilité ;
- couverture.

On obtient un problème d’allocation et de scheduling.

# 135\. APPLICATIONS À STANE OS / PERSONAL AI

Dans un système personnel intelligent, on peut théoriquement optimiser :

\[ J =

- \]

Le système peut alors décider :

- quel modèle utiliser ;
- quel outil appeler ;
- quand rechercher ;
- quand utiliser un modèle local ;
- quand utiliser une API distante ;
- quelle mémoire récupérer ;
- quel niveau de raisonnement employer.

L’optimisation devient ainsi un principe d’architecture et pas seulement une technique mathématique.

# 136\. APPLICATIONS À LA RECHERCHE D’HYPERPARAMÈTRES

On peut définir :

\[ h^\* = _h L_{}(h) \]

où (h) représente les hyperparamètres.

Cela donne :

\[ \]

# 137\. APPLICATIONS À LA PLANIFICATION

Un plan est une séquence :

\[ P=(a_1,a_2,,a_n) \]

On peut définir :

\[ J(P) = (P) \]

et chercher :

\[ P^\* = \_P J(P) \]

C’est la base conceptuelle de nombreux systèmes de planification.

# 138\. APPLICATIONS À LA ROBOTIQUE

Chaîne :

\[ \]

Les contraintes géométriques du Domaine D et les graphes du Domaine E peuvent être combinés avec l’optimisation pour construire des planificateurs complexes.

# 139\. APPLICATIONS À LA LOGISTIQUE

Un système logistique peut optimiser simultanément :

\[

- \]

Cela produit souvent des problèmes multi-objectifs, combinatoires ou mixtes.

# 140\. APPLICATIONS AUX RÉSEAUX

On peut optimiser :

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

La théorie des graphes et l’optimisation se complètent alors directement.

# 141\. PROJETS D’APPRENTISSAGE — NIVEAU 1

## Projet 1 — Visualiseur de gradient descent

Construire une application affichant :

\[ f(x) \]

puis la trajectoire :

\[ x_0,x_1,x_2, \]

Comparer plusieurs learning rates.

Objectif :

comprendre visuellement la dynamique de l’optimisation.

## Projet 2 — Optimisation d’une fonction 2D

Créer :

\[ f(x,y) \]

et afficher :

- surface ;
- contours ;
- gradient ;
- trajectoire ;
- optimum.

# 142\. PROJETS — NIVEAU 2

## Projet 3 — Comparateur d’optimiseurs

Comparer :

- SGD ;
- Momentum ;
- Adam ;
- Newton ;
- L-BFGS.

Mesurer :

- nombre d’itérations ;
- temps ;
- valeur finale ;
- convergence.

## Projet 4 — Solveur de programmation linéaire

Créer une petite interface permettant de définir :

\[ c^Tx \]

sous :

\[ Axb \]

Puis visualiser la région admissible en 2D.

# 143\. PROJETS — NIVEAU 3

## Projet 5 — Optimiseur de scheduling

Entrées :

- tâches ;
- ressources ;
- durée ;
- contraintes.

Objectif :

minimiser le temps total.

Comparer :

- recherche exhaustive ;
- heuristique ;
- programmation dynamique ;
- méthode locale.

## Projet 6 — Routeur intelligent

Utiliser un graphe et une fonction coût :

\[ C(P) \]

Comparer :

- plus court chemin ;
- coût pondéré ;
- optimisation multi-critères.

# 144\. PROJETS — NIVEAU 4

## Projet 7 — Hyperparameter optimizer

Créer un système qui cherche automatiquement :

\[ learning rate \]

\[ batch size \]

\[ weight decay \]

\[ architecture \]

et mesure les performances.

Comparer :

- Grid Search ;
- Random Search ;
- optimisation bayésienne.

# 145\. PROJET AVANCÉ — OPTIMISATION D’AGENT

Créer un agent ayant plusieurs stratégies.

Pour chaque action :

\[ J(a) = Q(a)

- C(a)
- T(a) \]

L’agent choisit l’action maximisant (J).

Ce projet permet de réunir :

- optimisation ;
- IA ;
- agents ;
- statistiques ;
- probabilités ;
- systèmes ;
- ingénierie logicielle.

# 146\. EXERCICES DE RECONNAISSANCE

Pour chaque problème, identifier :

1.  variables ;
2.  objectif ;
3.  contraintes ;
4.  nature continue/discrète ;
5.  convexité éventuelle ;
6.  méthode adaptée ;
7.  critère d’arrêt ;
8.  métrique de validation.

# 147\. EXERCICES THÉORIQUES

### Exercice 1

Déterminer les points stationnaires de :

\[ f(x)=x^3-3x \]

Puis classifier les points avec la dérivée seconde.

### Exercice 2

Appliquer gradient descent à :

\[ f(x)=x^2 \]

avec :

\[ \]

et :

\[ x_0=10 \]

Calculer plusieurs itérations.

### Exercice 3

Résoudre avec Lagrange :

\[ \_{x,y}x<sup>2+y</sup>2 \]

sous :

\[ x+y=1 \]

### Exercice 4

Formuler un problème d’allocation comme un programme linéaire.

### Exercice 5

Formuler un problème de sélection comme un programme binaire.

# 148\. CHALLENGE SANS IA

Pour chaque problème d’optimisation :

1.  formuler manuellement ;
2.  identifier les variables ;
3.  écrire l’objectif ;
4.  écrire les contraintes ;
5.  déterminer la famille du problème ;
6.  choisir une méthode ;
7.  prévoir les difficultés ;
8.  seulement ensuite utiliser l’IA.

L’objectif est d’empêcher l’IA de remplacer la capacité de modélisation.

# 149\. CHALLENGE AVEC IA

Demander à une IA :

« Voici mon problème. Ne propose pas immédiatement un algorithme. Identifie d’abord les variables, l’objectif, les contraintes, la nature du problème, sa structure mathématique et les hypothèses nécessaires. »

Puis comparer :

\[ \]

L’objectif est d’apprendre à utiliser l’IA comme **assistant de modélisation**, et non comme générateur aveugle de solutions.

# 150\. FICHES DE DEEP DIVE

Le Domaine J peut être approfondi à travers les fiches suivantes :

### J01 — Minimum et maximum

### J02 — Optimum local/global

### J03 — Convexité

### J04 — Gradient descent

### J05 — SGD

### J06 — Momentum

### J07 — Adam

### J08 — Newton

### J09 — BFGS

### J10 — L-BFGS

### J11 — Optimisation du second ordre

### J12 — Multiplicateurs de Lagrange

### J13 — KKT

### J14 — Dualité

### J15 — Programmation linéaire

### J16 — Simplexe

### J17 — Point intérieur

### J18 — Programmation entière

### J19 — Programmation binaire

### J20 — MIP/MILP

### J21 — Programmation dynamique

### J22 — Branch and Bound

### J23 — Relaxation

### J24 — Recherche locale

### J25 — Recuit simulé

### J26 — Algorithmes génétiques

### J27 — Recherche tabou

### J28 — Métaheuristiques

### J29 — Optimisation globale

### J30 — Optimisation stochastique

### J31 — Optimisation robuste

### J32 — Optimisation multi-objectifs

### J33 — Pareto

### J34 — Optimisation bayésienne

### J35 — Hyperparameter optimization

### J36 — Optimisation distribuée

### J37 — Federated optimization

### J38 — Optimisation online

### J39 — Optimisation en reinforcement learning

### J40 — Optimisation des réseaux neuronaux

### J41 — Régularisation

### J42 — Paysages de perte

### J43 — Conditionnement

### J44 — Stabilité numérique

### J45 — Scheduling

### J46 — Allocation de ressources

### J47 — Routage

### J48 — Robotique

### J49 — Logistique

### J50 — Finance

### J51 — Computer graphics

### J52 — Computer vision

### J53 — Signal processing

### J54 — Optimisation des systèmes

### J55 — Optimisation agentique

### J56 — Optimisation des appels d’outils

### J57 — Optimisation coût/latence

### J58 — Optimisation sous incertitude

### J59 — Optimisation adversariale

### J60 — Modélisation complète d’un problème réel

# 151\. CE QU’IL FAUT ABSOLUMENT SAVOIR RECONNAÎTRE

Un niveau solide ne signifie pas mémoriser toutes les méthodes.

Il faut surtout savoir reconnaître :

### « Je vois une fonction à minimiser »

→ optimisation.

### « Je vois un gradient »

→ optimisation différentiable.

### « Je vois une Hessienne »

→ courbure / second ordre.

### « Je vois (Axb) et une fonction linéaire »

→ programmation linéaire.

### « Je vois (x_i{0,1}) »

→ programmation binaire.

### « Je vois (x_iZ) »

→ programmation entière.

### « Je vois une contrainte (g(x)=0) »

→ Lagrangien possible.

### « Je vois (g(x)) »

→ KKT / optimisation sous contraintes.

### « Je vois un espace discret gigantesque »

→ optimisation combinatoire.

### « Je vois des sous-problèmes réutilisables »

→ programmation dynamique possible.

### « Je vois une fonction non différentiable ou boîte noire »

→ méthodes sans gradient possibles.

### « Je vois plusieurs objectifs »

→ optimisation multi-objectifs / Pareto.

### « Je vois une fonction coûteuse à évaluer »

→ optimisation bayésienne potentiellement pertinente.

### « Je vois une loss de réseau neuronal »

→ optimisation des paramètres.

# 152\. CHECKLIST DE MAÎTRISE

Avant de considérer le Domaine J comme acquis, il faut pouvoir expliquer :

- ce qu’est une fonction objectif ;
- ce qu’est une variable de décision ;
- ce qu’est une contrainte ;
- différence entre minimum local et global ;
- notion de convexité ;
- gradient ;
- Hessienne ;
- gradient descent ;
- learning rate ;
- SGD ;
- momentum ;
- Adam ;
- Newton ;
- quasi-Newton ;
- BFGS ;
- L-BFGS ;
- multiplicateurs de Lagrange ;
- KKT ;
- dualité ;
- programmation linéaire ;
- programmation entière ;
- programmation binaire ;
- programmation dynamique ;
- branch and bound ;
- relaxation ;
- recherche locale ;
- recuit simulé ;
- algorithmes génétiques ;
- optimisation stochastique ;
- optimisation robuste ;
- optimisation multi-objectifs ;
- Pareto ;
- optimisation bayésienne ;
- hyperparameter optimization ;
- optimisation distribuée ;
- relation entre optimisation et ML.

# 153\. CHECKLIST D’INGÉNIERIE

Face à un problème réel, être capable de répondre :

### Modèle

- Quelles sont mes variables ?
- Quelle est ma fonction objectif ?
- Quelles sont mes contraintes ?

### Mathématiques

- Le problème est-il continu ?
- Différentiable ?
- Convexe ?
- Linéaire ?
- Discret ?
- Stochastique ?

### Algorithme

- Gradient ?
- Newton ?
- LP ?
- MILP ?
- DP ?
- Heuristique ?
- Métaheuristique ?
- Optimisation bayésienne ?

### Système

- Combien de données ?
- Quel coût par évaluation ?
- Quelle mémoire ?
- Quelle latence ?
- Quelle précision ?

### Validation

- Comment savoir que la solution est bonne ?
- Quelle est la métrique ?
- Quelle est la robustesse ?
- Quel est le coût de la solution ?
- Existe-t-il une solution de référence ?

# 154\. SYNTHÈSE CONCEPTUELLE

Le Domaine J peut être résumé par la chaîne :

\[ \]

Pour le machine learning :

\[ \]

Pour un système :

\[ \]

# 155\. LA GRANDE CARTE DES DOMAINES

La progression construite jusqu’ici peut être comprise comme :

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

La transition :

\[ IJ \]

est particulièrement importante.

Le calcul différentiel fournit les outils permettant de comprendre :

\[ \]

L’optimisation transforme ces informations en :

\[ \]

Et le machine learning assemble ensuite :

\[ \]

pour produire des systèmes capables d’apprendre.

# 156\. FORMULE MENTALE FINALE

Lorsqu’un problème informatique semble complexe, apprendre à poser les questions suivantes :

**Qu’est-ce que je cherche à améliorer ?**

\[ \]

**Qu’est-ce que je peux modifier ?**

\[ \]

**Qu’est-ce que je n’ai pas le droit de violer ?**

\[ \]

**Comment mesurer une amélioration ?**

\[ \]

**Puis-je exploiter les dérivées ?**

\[ \]

**Le problème est-il convexe ?**

\[ \]

**Les solutions sont-elles discrètes ?**

\[ \]

**L’évaluation est-elle coûteuse ?**

\[ \]

**Ai-je plusieurs objectifs ?**

\[ \]

**Ai-je besoin d’une solution exacte ?**

\[ \]

Cette manière de penser est probablement plus importante que la mémorisation isolée des algorithmes.

# 157\. CRITÈRE FINAL DE MAÎTRISE

Le Domaine J est suffisamment maîtrisé lorsque, face à un nouveau problème informatique, l’on peut spontanément effectuer la transformation :

\[ \]

puis :

\[ \]

puis :

\[ \]

et enfin :

\[ \]

C’est cette capacité de **modélisation, sélection de méthode et raisonnement sur les compromis** qui transforme la connaissance de l’optimisation en véritable compétence d’ingénierie.

# 158\. SYNTHÈSE FINALE

L’optimisation est le domaine qui transforme une question générale :

« Que pourrais-je faire ? »

en une question mathématiquement exploitable :

« Parmi toutes les solutions admissibles, laquelle optimise mon objectif selon mes contraintes ? »

Elle constitue un pont direct entre les mathématiques et la construction de systèmes.

En machine learning :

\[ \]

En robotique :

\[ \]

En logistique :

\[ \]

En réseaux :

\[ \]

En systèmes intelligents :

\[ \]

Et dans l’ingénierie logicielle :

\[ \]

Le Domaine I explique **comment une fonction change**.

Le Domaine J explique **comment exploiter cette information pour rechercher une solution**.

Ensemble :

\[ \]

constitue l’une des chaînes mathématiques fondamentales de l’intelligence artificielle moderne.

**Domaine J — Optimisation : maîtrise fondamentale pour comprendre non seulement comment entraîner un modèle, mais comment formaliser et résoudre des problèmes de décision, de recherche, de planification et d’allocation dans des systèmes informatiques réels.**

## FIN DU DOCUMENT J

**Domaine suivant : Domaine K — à déterminer selon la cartographie mathématique globale du projet.**