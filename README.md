# Interest.java
1. You are writing a program (Interest) to determine interest on a savings account compounded annually.  Input  Ask from the user for the following:  Initial investment Annual deposit Number of years Interest Rate  Note that prompts to the user must be followed by a new line  Output  The example shown given the initial investment $1000 and annual deposit of $100, over 25 years of savings, using a compound interest of 6.5%. You can assume the annual deposit is faithfully deposited every year. Create a table with the columns Year, Interest, Deposit and Balance. For each year, calculate the required columns.  Each year should be on a separate line with columns separated by a single tab. The first line should be the column names. The second line should have the year ‘start’ and show the original investment amount under Balance.  All numbers (balance and interest) for each year should be truncated to 2 decimal places.  (int) (number*100.0)/100.0  Code structure  You should create a class called Interest. There should not be a package declared.  Create a method(s) that accept the scanner and a prompt as parameters and returns the user input. A separate method should accept the user input results as parameters, format and print the results. No print statement or scanner input should happen inside main ().  For these assignments you are limited to the language features in Chapters 1-3 of the textbook.  Remember, your program will be graded both on “external correctness” (whether your program compiles and produces exactly the expected outputs), and “internal design and style” (whether your source code follows the style guide).  Submit the final Interest.java file  Example  Enter your initial investment:  1000  Enter your annual deposit:  100  Enter number of Years:  25  Enter interest rate:  6.5  Year Interest Deposit Balance  start 1000.0  1 65.0 100.0 1165.0  2 75.72 100.0 1340.72  3 87.14 100.0 1527.86  4 99.31 100.0 1727.16  5 112.26 100.0 1939.42  6 126.06 100.0 2165.48  7 140.75 100.0 2406.23  8 156.4 100.0 2662.63  9 173.07 100.0 2935.7  10 190.82 100.0 3226.52


import java.util.Scanner;

public class Interest {

        public static void main(String[] args) {
                 inputNew();
        }

        public static void inputNew() {
                  Scanner Scann = new Scanner(System.in);
                  System.out.println("Enter your initial investment: ");
                  double amount = Scann.nextDouble();
                  System.out.println("Enter your annual deposit: ");
                  double annualDeposit = Scann.nextDouble(); 
                  System.out.println("Enter number of Years: ");
                  int years = Scann.nextInt();
                  System.out.println("Enter interest rate: ");
                  double yearlyInterestRate = Scann.nextDouble();

                  double compoundValue = 0; 
                  for (int m = 1; m <= years; m++) {
                           compoundValue = amount * Math.pow((1 + yearlyInterestRate / 100), m);
                  }
                  double sinterest = (amount + (annualDeposit * years)) * (1 + yearlyInterestRate);

// Display result (i n t)(compoundValue*100.0)/100.0);

        }
}
