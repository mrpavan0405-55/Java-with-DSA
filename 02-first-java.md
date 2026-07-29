Write a program to print whether a number is even or odd, also take input from the user.
import java.util.Scanner;

class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        if (num % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }
    }
}
Output:
Enter a number: 8
Even

=== Code Execution Successful ===

Take name as input and print a greeting message for that particular name.
import java.util.Scanner;

class Greeting {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.println("Hello, " + name + "! Welcome.");
    }
}
Output:
Enter your name: Pavan
Hello, Pavan! Welcome.

=== Code Execution Successful ===

Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
import java.util.Scanner;

class SimpleInterest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal: ");
        double p = sc.nextDouble();

        System.out.print("Enter Time: ");
        double t = sc.nextDouble();

        System.out.print("Enter Rate: ");
        double r = sc.nextDouble();

        double si = (p * t * r) / 100;

        System.out.println("Simple Interest = " + si);
    }
}
Output:
Enter Principal: 10000
Enter Time: 2
Enter Rate: 5
Simple Interest = 1000.0

=== Code Execution Successful ===

Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
import java.util.Scanner;

class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        if (op == '+') {
            System.out.println("Result = " + (num1 + num2));
        } else if (op == '-') {
            System.out.println("Result = " + (num1 - num2));
        } else if (op == '*') {
            System.out.println("Result = " + (num1 * num2));
        } else if (op == '/') {
            if (num2 != 0) {
                System.out.println("Result = " + (num1 / num2));
            } else {
                System.out.println("Division by zero is not allowed.");
            }
        } else {
            System.out.println("Invalid operator.");
        }
    }
}
Output:
Enter first number: 5
Enter second number: 25
Enter operator (+, -, *, /): +
Result = 30.0

=== Code Execution Successful ===

Take 2 numbers as input and print the largest number.
import java.util.Scanner;

class LargestNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter second number: ");
        int num2 = sc.nextInt();

        if (num1 > num2) {
            System.out.println("Largest number is: " + num1);
        } else if (num2 > num1) {
            System.out.println("Largest number is: " + num2);
        } else {
            System.out.println("Both numbers are equal.");
        }

        sc.close();
    }
}
Output:
Enter first number: 5
Enter second number: 15
Largest number is: 15

=== Code Execution Successful ===

Input currency in rupees and output in USD.
import java.util.Scanner;

class RupeesToUSD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter amount in Rupees: ");
        double rupees = sc.nextDouble();

        double exchangeRate = 83.0; // 1 USD = 83 INR
        double usd = rupees / exchangeRate;

        System.out.println("Amount in USD: " + usd);

        sc.close();
    }
}
Output:
Enter amount in Rupees: 8300
Amount in USD: 100.0

=== Code Execution Successful ===

To calculate Fibonacci Series up to n numbers
import java.util.Scanner;

class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of terms: ");
        int n = sc.nextInt();

        int a = 0, b = 1;

        System.out.println("Fibonacci Series:");

        for (int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        sc.close();
    }
}
Output:
Enter the number of terms: 10
Fibonacci Series:
0 1 1 2 3 5 8 13 21 34 
=== Code Execution Successful ===

To find out whether the given String is Palindrome or not.
import java.util.Scanner;

class PalindromeString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("The string is a Palindrome.");
        } else {
            System.out.println("The string is not a Palindrome.");
        }

        sc.close();
    }
}
output:
Enter a string: madam
The string is a Palindrome.

=== Code Execution Successful ===

To find Armstrong Number between two given number
import java.util.Scanner;

class ArmstrongRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter starting number: ");
        int start = sc.nextInt();

        System.out.print("Enter ending number: ");
        int end = sc.nextInt();

        System.out.println("Armstrong numbers between " + start + " and " + end + " are:");

        for (int i = start; i <= end; i++) {
            int num = i;
            int sum = 0;
            int digits = String.valueOf(num).length();
            int temp = num;

            while (temp > 0) {
                int rem = temp % 10;
                sum += (int) Math.pow(rem, digits);
                temp /= 10;
            }

            if (sum == num) {
                System.out.println(num);
            }
        }

        sc.close();
    }
}
Output:
Enter starting number: 1
Enter ending number: 50
Armstrong numbers between 1 and 50 are:
1
2
3
4
5
6
7
8
9

=== Code Execution Successful ===
