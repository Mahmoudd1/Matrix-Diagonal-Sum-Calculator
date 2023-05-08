# Matrix-Diagonal-Sum-Calculator

This program receives a square matrix mat and returns the sum of the matrix diagonals, as specified below:

- The sum includes all the elements on the primary diagonal.
- The sum also includes all the elements on the secondary diagonal that are not part of the primary diagonal.
- The method diagonalSum receives the matrix mat as input and returns an integer representing the sum of the matrix diagonals.

## Example 1:
Input: mat = [[1,2,3],[4,5,6],[7,8,9]]

Output: 25

Explanation: Diagonals sum: 1 + 5 + 9 + 3 + 7 = 25
Notice that element mat[1][1] = 5 is counted only once.

## Example 2:
Input: mat = [[1,1,1,1],[1,1,1,1],[1,1,1,1],[1,1,1,1]]

Output: 8


## Constraints:
n == mat.length == mat[i].length
1 <= n <= 100
1 <= mat[i][j] <= 100

## Approach
To calculate the matrix diagonal sum, the program iterates through each row of the matrix using a for-loop. At each iteration, the program:

Updates the current position on the primary diagonal (sum+=mat[i][j]).
If the current row is not the middle row of the matrix (m!=i), the program also updates the current position on the secondary diagonal (sum+=mat[k][m]), where k and m are calculated based on the current row and the matrix dimensions.

Complexity Analysis
Since we iterate through the matrix once, the time complexity of the solution is O(n^2), where n is the size of the matrix. 
The space complexity is O(1), since we only need to store a constant amount of variables.
