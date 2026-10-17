# **DOCUMENT 02 — UI / UX DESIGN**

## **Référentiel de culture technique et décisionnelle**

**Projet : AI-Augmented Technical Literacy**  
**Domaine 02 / 08 : UX/UI & Design**  
**Version : 1.0 — Référentiel fondamental**  
**Statut : Document de référence**

# **0\. FINALITÉ DU DOCUMENT**

## **0.1. Pourquoi ce document existe**

L’objectif de ce document n’est pas de faire de toi un designer UI/UX professionnel.

Il est de te donner suffisamment de culture, de vocabulaire, de raisonnement et de capacité d’analyse pour que tu puisses :

- comprendre un design lorsque tu le rencontres ;
- identifier les principes utilisés derrière une interface ;
- reconnaître un problème d’expérience utilisateur ;
- distinguer un problème d’UX d’un problème d’UI ;
- comprendre pourquoi une interface fonctionne ou ne fonctionne pas ;
- savoir quand un projet nécessite de la recherche utilisateur ;
- savoir quand travailler l’architecture de l’information ;
- savoir quand utiliser une animation ;
- savoir quand ne **pas** utiliser une animation ;
- comprendre le rôle de la typographie, des couleurs, de l’espace, des composants et de la hiérarchie visuelle ;
- construire ou faire construire une interface cohérente ;
- choisir entre différentes approches de design ;
- demander à une IA de produire quelque chose de spécifique plutôt qu’un énième design générique ;
- repérer les sorties d’IA superficielles ;
- auditer une interface produite par l’IA ;
- communiquer efficacement avec un designer ;
- communiquer efficacement avec une IA ;
- comprendre suffisamment le design pour prendre de meilleures décisions produit et techniques.

# **1\. LE PROBLÈME CENTRAL : « BEAU » ≠ « BON »**

C’est probablement la première distinction à intégrer.

Une interface peut être :

- belle mais difficile à utiliser ;
- moderne mais confuse ;
- minimaliste mais vide ;
- immersive mais lente ;
- originale mais incohérente ;
- esthétique mais inaccessible ;
- très animée mais fatigante ;
- extrêmement travaillée mais inutilement complexe.

Inversement, une interface peut être relativement simple visuellement et être excellente.

La question fondamentale n'est donc pas :

« Est-ce que c'est beau ? »

mais :

**« Est-ce que cette interface permet à la bonne personne d'accomplir la bonne tâche, avec le moins de friction inutile possible, tout en produisant une expérience cohérente avec le contexte ? »**

# **2\. LE MODÈLE MENTAL GLOBAL**

Pour comprendre le domaine, il faut distinguer plusieurs couches.

UTILISATEUR  
↓  
BESOINS / OBJECTIFS / CONTEXTE  
↓  
RECHERCHE UTILISATEUR  
↓  
UX  
↓  
ARCHITECTURE DE L'INFORMATION  
↓  
FLOWS / INTERACTIONS  
↓  
UI  
↓  
DESIGN SYSTEM  
↓  
IMPLÉMENTATION  
↓  
PERFORMANCE / ACCESSIBILITÉ  
↓  
MESURE / TEST  
↓  
AMÉLIORATION

Le design visuel n'est donc qu'une partie du système.

# **3\. NIVEAU A — CARTOGRAPHIE DU DOMAINE****3.1. Les grandes familles de l'UX/UI**

Le domaine peut être divisé en plusieurs grandes familles.

## **A. UX Research**

Comprendre :

- qui utilise le produit ;
- pourquoi ;
- dans quel contexte ;
- avec quels problèmes ;
- avec quelles attentes ;
- avec quelles contraintes ;
- avec quelles habitudes.

## **B. UX Design**

Concevoir l'expérience globale.

Questions :

- Que doit faire l'utilisateur ?
- Dans quel ordre ?
- Que doit-il comprendre ?
- Quelles décisions doit-il prendre ?
- Où risque-t-il de bloquer ?
- Quelle information doit apparaître à quel moment ?

## **C. Information Architecture**

Organiser l'information.

Exemples :

- navigation ;
- catégories ;
- menus ;
- pages ;
- hiérarchie ;
- recherche ;
- filtres ;
- taxonomie ;
- structure du contenu.

## **D. Interaction Design**

Définir comment l'utilisateur interagit avec le système.

Exemples :

- clic ;
- tap ;
- swipe ;
- drag & drop ;
- hover ;
- formulaire ;
- modal ;
- dropdown ;
- feedback ;
- transitions ;
- états d'interface.

## **E. UI Design**

Construire l'apparence et le langage visuel.

Exemples :

- couleurs ;
- typographie ;
- boutons ;
- cartes ;
- icônes ;
- espacements ;
- grilles ;
- images ;
- composants ;
- contrastes.

## **F. Design Systems**

Créer une logique réutilisable.

Exemples :

Design tokens  
↓  
Couleurs  
Typographie  
Espacements  
Rayons  
Ombres  
↓  
Composants  
↓  
Patterns  
↓  
Pages

## **G. Accessibility**

Permettre au plus grand nombre d'utiliser l'interface.

Cela concerne notamment :

- contraste ;
- clavier ;
- lecteurs d'écran ;
- taille des textes ;
- focus ;
- structure sémantique ;
- alternatives textuelles ;
- mouvements ;
- navigation.

## **H. Responsive Design**

Adapter l'expérience aux différentes tailles d'écran et modalités d'utilisation.

## **I. Content Design**

Les mots eux-mêmes font partie du design.

Exemples :

- labels ;
- boutons ;
- messages d'erreur ;
- onboarding ;
- titres ;
- instructions ;
- confirmations ;
- microcopy.

## **J. Conversion & Product Design**

Le design doit également servir des objectifs métier.

Exemples :

- inscription ;
- achat ;
- prise de contact ;
- demande de devis ;
- téléchargement ;
- activation ;
- rétention.

# **4\. UX ET UI : LA DISTINCTION FONDAMENTALE**

## **4.1. UX**

UX signifie **User Experience**.

Elle concerne l'expérience globale vécue par l'utilisateur.

Exemple :

Un utilisateur veut réserver un restaurant.

L'UX concerne :

1.  comprendre qu'il peut réserver ;
2.  trouver le restaurant ;
3.  choisir une date ;
4.  choisir une heure ;
5.  sélectionner le nombre de personnes ;
6.  renseigner les informations nécessaires ;
7.  comprendre que la réservation est confirmée.

# **4.2. UI**

UI signifie **User Interface**.

Elle concerne l'interface par laquelle l'utilisateur interagit avec le produit.

Elle concerne notamment :

- boutons ;
- couleurs ;
- typographie ;
- icônes ;
- cartes ;
- champs ;
- menus ;
- espacements ;
- illustrations ;
- animations.

# **4.3. Une analogie utile**

Imagine un restaurant.

### **UX**

- réservation facile ;
- menu compréhensible ;
- circulation logique ;
- temps d'attente raisonnable ;
- service cohérent.

### **UI**

- couleurs ;
- décoration ;
- typographie ;
- présentation du menu ;
- signalétique.

Un restaurant peut être magnifique mais mal organisé.

C'est exactement la différence.

# **5\. UNE INTERFACE N'EST PAS UNE IMAGE**

Une erreur fréquente consiste à considérer une interface comme une composition graphique.

Une interface est un **système interactif**.

Un bouton n'est pas simplement un rectangle coloré.

Il possède :

- un objectif ;
- un label ;
- une position ;
- un état ;
- une action ;
- un feedback ;
- des conditions ;
- éventuellement des erreurs.

Un bouton peut avoir les états :

Default  
Hover  
Focus  
Pressed  
Disabled  
Loading  
Success  
Error

Le design doit prévoir ces états.

# **6\. LES CONCEPTS ESSENTIELS — NIVEAU B****6.1. User**

L'utilisateur est la personne qui utilise le système.

Mais « utilisateur » ne signifie pas simplement :

« quelqu'un qui visite le site ».

Il possède :

- un objectif ;
- des connaissances ;
- des habitudes ;
- un contexte ;
- des contraintes ;
- une capacité technique ;
- un état émotionnel.

# **6.2. User Goal**

Ce que l'utilisateur cherche réellement à accomplir.

Exemple :

Un visiteur ne veut pas nécessairement :

« consulter la page Services ».

Il veut peut-être :

« savoir si cette agence peut créer mon site et combien cela pourrait me coûter ».

La différence est importante.

# **6.3. User Flow**

Le parcours permettant d'accomplir une tâche.

Exemple :

Accueil  
↓  
Services  
↓  
Service Web  
↓  
Portfolio  
↓  
Formulaire  
↓  
Confirmation

# **6.4. User Journey**

Le parcours plus global de l'utilisateur avec l'entreprise ou le produit.

Il peut commencer avant même l'utilisation du site.

Découverte  
↓  
Recherche  
↓  
Comparaison  
↓  
Visite  
↓  
Interaction  
↓  
Conversion  
↓  
Utilisation  
↓  
Fidélisation

# **6.5. Persona**

Représentation structurée d'un type d'utilisateur.

Un persona peut contenir :

- contexte ;
- objectifs ;
- frustrations ;
- motivations ;
- habitudes ;
- contraintes.

Mais attention :

Un persona inventé sans données réelles peut devenir une fiction inutile.

# **6.6. Pain Point**

Un problème rencontré par l'utilisateur.

Exemples :

- formulaire trop long ;
- navigation confuse ;
- informations difficiles à trouver ;
- prix cachés ;
- bouton ambigu ;
- temps de chargement trop long.

# **6.7. Friction**

Tout élément qui rend inutilement difficile l'accomplissement d'une tâche.

La friction n'est pas toujours mauvaise.

Une étape supplémentaire peut être justifiée si elle :

- augmente la sécurité ;
- réduit les erreurs ;
- protège l'utilisateur ;
- améliore la qualité des données.

La question est donc :

**Cette friction apporte-t-elle une valeur proportionnelle à son coût ?**

# **6.8. Affordance**

Une affordance désigne la possibilité d'action suggérée par un élément.

Exemple :

Un bouton ressemble à quelque chose sur lequel on peut cliquer.

Une poignée suggère qu'on peut la tirer.

En UI, les affordances doivent être suffisamment compréhensibles.

# **6.9. Signifier / Signifier cues**

Un élément visuel peut signaler comment il fonctionne.

Exemples :

- soulignement d'un lien ;
- curseur ;
- icône ;
- bouton ;
- champ de saisie.

# **6.10. Feedback**

Le système doit informer l'utilisateur de ce qui se passe.

Exemples :

Clic  
↓  
Loading  
↓  
Succès

ou

Soumission  
↓  
Erreur  
↓  
Explication  
↓  
Correction possible

Sans feedback, l'utilisateur peut se demander :

« Est-ce que mon clic a fonctionné ? »

# **6.11. System Status**

L'interface doit communiquer l'état actuel du système.

Exemples :

- chargement ;
- sauvegarde ;
- connexion ;
- erreur ;
- synchronisation ;
- paiement en attente ;
- paiement réussi.

# **6.12. Error Prevention**

Un bon design ne se contente pas de montrer les erreurs.

Il essaie de les empêcher.

Exemple :

Mauvais :

« Erreur : date invalide. »

Meilleur :

- calendrier ;
- dates passées désactivées ;
- validation en temps réel.

# **6.13. Error Recovery**

Quand une erreur arrive, l'utilisateur doit savoir :

1.  ce qui s'est passé ;
2.  pourquoi ;
3.  comment corriger.

# **6.14. Cognitive Load**

La charge cognitive correspond à l'effort mental nécessaire pour comprendre ou utiliser une interface.

Une interface peut augmenter la charge cognitive avec :

- trop d'informations ;
- trop de choix ;
- jargon ;
- navigation complexe ;
- animations inutiles ;
- hiérarchie faible ;
- incohérence.

# **6.15. Progressive Disclosure**

Ne pas montrer immédiatement tout ce qui existe.

Montrer d'abord ce qui est nécessaire.

Puis révéler progressivement les détails.

Très utile pour :

- dashboards ;
- applications complexes ;
- paramètres ;
- onboarding.

# **6.16. Mental Model**

L'utilisateur possède une représentation mentale de la manière dont quelque chose devrait fonctionner.

Si ton interface fonctionne complètement différemment de ses attentes, il devra apprendre ton système.

Un bon design exploite autant que possible les modèles mentaux déjà connus.

# **7\. LES PRINCIPES DE DESIGN À CONNAÎTRE****7.1. Hiérarchie visuelle**

Tous les éléments ne doivent pas avoir la même importance.

La hiérarchie peut être créée par :

- taille ;
- poids ;
- contraste ;
- position ;
- espace ;
- couleur ;
- densité.

# **7.2. Proximity**

Les éléments liés doivent visuellement être proches.

# **7.3. Similarity**

Les éléments ayant le même rôle devraient partager certains attributs visuels.

# **7.4. Alignment**

Les éléments doivent avoir une logique d'alignement.

Une interface peut sembler « amateur » simplement parce que ses alignements sont mauvais.

# **7.5. Contrast**

Le contraste permet de distinguer les éléments.

Il concerne :

- couleur ;
- taille ;
- poids ;
- forme ;
- espace.

# **7.6. Repetition**

Répéter les mêmes conventions crée de la cohérence.

# **7.7. Consistency**

Si deux boutons ont la même fonction, ils devraient généralement se comporter de manière similaire.

# **7.8. White Space**

L'espace vide n'est pas un espace perdu.

Il sert à :

- séparer ;
- respirer ;
- hiérarchiser ;
- focaliser ;
- rendre l'information plus lisible.

# **7.9. Visual Rhythm**

La répétition organisée des espacements, tailles et blocs crée un rythme visuel.

# **8\. GESTALT : COMPRENDRE LA PERCEPTION**

Les principes de Gestalt permettent de comprendre comment les utilisateurs organisent visuellement l'information.

À connaître notamment :

- proximité ;
- similarité ;
- continuité ;
- fermeture ;
- figure/fond ;
- région commune.

L'intérêt n'est pas de mémoriser une liste.

L'objectif est de comprendre :

**Comment le cerveau regroupe-t-il les éléments visuels ?**

# **9\. TYPOGRAPHIE**

La typographie est une composante structurelle de l'interface.

Elle influence :

- lisibilité ;
- hiérarchie ;
- personnalité ;
- densité ;
- crédibilité ;
- rythme.

## **À comprendre**

- font family ;
- font weight ;
- font size ;
- line height ;
- letter spacing ;
- paragraph width ;
- heading hierarchy.

# **9.1. Font pairing**

Deux polices peuvent être combinées.

Mais :

Plus de polices ≠ meilleur design.

Dans beaucoup de projets, une ou deux familles bien utilisées suffisent.

# **9.2. Type scale**

Une échelle typographique cohérente peut définir :

Display  
H1  
H2  
H3  
Body  
Small  
Caption

# **10\. COULEUR**

La couleur ne sert pas seulement à « faire joli ».

Elle peut transmettre :

- priorité ;
- état ;
- danger ;
- succès ;
- marque ;
- information.

Exemple :

Rouge → danger / erreur  
Vert → succès  
Orange → avertissement  
Bleu → information / confiance

Mais attention :

Ne jamais dépendre uniquement de la couleur pour transmettre une information.

# **10.1. Palette**

Une palette peut contenir :

Primary  
Secondary  
Accent  
Background  
Surface  
Text  
Muted  
Border  
Success  
Warning  
Error  
Info

# **11\. CONTRASTE**

Un contraste insuffisant peut rendre une interface difficile à lire.

Il faut penser au contraste entre :

- texte / arrière-plan ;
- bouton / arrière-plan ;
- éléments interactifs ;
- états actifs/inactifs.

# **12\. ICONOGRAPHIE**

Une icône doit avoir :

- une fonction ;
- une signification ;
- une cohérence visuelle.

Problème fréquent :

utiliser une icône uniquement parce qu'elle « ressemble bien ».

Une icône incompréhensible peut augmenter la confusion.

# **13\. IMAGERIE**

Les images jouent plusieurs rôles.

Elles peuvent :

- expliquer ;
- contextualiser ;
- inspirer ;
- rassurer ;
- montrer un produit ;
- raconter une histoire.

Mais une image décorative inutile peut simplement augmenter le poids de la page.

# **14\. ESPACEMENT**

Les systèmes d'espacement permettent de maintenir une cohérence.

Exemple conceptuel :

4  
8  
12  
16  
24  
32  
48  
64  
96

L'objectif n'est pas nécessairement d'utiliser ces valeurs exactes.

L'objectif est d'éviter :

« chaque élément est placé avec une valeur inventée ».

# **15\. GRILLE**

Une grille organise l'espace.

Elle permet de définir :

- colonnes ;
- marges ;
- gutters ;
- alignements ;
- largeur maximale.

Une grille cohérente facilite la lecture et la construction du responsive.

# **16\. RESPONSIVE DESIGN**

Le responsive n'est pas :

« rendre le site plus petit sur mobile ».

C'est adapter l'expérience aux contraintes du contexte.

Contraintes :

- largeur ;
- hauteur ;
- interaction tactile ;
- orientation ;
- densité ;
- connexion ;
- environnement.

# **16.1. Desktop-first vs Mobile-first**

### **Mobile-first**

On commence par les contraintes du petit écran puis on enrichit.

Avantages :

- oblige à prioriser ;
- limite la complexité ;
- facilite souvent le responsive.

### **Desktop-first**

On commence par une interface large puis on adapte.

Peut être pertinent pour :

- applications professionnelles ;
- dashboards ;
- outils complexes ;
- interfaces où l'espace desktop est central.

Ce n'est donc pas une religion.

# **17\. BREAKPOINTS**

Les breakpoints permettent d'adapter la mise en page.

Mais ils doivent découler du contenu.

Mauvais raisonnement :

« Je vais utiliser exactement trois breakpoints parce que tous les sites font ça. »

Meilleur raisonnement :

« À quelle largeur mon contenu cesse-t-il de fonctionner correctement ? »

# **18\. TOUCH DESIGN**

Sur mobile, l'utilisateur utilise principalement ses doigts.

Il faut donc considérer :

- taille des zones interactives ;
- distance entre boutons ;
- gestes ;
- clavier mobile ;
- scroll ;
- orientation.

# **19\. NAVIGATION**

La navigation doit permettre de répondre rapidement à :

« Où suis-je ? »

« Où puis-je aller ? »

« Comment revenir ? »

« Où trouver ce que je cherche ? »

# **19.1. Types de navigation**

- navbar ;
- sidebar ;
- tabs ;
- breadcrumbs ;
- bottom navigation ;
- mega menu ;
- contextual navigation ;
- search.

# **20\. INFORMATION ARCHITECTURE**

L'information architecture concerne la manière dont les contenus sont organisés.

Exemple :

Accueil  
├── Services  
│ ├── Développement Web  
│ ├── Automatisation  
│ └── Design  
├── Projets  
├── À propos  
└── Contact

# **20.1. Flat vs Deep Architecture**

### **Architecture plate**

Peu de niveaux.

Avantage :

- accès rapide.

Inconvénient :

- navigation principale potentiellement très longue.

### **Architecture profonde**

Plusieurs niveaux.

Avantage :

- organisation complexe.

Inconvénient :

- plus de clics ;
- risque de désorientation.

# **21\. SEARCH**

Une recherche peut être indispensable lorsque le volume d'information est important.

Exemples :

- marketplace ;
- bibliothèque ;
- documentation ;
- dashboard ;
- réseau social.

Sur un petit site de cinq pages, une recherche est souvent inutile.

# **22\. FILTERS & SORTING**

À distinguer.

### **Filter**

Réduit les résultats.

### **Sort**

Change leur ordre.

Exemple :

Filtrer :  
→ catégorie = chaussures  
<br/>Trier :  
→ prix croissant

# **23\. FORMULAIRES**

Les formulaires sont un domaine majeur de l'UX.

Principes :

- demander uniquement ce qui est nécessaire ;
- regrouper logiquement les champs ;
- utiliser des labels explicites ;
- afficher les contraintes ;
- valider intelligemment ;
- expliquer les erreurs ;
- conserver les données saisies lorsque possible.

# **24\. MICROCOPY**

La microcopy correspond aux petits textes de l'interface.

Exemples :

- labels ;
- placeholders ;
- erreurs ;
- confirmations ;
- boutons ;
- instructions.

Compare :

Envoyer

avec :

Demander mon devis

Le second fournit davantage de contexte.

# **25\. CTA**

Call To Action.

Un CTA doit indiquer clairement l'action.

Exemples :

- Découvrir les projets ;
- Commencer gratuitement ;
- Demander un devis ;
- Réserver une démonstration.

Éviter :

Cliquez ici.

# **26\. MODALES**

Une modal interrompt temporairement le flux principal.

Bonne utilisation :

- confirmation importante ;
- action nécessitant une décision ;
- contenu secondaire court.

Mauvaise utilisation :

- tout mettre dans des modales ;
- utiliser une modal pour chaque information.

# **27\. TOASTS**

Messages temporaires.

Exemple :

Projet sauvegardé.

Ils sont utiles pour les feedbacks courts.

Ils sont mauvais pour les erreurs critiques nécessitant une action.

# **28\. LOADING STATES**

Une interface doit gérer les états intermédiaires.

Exemples :

- spinner ;
- skeleton ;
- progress bar ;
- optimistic UI.

# **28.1. Skeleton**

Un skeleton reproduit approximativement la structure du contenu pendant son chargement.

Il peut améliorer la perception de fluidité.

# **29\. EMPTY STATES**

Une page vide doit expliquer ce qui se passe.

Mauvais :

Aucun résultat.

Meilleur :

Aucun projet ne correspond à vos filtres. Essayez de modifier votre recherche.

# **30\. DESIGN DES ERREURS**

Une bonne erreur doit répondre à :

1.  Qu'est-ce qui s'est passé ?
2.  Pourquoi ?
3.  Que puis-je faire ?

# **31\. ONBOARDING**

L'onboarding accompagne l'utilisateur dans la découverte du produit.

Il doit éviter de transformer l'expérience en tutoriel interminable.

Une bonne question :

L'utilisateur a-t-il réellement besoin de connaître cela maintenant ?

# **32\. ACCESSIBILITÉ**

L'accessibilité n'est pas une option esthétique.

Elle consiste à permettre l'utilisation du produit par des personnes ayant différentes capacités.

À connaître :

- clavier ;
- focus ;
- contraste ;
- structure sémantique ;
- texte alternatif ;
- labels ;
- navigation ;
- lecteurs d'écran ;
- réduction des mouvements ;
- taille du texte.

# **32.1. POURQUOI L'ACCESSIBILITÉ AMÉLIORE AUSSI L'UX**

Beaucoup de pratiques accessibles améliorent également l'expérience générale.

Exemples :

- labels explicites ;
- navigation clavier ;
- contraste ;
- structure claire ;
- messages d'erreur compréhensibles.

# **33\. UX PSYCHOLOGIQUE**

Il faut comprendre quelques mécanismes.

## **Recognition over recall**

Il est généralement plus facile de reconnaître quelque chose que de devoir le mémoriser.

## **Hick's Law**

Plus il y a de choix, plus le temps de décision peut augmenter.

Conséquence :

Trop de choix peut ralentir l'utilisateur.

## **Fitts's Law**

Le temps nécessaire pour atteindre une cible dépend notamment de sa taille et de sa distance.

Conséquence :

Les actions importantes doivent être suffisamment faciles à atteindre.

## **Jakob's Law**

Les utilisateurs passent leur temps sur beaucoup d'autres interfaces.

Ils s'attendent donc à retrouver certaines conventions.

Cela explique pourquoi :

- logo en haut ;
- navigation identifiable ;
- boutons reconnaissables ;
- panier identifiable ;

sont souvent plus efficaces que des inventions arbitraires.

# **34\. ORIGINALITÉ VS UTILISABILITÉ**

C'est une question importante pour toi.

Tu veux sortir du design générique.

Mais :

**Original ≠ meilleur.**

L'objectif est plutôt :

Convention utile  
+  
Identité propre  
+  
Hiérarchie  
+  
Cohérence  
\=  
Design distinctif

# **35\. POURQUOI CERTAINS SITES NON-IMMERSIFS PLAISENT**

Tu as fait une observation très pertinente.

Un site peut être peu immersif et pourtant excellent.

Pourquoi ?

Parce que son originalité peut venir de :

- sa direction artistique ;
- sa typographie ;
- son système de grille ;
- son contenu ;
- ses proportions ;
- ses photographies ;
- sa voix éditoriale ;
- sa palette ;
- ses composants ;
- ses détails ;
- sa cohérence ;
- son adéquation avec la marque.

L'immersion n'est qu'une stratégie parmi d'autres.

# **36\. LE DESIGN GÉNÉRIQUE**

Un design devient souvent générique lorsqu'il combine des choix très prévisibles.

Exemple :

Hero énorme  
+  
Gradient bleu/violet  
+  
Glassmorphism  
+  
Gros texte blanc  
+  
3 cartes  
+  
Icônes Lucide  
+  
Bouton arrondi  
+  
Animation au scroll  
+  
Section témoignages  
+  
Footer standard

Chaque élément peut être excellent individuellement.

Le problème est leur combinaison répétitive.

# **37\. LES SOURCES DE DISTINCTION**

Un design peut se différencier par :

### **1\. Art direction**

Une direction artistique forte.

### **2\. Typography**

Une typographie distinctive.

### **3\. Layout**

Une composition inhabituelle mais lisible.

### **4\. Content**

Un contenu réellement spécifique.

### **5\. Imagery**

Une photographie ou illustration cohérente.

### **6\. Interaction**

Des interactions pertinentes.

### **7\. Motion**

Une animation ayant un rôle.

### **8\. Brand**

Une identité reconnaissable.

### **9\. Density**

Un choix assumé de densité.

### **10\. Tone**

Une voix et une personnalité.

# **38\. DESIGN DISTINCTIF ≠ DESIGN COMPLEXE**

Un design peut être très simple :

Fond clair  
+  
Typographie forte  
+  
Grille particulière  
+  
Photographie remarquable  
+  
Micro-interactions  
+  
Copywriting précis

et être beaucoup plus distinctif qu'un site rempli d'effets 3D.

# **39\. NIVEAU C — TECHNOLOGIES ET OUTILS**

Il faut distinguer :

**outil de design**

et

**technologie d'implémentation**.

# **39.1. Figma**

Outil de conception collaborative.

Utilisé notamment pour :

- wireframes ;
- prototypes ;
- UI ;
- design systems ;
- collaboration.

# **39.2. Adobe XD**

Outil historique de conception UI/UX.

À connaître culturellement, mais il ne faut pas le considérer automatiquement comme le choix principal actuel.

# **39.3. Sketch**

Outil historiquement très important dans l'écosystème UI.

# **39.4. Framer**

Plateforme orientée design et création de sites avec une forte dimension visuelle.

# **39.5. Canva**

Très utile pour :

- contenus graphiques ;
- réseaux sociaux ;
- présentations ;
- visuels marketing.

Mais Canva n'est pas un remplacement complet de Figma pour le product/UI design complexe.

# **39.6. FigJam**

Outil de collaboration et de brainstorming associé à l'écosystème Figma.

# **40\. TECHNOLOGIES WEB QUI IMPACTENT LE DESIGN**

À connaître :

- HTML ;
- CSS ;
- JavaScript ;
- CSS frameworks ;
- React ;
- Vue ;
- Angular ;
- Next.js ;
- animations CSS ;
- SVG ;
- Canvas ;
- WebGL ;
- Web APIs.

# **41\. DESIGN SYSTEMS**

Un design system peut comprendre :

Design tokens  
+  
Components  
+  
Patterns  
+  
Guidelines  
+  
Documentation

# **41.1. Design Tokens**

Valeurs réutilisables.

Exemple :

color.primary  
spacing.md  
radius.lg  
font.body  
shadow.sm

# **41.2. Component**

Élément réutilisable.

Exemples :

- Button ;
- Input ;
- Modal ;
- Card ;
- Navbar ;
- Badge.

# **41.3. Pattern**

Combinaison de composants destinée à résoudre un problème récurrent.

# **42\. UI LIBRARIES**

Exemples de familles :

- Material Design ;
- Ant Design ;
- MUI ;
- Chakra UI ;
- shadcn/ui ;
- Radix ;
- Bootstrap.

Leur objectif varie.

Certaines fournissent des composants complets.

D'autres fournissent des primitives accessibles ou peu stylisées.

# **43\. TAILWIND ET UI DESIGN**

Tailwind n'est pas un système de design en lui-même.

C'est principalement une approche CSS utility-first.

On peut construire un design system avec Tailwind.

Mais utiliser Tailwind ne garantit absolument pas un bon design.

# **44\. BOOTSTRAP**

Bootstrap fournit notamment :

- composants ;
- système de grille ;
- styles ;
- conventions responsive.

Avantage :

rapidité de construction.

Risque :

interface ressemblant fortement à d'autres projets si elle n'est pas personnalisée.

# **45\. COMPONENT LIBRARY VS DESIGN SYSTEM**

Une bibliothèque de composants :

fournit des composants réutilisables.

Un design system :

définit également les règles, principes, tokens, usages, comportements et cohérence globale.

# **46\. NIVEAU D — COMPARAISONS STRUCTURANTES****46.1. UX vs UI**

|     |     |
| --- | --- |
| **UX** | **UI** |
| expérience | interface |
| logique | apparence |
| parcours | composants |
| architecture | style |
| recherche | design visuel |
| objectifs | perception |

Ils sont complémentaires.

# **46.2. UI vs Graphic Design**

Le graphic design travaille beaucoup sur la communication visuelle.

L'UI ajoute :

- interaction ;
- états ;
- comportement ;
- feedback ;
- système.

# **46.3. UX vs Product Design**

Le Product Design est généralement plus large.

Il peut intégrer :

- UX ;
- UI ;
- produit ;
- business ;
- stratégie ;
- recherche.

# **46.4. Wireframe vs Mockup vs Prototype**

### **Wireframe**

Structure.

### **Mockup**

Aspect visuel.

### **Prototype**

Interaction simulée.

Wireframe  
↓  
Mockup  
↓  
Prototype

Ce n'est pas toujours strictement linéaire, mais c'est un bon modèle mental.

# **46.5. Prototype vs Produit réel**

Un prototype simule.

Un produit réel :

- fonctionne ;
- possède une logique ;
- stocke des données ;
- gère les erreurs ;
- possède des performances ;
- doit être sécurisé.

# **46.6. Mobile-first vs Desktop-first**

Aucune règle universelle.

Décider selon :

- utilisateurs ;
- contexte ;
- produit ;
- contenu ;
- appareils dominants.

# **46.7. Minimalisme vs Minimal UI**

Minimalisme ne signifie pas :

« supprimer tout ».

Il signifie notamment :

supprimer ce qui n'apporte pas suffisamment de valeur.

# **46.8. Animation vs Motion Design**

Une animation peut être simplement fonctionnelle.

Le motion design peut participer à une direction artistique plus globale.

# **46.9. Animation utile vs animation décorative**

### **Utile**

- indique un changement ;
- explique une transition ;
- confirme une action ;
- attire l'attention vers une information importante.

### **Décorative**

- uniquement esthétique.

Une animation décorative peut être légitime.

Mais elle doit être évaluée par son coût.

# **47\. NIVEAU E — DÉCISIONS****47.1. Quand utiliser une animation ?**

Utilise-la lorsque :

- elle clarifie ;
- elle guide ;
- elle renforce la marque ;
- elle améliore la perception ;
- elle crée une transition naturelle.

Évite-la lorsqu'elle :

- ralentit ;
- distrait ;
- empêche une action ;
- fatigue ;
- dégrade les performances.

# **47.2. Quand utiliser la 3D ?**

La 3D est pertinente lorsque :

- le produit est spatial ;
- l'objet doit être visualisé ;
- la marque possède une direction artistique adaptée ;
- l'expérience immersive apporte quelque chose.

Elle n'est pas obligatoire pour rendre un site premium.

# **47.3. Quand utiliser un dashboard ?**

Lorsque l'utilisateur doit :

- surveiller ;
- comparer ;
- analyser ;
- manipuler beaucoup de données.

# **47.4. Quand utiliser une sidebar ?**

Lorsque l'application possède :

- beaucoup de sections ;
- une navigation persistante ;
- une logique d'application.

# **47.5. Quand utiliser bottom navigation ?**

Principalement pour certaines applications mobiles où quelques destinations principales doivent rester accessibles.

# **47.6. Quand utiliser une modal ?**

Pour une interaction secondaire ou une décision ponctuelle.

Pas pour cacher une partie essentielle de la navigation.

# **47.7. Quand utiliser une recherche ?**

Lorsque l'utilisateur peut raisonnablement ne pas savoir où se trouve l'information.

# **47.8. Quand utiliser un onboarding ?**

Lorsque le produit possède un modèle mental difficile à comprendre.

Pas simplement parce que :

« tous les SaaS ont un onboarding ».

# **48\. ARBRE DE DÉCISION UX**

Quel est l'objectif ?  
↓  
Qui est l'utilisateur ?  
↓  
Quelle tâche doit-il accomplir ?  
↓  
Quelle information lui faut-il ?  
↓  
Quel parcours est nécessaire ?  
↓  
Quels obstacles existent ?  
↓  
Quelle interface permet de résoudre cela ?  
↓  
Quels composants ?  
↓  
Quels états ?  
↓  
Quels cas d'erreur ?  
↓  
Quel responsive ?  
↓  
Quelle accessibilité ?  
↓  
Quel test ?

# **49\. ARBRE DE DÉCISION UI**

Quelle identité ?  
↓  
Quel contexte ?  
↓  
Quelle hiérarchie ?  
↓  
Quel contenu ?  
↓  
Quelle grille ?  
↓  
Quelle typographie ?  
↓  
Quelle palette ?  
↓  
Quels composants ?  
↓  
Quels états ?  
↓  
Quel niveau de densité ?  
↓  
Quel niveau d'animation ?

# **50\. NIVEAU F — DESIGN AUGMENTÉ PAR IA**

C'est ici que le document devient particulièrement important pour ton objectif.

L'IA sait générer du design.

Mais elle possède une tendance naturelle :

produire quelque chose qui ressemble à ce qu'elle a vu très souvent.

Donc :

Prompt vague  
↓  
Réponse statistiquement probable  
↓  
Design générique

# **51\. LE PROBLÈME DU PROMPT « FAIS-MOI UN BEAU SITE »**

Exemple :

Crée un portfolio moderne et professionnel avec React, Tailwind et des animations.

Ce prompt est techniquement exploitable.

Mais il est artistiquement pauvre.

Pourquoi ?

Parce que presque aucune décision n'est définie.

# **52\. PROMPT DESIGNER : LES VARIABLES À CONTRÔLER**

Un bon brief peut définir :

### **1\. Audience**

Qui regarde ?

### **2\. Objectif**

Que doit-il faire ?

### **3\. Positionnement**

Comment le projet veut-il être perçu ?

### **4\. Personality**

Sérieux ? audacieux ? premium ? humain ? technique ?

### **5\. Content**

Quelles informations existent réellement ?

### **6\. Information hierarchy**

Qu'est-ce qui est prioritaire ?

### **7\. Visual direction**

Typographie, palette, photographie, composition.

### **8\. Interaction**

Quels comportements ?

### **9\. Motion**

Pourquoi et où ?

### **10\. Constraints**

Performance, accessibilité, responsive.

### **11\. Anti-patterns**

Ce qu'il ne faut surtout pas faire.

# **53\. LE BRIEF ANTI-GÉNÉRIQUE**

Avant de demander à l'IA de designer, tu peux lui imposer :

CONTEXTE  
OBJECTIF  
UTILISATEUR  
POSITIONNEMENT  
PERSONNALITÉ  
CONTENU  
STRUCTURE  
DIRECTION ARTISTIQUE  
CONVENTIONS À CONSERVER  
CONVENTIONS À ÉVITER  
INTERACTIONS  
MOTION  
RESPONSIVE  
ACCESSIBILITÉ  
PERFORMANCE  
CONTRAINTES TECHNIQUES  
CRITÈRES D'ÉVALUATION

# **54\. L'IA DOIT RECEVOIR DES CONTRAINTES**

Une erreur consiste à penser :

« Plus je laisse l'IA libre, plus elle sera créative. »

Pas nécessairement.

Une bonne direction artistique peut émerger de contraintes fortes.

Exemple :

Utilise uniquement deux familles typographiques.

Pas de gradient.

Pas de glassmorphism.

Pas de carte arrondie générique.

Aucun bouton « Learn More ».

Les images doivent avoir une fonction narrative.

Les animations doivent expliquer ou renforcer une transition.

Ces contraintes obligent l'IA à chercher d'autres solutions.

# **55\. PROMPTER L'INTENTION, PAS SEULEMENT LE STYLE**

Mauvais :

« Fais un site premium. »

Meilleur :

« Le visiteur doit percevoir l'entreprise comme techniquement sérieuse, précise et mature avant même de consulter les services. »

Encore mieux :

« Le visiteur doit comprendre en moins de 10 secondes ce que l'entreprise fait, pour qui et pourquoi elle est différente. La direction artistique doit transmettre la précision et la confiance plutôt que le luxe ostentatoire. »

# **56\. NE PAS DEMANDER « UN DESIGN MODERNE »**

Le mot « moderne » est trop vague.

Demander :

- quel type de modernité ;
- pour quelle audience ;
- dans quel secteur ;
- avec quelle personnalité ;
- avec quelles contraintes.

# **57\. DEMANDER À L'IA DE JUSTIFIER SES CHOIX**

Tu peux demander :

Pour chaque décision importante, explique le problème utilisateur qu'elle résout.

Exemple :

Pourquoi cette navigation ?

Pourquoi ce CTA ?

Pourquoi cette hiérarchie ?

Pourquoi cette animation ?

Pourquoi cette densité ?

Cela permet de transformer l'IA de générateur en **partenaire de raisonnement**.

# **58\. DEMANDER PLUSIEURS DIRECTIONS**

Au lieu de :

« Fais le design. »

Demande :

Propose trois directions artistiques réellement différentes.

Par exemple :

### **Direction A**

Editorial / typographique.

### **Direction B**

Technologique / immersive.

### **Direction C**

Minimaliste / institutionnelle.

Puis comparer.

# **59\. DESIGN EXPLORATION**

L'IA peut servir à explorer :

Brief  
↓  
3 directions  
↓  
Comparaison  
↓  
Sélection  
↓  
Raffinement  
↓  
Design system  
↓  
Implémentation

C'est souvent meilleur que :

Prompt  
↓  
Code  
↓  
Acceptation

# **60\. L'IA NE DOIT PAS CHOISIR SEULE**

Tu peux déléguer :

- génération ;
- exploration ;
- variantes ;
- documentation ;
- implémentation.

Mais les décisions importantes doivent rester contrôlées :

- cible ;
- positionnement ;
- hiérarchie ;
- architecture ;
- compromis ;
- identité ;
- niveau d'originalité.

# **61\. NIVEAU G — CONTRÔLER ET AUDITER UNE INTERFACE**

Voici la partie qui te permettra de ne plus accepter aveuglément ce que produit l'IA.

# **62\. AUDIT 1 — CLARTÉ**

Demande :

Est-ce que je comprends immédiatement ce que fait le produit ?

# **63\. AUDIT 2 — HIÉRARCHIE**

Demande :

Quel élément mon regard voit-il en premier ?

Puis :

Est-ce réellement celui que je veux mettre en avant ?

# **64\. AUDIT 3 — NAVIGATION**

Demande :

- Où suis-je ?
- Où puis-je aller ?
- Où dois-je cliquer ?
- Comment revenir ?

# **65\. AUDIT 4 — COHÉRENCE**

Vérifier :

- boutons ;
- espacements ;
- typographie ;
- couleurs ;
- composants ;
- icônes ;
- états.

# **66\. AUDIT 5 — RESPONSIVE**

Ne pas simplement vérifier :

« Est-ce que ça ne déborde pas ? »

Vérifier :

- priorité du contenu ;
- navigation ;
- interactions ;
- tailles ;
- lisibilité ;
- densité ;
- ordre des éléments.

# **67\. AUDIT 6 — ACCESSIBILITÉ**

Vérifier :

- contraste ;
- clavier ;
- focus ;
- labels ;
- structure ;
- texte alternatif ;
- taille du texte ;
- mouvements.

# **68\. AUDIT 7 — PERFORMANCE PERÇUE**

Une interface peut techniquement être rapide mais sembler lente.

Examiner :

- loading ;
- skeleton ;
- transitions ;
- images ;
- animations ;
- feedback.

# **69\. AUDIT 8 — COHÉRENCE AVEC LA MARQUE**

Question :

Est-ce que cette interface pourrait appartenir à n'importe quelle autre entreprise ?

Si oui, problème potentiel.

# **70\. AUDIT 9 — GÉNÉRICITÉ**

Questions :

- Est-ce que je vois les mêmes patterns partout ?
- Les textes sont-ils génériques ?
- Les images sont-elles interchangeables ?
- La palette semble-t-elle arbitraire ?
- Les animations sont-elles ajoutées mécaniquement ?
- Les composants ressemblent-ils à une bibliothèque non personnalisée ?

# **71\. AUDIT 10 — UTILITÉ DES EFFETS**

Pour chaque effet :

Pourquoi existe-t-il ?

Si la réponse est :

« parce que ça fait moderne »

ce n'est pas suffisant.

# **72\. CHECKLIST ANTI-DESIGN IA**

Avant de valider un design généré par IA :

\[ \] Le produit est immédiatement compréhensible  
\[ \] La cible est claire  
\[ \] La hiérarchie est cohérente  
\[ \] Les CTA sont explicites  
\[ \] La navigation est logique  
\[ \] Les composants sont cohérents  
\[ \] Les espacements sont systématiques  
\[ \] La typographie est maîtrisée  
\[ \] Le contraste est suffisant  
\[ \] Les états sont prévus  
\[ \] Les erreurs sont prévues  
\[ \] Le responsive est réellement pensé  
\[ \] L'accessibilité est considérée  
\[ \] Les animations ont une raison  
\[ \] Les images ont une fonction  
\[ \] Le design possède une identité  
\[ \] Le contenu n'est pas générique  
\[ \] Le design correspond au positionnement  
\[ \] Les performances sont acceptables  
\[ \] Le résultat ne dépend pas d'effets superficiels

# **73\. LES 7 QUESTIONS À POSER À UNE IA AVANT D'ACCEPTER SON DESIGN**

### **1.**

Quel est l'objectif principal de cette page ?

### **2.**

Quelle est la hiérarchie visuelle et pourquoi ?

### **3.**

Quels sont les principaux risques UX ?

### **4.**

Quels choix pourraient rendre cette interface générique ?

### **5.**

Quelles conventions avons-nous volontairement conservées ?

### **6.**

Quelles conventions avons-nous volontairement rejetées ?

### **7.**

Comment testerais-tu cette interface avec de vrais utilisateurs ?

# **74\. COMMENT RECONNAÎTRE UNE MAUVAISE RÉPONSE DE L'IA**

Signaux d'alerte :

- vocabulaire très vague ;
- « modern and sleek » répété ;
- animations sans justification ;
- beaucoup de gradients ;
- trop de cartes ;
- trop de glassmorphism ;
- mêmes layouts ;
- CTA génériques ;
- absence de cas d'erreur ;
- aucune réflexion responsive ;
- aucune réflexion accessibilité ;
- aucune réflexion utilisateur.

# **75\. LE DESIGN SYSTEM COMME OUTIL ANTI-GÉNÉRICITÉ**

Paradoxalement, les systèmes peuvent aider à créer une identité.

Un système bien conçu définit :

- typographie ;
- couleurs ;
- espacements ;
- formes ;
- composants ;
- interactions ;
- motion ;
- règles.

L'originalité ne vient pas nécessairement de chaque élément.

Elle peut venir de leur combinaison cohérente.

# **76\. LE CONCEPT DE « DESIGN LANGUAGE »**

Une marque peut avoir un langage visuel.

Par exemple :

Typographie  
+  
Espacement  
+  
Formes  
+  
Couleur  
+  
Photographie  
+  
Motion  
+  
Illustration  
+  
Tone of voice

Ce langage permet de reconnaître la marque même sans logo.

# **77\. UI ET CONTENU**

Une interface n'est pas indépendante de son contenu.

Un mauvais contenu peut rendre un excellent design mauvais.

Exemple :

Un bouton :

Envoyer

peut être moins efficace que :

Demander mon devis

Le contenu participe à l'expérience.

# **78\. UX WRITING**

À connaître :

- clarté ;
- concision ;
- contexte ;
- ton ;
- action ;
- feedback.

Éviter les formulations inutilement techniques.

# **79\. DESIGN ET CONVERSION**

Le design peut influencer :

- confiance ;
- compréhension ;
- attention ;
- décision ;
- action.

Mais :

UX ≠ manipulation.

Un bon design facilite une décision pertinente.

# **80\. DARK PATTERNS**

Les dark patterns sont des techniques de design destinées à manipuler l'utilisateur.

Exemples :

- abonnement difficile à résilier ;
- bouton de refus caché ;
- culpabilisation ;
- options pré-cochées trompeuses ;
- frais révélés tardivement.

À connaître absolument.

# **81\. TRUST DESIGN**

La confiance peut être influencée par :

- cohérence ;
- transparence ;
- sécurité perçue ;
- informations claires ;
- preuves ;
- témoignages ;
- identité visuelle ;
- absence de comportements trompeurs.

# **82\. SOCIAL PROOF**

Exemples :

- témoignages ;
- clients ;
- statistiques ;
- certifications ;
- projets ;
- avis.

Mais la preuve doit être crédible.

# **83\. EMPTY STATES ET TRUST**

Une application vide ne doit pas sembler cassée.

Elle doit expliquer :

État  
+  
Explication  
+  
Action possible

# **84\. DESIGN ET SÉCURITÉ**

L'UI/UX interagit avec la cybersécurité.

Exemples :

- mot de passe ;
- MFA ;
- confirmation ;
- permissions ;
- sessions ;
- avertissements ;
- phishing.

Une sécurité trop compliquée peut provoquer des comportements dangereux.

C'est pourquoi :

**Security UX** existe.

# **85\. DESIGN ET PERFORMANCE**

Le design doit prendre en compte :

- poids des images ;
- vidéos ;
- animations ;
- 3D ;
- JavaScript ;
- fonts ;
- lazy loading ;
- responsive images.

Un design impossible à charger rapidement n'est pas nécessairement un bon design.

# **86\. DESIGN ET SEO**

Certaines décisions UI/UX ont des conséquences SEO :

- structure ;
- navigation ;
- contenu ;
- performance ;
- accessibilité ;
- liens ;
- HTML sémantique.

Le design ne doit donc pas être pensé complètement isolément du Web.

# **87\. DESIGN ET DÉVELOPPEMENT**

Un designer doit comprendre certaines contraintes techniques.

Un développeur doit comprendre certaines contraintes de design.

Exemple :

Un composant visuellement magnifique peut être extrêmement difficile à maintenir.

Il faut rechercher :

esthétique + cohérence + faisabilité + performance.

# **88\. DESIGN HANDOFF**

Le passage design → développement nécessite notamment :

- dimensions ;
- états ;
- responsive ;
- comportements ;
- assets ;
- typographie ;
- tokens ;
- composants.

Un prototype seul peut ne pas suffire.

# **89\. DEVELOPER EXPERIENCE ET DESIGN SYSTEM**

Un bon design system doit également être utilisable par les développeurs.

Il faut donc penser :

Design  
↕  
Documentation  
↕  
Components  
↕  
Code

# **90\. COMMENT CHOISIR UNE DIRECTION ARTISTIQUE**

Avant de choisir un style :

### **Étape 1**

Définir l'audience.

### **Étape 2**

Définir la perception recherchée.

### **Étape 3**

Définir les contraintes du secteur.

### **Étape 4**

Définir la personnalité.

### **Étape 5**

Définir les références.

### **Étape 6**

Définir ce que l'on refuse.

### **Étape 7**

Construire plusieurs directions.

### **Étape 8**

Comparer.

# **91\. MATRICE DE DIRECTION ARTISTIQUE**

|     |     |     |     |
| --- | --- | --- | --- |
| **Critère** | **Direction A** | **Direction B** | **Direction C** |
| Clarté |     |     |     |
| Originalité |     |     |     |
| Crédibilité |     |     |     |
| Cohérence marque |     |     |     |
| Performance |     |     |     |
| Accessibilité |     |     |     |
| Faisabilité |     |     |     |
| Conversion |     |     |     |
| Mémorisation |     |     |     |

# **92\. DESIGN PREMIUM**

« Premium » ne signifie pas nécessairement :

- noir ;
- énorme typographie ;
- animations ;
- gradients ;
- 3D.

Le premium peut venir de :

- précision ;
- cohérence ;
- qualité du contenu ;
- photographie ;
- espace ;
- typographie ;
- détail ;
- performance ;
- simplicité.

# **93\. DESIGN TECH**

Un design technique n'est pas nécessairement :

bleu + néon + grille + code.

Il peut être :

- éditorial ;
- industriel ;
- minimal ;
- brutaliste ;
- scientifique ;
- institutionnel.

Le secteur ne doit pas dicter automatiquement le style.

# **94\. DESIGN BRUTALISTE**

Caractéristiques possibles :

- forte typographie ;
- contraste ;
- structures volontairement brutes ;
- compositions non conventionnelles.

Pertinent dans certains contextes.

Pas nécessairement adapté à :

- banque ;
- administration ;
- assurance ;
- outil médical.

# **95\. DESIGN EDITORIAL**

Inspiré des magazines et publications.

Fort sur :

- typographie ;
- photographie ;
- composition ;
- storytelling.

Très intéressant pour :

- portfolios ;
- studios ;
- agences ;
- culture ;
- médias.

# **96\. DESIGN MINIMALISTE**

Peut être très efficace lorsqu'il repose sur :

- hiérarchie ;
- espace ;
- contenu ;
- typographie.

Le danger :

confondre minimalisme avec absence de personnalité.

# **97\. IMMERSIVE DESIGN**

Peut utiliser :

- 3D ;
- WebGL ;
- motion ;
- vidéo ;
- audio ;
- transitions ;
- storytelling.

Mais son coût peut être élevé.

Toujours demander :

Qu'est-ce que l'immersion apporte à l'expérience ?

# **98\. NIVEAU « QUAND PENSER À QUOI ? »**

Voici la carte mentale essentielle.

### **Je crée une application.**

Je pense à :

UX  
↓  
User flows  
↓  
Information architecture  
↓  
Wireframes  
↓  
UI  
↓  
Components  
↓  
Responsive  
↓  
Accessibility  
↓  
Implementation  
↓  
Testing

### **Je crée un site vitrine.**

Je pense à :

Positionnement  
↓  
Audience  
↓  
Message  
↓  
Information hierarchy  
↓  
Navigation  
↓  
Conversion  
↓  
Visual identity  
↓  
Responsive  
↓  
Performance

### **Je crée un SaaS.**

Je pense davantage à :

Onboarding  
Dashboard  
Navigation  
States  
Permissions  
Forms  
Empty states  
Errors  
Feedback  
Data density  
Accessibility

### **Je crée un portfolio.**

Je pense à :

Positionnement  
+  
Storytelling  
+  
Projects  
+  
Proof  
+  
Visual identity  
+  
Differentiation  
+  
Performance

### **Je crée un e-commerce.**

Je pense à :

Discovery  
Search  
Filters  
Product pages  
Trust  
Cart  
Checkout  
Errors  
Payments  
Mobile  
Conversion

# **99\. LE MODÈLE « 5 NIVEAUX » POUR TOUTE INTERFACE**

Pour analyser n'importe quelle interface :

## **Niveau 1 — Compréhension**

Est-ce que je comprends ?

## **Niveau 2 — Navigation**

Est-ce que je sais où aller ?

## **Niveau 3 — Action**

Est-ce que je sais quoi faire ?

## **Niveau 4 — Feedback**

Est-ce que je sais ce qui s'est passé ?

## **Niveau 5 — Confiance**

Est-ce que je fais confiance au système ?

# **100\. LE MODÈLE « POURQUOI ? » CONTRE LE DESIGN AUTOMATIQUE**

Quand l'IA propose quelque chose :

Pourquoi cette couleur ?

Pourquoi cette taille ?

Pourquoi ce composant ?

Pourquoi cette animation ?

Pourquoi cette position ?

Pourquoi cette information ici ?

Pourquoi cette information maintenant ?

Pourquoi cette interaction ?

Si l'IA ne peut pas fournir de justification cohérente, il faut réévaluer.

# **101\. CE QU'IL NE FAUT PAS DEVENIR**

Cette culture du design ne doit pas te transformer en quelqu'un qui :

- critique tout ;
- cherche constamment l'originalité ;
- refuse les conventions ;
- ajoute des animations partout ;
- complexifie les interfaces ;
- utilise du jargon pour paraître expert.

L'objectif est exactement l'inverse :

**être capable de savoir quand une convention est pertinente et quand il faut s'en écarter.**

# **102\. LA COMPÉTENCE CENTRALE : LE DESIGN JUDGMENT**

Le niveau avancé n'est pas :

connaître 500 règles.

C'est savoir arbitrer.

Exemple :

Originalité  
↕  
Familiarité  
<br/>Immersion  
↕  
Performance  
<br/>Minimalisme  
↕  
Information  
<br/>Sécurité  
↕  
Simplicité  
<br/>Esthétique  
↕  
Utilisabilité  
<br/>Créativité  
↕  
Convention

Il n'existe pas toujours de réponse absolue.

# **103\. MATRICE DE DÉCISION DESIGN**

Avant une décision importante :

|     |     |
| --- | --- |
| **Question** | **Réponse** |
| Quel problème résout-elle ? |     |
| Pour quel utilisateur ? |     |
| Quelle valeur apporte-t-elle ? |     |
| Quel coût cognitif ? |     |
| Quel coût technique ? |     |
| Quel coût performance ? |     |
| Quel impact accessibilité ? |     |
| Quel impact business ? |     |
| Existe-t-il une alternative plus simple ? |     |
| Est-elle cohérente avec la marque ? |     |

# **104\. CARTE DE PROGRESSION**

Le développement de ta culture UI/UX peut suivre cette progression.

## **Niveau 0 — Reconnaître**

Je connais le terme.

Exemples :

- responsive ;
- wireframe ;
- CTA ;
- design system ;
- prototype.

## **Niveau 1 — Comprendre**

Je peux expliquer :

- ce que c'est ;
- pourquoi cela existe.

## **Niveau 2 — Identifier**

Je peux reconnaître quand le concept apparaît dans un projet.

## **Niveau 3 — Décider**

Je peux déterminer :

« Dans ce projet, oui/non, j'en ai besoin. »

## **Niveau 4 — Diriger l'IA**

Je peux demander à l'IA de l'utiliser correctement.

## **Niveau 5 — Contrôler**

Je peux vérifier si l'IA l'a bien utilisé.

## **Niveau 6 — Implémenter**

Je peux construire une version simple.

## **Niveau 7 — Approfondir**

Je peux étudier le concept professionnellement.

# **105\. LES CONCEPTS À APPROFONDIR PLUS TARD**

Ce document constitue une carte. Certains sujets mériteront des sessions dédiées.

### **UX**

- User Research
- Personas
- User Journey
- User Flow
- Jobs To Be Done
- Information Architecture
- Usability Testing
- Heuristic Evaluation

### **UI**

- Typography
- Color
- Grid
- Spacing
- Visual hierarchy
- Composition
- Component design

### **Interaction**

- Affordance
- Feedback
- States
- Micro-interactions
- Motion
- Navigation

### **Product**

- Conversion
- Activation
- Onboarding
- Retention
- Trust
- Empty states

### **Design systems**

- Tokens
- Components
- Patterns
- Documentation
- Governance

### **Accessibility**

- WCAG
- Keyboard navigation
- Screen readers
- ARIA
- Contrast
- Focus management

### **Design augmenté par IA**

- Design prompting
- Design critique
- AI-generated UI audit
- Design-to-code
- Design iteration
- AI design systems

# **106\. LA FICHE DE MAÎTRISE D'UN CONCEPT**

Lorsqu'un concept sera étudié en profondeur, il pourra ensuite être transformé dans STANE OS selon ce format :

\# Concept  
<br/>\## Définition  
<br/>\## Pourquoi ça existe  
<br/>\## Problème résolu  
<br/>\## Quand y penser  
<br/>\## Quand ne pas l'utiliser  
<br/>\## Fonctionnement  
<br/>\## Exemple simple  
<br/>\## Exemple réel  
<br/>\## Alternatives  
<br/>\## Avantages  
<br/>\## Limites  
<br/>\## Erreurs fréquentes  
<br/>\## Comment le demander à une IA  
<br/>\## Comment contrôler l'IA  
<br/>\## Comment l'implémenter  
<br/>\## Ressources  
<br/>\## Exemple personnel  
<br/>\## Niveau de maîtrise

# **107\. LA VISION FINALE**

L'objectif n'est pas que tu regardes un site et dises :

« La typographie utilise une police sans-serif de type X. »

Ce n'est qu'une petite compétence.

L'objectif est que tu sois capable de dire :

« Le site cible probablement des clients professionnels. Le contenu est correctement hiérarchisé, mais le CTA principal est trop faible. La direction artistique est cohérente, mais le système visuel reste assez générique. Il n'est probablement pas nécessaire d'ajouter de la 3D : une meilleure direction typographique et photographique suffirait à différencier le produit. Sur mobile, la navigation devra être repensée plutôt que simplement réduite. »

**Voilà le niveau de raisonnement recherché.**

# **108\. LE NOUVEAU MODÈLE MENTAL À RETENIR**

Quand tu vois une interface, ne pense plus uniquement :

« Est-ce que c'est beau ? »

Pense :

QUI ?  
↓  
POURQUOI ?  
↓  
QUOI ?  
↓  
COMMENT ?  
↓  
DANS QUEL CONTEXTE ?  
↓  
QUEL PARCOURS ?  
↓  
QUELLE HIÉRARCHIE ?  
↓  
QUELLE INTERACTION ?  
↓  
QUELLE IDENTITÉ ?  
↓  
QUELLES CONTRAINTES ?  
↓  
QUELS COMPROMIS ?  
↓  
COMMENT TESTER ?

# **109\. LA PLACE DE L'IA DANS CE MODÈLE**

L'IA peut intervenir à presque toutes les étapes :

Recherche  
↓  
Synthèse  
↓  
Ideation  
↓  
Architecture  
↓  
Wireframe  
↓  
Direction artistique  
↓  
UI  
↓  
Prototype  
↓  
Code  
↓  
Audit  
↓  
Itération

Mais elle ne doit pas devenir le cerveau unique du processus.

Le modèle recherché est :

TOI  
↓  
Intentions + décisions + contraintes  
↓  
IA  
↓  
Génération + exploration + implémentation  
↓  
TOI  
↓  
Évaluation + contrôle + correction

# **110\. LE PRINCIPE DIRECTEUR DU DOMAINE**

**Ne cherche pas à rendre une interface différente à tout prix. Cherche à la rendre pertinente, cohérente, compréhensible et mémorable pour son contexte.**

L'originalité peut ensuite apparaître naturellement.

Une interface n'a pas besoin de crier :

« Regardez comme je suis créative ! »

pour être remarquable.

Parfois, une typographie exceptionnelle, une excellente photographie, une grille parfaitement maîtrisée, un contenu précis et quelques interactions bien pensées suffisent.

# **111\. CHECKLIST FINALE — CULTURE UI/UX**

À terme, tu dois être capable de répondre à ces questions.

### **Compréhension**

- Qu'est-ce que l'UX ?
- Qu'est-ce que l'UI ?
- Quelle différence ?
- Qu'est-ce que l'interaction design ?
- Qu'est-ce que l'information architecture ?

### **Utilisateur**

- Qui utilise le produit ?
- Quel est son objectif ?
- Quel est son contexte ?
- Quelles sont ses frustrations ?

### **Structure**

- Quel est le user flow ?
- Comment les informations sont-elles organisées ?
- Quelle est la navigation ?
- Quelle est la hiérarchie ?

### **Visuel**

- Pourquoi cette typographie ?
- Pourquoi cette couleur ?
- Pourquoi cette grille ?
- Pourquoi cet espacement ?
- Pourquoi cette image ?

### **Interaction**

- Que se passe-t-il au clic ?
- Quel feedback ?
- Quels états ?
- Que se passe-t-il en cas d'erreur ?

### **Responsive**

- Que se passe-t-il sur mobile ?
- Que se passe-t-il sur tablette ?
- Comment les priorités changent-elles ?

### **Accessibilité**

- Peut-on naviguer au clavier ?
- Le contraste est-il suffisant ?
- Les éléments sont-ils compréhensibles sans couleur ?
- Les lecteurs d'écran peuvent-ils comprendre la structure ?

### **Performance**

- Les images sont-elles optimisées ?
- Les animations sont-elles justifiées ?
- La 3D est-elle nécessaire ?
- Le chargement est-il acceptable ?

### **Identité**

- Pourquoi ce design appartient-il à cette marque ?
- Pourrait-il être celui d'une autre entreprise ?
- Qu'est-ce qui le rend mémorable ?

### **IA**

- Ai-je donné suffisamment de contexte ?
- Ai-je défini l'utilisateur ?
- Ai-je défini l'objectif ?
- Ai-je défini la direction ?
- Ai-je défini les contraintes ?
- Ai-je indiqué ce que je ne veux pas ?
- L'IA justifie-t-elle ses décisions ?
- Puis-je auditer son résultat ?

# **112\. SYNTHÈSE DU DOCUMENT**

Le domaine UX/UI peut être résumé par cette architecture :

UX / UI DESIGN  
│  
┌──────────────────┴──────────────────┐  
│ │  
UTILISATEUR PRODUIT  
│ │  
Recherche Objectifs  
│ │  
Besoins Business  
│ │  
└──────────────┬──────────────────────┘  
↓  
UX  
↓  
Information Architecture  
↓  
User Flows  
↓  
Interaction Design  
↓  
UI  
↓  
Design System + Components  
↓  
Responsive + Accessibility  
↓  
Implementation  
↓  
Testing + Analytics  
↓  
Iteration

Et avec l'IA :

INTENTION HUMAINE  
↓  
CONTEXTE  
↓  
CONTRAINTES  
↓  
DIRECTION  
↓  
──────────────  
IA  
──────────────  
↓  
EXPLORATION  
↓  
GÉNÉRATION  
↓  
IMPLÉMENTATION  
↓  
AUDIT HUMAIN  
↓  
CORRECTION  
↓  
TEST  
↓  
ITÉRATION

# **113\. CE QUE TU DOIS RETENIR AVANT DE PASSER À LA SUITE**

Tu n'as pas besoin de mémoriser ce document.

Tu dois surtout en sortir avec **une nouvelle manière de regarder les interfaces**.

Avant :

« Ce site est beau. »

Après ce document :

« Pourquoi ce site fonctionne-t-il ? »

Puis :

« Pour quel utilisateur ? »

Puis :

« Quel problème cette décision de design résout-elle ? »

Puis :

« Est-ce réellement nécessaire ? »

Puis :

« Est-ce adapté au contexte ? »

Puis :

« Est-ce accessible, performant et cohérent ? »

Et enfin :

**« Si je demande à une IA de produire quelque chose de similaire, quelles informations dois-je lui fournir pour qu'elle comprenne réellement l'intention plutôt que de générer un template générique ? »**

C'est précisément cette dernière capacité qui relie ce document à ton projet **AI-Augmented Technical Literacy**.