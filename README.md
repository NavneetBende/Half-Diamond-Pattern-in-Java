Half Diamond Pattern in Java
Programming is not just about solving complex problems or creating functional software; it is also an art form. One way to explore the artistic side of programming is by creating beautiful patterns and designs using code. In this section, we will delve into the fascinating world of geometric art and learn how to create a stunning half diamond pattern using Java.

Understanding the Half Diamond Pattern:
A half diamond pattern is a simple yet visually appealing geometric design. It consists of a series of lines or asterisks forming a diamond shape that is cut in half horizontally. When printed on the console, it produces a symmetric pattern that looks like the top half of a full diamond.

Before we jump into writing Java programs to generate this pattern, let's understand its structure. Consider an example where the user enters the number 5 as input. The half diamond pattern with input 5 would look like this:

*  
**  
***  
****  
*****  
****  
***  
**  
*  
As you can see, the pattern starts off volved with a single asterisk and gradually will increase the range of asterisks in every line till it reaches the input value (in this case, 5). After reaching the peak (5 asterisks in the 5th line), it reverses the process, reducing the range of asterisks in each next line till it reaches 1 once again.
Video Player is loading.Play

Next
Unmute
Current Time 
0:00
/
Duration 
18:10
 
Fullscreen

Backward Skip 10s

Play Video

Forward Skip 10s

Building the Half Diamond Pattern in Java:
Now that we apprehend the structure of the half diamond sample, let us write Java program to generate it. We will use specific techniques: one using nested loops and every other the use of a single loop. Both methods are simple and effective in making the favoured sample.

Approach 1: Using Nested Loops
HalfDiamondPattern.java

import java.util.Scanner;  
public class HalfDiamondPattern {  
    public static void main(String[] args) {  
        // Create a Scanner object to read input from the user  
        Scanner scanner = new Scanner(System.in);  
        // Ask the user to enter the number of rows for the half diamond pattern  
        System.out.print("Enter the number of rows: ");  
        // Read the user input and store it in the variable "rows"  
        int rows = scanner.nextInt();  
        // Calculate the total number of columns for the pattern  
        int totalColumns = rows * 2 - 1;  
        // Calculate the row number at the middle of the pattern  
        int midRow = rows;  
        // Loop through each row of the pattern  
        for (int i = 1; i <= totalColumns; i++) {  
            // Calculate the absolute distance of the current row from the middle row  
            int distance = Math.abs(midRow - i);  
            // Calculate the number of asterisks in each row based on the distance from the middle row  
            int asterisks = rows - distance;  
            // Print the asterisks in the current row to create the left half of the diamond  
            for (int j = 1; j <= asterisks; j++) {  
                System.out.print("*");  
            }  
            // Move to the next line to create a new row in the pattern  
            System.out.println();  
        }  
    }  
}  
Output:

*
**
***
****
*****
****
***
**
*
Approach 2: Using a Single Loop
HalfDiamondPattern.java

import java.util.Scanner;  
public class HalfDiamondPattern {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
        System.out.print("Enter the number of rows: ");  
        int rows = scanner.nextInt();  
        int totalColumns = rows * 2 - 1;  
        int midRow = rows;  
        // Loop through each row  
        for (int i = 1; i <= totalColumns; i++) {  
            // Calculate the absolute distance from the middle row  
            int distance = Math.abs(midRow - i);  
            // Calculate the number of asterisks in each row  
            int asterisks = rows - distance;  
            // Print the asterisks in the current row  
            for (int j = 1; j <= asterisks; j++) {  
                System.out.print("*");  
            }  
            System.out.println();  
        }  
    }  
}  
Output:

*
**
***
****
*****
****
***
**
*
Both approaches will produce the same output for any given input, and you can try different values to observe the various half diamond patterns.
