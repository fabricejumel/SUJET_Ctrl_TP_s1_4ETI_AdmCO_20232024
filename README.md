# SUJET_Ctrl_TP_s1_4ETI_AdmCO_20232024

Votre rendu sera un unique dépôt Git. Vous devrez définir et justifier l'organisation des branches, l'utilisation ou non de branches `dev`, de branches liées aux fonctionnalités, de branches distinctes pour les versions, ou l'utilisation de tags.


Testez le code `game_target_v3.py`. 

Pour chaque Version, vous devrez :

1. **Coder la ou les classes et le package associé et le déposer sur test Pypi**
1. **Mettre en place une logique de test, le plus complet possible en utilisant unitest** : en particulier, comment gérez-vous les éventuelles erreurs ?
1. **Afficher les choix sur le code final de la classe si vous avez du faire des changements** : après diverses corrections liées aux retours de Pylint. Affichez votre score et le retour de Pylint.
2. **Associer au projet gitlab le README le plus complet possible**
1. **Faire un gros effort sur les commentaires** : utilisez intensivement les docstrings.
1. **Tester l'installation du paquet à partir de gitlab avec une procedure dans le README** (1).
1. **Automatiser les phases de test et de création du .whl sur GitLab avec un fichier ci** (2).
1. Faire apparaitre votre arbe de commit dans le README, en expliquant les choix faitrs surt les branches et les tags


### Version 0

Le but est de mettre en forme le code donné pour en créer un package q

- Créez un package `Game`.donné 
- Proposez un module `RPS_Game`.
- Créez un sous-module `RPS_Tools` contenant une classe :
  - Créez une classe `RPS_SimpleGame`.

#### RPS_SimpleGame

Cette classe propose deux méthodes :

1. `SimplegameTwoplayers(player1choice, player2choice)` : retourne 0 en cas d'égalité, 1 si le joueur 1 gagne et 2 si le joueur 2 gagne.
2. `SimplegameOneplayer(player1choice)` : retourne 0 en cas d'égalité (même choix aléatoire fait par l'ordinateur), 1 si le joueur gagne ou 2 si l'ordinateur gagne.
   - `player1choice` et `player2choice` sont des caractères 'R', 'P' ou 'S'.

### Fonctionnalité 2

Créez une seconde classe `RPS_MultipleGame`. Dans cette classe, un joueur humain joue contre l'ordinateur en gardant une trace des parties précédentes. Cette classe utilisera la classe `RPS_SimpleGame`, plus précisément la méthode `SimplegameTwoplayers`. On souhaite stocker (à vous de définir comment) à la fois les anciennes parties pour analyse et avoir un historique récent pour la prise de décision. Il peut être pertinent d'associer les parties à des joueurs "identifiés".

### Fonctionnalité 3

L'ordinateur pourra alors utiliser l'historique des parties précédentes pour proposer une stratégie non aléatoire. Faites une proposition de structuration de code. Vous pourrez proposer une ou plusieurs stratégies qui utilisent cet historique.

---
**Note**:

- Assurez-vous de créer des fichiers README.md pour chaque branche ou fonctionnalité, expliquant clairement les changements et la logique derrière eux.
- Utilisez des outils d'intégration continue pour automatiser les tests et la génération de fichiers `.whl`.
