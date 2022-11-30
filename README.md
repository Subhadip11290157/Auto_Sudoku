# Sudo-in-Seconds
Sudoku is a popular puzzle that has held the interest of mathematicians for its complex possibilities of intermediate states. Generally, it takes from some minutes to even many hours to solve a single Sudoku based on its difficulty level. But, when it comes to computers, we can compute a solution in seconds. Thanks to the different algorithms that do so[2]. But that’s only when we have a proper matrix of integers (representing the board) available as an input to the algorithm. How often do we get a Sudoku board in such a format? Never. Thus, to address this issue, we have developed an all-in-one Sudoku solver! But first of all, let’s dive into the rules of the game.   

## Rules of the game:
Sudoku is a number puzzle that can have multiple solutions. It’s played on a grid of 9 x 9 spaces. Within the rows and columns are 9 “squares” (made up of 3 x 3 spaces). Each row, column and square (9 spaces each) needs to be filled out with the numbers 1-9, without repeating any numbers within the row, column or square. Initial board configuration comprises some vacant squares and the remaining squares filled with a number (1 to 9) each. The task is to fill up those vacancies without violating any of the rules (mentioned above). When all the squares are filled, the puzzle is solved!  

## Utility offered:
Considering the fact that Sudokus come in newspapers, magazines, books or even on mobile apps; all of which can be captured on camera, we have provided a live input capture feature via webcam(in PCs) / front camera(in smartphones). Now the user has to hold the puzzle in front of the device and the solved squares will be displayed in green on the live moving image of the board on the screen itself, that too in a matter of seconds. So we get to experience a hassle free, interactive interface and instant solution. It was never as easy as this to solve a Sudoku puzzle.

## Approach adopted:
The project is implemented in 4 key segments :-
- i) `Tracking the board` (in the frames of live video capture) and each and every box/cell in it distinctly. This also involves filters and pre-processing of the captured image with the help of OpenCV library functions. 
- ii) `Recognition of digits(1-9)` from images of all 81 cells. Then a matrix of integers is made, inserting them one by one into it.
- iii) The matrix of integers (which represents the puzzle) is `fed to the optimized backtracking algorithm`  for getting a solution matrix.
- iv) The solution matrix has to be `overlaid onto the live image of the puzzle board on the screen`, only highlighting the filled vacancies in green, using OpenCV again.
