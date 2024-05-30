# Decouvrir Python : une exploration pour développeurs.euses expérimentés.ées

Ce site à pour objet de faire découvrir le langage de programmation Python d'un point de vue de développeurs.euses expérimentés.ées.
Il est réalisé avec [MkDocs](https://www.mkdocs.org/) et plus précisément [sa déclinaison utilisant Material](https://squidfunk.github.io/mkdocs-material/).

## Utilisation avec Docker

[MkDocs](https://www.mkdocs.org/) est une application Python, mais il est possible d'utiliser [MkDocs](https://www.mkdocs.org/) via [Docker](https://www.docker.com/) sans avoir à installer Python.

* Initialisation, dans le répertoire dans lequel il faut créer le site : `docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material new .`
* Prévisualisation sur `localhost:8000` : `docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material`
* Construction du site : `docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build`
  * Le site (HTML) est généré dans le répertoire `site/decouvrir-python`

Pour lancer les lignes de commandes ci-dessus, utiliser une invite de commande Powershell (sous Windows) ou un shell Unix.

## Utilisation avec Python

Si vous avez Python installé sur votre machine et/ou si vous préférez utiliser l'application sans passer par Docker, voici la démarche recommandée.

* Créer un environnement virtuel avec `venv` avant d'installer **MkDocs** :
  * A la racine du répertoire dans une invite de commandes : `python -m venv venv --prompt="mkdocs"`
  * Un répertoire `venv` doit être créé : ajouter ce répertoire dans le `.gitignore`
* Activer l'environnement virtuel : `venv\Scripts\activate`
* Installer **MkDocs (with Material)** avec `pip`
  * `pip install mkdocs-material`
* A la fin de votre session de travail, désactiver l'environnement virtuel : `venv\Scripts\deactivate`

Une fois l'installation réalisée les commandes sont les suivantes :

* Initialisation : `mkdocs new`
* Prévisualisation : `mkdocs serve` ou `mkdocs serve --dirtyreload` si vous voulez juste mettre à jour la page courante (_build_ incomplet mais plus rapide).
* Construction du site : `mkdocs build`
  * Le site (HTML) est généré dans le répertoire `site/etude_fido2` et est complètement _autonome_ normalement.

Penser à activer l'environnement virtuel avant de lancer les commandes : `venv\Scripts\activate`
A la fin de votre session de travail, penser à désactiver l'environnement virtuel : `venv\Scripts\deactivate` (ce n'est pas dramatique si ce n'est pas fait, si vous fermait l'invite de commande).
