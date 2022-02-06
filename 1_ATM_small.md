# ATM small
```

import java.util.Scanner;

public class ATM {
	public static void main(String[] args) {
		int balance = 10000, pin = 1234, c = 3;
		@SuppressWarnings("resource")
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Enter your pin: ");
		while (c > 0) {
			if (pin == sc.nextInt()) {
				
				System.out.println("1. Savings Account\n2.Current Account");
				if (sc.nextInt() == 1 || sc.nextInt() == 2) {
					System.out.println("1.Check Balance\n2.Deposit\n3.Withdraw\n4.Exit");
					int ch = 0;
					do {
						ch = sc.nextInt();
						switch(ch) {
							case 1: System.out.println("Balance = " + balance);
								break;
							case 2: System.out.println("Enter Amount:");
									balance += sc.nextInt();
									System.out.println("New balance is " + balance);
								break;
							case 3: System.out.println("Enter Amount:");
									int amount = sc.nextInt(); 
									if (balance >= amount)
										balance -= amount;
									else
										System.out.println("Insufficient balance");
									System.out.println("New balance is " + balance);
								break;
							case 4:
								System.exit(0);
							default: System.out.println("Invalid");
								break;
						}
					} while(ch != 4);
				}
				
			} else {
				System.out.println("Invalid Pin");
				c --;
			}
		}		
	}
}

```