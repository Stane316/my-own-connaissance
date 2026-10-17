# DOCUMENT M — THÉORIE DE L’INFORMATION

## Mesurer, représenter, compresser et transmettre l’information

# 00 — PRÉDISPOSITION D’INTÉGRATION

Ce document constitue une **référence mathématique et informatique réutilisable** pour tout projet dans lequel intervient la notion d’information.

Lorsqu’un système utilise ce domaine, l’IA doit être capable d’identifier :

- quelles variables représentent l’information ;
- quelles variables représentent l’incertitude ;
- comment mesurer cette information ;
- comment mesurer la dépendance entre deux variables ;
- comment quantifier la différence entre deux distributions ;
- comment représenter l’information efficacement ;
- comment compresser les données ;
- comment transmettre l’information sur un canal bruité ;
- quelle quantité d’information un canal peut transporter ;
- comment exploiter l’information dans un modèle d’IA ;
- comment distinguer information utile, redondance, bruit et perte ;
- comment transformer ces notions mathématiques en mécanismes logiciels.

Le domaine ne doit donc pas être réduit à :

Entropie = incertitude.

Il faut comprendre le système plus général :

SOURCE  
↓  
INCERTITUDE  
↓  
INFORMATION  
↓  
REPRÉSENTATION  
↓  
CODAGE  
↓  
STOCKAGE / TRANSMISSION  
↓  
BRUIT / PERTURBATION  
↓  
DÉCODAGE  
↓  
INFORMATION RÉCUPÉRÉE

En intelligence artificielle, une autre chaîne devient essentielle :

DONNÉES  
↓  
REPRÉSENTATION  
↓  
INFORMATION PERTINENTE  
↓  
APPRENTISSAGE  
↓  
PRÉDICTION  
↓  
DÉCISION

La théorie de l’information fournit une partie du langage mathématique permettant d’analyser ces transformations.

# 01 — IDENTITÉ DU DOMAINE

## 01.1 — Nom

**Domaine M — Théorie de l’information**

## 01.2 — Idée centrale

La théorie de l’information étudie mathématiquement :

- la quantité d’information ;
- l’incertitude ;
- la dépendance entre variables ;
- la représentation des données ;
- la compression ;
- la transmission ;
- le bruit ;
- la capacité des canaux ;
- les limites fondamentales du traitement de l’information.

Elle a été formalisée principalement par Claude Shannon dans son travail fondateur de 1948 sur la communication. Stanford décrit la théorie de l’information comme une science des opérations sur les données telles que la compression, le stockage et la communication.

## 01.3 — Question fondamentale

Une formulation extrêmement utile est :

**Combien d’information contient une observation, une variable, un message ou une représentation, et combien d’information peut-on conserver, transmettre ou éliminer sans perdre ce qui nous intéresse ?**

Cette question conduit naturellement à :

- l’entropie ;
- l’information propre d’un événement ;
- l’entropie conditionnelle ;
- l’information mutuelle ;
- la divergence ;
- la compression ;
- la capacité ;
- le débit-distorsion ;
- le codage ;
- l’apprentissage statistique.

# 02 — PLACE DANS LA PYRAMIDE MATHÉMATIQUE

La théorie de l’information se situe à l’intersection de plusieurs domaines.

PROBABILITÉS  
↓  
variables aléatoires  
distributions  
espérance  
↓  
THÉORIE DE L'INFORMATION  
↓  
entropie  
information  
divergence  
information mutuelle  
codage  
capacité  
↓  
STATISTIQUES / ML / IA  
↓  
apprentissage  
classification  
NLP  
représentation  
génération  
↓  
INGÉNIERIE  
↓  
compression  
réseaux  
stockage  
communication  
systèmes distribués

Elle possède également des connexions profondes avec :

- la théorie des probabilités ;
- les statistiques ;
- la combinatoire ;
- l’algèbre ;
- la théorie des graphes ;
- l’optimisation ;
- la cryptographie ;
- la théorie des codes ;
- la théorie des langages ;
- le machine learning ;
- les systèmes distribués ;
- le traitement du signal.

# 03 — INFORMATION ET INCERTITUDE

## 03.1 — L’information n’est pas simplement une donnée

Une donnée brute :

42

n’a pas nécessairement une quantité d’information déterminée indépendamment du contexte.

Si l’on sait déjà avec certitude que la valeur est 42, observer 42 apporte très peu d’information.

Si l’on pensait que plusieurs valeurs étaient possibles et que l’observation révèle finalement 42, l’événement peut apporter davantage d’information.

La théorie de Shannon formalise cette intuition à partir des probabilités.

# 04 — INFORMATION AUTO-CONTENUE D’UN ÉVÉNEMENT

Pour un événement (x) de probabilité (p(x)), on définit la quantité d’information ou **surprise** :

\[ I(x)=-p(x) \]

ou :

\[ I(x)= \]

Si le logarithme est en base 2 :

\[ I(x)=-\_2 p(x) \]

l’unité est le **bit**.

## 04.1 — Interprétation

Un événement très probable contient peu d’information.

Un événement très improbable contient davantage d’information.

Par exemple :

\[ p(x)= \]

donne :

\[ I(x)=1 \]

Alors que :

\[ p(x)= \]

donne :

\[ I(x)=10 \]

## 04.2 — Pourquoi le logarithme ?

Le logarithme possède une propriété essentielle :

\[ (ab)=a+b \]

Ainsi, pour deux événements indépendants :

\[ I(x,y) = -\]

donne :

\[ I(x,y)=I(x)+I(y) \]

L’information de deux événements indépendants peut donc s’additionner.

C’est l’une des raisons fondamentales du choix logarithmique.

# 05 — UNITÉS D’INFORMATION

## 05.1 — Bit

Avec un logarithme en base 2 :

\[ I=-\_2 p \]

l’unité est le **bit**.

## 05.2 — Nat

Avec le logarithme naturel :

\[ I=-p \]

l’unité est le **nat**.

## 05.3 — Hartley

Avec un logarithme en base 10 :

\[ I=-\_{10}p \]

l’unité est parfois appelée **hartley**.

## 05.4 — Conversion

Entre nats et bits :

\[ 1 = \_2(e) \]

et :

\[ 1 = (2) \]

# 06 — ENTROPIE

L’entropie est l’une des notions centrales du domaine.

Pour une variable aléatoire discrète (X) :

\[ H(X) = -\_x p(x)\_2 p(x) \]

Équivalent :

\[ H(X) = \[-\_2 p(X)\] \]

L’entropie est donc l’information moyenne produite par la réalisation de (X).

Stanford donne précisément cette interprétation de l’entropie comme mesure de l’incertitude d’une variable aléatoire.

# 07 — INTERPRÉTATION DE L’ENTROPIE

L’entropie mesure principalement :

**l’incertitude moyenne avant d’observer la variable.**

Elle ne signifie donc pas simplement :

quantité physique de données.

Deux fichiers de même taille peuvent contenir des quantités d’information statistique très différentes.

## 07.1 — Variable déterministe

Si :

\[ P(X=x_0)=1 \]

alors :

\[ H(X)=0 \]

Il n’y a aucune incertitude.

## 07.2 — Distribution uniforme

Si (X) possède (N) valeurs équiprobables :

\[ P(X=x)=1N \]

alors :

\[ H(X)=\_2 N \]

C’est l’entropie maximale pour une variable possédant (N) états.

# 08 — ENTROPIE BINAIRE

Pour :

\[ XBernoulli(p) \]

on obtient :

\[ H(X) = -p_2p

- (1-p)\_2(1-p) \]

On note souvent :

\[ H_b(p) = -p_2p-(1-p)\_2(1-p) \]

## 08.1 — Propriété importante

\[ H_b(0)=0 \]

\[ H_b(1)=0 \]

et :

\[ H_b()=1 \]

L’incertitude est maximale lorsque les deux résultats sont équiprobables.

# 09 — PROPRIÉTÉS FONDAMENTALES DE L’ENTROPIE

Pour une variable discrète :

\[ H(X) \]

Si (X) possède (N) états :

\[ H(X)\_2N \]

avec égalité lorsque la distribution est uniforme.

## 09.1 — Concavité

L’entropie est une fonction concave de la distribution.

Cette propriété est importante pour :

- l’optimisation ;
- la théorie des canaux ;
- l’apprentissage ;
- les preuves de maximalité ;
- les algorithmes d’optimisation de l’information.

# 10 — ENTROPIE JOINTE

Pour deux variables (X) et (Y) :

\[ H(X,Y) = -\_{x,y}p(x,y)p(x,y) \]

Elle mesure l’incertitude concernant le couple :

\[ (X,Y) \]

## 10.1 — Cas indépendant

Si :

\[ XY \]

alors :

\[ p(x,y)=p(x)p(y) \]

et :

\[ H(X,Y)=H(X)+H(Y) \]

## 10.2 — Cas dépendant

En général :

\[ H(X,Y)H(X)+H(Y) \]

La différence correspond à l’information partagée entre les variables.

# 11 — ENTROPIE CONDITIONNELLE

L’entropie conditionnelle mesure l’incertitude restante sur (X) lorsqu’on connaît (Y).

\[ H(X|Y) = -\_{x,y}p(x,y)p(x|y) \]

On peut aussi écrire :

\[ H(X|Y) = \_Y\[H(X|Y=y)\] \]

## 11.1 — Interprétation

Avant de connaître (Y) :

\[ H(X) \]

Après observation de (Y) :

\[ H(X|Y) \]

La connaissance de (Y) réduit donc généralement l’incertitude.

## 11.2 — Règle fondamentale

\[ H(X|Y)H(X) \]

# 12 — RÈGLE DE LA CHAÎNE

Une identité fondamentale :

\[ H(X,Y) = H(X)+H(Y|X) \]

ou :

\[ H(X,Y) = H(Y)+H(X|Y) \]

Pour plusieurs variables :

\[ H(X_1,,X_n) = _{i=1}^n H(X_i|X_1,,X_{i-1}) \]

Cette règle est fondamentale pour analyser les séquences et les sources avec mémoire.

# 13 — INFORMATION MUTUELLE

L’information mutuelle entre (X) et (Y) est :

\[ I(X;Y) = H(X)-H(X|Y) \]

Également :

\[ I(X;Y) = H(Y)-H(Y|X) \]

et :

\[ I(X;Y) = H(X)+H(Y)-H(X,Y) \]

Elle mesure :

**combien l’observation de (Y) réduit l’incertitude sur (X).**

# 14 — INTERPRÉTATION GÉNÉRALE DE L’INFORMATION MUTUELLE

Avant d’observer (Y) :

\[ H(X) \]

Après observation :

\[ H(X|Y) \]

La quantité d’information acquise est :

\[ H(X)-H(X|Y) \]

donc :

\[ I(X;Y) \]

## 14.1 — Symétrie

Contrairement à certaines formes conditionnelles :

\[ I(X;Y)=I(Y;X) \]

## 14.2 — Indépendance

Si (X) et (Y) sont indépendantes :

\[ I(X;Y)=0 \]

Inversement, pour des variables discrètes :

\[ I(X;Y)=0 XY \]

# 15 — INFORMATION MUTUELLE COMME DISTANCE À L’INDÉPENDANCE

On peut écrire :

\[ I(X;Y) = D_{KL} ( P_{XY} | P_XP_Y ) \]

Cette identité est extrêmement importante.

Elle signifie que l’information mutuelle mesure la différence entre :

- la vraie distribution jointe (P_{XY}) ;
- la distribution qu’on obtiendrait si (X) et (Y) étaient indépendantes.

Cela relie directement :

information mutuelle  
↓  
divergence KL  
↓  
distance conceptuelle entre distributions

MIT traite explicitement la divergence, l’information mutuelle et les propriétés de traitement de l’information dans son cursus avancé.

# 16 — DIVERGENCE KL

Pour deux distributions (P) et (Q) :

\[ D_{KL}(P|Q) = \_xP(x) \]

Elle est également appelée :

- divergence de Kullback-Leibler ;
- relative entropy ;
- divergence informationnelle.

# 17 — INTERPRÉTATION DE LA KL

La KL mesure le coût informationnel de l’utilisation de (Q) lorsqu’une distribution réelle est (P).

Une manière intuitive de la comprendre :

P = réalité statistique  
Q = modèle / approximation  
<br/>D_KL(P || Q)  
\=  
coût de représenter P avec Q

Elle intervient donc naturellement dans :

- statistiques ;
- machine learning ;
- génération ;
- approximation de distributions ;
- compression ;
- Bayesian inference ;
- optimisation.

# 18 — PROPRIÉTÉS DE LA KL

\[ D_{KL}(P|Q) \]

avec égalité si et seulement si :

\[ P=Q \]

presque partout.

Cette propriété est liée à l’inégalité de Gibbs.

## 18.1 — Attention : ce n’est pas une distance classique

En général :

\[ D_{KL}(P|Q) D_{KL}(Q|P) \]

La KL n’est donc pas symétrique.

Elle ne vérifie pas non plus nécessairement l’inégalité triangulaire.

Il est donc préférable de parler de **divergence** plutôt que de distance.

# 19 — CROSS-ENTROPY

La cross-entropy entre (P) et (Q) est :

\[ H(P,Q) = -\_xP(x)Q(x) \]

Elle vérifie :

\[ H(P,Q) = H(P)+D_{KL}(P|Q) \]

Cette identité est fondamentale en machine learning.

# 20 — CROSS-ENTROPY EN IA

Dans une classification multiclasses, si :

- (y) = distribution cible ;
- (y) = distribution prédite ;

la loss cross-entropy est :

\[ L = -\_i y_iy_i \]

Pour une cible one-hot :

\[ L=-y_k \]

où (k) est la classe correcte.

## 20.1 — Interprétation

Une prédiction correcte et confiante :

\[ y_k \]

donne une petite perte.

Une prédiction très confiante mais incorrecte :

\[ y_k \]

donne une perte importante.

La cross-entropy n’est donc pas une notion étrangère à la théorie de l’information : elle est directement reliée à la divergence KL.

# 21 — JENSEN-SHANNON DIVERGENCE

Une divergence symétrisée couramment utilisée :

\[ JS(P,Q) = 12D_{KL}(P|M)

- 12D_{KL}(Q|M) \]

avec :

\[ M= \]

Contrairement à la KL :

\[ JS(P,Q)=JS(Q,P) \]

Elle est utile notamment pour :

- comparer des distributions ;
- clustering ;
- génération ;
- GANs ;
- analyse de représentations.

# 22 — INFORMATION MUTUELLE CONDITIONNELLE

Pour trois variables :

\[ I(X;Y|Z) \]

mesure l’information mutuelle entre (X) et (Y) une fois (Z) connu.

Une forme :

\[ I(X;Y|Z) = H(X|Z)-H(X|Y,Z) \]

Cette notion devient essentielle dans :

- réseaux bayésiens ;
- causalité statistique ;
- sélection de variables ;
- analyse de dépendances ;
- apprentissage ;
- théorie de l’information multi-utilisateurs.

# 23 — DATA PROCESSING INEQUALITY

Considérons une chaîne de Markov :

\[ XYZ \]

Cela signifie intuitivement que (Z) obtient son information à partir de (Y), qui lui-même dépend de (X).

Alors :

\[ I(X;Z)I(X;Y) \]

Une transformation ultérieure ne peut pas créer de l’information supplémentaire sur (X) si elle n’a accès qu’à (Y).

MIT inclut explicitement le **data processing theorem** parmi les résultats fondamentaux du domaine.

## 23.1 — Interprétation informatique

Supposons :

IMAGE ORIGINALE  
↓  
REDIMENSIONNEMENT  
↓  
COMPRESSION  
↓  
FEATURES  
↓  
CLASSIFICATION

Si une transformation détruit une information utile, les étapes suivantes ne peuvent pas magiquement la récupérer à partir de cette représentation seule.

Cette idée est extrêmement importante pour :

- pipelines ML ;
- compression ;
- prétraitement ;
- feature engineering ;
- systèmes de vision ;
- NLP ;
- pipelines de données.

# 24 — INÉGALITÉ DE FANO

L’inégalité de Fano relie :

- l’erreur de prédiction ;
- l’entropie ;
- l’incertitude restante.

Elle fournit notamment des bornes inférieures sur l’erreur de classification.

De manière schématique :

\[ H(X|Y) h(P_e)+P_e(|X|-1) \]

où :

- (P_e) est la probabilité d’erreur ;
- (h) est l’entropie binaire.

Elle permet donc de relier une limite d’information à une limite de performance d’un système de prédiction.

# 25 — ENTROPIE DIFFÉRENTIELLE

Pour une variable continue ayant une densité (f(x)) :

\[ h(X) = -f(x)f(x),dx \]

Attention :

l’entropie différentielle n’a pas exactement les mêmes propriétés que l’entropie discrète.

Elle peut notamment être négative.

Il ne faut donc pas interpréter directement (h(X)) comme une quantité absolue de bits stockables.

# 26 — ENTROPIE ET DISTRIBUTIONS GAUSSIENNES

Parmi les distributions continues ayant une variance donnée, la distribution gaussienne maximise l’entropie différentielle.

Cette propriété explique en partie son importance dans :

- traitement du signal ;
- communications ;
- statistiques ;
- bruit ;
- canaux AWGN ;
- estimation.

# 27 — ENTROPIE DE PROCESSUS

Pour une séquence :

\[ X_1,X_2,,X_n \]

l’entropie totale est :

\[ H(X_1,,X_n) \]

Mais une notion encore plus importante pour une source séquentielle est le **taux d’entropie** :

\[ H_ = \_{n} 1nH(X_1,,X_n) \]

lorsque la limite existe.

## 27.1 — Pourquoi ?

Pour des données avec dépendances :

AAAAAAA...

est beaucoup plus prévisible que :

KQ7ZP2...

Même si chaque caractère utilise théoriquement le même alphabet.

La structure temporelle permet donc de réduire le nombre moyen de bits nécessaires.

# 28 — ENTROPIE DU LANGAGE

Le langage naturel possède énormément de structure :

- fréquence des mots ;
- syntaxe ;
- contexte ;
- dépendances ;
- répétitions ;
- redondance.

Shannon a notamment étudié la prédiction et l’entropie de l’anglais imprimé. Stanford référence son article de 1951 consacré à ce problème.

Cela permet de comprendre pourquoi :

texte brut

peut souvent être fortement compressé.

# 29 — PRINCIPE DE COMPRESSION

Une source contient généralement :

- information ;
- redondance ;
- structure ;
- régularités.

La compression cherche à exploiter ces régularités.

Conceptuellement :

DONNÉES  
↓  
ANALYSE DES PROBABILITÉS  
↓  
IDENTIFICATION DES RÉGULARITÉS  
↓  
REPRÉSENTATION PLUS COURTE

# 30 — COMPRESSION SANS PERTE

Une compression **lossless** doit permettre :

\[ D(E(x))=x \]

où :

- (E) = encodeur ;
- (D) = décodeur.

Aucune information n’est perdue.

Exemples :

- ZIP ;
- PNG ;
- FLAC ;
- certains algorithmes de compression de texte.

# 31 — COMPRESSION AVEC PERTE

Dans une compression **lossy** :

\[ D(E(x))x \]

mais on cherche :

\[ D(E(x))x \]

L’objectif devient alors :

conserver suffisamment d’information utile tout en réduisant fortement le coût de représentation.

Exemples :

- JPEG ;
- certaines compressions audio ;
- vidéo ;
- modèles compressés ;
- représentation latente.

# 32 — THÉORÈME DE CODAGE DE SOURCE

Le théorème de codage de source de Shannon établit une limite fondamentale :

pour une source suffisamment longue, il est possible de compresser presque jusqu’à son entropie moyenne par symbole, mais pas de façon fiable en dessous de cette limite dans le cadre classique sans perte.

Autrement dit, l’entropie représente une limite fondamentale de la compression sans perte.

Les cours MIT et Stanford structurent explicitement la théorie autour de cette relation entre entropie, compression et codage.

# 33 — LONGUEUR MOYENNE D’UN CODE

Pour un code dont le symbole (x_i) possède une longueur :

\[ l_i \]

la longueur moyenne est :

\[ L=\_i p_i l_i \]

Un bon code cherche à minimiser :

\[ L \]

tout en restant décodable sans ambiguïté.

# 34 — CODES À LONGUEUR FIXE

Si l’alphabet possède (N) symboles, un code fixe nécessite approximativement :

\[ \_2N \]

bits par symbole.

Mais cela ignore les probabilités.

Si certains symboles sont beaucoup plus fréquents que d’autres, on peut faire mieux en moyenne.

# 35 — CODES À LONGUEUR VARIABLE

On peut donner :

- des codes courts aux symboles fréquents ;
- des codes longs aux symboles rares.

Exemple conceptuel :

A → 0  
B → 10  
C → 110  
D → 111

Mais il faut garantir que la séquence puisse être décodée sans ambiguïté.

# 36 — CODES PRÉFIXES

Un code est préfixe si aucun mot de code n’est le préfixe d’un autre.

Exemple :

A → 0  
B → 10  
C → 110  
D → 111

est préfixe.

Cela permet un décodage immédiat :

0 → A  
10 → B  
110 → C  
111 → D

# 37 — INÉGALITÉ DE KRAFT-MCMILLAN

Pour un code préfixe binaire :

\[ \_i2^{-l_i} \]

Cette condition caractérise les longueurs compatibles avec un code préfixe.

Elle constitue un pont fondamental entre :

probabilités  
+  
longueurs de code  
+  
structure arborescente

MIT et Stanford incluent explicitement Kraft-McMillan dans l’étude de la compression et des codes optimaux.

# 38 — CODE DE SHANNON

Une construction historique consiste à choisir des longueurs proches de :

\[ l_i-\_2p_i \]

L’idée est fondamentale :

plus un symbole est improbable, plus il faut de bits pour le représenter efficacement.

# 39 — CODE DE HUFFMAN

L’algorithme de Huffman construit un code préfixe optimal pour minimiser la longueur moyenne dans le cadre considéré.

Principe :

1.  trier les probabilités ;
2.  prendre les deux plus faibles ;
3.  les fusionner ;
4.  répéter ;
5.  reconstruire l’arbre ;
6.  attribuer les bits.

Structure :

probabilités  
↓  
fusion des plus faibles  
↓  
arbre binaire  
↓  
codes préfixes

Le programme MIT de théorie de l’information consacre explicitement des séances au codage de Huffman.

# 40 — COMPLEXITÉ DE HUFFMAN

Avec une file de priorité, une implémentation classique obtient typiquement :

\[ O(nn) \]

pour (n) symboles.

# 41 — CODAGE ARITHMÉTIQUE

Au lieu d’attribuer un mot binaire entier à chaque symbole, le codage arithmétique représente une séquence entière par un intervalle numérique.

Conceptuellement :

\[0,1)  
↓  
partition selon les probabilités  
↓  
symbole 1  
↓  
sous-intervalle  
↓  
symbole 2  
↓  
sous-intervalle plus petit  
↓  
...

Plus la séquence est probable, plus l’intervalle final peut être représenté efficacement.

# 42 — ENTROPY CODING

Les méthodes de codage entropique cherchent à rapprocher :

\[ \]

de :

\[ \]

Parmi les grandes familles :

- Huffman ;
- codage arithmétique ;
- Shannon-Fano ;
- ANS ;
- codage contextuel.

Le choix dépend du compromis entre :

- ratio ;
- vitesse ;
- mémoire ;
- complexité ;
- parallélisation.

# 43 — COMPRESSION UNIVERSELLE

Dans de nombreux systèmes, la vraie distribution de la source n’est pas connue.

Il faut donc apprendre ou estimer les régularités.

Cela conduit à :

- Lempel-Ziv ;
- modèles contextuels ;
- prédiction ;
- dictionnaires ;
- compression adaptative.

Les cours Stanford distinguent explicitement les taux d’entropie et la compression universelle.

# 44 — MODÈLES CONTEXTUELS

Pour une séquence :

A B A B A B A ...

prédire un symbole à partir du contexte peut fortement améliorer la compression.

Le modèle cherche :

\[ P(X_t|X_{t-1},X_{t-2},) \]

Le contexte réduit l’incertitude.

Cette idée est directement reliée au langage et aux modèles de langage modernes.

# 45 — NLP ET ENTROPIE

Dans le NLP, un modèle estime :

\[ P(w_t|w_1,,w_{t-1}) \]

La surprise d’un token est :

\[ -\_2P(w_t|context) \]

La somme des surprises donne une mesure du coût informationnel de la séquence.

# 46 — PERPLEXITÉ

La perplexité est liée à l’entropie moyenne.

Pour une séquence de (N) tokens :

\[ H = -1N \_{i=1}^{N} \_2P(w_i|context_i) \]

La perplexité peut être définie :

\[ PP=2^H \]

ou avec les logarithmes naturels :

\[ PP=e^H \]

selon la convention.

## 46.1 — Interprétation

Une perplexité plus faible signifie généralement que le modèle attribue davantage de probabilité aux événements observés.

Mais :

une perplexité basse ne signifie pas automatiquement qu’un système est meilleur sur toutes les tâches.

Elle mesure une propriété probabiliste spécifique.

# 47 — THÉORÈME AEP

L’**Asymptotic Equipartition Property** est l’une des idées fondamentales de la théorie de l’information.

Pour de longues séquences issues d’une source appropriée, les séquences typiques ont approximativement :

\[ 2^{nH(X)} \]

possibilités.

Chaque séquence typique possède une probabilité approximative :

\[ 2^{-nH(X)} \]

C’est une intuition centrale expliquant pourquoi l’entropie apparaît comme limite de compression.

MIT inclut explicitement l’AEP et les ensembles typiques dans son cursus.

# 48 — ENSEMBLE TYPIQUE

Pour une longue séquence :

\[ X^n=(X_1,,X_n) \]

les séquences typiques sont celles dont le comportement statistique est proche de celui attendu.

Conceptuellement :

toutes les séquences  
↓  
séquences improbables  
↓  
séquences typiques  
↓  
≈ 2^(nH) séquences

Cette idée est essentielle dans les preuves des théorèmes de codage.

# 49 — COMMUNICATION

Considérons :

MESSAGE  
↓  
ENCODEUR  
↓  
CANAL  
↓  
DÉCODEUR  
↓  
MESSAGE RECONSTRUIT

Le canal peut introduire :

- bruit ;
- erreurs ;
- pertes ;
- interférences ;
- distorsion.

La théorie de l’information cherche alors à répondre :

Jusqu’à quel débit peut-on communiquer de manière fiable ?

# 50 — CANAL

Un canal discret peut être représenté par :

\[ P(Y|X) \]

où :

- (X) = entrée ;
- (Y) = sortie.

Le canal est donc une transformation probabiliste :

\[ XY \]

# 51 — INFORMATION TRANSMISE

Une mesure naturelle de la quantité d’information transmise par le canal est :

\[ I(X;Y) \]

Elle mesure combien la sortie (Y) renseigne sur l’entrée (X).

# 52 — CAPACITÉ DU CANAL

La capacité d’un canal est :

\[ C = \_{P_X}I(X;Y) \]

Elle représente le débit maximal théorique auquel une communication fiable peut être obtenue dans le modèle considéré.

Stanford présente explicitement la capacité comme le maximum de l’information mutuelle sur la distribution d’entrée.

# 53 — THÉORÈME DE CODAGE DE CANAL DE SHANNON

L’idée fondamentale est :

\[ R<C \]

permet une communication fiable asymptotiquement avec des codes appropriés.

Alors que :

\[ R>C \]

ne permet pas une communication fiable dans le modèle classique.

Stanford résume ce résultat comme l’existence d’une limite (C) telle qu’en dessous de la capacité l’erreur peut être rendue arbitrairement petite, tandis qu’au-dessus elle devient inévitable.

# 54 — CAPACITÉ ET REDONDANCE

Cela conduit à une idée fondamentale :

la redondance n’est pas nécessairement du gaspillage.

Elle peut être utilisée pour :

- détecter des erreurs ;
- corriger des erreurs ;
- rendre une transmission fiable.

La théorie des codes exploite précisément cette redondance.

# 55 — CANAL BINAIRE SYMÉTRIQUE

Un canal BSC introduit une probabilité (p) d’inversion :

\[ 0 \]

avec probabilité (p), et :

\[ 1 \]

avec probabilité (p).

Sa capacité est :

\[ C=1-H_b(p) \]

pour un canal binaire symétrique.

# 56 — CANAL D’EFFACEMENT

Dans un Binary Erasure Channel, un symbole peut être remplacé par :

\[ ? \]

La capacité est :

\[ C=1- \]

pour une probabilité d’effacement (), dans le modèle binaire standard.

# 57 — CANAL AWGN

Le canal gaussien avec bruit additif est modélisé par :

\[ Y=X+N \]

où :

\[ NN(0,^2) \]

Sous une contrainte de puissance (P), la capacité classique est :

\[ C = \_2 ( 1+ ) \]

par utilisation réelle du canal, selon la normalisation retenue.

Pour une bande passante (B), une forme classique de Shannon-Hartley est :

\[ C = B_2 ( 1+ ) \]

# 58 — RAPPORT SIGNAL/BRUIT

Le rapport :

\[ SNR= \]

influence directement la capacité.

Augmenter le SNR permet généralement d’augmenter le débit théorique maximal.

Cela crée une relation fondamentale entre :

puissance  
+  
bruit  
+  
bande passante  
+  
débit

# 59 — CODES CORRECTEURS D’ERREURS

La théorie de l’information a conduit au développement d’importantes familles de codes :

- codes de Hamming ;
- codes cycliques ;
- codes convolutifs ;
- Turbo codes ;
- LDPC ;
- codes polaires ;
- codes Reed-Solomon.

Ils ajoutent une structure redondante permettant au récepteur de détecter ou corriger certaines erreurs.

Stanford présente notamment les codes polaires et la théorie du codage de canal dans ses cursus d’information theory.

# 60 — DÉTECTION VS CORRECTION

Deux objectifs différents :

### Détection

Identifier :

quelque chose est probablement incorrect.

### Correction

Déterminer :

quelle était probablement la valeur originale ?

Cette distinction est fondamentale en stockage et transmission.

# 61 — STOCKAGE

La théorie de l’information intervient dans :

- disques ;
- SSD ;
- mémoire ;
- stockage distribué ;
- RAID ;
- codes d’effacement ;
- correction d’erreurs ;
- systèmes de sauvegarde.

L’objectif est souvent :

capacité  
+  
fiabilité  
+  
résilience

# 62 — CODES D’EFFACEMENT

Dans les systèmes distribués, au lieu de simplement dupliquer les données :

A  
A  
A

on peut construire des fragments redondants :

Données  
↓  
fragments  
↓  
parité / codage  
↓  
stockage distribué

La perte d’une partie des fragments peut alors être tolérée.

Cela rapproche la théorie de l’information de :

- cloud ;
- stockage distribué ;
- systèmes tolérants aux pannes.

# 63 — COMPRESSION ET STOCKAGE

La quantité brute de bits n’est pas nécessairement la quantité minimale de bits.

Si :

\[ H(X)\_2|X| \]

alors la source contient beaucoup de structure exploitable.

La compression cherche précisément à exploiter cette différence.

# 64 — THÉORIE DÉBIT-DISTORSION

La compression avec perte introduit un nouveau compromis :

\[ \]

On définit une fonction :

\[ R(D) \]

où :

- (R) = débit nécessaire ;
- (D) = distorsion autorisée.

La théorie débit-distorsion cherche le plus petit débit nécessaire pour atteindre une distorsion donnée. Stanford présente (R(D)) comme la limite fondamentale de la compression avec perte.

# 65 — FONCTION DE DISTORSION

On définit une mesure :

\[ d(x,x) \]

Exemples :

\[ d(x,x)=|x-x| \]

ou :

\[ d(x,x)=(x-x)^2 \]

Pour des images, on peut utiliser des métriques plus perceptuelles.

# 66 — PROBLÈME GÉNÉRAL

Le problème devient :

\[ \]

sous :

\[ E\[d(X,X)\]D \]

La formulation fondamentale de la théorie est :

\[ R(D) = _{P_{X|X}:,E\[d(X,X)\]D} I(X;X) \]

# 67 — COMPRESSION ET IA GÉNÉRATIVE

Les représentations latentes peuvent être interprétées comme des tentatives de transformer :

données haute dimension  
↓  
représentation compacte  
↓  
reconstruction / génération

La théorie débit-distorsion fournit une manière conceptuelle d’analyser le compromis :

taille de représentation  
↕  
fidélité

Cette connexion devient particulièrement intéressante pour :

- autoencodeurs ;
- VAE ;
- compression neuronale ;
- image generation ;
- speech coding ;
- learned compression.

# 68 — INFORMATION BOTTLENECK

Le principe de l’**Information Bottleneck** cherche une représentation (T) qui :

- conserve l’information pertinente pour (Y) ;
- élimine autant que possible l’information non pertinente provenant de (X).

Une formulation classique :

\[ I(X;T)-I(T;Y) \]

On cherche donc un compromis entre :

\[ X \]

et :

\[ Y. \]

Des travaux associés au cadre Information Bottleneck formalisent précisément cette tension entre compression de (X) et conservation d’information sur (Y).

# 69 — INFORMATION BOTTLENECK EN MACHINE LEARNING

Conceptuellement :

X = données brutes  
↓  
T = représentation  
↓  
Y = tâche cible

On cherche :

\[ T \]

tel que :

\[ I(T;Y) \]

soit élevé, mais :

\[ I(X;T) \]

reste contrôlé.

Cela peut inspirer :

- feature learning ;
- représentation compacte ;
- réduction de dimension ;
- robustesse ;
- regularisation ;
- apprentissage multimodal.

# 70 — ARBRES DE DÉCISION

La théorie de l’information intervient directement dans les arbres de décision.

Pour un attribut (A), le gain d’information peut être écrit :

\[ IG(Y,A) = H(Y)-H(Y|A) \]

On choisit donc un attribut qui réduit fortement l’incertitude sur la variable cible.

ID3 utilise précisément le gain d’information pour sélectionner les variables lors de la construction de l’arbre.

# 71 — EXEMPLE D’ARBRE

Supposons :

Acheter ?  
↑  
revenu  
âge  
profession  
historique

L’entropie initiale mesure l’incertitude sur :

\[ Y= \]

Pour chaque variable :

\[ IG(Y,A) \]

mesure combien l’incertitude diminue.

La meilleure variable peut devenir le prochain nœud.

# 72 — LIMITES DU GAIN D’INFORMATION

Le gain d’information peut favoriser les variables possédant beaucoup de modalités.

C’est notamment une motivation derrière le **gain ratio** dans certaines variantes comme C4.5.

Il faut donc comprendre :

une métrique informationnelle est un outil de décision, pas une vérité absolue indépendante du problème.

# 73 — INFORMATION ET SÉLECTION DE VARIABLES

Une variable (X_i) peut être évaluée par :

\[ I(X_i;Y) \]

Une grande valeur peut indiquer que (X_i) contient beaucoup d’information sur (Y).

Mais sélectionner chaque variable uniquement selon :

\[ I(X_i;Y) \]

peut conduire à des redondances.

Deux variables peuvent chacune être fortement informatives tout en portant presque la même information.

Il faut donc parfois analyser :

\[ I(X_i;X_j) \]

et :

\[ I(X_i;Y|X_j) \]

# 74 — REDONDANCE

Une représentation peut contenir :

- information pertinente ;
- information redondante ;
- bruit ;
- information inutile pour la tâche.

On peut donc penser :

DATA  
├── signal utile  
├── redondance  
├── bruit  
└── information hors tâche

L’un des grands intérêts de la théorie de l’information en IA est précisément de formaliser certains de ces concepts.

# 75 — IA ET DIVERGENCE KL

La KL intervient dans :

- variational inference ;
- VAEs ;
- distillation ;
- Bayesian learning ;
- calibration ;
- comparaison de distributions ;
- génération probabiliste.

Dans un VAE, par exemple, une composante classique de l’objectif est une divergence entre une distribution latente approximative et un prior.

# 76 — DISTILLATION

Un modèle enseignant produit :

\[ P_T(y|x) \]

et le modèle étudiant :

\[ P_S(y|x) \]

On peut chercher à rapprocher :

\[ P_S \]

de :

\[ P_T \]

par une divergence telle que :

\[ D_{KL}(P_T|P_S) \]

La théorie de l’information devient alors un langage pour transférer une distribution de connaissances.

# 77 — NLP : INFORMATION CONTEXTUELLE

Dans le langage :

\[ I(X;Y) \]

peut mesurer une dépendance statistique entre :

- tokens ;
- mots ;
- caractères ;
- documents ;
- labels ;
- représentations.

Des concepts informationnels permettent ainsi d’étudier :

- dépendances lexicales ;
- sélection de features ;
- représentations ;
- prédictibilité ;
- compression du langage.

# 78 — MODÈLES DE LANGAGE ET COMPRESSION

Un modèle de langage performant attribue de fortes probabilités aux séquences plausibles.

Donc :

\[ -P(x) \]

peut être interprété comme un coût de description probabiliste.

Cela crée une connexion profonde :

prédiction  
↔  
compression  
↔  
modélisation probabiliste

Un meilleur modèle probabiliste peut donc souvent conduire à une meilleure compression théorique de la source.

# 79 — MDL — MINIMUM DESCRIPTION LENGTH

Le principe MDL propose de choisir un modèle en minimisant :

\[ L()

- L() \]

Autrement dit :

coût de décrire le modèle  
+  
coût de décrire les données avec le modèle

Le principe est directement lié aux idées de codage et de théorie de l’information. Stanford décrit explicitement MDL comme la minimisation de la longueur combinée de description du modèle et des données encodées avec ce modèle.

# 80 — MDL ET APPRENTISSAGE

Un modèle trop simple :

modèle court  
+  
données difficiles à expliquer

Un modèle trop complexe :

modèle coûteux  
+  
données faciles à expliquer

MDL cherche un compromis :

\[

- \]

Cela fournit une intuition informationnelle de la généralisation.

# 81 — BAYES ET INFORMATION

La théorie de l’information est fortement liée à Bayes.

On peut notamment écrire :

\[ P(H|D) = P(D|H)

- P(H)
- P(D) \]

Les termes logarithmiques transforment les produits en sommes.

Cela permet de raisonner en termes de :

- gain d’information ;
- surprise ;
- coût de description ;
- vraisemblance ;
- complexité.

# 82 — INFORMATION ET CRYPTOGRAPHIE

La cryptographie cherche notamment à empêcher un adversaire d’apprendre une information sensible.

La théorie de l’information permet de formaliser cette question.

On peut étudier :

\[ I(M;C) \]

où :

- (M) = message secret ;
- (C) = texte chiffré.

Si :

\[ I(M;C)=0 \]

alors le texte chiffré ne révèle, dans ce modèle probabiliste, aucune information sur le message.

# 83 — SECRET PARFAIT

Le concept de **perfect secrecy** de Shannon peut être exprimé par :

\[ P(M|C)=P(M) \]

ou de manière équivalente :

\[ I(M;C)=0 \]

Le one-time pad est l’exemple classique associé à cette propriété dans le modèle approprié. Shannon a formalisé mathématiquement cette notion de sécurité parfaite.

# 84 — IMPORTANT : INFORMATION THÉORIQUE ≠ CRYPTOGRAPHIE MODERNE ENTIÈRE

Il faut distinguer :

### Sécurité informationnelle

La sécurité reste valable même avec des ressources de calcul illimitées, dans le modèle considéré.

### Sécurité computationnelle

La sécurité repose sur l’hypothèse qu’un adversaire ne peut pas résoudre efficacement certains problèmes.

La cryptographie moderne utilise largement la seconde approche.

La théorie de l’information fournit néanmoins des bornes et des concepts fondamentaux.

# 85 — RÉSEAUX

Dans un réseau, on peut étudier :

- capacité ;
- débit ;
- bruit ;
- perte ;
- congestion ;
- codage ;
- redondance ;
- information transmise.

Une abstraction :

SOURCE  
↓  
ENCODEUR  
↓  
RÉSEAU  
↓  
BRUIT / PERTES  
↓  
DÉCODEUR  
↓  
DESTINATION

# 86 — COMMUNICATION NUMÉRIQUE

Une chaîne de communication peut être décomposée :

Application  
↓  
Encodage  
↓  
Compression  
↓  
Codage correcteur  
↓  
Modulation  
↓  
Canal  
↓  
Démodulation  
↓  
Décodage  
↓  
Décompression  
↓  
Application

La théorie de l’information fournit une partie du cadre permettant d’étudier les limites de cette chaîne.

# 87 — STOCKAGE DISTRIBUÉ

Les données peuvent être représentées comme :

\[ D (C_1,C_2,,C_n) \]

avec des fragments redondants.

Si certains fragments disparaissent :

\[ C_i= \]

la structure du code peut permettre de reconstruire (D).

Cette idée relie :

- théorie de l’information ;
- algèbre ;
- systèmes distribués ;
- tolérance aux pannes.

# 88 — INFORMATION ET SYSTÈMES DISTRIBUÉS

Dans un système distribué, une question centrale est :

quelle information chaque nœud possède-t-il ?

On peut alors raisonner sur :

- information locale ;
- information globale ;
- communication nécessaire ;
- incertitude ;
- synchronisation ;
- consensus.

La théorie de l’information peut donc servir de langage conceptuel pour analyser le coût de coordination.

# 89 — INFORMATION ET SYSTÈMES MULTI-AGENTS

Considérons plusieurs agents :

Agent A  
↘  
environnement  
↗  
Agent B

Chaque agent possède une observation partielle.

On peut alors étudier :

\[ I(O_A;S) \]

ou :

\[ I(O_A;O_B) \]

pour analyser :

- ce que chaque agent sait ;
- ce que les agents partagent ;
- ce qu’une communication supplémentaire apporte ;
- quelle information est redondante.

# 90 — APPRENTISSAGE PAR RENFORCEMENT

L’information peut intervenir dans :

- exploration ;
- incertitude ;
- représentation d’état ;
- information gain ;
- empowerment ;
- politiques à entropie maximale.

Une politique peut par exemple chercher à maximiser une entropie :

\[ H((|s)) \]

afin d’encourager l’exploration.

Des travaux récents relient explicitement théorie de l’information, exploration, représentation et reinforcement learning.

# 91 — INFORMATION GAIN EN EXPLORATION

Si un agent doit choisir une observation (A), on peut chercher à maximiser :

\[ I(S;O|A) \]

où :

- (S) = état inconnu ;
- (O) = observation future ;
- (A) = action.

L’action la plus intéressante est alors celle qui réduit le plus l’incertitude.

Cela donne une stratégie :

**agir pour apprendre.**

# 92 — INFORMATION ET ACTIVE LEARNING

En active learning, le système choisit les exemples à faire annoter.

Au lieu de demander :

donne-moi n'importe quelles données

il peut chercher :

quelles données réduiraient le plus mon incertitude ?

Une formulation possible repose sur :

\[ I(Y;X) \]

ou des variantes conditionnelles.

# 93 — INFORMATION ET SENSOR FUSION

Plusieurs capteurs peuvent produire :

\[ X_1,X_2,,X_n \]

On cherche à combiner les observations.

La théorie de l’information permet d’étudier :

- information complémentaire ;
- redondance ;
- dépendance ;
- incertitude résiduelle.

Applications :

- robotique ;
- IoT ;
- vision ;
- véhicules autonomes ;
- systèmes industriels.

# 94 — INFORMATION ET ANOMALIE

Un événement très improbable possède une forte surprise :

\[ I(x)=-P(x) \]

Cela peut servir à construire des scores d’anomalie.

Si :

\[ P(x) \]

alors :

\[ -P(x) \]

est élevé.

Cela ne signifie toutefois pas automatiquement que l’observation est une anomalie : la qualité du modèle probabiliste reste déterminante.

# 95 — INFORMATION ET DÉTECTION

Une observation peut être comparée à un modèle :

\[ D_{KL}(P|Q) \]

ou évaluée via :

\[ -P(x) \]

Cela permet de construire des systèmes de :

- détection de changement ;
- monitoring ;
- détection de dérive ;
- surveillance ;
- analyse de distribution.

# 96 — DISTRIBUTION SHIFT

Si :

\[ P_{train}(X) \]

diffère fortement de :

\[ P_{production}(X) \]

le système peut se comporter différemment.

La divergence entre distributions peut fournir un signal :

\[ D_{KL}(P_{production}|P_{train}) \]

ou d’autres mesures comme Jensen-Shannon.

# 97 — THÉORIE DE L’INFORMATION ET IA : VISION GLOBALE

On peut résumer les principales connexions :

ENTROPIE  
↓  
incertitude  
<br/>INFORMATION MUTUELLE  
↓  
dépendance  
<br/>KL  
↓  
différence entre distributions  
<br/>CROSS-ENTROPY  
↓  
qualité d'une distribution prédictive  
<br/>COMPRESSION  
↓  
représentation efficace  
<br/>DÉBIT-DISTORSION  
↓  
compromis taille / fidélité  
<br/>CAPACITÉ  
↓  
limite de transmission  
<br/>INFORMATION BOTTLENECK  
↓  
représentation pertinente  
<br/>MDL  
↓  
complexité / description  
<br/>FANO  
↓  
limites de prédiction

# 98 — DIFFÉRENCE ENTRE ENTROPIE, KL ET INFORMATION MUTUELLE

Il est essentiel de ne pas les confondre.

| Concept | Question |
| --- | --- |
| Entropie | Combien d’incertitude contient (X) ? |
| Entropie conditionnelle | Combien reste-t-il d’incertitude sur (X) après (Y) ? |
| Information mutuelle | Combien (X) et (Y) savent-ils l’un sur l’autre ? |
| KL  | À quel point (P) diffère-t-elle de (Q) ? |
| Cross-entropy | Quel coût moyen obtient-on en utilisant (Q) pour représenter (P) ? |
| Capacité | Combien d’information peut passer de manière fiable ? |
| Débit-distorsion | Combien de bits faut-il pour une qualité donnée ? |

# 99 — DIFFÉRENCE ENTRE INFORMATION ET DONNÉE

Une donnée :

"Paris"

est une représentation.

L’information dépend du contexte probabiliste.

Si l’événement est extrêmement prévisible, sa surprise peut être faible.

Si l’événement était improbable, sa réalisation peut apporter davantage d’information.

Il faut donc éviter :

donnée = information.

# 100 — INFORMATION ET CONTEXTE

La quantité d’information peut dépendre de ce qui est déjà connu.

Exemple :

X = météo demain

Si l’on sait déjà avec certitude :

X = pluie

une nouvelle observation confirmant la pluie apporte peu d’information.

Si toutes les issues étaient possibles, elle peut apporter beaucoup plus.

C’est exactement pourquoi l’entropie conditionnelle est importante.

# 101 — INFORMATION REDONDANTE

Supposons :

\[ Y=X \]

Alors :

\[ I(X;Y)=H(X) \]

Y contient toute l’information de X.

Mais si :

\[ Y \]

est une copie parfaite de (X), cette information est redondante du point de vue d’un système qui possède déjà (X).

La théorie de l’information permet donc de distinguer :

information disponible

de :

information nouvelle

# 102 — INFORMATION COMPLÉMENTAIRE

Deux variables peuvent chacune apporter une information différente :

\[ I(X;Y) \]

peut être faible alors que :

\[ I(X;Y|Z) \]

est important dans certains systèmes complexes.

Cette distinction est utile pour comprendre les interactions entre features.

# 103 — LIMITES DE L’INTERPRÉTATION

La théorie de l’information est puissante, mais ses mesures doivent être interprétées dans leur contexte.

Une forte information mutuelle ne signifie pas nécessairement :

- causalité ;
- utilité opérationnelle ;
- robustesse ;
- absence de biais.

De même :

\[ I(X;Y)>0 \]

signifie dépendance statistique, pas causalité.

# 104 — CAUSALITÉ ≠ INFORMATION MUTUELLE

Supposons :

\[ XZY \]

Alors (X) et (Y) peuvent être fortement dépendants.

Mais cela ne signifie pas :

\[ XY \]

La théorie de l’information mesure certaines dépendances.

La causalité nécessite un cadre supplémentaire.

# 105 — INFORMATION ET ALGORITHMES

Lorsqu’on utilise ce domaine dans un logiciel, il faut généralement suivre :

1\. définir les variables  
2\. définir les distributions  
3\. estimer les probabilités  
4\. choisir la mesure informationnelle  
5\. calculer  
6\. interpréter  
7\. tester la sensibilité  
8\. intégrer dans la décision

# 106 — ESTIMATION DE L’ENTROPIE

Dans les données réelles, les probabilités sont rarement connues exactement.

On estime :

\[ p(x) \]

puis :

\[ H(X) = -\_xp(x)p(x) \]

Cela introduit une erreur d’estimation.

# 107 — PROBLÈME DES DONNÉES RARES

Si un alphabet possède énormément de valeurs mais peu d’observations :

nombre de modalités  
≫  
nombre d'observations

les estimations naïves deviennent fragiles.

Cela concerne particulièrement :

- NLP ;
- génomique ;
- données catégorielles ;
- événements rares ;
- haute dimension.

# 108 — ZÉROS DE PROBABILITÉ

Avec :

\[ D_{KL}(P|Q) \]

si :

\[ P(x)>0 \]

mais :

\[ Q(x)=0 \]

alors :

\[ D_{KL}(P|Q)=+ \]

dans le cas discret.

En pratique, cela impose de traiter soigneusement :

- smoothing ;
- estimation ;
- régularisation ;
- support des distributions.

# 109 — LISSAGE

Pour éviter les probabilités nulles dans certains modèles de comptage, on peut utiliser :

- Laplace smoothing ;
- add-(k) smoothing ;
- modèles hiérarchiques ;
- priors bayésiens.

Exemple :

\[ p_i = {N+K} \]

pour un alphabet de taille (K).

# 110 — COMPLEXITÉ DE CALCUL

Pour (K) catégories, un calcul direct d’entropie peut coûter :

\[ O(K) \]

Une matrice jointe (P(X,Y)) peut coûter :

\[ O(K_XK_Y) \]

Une estimation naïve de nombreuses informations mutuelles peut donc devenir coûteuse.

Pour de grandes dimensions :

- approximation ;
- échantillonnage ;
- hashing ;
- discrétisation ;
- estimateurs neuronaux ;
- méthodes variationnelles

peuvent devenir nécessaires.

# 111 — INFORMATION MUTUELLE EN HAUTE DIMENSION

Estimer :

\[ I(X;Y) \]

pour des variables continues et de haute dimension est difficile.

On peut utiliser :

- estimateurs par voisinage ;
- bornes variationnelles ;
- modèles probabilistes ;
- méthodes de classification ;
- approches neuronales ;
- contrastive learning.

La théorie devient alors un pont entre mathématiques et ingénierie statistique.

# 112 — INFORMATION CONTRASTIVE

De nombreuses méthodes modernes de représentation cherchent à :

- rapprocher les représentations positives ;
- éloigner les négatives ;
- maximiser une quantité d’information utile.

Cela crée des connexions avec :

- mutual information ;
- contrastive learning ;
- embeddings ;
- représentation multimodale.

# 113 — IA MULTIMODALE

Supposons :

IMAGE  
↓  
représentation visuelle  
↓  
┐  
├── ALIGNEMENT  
┘  
↓  
TEXTE

On peut étudier les relations entre les représentations :

\[ I(Z_{image};Z_{text}) \]

ou des objectifs apparentés.

Cela aide à formaliser l’idée de représentation partagée.

# 114 — GÉNÉRATION

Dans un modèle génératif :

\[ P(X) \]

représente une distribution sur les données.

La surprise :

\[ -P(X) \]

mesure le coût informationnel d’une observation selon le modèle.

Une bonne modélisation probabiliste implique donc souvent une bonne capacité à attribuer des probabilités pertinentes aux observations.

# 115 — COMPRESSION NEURONALE

Une architecture peut apprendre :

X  
↓  
encodeur  
↓  
Z  
↓  
décodeur  
↓  
X̂

On peut analyser :

- dimension de (Z) ;
- information conservée ;
- reconstruction ;
- distorsion ;
- coût de stockage.

Cela rapproche :

autoencodeurs  
+  
théorie débit-distorsion  
+  
Information Bottleneck

# 116 — INFORMATION ET TRANSFORMERS

Dans un modèle séquentiel :

tokens  
↓  
embeddings  
↓  
attention  
↓  
représentations  
↓  
prédiction

les mécanismes d’attention peuvent être analysés comme des transformations d’information.

Attention :

il ne faut pas conclure automatiquement qu’une matrice d’attention constitue une mesure directe et complète de l’information ou de l’importance causale.

L’interprétation demande une analyse spécifique.

# 117 — INFORMATION ET SYSTÈMES DE RECOMMANDATION

On peut étudier :

\[ I(User;Item) \]

ou :

\[ I(User;Preference|Context) \]

pour comprendre quelles variables fournissent de l’information sur une préférence.

Cela peut aider à :

- sélectionner des features ;
- construire des systèmes de recommandation ;
- analyser des interactions ;
- mesurer la valeur de nouvelles observations.

# 118 — INFORMATION ET CYBERSÉCURITÉ

Applications :

- confidentialité ;
- détection d’anomalies ;
- fingerprinting ;
- analyse de trafic ;
- estimation d’entropie de secrets ;
- analyse de mots de passe ;
- génération aléatoire ;
- side-channel analysis.

# 119 — ENTROPIE DES MOTS DE PASSE

Un espace de recherche de taille (N) fournit au maximum :

\[ \_2N \]

bits d’incertitude si les possibilités sont équiprobables.

Mais un mot de passe humain n’est généralement pas uniforme.

Un mot de passe prévisible peut donc avoir une entropie effective bien inférieure à sa longueur apparente.

Ainsi :

longueur ≠ entropie réelle.

# 120 — INFORMATION ET ALÉATOIRE

Un générateur doit être analysé selon son modèle.

Un système peut produire des valeurs qui semblent aléatoires sans posséder une bonne imprévisibilité cryptographique.

La théorie de l’information peut mesurer certaines propriétés statistiques, mais :

entropie statistique élevée ≠ sécurité cryptographique garantie.

# 121 — INFORMATION ET WEB

Applications :

- compression HTTP ;
- cache ;
- optimisation des assets ;
- transmission vidéo ;
- streaming ;
- images ;
- CDN ;
- protocoles réseau ;
- réduction de bande passante.

# 122 — INFORMATION ET PERFORMANCE

Un fichier :

\[ 10,MB \]

n’est pas nécessairement incompressible.

Une forte redondance peut permettre :

\[ 10,MB,MB \]

sans perte, selon la structure des données.

La performance réseau peut donc être améliorée par la compréhension de la structure informationnelle.

# 123 — INFORMATION ET BASES DE DONNÉES

Applications possibles :

- compression de colonnes ;
- encodage ;
- dictionnaires ;
- bitmap encoding ;
- cardinalité ;
- statistiques de données ;
- estimation ;
- stockage.

La distribution des valeurs influence directement l’efficacité de certaines représentations.

# 124 — INFORMATION ET OBSERVABILITÉ

Dans un système logiciel, les logs sont eux-mêmes des données.

On peut chercher :

Quels événements apportent réellement de l'information ?

au lieu de stocker tout indistinctement.

Cela peut conduire à :

- logs adaptatifs ;
- compression intelligente ;
- échantillonnage ;
- détection d’événements rares ;
- observabilité orientée information.

# 125 — INFORMATION ET MONITORING

Supposons une métrique :

\[ X_t \]

On peut rechercher :

\[ -P(X_t) \]

comme score de surprise.

Une évolution de :

\[ P_t(X) \]

peut également être comparée à :

\[ P_{t-1}(X) \]

par une divergence.

On obtient alors une architecture de détection de dérive :

flux  
↓  
distribution courante  
↓  
comparaison  
↓  
divergence  
↓  
alerte

# 126 — INFORMATION ET UX

Même une interface utilisateur peut être étudiée sous l’angle informationnel.

Questions :

- quelle information l’utilisateur cherche-t-il ?
- quelle information possède-t-il déjà ?
- quelle information manque-t-il ?
- quelle interaction réduit le plus son incertitude ?
- quelle interface produit trop de bruit informationnel ?

On peut conceptualiser :

INCERTITUDE UTILISATEUR  
↓  
INTERACTION  
↓  
INFORMATION  
↓  
DÉCISION

# 127 — DESIGN INFORMATIONNEL

Une bonne interface peut être considérée comme une machine à réduire l’incertitude pertinente.

Exemple :

"Le paiement a-t-il fonctionné ?"

Une bonne interface répond clairement :

PAIEMENT CONFIRMÉ  
Référence : XXXX  
Montant : ...  
Date : ...

L’objectif n’est pas de maximiser l’information affichée.

Il est de maximiser :

**l’information utile par unité de complexité cognitive.**

# 128 — INFORMATION ET ANIMATION

Une animation peut communiquer un changement d’état :

ACTION  
↓  
TRANSITION  
↓  
NOUVEL ÉTAT

L’animation devient alors un canal d’information.

Elle peut communiquer :

- progression ;
- causalité ;
- continuité ;
- hiérarchie ;
- résultat.

Une animation décorative n’a pas nécessairement cette fonction.

# 129 — INFORMATION ET 3D

Dans une expérience 3D :

- perspective ;
- profondeur ;
- lumière ;
- mouvement ;
- contraste ;

peuvent communiquer la structure spatiale.

La 3D est donc aussi une représentation informationnelle.

Mais :

plus d’effets visuels ≠ plus d’information utile.

# 130 — PRINCIPLE DE SIGNAL VS BRUIT

Une interface, un modèle ou un système peut contenir :

SIGNAL  
+  
BRUIT

Le problème d’ingénierie devient :

comment maximiser le signal utile relativement au bruit et au coût ?

Cette intuition traverse :

- communications ;
- IA ;
- UI ;
- traitement du signal ;
- observabilité ;
- systèmes distribués.

# 131 — ARCHITECTURE LOGICIELLE D’UN MODULE INFORMATIONNEL

Une architecture générique peut être :

Data Source  
↓  
Preprocessing  
↓  
Probability Model  
↓  
Information Measures  
↓  
Decision / Optimization  
↓  
Visualization / Action

# 132 — ABSTRACTION LOGICIELLE

On peut définir des fonctions conceptuelles :

entropy(p)  
conditional_entropy(p_xy)  
mutual_information(p_xy)  
kl_divergence(p, q)  
cross_entropy(p, q)  
js_divergence(p, q)

Puis des modules :

estimators/  
coding/  
compression/  
channels/  
metrics/  
information_ml/

# 133 — VALIDATION D’UNE IMPLÉMENTATION

Pour chaque mesure :

### Vérifier les invariants

Entropie :

\[ H(X) \]

KL :

\[ D_{KL}(P|Q) \]

Information mutuelle :

\[ I(X;Y) \]

et :

\[ I(X;Y)=0 \]

pour l’indépendance.

# 134 — TESTS DE PROPRIÉTÉS

Un bon module de théorie de l’information ne doit pas seulement tester :

input → expected output

Il doit également tester :

propriétés mathématiques

Exemples :

uniforme → entropie maximale  
déterministe → entropie nulle  
indépendance → MI nulle  
P = Q → KL nulle

# 135 — NUMÉRIQUE ET STABILITÉ

La théorie de l’information rencontre directement le Domaine L — Analyse numérique.

Les probabilités très faibles peuvent conduire à :

\[ p \]

avec :

\[ p \]

Il faut donc éviter les calculs naïfs.

# 136 — LOG-PROBABILITÉS

Au lieu de multiplier :

\[ p_1p_2p_n \]

on travaille avec :

\[ p_1+p_2++p_n \]

Cela améliore souvent la stabilité numérique.

# 137 — LOG-SUM-EXP

Pour calculer :

\[ (\_i e^{z_i}) \]

on utilise :

\[ m+(\_i e^{z_i-m}) \]

où :

\[ m=\_i z_i \]

Cette technique est fondamentale pour les modèles probabilistes et le machine learning.

# 138 — SOFTMAX ET INFORMATION

Le softmax :

\[ P_i = {\_j e^{z_j}} \]

produit une distribution.

La cross-entropy est ensuite calculée sur cette distribution.

Ainsi :

logits  
↓  
softmax  
↓  
distribution  
↓  
cross-entropy  
↓  
gradient

relie directement :

algèbre  
+  
probabilités  
+  
théorie de l'information  
+  
optimisation.

# 139 — INFORMATION ET OPTIMISATION

Beaucoup de problèmes informationnels prennent la forme :

\[ _Q D_{KL}(P|Q) \]

ou :

\[ I(X;Y) \]

ou :

\[ R(D) \]

On retrouve donc constamment :

mesure informationnelle  
+  
contrainte  
+  
optimisation.

# 140 — ALGORITHME DE BLAHUT-ARIMOTO

Pour certains problèmes de capacité ou de débit-distorsion, l’algorithme de Blahut-Arimoto fournit une méthode itérative.

MIT enseigne explicitement son utilisation pour maximiser la capacité.

Conceptuellement :

initialisation  
↓  
mise à jour de distribution  
↓  
calcul d'information  
↓  
nouvelle distribution  
↓  
convergence

Il constitue un excellent exemple de rencontre entre :

- théorie de l’information ;
- optimisation ;
- probabilités ;
- algorithmes numériques.

# 141 — INFORMATION ET CONVEXITÉ

La théorie de l’information possède de nombreuses connexions avec :

- convexité ;
- concavité ;
- inégalités de Jensen ;
- optimisation convexe.

MIT consacre explicitement une partie de son cursus à la convexité, Jensen, la positivité de l’information mutuelle et les théorèmes de traitement de l’information.

# 142 — CHAÎNE CONCEPTUELLE COMPLÈTE

Une compréhension mature du domaine doit permettre de passer naturellement entre :

probabilité  
↓  
surprise  
↓  
entropie  
↓  
entropie conditionnelle  
↓  
information mutuelle  
↓  
divergence KL  
↓  
cross-entropy  
↓  
codage  
↓  
compression  
↓  
canal  
↓  
capacité  
↓  
codes correcteurs  
↓  
apprentissage  
↓  
représentation

# 143 — TABLEAU DES NOTIONS ESSENTIELLES

| Notion | Formule centrale | Question |
| --- | --- | --- |
| Information | (-p(x)) | Combien cet événement apporte-t-il ? |
| Entropie | (H(X)=-pp) | Quelle est l’incertitude moyenne ? |
| Entropie conditionnelle | (H(X | Y)) |
| Information mutuelle | (I(X;Y)) | Combien (Y) renseigne-t-il sur (X) ? |
| KL  | (D_{KL}(P\|Q)) | À quel point (P) diffère-t-elle de (Q) ? |
| Cross-entropy | (-PQ) | Quel est le coût de prédiction ? |
| Codage | (l_i) | Comment représenter efficacement ? |
| Compression | réduction du coût | Comment réduire la représentation ? |
| Capacité | (I(X;Y)) | Combien peut-on transmettre ? |
| Débit-distorsion | (R(D)) | Combien faut-il transmettre pour une qualité donnée ? |

# 144 — CARTE MENTALE DU DOMAINE

THÉORIE DE  
L'INFORMATION  
│  
┌─────────────────┼──────────────────┐  
│ │ │  
MESURER REPRÉSENTER TRANSMETTRE  
│ │ │  
Entropie Codage Canaux  
Surprise Huffman Bruit  
MI Arithmétique Capacité  
KL Compression Codes  
Cross-Entropy MDL Correction  
│ │ │  
└─────────────────┼──────────────────┘  
│  
IA / ML  
│  
┌───────────┼───────────┐  
│ │ │  
NLP Features Génération  
│ │ │  
modèles arbres latent  
langage décision spaces

# 145 — PATTERNS DE RECONNAISSANCE

Lorsqu’un problème contient :

### « incertitude »

penser :

\[ H(X) \]

### « surprise »

penser :

\[ -P(x) \]

### « information apportée par une observation »

penser :

\[ I(X;Y) \]

### « différence entre distributions »

penser :

\[ D_{KL} \]

ou une divergence adaptée.

### « prédiction probabiliste »

penser :

\[ \]

### « compression »

penser :

\[ H(X),H_, \]

### « communication fiable »

penser :

\[ C=I(X;Y) \]

### « compression avec perte »

penser :

\[ R(D) \]

### « représentation compacte mais pertinente »

penser :

\[ I(X;T),I(T;Y) \]

# 146 — ERREURS CLASSIQUES

## Erreur 1

Dire :

l’entropie est la quantité de données.

Faux.

Elle mesure une incertitude statistique moyenne dans un modèle donné.

## Erreur 2

Dire :

la KL est une distance.

Approximativement utile intuitivement, mais mathématiquement imprécis.

C’est une divergence et elle n’est pas symétrique.

## Erreur 3

Dire :

information mutuelle élevée = causalité.

Faux.

La dépendance statistique n’implique pas la causalité.

## Erreur 4

Dire :

compression = suppression de données.

Pas nécessairement.

La compression sans perte change la représentation.

## Erreur 5

Dire :

une forte entropie est toujours bonne.

Faux.

Cela dépend du problème.

Pour un secret, l’incertitude peut être souhaitable.

Pour un système prédictif, une forte incertitude peut signaler un problème.

## Erreur 6

Dire :

plus de bits signifie toujours plus d’information.

Faux.

Une représentation peut contenir énormément de redondance.

## Erreur 7

Utiliser une KL sans vérifier les supports.

Une probabilité nulle dans (Q) peut rendre :

\[ D_{KL}(P|Q) \]

infinie.

# 147 — MÉTHODE DE RÉSOLUTION D’UN PROBLÈME INFORMATIONNEL

## Étape 1 — Identifier les variables

Exemple :

X = données  
Y = label  
Z = représentation

## Étape 2 — Identifier les distributions

P(X)  
P(Y)  
P(X,Y)  
P(Y|X)

## Étape 3 — Identifier la question

incertitude ?  
dépendance ?  
différence ?  
compression ?  
transmission ?

## Étape 4 — Choisir la mesure

H  
H(.|.)  
I  
KL  
JS  
cross-entropy  
R(D)  
C

## Étape 5 — Calculer

Appliquer la formule ou un algorithme adapté.

## Étape 6 — Vérifier les propriétés

Exemples :

\[ H \]

\[ I \]

\[ KL \]

## Étape 7 — Interpréter

La valeur numérique seule n’est pas suffisante.

# 148 — WORKFLOW D’IMPLÉMENTATION

PROBLÈME  
↓  
VARIABLES  
↓  
PROBABILITÉS  
↓  
MESURE INFORMATIONNELLE  
↓  
FORMULE  
↓  
ESTIMATION  
↓  
CALCUL NUMÉRIQUE  
↓  
VALIDATION  
↓  
DÉCISION

# 149 — CRITÈRES DE QUALITÉ D’UN SYSTÈME INFORMATIONNEL

Un système doit être évalué selon :

- exactitude ;
- stabilité numérique ;
- coût mémoire ;
- coût CPU/GPU ;
- biais d’estimation ;
- variance ;
- robustesse ;
- interprétabilité ;
- qualité des distributions ;
- cohérence des unités ;
- qualité des données.

# 150 — THÉORIE DE L’INFORMATION ET COMPLEXITÉ

Une information peut être :

- facile à décrire ;
- difficile à décrire ;
- régulière ;
- aléatoire ;
- compressible ;
- incompressible selon un modèle.

Cela ouvre la porte à :

- complexité algorithmique ;
- Kolmogorov ;
- MDL ;
- minimum message length ;
- compression comme proxy de structure.

Attention toutefois :

complexité de Kolmogorov et entropie de Shannon sont des notions différentes.

# 151 — INFORMATION ALGORITHMIQUE

La complexité de Kolmogorov cherche conceptuellement :

quelle est la longueur du plus petit programme qui génère cette donnée ?

On obtient une autre notion :

\[ K(x) \]

Contrairement à Shannon :

- Shannon raisonne sur des distributions ;
- Kolmogorov raisonne sur une description algorithmique individuelle.

Les deux notions sont liées conceptuellement mais ne doivent pas être confondues.

# 152 — CRÉATIVITÉ : INFORMATION COMME RESSOURCE

Une idée intéressante pour les systèmes logiciels :

traiter l’information comme une ressource limitée.

Un système possède :

budget de données  
budget de stockage  
budget de bande passante  
budget de contexte  
budget de calcul  
budget d'attention

Il faut alors optimiser :

\[ {} \]

# 153 — CRÉATIVITÉ : INFORMATION DENSITY

On peut définir conceptuellement une densité :

\[ D_I= {} \]

Cette idée peut inspirer :

- dashboards ;
- interfaces ;
- rapports ;
- systèmes de monitoring ;
- agents IA ;
- bases de connaissances.

# 154 — CRÉATIVITÉ : AGENT IA INFORMATIONNEL

Un agent peut disposer d’un budget :

\[ B \]

pour lire des informations.

Au lieu de tout lire, il cherche les observations maximisant :

\[ \]

Pipeline :

QUESTIONS  
↓  
OBSERVATIONS CANDIDATES  
↓  
ESTIMATION DU GAIN INFORMATIONNEL  
↓  
SÉLECTION  
↓  
OBSERVATION  
↓  
MISE À JOUR

Cela produit un agent qui :

cherche activement l’information la plus utile.

# 155 — CRÉATIVITÉ : CONTEXTE IA

Dans un système d’agent :

historique  
+  
documents  
+  
outils  
+  
mémoire

le contexte disponible est limité.

On peut donc imaginer un **context compressor** qui cherche à conserver :

information essentielle  
+  
dépendances  
+  
décisions  
+  
contraintes

tout en supprimant :

redondance  
+  
répétition  
+  
bruit

Cela constitue une application directe des idées de compression et d’information pertinente.

# 156 — CRÉATIVITÉ : MÉMOIRE ADAPTATIVE

Une mémoire d’agent pourrait attribuer un score informationnel à une donnée :

\[ Score(x) = I(x;)

- Cost(x)
- Novelty(x) \]

L’idée serait de conserver davantage :

- décisions importantes ;
- préférences utiles ;
- contraintes ;
- connaissances nouvelles.

Et moins :

- répétitions ;
- informations obsolètes ;
- détails inutiles.

# 157 — CRÉATIVITÉ : ROUTAGE D’AGENTS

Supposons plusieurs agents :

Agent recherche  
Agent code  
Agent design  
Agent sécurité  
Agent analyse

Un routeur peut choisir l’agent dont l’action maximise le gain informationnel attendu.

Cela transforme :

routing

en problème de :

information gain

# 158 — CRÉATIVITÉ : RECHERCHE WEB

Un agent de recherche pourrait estimer :

\[ IG(q) = H()

- H(q) \]

Il privilégierait les requêtes qui ont le plus de chances de réduire l’incertitude.

C’est une manière de transformer :

recherche web

en :

stratégie active de réduction d’incertitude.

# 159 — CRÉATIVITÉ : DEBUGGING

Un bug peut être considéré comme une hypothèse :

\[ H={h_1,h_2,,h_n} \]

Chaque test produit une observation.

On peut choisir le test qui maximise :

\[ I(H;O) \]

Autrement dit :

quel test éliminera le plus d’hypothèses ?

Cela donne une stratégie de debugging informationnelle.

# 160 — DEBUGGING INFORMATIONNEL

Au lieu de :

modifier du code au hasard

faire :

hypothèses  
↓  
test discriminant  
↓  
observation  
↓  
réduction des hypothèses  
↓  
nouveau test

C’est une application particulièrement puissante de l’idée d’information mutuelle.

# 161 — CRÉATIVITÉ : UX ADAPTATIVE

Une interface peut observer les actions de l’utilisateur et estimer :

ce que l'utilisateur sait  
ce qu'il cherche  
ce qui lui manque

Puis afficher dynamiquement l’information la plus utile.

Cela conduit à :

- interfaces adaptatives ;
- onboarding intelligent ;
- assistance contextuelle ;
- progressive disclosure ;
- systèmes tutoriels.

# 162 — CRÉATIVITÉ : MONITORING INTELLIGENT

Au lieu d’envoyer 10 000 événements :

EVENT EVENT EVENT EVENT ...

un système peut chercher :

quels événements modifient réellement notre compréhension du système ?

Puis :

filtrer  
↓  
agréger  
↓  
compresser  
↓  
transmettre

Cela peut réduire :

- coût réseau ;
- coût stockage ;
- bruit opérationnel.

# 163 — PROJET 1 — CALCULATEUR D’ENTROPIE

### Objectif

Construire une bibliothèque :

entropy()  
joint_entropy()  
conditional_entropy()  
mutual_information()  
kl_divergence()  
cross_entropy()  
js_divergence()

### Contraintes

Implémenter d’abord sans bibliothèque spécialisée.

### Validation

Comparer aux propriétés mathématiques.

# 164 — PROJET 2 — COMPRESSEUR HUFFMAN

Construire :

input  
↓  
frequency table  
↓  
priority queue  
↓  
Huffman tree  
↓  
binary encoding  
↓  
compressed file

Puis :

compressed file  
↓  
Huffman tree  
↓  
decoded data

Tester :

\[ decode(encode(x))=x \]

# 165 — PROJET 3 — COMPARATEUR DE COMPRESSEURS

Comparer :

- Huffman ;
- LZ ;
- compression native ;
- éventuellement codage arithmétique.

Mesurer :

\[ compression ratio \]

\[ bits/symbol \]

\[ compression time \]

\[ decompression time \]

# 166 — PROJET 4 — ANALYSEUR INFORMATIONNEL DE TEXTE

Pour un corpus :

calculer :

- fréquence des caractères ;
- entropie ;
- entropie conditionnelle ;
- entropie par mot ;
- perplexité d’un modèle ;
- compression réelle.

Puis comparer :

texte naturel  
vs  
texte aléatoire  
vs  
texte répétitif

# 167 — PROJET 5 — ARBRE DE DÉCISION INFORMATIONNEL

Implémenter :

entropy()  
information_gain()  
split()  
build_tree()  
predict()

Puis comparer avec une bibliothèque ML.

Objectif :

comprendre réellement pourquoi un arbre choisit un attribut.

# 168 — PROJET 6 — CANAL BRUITÉ

Créer une simulation :

message  
↓  
encodeur  
↓  
canal bruité  
↓  
réception  
↓  
décodage

Mesurer :

\[ P_e \]

en fonction de :

\[ p \]

# 169 — PROJET 7 — CODE CORRECTEUR

Implémenter un petit code de Hamming.

Tester :

message  
↓  
encodage  
↓  
bit flip  
↓  
décodage  
↓  
message corrigé

Objectif :

comprendre concrètement comment la redondance devient une ressource de fiabilité.

# 170 — PROJET 8 — DÉTECTEUR DE DRIFT

Construire :

distribution référence  
↓  
distribution actuelle  
↓  
divergence  
↓  
score  
↓  
alerte

Comparer :

- KL ;
- Jensen-Shannon ;
- autres métriques.

# 171 — PROJET 9 — AGENT DE DEBUGGING INFORMATIONNEL

Créer un agent qui :

1.  liste les hypothèses ;
2.  propose des tests ;
3.  estime le pouvoir discriminant de chaque test ;
4.  choisit le prochain test ;
5.  élimine les hypothèses ;
6.  converge vers une cause probable.

Ce projet permet de transformer une notion théorique en système agentique.

# 172 — PROJET 10 — CONTEXT COMPRESSOR POUR IA

Créer un prototype qui reçoit :

historique conversationnel

et produit :

résumé informationnel

en conservant :

- objectifs ;
- contraintes ;
- décisions ;
- faits ;
- dépendances ;
- état du projet.

Mesurer :

taille avant  
taille après  
information conservée  
erreurs introduites

# 173 — DÉFI SANS IA

Implémenter manuellement :

### Niveau 1

Entropie.

### Niveau 2

Entropie conditionnelle.

### Niveau 3

Information mutuelle.

### Niveau 4

KL.

### Niveau 5

Huffman.

### Niveau 6

Canal BSC.

### Niveau 7

Code correcteur.

### Niveau 8

Analyse de corpus.

### Niveau 9

Information gain.

### Niveau 10

Petit système de compression.

# 174 — DÉFI AVEC IA

Demander à une IA de :

- générer plusieurs implémentations ;
- comparer les algorithmes ;
- produire des tests ;
- vérifier les invariants ;
- profiler les performances ;
- chercher des cas limites ;
- expliquer les erreurs numériques.

Mais la validation mathématique doit rester humaine.

# 175 — CHECKLIST DE MAÎTRISE

Avant de considérer le Domaine M comme maîtrisé, être capable d’expliquer :

## Fondements

- information ;
- surprise ;
- bit ;
- nat ;
- entropie ;
- entropie jointe ;
- entropie conditionnelle.

## Dépendances

- information mutuelle ;
- information mutuelle conditionnelle ;
- indépendance ;
- data processing inequality ;
- Fano.

## Divergences

- KL ;
- cross-entropy ;
- Jensen-Shannon.

## Compression

- code fixe ;
- code variable ;
- code préfixe ;
- Kraft-McMillan ;
- Shannon coding ;
- Huffman ;
- codage arithmétique ;
- compression universelle.

## Communication

- canal ;
- bruit ;
- BSC ;
- BEC ;
- AWGN ;
- capacité ;
- théorème de codage ;
- codes correcteurs.

## Compression avec perte

- distorsion ;
- (R(D)) ;
- compromis débit/qualité.

## IA

- cross-entropy ;
- KL loss ;
- information gain ;
- perplexité ;
- MDL ;
- Information Bottleneck ;
- information mutuelle.

## Applications

- NLP ;
- réseaux ;
- stockage ;
- cryptographie ;
- décision ;
- détection ;
- agents ;
- systèmes distribués.

# 176 — CONNEXIONS AVEC LES AUTRES DOMAINES

## Domaine G — Probabilités

Relation fondamentale :

\[ P(X) H(X) \]

Sans probabilités, pas de théorie de l’information de Shannon.

## Domaine H — Statistiques

Les distributions doivent souvent être estimées à partir de données.

## Domaine J — Optimisation

Beaucoup de problèmes informationnels sont des problèmes d’optimisation.

## Domaine L — Analyse numérique

Les mesures informationnelles sont calculées numériquement et peuvent être instables pour des probabilités extrêmes.

## Domaine A — Logique

La compression, les codes et la description des structures ont des connexions avec la notion de représentation.

## Domaine F — Combinatoire

Les codes, les alphabets et le comptage des séquences sont profondément combinatoires.

## Domaine C — Algèbre linéaire

Les codes correcteurs, les transformations et certains modèles de communication utilisent des structures linéaires.

## Domaine E — Graphes

Les arbres de Huffman et certains réseaux de communication peuvent être représentés par des graphes.

# 177 — TABLEAU DES CONNEXIONS

| Domaine | Connexion |
| --- | --- |
| Probabilités | distributions |
| Statistiques | estimation |
| Optimisation | maximisation/minimisation |
| Analyse numérique | calcul stable |
| Combinatoire | comptage des codes |
| Algèbre | codes linéaires |
| Graphes | arbres/canaux/réseaux |
| IA  | apprentissage probabiliste |
| NLP | prédiction/compression |
| Cyber | confidentialité |
| Réseaux | capacité |
| Stockage | redondance |

# 178 — FICHES DE DEEP-DIVE À CRÉER

Pour poursuivre l’apprentissage, le domaine M peut être divisé en fiches :

### M01 — Information et surprise

### M02 — Entropie

### M03 — Entropie conditionnelle

### M04 — Entropie jointe

### M05 — Information mutuelle

### M06 — KL divergence

### M07 — Cross-entropy

### M08 — Jensen-Shannon

### M09 — AEP et typicité

### M10 — Codage de source

### M11 — Kraft-McMillan

### M12 — Huffman

### M13 — Codage arithmétique

### M14 — Compression universelle

### M15 — Canaux et bruit

### M16 — Capacité

### M17 — Codes correcteurs

### M18 — Débit-distorsion

### M19 — Information et machine learning

### M20 — Information Bottleneck / MDL

# 179 — QUESTIONS À SE POSER AVANT UNE IMPLÉMENTATION

Avant d’utiliser une mesure informationnelle :

### 1.

Quelle est la variable aléatoire ?

### 2.

Quelle est sa distribution ?

### 3.

Cette distribution est-elle connue ou estimée ?

### 4.

Les variables sont-elles discrètes ou continues ?

### 5.

Quelle quantité veut-on mesurer ?

incertitude ?  
dépendance ?  
différence ?  
prédictibilité ?  
compression ?  
capacité ?

### 6.

Quelle métrique est adaptée ?

### 7.

Quelles sont les hypothèses ?

### 8.

Que signifie réellement le résultat ?

### 9.

Quels sont les biais d’estimation ?

### 10.

Quelle décision sera prise à partir de cette mesure ?

# 180 — INFORMATION VS UTILITÉ

Une distinction particulièrement importante :

\[ \]

Une donnée peut contenir beaucoup d’information au sens de Shannon tout en étant inutile pour la tâche.

Par exemple :

donnée très imprévisible

ne signifie pas :

donnée pertinente pour la prédiction.

Pour l’IA, la notion essentielle devient souvent :

**information pertinente par rapport à une variable ou une tâche.**

# 181 — INFORMATION PERTINENTE

Pour une tâche (Y), une représentation (T) peut être intéressante si elle conserve :

\[ I(T;Y) \]

tout en limitant sa complexité.

Cela constitue l’une des raisons pour lesquelles les concepts d’information mutuelle sont devenus importants dans le machine learning. Stanford présente explicitement la théorie de l’information comme utile non seulement pour communication et compression, mais aussi pour statistiques et machine learning.

# 182 — MODÈLE MENTAL FINAL

Il faut retenir quatre niveaux.

## Niveau 1 — Mesurer

Combien d'incertitude ?

→ Entropie.

## Niveau 2 — Comparer

À quel point deux distributions diffèrent-elles ?

→ KL / JS.

## Niveau 3 — Relier

Combien une variable renseigne-t-elle sur une autre ?

→ Information mutuelle.

## Niveau 4 — Ingénierie

Comment représenter, compresser et transmettre cette information ?

→ Codage, compression, capacité, théorie des canaux.

# 183 — MODÈLE MENTAL IA

Pour l’intelligence artificielle :

DONNÉES  
↓  
DISTRIBUTION  
↓  
INCERTITUDE  
↓  
INFORMATION  
↓  
REPRÉSENTATION  
↓  
COMPRESSION / SÉLECTION  
↓  
APPRENTISSAGE  
↓  
PRÉDICTION  
↓  
DÉCISION

La question centrale devient :

**quelle information doit être conservée pour accomplir correctement la tâche ?**

# 184 — MODÈLE MENTAL INGÉNIERIE

Pour l’ingénierie :

SOURCE  
↓  
ENCODAGE  
↓  
COMPRESSION  
↓  
TRANSMISSION / STOCKAGE  
↓  
BRUIT / PERTURBATION  
↓  
DÉCODAGE  
↓  
RECONSTRUCTION

Les questions fondamentales deviennent :

Combien de bits ?  
Quelle redondance ?  
Quel débit ?  
Quelle capacité ?  
Quel taux d'erreur ?  
Quelle distorsion ?  
Quel coût ?

# 185 — SYNTHÈSE ULTIME

La théorie de l’information peut être résumée par une chaîne extrêmement compacte :

\[ \]

Avec les notions centrales :

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

\[ \]

et, pour la compression avec perte :

\[ \]

Ces équations forment le noyau mathématique du domaine.

# 186 — CE QUE LE DOMAINE M DOIT PERMETTRE DE FAIRE

À terme, connaître ce domaine signifie être capable de regarder un problème informatique et de reconnaître :

**Il y a une incertitude → entropie.**

**Il y a une observation qui réduit cette incertitude → information mutuelle.**

**Il y a deux distributions à comparer → divergence.**

**Il faut prédire une distribution → cross-entropy.**

**Il faut réduire une représentation → compression.**

**Il faut transmettre malgré du bruit → codage correcteur.**

**Il faut connaître la limite de transmission → capacité.**

**Il faut compresser avec une perte contrôlée → débit-distorsion.**

**Il faut trouver une représentation compacte mais pertinente → Information Bottleneck.**

**Il faut choisir un modèle en fonction de sa capacité à décrire les données → MDL.**

**Il faut sélectionner une variable qui réduit l’incertitude → information gain.**

# 187 — VISION FINALE

La théorie de l’information n’est donc pas seulement une théorie de la communication.

Elle constitue une théorie générale permettant de raisonner sur :

- ce qui est connu ;
- ce qui est inconnu ;
- ce qui est surprenant ;
- ce qui est redondant ;
- ce qui est pertinent ;
- ce qui peut être compressé ;
- ce qui peut être transmis ;
- ce qui peut être reconstruit ;
- ce qui est perdu ;
- ce qui doit être conservé.

C’est précisément ce qui explique sa portée exceptionnelle.

Elle commence avec une question apparemment simple :

**Combien d’information contient quelque chose ?**

Puis elle mène à :

**Comment représenter cette information efficacement ?**

Puis :

**Comment la transmettre malgré le bruit ?**

Puis :

**Comment déterminer les limites fondamentales de cette transmission ?**

Et finalement :

**Comment construire des systèmes qui conservent l’information importante tout en éliminant ce qui ne l’est pas ?**

C’est cette dernière question qui rend le domaine particulièrement puissant pour :

- l’intelligence artificielle ;
- les modèles de langage ;
- le NLP ;
- la compression ;
- les réseaux ;
- le stockage ;
- la cryptographie ;
- les systèmes distribués ;
- les agents autonomes ;
- les interfaces ;
- les architectures logicielles.

La théorie de l’information devient alors non seulement une branche des mathématiques appliquées, mais une **théorie de l’économie de l’information** :

\[ \]

# 188 — RÉFÉRENCES DE RECHERCHE ET POURSUITE

Les références académiques particulièrement structurantes pour ce domaine comprennent les cours et notes de **MIT 6.441 Information Theory**, qui couvrent notamment entropie, divergence, information mutuelle, AEP, compression, Huffman, capacité, codage de canal, canaux gaussiens, codes linéaires et théorie débit-distorsion.

Les ressources **Stanford EE 276 / EE 376A** couvrent également l’entropie, les codes préfixes, Kraft-McMillan, Huffman, les taux d’entropie, la capacité, les théorèmes de codage, les codes polaires, la compression avec perte et les liens avec le machine learning.

Pour approfondir les connexions avec l’IA, l’Information Bottleneck, le MDL et les représentations, les travaux référencés par Stanford constituent une extension naturelle du domaine.

# 189 — RÈGLE D’UTILISATION POUR LES FUTURS PROJETS

Lorsqu’un futur projet contient :

compression  
probabilités  
classification  
NLP  
LLM  
communication  
réseaux  
stockage  
sécurité  
anomalies  
information gain  
représentation  
modèle probabiliste  
distribution

l’IA doit considérer **Domaine M — Théorie de l’information** comme une référence pertinente.

Elle doit alors :

1.  identifier les variables aléatoires ;
2.  identifier les distributions ;
3.  déterminer quelle information doit être mesurée ;
4.  sélectionner la mesure adaptée ;
5.  vérifier les hypothèses ;
6.  calculer ou estimer la quantité ;
7.  interpréter le résultat ;
8.  déterminer son implication algorithmique ;
9.  choisir une implémentation adaptée ;
10. rechercher ensuite les détails techniques spécifiques à la technologie utilisée.

Le domaine M doit donc fonctionner comme une couche de raisonnement :

PROBLÈME RÉEL  
↓  
MODÈLE PROBABILISTE  
↓  
MESURE INFORMATIONNELLE  
↓  
LIMITE / OBJECTIF  
↓  
ALGORITHME  
↓  
IMPLÉMENTATION  
↓  
SYSTÈME

**C’est cette transformation — de la notion abstraite d’information vers une décision informatique concrète — qui constitue la compétence réellement recherchée.**