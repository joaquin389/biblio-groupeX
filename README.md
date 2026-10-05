# \# Biblio

# 

# Biblio est une petite application en ligne de commande qui aide les bénévoles d'une bibliothèque associative à gérer les livres, les emprunts et les retards.

# 

# \## Prérequis

# 

# \- Python 3.12 ou une version plus récente.

# \- SQLite, fourni avec Python : aucune dépendance Python supplémentaire n'est à installer.

# \- GitHub Desktop pour cloner le dépôt, ou Git.

# 

# Si Python n'est pas installé, installez Python 3.12 ou une version plus récente depuis \[python.org](https://www.python.org/downloads/). Sous Windows, choisissez également l'option qui ajoute Python au `PATH` si l'installateur la propose.

# 

# \## Installation

# 

# 1\. Clonez le dépôt `https://github.com/joaquin389/biblio-groupeX` avec GitHub Desktop (`File > Clone repository > URL`) et ouvrez le dossier cloné.

# 2\. Ouvrez une invite de commandes dans ce dossier (`Repository > Open in Command Prompt` dans GitHub Desktop).

# 3\. Créez la base de démonstration :

# 

# ```console

# python biblio.py init

# ```

# 

# Résultat :

# 

# ```text

# Base initialisee : 6 livres, 3 membres.

# ```

# 

# Cette commande recrée la base de démonstration et efface les données Biblio déjà enregistrées dans cette base.

# 

# Si `python` n'est pas reconnu, utilisez `py` sous Windows. Sous macOS ou Linux, utilisez `python3`. Par exemple, l'initialisation s'écrit alors `py biblio.py init` ou `python3 biblio.py init`.

# 

# Commande équivalente sous Windows :

# 

# ```console

# py biblio.py init

# ```

# 

# Résultat :

# 

# ```text

# Base initialisee : 6 livres, 3 membres.

# ```

# 

# Commande équivalente sous macOS ou Linux :

# 

# ```console

# python3 biblio.py init

# ```

# 

# Résultat :

# 

# ```text

# Base initialisee : 6 livres, 3 membres.

# ```

# 

# \## Utilisation

# 

# Les exemples ci-dessous supposent que l'étape `init` de l'installation a déjà été effectuée. Remplacez `python` par `py` sous Windows ou `python3` sous macOS/Linux si nécessaire.

# 

# Lister les livres :

# 

# ```console

# python biblio.py livres

# ```

# 

# Résultat :

# 

# ```text

# \[1] L'Etranger (Albert Camus) : disponible

# \[2] Dune (Frank Herbert) : emprunte

# \[3] Le Petit Prince (Antoine de Saint-Exupery) : disponible

# \[4] Fondation (Isaac Asimov) : disponible

# \[5] Les Miserables (Victor Hugo) : disponible

# \[6] Neuromancien (William Gibson) : disponible

# ```

# 

# Rechercher un livre par titre :

# 

# ```console

# python biblio.py chercher Dune

# ```

# 

# Résultat :

# 

# ```text

# \[2] Dune (Frank Herbert)

# ```

# 

# Enregistrer l'emprunt du livre 3 par le membre 1 (Alice Martin) :

# 

# ```console

# python biblio.py emprunter 3 1

# ```

# 

# Résultat :

# 

# ```text

# Emprunt enregistre : livre 3, membre 1.

# ```

# 

# Enregistrer le retour du livre 3 :

# 

# ```console

# python biblio.py rendre 3

# ```

# 

# Résultat :

# 

# ```text

# Retour enregistre pour le livre 3.

# ```

# 

# Afficher les retards :

# 

# ```console

# python biblio.py retards

# ```

# 

# Exemple de résultat le 5 octobre 2026 (le nombre de jours évolue avec la date) :

# 

# ```text

# Dune, emprunte par Alice Martin : 254 jours de retard

# Fondation, emprunte par Bilal Haddad : 259 jours de retard

# ```

# 

# Dans la base de démonstration actuelle, la commande affiche aussi Fondation alors que son emprunt est marqué comme rendu. Ce résultat reflète le comportement actuel du programme.

# 

# \## Tests

# 

# Depuis le dossier du projet, lancez :

# 

# ```console

# python -m unittest discover -s tests -t . -v

# ```

# 

# Résultat attendu : les quatre tests passent et la dernière ligne indique `OK`.

# 

# ```text

# Ran 4 tests in <durée>

# 

# OK

# ```

# 

# \## Structure du projet

# 

# ```text

# .

# ├── biblio.py                  # Application en ligne de commande et accès SQLite

# ├── tests/

# │   └── test\_biblio.py         # Tests unitaires

# ├── docs/

# │   ├── adr/                   # Décisions d'architecture (ADR)

# │   └── circulation.md         # Règles de circulation de l'information

# ├── exercices/                 # Exercices de documentation

# └── .github/

# &#x20;   ├── ISSUE\_TEMPLATE/        # Modèles d'issues

# &#x20;   └── workflows/tests.yml    # Tests automatiques sur les pull requests

# ```

# 

# \## Contribuer

# 

# 1\. Ouvrez une issue pour décrire le bug ou l'évolution, en utilisant le modèle adapté.

# 2\. Créez une branche liée au sujet, par exemple `docs/<numero>-<mots-cles>` pour la documentation ou `feature/<numero>-<mots-cles>` pour une fonctionnalité.

# 3\. Faites des commits ciblés et ouvrez une pull request qui décrit les changements et indique `Closes #<numero>` si elle résout une issue.

# 4\. Demandez une review à un autre membre et corrigez les remarques.

# 5\. Après approbation, mergez la pull request. Aucun changement ne doit être poussé directement sur `main`.

# 

# \## Auteurs

# 

# \- @joaqu



