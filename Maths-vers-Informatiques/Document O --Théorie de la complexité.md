# DOCUMENT O — THÉORIE DE LA COMPLEXITÉ

## Comprendre ce qui est calculable, faisable et scalable

# 0\. PRÉDISPOSITION D’INTÉGRATION

## 0.1 Rôle de ce document

Ce document constitue une base de référence pour reconnaître, analyser et exploiter les concepts de **théorie de la complexité computationnelle** dans les projets de programmation, d’ingénierie logicielle, d’intelligence artificielle, d’algorithmique, d’optimisation, de cybersécurité, de systèmes distribués et de recherche.

Lorsqu’un problème de projet implique :

- une grande quantité de données ;
- des entrées dont la taille peut fortement augmenter ;
- plusieurs boucles imbriquées ;
- une récursion ;
- une recherche dans un espace de solutions ;
- une optimisation combinatoire ;
- un problème de décision ;
- une génération de toutes les possibilités ;
- une contrainte de temps ;
- une contrainte mémoire ;
- un traitement distribué ;
- une recherche exacte potentiellement coûteuse ;
- une question de faisabilité algorithmique ;
- un problème apparemment impossible à résoudre ;
- un algorithme dont le temps d’exécution explose lorsque l’entrée augmente ;

l’IA doit utiliser ce document pour déterminer :

1.  **ce que le problème demande réellement de calculer ;**
2.  **quelle est la taille pertinente de l’entrée ;**
3.  **quelle ressource est consommée ;**
4.  **comment cette consommation croît avec la taille de l’entrée ;**
5.  **quelle borne asymptotique décrit cette croissance ;**
6.  **si l’algorithme est efficace dans le cas considéré ;**
7.  **si le problème lui-même semble intrinsèquement difficile ;**
8.  **si une réduction permet de comparer sa difficulté à celle d’un autre problème ;**
9.  **si le problème est seulement difficile ou s’il est même non calculable ;**
10. **quelles stratégies permettent malgré tout de le traiter en pratique.**

# 1\. IDENTITÉ DU DOMAINE

## 1.1 Nom

**Domaine O — Théorie de la complexité**

## 1.2 Nature

La théorie de la complexité est une branche de l’informatique théorique qui étudie les **ressources nécessaires pour résoudre des problèmes computationnels**.

Elle ne demande donc pas seulement :

« Existe-t-il un algorithme ? »

mais également :

« Combien de temps faut-il ? »

« Combien de mémoire faut-il ? »

« Comment ces besoins évoluent-ils lorsque la taille du problème augmente ? »

« Existe-t-il une méthode suffisamment efficace pour rendre le problème praticable ? »

Elle cherche ainsi à distinguer les problèmes :

- faciles ;
- raisonnablement calculables ;
- coûteux ;
- extrêmement coûteux ;
- et, à la frontière avec la calculabilité, impossibles à résoudre algorithmiquement de manière générale.

# 2\. LA GRANDE QUESTION DU DOMAINE

La question centrale peut être résumée ainsi :

**« Est-ce que je peux programmer ça ? »**

devient :

**« Est-ce que je peux le calculer ? »**

puis :

**« Est-ce que je peux le calculer efficacement ? »**

puis :

**« Est-ce que je peux le calculer efficacement à grande échelle ? »**

Cette progression est fondamentale.

Un programme peut être :

- parfaitement correct ;
- toujours terminé ;
- mathématiquement efficace dans le sens théorique de calculabilité ;
- mais totalement inutilisable en pratique parce que son temps d’exécution augmente trop rapidement.

À l’inverse, un problème peut être extrêmement difficile mais posséder des approximations, heuristiques ou algorithmes spécialisés permettant de le traiter efficacement dans certains contextes.

# 3\. PLACE DANS LA PYRAMIDE MATHÉMATIQUE DE L’INFORMATIQUE

La théorie de la complexité se situe entre plusieurs domaines.

LOGIQUE / FONDEMENTS  
↓  
CALCULABILITÉ  
↓  
DÉCIDABILITÉ  
↓  
THÉORIE DE LA COMPLEXITÉ  
↓  
ANALYSE DES ALGORITHMES  
↓  
ALGORITHMES & STRUCTURES DE DONNÉES  
↓  
SYSTÈMES LOGICIELS RÉELS

Mais cette représentation est simplifiée.

Une autre manière de la comprendre est :

PROBLÈME  
│  
┌─────────┴─────────┐  
│ │  
Peut-il être calculé ? Non  
│  
Oui  
│  
Peut-il être décidé ?  
│  
Oui  
│  
Combien de ressources ?  
│  
┌──────┼──────────────┐  
│ │ │  
temps espace autres ressources  
│ │  
└──────┴──────┐  
↓  
CLASSIFICATION  
↓  
P / NP / PSPACE / EXP  
etc.

# 4\. CALCULABILITÉ, DÉCIDABILITÉ ET COMPLEXITÉ : NE PAS CONFONDRE

C’est l’une des distinctions les plus importantes de tout le document.

## 4.1 Calculabilité

La calculabilité demande :

**Existe-t-il un algorithme qui puisse résoudre le problème ?**

Si oui, le problème est calculable.

Si aucun algorithme général ne peut le résoudre, le problème est non calculable.

## 4.2 Décidabilité

La décidabilité concerne principalement les problèmes dont la réponse peut être exprimée sous forme :

OUI / NON

Un problème est décidable s’il existe une procédure algorithmique qui :

1.  reçoit toute entrée valide ;
2.  donne la bonne réponse ;
3.  termine toujours.

## 4.3 Complexité

La complexité intervient ensuite :

**Si le problème est calculable, combien coûte son calcul ?**

On obtient alors une hiérarchie conceptuelle :

Calculabilité  
↓  
Est-ce calculable ?  
↓  
Décidabilité  
↓  
Est-ce toujours décidable ?  
↓  
Complexité  
↓  
À quel coût ?  
↓  
Scalabilité  
↓  
Est-ce praticable à grande échelle ?

# 5\. LE MODÈLE DE CALCUL

Pour parler rigoureusement de complexité, il faut définir ce que signifie :

« une opération coûte quelque chose ».

La théorie utilise des modèles abstraits tels que :

- machine de Turing ;
- machine à accès aléatoire ;
- modèles RAM ;
- circuits ;
- automates et machines abstraites.

L’objectif n’est pas de reproduire exactement un processeur particulier.

Il s’agit de disposer d’un modèle suffisamment général pour comparer les algorithmes indépendamment des détails d’une machine particulière.

# 6\. TAILLE DE L’ENTRÉE

La complexité est généralement exprimée en fonction d’une variable :

\[ n \]

représentant la **taille de l’entrée**.

Mais (n) ne signifie pas toujours simplement « nombre d’éléments ».

Exemples :

### Tableau

\[ n = \]

### Graphe

\[ n = |V| + |E| \]

ou séparément :

\[ |V|, |E| \]

### Chaîne

\[ n = \]

### Nombre entier

La taille pertinente est généralement le **nombre de bits nécessaires pour représenter le nombre**, soit approximativement :

\[ \_2 N \]

et non (N) lui-même.

Cette distinction est fondamentale en complexité théorique.

# 7\. COMPLEXITÉ TEMPORELLE

La complexité temporelle mesure la quantité de calcul nécessaire en fonction de la taille de l’entrée.

On note souvent :

\[ T(n) \]

## 7.1 Exemple simple

for i in range(n):  
print(i)

Le nombre d’itérations est proportionnel à (n).

Donc :

\[ T(n)=(n) \]

## 7.2 Deux boucles imbriquées

for i in range(n):  
for j in range(n):  
...

Nombre d’itérations :

\[ n n = n^2 \]

Donc :

\[ T(n)=(n^2) \]

## 7.3 Trois boucles

for i in range(n):  
for j in range(n):  
for k in range(n):  
...

\[ T(n)=(n^3) \]

# 8\. COMPLEXITÉ SPATIALE

La complexité spatiale mesure la quantité de mémoire nécessaire.

On peut distinguer :

- mémoire totale ;
- mémoire auxiliaire ;
- mémoire de l’entrée ;
- mémoire de sortie ;
- pile d’appels ;
- structures intermédiaires.

Exemple :

copy = \[0\] \* n

nécessite :

\[ (n) \]

d’espace supplémentaire.

# 9\. COMPLEXITÉ TEMPORELLE ≠ COMPLEXITÉ SPATIALE

Un algorithme peut être :

- rapide mais gourmand en mémoire ;
- lent mais peu gourmand ;
- rapide et peu gourmand ;
- lent et gourmand.

On obtient un compromis classique :

\[ \]

Exemple :

mémoriser les résultats intermédiaires peut accélérer fortement un calcul.

C’est notamment le principe de la **programmation dynamique**.

# 10\. MEILLEUR CAS, PIRE CAS ET CAS MOYEN

La complexité n’est pas toujours une unique valeur.

## 10.1 Meilleur cas

\[ T_{}(n) \]

C’est le comportement le plus favorable.

## 10.2 Pire cas

\[ T_{}(n) \]

C’est le comportement le plus défavorable.

C’est souvent celui utilisé pour les garanties théoriques.

## 10.3 Cas moyen

\[ T_{}(n) \]

Il dépend d’une distribution des entrées.

Il faut donc préciser :

« moyen selon quelle distribution ? »

Sans cette précision, une analyse de cas moyen peut être ambiguë.

# 11\. NOTATION ASYMPTOTIQUE

La notation asymptotique permet d’étudier la croissance lorsque :

\[ n \]

Elle ignore principalement :

- les constantes multiplicatives ;
- les termes de plus faible ordre.

Par exemple :

\[ 7n^2 + 3n + 15 \]

est :

\[ (n^2) \]

# 12\. BIG-O — (O)

## 12.1 Idée intuitive

\[ f(n)=O(g(n)) \]

signifie essentiellement que (f) ne croît pas asymptotiquement plus vite que (g), à un facteur constant près.

Formellement :

\[ c>0,n_0 : \]

tel que :

\[ 0f(n)c,g(n) \]

pour tout :

\[ nn_0 \]

## 12.2 Interprétation

Big-O fournit une **borne supérieure asymptotique**.

Si :

\[ T(n)=3n^2+10n+5 \]

alors :

\[ T(n)=O(n^2) \]

## 12.3 Attention

Dire :

\[ T(n)=O(n^2) \]

ne signifie pas forcément :

\[ T(n)=(n^2) \]

car (O(n^2)) autorise aussi des fonctions plus petites :

\[ O(n) \]

\[ O(nn) \]

\[ O(1) \]

etc.

# 13\. BIG-OMEGA — ()

\[ f(n)=(g(n)) \]

signifie que (f) est asymptotiquement **au moins aussi grande** que (g), à une constante près.

Formellement :

\[ c>0,n_0: \]

\[ f(n)c,g(n) \]

pour tout :

\[ nn_0 \]

Omega donne donc une **borne inférieure asymptotique**.

# 14\. BIG-THETA — ()

\[ f(n)=(g(n)) \]

signifie que (f) et (g) ont le même ordre de croissance asymptotique.

C’est équivalent à :

\[ f(n)=O(g(n)) \]

et :

\[ f(n)=(g(n)) \]

simultanément.

Ainsi :

\[ 3n<sup>2+5n+7=(n</sup>2) \]

# 15\. RELATION ENTRE (O), () ET ()

O(g)  
│  
├── borne supérieure  
│  
Θ(g)  
│  
├── borne supérieure + inférieure  
│  
Ω(g)  
│  
└── borne inférieure

Une manière plus correcte de le voir :

\[ (g)=O(g)(g) \]

# 16\. PETIT-O ET PETIT-OMEGA

Même s’ils ne sont pas dans la liste minimale, ils doivent être connus.

## Petit-o

\[ f(n)=o(g(n)) \]

signifie :

\[ \_{n}=0 \]

Donc (f) croît strictement moins vite que (g).

Exemple :

\[ n=o(n^2) \]

## Petit-omega

\[ f(n)=(g(n)) \]

signifie :

\[ \_{n}= \]

Donc (f) croît strictement plus vite.

# 17\. TAUX DE CROISSANCE CLASSIQUES

Une hiérarchie utile est :

\[ O(1) \]

\[ O(n) \]

\[ O(n) \]

\[ O(nn) \]

\[ O(n^2) \]

\[ O(n^3) \]

\[ O(n^k) \]

\[ O(2^n) \]

\[ O(3^n) \]

\[ O(n!) \]

avec une croissance généralement de plus en plus rapide.

Mais il faut éviter de transformer cette liste en règle absolue : les constantes, la taille réelle des entrées, la structure des données, le parallélisme et l’environnement peuvent modifier fortement les performances pratiques.

# 18\. POURQUOI L’ASYMPTOTIQUE EST PUISSANTE

Supposons :

\[ T_1(n)=1000n \]

et :

\[ T_2(n)=n^2 \]

Pour de petites valeurs de (n), (T_2) peut être plus rapide.

Mais lorsque (n) devient suffisamment grand :

\[ n^2 1000n \]

La complexité permet donc d’anticiper le comportement à grande échelle.

# 19\. COMPLEXITÉ AMORTIE

La complexité amortie analyse le coût moyen d’une séquence d’opérations, même lorsque certaines opérations individuelles sont très coûteuses.

Exemple classique :

agrandir dynamiquement un tableau.

La plupart des insertions coûtent :

\[ O(1) \]

mais certaines nécessitent une copie :

\[ O(n) \]

Pour une séquence suffisamment longue, le coût amorti par insertion peut rester :

\[ O(1) \]

C’est important pour :

- tableaux dynamiques ;
- structures extensibles ;
- caches ;
- structures de données ;
- systèmes incrémentaux.

# 20\. COMPLEXITÉ DES ALGORITHMES RÉCURSIFS

Un algorithme récursif peut être représenté par une relation de récurrence.

Exemple :

\[ T(n)=2T(n/2)+O(n) \]

Cela correspond typiquement à une division du problème en deux sous-problèmes.

# 21\. MASTER THEOREM

Pour les récurrences de la forme :

\[ T(n)=aT()+f(n) \]

le Master Theorem permet de comparer :

\[ f(n) \]

avec :

\[ n^{\_b a} \]

et d’obtenir une borne asymptotique dans un grand nombre de cas.

Il est particulièrement utile pour analyser :

- merge sort ;
- divide and conquer ;
- certains algorithmes géométriques ;
- algorithmes récursifs sur tableaux ;
- certaines architectures parallèles.

# 22\. EXEMPLE : MERGE SORT

La récurrence est :

\[ T(n)=2T(n/2)+(n) \]

Le résultat est :

\[ T(n)=(nn) \]

C’est un exemple majeur montrant comment une structure récursive peut conduire à une complexité bien meilleure qu’une approche quadratique.

# 23\. COMPLEXITÉ DES STRUCTURES DE DONNÉES

La théorie de la complexité ne concerne pas seulement les algorithmes isolés.

Elle permet aussi de comparer :

- tableaux ;
- listes chaînées ;
- piles ;
- files ;
- tables de hachage ;
- arbres ;
- heaps ;
- arbres équilibrés ;
- graphes ;
- structures spécialisées.

Pour chaque structure, il faut analyser les opérations :

- recherche ;
- insertion ;
- suppression ;
- accès ;
- mise à jour ;
- parcours.

# 24\. COMPLEXITÉ D’UNE OPÉRATION ≠ COMPLEXITÉ DU SYSTÈME

Un endpoint peut avoir une complexité :

\[ O(n) \]

mais être appelé :

\[ 10^6 \]

fois.

La complexité globale dépend alors aussi du nombre d’appels.

Exemple :

\[ O(n)O(m)=O(nm) \]

Cette observation devient essentielle dans les applications web et distribuées.

# 25\. COMPLEXITÉ COMPOSÉE

Supposons :

requête  
↓  
recherche  
↓  
transformation  
↓  
tri  
↓  
agrégation

Si les étapes ont respectivement :

\[ O(n) \]

\[ O(n) \]

\[ O(n) \]

\[ O(nn) \]

\[ O(n) \]

la complexité dominante peut devenir :

\[ O(nn) \]

La complexité globale ne se résume donc pas à regarder arbitrairement une seule fonction.

# 26\. COMPLEXITÉ ET GRAPHES

Pour un graphe :

\[ G=(V,E) \]

la taille peut dépendre de :

\[ |V| \]

et :

\[ |E| \]

Un algorithme peut donc être exprimé sous la forme :

\[ O(|V|+|E|) \]

ou :

\[ O(|V||E|) \]

etc.

Cette distinction est cruciale en :

- réseaux ;
- routage ;
- graphes sociaux ;
- systèmes distribués ;
- recherche ;
- IA ;
- optimisation.

# 27\. PROBLÈME D’ALGORITHME VS PROBLÈME DE DÉCISION

La théorie de la complexité étudie souvent des **problèmes de décision**.

Exemple :

### Problème d’optimisation

Quel est le plus court chemin ?

### Problème de décision associé

Existe-t-il un chemin de longueur au plus (k) ?

Réduire un problème à une forme décisionnelle permet souvent de raisonner plus proprement sur sa complexité.

# 28\. P — POLYNOMIAL TIME

La classe :

\[ P \]

contient les problèmes de décision pouvant être résolus par une machine déterministe en temps polynomial :

\[ O(n^k) \]

pour une constante (k).

Exemples classiques :

- tri ;
- recherche dans certaines structures ;
- plus court chemin ;
- arbre couvrant minimal ;
- plus grande partie des problèmes classiques de graphes polynomiaux ;
- primalité.

# 29\. POURQUOI LE POLYNOMIAL EST IMPORTANT

La théorie considère souvent les algorithmes polynomiaux comme une approximation mathématique de la notion de **faisabilité efficace**.

Mais :

\[ O(n^{100}) \]

est théoriquement polynomial tout en pouvant être totalement impraticable.

Inversement :

\[ O(2^n) \]

peut être exploitable pour de très petites valeurs de (n).

Donc :

**P ≠ « rapide dans tous les cas pratiques ».**

P signifie plutôt :

« possède une croissance polynomialement bornée selon le modèle considéré ».

# 30\. NP — NONDETERMINISTIC POLYNOMIAL TIME

La classe :

\[ \]

est définie formellement à partir des machines non déterministes.

Une manière beaucoup plus intuitive de la comprendre est :

Une solution candidate peut être **vérifiée en temps polynomial**.

Pour un problème dans NP, on peut disposer d’un certificat (c) tel que :

\[ V(x,c) \]

puisse vérifier efficacement que (c) constitue une solution valide pour l’entrée (x).

# 31\. EXEMPLE : SAT

Problème :

Une formule logique possède-t-elle une affectation satisfaisante ?

Si quelqu’un fournit une affectation :

x1 = vrai  
x2 = faux  
x3 = vrai  
...

on peut vérifier rapidement si la formule est satisfaite.

Trouver cette affectation peut cependant être beaucoup plus difficile.

# 32\. P EST INCLUS DANS NP

On sait :

\[ P \]

Pourquoi ?

Si un problème peut être résolu rapidement, alors sa solution peut évidemment être vérifiée rapidement.

Mais on ne sait pas démontrer actuellement :

\[ P= \]

ou :

\[ P \]

La question P vs NP reste un problème ouvert majeur de l’informatique théorique.

# 33\. P VS NP

La question fondamentale est :

**Tout problème dont une solution peut être vérifiée efficacement peut-il également être résolu efficacement ?**

Formellement :

\[ P \]

Si :

\[ P=NP \]

alors tous les problèmes NP auraient des algorithmes polynomiaux.

Si :

\[ PNP \]

alors il existe des problèmes dont la vérification est polynomialement efficace mais dont la résolution n’est pas polynomialement efficace.

Le problème est toujours officiellement non résolu.

# 34\. NP-COMPLET

Un problème est **NP-complet** s’il satisfait deux conditions :

1.  il appartient à NP ;
2.  tout problème de NP peut lui être réduit en temps polynomial.

Un problème NP-complet est donc, intuitivement :

**au moins aussi difficile que tous les problèmes de NP, tout en appartenant lui-même à NP.**

# 35\. EXEMPLES DE PROBLÈMES NP-COMPLETS

Exemples classiques :

- SAT ;
- 3-SAT ;
- CLIQUE ;
- Vertex Cover ;
- Hamiltonian Cycle ;
- Subset Sum ;
- certaines versions de Knapsack ;
- TSP sous forme décisionnelle.

Le théorème de Cook-Levin établit notamment la NP-complétude de SAT.

# 36\. CONSÉQUENCE MAJEURE

Si un seul problème NP-complet possède un algorithme polynomial, alors :

\[ P=NP \]

Pourquoi ?

Parce que tous les problèmes de NP peuvent être réduits à ce problème.

Donc résoudre efficacement un seul problème NP-complet permettrait, via les réductions, de résoudre efficacement tous les problèmes de NP.

# 37\. NP-DIFFICILE

Un problème est **NP-difficile** lorsqu’il est au moins aussi difficile que tous les problèmes de NP, selon la notion de réduction considérée.

Mais il n’est pas nécessairement dans NP.

C’est la distinction fondamentale :

NP-complet  
\= dans NP  
\+ NP-difficile

alors que :

NP-difficile  
\= au moins aussi difficile que NP  
mais pas nécessairement dans NP

# 38\. NP-COMPLET VS NP-DIFFICILE

| Propriété | NP-complet | NP-difficile |
| --- | --- | --- |
| Dans NP | Oui | Pas nécessairement |
| Vérification polynomiale | Oui | Pas nécessairement |
| Au moins aussi difficile que NP | Oui | Oui |
| Peut être un problème d’optimisation | Généralement formulation décisionnelle | Oui |
| Peut être indécidable | Non, dans le cadre classique de NP | Dans des formulations très générales, la difficulté peut dépasser le cadre NP |

# 39\. EXEMPLE IMPORTANT : TSP

La version décisionnelle :

Existe-t-il une tournée de longueur ≤ (k) ?

est NP-complète.

La version optimisation :

Quelle est la tournée de longueur minimale ?

est NP-difficile.

Cette distinction montre pourquoi il faut toujours demander :

**De quelle formulation exacte du problème parle-t-on ?**

# 40\. RÉDUCTION

La réduction est l’un des concepts les plus puissants de la théorie de la complexité.

L’idée :

Transformer efficacement un problème (A) en un problème (B).

Si :

\[ A_p B \]

on dit que (A) se réduit polynomialement à (B).

Il existe alors une fonction :

\[ f \]

calculable en temps polynomial telle que :

\[ xA f(x)B \]

# 41\. INTUITION DE LA RÉDUCTION

Supposons que nous sachions résoudre (B).

Si nous pouvons transformer chaque instance de (A) en une instance de (B) efficacement :

Instance A  
↓  
transformation polynomialement calculable  
↓  
Instance B  
↓  
solveur B  
↓  
réponse pour A

alors un solveur de (B) nous donne indirectement un solveur de (A).

# 42\. SENS DE LA RÉDUCTION

Attention à une erreur extrêmement fréquente.

Si :

\[ A_p B \]

cela signifie que :

**B est au moins aussi difficile que A**, relativement à cette réduction.

Ce n’est pas l’inverse.

# 43\. TRANSITIVITÉ

Les réductions polynomialement calculables sont généralement transitives.

Si :

\[ A_p B \]

et :

\[ B_p C \]

alors :

\[ A_p C \]

Cette propriété permet de construire des chaînes de difficulté.

# 44\. PROUVER QU’UN PROBLÈME EST NP-COMPLET

Méthode classique :

## Étape 1

Montrer :

\[ ANP \]

## Étape 2

Choisir un problème connu NP-complet :

\[ B \]

## Étape 3

Construire :

\[ B_p A \]

## Étape 4

Conclure :

\[ A \]

est NP-complet.

# 45\. ERREUR CLASSIQUE DANS LES RÉDUCTIONS

Pour démontrer que (A) est difficile, il faut généralement réduire :

\[ \]

où (B) est déjà connu comme difficile.

Réduire :

\[ AB \]

ne suffit généralement pas à montrer que (A) est aussi difficile que (B).

# 46\. AUTRES TYPES DE RÉDUCTION

Il existe plusieurs notions.

### Réduction many-one

Une seule transformation :

\[ xf(x) \]

### Réduction de Turing

L’algorithme peut utiliser plusieurs appels à un oracle pour le problème cible.

### Réduction polynomial-time

La transformation elle-même est calculable en temps polynomial.

Le choix de la réduction doit toujours être explicité.

# 47\. COMPLEXITÉ ET DÉCIDABILITÉ

Une question essentielle :

« Ce problème est-il difficile ou impossible ? »

Ce ne sont pas les mêmes choses.

Un problème peut être :

### Facile

\[ O(n) \]

### Difficile mais calculable

\[ O(2^n) \]

### Extrêmement coûteux mais calculable

par exemple certaines complexités super-exponentielles.

### Non calculable

aucun algorithme général ne peut le résoudre.

# 48\. DÉCIDABILITÉ

Un problème de décision est décidable s’il existe un algorithme qui :

- répond correctement ;
- termine toujours ;
- pour toute entrée valide.

# 49\. SEMI-DÉCIDABILITÉ

Certains problèmes ne sont pas décidables, mais peuvent être reconnaissables.

Un algorithme peut :

- terminer et répondre OUI lorsqu’une propriété est vraie ;
- ne jamais terminer lorsque la propriété est fausse.

On parle alors de problème reconnaissable ou semi-décidable selon le cadre formel.

# 50\. PROBLÈME DE L’ARRÊT

Le **Halting Problem** demande :

Étant donné un programme (P) et une entrée (x), est-ce que (P(x)) finira par s’arrêter ?

Il n’existe pas d’algorithme général qui réponde correctement à cette question pour tous les programmes et toutes les entrées.

Le problème est donc indécidable.

# 51\. POURQUOI LE PROBLÈME DE L’ARRÊT EST FONDAMENTAL

Il démontre une limite profonde :

Certains problèmes ne sont pas simplement trop lents.

Ils sont :

**impossibles à résoudre algorithmiquement dans le cas général.**

Aucun ajout raisonnable de puissance matérielle ne supprime cette limite théorique.

# 52\. CALCULABILITÉ

Une fonction est calculable lorsqu’il existe un procédé algorithmique permettant de calculer sa valeur pour les entrées concernées.

Les modèles classiques de calcul conduisent à une notion robuste de calculabilité effective.

Cette idée est notamment associée à la **thèse de Church-Turing**.

# 53\. THÈSE DE CHURCH-TURING

Idée fondamentale :

Tout calcul effectivement réalisable par une procédure algorithmique peut être représenté par un modèle de calcul de type machine de Turing.

Ce n’est pas simplement une formule mathématique ordinaire ; c’est une thèse reliant la notion intuitive d’algorithme à des modèles formels.

# 54\. CALCULABILITÉ VS COMPLEXITÉ

C’est probablement la distinction la plus importante du document.

### Calculabilité

Est-ce possible en principe ?

### Complexité

Combien de ressources faut-il ?

Exemple conceptuel :

Problème A  
↓  
calculable  
↓  
O(n²)

Le problème est calculable et relativement efficace.

Autre problème :

Problème B  
↓  
calculable  
↓  
O(2^n)

Le problème est calculable mais potentiellement très difficile.

Autre problème :

Problème C  
↓  
non calculable

Aucun algorithme général ne peut le résoudre.

# 55\. LES GRANDES CLASSES DE COMPLEXITÉ

P et NP ne constituent qu’une petite partie de la théorie.

On rencontre notamment :

- P ;
- NP ;
- co-NP ;
- PSPACE ;
- EXP ;
- EXPSPACE ;
- classes probabilistes ;
- classes paramétrées ;
- classes d’approximation ;
- classes de comptage.

# 56\. CO-NP

co-NP est lié aux complémentaires des problèmes de NP.

Si :

\[ LNP \]

alors :

\[ LcoNP \]

La relation :

\[ PNPcoNP \]

est connue.

La relation exacte entre NP et co-NP soulève également des questions profondes.

# 57\. PSPACE

\[ PSPACE \]

désigne les problèmes résolubles avec une quantité de mémoire polynomialement bornée.

On connaît notamment :

\[ PNPPSPACE \]

mais plusieurs égalités ou séparations entre ces classes restent ouvertes.

# 58\. EXP

\[ EXP \]

regroupe les problèmes pouvant être résolus en temps exponentiel, typiquement sous une forme :

\[ 2<sup>{n</sup>k} \]

pour une constante (k).

On a :

\[ PEXP \]

et cette inclusion est connue comme stricte dans les cadres classiques.

# 59\. HIÉRARCHIE INTUITIVE

Une vision simplifiée :

P  
│  
├── problèmes polynomialement efficaces  
│  
NP  
│  
├── solutions vérifiables polynomialement  
│  
PSPACE  
│  
├── mémoire polynomialement bornée  
│  
EXP  
│  
└── temps exponentiel

Cette représentation ne doit cependant pas être interprétée comme une simple échelle « du facile à l’impossible ».

Les classes ont des définitions précises et leurs relations sont des objets mathématiques.

# 60\. COMPLEXITÉ DES PROBLÈMES D’OPTIMISATION

La complexité ne concerne pas uniquement les réponses OUI/NON.

On peut distinguer :

### Décision

Existe-t-il une solution d’une qualité au moins (k) ?

### Recherche

Donne-moi une solution valide.

### Optimisation

Donne-moi la meilleure solution.

### Comptage

Combien existe-t-il de solutions ?

Ces formulations peuvent avoir des complexités différentes.

# 61\. COMPLEXITÉ DU COMPTAGE

Compter peut être beaucoup plus difficile que décider.

Exemple :

SAT :  
"Existe-t-il une solution ?"  
<br/>vs  
<br/>#SAT :  
"Combien existe-t-il de solutions ?"

Cela mène notamment à la classe :

\[ #P \]

qui est importante en :

- probabilités computationnelles ;
- statistiques ;
- physique computationnelle ;
- réseaux ;
- IA ;
- inférence probabiliste.

# 62\. COMPLEXITÉ PARAMÉTRÉE

La complexité classique considère principalement :

\[ n \]

comme paramètre de taille.

Mais certains problèmes possèdent une structure supplémentaire.

On peut introduire un paramètre :

\[ k \]

et rechercher une complexité de la forme :

\[ f(k)n^{O(1)} \]

C’est l’idée centrale de la **Fixed-Parameter Tractability**, ou FPT.

# 63\. POURQUOI LA COMPLEXITÉ PARAMÉTRÉE EST PUISSANTE

Un problème globalement difficile peut devenir raisonnablement traitable si :

- un paramètre reste petit ;
- la difficulté exponentielle dépend seulement de ce paramètre ;
- la dépendance en (n) reste polynomiale.

Exemple conceptuel :

\[ 2^k n^3 \]

peut être acceptable si :

\[ kn \]

# 64\. COMPLEXITÉ D’APPROXIMATION

Lorsqu’un problème exact est trop difficile, on peut chercher :

une solution suffisamment proche de l’optimum.

Au lieu de :

\[ OPT \]

on cherche :

\[ SOL \]

avec une garantie du type :

\[ SOLOPT \]

pour un problème de minimisation.

Cela conduit aux :

- algorithmes d’approximation ;
- approximation schemes ;
- heuristiques ;
- métaheuristiques.

# 65\. HEURISTIQUES

Une heuristique cherche une solution efficace sans garantir nécessairement :

- l’optimalité ;
- une borne théorique universelle ;
- une performance identique sur toutes les instances.

Elle peut néanmoins être extrêmement utile en pratique.

Exemples :

- recherche locale ;
- recuit simulé ;
- algorithmes génétiques ;
- colonies de fourmis ;
- beam search ;
- stratégies gloutonnes.

# 66\. COMPLEXITÉ ET NP-DIFFICULTÉ : CE N’EST PAS « IMPOSSIBLE »

Dire :

« Le problème est NP-difficile »

ne signifie pas :

« Aucun programme ne peut le résoudre. »

Cela signifie essentiellement que, selon les réductions utilisées, le problème est au moins aussi difficile que les problèmes de NP.

On peut toujours avoir :

- des solutions exactes pour petites instances ;
- des cas particuliers polynomiaux ;
- des heuristiques ;
- des approximations ;
- des solveurs spécialisés ;
- de la programmation parallèle ;
- de la programmation dynamique ;
- des méthodes paramétrées.

# 67\. LE RÔLE DE LA TAILLE DES INSTANCES

Un algorithme exponentiel :

\[ O(2^n) \]

peut être acceptable pour :

\[ n=20 \]

mais devenir impraticable pour :

\[ n=100 \]

car :

\[ 2<sup>{20}</sup>6 \]

alors que :

\[ 2<sup>{100},27</sup>{30} \]

La croissance asymptotique explique cette explosion.

# 68\. COMPLEXITÉ ET SCALABILITÉ

La scalabilité demande :

Que se passe-t-il lorsque la charge augmente ?

Il faut examiner :

- taille des données ;
- nombre d’utilisateurs ;
- fréquence des requêtes ;
- taille des graphes ;
- nombre de paramètres ;
- nombre de modèles ;
- volume des fichiers ;
- nombre de nœuds ;
- fréquence des appels.

# 69\. COMPLEXITÉ D’UNE API

Supposons :

GET /search?q=...

Si chaque requête parcourt :

\[ n \]

éléments :

\[ O(n) \]

Avec :

\[ R \]

requêtes simultanées :

\[ O(Rn) \]

Mais une indexation adaptée peut transformer certaines recherches en :

\[ O(n) \]

ou en temps moyen proche de :

\[ O(1) \]

selon la structure.

La théorie de la complexité devient donc directement une question d’architecture.

# 70\. COMPLEXITÉ DES BASES DE DONNÉES

La complexité intervient dans :

- recherche ;
- indexation ;
- jointures ;
- tri ;
- agrégation ;
- pagination ;
- recherche full-text ;
- graph queries.

Une mauvaise requête peut transformer une opération raisonnable en :

\[ O(n^2) \]

ou pire.

# 71\. COMPLEXITÉ ET N+1

Le problème N+1 illustre une mauvaise composition algorithmique.

Au lieu de :

1 requête globale

on effectue :

1 requête  
+  
n requêtes supplémentaires

La complexité n’est pas nécessairement uniquement une notation asymptotique, mais le phénomène peut provoquer une explosion du coût total lorsque (n) augmente.

# 72\. COMPLEXITÉ ET IA

La théorie de la complexité intervient partout en IA :

- recherche ;
- planification ;
- optimisation ;
- apprentissage ;
- inférence ;
- génération ;
- clustering ;
- graph learning ;
- vision ;
- reconnaissance ;
- raisonnement symbolique.

Une question essentielle devient :

**Quelle partie du problème est intrinsèquement coûteuse ?**

# 73\. COMPLEXITÉ DE L’APPRENTISSAGE

L’entraînement d’un modèle peut dépendre de :

- nombre d’exemples ;
- nombre de paramètres ;
- nombre d’époques ;
- taille des batchs ;
- complexité du modèle ;
- coût de chaque couche ;
- coût mémoire ;
- coût des communications distribuées.

Il faut donc distinguer :

\[ \]

et :

\[ \]

# 74\. COMPLEXITÉ ET TRANSFORMERS

Attention à une ambiguïté linguistique.

Le mot **transformer** dans l’IA désigne une architecture neuronale.

La **théorie de la complexité** n’a aucun rapport direct avec le terme mathématique « transformée ».

Cependant, la complexité computationnelle est fondamentale dans les Transformers.

Par exemple, une attention dense naïve sur une séquence de longueur (n) implique typiquement un coût quadratique en (n) pour la construction des interactions attentionnelles :

\[ O(n^2) \]

Cette observation motive de nombreuses recherches sur :

- attention sparse ;
- attention locale ;
- attention linéaire ;
- kernels ;
- mémoire externe ;
- architectures hiérarchiques.

# 75\. COMPLEXITÉ ET MÉMOIRE EN IA

Une opération peut avoir une complexité temporelle acceptable mais nécessiter une mémoire prohibitive.

Pour un modèle, il faut considérer :

\[

- \]

La complexité spatiale devient donc aussi importante que la complexité temporelle.

# 76\. COMPLEXITÉ ET DISTRIBUTION

La parallélisation peut accélérer un calcul, mais elle ne supprime pas nécessairement sa complexité fondamentale.

Il faut considérer :

- coût du calcul ;
- coût de communication ;
- synchronisation ;
- équilibrage de charge ;
- latence ;
- bande passante ;
- réplication.

Ainsi :

\[ T_{} = T_{}

- T_{}
- T_{} \]

# 77\. LOI D’AMDAHL

Lorsqu’une fraction du programme est parallélisée, l’accélération globale est limitée par la partie séquentielle.

Si (p) est la fraction parallélisable et (s) le nombre de processeurs :

\[ Speedup = \]

Même avec :

\[ s \]

on obtient :

\[ Speedup_{}= \]

Cela montre pourquoi l’architecture doit être pensée avec la complexité et non uniquement avec la puissance matérielle.

# 78\. COMPLEXITÉ ET LATENCE

Deux systèmes peuvent avoir la même complexité asymptotique mais des latences très différentes.

Par exemple :

\[ T_1(n)=10^3n \]

et :

\[ T_2(n)=n \]

ont tous deux :

\[ (n) \]

mais leurs performances réelles peuvent être très différentes.

La notation asymptotique n’est donc pas un chronomètre.

# 79\. COMPLEXITÉ ASYMPTOTIQUE ≠ PERFORMANCE RÉELLE

La complexité permet de comprendre la croissance.

Elle ne remplace pas :

- benchmark ;
- profilage ;
- mesure mémoire ;
- observation de la latence ;
- analyse I/O ;
- tests de charge.

La bonne approche est :

Analyse théorique  
+  
Mesure expérimentale  
+  
Profilage  
+  
Analyse de charge

# 80\. COMPLEXITÉ ET CONSTANTES

Dire :

\[ O(n) \]

ignore les constantes.

Pourtant :

\[ 1000n \]

et :

\[ n \]

peuvent être très différents dans un système réel.

La notation asymptotique devient surtout informative lorsque l’on s’intéresse à l’évolution de (n).

# 81\. COMPLEXITÉ ET CACHE

Deux algorithmes peuvent avoir la même complexité :

\[ O(n) \]

mais des comportements matériels très différents à cause :

- cache CPU ;
- localité mémoire ;
- vectorisation ;
- branchements ;
- accès disque ;
- accès réseau.

Il faut donc distinguer :

**complexité abstraite**

et :

**coût matériel réel.**

# 82\. COMPLEXITÉ DE LECTURE/ÉCRITURE

Dans les systèmes modernes, les ressources ne sont pas seulement :

- CPU ;
- RAM.

Il faut aussi considérer :

- I/O ;
- réseau ;
- stockage ;
- GPU ;
- mémoire distribuée ;
- appels API ;
- énergie.

On peut donc définir plusieurs modèles de coût.

# 83\. COMPLEXITÉ ÉNERGÉTIQUE

Pour des systèmes embarqués ou massifs, la quantité d’énergie consommée devient une ressource computationnelle importante.

On peut alors chercher à réduire :

- nombre d’opérations ;
- transferts mémoire ;
- communications ;
- calculs inutiles.

Cela devient particulièrement pertinent en :

- edge AI ;
- IoT ;
- robotique ;
- systèmes embarqués ;
- mobile computing.

# 84\. COMPLEXITÉ ET ALGORITHMES EN LIGNE

Dans un algorithme online, les données arrivent progressivement.

Il faut analyser :

- coût par élément ;
- mémoire nécessaire ;
- coût total ;
- latence ;
- comportement dans le pire cas.

Les algorithmes streaming sont particulièrement importants lorsque les données ne peuvent pas être chargées entièrement en mémoire.

# 85\. COMPLEXITÉ ET ALGORITHMES RANDOMISÉS

Certains algorithmes utilisent le hasard.

On analyse alors :

- temps attendu ;
- probabilité d’erreur ;
- pire cas ;
- variance ;
- amplification de probabilité.

Les algorithmes randomisés peuvent transformer certains problèmes difficiles en solutions extrêmement efficaces en pratique.

# 86\. COMPLEXITÉ ET APPROCHE PROBABILISTE

Il faut distinguer :

temps déterministe  
temps espéré  
probabilité d'erreur  
probabilité de succès

Une affirmation comme :

« L’algorithme est (O(n)) »

est incomplète si l’algorithme est randomisé et que la borne concerne seulement l’espérance.

# 87\. COMPLEXITÉ DES ALGORITHMES APPROXIMATIFS

Un algorithme peut avoir :

\[ T(n)=O(n^3) \]

et fournir une solution exacte.

Un autre :

\[ T(n)=O(nn) \]

peut fournir une approximation.

La bonne décision dépend donc de :

\[

- \]

# 88\. COMPLEXITÉ ET QUALITÉ DE SOLUTION

Pour certains problèmes, chercher exactement l’optimum est inutilement coûteux.

On peut rechercher :

\[ \]

plutôt que :

\[ \]

Cette idée est fondamentale dans :

- planification ;
- logistique ;
- allocation ;
- ordonnancement ;
- génération ;
- recherche ;
- optimisation de réseaux.

# 89\. LE TRIANGLE : EXACTITUDE, OPTIMALITÉ, TEMPS

Pour les problèmes difficiles :

Solution exacte  
/\\  
/ \\  
/ \\  
/ \\  
temps raisonnable ── optimalité

Il faut parfois accepter un compromis.

Exemple :

- solution exacte + temps énorme ;
- solution approximative + temps faible ;
- solution heuristique + qualité variable.

# 90\. RECONNAÎTRE UN PROBLÈME POTENTIELLEMENT DIFFICILE

Signaux d’alerte :

- « trouver la meilleure configuration » ;
- « essayer toutes les combinaisons » ;
- « toutes les permutations » ;
- « toutes les sous-ensembles » ;
- « affecter chaque élément à une catégorie » ;
- « trouver le meilleur itinéraire » ;
- « satisfaire simultanément toutes ces contraintes » ;
- « choisir le sous-ensemble optimal » ;
- « planifier toutes les tâches » ;
- « trouver une configuration sans conflit ».

Ces formulations doivent immédiatement déclencher une analyse de complexité.

# 91\. COMBINATOIRE ET EXPLOSION

Si chaque élément peut prendre (k) états :

\[ k^n \]

possibilités apparaissent.

Si l’on doit examiner toutes les permutations :

\[ n! \]

Si l’on doit examiner tous les sous-ensembles :

\[ 2^n \]

Ces structures expliquent une grande partie des explosions combinatoires.

# 92\. FORCE BRUTE

La force brute consiste à explorer systématiquement toutes les possibilités.

Avantages :

- simple ;
- exacte ;
- facile à vérifier.

Inconvénient :

\[ \]

peut croître exponentiellement ou factoriellement.

La question devient alors :

Peut-on exploiter une structure mathématique pour éviter l’exploration complète ?

# 93\. STRATÉGIES POUR RÉDUIRE LA COMPLEXITÉ

Lorsqu’un algorithme est trop coûteux, plusieurs stratégies existent :

1.  meilleure structure de données ;
2.  meilleur algorithme ;
3.  indexation ;
4.  mémoïsation ;
5.  programmation dynamique ;
6.  divide and conquer ;
7.  pruning ;
8.  branch and bound ;
9.  approximation ;
10. heuristique ;
11. randomisation ;
12. paramétrisation ;
13. parallélisation ;
14. pré-calcul ;
15. cache ;
16. relaxation du problème.

# 94\. PROGRAMMATION DYNAMIQUE ET COMPLEXITÉ

La programmation dynamique exploite la présence de :

- sous-problèmes chevauchants ;
- sous-structure optimale.

Elle peut transformer un algorithme exponentiel naïf en algorithme polynomial dans certains problèmes.

Exemple conceptuel :

récursion naïve  
↓  
beaucoup de recomputations  
↓  
mémoïsation  
↓  
chaque sous-problème calculé une fois  
↓  
forte réduction du coût

# 95\. BRANCH AND BOUND

Branch and Bound explore un espace de solutions tout en éliminant les branches qui ne peuvent pas produire une meilleure solution.

Le pire cas peut rester exponentiel.

Mais l’élagage peut rendre la méthode extrêmement efficace sur certaines instances.

# 96\. PRUNING

Le pruning consiste à supprimer des parties de l’espace de recherche qui ne peuvent plus produire une solution utile.

Applications :

- recherche ;
- jeux ;
- optimisation ;
- SAT ;
- planification ;
- IA symbolique.

# 97\. COMPLEXITÉ ET SAT SOLVERS

Les solveurs SAT modernes exploitent de nombreuses techniques :

- propagation ;
- apprentissage de clauses ;
- heuristiques ;
- backtracking ;
- branching ;
- prétraitement.

Le fait que SAT soit NP-complet n’empêche donc pas les solveurs modernes d’être extrêmement performants sur de nombreuses instances réelles.

C’est une distinction importante entre :

**difficulté théorique dans le pire cas**

et :

**performance empirique sur des distributions d’instances réelles.**

# 98\. PIRE CAS VS MONDE RÉEL

Un problème peut être :

\[ NP \]

tout en étant facilement résoluble pour :

- petites instances ;
- instances structurées ;
- données réelles ;
- cas particuliers ;
- instances avec paramètres favorables.

La NP-complétude est une propriété théorique du problème général.

# 99\. CAS PARTICULIERS

Un problème globalement difficile peut avoir des sous-cas faciles.

Exemple conceptuel :

Problème général  
│  
┌─────┼──────┐  
│ │ │  
cas A cas B cas C  
│ │ │  
P P difficile

Il faut donc toujours rechercher :

**La structure particulière de mes données permet-elle de sortir du pire cas général ?**

# 100\. COMPLEXITÉ ET MODÉLISATION

Parfois, le problème n’est pas l’algorithme.

C’est le modèle.

Une mauvaise formulation peut transformer un problème simple en problème difficile.

Exemple :

Problème original  
↓  
mauvaise représentation  
↓  
espace énorme  
↓  
algorithme coûteux

Une bonne représentation peut produire :

Problème original  
↓  
structure mathématique  
↓  
nouvelle formulation  
↓  
algorithme efficace

# 101\. LE PRINCIPE DE DOMINATION

Dans une expression :

\[ T(n)=5n<sup>3+10n</sup>2+100n+50 \]

le terme dominant est :

\[ n^3 \]

donc :

\[ T(n)=(n^3) \]

Pour l’analyse asymptotique, les termes inférieurs deviennent négligeables lorsque (n) devient suffisamment grand.

# 102\. LOGARITHMES

Les logarithmes apparaissent constamment dans la complexité.

Une division répétée par 2 donne :

\[ n,n2,n4,n8, \]

Après (k) étapes :

\[ \]

Pour atteindre 1 :

\[ 2^k=n \]

donc :

\[ k=\_2 n \]

C’est pourquoi :

- recherche binaire ;
- arbres équilibrés ;
- divide and conquer ;

produisent souvent des complexités logarithmiques.

# 103\. COMPLEXITÉ LOGARITHMIQUE

\[ O(n) \]

est extrêmement favorable.

Doubler (n) n’augmente le coût que d’une quantité constante.

C’est l’une des raisons pour lesquelles les structures équilibrées et les index sont si puissants.

# 104\. COMPLEXITÉ LINÉAIRE

\[ O(n) \]

signifie que doubler la taille double approximativement le nombre d’opérations asymptotiquement.

C’est souvent optimal lorsqu’il faut nécessairement examiner tous les éléments.

# 105\. COMPLEXITÉ (nn)

\[ O(nn) \]

est fréquente dans :

- tri efficace ;
- divide and conquer ;
- certains algorithmes géométriques ;
- traitement de données.

Elle reste généralement très exploitable à grande échelle.

# 106\. COMPLEXITÉ QUADRATIQUE

\[ O(n^2) \]

devient rapidement problématique.

Si :

\[ n10n \]

alors :

\[ n<sup>2100n</sup>2 \]

Le coût est multiplié par environ 100.

# 107\. COMPLEXITÉ EXPONENTIELLE

\[ O(2^n) \]

double approximativement à chaque augmentation de (n) de 1.

Cela produit une explosion extrêmement rapide.

# 108\. COMPLEXITÉ FACTORIELLE

\[ O(n!) \]

est encore plus explosive.

Les permutations deviennent rapidement impossibles à explorer exhaustivement.

# 109\. COMPLEXITÉ SUPER-EXPONENTIELLE

Certaines fonctions croissent plus vite que :

\[ c^n \]

pour toute constante fixe (c).

Ces complexités apparaissent dans des problèmes particulièrement difficiles.

# 110\. COMPLEXITÉ ET ENCODAGE DE L’ENTRÉE

Un point avancé mais crucial :

la complexité dépend de la manière dont l’entrée est représentée.

Exemple :

un entier (N) possède environ :

\[ \_2N \]

bits.

Un algorithme polynomial en (N) peut donc être exponentiel en la taille binaire de l’entrée.

Cela explique pourquoi la théorie de la complexité définit soigneusement la taille des instances.

# 111\. COMPLEXITÉ DES NOMBRES

Pour des problèmes numériques, il faut distinguer :

- taille de la valeur ;
- taille de sa représentation ;
- nombre de bits ;
- précision demandée.

Cela devient particulièrement important en :

- cryptographie ;
- calcul numérique ;
- théorie des nombres ;
- optimisation ;
- calcul scientifique.

# 112\. COMPLEXITÉ ET PRÉCISION

Dans certains problèmes numériques, la taille du nombre ne suffit pas.

Il faut aussi considérer :

\[ p= \]

Le coût peut alors dépendre de :

\[ n,p \]

et non seulement de (n).

# 113\. COMPLEXITÉ DES ALGORITHMES NUMÉRIQUES

Un algorithme peut avoir :

\[ O(n^3) \]

opérations arithmétiques mais le coût de chaque opération peut lui-même dépendre de la taille des nombres manipulés.

Il existe donc une distinction entre :

- complexité arithmétique ;
- complexité bit ;
- complexité mémoire.

# 114\. COMPLEXITÉ ET CRYPTOGRAPHIE

La cryptographie dépend profondément de la complexité.

Une construction cryptographique cherche souvent à rendre certaines opérations :

- faciles pour le propriétaire de la clé ;
- difficiles pour un attaquant.

On cherche donc une asymétrie computationnelle.

Exemple conceptuel :

opération légitime  
↓  
rapide  
<br/>inversion sans secret  
↓  
très difficile

La sécurité computationnelle dépend alors d’hypothèses sur la difficulté de certains problèmes.

# 115\. COMPLEXITÉ ET SÉCURITÉ

Un système sécurisé doit considérer :

\[ \]

contre :

\[ \]

Si une attaque est :

\[ O(2^n) \]

elle peut être impraticable pour une valeur suffisamment grande de (n).

Mais si une amélioration transforme l’attaque en :

\[ O(n^3) \]

la situation change complètement.

# 116\. COMPLEXITÉ ET IA AGENTIQUE

Pour un agent autonome, la complexité peut apparaître dans :

- recherche d’actions ;
- planification ;
- génération de trajectoires ;
- raisonnement ;
- exploration ;
- allocation de ressources ;
- sélection d’outils ;
- recherche dans des documents ;
- planification multi-étapes.

Un agent ne doit donc pas simplement chercher :

« la meilleure action ».

Il peut devoir chercher :

« une bonne action trouvée suffisamment rapidement sous contrainte de budget ».

# 117\. COMPLEXITÉ ET RECHERCHE DANS UN ESPACE D’ACTIONS

Si un agent possède :

\[ b \]

actions possibles à chaque étape et cherche jusqu’à profondeur :

\[ d \]

alors une exploration naïve peut avoir :

\[ O(b^d) \]

états.

Cela explique la nécessité de :

- heuristiques ;
- pruning ;
- recherche guidée ;
- mémorisation ;
- approximation ;
- planification hiérarchique.

# 118\. COMPLEXITÉ ET RECHERCHE DOCUMENTAIRE

Une recherche naïve sur :

\[ n \]

documents coûte potentiellement :

\[ O(n) \]

par requête.

Une indexation adaptée peut réduire fortement le coût.

C’est l’un des grands principes derrière :

- index inversés ;
- arbres ;
- structures de recherche ;
- bases vectorielles ;
- caches.

# 119\. COMPLEXITÉ ET SYSTÈMES VECTORIELS

Dans une recherche vectorielle naïve :

\[ n \]

vecteurs de dimension :

\[ d \]

peuvent nécessiter approximativement :

\[ O(nd) \]

pour comparer une requête à tous les vecteurs.

Les méthodes ANN cherchent à réduire ce coût au prix éventuel d’un compromis :

\[ \]

# 120\. COMPLEXITÉ ET ARCHITECTURE LOGICIELLE

La complexité doit influencer l’architecture dès la conception.

Avant d’implémenter :

fonction  
↓  
API  
↓  
service  
↓  
base de données

il faut demander :

- quelle est la taille de l’entrée ?
- combien d’utilisateurs ?
- combien d’appels ?
- quelle fréquence ?
- quelle complexité ?
- quelle mémoire ?
- quelle latence acceptable ?
- quelle croissance prévue ?

# 121\. WORKFLOW D’ANALYSE DE COMPLEXITÉ

Lorsqu’un nouvel algorithme apparaît :

## Étape 1 — Définir l’entrée

Quelle variable représente la taille ?

\[ n=? \]

## Étape 2 — Identifier les opérations dominantes

Quelles opérations coûtent réellement ?

## Étape 3 — Compter

Combien de fois sont-elles exécutées ?

## Étape 4 — Construire (T(n))

\[ T(n)=? \]

## Étape 5 — Simplifier

Obtenir :

\[ O,, \]

## Étape 6 — Examiner les cas

- meilleur ;
- moyen ;
- pire.

## Étape 7 — Examiner l’espace

\[ S(n)=? \]

## Étape 8 — Tester la scalabilité

Que se passe-t-il lorsque :

\[ n=10<sup>3, 10</sup>5, 10^7, \]

## Étape 9 — Chercher une meilleure stratégie

- structure ;
- index ;
- DP ;
- pruning ;
- approximation ;
- parallélisme.

# 122\. WORKFLOW POUR UN PROBLÈME NOUVEAU

Lorsqu’on rencontre un problème jamais vu :

1\. Définir précisément le problème  
↓  
2\. Identifier entrée / sortie  
↓  
3\. Décision / recherche / optimisation / comptage ?  
↓  
4\. Chercher une formulation connue  
↓  
5\. Chercher un algorithme polynomial connu  
↓  
6\. Chercher une réduction connue  
↓  
7\. Tester l'appartenance à une classe  
↓  
8\. Chercher cas particuliers  
↓  
9\. Chercher approximation / heuristique  
↓  
10\. Évaluer la scalabilité

# 123\. TABLEAU DE RECONNAISSANCE RAPIDE

| Situation | Réflexe |
| --- | --- |
| boucle simple | (O(n)) |
| boucles imbriquées | multiplier les coûts |
| division par 2 répétée | (O(n)) |
| divide and conquer | récurrence |
| toutes les paires | (O(n^2)) |
| tous les sous-ensembles | (2^n) |
| toutes les permutations | (n!) |
| recherche dichotomique | (O(n)) |
| tri efficace | souvent (O(nn)) |
| recherche combinatoire | vérifier NP / exponentiel |
| optimisation globale | rechercher NP-difficulté |
| vérification rapide d’une solution | penser NP |
| réduction depuis un NP-complet | penser NP-complet |
| question « existe-t-il un algorithme ? » | calculabilité |
| question « l’algorithme termine-t-il toujours ? » | décidabilité |
| contrainte mémoire | complexité spatiale |
| croissance à grande échelle | analyse asymptotique |

# 124\. ERREURS CLASSIQUES

## Erreur 1

Dire :

« Big-O = complexité exacte »

Faux.

Big-O donne une borne supérieure asymptotique.

## Erreur 2

Dire :

« Big-O donne toujours le pire cas »

Faux.

On peut donner un Big-O du meilleur, du moyen ou du pire cas.

## Erreur 3

Confondre :

\[ O(n^2) \]

et :

\[ (n^2) \]

Le second est plus précis.

## Erreur 4

Dire :

« NP signifie non polynomial »

Faux.

NP signifie historiquement **nondeterministic polynomial time**.

L’interprétation « solutions vérifiables polynomialement » est l’intuition pratique la plus utile.

## Erreur 5

Dire :

« NP = problèmes impossibles »

Faux.

Les problèmes NP sont décidables dans le cadre classique.

## Erreur 6

Dire :

« NP-complet = impossible à résoudre »

Faux.

Il s’agit d’une difficulté théorique, principalement concernant l’existence d’algorithmes polynomiaux.

## Erreur 7

Dire :

« NP-difficile signifie indécidable »

Faux.

NP-difficile et indécidable appartiennent à des niveaux conceptuels différents.

## Erreur 8

Inverser une réduction.

Pour montrer que (A) est au moins aussi difficile que (B), il faut généralement construire :

\[ B_p A \]

et non :

\[ A_p B \]

## Erreur 9

Confondre calculabilité et complexité.

Un problème peut être :

- calculable mais extrêmement coûteux ;
- non calculable.

## Erreur 10

Croire que l’amélioration matérielle résout toute complexité.

Une machine plus rapide réduit les constantes.

Elle ne transforme pas automatiquement :

\[ 2^n \]

en :

\[ n^2 \]

# 125\. MATRICE DE DÉCISION

| Question | Domaine |
| --- | --- |
| Existe-t-il un algorithme ? | Calculabilité |
| L’algorithme termine-t-il toujours ? | Décidabilité |
| Combien d’opérations ? | Complexité temporelle |
| Combien de mémoire ? | Complexité spatiale |
| Comment croît le coût ? | Analyse asymptotique |
| Le problème est-il polynomial ? | P   |
| Une solution est-elle vérifiable rapidement ? | NP  |
| Le problème est-il aussi difficile que tous les problèmes NP ? | NP-difficile |
| Est-il à la fois dans NP et NP-difficile ? | NP-complet |
| Peut-on comparer deux problèmes ? | Réduction |
| L’exact est trop coûteux ? | Approximation / heuristique |
| Un paramètre est petit ? | Complexité paramétrée |

# 126\. CARTE MENTALE GLOBALE

THÉORIE DE LA COMPLEXITÉ  
│  
┌───────────────────┼───────────────────┐  
│ │ │  
CALCULABILITÉ COMPLEXITÉ RÉDUCTIONS  
│ │ │  
Peut-on ? Combien ? Comparer ?  
│ │ │  
┌─────┴─────┐ ┌─────┴─────┐ A ≤ B  
│ │ │ │  
Décidable Indécidable Temps Espace  
│ │  
┌─────┼─────┐ │  
│ │ │ │  
P NP EXP PSPACE  
│  
┌──────┴──────┐  
│ │  
NP-complet NP-difficile

# 127\. FICHE DE RECONNAISSANCE O01 — BIG-O

### Concept

Borne supérieure asymptotique.

### Formule

\[ f(n)=O(g(n)) \]

### Question

Jusqu’à quel ordre (f) peut-il croître ?

### Usage

- analyse d’algorithmes ;
- architecture ;
- comparaison de solutions.

# 128\. FICHE O02 — THÊTA

### Concept

Ordre asymptotique exact.

\[ f(n)=(g(n)) \]

### Question

Quel est réellement l’ordre de croissance ?

# 129\. FICHE O03 — OMEGA

### Concept

Borne inférieure asymptotique.

\[ f(n)=(g(n)) \]

### Question

Quel coût minimal asymptotique doit-on accepter ?

# 130\. FICHE O04 — COMPLEXITÉ TEMPORELLE

### Concept

Nombre asymptotique d’opérations.

### Variables

\[ T(n) \]

### Objectif

Mesurer la croissance du temps de calcul.

# 131\. FICHE O05 — COMPLEXITÉ SPATIALE

### Concept

Quantité asymptotique de mémoire.

\[ S(n) \]

### Applications

- systèmes embarqués ;
- backend ;
- bases de données ;
- IA ;
- calcul scientifique.

# 132\. FICHE O06 — P

\[ P= \]

Intuition :

problèmes efficacement calculables dans le modèle classique.

# 133\. FICHE O07 — NP

Intuition :

problèmes dont une solution candidate peut être vérifiée en temps polynomial.

Relation :

\[ PNP \]

# 134\. FICHE O08 — NP-COMPLET

\[ NP = NP NP \]

Ce sont les problèmes les plus difficiles de NP selon les réductions polynomialement calculables.

# 135\. FICHE O09 — NP-DIFFICILE

Un problème au moins aussi difficile que les problèmes de NP sous la notion de réduction considérée.

Il n’est pas nécessairement dans NP.

# 136\. FICHE O10 — RÉDUCTION

Transformation efficace :

\[ A_p B \]

permettant de convertir les instances de (A) en instances de (B).

C’est l’un des principaux outils pour démontrer la difficulté.

# 137\. FICHE O11 — DÉCIDABILITÉ

Un problème est décidable s’il existe une procédure qui :

- accepte toute entrée valide ;
- répond correctement ;
- termine toujours.

# 138\. FICHE O12 — CALCULABILITÉ

Question :

Existe-t-il un algorithme permettant de calculer la fonction ou de résoudre le problème ?

Elle se situe à un niveau plus fondamental que la complexité.

# 139\. FICHE O13 — PROBLÈME DE L’ARRÊT

Problème :

\[ \]

dans le cas général.

Réponse :

aucun algorithme général ne peut toujours répondre correctement.

# 140\. FICHE O14 — RÉCURRENCE

Une relation comme :

\[ T(n)=aT(n/b)+f(n) \]

permet d’analyser les algorithmes récursifs.

# 141\. FICHE O15 — MASTER THEOREM

Outil permettant de résoudre de nombreuses récurrences de type divide and conquer.

Forme :

\[ T(n)=aT(n/b)+f(n) \]

# 142\. FICHE O16 — COMPLEXITÉ AMORTIE

Analyse du coût moyen sur une séquence d’opérations.

Particulièrement importante pour les structures dynamiques.

# 143\. FICHE O17 — COMPLEXITÉ PARAMÉTRÉE

Recherche d’une complexité :

\[ f(k)n^{O(1)} \]

lorsqu’un paramètre (k) est petit.

# 144\. FICHE O18 — APPROXIMATION

Remplacer :

\[ solution optimale \]

par :

\[ solution suffisamment bonne \]

avec éventuellement une garantie mathématique.

# 145\. FICHE O19 — HEURISTIQUE

Méthode pratique qui cherche une bonne solution sans garantie générale d’optimalité.

# 146\. FICHE O20 — EXPLOSION COMBINATOIRE

Croissance rapide de l’espace des possibilités :

\[ 2^n,k^n,n! \]

Elle constitue l’un des principaux mécanismes derrière les problèmes computationnellement difficiles.

# 147\. PROJETS D’APPRENTISSAGE — NIVEAU 1

## Projet 1 — Analyseur de complexité

Construire un outil permettant d’entrer des fragments simples de pseudo-code et d’obtenir une estimation :

\[ O(1),O(n),O(n),O(nn),O(n^2),… \]

Objectif :

comprendre réellement la croissance.

# 148\. PROJET NIVEAU 2 — LABORATOIRE DE CROISSANCE

Implémenter :

- (n) ;
- (nn) ;
- (n^2) ;
- (n^3) ;
- (2^n) ;
- (n!).

Mesurer le temps réel pour différentes tailles.

Comparer :

\[ \]

avec :

\[ \]

# 149\. PROJET NIVEAU 3 — COMPARATEUR D’ALGORITHMES

Implémenter plusieurs solutions au même problème :

solution naïve  
solution améliorée  
solution optimale

Comparer :

- complexité ;
- temps ;
- mémoire ;
- comportement lorsque (n) augmente.

# 150\. PROJET NIVEAU 4 — TSP

Implémenter :

1.  force brute ;
2.  heuristique gloutonne ;
3.  recherche locale ;
4.  éventuellement programmation dynamique pour petites instances.

Observer expérimentalement l’explosion combinatoire.

# 151\. PROJET NIVEAU 5 — SAT

Construire un petit solveur SAT naïf.

Puis ajouter :

- pruning ;
- propagation ;
- heuristique de choix ;
- apprentissage simple.

Objectif :

comprendre pourquoi la structure algorithmique compte autant même dans un problème théoriquement difficile.

# 152\. PROJET NIVEAU 6 — LABORATOIRE P VS NP

Choisir plusieurs problèmes :

- recherche ;
- tri ;
- SAT ;
- clique ;
- chemin ;
- subset sum.

Pour chacun :

1.  définir la version décisionnelle ;
2.  définir la version recherche ;
3.  identifier le certificat ;
4.  analyser sa vérification ;
5.  rechercher sa classe de complexité.

# 153\. PROJET NIVEAU 7 — DÉCIDABILITÉ

Construire une petite machine de Turing ou un simulateur.

Explorer :

- programmes qui terminent ;
- programmes qui bouclent ;
- détection de cycles ;
- limites d’un détecteur général.

Objectif :

comprendre intuitivement pourquoi le problème de l’arrêt est différent d’un simple problème de performance.

# 154\. DÉFI SANS IA

Pour chaque algorithme :

1.  écrire l’algorithme ;
2.  déterminer (n) ;
3.  compter les opérations ;
4.  proposer (T(n)) ;
5.  déterminer (O) ;
6.  déterminer () si possible ;
7.  déterminer () ;
8.  analyser l’espace ;
9.  analyser meilleur/pire cas ;
10. vérifier expérimentalement.

Interdiction :

rechercher directement la réponse.

L’objectif est de développer l’intuition algorithmique.

# 155\. DÉFI AVEC IA

Donner à une IA un algorithme volontairement inefficace.

Demander :

« Analyse sa complexité, identifie les goulots d’étranglement et propose trois améliorations. »

Puis vérifier manuellement :

- les bornes ;
- les hypothèses ;
- les réductions ;
- les compromis.

L’objectif n’est pas de laisser l’IA faire l’analyse.

L’objectif est d’apprendre à **auditer l’analyse de l’IA**.

# 156\. DÉFI ARCHITECTURAL

Prendre une fonctionnalité réelle :

recherche de produits.

Construire trois versions :

V1 : scan complet  
V2 : indexation  
V3 : cache + index

Mesurer :

- complexité ;
- latence ;
- mémoire ;
- comportement lorsque la base passe de (10^3) à (10^6) éléments.

# 157\. DÉFI IA AGENTIQUE

Construire un agent possédant :

\[ b \]

actions possibles et une profondeur :

\[ d \]

Comparer :

### Force brute

\[ O(b^d) \]

### Recherche avec pruning

complexité potentiellement fortement réduite en pratique.

### Recherche heuristique

réduction de l’espace exploré.

Objectif :

comprendre pourquoi un agent intelligent doit contrôler son espace de recherche.

# 158\. CHALLENGE « SORTIR DES SENTIERS BATTUS »

Créer un système capable d’analyser automatiquement une tâche utilisateur et de déterminer :

1\. taille estimée de l'entrée  
2\. complexité théorique  
3\. complexité mémoire  
4\. croissance prévue  
5\. point de rupture  
6\. stratégie d'optimisation  
7\. alternative approximative  
8\. possibilité de parallélisation

Ce système pourrait devenir un :

**Complexity Advisor**

pour les développeurs.

# 159\. APPLICATION CRÉATIVE — COMPLEXITY BUDGET

Pour chaque fonctionnalité d’un produit, définir un budget :

CPU  
RAM  
latence  
I/O  
réseau  
coût cloud

Chaque nouvelle fonctionnalité doit respecter son budget.

Cela transforme la théorie de la complexité en outil d’architecture produit.

# 160\. APPLICATION CRÉATIVE — COMPLEXITY-AWARE AI

Un agent pourrait choisir automatiquement entre :

exact  
↓  
approximation  
↓  
heuristique  
↓  
échantillonnage  
↓  
abandon contrôlé

selon :

- taille de l’espace ;
- temps disponible ;
- qualité requise ;
- budget computationnel.

Cela permettrait de concevoir des agents qui ne cherchent pas naïvement la perfection.

# 161\. APPLICATION CRÉATIVE — SCALABILITY RADAR

Créer un outil qui prend une fonctionnalité et estime :

n = 10²  
n = 10³  
n = 10⁴  
n = 10⁵  
n = 10⁶  
n = 10⁷

puis affiche :

- temps estimé ;
- mémoire ;
- point de rupture ;
- coût cloud potentiel.

L’objectif :

détecter les problèmes d’architecture avant qu’ils deviennent des problèmes de production.

# 162\. APPLICATION CRÉATIVE — COMPLEXITY LINTER

Créer un linter capable de détecter :

boucles imbriquées  
requêtes N+1  
recalculs inutiles  
recherche linéaire répétée  
tri répété  
recherche exhaustive  
allocations inutiles

et de proposer :

complexité actuelle  
complexité potentielle  
alternative  
gain attendu

# 163\. APPLICATION CRÉATIVE — COMPLEXITY GRAPH

Représenter une application sous forme de graphe :

UI  
↓  
API  
↓  
Service  
↓  
Database  
↓  
External API

Chaque nœud possède :

\[ T_i(n) \]

et :

\[ S_i(n) \]

Le système calcule alors les chemins computationnels les plus coûteux.

Cela devient une forme de :

**cartographie dynamique de la complexité logicielle.**

# 164\. APPLICATION CRÉATIVE — COMPLEXITY-AWARE DATABASE

Une couche d’analyse pourrait observer les requêtes et détecter :

- scans complets ;
- mauvais joins ;
- index absents ;
- cardinalités dangereuses ;
- requêtes répétitives ;
- explosion combinatoire.

Elle pourrait ensuite recommander :

- index ;
- cache ;
- pagination ;
- pré-calcul ;
- matérialisation ;
- restructuration de requête.

# 165\. APPLICATION CRÉATIVE — COMPLEXITY-AWARE RAG

Pour un système RAG :

documents  
↓  
index  
↓  
retrieval  
↓  
reranking  
↓  
LLM

chaque étape possède un coût.

On peut donc optimiser :

\[ \]

La théorie de la complexité devient ainsi une composante de l’architecture d’un système IA.

# 166\. APPLICATION CRÉATIVE — COMPLEXITY-AWARE AGENTS

Un agent pourrait avoir un budget :

\[ B \]

et estimer le coût d’une action :

\[ C(a) \]

Il cherche alors :

\[ U(a) \]

sous :

\[ C(a)B \]

Cela relie :

- optimisation ;
- théorie de la complexité ;
- décision ;
- agents autonomes.

# 167\. CONNEXIONS AVEC LES AUTRES DOMAINES

## A — Logique

La complexité dépend fortement de :

- logique ;
- décidabilité ;
- satisfaisabilité ;
- raisonnement.

## B — Théorie des nombres

Applications :

- cryptographie ;
- primalité ;
- factorisation ;
- arithmétique algorithmique.

## C — Algèbre linéaire

La complexité intervient dans :

- multiplication matricielle ;
- systèmes linéaires ;
- calcul scientifique ;

## E — Graphes

Nombreux problèmes de graphes possèdent des complexités très différentes :

- BFS ;
- DFS ;
- shortest path ;
- matching ;
- clique ;
- coloring ;
- Hamiltonian path.

## F — Combinatoire

La combinatoire explique une grande partie des explosions :

\[ 2^n,n!,nk \]

## J — Optimisation

Une partie majeure des problèmes d’optimisation sont computationnellement difficiles.

## L — Analyse numérique

La complexité permet de comparer les coûts des méthodes numériques.

## M/N — Information et transformées

Compression, codage, recherche, traitement du signal et calcul peuvent tous être soumis à des contraintes de complexité.

# 168\. DISTINCTION ENTRE LES TROIS GRANDES QUESTIONS

Toute analyse algorithmique sérieuse devrait savoir répondre à ces trois questions :

### Question 1 — Calculabilité

\[ \]

### Question 2 — Complexité

\[ \]

### Question 3 — Ingénierie

\[ \]

# 169\. MODÈLE MENTAL FINAL

Retenir cette chaîne :

PROBLÈME  
↓  
FORMALISATION  
↓  
TAILLE DE L'ENTRÉE  
↓  
ALGORITHME  
↓  
RESSOURCES  
├── temps  
├── espace  
├── mémoire  
├── I/O  
└── communication  
↓  
ANALYSE ASYMPTOTIQUE  
├── O  
├── Ω  
└── Θ  
↓  
CLASSIFICATION  
├── P  
├── NP  
├── NP-complet  
├── NP-difficile  
├── PSPACE  
└── EXP...  
↓  
RÉDUCTION  
↓  
DIFFICULTÉ INTRINSÈQUE  
↓  
STRATÉGIE  
├── exact  
├── DP  
├── pruning  
├── approximation  
├── heuristique  
├── paramétrisation  
└── parallélisation  
↓  
SCALABILITÉ

# 170\. LES 12 IDÉES À ABSOLUMENT RETENIR

### 1.

\[ O \]

est une borne supérieure asymptotique.

### 2.

\[ \]

est une borne inférieure.

### 3.

\[ \]

décrit l’ordre asymptotique exact.

### 4.

La complexité dépend de la taille de l’entrée.

### 5.

Temps et espace sont deux ressources différentes.

### 6.

P signifie temps polynomial dans le modèle classique.

### 7.

NP ne signifie pas « non polynomial ».

### 8.

NP-complet signifie :

\[ NP + NP \]

### 9.

NP-difficile ne signifie pas impossible.

### 10.

Les réductions permettent de transférer la difficulté entre problèmes.

### 11.

Calculabilité et complexité sont différentes.

### 12.

Un problème peut être calculable mais pratiquement irréalisable.

# 171\. CHECKLIST DE MAÎTRISE

Je maîtrise réellement ce domaine si je peux :

- définir précisément (O) ;
- définir précisément () ;
- définir précisément () ;
- distinguer (O) et () ;
- expliquer (o) et () ;
- analyser une boucle ;
- analyser plusieurs boucles ;
- analyser une récursion ;
- résoudre des récurrences simples ;
- utiliser le Master Theorem ;
- analyser la mémoire ;
- distinguer meilleur/moyen/pire cas ;
- expliquer la complexité amortie ;
- reconnaître une explosion combinatoire ;
- expliquer P ;
- expliquer NP ;
- expliquer pourquoi (PNP) ;
- expliquer P vs NP ;
- définir NP-complet ;
- définir NP-difficile ;
- construire une réduction simple ;
- éviter l’inversion d’une réduction ;
- distinguer problème décisionnel et optimisation ;
- expliquer la calculabilité ;
- expliquer la décidabilité ;
- expliquer le problème de l’arrêt ;
- distinguer difficile et impossible ;
- expliquer PSPACE et EXP à haut niveau ;
- comprendre l’approximation ;
- comprendre les heuristiques ;
- comprendre la complexité paramétrée ;
- relier complexité et architecture logicielle ;
- relier complexité et IA ;
- évaluer la scalabilité d’un système.

# 172\. TEST ULTIME DE COMPRÉHENSION

Face à un nouveau problème, je dois pouvoir me poser immédiatement :

**1\. Quelle est la taille de mon entrée ?**

**2\. Quel est le type de problème : décision, recherche, optimisation ou comptage ?**

**3\. Quelle est la meilleure méthode connue ?**

**4\. Combien coûte cette méthode ?**

**5\. Quel est son (O), son () et éventuellement son () ?**

**6\. Quel est le coût mémoire ?**

**7\. Que se passe-t-il si (n) est multiplié par 10 ?**

**8\. Le problème possède-t-il une explosion combinatoire ?**

**9\. Est-il polynomial, NP, NP-complet ou NP-difficile ?**

**10\. Puis-je réduire le problème à une forme connue ?**

**11\. Existe-t-il une approximation ?**

**12\. Existe-t-il une heuristique ?**

**13\. Existe-t-il un paramètre petit permettant une solution FPT ?**

**14\. Puis-je exploiter une structure particulière des données ?**

**15\. Le problème est-il seulement difficile, ou est-il réellement non calculable ?**

# 173\. SYNTHÈSE FINALE

La théorie de la complexité fournit une manière rigoureuse de comprendre les limites computationnelles.

Elle apprend à distinguer :

\[ \]

de :

\[ \]

et :

\[ \]

Un programme peut exister sans être utilisable.

Un problème peut être calculable sans être efficacement calculable.

Un problème peut être difficile sans être impossible.

Et certains problèmes vont encore plus loin : ils sont **indécidables**, ce qui signifie qu’aucun algorithme général ne peut les résoudre correctement dans tous les cas.

La théorie de la complexité fournit alors plusieurs niveaux de lecture :

CALCULABILITÉ  
« Est-ce possible en principe ? »  
↓  
DÉCIDABILITÉ  
« Peut-on toujours terminer avec une réponse ? »  
↓  
COMPLEXITÉ  
« Combien de ressources faut-il ? »  
↓  
CLASSES  
« Quelle famille de difficulté ? »  
↓  
RÉDUCTIONS  
« À quels autres problèmes cette difficulté est-elle liée ? »  
↓  
ALGORITHMIQUE  
« Comment exploiter cette connaissance ? »  
↓  
INGÉNIERIE  
« Comment construire un système qui reste viable ? »

C’est pourquoi la théorie de la complexité n’est pas simplement une théorie de notation mathématique.

Elle constitue une **théorie de la faisabilité computationnelle**.

Son enseignement le plus important pour l’ingénieur logiciel est peut-être celui-ci :

**Ne demande pas seulement si ton programme fonctionne. Demande comment son coût évolue lorsque le monde réel grandit.**

Et son enseignement le plus profond est encore plus important :

**Il existe une différence fondamentale entre ce qu’une machine peut calculer, ce qu’elle peut calculer efficacement, et ce qu’aucune machine algorithmique générale ne peut calculer.**