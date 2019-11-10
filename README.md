# Board Game Framework
 
*     Framework BoardGames v0.5.0
*     to create new board games such Chess, Checkers, ...etc
*	  by Charif Achraf [Celrati](https://github.com/celrati)&& Oussama aouessar [Aizen93](https://github.com/Aizen93)



------------------------------------------------------
## --- HOW TO PLAY 

**e1 e3**  : move the piece from box e1 to box e3

**do o-o** : castle king side

**do o-o-o** : castle queen side

**do restart**   :  restart the game

**do abort**     :  abort the game

**do save** : saves the game into *a file save.oc*

**do load**  : loads the game from *save.oc*



## What has been done :

- Affichage des plateaux en version texte (terminal) et graphics
- Joue d'un coup a tour de role entre 2 joueurs
- Refus d'un coup si les regles ne sont pas respectés
- Affichage de l'aide avec la liste des coups possible a jouer
- Sauvegarde de partie (uniquement avec joueur vs joueur)
- Chargement d'une partie sauvegarder ou un fichier avec une liste de commande a jouer
- Possibilité de jouer contre une Intelligence artificiel aleatoire
- Les conditions d'arret d'un jeu (le jeu s'arrete quand un joueur a gagné selon les regles)
- 4 jeux au total ont été faite (Chess, Shatranj, Dansany chess, et checkers)



## HOW TO COMPILE THE PROGRAME

do:  `$> ./startGame.sh`

-----------------------------------------------------------------------------------------------------
## How to open graphics

the graphics are python scripts, to open them go to folder /Graphics/Classical[Your name game]Graphics
and do: `$> python start.py`


-----------------------------------------------------------------------------------------------------
## How to create a game in less than 30 min:

- Follow the steps bellow :
1 - create your pieces inside the Pieces folder

2 - add conditions to the PieceFactory inside Pieces/PieceFactory just do the same as the others pieces
	and just change the twochar that will represent your pieces
	
3 - add the #include of your pieces class inside the Pieces/PieceFactory !! important

4 - implement your board inside the games/boards folder just respect the same architecure as the ChessBoard !

5 - implement your game inside the games/boards folder just respect the same architecture as the ChessGame !

6 - think of create new method  "writeToFileChecker" inside the pipe/OutpurWriter.hpp and use it for your classes

7 - implement your rule inside the games/rule folder just respect the same architecture as the ChessRule !
    you must implements the check and checkAll methods of your ruler soo the imputReader can use them perfectly
    
8 - inside the files think of create initBoardChecker and use it to init your board inside your Board

9 - CheckerGame::launchGame(); implements this method inside your game and use it in the router 

10 - to test the game just uncomment the Router::get("chckerGame"); and comment the others 

11 - for the interface you will find everything inside the Graphics folder 
		create new folder CheckerChessGraphics inside the Graphics and code the script in python 
		to test it `$> python start.py`
		

12 - dont touch The StateDetector, you dont need it.
---------------------------------------------------------------------------------------------------------
