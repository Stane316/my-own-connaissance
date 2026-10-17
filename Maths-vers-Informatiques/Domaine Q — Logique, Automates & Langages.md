# DOMAINE Q — LOGIQUE, AUTOMATES & LANGAGES

## Comprendre comment décrire, reconnaître, analyser et exécuter des langages

**Question centrale :**

**Comment donner une définition mathématique précise à un langage, déterminer si une chaîne appartient à ce langage, et construire une machine capable de reconnaître ou de traiter systématiquement ses structures ?**

Ce domaine constitue l’un des ponts les plus directs entre :

- mathématiques discrètes ;
- logique ;
- théorie des langages ;
- algorithmique ;
- compilation ;
- interprétation ;
- analyse syntaxique ;
- protocoles ;
- validation ;
- intelligence artificielle symbolique.

Il permet notamment de comprendre pourquoi des outils aussi différents que :

- les expressions régulières ;
- les parsers ;
- les compilateurs ;
- les interpréteurs ;
- les grammaires ;
- les protocoles réseau ;
- les analyseurs de fichiers ;
- les validateurs ;
- les moteurs de recherche de motifs ;

peuvent être étudiés avec un même langage mathématique.

# 0\. PRÉDISPOSITION D’INTÉGRATION

Ce document doit être utilisé comme une **base de raisonnement formel sur les langages, les structures syntaxiques et les machines abstraites**.

Lorsqu’un projet contient :

- un langage ;
- une syntaxe ;
- un format ;
- un protocole ;
- une configuration ;
- des expressions ;
- des requêtes ;
- des commandes ;
- un fichier structuré ;
- un parser ;
- un compilateur ;
- un interpréteur ;
- une validation complexe ;
- des expressions régulières ;
- une machine à états ;
- une analyse syntaxique ;
- un moteur de règles ;

l’IA doit identifier :

1.  **Quel est l’alphabet ?**
2.  **Quelles chaînes sont valides ?**
3.  **Quel langage ces chaînes constituent-elles ?**
4.  **Le langage est-il régulier ?**
5.  **Une expression régulière suffit-elle ?**
6.  **Faut-il une grammaire ?**
7.  **Faut-il une mémoire pendant la reconnaissance ?**
8.  **Quel type d’automate correspond au problème ?**
9.  **La grammaire est-elle ambiguë ?**
10. **Quel algorithme d’analyse syntaxique utiliser ?**
11. **Quelle représentation intermédiaire construire ?**
12. **Le problème est-il décidable ?**
13. **Quelle complexité possède l’analyse ?**
14. **Comment gérer les erreurs ?**
15. **Comment faire évoluer le langage ?**

Le document doit empêcher une confusion fondamentale :

**Une regex, une grammaire, un parser et un compilateur ne sont pas quatre versions du même outil.**

Ils correspondent à des niveaux différents d’expression et de traitement des langages.

# 1\. IDENTITÉ DU DOMAINE

## Nom

**Logique, Automates & Langages**

## Domaine

Mathématiques discrètes + informatique théorique + génie logiciel.

## Nature

Ce domaine étudie :

- les langages formels ;
- leur structure ;
- leur génération ;
- leur reconnaissance ;
- les machines abstraites capables de les traiter ;
- les limites de ces machines.

Il forme une progression fondamentale :

text id="q0stack" ALPHABET ↓ CHAÎNES ↓ LANGAGES ↓ GRAMMAIRES ↓ AUTOMATES ↓ RECONNAISSANCE ↓ ANALYSE ↓ TRANSFORMATION ↓ EXÉCUTION

# 2\. LA GRANDE QUESTION DU DOMAINE

Supposons qu’un utilisateur fournisse :

if (x > 10) {  
print(x);  
}

Comment une machine sait-elle :

- quels caractères sont valides ?
- où commence un token ?
- ce qu’est if ?
- ce qu’est x ?
- ce qu’est > ?
- où commence le bloc ?
- quelle expression est contenue dans le bloc ?
- quelle structure possède l’ensemble ?
- quelle signification lui attribuer ?

On peut décomposer :

text id="qdecomp" texte brut ↓ caractères ↓ tokens ↓ syntaxe ↓ AST ↓ sémantique ↓ représentation intermédiaire ↓ exécution / compilation

Les automates et langages constituent une partie essentielle de cette chaîne.

# 3\. PLACE DANS LA PILE MATHÉMATIQUE ET INFORMATIQUE

text id="qstack" LOGIQUE ↓ ENSEMBLES ↓ LANGAGES FORMELS ↓ GRAMMAIRES ↓ AUTOMATES ↓ ALGORITHMES DE RECONNAISSANCE ↓ PARSERS ↓ COMPILATEURS / INTERPRÉTEURS ↓ LANGAGES DE PROGRAMMATION

Connexions fortes avec :

- A — Logique et fondements ;
- E — Théorie des graphes ;
- F — Combinatoire ;
- O — Théorie de la complexité ;
- théorie de la calculabilité ;
- algorithmique ;
- génie logiciel.

# 4\. ALPHABET

Un alphabet est un ensemble fini de symboles.

On le note généralement :

\[ \]

Exemple :

\[ ={0,1} \]

ou :

\[ ={a,b,c} \]

ou encore un alphabet de caractères :

Σ = {A, B, ..., Z, a, b, ..., z, 0, ..., 9, ...}

L’alphabet constitue la matière première des langages formels.

# 5\. CHAÎNE

Une chaîne est une séquence finie de symboles appartenant à un alphabet.

Exemple :

\[ 101001 \]

est une chaîne sur :

\[ ={0,1} \]

# 6\. MOT VIDE

Le mot vide est noté :

\[ \]

Il possède une longueur :

\[ ||=0 \]

Il est fondamental dans :

- les automates ;
- les grammaires ;
- les expressions régulières ;
- les langages.

# 7\. LONGUEUR D’UNE CHAÎNE

Pour :

\[ w=abcab \]

on a :

\[ |w|=5 \]

La longueur mesure le nombre de symboles.

# 8\. (^\*)

L’ensemble :

\[ ^\* \]

contient toutes les chaînes finies construites à partir de (), y compris :

\[ \]

Exemple :

\[ ={0,1} \]

alors :

\[ ^\*= {,0,1,00,01,10,11,000,} \]

# 9\. (^+)

On définit :

\[ <sup>+=</sup>\*-{} \]

C’est l’ensemble des chaînes non vides.

# 10\. LANGAGE FORMEL

Un langage formel est simplement un ensemble de chaînes sur un alphabet.

\[ L^\* \]

Exemple :

\[ L={w{0,1}^\* w1} \]

Un langage peut donc être vu comme :

**un ensemble de chaînes considérées comme valides selon une règle précise.**

# 11\. LANGAGE ≠ LANGAGE DE PROGRAMMATION

Un langage formel est un concept mathématique général.

Un langage de programmation est un système plus riche comprenant généralement :

- syntaxe ;
- grammaire ;
- sémantique ;
- règles de typage ;
- règles d’exécution ;
- bibliothèque ;
- environnement.

Ainsi :

text id="qlang" Langage formel ↓ syntaxe ↓ langage de programmation ↓ sémantique + exécution

# 12\. PROBLÈME DE RECONNAISSANCE

Étant donné :

\[ w \]

et un langage :

\[ L \]

le problème consiste à déterminer :

\[ wL;? \]

Réponse :

ACCEPT

ou :

REJECT

C’est l’une des questions fondamentales de la théorie des automates.

# 13\. LANGAGE DÉCIS

Une machine reconnaît un langage si elle peut déterminer l’appartenance des chaînes.

La question fondamentale devient :

la machine termine-t-elle toujours ?

Cette distinction mènera plus tard aux notions de :

- reconnaissance ;
- décision ;
- semi-décidabilité ;
- décidabilité ;
- calculabilité.

# 14\. LANGAGES PAR CLASSES

Une classification fondamentale est la hiérarchie de Chomsky :

text id="qchomsky" TYPE 3 Réguliers ↓ TYPE 2 Hors contexte ↓ TYPE 1 Sensibles au contexte ↓ TYPE 0 Récursivement énumérables

Correspondance approximative :

\`\`\`text id=“qmachines” Langages réguliers ↓ Automates finis

Langages hors contexte ↓ Automates à pile

Langages sensibles au contexte ↓ Automates linéairement bornés

Langages de type 0 ↓ Machines de Turing

  
<br/>Cette hiérarchie est l’un des grands cadres conceptuels du domaine.  
<br/>\---  
<br/>\# 15. LANGAGES RÉGULIERS  
<br/>Les langages réguliers constituent une classe fondamentale.  
<br/>Ils peuvent être décrits par :  
<br/>\- expressions régulières ;  
\- automates finis déterministes ;  
\- automates finis non déterministes.  
<br/>C’est une équivalence majeure :  
<br/>\\\[  
REGEX \\equiv DFA \\equiv NFA  
\\\]  
<br/>au sens de la classe de langages reconnue.  
<br/>\---  
<br/>\# 16. AUTOMATE FINI  
<br/>Un automate fini est une machine possédant un nombre fini d’états.  
<br/>Formellement, un DFA peut être représenté par :  
<br/>\\\[  
A=(Q,\\Sigma,\\delta,q_0,F)  
\\\]  
<br/>où :  
<br/>\- \\(Q\\) = ensemble fini des états ;  
\- \\(\\Sigma\\) = alphabet ;  
\- \\(\\delta\\) = fonction de transition ;  
\- \\(q_0\\) = état initial ;  
\- \\(F\\) = ensemble des états acceptants.  
<br/>\---  
<br/>\# 17. ÉTAT  
<br/>Un état représente une situation interne de la machine.  
<br/>Exemple :  
<br/>\`\`\`text id="qstate"  
q0 = début  
q1 = vu un 1  
q2 = nombre pair de 1  
...

L’automate ne mémorise pas nécessairement toute l’histoire.

Il mémorise seulement l’information nécessaire à la décision.

# 18\. TRANSITION

Une transition indique :

étant dans cet état et lisant ce symbole, vers quel état aller ?

Formellement :

\[ (q,a)=q’ \]

# 19\. ÉTAT INITIAL

\[ q_0 \]

représente le point de départ.

# 20\. ÉTATS ACCEPTANTS

\[ FQ \]

Une chaîne est acceptée si, après lecture complète, l’automate se trouve dans un état de (F).

# 21\. AUTOMATE DÉTERMINISTE

Dans un DFA :

\[ :QQ \]

Pour chaque :

- état ;
- symbole ;

il existe exactement une transition.

Donc :

text id="qdeter" état + symbole ↓ un seul état suivant

# 22\. AUTOMATE NON DÉTERMINISTE

Dans un NFA, plusieurs transitions peuvent être possibles.

On peut écrire :

\[ :Q^Q \]

Une transition peut donc produire un ensemble d’états possibles.

Conceptuellement :

text id="qnondeter" ┌→ q1 q0 + a ──┤ └→ q2

# 23\. NON-DÉTERMINISME

Le terme ne signifie pas :

machine aléatoire.

Le NFA est une machine mathématique où plusieurs chemins peuvent exister.

Une chaîne est acceptée si **au moins un chemin** mène à un état acceptant.

# 24\. ÉQUIVALENCE DFA / NFA

Un résultat fondamental :

tout NFA peut être converti en DFA reconnaissant le même langage.

Mais la conversion peut augmenter fortement le nombre d’états.

Si un NFA possède :

\[ n \]

états, la construction des sous-ensembles peut produire jusqu’à :

\[ 2^n \]

états.

# 25\. CONSTRUCTION PAR SOUS-ENSEMBLES

Principe :

text id="qsubset" NFA ↓ ensembles d'états ↓ DFA

Chaque état du DFA représente un ensemble d’états du NFA.

# 26\. EPSILON-TRANSITIONS

Un NFA peut autoriser des transitions consommant :

\[ \]

c’est-à-dire aucun symbole.

On parle alors souvent de :

\[ \]

Ces transitions facilitent la construction d’automates à partir d’expressions régulières.

# 27\. FERMETURE-()

Pour un état (q), la fermeture-() correspond aux états accessibles depuis (q) uniquement par des transitions ().

Elle est fondamentale lors de la conversion d’un ()-NFA en DFA.

# 28\. DIAGRAMME D’AUTOMATE

Exemple conceptuel :

text id="qdiagram" 1 ┌──────────┐ │ ↓ (q0) ──0──> (q1)\* ↑ │ └────1──────┘

Convention :

- cercle = état ;
- double cercle = état acceptant ;
- flèche = transition ;
- flèche entrante sans origine = état initial.

# 29\. LANGAGE RECONNU PAR UN AUTOMATE

On note :

\[ L(A) \]

le langage accepté par l’automate (A).

Deux automates peuvent avoir :

- des structures différentes ;
- des nombres d’états différents ;

mais reconnaître exactement le même langage.

# 30\. MINIMISATION D’AUTOMATES

Un DFA peut souvent être réduit.

Objectif :

obtenir un automate équivalent avec le moins d’états possible.

Une idée fondamentale :

deux états peuvent être fusionnés s’ils sont indiscernables du point de vue du langage reconnu.

# 31\. ALGORITHME DE MINIMISATION

On peut notamment utiliser des méthodes fondées sur :

- partitionnement ;
- raffinement de partitions ;
- distinction d’états.

L’objectif est d’obtenir le DFA minimal.

# 32\. THÉORÈME DE MYHILL-NERODE

Concept fondamental.

Deux chaînes peuvent être considérées équivalentes si aucune continuation ne permet de les distinguer du point de vue de l’appartenance au langage.

Cette relation permet notamment de caractériser les langages réguliers et le nombre minimal d’états d’un DFA.

# 33\. EXPRESSIONS RÉGULIÈRES

Une expression régulière permet de décrire certains langages réguliers.

Opérations fondamentales :

- union ;
- concaténation ;
- étoile de Kleene.

# 34\. UNION

Si :

\[ R \]

et :

\[ S \]

sont des expressions régulières :

\[ R|S \]

représente le choix entre les deux.

# 35\. CONCATÉNATION

Si :

\[ R \]

et :

\[ S \]

sont des expressions régulières :

\[ RS \]

représente une chaîne appartenant d’abord à (R), puis à (S).

# 36\. ÉTOILE DE KLEENE

\[ R^\* \]

signifie :

zéro ou plusieurs répétitions de (R).

Exemple :

\[ a^\* \]

représente :

\[ {,a,aa,aaa,} \]

# 37\. PLUS DE KLEENE

Souvent noté :

\[ R^+ \]

et représentant une ou plusieurs occurrences.

\[ R<sup>+=RR</sup>\* \]

# 38\. LANGAGES RÉGULIERS ET REGEX

Une expression régulière classique peut décrire :

- formats ;
- motifs ;
- tokens ;
- identifiants ;
- nombres ;
- séparateurs ;
- structures lexicales simples.

Exemple :

^\[A-Za-z_\]\[A-Za-z0-9_\]\*$

peut décrire une classe d’identifiants.

# 39\. REGEX DE PROGRAMMATION VS REGEX THÉORIQUE

Important :

Les moteurs regex modernes peuvent proposer des fonctionnalités qui dépassent le modèle strict des langages réguliers.

Exemples selon les moteurs :

- backreferences ;
- lookaround ;
- constructions conditionnelles ;
- récursion.

Il ne faut donc pas confondre :

**expression régulière au sens théorique**

et :

**syntaxe regex d’un moteur logiciel particulier**.

# 40\. TOKENISATION

La tokenisation transforme une séquence de caractères en unités lexicales.

Exemple :

x = 12 + 4

devient :

IDENT(x)  
ASSIGN  
NUMBER(12)  
PLUS  
NUMBER(4)

Cette étape est généralement appelée :

**analyse lexicale**.

# 41\. ANALYSEUR LEXICAL

Le lexer reconnaît des catégories comme :

- identifiant ;
- mot-clé ;
- nombre ;
- chaîne ;
- opérateur ;
- commentaire ;
- ponctuation.

Les automates finis sont particulièrement adaptés à cette tâche.

# 42\. LEXER

Pipeline :

text id="qlexer" source code ↓ lexer ↓ tokens

Le lexer peut être construit à partir :

regex  
↓  
NFA  
↓  
DFA  
↓  
scanner

C’est l’un des exemples les plus importants de passage de la théorie à l’ingénierie.

# 43\. GRAMMAIRE FORMELLE

Une grammaire peut être représentée par :

\[ G=(V,,P,S) \]

où :

- (V) = symboles non terminaux ;
- () = terminaux ;
- (P) = productions ;
- (S) = symbole initial.

# 44\. TERMINAUX

Les terminaux représentent les symboles effectivement présents dans les chaînes produites.

Dans un langage de programmation :

if  
+  
(  
)  
identifier  
number

peuvent être des terminaux conceptuels.

# 45\. NON-TERMINAUX

Les non-terminaux représentent des structures abstraites.

Exemple :

Expression  
Statement  
Program  
Block  
Function

# 46\. RÈGLES DE PRODUCTION

Exemple :

\[ ExpressionExpression+Term \]

ou :

\[ ExpressionTerm \]

Les productions définissent comment construire des phrases du langage.

# 47\. DÉRIVATION

À partir du symbole initial :

\[ S \]

on applique des productions.

Exemple :

text id="qderive" Expression ↓ Expression + Term ↓ Term + Term ↓ Number + Number

On obtient finalement une chaîne de terminaux.

# 48\. FORME SENTENTIELLE

Une forme sentientielle peut contenir :

- terminaux ;
- non-terminaux.

Elle représente un état intermédiaire de dérivation.

# 49\. ARBRE DE DÉRIVATION

Une dérivation peut être représentée par un arbre.

Exemple conceptuel :

text id="qparse" Expr / | \\ Expr + Term | | Number Number

L’arbre montre la structure syntaxique.

# 50\. PARSE TREE VS AST

Le parse tree représente davantage la structure grammaticale complète.

L’AST — Abstract Syntax Tree — supprime souvent les détails syntaxiques inutiles.

Exemple :

1 + 2 \* 3

AST :

text id="qast" + / \\ 1 \* / \\ 2 3

L’AST est généralement beaucoup plus utile pour les étapes ultérieures du compilateur.

# 51\. AMBIGUÏTÉ

Une grammaire est ambiguë si une même chaîne possède plusieurs arbres de dérivation distincts.

Exemple classique :

\[ 1+2\*3 \]

sans règles de priorité explicites.

Le système doit savoir :

\[ 1+(2\*3) \]

ou :

\[ (1+2)\*3 \]

# 52\. ASSOCIATIVITÉ

Les opérateurs peuvent être :

- associatifs à gauche ;
- associatifs à droite.

Exemple :

\[ a-b-c \]

peut signifier :

\[ (a-b)-c \]

# 53\. PRÉCÉDENCE

La précédence détermine quels opérateurs sont appliqués en premier.

Exemple :

\[ a+b\*c \]

est généralement :

\[ a+(b\*c) \]

# 54\. GRAMMAIRES HORS CONTEXTE

Une grammaire hors contexte possède des productions de forme :

\[ A \]

où (A) est un seul non-terminal.

Les langages engendrés sont appelés :

**context-free languages**.

# 55\. AUTOMATES À PILE

Les langages hors contexte sont liés aux automates à pile.

Un PDA possède :

- états ;
- entrée ;
- pile.

La pile apporte une mémoire structurée.

# 56\. POURQUOI UNE PILE ?

Considérons :

\[ a^n b^n \]

Il faut vérifier que le nombre de (a) correspond au nombre de (b).

Un automate fini possède une mémoire finie.

Une pile permet :

text id="qstack2" a → push a → push a → push ... b → pop b → pop b → pop

et vérifier que tout correspond.

# 57\. DFA VS PDA

| Machine | Mémoire | Langages |
| --- | --- | --- |
| DFA | finie | réguliers |
| NFA | finie | réguliers |
| PDA | pile | hors contexte |
| Turing | mémoire générale | classe beaucoup plus large |

# 58\. LANGAGES NON RÉGULIERS

Exemple :

\[ L={a^n b^nn} \]

n’est pas régulier.

Intuition :

un automate fini ne possède pas assez de mémoire pour compter arbitrairement les (a) et comparer avec les (b).

Mais un PDA peut le reconnaître.

# 59\. POMPAGE DES LANGAGES RÉGULIERS

Le pumping lemma peut être utilisé pour démontrer qu’un langage n’est pas régulier.

Idée :

Une chaîne suffisamment longue dans un langage régulier doit contenir une partie répétable.

Cela impose une structure de pompage.

# 60\. POMPAGE DES LANGAGES HORS CONTEXTE

Il existe également une version du pumping lemma pour les langages hors contexte.

Elle permet de montrer que certains langages ne sont pas hors contexte.

# 61\. CLOSURE PROPERTIES

Les langages réguliers sont fermés sous plusieurs opérations :

- union ;
- intersection ;
- complément ;
- concaténation ;
- étoile ;
- différence.

Ces propriétés sont extrêmement utiles pour raisonner sur les langages.

# 62\. LANGAGES HORS CONTEXTE : PROPRIÉTÉS

Ils sont notamment fermés sous :

- union ;
- concaténation ;
- étoile.

Mais certaines opérations, notamment l’intersection générale et le complément, ne préservent pas cette classe de la même manière.

# 63\. ANALYSE SYNTAXIQUE

Le parser reçoit :

tokens

et produit généralement :

AST

Pipeline :

text id="qparser" source ↓ lexer ↓ tokens ↓ parser ↓ AST

# 64\. TOP-DOWN PARSING

Le parser part du symbole initial et tente de construire la structure vers les tokens.

Exemples :

- recursive descent ;
- LL ;
- LL(k).

# 65\. RECURSIVE DESCENT

Chaque règle grammaticale peut correspondre à une fonction.

Exemple conceptuel :

parseExpression()  
parseTerm()  
parseFactor()

Une grammaire adaptée peut être directement transformée en code.

# 66\. PROBLÈME DE RÉCURSION GAUCHE

Une grammaire comme :

\[ EE+T \]

peut provoquer une récursion infinie dans un parser recursive descent naïf.

Il faut souvent transformer la grammaire.

# 67\. ÉLIMINATION DE LA RÉCURSION GAUCHE

On peut transformer :

\[ AA| \]

en une forme équivalente du type :

\[ AA’ \]

et :

\[ A’A’| \]

Cette transformation est fondamentale pour certains parsers top-down.

# 68\. LEFT FACTORING

Lorsque plusieurs productions commencent par la même séquence, on peut factoriser.

Exemple :

\[ A_1|\_2 \]

devient :

\[ AA’ \]

puis :

\[ A’\_1|\_2 \]

# 69\. BOTTOM-UP PARSING

Le parser commence généralement avec les tokens et reconstruit progressivement la structure vers le symbole initial.

Exemples :

- LR ;
- SLR ;
- LALR ;
- LR(1).

Ces familles sont fondamentales dans les outils de compilation.

# 70\. SHIFT-REDUCE

Un parser bottom-up utilise souvent des opérations :

text id="qshift" SHIFT REDUCE ACCEPT ERROR

### SHIFT

Ajouter un token à la pile.

### REDUCE

Remplacer une séquence reconnue par un non-terminal.

# 71\. LL VS LR

| Propriété | LL  | LR  |
| --- | --- | --- |
| Direction | top-down | bottom-up |
| Construction | symbole initial → entrée | entrée → symbole initial |
| Complexité conceptuelle | souvent plus simple | souvent plus puissante |
| Usage | recursive descent / parsers simples | compilateurs / grammaires riches |

# 72\. FIRST

Pour une grammaire, (FIRST()) indique les terminaux qui peuvent apparaître au début d’une dérivation de ().

Utilisé notamment dans :

- LL(1) ;
- construction de tables de parsing.

# 73\. FOLLOW

\[ FOLLOW(A) \]

représente les terminaux pouvant apparaître immédiatement après (A) dans certaines dérivations.

Également fondamental pour les parsers LL.

# 74\. LL(1)

Un parser LL(1) prend ses décisions à partir d’un seul symbole d’anticipation.

Une grammaire doit satisfaire certaines propriétés pour permettre une analyse déterministe LL(1).

# 75\. TABLE DE PARSING

Conceptuellement :

text id="qtable" token a b c Expr ... Term ... Factor ...

Le parser utilise :

- état ;
- symbole courant ;
- table ;

pour déterminer l’action.

# 76\. LR

LR signifie traditionnellement une lecture de gauche à droite avec construction d’une dérivation droite inversée.

Les parseurs LR sont particulièrement importants pour les compilateurs.

# 77\. LALR

**Look-Ahead LR**

LALR cherche à réduire la taille des tables par rapport à LR(1) tout en conservant une puissance importante.

Cette famille a historiquement été très utilisée dans les générateurs de parsers.

# 78\. PARSERS PRATIQUES

Dans les projets modernes, on peut utiliser :

- parser écrit manuellement ;
- générateur de parser ;
- parser combinators ;
- PEG ;
- bibliothèques spécialisées.

Le choix dépend :

- complexité de la grammaire ;
- performance ;
- maintenabilité ;
- messages d’erreur ;
- besoin de récupération.

# 79\. PEG

**Parsing Expression Grammar**

Les PEG décrivent la reconnaissance par une logique de choix ordonné.

Contrairement à certaines grammaires CFG classiques, l’ordre des alternatives peut être significatif.

Les PEG sont utilisées dans certains langages et outils modernes.

# 80\. PARSER COMBINATORS

Un parser peut être construit à partir de petits parseurs combinés.

Concept :

text id="qcombine" Parser&lt;A&gt; + Parser&lt;B&gt; ↓ Parser&lt;C&gt;

Cette approche est fréquente dans certains écosystèmes fonctionnels.

# 81\. ERROR RECOVERY

Un bon parser ne doit pas seulement dire :

ERROR

Il doit idéalement pouvoir indiquer :

- position ;
- token attendu ;
- token trouvé ;
- contexte ;
- suggestion ;
- récupération possible.

Exemple :

Erreur ligne 8, colonne 12 :  
')' attendu après l'expression.  
Token trouvé : '{'

# 82\. AST

L’AST représente la structure abstraite du programme.

Exemple :

text id="qast2" Assignment / \\ x Add / \\ 2 3

L’AST constitue une représentation centrale dans les compilateurs et interpréteurs.

# 83\. AST ≠ PARSE TREE

Le parse tree représente la dérivation grammaticale.

L’AST représente généralement la structure sémantiquement utile.

# 84\. ANALYSE SÉMANTIQUE

Une fois l’AST obtenu, il faut vérifier :

- variables déclarées ;
- types ;
- portée ;
- appels ;
- signatures ;
- règles du langage.

Pipeline :

text id="qsemantic" AST ↓ semantic analysis ↓ validated AST

# 85\. TABLE DES SYMBOLES

Le compilateur maintient souvent une structure :

text id="qsymbol" SymbolTable ├── variable ├── function ├── type ├── scope └── metadata

Elle permet notamment de résoudre les noms.

# 86\. PORTÉE

Une variable peut être accessible seulement dans une région du programme.

On distingue notamment :

- portée globale ;
- portée locale ;
- portée lexicale ;
- portée dynamique selon les langages.

# 87\. TYPAGE

L’analyse syntaxique ne suffit pas.

Exemple :

3 + "hello"

La syntaxe peut être correcte.

Mais la sémantique peut être invalide.

Il faut donc distinguer :

syntactically valid

de :

semantically valid

# 88\. COMPILATEUR

Un compilateur transforme généralement :

source program  
↓  
tokens  
↓  
AST  
↓  
semantic analysis  
↓  
IR  
↓  
optimization  
↓  
target code

# 89\. FRONT-END / MIDDLE-END / BACK-END

Architecture classique :

text id="qcompiler" SOURCE ↓ FRONT-END ├── lexer ├── parser └── semantic analysis ↓ IR ↓ MIDDLE-END └── optimization ↓ BACK-END ├── code generation └── target-specific optimization ↓ MACHINE CODE

# 90\. REPRÉSENTATION INTERMÉDIAIRE

Une IR permet de séparer :

text id="qir" source language ↓ IR ↓ target architecture

Exemples conceptuels :

- trois-adresses ;
- SSA ;
- bytecode ;
- IR spécifique à un compilateur.

# 91\. SSA

**Static Single Assignment**

Chaque variable logique est assignée une seule fois.

Exemple :

text id="qssa" x = 1 x = x + 2

peut devenir conceptuellement :

x1 = 1  
x2 = x1 + 2

SSA facilite plusieurs optimisations.

# 92\. INTERPRÉTEUR

Un interpréteur exécute directement une représentation du programme.

Conceptuellement :

text id="qinterp" source ↓ parse ↓ AST / bytecode ↓ interpreter ↓ execution

# 93\. BYTECODE

Un langage peut être compilé vers une représentation intermédiaire portable.

Exemple conceptuel :

text id="qbyte" source ↓ compiler ↓ bytecode ↓ VM ↓ machine

# 94\. MACHINE VIRTUELLE

Une VM définit :

- instructions ;
- pile ;
- registres conceptuels ;
- mémoire ;
- appels ;
- exceptions.

Elle constitue une machine abstraite exécutable.

# 95\. AUTOMATE À PILE ET VM

Connexion intéressante :

text id="qpushvm" PDA ↓ pile

et :

VM  
↓  
stack / call stack

La pile est une structure fondamentale dans l’exécution de langages.

# 96\. MACHINE DE TURING

La machine de Turing constitue un modèle abstrait extrêmement puissant du calcul.

Elle possède notamment :

- un ruban ;
- une tête de lecture/écriture ;
- un ensemble d’états ;
- une fonction de transition.

# 97\. RUBAN

Le ruban peut être vu comme une mémoire potentiellement non bornée.

Conceptuellement :

text id="qtape" ... | 0 | 1 | 1 | 0 | 1 | _ | _ | ... ↑ tête

# 98\. TRANSITION D’UNE MACHINE DE TURING

Une transition peut dépendre :

- état courant ;
- symbole lu.

Elle détermine :

- symbole à écrire ;
- mouvement de la tête ;
- nouvel état.

Conceptuellement :

\[ (q,a)=(q’,b,D) \]

où (D) peut représenter :

- gauche ;
- droite.

# 99\. MACHINE DE TURING ET CALCULABILITÉ

Les machines de Turing sont utilisées pour formaliser :

- algorithmes ;
- calculabilité ;
- décidabilité ;
- reconnaissance de langages.

Elles permettent de poser les limites fondamentales du calcul.

# 100\. LANGAGES ACCEPTÉS PAR TURING

Une machine de Turing peut reconnaître des classes de langages beaucoup plus larges que les automates finis.

Les langages associés aux machines de Turing sont liés à la classe des langages récursivement énumérables.

# 101\. DÉCIDEUR VS RECONNAISSEUR

Un décideur :

termine toujours.

Un reconnaisseur peut :

- accepter les chaînes du langage ;
- rejeter certaines chaînes ;

mais, selon le modèle, peut potentiellement ne jamais terminer sur une entrée hors langage.

Cette distinction est fondamentale.

# 102\. PROBLÈME DE L’ARRÊT

Question :

étant donnée une machine et une entrée, la machine va-t-elle terminer ?

Le problème général de l’arrêt est indécidable.

Cela constitue une limite fondamentale de l’informatique.

# 103\. AUTOMATES VS CALCULABILITÉ

On peut voir une progression :

\`\`\`text id=“qpower” Automate fini ↓ mémoire finie

Automate à pile ↓ pile

Machine de Turing ↓ mémoire générale

  
<br/>Chaque ajout de mémoire augmente la puissance expressive.  
<br/>\---  
<br/>\# 104. MÉMOIRE COMME SOURCE DE PUISSANCE  
<br/>C’est une idée mentale fondamentale.  
<br/>\`\`\`text id="qmemory"  
pas de mémoire variable  
↓  
états finis  
↓  
langages réguliers  
<br/>pile  
↓  
langages hors contexte  
<br/>mémoire générale  
↓  
calcul général

# 105\. HIÉRARCHIE DE CHOMSKY

| Type | Langages | Machine associée |
| --- | --- | --- |
| Type 3 | réguliers | automate fini |
| Type 2 | hors contexte | automate à pile |
| Type 1 | sensibles au contexte | automate linéairement borné |
| Type 0 | récursivement énumérables | machine de Turing |

# 106\. LANGAGES SENSIBLES AU CONTEXTE

Ils sont plus expressifs que les langages hors contexte.

Ils sont associés aux **linear bounded automata**.

Ils sont moins fréquemment utilisés directement dans les compilateurs classiques, mais sont importants pour comprendre la hiérarchie théorique.

# 107\. AUTOMATES LINÉAIREMENT BORNÉS

Un automate linéairement borné possède une mémoire limitée par une fonction linéaire de la taille de l’entrée.

Il correspond à une classe importante dans la hiérarchie de Chomsky.

# 108\. DÉCISION ET RECONNAISSANCE

Lorsqu’on rencontre un langage, demander :

text id="qdecision" Peut-on reconnaître ? ↓ Peut-on toujours terminer ? ↓ Peut-on décider ?

Cette chaîne connecte directement Q au domaine O.

# 109\. COMPLEXITÉ DES AUTOMATES

Pour un DFA, la reconnaissance d’une chaîne de longueur (n) peut être réalisée en :

\[ O(n) \]

si chaque transition est disponible efficacement.

Pour certains parseurs, la complexité dépend de :

- grammaire ;
- algorithme ;
- ambiguïté ;
- stratégie de parsing.

# 110\. COMPLEXITÉ DU PARSING

Selon le contexte :

- certains parsers peuvent être linéaires ;
- certaines méthodes générales peuvent atteindre des coûts cubiques ;
- certaines grammaires ou techniques peuvent conduire à des comportements beaucoup plus coûteux.

La structure de la grammaire influence donc directement la performance.

# 111\. AMBIGUÏTÉ ET PERFORMANCE

Une grammaire ambiguë peut produire plusieurs analyses possibles.

Un parser peut alors devoir :

- explorer plusieurs possibilités ;
- mémoriser des états ;
- effectuer du backtracking.

La conception de la grammaire devient donc aussi un problème d’optimisation.

# 112\. BACKTRACKING

Le parser essaie une possibilité.

Si elle échoue :

retour  
↓  
autre possibilité

Cela peut être simple à implémenter mais potentiellement coûteux.

Dans le pire cas :

\[ O(2^n) \]

ou davantage selon la structure du problème.

# 113\. MEMOIZATION ET PACKRAT

La mémorisation peut éviter de recalculer plusieurs fois les mêmes analyses.

Dans certains systèmes PEG, les parsers Packrat utilisent cette idée.

Le compromis classique :

text id="qtrade" plus de mémoire ↓ moins de recalcul ↓ meilleure complexité temporelle

# 114\. LANGAGE ET GRAPHE

Un automate peut être vu comme un graphe orienté :

text id="qgraph" états = sommets transitions = arêtes

Cette représentation permet de connecter :

- automates ;
- graphes ;
- BFS ;
- DFS ;
- analyse de chemins.

# 115\. AUTOMATE ET GRAPH ALGORITHMS

Applications :

- accessibilité ;
- détection d’états morts ;
- équivalence ;
- minimisation ;
- analyse de transitions ;
- recherche de chemins.

# 116\. ÉTATS MORTS

Un état mort est un état dont aucune continuation ne permet d’atteindre un état acceptant.

Ils peuvent être identifiés puis supprimés lors de certaines optimisations.

# 117\. ÉTATS INACCESSIBLES

Un état est inaccessible si aucun chemin depuis l’état initial ne permet de l’atteindre.

Ils peuvent également être supprimés.

# 118\. COMPLÉMENT D’UN DFA

Pour un DFA complet :

\[ L(A)^c \]

peut être obtenu en échangeant :

- états acceptants ;
- états non acceptants.

Il faut notamment gérer correctement les transitions manquantes.

# 119\. PRODUIT D’AUTOMATES

Pour combiner des propriétés, on peut construire un automate produit.

Exemple :

\`\`\`text id=“qproduct” A reconnaît propriété P B reconnaît propriété Q

A × B ↓ P ET Q

  
<br/>Cette technique est très utile en vérification formelle.  
<br/>\---  
<br/>\# 120. MODEL CHECKING  
<br/>Le model checking vérifie automatiquement si un système fini satisfait certaines propriétés.  
<br/>Conceptuellement :  
<br/>\`\`\`text id="qmodel"  
système  
↓  
modèle fini  
↓  
exploration  
↓  
propriété  
↓  
SATISFAIT / VIOLÉ

Il utilise fortement :

- automates ;
- graphes ;
- logique temporelle.

# 121\. AUTOMATES ET PROTOCOLES

Un protocole réseau peut être modélisé comme une machine à états.

Exemple :

text id="qprotocol" DISCONNECTED ↓ CONNECTING ↓ AUTHENTICATING ↓ ESTABLISHED ↓ CLOSING ↓ CLOSED

Chaque message provoque une transition.

# 122\. VALIDATION DES PROTOCOLES

Un automate permet de détecter :

- états impossibles ;
- transitions illégales ;
- séquences invalides ;
- deadlocks ;
- états non atteignables.

# 123\. VALIDATION DE FORMATS

Un fichier peut être défini comme un langage.

Exemple :

HEADER  
VERSION  
DATA\*  
END

Un parser peut vérifier sa conformité.

# 124\. VALIDATION DE CONFIGURATION

Une configuration :

server:  
port: 8080  
tls: true

peut être considérée comme une structure appartenant à un langage formel.

Le système doit vérifier :

- syntaxe ;
- structure ;
- types ;
- contraintes.

# 125\. VALIDATION DE REQUÊTES

Les langages de requête comme SQL possèdent :

- lexique ;
- grammaire ;
- AST ;
- sémantique.

Pipeline :

text id="qsql" SQL ↓ lexer ↓ parser ↓ AST ↓ semantic analysis ↓ query plan

# 126\. LANGAGES DSL

Un DSL — Domain-Specific Language — est conçu pour un domaine particulier.

Exemples :

- configuration ;
- requêtes ;
- règles métier ;
- workflows ;
- shaders ;
- infrastructure ;
- automation.

Créer un DSL implique notamment :

text id="qds" syntaxe ↓ grammaire ↓ parser ↓ AST ↓ sémantique ↓ exécution / génération

# 127\. DSL ET PRODUCT ENGINEERING

Un DSL peut réduire la complexité pour l’utilisateur.

Exemple :

deploy app to production

peut être transformé en :

validation  
→ build  
→ tests  
→ deploy  
→ monitoring

La logique complexe est cachée derrière un langage plus simple.

# 128\. LANGAGES DE CONFIGURATION

Un bon format de configuration doit répondre à :

- syntaxe ;
- validation ;
- types ;
- valeurs par défaut ;
- erreurs ;
- compatibilité ;
- versioning.

Les grammaires formelles fournissent une base pour formaliser cette syntaxe.

# 129\. COMPILATION ET TRANSFORMATION DE LANGAGES

Un compilateur peut être vu comme :

\[ L_{source}L_{target} \]

avec une transformation sémantiquement correcte.

L’objectif n’est pas seulement de reconnaître le langage source.

Il faut préserver le comportement.

# 130\. TRANSPILATION

Un transpiler transforme :

text id="qtrans" Langage A ↓ AST ↓ Langage B

Exemples génériques :

- langage moderne → JavaScript ;
- DSL → SQL ;
- DSL → configuration ;
- langage source → autre langage.

# 131\. COMPILATEUR COMME PIPELINE DE LANGAGES

Chaque étape produit une représentation appartenant à un langage donné.

text id="qpipe" Source Language ↓ Token Language ↓ AST Language ↓ IR Language ↓ Assembly / Bytecode ↓ Machine Language

Cette perspective est extrêmement puissante.

# 132\. SÉMANTIQUE

La syntaxe répond :

« Est-ce correctement formé ? »

La sémantique répond :

« Que signifie cette structure ? »

Exemple :

x + y

Syntaxiquement valide.

Mais il faut encore savoir :

- types de (x) et (y) ;
- opération + ;
- résultat ;
- effets.

# 133\. SÉMANTIQUE OPÉRATIONNELLE

Décrit comment un programme évolue étape par étape.

Conceptuellement :

\[ configuration configuration’ \]

# 134\. SÉMANTIQUE DÉNOTATIONNELLE

Associe une construction syntaxique à un objet mathématique représentant son sens.

# 135\. SÉMANTIQUE AXIOMATIQUE

Décrit le comportement à travers des propriétés et assertions.

Elle se connecte notamment à :

- logique de Hoare ;
- vérification formelle ;
- preuve de programmes.

# 136\. LOGIQUE DE HOARE

On utilise des triples :

\[ {P} C {Q} \]

où :

- (P) = précondition ;
- (C) = commande ;
- (Q) = postcondition.

Cela crée une connexion forte entre :

- logique ;
- programmes ;
- vérification.

# 137\. GRAMMAIRE ET TYPE SYSTEM

Les types peuvent être vus comme une autre forme de structure formelle.

Un type system impose des contraintes :

text id="qtype" expression ↓ type checking ↓ valid / invalid

Certaines propriétés de typage peuvent être formulées comme des systèmes de règles.

# 138\. PATTERN MATCHING

Les expressions structurées peuvent être reconnues selon des motifs.

Applications :

- compilateurs ;
- parsers ;
- arbres ;
- données ;
- IA symbolique.

# 139\. TERM REWRITING

Une structure peut être transformée par des règles :

\[ AB \]

Applications :

- simplification ;
- optimisation ;
- calcul symbolique ;
- compilateurs ;
- systèmes de règles.

# 140\. GRAMMAIRES ATTRIBUÉES

On peut associer des informations aux symboles grammaticaux.

Exemples :

- type ;
- valeur ;
- emplacement ;
- contexte.

Cela permet de rapprocher :

syntaxe  
+  
sémantique

dans les systèmes de compilation.

# 141\. AUTOMATES ET IA SYMBOLIQUE

Les automates peuvent représenter :

- règles ;
- états ;
- contraintes ;
- comportements ;
- séquences valides.

Applications :

- extraction ;
- validation ;
- contrôle ;
- agents symboliques ;
- planification ;
- vérification.

# 142\. AUTOMATES ET LLM

Les LLM génèrent des séquences de tokens.

Les grammaires peuvent contraindre ces séquences.

Conceptuellement :

text id="qllm" LLM ↓ candidate tokens ↓ grammar constraint ↓ valid tokens ↓ output

Cela permet d’utiliser des grammaires pour :

- sorties JSON structurées ;
- DSL ;
- appels d’outils ;
- SQL ;
- formats stricts.

# 143\. CONSTRAINED DECODING

Le modèle peut être empêché de produire certaines séquences invalides.

Un automate peut représenter les séquences autorisées.

text id="qconstraint" LLM distribution ↓ automaton / grammar ↓ mask invalid tokens ↓ next-token selection

C’est une connexion moderne extrêmement importante entre théorie des langages et IA générative.

# 144\. AGENTS IA ET PROTOCOLES FORMELS

Un agent peut être décrit par un automate :

text id="qagent" IDLE ↓ PLANNING ↓ TOOL_CALL ↓ WAITING ↓ OBSERVATION ↓ VALIDATION ↓ EXECUTION ↓ DONE

Cela permet de définir :

- états autorisés ;
- transitions ;
- conditions ;
- actions interdites.

# 145\. AGENT SAFETY VIA STATE MACHINES

Une architecture agentique peut utiliser un automate pour empêcher :

text id="qguard" UNAUTHENTICATED ↓ EXECUTE_PAYMENT

si aucune transition valide n’existe.

On obtient :

**la machine à états comme garde-fou architectural.**

# 146\. PROTOCOL ENGINEERING

Un protocole peut être spécifié par :

- états ;
- messages ;
- transitions ;
- invariants ;
- erreurs ;
- timeouts.

Puis implémenté à partir de cette spécification.

# 147\. PROPRIÉTÉS D’UN PROTOCOLE

On peut vérifier :

### Safety

« Rien de mauvais ne doit arriver. »

### Liveness

« Quelque chose de bon finira par arriver. »

Ces notions sont centrales dans la vérification des systèmes concurrents et distribués.

# 148\. DEADLOCK

Un système est bloqué lorsque plusieurs composants attendent indéfiniment.

Les graphes d’états et modèles formels peuvent aider à détecter ces situations.

# 149\. MODEL CHECKING ET ÉTATS

Le model checker explore les états accessibles.

text id="qmc" état initial ↓ états suivants ↓ exploration ↓ contre-exemple ou preuve

Un contre-exemple peut être une séquence :

state1 → state2 → state3 → error

# 150\. EXPRESSIVITÉ VS COMPLEXITÉ

Plus un formalisme est expressif, plus il peut devenir difficile à analyser.

Exemple conceptuel :

\`\`\`text id=“qexpress” regex / DFA ↓ simple et efficace

CFG / PDA ↓ plus expressif

Turing-complete ↓ puissant mais problèmes fondamentaux

  
<br/>C’est une tension fondamentale :  
<br/>\> \*\*expressivité ↔ analyseabilité ↔ performance.\*\*  
<br/>\---  
<br/>\# 151. TYPAGE DE PROBLÈME  
<br/>Lorsqu’un problème de traitement de texte apparaît :  
<br/>\`\`\`text  
simple motif  
↓  
regex  
<br/>structure imbriquée  
↓  
grammar / parser  
<br/>contexte + pile  
↓  
PDA / CFG  
<br/>calcul général  
↓  
machine de Turing / langage général

# 152\. QUAND UTILISER UNE REGEX ?

Bonne utilisation :

- motifs locaux ;
- tokens ;
- validation simple ;
- extraction ;
- recherche.

Exemples :

- email approximatif ;
- numéro ;
- identifiant ;
- date simple ;
- token lexical.

# 153\. QUAND NE PAS UTILISER UNE REGEX ?

Éviter de forcer une regex pour :

- structures fortement imbriquées ;
- expressions arithmétiques complexes ;
- langages complets ;
- SQL ;
- code source ;
- structures récursives.

Dans ces cas :

utiliser une grammaire et un parser.

# 154\. ARCHITECTURE D’UN PARSER MODERNE

text id="qmodern" INPUT ↓ LEXER ↓ TOKENS ↓ PARSER ↓ AST ↓ SEMANTIC ANALYZER ↓ VALIDATED AST ↓ IR ↓ EXECUTOR / CODE GENERATOR

# 155\. ARCHITECTURE D’UN INTERPRÉTEUR

text id="qint" SOURCE ↓ LEXER ↓ PARSER ↓ AST ↓ EVALUATOR ↓ RUNTIME

# 156\. ARCHITECTURE D’UN DSL

text id="qdsla" DSL ↓ Lexer ↓ Parser ↓ AST ↓ Validation ↓ Semantic analysis ↓ IR ↓ Backend

# 157\. ARCHITECTURE D’UN VALIDATEUR

text id="qvalid" INPUT ↓ LEXICAL VALIDATION ↓ SYNTAX VALIDATION ↓ STRUCTURAL VALIDATION ↓ SEMANTIC VALIDATION ↓ BUSINESS RULE VALIDATION ↓ VALID / INVALID

# 158\. FICHES D’APPROFONDISSEMENT

## Q01 — Langages formels

À maîtriser :

- alphabet ;
- chaîne ;
- mot vide ;
- (^\*) ;
- (^+) ;
- langage ;
- concaténation ;
- puissance d’un langage.

## Q02 — Automates finis

À maîtriser :

- état ;
- transition ;
- état initial ;
- état final ;
- fonction de transition ;
- langage reconnu.

## Q03 — DFA

À maîtriser :

- déterminisme ;
- complétion ;
- reconnaissance ;
- minimisation.

## Q04 — NFA

À maîtriser :

- non-déterminisme ;
- ()-transitions ;
- fermeture-() ;
- construction par sous-ensembles.

## Q05 — Expressions régulières

À maîtriser :

- union ;
- concaténation ;
- étoile ;
- plus ;
- classes ;
- quantificateurs ;
- différences entre théorie et moteurs pratiques.

## Q06 — Théorème de Kleene

À maîtriser :

langages réguliers ↔ automates finis ↔ expressions régulières.

## Q07 — Myhill-Nerode

À maîtriser :

- indistinguabilité ;
- classes d’équivalence ;
- DFA minimal ;
- caractérisation des langages réguliers.

## Q08 — Grammaires

À maîtriser :

- terminaux ;
- non-terminaux ;
- productions ;
- dérivation ;
- langage engendré.

## Q09 — CFG

À maîtriser :

- grammaire hors contexte ;
- arbre de dérivation ;
- ambiguïté ;
- forme normale de Chomsky.

## Q10 — Automates à pile

À maîtriser :

- pile ;
- push ;
- pop ;
- transition ;
- reconnaissance ;
- relation CFG/PDA.

## Q11 — Parsing

À maîtriser :

- top-down ;
- bottom-up ;
- recursive descent ;
- LL ;
- LR ;
- shift-reduce.

## Q12 — FIRST / FOLLOW

À maîtriser :

- calcul ;
- tables LL(1) ;
- conflits ;
- prédiction.

## Q13 — AST

À maîtriser :

- parse tree ;
- AST ;
- nœuds ;
- traversée ;
- transformation.

## Q14 — Analyse sémantique

À maîtriser :

- symbol table ;
- portée ;
- résolution ;
- typage ;
- contraintes.

## Q15 — Compilateurs

À maîtriser :

- front-end ;
- IR ;
- optimisation ;
- back-end ;
- code generation.

## Q16 — Machines de Turing

À maîtriser :

- ruban ;
- tête ;
- états ;
- transitions ;
- acceptation ;
- arrêt.

## Q17 — Calculabilité

À maîtriser :

- décidabilité ;
- reconnaissabilité ;
- problème de l’arrêt ;
- réduction.

## Q18 — Model Checking

À maîtriser :

- système à états ;
- propriété ;
- exploration ;
- safety ;
- liveness ;
- contre-exemple.

## Q19 — Parsing moderne

À maîtriser :

- PEG ;
- parser combinators ;
- backtracking ;
- memoization ;
- Packrat.

## Q20 — Langages pour IA

À maîtriser :

- constrained decoding ;
- grammar-guided generation ;
- structured output ;
- automates de contraintes ;
- protocoles agentiques.

# 159\. PROJETS D’APPRENTISSAGE

## Projet 1 — Simulateur de DFA

Créer :

Automate  
├── states  
├── alphabet  
├── transitions  
├── startState  
└── acceptStates

Puis :

accept("010101")

doit retourner :

true / false

# 160\. PROJET 2 — Convertisseur NFA → DFA

Implémenter :

NFA  
↓  
ε-closure  
↓  
subset construction  
↓  
DFA

Objectif :

comprendre concrètement le non-déterminisme.

# 161\. PROJET 3 — Minimisateur de DFA

Construire un outil qui :

1.  supprime les états inaccessibles ;
2.  partitionne les états ;
3.  raffine les partitions ;
4.  construit le DFA minimal.

# 162\. PROJET 4 — Moteur Regex Pédagogique

Construire une mini-syntaxe :

a  
ab  
a|b  
a\*

Puis :

Regex  
↓  
AST regex  
↓  
ε-NFA  
↓  
DFA  
↓  
matcher

# 163\. PROJET 5 — Lexer

Créer un lexer pour un mini-langage :

let x = 42 + 10;

Sortie :

LET  
IDENTIFIER  
ASSIGN  
NUMBER  
PLUS  
NUMBER  
SEMICOLON

# 164\. PROJET 6 — Parser arithmétique

Construire un parser pour :

2 + 3 \* (4 - 1)

Produire :

AST

puis l’évaluer.

# 165\. PROJET 7 — Mini-langage

Créer un langage :

let x = 10;  
<br/>if x > 5 {  
print(x);  
}

Pipeline :

source  
↓  
lexer  
↓  
parser  
↓  
AST  
↓  
semantic analysis  
↓  
interpreter

# 166\. PROJET 8 — Mini-interpréteur

Ajouter :

- variables ;
- expressions ;
- conditions ;
- boucles ;
- fonctions ;
- portée.

# 167\. PROJET 9 — DSL métier

Créer un DSL simple :

workflow payment {  
validate  
authorize  
charge  
notify  
}

Le parser construit un AST puis génère :

- JSON ;
- code ;
- configuration ;
- workflow exécutable.

# 168\. PROJET 10 — Validateur de protocole

Décrire un protocole :

INIT  
↓  
AUTH  
↓  
READY  
↓  
REQUEST  
↓  
RESPONSE  
↓  
CLOSE

Puis refuser toute séquence illégale.

# 169\. PROJET 11 — Grammar-Constrained LLM

Construire un système où la génération d’un modèle doit respecter une grammaire.

Exemple :

action ::= "search" | "calculate" | "finish"

Le modèle ne peut produire que des sorties correspondant au langage.

# 170\. PROJET 12 — Agent comme automate

Modéliser un agent :

IDLE  
↓  
PLAN  
↓  
CALL_TOOL  
↓  
OBSERVE  
↓  
VERIFY  
↓  
ACT  
↓  
DONE

Puis définir :

- transitions interdites ;
- transitions conditionnelles ;
- timeouts ;
- erreurs ;
- états de récupération.

# 171\. CHALLENGES SANS IA

## Challenge 1

Construire un DFA reconnaissant :

\[ L={w{0,1}^\* w1} \]

## Challenge 2

Construire un DFA reconnaissant les chaînes se terminant par :

01

## Challenge 3

Construire un NFA puis le convertir en DFA.

## Challenge 4

Minimiser un DFA donné.

## Challenge 5

Démontrer qu’un langage donné n’est pas régulier avec le pumping lemma.

## Challenge 6

Construire une grammaire pour :

\[ a^n b^n \]

## Challenge 7

Construire un PDA reconnaissant :

\[ a^n b^n \]

## Challenge 8

Construire un AST pour :

\[ 1+2\*3 \]

## Challenge 9

Calculer FIRST/FOLLOW d’une grammaire.

## Challenge 10

Construire un parser recursive descent.

## Challenge 11

Transformer une grammaire avec récursion gauche.

## Challenge 12

Construire une machine de Turing reconnaissant un langage simple.

# 172\. CHALLENGES AVEC IA

## Challenge IA 1 — Grammar Critic

Donner une grammaire à l’IA.

Demander :

- ambiguïtés ;
- récursion gauche ;
- conflits ;
- expressivité ;
- complexité.

Puis vérifier manuellement.

## Challenge IA 2 — Parser Generator

Donner une spécification DSL.

Demander à l’IA :

lexer  
+  
grammar  
+  
AST  
+  
parser

Puis tester des cas adversariaux.

## Challenge IA 3 — Automaton Synthesizer

Décrire un langage en français.

Demander à l’IA de produire :

DFA

Puis vérifier chaque état.

## Challenge IA 4 — Protocol Verifier

Donner une machine à états d’un protocole.

Demander à l’IA de rechercher :

- transitions impossibles ;
- deadlocks ;
- états inaccessibles ;
- séquences invalides ;
- violations de safety.

## Challenge IA 5 — Grammar-Constrained Agent

Construire un agent dont toutes les actions doivent appartenir à un langage formel.

# 173\. APPLICATIONS CRÉATIVES

## 173.1 State-Machine Security

Transformer chaque workflow sensible en automate :

AUTHENTICATED  
↓  
AUTHORIZED  
↓  
PAYMENT_PENDING  
↓  
PAYMENT_CONFIRMED

Une action interdite devient simplement une transition inexistante.

## 173.2 Grammar-Based API

Définir les requêtes API comme un langage.

Le serveur peut refuser toute requête qui n’appartient pas au langage autorisé.

## 173.3 Protocol Compiler

Décrire un protocole sous forme déclarative :

protocol Payment {  
authenticate  
authorize  
charge  
confirm  
}

Puis générer :

- state machine ;
- validation ;
- documentation ;
- tests ;
- code de base.

## 173.4 Agent Protocol Language

Créer un DSL pour les interactions d’agents :

agent A -> agent B : REQUEST  
agent B -> agent A : RESPONSE

Puis compiler la spécification en :

- automate ;
- validateurs ;
- tests ;
- simulateur.

## 173.5 AI Output Grammar

Créer une grammaire stricte :

response ::= intent + arguments + confidence

Le modèle est contraint à produire des sorties conformes.

## 173.6 Grammar-Based RAG

Les requêtes générées par l’agent peuvent être limitées à un langage sûr :

QUERY ::= SEARCH | FILTER | SORT

Cela peut réduire certaines classes d’erreurs structurelles.

## 173.7 Safe Tool Calling

Définir un langage des actions autorisées :

ACTION ::= READ | SEARCH | CREATE | UPDATE

Puis restreindre les sorties du modèle à cet ensemble.

## 173.8 Protocol Firewall

Un système peut utiliser une machine à états pour filtrer les messages selon l’état courant.

message  
↓  
current state  
↓  
allowed transition?  
↓  
ALLOW / REJECT

## 173.9 Configuration Language

Créer un DSL pour configurer une infrastructure.

server production {  
port 443  
tls enabled  
replicas 3  
}

Puis générer :

- fichiers de configuration ;
- infrastructure as code ;
- validation ;
- documentation.

## 173.10 Visual Programming

Une interface graphique peut être représentée comme un graphe d’états ou un AST.

L’utilisateur construit visuellement :

node  
↓  
node  
↓  
condition  
↙ ↘  
A B

puis le système génère du code.

# 174\. MATRICE DE RECONNAISSANCE

| Problème | Concept à suspecter |
| --- | --- |
| motif simple | regex |
| format lexical | automate fini |
| séquence avec état | DFA |
| alternatives multiples | NFA |
| structure imbriquée | grammaire |
| parenthèses équilibrées | CFG / PDA |
| expression arithmétique | parser |
| code source | lexer + parser |
| arbre syntaxique | AST |
| type incorrect | analyse sémantique |
| protocole à états | machine à états |
| workflow | automate |
| DSL | grammaire + parser |
| requête | lexer + parser + AST |
| calcul général | machine de Turing |
| problème potentiellement non décidable | calculabilité |
| vérification d’un système fini | model checking |
| sortie LLM structurée | grammaire + constrained decoding |
| agent à comportement contrôlé | state machine |

# 175\. LES DISTINCTIONS À NE JAMAIS OUBLIER

\`\`\`text id=“qdist” ALPHABET ≠ LANGAGE

CHAÎNE ≠ LANGAGE

REGEX ≠ PARSER

LEXER ≠ PARSER

SYNTAXE ≠ SÉMANTIQUE

DFA ≠ NFA

NFA ≠ MACHINE ALÉATOIRE

CFG ≠ REGEX

PDA ≠ DFA

AST ≠ PARSE TREE

COMPILATEUR ≠ INTERPRÉTEUR

RECONNAÎTRE ≠ DÉCIDER

CALCULABLE ≠ EFFICACE

ÉTAT ≠ MÉMOIRE GÉNÉRALE

PROTOCOLE ≠ SIMPLE SÉQUENCE DE MESSAGES

  
\---  
<br/>\# 176. MENTAL MODEL GLOBAL  
<br/>Le domaine Q peut être mémorisé avec cette chaîne :  
<br/>\`\`\`text id="qmental"  
ALPHABET  
↓  
CHAÎNES  
↓  
LANGAGES  
↓  
GRAMMAIRES  
↓  
AUTOMATES  
↓  
RECONNAISSANCE  
↓  
PARSING  
↓  
AST  
↓  
SÉMANTIQUE  
↓  
IR  
↓  
COMPILATION / INTERPRÉTATION  
↓  
EXÉCUTION

Et selon la puissance nécessaire :

text id="qpower2" REGEX ↓ DFA / NFA ↓ CFG / PDA ↓ TURING MACHINE

# 177\. CINQ GRANDES QUESTIONS

Lorsqu’un nouveau problème de langage apparaît, demander :

### 1\. Quelles sont les chaînes valides ?

Définir :

\[ L^\* \]

### 2\. Quelle mémoire est nécessaire ?

- aucune mémoire variable ;
- pile ;
- mémoire générale.

### 3\. Quel formalisme convient ?

- regex ;
- DFA ;
- NFA ;
- CFG ;
- PDA ;
- machine de Turing.

### 4\. Comment reconnaître ou analyser ?

- matcher ;
- lexer ;
- parser ;
- interpréteur ;
- compilateur.

### 5\. Quelle est la limite ?

- expressivité ;
- ambiguïté ;
- complexité ;
- décidabilité.

# 178\. CONNEXIONS AVEC LES AUTRES DOMAINES

## A — Logique et fondements

Connexion directe :

- logique formelle ;
- propositions ;
- preuves ;
- systèmes de règles ;
- sémantique ;
- calculabilité.

## E — Théorie des graphes

Les automates sont naturellement des graphes orientés.

Applications :

- parcours ;
- accessibilité ;
- minimisation ;
- model checking ;
- protocoles.

## F — Combinatoire

Intervient dans :

- nombre d’états ;
- nombre de chaînes ;
- constructions ;
- complexité ;
- explosion combinatoire.

## O — Complexité

Connexion fondamentale :

expressivité  
↓  
problèmes de décision  
↓  
algorithmes  
↓  
complexité

## P — Cryptographie

Connexion intéressante :

- protocoles ;
- machines à états ;
- formats ;
- validation ;
- protocoles cryptographiques ;
- parsing des messages.

Un protocole cryptographique peut être représenté comme une machine à états dont les transitions manipulent des primitives cryptographiques.

## M — Théorie de l’information

Connexion :

- entropie des chaînes ;
- compression ;
- codage ;
- représentation ;
- transmission.

# 179\. CRYPTOGRAPHIE + AUTOMATES

Un système sécurisé peut être modélisé :

text id="qcryptauto" STATE ↓ message ↓ authentication ↓ verification ↓ transition

La cryptographie protège le message.

L’automate vérifie si le message est autorisé dans l’état courant.

Cela produit une combinaison :

**sécurité cryptographique + sécurité comportementale.**

# 180\. COMPILATEUR + THÉORIE DES LANGAGES

Un compilateur peut être compris comme une succession de transformations :

text id="qcompiler2" LANGAGE SOURCE ↓ LANGAGE LEXICAL ↓ LANGAGE SYNTAXIQUE ↓ LANGAGE SÉMANTIQUE ↓ LANGAGE INTERMÉDIAIRE ↓ LANGAGE MACHINE

Chaque étape impose des contraintes formelles différentes.

# 181\. AGENTS IA + LANGAGES FORMELS

Un agent moderne peut être vu comme :

text id="qagent2" LLM ↓ génération probabiliste ↓ contraintes formelles ↓ langage autorisé ↓ parser ↓ validation ↓ action

Cela crée un principe très puissant :

**utiliser l’IA pour générer, mais utiliser les langages formels pour contrôler.**

# 182\. IA PROBABILISTE + SYSTÈMES FORMELS

On peut donc combiner :

text id="qhybrid" IA ↓ exploration créativité génération + FORMALISME ↓ validation contraintes sécurité ↓ ACTION

Cette architecture est particulièrement intéressante pour :

- agents ;
- outils ;
- workflows ;
- code generation ;
- automatisation ;
- systèmes critiques.

# 183\. TEST ULTIME

Prendre un mini-langage :

agent Alice {  
search("AI")  
summarize()  
publish()  
}

Être capable de concevoir :

1.  son alphabet ;
2.  ses tokens ;
3.  ses regex lexicales ;
4.  son lexer ;
5.  sa grammaire ;
6.  son parser ;
7.  son AST ;
8.  ses règles sémantiques ;
9.  son interpréteur ;
10. son automate d’exécution ;
11. ses règles d’erreur ;
12. ses propriétés de sécurité ;
13. ses tests ;
14. son analyse de complexité.

À ce stade, la théorie n’est plus séparée du génie logiciel.

Elle devient une méthode de conception.

# 184\. CHECKLIST DE MAÎTRISE

## Langages

- alphabet ;
- chaîne ;
- mot vide ;
- (^\*) ;
- langage ;
- concaténation.

## Automates

- DFA ;
- NFA ;
- ()-NFA ;
- transition ;
- acceptation ;
- conversion NFA → DFA ;
- minimisation.

## Expressions régulières

- union ;
- concaténation ;
- étoile ;
- plus ;
- regex → automate ;
- limites des regex pratiques.

## Grammaires

- terminaux ;
- non-terminaux ;
- productions ;
- dérivation ;
- arbre ;
- ambiguïté ;
- CFG.

## Parsing

- lexer ;
- parser ;
- recursive descent ;
- LL ;
- LR ;
- shift-reduce ;
- FIRST ;
- FOLLOW.

## Compilation

- AST ;
- table des symboles ;
- analyse sémantique ;
- IR ;
- optimisation ;
- génération de code.

## Calculabilité

- machine de Turing ;
- reconnaissance ;
- décision ;
- arrêt ;
- calculabilité.

## Applications

- compilateurs ;
- interpréteurs ;
- DSL ;
- validation ;
- protocoles ;
- model checking ;
- structured generation ;
- agents IA.

# 185\. SYNTHÈSE FINALE

La théorie des langages et des automates peut être comprise comme une progression :

text id="qfinal" SYMBOLES ↓ CHAÎNES ↓ LANGAGES ↓ RÈGLES ↓ GRAMMAIRES ↓ MACHINES ↓ RECONNAISSANCE ↓ ANALYSE ↓ TRANSFORMATION ↓ EXÉCUTION

Les différentes machines correspondent à différentes puissances :

\`\`\`text id=“qfinal2” AUTOMATE FINI ↓ mémoire finie ↓ langage régulier ↓ REGEX / DFA / NFA

↓  
<br/>AUTOMATE À PILE  
↓  
mémoire pile  
↓  
langage hors contexte  
↓  
CFG / PARSER  
<br/>↓  
<br/>MACHINE DE TURING  
↓  
mémoire générale  
↓  
calcul général  
↓  
CALCULABILITÉ

  
<br/>Le point fondamental est :  
<br/>\> \*\*La théorie des langages décrit ce qui constitue une structure valide ; les automates décrivent comment la reconnaître ; les grammaires décrivent comment la construire ; les parsers en extraient la structure ; les compilateurs et interpréteurs lui donnent un comportement.\*\*  
<br/>\---  
<br/>\# 186. FORMULE MENTALE ULTIME  
<br/>\`\`\`text id="qultimate"  
LANGAGE  
│  
┌─────────┴─────────┐  
↓ ↓  
DESCRIPTION RECONNAISSANCE  
│ │  
GRAMMAIRE AUTOMATE  
│ │  
└─────────┬─────────┘  
↓  
PARSER  
↓  
AST  
↓  
SÉMANTIQUE  
↓  
IR / EXÉCUTION  
↓  
COMPILATEUR / VM

Et la question à retenir :

**« Quelle est la structure du langage, quelle mémoire faut-il pour la reconnaître, et quelle machine permet de la traiter correctement ? »**

Cette question permet de passer naturellement :

**d’une regex à un automate, d’un automate à une grammaire, d’une grammaire à un parser, d’un parser à un compilateur, puis d’un langage formel à un système logiciel complet.**