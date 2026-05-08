import java.util.*;

public class Calculator {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        while (true) {

            try {

                System.out.print("Enter no1: ");
                double n1 = sc.nextDouble();

                System.out.print("Enter no2: ");
                double n2 = sc.nextDouble();

                System.out.print("Enter operator (+, -, *, /, %, ^): ");
                char o = sc.next().charAt(0);

                double result = 0;

                switch (o) {

                    case '+':
                        result = n1 + n2;
                        break;

                    case '-':
                        result = n1 - n2;
                        break;

                    case '*':
                        result = n1 * n2;
                        break;

                    case '/':

                        if (n2 == 0) {
                            throw new ArithmeticException("Division by 0 not allowed");
                        }

                        result = n1 / n2;
                        break;

                    case '%':

                        if (n2 == 0) {
                            throw new ArithmeticException("Modulo by 0 not allowed");
                        }

                        result = n1 % n2;
                        break;

                    case '^':

                        if (n1 == 0 && n2 < 0) {
                            throw new IllegalArgumentException("Invalid power operation");
                        }

                        result = Math.pow(n1, n2);
                        break;

                    default:
                        throw new IllegalArgumentException("Invalid Operator");
                }

                System.out.println("Result: " + result);

            }

            catch (ArithmeticException e) {
                System.out.println("Arithmetic Error: " + e.getMessage());
            }

            catch (IllegalArgumentException e) {
                System.out.println("Illegal Argument Error: " + e.getMessage());
            }

            System.out.print("Want another operation? (y/n): ");
            char y = sc.next().charAt(0);

            if (y == 'n' || y == 'N') {
                System.out.println("Exiting...");
                break;
            }
        }

        sc.close();
    }
}
