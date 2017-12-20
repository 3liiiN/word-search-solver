# word-search-solver
A program that solves word search puzzles of arbitrary dimensions. Locates all words of length 6 or more that appear horizontally, vertically, and diagonally, either forwards or backwards (no wraparounds).

- Uses "words.txt" as dictionary
- Uses "puzzle.txt" as puzzle
- Generates "answers.txt" to report found words alphabetically with start and end positions
- Dictionary stored in an unordered_set. Puzzle rows, columns,
	   and diagonals (both directions) stored in vectors. 
	   Found words and locations stored alphabetically in a multimap.
- Matrix (row, column):<br />
	  (0,0) (0,1) (0,2) …<br />
		(1,0) (1,1) (1,2) …<br />
		(2,0) (2,1) (2,2) …<br />
		  .<br />
		  .<br />
		  .<br />

## Output
![alt text](https://user-images.githubusercontent.com/34634457/34187055-49ead426-e4e4-11e7-9501-b720fcf87e2c.png)
