# TIC-TAC-TOE-game
A TIC-TAC-TOE game made using HTML, CSS &amp; JS


**HTML code for a Tic Tac Toe game webpage**

It begins with the declaration of a DOCTYPE to specify that this is an HTML document. 
The html tag defines the beginning and end of the HTML document, and the lang attribute specifies the language of the document, which is English (en).
The head section contains various metadata information about the document, such as the character encoding (meta charset), the compatibility mode for Internet Explorer (meta http-equiv), and the viewport configuration (meta name="viewport"), which specifies the size and scale of the content when displayed on different devices. 
Additionally, it includes a reference to an external style sheet file (link rel="stylesheet" href="style.css"), which defines the styling for the webpage.
The body section defines the visible content of the webpage. 
The div with class="container" is a wrapper for the entire content of the webpage, while the div with class="game" contains the actual game board. 
The game board is made up of 9 div elements with class="cell" that represent the individual cells of the board. 
The cells are grouped into three rows, each with three cells, using the div elements with class="cells".
The h1 element with class="heading" is the title of the game, and there is a div element with class="score" that displays the score of the game. 
The score section includes two span elements with IDs playerXScore and playerOScore that represent the score for the X and O players, respectively, and a span element with ID draws that represents the number of draws. 
The button with class="resetBtn" is used to reset the game to its initial state. Finally, there is a div element with class="toast" that is used to display messages to the user.
The script element at the end of the body section includes a reference to an external JavaScript file (src="script.js") that contains the logic for the game.

**CSS code for a Tic Tac Toe game webpage**

This code defines the styling for a Tic Tac Toe game, including the font, colors, and layout. 
It uses the Google Fonts API to import the "Poppins" font family and sets the background color to #5543a3. 
The game board is defined using flexbox and each cell is a square with a border, while the X's and O's are represented by images. 
The score section displays the scores for each player and the number of draws. 
The "New Game" button resets the game board, and the "toast" element displays messages during gameplay.

**JS code for a Tic Tac Toe game webpage**

The code defines a number of variables, including:

cells: an array of all the game cells.
playerXScoreSpan: a reference to the HTML element that shows the score for player X.
playerOScoreSpan: a reference to the HTML element that shows the score for player O.
resetBtn: a reference to the HTML element that resets the game.
toastDiv: a reference to the HTML element that shows a toast message.
draws: a reference to the HTML element that shows the number of draws.
It also defines some constants:

playerX: a string representing player X.
playerO: a string representing player O.
The code initializes some variables:

playerXScore and playerOScore: variables that store the score for player X and player O, respectively.
currentLevel: a variable that stores the current level of the game.
flag: a variable that determines whether or not the game is still in progress.
currentPlayer: a variable that stores the current player.
The winCombos array stores all possible winning combinations for the game.

The for loop iterates through all the cells in the cells array and attaches an event listener to each cell that calls the cellClicked() function when clicked.
The cellClicked() function is called when a player clicks on a cell. 
It checks if the flag variable is true and whether the clicked cell is empty. 
If both conditions are met, it appends an image of the current player to the cell using the addImg() function, then checks for a winner using the checkWinner() function and checks for a draw using the checkDraw() function. 
If the current player is X, it switches to O, and vice versa.
The addImg() function creates and returns an HTML image element with a src attribute pointing to an image of the current player.
The checkWinner() function checks all possible win combinations using a for loop. 
If a winning combination is found and all three cells have the same content, it displays a toast message announcing the winner, increments the score of the current player using the updateScore() function, sets the flag variable to false, increments the currentLevel variable, and resets the game after 2 seconds using the reset() function.
The checkDraw() function checks if all the cells are filled and no winner is found. If true, it displays a toast message announcing a draw, increments the currentLevel variable, and resets the game after 2 seconds using the reset() function.
The toast() function displays a toast message by adding the show class to the toastDiv element, setting its text content to the message passed as an argument, and removing the show class after 1 second using setTimeout().
The updateScore() function increments the score of the current player, updates the score element in the HTML, and switches the current player.
The reset() function resets all cells, sets the flag variable to true, and resets the level.
Finally, the resetBtn element has an event listener attached to it that calls the reset() function, sets the score variables to 0, and displays a reset message using the toast() function. 
After 2 seconds, it increments the level and sets the flag variable to true
