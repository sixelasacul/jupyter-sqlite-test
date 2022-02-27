# Jupyter/SQLite test

D'abord, on installe `pipenv` à partir de `pip` pour Python :

```sh
pip install --user pipenv
```

`pipenv` permet de gérer des dépendences localement, afin de contenir seulement
ce qu'il faut pour qu'un project fonctionne, de manière reproducible.
Ensuite, on intalle les dépendences du projet :

```sh
pipenv install
```

## Scripts

Avec `pipenv`, on peut créer des scripts pour facilement exécuter des commandes.
Actuellement, le project a 2 commandes :

- `notebook` pour exécuter Jupyter afin de manipuler les documents;
- `voila` pour faire un rendu du document principal sous forme de page HTML;
- `reset-db` pour supprimer le fichier de la base de données.

Pour les exécuter, il faut écrire :

```sh
pipenv run <command>
```

## Shell

On peut aussi utiliser `pipenv` pour obtenir un environnement dans le terminal
ayant accès uniquement aux dépendences installées pour le projet, afin de tester
d'autres commandes pas forcément gérées par un script :

```sh
pipenv shell
```

## Fichiers

Les fichiers `.ipynb` sont les documents utilisés par Jupyter Lab/Notebook et
Voila. Le fichier `.db` correspond à la base de données SQLite. Les fichiers
`Pipfile` sont utilisés par `pipenv` et permettent de gérer les dépendences et
les scripts.