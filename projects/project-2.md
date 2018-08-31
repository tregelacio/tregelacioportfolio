---
layout: project
type: project
image: images/vacay-square.png
title: Sudoku Solver
# All dates must be YYYY-MM-DD format!
date: 2018-03-15
labels:
  - Java
  - Recursion
summary: A recursively solving sudoku solver that I created in ICS 211.
---

<img class="ui medium right floated rounded image" src="../images/vacay-home-page.png">
	
   A sudoku solver that takes in values from an incomplete sudoku puzzled solves it using recursion by inserting different values into the boxes until it is completely solved. If a single box up until a certain point doesn’t fit within the rules of sudoku then the program recursively goes back to that spot to test the next available number that is in the array. 

   This was an assignment given in a class that taught Intermediate Java. From here we learned about certain techniques that weren’t shown in the previous Java class. From this assignment, it was important that the recursive method worked perfectly as well as efficiently because with the three test sudoku puzzles, we had to make sure the last puzzle took the longest with the recursive method. The tests were designed so that we are able to visually see how long the puzzles would take and how they differ from each other.

   This project has given me a stronger understanding of recursion, which was one of the most difficult topics in the course. Trying to understand how to structure the recursive method was one of the challenges that I had that I overcame.
   

   
```j
  public static boolean checkSudoku(int[][] sudoku, boolean printErrors) {
    if (sudoku.length != 16) {
      if (printErrors) {
        System.out.println("sudoku has " + sudoku.length + " rows, should have 16");
      }
      return false;
    }
    for (int i = 0; i < sudoku.length; i++) {
      if (sudoku[i].length != 16) {
        if (printErrors) {
          System.out.println("sudoku row " + i + " has " + sudoku[i].length + " cells, should have 16");
        }
        return false;
      }
    }
    /* check each cell for conflicts */
    for (int i = 0; i < sudoku.length; i++) {
      for (int j = 0; j < sudoku.length; j++) {
        int cell = sudoku[i][j];
        if (cell == -1) {
          continue; /* blanks are always OK */
        }
        if ((cell < 0) || (cell > 16)) {
          if (printErrors) {
            System.out
                .println("sudoku row " + i + " column " + j + " has illegal value " + String.format("%02X", cell));
          }
          return false;
        }
        /* does it match any other value in the same row? */
        for (int m = 0; m < sudoku.length; m++) {
          if ((j != m) && (cell == sudoku[i][m])) {
            if (printErrors) {
              System.out.println(
                  "sudoku row " + i + " has " + String.format("%X", cell) + " at both positions " + j + " and " + m);
            }
            return false;
          }
        }
        /* does it match any other value it in the same column? */
        for (int k = 0; k < sudoku.length; k++) {
          if ((i != k) && (cell == sudoku[k][j])) {
            if (printErrors) {
              System.out.println(
                  "sudoku column " + j + " has " + String.format("%X", cell) + " at both positions " + i + " and " + k);
            }
            return false;
          }
        }
        /* does it match any other value in the 4x4? */
        for (int k = 0; k < 4; k++) {
          for (int m = 0; m < 4; m++) {
            int testRow = (i / 4 * 4) + k; /* test this row */
            int testCol = (j / 4 * 4) + m; /* test this col */
            if ((i != testRow) && (j != testCol) && (cell == sudoku[testRow][testCol])) {
              if (printErrors) {
                System.out.println("sudoku character " + String.format("%X", cell) + " at row " + i + ", column " + j
                    + " matches character at row " + testRow + ", column " + testCol);
              }
              return false;
            }
          }
        }
      }
    }
    return true;
  }
```

 
Source: <a href="https://github.com/theVacay/vacay"><i class="large github icon"></i>theVacay/vacay</a>
