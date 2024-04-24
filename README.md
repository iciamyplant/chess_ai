# chess_ai

## Algos

|Algo|Definition|Commentaires|
|-----|-----|------|
|IA Minimax IA avec élagage alpha-bêta|algorithme de base pour la recherche en arborescence dans les jeux à deux joueurs. Il explore de manière récursive les différentes lignes de jeu en maximisant le score pour le joueur actuel tout en minimisant le score pour l'adversaire. L'élagage alpha-bêta permet de réduire le nombre de nœuds explorés, ce qui améliore considérablement l'efficacité de la recherche| ex: deepblue d'IBM qui bat Kasparov en 1997|
|IA NegaMax| variante simplifiée du Minimax, utilisée spécifiquement pour les jeux à deux joueurs à somme nulle comme les échecs. Il simplifie l'implémentation et l'analyse en supposant que l'adversaire maximise également son score||
|Reinforcement Learning|Cette approche consiste à entraîner l'IA à jouer aux échecs en lui permettant de jouer contre elle-même ou contre d'autres adversaires, en apprenant des récompenses et des sanctions en fonction des résultats des parties. Les méthodes populaires incluent le Q-learning, les réseaux de neurones profonds, et les méthodes basées sur les politiques||
|Méthodes Monte Carlo |Les méthodes Monte Carlo, telles que MCTS (Monte Carlo Tree Search), sont des techniques de recherche stochastique qui utilisent des échantillons aléatoires pour évaluer les différents coups possibles. Elles sont souvent utilisées pour les jeux avec un grand facteur d'arborescence comme les échecs||

- comprendre minimax et megamax
- étapes pour coder un tel algorithme


1. Implémenter le plateau
--> pygame pour l'interface graphique
3. Implémenter le déplacement des pièces
4. Création de l'IA
--> algorithme min max, indique le meilleur coup à faire selon une fonction qui évolue le plateau
5. Ajouter algorithme alpha beta pour aller plus vite qui consiste à ne pas explorer les branches inutiles
6. Tester contre des joueurs


Reinforcement Learning Chess

https://www.kaggle.com/code/arjanso/reinforcement-learning-chess-1-policy-iteration

- Notebook 1 : ==> Move Chess
- Notebook 2 : ==> Move Chess
- Notebook 3 : Q-networks ==> Capture chess
- Notebook 4 : Policy-gradients ==> Capture chess
- Notebook 5 : V-network et Monte Carlo Tree Search ==> Real Chess


https://www.youtube.com/watch?v=w4FFX_otR-4

1. Board Representation
--> trouver comment on va représenter la position des pions : on pourrait stocker dans une array, mais il y a mieux : bitboard method, 1 s'il y a un pion
--> tout le plateau peut etre representé par 12 bitboards, pour chaque type de pion : pion blanc, pion noir, reine blanche, reine noire, roi blanc, roi noir, cavalier blanc, cavalier noir ...
--> et enfin quelques bitboards pour les règles
2. Fonction d'évaluation
--> Avant de trouver le meilleur mouv, on doit trouver quel emplacement est mieux qu'un autre avec une fonction d'évaluation
--> telle pièce a tel endroit vaut mieux que tel pièce a cet endroit == traduit par un chiffre
4. Search with minimax algorithm
--> on commence par extraire tous les mouvements qu'on a le droit de faire
--> pour chaque mouvement on applique l'evaluation function pour avoir leur score
--> on choisit le best mouv
5. Algorithm Alpha Beta
--> réduire le nombre de nœuds explorés, améliore l'efficacité de la recherche

I- implémenter la représentation du plateau
- représenter la position des pions
- les règles : genre comment les pions peuvent se déplacer etc.
II - Coder l'IA

III - Tester notre IA contre des vrais joueurs
- d'abord sur chess.com
- ensuite avec des vrais joueurs en physique


References
- https://github.com/zjeffer/chess-deep-rl
- https://github.com/arjangroen/RLC/tree/master
- https://github.com/bellerb/chappie.ai ==> https://towardsdatascience.com/playing-chess-with-a-generalized-ai-b83d64ac71fe
- ML simple : https://medium.com/@waleedmousa975/a-step-by-step-guide-to-developing-a-chess-game-with-an-ai-opponent-using-python-e06374fcc04a
- CNN mais sans reinforcement : https://www.youtube.com/watch?v=aOwvRvTPQrs
- https://www.kaggle.com/competitions/train-an-ai-to-play-chess et dans cette vidéo : https://www.youtube.com/watch?v=l0bv8IgELfU
- https://www.freecodecamp.org/news/simple-chess-ai-step-by-step-1d55a9266977/, https://github.com/lhartikk/simple-chess-ai, https://jsfiddle.net/q76uzxwe/1/
- https://github.com/geochri/AlphaZero_Chess
- https://github.com/genyrosk/gym-chess ==> sur gym
- https://github.com/Zeta36/chess-alpha-zero
   
