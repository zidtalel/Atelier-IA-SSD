Cours : Utiliser des outils d’IA dans un contexte de projet de données

---

Slide 1 : Titre et Mise en contexte
Titre : Thématique 4 : L'IA au service du spécialiste de données
Sous-titre : L'évolution vers le "Spécialiste de solutions de données 2.0"

Contenu :

* Bienvenue dans la nouvelle ère de la donnée : Pourquoi l'IA change tout.
* Objectif global : Intégrer les outils d'IA générative non pas comme des gadgets, mais comme des piliers de votre flux de travail.

Ce que nous allons couvrir ensemble :

1. Comprendre le paysage : De l'algorithme classique à l'IA qui écrit du code.
2. Booster sa productivité : Automatiser les tâches répétitives (nettoyage, conversion, documentation).
3. L'éthique et la sécurité : Savoir où s'arrêter pour protéger les données de l'entreprise.
4. Pratique réelle : Expérimenter avec des outils et des méthodes de "Prompt Engineering".

Le mot d'ordre : L'IA ne remplacera pas le spécialiste de données, mais le spécialiste qui utilise l'IA remplacera celui qui ne l'utilise pas.

---

Slide 2 : Le paysage de l'Intelligence Artificielle (Rappel et Focus) Titre : Petit lexique de l'IA pour nous situer Contenu :

Intelligence Artificielle (IA) : Discipline visant à simuler l'intelligence humaine pour accomplir des tâches complexes.

Apprentissage automatique (Machine Learning) : Apprendre à partir des données plutôt que de suivre des règles fixes.

Réseaux de neurones : Modèles mathématiques traitant l'information par couches, essentiels pour la reconnaissance de motifs.

Focus : Les LLM (Large Language Models)

Définition : Modèles de langage géants entraînés sur des quantités massives de texte.

Pourquoi pour nous ? Ils "comprennent" la logique des langages informatiques (SQL, Python, JSON).

Exemples : GPT-4 (OpenAI), Claude (Anthropic), Gemini (Google), Llama (Meta).

Le lien avec l'IA Générative : Les LLM sont le moteur qui permet de générer du contenu (code, texte, schémas) à partir d'une simple phrase.

---

Slide 3 : Le concept de "Spécialiste augmenté" Titre : De l'artisan à l'ingénieur augmenté Contenu :

Un changement de posture :

Hier : L'artisan qui forge chaque pièce à la main (Écriture manuelle de chaque ligne de code).

Aujourd'hui : L'ingénieur qui utilise des machines de précision pour assembler des systèmes complexes.

La nouvelle répartition du temps :

Avant : 80% du temps sur la syntaxe et le débogage / 20% sur la logique et l'architecture.

Augmenté : 20% sur la génération assistée / 80% sur la validation, la sécurité et l'optimisation.

Vos nouvelles "Super-compétences" :

Esprit critique : Savoir quand l'IA "hallucine" (invente des solutions fausses).

Capacité de synthèse : Savoir expliquer un problème complexe à une machine.

Intégration : Savoir assembler plusieurs morceaux de code générés en une solution cohérente.

La valeur ajoutée du spécialiste :

L'IA connaît la syntaxe, mais VOUS connaissez le contexte métier (les besoins de votre client).

Le spécialiste augmenté produit plus vite, avec moins d'erreurs répétitives, et se concentre sur les problèmes complexes.

---

Slide 4 : Le nouveau cycle de travail (Le Workflow IA) Titre : Comment travaille-t-on avec une IA ? Contenu :

Étape 1 : Conception & Intention (L'Humain)

Définir précisément le problème technique à résoudre.

Choisir la stratégie (ex: "Je veux transformer ce JSON en table SQL").

Étape 2 : Requête & Génération (L'IA)

Rédiger un prompt structuré.

L'IA génère une première version du code ou de la structure.

Étape 3 : Critique & Ajustement (L'Humain + IA)

Tester le code : Est-ce qu'il fonctionne ? Est-ce qu'il respecte les normes ?

Demander des corrections à l'IA si nécessaire ("Optimise la performance", "Ajoute des commentaires").

Étape 4 : Intégration & Sécurisation (L'Humain)

Insérer le morceau de solution dans le projet global.

Valider que les données sensibles ne sont pas exposées.

Règle d'or : "Trust, but Verify" (Faire confiance, mais vérifier). L'IA est votre stagiaire très rapide, pas votre patron.


---

Slide 5 : L'IA au service de vos missions (Cas concrets) Titre : Comment l'IA soutient vos responsabilités réelles Contenu :

Spécialiste de données (Votre rôle)

Cas 1 : "Génère un script Python pour convertir ce fichier XML complexe en une table SQL."

Cas 2 : "Rédige la documentation technique de cette base de données à partir de mon schéma."

Analyste de données / Analyste d'affaires (BA)

Cas 1 : "Propose 3 indicateurs clés (KPI) pour mesurer la performance des ventes d'une librairie."

Cas 2 : "Analyse ce tableau de résultats et résume les 3 tendances principales en quelques points."

Architecte de données

Cas 1 : "Dessine-moi une structure de données optimale pour gérer un inventaire multi-boutiques."

Cas 2 : "Compare les avantages de stocker ces données sur Azure vs AWS pour une petite PME."

Développeur (Application/BI)

Cas 1 : "Crée une requête SQL pour afficher les 10 meilleurs clients du mois dernier."

Cas 2 : "Trouve l'erreur dans ce code qui empêche l'affichage des dates au format québécois."

Testeur (QA)

Cas 1 : "Génère un jeu de 50 fausses données (noms, adresses, courriels) pour tester mon système."

Cas 2 : "Énumère les cas limites (edge cases) à tester pour un formulaire d'inscription d'étudiants."

---

Slide 6 : Activité interactive - Remue-méninges Titre : Discussion ouverte : Peurs vs Opportunités Contenu :

Selon vous, l'IA va-t-elle remplacer le spécialiste de données ?

Quels sont les types de tâches que vous aimeriez déléguer à une IA dès demain ?

Quels sont les risques si on fait une confiance aveugle à l'IA ?

Objectif : Comprendre que l'outil est puissant mais nécessite un pilote qualifié.

---

Slide 7 : Panorama des outils d’IA (La boîte à outils)
Titre : Les agents conversationnels et assistants de code
Contenu :

* Les généralistes (Agents conversationnels) :

* ChatGPT (OpenAI) : Le pionnier, très polyvalent pour le code et la logique.
* Gemini (Google) : Fort pour l'intégration avec l'écosystème Cloud et l'analyse de documents.
* Claude (Anthropic) : Réputé pour son écriture naturelle et sa précision dans le respect des consignes.

* Les spécialistes (Assistants de code) :

* GitHub Copilot : Directement intégré dans votre éditeur (VS Code). Il suggère du code en temps réel pendant que vous tapez.
* Cursor : Un éditeur de code entièrement bâti autour de l'IA.

* Pourquoi plusieurs outils ?

* Chaque modèle a sa "personnalité". Un spécialiste de données teste souvent un problème complexe sur deux modèles différents pour comparer les solutions.

---

Slide 8 : Cas d'usage 1 - La documentation technique
Titre : Fini la page blanche : Documenter sans effort
Contenu :

* Le problème : La documentation est cruciale mais souvent délaissée car chronophage.
* Ce que l'IA peut faire pour vous :

* Générer un "Dictionnaire de données" à partir d'un script SQL.
* Expliquer en langage clair une fonction complexe que vous venez d'écrire.
* Créer un fichier "README" professionnel pour expliquer comment utiliser votre solution.

* Exemple de demande (Prompt) :

* « Voici mon code SQL pour le calcul des taxes. Génère une documentation sous forme de tableau expliquant le rôle de chaque variable et les règles de calcul utilisées. »

---

Slide 9 : Cas d'usage 2 - Migration et Transformation
Titre : Le traducteur de formats universel
Contenu :

* Le défi : Recevoir des données dans un format illisible ou incompatible (ex: vieux fichiers texte, XML complexe).
* La solution IA :

* Convertir instantanément des structures (ex: CSV vers JSON, ou SQL vers NoSQL).
* Créer des scripts de "mapping" : Faire correspondre les colonnes du vieux système vers le nouveau.

* Exemple concret :

* Vous avez 50 colonnes de données client. L'IA peut générer le script qui renomme et réorganise ces colonnes pour qu'elles entrent parfaitement dans votre nouvelle base de données.
* "Transforme ce fichier CSV de ventes en un objet JSON structuré par catégorie de produit."

---

Slide 10 : Cas d'usage 3 - Nettoyage automatisé (Data Cleaning)
Titre : Chasser les anomalies avec l'IA
Contenu :

* Le travail ingrat du spécialiste : Nettoyer les erreurs de saisie humaine.
* L'apport de l'IA :

* Détection de motifs : Repérer les formats de courriels invalides ou les codes postaux erronés.
* Standardisation : Mettre tous les numéros de téléphone au même format (ex: +1 514...).
* Complétion : Suggérer la ville manquante à partir d'un code postal.

* Mise en garde :

* L'IA peut "inventer" des données pour combler les trous (hallucination).
* Toujours vérifier les données nettoyées avec un échantillon de contrôle.

---

Slide 11 : Démo Flash - L'IA en action
Titre : Démonstration : De la donnée brute à la solution
Contenu :

* [Espace pour une démo en direct ou capture d'écran]
* Scénario de la démo :

1. On prend un fichier texte mal structuré.
2. On demande à l'IA de le transformer en table propre.
3. On lui demande de générer le code Python pour automatiser ce nettoyage à l'avenir.

* Observation : Regardez la vitesse d'exécution par rapport à un codage manuel. Notez aussi que le code généré nécessite une petite correction pour être parfait.

---
