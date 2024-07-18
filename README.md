Here's a `README.md` file for the GitHub repository containing the `Linear` and `multi_tetranacci` Tetranacci calculators:

---

# Tetranacci Calculators

This repository contains two Java programs to calculate Tetranacci numbers:
1. `Linear`: Calculates the first 200 Tetranacci numbers using a linear dynamic programming approach.
2. `multi_tetranacci`: Calculates every 5th Tetranacci number up to the 200th term using a recursive approach.

## Tetranacci Sequence
The Tetranacci sequence is a generalization of the Fibonacci sequence where each term is the sum of the previous four terms:
- T(0) = 0
- T(1) = 0
- T(2) = 0
- T(3) = 1
- T(n) = T(n-1) + T(n-2) + T(n-3) + T(n-4) for n > 3

## Files
- `Linear.java`: Contains the linear dynamic programming implementation to calculate Tetranacci numbers.
- `multi_tetranacci.java`: Contains the recursive implementation to calculate every 5th Tetranacci number up to the 200th term.

## How to Run

### Linear.java
1. **Compile**: `javac Linear.java`
2. **Run**: `java Linear`
3. The program will generate the first 200 Tetranacci numbers and write the results along with execution times to `LinearTetranacci.txt`.

### multi_tetranacci.java
1. **Compile**: `javac multi_tetranacci.java`
2. **Run**: `java multi_tetranacci`
3. The program will generate every 5th Tetranacci number up to the 200th term and write the results along with execution times to `MultiTetranacci.txt`.

## Output Files
- `LinearTetranacci.txt`: Contains the Tetranacci numbers calculated by `Linear.java` and the execution times.
- `MultiTetranacci.txt`: Contains the Tetranacci numbers calculated by `multi_tetranacci.java` and the execution times.

## Pseudo Code

### Linear.java
```text
1. Initialize PrintWriter pw to null
2. Initialize n to 0
3. Record start_time as the current system time
4. Try to create a PrintWriter with "LinearTetranacci.txt"
   a. If successful, proceed to step 5
   b. If an exception (FileNotFoundException) occurs, print an error message
5. Loop i from 0 to 200:
   a. Calculate the tetranacci number for n and store it in result
   b. Print "Linear_Tetranacci(" followed by i and ") = " followed by result
   c. Create a string s with the same message
   d. Write string s to the PrintWriter pw
   e. Record endtime as the current system time
   f. Calculate executiontime as endtime - start_time
   g. Print "Execution Time: " followed by executiontime and "ms"
   h. Create a string exe with the same message
   i. Write string exe to the PrintWriter pw
   j. Flush the PrintWriter pw
   k. Increment n by 1
6. Close the PrintWriter pw
7. End of program

Function tetranacci(n):
1. If n is 0, 1, or 2, return 0
2. If n is 3, return 1
3. Otherwise, create an array tetranacci of size n+1
4. Set tetranacci[0], tetranacci[1], and tetranacci[2] to 0
5. Set tetranacci[3] to 1
6. Loop from 4 to n:
   a. Calculate tetranacci[i] as tetranacci[i-1] + tetranacci[i-2] + tetranacci[i-3] + tetranacci[i-4]
7. Return tetranacci[n]
```

### multi_tetranacci.java
```text
1. Initialize terms to 5
2. Initialize PrintWriter pw to null
3. Print "Multi_tetranacci calculator"
4. Record start_time as the current system time
5. Try to create a PrintWriter with "MultiTetranacci.txt"
   a. If successful, proceed to step 6
   b. If an exception (FileNotFoundException) occurs, print an error message
6. Initialize i to 0
7. While i is less than or equal to 200, do the following:
   a. Calculate the tetranacci number for the current terms and store it in result
   b. Print "term :- " followed by terms and " output = " followed by result
   c. Create a string s with the same message
   d. Write string s to the PrintWriter pw
   e. Increment terms by 5
   f. Record endtime as the current system time
   g. Calculate executiontime as endtime - start_time
   h. Print "Execution Time: " followed by executiontime and "ms"
   i. Create a string exe with the same message
   j. Write string exe to the PrintWriter pw
   k. Flush the PrintWriter pw
   l. Increment i by 5
8. Close the PrintWriter pw
9. End of program

Function tetranacci(n):
1. If n is 0, 1, or 2, return 0
2. If n is 3, return 1
3. Otherwise, return the sum of tetranacci(n-1), tetranacci(n-2), tetranacci(n-3), and tetranacci(n-4)
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This `README.md` provides a comprehensive guide for understanding, compiling, and running the Tetranacci calculators, along with detailed descriptions of the programs and their functionality.
