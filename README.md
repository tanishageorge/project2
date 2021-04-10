# project2

package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        int principal = 0;
        double rate = 0;

        while(true) {
            System.out.println("Principal(1k -1M): ");
            principal = scan.nextInt();

            if (principal < 1_000_000 && principal > 1000)
                break;
            System.out.println("Enter within the range: ");

        }

        while(true) {
            System.out.println("Monthly Interest Rate: ");
            rate = scan.nextDouble() / 100;

            if (rate >= 1) {
                break;
            }
            System.out.println("Enter a value above 1: ");
        }

        System.out.println("Number of payments: ");
        int pay = scan.nextInt();

        double rates = (Math.pow(rate + 1, pay) * rate) /
                (Math.pow(rate + 1, pay) -1);


        double total = principal * rates;
        System.out.println("Mortgage: " + total);

        greetUser("Ameya", "Ameya");
    }

    public static void greetUser(String firstName, String lastName){
        System.out.println("Hello " + firstName + " "+ lastName);
    }
}
