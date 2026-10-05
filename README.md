# ArtificialInquiries_7B

## Exercice 7B — Choosing the Models

Ce repository correspond à l'exercice **7B — Choosing the Models**
du document *Artificial Inquiries: A Vademecum for Workers in the Age of AI*.

L'objectif de cet exercice est de sélectionner plusieurs modèles ou exécutants
afin de leur faire réaliser les mêmes tâches et de comparer ensuite leurs résultats.

Dans le cadre de ce projet, l'exercice est adapté à une comparaison entre
deux environnements d'exécution de modèles de langage locaux :

- Ollama
- LM Studio

---

## Sujet

**Ollama vs LM Studio**

Le projet cherche à comparer deux solutions permettant d'exécuter
des modèles de langage localement sur un ordinateur.

Ollama et LM Studio ne sont pas eux-mêmes des modèles de langage.
Ce sont des environnements permettant de charger et d'exécuter
des modèles locaux.

L'idée est donc de conserver autant que possible le même modèle,
les mêmes tâches et les mêmes paramètres afin d'observer les différences
liées principalement au runtime utilisé.

---

## Question de recherche

**Quelles différences peut-on observer entre Ollama et LM Studio
lorsque le même modèle local réalise les mêmes tâches dans des conditions similaires ?**

La comparaison peut porter notamment sur :

- le temps de réponse ;
- la stabilité ;
- la facilité d'utilisation ;
- les erreurs rencontrées ;
- la qualité des réponses ;
- les performances disponibles ;
- la gestion des modèles.

---

## Lien avec l'exercice 7B

Dans le document *Artificial Inquiries*, l'exercice 7B demande de choisir
plusieurs modèles ou exécutants qui réaliseront les quatre tâches préparées
précédemment.

Le principe est de conserver les mêmes tâches afin de pouvoir comparer
les résultats obtenus.

Dans cette adaptation :

- Ollama représente un premier environnement d'exécution ;
- LM Studio représente un second environnement d'exécution ;
- le même modèle doit être utilisé lorsque cela est possible ;
- les mêmes prompts doivent être envoyés aux deux runtimes.

La variable principale étudiée devient donc le runtime utilisé.

---

## Principe expérimental

Pour rendre la comparaison la plus équitable possible, les conditions
suivantes doivent rester identiques :

- même ordinateur ;
- même modèle ;
- même quantification si possible ;
- même prompt ;
- même température ;
- même nombre maximum de tokens ;
- mêmes tâches.

La principale différence entre les expériences doit être :

**Ollama vs LM Studio**

---

## Tâches prévues

Plusieurs tâches simples peuvent être utilisées pour la comparaison.

### T1 — Explication générale

Demander au modèle d'expliquer un concept simple.

Objectif :

- observer la qualité générale de la réponse ;
- mesurer le temps de génération.

### T2 — Programmation

Demander au modèle de produire un petit code Python.

Objectif :

- observer la capacité à suivre des instructions ;
- comparer la qualité du code généré.

### T3 — Résumé

Fournir un texte et demander un résumé.

Objectif :

- tester la capacité de synthèse ;
- comparer la précision des réponses.

### T4 — Raisonnement simple

Donner un petit problème nécessitant une explication structurée.

Objectif :

- observer le raisonnement ;
- comparer la clarté des réponses.

---

## Données à collecter

Pour chaque expérience, les informations suivantes pourront être enregistrées :

- identifiant de l'expérience ;
- tâche utilisée ;
- runtime utilisé ;
- modèle utilisé ;
- prompt ;
- paramètres ;
- date et heure ;
- réussite ou erreur ;
- temps de réponse ;
- réponse générée ;
- nombre de tokens si disponible ;
- tokens par seconde si disponible ;
- observations manuelles.

---

## Évaluation

L'évaluation peut être divisée en deux parties.

### Mesures automatiques

- temps de réponse ;
- succès ou erreur ;
- longueur de la réponse ;
- tokens par seconde si disponibles.

### Évaluation manuelle

La réponse peut également être évaluée selon :

- la correction ;
- le respect de la consigne ;
- la clarté ;
- la qualité générale.

---

## Architecture des données

Les principales entités prévues pour l'exercice sont :

- `Task`
- `Runtime`
- `Model`
- `Experiment`
- `Result`
- `Evaluation`

Le diagramme de classes correspondant est disponible dans :

`diagram_class.md`

---

## Omeka S

Omeka S sera utilisé pour représenter et organiser les données produites
pendant l'expérience.

Il pourra permettre de stocker des informations telles que :

- les tâches ;
- les modèles ;
- les runtimes ;
- les expériences ;
- les résultats ;
- les évaluations.

Un exemple de ressource pourrait être :

```text
Experiment ID: EXP001

Task: T1

Runtime: Ollama

Model: Mistral

Response Time: 4.2 s

Success: Yes
