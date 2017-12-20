# word-search-solver
A program that solves word search puzzles of arbitrary dimensions. It locates the start and end positions of all length 6 or longer words from a dictionary that appear horizontally, vertically, and diagonally, either forwards or backwards in the puzzle. Wraparounds are excluded.

- Uses "words.txt" as dictionary
- Uses "puzzle.txt" as puzzle
- Position matrix (row, column):<br />
	  (0,0) (0,1) (0,2) …<br />
		(1,0) (1,1) (1,2) …<br />
		(2,0) (2,1) (2,2) …<br />
		  .<br />
		  .<br />
		  .<br />

## Data Structures: 
- Dictionary is stored in an unordered_set. 
- Every puzzle row, column, and diagonal (both directions // and \\\\ ) is turned into a string with no spaces. 
 The row strings are pushed in order into a vector of row strings, the column strings are pushed in order into
 a vector of column strings, and the diagonal strings are pushed in order into their respective vectors of diagonal strings
- Serial search is performed for each dictionary word length 6 or longer in every
  string in each vector, forwards and backwards. Words can only be found in diagonals if the puzzle has at least 6x6 dimensions.
  
  **Forwards:**
  ```
	// Search rows
	// --------->
	// --------->
	// --------->
	
	// Search columns
	// | | |
	// | | |
	// V V V
	
	// Search diagonals, if possible
	//  \ \ \              / / /
	//   \ \ \    and     / / /
	//    V V V          V V V
	
  ```
    
  **Backwards:**
  ```
	// Search rows
	// <---------
	// <---------
	// <---------
	
	// Search columns
	// ^ ^ ^
	// | | |
	// | | |
	
	// Search diagonals, if possible
	// ^ ^ ^                ^ ^ ^
	//  \ \ \     and      / / /
	//   \ \ \            / / /
	
  ```
- Found words and their start and end positions are stored alphabetically in a multimap. Positions are calculated from row/column/diagonal number within the vector (since they are in order) and the positions of the beginning/end character of the word within the row/column/diagonal string.


## Output
"answers.txt" is generated to report found words alphabetically with start and end positions.

![alt text](https://user-images.githubusercontent.com/34634457/34187055-49ead426-e4e4-11e7-9501-b720fcf87e2c.png)
