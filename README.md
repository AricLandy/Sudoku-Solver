# Sudoku Solver
[![Build Status](https://travis-ci.org/AricLandy/Sudoku-Solver.svg?branch=master)](https://travis-ci.org/AricLandy/Sudoku-Solver)

This Project was developed before I used Git Hub to show my work, all of the code was written by me, just unfortunately not using proper source control techniques. 
## How it works
This solver uses a backtracking algorithm. 
A custom iterator starts at the top left of the puzzle and moves down to the bottom right. When it is at each element, it tests all possible values (starting at 1 all the way to 9). When an element is considered promising (see "Promising"), the iterator moves on to the next element. If all possibilities are exhausted and none are "promising", the program moves back to the previous element and starts incrementing it from where it previously left off. When the program reaches a "promising" value at the last element, the puzzle is solved  
### Example Output
```
 ------- ------- -------
|   6   | 1   4 |   5   | 
|     8 | 3   5 | 6     | 
| 2     |       |     1 | 
 ------- ------- -------
| 8     | 4   7 |     6 | 
|     6 |       | 3     | 
| 7     | 9   1 |     4 | 
 ------- ------- -------
| 5     |       |     2 | 
|     7 | 2   6 | 9     | 
|   4   | 5   8 |   7   | 
 ------- ------- -------
 ------- ------- -------
| 9 6 3 | 1 7 4 | 2 5 8 | 
| 1 7 8 | 3 2 5 | 6 4 9 | 
| 2 5 4 | 6 8 9 | 7 3 1 | 
 ------- ------- -------
| 8 2 1 | 4 3 7 | 5 9 6 | 
| 4 9 6 | 8 5 2 | 3 1 7 | 
| 7 3 5 | 9 6 1 | 8 2 4 | 
 ------- ------- -------
| 5 8 9 | 7 1 3 | 4 6 2 | 
| 3 1 7 | 2 4 6 | 9 8 5 | 
| 6 4 2 | 5 9 8 | 1 7 3 | 
 ------- ------- -------
 ```
### Promising
An element is considered promising if it is valid in terms of the Sudoku puzzle rules. This means that there can not be any elements of the same value in the same row, column, or box
## How to Run
1) Clone this repository
``` shell
git clone https://github.com/AricLandy/Sudoku-Solver.git
```
2) Build and run with the test-1-input.txt
``` shell
make solve
./solve
```
## Further Expansion Ideas
1) This puzzle only works for a standard 9x9 puzzle but since most of the code is written generically, a few minor modifications could allow it to work for Sudoku puzzles of any size
2) The main way to run this program is to create a textfile and then edit main.cpp to take in that specific text file. Adding a graphical way to input data would be very helpfull
