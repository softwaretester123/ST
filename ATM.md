# ATM Code

```ATM.java
package ATM;

import java.util.Scanner;

public class ATM {
    int checkAccountType(int t) {
        if (t == 1) {
            System.out.println("Opened Savings Account.");
            return 1;
        } else if (t == 2) {
            System.out.println("Opened Current Account.");
            return 2;
	    } else {
	    	System.out.println("Invalid Account Type.");
	    	return 0;
	    }
	}

	public int deposit(int balance, int amount) {
		if (amount < 0)
			System.out.println("Invalid Amount.");
		else
			balance = balance + amount;
		return balance;
	}

	public int withdraw(int balance, int amount) {
		if (amount < 0) {
			System.out.println("Invalid Amount.");
		} else if (amount > balance) {
			System.out.println("Insuffucient Balance.");
		} else {
			balance -= amount;
		}
		return balance;
	}

	public static void main(String[] args) {
		int pin = 1234, balance = 10000, k = 0, t = 0;

		Scanner sc = new Scanner(System.in);

		ATM atm = new ATM();

		while (k < 3) {
			System.out.println("Enter Pin: ");
			if (pin == sc.nextInt()) {
				System.out.println("\n\n\n\n\n\n");
				System.out.println("=============");
				System.out.println("   Welcome   ");
				System.out.println("=============");
				break;
			} else {
				k ++;
				System.out.println("Incorrect Pin, you have " + (3 - k) + " attempts left");
			}

			if (k == 3) {
				System.out.println("3 tries over. ATM locked.");
				System.exit(0);
			}

		}

		while (t == 0) {
			System.out.println("Enter Account Type:\n1. Savings Account\n2. Current Account");
			t = sc.nextInt();
			t = atm.checkAccountType(t);
		}

		int transaction = 0, amt;

		while (t != 4) {
			System.out.println("\n\n\n\n\n\n");
			System.out.println("Enter the operation:\n1. Deposit\n2. Withdraw\n3. Check Balance\n4. Exit");
			transaction = sc.nextInt();
			switch (transaction) {
				case 1: System.out.println("Enter the amount : ");
						amt = sc.nextInt();
						if (amt % 500 == 0) {
							balance = atm.deposit(balance, amt);
						} else {
							System.out.println("===========================");
							System.out.println("Denomination Not Available.");
							System.out.println("===========================");
						}
					break;
				case 2:System.out.println("Enter the amount : ");
					   amt = sc.nextInt();
					   if (amt % 500 == 0) {
						   balance = atm.withdraw(balance, amt);
					   } else {
						   System.out.println("===========================");
						   System.out.println("Denomination Not Available.");
						   System.out.println("===========================");
					   }
					break;
				case 3: System.out.println(balance);
					break;
				case 4:
					System.exit(0);
			}
		}


	}
}

```
