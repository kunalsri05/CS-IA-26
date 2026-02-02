import java.util.ArrayList;
import java.util.Scanner;

public class Main {

    static ArrayList<Double> expenses = new ArrayList<>();
    static double spendingLimit = 0;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        boolean isrunning = true;

        while (isrunning) {
            System.out.println("Welcome Urvi. Enter your selection below:");
            System.out.println("1 Add Expense");
            System.out.println("2 Set Spending Limit");
            System.out.println("3 View Total Spending");
            System.out.println("0 Exit");
            System.out.print("Choice: ");

            String choice = sc.nextLine();

            if (choice.equals("1")) {
                System.out.print("Enter amount: ");
                double amount = Double.parseDouble(sc.nextLine());
                expenses.add(amount);

                //double total = getTotal(); DO GET TOTAL CLASS
                if (spendingLimit > 0 && total > spendingLimit) {
                    System.out.println("");
                }
            }

            else if (choice.equals("2")) {
                System.out.print("Enter limit: ");
                spendingLimit = Double.parseDouble(sc.nextLine());
            }

            else if (choice.equals("3")) {
                //System.out.println("Total spent: $" + getTotal());
            }

            else if (choice.equals("0")) {
                isrunning = false;
            }
        }

        sc.close();
    }


}

