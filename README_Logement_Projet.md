
# Projet Logement Éco-Responsable

## Description
Ce projet vise à créer une plateforme de gestion intelligente d'un logement permettant de surveiller les factures, les capteurs et d'autres données associées. L'objectif est de suivre la consommation d'énergie et de simplifier la gestion de la maison via une interface web.

## Contenu de l'archive

### 1. Base de données
- **logement.db** : Base de données SQLite contenant les tables nécessaires pour stocker les informations des pièces, capteurs, mesures, factures et logements.
- **logement.sql** : Script SQL pour initialiser et configurer la structure de la base de données.

### 2. Scripts Python
- **get_post.py** : Serveur web Flask permettant d'interagir avec la base de données via des routes REST pour gérer les factures, afficher les données des capteurs, et générer des graphiques.
- **remplissage.py** : Script pour remplir automatiquement la base de données avec des données aléatoires de factures et de mesures pour les capteurs.

### 3. Script Bash
- **add_factures.sh** : Script bash utilisant `curl` pour ajouter automatiquement des factures mensuelles de différents types (Électricité, Déchets, Eau, Gaz) via des requêtes HTTP POST.

### 4. Fichier Divers
- **curl** : Fichier non détaillé, potentiellement utilisé pour des commandes liées à des requêtes HTTP.

## Instructions d'utilisation

### 1. Initialisation de la base de données
Si nécessaire, exécutez le script SQL pour créer les tables :
```bash
sqlite3 logement.db < logement.sql
```

### 2. Remplir la base de données
Lancer le script Python pour insérer des données aléatoires :
```bash
python3 remplissage.py
```

### 3. Lancer le serveur Flask
Démarrer le serveur web pour interagir avec l'application :
```bash
python3 get_post.py
```
Le serveur sera accessible via `http://127.0.0.1:5000`

### 4. Ajouter des factures automatiquement
Utiliser le script bash pour insérer des factures :
```bash
bash add_factures.sh
```

## Fonctionnalités
- Visualisation des pièces du logement.
- Suivi des factures (électricité, eau, gaz, déchets) avec graphiques interactifs.
- Gestion des capteurs et des mesures.
- Récupération des prévisions météo en temps réel.

## Prérequis
- Python 3.x
- Flask (`pip install flask`)
- SQLite3
- cURL

## Auteur
Yedam KIM - Étudiant en cycle d'ingénieur à Polytech Sorbonne

---

*Projet réalisé dans le cadre du projet "Logement Éco-Responsable".*
