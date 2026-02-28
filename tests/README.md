# Module Tests

## Raison d'être du module
Ce répertoire centralise l'ensemble de la suite de tests automatisés du projet. Ces tests servent à vérifier à travers un environnement isolé que la logique métier (opérations mathématiques) et les routes de l'API web (Flask) se comportent selon les attentes. Ils garantissent la stabilité du code et permettent d'empêcher les éventuelles régressions (bris de code par inadvertance suite à de nouvelles fonctionnalités).

## Principaux fichiers et responsabilités
*Note : Si les fichiers n'existent pas encore, ils seront les standards du projet.*
*   `test_operators.py` : Scripts de test visant à affirmer la robustesse unitaire de chaque constructeur algébrique (`add`, `subtract`, `multiply`, `divide`). Relève les cas de limites (division par zéro, formats valides, etc.).
*   `test_app.py` : Scripts de validation visant le comportement d'analyse arithmétique globale et l'accessibilité HTTP (réponse 200 de la route `'/'`, injection correcte en methode POST, etc).

## Dépendances ou hypothèses
*   Le framework de test est **Pytest**.
*   Les tests doivent être exécutables à la racine du projet via la commande `pytest` ou `pytest -q`.
*   Hypothèse que chaque fichier source du projet possède un fichier miroir équivalent pour le test unitaire dans ce répertoire.
