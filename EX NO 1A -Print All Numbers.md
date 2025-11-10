
# EX 1A Print All Numbers 
## DATE: 09-08-2025
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Start the program and import the `Scanner` class to take user input.
2. Create a `Scanner` object to read an integer input `N` from the user.
3. Check if `N` is greater than 0; if not, display `"Invalid input. N must be greater than 0."`
4. Use a `for` loop to iterate from 1 to `N`.
5. Print each number separated by a space on the same line.  

## Program:
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter an integer N: ");
        int N = scanner.nextInt();
        
        for (int i = 1; i <= N; i++) {
            System.out.print(i);
            if (i < N) System.out.print(" ");
        }
        
        scanner.close();
    }
}

```

## Output:
<img width="394" height="86" alt="image" src="https://github.com/user-attachments/assets/1f311836-ade1-40b1-84a2-5fbc13b43236" />



## Result:
The program successfully print all the numbers from 1 to N. 

```
/*
Program to implement Reverse a String
Developed by: ASWIN B
Register Number:  212224110007
*/
```
