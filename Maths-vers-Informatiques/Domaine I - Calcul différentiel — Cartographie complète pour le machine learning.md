# DOCUMENT I — CALCUL DIFFÉRENTIEL

## Cartographie complète pour le machine learning, l’optimisation, les réseaux neuronaux, la simulation et la computer graphics

# 0 — IDENTITÉ DU DOMAINE

## 0.1 — Nom

**Domaine I — Calcul différentiel**

## 0.2 — Définition générale

Le calcul différentiel étudie la manière dont une quantité varie lorsqu’une autre quantité varie.

Il cherche notamment à répondre à des questions comme :

- à quelle vitesse une fonction change-t-elle ?
- dans quelle direction change-t-elle le plus rapidement ?
- comment une petite modification de l’entrée affecte-t-elle la sortie ?
- comment plusieurs variables interagissent-elles ?
- où une fonction atteint-elle un minimum ou un maximum ?
- comment optimiser une fonction ?
- comment propager l’effet d’une modification à travers une succession de fonctions ?

La notion centrale est celle de **dérivée**.

Pour une fonction d’une variable :

\[ f : \]

la dérivée (f’(x)) mesure le taux de variation local de (f).

Dans plusieurs variables, cette idée devient :

- dérivées partielles ;
- gradient ;
- dérivées directionnelles ;
- Jacobienne ;
- Hessienne ;
- différentielle totale ;
- règle de chaîne multivariable.

# 1 — PLACE DU CALCUL DIFFÉRENTIEL DANS LA CARTOGRAPHIE MATHÉMATIQUE

Le calcul différentiel se situe à l’intersection de plusieurs domaines.

Algèbre  
↓  
Fonctions  
↓  
Limites  
↓  
Calcul différentiel  
↓  
Optimisation  
↓  
Calcul numérique  
↓  
Machine Learning

Mais il possède également des connexions fortes avec :

Calcul différentiel  
├── Algèbre linéaire  
├── Probabilités  
├── Statistiques  
├── Géométrie  
├── Optimisation  
├── Analyse numérique  
├── Équations différentielles  
└── Machine Learning

Une compréhension sérieuse du Machine Learning nécessite donc de comprendre au minimum :

\[ \]

# 2 — LA GRANDE CARTOGRAPHIE DU DOMAINE

Le domaine peut être organisé en plusieurs grandes familles.

### A. Fondements

- fonctions ;
- limites ;
- continuité ;
- voisinage ;
- variation locale.

### B. Calcul différentiel à une variable

- dérivée ;
- dérivées usuelles ;
- règles de dérivation ;
- dérivation composée ;
- dérivation implicite ;
- extrema.

### C. Calcul différentiel multivariable

- dérivées partielles ;
- gradient ;
- dérivées directionnelles ;
- différentiabilité ;
- Jacobienne ;
- Hessienne.

### D. Approximation locale

- développement de Taylor ;
- approximation linéaire ;
- approximation quadratique ;
- erreurs locales.

### E. Optimisation

- extrema ;
- points critiques ;
- convexité ;
- contraintes ;
- multiplicateurs de Lagrange ;
- optimisation numérique.

### F. Calcul différentiel matriciel

- vecteurs ;
- matrices ;
- Jacobiennes ;
- gradients ;
- Hessiennes ;
- notation différentielle.

### G. Optimisation numérique

- gradient descent ;
- momentum ;
- Newton ;
- quasi-Newton ;
- méthodes du second ordre ;
- learning rate.

### H. Machine Learning

- fonction de perte ;
- gradient de la loss ;
- backpropagation ;
- chain rule ;
- optimisation des paramètres ;
- entraînement des réseaux neuronaux.

### I. Deep Learning

- couches ;
- activations ;
- gradients ;
- vanishing gradients ;
- exploding gradients ;
- autograd ;
- différentiation automatique.

### J. Simulation et physique

- vitesse ;
- accélération ;
- équations différentielles ;
- intégration temporelle ;
- dynamique.

### K. Computer Graphics

- transformations ;
- normales ;
- éclairage ;
- optimisation géométrique ;
- animation ;
- différentiation de rendu.

# 3 — VOCABULAIRE FONDAMENTAL

Avant toute formule, il faut maîtriser les termes suivants.

| Concept | Signification |
| --- | --- |
| Fonction | Association entre des entrées et des sorties |
| Variable | Quantité susceptible de varier |
| Domaine | Ensemble des entrées autorisées |
| Image | Valeur produite par la fonction |
| Limite | Comportement local d’une fonction |
| Continuité | Absence de rupture locale |
| Dérivée | Taux de variation local |
| Différentielle | Approximation linéaire locale |
| Gradient | Direction de variation maximale |
| Jacobienne | Matrice des dérivées premières |
| Hessienne | Matrice des dérivées secondes |
| Point critique | Point où le gradient s’annule ou n’existe pas |
| Minimum local | Valeur inférieure dans un voisinage |
| Maximum local | Valeur supérieure dans un voisinage |
| Convexité | Structure permettant notamment de raisonner sur les minima |
| Fonction de perte | Fonction mesurant l’erreur d’un modèle |
| Paramètre | Variable apprise par un modèle |
| Optimisation | Recherche de paramètres minimisant ou maximisant une fonction |

# 4 — FONCTIONS

Une fonction associe une entrée à une sortie.

\[ f : XY \]

Exemple :

\[ f(x)=x^2 \]

À chaque (x), on associe :

\[ f(x)=x^2 \]

En Machine Learning :

\[ f_(x) \]

désigne souvent un modèle dépendant de paramètres ().

# 5 — FONCTIONS D’UNE VARIABLE

Une fonction scalaire d’une variable possède la forme :

\[ f: \]

Exemples :

\[ f(x)=x^2 \]

\[ f(x)=(x) \]

\[ f(x)=e^x \]

\[ f(x)=(x) \]

Ces fonctions constituent les briques élémentaires du calcul différentiel.

# 6 — LIMITE

La limite décrit le comportement d’une fonction lorsqu’une variable se rapproche d’une valeur.

\[ \_{xa}f(x) \]

Elle permet de formaliser la notion de comportement local.

La dérivée sera construite à partir d’une limite.

# 7 — CONTINUITÉ

Une fonction est continue en (a) si :

\[ \_{xa}f(x)=f(a) \]

Intuitivement :

une petite variation de l’entrée entraîne une petite variation de la sortie.

La continuité ne garantit cependant pas automatiquement la différentiabilité.

# 8 — TAUX DE VARIATION MOYEN

Entre deux points (x) et (x+h) :

\[ \]

mesure le taux de variation moyen.

C’est la pente de la droite reliant les deux points.

Lorsque (h) devient très petit, on obtient la dérivée.

# 9 — DÉRIVÉE

La dérivée de (f) en (x) est :

\[ f’(x) = \_{h} \]

si cette limite existe.

La dérivée représente le **taux de variation instantané**.

# 10 — INTERPRÉTATION GÉOMÉTRIQUE

La dérivée correspond à la pente de la tangente à la courbe.

Courbe  
/  
/  
\---•----------------  
tangente

Si :

\[ f’(x)>0 \]

la fonction augmente localement.

Si :

\[ f’(x)<0 \]

elle diminue localement.

Si :

\[ f’(x)=0 \]

la tangente est horizontale.

# 11 — INTERPRÉTATION PHYSIQUE

Si :

\[ x(t) \]

représente une position, alors :

\[ v(t)=x’(t) \]

représente la vitesse.

Et :

\[ a(t)=v’(t)=x’’(t) \]

représente l’accélération.

Ainsi :

\[ \]

est une application fondamentale du calcul différentiel.

# 12 — DÉRIVÉES FONDAMENTALES

Pour (n) :

\[ x<sup>n=nx</sup>{n-1} \]

Constante :

\[ c=0 \]

Exponentielle :

\[ e<sup>x=e</sup>x \]

Logarithme :

\[ (x)=1x \]

Sinus :

\[ (x)=(x) \]

Cosinus :

\[ (x)=-(x) \]

# 13 — RÈGLE DE SOMME

Si :

\[ f(x)=g(x)+h(x) \]

alors :

\[ f’(x)=g’(x)+h’(x) \]

La dérivation est linéaire.

# 14 — RÈGLE DE MULTIPLICATION PAR UNE CONSTANTE

\[ \[cf(x)\] = cf’(x) \]

# 15 — RÈGLE DU PRODUIT

Si :

\[ f(x)=u(x)v(x) \]

alors :

\[ f’(x)=u’(x)v(x)+u(x)v’(x) \]

# 16 — RÈGLE DU QUOTIENT

Si :

\[ f(x)= \]

alors :

\[ f’(x) = {v(x)^2} \]

avec (v(x)).

# 17 — RÈGLE DE LA CHAÎNE

C’est l’une des notions les plus importantes pour le Machine Learning.

Si :

\[ y=f(g(x)) \]

alors :

\[ = f’(g(x))g’(x) \]

Autrement dit :

\[ \]

Cette règle permet de différencier une composition de fonctions.

# 18 — POURQUOI LA RÈGLE DE LA CHAÎNE EST CENTRALE EN ML

Un réseau neuronal est essentiellement une composition de fonctions.

Par exemple :

\[ x z_1 a_1 z_2 a_2 L \]

On peut écrire :

\[ L = f_n(f_{n-1}(f_2(f_1(x)))) \]

Pour déterminer comment la perte (L) dépend d’un paramètre, on applique la règle de la chaîne.

C’est précisément le principe mathématique de la **backpropagation**.

# 19 — DÉRIVATION IMPLICITE

Toutes les relations ne sont pas données sous la forme :

\[ y=f(x) \]

On peut avoir :

\[ F(x,y)=0 \]

On dérive alors les deux membres par rapport à (x).

Exemple :

\[ x<sup>2+y</sup>2=1 \]

donne :

\[ 2x+2y=0 \]

donc :

\[ =- \]

# 20 — DÉRIVÉE SECONDE

La dérivée de la dérivée est :

\[ f’’(x) \]

Elle renseigne notamment sur la courbure locale.

Si :

\[ f’’(x)>0 \]

la fonction est localement convexe.

Si :

\[ f’’(x)<0 \]

elle est localement concave.

# 21 — DÉRIVÉES D’ORDRE SUPÉRIEUR

On peut continuer :

\[ f’(x) \]

\[ f’’(x) \]

\[ f’’’(x) \]

etc.

La notation générale :

\[ f^{(n)}(x) \]

désigne la dérivée d’ordre (n).

Ces dérivées apparaissent notamment dans les développements de Taylor et certaines méthodes numériques.

# 22 — DIFFÉRENTIELLE

Pour une fonction d’une variable :

\[ df=f’(x)dx \]

La différentielle fournit une approximation locale de la variation.

Pour une petite variation (dx) :

\[ fdf \]

donc :

\[ ff’(x)x \]

# 23 — APPROXIMATION LINÉAIRE

Autour d’un point (a) :

\[ f(x) f(a)+f’(a)(x-a) \]

C’est l’approximation par la tangente.

Elle constitue le premier niveau du développement de Taylor.

# 24 — DÉVELOPPEMENT DE TAYLOR

Autour de (a) :

\[ f(x) f(a)

- f’(a)(x-a)
- (x-a)^2 + \]

Formellement :

\[ f(x) = \_{k=0}^{n} (x-a)^k

- R_n(x) \]

Le terme (R_n) représente le reste.

# 25 — POURQUOI TAYLOR EST IMPORTANT EN OPTIMISATION

Autour d’un point (x), une fonction peut être approximée par :

\[ f(x+x) f(x)

- f(x)^Tx
- x^THx \]

Cette formule explique mathématiquement pourquoi :

- le gradient décrit la variation de premier ordre ;
- la Hessienne décrit la courbure de second ordre.

# 26 — FONCTIONS DE PLUSIEURS VARIABLES

On considère maintenant :

\[ f:^n \]

Exemple :

\[ f(x,y)=x<sup>2+y</sup>2 \]

La fonction dépend de plusieurs variables.

On ne possède plus une seule dérivée.

On introduit les **dérivées partielles**.

# 27 — DÉRIVÉE PARTIELLE

La dérivée partielle par rapport à (x) consiste à faire varier (x) en maintenant les autres variables constantes.

\[ \]

Exemple :

\[ f(x,y)=x<sup>2+3xy+y</sup>2 \]

Alors :

\[ = 2x+3y \]

et :

\[ = 3x+2y \]

# 28 — GRADIENT

Pour :

\[ f:^n \]

le gradient est :

\[ f(x) =

\]

Le gradient est donc un vecteur.

# 29 — INTERPRÉTATION DU GRADIENT

Le gradient indique la direction de **plus forte augmentation locale** de la fonction.

Sa norme :

\[ |f(x)| \]

mesure l’intensité maximale de cette variation directionnelle.

La direction de descente maximale est :

\[ -f(x) \]

C’est le fondement de la descente de gradient.

# 30 — DÉRIVÉE DIRECTIONNELLE

Pour une direction (u), la dérivée directionnelle est :

\[ D_uf(x) = f(x)^Tu \]

si (u) est un vecteur directionnel.

Si (u) est unitaire :

\[ D_uf(x)=f(x)u \]

# 31 — PROPRIÉTÉ FONDAMENTALE DU GRADIENT

Pour une direction unitaire (u) :

\[ D_uf(x) = |f(x)| \]

où () est l’angle entre le gradient et (u).

Le maximum est obtenu lorsque :

\[ u= {|f(x)|} \]

Le minimum lorsque :

\[ u= - {|f(x)|} \]

# 32 — SURFACES DE NIVEAU

Une surface de niveau est définie par :

\[ f(x,y)=c \]

Le gradient est orthogonal aux surfaces de niveau.

Ainsi :

\[ f(x,y) \]

Cette propriété est importante en géométrie, optimisation et visualisation des fonctions de perte.

# 33 — DIFFÉRENTIABILITÉ

Une fonction est différentiable en un point si elle peut être correctement approximée localement par une application linéaire.

Pour :

\[ f:<sup>n</sup>m \]

on cherche une application linéaire (A) telle que :

\[ f(x+h) = f(x)+Ah+r(h) \]

avec :

\[ \]

lorsque :

\[ h \]

# 34 — DIFFÉRENTIELLE TOTALE

Pour :

\[ f:^n \]

la différentielle est :

\[ df = \_{i=1}^{n} dx_i \]

Sous forme vectorielle :

\[ df=f(x)^Tdx \]

Cette formule est fondamentale pour comprendre la relation entre différentielle et gradient.

# 35 — JACOBIENNE

Pour une fonction :

\[ F:<sup>n</sup>m \]

la Jacobienne est la matrice des dérivées premières :

\[ J_F(x) =

\]

Sa dimension est :

\[ mn \]

# 36 — JACOBIENNE ET DIFFÉRENTIELLE

Localement :

\[ F(x+x) F(x)+J_F(x)x \]

La Jacobienne est donc la généralisation multidimensionnelle de la dérivée.

# 37 — GRADIENT ET JACOBIENNE : DIFFÉRENCE

Pour :

\[ f:^n \]

le gradient est un vecteur.

Pour :

\[ F:<sup>n</sup>m \]

la Jacobienne est une matrice.

Conceptuellement :

scalaire → scalaire  
↓  
dérivée  
<br/>vecteur → scalaire  
↓  
gradient  
<br/>vecteur → vecteur  
↓  
Jacobienne

Les conventions ligne/colonne peuvent varier selon les ouvrages et bibliothèques ; il faut donc toujours vérifier la convention utilisée.

# 38 — HESSIENNE

Pour une fonction scalaire :

\[ f:^n \]

la Hessienne contient les dérivées secondes :

\[ H_f(x) = ^2f(x) \]

avec :

\[ H_f(x) =

\]

# 39 — INTERPRÉTATION DE LA HESSIENNE

Le gradient indique :

comment la fonction varie.

La Hessienne indique :

comment cette variation elle-même change.

Autrement dit :

gradient → pente locale  
Hessienne → courbure locale

# 40 — SYMÉTRIE DE LA HESSIENNE

Sous des hypothèses régulières de continuité des dérivées secondes :

\[ {x_ix_j} = {x_jx_i} \]

La Hessienne est alors symétrique.

# 41 — RÈGLE DE LA CHAÎNE MULTIVARIABLE

Si :

\[ z=f(u) \]

et :

\[ u=g(x) \]

alors :

\[ = \]

Dans le cas vectoriel :

\[ J_{fg}(x) = J_f(g(x))J_g(x) \]

Cette formule est au cœur de la backpropagation.

# 42 — RÈGLE DE LA CHAÎNE ET RÉSEAUX NEURONAUX

Considérons :

\[ x z a L \]

avec :

\[ z=Wx+b \]

\[ a=(z) \]

\[ L=L(a,y) \]

Alors :

\[ = \]

La backpropagation n’est donc pas une formule mystérieuse.

C’est une application systématique de la règle de chaîne.

# 43 — POINTS CRITIQUES

Un point (x^\*) peut être critique lorsque :

\[ f(x^\*)=0 \]

ou lorsque la dérivée n’existe pas.

Un point critique n’est pas nécessairement un minimum.

Il peut être :

- minimum local ;
- maximum local ;
- point selle ;
- point dégénéré.

# 44 — MINIMUM LOCAL

(x^\*) est un minimum local si, dans un voisinage de (x^\*) :

\[ f(x^\*)f(x) \]

# 45 — MAXIMUM LOCAL

(x^\*) est un maximum local si :

\[ f(x^\*)f(x) \]

dans un voisinage du point.

# 46 — POINT SELLE

Un point selle est un point où le comportement de la fonction varie dans différentes directions.

Exemple classique :

\[ f(x,y)=x<sup>2-y</sup>2 \]

Au point :

\[ (0,0) \]

le gradient est nul.

Mais le point n’est ni minimum ni maximum.

# 47 — TEST DE LA DÉRIVÉE SECONDE EN UNE VARIABLE

Si :

\[ f’(x^\*)=0 \]

alors :

- si (f’’(x^\*)>0), minimum local ;
- si (f’’(x^\*)<0), maximum local ;
- si (f’’(x^\*)=0), le test est inconclusif.

# 48 — TEST HESSIEN EN PLUSIEURS VARIABLES

Pour un point critique (x^\*) :

### Hessienne définie positive

\[ H(x^\*) \]

implique un minimum local strict sous les conditions appropriées.

### Hessienne définie négative

\[ H(x^\*) \]

implique un maximum local strict.

### Hessienne avec directions positives et négatives

Le point est de type selle.

### Hessienne semi-définie

Le test peut être inconclusif.

# 49 — VALEURS PROPRES ET COURBURE

Les valeurs propres de la Hessienne renseignent sur les directions principales de courbure.

Si :

\[ \_i>0 \]

dans toutes les directions, la courbure est positive.

Si certaines valeurs propres sont positives et d’autres négatives, on observe un comportement de selle.

Cette connexion explique pourquoi le calcul différentiel rejoint directement l’algèbre linéaire.

# 50 — CONVEXITÉ

Une fonction (f) est convexe si, pour (x,y) et (t) :

\[ f(tx+(1-t)y) tf(x)+(1-t)f(y) \]

Géométriquement, le graphe se situe sous ses cordes.

# 51 — CONVEXITÉ ET OPTIMISATION

Pour une fonction convexe, tout minimum local est également un minimum global.

C’est une propriété extrêmement importante en optimisation.

Elle permet de distinguer :

optimisation générale  
→ paysage potentiellement complexe  
<br/>optimisation convexe  
→ structure beaucoup plus contrôlée

# 52 — CRITÈRE HESSIEN DE CONVEXITÉ

Pour une fonction deux fois différentiable :

\[ H_f(x) \]

sur un domaine convexe constitue un critère de convexité.

Si :

\[ H_f(x) \]

partout, on obtient une forme de convexité stricte sous les hypothèses appropriées.

# 53 — LIPSCHITZIANITÉ DU GRADIENT

Une fonction possède un gradient (L)-Lipschitz si :

\[ |f(x)-f(y)| L|x-y| \]

Cette propriété est fondamentale dans l’analyse de convergence de la descente de gradient.

# 54 — CONDITIONNEMENT

Une fonction peut varier beaucoup plus fortement dans certaines directions que dans d’autres.

Cela conduit à des paysages étirés.

Un mauvais conditionnement peut ralentir l’optimisation.

La géométrie de la Hessienne joue un rôle central dans ce phénomène.

# 55 — DESCENTE DE GRADIENT

Le principe est :

\[ x_{k+1} = x_k-f(x_k) \]

où :

- (x_k) est l’état actuel ;
- () est le learning rate ;
- (f(x_k)) est le gradient.

On se déplace dans la direction opposée au gradient.

# 56 — POURQUOI LE SIGNE « MOINS » ?

Le gradient indique la direction de croissance maximale.

Pour diminuer (f), on choisit donc :

\[ -f(x) \]

D’où :

\[ x_{k+1} = x_k-f(x_k) \]

# 57 — LEARNING RATE

Le paramètre :

\[ \]

contrôle la taille du déplacement.

S’il est trop petit :

- apprentissage lent ;
- nombreuses itérations.

S’il est trop grand :

- oscillations ;
- divergence possible ;
- dépassement des minima.

Le learning rate est donc un paramètre d’optimisation essentiel.

# 58 — DESCENTE DE GRADIENT STOCHASTIQUE

Au lieu d’utiliser toute la fonction de perte sur toutes les données, on peut estimer le gradient à partir d’un mini-batch.

\[ \_{t+1} = \_t

- \_L_B(\_t) \]

où (B) représente un mini-batch.

Cela constitue le principe de SGD et de nombreux optimiseurs modernes.

# 59 — MOMENTUM

Le momentum introduit une mémoire des gradients précédents.

Une forme classique :

\[ v_t = v_{t-1}

- (1-)g_t \]

puis :

\[ _t =_ {t-1}

- v_t \]

L’idée est de réduire certains zigzags et d’accélérer le déplacement dans les directions cohérentes.

# 60 — ADAM

Adam combine notamment des estimations de premier et second moments du gradient.

On calcule :

\[ m_t = _1m_{t-1}

- (1-\_1)g_t \]

et :

\[ v_t = _2v_{t-1}

- (1-\_2)g_t^2 \]

avec correction du biais puis mise à jour des paramètres.

L’intérêt est d’adapter la taille effective des mises à jour selon les paramètres.

# 61 — MÉTHODES DU SECOND ORDRE

Les méthodes du premier ordre utilisent principalement :

\[ f \]

Les méthodes du second ordre utilisent également :

\[ H_f \]

Exemple :

\[ x_{k+1} = x_k-H(x_k)^{-1}f(x_k) \]

C’est l’idée de la méthode de Newton.

# 62 — MÉTHODE DE NEWTON

Pour résoudre :

\[ f’(x)=0 \]

on peut utiliser :

\[ x_{k+1} = x_k- \]

En optimisation multivariable :

\[ x_{k+1} = x_k- H(x_k)^{-1}f(x_k) \]

# 63 — LIMITES DES MÉTHODES DE NEWTON

Elles nécessitent :

- calcul de la Hessienne ;
- résolution d’un système linéaire ;
- coût computationnel potentiellement élevé ;
- gestion de Hessiennes mal conditionnées ou non définies positives.

Pour de très grands modèles de ML, une Hessienne complète peut être beaucoup trop coûteuse à stocker.

# 64 — QUASI-NEWTON

Les méthodes quasi-Newton cherchent à approximer la Hessienne ou son inverse.

Exemples :

- BFGS ;
- L-BFGS.

Elles cherchent à obtenir une partie des avantages des méthodes du second ordre sans construire explicitement une Hessienne complète.

# 65 — OPTIMISATION SOUS CONTRAINTES

On peut chercher :

\[ \_x f(x) \]

sous :

\[ g_i(x) \]

et :

\[ h_j(x)=0 \]

Cela conduit à l’optimisation contrainte.

# 66 — MULTIPLICATEURS DE LAGRANGE

Pour :

\[ f(x) \]

sous :

\[ g(x)=0 \]

on construit :

\[ (x,) = f(x)+g(x) \]

et on cherche les points satisfaisant les conditions stationnaires appropriées.

# 67 — CONDITIONS KKT

Pour des problèmes d’optimisation avec contraintes, les conditions de Karush-Kuhn-Tucker généralisent les multiplicateurs de Lagrange.

Elles font intervenir notamment :

- stationnarité ;
- faisabilité primale ;
- faisabilité duale ;
- complémentarité.

Elles sont fondamentales en optimisation moderne.

# 68 — DIFFÉRENTIATION MATRICIELLE

En Machine Learning, les variables sont rarement de simples scalaires.

On manipule :

- vecteurs ;
- matrices ;
- tenseurs.

Il faut donc savoir différencier des expressions matricielles.

# 69 — EXEMPLE VECTORIEL

Soit :

\[ f(x)=a^Tx \]

Alors :

\[ \_x f=a \]

# 70 — FORME QUADRATIQUE

Pour :

\[ f(x)=x^TAx \]

on obtient, dans le cas général :

\[ \_x f = (A+A^T)x \]

Si (A) est symétrique :

\[ \_x f=2Ax \]

et :

\[ H=2A \]

# 71 — LE CAS DU SQUARED ERROR

Considérons :

\[ f(x)=|Ax-b|^2 \]

Alors :

\[ f(x) = A^T(Ax-b) \]

et :

\[ H=A^TA \]

Cette structure apparaît partout en régression, optimisation et apprentissage.

# 72 — LOG-LIKELIHOOD ET CALCUL DIFFÉRENTIEL

En statistiques et ML, on cherche souvent à maximiser :

\[ () \]

ou à minimiser :

\[ -() \]

Le gradient :

\[ \_() \]

indique comment modifier les paramètres.

La Hessienne :

\[ \_^2() \]

décrit la courbure locale de la vraisemblance.

Le calcul différentiel constitue donc le pont entre les domaines G, H et I.

# 73 — FONCTION DE PERTE

Un modèle produit :

\[ y=f_(x) \]

On définit une fonction de perte :

\[ L(y,y) \]

Puis une fonction objectif :

\[ J() = 1n _{i=1}^{n} L(f_(x_i),y_i) \]

L’entraînement cherche alors :

\[ ^\* = \_J() \]

Le calcul différentiel intervient pour calculer :

\[ \_J() \]

# 74 — CHAÎNE FONDAMENTALE DU MACHINE LEARNING

La chaîne centrale est :

\[ f(x) f’(x) f(x) \]

Plus précisément :

\[ \]

Cette boucle constitue l’une des structures mathématiques fondamentales du Machine Learning.

# 75 — BACKPROPAGATION

La backpropagation calcule efficacement les dérivées de la fonction de perte par rapport aux paramètres du réseau.

Elle exploite la structure en graphe de calcul.

Entrée  
↓  
Couche 1  
↓  
Couche 2  
↓  
Couche 3  
↓  
Sortie  
↓  
Loss  
↓  
Gradient  
↓  
Retour vers les paramètres

# 76 — GRAPHE DE CALCUL

Une expression complexe peut être décomposée en opérations élémentaires.

Exemple :

\[ L=(wx+b-y)^2 \]

On peut construire :

x ──┐  
× → wx ──┐  
w ──┘ +  
↓  
b ───────────┘  
↓  
erreur  
↓  
carré  
↓  
L

La différentiation consiste ensuite à remonter ce graphe.

# 77 — GRADIENT LOCAL

Chaque opération du graphe possède une dérivée locale.

La règle de chaîne combine ces dérivées.

Si :

\[ z=f(y) \]

et :

\[ y=g(x) \]

alors :

\[ = \]

La backpropagation répète ce principe à grande échelle.

# 78 — DIFFÉRENTIATION AUTOMATIQUE

La différentiation automatique, ou autodiff, construit les dérivées à partir du graphe de calcul.

Elle n’est pas simplement :

- de la dérivation symbolique ;
- ni de la différence finie.

Elle applique systématiquement les règles de différentiation aux opérations exécutées.

# 79 — FORWARD MODE ET REVERSE MODE

Deux grandes stratégies :

### Forward mode

On propage les dérivées vers l’avant.

Particulièrement intéressant lorsque le nombre d’entrées est relativement faible par rapport au nombre de sorties.

### Reverse mode

On effectue une propagation inverse.

Particulièrement intéressant lorsque l’on possède :

- énormément de paramètres ;
- une sortie scalaire.

C’est précisément pourquoi le reverse mode est central dans l’entraînement des réseaux neuronaux.

# 80 — DIFFÉRENCE FINIE

Une dérivée peut être approximée numériquement.

Différence avant :

\[ f’(x) \]

Différence centrée :

\[ f’(x) \]

Ces méthodes sont utiles pour vérifier des gradients.

# 81 — GRADIENT CHECKING

Pour tester une implémentation de gradient :

\[ g_{} \]

est comparé à :

\[ g_{} \]

Une erreur relative peut être calculée.

Le gradient checking est particulièrement utile pour déboguer une implémentation de backpropagation.

# 82 — PROBLÈME DES ERREURS NUMÉRIQUES

Choisir (h) trop grand provoque une erreur de troncature.

Choisir (h) trop petit peut provoquer des erreurs d’arrondi.

Il faut donc choisir un pas approprié.

C’est une illustration importante de la différence entre :

mathématiques exactes  
↓  
calcul numérique  
↓  
approximation informatique

# 83 — VANISHING GRADIENT

Dans une longue composition :

\[ f_nf_{n-1}f_1 \]

la règle de chaîne produit des produits de dérivées.

Si les facteurs sont souvent inférieurs à 1 :

\[ \_i a_i \]

peut devenir extrêmement petit.

Le gradient peut alors tendre vers zéro.

C’est le phénomène de **vanishing gradient**.

# 84 — EXPLODING GRADIENT

Inversement, si les facteurs sont fréquemment supérieurs à 1 :

\[ \_i a_i \]

peut devenir extrêmement grand.

On obtient alors un **exploding gradient**.

# 85 — FONCTIONS D’ACTIVATION ET DÉRIVÉES

Les activations courantes comprennent :

- sigmoid ;
- tanh ;
- ReLU ;
- variantes de ReLU ;
- fonctions lisses modernes.

Exemple :

\[ (x)= \]

et :

\[ ’(x) = (x)(1-(x)) \]

La dérivée de l’activation participe directement à la backpropagation.

# 86 — RELU

La fonction ReLU est :

\[ (x) = (0,x) \]

Sa dérivée est :

\[ ’(x) =

\]

Le point (x=0) nécessite une convention particulière pour l’implémentation.

# 87 — SOFTMAX

Pour des logits (z_i) :

\[ (z_i) = {\_j e^{z_j}} \]

Sa Jacobienne est non diagonale :

\[ = s_i(\_{ij}-s_j) \]

Cela montre pourquoi le calcul matriciel devient indispensable en classification multiclasse.

# 88 — CROSS-ENTROPY ET DIFFÉRENTIATION

Pour une classification, la combinaison softmax + cross-entropy possède une structure particulièrement favorable pour le calcul du gradient.

Dans la formulation standard :

\[ L=-\_i y_ip_i \]

on obtient par rapport aux logits une expression simplifiée liée à :

\[ p-y \]

Cette propriété est très importante dans les implémentations de réseaux neuronaux.

# 89 — RÉSEAU NEURONAL COMME COMPOSITION DIFFÉRENTIABLE

Un réseau peut être représenté comme :

\[ f_ = f_Lf_{L-1}f_1 \]

L’entraînement cherche :

\[ \_J() \]

Le gradient :

\[ \_J \]

est calculé par différentiation de la composition.

Ainsi :

\[ \]

# 90 — PAYSAGE DE PERTE

La fonction :

\[ J() \]

définit un paysage dans l’espace des paramètres.

On peut y observer :

- minima ;
- maxima ;
- selles ;
- vallées ;
- plateaux ;
- régions fortement courbées ;
- régions faiblement courbées.

L’optimisation consiste à parcourir ce paysage.

# 91 — MINIMA LOCAUX ET GLOBAUX

Un minimum local n’est pas nécessairement global.

En optimisation non convexe :

\[ x_{} x_{} \]

Cette distinction est fondamentale pour comprendre les problèmes d’apprentissage complexes.

# 92 — POINTS SELLES DANS LES MODÈLES COMPLEXES

Dans les espaces de grande dimension, les points selles peuvent devenir importants dans l’analyse des paysages d’optimisation.

La Hessienne permet d’étudier la courbure locale.

# 93 — PLATEAUX

Un plateau correspond à une région dans laquelle :

\[ |f(x)| \]

est faible.

Les mises à jour deviennent alors petites.

Cela peut ralentir l’apprentissage.

# 94 — COURBURE ET CONDITIONNEMENT

Une vallée étroite peut avoir :

- forte courbure dans une direction ;
- faible courbure dans une autre.

Une descente de gradient naïve peut alors zigzaguer.

Cela explique l’intérêt de :

- momentum ;
- préconditionnement ;
- méthodes adaptatives ;
- méthodes du second ordre.

# 95 — NORMALISATION ET GÉOMÉTRIE DE L’OPTIMISATION

La mise à l’échelle des variables influence la géométrie du problème.

Deux variables ayant des échelles très différentes peuvent produire un paysage fortement anisotrope.

La normalisation peut donc faciliter l’optimisation.

# 96 — OPTIMISATION STOCHASTIQUE

Dans le ML moderne, le gradient exact de l’objectif total est souvent remplacé par une estimation.

\[ g_t J(\_t) \]

Cette estimation introduit du bruit.

Le bruit peut parfois être défavorable, mais il peut également modifier favorablement la dynamique de recherche dans certains problèmes.

# 97 — GRADIENT DESCENT ET RÉGRESSION LINÉAIRE

Pour :

\[ J(w) = \_i (w<sup>Tx_i-y_i)</sup>2 \]

on obtient :

\[ J(w) = 1n X^T(Xw-y) \]

La mise à jour devient :

\[ w_{t+1} = w_t-J(w_t) \]

Cela fournit l’un des exemples les plus simples d’apprentissage par optimisation.

# 98 — RÉGULARISATION

On peut modifier l’objectif :

\[ J() = L()+R() \]

Exemple L2 :

\[ R()=||\_2^2 \]

Alors :

\[ R()=2 \]

La régularisation influence donc directement le gradient.

# 99 — DÉRIVATION D’UNE FONCTION DE PERTE

Pour un modèle :

\[ y=f_(x) \]

et une perte :

\[ L(y,y) \]

on cherche :

\[ \_L \]

La chaîne fondamentale est :

\[ = \]

Dans un réseau profond, cette relation se propage à travers toutes les couches.

# 100 — DÉRIVÉES ET BIAIS/VARIANCE EN ML

Le calcul différentiel ne suffit pas à expliquer le comportement statistique d’un modèle.

Il faut le combiner avec le domaine H.

Statistiques  
→ mesure l'erreur et l'incertitude  
<br/>Calcul différentiel  
→ indique comment modifier les paramètres  
<br/>Optimisation  
→ décide comment effectuer les modifications  
<br/>Machine Learning  
→ utilise les trois

# 101 — DIFFÉRENTIATION DES TENSEURS

Les modèles modernes manipulent des tenseurs.

Le principe reste le même :

\[ \]

Chaque opération possède une règle de différentiation.

La difficulté devient principalement une question de :

- dimensions ;
- broadcasting ;
- contraction ;
- mémoire ;
- efficacité computationnelle.

# 102 — JACOBIENNES DE TENSEURS

Dans la pratique, on ne construit généralement pas explicitement toutes les Jacobiennes gigantesques.

On utilise des produits Jacobienne-vecteur ou vecteur-Jacobienne.

Cela permet d’exploiter la structure computationnelle.

# 103 — JVP ET VJP

### JVP

Jacobian-vector product :

\[ Jv \]

### VJP

Vector-Jacobian product :

\[ v^TJ \]

Le reverse mode repose essentiellement sur des calculs de type VJP.

Ces opérations sont centrales dans les systèmes modernes de différentiation automatique.

# 104 — GRADIENT D’UNE SORTIE SCALAIRE

Pour :

\[ f:^n \]

le gradient possède (n) composantes.

C’est précisément le cas idéal pour le reverse mode :

beaucoup de paramètres  
↓  
une loss scalaire  
↓  
reverse-mode autodiff

# 105 — HESSIENNE EN DEEP LEARNING

La Hessienne complète peut être énorme.

Si un modèle possède (n) paramètres :

\[ H^{nn} \]

Le stockage naïf nécessite :

\[ O(n^2) \]

éléments.

C’est généralement prohibitif pour de très grands modèles.

# 106 — HESSIAN-VECTOR PRODUCT

Plutôt que construire :

\[ H \]

on peut calculer :

\[ Hv \]

directement.

Cela permet d’exploiter certaines informations du second ordre avec un coût et une mémoire plus raisonnables.

# 107 — DIFFÉRENTIATION ET COMPUTER GRAPHICS

Le calcul différentiel intervient dans :

- animation ;
- optimisation de formes ;
- reconstruction 3D ;
- rendu différentiable ;
- estimation de paramètres ;
- inverse rendering ;
- simulation ;
- contrôle.

# 108 — TRANSFORMATIONS GÉOMÉTRIQUES

Une transformation peut être écrite :

\[ y=f(x) \]

Sa Jacobienne décrit comment de petites perturbations de (x) affectent (y).

C’est utile pour :

- transformations ;
- projection ;
- optimisation géométrique ;
- estimation de pose ;
- vision par ordinateur.

# 109 — NORMALES ET GÉOMÉTRIE DIFFÉRENTIELLE

Pour une surface implicite :

\[ F(x,y,z)=0 \]

le gradient :

\[ F \]

est normal à la surface sous les conditions régulières appropriées.

Le calcul différentiel rejoint ainsi directement la géométrie computationnelle.

# 110 — SIMULATION PHYSIQUE

Une dynamique peut être décrite par :

\[ =v \]

et :

\[ =a \]

Le calcul différentiel permet donc de modéliser :

- mouvement ;
- vitesse ;
- accélération ;
- forces ;
- dynamique des systèmes.

# 111 — ÉQUATIONS DIFFÉRENTIELLES

Une équation différentielle relie une fonction à ses dérivées.

Exemple :

\[ =f(x,t) \]

Les équations différentielles constituent un prolongement naturel du calcul différentiel.

Elles sont particulièrement importantes pour :

- simulation ;
- physique ;
- contrôle ;
- modélisation ;
- dynamique ;
- systèmes scientifiques.

# 112 — INTÉGRATION NUMÉRIQUE ET DIFFÉRENTIATION

Le calcul différentiel et l’intégration sont profondément liés.

Le théorème fondamental du calcul relie dérivée et intégrale.

En informatique scientifique, on travaille souvent avec :

différentiation  
+  
intégration  
+  
approximation numérique

# 113 — DIFFÉRENTIATION ET CONTRÔLE

Dans les systèmes de contrôle, on optimise souvent une trajectoire ou une politique.

Le gradient permet d’évaluer comment une modification des paramètres affecte un objectif.

Cette idée rejoint :

- contrôle optimal ;
- robotique ;
- reinforcement learning.

# 114 — REINFORCEMENT LEARNING

Une politique peut être paramétrée par :

\[ \_(a|s) \]

L’objectif dépend de :

\[ J() \]

On cherche :

\[ \_J() \]

Le calcul différentiel devient alors un élément du mécanisme d’apprentissage de la politique.

# 115 — OPTIMISATION ET PROBABILITÉS

Dans les modèles probabilistes :

\[ p_(x) \]

dépend de paramètres.

On peut chercher :

\[ _p_(x) \]

Cette quantité apparaît dans :

- maximum de vraisemblance ;
- modèles probabilistes ;
- estimation ;
- méthodes de gradient ;
- apprentissage génératif.

# 116 — OPTIMISATION ET STATISTIQUES

Le maximum de vraisemblance cherche :

\[ ^\* = _ L() \]

ou :

\[ ^\* = _ -L() \]

Le gradient permet de chercher efficacement ce paramètre.

Ainsi :

\[ \]

# 117 — GRADIENT D’UNE ESPÉRANCE

Dans certains modèles probabilistes, on doit différencier :

\[ {xp_} \[f_(x)\] \]

Ce type de problème conduit à des techniques avancées :

- score function ;
- reparameterization trick ;
- différentiation sous le signe intégral ;
- méthodes Monte Carlo différentiables.

# 118 — REPARAMÉTRISATION

L’idée consiste à réécrire une variable aléatoire dépendant de () sous la forme :

\[ z=g(,) \]

où () possède une distribution indépendante de ().

On peut alors propager le gradient à travers (g).

Cette idée est centrale dans certaines méthodes d’apprentissage génératif.

# 119 — DIFFÉRENTIATION ET MODÈLES GÉNÉRATIFS

Dans certains modèles génératifs, l’entraînement nécessite de différencier :

- distributions ;
- transformations ;
- fonctions de coût ;
- échantillonnages reparamétrés.

Le calcul différentiel devient donc un outil de base de l’apprentissage génératif moderne.

# 120 — OPTIMISATION LOCALE

Le calcul différentiel est essentiellement local.

Il décrit ce qui se passe lorsque :

\[ x \]

Cette information locale peut ensuite être utilisée pour construire des algorithmes globaux d’optimisation.

# 121 — LOCAL VS GLOBAL

Une information différentielle :

\[ f(x) \]

décrit le comportement autour de (x).

Elle ne garantit pas automatiquement :

\[ = \]

Pour obtenir des garanties globales, il faut exploiter des structures supplémentaires :

- convexité ;
- coercivité ;
- compacité ;
- conditions particulières du problème.

# 122 — STATIONNARITÉ

Une condition fondamentale d’optimalité intérieure est :

\[ f(x^\*)=0 \]

Mais cette condition est seulement nécessaire sous certaines hypothèses, pas suffisante.

C’est une distinction importante :

gradient nul  
≠  
minimum garanti

# 123 — DESCENTE DE GRADIENT COMME ALGORITHME

Schéma :

Initialiser θ  
<br/>↓  
<br/>Calculer la prédiction  
<br/>↓  
<br/>Calculer la loss  
<br/>↓  
<br/>Calculer le gradient  
<br/>↓  
<br/>Mettre à jour θ  
<br/>↓  
<br/>Répéter

Mathématiquement :

\[ \_{t+1} = \_t-_t_J(\_t) \]

# 124 — CRITÈRES D’ARRÊT

Une optimisation peut être arrêtée lorsque :

\[ |J()|< \]

ou lorsque :

\[ |J_{t+1}-J_t|< \]

ou après un nombre maximal d’itérations.

En ML, on utilise également des critères liés à la validation.

# 125 — CONVERGENCE

Une suite :

\[ x_k \]

converge vers (x^\*) si :

\[ x_kx^\* \]

L’analyse de convergence cherche à déterminer :

- si l’algorithme converge ;
- vers quoi il converge ;
- à quelle vitesse ;
- sous quelles hypothèses.

# 126 — TAUX DE CONVERGENCE

On distingue notamment :

- convergence linéaire ;
- superlinéaire ;
- quadratique.

La méthode de Newton peut présenter une convergence quadratique locale sous des hypothèses appropriées.

# 127 — COMPLEXITÉ DU CALCUL DIFFÉRENTIEL NUMÉRIQUE

La complexité dépend notamment de :

- nombre de variables ;
- structure des fonctions ;
- dimension des matrices ;
- nombre de couches ;
- nombre de paramètres ;
- coût d’une évaluation forward ;
- coût d’une différentiation backward.

Dans les réseaux neuronaux modernes, le coût de la backpropagation est généralement du même ordre de grandeur que quelques évaluations du réseau, plutôt que celui d’une Jacobienne dense complète.

# 128 — STRUCTURES DE DONNÉES IMPLIQUÉES

Le calcul différentiel informatique utilise notamment :

- vecteurs ;
- matrices ;
- tenseurs ;
- graphes de calcul ;
- graphes orientés acycliques ;
- buffers de gradients ;
- structures de mémorisation d’opérations.

# 129 — GRAPHE DE CALCUL ET MÉMOIRE

Pour calculer les gradients en reverse mode, il faut souvent conserver certaines valeurs intermédiaires du passage avant.

Cela crée un compromis :

plus de mémoire  
→  
moins de recomputation  
<br/>moins de mémoire  
→  
plus de recalcul

Cette question est fondamentale dans l’entraînement des grands modèles.

# 130 — CHECKPOINTING

Le gradient checkpointing consiste à ne pas conserver toutes les activations.

Certaines sont recalculées lors du backward.

On échange donc :

\[ \]

# 131 — NUMERICAL STABILITY

Une formule mathématiquement correcte peut être numériquement instable.

Il faut surveiller :

- overflow ;
- underflow ;
- cancellation ;
- divisions par de petites quantités ;
- exponentielles ;
- logarithmes.

La stabilité numérique est aussi importante que la formule analytique.

# 132 — LOG-SUM-EXP

Pour calculer :

\[ \_i e^{x_i} \]

de manière stable, on utilise généralement :

\[ m+\_i e^{x_i-m} \]

avec :

\[ m=\_i x_i \]

Cette technique est particulièrement importante dans les modèles probabilistes et la classification.

# 133 — GRADIENT CLIPPING

Pour éviter des gradients excessivement grands, on peut limiter leur norme.

Par exemple :

\[ g g \]

lorsque :

\[ |g|>c \]

Cette technique est particulièrement utile dans certaines architectures et problèmes d’entraînement.

# 134 — GRADIENT ACCUMULATION

Lorsque la mémoire GPU ne permet pas un grand batch, on peut accumuler plusieurs gradients avant d’effectuer une mise à jour.

Cela modifie la manière dont le gradient est agrégé sans modifier nécessairement le modèle mathématique de base.

# 135 — DÉRIVÉES ET AUTO-DIFF DANS LES FRAMEWORKS

Les frameworks modernes de ML fournissent des moteurs de différentiation automatique.

Le principe conceptuel reste :

opération  
↓  
graphe  
↓  
valeurs intermédiaires  
↓  
dérivées locales  
↓  
règle de chaîne  
↓  
gradient

L’outil automatise le calcul ; il ne remplace pas la compréhension mathématique.

# 136 — DIFFÉRENCIATION SYMBOLIQUE

Un système symbolique manipule les expressions elles-mêmes.

Exemple :

\[ f(x)=x^2 \]

donne :

\[ f’(x)=2x \]

La dérivée est obtenue analytiquement.

# 137 — DIFFÉRENCIATION NUMÉRIQUE

On approxime la dérivée par des évaluations de la fonction.

Exemple :

\[ f’(x) \]

Elle est simple mais sujette aux erreurs numériques.

# 138 — DIFFÉRENCIATION AUTOMATIQUE

L’autodiff applique automatiquement les règles de différentiation aux opérations d’un programme.

Elle est donc conceptuellement différente de :

- différentiation symbolique ;
- différences finies.

# 139 — COMPARAISON DES TROIS APPROCHES

| Méthode | Principe | Usage |
| --- | --- | --- |
| Symbolique | Manipuler les expressions | Mathématiques symboliques |
| Numérique | Approximer avec des évaluations | Vérification |
| Automatique | Propager les dérivées dans un graphe | ML  |

# 140 — CONNEXION AVEC L’ALGÈBRE LINÉAIRE

Le domaine C fournit :

- vecteurs ;
- matrices ;
- produits matriciels ;
- valeurs propres ;
- normes.

Le calcul différentiel les utilise directement.

Exemple :

\[ f(x) \]

est un vecteur.

\[ J_f(x) \]

est une matrice.

\[ H_f(x) \]

est une matrice symétrique dans les conditions régulières usuelles.

# 141 — CONNEXION AVEC LA GÉOMÉTRIE COMPUTATIONNELLE

Le gradient permet de définir :

- normales ;
- surfaces de niveau ;
- directions locales ;
- distances signées.

La Jacobienne décrit les déformations locales.

La Hessienne décrit des aspects de la courbure.

# 142 — CONNEXION AVEC LES PROBABILITÉS

Les modèles probabilistes utilisent des fonctions dépendant de paramètres.

On différencie :

\[ p_(x) \]

ou :

\[ p_(x) \]

pour effectuer de l’estimation et de l’optimisation.

# 143 — CONNEXION AVEC LES STATISTIQUES

Le domaine H utilise notamment :

- maximum de vraisemblance ;
- régression ;
- estimation ;
- fonction de perte ;
- optimisation.

Le calcul différentiel explique comment obtenir les estimateurs par optimisation.

# 144 — CONNEXION AVEC LA COMBINATOIRE

La combinatoire travaille souvent sur des structures discrètes, tandis que le calcul différentiel travaille sur des variations continues.

Mais ils se rencontrent dans :

- probabilités ;
- optimisation ;
- analyse d’algorithmes ;
- espaces de paramètres ;
- méthodes combinatoires optimisées numériquement.

# 145 — CONNEXION AVEC LA THÉORIE DES GRAPHES

Les graphes de calcul sont des graphes orientés représentant les dépendances entre opérations.

Ainsi :

Théorie des graphes  
↓  
graphe de calcul  
↓  
différentiation  
↓  
backpropagation

Le domaine E trouve donc une application directe dans le calcul différentiel automatique.

# 146 — APPLICATIONS WEB

Le calcul différentiel intervient indirectement dans :

- recommandations ;
- recherche ;
- ranking ;
- personnalisation ;
- systèmes de prédiction ;
- détection de fraude ;
- systèmes publicitaires ;
- optimisation de modèles.

Il peut également intervenir directement dans des applications graphiques et interactives avancées.

# 147 — APPLICATIONS SYSTÈMES

Dans les systèmes informatiques :

- optimisation de ressources ;
- contrôle ;
- planification ;
- calibration ;
- estimation de paramètres ;
- simulation ;
- robotique ;
- systèmes autonomes.

# 148 — APPLICATIONS IA

Applications majeures :

- classification ;
- régression ;
- réseaux neuronaux ;
- vision ;
- NLP ;
- modèles génératifs ;
- reinforcement learning ;
- détection d’anomalies ;
- optimisation de politiques ;
- apprentissage représentationnel.

# 149 — APPLICATIONS COMPUTER VISION

Le calcul différentiel intervient dans :

- estimation de pose ;
- optimisation de caméra ;
- reconstruction 3D ;
- optical flow ;
- calibration ;
- reconstruction différentiable ;
- apprentissage de représentations visuelles.

# 150 — APPLICATIONS 3D

Dans un moteur 3D, on peut chercher à optimiser :

- position ;
- rotation ;
- paramètres de caméra ;
- paramètres de matériau ;
- éclairage ;
- géométrie.

Le gradient indique comment modifier ces paramètres pour réduire une erreur.

# 151 — APPLICATIONS EN ANIMATION

Une trajectoire :

\[ x(t) \]

permet d’obtenir :

\[ v(t)=x’(t) \]

et :

\[ a(t)=x’’(t) \]

Le contrôle de l’accélération permet d’obtenir des animations plus naturelles.

# 152 — INTERPOLATION

On peut utiliser différentes fonctions pour contrôler une transition :

\[ x(t)=f(t) \]

Les propriétés de :

\[ f’(t) \]

et :

\[ f’’(t) \]

permettent de contrôler :

- vitesse ;
- accélération ;
- fluidité ;
- continuité du mouvement.

# 153 — DIFFÉRENTIABILITÉ ET ANIMATION

Une transition peut être :

- continue ;
- dérivable ;
- deux fois dérivable.

Une transition visuellement fluide peut nécessiter plus qu’une simple continuité.

Le contrôle des dérivées permet de construire des mouvements avec des transitions plus naturelles.

# 154 — PROJET 1 — VISUALISATEUR DE DÉRIVÉE

Construire une application qui affiche :

- une fonction ;
- sa tangente ;
- la pente ;
- la valeur de la dérivée.

Exemples :

\[ x^2 \]

\[ x \]

\[ e^x \]

Objectif :

comprendre visuellement la dérivée.

# 155 — PROJET 2 — VISUALISATEUR DE GRADIENT

Construire une surface :

\[ f(x,y) \]

avec :

- courbes de niveau ;
- gradient ;
- direction de descente ;
- trajectoire d’un optimiseur.

Objectif :

visualiser la relation entre gradient et optimisation.

# 156 — PROJET 3 — MINI GRADIENT DESCENT

Implémenter :

\[ x_{t+1} = x_t-f(x_t) \]

sur plusieurs fonctions.

Tester :

- learning rate faible ;
- learning rate raisonnable ;
- learning rate élevé.

Observer :

- convergence ;
- oscillation ;
- divergence.

# 157 — PROJET 4 — RÉGRESSION LINÉAIRE PAR GRADIENT DESCENT

Implémenter une régression :

\[ y=Xw+b \]

avec :

\[ J(w,b) = 1n \_i (y_i-y_i)^2 \]

Puis calculer manuellement :

\[ \_wJ \]

et :

\[ \]

# 158 — PROJET 5 — MINI RÉSEAU NEURONAL SANS AUTODIFF

Construire un petit réseau neuronal en calculant manuellement :

- forward ;
- loss ;
- dérivées ;
- backward ;
- mise à jour.

Objectif :

comprendre réellement la backpropagation avant d’utiliser un framework.

# 159 — PROJET 6 — AUTODIFF MINIMAL

Construire un mini moteur capable de représenter :

addition  
multiplication  
puissance  
exp  
log

et de calculer automatiquement les dérivées.

Cela permet de comprendre les principes fondamentaux d’un moteur d’autodiff.

# 160 — PROJET 7 — VISUALISATION DE HESSIENNE

Pour une fonction :

\[ f(x,y) \]

afficher :

- surface ;
- gradient ;
- Hessienne ;
- valeurs propres ;
- directions principales.

Objectif :

relier calcul différentiel et algèbre linéaire.

# 161 — PROJET 8 — OPTIMISATION SOUS CONTRAINTE

Implémenter un problème du type :

\[ f(x,y) \]

sous :

\[ g(x,y)=0 \]

et visualiser :

- fonction ;
- contrainte ;
- point optimal ;
- gradient ;
- multiplicateur de Lagrange.

# 162 — EXERCICES DE MAÎTRISE — NIVEAU 1

Être capable de dériver sans assistance :

\[ x^n \]

\[ e^x \]

\[ x \]

\[ x \]

\[ x \]

ainsi que des compositions et produits.

# 163 — EXERCICES — NIVEAU 2

Calculer :

\[ f(x,y) \]

pour plusieurs fonctions.

Puis déterminer :

- points critiques ;
- Hessienne ;
- nature des points.

# 164 — EXERCICES — NIVEAU 3

Pour une fonction :

\[ f:^n \]

être capable d’expliquer :

- gradient ;
- dérivée directionnelle ;
- Hessienne ;
- convexité ;
- conditionnement.

# 165 — EXERCICES — NIVEAU 4

Pour une fonction composée :

\[ L=f_3(f_2(f_1(x))) \]

calculer :

\[ \]

manuellement par la règle de chaîne.

# 166 — EXERCICES — NIVEAU 5

Prendre un neurone :

\[ z=wx+b \]

\[ a=(z) \]

\[ L=(a-y)^2 \]

et calculer :

\[ \]

manuellement.

# 167 — EXERCICES — NIVEAU 6

Pour un réseau à plusieurs couches, écrire la chaîne complète des dérivées.

L’objectif n’est pas de mémoriser une formule unique.

L’objectif est de savoir reconstruire le gradient à partir de la règle de chaîne.

# 168 — DÉFIS SANS IA

### Défi 1

Expliquer la dérivée sans utiliser la définition apprise par cœur.

### Défi 2

Expliquer pourquoi le gradient indique la direction de plus forte croissance.

### Défi 3

Démontrer la règle de chaîne sur un exemple simple.

### Défi 4

Expliquer pourquoi :

\[ f=0 \]

ne signifie pas nécessairement minimum.

### Défi 5

Expliquer pourquoi la backpropagation est une application de la règle de chaîne.

# 169 — DÉFIS AVEC IA

L’IA peut être utilisée pour :

- générer des fonctions d’entraînement ;
- vérifier les dérivées ;
- proposer des contre-exemples ;
- expliquer une erreur ;
- générer des paysages d’optimisation ;
- comparer deux optimiseurs ;
- analyser un gradient.

Mais une règle importante demeure :

Tu dois être capable de reconstruire le raisonnement sans l’IA.

# 170 — FICHES DE DEEP DIVE À CONSTRUIRE

Le domaine I peut être approfondi à travers les fiches suivantes.

### I01 — Limites

### I02 — Continuité

### I03 — Définition de la dérivée

### I04 — Règles de dérivation

### I05 — Règle de chaîne

### I06 — Dérivation implicite

### I07 — Dérivées secondes

### I08 — Taylor

### I09 — Différentielles

### I10 — Dérivées partielles

### I11 — Gradient

### I12 — Dérivées directionnelles

### I13 — Surfaces de niveau

### I14 — Différentiabilité multivariable

### I15 — Jacobienne

### I16 — Hessienne

### I17 — Convexité

### I18 — Points critiques

### I19 — Extrema

### I20 — Points selles

### I21 — Optimisation locale

### I22 — Optimisation globale

### I23 — Multiplicateurs de Lagrange

### I24 — Conditions KKT

### I25 — Gradient Descent

### I26 — SGD

### I27 — Momentum

### I28 — Adam

### I29 — Newton

### I30 — Quasi-Newton

### I31 — Conditionnement

### I32 — Lipschitz

### I33 — Convergence

### I34 — Différences finies

### I35 — Gradient Checking

### I36 — Différentiation automatique

### I37 — Forward Mode

### I38 — Reverse Mode

### I39 — JVP

### I40 — VJP

### I41 — Backpropagation

### I42 — Fonctions d’activation

### I43 — Vanishing Gradient

### I44 — Exploding Gradient

### I45 — Hessian-vector products

### I46 — Optimisation des réseaux neuronaux

### I47 — Loss Functions

### I48 — Régularisation

### I49 — Optimisation probabiliste

### I50 — Maximum de vraisemblance

### I51 — Calcul différentiel et vision

### I52 — Calcul différentiel et 3D

### I53 — Calcul différentiel et simulation

### I54 — Équations différentielles

### I55 — Contrôle optimal

### I56 — Différentiable Rendering

### I57 — Différentiation des tenseurs

### I58 — Optimisation sous contraintes

### I59 — Analyse numérique

### I60 — Calcul différentiel appliqué au Deep Learning

# 171 — CE QU’IL FAUT ABSOLUMENT RETENIR

Le noyau minimal de maîtrise doit contenir :

\[ \]

puis :

\[ \]

puis :

\[ \]

et enfin :

\[ \]

# 172 — LES QUATRE OBJETS À NE PAS CONFONDRE

### Dérivée

Pour une fonction :

\[ f: \]

on obtient :

\[ f’(x) \]

### Gradient

Pour :

\[ f:^n \]

on obtient :

\[ f(x) \]

### Jacobienne

Pour :

\[ F:<sup>n</sup>m \]

on obtient :

\[ J_F(x) \]

### Hessienne

Pour :

\[ f:^n \]

on obtient :

\[ H_f(x) \]

La hiérarchie conceptuelle est :

Dérivée  
↓  
Dérivées partielles  
↓  
Gradient / Jacobienne  
↓  
Hessienne

# 173 — LA GRANDE CHAÎNE DU MACHINE LEARNING

Le raisonnement complet peut être résumé ainsi :

Données  
↓  
Modèle fθ  
↓  
Prédictions  
↓  
Fonction de perte J(θ)  
↓  
Différentiation  
↓  
Gradient ∇J(θ)  
↓  
Optimiseur  
↓  
Nouvelle valeur de θ  
↓  
Nouvelle prédiction  
↓  
Nouvelle perte  
↓  
Répétition

Mathématiquement :

\[ \_{t+1} = \_t

- _t_ J(\_t) \]

C’est l’une des équations les plus importantes à comprendre pour le Machine Learning.

# 174 — LA GRANDE CHAÎNE DE LA BACKPROPAGATION

Paramètres  
↓  
Opérations  
↓  
Sortie  
↓  
Loss  
↓  
Dérivée locale  
↓  
Règle de chaîne  
↓  
Gradient  
↓  
Paramètres

La backpropagation peut donc être comprise comme :

\[ \]

# 175 — LES ERREURS CONCEPTUELLES À ÉVITER

### Erreur 1

Dire :

« Le gradient est simplement une dérivée. »

Il faut préciser qu’il généralise l’idée de dérivée à une fonction scalaire de plusieurs variables.

### Erreur 2

Dire :

« Gradient nul = minimum. »

Faux en général.

Un point selle peut avoir :

\[ f=0 \]

### Erreur 3

Confondre :

\[ f \]

et :

\[ J_f \]

Les conventions de représentation doivent être précisées.

### Erreur 4

Croire que la backpropagation est une méthode d’optimisation.

La backpropagation **calcule les gradients**.

L’optimiseur utilise ensuite ces gradients pour modifier les paramètres.

### Erreur 5

Croire que Adam calcule le gradient.

Le gradient provient de la différentiation.

Adam est une méthode de mise à jour utilisant les gradients.

# 176 — DIFFÉRENCIER TROIS NIVEAUX

Il faut absolument séparer :

### Niveau 1 — Calcul différentiel

\[ \]

### Niveau 2 — Optimisation

\[ \]

### Niveau 3 — Apprentissage

\[ \]

Ces trois niveaux sont liés mais ne sont pas identiques.

# 177 — SYNTHÈSE DES DOMAINES PRÉCÉDENTS

La progression mathématique construite jusqu’ici peut être résumée ainsi :

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

# 178 — RELATION ENTRE G, H ET I

Ces trois domaines doivent être compris ensemble pour l’IA.

### Probabilités

\[ \]

### Statistiques

\[ \]

### Calcul différentiel

\[ \]

En Machine Learning :

\[ \]

# 179 — CRITÈRE DE MAÎTRISE DU DOMAINE I

Une maîtrise réelle du calcul différentiel appliqué au ML signifie être capable de :

1.  expliquer intuitivement une dérivée ;
2.  calculer des dérivées usuelles ;
3.  appliquer la règle du produit ;
4.  appliquer la règle du quotient ;
5.  appliquer la règle de la chaîne ;
6.  dériver implicitement ;
7.  calculer des dérivées partielles ;
8.  construire un gradient ;
9.  interpréter géométriquement un gradient ;
10. calculer une Jacobienne ;
11. calculer une Hessienne ;
12. interpréter la courbure ;
13. identifier des points critiques ;
14. distinguer minimum, maximum et selle ;
15. comprendre la convexité ;
16. comprendre les contraintes ;
17. utiliser les multiplicateurs de Lagrange ;
18. comprendre la descente de gradient ;
19. expliquer le rôle du learning rate ;
20. comprendre SGD ;
21. comprendre momentum ;
22. comprendre Adam ;
23. comprendre Newton ;
24. comprendre le rôle du second ordre ;
25. comprendre le conditionnement ;
26. expliquer la règle de chaîne dans un réseau neuronal ;
27. reconstruire une backpropagation simple à la main ;
28. comprendre l’autodiff ;
29. distinguer forward mode et reverse mode ;
30. comprendre JVP et VJP ;
31. comprendre vanishing et exploding gradients ;
32. comprendre la relation entre loss et gradient ;
33. vérifier numériquement un gradient ;
34. relier différentiation et optimisation ;
35. relier optimisation et apprentissage ;
36. relier calcul différentiel à simulation et computer graphics.

# 180 — SYNTHÈSE FINALE

Le calcul différentiel ne doit pas être mémorisé comme une simple collection de règles de dérivation.

Son idée fondamentale est :

\[ \]

À une variable :

\[ f(x) f’(x) \]

À plusieurs variables :

\[ f(x) f(x) \]

Pour une transformation vectorielle :

\[ F(x) J_F(x) \]

Pour la courbure :

\[ f(x) H_f(x) \]

Pour l’optimisation :

\[ f(x) x-f(x) \]

Pour les réseaux neuronaux :

\[ \]

Pour le Machine Learning :

\[ \]

Pour la simulation :

\[ \]

Pour la computer graphics :

\[ \]

Le point central à retenir est donc :

**Le calcul différentiel fournit le langage mathématique permettant de mesurer comment un système change localement. L’optimisation transforme cette information en décisions, et le Machine Learning utilise ces décisions répétées pour ajuster automatiquement les paramètres d’un modèle.**

Le domaine I constitue ainsi le pont mathématique direct entre :

\[ \]

et, plus largement :

\[ \]

## FIN DU DOCUMENT I

**Domaine : Calcul différentiel**

**Fonction principale dans la cartographie :** comprendre les variations locales, construire les gradients, analyser la courbure et fournir les mécanismes mathématiques permettant l’optimisation et l’apprentissage.

**Noyau absolument fondamental :**

\[ \]

**Domaine suivant : Domaine J — à définir selon la cartographie mathématique globale du projet.**