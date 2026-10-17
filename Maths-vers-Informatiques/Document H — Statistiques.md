# DOCUMENT H — STATISTIQUES

## Cartographie complète pour les mathématiques appliquées, la data science, l’analytics, l’expérimentation, le machine learning et l’IA

# 0\. IDENTITÉ ET MISSION DU DOMAINE

## 0.1 Nom

**Domaine H — Statistiques**

## 0.2 Mission

Les statistiques constituent l’ensemble des méthodes mathématiques permettant de :

- collecter des données ;
- organiser des observations ;
- résumer un jeu de données ;
- visualiser des distributions ;
- mesurer la dispersion ;
- détecter des structures ;
- estimer des paramètres inconnus ;
- quantifier l’incertitude ;
- comparer des populations ou des groupes ;
- tester des hypothèses ;
- étudier des relations entre variables ;
- construire des modèles ;
- effectuer des prédictions ;
- évaluer des modèles ;
- prendre des décisions à partir de données.

Si les probabilités du Domaine G partent généralement d’un **modèle aléatoire pour déduire ce qui peut être observé**, les statistiques partent principalement de **données observées pour apprendre quelque chose sur le phénomène qui les a produites**.

# 1\. PLACE DU DOMAINE H DANS LA CARTE MATHÉMATIQUE

Le Domaine H dépend fortement des domaines précédents.

## Domaine A — Logique et fondements

Apporte :

- raisonnement ;
- ensembles ;
- propositions ;
- quantificateurs ;
- formalisation.

## Domaine B — Théorie des nombres

Intervient indirectement dans :

- génération pseudo-aléatoire ;
- cryptographie ;
- algorithmes numériques.

## Domaine C — Algèbre linéaire

Devient central pour :

- régression linéaire ;
- covariance ;
- matrices de données ;
- PCA ;
- moindres carrés ;
- machine learning.

## Domaine D — Géométrie computationnelle

Intervient notamment dans :

- visualisation spatiale ;
- données multidimensionnelles ;
- clustering ;
- analyse géométrique des données.

## Domaine E — Graphes

Intervient dans :

- réseaux de données ;
- graphes statistiques ;
- réseaux bayésiens ;
- modèles relationnels.

## Domaine F — Combinatoire

Fournit notamment :

- dénombrement ;
- échantillonnage ;
- espaces de configurations ;
- probabilités discrètes.

## Domaine G — Probabilités

C’est le fondement immédiat du Domaine H :

\[ \]

Les probabilités permettent de modéliser l’incertitude.

Les statistiques permettent d’exploiter les observations pour apprendre sur cette incertitude.

# 2\. STATISTIQUES DESCRIPTIVES ET INFÉRENTIELLES

Le domaine possède deux grandes familles.

## 2.1 Statistiques descriptives

Elles cherchent à répondre :

Que contiennent les données ?

Exemples :

- moyenne ;
- médiane ;
- mode ;
- variance ;
- écart-type ;
- quantiles ;
- histogrammes ;
- corrélations.

## 2.2 Statistiques inférentielles

Elles cherchent à répondre :

Que peut-on déduire d’une population à partir d’un échantillon ?

Exemples :

- estimation ;
- intervalles de confiance ;
- tests d’hypothèse ;
- p-values ;
- modèles statistiques.

# 3\. CARTOGRAPHIE GLOBALE DU DOMAINE H

Le domaine peut être organisé en grandes familles.

### H1 — Données et observations

- population ;
- échantillon ;
- variable ;
- observation ;
- dataset ;
- données quantitatives ;
- données qualitatives.

### H2 — Statistiques descriptives

- moyenne ;
- médiane ;
- mode ;
- quantiles ;
- variance ;
- écart-type ;
- covariance ;
- corrélation.

### H3 — Visualisation statistique

- histogramme ;
- boxplot ;
- scatterplot ;
- barplot ;
- densité ;
- séries temporelles.

### H4 — Échantillonnage

- échantillonnage aléatoire ;
- stratification ;
- biais ;
- représentativité ;
- taille d’échantillon.

### H5 — Estimation

- estimateur ;
- biais ;
- variance ;
- consistance ;
- efficacité ;
- maximum de vraisemblance ;
- MAP.

### H6 — Intervalles

- intervalle de confiance ;
- marge d’erreur ;
- précision ;
- couverture.

### H7 — Tests

- hypothèse nulle ;
- hypothèse alternative ;
- statistique de test ;
- p-value ;
- seuil ;
- puissance ;
- erreurs de type I et II.

### H8 — Relations entre variables

- covariance ;
- corrélation ;
- régression ;
- dépendance ;
- résidus.

### H9 — Modèles statistiques

- régression linéaire ;
- régression multiple ;
- régression polynomiale ;
- régression logistique ;
- modèles généralisés.

### H10 — Expérimentation

- A/B testing ;
- randomisation ;
- contrôle ;
- traitement ;
- effet ;
- causalité.

### H11 — Machine learning

- prédiction ;
- validation ;
- métriques ;
- généralisation ;
- biais-variance ;
- calibration.

### H12 — Analytics

- KPI ;
- tendances ;
- anomalies ;
- segmentation ;
- cohortes ;
- forecasting.

# 4\. VOCABULAIRE FONDAMENTAL

## 4.1 Population

Ensemble complet des individus ou objets étudiés.

Exemple :

Tous les utilisateurs d’une application.

## 4.2 Échantillon

Sous-ensemble observé de la population.

Exemple :

10 000 utilisateurs sélectionnés pour une étude.

## 4.3 Observation

Une unité de données.

## 4.4 Variable

Une caractéristique mesurée.

Exemples :

- âge ;
- revenu ;
- temps de réponse ;
- nombre de clics ;
- classe ;
- température.

# 5\. TYPES DE VARIABLES

## 5.1 Qualitative nominale

Catégories sans ordre naturel.

Exemples :

- pays ;
- navigateur ;
- couleur.

## 5.2 Qualitative ordinale

Catégories possédant un ordre.

Exemples :

- faible ;
- moyen ;
- élevé.

## 5.3 Quantitative discrète

Valeurs généralement entières.

Exemples :

- nombre de clics ;
- nombre de bugs ;
- nombre de commandes.

## 5.4 Quantitative continue

Valeurs pouvant appartenir à un intervalle continu.

Exemples :

- temps ;
- distance ;
- poids ;
- température.

# 6\. MOYENNE ARITHMÉTIQUE

Pour :

\[ x_1,,x_n \]

la moyenne est :

\[ x = 1n \_{i=1}^{n}x_i \]

Elle représente le centre arithmétique des observations.

# 7\. MOYENNE PONDÉRÉE

Lorsque les observations possèdent des poids :

\[ x_w = {\_iw_i} \]

Applications :

- notes ;
- KPI ;
- agrégation ;
- sondages ;
- pondération d’échantillons.

# 8\. MÉDIANE

La médiane est la valeur qui sépare les observations ordonnées en deux groupes de taille comparable.

Elle est particulièrement utile lorsque les données contiennent des valeurs extrêmes.

Exemple :

\[ 1,2,3,4,100 \]

Moyenne :

\[ 22 \]

Médiane :

\[ 3 \]

La différence illustre la sensibilité de la moyenne aux valeurs extrêmes.

# 9\. MODE

Le mode est la valeur ou catégorie la plus fréquente.

Il est particulièrement utile pour :

- données catégorielles ;
- fréquences ;
- valeurs discrètes.

# 10\. MOYENNE, MÉDIANE ET MODE

Ces trois mesures décrivent le centre des données, mais ne sont pas interchangeables.

### Moyenne

Sensible aux valeurs extrêmes.

### Médiane

Plus robuste aux valeurs extrêmes.

### Mode

Mesure la fréquence maximale.

# 11\. QUANTILES

Les quantiles divisent les données ordonnées en proportions.

### Quartiles

\[ Q_1, Q_2, Q_3 \]

avec :

\[ Q_2= \]

# 12\. ÉCART INTERQUARTILE

\[ IQR=Q_3-Q_1 \]

L’IQR mesure la dispersion de la moitié centrale des observations.

Il est relativement robuste aux valeurs extrêmes.

# 13\. PERCENTILES

Le percentile (p) indique une valeur sous laquelle se situe approximativement une proportion (p) des observations.

Exemple :

le 95e percentile de latence permet d’étudier la valeur en dessous de laquelle se trouvent environ 95 % des observations.

Applications :

- performance Web ;
- monitoring ;
- SLA ;
- analytics ;
- systèmes distribués.

# 14\. VARIANCE

Pour une population :

\[ ^2 = 1N \_{i=1}<sup>{N}(x_i-)</sup>2 \]

Pour un échantillon, l’estimateur classique de la variance utilise :

\[ s^2 = \_{i=1}^{n}(x_i-x)^2 \]

La différence entre (N) et (n-1) est fondamentale.

genui{“learning_viz”:{“type_id”:“VARIANCE”,“locale_override”:“fr-FR”}}

# 15\. POURQUOI (n-1) ?

Lorsqu’on estime la variance de la population à partir de la moyenne calculée sur l’échantillon, une correction de degrés de liberté est nécessaire.

Cette correction est associée à l’estimateur sans biais classique de la variance.

# 16\. ÉCART-TYPE

\[ s= \]

L’écart-type possède les mêmes unités que la variable étudiée.

genui{“learning_viz”:{“type_id”:“STANDARD_DEVIATION”,“initial_values”:{“sigma”:1.5},“locale_override”:“fr-FR”}}

Il est généralement plus interprétable que la variance.

# 17\. DISPERSION ROBUSTE

D’autres mesures peuvent être utilisées :

- IQR ;
- MAD ;
- écart absolu moyen ;
- quantiles.

La mesure adaptée dépend de la distribution et de la présence éventuelle d’outliers.

# 18\. COEFFICIENT DE VARIATION

Lorsque la moyenne est positive et que la comparaison est pertinente :

\[ CV= \]

Il permet de comparer des dispersions relatives entre variables ayant des échelles différentes.

# 19\. ASYMÉTRIE

Une distribution peut être :

- symétrique ;
- asymétrique à droite ;
- asymétrique à gauche.

L’asymétrie influence notamment :

- moyenne ;
- médiane ;
- choix des transformations ;
- choix des modèles.

# 20\. OUTLIERS

Un outlier est une observation particulièrement éloignée du reste des données selon un critère donné.

Une règle classique basée sur l’IQR utilise :

\[ x<Q_1-1.5IQR \]

ou :

\[ x>Q_3+1.5IQR \]

Attention :

un outlier n’est pas automatiquement une erreur.

Il peut représenter :

- une erreur de mesure ;
- un événement rare réel ;
- une population différente ;
- une fraude ;
- une anomalie système.

# 21\. DISTRIBUTION DES DONNÉES

Une distribution décrit comment les observations sont réparties.

On peut l’étudier avec :

- histogramme ;
- densité ;
- quantiles ;
- boxplot ;
- statistiques résumées.

# 22\. HISTOGRAMME

Un histogramme regroupe les observations dans des intervalles.

Il permet d’observer :

- concentration ;
- dispersion ;
- asymétrie ;
- multimodalité ;
- valeurs extrêmes.

Le choix des classes influence fortement la lecture.

# 23\. BOXPLOT

Le boxplot représente notamment :

- médiane ;
- quartiles ;
- IQR ;
- observations extrêmes selon la convention choisie.

Il est très utile pour comparer rapidement plusieurs groupes.

# 24\. SCATTERPLOT

Le nuage de points représente deux variables quantitatives.

Il permet d’observer :

- relation ;
- tendance ;
- dispersion ;
- clusters ;
- valeurs atypiques.

# 25\. COVARIANCE STATISTIQUE

Pour deux variables (X,Y) :

\[ Cov(X,Y) = E\[(X-E\[X\])(Y-E\[Y\])\] \]

Estimateur empirique :

\[ s_{XY} = \_i (x_i-x)(y_i-y) \]

# 26\. CORRÉLATION DE PEARSON

\[ r = {s_Xs_Y} \]

avec :

\[ -1r \]

Interprétation générale :

- proche de (1) : relation linéaire positive ;
- proche de (-1) : relation linéaire négative ;
- proche de (0) : faible relation linéaire.

genui{“learning_viz”:{“type_id”:“CORRELATION”,“initial_values”:{“pattern”:“positive”},“locale_override”:“fr-FR”}}

# 27\. CORRÉLATION ≠ CAUSALITÉ

Une corrélation peut provenir :

- d’une causalité ;
- d’une causalité inverse ;
- d’une variable confondante ;
- d’une relation indirecte ;
- d’un hasard ;
- d’un biais de sélection.

Donc :

\[ corr(X,Y) \]

# 28\. CORRÉLATION DE SPEARMAN

Spearman mesure une association monotone à partir des rangs.

Elle est utile lorsque :

- la relation n’est pas nécessairement linéaire ;
- les variables sont ordinales ;
- la robustesse aux distributions est recherchée.

# 29\. RÉGRESSION

La régression cherche à modéliser une variable cible en fonction d’une ou plusieurs variables explicatives.

Forme générale :

\[ Y=f(X)+ \]

où :

- (Y) = variable cible ;
- (X) = variables explicatives ;
- (f) = fonction ;
- () = bruit ou erreur.

# 30\. RÉGRESSION LINÉAIRE SIMPLE

Le modèle :

\[ Y=\_0+\_1X+ \]

L’estimation donne :

\[ Y=b_0+b_1X \]

genui{“learning_viz”:{“type_id”:“LEAST_SQUARE_REGRESSION”,“locale_override”:“fr-FR”}}

# 31\. INTERPRÉTATION DES COEFFICIENTS

\[ \_0 \]

est l’intercept.

\[ \_1 \]

représente la variation moyenne attendue de (Y) associée à une variation d’une unité de (X), dans le cadre du modèle.

Cette interprétation dépend du modèle et des hypothèses.

# 32\. MOINDRES CARRÉS

On choisit les coefficients minimisant :

\[ \_i (y_i-y_i)^2 \]

Les termes :

\[ e_i=y_i-y_i \]

sont les résidus.

# 33\. FORME MATRICIELLE

Pour une régression linéaire :

\[ y=X+ \]

L’estimateur des moindres carrés, lorsque les conditions permettent l’inversion, est :

\[ = (X<sup>TX)</sup>{-1}X^Ty \]

En pratique, des méthodes numériques comme QR ou SVD sont souvent préférables à l’inversion explicite.

Cela crée une connexion directe avec le Domaine C.

# 34\. RÉGRESSION LINÉAIRE MULTIPLE

\[ Y = \_0

- \_1X_1 ++ \_pX_p + \]

Elle permet d’intégrer plusieurs variables explicatives.

# 35\. RÉGRESSION POLYNOMIALE

On peut utiliser :

\[ Y= \_0+\_1X+\_2X<sup>2++\_kX</sup>k+ \]

Même si le modèle est non linéaire en (X), il reste linéaire par rapport aux paramètres (\_i).

# 36\. RÉGRESSION LOGISTIQUE

Elle est principalement utilisée pour la classification binaire.

On modélise :

\[ P(Y=1X) \]

avec une fonction logistique :

\[ P(Y=1X) = (\_0+^TX) \]

où :

\[ (z)= \]

Elle constitue un pont majeur entre statistiques et machine learning.

# 37\. RÉSULTATS D’UNE RÉGRESSION

On peut analyser :

- coefficients ;
- erreurs standards ;
- intervalles de confiance ;
- p-values ;
- résidus ;
- (R^2) ;
- (R^2) ajusté ;
- diagnostics.

# 38\. COEFFICIENT DE DÉTERMINATION

\[ R^2 = 1- \]

Il mesure une certaine proportion de la variabilité expliquée par le modèle dans le cadre de la régression considérée.

Attention :

un (R^2) élevé ne prouve pas qu’un modèle est causal, correct ou utile en prédiction hors échantillon.

# 39\. RÉSIDUS

\[ e_i=y_i-y_i \]

L’analyse des résidus permet de rechercher :

- non-linéarité ;
- hétéroscédasticité ;
- valeurs atypiques ;
- structure non modélisée ;
- violations d’hypothèses.

# 40\. HYPOTHÈSES CLASSIQUES DE LA RÉGRESSION LINÉAIRE

Selon le cadre d’inférence, on peut rencontrer des hypothèses concernant :

- linéarité ;
- indépendance ;
- espérance conditionnelle nulle ;
- variance constante ;
- normalité des erreurs pour certaines procédures exactes en petit échantillon.

Ces hypothèses doivent être distinguées de ce qui est nécessaire uniquement pour certaines propriétés particulières des estimateurs.

# 41\. ÉCHANTILLONNAGE

L’échantillonnage consiste à sélectionner une partie de la population.

Objectif :

\[ \]

# 42\. ÉCHANTILLONNAGE ALÉATOIRE SIMPLE

Chaque unité possède une probabilité connue et contrôlée d’être sélectionnée, idéalement égale selon le schéma considéré.

# 43\. ÉCHANTILLONNAGE STRATIFIÉ

La population est divisée en strates puis échantillonnée à l’intérieur de celles-ci.

Applications :

- sondages ;
- analytics ;
- études de populations hétérogènes.

# 44\. ÉCHANTILLONNAGE SYSTÉMATIQUE

On sélectionne des unités selon une règle régulière après un point de départ défini.

# 45\. ÉCHANTILLONNAGE PAR GRAPPES

On sélectionne des groupes entiers ou des grappes.

Il peut être utile lorsque l’échantillonnage individuel est coûteux.

# 46\. BIAIS D’ÉCHANTILLONNAGE

Un biais apparaît lorsque le mécanisme de sélection favorise systématiquement certaines observations.

Exemples :

- biais de sélection ;
- biais de non-réponse ;
- biais de survivant ;
- biais de couverture.

# 47\. REPRÉSENTATIVITÉ

Un échantillon représentatif n’est pas simplement un échantillon « qui ressemble visuellement » à la population.

La représentativité dépend :

- de la population cible ;
- du mécanisme d’échantillonnage ;
- des variables étudiées ;
- du biais ;
- de la non-réponse ;
- de la structure des données.

# 48\. TAILLE D’ÉCHANTILLON

Une taille d’échantillon plus grande réduit généralement l’incertitude d’échantillonnage, toutes choses égales par ailleurs.

Mais elle ne corrige pas automatiquement :

- un biais systématique ;
- une mauvaise mesure ;
- une mauvaise définition de population ;
- une mauvaise expérimentation.

# 49\. ESTIMATEUR

Un estimateur est une fonction des données utilisée pour estimer un paramètre inconnu.

Paramètre :

\[ \]

Estimateur :

\[ \]

# 50\. BIAIS D’UN ESTIMATEUR

\[ Bias() = E\[\]- \]

Un estimateur est sans biais si :

\[ E\[\]= \]

# 51\. VARIANCE D’UN ESTIMATEUR

\[ Var() \]

mesure sa variabilité d’un échantillon à l’autre.

Deux estimateurs peuvent avoir :

- même biais ;
- mais des variances différentes.

# 52\. ERREUR QUADRATIQUE MOYENNE

La MSE est :

\[ MSE() = E\[(-)^2\] \]

Elle se décompose en :

\[ MSE = Bias^2+Variance \]

Cette décomposition est fondamentale pour comprendre le compromis biais-variance.

# 53\. CONSISTANCE

Un estimateur est consistant lorsqu’il se rapproche de la vraie valeur lorsque :

\[ n \]

sous les conditions appropriées.

# 54\. EFFICACITÉ

L’efficacité compare la précision de différents estimateurs, souvent à travers leur variance dans une classe d’estimateurs donnée.

# 55\. MAXIMUM DE VRAISEMBLANCE

Pour des observations (x_1,,x_n) et un paramètre () :

\[ L() = P(X_1=x_1,,X_n=x_n) \]

dans le cas discret, ou la densité jointe dans le cas continu.

L’estimateur du maximum de vraisemblance est :

\[ _{MLE} =_ L() \]

# 56\. LOG-VRAISEMBLANCE

On travaille souvent avec :

\[ ()=L() \]

car :

\[ \_iL_i = \_iL_i \]

Cela simplifie les calculs et améliore souvent la stabilité numérique.

# 57\. MAXIMUM A POSTERIORI

Dans une approche bayésienne :

\[ _{MAP} =_ P(D) \]

et :

\[ P(D) P(D)P() \]

Ainsi :

\[ MAP = Likelihood+Prior \]

dans l’espace logarithmique, à une constante près.

# 58\. INTERVALLE DE CONFIANCE

Un intervalle de confiance fournit une procédure statistique destinée à produire des intervalles ayant une couverture donnée dans le cadre fréquentiste considéré.

Forme conceptuelle :

\[ \]

# 59\. MARGE D’ERREUR

Dans de nombreux cas approximatifs :

\[ Marge z_{/2} SE \]

où (SE) représente l’erreur standard.

# 60\. ERREUR STANDARD

L’erreur standard mesure la variabilité d’un estimateur d’un échantillon à l’autre.

Pour la moyenne dans un cadre classique :

\[ SE(X) = \]

# 61\. INTERVALLE DE CONFIANCE POUR UNE MOYENNE

Sous les hypothèses appropriées, lorsque la variance est inconnue :

\[ x t_{/2,n-1} \]

Le choix de la loi dépend des hypothèses et du contexte.

# 62\. TEST D’HYPOTHÈSE

Un test statistique compare les données à une hypothèse de référence.

On définit :

### (H_0)

Hypothèse nulle.

### (H_1)

Hypothèse alternative.

# 63\. STATISTIQUE DE TEST

On construit une quantité :

\[ T(X) \]

dont la distribution sous (H_0) est connue ou approximable.

On compare ensuite la valeur observée à cette distribution.

# 64\. P-VALUE

La p-value mesure, sous (H_0), à quel point les données observées sont extrêmes selon la statistique de test et l’alternative considérée.

Elle ne signifie pas :

\[ P(H_0données) \]

C’est une distinction fondamentale.

# 65\. SEUIL DE SIGNIFICATION

On fixe généralement :

\[ \]

par exemple :

\[ \]

Puis on définit une règle de décision.

Attention :

\[ \]

ne signifie pas automatiquement :

\[ P(H_0)=0.95 \]

# 66\. ERREUR DE TYPE I

Rejeter (H_0) alors qu’elle est vraie.

Probabilité contrôlée, dans le cadre du test, par :

\[ \]

# 67\. ERREUR DE TYPE II

Ne pas rejeter (H_0) alors que l’alternative considérée est vraie.

Probabilité :

\[ \]

# 68\. PUISSANCE STATISTIQUE

\[ Power=1- \]

La puissance représente la capacité d’un test à détecter un effet donné lorsqu’il existe réellement, selon les hypothèses et paramètres du test.

# 69\. TAILLE D’EFFET

Un résultat statistiquement significatif n’est pas nécessairement important en pratique.

Il faut distinguer :

- existence d’une différence ;
- taille de la différence ;
- incertitude ;
- importance pratique.

Exemples de tailles d’effet :

- différence de moyennes ;
- différence de proportions ;
- odds ratio ;
- Cohen’s (d).

# 70\. TESTS PARAMÉTRIQUES ET NON PARAMÉTRIQUES

## Paramétriques

Reposent sur certaines hypothèses concernant la distribution ou les paramètres.

Exemples :

- test t ;
- ANOVA ;
- tests liés à la régression.

## Non paramétriques

Reposent sur des hypothèses différentes ou plus faibles.

Exemples :

- Mann-Whitney ;
- Wilcoxon ;
- Kruskal-Wallis ;
- Spearman.

# 71\. TEST T

Utilisé dans différents contextes pour comparer des moyennes.

Variantes :

- un échantillon ;
- deux échantillons indépendants ;
- échantillons appariés.

# 72\. ANOVA

L’analyse de variance permet notamment de comparer plusieurs moyennes.

Elle décompose la variabilité en différentes composantes.

Idée centrale :

\[ Variabilité totale = Variabilité entre groupes

- Variabilité intra groupes \]

# 73\. TEST DU KHI-DEUX

Utilisé notamment pour :

- indépendance entre variables catégorielles ;
- adéquation ;
- analyse de tableaux de contingence.

# 74\. TESTS MULTIPLES

Si l’on réalise beaucoup de tests, la probabilité d’obtenir au moins un résultat significatif par hasard augmente.

Il faut donc considérer des corrections ou contrôles comme :

- Bonferroni ;
- Holm ;
- contrôle du FDR.

# 75\. FDR

Le False Discovery Rate vise à contrôler une proportion attendue de faux positifs parmi les résultats déclarés significatifs.

Il est particulièrement pertinent lorsque l’on effectue de nombreux tests.

# 76\. A/B TESTING

Un A/B test compare généralement deux variantes :

- A = contrôle ;
- B = traitement.

Exemple :

\[ conversion_A \]

contre :

\[ conversion_B \]

# 77\. RANDOMISATION

La randomisation consiste à attribuer les participants ou observations aux groupes selon un mécanisme aléatoire.

Elle permet notamment de réduire certaines sources de confusion et constitue un élément fondamental des essais contrôlés.

# 78\. EXPÉRIMENTATION

Une expérimentation bien conçue cherche à contrôler :

- population ;
- intervention ;
- groupe de contrôle ;
- randomisation ;
- métrique ;
- durée ;
- taille d’échantillon ;
- critères d’analyse.

# 79\. CAUSALITÉ

Les statistiques descriptives montrent des associations.

Les expériences randomisées peuvent fournir une base beaucoup plus solide pour l’inférence causale.

Il faut distinguer :

\[ P(YX) \]

de questions causales telles que :

\[ P(Ydo(X=x)) \]

dans les cadres causaux appropriés.

# 80\. DATA SCIENCE

La statistique constitue une partie centrale de la data science.

Pipeline conceptuel :

\[ Données Nettoyage Exploration Modélisation Validation Interprétation \]

À chaque étape interviennent des concepts statistiques.

# 81\. EXPLORATORY DATA ANALYSIS

L’EDA consiste à explorer les données avant de construire un modèle final.

On cherche notamment :

- distributions ;
- corrélations ;
- valeurs manquantes ;
- outliers ;
- tendances ;
- relations ;
- groupes ;
- anomalies.

# 82\. DATA QUALITY ET STATISTIQUES

Il faut examiner :

- taux de valeurs manquantes ;
- doublons ;
- distributions ;
- incohérences ;
- valeurs extrêmes ;
- changements de distribution.

Une statistique calculée sur des données défectueuses peut être parfaitement exacte mathématiquement mais complètement trompeuse.

# 83\. STATISTIQUES ET MACHINE LEARNING

Le ML utilise constamment :

- moyenne ;
- variance ;
- covariance ;
- distributions ;
- vraisemblance ;
- optimisation ;
- validation ;
- métriques ;
- estimation.

# 84\. TRAIN / VALIDATION / TEST

Un dataset peut être séparé en :

- entraînement ;
- validation ;
- test.

Objectif :

évaluer la capacité de généralisation plutôt que simplement mesurer l’ajustement sur les données d’entraînement.

# 85\. SURAPPRENTISSAGE

Le surapprentissage apparaît lorsque le modèle s’adapte trop fortement aux données d’entraînement.

On observe typiquement :

\[ Erreur_{train} Erreur_{test} \]

# 86\. SOUS-APPRENTISSAGE

Le modèle est trop simple pour capturer suffisamment la structure des données.

# 87\. BIAIS-VARIANCE EN MACHINE LEARNING

Un modèle peut être :

- trop rigide → biais élevé ;
- trop flexible → variance élevée.

L’objectif est de trouver un compromis adapté au problème et aux données.

# 88\. VALIDATION CROISÉE

La validation croisée permet d’évaluer un modèle sur plusieurs partitions des données.

Exemple :

### k-fold

Les données sont divisées en (k) groupes.

Chaque groupe sert successivement de validation.

On obtient plusieurs estimations de performance.

# 89\. BOOTSTRAP

Le bootstrap consiste à créer de nombreux échantillons rééchantillonnés avec remise à partir des données observées.

Il permet d’approcher :

- distribution d’un estimateur ;
- incertitude ;
- intervalle ;
- biais ;
- variance.

# 90\. JACKKNIFE

Le jackknife construit des estimations en retirant successivement certaines observations ou groupes d’observations.

Applications :

- biais ;
- variance ;
- diagnostics.

# 91\. PRÉDICTION

Une prédiction statistique cherche à estimer une variable future ou inconnue.

On distingue :

- estimation d’un paramètre ;
- prédiction d’une observation ;
- intervalle de confiance ;
- intervalle de prédiction.

# 92\. INTERVALLE DE PRÉDICTION

Un intervalle de prédiction prend généralement en compte :

- incertitude sur le modèle ;
- variabilité individuelle future.

Il est donc généralement plus large qu’un intervalle de confiance concernant uniquement une moyenne ou un paramètre.

# 93\. SÉRIES TEMPORELLES

Les données temporelles introduisent des dépendances entre observations.

Concepts à reconnaître :

- tendance ;
- saisonnalité ;
- autocorrélation ;
- stationnarité ;
- bruit ;
- lissage ;
- prévision.

# 94\. AUTOCORRÉLATION

L’autocorrélation mesure la relation entre une série et des versions retardées d’elle-même.

Elle est importante pour :

- monitoring ;
- finance ;
- IoT ;
- systèmes ;
- forecasting.

# 95\. DÉTECTION D’ANOMALIES

Les statistiques peuvent identifier des observations inhabituelles à l’aide de :

- z-score ;
- IQR ;
- distance robuste ;
- modèles probabilistes ;
- résidus ;
- seuils adaptatifs.

# 96\. Z-SCORE

Pour une observation (x) :

\[ z= \]

Il mesure la distance à la moyenne en nombre d’écarts-types.

# 97\. NORMALISATION ET STANDARDISATION

Standardiser :

\[ z_i= \]

Cela produit une variable centrée et réduite selon l’estimation utilisée.

Applications :

- ML ;
- comparaison de variables ;
- optimisation ;
- analyse exploratoire.

# 98\. STATISTIQUES ROBUSTES

Lorsque les données contiennent des valeurs extrêmes ou des distributions non idéales, on peut préférer :

- médiane ;
- IQR ;
- MAD ;
- estimateurs robustes ;
- régression robuste.

# 99\. DONNÉES MANQUANTES

Les données manquantes peuvent provenir de :

- absence de réponse ;
- panne ;
- collecte incomplète ;
- filtrage ;
- événement non observé.

Il faut distinguer :

- MCAR ;
- MAR ;
- MNAR.

Le mécanisme de manque peut influencer fortement l’analyse.

# 100\. SIMPSON’S PARADOX

Une relation observée globalement peut s’inverser lorsque les données sont séparées par une variable de stratification.

Cela montre l’importance :

- des variables confondantes ;
- de la stratification ;
- de l’analyse conditionnelle.

# 101\. MULTICOLINÉARITÉ

Dans une régression multiple, les variables explicatives peuvent être fortement corrélées.

Conséquences possibles :

- coefficients instables ;
- erreurs standards élevées ;
- interprétation difficile.

# 102\. HÉTÉROSCÉDASTICITÉ

La variance des erreurs peut dépendre du niveau des prédictions ou des variables explicatives.

Cela peut affecter certaines procédures d’inférence.

# 103\. SÉLECTION DE VARIABLES

Méthodes possibles :

- sélection basée sur des critères statistiques ;
- régularisation ;
- méthodes de recherche ;
- connaissances du domaine.

Il faut éviter la sélection naïve sur le même jeu de données utilisé pour une inférence finale sans tenir compte du processus de sélection.

# 104\. RÉGULARISATION

La régularisation ajoute une pénalisation à l’objectif.

### Ridge

\[ _ \]

### Lasso

\[ _ \]

Cela crée un pont entre :

- statistiques ;
- algèbre linéaire ;
- optimisation ;
- machine learning.

# 105\. MÉTRIQUES DE RÉGRESSION

À connaître :

### MAE

\[ MAE = 1n_i|y_i-y_i| \]

### MSE

\[ MSE = 1n_i(y_i-y_i)^2 \]

### RMSE

\[ RMSE= \]

### (R^2)

Mesure liée à la variabilité expliquée dans le cadre du modèle.

# 106\. MÉTRIQUES DE CLASSIFICATION

À connaître :

- accuracy ;
- precision ;
- recall ;
- specificity ;
- F1-score ;
- ROC-AUC ;
- PR-AUC.

Matrice de confusion :

|     | Réel positif | Réel négatif |
| --- | --- | --- |
| Prédit positif | TP  | FP  |
| Prédit négatif | FN  | TN  |

genui{“learning_viz”:{“type_id”:“CLASSIFICATION_THRESHOLD”,“initial_values”:{“threshold”:0.5},“locale_override”:“fr-FR”}}

# 107\. ACCURACY

\[ Accuracy= {TP+TN+FP+FN} \]

Elle peut être trompeuse en présence de classes très déséquilibrées.

# 108\. PRECISION

\[ Precision= \]

Elle répond approximativement à :

Parmi les prédictions positives, quelle proportion est correcte ?

# 109\. RECALL

\[ Recall= \]

Il répond approximativement à :

Parmi les vrais positifs, quelle proportion a été détectée ?

# 110\. F1-SCORE

\[ F_1= 2 {Precision+Recall} \]

# 111\. THRESHOLD ET CLASSIFICATION

Un modèle peut produire :

\[ P(Y=1X) \]

Un seuil transforme cette probabilité en décision.

Changer le seuil modifie :

- TP ;
- FP ;
- TN ;
- FN ;
- precision ;
- recall.

Il faut donc distinguer :

\[ \]

et :

\[ \]

# 112\. CALIBRATION

Un modèle probabiliste est calibré si, approximativement, parmi les prédictions auxquelles il attribue une probabilité (p), la fréquence empirique de l’événement est proche de (p).

Exemple :

parmi les prédictions à 0,8, environ 80 % devraient être positives dans un modèle bien calibré, dans le cadre d’une évaluation appropriée.

# 113\. ANALYTICS

Les statistiques sont fondamentales pour :

- DAU ;
- MAU ;
- conversion ;
- rétention ;
- churn ;
- panier moyen ;
- temps de session ;
- latence ;
- taux d’erreur ;
- cohortes.

# 114\. COHORTES

Une cohorte regroupe des individus partageant une caractéristique temporelle ou contextuelle.

Exemples :

- utilisateurs inscrits en janvier ;
- clients acquis via une campagne ;
- utilisateurs ayant réalisé une première action donnée.

On peut ensuite comparer leur comportement dans le temps.

# 115\. KPI ET DISTRIBUTIONS

Un KPI ne doit pas toujours être résumé par une moyenne.

Selon le contexte, il peut être pertinent d’étudier :

- médiane ;
- percentiles ;
- distribution ;
- variance ;
- segments ;
- évolution temporelle.

# 116\. A/B TESTING ET MÉTRIQUES

Pour une expérience :

\[ Ap_A \]

\[ Bp_B \]

On peut étudier :

\[ =p_B-p_A \]

ou une mesure relative.

Mais il faut aussi considérer :

- intervalle ;
- incertitude ;
- taille d’effet ;
- puissance ;
- multiplicité ;
- durée ;
- biais.

# 117\. P-HACKING

Le p-hacking désigne diverses pratiques qui exploitent ou multiplient les analyses jusqu’à obtenir artificiellement un résultat statistiquement significatif.

Exemples :

- multiplier les tests sans correction ;
- arrêter une expérience lorsque le résultat devient significatif ;
- sélectionner a posteriori les métriques favorables.

# 118\. HARKING

HARKing signifie formuler une hypothèse après avoir observé les résultats tout en la présentant comme une hypothèse formulée avant l’analyse.

Cela peut conduire à une interprétation trompeuse des résultats.

# 119\. REPRODUCTIBILITÉ

Une analyse statistique sérieuse doit idéalement permettre de reproduire :

- les données utilisées ;
- les transformations ;
- les paramètres ;
- les méthodes ;
- les métriques ;
- les tests ;
- les visualisations.

# 120\. SIGNIFICATIVITÉ STATISTIQUE VS IMPORTANCE PRATIQUE

Une différence peut être :

- statistiquement significative ;
- mais pratiquement négligeable.

Inversement, un effet potentiellement important peut ne pas être détecté avec un échantillon trop petit.

Il faut donc examiner ensemble :

\[ \]

# 121\. INTERVALLE DE CONFIANCE VS INTERVALLE DE PRÉDICTION

### Intervalle de confiance

Concerne généralement l’incertitude sur un paramètre ou une quantité moyenne.

### Intervalle de prédiction

Concerne l’incertitude sur une future observation individuelle.

La seconde inclut généralement davantage de variabilité.

# 122\. STATISTIQUES ET PROBABILITÉS

Le lien fondamental est :

\[ \]

alors que :

\[ \]

Cette distinction doit être profondément maîtrisée.

# 123\. MÉTHODE GÉNÉRALE D’ANALYSE STATISTIQUE

## Étape 1 — Définir la question

Que cherche-t-on à savoir ?

## Étape 2 — Définir la population

Sur qui ou quoi veut-on conclure ?

## Étape 3 — Examiner les données

- type ;
- taille ;
- qualité ;
- valeurs manquantes.

## Étape 4 — Décrire

- moyenne ;
- médiane ;
- variance ;
- quantiles ;
- distributions.

## Étape 5 — Visualiser

- histogramme ;
- boxplot ;
- scatterplot ;
- séries temporelles.

## Étape 6 — Explorer les relations

- corrélation ;
- groupes ;
- tendances.

## Étape 7 — Formuler les hypothèses

Que suppose-t-on ?

## Étape 8 — Choisir la méthode

- estimation ;
- test ;
- régression ;
- modèle probabiliste.

## Étape 9 — Quantifier l’incertitude

- erreur standard ;
- intervalle ;
- bootstrap ;
- distribution d’échantillonnage.

## Étape 10 — Vérifier les hypothèses

Le modèle est-il approprié ?

## Étape 11 — Interpréter

Quelle conclusion est réellement soutenue ?

## Étape 12 — Vérifier la robustesse

La conclusion dépend-elle fortement :

- d’une observation ;
- d’un choix de modèle ;
- d’une hypothèse ;
- d’une transformation ?

# 124\. ALGORITHMES ET TECHNIQUES À MAÎTRISER

## Statistiques descriptives

- moyenne ;
- médiane ;
- variance ;
- quantiles ;
- covariance ;
- corrélation.

## Inférence

- estimation ;
- maximum de vraisemblance ;
- MAP ;
- intervalles ;
- tests.

## Régression

- moindres carrés ;
- régression linéaire ;
- régression logistique.

## Rééchantillonnage

- bootstrap ;
- jackknife ;
- cross-validation.

## Expérimentation

- randomisation ;
- A/B testing ;
- tests statistiques.

## Data science

- EDA ;
- détection d’outliers ;
- traitement des données manquantes ;
- évaluation.

# 125\. STRUCTURES MATHÉMATIQUES ASSOCIÉES

Les statistiques utilisent :

- vecteurs ;
- matrices ;
- distributions ;
- tableaux de contingence ;
- tenseurs ;
- séries temporelles ;
- échantillons ;
- graphes ;
- fonctions de vraisemblance.

# 126\. COMPLEXITÉ COMPUTATIONNELLE

Les opérations statistiques peuvent aller de :

\[ O(n) \]

pour une moyenne ou une variance simple, jusqu’à des coûts beaucoup plus élevés pour :

- régression ;
- inversion ou factorisation matricielle ;
- bootstrap ;
- validation croisée ;
- recherche de modèles ;
- hyperparameter search.

Si l’on effectue :

\[ B \]

rééchantillonnages sur :

\[ n \]

observations, le coût peut être approximativement :

\[ O(Bn) \]

pour une statistique simple.

# 127\. STATISTIQUES À GRANDE ÉCHELLE

Avec des millions ou milliards d’observations, il faut considérer :

- mémoire ;
- streaming ;
- calcul distribué ;
- approximation ;
- agrégation ;
- échantillonnage.

Certaines statistiques peuvent être calculées en ligne sans stocker toutes les observations.

# 128\. STATISTIQUES EN STREAMING

On peut mettre à jour certaines quantités au fur et à mesure de l’arrivée des données.

Exemples :

- moyenne en ligne ;
- variance en ligne ;
- compteurs ;
- quantiles approximatifs.

Applications :

- monitoring ;
- IoT ;
- logs ;
- systèmes distribués.

# 129\. DRIFT STATISTIQUE

Une distribution de données peut évoluer avec le temps.

On peut observer :

\[ P_t(X)P_{t+}(X) \]

Ce phénomène peut dégrader les performances d’un modèle.

Applications :

- ML en production ;
- monitoring ;
- fraude ;
- recommandation ;
- détection de changements.

# 130\. CONCEPT DRIFT

Dans un système prédictif :

\[ P(YX) \]

peut évoluer.

Il faut alors distinguer :

- changement de distribution des entrées ;
- changement de relation entrée-sortie ;
- changement de fréquence des classes.

# 131\. STATISTIQUES ET DÉTECTION DE CHANGEMENT

On peut utiliser :

- tests statistiques ;
- fenêtres glissantes ;
- comparaison de distributions ;
- scores d’écart ;
- méthodes séquentielles.

# 132\. STATISTIQUES ROBUSTES ET IA

Les données réelles contiennent souvent :

- bruit ;
- outliers ;
- labels incorrects ;
- distributions déséquilibrées ;
- valeurs manquantes.

La statistique robuste permet de construire des méthodes moins sensibles à certains de ces problèmes.

# 133\. PROJETS PRATIQUES PROGRESSIFS

## Projet 1 — Analyse descriptive d’un dataset

Calculer :

- moyenne ;
- médiane ;
- mode ;
- variance ;
- écart-type ;
- quartiles ;
- IQR.

## Projet 2 — Dashboard statistique

Construire un dashboard présentant :

- distributions ;
- KPI ;
- percentiles ;
- anomalies ;
- tendances.

## Projet 3 — Analyse de corrélation

Étudier un dataset multidimensionnel et construire une matrice de corrélation.

## Projet 4 — Régression linéaire

Prédire une variable quantitative.

Analyser :

- coefficients ;
- résidus ;
- (R^2) ;
- erreur.

## Projet 5 — Régression logistique

Construire un classifieur binaire et analyser :

- probabilités ;
- seuil ;
- precision ;
- recall ;
- F1.

## Projet 6 — A/B testing

Simuler une expérimentation avec :

- contrôle ;
- traitement ;
- métrique ;
- taille d’échantillon ;
- test ;
- intervalle.

## Projet 7 — Bootstrap

Estimer l’incertitude d’une métrique sans utiliser directement une formule paramétrique.

## Projet 8 — Détection d’anomalies

Comparer :

- z-score ;
- IQR ;
- méthode robuste.

## Projet 9 — Analyse de série temporelle

Analyser :

- tendance ;
- saisonnalité ;
- autocorrélation ;
- anomalies.

## Projet 10 — Monitoring ML

Construire un système détectant :

- drift ;
- baisse de performance ;
- changement de distribution.

# 134\. EXERCICES DE MAÎTRISE

## Niveau 1

Calculer :

- moyenne ;
- médiane ;
- variance ;
- écart-type.

## Niveau 2

Interpréter :

- corrélation ;
- quantiles ;
- outliers.

## Niveau 3

Construire une régression.

## Niveau 4

Interpréter des coefficients.

## Niveau 5

Construire un intervalle de confiance.

## Niveau 6

Réaliser un test d’hypothèse.

## Niveau 7

Analyser un A/B test.

## Niveau 8

Comparer plusieurs modèles statistiques.

## Niveau 9

Construire une analyse reproductible complète.

# 135\. DÉFIS SANS IA

### Défi 1

Calculer moyenne, médiane et variance à la main.

### Défi 2

Expliquer pourquoi moyenne et médiane peuvent diverger fortement.

### Défi 3

Démontrer la décomposition :

\[ MSE=Bias^2+Variance \]

### Défi 4

Dériver les moindres carrés.

### Défi 5

Expliquer ce qu’est réellement une p-value.

### Défi 6

Construire un intervalle de confiance.

### Défi 7

Analyser un A/B test sans outil automatique.

### Défi 8

Identifier un biais d’échantillonnage dans un scénario réel.

### Défi 9

Expliquer pourquoi corrélation ne signifie pas causalité.

# 136\. DÉFIS AVEC IA

Utiliser l’IA comme :

- générateur de datasets ;
- professeur ;
- critique méthodologique ;
- générateur d’hypothèses ;
- vérificateur de calcul ;
- assistant de visualisation.

Mais ne pas déléguer :

- la définition de la question ;
- le choix de la population ;
- l’interprétation finale ;
- l’évaluation des hypothèses.

# 137\. CATALOGUE DES FICHES INDIVIDUELLES

### H01

Population, échantillon et variables.

### H02

Types de variables.

### H03

Moyenne.

### H04

Médiane.

### H05

Mode.

### H06

Quantiles et percentiles.

### H07

Variance.

### H08

Écart-type.

### H09

IQR et statistiques robustes.

### H10

Distributions.

### H11

Covariance.

### H12

Corrélation de Pearson.

### H13

Corrélation de Spearman.

### H14

Outliers.

### H15

Échantillonnage.

### H16

Biais d’échantillonnage.

### H17

Estimateurs.

### H18

Biais d’un estimateur.

### H19

Variance d’un estimateur.

### H20

MSE.

### H21

Consistance.

### H22

Maximum de vraisemblance.

### H23

MAP.

### H24

Intervalles de confiance.

### H25

Erreur standard.

### H26

Tests d’hypothèse.

### H27

p-value.

### H28

Erreurs de type I et II.

### H29

Puissance statistique.

### H30

Taille d’effet.

### H31

Tests t.

### H32

ANOVA.

### H33

Khi-deux.

### H34

Tests non paramétriques.

### H35

Tests multiples.

### H36

FDR.

### H37

Régression linéaire.

### H38

Régression multiple.

### H39

Moindres carrés.

### H40

Régression logistique.

### H41

Résidus.

### H42

(R^2).

### H43

Bootstrap.

### H44

Jackknife.

### H45

Validation croisée.

### H46

A/B testing.

### H47

Randomisation.

### H48

Causalité.

### H49

Analyse exploratoire.

### H50

Séries temporelles.

### H51

Autocorrélation.

### H52

Détection d’anomalies.

### H53

Statistiques robustes.

### H54

Données manquantes.

### H55

Drift statistique.

### H56

Concept drift.

### H57

Évaluation ML.

### H58

Calibration.

### H59

Métriques de classification.

### H60

Métriques de régression.

# 138\. CONNEXIONS AVEC LES DOMAINES PRÉCÉDENTS

## F → H

La combinatoire permet de comprendre :

- espaces d’échantillonnage ;
- configurations ;
- dénombrement.

## G → H

C’est la connexion la plus importante :

\[ \]

Les probabilités modélisent les données possibles.

Les statistiques utilisent les données observées pour inférer les paramètres ou propriétés du modèle.

## C → H

L’algèbre linéaire fournit :

- matrices ;
- vecteurs ;
- projections ;
- SVD ;
- systèmes linéaires.

Elle est indispensable pour la régression et de nombreux modèles statistiques.

## E → H

Les graphes permettent :

- réseaux ;
- dépendances ;
- structures relationnelles ;
- modèles graphiques.

# 139\. CARTE CONCEPTUELLE G → H

La relation fondamentale est :

\[ \]

et :

\[ \]

On obtient :

\[ \]

puis :

\[ \]

puis :

\[ \]

et :

\[ \]

# 140\. CRITÈRE DE MAÎTRISE

La maîtrise du Domaine H ne signifie pas savoir appliquer mécaniquement une fonction statistique.

Elle signifie être capable de :

1.  identifier la population ;
2.  identifier l’échantillon ;
3.  identifier les variables ;
4.  comprendre le mécanisme d’échantillonnage ;
5.  décrire correctement les données ;
6.  choisir une mesure de tendance centrale ;
7.  choisir une mesure de dispersion ;
8.  détecter des valeurs atypiques ;
9.  mesurer des associations ;
10. distinguer corrélation et causalité ;
11. construire un estimateur ;
12. comprendre biais et variance ;
13. construire ou interpréter un intervalle ;
14. formuler un test ;
15. interpréter correctement une p-value ;
16. comprendre les erreurs statistiques ;
17. analyser la puissance ;
18. construire une régression ;
19. diagnostiquer un modèle ;
20. concevoir une expérimentation ;
21. analyser un A/B test ;
22. évaluer un modèle prédictif ;
23. comprendre le bootstrap ;
24. détecter un drift ;
25. communiquer une conclusion sans dépasser ce que les données permettent d’affirmer.

# 141\. CHECKLIST FINALE

## Données

- Population
- Échantillon
- Observation
- Variable
- Types de variables

## Description

- Moyenne
- Médiane
- Mode
- Quantiles
- Percentiles
- Variance
- Écart-type
- IQR
- MAD
- Distribution
- Outliers

## Relations

- Covariance
- Pearson
- Spearman
- Corrélation ≠ causalité

## Échantillonnage

- Aléatoire simple
- Stratifié
- Systématique
- Grappes
- Biais
- Représentativité
- Taille d’échantillon

## Estimation

- Estimateur
- Biais
- Variance
- MSE
- Consistance
- Efficacité
- MLE
- MAP

## Inférence

- Intervalle de confiance
- Erreur standard
- Hypothèse nulle
- Hypothèse alternative
- Statistique de test
- p-value
- Type I
- Type II
- Puissance
- Taille d’effet

## Tests

- Test t
- ANOVA
- Khi-deux
- Tests non paramétriques
- Tests multiples
- FDR

## Régression

- Régression linéaire
- Régression multiple
- Moindres carrés
- Régression logistique
- Résidus
- (R^2)
- Multicolinéarité
- Hétéroscédasticité

## Expérimentation

- Randomisation
- Contrôle
- Traitement
- A/B testing
- Causalité
- Puissance

## ML

- Train/validation/test
- Cross-validation
- Biais-variance
- Calibration
- Classification
- Régression
- Métriques
- Généralisation

## Production

- Monitoring
- Drift
- Concept drift
- Anomalies
- Statistiques en streaming

# 142\. SYNTHÈSE ULTIME

Le Domaine H peut être résumé par une chaîne fondamentale :

\[ \]

Les statistiques permettent donc de transformer :

\[ \]

en :

\[ \]

puis en :

\[ \]

puis en :

\[ \]

# 143\. POSITION DU DOMAINE H DANS LA CARTOGRAPHIE GLOBALE

La progression construite jusqu’ici peut maintenant être résumée ainsi :

\[ A: \]

\[ B: \]

\[ C: \]

\[ D: \]

\[ E: \]

\[ F: \]

\[ G: \]

\[ H: \]

Le Domaine H constitue ainsi le pont entre les mathématiques probabilistes et la pratique moderne de la **data science, de l’analytics, de l’expérimentation et du machine learning**.

# CONCLUSION DU DOMAINE H

La statistique ne consiste pas simplement à calculer une moyenne ou une variance.

Elle fournit une méthodologie complète permettant de passer :

\[ \]

Elle permet notamment de répondre à des questions telles que :

- Que montrent réellement les données ?
- Quelle est la variabilité du phénomène ?
- Notre échantillon est-il pertinent ?
- Quelle valeur peut-on attribuer à un paramètre inconnu ?
- Quelle incertitude accompagne cette estimation ?
- Une différence observée est-elle compatible avec le hasard ?
- Quelle relation existe entre deux variables ?
- Peut-on prédire une nouvelle observation ?
- Une expérience fournit-elle suffisamment d’évidence ?
- Un modèle généralise-t-il ?
- Les données d’aujourd’hui ressemblent-elles encore à celles utilisées pour construire le modèle ?

La grande idée du Domaine H est donc :

\[ \]

Et sa relation avec le Domaine G peut être retenue sous la forme :

\[ \]

\[ \]

Le Domaine H constitue ainsi l’une des bases mathématiques directes de la **data science, de l’analytics, de l’expérimentation, du machine learning et de l’IA appliquée aux données**.

**Domaine suivant : Domaine I — à déterminer selon la cartographie mathématique globale du projet.**