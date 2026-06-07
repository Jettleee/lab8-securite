
📦 LabSec08-Workspace
 ┣ 📂 00-scope       # Périmètre de l'analyse, APK source et validation de l'intégrité
 ┣ 📂 01-bevigil     # Collecte d'informations exposées et OSINT applicatif
 ┣ 📂 02-yaazhini    # Résultats de l'analyse statique automatisée
 ┣ 📂 03-triage      # Consolidation, déduplication et contextualisation des risques
 ┗ 📂 04-report      # Livrables finaux et rapports de synthèse

```

> 📝 **Indicateurs de traçabilité :** Les fichiers `analyse_info.txt` et `commands.log` consignent de manière immuable les configurations de l'environnement, l'identité des artefacts manipulés ainsi que l'historique complet des commandes exécutées.

---

## ⚙️ Méthodologie d'Analyse Étape par Étape

### 1. Cadrage & Intégrité (`00-scope`)

Le processus débute par l'isolation de l'APK dans le répertoire de scope. Un calcul d'empreinte cryptographique **SHA-256** est systématiquement effectué. Cette étape critique assure l'intégrité de la cible tout au long du cycle de vie de l'analyse et certifie que les résultats produits correspondent de manière univoque à l'artefact audité.

### 2. Renseignement & OSINT Externe (`01-bevigil`)

Utilisation de la plateforme **BeVigil** pour extraire une première cartographie des métadonnées, des permissions demandées et des potentielles chaînes de caractères sensibles (clés d'API, endpoints, configurations) exposées publiquement ou structurellement au sein de l'application.

### 3. Analyse Statique Automatisée (`02-yaazhini`)

Déploiement de l'outil **Yaazhini** afin d'auditer en profondeur le code décompilé, le fichier `AndroidManifest.xml` et les ressources embarquées. Cette phase met en évidence les faiblesses de configuration, les API non sécurisées et les mauvaises pratiques de développement.

### 4. Triage Évolué & Cartographie OWASP MASVS (`03-triage`)

Phase de post-traitement consistant à consolider les alertes issues de BeVigil et Yaazhini. Ce processus permet de :

* Éliminer les faux positifs et les doublons d'outils.
* Qualifier l'impact réel de chaque constat.
* Corréler les vulnérabilités retenues avec le référentiel de sécurité mobile **OWASP MASVS** (Mobile Application Security Verification Standard).

---

## 📸 Registre des Preuves & Journal de Bord

### Phase 01 : Initialisation & Structure du Périmètre

#### 🔹 Définition du Scope Applicatif

L'artefact d'origine est isolé de manière étanche pour prévenir toute contamination ou modification accidentelle.


#### 🔹 Organisation du Plan de Travail

Une arborescence compartimentée est mise en place pour structurer rigoureusement chaque phase du projet.


#### 🔹 Fichiers de Reproductibilité

Préparation des descripteurs de contexte pour garantir un suivi d'audit transparent et auditable.


#### 🔹 Métadonnées de l'Environnement

Consignation formelle de la date, de la version du système, de l'identité de la cible et du profil de l'analyste.


#### 🔹 Empreinte Cryptographique (SHA-256)

Validation de la signature de l'APK via un calcul de hash cryptographique univoque.


---

### Phase 02 : Évaluation & Triage des Vulnérabilités

#### 🔹 Signaux de Sécurité Externe (BeVigil)

Vue synthétique des premiers indicateurs de risques et des surfaces d'exposition détectées en ligne.


#### 🔹 Cartographie Matricielle des Risques (Yaazhini)

Extraction des anomalies de sécurité sous forme de matrice tabulaire facilitant la lecture des failles de code.


#### 🔹 Synthèse Exécutive des Détections

Compilation globale des sévérités identifiées par l'outil, servant de base de travail pour la phase de triage final.


---

## 🏆 Livrables & Résultats Obtenus

À l'issue de ce laboratoire, les objectifs suivants ont été pleinement atteints :

1. **Workspace standardisé** et structuré selon les meilleures pratiques de l'ingénierie de sécurité.
2. **Identification formelle** de la cible par hachage cryptographique non répudiable.
3. **Collecte brute** des télémétries de vulnérabilité via des technologies complémentaires (BeVigil & Yaazhini).
4. **Matrice de triage opérationnelle** prête pour la remédiation, établissant un pont direct avec les exigences de conformité **OWASP MASVS**.
"""



* **Structuration Technique** : Le contenu est maintenant divisé de manière logique (Fiche technique, Objectifs, Architecture, Méthodologie, Journal de bord) pour faciliter la lecture.
* **Vocabulaire d'Ingénierie** : Le ton a été revu pour adopter un vocabulaire propre à la cyber-défense (ex: "Empreinte cryptographique", "Triage évolué", "Cartographie OWASP MASVS", "Intégrité").
* **Préservation des Preuves** : Les liens vers vos captures d'écran ont été conservés exactement comme dans votre texte d'origine afin que les images s'affichent correctement dans votre répertoire.

```
