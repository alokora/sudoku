                                SUDOKU GAME: C++ Programming


Sudoku is one of the most popular classic games. The playing grid of sudoku consists of the n^2*n^2 squares space for n=2, 3, 4, 5, and so on. The game initially has n^2 squares combining rows and columns. Out of these n^2 squares, every square is a separate grid of n*n square spaces. Every row and column has n^2 squares.
 It can be either one player or multiple players can play it online,  where the competitors try to fill the boxes faster than their opponents. The game’s primary purpose is to fill boxes in every square with unique numbers. The exciting thing about the Sudoku game is that no column, row, or square allows repeating a number.
We implement it for the 9*9 grid.
                       
                            
3		6	5		8	4		
5	2							
	8	7					3	1
		3		1			8	
9			8	6	3			5
	5			9		6		
1	3					2	5	0
							7	4
		5	2		6	3		





1.	The game board should be of 9*9 squares space.
2.	The game should display the grid with some of the boxes already filled with random numbers ranging from 1 to 9.
3.	The game should allow the player to fill in empty boxes.
4.	The game should not allow the player to repeat any number in any row, column, or square.
5.	If the player fills all the boxes with correct numbers and without any repetition, he wins the game.


 To solve the sudoku we use recursion with backtracking. Backtracking is a useful algorithm for solving the problem with recursion by building a solution incrementally. Generally, backtracking involves starting with a possible solution, and if it doesn’t work, you backtrack and try another solution until you find the correct one.
We implemented steps to solve it
1.	Level – we defined a level in a grid of 9*9 squares, every square out of 9*9 such squares, and traversed each level.

2.	Choice- for each level we have the choice of filling  (1-9) numbers, after iterating and filling each, we checked whether it is valid or not using check(); 


3.	Check()- to check the repetition of any number in any row, column, and grid of 3*3 squares, if yes, then return false else return true. 

4.	Place- after a check() returns true, we place the choice and move to the next level, when the level ends we increment the answer.


