# **DOMAINE U — LOGIQUE FLOUE**

## **Représenter les degrés, raisonner avec des concepts vagues et concevoir des systèmes intelligents adaptatifs**

**Identifiant :** U

**Domaine mathématique :** Logique floue, ensembles flous et raisonnement approximatif

**Domaines informatiques associés :** Intelligence artificielle, systèmes experts, systèmes de contrôle, robotique, décision, automatisation et systèmes intelligents

**Nature du document :** Référentiel mathématique, logique, algorithmique et informatique

**Objectif :** Fournir les connaissances nécessaires pour formaliser l'imprécision des concepts, construire des systèmes de raisonnement flou, concevoir des contrôleurs et intégrer la logique floue dans des architectures logicielles intelligentes.

# **0\. FINALITÉ ET MODE D'UTILISATION DU DOCUMENT**

## **0.1. Rôle du domaine U dans le référentiel mathématique**

La logique classique permet notamment de représenter une proposition par deux valeurs de vérité : vrai ou faux. La logique floue introduit un cadre permettant de représenter des degrés de vérité ou, plus précisément dans le modèle standard des ensembles flous, des degrés d'appartenance à un ensemble.

En logique classique, on peut représenter l'appartenance à un ensemble _AA_ par une fonction caractéristique :

_μA(x)∈{0,1}\\mu_A(x)\\in\\{0,1\\}_

Dans un ensemble flou, cette fonction prend généralement ses valeurs dans l'intervalle _\[0,1\]\[0,1\]_ :

_μA(x)∈\[0,1\]\\mu_A(x)\\in\[0,1\]_

La valeur obtenue indique le degré auquel l'élément _xx_ appartient à l'ensemble flou _AA_.

Par exemple, pour une variable linguistique « température », une température mesurée peut avoir un degré d'appartenance de _0,730{,}73_ à l'ensemble flou « chaude ».

Cette valeur n'est pas universelle : elle dépend de la fonction d'appartenance choisie, de son domaine et de la définition opérationnelle de « chaude ».

La logique floue permet ainsi de traduire des descriptions qualitatives en modèles mathématiques utilisables par des logiciels.

Elle répond à des questions comme :

- À quel degré une température peut-elle être considérée comme chaude ?
- Comment représenter une distance comme « proche » ou « très proche » ?
- Comment combiner plusieurs critères imprécis pour évaluer un risque ?
- Comment transformer des règles linguistiques en décisions numériques ?
- Comment construire un contrôleur capable d'ajuster progressivement une commande ?
- Comment intégrer des connaissances expertes dans un système logiciel ?
- Comment gérer des catégories dont les frontières ne sont pas nettes ?
- Comment concevoir des systèmes qui raisonnent à partir de règles qualitatives plutôt que de seuils stricts ?

La logique floue n'est pas simplement une variante de la logique booléenne. Elle constitue une famille de méthodes mathématiques et informatiques pour modéliser les concepts graduels, les règles approximatives et certaines formes d'incertitude linguistique.

## **0.2. Objectifs de maîtrise**

La maîtrise du domaine doit permettre de :

1.  distinguer logique classique, logique floue et probabilités ;
2.  comprendre la notion d'ensemble flou ;
3.  définir et manipuler des fonctions d'appartenance ;
4.  concevoir des variables linguistiques ;
5.  choisir des opérateurs flous adaptés ;
6.  formaliser des règles de type « SI… ALORS… » ;
7.  construire un système d'inférence floue ;
8.  comprendre les méthodes de Mamdani, Sugeno et Tsukamoto ;
9.  transformer une sortie floue en décision numérique ;
10. concevoir un contrôleur flou ;
11. intégrer la logique floue dans un système expert ou un agent intelligent ;
12. appliquer les méthodes floues à la robotique et à la décision ;
13. tester la cohérence, la robustesse et la stabilité d'un modèle ;
14. comprendre les limites de cette approche ;
15. combiner la logique floue avec d'autres méthodes d'IA lorsque cela est pertinent.

## **0.3. Comment utiliser cette référence**

Lorsqu'un projet implique des catégories graduelles, des règles linguistiques ou des décisions fondées sur plusieurs critères, suivre cette démarche :

1.  **Reconnaître le besoin :** le problème nécessite-t-il de représenter des concepts aux frontières imprécises ?
2.  **Définir les variables :** quelles grandeurs sont observées et quelles décisions doivent être produites ?
3.  **Définir les ensembles flous :** quels termes linguistiques décrivent chaque variable ?
4.  **Choisir les fonctions d'appartenance :** comment calculer les degrés associés aux observations ?
5.  **Formaliser les règles :** quelles relations existent entre les conditions et les conséquences ?
6.  **Choisir le moteur d'inférence :** quelle méthode convient aux règles et aux sorties attendues ?
7.  **Calculer la sortie :** faut-il une décision linguistique ou une valeur numérique ?
8.  **Valider :** le système se comporte-t-il correctement aux frontières et dans les cas inhabituels ?
9.  **Optimiser :** les fonctions et règles peuvent-elles être simplifiées ou calibrées ?
10. **Comparer :** une méthode floue est-elle réellement préférable à un seuil classique, un modèle probabiliste ou une méthode d'apprentissage ?

# **1\. IDENTITÉ MATHÉMATIQUE DU DOMAINE**

## **1.1. La question fondamentale**

La question centrale de la logique floue est :

**Comment représenter et exploiter mathématiquement des concepts dont l'appartenance n'est pas naturellement limitée à une frontière nette ?**

Considérons une température.

Un programme classique pourrait définir :

if temperature >= 30:  
category = "chaude"  
else:  
category = "pas chaude"  

Cette règle impose une frontière brutale à _3030_. Une température de _29,929{,}9_ serait considérée comme non chaude, alors qu'une température de _3030_ serait chaude.

Pour certains systèmes, cette discontinuité n'est pas souhaitable.

Une approche floue peut définir une fonction d'appartenance :

_μchaude(T)∈\[0,1\]\\mu_{\\text{chaude}}(T)\\in\[0,1\]_

La fonction associe à chaque température _TT_ un degré d'appartenance à la catégorie « chaude ».

Par exemple, un modèle hypothétique pourrait produire :

|     |     |
| --- | --- |
| **Température** | **Degré d'appartenance à « chaude »** |
| 20\\,^\\circ C | 0,00 |
| 24\\,^\\circ C | 0,10 |
| 27\\,^\\circ C | 0,40 |
| 30\\,^\\circ C | 0,73 |
| 34\\,^\\circ C | 1,00 |

Ces valeurs illustrent un modèle possible, pas une définition universelle de la température chaude.

L'intérêt consiste à remplacer une classification rigide par une représentation graduelle adaptée à l'objectif du système.

## **1.2. La notion de degré d'appartenance**

Un ensemble flou _AA_ défini sur un univers _XX_ est caractérisé par une fonction :

_μA:X→\[0,1\]\\mu_A:X\\rightarrow\[0,1\]_

Pour tout élément _x∈Xx\\in X_, _μA(x)\\mu_A(x)_ indique son degré d'appartenance à _AA_.

Dans le modèle standard :

- _μA(x)=0\\mu_A(x)=0_ signifie que _xx_ n'appartient pas à _AA_ selon ce modèle ;
- _μA(x)=1\\mu_A(x)=1_ signifie que _xx_ appartient pleinement à _AA_ ;
- _0<μA(x)<10<\\mu_A(x)<1_ représente une appartenance partielle.

La fonction d'appartenance formalise une définition opérationnelle du concept. Elle ne révèle pas une propriété universelle indépendante du contexte.

## **1.3. Logique floue et logique classique**

La logique classique reste parfaitement adaptée aux situations dans lesquelles les règles exigent une distinction stricte.

Exemples :

- un utilisateur possède-t-il une autorisation valide ?
- un paiement a-t-il été confirmé ?
- un fichier existe-t-il ?
- une contrainte légale est-elle satisfaite ?

Ces conditions peuvent nécessiter des valeurs booléennes.

La logique floue devient intéressante lorsque le système doit raisonner sur des concepts graduels :

- vitesse faible ;
- risque élevé ;
- température confortable ;
- distance proche ;
- confiance relativement forte ;
- qualité satisfaisante ;
- niveau de congestion important.

Il est possible de combiner les deux approches : utiliser une évaluation floue pour apprécier une situation, puis une condition stricte pour autoriser ou interdire une action.

## **1.4. Logique floue et probabilité**

Il s'agit d'une distinction fondamentale.

La probabilité représente l'incertitude concernant la réalisation d'un événement ou la valeur d'une variable aléatoire, dans un modèle probabiliste.

Le degré d'appartenance représente la compatibilité d'une valeur avec un concept flou.

Supposons qu'une température de 30\\,^\\circ C ait :

_μchaude(30)=0,73\\mu_{\\text{chaude}}(30)=0{,}73_

Cela signifie que cette température appartient à l'ensemble flou « chaude » avec un degré de _0,730{,}73_, selon la fonction choisie.

Cela ne signifie pas :

_P(tempeˊrature chaude)=0,73P(\\text{température chaude})=0{,}73_

Ces deux nombres peuvent parfois coexister dans un même système, mais ils représentent des quantités différentes.

La logique floue traite principalement la gradualité des concepts. Les probabilités traitent principalement l'incertitude aléatoire. Les deux approches peuvent être combinées lorsqu'un problème contient les deux phénomènes.

# **2\. PLACE DU DOMAINE U DANS LA CHAÎNE MATHÉMATIQUE ET INFORMATIQUE**

## **2.1. Fondations mathématiques nécessaires**

### **A. Logique et fondements**

La logique permet de formaliser les propositions, les règles et les relations entre conditions et conclusions.

La logique floue prolonge certaines structures logiques en permettant des degrés de vérité ou des opérateurs graduels.

### **B. Théorie des ensembles**

Les ensembles flous généralisent les ensembles classiques en remplaçant l'appartenance binaire par une fonction d'appartenance graduelle.

La théorie des ensembles fournit le langage de base pour représenter les catégories floues.

### **C. Fonctions et analyse**

Les fonctions d'appartenance peuvent être triangulaires, trapézoïdales, gaussiennes ou définies par d'autres fonctions mathématiques.

Leur continuité, leur forme, leur support et leurs paramètres influencent les sorties du système.

### **D. Algèbre**

Les opérateurs flous utilisent des opérations telles que le minimum, le maximum, le produit et d'autres fonctions définies sur _\[0,1\]\[0,1\]_.

Ces opérations servent à combiner les degrés d'appartenance.

### **E. Probabilités et statistiques**

Les probabilités permettent de modéliser l'incertitude aléatoire. Les statistiques peuvent aider à calibrer les fonctions d'appartenance à partir de données.

Il faut toutefois conserver la distinction entre degré d'appartenance et probabilité.

### **F. Optimisation**

L'optimisation permet d'ajuster les paramètres des fonctions d'appartenance, les règles ou les poids d'un système flou.

Elle peut être utilisée pour améliorer la performance à partir de données ou d'un objectif mesurable.

### **G. Analyse numérique**

Les calculs flous sont souvent exécutés numériquement. La discrétisation, la précision et les méthodes d'intégration peuvent influencer les résultats.

### **H. Théorie du contrôle**

Les contrôleurs flous transforment des observations en commandes en s'appuyant sur des règles graduelles.

Ils peuvent être utilisés lorsque des experts savent décrire qualitativement le comportement souhaité sans disposer d'un modèle analytique complet.

## **2.2. Les principaux prolongements informatiques**

La logique floue peut être utilisée dans :

- les systèmes experts ;
- le contrôle de processus ;
- la robotique ;
- les systèmes de décision ;
- les systèmes d'aide au diagnostic ;
- les évaluations multicritères ;
- la classification graduelle ;
- les systèmes embarqués ;
- l'automatisation ;
- les systèmes hybrides d'IA ;
- certaines méthodes de clustering ;
- les interfaces d'interprétation de données ;
- la gestion de la qualité et du risque.

Elle est particulièrement utile lorsque les règles métier peuvent être exprimées sous forme linguistique, mais que leur application nécessite des calculs numériques.

# **3\. TAXONOMIE DE LA LOGIQUE FLOUE**

## **3.1. Ensembles classiques et ensembles flous**

Dans un ensemble classique, un élément appartient ou n'appartient pas à l'ensemble.

La fonction caractéristique est :

_χA(x)={1si x∈A0si x∉A\\chi_A(x)= \\begin{cases} 1 & \\text{si }x\\in A\\\\ 0 & \\text{si }x\\notin A \\end{cases}_

Dans un ensemble flou, l'appartenance est graduelle :

_μA(x)∈\[0,1\]\\mu_A(x)\\in\[0,1\]_

Les ensembles classiques peuvent être considérés comme un cas particulier des ensembles flous lorsque toutes les valeurs de la fonction d'appartenance sont limitées à _00_ ou _11_.

## **3.2. Logique floue de type 1**

Dans la logique floue de type 1, chaque élément possède un degré d'appartenance déterminé par une valeur unique.

Par exemple :

_μrapide(v)=0,82\\mu_{\\text{rapide}}(v)=0{,}82_

La valeur peut dépendre d'une vitesse _vv_ et d'une fonction d'appartenance définie.

Cette approche est relativement simple à calculer et à interpréter.

## **3.3. Logique floue de type 2**

Dans les ensembles flous de type 2, les degrés d'appartenance peuvent eux-mêmes être représentés par des ensembles flous.

Cette extension permet de représenter certaines incertitudes portant sur la définition même des fonctions d'appartenance.

Elle peut être utile lorsque plusieurs experts ne s'accordent pas sur la frontière d'un concept ou lorsque cette frontière varie selon le contexte.

Les systèmes de type 2 sont généralement plus complexes à calculer et à calibrer.

## **3.4. Systèmes flous linguistiques et systèmes flous numériques**

Un système flou linguistique repose sur des règles compréhensibles, telles que :

« SI la température est élevée ET l'humidité est forte, ALORS réduire la puissance de chauffage. »

Un système flou numérique peut utiliser des fonctions de sortie ou des modèles mathématiques plutôt que des conclusions uniquement linguistiques.

Les systèmes de Mamdani sont souvent appréciés pour leur lisibilité linguistique. Les systèmes de Sugeno utilisent généralement des conclusions numériques, ce qui facilite certaines formes d'optimisation et d'intégration.

## **3.5. Logique floue et méthodes hybrides**

La logique floue peut être associée à :

- des réseaux de neurones ;
- des algorithmes génétiques ;
- des méthodes d'optimisation ;
- des systèmes probabilistes ;
- des contrôleurs classiques ;
- des agents intelligents ;
- des modèles physiques.

Ces combinaisons permettent de conserver certaines capacités d'interprétation tout en exploitant des données ou des méthodes d'apprentissage.

# **4\. NOTION U01 — ENSEMBLES FLOUS**

## **4.1. Définition formelle**

Soit un univers de discours _XX_.

Un ensemble flou _AA_ est caractérisé par une fonction d'appartenance :

_μA:X→\[0,1\]\\mu_A:X\\rightarrow\[0,1\]_

L'ensemble flou peut être représenté par l'ensemble des couples :

_A={(x,μA(x))∣x∈X}A=\\{(x,\\mu_A(x))\\mid x\\in X\\}_

Chaque couple associe un élément à son degré d'appartenance.

Par exemple, si _XX_ représente des niveaux de vitesse, un ensemble flou « vitesse élevée » peut associer à chaque vitesse un degré compris entre _00_ et _11_.

## **4.2. Univers de discours**

L'univers de discours représente le domaine de valeurs possibles pour une variable.

Exemples :

- température : de _−10-10_ à 50\\,^\\circ C ;
- vitesse : de _00_ à _150150_ km/h ;
- niveau de batterie : de _00_ à _100100_ % ;
- distance : de _00_ à _2020_ mètres ;
- score de risque : de _00_ à _100100_.

Le choix de l'univers est important.

Une fonction conçue pour une température comprise entre _00_ et 40\\,^\\circ C ne doit pas être utilisée sans précaution pour des températures de plusieurs centaines de degrés.

Il faut définir ce que le système doit faire en dehors du domaine prévu.

## **4.3. Support, noyau et frontière**

Pour un ensemble flou _AA_, plusieurs notions permettent de décrire sa forme.

### **Support**

Le support de _AA_ est l'ensemble des valeurs pour lesquelles le degré d'appartenance est strictement positif :

_supp⁡(A)={x∈X∣μA(x)>0}\\operatorname{supp}(A)=\\{x\\in X\\mid \\mu_A(x)>0\\}_

### **Noyau**

Le noyau est l'ensemble des valeurs qui appartiennent pleinement à _AA_ :

_core⁡(A)={x∈X∣μA(x)=1}\\operatorname{core}(A)=\\{x\\in X\\mid \\mu_A(x)=1\\}_

### **Frontière**

La frontière désigne généralement la zone dans laquelle le degré d'appartenance est intermédiaire.

La définition exacte de la frontière peut varier selon les propriétés étudiées. Dans les applications, il est souvent utile de préciser les intervalles dans lesquels la fonction passe de valeurs faibles à des valeurs élevées.

## **4.4. Coupes alpha**

Une coupe alpha permet de transformer un ensemble flou en un ensemble classique.

Pour _α∈\[0,1\]\\alpha\\in\[0,1\]_, la coupe forte est :

_Aα={x∈X∣μA(x)>α}A_\\alpha=\\{x\\in X\\mid \\mu_A(x)>\\alpha\\}_

La coupe faible utilise la condition :

_Aα={x∈X∣μA(x)≥α}A_\\alpha=\\{x\\in X\\mid \\mu_A(x)\\geq\\alpha\\}_

Ces deux conventions sont utilisées en mathématiques. Il faut indiquer celle qui est choisie dans une implémentation.

Les coupes alpha sont utiles pour analyser un ensemble flou à différents niveaux d'exigence.

## **4.5. Hauteur et normalité**

La hauteur d'un ensemble flou est :

_h(A)=sup⁡x∈XμA(x)h(A)=\\sup_{x\\in X}\\mu_A(x)_

Un ensemble flou est normal si sa hauteur vaut _11_, c'est-à-dire si au moins une valeur atteint le degré maximal dans le cadre usuel des ensembles considérés.

Un ensemble flou non normal peut être pertinent si le concept ne peut jamais être pleinement satisfait dans le domaine étudié.

## **4.6. Exemples d'ensembles flous**

### **Exemple A — Température chaude**

On peut définir un ensemble « chaude » avec une montée progressive du degré d'appartenance, suivie d'une zone où le degré reste élevé.

### **Exemple B — Distance proche**

La proximité peut dépendre de l'application.

Une distance de deux mètres peut être proche pour un robot industriel, mais très éloignée pour un capteur microscopique.

### **Exemple C — Risque élevé**

Un score de risque peut appartenir partiellement à plusieurs catégories : moyen, élevé ou très élevé.

Cela permet d'éviter des changements abrupts lorsque le score se situe près d'un seuil.

## **4.7. Applications informatiques**

Les ensembles flous permettent de représenter des catégories qualitatives dans :

- les moteurs de règles ;
- les contrôleurs ;
- les systèmes d'évaluation ;
- les interfaces d'aide à la décision ;
- les systèmes de classification graduelle ;
- les moteurs de recommandation fondés sur des critères qualitatifs.

# **5\. NOTION U02 — FONCTIONS D'APPARTENANCE**

## **5.1. Rôle**

La fonction d'appartenance transforme une valeur numérique en degré d'appartenance à un concept.

Elle constitue l'un des éléments les plus importants d'un système flou, car sa forme détermine comment les valeurs sont interprétées.

Il n'existe pas une fonction universelle adaptée à tous les concepts.

Le choix dépend :

- du sens du terme ;
- des données disponibles ;
- du comportement attendu ;
- des contraintes de calcul ;
- du niveau d'interprétabilité recherché.

## **5.2. Fonction triangulaire**

Une fonction triangulaire est définie par trois paramètres _a,b,ca,b,c_, avec _a≤b≤ca\\leq b\\leq c_.

_μ(x)={0x≤ax−ab−aa<x≤bc−xc−bb<x<c0x≥c\\mu(x)= \\begin{cases} 0 & x\\leq a\\\\ \\dfrac{x-a}{b-a} & a<x\\leq b\\\\ \\dfrac{c-x}{c-b} & b<x<c\\\\ 0 & x\\geq c \\end{cases}_

Cette expression suppose _a<b<ca<b<c_. Les cas dégénérés doivent être traités séparément.

La fonction augmente linéairement jusqu'à _bb_, puis diminue jusqu'à _cc_.

Exemple : un système peut utiliser une fonction triangulaire pour représenter la notion de « vitesse modérée ».

**Avantages :**

- simple ;
- rapide à calculer ;
- facile à interpréter ;
- peu de paramètres.

**Limites :**

- les changements de pente sont brusques ;
- le modèle peut être trop simpliste pour certains phénomènes physiques.

## **5.3. Fonction trapézoïdale**

Une fonction trapézoïdale utilise quatre paramètres _a,b,c,da,b,c,d_, avec _a≤b≤c≤da\\leq b\\leq c\\leq d_.

_μ(x)={0x≤ax−ab−aa<x<b1b≤x≤cd−xd−cc<x<d0x≥d\\mu(x)= \\begin{cases} 0 & x\\leq a\\\\ \\dfrac{x-a}{b-a} & a<x<b\\\\ 1 & b\\leq x\\leq c\\\\ \\dfrac{d-x}{d-c} & c<x<d\\\\ 0 & x\\geq d \\end{cases}_

Elle représente un concept qui est pleinement satisfait sur un intervalle.

Les cas où deux paramètres sont égaux doivent être définis soigneusement pour éviter une division par zéro.

**Applications :**

- température confortable ;
- niveau de batterie satisfaisant ;
- vitesse dans une plage souhaitée ;
- mesure conforme à une tolérance.

## **5.4. Fonction gaussienne**

Une fonction gaussienne peut être définie par :

_μ(x)=exp⁡(−(x−c)22σ2)\\mu(x)= \\exp\\left(-\\frac{(x-c)^2}{2\\sigma^2}\\right)_

où :

- _cc_ représente le centre ;
- _σ>0\\sigma>0_ contrôle la largeur.

La fonction atteint son maximum en _cc_ et diminue progressivement lorsque l'on s'en éloigne.

Elle est utile pour représenter des catégories dont l'appartenance diminue de manière régulière.

**Avantages :**

- fonction lisse ;
- transitions progressives ;
- paramètres intuitifs.

**Limites :**

- calcul plus coûteux que des fonctions linéaires simples ;
- support théoriquement infini ;
- calibration parfois moins intuitive.

## **5.5. Fonction sigmoïde**

Une fonction sigmoïde peut être définie par :

_μ(x)=11+exp⁡(−a(x−c))\\mu(x)=\\frac{1}{1+\\exp(-a(x-c))}_

où _aa_ contrôle la pente et _cc_ la position de transition.

Pour _a>0a>0_, elle représente un degré croissant qui passe progressivement de valeurs proches de zéro à des valeurs proches de un.

Pour représenter un concept décroissant, on peut inverser son orientation ou utiliser une transformation appropriée.

Elle est utile pour représenter des concepts comme « suffisamment élevé » ou « de plus en plus pertinent ».

## **5.6. Fonctions en cloche et fonctions personnalisées**

D'autres fonctions peuvent être utilisées :

- fonctions en cloche généralisées ;
- fonctions polynomiales ;
- fonctions par morceaux ;
- fonctions dérivées de contraintes métier ;
- fonctions apprises à partir de données.

Une fonction personnalisée doit respecter les propriétés nécessaires au modèle et être testée sur tout son domaine.

## **5.7. Chevauchement des fonctions**

Les catégories floues peuvent se chevaucher.

Une température donnée peut appartenir partiellement à « tiède » et à « chaude ».

Ce chevauchement permet une transition progressive entre les catégories.

Un système dont les fonctions ne se chevauchent jamais peut retrouver des changements abrupts ou des zones sans couverture.

À l'inverse, un chevauchement excessif peut rendre les règles difficiles à interpréter.

## **5.8. Calibration des fonctions**

Les paramètres peuvent être définis par :

- expertise métier ;
- données historiques ;
- contraintes physiques ;
- essais expérimentaux ;
- optimisation ;
- apprentissage automatique ;
- combinaison de plusieurs méthodes.

La calibration doit vérifier que les fonctions correspondent réellement au sens des catégories utilisées.

Une fonction mathématiquement correcte peut être sémantiquement inadaptée.

# **6\. NOTION U03 — VARIABLES LINGUISTIQUES**

## **6.1. Définition**

Une variable linguistique est une variable dont les valeurs sont des termes linguistiques associés à des ensembles flous.

Par exemple, pour la variable « température », les termes peuvent être :

_T={froide,tieˋde,chaude,treˋs chaude}T=\\{\\text{froide},\\text{tiède},\\text{chaude},\\text{très chaude}\\}_

Chaque terme possède sa propre fonction d'appartenance.

La variable linguistique ne remplace pas nécessairement la mesure numérique. Elle fournit une représentation qualitative de cette mesure.

## **6.2. Structure d'une variable linguistique**

Une variable linguistique peut être définie par :

- son nom ;
- son univers de discours ;
- ses termes linguistiques ;
- les fonctions d'appartenance associées ;
- les unités ;
- les conventions de mesure.

Exemple :

**Variable :** température

**Univers :** \[0,50\]\\,^\\circ C

**Termes :**

- froide ;
- modérée ;
- chaude ;
- très chaude.

Les fonctions associées doivent être définies explicitement.

## **6.3. Modificateurs linguistiques**

Les expressions linguistiques peuvent être modifiées par des termes tels que :

- très ;
- peu ;
- plus ou moins ;
- extrêmement ;
- approximativement.

Un modificateur peut être représenté par une transformation de la fonction d'appartenance.

Par exemple, dans une convention courante :

_μtreˋs A(x)=μA(x)2\\mu_{\\text{très }A}(x)=\\mu_A(x)^2_

Cette transformation renforce les valeurs proches de _11_ et diminue les valeurs intermédiaires.

Une autre convention pourrait utiliser une puissance différente. Le choix doit être cohérent avec le sens attribué au modificateur.

## **6.4. Négation linguistique**

La négation d'un ensemble flou peut être définie par :

_μ¬A(x)=1−μA(x)\\mu_{\\neg A}(x)=1-\\mu_A(x)_

Il s'agit de la négation standard.

Cependant, « non chaud » n'est pas toujours synonyme de « froid ». Selon le contexte, une température peut être ni chaude ni froide, mais modérée.

Il est donc souvent préférable de définir explicitement les catégories linguistiques plutôt que de supposer que leur négation représente automatiquement une catégorie métier.

## **6.5. Partition floue**

Une partition floue divise l'univers de discours en plusieurs ensembles flous.

Dans une partition normalisée, on peut rechercher la propriété :

_∑i=1nμAi(x)=1\\sum_{i=1}^{n}\\mu_{A_i}(x)=1_

pour chaque valeur _xx_ de l'univers.

Cette propriété est utile dans certains modèles, mais elle n'est pas obligatoire pour toutes les applications de logique floue.

D'autres systèmes utilisent des partitions où la somme peut être différente de _11_, selon la sémantique des catégories et la méthode d'inférence.

## **6.6. Applications informatiques**

Les variables linguistiques sont utiles lorsque les experts peuvent décrire le comportement attendu en termes qualitatifs.

Exemples :

- un thermostat ;
- un système de ventilation ;
- une évaluation de risque ;
- un assistant de diagnostic ;
- un robot de navigation ;
- un moteur de règles métier.

# **7\. NOTION U04 — OPÉRATEURS FLOUS**

## **7.1. Rôle**

Les opérateurs flous permettent de combiner des degrés d'appartenance.

Ils jouent un rôle comparable à celui des opérateurs logiques dans un système classique, mais ils doivent être définis dans le cadre du modèle flou utilisé.

Les opérateurs les plus courants concernent :

- la conjonction ;
- la disjonction ;
- la négation ;
- l'implication.

Il n'existe pas une seule définition universelle de ces opérations dans toutes les logiques floues.

## **7.2. Conjonction : ET**

Soient deux degrés :

_a=μA(x),b=μB(x)a=\\mu_A(x),\\qquad b=\\mu_B(x)_

Une conjonction floue combine ces degrés.

### **Minimum**

_Tmin⁡(a,b)=min⁡(a,b)T_{\\min}(a,b)=\\min(a,b)_

Exemple :

_Tmin⁡(0,7,0,4)=0,4T_{\\min}(0{,}7,0{,}4)=0{,}4_

La conjonction ne peut pas être plus forte que le degré le plus faible.

### **Produit algébrique**

_Tprod(a,b)=abT_{\\mathrm{prod}}(a,b)=ab_

Exemple :

_Tprod(0,7,0,4)=0,28T_{\\mathrm{prod}}(0{,}7,0{,}4)=0{,}28_

Le produit peut réduire davantage le degré combiné.

### **Autres t-normes**

Il existe d'autres opérateurs de conjonction, notamment les t-normes de Łukasiewicz et de Gödel.

Le choix dépend de la sémantique souhaitée et du comportement du moteur d'inférence.

## **7.3. Disjonction : OU**

Une disjonction floue combine plusieurs degrés.

### **Maximum**

_Smax⁡(a,b)=max⁡(a,b)S_{\\max}(a,b)=\\max(a,b)_

Exemple :

_Smax⁡(0,7,0,4)=0,7S_{\\max}(0{,}7,0{,}4)=0{,}7_

### **Somme probabiliste**

_Sprob(a,b)=a+b−abS_{\\mathrm{prob}}(a,b)=a+b-ab_

Exemple :

_Sprob(0,7,0,4)=0,82S_{\\mathrm{prob}}(0{,}7,0{,}4)=0{,}82_

Cette opération ne doit pas être interprétée comme une probabilité, même si sa forme rappelle certaines formules probabilistes.

### **Autres s-normes**

D'autres opérations sont possibles, notamment la somme bornée :

_Sborneˊe(a,b)=min⁡(1,a+b)S_{\\mathrm{bornée}}(a,b)=\\min(1,a+b)_

Ces choix ne produisent pas nécessairement les mêmes résultats.

## **7.4. Négation**

La négation standard est :

_N(a)=1−aN(a)=1-a_

Ainsi :

_N(0,73)=0,27N(0{,}73)=0{,}27_

Cette transformation est courante, mais d'autres opérateurs de négation existent.

## **7.5. Implication floue**

Une règle de type « SI _AA_, ALORS _BB_ » nécessite un mécanisme qui relie l'antécédent à la conséquence.

Plusieurs méthodes sont possibles :

- implication de Mamdani ;
- implication de Łukasiewicz ;
- implication de Gödel ;
- implication fondée sur d'autres opérations floues.

Dans les systèmes de Mamdani, la conséquence peut être tronquée par le degré d'activation de la règle.

Dans les systèmes de Sugeno, la sortie de la règle est généralement calculée par une fonction numérique.

Il faut donc éviter de considérer toutes les méthodes d'implication comme équivalentes.

## **7.6. Choisir les opérateurs**

Le choix d'un opérateur peut modifier les sorties d'un système.

Pour une conjonction, le minimum et le produit ne réagissent pas de la même manière lorsque plusieurs conditions sont partiellement satisfaites.

Le minimum conserve le plus petit degré, tandis que le produit combine les degrés multiplicativement.

Il faut :

1.  choisir une sémantique ;
2.  la documenter ;
3.  tester les cas limites ;
4.  vérifier la cohérence avec les règles métier ;
5.  éviter de mélanger arbitrairement des conventions différentes.

# **8\. NOTION U05 — RÈGLES FLOUES ET RAISONNEMENT APPROXIMATIF**

## **8.1. Structure d'une règle**

Une règle floue classique peut être formulée ainsi :

**SI** une ou plusieurs conditions sont satisfaites à certains degrés, **ALORS** une conséquence est activée.

Exemple :

« SI la température est élevée ET l'humidité est forte, ALORS la ventilation doit être importante. »

Une règle comprend :

- un antécédent ;
- un opérateur de combinaison ;
- une conséquence ;
- éventuellement un poids ou une priorité.

## **8.2. Degré d'activation d'une règle**

Supposons :

_μeˊleveˊe(T)=0,8\\mu_{\\text{élevée}}(T)=0{,}8_

et :

_μforte(H)=0,6\\mu_{\\text{forte}}(H)=0{,}6_

Si la conjonction utilise le minimum, le degré d'activation vaut :

_α=min⁡(0,8,0,6)=0,6\\alpha=\\min(0{,}8,0{,}6)=0{,}6_

Si elle utilise le produit :

_α=0,8×0,6=0,48\\alpha=0{,}8\\times0{,}6=0{,}48_

Le résultat dépend donc du choix de l'opérateur.

## **8.3. Base de règles**

Un système flou peut contenir plusieurs règles.

Exemple de contrôle de ventilation :

1.  SI température froide, ALORS ventilation faible.
2.  SI température modérée, ALORS ventilation moyenne.
3.  SI température chaude, ALORS ventilation forte.
4.  SI température chaude ET humidité forte, ALORS ventilation très forte.

Les règles doivent être cohérentes entre elles et couvrir les situations que le système peut rencontrer.

## **8.4. Complétude et cohérence**

Une base de règles doit être examinée pour vérifier :

- les situations non couvertes ;
- les règles contradictoires ;
- les conditions redondantes ;
- les sorties incompatibles ;
- les cas limites ;
- les règles qui ne s'activent jamais ;
- les règles trop générales ;
- les combinaisons de conditions imprévues.

Une base de règles trop petite peut ignorer des situations importantes.

Une base trop volumineuse peut devenir difficile à maintenir et à expliquer.

## **8.5. Poids des règles**

Certaines architectures attribuent un poids à chaque règle.

Ce poids peut influencer la contribution de la règle à la sortie finale.

Cependant, le poids n'a pas automatiquement une signification probabiliste. Il représente une convention de modélisation qui doit être définie et documentée.

## **8.6. Raisonnement explicable**

L'un des avantages des systèmes flous fondés sur des règles est la possibilité de retracer le raisonnement :

- valeur mesurée ;
- degré d'appartenance à chaque catégorie ;
- règles activées ;
- degré d'activation ;
- contributions des règles ;
- sortie calculée.

Cette traçabilité peut être utile pour les systèmes experts et les outils d'aide à la décision.

Elle ne garantit toutefois pas que le modèle soit juste : une règle explicable peut être mal conçue.

# **9\. NOTION U06 — SYSTÈMES D'INFÉRENCE FLOUE**

## **9.1. Architecture générale**

Un système d'inférence floue transforme des entrées numériques en une sortie au moyen de fonctions d'appartenance et de règles.

Une architecture classique comprend :

1.  les entrées ;
2.  la fuzzification ;
3.  le moteur d'inférence ;
4.  la base de règles ;
5.  l'agrégation des conséquences ;
6.  la défuzzification, si nécessaire ;
7.  la sortie numérique ou linguistique.

Le terme « fuzzification » désigne ici la conversion des entrées numériques en degrés d'appartenance aux ensembles flous définis.

## **9.2. Étape 1 — Fuzzification**

Pour chaque entrée, on calcule les degrés d'appartenance aux catégories correspondantes.

Exemple :

T=30\\,^\\circ C

peut produire :

_μmodeˊreˊe(T)=0,3\\mu_{\\text{modérée}}(T)=0{,}3_ _μchaude(T)=0,7\\mu_{\\text{chaude}}(T)=0{,}7_

Ces nombres sont illustratifs et dépendent des fonctions définies.

Une entrée peut activer plusieurs ensembles flous simultanément.

## **9.3. Étape 2 — Évaluation des règles**

Le moteur calcule le degré d'activation de chaque règle.

Pour une règle comportant plusieurs conditions, le résultat dépend de l'opérateur utilisé.

## **9.4. Étape 3 — Implication**

Le degré d'activation influence la conséquence.

Dans un système de Mamdani utilisant le minimum, un ensemble flou de sortie peut être tronqué au niveau du degré d'activation de la règle.

Avec d'autres méthodes, la conséquence peut être transformée différemment.

## **9.5. Étape 4 — Agrégation**

Les conséquences des différentes règles sont combinées pour obtenir une sortie floue globale.

Une méthode courante utilise le maximum des contributions.

D'autres méthodes peuvent être adaptées à l'architecture retenue.

## **9.6. Étape 5 — Défuzzification**

Si la sortie doit être une valeur numérique, il faut généralement la transformer à partir de la représentation floue agrégée.

La défuzzification est particulièrement fréquente dans les contrôleurs et les systèmes de décision.

Elle n'est pas nécessaire dans toutes les applications : certains systèmes peuvent conserver une sortie floue ou utiliser directement les degrés calculés.

# **10\. NOTION U07 — MÉTHODES DE MAMDANI, SUGENO ET TSUKAMOTO**

## **10.1. Système de Mamdani**

Le système de Mamdani utilise généralement :

- des entrées fuzzifiées ;
- des règles linguistiques ;
- des conséquences représentées par des ensembles flous ;
- une agrégation des sorties ;
- une défuzzification éventuelle.

Exemple :

« SI la température est chaude, ALORS la puissance de refroidissement est élevée. »

La conséquence « élevée » correspond à un ensemble flou défini sur l'univers des puissances.

**Avantages :**

- règles faciles à lire ;
- interprétation intuitive ;
- adapté aux connaissances expertes ;
- utile pour le contrôle fondé sur des descriptions qualitatives.

**Limites :**

- défuzzification parfois coûteuse ;
- calibration des fonctions nécessaire ;
- nombre de règles susceptible de croître rapidement.

## **10.2. Système de Sugeno**

Dans un système de Sugeno, la conséquence de chaque règle est généralement une constante ou une fonction numérique des entrées.

Une règle peut prendre la forme :

« SI la température est élevée ET l'humidité est forte, ALORS la commande vaut _f(T,H)f(T,H)_. »

Dans un modèle de premier ordre, on peut avoir :

_zi=piT+qiH+riz_i=p_iT+q_iH+r_i_

où _pi,qi,rip_i,q_i,r_i_ sont les paramètres de la règle.

Si les degrés d'activation sont _wiw_i_, une sortie courante est :

_z=∑iwizi∑iwiz= \\frac{\\sum_i w_i z_i} {\\sum_i w_i}_

lorsque la somme des poids est strictement positive.

**Avantages :**

- sortie numérique directe ;
- calcul efficace ;
- intégration facilitée avec l'optimisation ;
- utile pour des systèmes hybrides ou adaptatifs.

**Limites :**

- conséquences parfois moins intuitives pour les experts ;
- interprétation dépendante de la structure des fonctions de sortie ;
- calibration nécessaire.

## **10.3. Système de Tsukamoto**

Dans une méthode de Tsukamoto, la conséquence de chaque règle est associée à une fonction d'appartenance monotone.

Chaque règle fournit une valeur numérique correspondant à son degré d'activation, puis les sorties sont généralement combinées par une moyenne pondérée.

Cette approche est utile lorsque les ensembles de sortie peuvent être représentés par des fonctions monotones appropriées.

Elle impose toutefois des contraintes plus fortes sur les fonctions de sortie que certaines formulations de Mamdani.

## **10.4. Comparaison**

|     |     |     |     |
| --- | --- | --- | --- |
| **Critère** | **Mamdani** | **Sugeno** | **Tsukamoto** |
| Conséquence d'une règle | Ensemble flou | Constante ou fonction numérique | Ensemble à fonction monotone |
| Sortie globale | Agrégation floue | Combinaison numérique pondérée | Combinaison numérique pondérée |
| Défuzzification classique | Souvent nécessaire | Généralement inutile sous la même forme | La sortie est obtenue par pondération |
| Interprétabilité linguistique | Élevée dans de nombreux modèles | Dépend des fonctions numériques | Dépend des ensembles monotones |
| Calcul | Peut nécessiter l'intégration numérique | Souvent efficace | Variable selon la formulation |
| Usage fréquent | Contrôle linguistique, systèmes experts | Contrôle et modèles adaptatifs | Applications compatibles avec les contraintes de monotonie |

Le choix doit dépendre du problème, de la nature des règles, des exigences d'interprétation et du coût de calcul.

# **11\. NOTION U08 — DÉFUZZIFICATION**

## **11.1. Rôle**

La défuzzification transforme une sortie floue en une valeur numérique lorsque le système doit produire une commande, un score ou une décision quantitative.

Elle est particulièrement importante dans les contrôleurs.

Il n'existe pas une méthode optimale pour toutes les situations.

## **11.2. Méthode du centroïde**

La méthode du centroïde, aussi appelée centre de gravité, est très utilisée.

Pour une fonction d'appartenance agrégée _μ(y)\\mu(y)_, la sortie peut être calculée par :

_y∗=∫Yy μ(y) dy∫Yμ(y) dyy^\*= \\frac{\\int_Y y\\,\\mu(y)\\,dy} {\\int_Y \\mu(y)\\,dy}_

Cette formule suppose que le dénominateur est strictement positif et que les intégrales sont définies.

Le résultat correspond au centre de gravité de la distribution floue selon cette représentation.

Dans une implémentation discrète, une approximation est :

_y∗≈∑j=1myjμ(yj)∑j=1mμ(yj)y^\* \\approx \\frac{\\sum_{j=1}^{m}y_j\\mu(y_j)} {\\sum_{j=1}^{m}\\mu(y_j)}_

lorsque le dénominateur est non nul.

## **11.3. Méthode du maximum**

Cette famille de méthodes sélectionne une valeur associée au degré d'appartenance maximal.

Les variantes comprennent :

- premier maximum ;
- dernier maximum ;
- moyenne des maxima.

Elles sont souvent plus simples à calculer, mais peuvent produire des changements brusques ou des résultats différents selon la convention retenue.

## **11.4. Méthodes pondérées**

Dans les systèmes de Sugeno, une sortie peut être calculée par moyenne pondérée des sorties des règles.

_y∗=∑iwizi∑iwiy^\*=\\frac{\\sum_i w_i z_i}{\\sum_i w_i}_

où _wiw_i_ est le degré d'activation de la règle et _ziz_i_ sa sortie numérique.

Cette formule nécessite un dénominateur positif.

## **11.5. Cas sans activation**

Si aucune règle ne s'active ou si l'agrégation produit une fonction nulle, la défuzzification par centroïde peut être indéfinie.

Le système doit définir une stratégie de repli, par exemple :

- une valeur sûre par défaut ;
- une dernière commande valide ;
- un mode de contrôle classique ;
- une demande de recalibrage ;
- une interruption contrôlée.

Le choix dépend du risque associé à l'application.

# **12\. NOTION U09 — CONTRÔLE FLOU**

## **12.1. Définition**

Le contrôle flou utilise la logique floue pour transformer des mesures en commandes.

Il est particulièrement intéressant lorsque les experts savent décrire le comportement souhaité avec des règles qualitatives.

Exemple :

- SI l'erreur est grande ET qu'elle augmente, ALORS agir fortement ;
- SI l'erreur est faible, ALORS agir doucement ;
- SI l'erreur est presque nulle, ALORS réduire la commande.

Le contrôleur ne nécessite pas toujours un modèle analytique précis du système, mais il doit tout de même être conçu et validé rigoureusement.

## **12.2. Erreur et variation d'erreur**

Un contrôleur peut utiliser :

- l'erreur _e(t)e(t)_ entre la consigne et la mesure ;
- la variation de l'erreur _Δe(t)\\Delta e(t)_ ;
- d'autres mesures pertinentes.

Par exemple :

_e(t)=r(t)−y(t)e(t)=r(t)-y(t)_

où :

- _r(t)r(t)_ est la consigne ;
- _y(t)y(t)_ est la valeur mesurée.

La variation peut être approximée par :

_Δe(t)=e(t)−e(t−Δt)\\Delta e(t)=e(t)-e(t-\\Delta t)_

Ces grandeurs sont ensuite converties en ensembles flous.

## **12.3. Exemple de contrôleur de température**

Entrées :

- température mesurée ;
- écart par rapport à la consigne.

Sortie :

- puissance de chauffage ou de refroidissement.

Termes possibles :

- température basse ;
- température confortable ;
- température élevée ;
- erreur négative ;
- erreur faible ;
- erreur positive ;
- commande faible ;
- commande moyenne ;
- commande forte.

Les règles relient les entrées aux commandes.

## **12.4. Avantages**

- possibilité d'intégrer des connaissances expertes ;
- représentation progressive des transitions ;
- comportement compréhensible ;
- adaptation possible à des systèmes difficiles à modéliser ;
- calcul souvent réalisable sur des systèmes embarqués.

## **12.5. Limites**

- les règles et fonctions peuvent être mal calibrées ;
- les performances ne sont pas garanties par la seule présence de logique floue ;
- le système peut osciller ou réagir trop lentement ;
- les interactions entre variables peuvent devenir complexes ;
- la stabilité du système doit être étudiée ;
- les capteurs peuvent être défaillants ;
- la logique floue ne remplace pas les limites de sécurité.

Dans un système physique, il faut tester les transitions, les perturbations, les saturations et les scénarios dangereux.

# **13\. APPLICATIONS À L'INTELLIGENCE ARTIFICIELLE ET AUX SYSTÈMES EXPERTS**

## **13.1. Systèmes experts flous**

Un système expert flou représente des connaissances sous forme de règles linguistiques et de fonctions d'appartenance.

Il peut être utile lorsque les connaissances sont qualitatives et que les frontières des catégories ne sont pas nettes.

Exemple d'évaluation d'une machine :

- SI la vibration est élevée ET la température est élevée, ALORS le niveau de surveillance est très élevé ;
- SI la vibration est modérée ET la température est normale, ALORS le niveau de surveillance est moyen.

La sortie peut être un niveau de surveillance ou une valeur numérique.

## **13.2. Systèmes d'aide à la décision**

Un système d'aide à la décision peut utiliser plusieurs critères :

- coût ;
- délai ;
- fiabilité ;
- risque ;
- qualité ;
- impact.

Les critères peuvent être représentés par des ensembles flous, puis combinés à l'aide de règles ou de fonctions d'agrégation.

Il faut toutefois distinguer :

- les degrés d'appartenance ;
- les poids des critères ;
- les préférences du décideur ;
- les probabilités de résultats incertains.

Ces éléments peuvent intervenir ensemble, mais ils n'ont pas la même signification.

## **13.3. Logique floue et classification**

Un classificateur classique peut affecter une observation à une seule classe.

Une classification floue peut attribuer à l'observation plusieurs degrés d'appartenance.

Exemple :

- classe « faible risque » : _0,150{,}15_ ;
- classe « risque moyen » : _0,650{,}65_ ;
- classe « risque élevé » : _0,350{,}35_.

Ces valeurs ne constituent pas automatiquement une distribution de probabilités.

Elles représentent les degrés de compatibilité avec les catégories du modèle.

## **13.4. Logique floue et systèmes de recommandation**

Un système de recommandation peut représenter des critères comme :

- proximité ;
- coût raisonnable ;
- bonne qualité ;
- forte pertinence ;
- délai court.

Des règles peuvent combiner ces critères pour produire un score de préférence.

Cette méthode peut être utile lorsque les règles métier sont explicites, mais elle ne remplace pas nécessairement les modèles statistiques ou les méthodes d'apprentissage sur de grandes quantités de données.

## **13.5. Logique floue et IA générative**

Un modèle de langage peut aider à :

- formuler des règles candidates ;
- identifier des variables ;
- proposer des fonctions d'appartenance ;
- générer des scénarios de test ;
- expliquer les résultats ;
- transformer des connaissances expertes en règles structurées.

Cependant, un modèle génératif ne garantit pas que les règles produites soient mathématiquement cohérentes ou adaptées à l'application.

Les règles doivent être vérifiées, testées et validées par rapport aux objectifs du système.

# **14\. APPLICATIONS À LA ROBOTIQUE**

## **14.1. Navigation**

Un robot peut évaluer des notions telles que :

- obstacle proche ;
- vitesse élevée ;
- direction favorable ;
- espace dégagé ;
- risque de collision.

Les mesures des capteurs sont converties en degrés d'appartenance, puis combinées pour sélectionner une commande.

## **14.2. Évitement d'obstacles**

Entrées possibles :

- distance à l'obstacle ;
- angle de l'obstacle ;
- vitesse actuelle ;
- direction souhaitée.

Sorties :

- vitesse de déplacement ;
- angle de rotation ;
- niveau de freinage.

Exemple de règles :

- SI obstacle très proche, ALORS freiner fortement ;
- SI obstacle proche ET situé à gauche, ALORS tourner vers la droite ;
- SI espace dégagé ET trajectoire favorable, ALORS avancer plus rapidement.

Ces règles sont illustratives. Un système réel doit intégrer la géométrie du robot, ses contraintes dynamiques et des mécanismes de sécurité.

## **14.3. Fusion de mesures**

La logique floue peut combiner plusieurs évaluations graduelles issues de capteurs.

Elle ne résout pas automatiquement tous les problèmes de fusion sensorielle. Les mesures peuvent également nécessiter :

- un filtrage ;
- une estimation probabiliste ;
- une calibration ;
- une synchronisation ;
- une détection de panne.

## **14.4. Contrôle de mouvement**

Un contrôleur flou peut ajuster :

- la vitesse ;
- l'accélération ;
- l'orientation ;
- la force de commande ;
- les corrections de trajectoire.

La qualité du contrôle doit être évaluée selon :

- la précision ;
- la stabilité ;
- le temps de réponse ;
- la consommation énergétique ;
- la résistance aux perturbations ;
- la sécurité.

# **15\. APPLICATIONS AU CONTRÔLE ET À L'AUTOMATISATION**

## **15.1. Contrôle industriel**

La logique floue peut servir à contrôler :

- la température ;
- la pression ;
- le débit ;
- la vitesse ;
- l'humidité ;
- certains procédés industriels.

Elle est particulièrement utile lorsque des opérateurs expérimentés peuvent décrire le comportement souhaité en règles linguistiques.

## **15.2. Gestion de l'énergie**

Un système de gestion énergétique peut combiner :

- niveau de batterie ;
- demande estimée ;
- température ;
- coût énergétique ;
- disponibilité des ressources.

Les sorties peuvent orienter les décisions de charge, de décharge ou de répartition des ressources.

La sécurité électrique et les contraintes physiques doivent rester garanties par des mécanismes spécifiques.

## **15.3. Systèmes de ventilation**

Un contrôleur peut utiliser :

- température ;
- humidité ;
- présence ;
- qualité de l'air ;
- consommation énergétique.

Les règles permettent de définir des commandes graduelles.

Il faut éviter les comportements contradictoires, comme augmenter simultanément le chauffage et le refroidissement sans justification.

## **15.4. Maintenance prédictive**

Un système flou peut combiner des indicateurs tels que :

- vibration ;
- température ;
- fréquence des anomalies ;
- durée de fonctionnement ;
- gravité des écarts.

Il peut produire un niveau de priorité pour une inspection.

Il faut toutefois distinguer une évaluation floue du risque d'une estimation statistique de la probabilité de panne.

# **16\. IMPLICATIONS POUR L'ARCHITECTURE LOGICIELLE**

## **16.1. Séparer les responsabilités**

Une architecture logicielle floue devrait distinguer :

**Modèle des variables**

- univers de discours ;
- unités ;
- termes linguistiques ;
- fonctions d'appartenance.

**Moteur d'inférence**

- opérateurs ;
- règles ;
- degrés d'activation ;
- agrégation.

**Moteur de sortie**

- défuzzification ;
- décision ;
- stratégie de repli.

**Configuration**

- paramètres ;
- version des règles ;
- seuils de sécurité ;
- limites opérationnelles.

**Évaluation**

- tests ;
- scénarios ;
- métriques ;
- journaux ;
- rapports.

Cette séparation facilite la maintenance et permet de comparer plusieurs modèles sans réécrire toute l'application.

## **16.2. Modèle de données conceptuel**

Un système flou peut être représenté ainsi :

FuzzySystem  
├── input_variables  
│ ├── universe  
│ └── membership_functions  
├── output_variables  
│ ├── universe  
│ └── membership_functions  
├── operators  
├── rules  
├── inference_method  
├── aggregation_method  
├── defuzzification_method  
└── fallback_policy  

Une variable peut être représentée par :

FuzzyVariable  
├── name  
├── unit  
├── min_value  
├── max_value  
└── linguistic_terms  
├── label  
├── membership_function  
└── parameters  

Une règle peut être représentée par :

FuzzyRule  
├── antecedent  
├── logical_operators  
├── consequent  
├── weight  
└── metadata  

Il s'agit de structures conceptuelles. Le modèle concret doit être adapté à l'application.

## **16.3. Validation des entrées**

Le moteur doit gérer :

- valeurs manquantes ;
- mesures hors domaine ;
- unités incohérentes ;
- valeurs non numériques ;
- données corrompues ;
- capteurs indisponibles.

Il ne faut pas attribuer silencieusement un degré d'appartenance arbitraire à une donnée invalide.

La politique de traitement doit être explicite.

## **16.4. Versionnement des règles**

Les règles et les fonctions d'appartenance influencent directement le comportement du système.

Il est donc utile de versionner :

- les ensembles flous ;
- les paramètres ;
- les opérateurs ;
- les règles ;
- les méthodes d'inférence ;
- les méthodes de défuzzification.

Lorsqu'un résultat change, le versionnement aide à déterminer si la cause vient des données, des règles ou de l'algorithme.

## **16.5. Tests unitaires**

Tester au minimum :

- les valeurs aux extrémités des domaines ;
- les points de transition ;
- les degrés d'appartenance égaux à _00_ ou _11_ ;
- les valeurs intermédiaires ;
- les fonctions aux paramètres limites ;
- les règles qui ne s'activent pas ;
- les contradictions ;
- les cas où la défuzzification est impossible ;
- les valeurs hors domaine.

## **16.6. Tests de propriétés**

Selon le système, vérifier :

- que les degrés restent dans _\[0,1\]\[0,1\]_ ;
- que les fonctions respectent leurs propriétés prévues ;
- que les sorties restent dans les limites physiques ;
- que des variations raisonnables des entrées ne provoquent pas des changements absurdes ;
- que les règles de sécurité restent prioritaires ;
- que le système possède un comportement défini dans les cas non couverts.

La monotonie d'une sortie n'est pas universellement souhaitable. Elle doit être vérifiée uniquement lorsqu'elle correspond à une propriété attendue du modèle.

## **16.7. Performance**

Les performances dépendent notamment :

- du nombre de règles ;
- du nombre de variables ;
- du nombre de termes linguistiques ;
- de la forme des fonctions ;
- de la méthode d'inférence ;
- de la résolution numérique ;
- du matériel utilisé.

Les systèmes flous peuvent être efficaces, mais une base de règles volumineuse peut devenir coûteuse à évaluer.

# **17\. WORKFLOW DE CONCEPTION D'UN SYSTÈME FLOU**

## **Étape 1 — Définir le problème**

Préciser la décision à produire et la raison pour laquelle des catégories graduelles sont utiles.

Ne pas utiliser la logique floue uniquement parce qu'elle semble plus sophistiquée qu'un seuil classique.

## **Étape 2 — Identifier les variables**

Distinguer :

- entrées mesurées ;
- variables intermédiaires ;
- sorties ;
- contraintes ;
- variables de contexte.

Préciser les unités et les plages admissibles.

## **Étape 3 — Définir les catégories linguistiques**

Pour chaque variable, choisir les termes utiles.

Exemple :

- faible ;
- moyen ;
- élevé.

Le nombre de catégories doit rester suffisant pour représenter le phénomène sans rendre les règles excessivement complexes.

## **Étape 4 — Construire les fonctions d'appartenance**

Choisir les formes et paramètres.

Vérifier :

- la couverture du domaine ;
- les zones de chevauchement ;
- la signification des transitions ;
- les valeurs extrêmes ;
- les éventuelles zones sans activation.

## **Étape 5 — Choisir les opérateurs**

Décider comment combiner les conditions et les conséquences.

Documenter les conventions retenues.

## **Étape 6 — Écrire la base de règles**

Définir les relations entre les entrées et les sorties.

Rechercher les contradictions, les règles redondantes et les cas non couverts.

## **Étape 7 — Choisir le moteur d'inférence**

Mamdani est souvent adapté aux règles linguistiques.

Sugeno est souvent intéressant lorsque les sorties numériques et l'optimisation sont importantes.

Tsukamoto peut être adapté lorsque les fonctions de sortie monotones conviennent au problème.

## **Étape 8 — Définir la sortie**

Déterminer si le système doit produire :

- un ensemble flou ;
- un score ;
- une commande ;
- une catégorie ;
- une recommandation.

Si une valeur numérique est nécessaire, choisir la méthode de défuzzification.

## **Étape 9 — Définir les comportements de repli**

Préciser ce que le système doit faire si :

- aucune règle ne s'active ;
- les données sont invalides ;
- la sortie est indéfinie ;
- le système rencontre une situation inconnue ;
- une contrainte de sécurité est violée.

## **Étape 10 — Tester et calibrer**

Comparer les résultats aux attentes des experts, aux données de référence ou à un modèle de base.

Ajuster les paramètres en conservant une trace des modifications.

## **Étape 11 — Évaluer les performances**

Mesurer la qualité de la décision, la stabilité, le temps de calcul et la robustesse.

## **Étape 12 — Documenter les limites**

Décrire les hypothèses, les scénarios testés, les conditions de validité et les risques d'utilisation.

# **18\. FICHES DE RECONNAISSANCE : QUELLE NOTION UTILISER ?**

|     |     |
| --- | --- |
| **Situation observée** | **Notion à examiner** |
| Une catégorie possède des frontières graduelles | Ensemble flou |
| Il faut convertir une mesure en degré d'appartenance | Fonction d'appartenance |
| Un concept est décrit par plusieurs termes linguistiques | Variable linguistique |
| Il faut combiner plusieurs conditions graduelles | Opérateurs flous |
| Un expert exprime ses connaissances par des règles | Base de règles floues |
| Il faut transformer des règles en sortie | Système d'inférence floue |
| Les conséquences sont des ensembles linguistiques | Système de Mamdani |
| Les conséquences sont des fonctions numériques | Système de Sugeno |
| Les sorties de règles monotones sont combinées | Méthode de Tsukamoto |
| Une sortie floue doit devenir une valeur de commande | Défuzzification |
| Il faut ajuster une commande à partir de mesures | Contrôle flou |
| Il faut représenter une incertitude sur les fonctions elles-mêmes | Logique floue de type 2 |
| Il faut classer une observation dans plusieurs catégories avec des degrés | Classification floue |
| Il faut regrouper des données en groupes pouvant se chevaucher | Clustering flou |
| Les catégories sont graduelles, mais les événements sont aussi aléatoires | Combinaison raisonnée avec les probabilités |
| Les règles doivent être adaptées à partir de données | Système flou adaptatif ou neuro-flou |
| Les données sortent du domaine prévu | Gestion explicite des valeurs hors domaine |
| Une commande physique peut être dangereuse | Contrôle flou complété par des contraintes de sécurité |

# **19\. CATALOGUE D'APPROFONDISSEMENT**

## **U01 — Ensembles flous**

**Questions à approfondir :**

- Comment définir formellement un ensemble flou ?
- Comment calculer son support, son noyau et sa hauteur ?
- Comment interpréter les coupes alpha ?
- Quand un ensemble flou est-il normal ?
- Comment représenter un ensemble flou sur un univers continu ?

**Compétences visées :** représenter mathématiquement des concepts graduels.

## **U02 — Fonctions d'appartenance**

**Questions à approfondir :**

- Quand choisir une fonction triangulaire ou trapézoïdale ?
- Quand utiliser une fonction gaussienne ou sigmoïde ?
- Comment définir les paramètres ?
- Comment éviter les zones sans couverture ?
- Comment calibrer les fonctions à partir de données ?

**Compétences visées :** construire des catégories floues interprétables et adaptées au problème.

## **U03 — Variables linguistiques**

**Questions à approfondir :**

- Comment choisir les termes linguistiques ?
- Comment organiser une partition floue ?
- Comment formaliser les modificateurs comme « très » ?
- Comment éviter les catégories redondantes ?
- Comment vérifier la cohérence sémantique des ensembles ?

**Compétences visées :** transformer des connaissances qualitatives en représentations mathématiques.

## **U04 — Opérateurs flous**

**Questions à approfondir :**

- Quelles sont les propriétés d'une t-norme ?
- Quelles sont les propriétés d'une s-norme ?
- Comment comparer minimum et produit ?
- Comment choisir une négation ?
- Comment sélectionner une implication floue ?

**Compétences visées :** construire un moteur de raisonnement cohérent.

## **U05 — Règles floues**

**Questions à approfondir :**

- Comment formaliser un antécédent complexe ?
- Comment traiter plusieurs règles activées simultanément ?
- Comment détecter les contradictions ?
- Comment traiter les règles pondérées ?
- Comment gérer une base incomplète ?

**Compétences visées :** concevoir des systèmes experts flous.

## **U06 — Inférence de Mamdani**

**Questions à approfondir :**

- Comment calculer l'activation des règles ?
- Comment tronquer les conséquences ?
- Comment agréger les sorties ?
- Comment réaliser une défuzzification ?
- Comment tester la cohérence de la sortie ?

**Compétences visées :** développer des moteurs d'inférence interprétables.

## **U07 — Systèmes de Sugeno et Tsukamoto**

**Questions à approfondir :**

- Comment définir des sorties numériques ?
- Comment calculer les moyennes pondérées ?
- Comment gérer une somme de poids nulle ?
- Comment comparer le coût de calcul avec Mamdani ?
- Comment calibrer les paramètres ?

**Compétences visées :** construire des systèmes flous efficaces et adaptatifs.

## **U08 — Défuzzification**

**Questions à approfondir :**

- Comment calculer le centroïde ?
- Comment choisir une méthode de maximum ?
- Comment approximer les intégrales ?
- Comment gérer les sorties vides ?
- Comment mesurer la sensibilité aux paramètres ?

**Compétences visées :** transformer une représentation floue en décision numérique fiable.

## **U09 — Contrôle flou**

**Questions à approfondir :**

- Comment choisir les entrées et sorties d'un contrôleur ?
- Comment construire la base de règles ?
- Comment éviter les oscillations ?
- Comment comparer un contrôleur flou à un PID classique ?
- Comment tester la robustesse aux perturbations ?

**Compétences visées :** construire des contrôleurs et des systèmes automatisés.

## **U10 — Logique floue et décision**

**Questions à approfondir :**

- Comment combiner plusieurs critères ?
- Comment distinguer degrés d'appartenance et poids ?
- Comment définir un score global ?
- Comment analyser la sensibilité des résultats ?
- Comment présenter les raisons d'une décision ?

**Compétences visées :** développer des outils d'aide à la décision.

## **U11 — Logique floue et robotique**

**Questions à approfondir :**

- Comment transformer des mesures de distance en catégories floues ?
- Comment combiner plusieurs capteurs ?
- Comment choisir des commandes graduelles ?
- Comment gérer les situations dangereuses ?
- Comment tester les transitions de commande ?

**Compétences visées :** développer des contrôleurs pour robots et systèmes embarqués.

## **U12 — Systèmes neuro-flous**

**Questions à approfondir :**

- Comment apprendre les fonctions d'appartenance ?
- Comment ajuster les paramètres des règles ?
- Comment combiner réseaux de neurones et logique floue ?
- Comment préserver l'interprétabilité ?
- Comment comparer un modèle neuro-flou à un modèle non flou ?

**Compétences visées :** construire des systèmes hybrides d'apprentissage et de raisonnement.

# **20\. PROJETS ET EXPÉRIMENTATIONS PRATIQUES**

## **Projet 1 — Bibliothèque d'ensembles flous**

**Objectif :** créer une bibliothèque qui permet de définir et d'évaluer des fonctions d'appartenance.

Fonctionnalités :

- univers de discours ;
- fonctions triangulaires ;
- fonctions trapézoïdales ;
- fonctions gaussiennes ;
- fonctions sigmoïdes ;
- calcul des degrés ;
- validation des paramètres ;
- affichage des résultats ;
- gestion des valeurs hors domaine.

**Sans IA :** implémenter les fonctions et les tests unitaires.

**Avec IA :** demander une revue des cas limites et des propriétés mathématiques, puis vérifier les résultats avec des exemples calculés manuellement.

**Critère de réussite :** les fonctions respectent leur définition et renvoient des degrés dans _\[0,1\]\[0,1\]_.

## **Projet 2 — Système expert d'évaluation de risque**

**Objectif :** produire une évaluation graduelle à partir de plusieurs critères.

Entrées possibles :

- gravité ;
- fréquence ;
- exposition ;
- niveau de protection.

Sortie :

- priorité de traitement.

Étapes :

1.  définir les variables ;
2.  construire les ensembles flous ;
3.  définir les règles ;
4.  choisir le moteur d'inférence ;
5.  produire un score ;
6.  tester les cas extrêmes ;
7.  expliquer les règles qui influencent la sortie.

**Critère de réussite :** le système produit des évaluations cohérentes avec les règles documentées et permet de retracer ses décisions.

**Précaution :** pour une application de sécurité réelle, le système flou doit être validé et ne doit pas remplacer les obligations de conformité ou les contrôles impératifs.

## **Projet 3 — Contrôleur de ventilation**

**Objectif :** déterminer une commande de ventilation à partir de la température et de l'humidité.

Entrées :

- température ;
- humidité.

Sortie :

- puissance de ventilation.

Étapes :

1.  définir les domaines ;
2.  choisir les catégories linguistiques ;
3.  créer les fonctions d'appartenance ;
4.  écrire les règles ;
5.  implémenter Mamdani ;
6.  défuzzifier ;
7.  simuler des scénarios ;
8.  analyser la sensibilité.

**Extension :** comparer le système à un contrôleur à seuils fixes.

**Critère de réussite :** la commande évolue de manière cohérente sur les scénarios testés et ne présente pas de discontinuités injustifiées.

## **Projet 4 — Robot d'évitement d'obstacles**

**Objectif :** produire des commandes de mouvement à partir de mesures de distance.

Entrées :

- distance avant ;
- distance gauche ;
- distance droite.

Sorties :

- vitesse ;
- direction.

Étapes :

1.  simuler un environnement ;
2.  définir les ensembles flous de distance ;
3.  définir les règles ;
4.  calculer les commandes ;
5.  mesurer les collisions ;
6.  tester des obstacles variés ;
7.  comparer plusieurs configurations.

**Critère de réussite :** le robot évite les obstacles dans les scénarios de test sans utiliser des comportements arbitraires hors des cas prévus.

**Précaution :** une simulation réussie ne suffit pas à garantir la sécurité d'un robot réel.

## **Projet 5 — Système de recommandation multicritère**

**Objectif :** classer des options à partir de plusieurs critères graduels.

Exemple :

- prix raisonnable ;
- qualité élevée ;
- délai court ;
- proximité importante.

Le système attribue des degrés aux critères, applique des règles et produit un score de recommandation.

**Extension :** comparer le système flou à une somme pondérée classique.

**Critère de réussite :** expliquer pourquoi le classement change lorsque les préférences ou les fonctions d'appartenance sont modifiées.

## **Projet 6 — Comparaison Mamdani / Sugeno**

**Objectif :** implémenter deux moteurs d'inférence pour un même problème.

Comparer :

- précision ;
- coût de calcul ;
- stabilité des sorties ;
- interprétabilité ;
- facilité de calibration ;
- comportement aux frontières.

**Critère de réussite :** justifier le choix du moteur à partir de mesures plutôt que d'une préférence générale.

## **Projet 7 — Système neuro-flou**

**Objectif :** adapter les paramètres d'un système flou à partir de données.

Étapes :

1.  constituer un jeu de données ;
2.  définir les variables ;
3.  construire une base de règles initiale ;
4.  ajuster certains paramètres ;
5.  mesurer l'erreur ;
6.  comparer avant et après apprentissage ;
7.  vérifier l'interprétabilité.

**Critère de réussite :** montrer que l'adaptation améliore un indicateur mesurable sans rendre le système incohérent ou impossible à interpréter.

# **21\. EXPLORATION CRÉATIVE : SORTIR DES APPLICATIONS CLASSIQUES**

## **21.1. Agent intelligent à raisonnement hybride**

Concevoir un agent qui utilise :

- des règles strictes pour les contraintes obligatoires ;
- la logique floue pour évaluer les préférences ;
- un modèle probabiliste pour l'incertitude ;
- un moteur de planification pour choisir les actions.

Exemple : un robot doit respecter une contrainte de sécurité absolue tout en choisissant un itinéraire selon la proximité des obstacles, le confort du mouvement et la consommation énergétique.

La logique floue ne remplace pas les contraintes strictes. Elle contribue à évaluer les compromis à l'intérieur de l'espace des décisions admissibles.

## **21.2. Assistant de diagnostic explicable**

Construire un système qui transforme plusieurs indicateurs en un niveau de priorité.

L'assistant doit expliquer :

- les mesures utilisées ;
- les degrés d'appartenance ;
- les règles activées ;
- les facteurs qui influencent la sortie ;
- les limites du résultat.

Il faut distinguer un outil d'aide au diagnostic d'un système fournissant un diagnostic certifié ou médical.

## **21.3. Système de qualité logicielle**

Un moteur flou peut combiner des indicateurs tels que :

- complexité du code ;
- couverture de tests ;
- gravité des anomalies ;
- dette technique ;
- stabilité des versions.

La sortie peut être une priorité de revue ou de maintenance.

Le système doit éviter de transformer un score flou en vérité objective sur la qualité du logiciel.

## **21.4. Gestion adaptative des ressources informatiques**

Un système peut combiner :

- charge CPU ;
- utilisation mémoire ;
- latence ;
- urgence des requêtes ;
- coût de calcul.

Les règles orientent les décisions d'allocation de ressources.

Exemple :

- SI la charge est élevée ET la latence est forte, ALORS augmenter la capacité disponible ;
- SI la charge est faible ET le coût énergétique est élevé, ALORS réduire les ressources actives.

Une application réelle doit aussi intégrer les contraintes de capacité, les délais de démarrage et les mécanismes de protection contre les oscillations.

## **21.5. Système de négociation floue**

Un agent peut évaluer des offres selon des concepts graduels :

- prix acceptable ;
- délai satisfaisant ;
- qualité élevée ;
- risque faible.

La logique floue peut aider à calculer un score d'acceptabilité.

Cependant, ce score ne remplace pas la théorie des jeux : si plusieurs agents poursuivent des objectifs différents et réagissent les uns aux autres, il faut également modéliser les stratégies et les incitations.

## **21.6. Fusion d'indicateurs pour un agent de cybersécurité**

Un agent peut utiliser des degrés flous pour caractériser :

- activité inhabituelle ;
- fréquence élevée de requêtes ;
- comportement suspect ;
- niveau d'exposition ;
- gravité potentielle.

Le résultat peut orienter une analyse supplémentaire.

La logique floue ne prouve pas qu'une activité est malveillante. Il faut éviter de confondre un score de suspicion avec une probabilité de compromission.

## **21.7. Génération assistée de règles**

Un outil peut transformer des descriptions métier en propositions de règles floues.

Le workflow pourrait être :

1.  recueillir les définitions des experts ;
2.  identifier les variables ;
3.  proposer des catégories ;
4.  générer les fonctions d'appartenance ;
5.  construire les règles ;
6.  détecter les contradictions ;
7.  générer des tests ;
8.  soumettre les règles à validation.

Ce processus peut accélérer la conception, mais la validation finale doit rester fondée sur des critères explicites.

# **22\. LIENS AVEC LES AUTRES DOMAINES MATHÉMATIQUES**

|     |     |
| --- | --- |
| **Domaine** | **Relation avec la logique floue** |
| A — Logique et fondements | Formalisation des règles, connecteurs et raisonnements |
| B — Théorie des nombres | Applications spécialisées ; relation directe généralement limitée |
| C — Algèbre linéaire | Modèles numériques, systèmes hybrides et optimisation des paramètres |
| D — Géométrie computationnelle | Proximité graduelle, classification de formes et contrôle spatial |
| E — Théorie des graphes | Évaluation floue des liens, des risques ou des priorités dans un réseau |
| F — Combinatoire et optimisation combinatoire | Décisions multicritères et optimisation de règles |
| G — Probabilités | Complémentarité entre gradualité des concepts et incertitude aléatoire |
| H — Statistiques | Calibration, analyse de données et validation empirique |
| I — Calcul différentiel | Fonctions d'appartenance lisses et optimisation de paramètres |
| J — Optimisation | Ajustement des fonctions, des règles et des sorties |
| K — Fractales, chaos et systèmes dynamiques | Contrôle de certains systèmes non linéaires, sans garantie automatique de stabilité |
| L — Analyse numérique | Calcul du centroïde, discrétisation et approximation |
| M — Théorie de l'information | Traitement de l'incertitude, information et modèles hybrides |
| N — Transformées | Applications spécialisées au traitement de signaux avant leur interprétation floue |
| O — Théorie de la complexité | Analyse du coût des moteurs d'inférence et des bases de règles |
| P — Cryptographie | Applications indirectes ; la logique floue ne remplace pas les primitives cryptographiques |
| Q — Logique, automates et langages | Formalisation des règles et intégration dans les systèmes à états |
| R — Algèbre abstraite | Structures algébriques utiles à certaines généralisations de la logique |
| S — Topologie | Étude de certaines propriétés structurelles de fonctions et espaces ; relation surtout spécialisée |
| T — Théorie des jeux | Décision stratégique et comportements multi-agents, lorsque les intérêts des acteurs interagissent |

Les relations les plus directes pour les applications courantes sont généralement celles avec la logique, les fonctions, l'analyse numérique, l'optimisation, les statistiques, la théorie du contrôle et l'intelligence artificielle.

# **23\. ERREURS CONCEPTUELLES À ÉVITER**

## **23.1. Confondre degré d'appartenance et probabilité**

Un degré de _0,730{,}73_ à l'ensemble « chaude » n'indique pas automatiquement une probabilité de 73 %.

Cette confusion peut conduire à des interprétations incorrectes dans les systèmes de décision.

## **23.2. Utiliser la logique floue partout**

Si le problème nécessite une règle strictement binaire, la logique classique peut être plus simple et plus sûre.

Exemple : un paiement confirmé ou non confirmé ne doit pas être traité comme une appartenance graduelle sans justification particulière.

## **23.3. Définir arbitrairement les fonctions d'appartenance**

Les fonctions déterminent la manière dont les observations sont interprétées.

Des paramètres choisis sans justification peuvent rendre les résultats incohérents, même si le moteur d'inférence est correctement implémenté.

## **23.4. Confondre poids et degré d'appartenance**

Un poids exprime souvent l'importance d'un critère ou d'une règle.

Un degré d'appartenance exprime le degré de compatibilité d'une valeur avec un ensemble flou.

Les deux quantités peuvent être comprises entre _00_ et _11_, mais elles ne possèdent pas nécessairement la même signification.

## **23.5. Supposer qu'une sortie floue est toujours fiable**

Un système flou peut produire une valeur précise à partir d'un modèle incorrect.

La précision numérique ne garantit pas la validité du raisonnement.

## **23.6. Négliger les zones non couvertes**

Si aucune règle ne s'active, le système peut ne pas produire de sortie exploitable.

Il faut tester les valeurs extrêmes, les données manquantes et les situations non prévues.

## **23.7. Multiplier excessivement les règles**

Avec _nn_ variables comportant chacune _mm_ catégories, une base exhaustive peut atteindre :

_mnm^n_

combinaisons possibles, si toutes les catégories de chaque variable sont combinées.

Cette croissance rend les bases de règles difficiles à concevoir et à maintenir.

Il faut exploiter les dépendances utiles, simplifier les variables et éviter les combinaisons inutiles.

## **23.8. Ignorer la stabilité du contrôleur**

Un contrôleur flou n'est pas automatiquement stable.

Les délais, les saturations, les perturbations, les dynamiques du système et les règles peuvent produire des oscillations ou des réponses inadéquates.

## **23.9. Confondre interprétabilité et vérité**

Une règle linguistique est souvent facile à lire, mais elle peut être erronée.

La transparence du modèle facilite l'audit ; elle ne remplace pas la validation.

## **23.10. Négliger les contraintes de sécurité**

Dans les applications physiques ou sensibles, la logique floue doit être associée à des mécanismes qui imposent les limites impératives.

Les contraintes de sécurité ne doivent pas dépendre uniquement d'une règle floue susceptible de s'activer partiellement.

# **24\. MENTAL MODEL — COMMENT RAISONNER AVEC LA LOGIQUE FLOUE**

Pour analyser un problème, suivre les questions suivantes.

**1\. Le concept est-il réellement graduel ?**

Vérifier si les catégories possèdent des frontières floues ou si une règle binaire suffit.

**2\. Quelle est la variable mesurée ?**

Définir son unité, son domaine et les valeurs admissibles.

**3\. Quels termes linguistiques décrivent la situation ?**

Choisir les catégories qui ont un sens pour l'expert ou l'utilisateur.

**4\. Comment calculer les degrés ?**

Définir les fonctions d'appartenance et leurs paramètres.

**5\. Comment combiner les conditions ?**

Choisir les opérateurs flous selon la sémantique souhaitée.

**6\. Quelles règles relient les entrées aux sorties ?**

Formaliser les connaissances et vérifier les contradictions.

**7\. Quel moteur d'inférence convient ?**

Choisir Mamdani, Sugeno, Tsukamoto ou une autre formulation adaptée.

**8\. La sortie doit-elle être numérique ?**

Si oui, définir la méthode de défuzzification ou le mécanisme de calcul numérique.

**9\. Comment le système réagit-il aux cas inhabituels ?**

Prévoir les entrées invalides, les zones non couvertes et les règles non activées.

**10\. Comment vérifier que le système est utile ?**

Comparer ses résultats à une référence et mesurer sa robustesse.

**11\. Les résultats ont-ils été interprétés correctement ?**

Ne pas confondre degré d'appartenance, probabilité, poids et confiance.

**12\. La logique floue est-elle la meilleure méthode ?**

Comparer les avantages et les limites d'un modèle flou avec ceux d'une règle classique, d'un modèle probabiliste ou d'un système appris.

La logique floue ne consiste pas à rendre les décisions arbitraires. Elle consiste à formaliser progressivement des concepts qui ne possèdent pas naturellement des frontières strictes.

# **25\. SYNTHÈSE DES IDÉES ESSENTIELLES**

1.  La logique floue permet de représenter des degrés d'appartenance à des concepts.
2.  Un ensemble flou est défini par une fonction d'appartenance prenant ses valeurs dans _\[0,1\]\[0,1\]_.
3.  Le degré d'appartenance n'est pas automatiquement une probabilité.
4.  Les fonctions d'appartenance déterminent comment les valeurs numériques sont interprétées.
5.  Les variables linguistiques associent des termes qualitatifs à des ensembles flous.
6.  Les opérateurs flous permettent de combiner des degrés.
7.  Les choix d'opérateurs peuvent modifier les résultats.
8.  Les règles floues représentent des connaissances sous forme de conditions et de conséquences.
9.  Le moteur d'inférence transforme les règles en résultats.
10. Mamdani utilise généralement des conséquences floues.
11. Sugeno utilise généralement des conséquences numériques.
12. Tsukamoto repose sur des conséquences à fonctions d'appartenance monotones.
13. La défuzzification transforme une sortie floue en valeur numérique lorsqu'elle est nécessaire.
14. Le contrôle flou permet de convertir des mesures en commandes graduelles.
15. Les systèmes experts flous rendent certaines connaissances qualitatives calculables.
16. La logique floue peut être utilisée en robotique, en contrôle, en décision et en IA.
17. Les fonctions et les règles doivent être calibrées et validées.
18. Une sortie numérique précise n'est pas nécessairement correcte.
19. La logique floue ne remplace pas les règles strictes de sécurité.
20. Les modèles flous peuvent être combinés aux probabilités, à l'optimisation et à l'apprentissage automatique.
21. Le nombre de règles peut croître rapidement avec le nombre de variables.
22. Le choix du modèle doit être justifié par le problème, pas par la sophistication apparente de la méthode.

# **26\. CHECKLIST DE MAÎTRISE DU DOMAINE U**

## **Fondements**

- Je sais distinguer logique classique, logique floue et probabilités.
- Je sais définir un ensemble flou.
- Je sais expliquer la signification d'un degré d'appartenance.
- Je sais définir un univers de discours.
- Je sais calculer le support, le noyau et une coupe alpha.
- Je sais expliquer les différences entre les ensembles flous de type 1 et de type 2.

## **Fonctions et variables linguistiques**

- Je sais implémenter une fonction triangulaire.
- Je sais implémenter une fonction trapézoïdale.
- Je sais utiliser une fonction gaussienne ou sigmoïde.
- Je sais choisir les paramètres d'une fonction.
- Je sais construire une variable linguistique.
- Je sais expliquer l'effet du chevauchement des fonctions.

## **Opérateurs et règles**

- Je sais calculer une conjonction par minimum ou par produit.
- Je sais calculer une disjonction par maximum.
- Je sais appliquer une négation standard.
- Je sais expliquer le rôle des implications floues.
- Je sais calculer le degré d'activation d'une règle.
- Je sais identifier les contradictions et les zones non couvertes.

## **Systèmes d'inférence**

- Je sais décrire les étapes d'un système flou.
- Je sais expliquer la méthode de Mamdani.
- Je sais expliquer la méthode de Sugeno.
- Je sais identifier les contraintes propres à Tsukamoto.
- Je sais calculer une défuzzification par centroïde.
- Je sais traiter le cas où aucune règle ne s'active.

## **Applications informatiques**

- Je sais construire un système expert flou.
- Je sais concevoir un petit contrôleur flou.
- Je sais comparer un système flou à un système à seuils.
- Je sais tester la robustesse aux valeurs extrêmes.
- Je sais versionner les règles et les paramètres.
- Je sais distinguer un score flou d'une probabilité de risque.
- Je sais définir les limites de sécurité et le comportement de repli.

# **27\. ÉPREUVE FINALE DE MAÎTRISE**

Pour considérer le domaine comme suffisamment maîtrisé pour un projet informatique, il faut pouvoir réaliser les tâches suivantes sans se limiter à reproduire une définition.

## **Épreuve A — Formalisation mathématique**

Définir une variable linguistique, son univers de discours et au moins trois fonctions d'appartenance.

Calculer les degrés obtenus pour plusieurs valeurs et expliquer les transitions entre catégories.

## **Épreuve B — Moteur de règles**

Créer une base de règles utilisant plusieurs variables.

Calculer les degrés d'activation avec différents opérateurs et expliquer pourquoi les résultats peuvent changer.

## **Épreuve C — Système d'inférence**

Implémenter un moteur de Mamdani ou de Sugeno.

Vérifier le résultat sur des exemples calculés manuellement et tester les cas sans activation.

## **Épreuve D — Décision ou contrôle**

Construire un système qui transforme plusieurs mesures en une décision ou une commande.

Comparer ses résultats à une méthode classique à seuils fixes.

Expliquer les avantages, les coûts et les limites de l'approche floue.

## **Épreuve E — Validation expérimentale**

Construire un ensemble de scénarios incluant :

- valeurs habituelles ;
- valeurs aux frontières ;
- valeurs extrêmes ;
- données invalides ;
- situations non prévues.

Mesurer les performances, les changements de sortie et la robustesse.

## **Épreuve F — Analyse critique**

Présenter un système intelligent utilisant la logique floue.

Expliquer :

- les variables ;
- les fonctions d'appartenance ;
- les règles ;
- les opérateurs ;
- le moteur d'inférence ;
- la méthode de sortie ;
- les résultats mesurés ;
- les limites ;
- les conditions d'échec ;
- les protections nécessaires.

La maîtrise du domaine suppose de savoir construire un modèle dont le comportement est compréhensible, mesurable et adapté au problème.

# **28\. CONCLUSION GÉNÉRALE**

La logique floue fournit un cadre mathématique pour représenter des concepts graduels et transformer des connaissances qualitatives en calculs exploitables par un logiciel.

Elle est particulièrement pertinente lorsque des experts peuvent décrire le comportement souhaité en termes comme « faible », « élevé », « proche », « risqué » ou « suffisamment bon », mais que le système doit produire une décision numérique ou une commande concrète.

Son intérêt pour l'intelligence artificielle, la robotique, les systèmes experts et le contrôle réside dans la possibilité de relier des descriptions linguistiques à des mécanismes de calcul explicites.

Pour un ingénieur logiciel, sa valeur se situe dans la capacité à construire des systèmes qui gèrent des transitions progressives entre catégories, combinent des règles métier et expliquent les contributions des différents critères.

La démarche exige néanmoins de la rigueur. Les fonctions d'appartenance doivent être justifiées, les règles doivent être cohérentes et les sorties doivent être validées. Un système flou n'est ni automatiquement intelligent, ni automatiquement robuste, ni nécessairement supérieur à une méthode classique.

Il est utile de distinguer trois niveaux :

1.  **La représentation :** comment les concepts graduels sont décrits par des ensembles et des fonctions d'appartenance.
2.  **Le raisonnement :** comment les opérateurs et les règles transforment les observations en résultats.
3.  **L'application informatique :** comment le système utilise ces résultats pour décider, contrôler, recommander ou agir.

Ces trois niveaux doivent rester cohérents avec l'objectif réel.

**Principe directeur du domaine U :** lorsqu'une situation ne se laisse pas naturellement découper en catégories strictement binaires, la logique floue permet de représenter les degrés intermédiaires, de formaliser les règles qualitatives et de transformer ces représentations en décisions calculables — à condition de définir clairement leur signification et de valider leur comportement.