## Question :
Withdrawing Cash (Q1)

The code provided reads in the users bank balance and stores it in the variable balance. It then reads in the amount the user would like to withdraw and stores it in a variable called withdraw.

Your task is print various output situations depending on whether they have enough money to withdraw, have exactly the right amount to withdraw or not enough to withdraw. Refer to the below input/output examples for the exact prompts that need to be printed.
```java
import java.util.Scanner;

public class Withdraw {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
System.out.print("Enter your bank balance: ");
double balance = sc.nextDouble();
System.out.print("Enter your withdrawal amount: ");
double withdraw = sc.nextDouble();
// DON'T TOUCH ANY CODE ABOVE THIS LINE

// Your code goes here!

}
}
```

## Solution :
The answer provided below has been developed in a clear step by step manner.
Step: 1
The situation when the customer wants to withdraw amount from the bank could be :-

1. If the user enters greater amount than the balance he/she already has.
2. If the user enters amount less than the balance he/she already has.
3. If  the user enters amount equal to the balance he/she already has.
4. If the user enters no amount or 0.

Explanation:
Added explanation of the asked question above.

Step: 2
Attached the code with comments for better understanding :-

```java
import java.util.Scanner;

public class Withdraw {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter your bank balance: ");
		double balance = sc.nextDouble();
		System.out.print("Enter your withdrawal amount: ");
		double withdraw = sc.nextDouble();
		// DON'T TOUCH ANY CODE ABOVE THIS LINE

		// Your code goes here!
		// Conditions as mentioned in the explanation above.
		if (balance < withdraw) {
			System.out.println("Your balance is too low");
		} else if (balance >= withdraw) {
			balance -= withdraw;
			System.out.println("The left amount is " + balance);
		} else if (withdraw == 0) {
			System.out.println("Please enter a greater amount than 0 , and try again...");
		}

	}
}
```

Attaching the output of the program :
![image](https://user-images.githubusercontent.com/78461084/197188622-d5541e2e-869f-4252-a6d9-2ec3b335a9d9.png)

### Give this Project a Star :star:
