# Pipeline CI avec GitHub Actions
## Ce dépôt contient une pipeline CI pour un projet Python avec les étapes suivantes:

- Cloner le dépôt
- Linting du code avec Pylint
- Analyse de complexité cyclomatique avec Radon
- Tests unitaires
- Build Docker et push vers Docker Hub

Chaque étape est définie dans un job séparé.

JOBS

## clone-repo
Clone le dépôt dans le workspace.

## lint

Installe les dépendances dans un environnement virtuel.
Exécute Pylint et enregistre le rapport.

## cyclomatic

Analyse la complexité cyclomatique avec Radon.

## build

Build l'image Docker et la push vers Docker Hub. Nécessite les credentials Docker Hub dans les secrets.



## Utilisation
Pour utiliser cette pipeline:

- Dupliquer ce dépôt
- Changer le dépôt à cloner dans clone-repo
- Pusher du code dans le dépôt cloné
- La pipeline sera lancée automatiquement
Les rapports linting, complexité et tests seront disponibles comme artifacts.
