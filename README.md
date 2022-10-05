# CNN Chess Model using Stockfish evaluations 
 
# Two files: ChessCNN and MinMaxAglorithm 

- ChessCNN: Defines a chess board data gathering method which creates a random board using python chess APIs, then has Stockfish read the board and give it an evaluation in favor of black or white. The board is then separated into 3-dimensions which accounts for the 8x8 board and the 6 different pieces: Black/White Pawns, Bishops, Knights, Rooks, Queens, Kings, and then all the possible white and black attack squares. I then build a CNN which had 2 convolutional layers, 2 batch normalization layers, 2 acctivation layers, a flatten layer, then 2 dense layers to finalize 1 dimensional output. 
- 
- MinMaxAlgorithm: Define an algorithm which takes a specific boardstate and iteravely calculates the best possible move for the moving player while assuming the opposing player will also make their best move. This is called a Mini-Max Algorithm and is a very strong choice for picking an option out of a tree of possibilities. The rest of the code uses this algorithm to have the CNN play against Stockfish, itself, and a real player. 
