# PROTOCOL.md: Écosystème de Développement Axé sur les Compétences (Skill-Driven Development)

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · [Deutsch](PROTOCOL_de.md) · [Español](PROTOCOL_es.md) · **Français** · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · [Português](PROTOCOL_pt.md)

## 1. Concept et Philosophie

Ce document décrit la méthodologie de développement au sein du portefeuille, adaptée à un écosystème d'agents hybrides. Le protocole couvre l'ensemble du cycle de vie du produit — de l'ébauche architecturale initiale à la génération finale des artefacts de présentation.

Principe fondamental : **Les décisions architecturales doivent être explicites, reproductibles et défendables.** Nous sommes passés de la simple écriture de code au **Développement Axé sur les Compétences (Skill-Driven Development)**, où les opérations de routine, la conception, les tests et les analyses sont délégués à des compétences spécialisées d'agents spécifiques.

---

## 2. Rôles et Répartition des Compétences

Trois entités principales et l'environnement d'agents unifié participent au processus. Leurs rôles sont strictement séparés et ne se chevauchent pas.

### 2.1. Developer (Humain)
Le propriétaire du produit. A le dernier mot sur chaque point de décision architecturale, approuve le périmètre, définit la direction du développement et accepte les livrables des agents.

### 2.2. OpenCode (Intégrateur Autonome)
L'agent d'exécution, opérant dans le terminal avec une fenêtre de contexte allant jusqu'à 1M de tokens. Responsable de l'écriture du code, de la construction des interfaces et de la génération de documents et d'artefacts multimédias.
Possède l'arsenal de compétences suivant :
*   **Ingenierie et Code :** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **Design et Frontend :** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **Documentation et Bureau :** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **Communication et Formation :** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (Architecte et Analyste)
Agit en tant que centre de données et réviseur architectural. N'écrit pas de code de production directement, mais vérifie la logique, analyse les données de la base de données et formule des tâches pour OpenCode.
Arsenal de compétences :
*   **Gestion du Contexte :** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **Analyse et Validation :** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **BD et Visualisation des Données :** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (Environnement d'Agents Unifié)
Un environnement entièrement autonome qui intègre l'ensemble des 33 compétences.
*   **Règle clé :** Toute la documentation du projet doit désormais être créée et maintenue exclusivement via Antigravity, en exploitant les modèles Gemini et Claude (en tant que meilleurs outils de documentation avec un accès illimité aux compétences).

---

## 3. Étapes du Protocole (Cycle de Vie du Projet)

### Étape 1 : Initialisation et ARCHITECTURE.md
L'architecture est formulée avant qu'une seule ligne de code ne soit écrite.
1.  **Claude Desktop** active les compétences `morning` et `Import-memory` pour charger le contexte et les travaux précédents. Applique ensuite `analyze` pour décomposer les exigences.
2.  **OpenCode** utilise `build-project-docs` pour créer une ébauche de `ARCHITECTURE.md`.
3.  Le document se consolide : structures de données, formats de stockage, pile technique et découpage des modules.

### Étape 2 : Grill-me (Stress-Test de l'Architecture)
L'architecture n'est pas acceptée sur parole. Elle doit être attaquée et remise en question.
1.  **Claude Desktop** applique `data-context-extractor` pour identifier les « angles morts » dans les données et `doc-coauthoring` pour générer des questions inconfortables.
2.  **OpenCode** peut utiliser `discernment-nudge` pour une auto-évaluation critique des solutions techniques proposées.
3.  Chaque point de décision litigieux est clos par une triade : **solution choisie -> raison du rejet de l'alternative -> exclusions du périmètre**.

### Étape 3 : Écarts Délibérés (Deliberate Deviations)
Une section dans `ARCHITECTURE.md` où nous enregistrons toutes les fonctionnalités et capacités que nous **choisissons consciemment de ne pas concevoir**. La limite des capacités d'un projet fait partie intégrante de son architecture. Si une décision change en cours de développement, l'ancienne décision est déplacée ici avec la raison.

### Étape 4 : Mise en Œuvre Module par Module
Le développement progresse de bas en haut le long du graphe de dépendance.
1.  **OpenCode** implémente le cœur du projet. Pour les intégrations et les protocoles, `mcp-builder` et `claude-api` sont utilisés.
2.  Lors du travail sur l'aspect visuel, **OpenCode** active la chaîne : `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`.
3.  Pour la génération de graphiques procéduraux ou de canevas complexes, `algorithmic-art` et `canvas-design` sont appliqués.

### Étape 5 : Revue de Code & Tests
La vérification est toujours séparée de l'écriture du code.
1.  **OpenCode** effectue une passe distincte en utilisant `code-review-skill`, identifiant les bogues et les compromis.
2.  Les tests d'interface utilisateur et d'intégration sont menés via la compétence `webapp-testing`. Le résultat du test (stdout/stderr) est enregistré sans modification.
3.  **Claude Desktop** intervient pour vérifier le traitement des données : il utilise `sql-queries` et `write-query` pour vérifier l'intégrité de la base de données, ainsi que `validate-data` et `statistical-analysis` pour vérifier la logique métier.

### Étape 6 : Génération d'Artefacts et Analyses
Le projet doit être présenté à l'utilisateur ou aux parties prenantes.
1.  **Claude Desktop**, en utilisant `build-dashboard`, `create-viz` et `data-visualization`, forme des rapports basés sur les résultats ou les métriques de l'application.
2.  **OpenCode** conditionne ces données dans des artefacts commerciaux prêts à l'emploi :
    *   Rapports et spécifications : compétences `pdf`, `docx`, `xlsx`.
    *   Présentations d'architecture : compétence `pptx`.
    *   Formation et documents internes : `academy-guide`, `internal-comms`.
    *   Contenu dynamique pour les annonces : `slack-gif-creator`.

### Étape 7 : Liste de Contrôle Finale
Avant la publication, les éléments suivants sont vérifiés :
*   Synchronisation du code final avec `ARCHITECTURE.md`.
*   Présence de journaux de test réels.
*   Absence de fichiers temporaires, de caches et de clés secrètes.

---

## 4. Politique de Sélection des Modèles (Model Selection Policy)

OpenCode fonctionne sur des modèles gratuits, dont le choix est dicté par la tâche :

| Modèle | Rôle | Objectif | Statut de Confidentialité |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | Agent Autonome (Cœur) | Exécution de la matrice principale de compétences, contexte de 1M de tokens, logique multi-étapes dans le terminal. | Niveau gratuit permanent |
| **Nemotron 3 Ultra Free** | Analyste Profond | Mathématiques lourdes, algorithmes complexes, refactorisation du système à grande échelle. | **Essai NVIDIA** — les données sont enregistrées pour améliorer le produit. |
| **Nemotron 3.5 Lightning Free** | Exécuteur en Arrière-plan | Validation rapide, appels de fonctions utilitaires, traitement de pipelines de masse. | **Essai NVIDIA** — identique à Ultra. |
| **MiMo V2.5 Free** | Assistant UI/UX | Débogage de captures d'écran, `frontend-design` à la volée. | Période gratuite temporaire. |

Pour **Antigravity**, **Gemini 3.5 Flash (Medium)** est utilisé comme moteur principal pour garantir une consommation minimale des limites/quotas et permettre un travail continu sur les tâches et la documentation.

**Restriction de Sécurité :** Il est **strictement interdit** de transmettre des clés privées, des tokens, des bases de données réelles et des dépôts privés aux points de terminaison d'essai (Nemotron, MiMo). Seul un environnement local ou de confiance est utilisé pour les données sensibles.

---

## 5. Principes Fondamentaux de l'Écosystème

1. **Une décision explicite vaut mieux qu'un choix par défaut pratique.** Si un agent rencontre un dilemme, il ne devine pas ; il formule des options et attend l'approbation (ou enregistre un compromis).
2. **Les compétences sont utilisées aux fins prévues.** Il n'est pas nécessaire de générer des tableaux Markdown si un rapport Excel est requis (utilisez `xlsx`). Il n'est pas nécessaire de décrire un tableau de bord par écrit (utilisez `build-dashboard` + `create-viz`).
3. **Un bogue détecté lors de la revue signifie un système fonctionnel.** Une découverte lors de l'étape de revue via `code-review-skill` est la preuve que le filtre à deux étapes fonctionne.
4. **Les limites du projet sont inviolables.** Un outil à moitié fini qui « fait tout » est pire qu'un outil hautement spécialisé doté d'une section Écarts Délibérés (Deliberate Deviations) clairement documentée.
