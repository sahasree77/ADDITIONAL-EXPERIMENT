# ADDITIONAL-EXPERIMENT
# Additional1
# TITLE: Additional-1.) Java program to Insert a sub string into a given main string from a given position
```
import java.util.Scanner;

class SubString {

    public static void main(String args[]) {

        String mainString;
        String subString;
        int position;

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the main String: ");
        mainString = sc.nextLine();

        System.out.print("Enter the sub String: ");
        subString = sc.nextLine();

        System.out.print("Enter the position to insert: ");
        position = sc.nextInt();

        int length = mainString.length() - 1;
        String resultString;

        if (position >= 0 && position <= length) {

            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            resultString = firstPart + subString + secondPart;

            System.out.println("Resultant string = " + resultString);
        }
        else {

            System.out.println("Substring is not possible to insert");
            System.out.println("Its condition 0 <= position <= length of main string");
        }
    }
}
```
# output
![screenshot](exp_additional-1.png)
#Additional2
## TITLE: 2.)Implement the sum of the n Fibonacci numbers
```
import java.util.Scanner;
class Fibonacci {
int sum;
int n;
int firstNumber;
int secondNumber;
int thirdNumber;
Fibonacci(int number) {
n = number;
firstNumber = 0;
secondNumber = 1;
thirdNumber = 0;
sum = 0;
}
void generate() {
if(n>0)
System.out.print("Fibonacci series: ");
while (n > 0) {
if (n == 1) {
System.out.println(firstNumber + ".");
sum = sum + firstNumber;
} else {
System.out.print(firstNumber + ", ");
sum = sum + firstNumber;
}
thirdNumber = firstNumber + secondNumber;
firstNumber = secondNumber;
secondNumber = thirdNumber;
n--;
}
System.out.println("Sum of Fibonacci series = " + sum);
}
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
System.out.print("Enter the value of n: ");
int number = sc.nextInt();
Fibonacci f = new Fibonacci(number);
f.generate();
}
}
```
# OUTPUT
![ADDITIONALEXP 2 OUTPUT](exp_additional2_output.png)
