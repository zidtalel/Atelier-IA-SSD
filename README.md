# 🎓 Data Solutions & IA - Formation GitHub Copilot pour Data Solutions

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Formation](https://img.shields.io/badge/Type-Formation-blue.svg)](.)
[![GitHub Copilot](https://img.shields.io/badge/GitHub-Copilot-purple.svg)](https://github.com/features/copilot)

## 📋 Description

Formation complète et interactive sur l'utilisation de l'IA générative et du prompt engineering avancé pour les professionnels des Data Solutions. Cette masterclass explore comment GitHub Copilot et les Large Language Models (LLMs) peuvent transformer les pratiques de pipelines ETL, de validation de données, de génération de scripts SQL et d'automation des transformations de données.

## 🎯 Objectifs de la Formation

À l'issue de cette formation, vous serez capable de :

- ✅ **Comprendre le potentiel de l'IA en Data** - Identifier les tâches optimisables et les limites critiques
- ✅ **Maîtriser le prompt engineering** - Utiliser les 5 composantes essentielles (Rôle, Tâche, Contexte, Contraintes, Format)
- ✅ **Générer des scripts SQL** - Créer des pipelines ETL guidés par des spécifications
- ✅ **Valider et transformer les données** - Appliquer JSON Schema et règles de validation avancées
- ✅ **Appliquer des techniques avancées** - Utiliser Few-Shot Learning, Chain-of-Thought et agents autonomes

## 📚 Structure du Projet

```
Atelier-IA-SSD/
├── docs/
│   ├── assets/
│   │   ├── style.css              # Styles CSS communs
│   │   └── images/                # Images et captures d'écran
│   ├── section-1/
│   │   └── index.html            # Le Paysage de l'IA Générative pour Data Solutions
│   ├── section-2/
│   │   └── index.html            # L'Art du Prompting
│   ├── section-3/
│   │   └── index.html            # Cas d'Usage Avancés (Sous Construction)
│   └── section-4/
│       └── index.html            # Mise en Production et Automation (Sous Construction)
├── index.html                     # Page d'accueil de la formation
├── Cours IA.md                    # Contenu du cours
├── LICENSE                        # Licence du projet
└── README.md                      # Ce fichier
```

## 📖 Contenu des Sections

### 🌐 Section 1 : Le Paysage de l'IA Générative pour Data Solutions (30 min)

**Objectifs :**
- Définir l'IA comme accélérateur de pipelines de données
- Identifier les tâches Data Solutions optimisables (scripts SQL, transformations, validations)
- Reconnaître le potentiel ET les limites de l'IA
- Démonstration pratique : Génération de scripts SQL ETL pour données clients

**Concepts clés :**
- LLMs et reconnaissance de patterns dans les données
- Paradigme du prompting : passer du "Comment" au "Quoi"
- Règles "Garbage In, Garbage Out"
- Hallucinations de colonnes/tables PostgreSQL et validation humaine

### 🎨 Section 2 : L'Art du Prompting (40 min)

**Objectifs :**
- Maîtriser les 5 composantes d'un prompt efficace
- Appliquer les techniques avancées (Few-Shot Learning avec JSON Schema, Chain-of-Thought)
- Pratiquer sur des cas réels de Data Solutions
- Éviter les anti-patterns courants

**Techniques enseignées :**
- 🔵 **Rôle** : Expert en data engineering et SQL
- 🟢 **Tâche** : Valider, transformer, générer des scripts ETL
- 🟡 **Contexte** : Schémas PostgreSQL, règles métier
- 🔴 **Contraintes** : Performance, qualité des données, compliance
- 🟣 **Format** : JSON Schema, SQL scripts, validation reports

**Module 2.2 : Few-Shot Learning** - JSON Schema Validation
- Démonstration de validation de CSV avant transformation
- Règles métier appliquées via JSON Schema
- Analyse ligne-par-ligne des violations

### ⏳ Section 3 : Cas d'Usage Avancés (Sous Construction)

**À venir :**
- Optimisation avancée des pipelines ETL
- Déduplication et nettoyage de données
- Gestion des cas limites et exceptions
- Études de cas réels en production

### ⏳ Section 4 : Mise en Production et Automation (Sous Construction)

**À venir :**
- CI/CD pour pipelines ETL
- Versioning et suivi des modifications
- Monitoring et alertes
- Sécurité des données et compliance
- Collaboration en équipe

## 🚀 Installation et Utilisation

### Prérequis

- Un navigateur web moderne (Chrome, Firefox, Edge)
- VS Code avec l'extension GitHub Copilot (pour les exercices pratiques)
- PostgreSQL 15+ (pour les exemples et exercices)
- Python 3.11+ (pour les scripts de transformation)

### Lancement de la Formation

1. **Cloner ou télécharger le projet**
   ```bash
   git clone https://github.com/zidtalel/Atelier-IA-SSD.git
   cd Atelier-IA-SSD
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
   - Sections 1 & 2 sont complètes (~70 minutes)
   - Sections 3 & 4 sont en développement
   - Les prompts sont copiables d'un clic

## 🛠️ Technologies Utilisées

### Frontend Formation
- HTML5 sémantique
- CSS3 (variables CSS, grid, flexbox)
- JavaScript Vanilla (interactions, copie de prompts)

### Data Solutions
- **Base de données** : PostgreSQL 15+
- **Scripts** : SQL, Python 3.11+
- **Validation** : JSON Schema
- **Outils** : VS Code, GitHub Copilot

## 📊 Durée et Format

- **Durée totale actuelle** : ~70 minutes
  - Section 1 : 30 minutes
  - Section 2 : 40 minutes (NOYAU de la formation)
  - Section 3 : À venir
  - Section 4 : À venir

- **Format** : Formation interactive avec :
  - Présentations théoriques
  - Démonstrations pratiques
  - Exercices hands-on
  - Prompts copiables et réutilisables

## 🎓 Public Cible

- Data Engineers et Data Analysts
- Data Scientists
- Développeurs impliqués dans ETL et data pipelines
- Data Architects
- Product Owners / Scrum Masters
- Toute personne intéressée par l'IA générative appliquée aux Data Solutions

## 📝 Évaluation

À la fin de la formation, vos retours sont précieux pour améliorer ce cours.

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :
- Signaler des bugs ou des erreurs
- Proposer des améliorations de contenu
- Partager vos retours d'expérience

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🙏 Remerciements

- GitHub Copilot pour les capacités d'IA générative
- La communauté Data et Engineering pour les retours
- Tous les participants qui contribuent à améliorer cette formation

## 📞 Contact

Pour toute question ou suggestion concernant cette formation, n'hésitez pas à me contacter : talel.zid@bdeb.qc.ca

---

**🚀 Bonne formation et bon apprentissage du prompt engineering pour les Data Solutions !**
