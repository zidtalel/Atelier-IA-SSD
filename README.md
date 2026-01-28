# 🎓 QA Prompt Masterclass - Formation GitHub Copilot pour QA

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Formation](https://img.shields.io/badge/Type-Formation-blue.svg)](.)
[![GitHub Copilot](https://img.shields.io/badge/GitHub-Copilot-purple.svg)](https://github.com/features/copilot)

## 📋 Description

Formation complète et interactive sur l'utilisation de l'IA générative et du prompt engineering avancé pour les professionnels du Quality Assurance (QA). Cette masterclass explore comment GitHub Copilot et les Large Language Models (LLMs) peuvent transformer les pratiques de test, de l'automatisation à la génération de code, en passant par l'analyse de logs et la création de tests E2E avancés.

## 🎯 Objectifs de la Formation

À l'issue de cette formation, vous serez capable de :

- ✅ **Comprendre le potentiel de l'IA en QA** - Identifier les tâches optimisables et les limites critiques
- ✅ **Maîtriser le prompt engineering** - Utiliser les 5 composantes essentielles (Rôle, Tâche, Contexte, Contraintes, Format)
- ✅ **Construire des applications avec l'IA** - Générer du code backend/frontend guidé par des spécifications
- ✅ **Créer des tests avancés** - Automatiser les tests E2E avec Cypress et techniques de simulation
- ✅ **Appliquer des techniques avancées** - Utiliser @workspace, #file, mutant testing et agents autonomes

## 📚 Structure du Projet

```
qa-prompt-masterclass/
├── docs/
│   ├── assets/
│   │   ├── style.css              # Styles CSS communs
│   │   ├── images/                # Images et captures d'écran
│   │   ├── navdash.zip           # Projet de base NavDash (vide)
│   │   └── navdashdev.zip        # Projet NavDash opérationnel (sans tests)
│   ├── section-1/
│   │   ├── index.html            # Le Paysage de l'IA Générative en QA
│   │   └── GUIDE-DEMO.md         # Guide pour la démonstration live
│   ├── section-2/
│   │   └── index.html            # L'Art du Prompting
│   ├── section-3/
│   │   └── index.html            # IA et Outillage QA
│   └── section-4/
│       └── index.html            # Cas d'Usage Avancés & Perspectives
├── index.html                     # Page d'accueil de la formation
├── LICENSE                        # Licence du projet
└── README.md                      # Ce fichier
```

## 📖 Contenu des Sections

### 🌐 Section 1 : Le Paysage de l'IA Générative en QA (20 min)

**Objectifs :**
- Définir l'IA comme accélérateur de tests
- Identifier les tâches QA optimisables (rédaction, codage, analyse)
- Reconnaître le potentiel ET les limites de l'IA
- Démonstration pratique : Génération de tests Gherkin pour Xray

**Concepts clés :**
- LLMs et reconnaissance de patterns
- Paradigme du prompting : passer du "Comment" au "Quoi"
- Règles "Garbage In, Garbage Out"
- Hallucinations et validation humaine

### 🎨 Section 2 : L'Art du Prompting (50 min)

**Objectifs :**
- Maîtriser les 5 composantes d'un prompt efficace
- Appliquer les techniques avancées (Few-Shot Learning, Chain-of-Thought)
- Pratiquer sur des cas réels de QA
- Éviter les anti-patterns courants

**Techniques enseignées :**
- 🔵 **Rôle** : Définir le persona de l'IA
- 🟢 **Tâche** : Spécifier l'objectif clairement
- 🟡 **Contexte** : Fournir le domaine métier
- 🔴 **Contraintes** : Imposer des règles strictes
- 🟣 **Format** : Définir le format de sortie

### 💻 Section 3 : IA et Outillage QA (50 min)

**Projet pratique : NavDash**
Application de tableau de bord diagnostic construite de A à Z avec 7 prompts successifs.

**Workflow complet :**
1. **Module 3.1** - Fondations (instructions.md, prd.md)
2. **Module 3.2** - Développement Frontend (Backend Spring Boot, JavaScript, CSS)
3. **Module 3.3** - Tests E2E Cypress avancés (cy.stub, simulations d'APIs natives)

**Technologies :**
- Java 17, Spring Boot 2.7.18
- Thymeleaf, JavaScript Vanilla
- Cypress 13, TypeScript 5
- APIs natives du navigateur (Battery, Network, Performance)

### ⚡ Section 4 : Cas d'Usage Avancés & Perspectives (40 min)

**Objectifs :**
- Maîtriser le contexte implicite (@workspace, #file, @terminal)
- Appliquer le Mutant Testing pour renforcer les tests
- Analyser l'impact des modifications avec l'IA
- Anticiper l'avenir : agents autonomes et auto-healing tests

**Techniques avancées :**
- Injection de contexte intelligent
- Génération de mutations de code
- Prédiction des zones à risque
- Perspectives : agents autonomes, test self-healing

## 🚀 Installation et Utilisation

### Prérequis

- Un navigateur web moderne (Chrome, Firefox, Edge)
- VS Code avec l'extension GitHub Copilot (pour les exercices pratiques)
- Java 17+ et Maven (pour le projet NavDash)
- Node.js 16+ (pour les tests Cypress)

### Lancement de la Formation

1. **Cloner ou télécharger le projet**
   ```bash
   git clone <repository-url>
   cd qa-prompt-masterclass
   ```

2. **Ouvrir la formation**
   - Double-cliquez sur `index.html` dans le dossier racine
   - Ou utilisez un serveur local :
     ```bash
     # Avec Python
     python -m http.server 8000
     
     # Avec Node.js (npx)
     npx serve
     ```
   - Accédez à `http://localhost:8000`

3. **Navigation**
   - Suivez les sections dans l'ordre (1 → 2 → 3 → 4)
   - Chaque section contient des exercices pratiques et des pauses
   - Les prompts sont copiables d'un clic

### Projet NavDash (Section 3)

**Option 1 : Démarrage depuis zéro**
- Téléchargez `docs/assets/navdash.zip`
- Suivez les 7 prompts successifs pour construire l'application

**Option 2 : Point de départ pour les tests (Prompts 6 & 7)**
- Téléchargez `docs/assets/navdashdev.zip`
- Application complète sans les tests Cypress
- Idéal si vous voulez vous concentrer sur la partie tests E2E

## 🛠️ Technologies Utilisées

### Frontend Formation
- HTML5 sémantique
- CSS3 (variables CSS, grid, flexbox)
- JavaScript Vanilla (interactions, copie de prompts)

### Projet NavDash
- **Backend** : Java 17, Spring Boot 2.7.18, Maven
- **Frontend** : Thymeleaf, JavaScript ES6+, CSS3
- **Tests** : Cypress 13.x, TypeScript 5.x
- **APIs** : Battery Status API, Network Information API, Performance API

## 📊 Durée et Format

- **Durée totale** : ~3h00
  - Section 1 : 20 minutes
  - Section 2 : 50 minutes
  - Section 3 : 50 minutes
  - Section 4 : 40 minutes

- **Format** : Formation interactive avec :
  - Présentations théoriques
  - Démonstrations live
  - Pauses pratiques guidées
  - Exercices hands-on

## 🎓 Public Cible

- Testeurs QA et QA Automation Engineers
- Développeurs impliqués dans les tests
- Product Owners / Scrum Masters
- Architectes logiciels
- Toute personne intéressée par l'IA générative appliquée au testing

## 📝 Évaluation

À la fin de la formation, un formulaire d'évaluation est disponible via :
- Code QR (Section 4)
- Lien direct : https://forms.office.com/r/fChJrSZ9Mt

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :
- Signaler des bugs ou des erreurs
- Proposer des améliorations de contenu
- Partager vos retours d'expérience

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🙏 Remerciements

- GitHub Copilot pour les capacités d'IA générative
- La communauté QA pour les retours et suggestions
- Tous les participants qui contribuent à améliorer cette formation

## 📞 Contact

Pour toute question ou suggestion concernant cette formation, n'hésitez pas à me contacter par courriel : talel.zid@bdeb.qc.ca

---

**🚀 Bonne formation et bon apprentissage du prompt engineering pour le QA !**
