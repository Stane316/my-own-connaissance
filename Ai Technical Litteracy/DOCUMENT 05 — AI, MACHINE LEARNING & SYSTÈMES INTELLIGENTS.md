# **DOCUMENT 05 — AI, MACHINE LEARNING & SYSTÈMES INTELLIGENTS**

**Version : 1.0 — Document de fondation**

**Objectif :** construire une culture technique solide permettant de comprendre, choisir, diriger, intégrer et auditer des technologies d’IA et de systèmes intelligents sans avoir besoin de devenir spécialiste de chaque sous-domaine.

# **0\. Positionnement du document**

L’objectif de ce document n’est **pas** de faire de toi un chercheur en intelligence artificielle.

Il n’est pas non plus de te transformer immédiatement en ingénieur Machine Learning capable d'entraîner des modèles complexes.

L’objectif est différent et, dans ton cas, beaucoup plus stratégique :

**Être suffisamment alphabétisé en IA pour comprendre ce qu'une solution d'IA fait réellement, déterminer si elle est pertinente, choisir la bonne approche, demander à une IA de la construire correctement, contrôler ce qu'elle produit et détecter lorsqu'elle raconte n'importe quoi.**

Autrement dit :

**Tu ne dois pas seulement savoir utiliser l'IA.**

**Tu dois savoir raisonner sur l'IA.**

# **1\. Le problème que ce document doit résoudre**

Aujourd'hui, une personne peut demander à une IA :

« Construis-moi une application avec de l'intelligence artificielle. »

L'IA peut répondre avec :

- une API de LLM ;
- un modèle de classification ;
- un chatbot ;
- un système RAG ;
- une base vectorielle ;
- des embeddings ;
- un agent ;
- du fine-tuning ;
- une architecture complexe ;
- ou simplement un appel à une API externe.

Le problème est que **toutes ces solutions ne répondent pas au même problème.**

Et si tu ne connais pas les concepts, tu ne peux pas savoir :

- si la solution est pertinente ;
- si elle est inutilement complexe ;
- si elle est coûteuse ;
- si elle est sécurisée ;
- si le modèle est adapté ;
- si les données sont suffisantes ;
- si le résultat est réellement fiable ;
- si l'IA a choisi une architecture correcte ;
- si une approche déterministe aurait été meilleure ;
- ou si l'IA a simplement ajouté « de l'IA » parce que tu lui as demandé de l'IA.

C'est précisément ce que ce document doit empêcher.

# **2\. La carte mentale centrale du domaine**

Le domaine est immense.

Il faut donc commencer par une représentation simple :

INTELLIGENCE ARTIFICIELLE  
│  
┌───────────────────┼───────────────────┐  
│ │ │  
IA symbolique MACHINE LEARNING SYSTÈMES INTELLIGENTS  
│ │ │  
règles/logique apprentissage perception  
statistique décision  
│ action  
┌─────────────┼─────────────┐  
│ │ │  
ML classique DL RL  
│ │ │  
arbres, SVM, réseaux agents /  
régression... neuronaux décision  
│  
┌───────────┼───────────┐  
│ │ │  
CNN/RNN Transformers modèles  
multimodaux  
│  
┌──────────────┼─────────────┐  
│ │ │  
LLM Vision Audio  
│  
┌─────────┼──────────┐  
│ │ │  
prompting RAG fine-tuning  
│  
embeddings  
│  
vector database  
│  
applications  
│  
agents / workflows

Cette carte permet déjà de comprendre une chose fondamentale :

**« IA » n'est pas une technologie unique.**

C'est une famille extrêmement large de méthodes, modèles, architectures et systèmes.

# **3\. Le modèle de raisonnement fondamental**

Pour comprendre presque n'importe quel projet IA, utilise cette chaîne :

PROBLÈME  
↓  
OBJECTIF  
↓  
ENTRÉES / DONNÉES  
↓  
REPRÉSENTATION  
↓  
MÉTHODE / MODÈLE  
↓  
APPRENTISSAGE  
↓  
PRÉDICTION / GÉNÉRATION  
↓  
ÉVALUATION  
↓  
DÉPLOIEMENT  
↓  
SURVEILLANCE  
↓  
FEEDBACK  
↓  
AMÉLIORATION

Pour les systèmes intelligents complets :

MONDE  
↓  
PERCEPTION  
↓  
DONNÉES  
↓  
REPRÉSENTATION  
↓  
RAISONNEMENT / MODÈLE  
↓  
DÉCISION  
↓  
ACTION  
↓  
OBSERVATION  
↓  
NOUVEL ÉTAT

Cette seconde chaîne est extrêmement importante.

Elle permet de comprendre les :

- agents ;
- robots ;
- systèmes autonomes ;
- recommandations ;
- systèmes de décision ;
- assistants intelligents ;
- systèmes de détection ;
- systèmes de contrôle.

# **NIVEAU A — VUE GLOBALE : QU'EST-CE QUE L'IA ?**

# **A.1 — Intelligence artificielle**

## **Définition**

L'**intelligence artificielle (IA)** désigne l'ensemble des méthodes permettant à des systèmes informatiques d'accomplir des tâches qui nécessitent habituellement certaines capacités associées à l'intelligence humaine.

Par exemple :

- percevoir ;
- reconnaître ;
- classer ;
- prédire ;
- comprendre du langage ;
- générer du contenu ;
- raisonner ;
- prendre des décisions ;
- planifier ;
- apprendre.

Attention :

Une machine qui produit un résultat intelligent n'est pas nécessairement intelligente au sens humain.

# **A.2 — IA symbolique**

L'IA symbolique repose notamment sur :

- règles ;
- logique ;
- connaissances explicites ;
- arbres de décision ;
- systèmes experts ;
- moteurs d'inférence.

Exemple :

SI température > 38°C  
ET toux = vraie  
ALORS risque_infection = élevé

Aucun entraînement statistique n'est nécessaire pour cette règle.

L'être humain définit explicitement le raisonnement.

### **Pourquoi cela existe-t-il ?**

Parce que certains problèmes peuvent être parfaitement décrits par des règles.

### **Quand y penser ?**

Lorsque :

- les règles sont connues ;
- le comportement doit être déterministe ;
- l'explicabilité est importante ;
- les données d'apprentissage sont inexistantes ou insuffisantes.

# **A.3 — Machine Learning**

Le **Machine Learning (ML)** est une branche de l'IA dans laquelle un système apprend des régularités à partir de données afin d'effectuer une tâche.

Au lieu de dire :

SI X ALORS Y

on fournit généralement :

DONNÉES → APPRENTISSAGE → MODÈLE

Puis :

NOUVELLE DONNÉE → MODÈLE → PRÉDICTION

Exemple :

Tu disposes de milliers de transactions :

montant  
heure  
pays  
type de carte  
historique  
...

et tu connais pour chacune :

fraude = oui/non

Un modèle peut apprendre les relations statistiques permettant de prédire :

transaction → probabilité de fraude

# **A.4 — Deep Learning**

Le **Deep Learning (DL)** est une sous-branche du Machine Learning basée principalement sur des réseaux neuronaux comportant plusieurs couches.

IA  
└── Machine Learning  
└── Deep Learning

Le Deep Learning est particulièrement important pour :

- images ;
- audio ;
- langage ;
- vidéo ;
- données complexes ;
- modèles génératifs.

# **A.5 — Intelligence artificielle générative**

L'IA générative désigne des systèmes capables de **produire du contenu nouveau** à partir de ce qu'ils ont appris.

Elle peut générer :

- texte ;
- images ;
- audio ;
- vidéo ;
- code ;
- musique ;
- données synthétiques.

Exemple :

Prompt  
↓  
Modèle génératif  
↓  
Texte généré

ou :

Prompt  
↓  
Modèle d'image  
↓  
Image générée

# **A.6 — Système intelligent**

Un **système intelligent** est plus large qu'un simple modèle.

Un modèle peut être :

image → classification

Mais un système intelligent peut être :

capteur  
↓  
données  
↓  
prétraitement  
↓  
modèle IA  
↓  
décision  
↓  
action  
↓  
journalisation  
↓  
feedback

C'est une distinction essentielle.

**Modèle ≠ application IA ≠ système intelligent.**

# **NIVEAU B — LES GRANDES FAMILLES D'APPRENTISSAGE**

# **B.1 — Apprentissage supervisé**

On possède :

X = données d'entrée  
Y = réponse attendue

Le modèle apprend :

X → Y

Exemple :

email → spam / non-spam

Données :

|     |     |
| --- | --- |
| **Email** | **Label** |
| message 1 | spam |
| message 2 | normal |
| message 3 | spam |

### **Problèmes typiques**

- classification ;
- régression ;
- prédiction.

# **B.2 — Classification**

Le modèle choisit une catégorie.

Exemple :

photo → chat  
photo → chien  
photo → autre

Ou :

transaction → fraude / normale

Ou :

client → faible / moyen / élevé

# **B.3 — Régression**

La sortie est généralement une valeur numérique.

Exemple :

surface + localisation + nombre de chambres  
↓  
modèle  
↓  
prix estimé

Classification :

chat / chien

Régression :

327 500 FCFA

# **B.4 — Apprentissage non supervisé**

Il n'y a pas nécessairement de réponse correcte fournie.

Le modèle cherche des structures dans les données.

Exemple :

clients  
↓  
algorithme  
↓  
groupes de clients

Applications :

- clustering ;
- segmentation ;
- détection d'anomalies ;
- exploration de données.

# **B.5 — Clustering**

On cherche des groupes naturels.

Exemple :

100 000 clients  
↓  
clustering  
↓  
┌────────┬────────┬────────┐  
│ Groupe │ Groupe │ Groupe │  
│ A │ B │ C │  
└────────┴────────┴────────┘

Le modèle ne reçoit pas nécessairement :

« Voici les clients premium. »

Il peut découvrir des regroupements selon les caractéristiques observées.

# **B.6 — Apprentissage semi-supervisé**

Une partie des données est labellisée et une autre ne l'est pas.

Utile lorsque :

10 000 000 images  
↓  
seulement  
10 000 annotées

L'annotation humaine étant coûteuse, on cherche à exploiter les données non annotées.

# **B.7 — Self-supervised learning**

Le modèle construit une partie de son propre signal d'apprentissage à partir des données.

C'est fondamental dans de nombreux modèles modernes.

Exemple simplifié :

"Le ciel est \___"

Le modèle apprend à prédire un élément manquant.

Les données n'ont pas nécessairement besoin d'être annotées manuellement comme dans un dataset classique de classification.

# **B.8 — Reinforcement Learning**

Dans l'apprentissage par renforcement, un agent interagit avec un environnement.

ENVIRONNEMENT  
↑  
│  
récompense  
│  
│  
AGENT ───────→ ACTION  
↑  
│  
ÉTAT / OBSERVATION

L'agent cherche à maximiser une récompense cumulative.

Exemples :

- jeux ;
- robotique ;
- contrôle ;
- optimisation ;
- systèmes décisionnels.

# **B.9 — Exploration vs exploitation**

Un agent doit parfois :

**Explorer**

essayer quelque chose de nouveau.

ou :

**Exploiter**

utiliser ce qui fonctionne déjà.

C'est un problème central du Reinforcement Learning.

# **NIVEAU C — DONNÉES : LE CARBURANT DU MACHINE LEARNING**

Une erreur fréquente est :

« J'ai besoin d'un meilleur modèle. »

Alors que le vrai problème est parfois :

« Mes données sont mauvaises. »

# **C.1 — Dataset**

Un **dataset** est un ensemble structuré de données utilisé notamment pour analyser, entraîner ou évaluer un modèle.

Exemple :

dataset.csv

avec :

age,revenu,ville,achat  
20,150000,Cotonou,oui  
31,300000,Abomey-Calavi,non  
...

# **C.2 — Feature**

Une **feature** est une caractéristique utilisée par le modèle.

Exemple :

Pour prédire un prix immobilier :

surface  
nombre_de_chambres  
quartier  
distance_centre  
âge_bâtiment

sont des features potentielles.

# **C.3 — Label / Target**

La variable que le modèle doit prédire.

Exemple :

features :  
surface  
quartier  
chambres  
<br/>target :  
prix

# **C.4 — Data cleaning**

Les données réelles peuvent contenir :

- valeurs manquantes ;
- doublons ;
- erreurs ;
- incohérences ;
- valeurs extrêmes ;
- mauvais formats ;
- biais ;
- données obsolètes.

Avant d'entraîner :

Données brutes  
↓  
Nettoyage  
↓  
Validation  
↓  
Transformation  
↓  
Dataset exploitable

# **C.5 — Data preprocessing**

Le prétraitement transforme les données afin qu'elles soient utilisables par le modèle.

Exemples :

- normalisation ;
- standardisation ;
- encodage ;
- tokenisation ;
- suppression du bruit ;
- transformation des variables ;
- redimensionnement des images.

# **C.6 — Data leakage**

Concept **absolument essentiel**.

Le data leakage survient lorsqu'une information qui ne devrait pas être disponible au moment de la prédiction se retrouve indirectement dans les données utilisées pour apprendre.

Résultat :

performance apparente : excellente  
performance réelle : mauvaise

C'est l'un des pièges majeurs du Machine Learning.

# **C.7 — Biais des données**

Si les données représentent mal la réalité, le modèle peut apprendre une représentation biaisée.

DONNÉES BIAISÉES  
↓  
APPRENTISSAGE  
↓  
MODÈLE BIAISÉ  
↓  
DÉCISIONS BIAISÉES

Un modèle n'est donc pas automatiquement objectif simplement parce qu'il est mathématique.

# **C.8 — Qualité des données**

Avant de demander à une IA d'entraîner un modèle, demande :

Les données sont-elles :  
\- suffisamment nombreuses ?  
\- représentatives ?  
\- propres ?  
\- cohérentes ?  
\- récentes ?  
\- correctement labellisées ?  
\- exemptes de leakage ?  
\- compatibles avec l'objectif ?

# **NIVEAU D — COMMENT UN MODÈLE APPREND**

# **D.1 — Modèle**

Un modèle est une représentation mathématique apprise ou définie permettant de transformer des entrées en sorties.

Simplifié :

X → MODÈLE → Ŷ

où :

- X = entrée ;
- Ŷ = prédiction.

# **D.2 — Paramètres**

Un modèle possède des paramètres internes ajustés pendant l'entraînement.

Dans un réseau neuronal, ce sont notamment les **poids**.

Le modèle cherche des valeurs permettant de produire de meilleures prédictions.

# **D.3 — Fonction de perte**

Le modèle doit savoir :

« À quel point suis-je mauvais ? »

La fonction de perte mesure l'écart entre :

réponse réelle

et

prédiction

Conceptuellement :

Prédiction  
↓  
Comparaison  
↓  
Erreur  
↓  
Loss

# **D.4 — Optimisation**

L'algorithme d'optimisation cherche à modifier les paramètres pour réduire la perte.

Conceptuellement :

paramètres  
↓  
prédiction  
↓  
loss  
↓  
ajustement  
↓  
nouveaux paramètres  
↓  
...

# **D.5 — Gradient descent**

La descente de gradient est une méthode fondamentale d'optimisation.

Idée simplifiée :

déterminer dans quelle direction modifier les paramètres pour réduire l'erreur.

Tu n'as pas besoin, à ton niveau actuel, de savoir dériver tous les gradients à la main.

Mais tu dois comprendre :

- pourquoi elle existe ;
- ce qu'elle optimise ;
- qu'elle agit sur les paramètres ;
- qu'elle est centrale dans l'entraînement de nombreux modèles.

# **D.6 — Learning rate**

Le **learning rate** détermine notamment l'amplitude des mises à jour pendant l'apprentissage.

Trop élevé :

apprentissage instable

Trop faible :

apprentissage très lent

# **D.7 — Epoch**

Une epoch correspond approximativement à un passage complet sur les données d'entraînement.

Exemple :

dataset  
↓  
epoch 1  
↓  
epoch 2  
↓  
epoch 3

# **D.8 — Batch**

Au lieu de traiter tout le dataset simultanément, les données sont souvent traitées par groupes.

dataset  
↓  
batch 1  
batch 2  
batch 3  
...

# **D.9 — Overfitting**

Le modèle apprend trop bien les données d'entraînement mais généralise mal.

TRAIN → excellent  
NOUVELLES DONNÉES → mauvais

C'est le modèle qui a essentiellement « mémorisé » certains détails plutôt qu'appris une généralisation robuste.

# **D.10 — Underfitting**

Le modèle est trop simple ou insuffisamment entraîné pour capturer les relations importantes.

TRAIN → mauvais  
TEST → mauvais

# **D.11 — Généralisation**

La vraie question n'est pas :

« Est-ce que le modèle connaît bien mes données ? »

mais :

**« Est-ce qu'il fonctionne correctement sur des données qu'il n'a jamais vues ? »**

C'est l'une des idées centrales du Machine Learning.

# **NIVEAU E — TRAIN / VALIDATION / TEST**

Une division classique :

Dataset  
│  
├── Training  
│  
├── Validation  
│  
└── Test

### **Training**

Pour apprendre.

### **Validation**

Pour comparer/configurer les choix pendant le développement.

### **Test**

Pour mesurer la performance finale sur des données réservées.

# **E.1 — Pourquoi séparer les données ?**

Parce que si tu évalues le modèle sur les mêmes données qu'il a utilisées pour apprendre, tu risques de surestimer ses performances.

# **E.2 — Cross-validation**

La cross-validation permet de réaliser plusieurs découpages afin d'obtenir une estimation plus robuste dans certains contextes.

Elle est particulièrement utile avec des datasets limités.

# **NIVEAU F — ÉVALUER UN MODÈLE**

Un modèle ne doit jamais être jugé par :

« Ça a l'air de marcher. »

Il faut définir des métriques.

# **F.1 — Accuracy**

Proportion de prédictions correctes.

Utile dans certains problèmes, mais dangereuse lorsqu'il existe un fort déséquilibre entre les classes.

# **F.2 — Precision**

Parmi les éléments prédits positifs :

combien sont réellement positifs ?

# **F.3 — Recall**

Parmi les éléments réellement positifs :

combien avons-nous détectés ?

# **F.4 — F1-score**

Combine precision et recall dans une métrique équilibrée selon une moyenne harmonique.

# **F.5 — Matrice de confusion**

Elle permet notamment de distinguer :

- vrais positifs ;
- vrais négatifs ;
- faux positifs ;
- faux négatifs.

PRÉDIT  
Positif Négatif  
RÉEL Positif TP FN  
Négatif FP TN

# **F.6 — Pourquoi les faux positifs/faux négatifs sont importants ?**

Imagine :

détection de fraude

Un faux positif :

transaction normale classée comme fraude.

Un faux négatif :

fraude classée comme normale.

Les conséquences peuvent être très différentes.

Donc :

**La bonne métrique dépend du problème métier.**

# **F.7 — ROC-AUC / PR-AUC**

Ces métriques permettent d'évaluer des modèles de classification selon différents seuils.

Tu dois surtout savoir :

- qu'elles existent ;
- pourquoi elles existent ;
- dans quels contextes elles peuvent être pertinentes ;
- qu'une seule métrique ne suffit pas toujours.

# **F.8 — Calibration**

Un modèle peut produire :

fraude = 0.90

La question est :

Est-ce que les prédictions à 90 % correspondent réellement à environ 90 % de probabilité ?

C'est le problème de la calibration.

Très important pour les systèmes de décision.

# **NIVEAU G — ALGORITHMES DE MACHINE LEARNING À RECONNAÎTRE**

Tu n'as pas besoin de maîtriser mathématiquement tous ces modèles immédiatement.

Mais tu dois savoir les situer.

## **G.1 — Régression linéaire**

Prédiction numérique avec une relation modélisée de manière linéaire.

## **G.2 — Régression logistique**

Malgré son nom, elle est couramment utilisée pour la classification.

## **G.3 — Decision Tree**

Modèle basé sur des décisions successives.

âge > 30 ?  
│  
┌─┴─┐  
Oui Non  
│ │  
...

Avantages :

- relativement interprétable ;
- utile sur données tabulaires.

## **G.4 — Random Forest**

Ensemble de nombreux arbres.

Idée :

Arbre 1 ─┐  
Arbre 2 ─┤  
Arbre 3 ─┤→ décision collective  
Arbre 4 ─┤  
Arbre N ─┘

## **G.5 — Gradient Boosting**

Construit progressivement des modèles qui cherchent à corriger les erreurs des précédents.

Famille extrêmement importante pour les données tabulaires.

Tu dois reconnaître notamment :

- XGBoost ;
- LightGBM ;
- CatBoost.

## **G.6 — SVM**

Support Vector Machine.

Méthode permettant notamment de trouver une frontière de séparation entre classes.

## **G.7 — KNN**

K-Nearest Neighbors.

Principe simplifié :

les éléments similaires ont tendance à appartenir à des catégories similaires.

## **G.8 — K-means**

Algorithme classique de clustering.

# **NIVEAU H — DEEP LEARNING**

# **H.1 — Réseau neuronal**

Un réseau neuronal est composé de couches de neurones artificiels.

Input  
↓  
Hidden Layer  
↓  
Hidden Layer  
↓  
Output

Chaque connexion possède notamment un poids.

# **H.2 — Neurone artificiel**

Schématiquement :

x₁ ──┐  
x₂ ──┼→ combinaison pondérée → activation → sortie  
x₃ ──┘

# **H.3 — Fonction d'activation**

Elle introduit une non-linéarité permettant au réseau de modéliser des relations complexes.

Tu dois reconnaître :

- ReLU ;
- sigmoid ;
- tanh ;
- softmax.

# **H.4 — CNN**

**Convolutional Neural Network.**

Historiquement particulièrement important pour la vision :

- classification d'images ;
- détection ;
- segmentation ;
- traitement spatial.

# **H.5 — RNN**

**Recurrent Neural Network.**

Conçu pour traiter des séquences avec une notion d'état précédent.

Historiquement important pour :

- texte ;
- séries temporelles ;
- audio.

# **H.6 — LSTM / GRU**

Variantes de réseaux récurrents permettant de mieux gérer certaines dépendances dans les séquences.

# **NIVEAU I — TRANSFORMERS**

Le Transformer est l'un des concepts les plus importants de l'IA moderne.

Il est à la base d'une immense partie des modèles actuels de langage et de nombreux modèles multimodaux.

# **I.1 — Pourquoi les Transformers ?**

Ils permettent notamment de traiter efficacement les relations entre différents éléments d'une séquence.

Concept central :

**attention**

# **I.2 — Attention**

L'attention permet au modèle d'accorder différents poids à différentes parties de l'entrée lorsqu'il produit une représentation ou une sortie.

Exemple simplifié :

Le développeur utilise Python parce qu'il est flexible.  
↑  
"il" → Python

Le modèle doit comprendre quelles parties du contexte sont pertinentes.

# **I.3 — Self-attention**

Chaque élément d'une séquence peut être mis en relation avec les autres éléments.

C'est fondamental dans l'architecture Transformer.

# **I.4 — Token**

Un modèle de langage ne lit pas nécessairement le texte exactement comme un humain.

Le texte est découpé en unités appelées **tokens**.

Texte  
↓  
Tokenisation  
↓  
tokens  
↓  
modèle

Un token peut correspondre à :

- un mot ;
- une partie de mot ;
- un symbole ;
- une ponctuation ;
- etc.

# **I.5 — Tokenisation**

La tokenisation transforme le texte en représentation exploitable par le modèle.

Elle influence :

- longueur du contexte ;
- coût ;
- capacité du modèle à traiter le texte ;
- traitement des langues.

# **I.6 — Context window**

La fenêtre de contexte correspond à la quantité maximale de tokens qu'un modèle peut prendre en compte dans une requête/contexte donné selon ses capacités et sa configuration.

Important :

**Un modèle ayant une grande fenêtre de contexte n'est pas automatiquement capable de comprendre parfaitement tout ce contexte.**

# **NIVEAU J — EMBEDDINGS**

Concept extrêmement important pour ton futur travail avec :

- RAG ;
- recherche sémantique ;
- recommandation ;
- classification ;
- clustering ;
- systèmes intelligents.

# **J.1 — Embedding**

Un embedding représente une information sous forme d'un vecteur numérique permettant de capturer certaines relations sémantiques.

Simplifié :

"chat"  
↓  
\[0.12, -0.83, 0.44, ...\]

# **J.2 — Pourquoi les embeddings ?**

Ils permettent de comparer des éléments selon leur proximité dans un espace vectoriel.

Par exemple :

"voiture"

peut être plus proche de :

"automobile"

que de :

"banane"

# **J.3 — Similarité**

On peut mesurer la proximité entre vecteurs.

Une méthode connue :

cosine similarity.

Tu n'as pas besoin de la dériver immédiatement, mais tu dois savoir qu'elle permet notamment de mesurer une proximité directionnelle entre embeddings.

# **NIVEAU K — LLM**

# **K.1 — Large Language Model**

Un **LLM** est un modèle de langage de grande taille entraîné sur d'importants volumes de données afin de modéliser et générer du langage.

Il peut notamment :

- générer ;
- résumer ;
- transformer ;
- classifier ;
- traduire ;
- expliquer ;
- produire du code ;
- extraire de l'information.

# **K.2 — Ce qu'un LLM n'est pas**

Un LLM n'est pas :

- une base de données parfaite ;
- une encyclopédie garantie ;
- une source de vérité absolue ;
- un moteur logique parfait ;
- un système automatiquement connecté au monde réel.

Il produit des sorties à partir de son fonctionnement et de son contexte.

# **K.3 — Préentraînement**

Pendant le préentraînement, le modèle apprend des régularités générales à partir de grandes quantités de données.

# **K.4 — Instruction tuning**

Le modèle peut ensuite être adapté pour mieux suivre des instructions.

# **K.5 — Alignment**

L'alignement vise notamment à rendre les comportements du modèle plus compatibles avec les objectifs et contraintes souhaités.

Il peut impliquer différentes techniques et processus.

# **K.6 — Inference**

L'inférence correspond à l'utilisation d'un modèle entraîné pour produire une sortie.

Input  
↓  
Modèle entraîné  
↓  
Inference  
↓  
Output

# **NIVEAU L — PROMPTING**

Le prompting n'est pas simplement :

« écrire une bonne phrase ».

C'est une manière de spécifier un problème au modèle.

# **L.1 — Prompt**

Un prompt peut contenir :

- objectif ;
- contexte ;
- données ;
- contraintes ;
- format attendu ;
- critères de qualité ;
- exemples ;
- règles ;
- limites ;
- méthode de vérification.

# **L.2 — Prompt vague**

Construis-moi un système RAG.

Problème :

l'IA doit inventer presque toute l'architecture.

# **L.3 — Prompt structuré**

OBJECTIF  
Construire...  
<br/>CONTEXTE  
...  
<br/>DONNÉES  
...  
<br/>CONTRAINTES  
...  
<br/>ARCHITECTURE  
...  
<br/>CRITÈRES  
...  
<br/>GESTION DES ERREURS  
...  
<br/>SÉCURITÉ  
...  
<br/>ÉVALUATION  
...  
<br/>LIVRABLES  
...  
<br/>AVANT D'IMPLÉMENTER  
Explique les choix...

Cela réduit énormément l'espace d'interprétation.

# **L.4 — Few-shot prompting**

On fournit quelques exemples du comportement attendu.

Exemple 1  
entrée → sortie  
<br/>Exemple 2  
entrée → sortie  
<br/>Nouvelle entrée  
→ ?

# **L.5 — Structured output**

Lorsque le système doit être consommé par un programme, il est souvent préférable de demander un format strict :

{  
"category": "...",  
"confidence": 0.0,  
"reason": "..."  
}

Cela permet de séparer :

raisonnement / texte libre

de :

données machine-readable

# **NIVEAU M — RAG**

Le RAG est un concept que tu dois absolument maîtriser.

# **M.1 — Retrieval-Augmented Generation**

Le principe :

QUESTION  
↓  
RECHERCHE DE DOCUMENTS  
↓  
DOCUMENTS PERTINENTS  
↓  
CONTEXTE  
↓  
LLM  
↓  
RÉPONSE

Au lieu de demander au modèle de répondre uniquement avec ses connaissances internes, on lui fournit des informations récupérées.

# **M.2 — Pourquoi le RAG existe ?**

Pour permettre notamment :

- utilisation de documents privés ;
- connaissances spécifiques ;
- informations actualisées ;
- recherche documentaire ;
- réponses contextualisées.

# **M.3 — Pipeline RAG**

Un système RAG peut être construit comme :

DOCUMENTS  
↓  
Extraction  
↓  
Nettoyage  
↓  
Chunking  
↓  
Embeddings  
↓  
Vector Database  
↓  
Retrieval  
↓  
Context  
↓  
LLM  
↓  
Answer

# **M.4 — Chunking**

Les documents sont découpés en morceaux.

Mauvais chunking :

chunks trop grands  
→ contexte bruité

ou :

chunks trop petits  
→ contexte fragmenté

Le chunking est donc une vraie décision d'architecture.

# **M.5 — Vector database**

Une base vectorielle permet notamment de stocker et rechercher des représentations vectorielles.

Exemples à reconnaître :

- pgvector ;
- Pinecone ;
- Weaviate ;
- Qdrant ;
- Milvus.

Tu n'as pas besoin de tous les maîtriser.

Tu dois savoir :

**Pourquoi une base vectorielle intervient dans un RAG.**

# **M.6 — Retrieval**

Le système doit récupérer les passages pertinents.

Deux grandes approches à connaître :

### **Recherche lexicale**

Basée notamment sur les termes.

### **Recherche sémantique**

Basée notamment sur les embeddings.

# **M.7 — Hybrid search**

Combine plusieurs mécanismes de recherche.

lexical  
+  
semantic  
↓  
hybrid retrieval

# **M.8 — Reranking**

Après récupération des documents, un second mécanisme peut réordonner les résultats pour sélectionner les passages les plus pertinents.

# **M.9 — Grounding**

Une réponse est davantage « grounded » lorsqu'elle s'appuie explicitement sur des informations récupérées ou vérifiables plutôt que sur une génération non contrainte.

# **M.10 — Hallucination**

Un LLM peut générer une information fausse avec un ton très convaincant.

Exemple :

Réponse :  
"Cette entreprise a été fondée en 1987."  
<br/>Réalité :  
aucune preuve.

Le problème n'est donc pas uniquement :

« l'IA peut se tromper ».

Le problème est :

**elle peut produire une erreur qui ressemble à une réponse certaine.**

# **M.11 — Comment réduire les hallucinations ?**

Approches possibles :

- RAG ;
- sources ;
- outils externes ;
- contraintes ;
- validation ;
- structured output ;
- vérification indépendante ;
- human-in-the-loop ;
- limitation du domaine ;
- refus lorsqu'information insuffisante.

# **NIVEAU N — FINE-TUNING**

# **N.1 — Définition**

Le fine-tuning consiste à adapter un modèle préexistant avec des données supplémentaires afin de modifier ou spécialiser certains comportements.

# **N.2 — Fine-tuning ≠ RAG**

C'est une confusion extrêmement fréquente.

### **RAG**

On fournit des informations au moment de l'utilisation.

Question  
↓  
Recherche  
↓  
Contexte  
↓  
Modèle

### **Fine-tuning**

On modifie les paramètres du modèle via un processus d'entraînement supplémentaire.

Modèle préexistant  
↓  
données spécialisées  
↓  
entraînement supplémentaire  
↓  
modèle adapté

# **N.3 — Quand penser au RAG ?**

Lorsque le problème principal est :

**« Le modèle doit avoir accès à des connaissances spécifiques. »**

# **N.4 — Quand penser au fine-tuning ?**

Lorsque le problème est davantage :

**« Le comportement, le style, la tâche ou certaines capacités doivent être spécialisés. »**

Mais il ne faut jamais partir automatiquement vers le fine-tuning.

# **N.5 — PEFT / LoRA**

À reconnaître :

- PEFT ;
- LoRA ;
- QLoRA.

Ces techniques permettent notamment d'adapter efficacement certains modèles sans modifier tous leurs paramètres de la même manière qu'un entraînement complet.

# **NIVEAU O — IA LOCALE VS IA CLOUD**

# **O.1 — Cloud AI**

Le modèle tourne sur une infrastructure distante.

Application  
↓ Internet  
API  
↓  
Modèle distant  
↓  
Réponse

Avantages :

- modèles puissants ;
- infrastructure gérée ;
- mise à l'échelle ;
- accès rapide aux nouveaux modèles.

Inconvénients :

- coût ;
- dépendance fournisseur ;
- latence réseau ;
- questions de confidentialité ;
- disponibilité ;
- limites d'API.

# **O.2 — Local AI**

Le modèle tourne sur ta machine ou ton infrastructure.

Application  
↓  
Machine locale  
↓  
Modèle

Avantages :

- confidentialité potentiellement meilleure ;
- fonctionnement hors ligne selon architecture ;
- contrôle ;
- coûts d'inférence potentiellement réduits après investissement matériel.

Inconvénients :

- matériel ;
- RAM/VRAM ;
- performances ;
- maintenance ;
- modèles parfois moins puissants.

# **O.3 — Quantization**

La quantification réduit notamment la précision numérique utilisée pour représenter les paramètres du modèle.

Objectifs :

- réduire la mémoire ;
- faciliter l'exécution locale ;
- accélérer certaines inférences.

Contrepartie possible :

- perte de qualité selon la méthode et le modèle.

# **O.4 — Ollama**

Ollama est un outil permettant notamment d'exécuter et de gérer certains modèles localement.

Tu dois surtout comprendre :

Ollama  
≠  
modèle

Ollama est l'environnement/outillage d'exécution.

Le modèle est autre chose.

# **O.5 — API de modèle**

Une application peut appeler un modèle distant via API.

Frontend  
↓  
Backend  
↓  
AI API  
↓  
Model

Point de sécurité essentiel :

**Une clé API ne doit généralement pas être exposée directement dans le frontend public.**

# **NIVEAU P — MULTIMODALITÉ**

Une IA multimodale peut travailler avec plusieurs types de données.

Par exemple :

texte  
image  
audio  
vidéo

# **P.1 — Vision**

Applications :

- classification ;
- détection d'objets ;
- OCR ;
- segmentation ;
- analyse d'images.

# **P.2 — OCR**

**Optical Character Recognition**

Transforme une image contenant du texte en texte exploitable.

photo facture  
↓  
OCR  
↓  
texte  
↓  
extraction structurée

# **P.3 — Speech-to-Text**

Transforme l'audio en texte.

audio → transcription

# **P.4 — Text-to-Speech**

Transforme du texte en voix.

texte → voix

# **P.5 — Audio intelligence**

Peut inclure :

- transcription ;
- diarisation ;
- classification audio ;
- détection d'événements ;
- analyse vocale.

# **NIVEAU Q — AGENTS ET SYSTÈMES À OUTILS**

Un agent est plus qu'un chatbot.

# **Q.1 — Chatbot simple**

User  
↓  
LLM  
↓  
Response

# **Q.2 — Système avec outils**

User  
↓  
LLM  
↓  
Tool selection  
├── database  
├── web  
├── API  
├── calculator  
└── code execution  
↓  
Result  
↓  
LLM  
↓  
Response

# **Q.3 — Agent**

Conceptuellement :

OBJECTIF  
↓  
OBSERVATION  
↓  
PLAN / DÉCISION  
↓  
ACTION  
↓  
RÉSULTAT  
↓  
NOUVELLE OBSERVATION  
↓  
...

L'agent peut donc avoir :

- un objectif ;
- un état ;
- des outils ;
- une mémoire ;
- des boucles ;
- des critères d'arrêt.

# **Q.4 — Tool calling**

Le modèle peut produire une demande structurée :

{  
"tool": "get_weather",  
"arguments": {  
"city": "Cotonou"  
}  
}

Le programme exécute réellement l'outil.

C'est fondamental :

**Le LLM ne fait pas nécessairement l'action lui-même.**

Il peut demander à ton application de l'effectuer.

# **Q.5 — Agentic workflow**

Il faut distinguer :

### **Workflow déterministe**

A → B → C → D

### **Workflow agentique**

objectif  
↓  
choix de l'action  
↓  
outil  
↓  
observation  
↓  
choix suivant

Un agent est donc utile lorsque la séquence d'actions ne peut pas être entièrement déterminée à l'avance.

# **Q.6 — Quand NE PAS utiliser un agent**

Très important.

Si le processus est :

A → B → C

et toujours identique :

un workflow classique est souvent préférable.

Un agent ajoute :

- complexité ;
- coût ;
- imprévisibilité ;
- surface d'erreur ;
- surface de sécurité.

# **NIVEAU R — MEMORY**

Le terme « mémoire » peut désigner plusieurs choses.

# **R.1 — Context memory**

Ce que le modèle reçoit dans la conversation actuelle.

# **R.2 — Conversation history**

Historique conservé par l'application.

# **R.3 — External memory**

Informations stockées dans :

- base SQL ;
- vector database ;
- fichiers ;
- système documentaire.

# **R.4 — Long-term memory**

Une application peut conserver certaines informations utiles d'une interaction à l'autre.

Mais :

mémoire ≠ intelligence.

Une mémoire mal conçue peut également introduire :

- erreurs ;
- informations obsolètes ;
- problèmes de confidentialité ;
- contradictions.

# **NIVEAU S — AI ENGINEERING**

À ce stade, il faut passer du modèle à l'application.

# **S.1 — Architecture générale**

Une application IA peut ressembler à :

USER  
↓  
FRONTEND  
↓  
BACKEND  
↓  
ORCHESTRATION  
├── LLM  
├── RAG  
├── DATABASE  
├── TOOLS  
├── MEMORY  
└── BUSINESS LOGIC  
↓  
VALIDATION  
↓  
RESPONSE

# **S.2 — AI application ≠ model**

Tu peux utiliser un modèle existant et construire une application très complexe autour.

La valeur peut être dans :

- données ;
- UX ;
- workflow ;
- intégration ;
- contexte ;
- sécurité ;
- spécialisation ;
- orchestration ;
- validation.

# **S.3 — AI orchestration**

L'orchestration consiste à coordonner :

- modèles ;
- outils ;
- mémoire ;
- retrieval ;
- logique métier ;
- validation ;
- appels API.

# **S.4 — Model routing**

Une application peut choisir différents modèles selon la tâche.

requête  
↓  
router  
├── tâche simple → petit modèle  
├── tâche complexe → modèle puissant  
├── vision → modèle multimodal  
└── local/private → modèle local

Objectif :

optimiser qualité, coût, latence et confidentialité.

# **S.5 — Latency**

Temps nécessaire pour obtenir le résultat.

# **S.6 — Throughput**

Quantité de requêtes traitées sur une période donnée.

# **S.7 — Cost per request**

Coût d'une interaction.

Dans une application IA commerciale :

coût IA  
+  
infrastructure  
+  
stockage  
+  
réseau  
+  
outils  
+  
monitoring

doit être compatible avec :

revenus / valeur créée

# **NIVEAU T — MLOPS / LLMOPS**

Un modèle en laboratoire n'est pas encore un produit fiable.

# **T.1 — MLOps**

Ensemble de pratiques permettant de gérer le cycle de vie des modèles ML :

data  
↓  
training  
↓  
evaluation  
↓  
deployment  
↓  
monitoring  
↓  
retraining

# **T.2 — LLMOps**

Extension/adaptation de ces pratiques aux systèmes utilisant notamment des LLM.

On surveille notamment :

- qualité ;
- coût ;
- latence ;
- erreurs ;
- tokens ;
- prompts ;
- retrieval ;
- sécurité ;
- régressions.

# **T.3 — Model registry**

Système permettant notamment de gérer les versions des modèles.

# **T.4 — Dataset versioning**

Les datasets doivent parfois être versionnés.

Pourquoi ?

Parce que :

Modèle v2

peut avoir été entraîné sur :

Dataset v17

et il faut pouvoir retrouver ce contexte.

# **T.5 — Experiment tracking**

On doit pouvoir savoir :

modèle  
+  
dataset  
+  
hyperparamètres  
+  
version code  
+  
métriques  
\=  
expérience

# **T.6 — Model drift**

La réalité peut changer.

Exemple :

données 2025  
↓  
modèle

Mais en 2027 :

comportement utilisateurs changé  
marché changé  
attaques changées  
vocabulaire changé

Le modèle peut devenir moins performant.

# **T.7 — Data drift**

Les données d'entrée changent.

# **T.8 — Concept drift**

La relation entre les données et la cible change.

C'est plus profond.

X → Y

qui fonctionnait auparavant peut ne plus fonctionner de la même manière.

# **NIVEAU U — ÉVALUATION DES LLM**

Une réponse qui « semble bonne » n'est pas une métrique.

# **U.1 — Evaluation dataset**

Créer un ensemble de cas représentatifs.

Question 1 → expected behavior  
Question 2 → expected behavior  
...

Puis tester différentes versions du système.

# **U.2 — Golden dataset**

Ensemble de cas de référence utilisé pour comparer les versions.

# **U.3 — Evaluation automatique**

Certaines dimensions peuvent être évaluées automatiquement.

Mais :

automatiser l'évaluation ne signifie pas que l'évaluation est parfaite.

# **U.4 — Human evaluation**

Des humains évaluent les réponses selon des critères.

Exemples :

- exactitude ;
- pertinence ;
- sécurité ;
- ton ;
- fidélité aux sources ;
- utilité.

# **U.5 — Regression testing**

Lorsqu'une nouvelle version est déployée :

vérifie-t-elle que les anciennes capacités importantes fonctionnent toujours ?

# **U.6 — LLM-as-a-judge**

Un LLM peut être utilisé pour évaluer d'autres réponses.

C'est utile dans certains contextes, mais comporte ses propres biais.

Donc :

**ne jamais considérer automatiquement un LLM juge comme une vérité absolue.**

# **NIVEAU V — IA + SÉCURITÉ**

C'est ici que ton Document 03 rejoint le Document 05.

# **V.1 — Prompt injection**

Un utilisateur peut tenter d'influencer le comportement du système via une instruction malveillante.

Exemple conceptuel :

Document externe :  
"Ignore les instructions précédentes..."

Si ton système RAG traite ce document comme une instruction, il peut être manipulé.

# **V.2 — Indirect prompt injection**

L'instruction malveillante n'est pas nécessairement fournie directement par l'utilisateur.

Elle peut être présente dans :

- une page web ;
- un document ;
- un email ;
- une base de données ;
- une donnée récupérée.

# **V.3 — Data exfiltration**

Un système connecté à des données privées peut être manipulé pour révéler des informations qu'il ne devrait pas exposer.

# **V.4 — Excessive agency**

Un agent possède trop de permissions.

Exemple dangereux :

LLM  
↓  
accès complet à la base  
↓  
suppression possible

Meilleure approche :

LLM  
↓  
outil limité  
↓  
permission contrôlée  
↓  
validation

# **V.5 — Human-in-the-loop**

Certaines actions sensibles nécessitent une validation humaine.

Agent  
↓  
action sensible  
↓  
validation humaine  
↓  
exécution

Exemples :

- transfert d'argent ;
- suppression de données ;
- envoi massif ;
- décision médicale ;
- décision juridique ;
- action administrative critique.

# **V.6 — Secrets**

Ne jamais exposer inutilement :

- clés API ;
- tokens ;
- credentials ;
- données privées.

Une IA qui génère du code doit être auditée comme n'importe quel développeur.

# **V.7 — Permissions minimales**

Principe :

donner au système uniquement les permissions nécessaires.

C'est le **principle of least privilege**.

# **NIVEAU W — IA RESPONSABLE**

Un système IA doit aussi être évalué sur :

- confidentialité ;
- biais ;
- sécurité ;
- explicabilité ;
- robustesse ;
- traçabilité ;
- responsabilité ;
- conformité ;
- impact utilisateur.

# **W.1 — Human-in-the-loop**

L'humain conserve un rôle dans les décisions importantes.

# **W.2 — Human-on-the-loop**

Le système fonctionne de manière plus autonome, mais l'humain supervise.

# **W.3 — Human-out-of-the-loop**

Le système agit sans intervention humaine directe.

Plus l'autonomie augmente :

plus les mécanismes de contrôle deviennent importants.

# **NIVEAU X — CHOISIR LA BONNE TECHNOLOGIE**

C'est probablement la partie la plus importante pour ton objectif.

# **X.1 — Ne commence jamais par le modèle**

Commence par :

**Quel problème devons-nous résoudre ?**

Puis :

Problème  
↓  
objectif  
↓  
données disponibles  
↓  
niveau de précision requis  
↓  
contraintes  
↓  
méthode

# **X.2 — Règles ou Machine Learning ?**

Utilise plutôt des règles si :

- logique simple ;
- règles stables ;
- résultat déterministe ;
- données insuffisantes.

Utilise ML si :

- relations difficiles à expliciter ;
- données disponibles ;
- besoin de prédiction/classification.

# **X.3 — ML classique ou Deep Learning ?**

ML classique souvent intéressant lorsque :

- données tabulaires ;
- dataset relativement limité ;
- besoin d'interprétabilité ;
- problème classique.

Deep Learning souvent pertinent lorsque :

- données complexes ;
- images ;
- audio ;
- langage ;
- très grands datasets ;
- représentation difficile à définir manuellement.

# **X.4 — API LLM ou modèle local ?**

Pose :

Confidentialité ?  
Coût ?  
Latence ?  
Puissance nécessaire ?  
Connexion Internet ?  
Matériel disponible ?  
Volume ?

# **X.5 — Prompting ou RAG ?**

Si le problème est :

« Le modèle ne connaît pas mes documents. »

→ pense RAG.

Si le problème est :

« Le modèle répond mal à cause d'instructions insuffisamment structurées. »

→ prompting.

# **X.6 — RAG ou fine-tuning ?**

|     |     |
| --- | --- |
| **Besoin** | **Première piste** |
| connaissances privées | RAG |
| informations actualisées | RAG |
| citations de sources | RAG |
| style spécifique | fine-tuning possible |
| format/comportement spécialisé | fine-tuning possible |
| connaissances qui changent souvent | RAG |
| comportement stable à grande échelle | fine-tuning possible |

Ce tableau est une orientation, pas une règle absolue.

# **X.7 — Workflow ou agent ?**

Séquence connue ?  
│  
┌───┴───┐  
OUI NON  
│ │  
workflow agent

Mais même lorsqu'un agent est possible :

commence par demander si un workflow déterministe suffit.

# **NIVEAU Y — COMMENT DIRIGER UNE IA QUI CONSTRUIT UN SYSTÈME IA**

À partir de maintenant, ton rôle change.

Tu ne dois plus dire simplement :

« Fais-moi un chatbot IA. »

Tu dois agir comme un **AI Product/Technical Lead assisté par IA**.

# **Y.1 — Étape 1 : définir le problème**

Demande :

Quel problème utilisateur voulons-nous résoudre ?

# **Y.2 — Étape 2 : définir la sortie**

Exemple :

entrée :  
transaction  
<br/>sortie :  
fraude = oui/non  
score = 0–1

# **Y.3 — Étape 3 : définir les contraintes**

latence < X  
coût < Y  
confidentialité  
disponibilité  
précision  
volume

# **Y.4 — Étape 4 : demander plusieurs architectures**

Ne demande pas :

« Construis la meilleure architecture. »

Demande :

« Propose trois architectures possibles, compare-les selon coût, précision, complexité, maintenance, sécurité et évolutivité, puis recommande-en une. »

# **Y.5 — Étape 5 : forcer les hypothèses**

Demande :

Liste toutes tes hypothèses.  
Ne suppose pas qu'une donnée existe.  
Signale les informations manquantes.

# **Y.6 — Étape 6 : imposer un plan avant le code**

1\. architecture  
2\. données  
3\. modèle  
4\. évaluation  
5\. sécurité  
6\. intégration  
7\. monitoring  
8\. tests  
9\. déploiement

Puis seulement :

implémentation.

# **Y.7 — Étape 7 : demander des critères d'acceptation**

Exemple :

Le système est acceptable si :  
<br/>\- accuracy ≥ X  
\- recall ≥ Y  
\- latence < Z  
\- aucune donnée sensible exposée  
\- toutes les requêtes sont journalisées  
\- fallback fonctionnel

# **NIVEAU Z — COMMENT AUDITER LE TRAVAIL D'UNE IA**

C'est ici que ta culture IA devient réellement utile.

# **Z.1 — Ne jamais demander seulement :**

« Est-ce correct ? »

Une IA peut très bien répondre :

« Oui, c'est correct. »

Demande plutôt :

### **Architecture**

« Explique pourquoi cette architecture répond au problème. »

### **Hypothèses**

« Liste toutes les hypothèses utilisées. »

### **Alternatives**

« Quelles architectures concurrentes étaient possibles ? »

### **Risques**

« Quels sont les principaux modes d'échec ? »

### **Données**

« Comment sais-tu que les données sont suffisantes ? »

### **Évaluation**

« Comment mesures-tu objectivement la qualité ? »

### **Sécurité**

« Quelles attaques ou fuites sont possibles ? »

### **Production**

« Comment surveillerais-tu ce système en production ? »

# **Z.2 — Le test du contre-exemple**

Demande :

« Donne-moi des cas dans lesquels ton approche échouerait. »

Puis :

« Construis des tests pour ces cas. »

# **Z.3 — Le test adversarial**

Demande :

« Essaie maintenant de casser ton propre système. »

L'IA doit chercher :

- entrées extrêmes ;
- données malformées ;
- ambiguïtés ;
- prompt injection ;
- contexte absent ;
- informations contradictoires ;
- données hors distribution.

# **Z.4 — Le test d'abstention**

Un bon système doit parfois pouvoir dire :

« Je ne sais pas. »

Donc demande :

« Que fait le système lorsqu'il n'a pas suffisamment d'informations pour répondre ? »

# **Z.5 — Le test de confiance**

Ne confonds jamais :

confidence du modèle

avec :

vérité réelle

Une prédiction très confiante peut être fausse.

# **Z.6 — Le test de provenance**

Pour une application utilisant des connaissances :

Réponse  
↓  
Sources ?  
↓  
Passages utilisés ?  
↓  
Correspondance ?

Particulièrement important pour RAG.

# **Z.7 — Le test de reproductibilité**

Demande :

« Peut-on reproduire ce résultat avec la même configuration ? »

Il faut pouvoir retrouver :

- version du modèle ;
- prompt ;
- données ;
- paramètres ;
- code ;
- environnement.

# **Z.8 — Le test de régression**

Après modification :

ancienne version  
↓  
tests  
↓  
nouvelle version  
↓  
tests  
↓  
comparaison

# **NIVEAU AA — LE STANDARD STANE POUR LES PROJETS IA**

À partir de ce document, voici le standard que tu peux utiliser pour tout projet IA.

## **1\. PROBLÈME**

Quel problème réel résout-on ?

## **2\. UTILISATEUR**

Pour qui ?

## **3\. OBJECTIF**

Quel résultat doit être obtenu ?

## **4\. INPUT**

Quelles données entrent ?

## **5\. OUTPUT**

Quelle sortie attend-on ?

## **6\. MÉTHODE**

Pourquoi IA ?  
Pourquoi cette approche ?  
Pourquoi ce modèle ?

## **7\. DONNÉES**

Source  
qualité  
volume  
représentativité  
biais  
fraîcheur  
privacy

## **8\. ÉVALUATION**

Quelle métrique ?  
Quel seuil ?  
Quel dataset de test ?  
Quels cas limites ?

## **9\. SÉCURITÉ**

Quelles données sensibles ?  
Quelles permissions ?  
Quels abus possibles ?  
Prompt injection ?  
Data leakage ?

## **10\. PERFORMANCE**

latence  
coût  
throughput  
mémoire  
CPU/GPU

## **11\. ROBUSTESSE**

Que se passe-t-il si :  
\- données manquantes ?  
\- données incorrectes ?  
\- requête ambiguë ?  
\- modèle indisponible ?  
\- contexte absent ?

## **12\. EXPLICABILITÉ**

Peut-on comprendre pourquoi le système produit ce résultat ?

## **13\. MONITORING**

qualité  
coût  
latence  
erreurs  
drift  
sécurité

## **14\. FALLBACK**

Que fait le système si l'IA échoue ?

## **15\. HUMAIN**

Quand faut-il demander une validation humaine ?

# **NIVEAU AB — LE « AI DECISION TREE » DE STANE**

Lorsqu'une idée de projet arrive, parcours cette séquence.

PROBLÈME  
│  
▼  
Une IA est-elle  
nécessaire ?  
/ \\  
NON OUI  
│ │  
solution classique ▼  
Données disponibles ?  
/ \\  
NON OUI  
│ │  
collecte / règles ▼  
Quel type ?  
┌────────────┼────────────┐  
│ │ │  
prédire générer décider  
│ │ │  
ML LLM agent/RL  
│ │ │  
▼ ▼ ▼  
modèle adapté RAG ? workflow ?  
│ │  
fine-tuning ? agent ?  
│  
▼  
évaluation  
│  
▼  
sécurité  
│  
▼  
déploiement  
│  
▼  
monitoring

# **NIVEAU AC — LES CONFUSIONS QUE TU DOIS ABSOLUMENT ÉVITER**

## **AI vs ML**

**IA** = domaine large.

**ML** = sous-domaine de l'IA basé sur l'apprentissage à partir de données.

## **ML vs Deep Learning**

**Deep Learning** = sous-ensemble du ML utilisant notamment des réseaux neuronaux profonds.

## **LLM vs IA**

Un LLM est un type de modèle d'IA spécialisé dans le langage.

## **LLM vs chatbot**

Un LLM est un modèle.

Un chatbot est une application pouvant utiliser un LLM.

## **RAG vs fine-tuning**

RAG :

apporter des connaissances au moment de l'utilisation.

Fine-tuning :

adapter le modèle par entraînement supplémentaire.

## **Embedding vs LLM**

Embedding :

représentation vectorielle.

LLM :

modèle génératif/de langage.

## **Vector database vs database classique**

Une base SQL classique stocke notamment des données structurées.

Une base vectorielle permet notamment de rechercher selon la proximité entre vecteurs.

Les deux peuvent coexister.

## **Prompt vs modèle**

Le prompt donne les instructions/contexte.

Le modèle est le moteur qui traite ces informations.

## **Training vs inference**

Training :

apprendre.

Inference :

utiliser le modèle entraîné.

## **Confidence vs correctness**

confiance élevée  
≠  
vérité garantie

## **Agent vs automation**

Automation :

règles définies

Agent :

système capable de choisir certaines actions

# **NIVEAU AD — QUAND DOIS-TU PENSER À CHAQUE CONCEPT ?**

Voici la carte mentale opérationnelle.

|     |     |
| --- | --- |
| **Si tu rencontres…** | **Pense à…** |
| prédire une valeur | régression |
| choisir une catégorie | classification |
| découvrir des groupes | clustering |
| données avec labels | supervised learning |
| énormément de données non annotées | self-supervised |
| récompense/action | reinforcement learning |
| images complexes | deep learning / vision |
| texte complexe | Transformers / LLM |
| documents privés | RAG |
| recherche sémantique | embeddings |
| stockage vectoriel | vector database |
| style/comportement spécialisé | fine-tuning |
| plusieurs outils | tool calling |
| décisions dynamiques | agent |
| séquence fixe | workflow |
| exécution locale | local model |
| forte confidentialité | local/private deployment |
| besoin de modèle très puissant | cloud API possible |
| erreurs répétées | evaluation |
| baisse de performance | drift |
| réponses inventées | hallucination |
| données contaminées | data leakage |
| action dangereuse | human-in-the-loop |
| modèle difficile à comparer | benchmark/evaluation dataset |
| système en production | monitoring/MLOps |

# **NIVEAU AE — COMMENT DEMANDER À L'IA DE NE PAS « FAIRE SEMBLANT »**

Une des règles les plus importantes :

**Ne demande jamais uniquement à l'IA de construire. Demande-lui également de justifier, tester et critiquer.**

## **Prompt d'architecture**

Tu es l'architecte IA du projet.  
<br/>Avant toute implémentation :  
<br/>1\. reformule le problème ;  
2\. identifie les objectifs ;  
3\. liste les données nécessaires ;  
4\. liste les données réellement disponibles ;  
5\. identifie les contraintes ;  
6\. propose au moins trois architectures ;  
7\. compare-les ;  
8\. explique les compromis ;  
9\. identifie les risques ;  
10\. recommande une architecture.  
<br/>Ne commence pas le code avant cette analyse.  
Signale explicitement toute hypothèse non vérifiée.

# **Prompt de sélection du modèle**

Compare les modèles/approches possibles pour ce problème.  
<br/>Pour chacun, analyse :  
<br/>\- précision attendue ;  
\- données nécessaires ;  
\- coût ;  
\- latence ;  
\- complexité ;  
\- maintenance ;  
\- confidentialité ;  
\- explicabilité ;  
\- scalabilité ;  
\- risques.  
<br/>Ne recommande pas le modèle le plus puissant par défaut.  
Recherche la solution la plus adaptée au problème.

# **Prompt d'audit**

Agis maintenant comme un reviewer indépendant.  
<br/>Tu dois essayer de trouver des erreurs dans ta propre solution.  
<br/>Analyse :  
<br/>1\. architecture ;  
2\. données ;  
3\. preprocessing ;  
4\. modèle ;  
5\. entraînement ;  
6\. métriques ;  
7\. sécurité ;  
8\. confidentialité ;  
9\. performance ;  
10\. cas limites ;  
11\. hallucinations ;  
12\. monitoring ;  
13\. maintenance.  
<br/>Pour chaque problème :  
\- gravité ;  
\- pourquoi c'est un problème ;  
\- preuve ;  
\- correction ;  
\- méthode de vérification.

# **Prompt anti-complexité**

Cherche maintenant à simplifier l'architecture.  
<br/>Pour chaque composant :  
\- est-il réellement nécessaire ?  
\- peut-il être supprimé ?  
\- peut-il être remplacé par une solution déterministe ?  
\- apporte-t-il suffisamment de valeur pour justifier sa complexité ?  
<br/>Ne conserve un composant que si sa valeur est démontrable.

# **NIVEAU AF — LA BOUCLE COMPLÈTE D'UN PROJET IA**

Voici le cycle que tu dois progressivement internaliser :

┌──────────────────┐  
│ PROBLÈME │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ DONNÉES │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ APPROCHE │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ MODÈLE │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ ÉVALUATION │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ INTÉGRATION │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ DÉPLOIEMENT │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ MONITORING │  
└────────┬─────────┘  
↓  
┌──────────────────┐  
│ FEEDBACK │  
└────────┬─────────┘  
│  
└──────────→ amélioration

# **NIVEAU AG — L'IA COMME COMPOSANT, PAS COMME MAGIE**

Une erreur fondamentale serait de concevoir un produit comme :

APP  
↓  
AI  
↓  
MAGIE

Une architecture mature ressemble davantage à :

APPLICATION  
│  
┌─────────────┼─────────────┐  
│ │ │  
logique données IA  
métier │  
│ │  
│ ┌────────┼────────┐  
│ │ │ │  
DB LLM RAG Tools  
│ │ │ │  
└────────────────┼────────┼────────┘  
│  
VALIDATION  
│  
OUTPUT

L'IA n'est donc qu'un **composant du système**.

# **NIVEAU AH — LES PRINCIPES DE CONCEPTION À RETENIR**

## **Principe 1**

**Commencer par le problème, jamais par le modèle.**

## **Principe 2**

**Utiliser l'IA seulement lorsqu'elle apporte une valeur réelle.**

## **Principe 3**

**Préférer la solution la plus simple qui atteint l'objectif.**

## **Principe 4**

**Une bonne donnée vaut parfois mieux qu'un modèle plus complexe.**

## **Principe 5**

**Une métrique doit être liée au problème réel.**

## **Principe 6**

**Une démonstration réussie ne prouve pas la robustesse.**

## **Principe 7**

**Un modèle puissant peut toujours produire une erreur.**

## **Principe 8**

**Plus un système est autonome, plus ses garde-fous doivent être forts.**

## **Principe 9**

**Une IA doit être testée comme un composant logiciel critique.**

## **Principe 10**

**Toute sortie importante doit avoir un mécanisme de contrôle approprié.**

# **NIVEAU AI — CHECKLIST DE CULTURE IA**

Avant de considérer que tu comprends suffisamment un système IA, tu dois pouvoir répondre à ces questions.

### **Problème**

- Quel problème résout-il ?
- Pourquoi l'IA est-elle nécessaire ?
- Pourquoi une solution classique ne suffit-elle pas ?

### **Données**

- Quelles données utilise-t-il ?
- Sont-elles suffisamment nombreuses ?
- Sont-elles représentatives ?
- Sont-elles propres ?
- Y a-t-il du leakage ?

### **Modèle**

- Quel type de modèle ?
- Pourquoi celui-ci ?
- Quelles alternatives ?

### **Entraînement**

- Comment apprend-il ?
- Quelle loss ?
- Quels paramètres ?
- Comment éviter l'overfitting ?

### **Évaluation**

- Quelle métrique ?
- Pourquoi ?
- Sur quel dataset ?
- Quels cas limites ?

### **Application**

- Où tourne le modèle ?
- Comment l'application l'appelle-t-elle ?
- Quel est le coût ?
- Quelle latence ?

### **Sécurité**

- Quelles données sont sensibles ?
- Quelles permissions ?
- Quelles attaques ?
- Quel fallback ?

### **Production**

- Comment surveiller ?
- Comment détecter le drift ?
- Comment versionner ?
- Comment revenir à une version précédente ?

### **IA générative**

- Hallucination ?
- RAG ?
- Sources ?
- Prompt injection ?
- Tool calling ?
- Human-in-the-loop ?

# **NIVEAU AJ — VOCABULAIRE À SAVOIR RECONNAÎTRE**

Tu n'as pas encore besoin de maîtriser chaque terme, mais tu dois pouvoir comprendre sa place lorsqu'il apparaît.

### **Fondamentaux**

- AI
- ML
- Deep Learning
- supervised learning
- unsupervised learning
- self-supervised learning
- reinforcement learning
- dataset
- feature
- label
- target
- training
- validation
- test
- model
- parameter
- hyperparameter
- loss
- optimizer
- gradient
- epoch
- batch
- learning rate

### **ML**

- regression
- classification
- clustering
- anomaly detection
- decision tree
- random forest
- gradient boosting
- XGBoost
- LightGBM
- CatBoost
- SVM
- KNN

### **Deep Learning**

- neural network
- neuron
- layer
- weight
- activation function
- backpropagation
- CNN
- RNN
- LSTM
- GRU
- Transformer
- attention
- self-attention

### **LLM**

- token
- tokenizer
- context window
- embedding
- LLM
- pretraining
- instruction tuning
- alignment
- inference
- temperature
- sampling
- hallucination
- multimodal

### **GenAI**

- prompting
- few-shot
- structured output
- RAG
- chunking
- retrieval
- reranking
- grounding
- vector database
- fine-tuning
- LoRA
- QLoRA
- PEFT

### **AI Engineering**

- tool calling
- function calling
- agent
- workflow
- orchestration
- memory
- model routing
- guardrails
- fallback
- human-in-the-loop
- evaluation
- observability

### **Production**

- MLOps
- LLMOps
- deployment
- monitoring
- drift
- data drift
- concept drift
- model registry
- experiment tracking
- dataset versioning
- latency
- throughput
- inference cost
- quantization

### **Sécurité**

- prompt injection
- indirect prompt injection
- data leakage
- data exfiltration
- excessive agency
- least privilege
- secrets
- access control
- sandboxing

# **NIVEAU AK — LA CARTE DE MAÎTRISE PERSONNELLE**

Pour ton objectif, la progression ne doit pas être :

« apprendre toute l'IA ».

Elle doit être :

RECONNAÎTRE  
↓  
COMPRENDRE  
↓  
IDENTIFIER LE BESOIN  
↓  
CHOISIR  
↓  
DIRIGER L'IA  
↓  
CONTRÔLER L'IA  
↓  
APPROFONDIR  
↓  
PRATIQUER  
↓  
FICHE STANE OS

# **NIVEAU AL — CE QUE TU DEVRAIS SAVOIR FAIRE APRÈS CE DOCUMENT**

Tu dois progressivement être capable de regarder un projet et de dire :

« Ici, je n'ai probablement pas besoin d'IA. »

ou :

« Ici, une classification supervisée semble suffisante. »

ou :

« Ici, le problème est surtout documentaire : je pense RAG. »

ou :

« Ici, les connaissances changent trop rapidement pour être mises dans le modèle ; il faut probablement une source externe. »

ou :

« Ici, un agent est inutilement complexe : un workflow déterministe suffit. »

ou :

« Ici, le modèle produit des réponses plausibles mais non vérifiables : il faut un mécanisme de grounding. »

ou :

« Ici, l'accuracy n'est pas la bonne métrique parce que le coût des faux négatifs est beaucoup plus important. »

ou :

« Le modèle semble performant, mais je soupçonne un data leakage. »

ou :

« Cette IA a généré du code, mais je dois vérifier les permissions, les secrets, les appels API et les validations. »

C'est **exactement cette capacité de raisonnement** que nous cherchons à construire.

# **NIVEAU AM — INTÉGRATION AVEC LES AUTRES DOMAINES**

Le domaine IA ne doit surtout pas être étudié isolément.

Il se connecte directement aux sept autres.

IA / ML  
│  
┌───────────────┼────────────────┐  
│ │ │  
WEB UX/UI CYBERSÉCURITÉ  
│ │ │  
API / backend expérience données / accès  
│ │ │  
└───────────────┼────────────────┘  
│  
PRODUIT  
│  
┌─────────┴─────────┐  
│ │  
SEO MARKETING  
│ │  
└─────────┬─────────┘  
│  
ARCHITECTURE  
│  
SYSTÈME GLOBAL

Exemple concret :

Tu construis un assistant IA pour une entreprise.

Tu as besoin de :

### **Web**

API, frontend, backend.

### **UX/UI**

Conversation, feedback, erreurs, onboarding.

### **Cybersecurity**

Permissions, secrets, injection, données privées.

### **SEO**

Si certaines réponses/connaissances doivent être publiques et découvrables.

### **Product**

Problème utilisateur, valeur, coût, KPI.

### **Branding**

Personnalité et positionnement de l'assistant.

### **Architecture**

Modèle, base, cache, RAG, outils, monitoring.

L'IA seule ne suffit donc pas.

# **NIVEAU AN — LA FORMULE STANE POUR LIRE N'IMPORTE QUEL PROJET IA**

Lorsque tu rencontres un nouveau terme sur LinkedIn, YouTube, GitHub, X ou dans un projet, ne cherche pas immédiatement à le mémoriser.

Pose ces questions :

1\. QU'EST-CE QUE C'EST ?  
↓  
2\. POURQUOI CELA EXISTE ?  
↓  
3\. QUEL PROBLÈME CELA RÉSOUT ?  
↓  
4\. QUAND EN AI-JE BESOIN ?  
↓  
5\. QU'EST-CE QUI EXISTAIT AVANT ?  
↓  
6\. QUELLES SONT LES ALTERNATIVES ?  
↓  
7\. QUELS SONT LES COMPROMIS ?  
↓  
8\. COMMENT UNE IA POURRAIT-ELLE L'IMPLÉMENTER ?  
↓  
9\. COMMENT VÉRIFIER SON IMPLÉMENTATION ?  
↓  
10\. DANS QUELS CAS CELA ÉCHOUE ?

C'est la version IA de ta méthode de **littératie technique**.

# **NIVEAU AO — LES 25 CONCEPTS PRIORITAIRES À APPROFONDIR**

Après lecture de ce document, voici les notions qui méritent probablement les premières vraies séances de profondeur :

1.  **AI vs ML vs Deep Learning**
2.  **Supervised Learning**
3.  **Classification**
4.  **Regression**
5.  **Clustering**
6.  **Training / Validation / Test**
7.  **Overfitting / Underfitting**
8.  **Features / Labels**
9.  **Loss Function**
10. **Gradient Descent**
11. **Evaluation Metrics**
12. **Neural Networks**
13. **Transformers**
14. **Attention**
15. **Tokens**
16. **Embeddings**
17. **LLM**
18. **Prompt Engineering**
19. **RAG**
20. **Vector Databases**
21. **Fine-tuning / LoRA**
22. **Agents / Tool Calling**
23. **AI Evaluation**
24. **MLOps / LLMOps**
25. **AI Security / Guardrails**

Ces 25 concepts constituent une **colonne vertébrale**. Ils ne représentent pas toute l'IA, mais ils couvrent une très grande partie des conversations, architectures et projets que tu rencontreras.

# **NIVEAU AP — CE QUI EST HORS DU PÉRIMÈTRE IMMÉDIAT**

Il faut également savoir ce que nous ne cherchons **pas encore** à maîtriser.

Pas maintenant :

- démontrer mathématiquement chaque algorithme ;
- implémenter un Transformer from scratch ;
- entraîner un LLM géant ;
- construire un framework ML complet ;
- maîtriser toutes les architectures CNN ;
- devenir spécialiste de chaque algorithme ;
- apprendre tous les modèles existants ;
- devenir chercheur en IA.

Ce serait contre-productif pour ton objectif.

Le but actuel est :

**avoir une carte suffisamment précise pour savoir où aller lorsqu'un problème apparaît.**

Ensuite seulement, on descend dans le détail.

# **NIVEAU AQ — LA DIFFÉRENCE ENTRE « SAVOIR UTILISER » ET « SAVOIR DIRIGER »**

C'est probablement la distinction la plus importante de tout ce document.

### **Niveau 1 — Utilisateur**

« ChatGPT, écris-moi ça. »

### **Niveau 2 — Power User**

« Utilise ce contexte, ce format et ces contraintes. »

### **Niveau 3 — AI Builder**

« Construis cette architecture RAG. »

### **Niveau 4 — AI Technical Lead**

« Compare RAG, fine-tuning et approche hybride. Voici les contraintes. Justifie ton choix. »

### **Niveau 5 — AI Auditor**

« Prouve-moi que ton système fonctionne, montre-moi les métriques, les cas d'échec, les risques et les tests. »

### **Niveau que nous cherchons pour STANE**

**Niveau 4 → Niveau 5.**

Tu dois être capable de **piloter l'IA sans avoir besoin de tout implémenter toi-même**.

# **NIVEAU AR — LA RÈGLE D'OR**

Lorsque tu travailles avec une IA :

**Ne demande pas seulement : « Est-ce que tu peux le faire ? »**

Demande :

**« Pourquoi cette approche ? »**

Puis :

**« Quelles sont les alternatives ? »**

Puis :

**« Quelles sont tes hypothèses ? »**

Puis :

**« Comment vas-tu mesurer que cela fonctionne ? »**

Puis :

**« Dans quels cas cela échoue ? »**

Puis :

**« Comment puis-je vérifier indépendamment que tu as raison ? »**

Et enfin :

**« Qu'est-ce qui me ferait changer d'avis sur cette architecture ? »**

C'est là que l'utilisation de l'IA cesse d'être une simple consommation de réponses et devient une **collaboration technique contrôlée**.

# **CONCLUSION — LA CARTE MENTALE À CONSERVER**

Si tu devais ne retenir qu'une seule représentation de tout ce document, garde celle-ci :

PROBLÈME  
↓  
DONNÉES  
↓  
REPRÉSENTATION  
↓  
┌───────┴───────┐  
│ │  
RÈGLES ML  
↓  
DEEP LEARNING  
↓  
TRANSFORMER  
↓  
LLM  
↓  
┌─────────────────┼─────────────────┐  
│ │ │  
PROMPT RAG FINE-TUNING  
│ │ │  
└─────────────────┼─────────────────┘  
↓  
AI APPLICATION  
↓  
┌──────────┼──────────┐  
│ │ │  
TOOLS MEMORY WORKFLOW  
│ │ │  
└──────────┼──────────┘  
↓  
AGENT  
↓  
EVALUATION  
↓  
SECURITY  
↓  
DEPLOYMENT  
↓  
MONITORING  
↓  
FEEDBACK  
↓  
IMPROVEMENT

Et surtout :

NE PAS COMMENCER PAR  
« QUEL MODÈLE ? »  
│  
↓  
COMMENCER PAR  
« QUEL PROBLÈME ? »  
│  
↓  
« QUELLE DONNÉE ? »  
│  
↓  
« QUELLE SOLUTION ? »  
│  
↓  
« COMMENT MESURER ? »  
│  
↓  
« COMMENT CONTRÔLER ? »

## **Niveau de maîtrise visé pour STANE OS**

À terme, chaque notion importante rencontrée dans ce document pourra devenir une fiche indépendante selon ton modèle :

CONCEPT  
│  
├── Définition  
├── Pourquoi ça existe  
├── Problème résolu  
├── Quand y penser  
├── Comment ça fonctionne  
├── Prérequis  
├── Alternatives  
├── Comparaisons  
├── Exemple réel  
├── Quand NE PAS l'utiliser  
├── Comment demander à l'IA de l'utiliser  
├── Comment contrôler l'IA  
├── Erreurs fréquentes  
├── Cas limites  
├── Sécurité  
├── Ressources  
└── Niveau de maîtrise STANE

**Document 05 constitue donc la carte du territoire IA.** La prochaine étape logique du projet n'est pas d'ajouter encore des notions à cette carte, mais de prendre progressivement les concepts prioritaires et de les transformer en **compréhension opérationnelle** : explication profonde → exemples → choix d'architecture → mini-implémentation → exercice → utilisation avec IA → audit → fiche STANE OS.