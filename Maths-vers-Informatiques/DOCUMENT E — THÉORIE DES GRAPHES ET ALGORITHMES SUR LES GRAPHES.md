# **DOCUMENT E — THÉORIE DES GRAPHES ET ALGORITHMES SUR LES GRAPHES**

## **Cartographie complète pour l’informatique, les algorithmes, les systèmes, les réseaux, le Web et l’intelligence artificielle**

# **0 — IDENTITÉ DU DOMAINE**

## **0.1 Définition générale**

La **théorie des graphes** est la branche des mathématiques discrètes qui étudie des structures composées principalement :

- d’objets appelés **sommets** ;
- de relations entre ces objets appelées **arêtes**.

Un graphe permet donc de représenter une situation dans laquelle des éléments entretiennent des relations.

Formellement, un graphe non orienté peut être représenté par :

_G=(V,E)G=(V,E)_

où :

- _VV_ est l’ensemble des sommets ;
- _EE_ est l’ensemble des arêtes.

Pour un graphe orienté :

_G=(V,A)G=(V,A)_

où _AA_ représente les arcs orientés.

## **0.2 Pourquoi les graphes sont fondamentaux en informatique**

Une immense quantité de problèmes informatiques peut être reformulée sous forme de graphe.

Exemples :

Pages Web  
↓  
liens hypertextes  
↓  
Graphe  
<br/>Utilisateurs  
↓  
relations sociales  
↓  
Graphe  
<br/>Ordinateurs  
↓  
connexions réseau  
↓  
Graphe  
<br/>Tâches  
↓  
dépendances  
↓  
Graphe  
<br/>États d'un système  
↓  
transitions  
↓  
Graphe  
<br/>Villes  
↓  
routes  
↓  
Graphe  
<br/>Objets 3D  
↓  
relations de voisinage  
↓  
Graphe  
<br/>Entités IA  
↓  
relations sémantiques  
↓  
Graphe  

La théorie des graphes fournit donc une abstraction permettant de transformer un problème complexe en :

Objets  
+  
Relations  
+  
Contraintes  
+  
Parcours  
+  
Optimisation  

# **1 — PLACE DU DOMAINE E DANS LA CARTOGRAPHIE MATHÉMATIQUE**

La progression globale peut être comprise ainsi :

A — LOGIQUE ET FONDEMENTS  
↓  
raisonner sur les objets et les propositions  
<br/>B — THÉORIE DES NOMBRES  
↓  
raisonner sur les structures discrètes numériques  
<br/>C — ALGÈBRE LINÉAIRE / GÉOMÉTRIE LINÉAIRE  
↓  
représenter et transformer les espaces  
<br/>D — GÉOMÉTRIE COMPUTATIONNELLE  
↓  
raisonner sur les relations spatiales  
<br/>E — THÉORIE DES GRAPHES  
↓  
raisonner sur les relations discrètes  
<br/>F — COMBINATOIRE  
↓  
compter et analyser les structures discrètes  
<br/>...  

Le domaine E est donc le grand domaine des **relations discrètes**.

# **2 — CARTOGRAPHIE GLOBALE DU DOMAINE**

La théorie des graphes peut être organisée en grandes familles.

## **Famille A — Fondations des graphes**

- sommets ;
- arêtes ;
- arcs ;
- voisinage ;
- degré ;
- ordre ;
- taille ;
- sous-graphes ;
- graphes simples ;
- multigraphes ;
- graphes pondérés.

## **Famille B — Graphes orientés et non orientés**

- graphes non orientés ;
- graphes orientés ;
- graphes mixtes ;
- graphes acycliques ;
- DAG ;
- graphes complets ;
- graphes bipartis ;
- graphes réguliers ;
- graphes planaires.

## **Famille C — Parcours**

- parcours ;
- chemin ;
- marche ;
- sentier ;
- cycle ;
- circuit ;
- BFS ;
- DFS.

## **Famille D — Connexité**

- composantes connexes ;
- forte connexité ;
- faible connexité ;
- ponts ;
- points d'articulation ;
- composantes fortement connexes.

## **Famille E — Arbres**

- arbres ;
- racines ;
- feuilles ;
- profondeur ;
- hauteur ;
- arbres binaires ;
- arbres couvrants ;
- arbres couvrants minimaux ;
- arbres de recherche ;
- arbres de dépendances.

## **Famille F — Plus courts chemins**

- chemins pondérés ;
- Dijkstra ;
- Bellman-Ford ;
- Floyd-Warshall ;
- A\* ;
- chemins négatifs ;
- cycles négatifs ;
- distances entre tous les couples.

## **Famille G — Arbres couvrants minimaux**

- Kruskal ;
- Prim ;
- Union-Find ;
- propriétés des MST.

## **Famille H — Coloration**

- coloration des sommets ;
- coloration des arêtes ;
- nombre chromatique ;
- graphes bipartis ;
- coloration gloutonne ;
- applications à l'allocation de ressources.

## **Famille I — Flots**

- réseau de flot ;
- source ;
- puits ;
- capacité ;
- flux ;
- coupe ;
- flot maximal ;
- coupe minimale ;
- Ford-Fulkerson ;
- Edmonds-Karp.

## **Famille J — Couplages**

- couplage ;
- couplage maximal ;
- couplage maximum ;
- couplage parfait ;
- graphes bipartis ;
- algorithmes de matching.

## **Famille K — Graphes de dépendances**

- DAG ;
- ordre topologique ;
- dépendances ;
- planification ;
- compilation ;
- pipelines ;
- gestion de packages ;
- workflows.

## **Famille L — Graphes avancés**

- graphes planaires ;
- graphes de flot ;
- graphes de connaissances ;
- graphes aléatoires ;
- graphes dynamiques ;
- hypergraphes ;
- graphes temporels ;
- graphes probabilistes.

## **Famille M — Structures de données pour graphes**

- matrice d'adjacence ;
- liste d'adjacence ;
- liste d'arêtes ;
- représentation CSR ;
- heaps ;
- Union-Find ;
- structures spécialisées pour les graphes dynamiques.

## **Famille N — Applications informatiques**

- réseaux ;
- Web ;
- systèmes distribués ;
- bases de données ;
- compilateurs ;
- moteurs de recherche ;
- navigation ;
- systèmes de recommandation ;
- IA ;
- computer vision ;
- robotique ;
- jeux vidéo ;
- moteurs 3D.

# **3 — VOCABULAIRE FONDAMENTAL**

## **3.1 Sommet**

Un **sommet** représente une entité.

Exemple :

Utilisateur  
Serveur  
Ville  
Page Web  
Tâche  
État  
Produit  

On peut écrire :

_V={A,B,C,D}V=\\{A,B,C,D\\}_

## **3.2 Arête**

Une arête représente une relation entre deux sommets.

Dans un graphe non orienté :

_{A,B}\\{A,B\\}_

signifie que _AA_ et _BB_ sont connectés.

## **3.3 Arc**

Dans un graphe orienté :

_(A,B)(A,B)_

indique une relation allant de _AA_ vers _BB_.

A ───→ B  

La relation inverse n'est pas automatiquement présente.

## **3.4 Ordre d'un graphe**

Le nombre de sommets :

_∣V∣|V|_

est appelé l'ordre du graphe.

## **3.5 Taille d'un graphe**

Le nombre d'arêtes :

_∣E∣|E|_

est la taille du graphe.

## **3.6 Voisins**

Deux sommets sont voisins lorsqu'ils sont reliés directement.

A ─── B  

_AA_ et _BB_ sont voisins.

# **4 — TYPES DE GRAPHES**

## **4.1 Graphe simple**

Un graphe simple ne possède :

- ni boucle ;
- ni arêtes multiples entre deux mêmes sommets.

## **4.2 Graphe multigraphe**

Plusieurs arêtes peuvent relier les mêmes sommets.

A ═══ B  
\\\___/  

## **4.3 Graphe orienté**

Chaque relation possède une direction.

A → B → C  

## **4.4 Graphe non orienté**

Les relations sont symétriques.

A ─ B ─ C  

## **4.5 Graphe pondéré**

Chaque arête possède un poids.

A ──5── B ──2── C  

Le poids peut représenter :

- distance ;
- coût ;
- temps ;
- latence ;
- énergie ;
- risque ;
- prix ;
- capacité.

## **4.6 Graphe complet**

Un graphe complet _KnK_n_ possède une arête entre chaque paire de sommets.

Nombre d'arêtes :

_∣E∣=n(n−1)2|E|=\\frac{n(n-1)}{2}_

pour un graphe simple non orienté.

## **4.7 Graphe biparti**

Les sommets peuvent être divisés en deux ensembles :

_V=A∪BV=A\\cup B_

avec :

_A∩B=∅A\\cap B=\\varnothing_

et aucune arête entre deux sommets du même ensemble.

A1 ─── B1  
A1 ─── B2  
A2 ─── B2  

Applications :

- matching ;
- affectation ;
- recommandation ;
- recrutement ;
- allocation de ressources.

## **4.8 Graphe régulier**

Tous les sommets possèdent le même degré.

Un graphe _kk_\-régulier vérifie :

_deg(v)=kdeg(v)=k_

pour tout sommet _vv_.

## **4.9 DAG**

DAG signifie :

**Directed Acyclic Graph**

C'est un graphe :

- orienté ;
- sans cycle dirigé.

Exemple :

A → B → D  
\\ ↑  
→ C ───┘  

Les DAG sont extrêmement importants en informatique.

Applications :

- dépendances ;
- compilation ;
- pipelines ;
- workflows ;
- scheduling ;
- systèmes de build ;
- graphes de tâches.

# **5 — DEGRÉS**

## **5.1 Degré dans un graphe non orienté**

Le degré d'un sommet _vv_ est :

_deg(v)deg(v)_

C'est le nombre d'arêtes incidentes à _vv_.

## **5.2 Degré entrant**

Dans un graphe orienté :

_deg−(v)deg^-(v)_

désigne le nombre d'arcs entrants.

## **5.3 Degré sortant**

_deg+(v)deg^+(v)_

désigne le nombre d'arcs sortants.

## **5.4 Identité fondamentale**

Dans un graphe non orienté :

_∑v∈Vdeg(v)=2∣E∣\\sum_{v\\in V}deg(v)=2|E|_

C'est le **lemme de la poignée de main**.

Chaque arête contribue deux fois à la somme des degrés.

# **6 — MARCHES, CHEMINS ET CYCLES**

Ces notions doivent être distinguées.

## **6.1 Marche**

Une marche peut réutiliser des sommets et des arêtes.

## **6.2 Sentier**

Un sentier ne réutilise pas une arête.

## **6.3 Chemin**

Un chemin est une succession de sommets reliés.

Dans de nombreuses conventions informatiques, on réserve le terme chemin à une séquence sans répétition de sommets.

## **6.4 Cycle**

Un cycle revient au sommet de départ.

A  
│\\  
│ \\  
B──C  

## **6.5 Cycle dirigé**

Dans un graphe orienté :

A → B  
↑ ↓  
D ← C  

# **7 — CONNECTIVITÉ**

## **7.1 Graphe connexe**

Un graphe non orienté est connexe si tout sommet peut atteindre tout autre sommet.

## **7.2 Composante connexe**

Une composante connexe est une partie maximale du graphe dans laquelle tous les sommets sont mutuellement accessibles.

## **7.3 Connexité forte**

Dans un graphe orienté, deux sommets appartiennent à la même composante fortement connexe si chacun peut atteindre l'autre.

## **7.4 Connexité faible**

Un graphe orienté est faiblement connexe lorsque son graphe sous-jacent non orienté est connexe.

# **8 — PONTS ET POINTS D'ARTICULATION**

## **8.1 Pont**

Une arête est un **pont** si sa suppression augmente le nombre de composantes connexes.

Exemple :

A ─ B ─ C  

L'arête _B−CB-C_ est critique si elle constitue l'unique connexion vers _CC_.

## **8.2 Point d'articulation**

Un sommet est un point d'articulation si sa suppression déconnecte le graphe.

Applications :

- analyse de réseaux ;
- infrastructure ;
- réseaux informatiques ;
- résilience ;
- détection de points critiques.

# **9 — ARBRES**

## **9.1 Définition**

Un arbre est un graphe :

- non orienté ;
- connexe ;
- acyclique.

## **9.2 Propriété fondamentale**

Un arbre à _nn_ sommets possède exactement :

_n−1n-1_

arêtes.

## **9.3 Propriétés équivalentes**

Pour un graphe ayant _nn_ sommets, les propriétés suivantes sont liées :

connexe + n−1 arêtes  
⇅  
acyclique + n−1 arêtes  
⇅  
connexe + acyclique  

## **9.4 Racine**

Un arbre enraciné possède un sommet choisi comme racine.

## **9.5 Parent / enfant**

A  
/ \\  
B C  
/ \\  
D E  

_AA_ est parent de _BB_ et _CC_.

_BB_ est parent de _DD_ et _EE_.

## **9.6 Feuille**

Un sommet sans enfant.

## **9.7 Profondeur**

La profondeur d'un sommet est sa distance depuis la racine.

## **9.8 Hauteur**

La hauteur de l'arbre correspond à la profondeur maximale.

# **10 — ARBRES COUVRANTS**

Un arbre couvrant d'un graphe connexe est un arbre contenant :

- tous les sommets ;
- suffisamment d'arêtes pour rester connexe ;
- aucune arête inutile formant un cycle.

## **10.1 Minimum Spanning Tree**

Dans un graphe pondéré, un **MST** est un arbre couvrant de poids total minimal.

Deux algorithmes fondamentaux :

- Kruskal ;
- Prim.

# **11 — REPRÉSENTATIONS INFORMATIQUES DES GRAPHES**

## **11.1 Matrice d'adjacence**

Pour _nn_ sommets :

_AijA_{ij}_

indique si _ii_ et _jj_ sont reliés.

Exemple :

A B C  
A 0 1 1  
B 1 0 0  
C 1 0 0  

Complexité mémoire :

_O(V2)O(V^2)_

Avantage :

_O(1)O(1)_

pour tester l'existence d'une arête.

## **11.2 Liste d'adjacence**

A → B, C  
B → A  
C → A  

Mémoire :

_O(V+E)O(V+E)_

Très adaptée aux graphes creux.

## **11.3 Liste d'arêtes**

(A,B)  
(A,C)  
(B,D)  

Simple et utile notamment pour :

- Kruskal ;
- Bellman-Ford ;
- traitement de données de graphes.

## **11.4 CSR**

**Compressed Sparse Row**

Structure importante pour les grands graphes creux.

Applications :

- calcul scientifique ;
- GPU ;
- graphes massifs ;
- IA ;
- bases de données.

# **12 — BFS : BREADTH-FIRST SEARCH**

## **12.1 Principe**

BFS explore le graphe couche par couche.

A  
/ | \\  
B C D  
/ \\  
E F  

Ordre possible :

A  
B C D  
E F  

## **12.2 Structure utilisée**

BFS utilise une **file**.

QUEUE  
<br/>entrée → \[B\]\[C\]\[D\] → sortie  

## **12.3 Complexité**

Avec une liste d'adjacence :

_O(V+E)O(V+E)_

## **12.4 Applications**

- plus court chemin non pondéré ;
- distance minimale en nombre d'arêtes ;
- exploration ;
- niveaux ;
- détection de composantes ;
- bipartition ;
- propagation ;
- recherche dans un état discret.

# **13 — DFS : DEPTH-FIRST SEARCH**

## **13.1 Principe**

DFS explore aussi profondément que possible avant de revenir en arrière.

A  
↓  
B  
↓  
E  
↓  
retour  

## **13.2 Structure utilisée**

DFS peut utiliser :

- une pile ;
- la récursion.

## **13.3 Complexité**

_O(V+E)O(V+E)_

avec une liste d'adjacence.

## **13.4 Applications**

- détection de cycles ;
- composantes ;
- topological sort ;
- ponts ;
- points d'articulation ;
- SCC ;
- exploration de labyrinthes ;
- analyse de dépendances.

# **14 — BFS VS DFS**

|     |     |     |
| --- | --- | --- |
| **Aspect** | **BFS** | **DFS** |
| Structure | File | Pile/récursion |
| Exploration | par niveaux | en profondeur |
| Plus court chemin non pondéré | Oui | Non, en général |
| Détection de cycle | Oui | Oui |
| Topological sort | Non standard | Oui |
| SCC | Indirect | Fondamental |
| Mémoire | potentiellement élevée | dépend de la profondeur |

Le choix dépend du **problème**, pas d'une préférence personnelle.

# **15 — ORDRE TOPOLOGIQUE**

Un ordre topologique est un ordre des sommets d'un DAG tel que :

_u→vu\\rightarrow v_

implique que _uu_ apparaît avant _vv_.

Exemple :

HTML  
↓  
CSS  
↓  
React  
↓  
Application  

## **15.1 Applications**

- compilation ;
- dépendances npm ;
- Make ;
- CI/CD ;
- planification ;
- cours avec prérequis ;
- pipelines ;
- workflows.

## **15.2 Algorithmes**

Deux grandes approches :

### **DFS**

Utiliser les temps de sortie.

### **Kahn**

Utiliser les degrés entrants.

Structure principale :

queue des sommets de degré entrant nul  

Complexité :

_O(V+E)O(V+E)_

# **16 — PLUS COURT CHEMIN**

Le problème général consiste à trouver un chemin minimisant :

_∑w(e)\\sum w(e)_

où _w(e)w(e)_ est le poids de chaque arête.

# **17 — DIJKSTRA**

## **17.1 Conditions**

Dijkstra est adapté lorsque les poids sont :

_w(e)≥0w(e)\\geq0_

## **17.2 Principe**

À chaque étape :

1.  sélectionner le sommet non traité ayant la plus petite distance ;
2.  considérer ses voisins ;
3.  effectuer une relaxation.

## **17.3 Relaxation**

Si :

_dist\[v\]>dist\[u\]+w(u,v)dist\[v\]>dist\[u\]+w(u,v)_

alors :

_dist\[v\]=dist\[u\]+w(u,v)dist\[v\]=dist\[u\]+w(u,v)_

## **17.4 Structure**

Avec une file de priorité / heap :

_O((V+E)log⁡V)O((V+E)\\log V)_

selon l'implémentation.

## **17.5 Applications**

- navigation ;
- routage ;
- jeux vidéo ;
- robotique ;
- réseaux ;
- systèmes de recommandation ;
- recherche de trajectoires.

# **18 — BELLMAN-FORD**

Bellman-Ford accepte les poids négatifs.

Il peut également détecter les cycles négatifs accessibles depuis la source.

Complexité :

_O(VE)O(VE)_

## **Comparaison**

Dijkstra  
→ poids non négatifs  
→ généralement plus rapide  
<br/>Bellman-Ford  
→ poids négatifs possibles  
→ détecte les cycles négatifs  

# **19 — FLOYD-WARSHALL**

Floyd-Warshall calcule les distances minimales entre **toutes les paires** de sommets.

Complexité :

_O(V3)O(V^3)_

Mémoire typique :

_O(V2)O(V^2)_

## **Principe**

Il repose sur une programmation dynamique.

On cherche progressivement :

quel est le meilleur chemin entre _ii_ et _jj_ si l'on autorise certains sommets intermédiaires ?

Relation fondamentale :

_Dij(k)=min⁡(Dij(k−1),Dik(k−1)+Dkj(k−1))D_{ij}^{(k)} = \\min \\left( D_{ij}^{(k-1)}, D_{ik}^{(k-1)}+D_{kj}^{(k-1)} \\right)_

# **20 — A\***

A\* combine :

- coût déjà parcouru ;
- estimation du coût restant.

Fonction :

_f(n)=g(n)+h(n)f(n)=g(n)+h(n)_

où :

- _g(n)g(n)_ = coût depuis le départ ;
- _h(n)h(n)_ = heuristique vers l'objectif ;
- _f(n)f(n)_ = estimation totale.

## **20.1 Heuristique admissible**

Une heuristique est admissible si elle ne surestime pas le coût réel.

_h(n)≤h∗(n)h(n)\\leq h^\*(n)_

## **20.2 Applications**

- jeux ;
- navigation ;
- robotique ;
- pathfinding ;
- interfaces interactives ;
- mondes 2D/3D.

# **21 — COMPARAISON DES ALGORITHMES DE CHEMIN**

|     |     |     |     |
| --- | --- | --- | --- |
| **Algorithme** | **Poids négatifs** | **Tous couples** | **Heuristique** |
| BFS | Non pondéré | Non | Non |
| Dijkstra | Non | Non | Non |
| Bellman-Ford | Oui | Non | Non |
| Floyd-Warshall | Oui, selon conditions | Oui | Non |
| A\* | généralement non négatif | Non | Oui |

# **22 — KRUSKAL**

Kruskal construit un arbre couvrant minimal.

## **Principe**

1.  Trier les arêtes par poids croissant.
2.  Ajouter une arête si elle ne crée pas de cycle.
3.  Arrêter lorsque _V−1V-1_ arêtes sont sélectionnées.

## **Structure fondamentale**

**Union-Find / Disjoint Set Union**

Opérations :

- find
- union

Avec compression de chemin et union par rang/taille, les opérations sont extrêmement efficaces en pratique.

## **Complexité dominante**

Tri :

_O(Elog⁡E)O(E\\log E)_

# **23 — PRIM**

Prim construit progressivement un MST.

Il part d'un sommet puis ajoute à chaque étape l'arête de plus faible coût reliant :

arbre courant  
↓  
sommet extérieur  

Avec un heap :

_O(Elog⁡V)O(E\\log V)_

selon la représentation.

# **24 — KRUSKAL VS PRIM**

|     |     |     |
| --- | --- | --- |
| **Critère** | **Kruskal** | **Prim** |
| Stratégie | arêtes globales | expansion |
| Structure clé | Union-Find | Priority Queue |
| Tri des arêtes | Oui | Pas nécessaire |
| Très adapté aux graphes clairsemés | Oui | Oui |
| Fonctionne sur graphe connexe | Oui | Oui |

# **25 — COLORATION DES GRAPHES**

Une coloration des sommets attribue des couleurs aux sommets de manière que deux sommets adjacents aient des couleurs différentes.

## **25.1 Nombre chromatique**

Le nombre minimal de couleurs nécessaires est :

_χ(G)\\chi(G)_

## **25.2 Graphe biparti**

Un graphe est biparti si et seulement s'il peut être colorié avec deux couleurs.

Une caractérisation fondamentale :

Un graphe est biparti si et seulement s'il ne contient aucun cycle impair.

## **25.3 Applications**

- allocation de fréquences ;
- registres CPU ;
- scheduling ;
- attribution de ressources ;
- planification ;
- conflits de contraintes ;
- affectation de créneaux.

# **26 — COLORATION GLOUTONNE**

On traite les sommets selon un ordre donné et on attribue à chacun la plus petite couleur disponible.

Cette méthode est :

- simple ;
- rapide ;
- souvent utile en pratique ;

mais elle ne garantit pas toujours le nombre chromatique optimal.

# **27 — FLOTS DANS LES GRAPHES**

Un réseau de flot possède généralement :

Source  
↓  
réseau  
↓  
Puits  

Chaque arête possède une capacité :

_c(u,v)c(u,v)_

Le flot doit respecter :

_0≤f(u,v)≤c(u,v)0\\leq f(u,v)\\leq c(u,v)_

et la conservation du flot aux sommets intermédiaires.

# **28 — FLOt MAXIMAL**

Objectif :

_max⁡∣f∣\\max |f|_

où _∣f∣|f|_ est le flux total allant de la source au puits.

# **29 — FORD-FULKERSON**

Principe :

1.  trouver un chemin augmentant ;
2.  augmenter le flot ;
3.  mettre à jour le graphe résiduel ;
4.  recommencer.

# **30 — EDMONDS-KARP**

Edmonds-Karp est une implémentation de Ford-Fulkerson utilisant BFS pour rechercher les chemins augmentants.

Complexité :

_O(VE2)O(VE^2)_

# **31 — THÉORÈME MAX-FLOW MIN-CUT**

Une idée fondamentale :

_Flot maximal=Coupe minimale\\boxed{\\text{Flot maximal}=\\text{Coupe minimale}}_

La valeur maximale du flot entre source et puits est égale à la capacité minimale d'une coupe séparant la source du puits.

Applications :

- réseaux ;
- bande passante ;
- logistique ;
- allocation ;
- segmentation d'images ;
- systèmes distribués.

# **32 — COUPLAGE**

Un couplage est un ensemble d'arêtes ne partageant aucun sommet.

A ─ B  
<br/>C ─ D  

Ces deux arêtes forment un couplage.

## **32.1 Couplage maximal**

Un couplage auquel on ne peut plus ajouter d'arête.

## **32.2 Couplage maximum**

Un couplage ayant le plus grand nombre possible d'arêtes.

Ces deux notions ne sont pas identiques.

## **32.3 Couplage parfait**

Tous les sommets sont couverts.

# **33 — COUPLAGE BIPARTI**

Les graphes bipartis permettent de modéliser :

Étudiants  
↕  
Projets  

ou :

Travailleurs  
↕  
Tâches  

ou :

Utilisateurs  
↕  
Produits  

Applications :

- recrutement ;
- affectation ;
- matching ;
- recommandation ;
- allocation de ressources.

# **34 — GRAPHES DE DÉPENDANCES**

Une dépendance peut être représentée par :

A → B  

signifiant :

B dépend de A.

## **Applications**

### **Gestion de packages**

Application  
↓  
Framework  
↓  
Bibliothèque  
↓  
Runtime  

### **Compilation**

source  
↓  
analyse  
↓  
AST  
↓  
optimisation  
↓  
code  

### **CI/CD**

build  
↓  
test  
↓  
security scan  
↓  
deploy  

### **Planification**

Tâche A  
↓  
Tâche B  
↓  
Tâche C  

Le DAG est donc une structure centrale de l'ingénierie logicielle.

# **35 — COMPOSANTES FORTEMENT CONNEXES**

Dans un graphe orienté, une composante fortement connexe est un ensemble maximal de sommets mutuellement atteignables.

Algorithmes classiques :

- Kosaraju ;
- Tarjan.

Complexité :

_O(V+E)O(V+E)_

# **36 — ALGORITHMES DE TARJAN**

Tarjan peut notamment être utilisé pour :

- SCC ;
- points d'articulation ;
- ponts.

Il repose sur une exploration DFS enrichie d'informations structurelles.

Notions importantes :

- ordre DFS ;
- low-link ;
- pile ;
- relation ancêtre/descendant.

# **37 — GRAPHES PLANAIRES**

Un graphe planaire peut être représenté dans le plan sans croisement d'arêtes.

Ils établissent un pont important entre :

- théorie des graphes ;
- géométrie computationnelle ;
- cartographie ;
- visualisation ;
- maillage.

# **38 — FORMULE D'EULER POUR LES GRAPHES PLANAIRES**

Pour un graphe planaire connexe :

_V−E+F=2V-E+F=2_

où :

- _VV_ = sommets ;
- _EE_ = arêtes ;
- _FF_ = faces.

Cette relation est fondamentale dans l'analyse topologique des structures planaires.

# **39 — GRAPHES ET GÉOMÉTRIE COMPUTATIONNELLE**

Le domaine D et le domaine E sont fortement liés.

Exemples :

Triangulation  
↓  
graphe de voisinage  
<br/>Mesh 3D  
↓  
graphe sommets/arêtes/faces  
<br/>Voronoi  
↓  
graphe dual  

La géométrie décrit :

où se trouvent les objets.

Les graphes décrivent :

comment ils sont reliés.

# **40 — GRAPHES ET MATRICES**

La matrice d'adjacence fournit une représentation matricielle du graphe.

Elle permet notamment d'étudier :

- chemins ;
- connectivité ;
- spectre du graphe ;
- propagation ;
- diffusion.

Une puissance de la matrice d'adjacence peut être interprétée en termes du nombre de marches de longueur donnée entre deux sommets.

# **41 — GRAPHES ET ALGÈBRE LINÉAIRE**

Pour un graphe, on peut définir une matrice de Laplace :

_L=D−AL=D-A_

où :

- _DD_ = matrice diagonale des degrés ;
- _AA_ = matrice d'adjacence.

La théorie spectrale des graphes utilise les valeurs propres de matrices associées aux graphes.

Applications :

- clustering ;
- analyse de réseaux ;
- semi-supervised learning ;
- graph neural networks ;
- réduction dimensionnelle ;
- détection de communautés.

# **42 — GRAPHES DANS LES SYSTÈMES INFORMATIQUES**

## **42.1 Systèmes distribués**

Les machines peuvent être représentées par :

Node  
↓  
Machine  

et les connexions :

Edge  
↓  
communication  

On peut alors étudier :

- routage ;
- disponibilité ;
- centralité ;
- pannes ;
- propagation.

## **42.2 Réseaux informatiques**

Client  
↓  
Switch  
↓  
Router  
↓  
Server  

Le graphe permet d'étudier :

- chemins ;
- coûts ;
- redondance ;
- congestion ;
- résilience.

## **42.3 Systèmes de fichiers**

Un système de fichiers possède naturellement une structure d'arbre.

/  
├── home  
│ └── user  
├── etc  
└── var  

## **42.4 Processus et dépendances**

Les dépendances entre processus peuvent être modélisées comme un graphe.

Cela permet de détecter :

- cycles ;
- blocages ;
- dépendances critiques.

# **43 — GRAPHES ET BASES DE DONNÉES**

Les graphes sont adaptés lorsque les relations sont aussi importantes que les entités.

Exemple :

Utilisateur  
↓ aime  
Produit  
↓ appartient  
Catégorie  
↓ similaire  
Produit  

Ils sont particulièrement pertinents pour :

- knowledge graphs ;
- recommandations ;
- réseaux sociaux ;
- relations complexes.

# **44 — GRAPHES DANS LE WEB**

Le Web peut être vu comme un graphe dirigé :

Page A  
↓  
Page B  
↓  
Page C  

Les hyperliens représentent des arcs.

Applications :

- crawling ;
- analyse de liens ;
- recherche ;
- recommandation ;
- détection de communautés ;
- ranking.

# **45 — GRAPHES DANS LES APPLICATIONS WEB**

## **45.1 Navigation**

Page  
↓  
route  
↓  
Page  

## **45.2 Workflow**

Draft  
↓  
Review  
↓  
Approved  
↓  
Published  

## **45.3 Machine à états**

Chaque état est un sommet.

Chaque transition est un arc.

IDLE  
↓  
LOADING  
↓  
SUCCESS  

ou :

IDLE → LOADING  
↓  
ERROR  
↓  
RETRY  

# **46 — GRAPHES DANS LES MOTEURS IA**

Les graphes apparaissent à plusieurs niveaux.

## **46.1 Knowledge Graph**

Personne  
↓ travaille_pour  
Entreprise  
↓ située_à  
Ville  

## **46.2 Graphe de dépendances**

Pour représenter :

- tâches ;
- outils ;
- agents ;
- ressources.

## **46.3 Graphes de connaissances pour RAG**

Un système peut représenter :

Entité  
↓  
Relation  
↓  
Entité  

Cela permet de récupérer des informations par relations plutôt que seulement par proximité textuelle.

# **47 — GRAPH NEURAL NETWORKS**

Les **Graph Neural Networks** utilisent directement la structure d'un graphe.

Chaque sommet possède éventuellement un vecteur de caractéristiques :

_xvx_v_

Le modèle agrège les informations des voisins.

Schéma conceptuel :

Voisins  
↓  
Message Passing  
↓  
Agrégation  
↓  
Mise à jour du sommet  

Une couche peut être conceptualisée comme :

_hv(l+1)=UPDATE(hv(l),AGGREGATE({hu(l):u∈N(v)}))h_v^{(l+1)} = \\text{UPDATE} \\left( h_v^{(l)}, \\text{AGGREGATE} \\left( \\{h_u^{(l)}:u\\in N(v)\\} \\right) \\right)_

Applications :

- molécules ;
- recommandations ;
- détection de fraude ;
- réseaux sociaux ;
- knowledge graphs ;
- systèmes de recommandation.

# **48 — GRAPHES ET COMPUTER VISION**

Une image peut être transformée en graphe.

Exemples :

Pixels  
↓  
sommets  
<br/>voisinage  
↓  
arêtes  

Applications :

- segmentation ;
- détection de régions ;
- contours ;
- correspondance ;
- analyse de structures.

# **49 — GRAPHES ET ROBOTIQUE**

Un robot peut représenter son environnement comme :

Position A  
↓  
Position B  
↓  
Position C  

Les arêtes peuvent représenter :

- mouvement ;
- distance ;
- énergie ;
- risque.

A\* et Dijkstra deviennent alors des outils de planification de trajectoires.

# **50 — GRAPHES DANS LES JEUX VIDÉO**

Un monde peut être représenté comme :

Node  
↓  
position navigable  
<br/>Edge  
↓  
déplacement possible  

A\* est particulièrement utilisé pour le pathfinding.

Structures possibles :

- grille ;
- navigation mesh ;
- waypoint graph ;
- graphe de salles.

# **51 — GRAPHES ET NAVIGATION MESH**

Un navmesh peut être vu comme un graphe :

Triangle A  
↕  
Triangle B  
↕  
Triangle C  

Le moteur cherche ensuite un chemin sur les cellules navigables.

La géométrie computationnelle fournit la géométrie.

La théorie des graphes fournit la connectivité.

# **52 — GRAPHES ET IA AGENTIQUE**

Un workflow agentique peut être représenté comme un graphe :

Input  
↓  
Planner  
↓  
Tool Selection  
↓  
Tool  
↓  
Observation  
↓  
Decision  

Un système plus complexe peut devenir :

Agent  
├── Search  
├── Database  
├── Calculator  
├── Browser  
└── Memory  

Les graphes permettent de formaliser :

- dépendances ;
- transitions ;
- états ;
- outils ;
- branches ;
- boucles ;
- conditions.

# **53 — GRAPHES D'ÉTATS**

Une machine à états finis peut être représentée par :

_G=(V,E)G=(V,E)_

où :

- _VV_ = états ;
- _EE_ = transitions.

Exemple :

LOCKED  
↓ unlock  
UNLOCKED  
↓ lock  
LOCKED  

Applications :

- UI ;
- jeux ;
- protocoles ;
- systèmes embarqués ;
- workflows ;
- agents.

# **54 — GRAPHES ET SÉCURITÉ**

Applications :

- graphes d'attaque ;
- dépendances logicielles ;
- propagation de vulnérabilités ;
- analyse de privilèges ;
- relations entre comptes ;
- détection de comportements anormaux ;
- réseaux de confiance.

Un graphe de dépendances permet notamment d'identifier les composants dont la compromission peut affecter une chaîne entière.

# **55 — COMPLEXITÉ ALGORITHMIQUE : TABLEAU CENTRAL**

|     |     |
| --- | --- |
| **Problème / algorithme** | **Complexité indicative** |
| BFS | _O(V+E)O(V+E)_ |
| DFS | _O(V+E)O(V+E)_ |
| Topological Sort | _O(V+E)O(V+E)_ |
| SCC | _O(V+E)O(V+E)_ |
| Dijkstra + heap | _O((V+E)log⁡V)O((V+E)\\log V)_ |
| Bellman-Ford | _O(VE)O(VE)_ |
| Floyd-Warshall | _O(V3)O(V^3)_ |
| Kruskal | _O(Elog⁡E)O(E\\log E)_ |
| Prim + heap | _O(Elog⁡V)O(E\\log V)_ |
| Edmonds-Karp | _O(VE2)O(VE^2)_ |
| Matrice d'adjacence | _O(V2)O(V^2)_ mémoire |
| Liste d'adjacence | _O(V+E)O(V+E)_ mémoire |

Les complexités exactes dépendent de la représentation et des structures utilisées.

# **56 — PROBLÈMES DE DÉGÉNÉRESCENCE ET CAS LIMITES**

Un véritable raisonnement algorithmique sur les graphes doit considérer :

- graphe vide ;
- un seul sommet ;
- sommets isolés ;
- graphe déconnecté ;
- arêtes parallèles ;
- boucles ;
- cycles ;
- graphes très denses ;
- graphes très creux ;
- poids nuls ;
- poids négatifs ;
- cycles négatifs ;
- DAG ;
- graphe complet.

# **57 — GRAPHES CREUX VS GRAPHES DENSES**

## **Graphe creux**

_E≪V2E\\ll V^2_

Une liste d'adjacence est généralement appropriée.

## **Graphe dense**

_E≈V2E\\approx V^2_

Une matrice d'adjacence peut devenir pertinente.

Le choix de la structure de données dépend donc du **rapport entre _VV_ et _EE_**.

# **58 — PRINCIPES DE MODÉLISATION**

Avant de choisir un algorithme :

## **Question 1**

Quels sont les objets ?

→ sommets.

## **Question 2**

Quelle relation existe entre eux ?

→ arêtes.

## **Question 3**

La relation est-elle directionnelle ?

→ orienté / non orienté.

## **Question 4**

La relation possède-t-elle un coût ?

→ pondéré.

## **Question 5**

Le coût peut-il être négatif ?

→ influence fortement le choix de l'algorithme.

## **Question 6**

Cherche-t-on :

- existence ?
- parcours ?
- plus court chemin ?
- arbre couvrant ?
- coloration ?
- flot ?
- couplage ?
- dépendances ?

Cette phase de modélisation est aussi importante que l'implémentation.

# **59 — ERREURS CLASSIQUES À ÉVITER**

## **Erreur 1**

Utiliser Dijkstra avec des poids négatifs.

## **Erreur 2**

Confondre :

chemin  
sentier  
marche  
cycle  

## **Erreur 3**

Confondre :

couplage maximal  
couplage maximum  

## **Erreur 4**

Confondre :

arbre couvrant  
plus court chemin  
MST  

Ils répondent à des problèmes différents.

## **Erreur 5**

Utiliser une matrice d'adjacence pour un graphe immense et très creux sans raison.

## **Erreur 6**

Croire que BFS trouve toujours le plus court chemin.

Il le fait dans un graphe non pondéré lorsque le coût d'une arête est uniforme.

## **Erreur 7**

Croire que DFS donne un plus court chemin.

Ce n'est pas son objectif.

# **60 — ALGORITHMES À CONNAÎTRE PAR NIVEAU**

## **Niveau fondamental**

- BFS ;
- DFS ;
- recherche de composantes ;
- détection de cycle ;
- topological sort.

## **Niveau intermédiaire**

- Dijkstra ;
- Bellman-Ford ;
- Kruskal ;
- Prim ;
- Union-Find ;
- SCC.

## **Niveau avancé**

- Floyd-Warshall ;
- A\* ;
- Ford-Fulkerson ;
- Edmonds-Karp ;
- matching ;
- Tarjan ;
- algorithmes de flots avancés.

## **Niveau spécialisé**

- graphes dynamiques ;
- graphes massifs ;
- graphes probabilistes ;
- graphes temporels ;
- spectral graph theory ;
- graph neural networks ;
- algorithmes distribués sur graphes.

# **61 — STRUCTURES DE DONNÉES ASSOCIÉES**

## **Fondamentales**

- tableau ;
- liste ;
- file ;
- pile ;
- heap ;
- hash map.

## **Spécialisées**

- Union-Find ;
- CSR ;
- structures de priorité ;
- représentations compactes ;
- structures de graphes dynamiques.

# **62 — PROPRIÉTÉS ET THÉORÈMES À RETENIR**

## **Théorème / propriété 1**

Un arbre à _nn_ sommets possède :

_n−1n-1_

arêtes.

## **Théorème / propriété 2**

Dans un graphe non orienté :

_∑deg(v)=2E\\sum deg(v)=2E_

## **Théorème / propriété 3**

Un graphe biparti n'a aucun cycle impair.

Réciproquement :

_G biparti  ⟺  G sans cycle impairG\\text{ biparti} \\iff G\\text{ sans cycle impair}_

## **Théorème / propriété 4**

Pour un graphe planaire connexe :

_V−E+F=2V-E+F=2_

## **Théorème / propriété 5**

Un graphe connexe possède un arbre couvrant.

## **Théorème / propriété 6**

Un MST minimise la somme des poids des arêtes parmi les arbres couvrants.

## **Théorème / propriété 7**

Max-flow = min-cut.

## **Théorème / propriété 8**

Un DAG possède un ordre topologique.

# **63 — CONCEPTS AVANCÉS À RECONNAÎTRE**

Même sans les maîtriser immédiatement en profondeur, il faut savoir identifier :

- graphes planaires ;
- graphes eulériens ;
- graphes hamiltoniens ;
- graphes parfaits ;
- graphes aléatoires ;
- graphes dynamiques ;
- hypergraphes ;
- graphes de connaissances ;
- graphes de contraintes ;
- graphes temporels ;
- graphes probabilistes ;
- graphes spectraux ;
- graphes multilayer.

# **64 — GRAPHE EULÉRIEN**

Un graphe est lié à un parcours eulérien lorsqu'on cherche à parcourir chaque arête exactement une fois.

# **65 — GRAPHE HAMILTONIEN**

Un problème hamiltonien cherche un cycle passant par tous les sommets selon certaines conditions.

Cela conduit notamment au célèbre :

**Traveling Salesman Problem — TSP**

qui consiste à chercher une tournée minimale visitant tous les points.

Le TSP est un problème central d'optimisation combinatoire.

# **66 — GRAPHES ET NP-COMPLÉTUDE**

Plusieurs problèmes fondamentaux de graphes sont difficiles au sens de la complexité algorithmique.

Exemples classiques :

- TSP ;
- clique maximum ;
- coloration minimale ;
- vertex cover ;
- Hamiltonian Cycle.

Il faut donc distinguer :

problème facilement résoluble exactement  

de :

problème nécessitant souvent  
heuristiques / approximation / recherche exponentielle  

# **67 — GRAPHES ET APPROXIMATION**

Lorsqu'un problème exact est trop coûteux, on peut utiliser :

- heuristiques ;
- approximation ;
- recherche locale ;
- algorithmes gloutons ;
- métaheuristiques ;
- programmation dynamique lorsque la structure le permet.

# **68 — GRAPHES DANS LES SYSTÈMES DISTRIBUÉS**

Les nœuds représentent :

- machines ;
- processus ;
- services.

Les arêtes représentent :

- communications ;
- dépendances ;
- liens réseau.

On peut étudier :

- consensus ;
- propagation ;
- détection de pannes ;
- topologie ;
- routage.

# **69 — GRAPHES ET MICROSERVICES**

Une architecture microservices peut être représentée par :

Frontend  
↓  
API Gateway  
↓  
Auth  
↓  
Orders  
↓  
Payments  

Ce graphe permet d'identifier :

- dépendances ;
- points critiques ;
- cycles ;
- chemins de requêtes ;
- propagation des pannes.

# **70 — GRAPHES ET ARCHITECTURE LOGICIELLE**

Les graphes peuvent représenter :

Module  
↓ dépend  
Module  

On peut ensuite détecter :

- dépendances circulaires ;
- composants fortement couplés ;
- composants centraux ;
- chemins critiques.

# **71 — GRAPHES ET COMPILATEURS**

Les compilateurs utilisent plusieurs graphes :

- graphe syntaxique ;
- AST ;
- graphe de dépendances ;
- graphe de contrôle ;
- graphe de flot de données ;
- graphe d'interférence.

Le **Control Flow Graph** représente les chemins possibles d'exécution d'un programme.

# **72 — GRAPHES DE CONTRÔLE**

Exemple :

Start  
↓  
Condition  
↙ ↘  
A B  
↘ ↙  
End  

Applications :

- analyse statique ;
- optimisation ;
- couverture de tests ;
- détection de chemins ;
- vérification de programmes.

# **73 — GRAPHES ET TESTS LOGICIELS**

On peut modéliser les chemins d'exécution :

Input  
↓  
Validation  
↓  
Auth  
↓  
Dashboard  

Les tests peuvent chercher à couvrir :

- sommets ;
- arêtes ;
- chemins ;
- branches.

# **74 — GRAPHES ET MOTEURS DE WORKFLOW**

Exemple :

Upload  
↓  
Validation  
↓  
Processing  
├── Success → Storage  
└── Error → Retry  

Le graphe permet de représenter explicitement :

- transitions ;
- conditions ;
- retries ;
- branches ;
- états terminaux.

# **75 — FICHES INDIVIDUELLES À PRODUIRE ULTÉRIEUREMENT**

Le document E sert de carte générale.

Il pourra être décliné en fiches spécialisées.

### **E1 — Fondations de la théorie des graphes****E2 — Représentation des graphes****E3 — Degrés et voisinages****E4 — Marches, chemins, cycles****E5 — Connexité****E6 — Ponts et points d'articulation****E7 — BFS****E8 — DFS****E9 — Détection de cycles****E10 — Composantes connexes****E11 — Composantes fortement connexes****E12 — Ordre topologique****E13 — Arbres****E14 — Arbres enracinés****E15 — Arbres couvrants****E16 — MST****E17 — Union-Find****E18 — Kruskal****E19 — Prim****E20 — Plus courts chemins****E21 — Dijkstra****E22 — Bellman-Ford****E23 — Floyd-Warshall****E24 — A\*****E25 — Coloration****E26 — Graphes bipartis****E27 — Couplage****E28 — Flots****E29 — Ford-Fulkerson****E30 — Edmonds-Karp****E31 — Max-flow / Min-cut****E32 — Graphes de dépendances****E33 — DAG et workflows****E34 — Graphes planaires****E35 — Graphes eulériens****E36 — Graphes hamiltoniens****E37 — TSP****E38 — Graphes et NP-complétude****E39 — Graphes aléatoires****E40 — Graphes dynamiques****E41 — Graphes de connaissances****E42 — Graphes pour le Web****E43 — Graphes pour les systèmes distribués****E44 — Graphes pour les réseaux****E45 — Graphes pour les compilateurs****E46 — Control Flow Graph****E47 — Data Flow Graph****E48 — Graphes pour les systèmes de recommandation****E49 — Graph Neural Networks****E50 — Graphes pour l'IA agentique****E51 — Graphes et computer vision****E52 — Graphes et robotique****E53 — Graphes et moteurs de jeux****E54 — Navigation Mesh****E55 — Graphes et moteurs 3D****E56 — Théorie spectrale des graphes****E57 — Laplacien des graphes****E58 — Centralité et communautés****E59 — Graphes de dépendances logicielles****E60 — Graphes massifs et calcul distribué**

# **76 — CE QU'IL FAUT ABSOLUMENT RETENIR**

La maîtrise minimale du domaine E doit permettre de reconnaître immédiatement :

### **Structure**

V  
E  
adjacence  
degré  
orientation  
poids  

### **Parcours**

BFS  
DFS  

### **Structure**

arbre  
DAG  
graphe biparti  
graphe pondéré  

### **Connectivité**

composantes  
SCC  
ponts  
articulations  

### **Chemins**

BFS  
Dijkstra  
Bellman-Ford  
Floyd-Warshall  
A\*  

### **Arbres couvrants**

Kruskal  
Prim  
Union-Find  

### **Optimisation**

coloration  
flot  
couplage  

### **Dépendances**

DAG  
topological sort  

### **IA / systèmes**

knowledge graph  
GNN  
workflow graph  
dependency graph  
state graph  

# **77 — QUESTIONS DE RECONNAISSANCE À SAVOIR RÉPONDRE**

Face à un problème, être capable de demander :

### **1**

Les objets sont-ils des sommets ?

### **2**

Les relations sont-elles orientées ?

### **3**

Les relations ont-elles un poids ?

### **4**

Le graphe est-il creux ou dense ?

### **5**

Cherche-t-on une connexion ?

### **6**

Cherche-t-on un chemin ?

### **7**

Cherche-t-on le chemin minimal ?

### **8**

Les poids sont-ils négatifs ?

### **9**

Cherche-t-on un arbre couvrant ?

### **10**

Cherche-t-on un coût global minimal ?

### **11**

Existe-t-il des dépendances ?

### **12**

Existe-t-il des cycles ?

### **13**

Cherche-t-on à affecter des ressources ?

### **14**

Le problème peut-il devenir un problème de flot ?

### **15**

Le problème peut-il devenir un problème de couplage ?

### **16**

La structure est-elle un DAG ?

### **17**

Le graphe représente-t-il un espace géométrique ?

### **18**

Le graphe représente-t-il un réseau ?

### **19**

Le graphe représente-t-il des connaissances ?

### **20**

Le graphe représente-t-il des états ou des transitions ?

# **78 — PROJETS PRATIQUES DE MAÎTRISE**

## **Projet E1 — Graph Explorer**

Construire une interface permettant de :

- créer des sommets ;
- créer des arêtes ;
- orienter les arêtes ;
- ajouter des poids ;
- visualiser BFS ;
- visualiser DFS.

## **Projet E2 — Pathfinding Lab**

Construire un laboratoire permettant de comparer :

- BFS ;
- Dijkstra ;
- A\*.

Afficher :

- nombre de nœuds explorés ;
- chemin final ;
- coût ;
- temps ;
- différence entre heuristiques.

## **Projet E3 — Dependency Graph**

Créer un moteur représentant les dépendances entre packages.

Fonctionnalités :

- ajout de package ;
- dépendances ;
- détection de cycle ;
- ordre d'installation ;
- visualisation.

## **Projet E4 — MST Visualizer**

Comparer :

- Kruskal ;
- Prim.

Afficher progressivement la construction de l'arbre.

## **Projet E5 — Network Analyzer**

Créer un outil permettant d'analyser un réseau :

- degrés ;
- composantes ;
- ponts ;
- points d'articulation ;
- chemins ;
- centralité.

## **Projet E6 — Workflow Engine**

Construire un moteur de workflow basé sur un DAG.

Exemple :

Upload  
↓  
Validation  
↓  
Processing  
↓  
Review  
↓  
Publish  

## **Projet E7 — Mini Knowledge Graph**

Construire :

Entity  
↓  
Relation  
↓  
Entity  

avec :

- recherche ;
- exploration ;
- voisinage ;
- chemins ;
- visualisation.

## **Projet E8 — Agent Graph**

Construire un moteur où :

Agent  
↓  
Decision  
├── Tool A  
├── Tool B  
└── Tool C  

est représenté explicitement sous forme de graphe.

## **Projet E9 — Navigation 2D/3D**

Construire une carte avec :

- obstacles ;
- nœuds ;
- connexions ;
- A\* ;
- visualisation du chemin.

## **Projet E10 — Graph Neural Network Explorer**

Construire une petite expérience montrant :

Graph  
↓  
Message Passing  
↓  
Node Embeddings  
↓  
Prediction  

# **79 — EXERCICES PROGRESSIFS**

## **Niveau 1 — Reconnaissance**

À partir d'une situation réelle :

modéliser les sommets et les arêtes.

## **Niveau 2 — Implémentation**

Implémenter :

- liste d'adjacence ;
- matrice d'adjacence ;
- BFS ;
- DFS.

## **Niveau 3 — Analyse**

Calculer :

- degrés ;
- composantes ;
- cycles ;
- distances.

## **Niveau 4 — Optimisation**

Implémenter :

- Dijkstra ;
- Kruskal ;
- Prim.

## **Niveau 5 — Structures avancées**

Implémenter :

- SCC ;
- topological sort ;
- max-flow ;
- matching.

## **Niveau 6 — Application**

Transformer un véritable problème informatique en graphe.

# **80 — CHALLENGES SANS IA**

Pour développer une véritable autonomie :

### **Challenge 1**

Implémenter BFS sans regarder de code.

### **Challenge 2**

Implémenter DFS sans regarder de code.

### **Challenge 3**

Expliquer pourquoi BFS donne le plus court chemin dans un graphe non pondéré.

### **Challenge 4**

Expliquer pourquoi Dijkstra ne fonctionne pas correctement avec des poids négatifs.

### **Challenge 5**

Implémenter Dijkstra.

### **Challenge 6**

Implémenter Kruskal avec Union-Find.

### **Challenge 7**

Construire un ordre topologique.

### **Challenge 8**

Détecter un cycle dans un DAG candidat.

### **Challenge 9**

Transformer un problème réel en graphe.

### **Challenge 10**

Choisir l'algorithme sans demander à l'IA.

# **81 — CHALLENGES AVEC IA**

L'IA peut ensuite être utilisée comme :

- critique ;
- vérificateur ;
- générateur de cas limites ;
- partenaire de raisonnement ;
- outil de comparaison.

Exemple :

« Voici mon modèle de graphe et mon choix d'algorithme. Trouve les hypothèses implicites que j'ai oubliées sans me donner directement la solution. »

Puis :

« Génère 20 cas limites capables de casser mon implémentation. »

Puis :

« Compare mon implémentation avec les propriétés théoriques de l'algorithme. »

L'objectif est que l'IA augmente le raisonnement plutôt qu'elle ne le remplace.

# **82 — CONNEXIONS AVEC LES AUTRES DOMAINES**

## **Domaine A — Logique**

Les graphes permettent de formaliser :

- relations ;
- contraintes ;
- états ;
- décisions ;
- preuves.

## **Domaine B — Théorie des nombres**

Les poids et les algorithmes peuvent nécessiter :

- arithmétique exacte ;
- modularité ;
- grands entiers.

## **Domaine C — Algèbre linéaire**

Connexion directe avec :

- matrices d'adjacence ;
- Laplacien ;
- valeurs propres ;
- embeddings ;
- GNN.

## **Domaine D — Géométrie computationnelle**

Connexion directe avec :

- graphes de voisinage ;
- triangulations ;
- meshes ;
- navigation ;
- structures spatiales.

## **Domaine F — Combinatoire**

Connexion avec :

- dénombrement ;
- coloration ;
- chemins ;
- sous-graphes ;
- structures discrètes.

## **IA**

Connexion avec :

- knowledge graphs ;
- GNN ;
- recherche ;
- recommandation ;
- raisonnement relationnel.

# **83 — CARTE MENTALE FINALE**

THÉORIE DES GRAPHES  
│  
┌────────────────┼────────────────┐  
│ │ │  
STRUCTURES PARCOURS OPTIMISATION  
│ │ │  
┌────┼────┐ ┌───┴───┐ ┌───┼────┐  
│ │ │ │ │ │ │ │  
DAG Arbre Biparti BFS DFS Chemin MST Flot  
│ │ │ │ │ │ │ │  
│ │ │ │ │ │ │ │  
└────┴────┴───────┴───────┴───────┴───┴────┘  
│  
APPLICATIONS  
│  
┌──────────┬────────┼─────────┬──────────┐  
│ │ │ │ │  
WEB RÉSEAUX SYSTÈMES IA 3D  
│ │ │ │ │  
crawling routing dépendances GNN navigation  
ranking topology workflow KG pathfinding  
liens résilience compiler agents navmesh  

# **84 — CRITÈRE DE MAÎTRISE DU DOMAINE E**

La maîtrise ne consiste pas à connaître par cœur 50 algorithmes.

Elle consiste à être capable de faire :

PROBLÈME RÉEL  
↓  
ABSTRACTION  
↓  
GRAPHE  
↓  
TYPE DE GRAPHE  
↓  
PROPRIÉTÉS  
↓  
ALGORITHME  
↓  
STRUCTURE DE DONNÉES  
↓  
COMPLEXITÉ  
↓  
IMPLÉMENTATION  
↓  
VALIDATION  
↓  
APPLICATION  

À terme, face à un problème, il doit devenir naturel de penser :

« Ce problème peut-il être représenté comme un graphe ? »

Puis :

« Quelle structure possède ce graphe ? »

Puis :

« Quelle propriété suis-je réellement en train de chercher ? »

Puis :

« Quel algorithme exploite cette propriété ? »

C'est cette capacité de **modélisation algorithmique** qui constitue le cœur de la maîtrise du domaine.

# **85 — CHECKLIST FINALE DE MAÎTRISE**

## **Fondations**

- définir un graphe ;
- distinguer sommet, arête et arc ;
- distinguer orienté / non orienté ;
- distinguer pondéré / non pondéré ;
- calculer un degré ;
- comprendre l'adjacence.

## **Parcours**

- comprendre BFS ;
- comprendre DFS ;
- implémenter BFS ;
- implémenter DFS ;
- détecter un cycle ;
- trouver les composantes.

## **Structures**

- arbre ;
- arbre enraciné ;
- DAG ;
- biparti ;
- graphe complet ;
- graphe planaire.

## **Chemins**

- BFS pour graphe non pondéré ;
- Dijkstra ;
- Bellman-Ford ;
- Floyd-Warshall ;
- A\* ;
- comprendre les hypothèses de chaque algorithme.

## **Arbres couvrants**

- MST ;
- Kruskal ;
- Prim ;
- Union-Find.

## **Optimisation**

- coloration ;
- couplage ;
- flot ;
- min-cut ;
- max-flow.

## **Dépendances**

- DAG ;
- ordre topologique ;
- analyse de dépendances ;
- workflows.

## **Applications**

- réseaux ;
- Web ;
- systèmes ;
- bases de données ;
- IA ;
- GNN ;
- knowledge graphs ;
- navigation ;
- jeux ;
- robotique.

## **Ingénierie**

- choisir la bonne représentation ;
- analyser _VV_ et _EE_ ;
- raisonner sur la complexité ;
- gérer les cas limites ;
- tester sur graphes petits ;
- tester sur graphes adversariaux ;
- comparer théorie et implémentation.

# **86 — SYNTHÈSE ULTIME**

Le domaine E peut finalement être résumé par cette chaîne :

SOMMETS  
↓  
RELATIONS  
↓  
GRAPHES  
↓  
STRUCTURE  
↓  
PARCOURS  
↓  
CONNECTIVITÉ  
↓  
CHEMINS  
↓  
OPTIMISATION  
↓  
DÉPENDANCES  
↓  
RÉSEAUX  
↓  
SYSTÈMES  
↓  
IA  

La théorie des graphes fournit ainsi l'un des langages mathématiques les plus importants pour représenter les **relations, dépendances, connexions, transitions et chemins** dans les systèmes informatiques.

Elle constitue un pont direct entre les mathématiques discrètes et :

- l'algorithmique ;
- l'ingénierie logicielle ;
- les réseaux ;
- les systèmes distribués ;
- le Web ;
- les bases de données ;
- la recherche ;
- l'IA ;
- la robotique ;
- les moteurs de jeux ;
- les systèmes 2D/3D.

# **87 — POSITION DU DOMAINE E DANS LA SUITE**

A — Logique et fondements  
B — Théorie des nombres  
C — Algèbre linéaire / géométrie linéaire  
D — Géométrie computationnelle  
E — Théorie des graphes et algorithmes sur les graphes  
↓  
F — Combinatoire  

## **DOMAINE SUIVANT**

**F — COMBINATOIRE**

La combinatoire prolongera naturellement le domaine E en étudiant plus systématiquement le **dénombrement, les arrangements, permutations, combinaisons, récurrences, principes de comptage, structures discrètes et problèmes d'optimisation combinatoire**.