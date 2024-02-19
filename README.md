# SUJET_Ctrl_TP_s1_4ETI_AdmCO_20232024

Votre rendu sera un unique dépôt Git. Vous devrez définir et justifier l'organisation des branches, l'utilisation ou non de branches `dev`, de branches liées aux fonctionnalités, de branches distinctes pour les versions, ou l'utilisation de tags.


Testez le code [game_target_v3.py](./game_target_v3.py)

Dans le cas ou le sujet ne vous paraitrez peu clair ou erronné, proposez des changements en les justifiant pour pouvoir répondre aux questions .
Même si rien ne marche, remplissez au mieux les attendus en étant clair sur ce qui marche et ce qui ne marche pas (cf la suite)

Pour chaque Version, vous devrez :

1. ***Expliquer ce qui marche et ce qui ne marche pas***
1. ***Joindre des copies d'écran, du résultats des scripts exécutés***
1. **Expliquer l'usage de venv, dans votre cas (NE PAS JOINDRE DE REPERTOIRE Venv dans votre git ou de fichiers temporaires)**
1. **Coder la ou les classes et le package associé et les déposer sur test Pypi**
1. **Mettre en place une logique de test, le plus complet possible en utilisant unitest** : en particulier, comment gérez-vous les éventuelles erreurs ?
1. **Afficher les choix sur le code final de la classe si vous avez dû faire des changements** :  Affichez votre score et le retour de Pylint.
1. **Associer au projet gitlab le README le plus complet possible**
1. **Faire un gros effort sur les commentaires** : utilisez intensivement les docstrings.
1. **Proposer l'installation du paquet à partir de gitlab avec une procedure dans le README**
1.  **Proposer l'installation du paquet à partir de test pypi avec une procédure dans le README**
1. **Automatiser les phases de test et de création du .whl sur GitLab avec un fichier ci** 
1. Faire apparaitre votre arbre de commit dans le README, en expliquant les choix faits sur les branches et les tags


### Version 1 (8 points + bonus)

Le but est de cette version est de mettre en forme le code donné pour en créer un package (logique setup.py ou éventuellemnt pyproject.toml) en modifiant a minima le code donné (même si il vous semble incorrect ou peu pertinent). On mettra aussi en place toute la logique de test unitaires  (on relira l'attendu précédent Pour chaque Version, vous devrez : ...)

### Version 2 ( 6 points + des bonus)

Le code proposé présente beaucoup d'améliorations possibles . En particulier, le fait de modifier directement la grille (grid) sans passer par une méthode qui apporterait des sécurités est problématique . 
Ensuite le fait que le  code suivant ne genere pas d'erreur est aussi problematique 
```python
if __name__ == "__main__":

    # Création de la grille et du robot
    grid = Grid(5, 5)
    robot = Robot(10, 10)

    # Création du jeu avec l'option d'affichage de la grille et une limite d'étapes
    game = Game(grid, robot, max_steps=1000, show_grid=False)

    # Exécution des tours de jeu jusqu'à ce que le robot touche la cible ou que la limite d'étapes soit dépassée
    while not game.run_turn():
        pass

    # Vérification si le robot a atteint la cible ou non et affichage du message approprié
    if game.target_reached:
        print("Félicitations ! Le robot a atteint la cible en {} étapes.".format(game.steps))
    else:
        print("Le robot n'a pas réussi à atteindre la cible dans le nombre maximum d'étapes.")
```
Proposer des correctifs à  ces problèmes et d'autres problème que vous auriez constaté . Il est imporrtant que tous les changements se reperercutent sur les tests unitaires . N'hésitez pas à améliorer au passage vos tests unitaires si il n'était pas suffisemment complet sur la version 1.
 (on relira l'attendu précédent Pour chaque Version, vous devrez : ...)

### Version 3 ( 6 points + bonus)

On souhaite définir différentes stratégies de déplacement du robot. Proposez en plus de la stratégie de base  aléatoire , 2 autres stratégies (qui peuvent aussi ou pas comporter une part  d'aléatoire). A vous de proposez une facon pertinente de changer quelle stratégie est utilisé, cela doit pouvoir être défini dans le "main" sans avoir à changer à la main le code des différentes classes.
 (on relira l'attendu précédent Pour chaque Version, vous devrez : ...)



