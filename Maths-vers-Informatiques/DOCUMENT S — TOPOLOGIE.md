# **DOCUMENT S — TOPOLOGIE**

## **Comprendre la structure des espaces, la continuité, les formes et les invariants pour l’analyse des données et les systèmes informatiques**

**Nature du document :** référence mathématique, conceptuelle, algorithmique et informatique approfondie

**Domaine :** S — Topologie

**Niveau visé :** fondements solides, maîtrise conceptuelle, exploration algorithmique et applications avancées

**Public cible :** étudiant en génie logiciel, développeur, ingénieur en intelligence artificielle, ingénieur en robotique, spécialiste de la vision par ordinateur, de la géométrie computationnelle ou de l’analyse de données.

# **0\. PRÉDISPOSITION D’INTÉGRATION DU DOMAINE**

## **0.1. Mission du domaine**

La topologie étudie les propriétés des espaces qui restent préservées sous certaines déformations continues.

Elle cherche notamment à comprendre :

- Quels objets peuvent être considérés comme proches ou voisins ?
- Quand une transformation est-elle continue ?
- Un espace est-il constitué d’une seule composante ou de plusieurs parties séparées ?
- Un espace est-il compact, et quelles conséquences cela entraîne-t-il ?
- Peut-on déformer continûment un objet vers un autre ?
- Quels trous, cycles ou autres caractéristiques persistent malgré les déformations ?
- Comment reconnaître une structure globale à partir d’observations locales ?
- Comment extraire des propriétés structurelles d’un ensemble de données bruitées ?
- Comment représenter l’espace libre dans lequel un robot peut se déplacer ?
- Comment étudier la forme d’un objet indépendamment de ses dimensions exactes ?

La topologie offre une autre manière de comprendre les données et les systèmes : au lieu de s’intéresser seulement aux valeurs numériques ou aux distances, elle étudie les relations structurelles entre les éléments.

## **0.2. Principe directeur**

La topologie cherche à comprendre quelles propriétés d’un espace survivent lorsque l’on déforme continûment cet espace, sans déchirer ni recoller arbitrairement ses parties.

Une tasse et un beignet sont l’exemple pédagogique classique : dans le cadre de la topologie générale, ils peuvent être considérés comme équivalents si leurs surfaces se déforment continûment l’une vers l’autre en préservant la structure topologique pertinente.

Cet exemple ne signifie pas que leurs géométries, leurs volumes ou leurs distances sont identiques. Il illustre la différence entre la géométrie métrique et la structure topologique.

## **0.3. Pourquoi ce domaine est intéressant en informatique**

La topologie permet d’aborder des problèmes où les propriétés globales sont plus importantes que les valeurs individuelles.

Exemples :

- détecter des groupes de points reliés entre eux ;
- distinguer une boucle d’un amas de points ;
- analyser la structure d’un nuage de données ;
- étudier la connectivité d’un réseau ;
- représenter les configurations accessibles à un robot ;
- analyser la forme de surfaces et d’objets tridimensionnels ;
- détecter des structures persistantes dans des données bruitées ;
- caractériser les transformations qui préservent les relations structurelles.

## **0.4. Ce que la topologie n’est pas**

La topologie ne se réduit pas :

- à la géométrie ;
- au calcul de distances ;
- à la théorie des graphes ;
- à la visualisation de données en trois dimensions ;
- à la détection de clusters ;
- à l’étude des trous dans des objets ;
- à un algorithme particulier de machine learning.

Ces disciplines peuvent utiliser des outils topologiques, mais elles ne sont pas équivalentes.

La topologie générale fournit le langage abstrait. La topologie algébrique associe des structures algébriques à des espaces. La topologie computationnelle développe des méthodes pour représenter et calculer des propriétés topologiques. La TDA exploite ces méthodes pour analyser des données.

# **1\. IDENTITÉ DU DOMAINE**

## **1.1. Définition générale**

La topologie est la branche des mathématiques qui étudie les espaces topologiques, les applications continues et les propriétés qui sont préservées par les homéomorphismes.

Elle s’intéresse notamment à :

- l’ouverture et la fermeture des ensembles ;
- les voisinages ;
- la continuité ;
- la connexité ;
- la compacité ;
- les espaces produits et quotients ;
- les déformations continues ;
- les invariants topologiques ;
- les groupes et autres structures associés aux espaces.

Contrairement à la géométrie euclidienne, la topologie n’exige pas nécessairement une distance précise entre tous les points.

## **1.2. Objet d’étude**

Les objets fondamentaux du domaine sont :

1.  les ensembles munis d’une topologie ;
2.  les ouverts et les fermés ;
3.  les voisinages ;
4.  les applications continues ;
5.  les espaces connexes ;
6.  les espaces compacts ;
7.  les espaces métriques considérés du point de vue topologique ;
8.  les homéomorphismes ;
9.  les homotopies ;
10. les invariants topologiques ;
11. les espaces et complexes utilisés en topologie algébrique ;
12. les représentations discrètes permettant de calculer des propriétés topologiques.

## **1.3. Trois niveaux de lecture**

|     |     |     |
| --- | --- | --- |
| **Niveau** | **Question centrale** | **Exemple** |
| Topologie générale | Quelles propriétés définissent l’espace et la continuité ? | Définir les ouverts et les voisinages |
| Topologie algébrique | Quelles structures algébriques décrivent les propriétés topologiques ? | Groupes fondamentaux, homologie |
| Topologie computationnelle | Comment calculer ou approximer ces propriétés ? | Complexes simpliciaux, homologie persistante |

Ces niveaux sont complémentaires, mais ils ne doivent pas être confondus.

# **2\. LA GRANDE QUESTION DU DOMAINE**

La question centrale est :

**Comment caractériser la structure globale d’un espace à partir des relations entre ses points, et quelles propriétés restent invariantes sous des transformations continues ?**

Cette question se décline en plusieurs problèmes.

### **Question 1 — Voisinage**

Qu’est-ce qui signifie qu’un point est proche d’un autre, lorsque l’on ne dispose pas nécessairement d’une distance numérique ?

### **Question 2 — Continuité**

Comment déterminer si une transformation respecte la structure de voisinage d’un espace ?

### **Question 3 — Connexité**

L’espace forme-t-il une seule composante, ou peut-il être séparé en plusieurs parties disjointes ?

### **Question 4 — Compacité**

L’espace possède-t-il une propriété globale qui garantit, sous certaines hypothèses, que des comportements locaux peuvent être ramenés à un nombre fini de voisinages ?

### **Question 5 — Déformation**

Deux objets peuvent-ils être déformés l’un vers l’autre sans rupture, ou existe-t-il une obstruction topologique ?

### **Question 6 — Invariants**

Quelles propriétés permettent de distinguer deux espaces, ou de montrer qu’ils ne sont pas topologiquement équivalents ?

### **Question 7 — Données**

Quelles structures topologiques peut-on extraire d’un ensemble fini de mesures, même si les données sont bruitées ou incomplètes ?

### **Question 8 — Calcul**

Comment calculer ces propriétés à l’aide d’algorithmes, sans manipuler directement des espaces continus arbitrairement complexes ?

# **3\. POSITIONNEMENT DANS LA PILE MATHÉMATIQUE**

Le domaine S se situe au croisement de l’analyse, de la géométrie, de l’algèbre et du calcul scientifique.

|     |     |     |
| --- | --- | --- |
| **Niveau** | **Domaine** | **Rôle** |
| Fondements | Logique et théorie des ensembles | Définir les objets et les applications |
| Distances | Espaces métriques | Quantifier la proximité |
| Topologie générale | Espaces topologiques | Formaliser ouverts, voisinages et continuité |
| Géométrie | Géométrie différentielle et computationnelle | Étudier les formes et les structures géométriques |
| Algèbre | Algèbre abstraite | Fournir des structures pour décrire des symétries et des transformations |
| Topologie algébrique | Groupes fondamentaux, homologie, cohomologie | Associer des invariants algébriques aux espaces |
| Algorithmique | Topologie computationnelle | Représenter et calculer des propriétés |
| Données | Topological Data Analysis | Étudier la forme des données et les structures persistantes |
| Applications | IA, robotique, vision, réseaux | Exploiter les propriétés topologiques dans des systèmes réels |

## **3.1. Chaîne de raisonnement**

_Donneˊes ou espace→Structure topologique→Proprieˊteˊs→Invariants→Calcul→Interpreˊtation→Application\\text{Données ou espace} \\rightarrow \\text{Structure topologique} \\rightarrow \\text{Propriétés} \\rightarrow \\text{Invariants} \\rightarrow \\text{Calcul} \\rightarrow \\text{Interprétation} \\rightarrow \\text{Application}_

Exemple :

1.  On dispose d’un nuage de points.
2.  On choisit une représentation des voisinages.
3.  On construit un complexe simplicial.
4.  On calcule une homologie.
5.  On étudie les cycles détectés.
6.  On examine leur persistance lorsque le seuil de voisinage varie.
7.  On interprète les structures observées dans le contexte métier.

Le résultat mathématique ne fournit pas automatiquement une interprétation métier : celle-ci dépend des données, des hypothèses et du contexte.

# **4\. ENSEMBLES, DISTANCES ET VOISINAGES**

## **4.1. Ensemble**

Un ensemble _XX_ est une collection d’éléments.

En topologie, les éléments peuvent représenter :

- des points géométriques ;
- des états d’un système ;
- des observations ;
- des configurations possibles ;
- des sommets ou des positions ;
- des objets abstraits.

Un espace topologique n’est pas seulement un ensemble : il est muni d’une structure qui détermine quels sous-ensembles sont ouverts.

## **4.2. Distance**

Une distance sur _XX_ est une fonction :

_d:X×X→R≥0d:X\\times X\\rightarrow\\mathbb{R}\_{\\geq0}_

satisfaisant notamment :

_d(x,y)=0  ⟺  x=yd(x,y)=0\\iff x=y_ _d(x,y)=d(y,x)d(x,y)=d(y,x)_ _d(x,z)≤d(x,y)+d(y,z)d(x,z)\\leq d(x,y)+d(y,z)_

Ces propriétés définissent une métrique.

Une métrique permet de construire une topologie, mais toutes les topologies ne proviennent pas nécessairement d’une métrique.

## **4.3. Boule ouverte**

Dans un espace métrique, une boule ouverte de centre _xx_ et de rayon _r>0r>0_ est :

_B(x,r)={y∈X∣d(x,y)<r}B(x,r)=\\{y\\in X\\mid d(x,y)<r\\}_

Elle représente les points situés à une distance strictement inférieure à _rr_ de _xx_.

Les boules ouvertes servent à définir les voisinages et la continuité dans les espaces métriques.

## **4.4. Voisinage**

Un voisinage d’un point _xx_ est un ensemble qui contient un ouvert contenant _xx_.

L’idée centrale est qu’un point peut être étudié à travers ce qui se passe autour de lui, sans avoir besoin de connaître une distance exacte entre tous les points.

## **4.5. Pourquoi les voisinages importent**

Les voisinages servent à définir :

- les ouverts ;
- la continuité ;
- les limites ;
- l’intérieur et l’adhérence ;
- la convergence ;
- certaines propriétés locales d’un espace.

Dans les applications, le choix du voisinage dépend de la représentation et du problème.

Un voisinage défini par une distance euclidienne ne produit pas nécessairement les mêmes résultats qu’un voisinage défini par une distance géodésique ou une relation de connectivité.

# **5\. ESPACES TOPOLOGIQUES**

## **5.1. Définition**

Un espace topologique est un ensemble _XX_ muni d’une famille _T\\mathcal{T}_ de sous-ensembles de _XX_, appelée topologie, satisfaisant trois axiomes :

1.  _∅\\varnothing_ et _XX_ appartiennent à _T\\mathcal{T}_ ;
2.  toute union, même infinie, d’éléments de _T\\mathcal{T}_ appartient à _T\\mathcal{T}_ ;
3.  toute intersection finie d’éléments de _T\\mathcal{T}_ appartient à _T\\mathcal{T}_.

Les éléments de _T\\mathcal{T}_ sont les ouverts.

On écrit :

_(X,T)(X,\\mathcal{T})_

pour désigner l’espace topologique.

## **5.2. Pourquoi les axiomes sont importants**

Ils garantissent une cohérence dans la manière de combiner les régions considérées comme ouvertes.

Ils fournissent le cadre abstrait dans lequel la continuité peut être définie, même sans distance.

## **5.3. Topologie discrète**

Dans la topologie discrète, tous les sous-ensembles de _XX_ sont ouverts.

_T=P(X)\\mathcal{T}=\\mathcal{P}(X)_

où _P(X)\\mathcal{P}(X)_ désigne l’ensemble des parties de _XX_.

Dans cet espace, chaque point peut être isolé par un ouvert réduit à ce point.

Toute application dont la source est discrète est continue.

## **5.4. Topologie grossière ou indiscrète**

Dans la topologie indiscrète, seuls _∅\\varnothing_ et _XX_ sont ouverts.

_T={∅,X}\\mathcal{T}=\\{\\varnothing,X\\}_

Cette topologie contient très peu d’informations sur les voisinages.

Toute application vers un espace indiscret est continue.

## **5.5. Topologie induite**

Si _A⊆XA\\subseteq X_, la topologie induite sur _AA_ est formée des ensembles :

_A∩U,U∈TA\\cap U,\\qquad U\\in\\mathcal{T}_

Cette construction permet d’étudier un sous-ensemble en conservant la structure héritée de l’espace parent.

Elle est utile pour analyser une surface, un sous-ensemble de points ou une partie d’un espace de configurations.

## **5.6. Topologie produit**

La topologie produit permet de construire une topologie sur un produit cartésien d’espaces.

Elle est importante pour étudier les espaces de plusieurs variables et les systèmes dont l’état est composé de plusieurs éléments.

Exemple : l’espace des positions et orientations d’un robot peut être construit à partir de plusieurs espaces de configuration, même si la structure exacte dépend du robot considéré.

## **5.7. Topologie quotient**

La topologie quotient formalise une construction dans laquelle certains éléments sont identifiés selon une relation d’équivalence.

Elle permet de construire un nouvel espace à partir d’un espace existant.

Cette idée est utile pour comprendre certaines surfaces, les espaces de configurations et les constructions topologiques.

## **5.8. Espace séparé**

Un espace topologique est séparé, ou de Hausdorff, si deux points distincts peuvent être contenus dans deux ouverts disjoints.

Cette propriété garantit une forme de distinction topologique entre les points.

Elle joue un rôle important dans de nombreux théorèmes de topologie générale.

## **5.9. Applications informatiques**

Les espaces topologiques peuvent servir à formaliser :

- des espaces de configurations ;
- des données organisées par voisinages ;
- des espaces de transformations ;
- des espaces de formes ;
- des espaces de solutions ;
- des structures continues dans les systèmes de modélisation.

En pratique, une application informatique utilise généralement une représentation finie ou calculable de l’espace étudié.

# **6\. OUVERTS, FERMÉS ET PROPRIÉTÉS LOCALES**

## **6.1. Ensemble ouvert**

Un ensemble est ouvert s’il appartient à la topologie de l’espace.

Dans _R\\mathbb{R}_ muni de sa topologie usuelle, l’intervalle :

_(0,1)(0,1)_

est ouvert.

L’ouverture est une notion topologique, et non simplement une question de représentation graphique.

## **6.2. Ensemble fermé**

Un ensemble est fermé si son complémentaire est ouvert.

Dans _R\\mathbb{R}_, l’intervalle :

_\[0,1\]\[0,1\]_

est fermé.

Un ensemble peut être à la fois ouvert et fermé, ou ne posséder aucune de ces deux propriétés.

Dans la topologie discrète, tous les ensembles sont à la fois ouverts et fermés.

## **6.3. Intérieur**

L’intérieur de _AA_, noté _Int⁡(A)\\operatorname{Int}(A)_, est le plus grand ouvert contenu dans _AA_.

Il rassemble les points autour desquels on peut trouver un voisinage entièrement inclus dans _AA_.

## **6.4. Adhérence**

L’adhérence de _AA_, notée _A‾\\overline{A}_, est le plus petit fermé contenant _AA_.

Elle contient _AA_ ainsi que les points dont chaque voisinage rencontre _AA_.

## **6.5. Frontière**

La frontière de _AA_ peut être définie par :

_∂A=A‾∖Int⁡(A)\\partial A=\\overline{A}\\setminus\\operatorname{Int}(A)_

Elle sépare, au sens topologique, l’intérieur de l’ensemble de son extérieur.

Cette notion est importante pour l’analyse de formes et de régions, mais la frontière topologique ne coïncide pas toujours avec une frontière visuellement évidente dans une représentation numérique.

## **6.6. Densité**

Un sous-ensemble _AA_ est dense dans _XX_ si :

_A‾=X\\overline{A}=X_

Autrement dit, chaque ouvert non vide de _XX_ rencontre _AA_.

Les rationnels sont denses dans les réels pour la topologie usuelle.

Cette notion montre qu’un sous-ensemble peut être très riche du point de vue topologique sans contenir tous les points de l’espace.

## **6.7. Pourquoi ces notions importent**

Les ouverts, fermés, intérieurs et adhérences interviennent dans :

- la définition de la continuité ;
- l’étude des limites ;
- l’analyse des frontières ;
- la modélisation de régions ;
- la compréhension de la densité des observations ;
- les théorèmes de compacité.

# **7\. CONTINUITÉ**

## **7.1. Définition topologique**

Soient _XX_ et _YY_ deux espaces topologiques.

Une application :

_f:X→Yf:X\\rightarrow Y_

est continue si, pour tout ouvert _VV_ de _YY_, son image réciproque :

_f−1(V)f^{-1}(V)_

est ouverte dans _XX_.

La préimage est définie par :

_f−1(V)={x∈X∣f(x)∈V}f^{-1}(V)=\\{x\\in X\\mid f(x)\\in V\\}_

Il ne faut pas confondre cette préimage avec l’inverse d’une fonction, qui n’existe pas nécessairement.

## **7.2. Continuité métrique**

Pour les espaces métriques, la continuité en un point _xx_ peut s’exprimer avec la définition _ε\\varepsilon_\-_δ\\delta_.

Pour tout _ε>0\\varepsilon>0_, il existe _δ>0\\delta>0_ tel que :

_dX(x,y)<δ⇒dY(f(x),f(y))<εd_X(x,y)<\\delta \\Rightarrow d_Y(f(x),f(y))<\\varepsilon_

Cette définition formalise l’idée qu’une petite variation de l’entrée peut être associée à une variation arbitrairement petite de la sortie, au voisinage du point.

## **7.3. Continuité et voisinages**

La continuité exprime la préservation des relations de voisinage.

Une transformation continue ne crée pas de rupture topologique au sens de cette définition.

Elle peut néanmoins modifier les distances, les angles, les longueurs et les volumes.

## **7.4. Homéomorphisme**

Un homéomorphisme est une bijection continue dont l’inverse est également continu.

Deux espaces homéomorphes sont équivalents du point de vue topologique.

Ils peuvent avoir des formes géométriques très différentes.

L’homéomorphisme est donc une notion plus forte qu’une simple bijection ou qu’une application continue.

## **7.5. Invariance topologique**

Une propriété est topologique si elle est préservée par les homéomorphismes.

Exemples de propriétés topologiques :

- la connexité ;
- la compacité ;
- le nombre de composantes connexes ;
- certaines caractéristiques homologiques.

Les longueurs et les angles ne sont pas des invariants topologiques.

## **7.6. Continuité et calcul numérique**

En informatique, une fonction continue sur le papier peut être approchée par un algorithme numérique qui introduit des erreurs.

Il faut donc distinguer :

- la continuité mathématique ;
- la stabilité numérique ;
- la sensibilité aux perturbations ;
- la précision des calculs ;
- la robustesse de l’implémentation.

Ces notions sont liées, mais non équivalentes.

# **8\. CONNEXITÉ**

## **8.1. Définition**

Un espace topologique est connexe s’il ne peut pas être décomposé en deux ouverts disjoints non vides dont l’union est l’espace entier.

Intuitivement, un espace connexe ne possède pas de séparation topologique en deux parties ouvertes disjointes.

Cette définition est plus générale que la possibilité de tracer un chemin entre deux points.

## **8.2. Connexité par arcs**

Un espace est connexe par arcs si, pour toute paire de points _x,yx,y_, il existe une application continue :

_γ:\[0,1\]→X\\gamma:\[0,1\]\\rightarrow X_

telle que :

_γ(0)=x,γ(1)=y\\gamma(0)=x,\\qquad \\gamma(1)=y_

Cette application représente un chemin continu reliant les deux points.

Tout espace connexe par arcs est connexe, mais la réciproque n’est pas toujours vraie.

## **8.3. Composantes connexes**

Une composante connexe est un sous-espace connexe maximal.

Un espace peut contenir plusieurs composantes connexes.

Le nombre de composantes est souvent une première caractéristique topologique utile pour analyser une structure.

## **8.4. Exemples**

- Un intervalle réel est connexe.
- Deux disques séparés dans le plan forment un espace à deux composantes connexes.
- Un graphe possède des composantes connexes déterminées par les chemins entre ses sommets.
- Une surface peut être connexe tout en contenant des trous.

La connexité ne suffit donc pas à décrire toute la structure d’un espace.

## **8.5. Connexité et réseaux**

Dans un réseau représenté par un graphe, la connexité permet de déterminer quelles entités peuvent communiquer par un chemin.

Applications :

- diagnostic de réseaux ;
- analyse de communautés ;
- connectivité de systèmes distribués ;
- analyse de dépendances ;
- disponibilité des services.

Attention : la connexité d’un graphe est une propriété discrète qui ne capture pas nécessairement toute la topologie d’un espace continu sous-jacent.

## **8.6. Connexité et TDA**

Dans un nuage de points, on peut relier deux points lorsque leur distance est inférieure à un seuil.

En faisant varier ce seuil, des composantes apparaissent et fusionnent.

Le suivi de ces événements constitue l’un des aspects de l’homologie persistante de dimension zéro.

Cette approche permet d’étudier la structure des données à plusieurs échelles.

# **9\. COMPACITÉ**

## **9.1. Définition**

Un espace topologique est compact si tout recouvrement de l’espace par des ouverts admet un sous-recouvrement fini.

Autrement dit, si une famille d’ouverts recouvre l’espace entier, on peut en sélectionner un nombre fini qui suffit encore à le recouvrir.

Cette définition est générale et ne dépend pas nécessairement d’une distance.

## **9.2. Intuition**

La compacité exprime une propriété globale de finitude au niveau des recouvrements ouverts.

Elle permet, sous des hypothèses appropriées, de transformer certaines affirmations locales en conclusions globales.

Elle ne signifie pas que l’espace contient un nombre fini de points.

## **9.3. Théorème de Heine–Borel**

Dans _Rn\\mathbb{R}^n_ muni de la topologie usuelle, un ensemble est compact si et seulement s’il est fermé et borné.

Ce résultat est propre aux espaces euclidiens de dimension finie dans leur topologie usuelle. Il ne doit pas être généralisé sans précaution à tout espace topologique.

## **9.4. Théorème des valeurs extrêmes**

Une fonction continue à valeurs réelles définie sur un espace compact non vide atteint son minimum et son maximum.

Ce résultat est particulièrement important en optimisation.

Il permet de garantir l’existence d’une solution optimale dans de nombreuses situations, sans garantir nécessairement qu’on sache la calculer efficacement.

## **9.5. Compacité et optimisation**

La compacité est utile lorsqu’on veut démontrer :

- l’existence d’un minimum ;
- l’existence d’un maximum ;
- l’existence d’une solution à certains problèmes ;
- certaines propriétés de convergence.

Il faut distinguer l’existence mathématique d’une solution de la possibilité de la calculer numériquement.

## **9.6. Compacité en informatique**

Les applications peuvent concerner :

- les espaces de paramètres bornés ;
- les domaines de recherche ;
- la géométrie computationnelle ;
- la planification ;
- les preuves d’existence de solutions ;
- certains problèmes de modélisation.

Dans les systèmes numériques, les domaines utilisés sont souvent des approximations discrètes d’espaces compacts.

# **10\. HOMOTOPIE ET DÉFORMATIONS**

## **10.1. Intuition**

L’homotopie étudie les déformations continues d’applications.

Deux objets peuvent avoir des représentations géométriques différentes tout en conservant certaines propriétés de déformation.

Il faut distinguer :

- l’homéomorphisme, qui exprime une équivalence topologique complète ;
- l’homotopie, qui exprime une déformation continue entre applications ;
- l’équivalence d’homotopie, qui est une relation d’équivalence plus faible que l’homéomorphisme.

## **10.2. Définition d’une homotopie**

Soient _f,g:X→Yf,g:X\\rightarrow Y_ deux applications continues.

Une homotopie entre _ff_ et _gg_ est une application continue :

_H:X×\[0,1\]→YH:X\\times\[0,1\]\\rightarrow Y_

telle que :

_H(x,0)=f(x)H(x,0)=f(x)_

et :

_H(x,1)=g(x)H(x,1)=g(x)_

pour tout _x∈Xx\\in X_.

On peut interpréter _H(x,t)H(x,t)_ comme la position de l’image de _xx_ au cours d’une déformation paramétrée par _tt_.

## **10.3. Homotopie de chemins**

Deux chemins ayant les mêmes extrémités sont homotopes lorsque l’un peut être déformé continûment en l’autre, tout en respectant les contraintes imposées aux extrémités.

Dans un espace contenant des trous, deux chemins reliant les mêmes points peuvent appartenir à des classes d’homotopie différentes.

## **10.4. Contractibilité**

Un espace est contractile s’il est homotope à un point.

Intuitivement, il peut être déformé continûment jusqu’à un point dans le cadre de la définition topologique appropriée.

Un disque est contractile.

Un cercle n’est pas contractile.

## **10.5. Équivalence d’homotopie**

Deux espaces _XX_ et _YY_ sont homotopiquement équivalents lorsqu’il existe des applications continues entre eux dont les compositions sont homotopes aux applications identités correspondantes.

Cette notion permet de simplifier certains espaces tout en conservant des informations topologiques importantes.

## **10.6. Pourquoi l’homotopie importe**

Elle permet :

- de classifier des chemins ;
- d’étudier les boucles ;
- d’analyser les trous ;
- de simplifier des espaces ;
- de comprendre des obstacles en robotique ;
- de distinguer certaines configurations impossibles à déformer l’une vers l’autre.

# **11\. INVARIANTS TOPOLOGIQUES**

## **11.1. Définition**

Un invariant topologique est une propriété ou une quantité qui reste identique lorsque deux espaces sont homéomorphes.

Les invariants permettent de distinguer certaines structures.

Cependant, deux espaces ayant le même invariant ne sont pas nécessairement homéomorphes. Un invariant particulier peut être insuffisant pour les distinguer.

## **11.2. Exemples d’invariants**

- le nombre de composantes connexes ;
- le groupe fondamental ;
- les groupes d’homologie ;
- les nombres de Betti ;
- la caractéristique d’Euler, pour les espaces auxquels elle s’applique ;
- certaines propriétés de séparation ;
- certaines propriétés de compacité.

## **11.3. Invariants versus mesures géométriques**

Les longueurs, les angles et les volumes dépendent de la géométrie et de la métrique.

Ils ne sont pas, en général, préservés par un homéomorphisme.

Les invariants topologiques s’intéressent à des propriétés plus structurelles.

Cette distinction permet de choisir le bon outil :

- une distance est adaptée à la proximité quantitative ;
- un invariant topologique peut être adapté à la structure globale.

## **11.4. Invariants et données**

Dans une analyse de données, les invariants peuvent révéler des structures globales qui ne sont pas évidentes dans une projection visuelle.

Par exemple, un nuage de points peut sembler dispersé en deux dimensions tout en échantillonnant une structure ayant une boucle persistante.

La validité de l’interprétation dépend néanmoins de la qualité des données, de la méthode de construction et des échelles considérées.

# **12\. TOPOLOGIE ALGÉBRIQUE**

## **12.1. Définition**

La topologie algébrique associe des structures algébriques à des espaces topologiques afin d’étudier leurs propriétés.

Elle permet de transformer certains problèmes topologiques en problèmes portant sur des groupes, des espaces vectoriels ou des applications algébriques.

L’idée centrale est de construire des invariants calculables qui conservent des informations sur la structure de l’espace.

## **12.2. Groupe fondamental**

Le groupe fondamental d’un espace, noté :

_π1(X,x0)\\pi_1(X,x_0)_

étudie les classes d’homotopie de boucles basées en un point _x0x_0_, avec une opération de composition adaptée.

Il permet de distinguer certaines structures que la seule connexité ne permet pas de différencier.

Par exemple, le cercle possède un groupe fondamental isomorphe à _Z\\mathbb{Z}_, tandis que le disque possède un groupe fondamental trivial.

## **12.3. Homologie**

L’homologie associe à un espace une suite de groupes abéliens ou, dans une version vectorielle, d’espaces vectoriels.

Elle permet d’étudier différentes dimensions de structures topologiques :

- composantes ;
- cycles ;
- surfaces et cavités dans les cadres appropriés.

Dans les espaces simples, l’homologie est souvent plus directement calculable que le groupe fondamental.

## **12.4. Nombres de Betti**

Les nombres de Betti _βk\\beta_k_ mesurent, dans les cadres usuels où ils sont définis, le nombre de caractéristiques indépendantes de dimension _kk_ détectées par l’homologie à coefficients dans un corps.

Interprétation intuitive dans des exemples classiques :

- _β0\\beta_0_ : nombre de composantes connexes ;
- _β1\\beta_1_ : nombre de cycles indépendants ;
- _β2\\beta_2_ : nombre de cavités de dimension deux, dans les situations tridimensionnelles usuelles.

Ces interprétations sont utiles, mais leur signification précise dépend du complexe et de la théorie d’homologie utilisée.

## **12.5. Cohomologie**

La cohomologie est une théorie complémentaire à l’homologie.

Elle fournit des structures algébriques supplémentaires et peut révéler des informations qui ne sont pas résumées par les seuls nombres de Betti.

Elle intervient dans des domaines plus avancés de la topologie, de la géométrie et de certaines approches computationnelles.

## **12.6. Caractéristique d’Euler**

Pour un complexe fini approprié, la caractéristique d’Euler peut s’écrire :

_χ=∑k≥0(−1)kβk\\chi=\\sum_{k\\geq0}(-1)^k\\beta_k_

Elle peut aussi être calculée à partir du nombre de cellules ou de simplexes de chaque dimension dans les cadres où la formule est applicable.

Cette quantité condense plusieurs informations topologiques en un invariant numérique.

## **12.7. Limites des invariants algébriques**

Un invariant peut distinguer deux espaces sans permettre de les classifier complètement.

Deux espaces non homéomorphes peuvent partager les mêmes nombres de Betti, la même caractéristique d’Euler ou d’autres invariants.

Il est donc important de comprendre ce qu’un invariant capture et ce qu’il laisse de côté.

# **13\. COMPLEXES SIMPLICIAUX ET REPRÉSENTATIONS DISCRÈTES**

## **13.1. Pourquoi discrétiser ?**

Les données informatiques sont souvent finies, alors que les espaces étudiés peuvent être continus.

Pour calculer des propriétés topologiques, on construit donc des objets combinatoires finis qui représentent une partie de la structure de l’espace.

Les complexes simpliciaux sont l’un des outils majeurs de cette représentation.

## **13.2. Simplexes**

Les simplexes sont les éléments de base d’un complexe simplicial.

- Un simplexe de dimension _00_ est un sommet.
- Un simplexe de dimension _11_ est une arête.
- Un simplexe de dimension _22_ est un triangle rempli.
- Un simplexe de dimension _33_ est un tétraèdre rempli.

Il ne faut pas confondre un triangle rempli avec son seul contour : cette différence modifie les propriétés topologiques.

## **13.3. Complexe simplicial**

Un complexe simplicial est une collection de simplexes telle que :

- toute face d’un simplexe appartient au complexe ;
- l’intersection de deux simplexes est vide ou correspond à une face commune, dans la définition géométrique usuelle.

Cette structure permet de construire des matrices de bord et de calculer des groupes d’homologie.

## **13.4. Complexe de Vietoris–Rips**

À partir d’un nuage de points muni d’une distance et d’un seuil _ε\\varepsilon_, on construit un complexe de Vietoris–Rips.

Les points sont reliés lorsque leur distance satisfait le seuil. Les simplexes de dimensions supérieures sont ajoutés lorsque toutes les paires de sommets satisfont la condition de voisinage correspondante.

Cette construction est particulièrement importante en analyse topologique des données.

## **13.5. Complexe de Čech**

Le complexe de Čech est construit à partir des intersections de boules autour des points.

Il est lié à l’union de boules et fournit un autre moyen de représenter la topologie d’un nuage de points.

Sous des hypothèses appropriées, il possède des liens théoriques avec l’union de ces boules.

## **13.6. Autres représentations**

Selon les données et le problème, on peut utiliser :

- des graphes ;
- des maillages ;
- des complexes cellulaires ;
- des complexes cubiques ;
- des complexes de voisinage ;
- des triangulations ;
- des représentations symboliques.

Le choix de représentation influence les propriétés calculées, les coûts et les erreurs possibles.

# **14\. TOPOLOGICAL DATA ANALYSIS**

## **14.1. Définition**

La _Topological Data Analysis_ (TDA), ou analyse topologique des données, regroupe des méthodes qui exploitent les concepts de topologie pour analyser la structure des données.

Elle vise notamment à identifier des caractéristiques structurelles telles que :

- les composantes ;
- les cycles ;
- les cavités ;
- les structures présentes à plusieurs échelles ;
- les changements topologiques sous variation de paramètres.

## **14.2. Principe général**

Un pipeline typique peut être résumé ainsi :

_Donneˊes→Voisinages→Filtration→Homologie→Persistance→Interpreˊtation\\text{Données} \\rightarrow \\text{Voisinages} \\rightarrow \\text{Filtration} \\rightarrow \\text{Homologie} \\rightarrow \\text{Persistance} \\rightarrow \\text{Interprétation}_

Chaque étape comporte des choix qui doivent être justifiés.

## **14.3. Étape 1 — Préparation des données**

Les données peuvent être :

- des points dans un espace métrique ;
- des mesures issues de capteurs ;
- des représentations d’images ;
- des observations temporelles ;
- des données de graphes ;
- des vecteurs de caractéristiques.

Il faut comprendre les variables, les unités, les valeurs manquantes et les transformations appliquées.

Une mauvaise représentation des données peut produire une structure topologique artificielle.

## **14.4. Étape 2 — Construction des voisinages**

On choisit une règle de proximité :

- distance euclidienne ;
- distance géodésique ;
- distance dans un espace de caractéristiques ;
- distance définie par le domaine métier ;
- relation de voisinage particulière.

Le choix de la distance peut changer la structure détectée.

## **14.5. Étape 3 — Filtration**

Une filtration est une famille croissante de complexes :

_K0⊆K1⊆K2⊆⋯K_0\\subseteq K_1\\subseteq K_2\\subseteq\\cdots_

À mesure que le paramètre augmente, de nouveaux simplexes apparaissent.

Les structures topologiques peuvent apparaître, fusionner ou disparaître.

La filtration permet d’étudier les données à plusieurs échelles.

## **14.6. Étape 4 — Homologie persistante**

L’homologie persistante suit la naissance et la disparition de classes d’homologie au cours d’une filtration.

Une structure est dite persistante si elle reste présente sur une plage suffisamment importante du paramètre choisi.

La persistance constitue une mesure de stabilité relative à cette filtration, et non une preuve automatique que la structure est pertinente pour le domaine métier.

## **14.7. Diagramme de persistance**

Un diagramme de persistance représente les classes par leurs paramètres de naissance et de mort.

Les points proches de la diagonale correspondent à des durées de vie faibles dans la filtration considérée.

Les points éloignés de la diagonale correspondent à des durées de vie plus importantes.

L’interprétation des diagrammes dépend de l’échelle, du bruit, de la construction du complexe et du contexte des données.

## **14.8. Code-barres de persistance**

Le code-barres représente chaque classe par un intervalle entre sa naissance et sa disparition.

Cette visualisation facilite la comparaison de structures persistantes.

## **14.9. Pourquoi la persistance est utile**

Une caractéristique topologique observée à une seule échelle peut être causée par le bruit ou par un choix arbitraire de seuil.

L’étude de plusieurs échelles aide à distinguer des structures robustes de structures éphémères.

Cela ne dispense pas de validation statistique ou métier, mais fournit un outil supplémentaire.

## **14.10. Limites de la TDA**

La TDA peut être coûteuse en temps et en mémoire.

Les résultats dépendent :

- de la distance ;
- de la normalisation ;
- de la filtration ;
- du type de complexe ;
- du niveau d’homologie ;
- de la densité des observations ;
- de la présence de bruit ;
- des paramètres de calcul.

La TDA doit donc être considérée comme une famille de méthodes analytiques, et non comme un détecteur universel de structure.

# **15\. APPLICATION À L’ANALYSE DE DONNÉES**

## **15.1. Au-delà des statistiques classiques**

Les méthodes statistiques classiques étudient notamment les distributions, les moyennes, les variances et les relations entre variables.

La TDA peut compléter ces analyses en étudiant certaines propriétés globales de la forme des données.

Les deux approches ne sont pas concurrentes par défaut.

## **15.2. Détection de structures**

La TDA peut contribuer à identifier :

- plusieurs composantes ;
- des boucles dans un espace de caractéristiques ;
- des structures persistantes ;
- des différences entre groupes de données ;
- des changements de structure entre populations.

Une boucle dans un nuage de points n’a toutefois pas nécessairement une signification métier directe.

## **15.3. Analyse de données de grande dimension**

Des données de grande dimension peuvent être échantillonnées sur une structure de dimension intrinsèque plus faible.

La topologie peut fournir des indices sur la structure de cet espace, sous certaines hypothèses.

Elle ne garantit pas à elle seule la récupération exacte de la variété ou de la structure sous-jacente.

## **15.4. Détection d’anomalies**

Une structure topologique inhabituelle peut être un signal d’intérêt.

Exemples :

- apparition de composantes nouvelles ;
- changement dans les caractéristiques persistantes ;
- modification de la structure d’un ensemble de capteurs ;
- changement de topologie dans des données de réseau.

Une anomalie topologique ne correspond pas nécessairement à une anomalie statistique, et inversement.

## **15.5. Comparaison de groupes**

On peut comparer des diagrammes de persistance ou des résumés topologiques entre différents ensembles de données.

Il faut toutefois contrôler :

- les tailles d’échantillon ;
- les distributions ;
- les distances ;
- les paramètres de calcul ;
- les effets de normalisation.

## **15.6. Applications potentielles**

- analyse de données biomédicales ;
- données de capteurs ;
- analyse de comportements ;
- séries temporelles ;
- surveillance de systèmes ;
- comparaison de représentations apprises ;
- exploration de données scientifiques.

La pertinence réelle doit être établie par comparaison avec des méthodes de référence.

# **16\. APPLICATION À LA GÉOMÉTRIE COMPUTATIONNELLE**

## **16.1. Rôle de la topologie**

La géométrie computationnelle développe des algorithmes pour manipuler des objets géométriques.

La topologie intervient lorsque l’on veut préserver ou calculer :

- la connexité ;
- les composantes ;
- les frontières ;
- les trous ;
- les relations d’adjacence ;
- la cohérence des maillages.

## **16.2. Maillages**

Un maillage représente une surface ou un volume à l’aide d’éléments discrets.

Les maillages sont utilisés en :

- simulation ;
- rendu 3D ;
- modélisation ;
- conception assistée par ordinateur ;
- vision par ordinateur ;
- calcul scientifique.

Une erreur topologique dans un maillage peut produire des surfaces non-manifold, des trous involontaires ou des connexions incorrectes.

## **16.3. Topologie d’un maillage**

Les vérifications possibles comprennent :

- nombre de composantes ;
- nombre de sommets, arêtes et faces ;
- cohérence des adjacences ;
- détection de bords ;
- détection de faces ou d’arêtes non-manifold ;
- cohérence des orientations ;
- caractéristique d’Euler, dans les cadres appropriés.

Ces vérifications ne remplacent pas toutes les validations géométriques.

## **16.4. Calcul de frontières**

La topologie peut aider à distinguer les régions intérieures, les frontières et les parties séparées d’une représentation.

Dans les données discrètes, ces notions dépendent de la construction du maillage et de la représentation adoptée.

## **16.5. Applications**

- reconstruction de surfaces ;
- nettoyage de maillages ;
- segmentation d’objets ;
- analyse de modèles 3D ;
- détection de trous ;
- réparation de géométries ;
- traitement de données issues de scanners.

# **17\. APPLICATION À LA ROBOTIQUE**

## **17.1. Espace de configuration**

L’espace de configuration d’un robot décrit l’ensemble des configurations possibles de ses articulations ou de ses paramètres.

Il peut inclure :

- des positions ;
- des orientations ;
- des angles articulaires ;
- des contraintes mécaniques ;
- des configurations interdites.

Sa structure topologique influence les possibilités de déplacement.

## **17.2. Espace libre**

L’espace libre correspond à l’ensemble des configurations qui ne provoquent pas de collision avec les obstacles et satisfont les contraintes retenues.

La planification de mouvement consiste notamment à trouver un chemin continu dans cet espace libre entre une configuration initiale et une configuration finale.

## **17.3. Obstacles topologiques**

Des obstacles peuvent séparer des régions de l’espace libre ou créer des classes de chemins différentes.

Deux chemins reliant les mêmes configurations peuvent être non homotopes s’ils contournent des obstacles de manières différentes.

## **17.4. Planification de mouvement**

La topologie aide à comprendre :

- l’existence de chemins ;
- les composantes de l’espace libre ;
- les classes de chemins ;
- les obstacles ;
- certaines limites des stratégies de planification.

Elle ne remplace pas les algorithmes de planification, les contraintes dynamiques ni la vérification des collisions.

## **17.5. Représentations discrètes**

Les systèmes pratiques utilisent souvent :

- des grilles ;
- des graphes de configurations ;
- des cartes topologiques ;
- des maillages ;
- des échantillonnages aléatoires ;
- des graphes de visibilité.

Ces représentations doivent préserver autant que possible les propriétés pertinentes de l’espace réel.

## **17.6. Applications**

- robots mobiles ;
- bras robotisés ;
- navigation autonome ;
- planification de trajectoires ;
- manipulation d’objets ;
- exploration d’environnements ;
- cartographie topologique.

# **18\. APPLICATION À LA VISION PAR ORDINATEUR**

## **18.1. Topologie des images**

Une image numérique peut être considérée comme un ensemble de pixels auxquels sont associées des valeurs.

Selon la représentation, on peut étudier :

- les composantes d’une région ;
- les trous dans une segmentation ;
- les frontières ;
- les adjacences ;
- la topologie des surfaces reconstruites.

La connectivité des pixels dépend de la convention choisie, par exemple la connectivité à quatre ou à huit voisins dans une image bidimensionnelle.

## **18.2. Segmentation**

La segmentation partitionne une image en régions.

La topologie peut aider à vérifier :

- si une région est fragmentée ;
- si un objet contient des trous ;
- si des régions se touchent ;
- si une segmentation a créé des connexions involontaires.

## **18.3. Reconstruction 3D**

Les méthodes de reconstruction produisent des nuages de points, des surfaces ou des volumes.

L’analyse topologique peut contribuer à détecter :

- des trous ;
- des composantes séparées ;
- des défauts de maillage ;
- des incohérences structurelles.

Il faut distinguer les trous topologiques des trous dus à une absence d’observations ou à un défaut de reconstruction.

## **18.4. Reconnaissance de formes**

Les invariants topologiques peuvent fournir des caractéristiques complémentaires à celles qui décrivent la texture, la couleur ou la géométrie.

Ils sont utiles lorsque certaines propriétés structurelles doivent être préservées malgré des déformations.

Ils ne garantissent pas à eux seuls une bonne reconnaissance d’objets.

## **18.5. Apprentissage profond**

Des outils topologiques peuvent être utilisés pour analyser des représentations latentes ou pour introduire certaines contraintes dans l’apprentissage.

Il faut cependant distinguer :

- l’analyse topologique d’un espace latent ;
- l’utilisation d’invariants topologiques comme caractéristiques ;
- les pertes d’apprentissage conçues pour préserver certaines structures ;
- les garanties mathématiques réellement démontrées.

# **19\. APPLICATION AUX RÉSEAUX**

## **19.1. Topologie d’un réseau**

En informatique, la topologie d’un réseau désigne souvent son organisation en nœuds et en liens.

Cette utilisation du terme correspond à une représentation discrète de la connectivité, fréquemment étudiée par la théorie des graphes.

Elle ne se confond pas automatiquement avec la topologie mathématique d’un espace continu.

## **19.2. Réseaux informatiques**

Les questions typiques comprennent :

- quels nœuds sont connectés ;
- quelles composantes peuvent communiquer ;
- quelles coupures séparent le réseau ;
- comment les connexions évoluent ;
- quels chemins restent accessibles après une panne.

Ces problèmes sont généralement modélisés par des graphes, mais des outils topologiques plus avancés peuvent compléter leur analyse.

## **19.3. Réseaux dynamiques**

Un réseau peut évoluer dans le temps.

On peut étudier la naissance et la disparition de connexions ou de composantes, et parfois analyser ces changements à l’aide de constructions de persistance.

La représentation doit tenir compte du caractère temporel et potentiellement dirigé des relations.

## **19.4. Réseaux neuronaux et données relationnelles**

Dans les graphes de données, la topologie relationnelle influence la diffusion de l’information, la propagation des messages et la structure des voisinages.

Les méthodes de topologie algébrique peuvent parfois fournir des informations supplémentaires sur la structure globale.

Toutefois, une représentation par graphe, une analyse de graphe et une TDA sont des approches différentes.

# **20\. APPLICATION À LA MODÉLISATION**

## **20.1. Modéliser un espace**

La topologie permet de représenter des relations structurelles qui ne dépendent pas uniquement des distances.

Elle est utile pour modéliser :

- des espaces de configurations ;
- des espaces de paramètres ;
- des surfaces ;
- des relations de proximité ;
- des transformations continues ;
- des espaces de solutions.

## **20.2. Modèles continus et discrets**

Un modèle peut être défini dans un espace continu, puis discrétisé pour être calculé.

Le passage au discret peut introduire :

- des pertes de connectivité ;
- des connexions artificielles ;
- des trous involontaires ;
- des approximations de frontières ;
- des erreurs d’échantillonnage.

Il faut vérifier quelles propriétés sont préservées par la discrétisation.

## **20.3. Modélisation scientifique**

Les outils topologiques peuvent intervenir dans :

- la simulation physique ;
- la reconstruction de surfaces ;
- l’analyse de formes ;
- la modélisation de systèmes dynamiques ;
- l’étude de configurations accessibles ;
- l’analyse de données scientifiques.

La topologie fournit un langage structurel, tandis que les modèles physiques et les équations déterminent d’autres aspects du système.

# **21\. THÉORÈMES ET RÉSULTATS FONDAMENTAUX**

## **21.1. Théorème des valeurs extrêmes**

Une fonction continue à valeurs réelles définie sur un espace compact non vide atteint son minimum et son maximum.

**Usage :** établir l’existence d’optima dans certains problèmes d’analyse et d’optimisation.

## **21.2. Image continue d’un espace connexe**

L’image continue d’un espace connexe est connexe.

**Usage :** démontrer qu’une transformation continue ne peut pas séparer l’image en deux parties topologiquement disjointes dans les conditions du théorème.

## **21.3. Image continue d’un espace compact**

L’image continue d’un espace compact est compacte.

**Usage :** transférer une propriété globale d’un espace vers son image.

## **21.4. Compacité et espaces de Hausdorff**

Dans un espace de Hausdorff, tout sous-ensemble compact est fermé.

Cette propriété ne doit pas être appliquée sans l’hypothèse de séparation appropriée.

## **21.5. Invariance par homéomorphisme**

Les espaces homéomorphes partagent les propriétés topologiques.

Cela justifie l’utilisation des invariants pour comparer des espaces indépendamment de leur représentation géométrique.

## **21.6. Théorème de Brouwer sur le point fixe**

Toute application continue d’une boule fermée de dimension finie dans elle-même possède un point fixe.

Ce résultat possède des applications importantes en analyse, en équations et en économie mathématique.

Il exige des hypothèses précises : il ne s’applique pas à toute application ni à tout espace.

## **21.7. Théorème de Borsuk–Ulam**

Dans sa formulation classique, toute application continue de la sphère _SnS^n_ vers _Rn\\mathbb{R}^n_ envoie au moins une paire de points antipodaux sur la même valeur.

Ce théorème illustre la puissance des arguments topologiques dans des problèmes d’apparence géométrique ou combinatoire.

## **21.8. Théorème de classification des surfaces compactes**

Les surfaces topologiques compactes connexes possèdent une classification structurelle selon leur orientabilité et leur genre, sous les hypothèses usuelles de la théorie des surfaces.

Ce résultat est un exemple important de classification par invariants et propriétés topologiques.

## **21.9. Théorème de Nerve**

Le théorème du nerf relie, sous des hypothèses adaptées sur une couverture et ses intersections, la topologie de l’union des ensembles à celle du complexe de nerf correspondant.

Il fournit un lien théorique important entre espaces continus et complexes simpliciaux, notamment dans certaines méthodes de TDA.

## **21.10. Pourquoi les théorèmes importent en informatique**

Un théorème topologique peut permettre de :

- démontrer l’existence d’une solution ;
- établir qu’une transformation conserve une propriété ;
- distinguer deux classes d’espaces ;
- justifier une représentation discrète ;
- comprendre les limites d’un algorithme ;
- concevoir une méthode de calcul plus fiable.

# **22\. TOPOLOGIE COMPUTATIONNELLE ET ALGORITHMES**

## **22.1. Objectif**

La topologie computationnelle développe des méthodes permettant de représenter, calculer et comparer des structures topologiques à partir de données finies.

Les objets manipulés comprennent souvent :

- des graphes ;
- des complexes simpliciaux ;
- des maillages ;
- des matrices de bord ;
- des filtrations ;
- des représentations d’homologie.

## **22.2. Calcul de composantes connexes**

Pour un graphe, les composantes connexes peuvent être calculées par des parcours en profondeur ou en largeur.

Ces algorithmes sont efficaces et constituent souvent la première étape d’une analyse structurelle.

## **22.3. Union-Find**

La structure Union-Find maintient une partition dynamique d’éléments en composantes.

Elle permet notamment :

- de fusionner des composantes ;
- de déterminer si deux éléments appartiennent à la même composante ;
- de suivre les fusions au cours d’une construction.

Elle est utile dans certaines approches de connexité et dans la compréhension de l’homologie persistante de dimension zéro.

## **22.4. Matrices de bord**

Dans un complexe simplicial, les opérateurs de bord sont représentés par des matrices.

Les relations fondamentales entre les opérateurs de bord permettent de définir les cycles et les frontières.

L’homologie s’obtient en étudiant les cycles modulo les frontières.

Dans les calculs sur un corps, cette démarche devient un problème d’algèbre linéaire exacte.

## **22.5. Réduction matricielle**

Le calcul de l’homologie persistante utilise des variantes de réduction de matrices de bord.

Le coût dépend :

- du nombre de simplexes ;
- de la dimension ;
- de la densité des relations ;
- de la représentation ;
- du corps de coefficients ;
- de l’algorithme de réduction.

La construction du complexe peut être plus coûteuse que le calcul d’homologie lui-même.

## **22.6. Complexité et passage à l’échelle**

Les complexes simpliciaux peuvent croître rapidement avec le nombre de points.

Dans un complexe de Vietoris–Rips, de nombreux simplexes apparaissent lorsque les voisinages deviennent denses.

Il faut donc contrôler :

- le nombre de points ;
- le seuil ;
- la dimension maximale ;
- la sparsité ;
- la représentation des voisinages ;
- les besoins en mémoire.

## **22.7. Stratégies d’optimisation**

Selon le problème :

- réduire les données sans détruire les propriétés pertinentes ;
- limiter la dimension maximale ;
- exploiter des structures creuses ;
- utiliser des algorithmes spécialisés ;
- paralléliser certaines étapes ;
- sélectionner des seuils raisonnables ;
- utiliser des représentations adaptées ;
- comparer les résultats avec des méthodes de référence.

Toute simplification doit être évaluée au regard des propriétés qu’elle conserve.

# **23\. ERREURS CONCEPTUELLES À ÉVITER**

## **23.1. Confondre topologie et géométrie**

La géométrie étudie notamment les distances, les angles, les courbures et les mesures.

La topologie étudie des propriétés plus structurelles, préservées par les homéomorphismes.

## **23.2. Croire que toute continuité implique une bijection**

Une fonction continue n’est pas nécessairement injective ou surjective.

L’homéomorphisme exige une bijection continue dont l’inverse est continu.

## **23.3. Confondre connexité et connexité par arcs**

La connexité par arcs implique la connexité, mais la réciproque est fausse en général.

## **23.4. Confondre compacité et finitude**

Un espace compact peut contenir une infinité de points.

L’intervalle fermé _\[0,1\]\[0,1\]_ est compact dans _R\\mathbb{R}_.

## **23.5. Croire que les mêmes invariants garantissent le même espace**

Deux espaces non homéomorphes peuvent partager certains invariants.

Un invariant ne constitue pas nécessairement une classification complète.

## **23.6. Confondre trou géométrique et classe d’homologie**

Une cavité visuelle, un trou dans un maillage et une classe d’homologie sont des notions liées, mais leur correspondance dépend de la représentation et du cadre mathématique.

## **23.7. Interpréter toute persistance comme une vérité métier**

Une classe persistante peut être mathématiquement stable dans une filtration sans être pertinente pour la question métier.

Il faut confronter les résultats à la connaissance du domaine et à des analyses complémentaires.

## **23.8. Supposer que la TDA remplace le machine learning**

La TDA peut fournir des caractéristiques, des diagnostics ou des contraintes. Elle ne remplace pas systématiquement la modélisation statistique, l’apprentissage ou la validation.

## **23.9. Ignorer le choix de distance**

La distance utilisée pour construire un complexe peut modifier les structures observées.

Une analyse robuste doit justifier le choix de métrique et tester la sensibilité aux paramètres.

## **23.10. Confondre propriété mathématique et approximation numérique**

Une propriété exacte de l’espace continu peut être mal représentée par un échantillonnage trop faible, un maillage défectueux ou une précision numérique insuffisante.

# **24\. FICHES DE RECONNAISSANCE : QUELLE NOTION UTILISER ?**

## **S01 — Espace topologique**

**Indices :** on veut définir les ouverts et les voisinages sans imposer de distance.

**Questions :**

- Quels sous-ensembles sont considérés comme ouverts ?
- La structure satisfait-elle les axiomes topologiques ?
- Quelle topologie est induite sur un sous-ensemble ?

**Applications :** formalisation d’espaces abstraits, continuité, espaces de configurations.

## **S02 — Continuité**

**Indices :** on veut savoir si une transformation préserve les relations de voisinage.

**Questions :**

- Les préimages des ouverts sont-elles ouvertes ?
- Les petites variations locales restent-elles contrôlées dans le cadre métrique ?

**Applications :** analyse, modélisation, transformations continues.

## **S03 — Homéomorphisme**

**Indices :** on veut savoir si deux espaces ont la même structure topologique.

**Questions :**

- L’application est-elle bijective ?
- Est-elle continue ?
- Son inverse est-il continu ?

**Applications :** classification topologique, comparaison de formes.

## **S04 — Connexité**

**Indices :** on veut identifier les composantes d’un espace.

**Questions :**

- L’espace peut-il être séparé en deux ouverts disjoints non vides ?
- Existe-t-il des chemins entre les points ?
- Combien de composantes sont présentes ?

**Applications :** réseaux, segmentation, TDA, espace libre d’un robot.

## **S05 — Compacité**

**Indices :** on veut établir une propriété globale de finitude ou démontrer l’existence d’un optimum.

**Questions :**

- L’espace est-il compact ?
- Le théorème applicable exige-t-il d’autres hypothèses ?
- Une fonction continue atteint-elle ses extrema dans le cadre étudié ?

**Applications :** optimisation, analyse, modélisation.

## **S06 — Homotopie**

**Indices :** on veut comparer des chemins ou des applications par déformation continue.

**Questions :**

- Les extrémités doivent-elles rester fixes ?
- Quelles contraintes doivent être conservées ?
- Les objets sont-ils homotopiquement équivalents ?

**Applications :** robotique, classes de chemins, obstacles.

## **S07 — Invariants topologiques**

**Indices :** on veut caractériser un espace indépendamment de sa représentation géométrique.

**Questions :**

- Quelle propriété est préservée ?
- Cet invariant suffit-il à distinguer les espaces considérés ?
- Quelles informations perd-il ?

**Applications :** comparaison de formes, classification, analyse structurelle.

## **S08 — Homologie**

**Indices :** on veut calculer des caractéristiques topologiques de différentes dimensions.

**Questions :**

- Quelle représentation discrète utilise-t-on ?
- Quel corps de coefficients choisit-on ?
- Quelles dimensions d’homologie sont pertinentes ?

**Applications :** TDA, maillages, analyse de formes.

## **S09 — Homologie persistante**

**Indices :** on veut étudier la stabilité des structures lorsque l’échelle change.

**Questions :**

- Quelle filtration est utilisée ?
- Comment les classes naissent-elles et disparaissent-elles ?
- Quelle interprétation donner à leur persistance ?

**Applications :** analyse de données, détection de structures robustes.

## **S10 — Topologie computationnelle**

**Indices :** on doit calculer des propriétés topologiques à partir d’une représentation finie.

**Questions :**

- Quelle structure discrète représente l’espace ?
- Quel algorithme calcule la propriété recherchée ?
- Quels sont les coûts en temps et en mémoire ?

**Applications :** vision par ordinateur, géométrie computationnelle, TDA.

# **25\. FICHES D’APPROFONDISSEMENT**

## **S11 — Topologie générale**

À approfondir :

- bases et sous-bases ;
- voisinages ;
- intérieur, adhérence et frontière ;
- topologies induites ;
- espaces produits ;
- espaces quotients ;
- espaces séparés ;
- axiomes de dénombrabilité ;
- espaces métrisables ;
- convergence.

**Objectif :** comprendre comment une topologie est construite et comment elle gouverne les notions locales et globales.

## **S12 — Continuité et homéomorphismes**

À approfondir :

- continuité topologique ;
- continuité métrique ;
- applications ouvertes et fermées ;
- homéomorphismes ;
- invariance topologique ;
- espaces localement homéomorphes ;
- stabilité sous composition.

**Objectif :** comparer des espaces et comprendre les transformations qui préservent leur structure.

## **S13 — Connexité**

À approfondir :

- espaces connexes ;
- connexité par arcs ;
- composantes connexes ;
- connexité locale ;
- chemins ;
- connexité dans les graphes ;
- connexité de données échantillonnées.

**Objectif :** analyser les parties séparées et les chemins possibles dans un espace.

## **S14 — Compacité**

À approfondir :

- recouvrements ouverts ;
- sous-recouvrements finis ;
- compacité séquentielle dans les cadres métriques ;
- compacité en dimension finie ;
- Heine–Borel ;
- théorème des valeurs extrêmes ;
- produits d’espaces compacts ;
- applications continues d’espaces compacts.

**Objectif :** utiliser la compacité pour établir des résultats globaux et des propriétés d’existence.

## **S15 — Homotopie et groupe fondamental**

À approfondir :

- homotopie de fonctions ;
- homotopie de chemins ;
- lacets ;
- groupe fondamental ;
- espaces contractiles ;
- équivalence d’homotopie ;
- revêtements ;
- classes de chemins.

**Objectif :** comprendre les déformations et les obstructions topologiques.

## **S16 — Homologie et cohomologie**

À approfondir :

- chaînes ;
- opérateurs de bord ;
- cycles ;
- frontières ;
- groupes d’homologie ;
- nombres de Betti ;
- coefficients ;
- cohomologie ;
- caractéristique d’Euler.

**Objectif :** associer des invariants algébriques aux espaces.

## **S17 — Topologie algébrique computationnelle**

À approfondir :

- complexes simpliciaux ;
- complexes cellulaires ;
- matrices de bord ;
- réduction matricielle ;
- calcul des groupes d’homologie ;
- calcul de la caractéristique d’Euler ;
- représentations creuses.

**Objectif :** relier les définitions abstraites à des algorithmes effectifs.

## **S18 — Topological Data Analysis**

À approfondir :

- choix de métrique ;
- complexes de Vietoris–Rips ;
- complexes de Čech ;
- filtrations ;
- homologie persistante ;
- diagrammes de persistance ;
- codes-barres ;
- distances entre diagrammes ;
- stabilité ;
- validation statistique.

**Objectif :** concevoir une analyse topologique des données rigoureuse et interprétable.

## **S19 — Géométrie computationnelle et topologie des maillages**

À approfondir :

- maillages polygonaux ;
- surfaces triangulées ;
- bords et orientations ;
- non-manifold ;
- composantes ;
- caractéristique d’Euler ;
- reconstruction de surfaces ;
- réparations topologiques.

**Objectif :** vérifier et traiter la structure des objets géométriques numériques.

## **S20 — Topologie et robotique**

À approfondir :

- espaces de configuration ;
- espaces libres ;
- obstacles ;
- classes d’homotopie ;
- planification de mouvement ;
- cartes topologiques ;
- graphes de configurations ;
- méthodes d’échantillonnage.

**Objectif :** comprendre comment la structure de l’espace contraint les trajectoires d’un robot.

## **S21 — Topologie et vision par ordinateur**

À approfondir :

- connectivité des pixels ;
- topologie de segmentation ;
- reconstruction 3D ;
- analyse de maillages ;
- trous et composantes ;
- invariants de forme ;
- caractéristiques topologiques pour l’apprentissage.

**Objectif :** exploiter les propriétés structurelles dans le traitement d’images et la reconstruction de formes.

## **S22 — Topologie et systèmes dynamiques**

À approfondir :

- espaces d’états ;
- trajectoires ;
- attracteurs ;
- invariance ;
- espaces de phases ;
- stabilité topologique ;
- dynamique qualitative ;
- liens avec les systèmes dynamiques et la théorie du chaos.

**Objectif :** comprendre les propriétés structurelles des trajectoires et des espaces d’états.

# **26\. PROJETS D’APPRENTISSAGE SANS IA**

## **Projet 1 — Laboratoire des topologies**

Construire plusieurs espaces topologiques finis.

Pour chacun :

1.  définir l’ensemble ;
2.  définir les ouverts ;
3.  vérifier les axiomes ;
4.  calculer les fermés ;
5.  identifier les voisinages ;
6.  déterminer les propriétés de séparation lorsque c’est pertinent.

**Livrable :** un catalogue d’espaces finis avec leurs propriétés.

## **Projet 2 — Analyse de composantes**

Implémenter un programme qui calcule les composantes connexes d’un graphe.

Comparer :

- parcours en profondeur ;
- parcours en largeur ;
- Union-Find.

**Livrable :** implémentation, tests et analyse de complexité.

## **Projet 3 — Exploration des homéomorphismes**

Étudier des exemples simples de courbes, de surfaces et d’espaces finis.

Identifier les propriétés topologiques conservées et les propriétés géométriques qui peuvent changer.

**Livrable :** dossier illustré avec des exemples et des contre-exemples.

## **Projet 4 — Homologie d’un petit complexe**

Construire un complexe simplicial fini.

Le programme doit :

- représenter les sommets, arêtes et faces ;
- construire les matrices de bord ;
- calculer leurs rangs ;
- déterminer les nombres de Betti dans un cadre approprié ;
- comparer le résultat avec une analyse manuelle.

**Livrable :** code et justification mathématique.

## **Projet 5 — Première analyse de persistance**

Générer un petit nuage de points synthétiques contenant :

- plusieurs groupes ;
- une boucle ;
- du bruit.

Construire une filtration, calculer l’homologie persistante et visualiser le code-barres.

**Livrable :** pipeline reproductible et analyse des résultats.

## **Projet 6 — Validation topologique d’un maillage**

Créer ou utiliser un maillage 3D et détecter :

- les composantes ;
- les bords ;
- les arêtes non-manifold ;
- les faces incohérentes ;
- les défauts de connectivité.

**Livrable :** outil de diagnostic et jeu de tests.

# **27\. PROJETS D’APPRENTISSAGE AVEC IA**

## **Projet 7 — Assistant d’exploration topologique**

Construire une interface dans laquelle l’utilisateur choisit un espace ou une représentation discrète et explore :

- les composantes ;
- les voisinages ;
- les cycles ;
- les changements de structure ;
- les invariants calculés.

L’IA peut expliquer les résultats, mais les calculs doivent être réalisés par un algorithme vérifiable.

## **Projet 8 — Analyse comparative de nuages de points**

Concevoir un pipeline de TDA sur deux jeux de données.

L’IA peut aider à :

- documenter les données ;
- proposer des hypothèses ;
- expliquer les choix de métrique ;
- générer des visualisations ;
- préparer une synthèse.

Les conclusions doivent être vérifiées par des analyses quantitatives et des tests de robustesse.

## **Projet 9 — Diagnostic de maillages assisté**

Construire un outil qui identifie des défauts topologiques dans des maillages.

L’IA peut expliquer les erreurs et proposer des réparations, mais chaque modification doit être vérifiée par les algorithmes de validation.

## **Projet 10 — Caractéristiques topologiques pour un modèle ML**

Extraire des caractéristiques issues d’une analyse topologique, puis les comparer à des caractéristiques classiques dans une tâche d’apprentissage.

Comparer :

- les performances ;
- la robustesse ;
- le coût ;
- la sensibilité aux paramètres ;
- l’interprétabilité.

Le but est de déterminer si la TDA apporte une amélioration réelle.

# **28\. DÉFIS ALGORITHMIQUES**

## **Défi 1 — Composantes connexes**

Étant donné un graphe, calculer toutes ses composantes.

Comparer plusieurs algorithmes et mesurer le coût sur des graphes de tailles différentes.

## **Défi 2 — Filtration de voisinage**

À partir d’un nuage de points, construire des graphes de voisinage pour plusieurs seuils.

Suivre l’apparition et la fusion des composantes.

## **Défi 3 — Complexe simplicial**

Construire un complexe simplicial à partir d’un petit ensemble de points.

Vérifier la fermeture par faces et la cohérence de la représentation.

## **Défi 4 — Calcul d’homologie**

Construire les matrices de bord d’un complexe fini.

Calculer les rangs nécessaires et déterminer les nombres de Betti.

## **Défi 5 — Homologie persistante**

Suivre les classes d’homologie à travers une filtration.

Produire un diagramme de persistance et un code-barres.

## **Défi 6 — Robustesse topologique**

Perturber un nuage de points et observer les changements des invariants calculés.

Déterminer quelles structures semblent robustes et lesquelles dépendent fortement des paramètres.

## **Défi 7 — Réparation de maillage**

Détecter un défaut topologique dans un maillage, proposer une réparation et vérifier que le résultat satisfait les contraintes attendues.

## **Défi 8 — Planification topologique**

Construire un espace libre simplifié avec des obstacles et rechercher plusieurs chemins entre une position initiale et une position finale.

Étudier les classes de chemins et les obstacles qui les distinguent.

# **29\. DÉFIS DE RAISONNEMENT MATHÉMATIQUE**

## **Défi 9 — Distinguer deux espaces**

Choisir deux espaces simples et rechercher un invariant permettant de montrer qu’ils ne sont pas homéomorphes.

Si un invariant ne suffit pas, expliquer pourquoi.

## **Défi 10 — Continuité**

Déterminer si une application est continue en utilisant :

- la définition par les ouverts ;
- la définition _ε\\varepsilon_\-_δ\\delta_ lorsque le cadre métrique le permet.

## **Défi 11 — Connexité et chemins**

Construire un exemple illustrant la différence entre connexité et connexité par arcs.

Expliquer pourquoi les deux notions ne sont pas équivalentes en général.

## **Défi 12 — Compacité**

Identifier les hypothèses nécessaires pour appliquer un théorème de compacité.

Construire un contre-exemple lorsqu’une hypothèse importante est supprimée.

## **Défi 13 — Homotopie**

Comparer plusieurs chemins dans un espace contenant des obstacles.

Déterminer quelles déformations sont possibles lorsque les extrémités doivent rester fixes.

## **Défi 14 — Interprétation d’un diagramme de persistance**

Analyser un diagramme de persistance et expliquer :

- quelles classes apparaissent ;
- combien de temps elles persistent ;
- quelles conclusions sont justifiées ;
- quelles conclusions seraient excessives.

# **30\. APPLICATIONS CRÉATIVES ET SORTIE DES SENTIERS BATTUS**

L’objectif est d’identifier les situations dans lesquelles la structure topologique apporte une information que les méthodes classiques ne fournissent pas directement.

## **30.1. Surveillance de la structure d’un système**

Construire un système qui suit la structure d’un ensemble de capteurs ou d’observations dans le temps.

Le système peut détecter des changements dans :

- le nombre de composantes ;
- les cycles ;
- les structures persistantes ;
- les relations de voisinage.

Applications :

- surveillance industrielle ;
- détection de changements ;
- diagnostic de systèmes complexes.

## **30.2. Cartographie topologique d’un environnement**

Construire une représentation qui décrit les régions et leurs connexions plutôt que les coordonnées précises de chaque point.

Applications :

- navigation robotique ;
- exploration d’environnements ;
- cartographie de bâtiments ;
- systèmes de navigation à haut niveau.

## **30.3. Analyse structurelle de données multimodales**

Construire une représentation combinant plusieurs sources de données.

Comparer la structure topologique de chaque modalité et étudier les changements induits par leur fusion.

Applications :

- capteurs ;
- données scientifiques ;
- analyse d’images et de signaux ;
- représentations apprises.

## **30.4. Détection de changements dans des données temporelles**

Transformer des fenêtres temporelles en représentations topologiques et suivre leur évolution.

L’objectif est de détecter des modifications structurelles qui ne se résument pas à une variation de moyenne ou de variance.

Il faut comparer cette approche à des méthodes de détection de changements existantes.

## **30.5. Diagnostic automatique de géométries**

Créer un moteur qui analyse un objet 3D et distingue :

- les défauts topologiques ;
- les problèmes de maillage ;
- les problèmes géométriques ;
- les incertitudes liées à la reconstruction.

Cette distinction est importante pour éviter de traiter un défaut géométrique comme un défaut topologique, ou inversement.

## **30.6. Analyse de la structure d’un espace latent**

Extraire les représentations intermédiaires d’un modèle d’IA et étudier leur structure topologique.

Comparer les représentations :

- avant et après entraînement ;
- entre différentes classes ;
- sous perturbation ;
- entre modèles distincts.

L’objectif est d’étudier la structure apprise, sans supposer que toute caractéristique topologique détectée possède une signification sémantique.

## **30.7. Recherche de chemins dans des espaces contraints**

Modéliser les configurations possibles d’un système et étudier les chemins compatibles avec les contraintes.

Applications :

- robotique ;
- animation ;
- planification ;
- systèmes de manipulation ;
- navigation autonome.

La topologie peut révéler des obstructions structurelles avant même de lancer une recherche exhaustive.

# **31\. LIENS AVEC L’INTELLIGENCE ARTIFICIELLE**

## **31.1. Topologie des données d’apprentissage**

Les données d’apprentissage peuvent être considérées comme des échantillons d’une structure sous-jacente.

La TDA permet d’étudier certaines propriétés de cette structure à partir des observations.

Les conclusions dépendent de la densité de l’échantillonnage, du bruit, de la métrique et des hypothèses sur la structure sous-jacente.

## **31.2. Représentations latentes**

Les modèles d’apprentissage apprennent souvent des représentations vectorielles.

L’analyse topologique peut servir à examiner :

- la séparation des classes ;
- les composantes ;
- les cycles ;
- les changements structurels au cours de l’apprentissage ;
- la robustesse des représentations.

Ces analyses sont complémentaires aux métriques de performance et aux outils d’explicabilité.

## **31.3. Apprentissage topologique**

Certaines méthodes intègrent des contraintes topologiques dans la fonction de perte ou dans le prétraitement.

Exemples :

- préserver la connexité d’une segmentation ;
- pénaliser des trous indésirables ;
- favoriser une structure topologique cible ;
- comparer des représentations via des caractéristiques topologiques.

Ces méthodes doivent définir précisément la propriété recherchée et la manière dont elle est différentiée ou optimisée.

## **31.4. Limites**

Les calculs topologiques peuvent être coûteux, et certaines représentations ne sont pas directement différentiables.

Il faut également éviter de forcer une topologie incorrecte : un modèle ne doit pas préserver artificiellement des structures qui ne sont pas pertinentes pour la tâche.

# **32\. ARCHITECTURE D’UN SYSTÈME DE TDA**

Une architecture pratique peut être organisée en couches.

## **32.1. Couche 1 — Ingestion**

Responsabilités :

- charger les données ;
- vérifier les types ;
- détecter les valeurs manquantes ;
- contrôler les dimensions ;
- enregistrer les métadonnées.

## **32.2. Couche 2 — Prétraitement**

Responsabilités :

- normaliser si nécessaire ;
- sélectionner les variables ;
- traiter les valeurs aberrantes ;
- définir la métrique ;
- vérifier les effets du prétraitement.

## **32.3. Couche 3 — Construction topologique**

Responsabilités :

- calculer les voisinages ;
- construire le complexe ;
- définir la filtration ;
- contrôler la taille de la représentation.

## **32.4. Couche 4 — Calcul**

Responsabilités :

- calculer les composantes ;
- calculer l’homologie ;
- calculer la persistance ;
- stocker les résultats intermédiaires.

## **32.5. Couche 5 — Interprétation**

Responsabilités :

- produire des diagrammes ;
- comparer les structures ;
- évaluer la stabilité ;
- relier les résultats au contexte métier.

## **32.6. Couche 6 — Validation**

Responsabilités :

- tester plusieurs paramètres ;
- comparer avec des données synthétiques connues ;
- vérifier les résultats ;
- mesurer les coûts ;
- documenter les limites.

## **32.7. Principe architectural**

Un résultat topologique doit pouvoir être relié à la donnée d’origine, à la métrique choisie, à la filtration utilisée et à l’algorithme qui l’a produit.

Sans cette traçabilité, un résultat peut être difficile à interpréter ou à reproduire.

# **33\. MODÈLE DE DONNÉES POUR UN LABORATOIRE TOPOLOGIQUE**

## **33.1. Entité Dataset**

Attributs :

- identifiant ;
- origine ;
- dimensions ;
- nombre de points ;
- variables ;
- prétraitement ;
- métadonnées ;
- version.

## **33.2. Entité Metric**

Attributs :

- nom ;
- domaine d’application ;
- paramètres ;
- méthode de calcul ;
- contraintes ;
- justification du choix.

## **33.3. Entité Complex**

Attributs :

- type de complexe ;
- sommets ;
- simplexes ;
- dimension maximale ;
- filtration ;
- méthode de construction.

## **33.4. Entité TopologicalInvariant**

Attributs :

- type d’invariant ;
- dimension ;
- valeur ou représentation ;
- coefficients ;
- paramètres ;
- méthode de calcul.

## **33.5. Entité PersistenceClass**

Attributs :

- dimension d’homologie ;
- naissance ;
- disparition, si définie dans la filtration ;
- durée de vie ;
- représentation ;
- méthode de calcul.

## **33.6. Entité Experiment**

Attributs :

- jeu de données ;
- paramètres ;
- métrique ;
- algorithme ;
- durée ;
- mémoire ;
- résultats ;
- limites ;
- comparaison de référence.

Ce modèle facilite la reproductibilité et la comparaison des analyses.

# **34\. MÉTHODE D’ANALYSE D’UN PROBLÈME TOPOLOGIQUE**

Lorsqu’un problème semble relever de la topologie, suivre cette méthode.

## **Étape 1 — Identifier l’objet**

S’agit-il d’un espace abstrait, d’un nuage de points, d’un graphe, d’un maillage, d’une image ou d’un espace de configurations ?

## **Étape 2 — Identifier la structure disponible**

Dispose-t-on :

- d’une topologie explicite ;
- d’une métrique ;
- d’une relation de voisinage ;
- d’une représentation discrète ;
- d’une structure géométrique ?

## **Étape 3 — Formuler la question**

Cherche-t-on :

- une propriété locale ;
- une continuité ;
- des composantes ;
- une propriété de compacité ;
- une classe d’homotopie ;
- un invariant ;
- une structure persistante ?

## **Étape 4 — Choisir la notion mathématique**

Sélectionner l’outil correspondant au problème.

Ne pas utiliser l’homologie uniquement parce qu’elle est disponible si une simple analyse de composantes suffit.

## **Étape 5 — Choisir une représentation calculable**

Exemples :

- graphe ;
- complexe simplicial ;
- maillage ;
- matrice de bord ;
- filtration.

## **Étape 6 — Définir les paramètres**

Préciser :

- la distance ;
- le seuil ;
- le type de complexe ;
- la dimension ;
- le corps de coefficients ;
- les conditions de validité.

## **Étape 7 — Calculer**

Utiliser un algorithme adapté à la taille et à la structure des données.

## **Étape 8 — Vérifier la stabilité**

Modifier les paramètres dans des plages raisonnables et vérifier si les conclusions importantes persistent.

## **Étape 9 — Interpréter**

Relier les résultats aux questions du domaine métier.

## **Étape 10 — Documenter les limites**

Préciser les hypothèses, les approximations et les conclusions qui ne sont pas justifiées par les résultats.

# **35\. CHECKLIST DE MAÎTRISE**

## **Niveau 1 — Fondements**

- Je sais définir un espace topologique.
- Je comprends les axiomes d’une topologie.
- Je distingue ouverts et fermés.
- Je comprends les voisinages.
- Je distingue une métrique d’une topologie.
- Je comprends l’intérieur, l’adhérence et la frontière.

## **Niveau 2 — Continuité et propriétés globales**

- Je sais définir la continuité topologique.
- Je comprends la définition métrique de la continuité.
- Je distingue continuité et homéomorphisme.
- Je comprends la connexité.
- Je distingue connexité et connexité par arcs.
- Je comprends la compacité.
- Je sais appliquer les théorèmes de base sous leurs hypothèses.

## **Niveau 3 — Déformations et invariants**

- Je sais définir une homotopie.
- Je comprends les classes d’homotopie de chemins.
- Je comprends la contractibilité.
- Je sais expliquer la notion d’invariant topologique.
- Je comprends le rôle du groupe fondamental.
- Je comprends les groupes d’homologie et les nombres de Betti.

## **Niveau 4 — Représentations discrètes**

- Je sais représenter un petit complexe simplicial.
- Je comprends les matrices de bord.
- Je sais expliquer la différence entre un graphe et un complexe simplicial.
- Je comprends les complexes de Vietoris–Rips et de Čech.
- Je comprends la construction d’une filtration.

## **Niveau 5 — Algorithmique et TDA**

- Je sais calculer des composantes connexes.
- Je comprends les principes de l’homologie persistante.
- Je sais interpréter un diagramme de persistance.
- Je sais analyser la sensibilité aux paramètres.
- Je comprends les coûts de calcul et de mémoire.
- Je sais distinguer un résultat mathématique d’une interprétation métier.

## **Niveau 6 — Applications**

- Je comprends les usages topologiques en vision par ordinateur.
- Je comprends le rôle de la topologie dans la planification robotique.
- Je sais expliquer comment la TDA complète l’analyse de données.
- Je comprends les enjeux topologiques des maillages.
- Je sais concevoir un pipeline reproductible de TDA.
- Je sais évaluer si une méthode topologique apporte une valeur réelle au problème.

# **36\. TEST ULTIME DE MAÎTRISE**

Pour considérer le domaine comme réellement assimilé, il faut pouvoir répondre aux questions suivantes avec une définition, un raisonnement et un exemple.

1.  Qu’est-ce qui distingue un espace topologique d’un espace métrique ?
2.  Pourquoi les ouverts sont-ils au centre de la définition de la continuité ?
3.  Quelle différence existe-t-il entre continuité et homéomorphisme ?
4.  Pourquoi la connexité n’est-elle pas équivalente à la connexité par arcs ?
5.  Pourquoi un espace compact peut-il contenir une infinité de points ?
6.  Comment la compacité peut-elle garantir l’existence d’un optimum ?
7.  Quelle différence existe-t-il entre homotopie et homéomorphisme ?
8.  Pourquoi deux espaces ayant les mêmes nombres de Betti ne sont-ils pas nécessairement homéomorphes ?
9.  Comment l’homologie représente-t-elle certaines caractéristiques topologiques ?
10. Pourquoi utilise-t-on des complexes simpliciaux pour calculer des propriétés topologiques ?
11. Comment une filtration permet-elle d’étudier un nuage de points à plusieurs échelles ?
12. Que signifie la persistance d’une classe d’homologie ?
13. Pourquoi une caractéristique persistante n’est-elle pas automatiquement pertinente pour le domaine métier ?
14. Comment la topologie peut-elle contribuer à la planification d’un robot ?
15. Comment détecter des défauts topologiques dans un maillage ?
16. Quelles sont les limites de la TDA face à des données bruitées ou de grande dimension ?
17. Comment vérifier qu’un résultat topologique est stable lorsque les paramètres changent ?
18. Comment choisir entre une analyse de graphe classique et une méthode de topologie algébrique ?

La maîtrise ne consiste pas seulement à connaître les termes : il faut savoir quand les utiliser, quelles hypothèses ils exigent et quelles conclusions ils autorisent.

# **37\. LES DOUZE IDÉES À RETENIR**

1.  La topologie étudie la structure des espaces et les propriétés préservées par les transformations topologiques appropriées.
2.  Un espace topologique est un ensemble muni d’une famille d’ouverts satisfaisant des axiomes.
3.  La continuité exprime la préservation des relations de voisinage.
4.  Un homéomorphisme établit une équivalence topologique entre deux espaces.
5.  La connexité décrit l’absence de séparation topologique en parties ouvertes disjointes non vides.
6.  La compacité est une propriété globale définie par les recouvrements ouverts.
7.  L’homotopie permet d’étudier les déformations continues d’applications et de chemins.
8.  Les invariants topologiques fournissent des caractéristiques préservées par les homéomorphismes.
9.  La topologie algébrique associe des structures algébriques aux espaces.
10. Les complexes simpliciaux permettent de représenter des structures topologiques sous une forme calculable.
11. La TDA étudie la forme des données, notamment grâce à l’homologie persistante.
12. Les applications informatiques exigent de relier les concepts mathématiques à des représentations discrètes, des algorithmes, des paramètres et une interprétation rigoureuse.

# **38\. MODÈLE MENTAL FINAL**

Le modèle mental du domaine S peut être résumé ainsi :

**ESPACE → VOISINAGES → TOPOLOGIE → CONTINUITÉ → PROPRIÉTÉS GLOBALES → DÉFORMATIONS → INVARIANTS → REPRÉSENTATIONS DISCRÈTES → CALCUL → INTERPRÉTATION.**

Chaque étape répond à une question :

- **Espace :** quels objets étudie-t-on ?
- **Voisinages :** quelles relations locales sont importantes ?
- **Topologie :** quels ensembles sont ouverts ?
- **Continuité :** quelles transformations préservent la structure de voisinage ?
- **Propriétés globales :** l’espace est-il connexe ou compact ?
- **Déformations :** quelles applications ou quels chemins sont homotopes ?
- **Invariants :** quelles caractéristiques résistent aux déformations ?
- **Représentations discrètes :** comment traduire l’espace en une structure calculable ?
- **Calcul :** comment obtenir les propriétés recherchées ?
- **Interprétation :** que signifient les résultats dans le problème réel ?

L’idée fondamentale est de comprendre que la structure globale d’un objet ne se résume pas à ses dimensions, à ses coordonnées ou à ses distances.

Un nuage de points, une surface, un réseau ou un espace de configurations peut posséder des propriétés structurelles qui ne sont pas visibles à partir d’une simple mesure locale.

La topologie offre des outils pour les formuler, les distinguer et parfois les calculer.

# **39\. SYNTHÈSE FINALE**

La topologie constitue une approche mathématique essentielle pour comprendre les propriétés structurelles des espaces.

La topologie générale définit les espaces, les ouverts, les voisinages et la continuité. La connexité permet d’étudier les composantes, tandis que la compacité fournit des résultats importants sur les propriétés globales et l’existence de solutions. L’homotopie permet de comparer des chemins et des applications par déformation continue. Les invariants topologiques donnent des moyens de distinguer des structures indépendamment de certaines variations géométriques.

La topologie algébrique prolonge cette approche en associant des groupes et d’autres structures algébriques aux espaces. L’homologie, les nombres de Betti et le groupe fondamental permettent d’étudier différentes caractéristiques topologiques.

La topologie computationnelle rend ces concepts accessibles aux systèmes informatiques grâce à des graphes, des maillages, des complexes simpliciaux et des algorithmes de calcul. La Topological Data Analysis exploite notamment les filtrations et l’homologie persistante pour analyser la structure de données observées à plusieurs échelles.

Les applications sont nombreuses :

- en analyse de données, pour rechercher des structures persistantes ;
- en géométrie computationnelle, pour analyser les maillages ;
- en robotique, pour comprendre les espaces libres et les classes de chemins ;
- en vision par ordinateur, pour étudier la structure des segmentations et des surfaces ;
- dans les réseaux, pour analyser la connectivité ;
- en modélisation, pour formaliser les propriétés structurelles des espaces.

La maîtrise du domaine repose sur trois compétences complémentaires :

- **Compréhension mathématique :** savoir définir les espaces et démontrer leurs propriétés.
- **Maîtrise computationnelle :** savoir représenter les structures et calculer leurs invariants.
- **Capacité d’interprétation :** savoir relier les résultats mathématiques à un problème réel sans dépasser ce qu’ils permettent de conclure.

Le but ultime n’est pas d’utiliser la topologie dans chaque problème. Il est de reconnaître les situations où les relations de voisinage, les déformations ou les invariants révèlent une structure que les distances et les statistiques seules ne décrivent pas suffisamment.

**Ne demande pas seulement quelle distance sépare les éléments. Demande quelle structure les relie, quelles propriétés survivent aux déformations et quelles caractéristiques globales peuvent être extraites des données.**