# 🎓 Formation QA & IA Générative - Instructions de Préparation

## 📋 Informations Générales

**Titre** : L'IA Générative au Service du QA : Du Prompting Avancé à l'Automatisation Intelligente

**Durée** : 3h30 à 4h (demi-journée)

**Niveau** : Intermédiaire

**Date/Lieu** : À définir

**Nombre de participants** : 8

**Plateforme de contenu** : GitHub Pages (pages web statiques + exemples interactifs)

**URL de distribution** : À générer lors du déploiement

---

## 👥 Public Cible

- **Profil 1 (50%)** : Testeurs manuels - Pas d'expérience de scripting, cherchent à automatiser/optimiser leurs tests
- **Profil 2 (50%)** : Scripteurs QA - Familiers avec l'automatisation, veulent améliorer leur productivité avec l'IA
- **Prérequis** : Tous maîtrisent GitHub et disposent d'un accès à **GitHub Copilot**
- **Infrastructure** : Ordinateurs portables avec outils installés :
  - TestComplete
  - Cypress
  - Locus
  - Jira
  - Xray
  - GitHub Copilot

---

## 🎯 Domaine Métier

**Secteur** : **Finances**

Les exemples et cas d'usage doivent être contextualisés dans le domaine financier :
- Virement bancaire
- Calcul d'intérêts
- Validation de montants
- Flux d'authentification 2FA
- Gestion de portefeuille
- Conformité et audit trails

---

## 📚 Structure de la Formation (4 Sections)

### **Section I : Le Paysage de l'IA Générative en QA** (25 min)
*Contexte et fondamentaux*

**Objectifs pédagogiques** :
- Définir l'IA comme **accélérateur, non remplaçant**
- Comprendre les Grands Modèles de Langage (LLMs) en contexte QA
- Identifier les tâches QA les plus optimisables
- Reconnaître le potentiel ET les limites critiques

#### **1.1 Introduction : L'IA comme Accélérateur**

**Concept Central** : L'IA Générative n'est pas magique, ce sont des **LLMs entraînés** sur des quantités massives de code et texte.

**Paradigme du Prompting Avancé** : Passer du "Comment" au "Quoi"
- **Avant** : QA passe du temps sur la syntaxe, le formatage, la structure
- **Après** : QA se concentre sur la stratégie, la valeur métier, les risques (IA gère le "Comment")

**Les Tâches QA les Plus Optimisables** :

| Domaine | Cas d'Usage | Impact |
|---------|-----------|--------|
| **Rédaction** | Génération de cas de test Gherkin, documentation, User Stories structurées | 🟢 Très Optimisable |
| **Codage** | Génération de scripts API setup, fonctions utilitaires complexes, mocks de données | 🟢 Très Optimisable |
| **Analyse** | Débogage de logs (Locus), identification des causes de flakiness | 🟢 Très Optimisable |

#### **1.2 Potentiel vs. Limites : Le Contrat de Confiance (15 min)**

**Ce que l'IA fait TRÈS bien (Potentiel)** :
- ✅ **Génération de Structure** : Créer des formats rigides (JSON, Gherkin, TypeScript)
- ✅ **Standardisation** : Appliquer des contraintes strictes (ex: n'utiliser que data-cy)
- ✅ **Diagnostic Rapide** : Analyser un log volumineux et proposer des hypothèses de correction
- ✅ **Paraphrase Intelligente** : Rédiger différentes versions du même test

**Les Limites Cruciales - Les Règles de l'Utilisateur** :
- ⚠️ **"Garbage In, Garbage Out"** : Sans contexte, l'IA génère du code générique et non conforme → **C'est le pont vers la Section II (Prompting)**
- ⚠️ **Pas de Jugement Métier** : L'IA ne comprend pas la valeur d'un test sans un prompt qui lui donne ce rôle (Persona)
- ⚠️ **Les Hallucinations** : L'IA peut inventer des sélecteurs ou fonctions qui n'existent pas
- ⚠️ **Pas de Compréhension Réelle** : L'IA ne "comprend" pas les règles métier - elle mime les patterns

**💡 Le Message Clé** : Plus vous maîtrisez le **prompting**, meilleur sera le résultat. D'où la priorité à la Section II.

#### **1.3 Démonstration "Effet Waouh" (10-15 min)**

**Scénario** : Utiliser un prompt avancé pré-préparé pour générer un test complet end-to-end.

**L'Exemple Concret** : Modification d'un Projet Redmine
- Temps **sans IA** : 15-20 minutes (consulter doc API, écrire code, tester)
- Temps **avec IA + bon prompt** : 2-3 minutes (copier résultat, adapter contexte)

**Les 3 Étapes** :
1. Exécuter **Prompt Avancé 1** (création projet API) → IA génère le code
2. Montrer le résultat → souligner la complexité du code généré
3. Exécuter **Prompt Avancé 2** (test UI) → montrer le test complet
4. Exécuter **Prompt Avancé 3** (suppression API) → montrer le nettoyage

**Le Message** : Ce résultat n'est possible que si l'on maîtrise **l'Anatomie du Prompt** (Rôle, Tâche, Contexte, Contraintes, Format) → **transition vers Section II**.

**Format** :
- Présentation slides + démo en direct (live coding)
- 2-3 démos courtes d'outils (Copilot, Xray)

**Livrables** :
- Page HTML statique avec contenus, ressources, et liens vers Section II


### **Section II : L'Art du Prompting - De la Requête Basique à la Commande Optimale** (90 min - NOYAU)

**C'est la section la plus importante et celle qui demande le plus de pratique**

**Objectifs pédagogiques** :
- Maîtriser les techniques de prompting avancées (Persona, Few-Shot, Chain-of-Thought)
- Comprendre les mécanismes sous-jacents
- Adapter le prompting au contexte QA
- Générer des artefacts testables et reproductibles

#### **Module 2.1 : Anatomie d'un Prompt Efficace - Les 5 Composantes** (20 min)

Les 5 composantes essentielles d'un prompt performant :

| Composante | Description | Pourquoi c'est crucial pour la QA |
|-----------|-----------|--------------------------------|
| **A. Rôle (Persona)** | "Agis comme..." | Force l'IA à adopter un état d'esprit précis (ex: Dev Full-Stack, Testeur Sécurité, QA débutant). |
| **B. Tâche (Goal)** | "Génère/Analyse/Débogue..." | L'action claire attendue. |
| **C. Contexte (Input)** | Les données d'entrée (code, logs, User Story, environnements). | L'IA doit comprendre l'environnement technique (ex: Cypress, Python, Xray Gherkin). |
| **D. Contraintes (Rules)** | Format, longueur, standards de code, bonnes pratiques. | **Assure la conformité QA** (ex: "N'utilise que data-cy", "Respecte POM"). |
| **E. Format (Output)** | Le livrable précis (JSON, Markdown, Gherkin, tableau). | Permet l'**intégration directe** dans Jira, Xray ou les scripts. |



#### **Module 2.2 : Les Techniques de Prompting Avancées** (30 min)

**A. Persona Prompting (Le Chapeau de l'Expert)**

L'idée : Demander à l'IA d'adopter un rôle spécifique **améliore drastiquement la qualité**.

Exemple :

Prompt Basique (❌ Générrique) :
```
Écris-moi un test pour la connexion.
```

Prompt Structuré (✅ Efficace) :
```
**Rôle** : Tu es un ingénieur QA senior spécialisé en Cypress.
**Tâche** : Écris un test end-to-end pour la connexion.
**Contexte** : 
Cypress + TypeScript, Page Object Model.

Voici le code HTML réel du formulaire de connexion :
```html
<form onsubmit="return keepAnchorOnSignIn(this);" action="/login" accept-charset="UTF-8" name="form-135c0b32" method="post">
  <input name="utf8" type="hidden" value="✓" autocomplete="off">
  <input type="hidden" name="authenticity_token" value="8QarMovvHJAixMfws8J701f3rvmvfIvtfaH5KS0R6XDDA60hQb44mthQUBRiiJXKaz1Gy0hiyrj+9QNpCfVhww==" autocomplete="off">
  <input type="hidden" name="back_url" value="/logout" autocomplete="off">
  
  <label for="username">Identifiant</label>
  <input type="text" name="username" id="username" tabindex="1" autofocus="autofocus">
  
  <label for="password">Mot de passe</label>
  <input type="password" name="password" id="password" tabindex="2">
  
  <label for="autologin">
    <input type="checkbox" name="autologin" id="autologin" value="1" tabindex="4"> Rester connecté
  </label>
  
  <input type="submit" name="login" value="Connexion" tabindex="5" id="login-submit">
</form>
```

**Contraintes** : N'utilise que des locators solides. Gère les timeouts asynchrones.
**Format** : Code TypeScript complet, prêt à l'emploi.
```

**B. Chain-of-Thought (CoT) - La Pensée Logique**

L'idée : Demander à l'IA de **décrire son raisonnement étape par étape** augmente drastiquement la qualité des sorties complexes.

Exemple - Analyser un log d'erreur complexe :

```
**Rôle** : Tu es un analyste DevOps spécialisé en diagnostic de logs d'application et bases de données.

**Tâche** : Analyse le log d'erreur ci-dessous et propose :
1) La cause racine la plus probable.
2) Une correction immédiate.
3) Une suggestion pour prévenir ce problème.

**Contexte** : 
Voici un extrait des logs d'une application Redmine lors d'un test automatisé :

```
[2025-11-02T14:35:12.500Z] INFO [c0a1d4f2] - Request received: GET /issues/list.json from 10.0.0.5. Processing time: 90ms.
[2025-11-02T14:35:12.520Z] INFO [a8e7c6d3] - Scheduler task 'CleanupSessions' started.
[2025-11-02T14:35:12.555Z] INFO [c0a1d4f2] - Database query: SELECT issues where status=open. Rows returned: 450.
[2025-11-02T14:35:12.601Z] INFO [a9f3b2d1] - Request received: PATCH /projects/test-modify.json from 192.168.1.10. Starting transaction.
[2025-11-02T14:35:12.610Z] INFO [c0a1d4f2] - Request finished successfully.
[2025-11-02T14:35:12.650Z] INFO [a9f3b2d1] - User 'qa-tester' authorized successfully. Starting project update.
[2025-11-02T14:35:12.670Z] INFO [b1c2d3e4] - Request received: GET /users/current.json from 10.0.0.6. Processing time: 30ms.
[2025-11-02T14:35:12.701Z] INFO [a8e7c6d3] - Scheduler task 'CleanupSessions' finished. Duration: 181ms.
[2025-11-02T14:35:12.720Z] INFO [b1c2d3e4] - Request finished successfully.
[2025-11-02T14:35:12.755Z] INFO [a9f3b2d1] - Database query: UPDATE projects SET description = 'Nouvelle description testée par IA' WHERE identifier = 'test-modify'.
[2025-11-02T14:35:12.760Z] INFO [d4e5f6g7] - Request received: POST /issues/1234/notes.json from 192.168.1.12. Starting transaction.
[2025-11-02T14:35:12.775Z] INFO [d4e5f6g7] - User 'dev-team' authorized. Comment added to issue 1234.
[2025-11-02T14:35:12.789Z] ERROR [a9f3b2d1] - **ConstraintViolationException: Column 'updated_on' cannot be NULL.** Transaction rollback initiated.
[2025-11-02T14:35:12.800Z] INFO [d4e5f6g7] - Transaction committed successfully. Response time: 40ms.
[2025-11-02T14:35:12.805Z] WARN [a9f3b2d1] - Could not commit transaction. Retrying logic failed.
[2025-11-02T14:35:12.820Z] INFO [f7g8h9i0] - Request received: GET /settings.json from 10.0.0.7. Processing time: 50ms.
[2025-11-02T14:35:12.835Z] INFO [f7g8h9i0] - Configuration fetched successfully.
[2025-11-02T14:35:12.850Z] ERROR [a9f3b2d1] - **HTTP 500 Internal Server Error sent to client.** Cause: Transaction failed due to backend database constraint.
[2025-11-02T14:35:12.870Z] INFO [j1k2l3m4] - Request received: GET /notifications/unread.json from 10.0.0.8. Processing time: 65ms.
[2025-11-02T14:35:12.899Z] INFO [a9f3b2d1] - Response time: 298ms.
[2025-11-02T14:35:12.905Z] INFO [j1k2l3m4] - Request finished successfully.
[2025-11-02T14:35:13.001Z] INFO [k5l6m7n8] - Request received: GET /status from 10.0.0.9. Processing time: 10ms.
[2025-11-02T14:35:13.020Z] INFO [o9p0q1r2] - Request received: GET /projects/summary.json from 192.168.1.10.
[2025-11-02T14:35:13.050Z] INFO [o9p0q1r2] - User 'qa-tester' is checking project summary after failure.
[2025-11-02T14:35:13.080Z] INFO [r3s4t5u6] - Database query: INSERT INTO audit_log VALUES ('User login success', 'admin').
[2025-11-02T14:35:13.100Z] INFO [o9p0q1r2] - Project summary generated. Response time: 80ms.
[2025-11-02T14:35:13.120Z] INFO [v7w8x9y0] - Request received: GET /time_entries/activities.json from 10.0.0.11.
[2025-11-02T14:35:13.150Z] INFO [v7w8x9y0] - List of activities retrieved.
```

**Contraintes** : Avant de donner la réponse, décris ton raisonnement étape par étape en analysant :
- Les requêtes concurrentes
- Les timestamps et corrélations d'ID de transaction
- La séquence d'événements menant à l'erreur
- Les contraintes de base de données impliquées

**Format** : Un tableau Markdown avec les trois points demandés.
```

**Impact** : L'IA ne donne pas seulement la réponse, elle **justifie son diagnostic** comme un ingénieur expérimenté en analysant les 28 lignes de logs pour isoler le problème lié à la transaction [a9f3b2d1].

**C. Few-Shot Prompting (L'Exemple Maître)**

L'idée : Fournir un ou deux exemples de la sortie souhaitée **avant** la vraie requête.

Exemple - Générer des données de test financières avec structure spécifique :

```
**Rôle** : Expert en génération de données de test pour applications financières.

**Tâche** : Génère 10 cas de test pour la validation d'IBAN avec différents scénarios (valides et invalides).

**Exemples de Format Souhaité** :

Cas 1:
{
  "iban": "FR7630006000011234567890189",
  "pays": "France",
  "valide": true,
  "raison": "IBAN français valide avec checksum correct"
}

Cas 2:
{
  "iban": "FR7630006000011234567890188",
  "pays": "France", 
  "valide": false,
  "raison": "Checksum incorrect (dernier chiffre modifié)"
}

Cas 3:
{
  "iban": "DE891234567890123456",
  "pays": "Allemagne",
  "valide": false,
  "raison": "Longueur invalide (IBAN allemand doit avoir 22 caractères)"
}

**Contexte** : 
- IBAN français : 27 caractères (FR + 2 chiffres contrôle + 23 chiffres)
- IBAN allemand : 22 caractères (DE + 2 chiffres contrôle + 18 chiffres)
- IBAN belge : 16 caractères (BE + 2 chiffres contrôle + 12 chiffres)

**Contraintes** : 
- Suivre EXACTEMENT le format JSON des exemples
- Inclure au moins 5 cas valides et 5 cas invalides
- Varier les raisons d'invalidité (checksum, longueur, format, pays inexistant)

**Format** : Array JSON avec objets structurés comme dans les exemples.
```

**Impact** : L'IA génère des données de test cohérentes, structurées et variées en suivant précisément le pattern fourni. Les exemples montrent clairement ce qui est attendu (structure, diversité des cas, niveau de détail).

**Exercice Pratique 2.2.1** :
- Comparer un prompt SIMPLE vs. PERSONA vs. CoT vs. FEW-SHOT
- Analyser les différences de qualité
- Mesurer le temps de génération

#### **Module 2.3 : Prompting pour la Génération de Tests** (20 min)

**Cas d'Usage 1 : Générer des Cas de Test Gherkin pour Xray**

```
**Rôle** : Analyste QA expert en BDD.

**Tâche** : Transforme la User Story ci-dessous en 5 scénarios Gherkin.

**Contexte** : La Story doit couvrir : Succès, Erreur de Validation, Cas Limites.

**Format** : Gherkin pur (Feature, Scénario, Étant donné, Quand, Alors).

[USER STORY ICI]
```

**Cas d'Usage 2 : Générer des Scripts Cypress Complets (Arrange-Act-Assert)**

```
**Rôle** : Ingénieur QA Cypress avec 5 ans d'expérience.

**Tâche** : Génère un test E2E pour [scénario métier].

**Contexte** : Page Object Model, data-test-id, TypeScript.

**Format** : Code complet, avec setup, test, et cleanup.
```

**Cas d'Usage 3 : Générer des Données de Test Financières Valides**

```
**Rôle** : Expert en données financières et normes ISO 13616 (IBAN).

**Tâche** : Génère 10 virements de test valides pour [contexte].

**Contraintes** : 
- IBANs conformes ISO 13616
- Montants entre 0.01€ et 999,999.99€
- Devises variées (EUR, USD, GBP)
- Dates futures interdites

**Format** : Tableau CSV ou JSON.
```

**Exercice Pratique 2.2.2** :
- Générer un cas de test complet pour un flux métier (testeurs manuels)
- Générer un script Cypress pour 3 scénarios (scripteurs)
- Générer des données de test financières valides (tous)

#### **Module 2.4 : Prompting pour l'Analyse et le Debugging** (20 min)

**Cas d'Usage 1 : Déboguer un Test Flaky avec CoT**

```
**Rôle** : Débogueur Test Automation.

**Tâche** : Identifie la cause et propose DEUX solutions :
- Solution 1 : Avec cy.wait() (rapide)
- Solution 2 : Avec cy.get().should() (robuste - recommandée)

**Contexte** : 
[LOG D'ERREUR COMPLÈTE]

**Contraintes** : Avant de répondre, décris ton raisonnement étape par étape.

**Format** : Deux blocs de code TypeScript avec annotations.
```

**Cas d'Usage 2 : Analyser un Incident Production avec Chain-of-Thought**

Voir **Prompt Avancé 9** dans le fichier `prompts-avances.md`.

**Cas d'Usage 3 : Évaluer la Robustesse des Sélecteurs**

```
**Rôle** : Expert en stabilité des sélecteurs Cypress.

**Tâche** : Classe ces 3 sélecteurs par robustesse :
1. cy.get('button').first()
2. cy.get('.btn-primary')
3. cy.get('[data-test-id="submit"]')

**Contraintes** : Utilise une échelle 1-5, explique les risques.

**Format** : Tableau Markdown comparatif.
```

**Exercice Pratique 2.3.1** :
- Analyser un script défaillant avec Copilot
- Proposer des corrections
- Implémenter les améliorations

#### **Module 2.5 : Techniques Avancées - Prompt Chaining & RAG** (20 min)

**A. Prompt Chaining (Décomposer en Sous-Prompts)**

Générer un test **complet** en 3 étapes chaînées :

```
**Étape 1 - Setup** : Génère createProjectAPI()
**Étape 2 - Test** : Génère le test de modification (utilise résultat étape 1)
**Étape 3 - Teardown** : Génère deleteProjectAPI()

Résultat final : Un fichier complet avec les 3 étapes.
```

**B. RAG (Retrieval-Augmented Generation) - Contexte Spécifique du Projet**

Au lieu de donner des instructions génériques, fournissez :
- Les conventions du projet (noms, formats, patterns)
- Les fichiers de configuration (tsconfig.json, cypress.config.js)
- Les exemples existants (code réel du projet)

```
**Contexte Projet** :
```yaml
Application: Redmine v4.2
Framework: Cypress v13.0
Conventions:
  - Sélecteurs: MUST use data-test-id
  - Nommage: snake_case
  - POM: Structure Pages/ et Specs/
```

**Résultat** : Code 100% conforme au projet, sans ajustements nécessaires.
```

**Exercice Pratique 2.4.1** :
- Construire une chaîne de prompts complète
- Générer un test end-to-end intégrant setup + test + teardown
- Valider le résultat en l'exécutant

**Format Section II** :
- Présentation théorique (slides + démos)
- **5 exercices pratiques** (en groupe ou individuels)
- Feedback collectif après chaque exercice

**Livrables Section II** :
- Page web avec modules interactifs
- Fichiers d'exercices pré-structurés
- **Fichier `prompts-avances.md`** : 14 prompts prêts à copier/coller
- Mémo "Quick Tips" pour le prompting
- Exemples annotés (avant/après)




### **Section III : IA et Outillage QA - Levier de Productivité Ciblé** (50 min)

**Intégration pratique avec les outils existants**

**Objectifs pédagogiques** :
- Intégrer l'IA dans les workflows existants
- Maximiser la productivité avec les outils cités
- Comprendre les extensions/plugins disponibles
- Appliquer les cas d'usage métier spécifiques

#### **Module 3.1 : GitHub Copilot dans l'IDE** (15 min)

**Cas d'Usage** : Génération de code intelligent pour Cypress et TestComplete

Démonstration en direct :
1. Générer une fonction API complexe (avec Copilot)
2. Génération d'un Page Object Model (POM)
3. Autocomplétion intelligente sur TestComplete

**Exercice Pratique 3.1.1** :
- Compléter un script de test Cypress avec Copilot (5-10 min)
- Comparer temps manuel vs. avec IA
- Mesurer la productivité

**Livrables** :
- Template POM pré-optimisé pour Cypress
- Snippets Copilot pour Cypress
- Best practices IDE

#### **Module 3.2 : Xray & Jira + IA** (15 min)

**Cas d'Usage** : Automatisation complète User Story → Cas de Test → Exécution

Flux complet :
```
User Story Jira → [IA génère] → Scénarios Gherkin → [Import] → Xray → [Exécution automatisée]
```

**Techniques** :
- Transformation User Story → Gherkin avec Few-Shot Prompting
- Identification automatique des conditions limites
- Génération de données de test conformes

**Démonstration** :
- Coller une User Story Jira
- Générer les cas de test avec Copilot
- Copier/coller dans Xray

**Exercice Pratique 3.2.1** :
- Générer des cas de test à partir d'une US Jira (15 min)
- Les formatter pour Xray
- Vérifier la couverture des critères d'acceptation

**Livrables** :
- Guide : User Story → Gherkin
- Template de cas de test Xray
- Checklist de couverture

#### **Module 3.3 : TestComplete + IA** (10 min)

**Cas d'Usage** : Générer des scripts TestComplete robustes avec sélecteurs intelligents

Techniques :
- Génération de fonctions utilitaires TestComplete
- Gestion des objets et des propriétés
- Maintenance assistée par IA

**Démonstration courte** :
- Générer un script TestComplete pour flux d'authentification
- Souligner la robustesse des sélecteurs

**Exercice Pratique 3.3.1** :
- Générer un script TestComplete pour un flux simple
- Valider son exécution

**Livrables** :
- Template script TestComplete
- Bonnes pratiques de sélecteurs

#### **Module 3.4 : Cypress + IA** (10 min)

**Cas d'Usage** : Patterns Cypress modernes + Copilot

Techniques :
- Page Object Model generation automatique
- Gestion des attentes asynchrones avec CoT
- Assertions intelligentes

**Démonstration** :
- Générer un POM Cypress avec Copilot
- Souligner la qualité du code généré

**Exercice Pratique 3.4.1** :
- Générer un test Cypress E2E complet (10-15 min)
- Inclure setup, test, et cleanup
- Exécuter le test

**Livrables** :
- Template POM Cypress
- Patterns de test robustes
- Checklist de qualité

**Format Section III** :
- Démos interactives (live coding)
- **4 exercices courts** (1 par outil, 5-10 min chacun)
- Partage des résultats

**Livrables Section III** :
- Page web : guide d'intégration par outil
- Templates de scripts pré-optimisés
- Checklist de configuration pour chaque outil
- Cas d'usage concrets dans le contexte financier (virements, 2FA, calculs)




### **Section IV : Les Pouvoirs Avancés de l'IA - Au-delà de l'Assistance** (30 min)

**Cas avancés et perspectives**

**Objectifs pédagogiques** :
- Explorer les cas d'usage avancés et moins évidents
- Comprendre les limites réelles et bonnes pratiques
- Envisager l'évolution future (agents autonomes, etc.)
- Définir une stratégie de déploiement en équipe

#### **Module 4.1 : Injection de Contexte Implicite (Le Secret des Pros)** (10 min)

**L'Idée Centrale** : Transformer l'IA d'un "simple générateur de texte" en un "partenaire de code informé" grâce au contexte.

**A. Fichiers d'Instructions Permanents**

Concept : Un fichier `.github/copilot/prompt_settings.json` ou `**/*.instructions` dans le répertoire définit les conventions **globales** pour tous les prompts de ce répertoire.

Exemple :

```json
{
  "conventions": {
    "selectors": "MUST use data-test-id only",
    "naming": "snake_case for functions, camelCase for variables",
    "framework": "Cypress with TypeScript",
    "style": "Page Object Model mandatory"
  },
  "domain": "Finance - SEPA transfers, IBAN validation, 2FA flows"
}
```

**Impact** : Copilot génère **immédiatement du code conforme** sans ajustements.

**B. Commandes de Contexte dans Copilot Chat**

Copilot propose plusieurs commandes pour **restreindre le champ d'action** :

- **`/env`** : Analyse automatiquement l'environnement du projet (dépendances, versions)
- **`/workspace`** : Indexe tout le workspace pour le contexte
- **`/code`** : Limite la génération à un fichier/fonction spécifique
- **`/tests`** : Reste dans le contexte des tests uniquement

**Exemple d'utilisation** :

```
/code /src/tests/cypress/pages/LoginPage.ts
"Génère une méthode waitForSuccessMessage() suivant le pattern du fichier."
```

**Impact** : L'IA génère du code **100% cohérent** avec les conventions du projet.

**C. Bonnes Pratiques pour l'Injection de Contexte**

1. **Fournir le contexte réel** : URLs, versions, dépendances exactes
2. **Inclure des exemples** : Un exemple existant = 1000 mots de documentation
3. **Documenter les règles métier** : "Pas de montants > 999,999.99€"
4. **Version le contexte** : Mettre à jour les fichiers `.instructions` avec le projet

**Exercice Pratique 4.1.1** :
- Créer un fichier `.instructions` pour le projet
- Générer du code AVEC contexte vs. SANS contexte
- Comparer la qualité et le temps d'ajustement

**Livrables** :
- Template `.instructions` pour Redmine QA
- Guide d'injection de contexte
- Checklist de configuration

#### **Module 4.2 : Techniques de Test Disruption & Mutant Testing** (10 min)

**L'Idée Centrale** : Utiliser l'IA pour **tester la qualité des tests eux-mêmes** (Mutant Testing).

**Concept du Mutant Testing** :
1. Introduire des "mutations" (petits changements) dans le code
2. Vérifier que les tests détectent ces mutations
3. Un bon test tue beaucoup de mutations
4. Un mauvais test ne tue aucune mutation

**Exemple** :

Code original :
```typescript
if (amount > 999999.99) {
  throw new Error("Amount too large");
}
```

Mutation 1 : `amount >= 999999.99`
Mutation 2 : `amount > 999999`
Mutation 3 : Supprimer la vérification entièrement

**Votre test détecte-t-il ces 3 mutations ?**

**Utilisation de l'IA pour le Mutant Testing** :

```
**Rôle** : Expert en Mutant Testing.

**Tâche** : Génère 5 mutations du code ci-dessous et propose un test 
qui tue chacune de ces mutations.

**Code** :
[INSÉRER CODE ICI]

**Contraintes** : Les mutations doivent être réalistes, pas triviales.

**Format** : Tableau avec colonnes Mutation | Code Muté | Test qui tue la mutation
```

**Impact** : Augmenter la qualité des tests et leur capacité de détection.

**Exercice Pratique 4.2.1** :
- Analyser un test existant
- Générer des mutations potentielles avec Copilot
- Renforcer le test pour tuer ces mutations

**Livrables** :
- Guide de Mutant Testing avec IA
- Template de mutation pour différents types de code
- Checklist de qualité de test

#### **Module 4.3 : Analyse d'Impact et Prédiction (Avancé)** (5 min)

**L'Idée** : Utiliser l'IA pour **prédire l'impact** d'un changement de code sur les tests.

Exemple :

```
**Rôle** : Analyste d'impact de changement.

**Tâche** : On modifie la règle de validation de montant de :
  - Avant : max 999,999.99€
  - Après : max 100,000€

Identifie :
1. Les tests affectés
2. Les données de test qui deviennent invalides
3. Les cas limites à ajouter

**Format** : Rapport structuré avec listes.
```

**Impact** : Anticiper les défaillances et les ajustements nécessaires.

#### **Module 4.4 : Génération de Documentation & Maintenance** (5 min)

**Cas d'Usage** :
- Générer de la documentation de test automatiquement
- Maintenir la documentation à jour
- Générer des reports automatisés
- Créer une knowledge base auto-générée

Exemple :

```
**Tâche** : Génère un README complet pour cette suite de tests Cypress.

**Contexte** : [Pointer vers src/tests/cypress/]

**Format** : Markdown structuré avec sections : Setup, Exécution, Maintenance, Troubleshooting
```

**Impact** : Réduire le temps de documentation de 80%.

#### **Module 4.5 : Collaboration & Bonnes Pratiques d'Équipe** (5 min)

**Stratégies d'Équipe** :

1. **Prompts Library** : Maintenir un répertoire des prompts éprouvés (README + exemples)
2. **Code Review des Prompts** : Valider que les prompts générés sont corrects
3. **Versioning des Prompts** : Tracker les versions comme du code
4. **Standards Collectifs** : Définir les conventions de prompting en équipe

Exemple de Prompts Library :

```
prompts-library/
├── README.md (indexe tous les prompts)
├── test-generation/
│   ├── gherkin-from-story.md (prêt à copier)
│   └── cypress-e2e-test.md (prêt à copier)
├── debugging/
│   └── flaky-test-analysis.md
└── validation/
    └── iban-validation.md
```

**Exercice Pratique 4.5.1** :
- Créer une Prompts Library pour l'équipe
- Documenter 5 prompts clés
- Versionner et partager

#### **Module 4.6 : Perspectives Futures & Veille Technologique** (5 min)

**Les Évolutions Attendues** :

1. **Agents Autonomes** : L'IA pourra exécuter des tests autonomement et proposer des corrections
2. **Auto-Healing Tests** : Les tests se répareront automatiquement lors de changements UI
3. **Prédiction de Bugs** : L'IA identifiera les bugs avant la production
4. **Test Synthesis** : Générer les tests directement à partir du code source

**Préparation** :
- Rester à jour via blogs (TestCraft, Applitools, LambdaTest)
- Experimenter avec les nouvelles versions de Copilot
- Documenter les success stories et learnings

**Ressources** :
- GitHub Copilot documentation officielle
- OpenAI Prompting best practices
- Articles sur AI in Testing

**Format Section IV** :
- Présentation courte (30 min)
- Débat/discussion avec les participants
- Partage de vision future

**Livrables Section IV** :
- Page web : cas avancés et bonnes pratiques
- Template de `.instructions` pour l'équipe
- Guide de Mutant Testing avec IA
- Template de Prompts Library
- Guide de collaboration équipe
- Ressources de veille technologique



---

## 📊 Timing Détaillé

| Section | Durée | Format |
|---------|-------|--------|
| I. Paysage IA | 25 min | Présentation + démos |
| II.1 Fondamentaux | 20 min | Théorie + exercice |
| II.2 Génération Tests | 30 min | Théorie + 3 exercices |
| II.3 Analyse & Debug | 20 min | Théorie + exercice |
| II.4 Avancés | 20 min | Théorie + exercice |
| **Pause** | **10 min** | |
| III.1 Copilot IDE | 15 min | Démo + exercice |
| III.2 Xray/Jira | 15 min | Démo + exercice |
| III.3 TestComplete | 10 min | Démo + exercice |
| III.4 Cypress | 10 min | Démo + exercice |
| IV. Avancés | 30 min | Théorie + débat |
| **Questions & Clôture** | **5 min** | |
| **TOTAL** | **220 min (3h40)** | |

---

## 🛠️ Architecture Technique du Contenu

```
qa-prompt-masterclass/
├── .preparation/                    # Dossier ISOLÉ de préparation
│   ├── INSTRUCTIONS.md             # Ce fichier
│   ├── PRD.md                       # Product Requirements Document
│   ├── planning/
│   │   ├── timeline.md             # Calendrier de production
│   │   ├── ressources.md           # Ressources nécessaires
│   │   └── checklist-deploiement.md
│   └── docs/
│       ├── contexte-financier.md   # Domaine métier (IBAN, calculs, etc.)
│       ├── exemples-code.md        # Code utilisé en demos
│       └── references-externes.md  # Articles, docs, outils
├── docs/                            # Contenu PUBLIC de la formation
│   ├── index.html                  # Page d'accueil principale
│   ├── section-1/                  # Paysage IA
│   │   ├── index.html
│   │   ├── slides.html
│   │   └── ressources.md
│   ├── section-2/                  # Prompting (noyau)
│   │   ├── index.html
│   │   ├── module-1.html
│   │   ├── module-2.html
│   │   ├── module-3.html
│   │   ├── module-4.html
│   │   ├── exercices.md
│   │   └── solutions/
│   ├── section-3/                  # Outillage QA
│   │   ├── index.html
│   │   ├── copilot-ide.html
│   │   ├── xray-jira.html
│   │   ├── testcomplete.html
│   │   ├── cypress.html
│   │   └── exercices.md
│   ├── section-4/                  # Avancés
│   │   ├── index.html
│   │   ├── analyse-impact.html
│   │   ├── documentation.html
│   │   ├── bonnes-pratiques.html
│   │   └── ressources-futures.md
│   ├── assets/
│   │   ├── css/
│   │   ├── js/
│   │   └── img/
│   └── exercices/                  # Fichiers d'exercices prêts à l'emploi
│       ├── section-2/
│       ├── section-3/
│       └── section-4/
└── README.md                        # Vue d'ensemble du projet
```

---

## 📝 Exercices - Format & Livrables

### Format Mixte

**Type 1 : Exercices sur machines** (testeurs manuels + scripteurs)
- Prompts à affiner directement dans GitHub Copilot
- Scripts à compléter/déboguer
- Cas de test à générer dans Jira/Xray
- **Durée** : 5-10 min par exercice
- **Livrable** : Prompt optimisé + résultat généré

**Type 2 : Démos interactives**
- Démonstration en direct (animateur)
- Les participants voient les étapes
- Questions en temps réel
- **Durée** : 3-5 min par démo

### Processus pour Chaque Exercice

1. **Setup** : Fichiers pré-structurés disponibles (templates vides à compléter)
2. **Instructions claires** : "Générer N cas de test pour le scénario X"
3. **Guidance progressive** : Prompts suggestifs si bloqué
4. **Validation** : Points de contrôle simples
5. **Partage** : Volontaire - montrer son résultat (5-10 min)

### Livrables Générés par les Participants

Selon les exercices :
- **Prompts optimisés** → sauvegardés dans une "prompts library"
- **Scripts de test** → TestComplete (.tcl), Cypress (.js)
- **Cas de test** → Format Xray (JSON/CSV)
- **Données de test** → CSV financières valides
- **Documentation** → Markdown ou HTML

---

## 🎮 Engagement & Interactivité

### Stratégies d'Engagement

1. **Pair programming** : Testeurs manuels + Scripteurs travaillent ensemble
2. **Live coding** : Partager l'écran, montrer les résultats en direct
3. **Q&A slots** : 5 min après chaque section majeure
4. **Défi bonus** : Exercice "champion" à la fin

### Outils de Participation

- **GitHub Copilot** : Outil principal pour tous les exercices
- **Chat collaboratif** : Slack/Teams pendant la formation
- **Live editor** : CodePen/Replit pour les démos interactives
- **Poll/Quizz** : Validation de compréhension

---

## 📦 Prérequis Techniques (Participants)

**À installer/configurer AVANT la formation** :

- [ ] Visual Studio Code (ou équivalent)
- [ ] GitHub Copilot activé + authentifié
- [ ] Git configuré
- [ ] Node.js 18+ (pour Cypress)
- [ ] Cypress installé localement
- [ ] TestComplete configuré (accès à la licence)
- [ ] Accès à Jira + Xray
- [ ] Accès au dépôt GitHub de formation (fork possible)

**Checklist pré-formation** :
- Email d'accès au dépôt GitHub
- Vérification accès Copilot
- Test des outils (30 min avant)

---

## 🎓 Objectifs de Sorties

À la fin de la formation, les participants seront capables de :

✅ **Section I** :
- Comprendre le rôle et les limites de l'IA en QA
- Identifier des cas d'usage pertinents

✅ **Section II** (PRIORITAIRE) :
- Rédiger des prompts efficaces et reproductibles
- Générer des tests et scripts automatiquement
- Déboguer avec l'IA

✅ **Section III** :
- Intégrer l'IA dans leur workflow quotidien
- Utiliser les bons outils pour la bonne tâche
- Augmenter leur productivité

✅ **Section IV** :
- Explorer des cas avancés
- Partager les bonnes pratiques en équipe
- Rester à jour sur l'évolution de l'IA

---

## 📚 Ressources de Référence

### Documentations Officielles
- GitHub Copilot Best Practices
- TestComplete AI Features (si dispo)
- Cypress Documentation
- Xray API

### Contexte Métier (Finances)
- Normes IBAN/BIC
- PCI DSS (sécurité paiements)
- Flux de conformité
- Formats de données financières

### Articles & Inspiration
- State of QA 2025 reports
- Prompting techniques (OpenAI, Anthropic)
- AI in Testing (TestCraft, etc.)

---

## ✅ Checklist de Production

- [ ] Rédiger le PRD détaillé (`PRD.md`)
- [ ] Identifier les exemples métier (finance)
- [ ] Écrire tous les scripts d'exercices
- [ ] Créer les templates vides (pour les participants)
- [ ] Générer les solutions (pour l'animateur)
- [ ] Concevoir les pages HTML
- [ ] Générer les démos interactives
- [ ] Tester tous les exercices end-to-end
- [ ] Valider avec un groupe pilote
- [ ] Déployer sur GitHub Pages
- [ ] Générer l'URL publique
- [ ] Créer la documentation de support

---

## 📞 Points de Contact & Escalades

- **Animateur Principal** : À définir
- **Support Technique** : À définir
- **Backup Présentations** : À définir
- **Contact Participants** : À définir

---

## 📅 Prochaines Étapes

1. **Valider ce document** ✓
2. **Rédiger le PRD** → détails de chaque section
3. **Collecter les exemples métier** → contexte financier
4. **Créer les scripts/solutions**
5. **Concevoir l'interface web**
6. **Tester et itérer**
7. **Déployer**

---

**Version** : 1.0 | **Date** : 16 Nov 2025 | **Auteur** : Talel Zid Préparation Formation QA-IA
