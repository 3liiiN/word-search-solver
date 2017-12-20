# word-search-solver
A program that solves word search puzzles of arbitrary dimensions. Locates all words of length 6 or more that appear horizontally, vertically, and diagonally, either forwards or backwards (no wraparounds).

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
- Each puzzle row, columns,and diagonal (both directions) is turned into a string with no spaces. 
 The row strings are pushed in order into a vector of row strings, the column strings are pushed  in order into
 a vector of column strings, and the diagonal strings are pushed  in order into their respective vectors of diagonal strings
- Serial search is performed for each dictionary word length 6 or longer in every
  string in each vector, forwards and backwards
  ```
  	 // Search rows
        // --------->
        // --------->
        // --------->
	
  ```
- Found words and their start and end positions are stored alphabetically in a multimap.  


## Output
"answers.txt" is generated to report found words alphabetically with start and end positions.

![alt text](https://user-images.githubusercontent.com/34634457/34187055-49ead426-e4e4-11e7-9501-b720fcf87e2c.png)
