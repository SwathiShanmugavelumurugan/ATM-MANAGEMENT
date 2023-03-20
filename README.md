# ATM-MANAGEMENT

package ATMPROJECT;

import java.util.Scanner;

public class ATM {
	
	public static void main(String[]args) {
		 int pin = 1234;
		 int balance = 10000;
		 
		 int AddAmount = 0;
		 int TakeAmount = 0;
		 
		 String name;
		 Scanner sc = new Scanner(System.in);
		 
		 System.out.println("Enter your pin number");
		 
		 int password = sc.nextInt();
		 
		 if(password==pin) {
			 System.out.println("Enter your Name");
			  name = sc.next();
			 System.out.println("Welcome"+name);
			  
		while(true)  {
			System.out.println("press 1 to check your balance");
			System.out.println("press 2 to Add amount");
			System.out.println("press 3 to Take Amount");
			System.out.println("press 4 to Take Receipt");
			System.out.println("press 5 to EXIT");
			
			int opt = sc.nextInt();
			switch(opt) 
			{
			case 1:
				System.out.println("your current balance is" + balance);
				break;
			case 2:
				System.out.println("Amount of Money to be Credit");
				AddAmount=sc.nextInt();
				System.out.println("Successfully credited");
				balance=AddAmount+balance;
				System.out.println(balance);
				break;
			case 3:
				System.out.println("Amount of Money to be debit");
				TakeAmount =sc.nextInt();
				if(TakeAmount>balance) {
					System.out.println("Insufficient Balance");
				}else {
					System.out.println("Successfully Debited");
					balance=balance-TakeAmount;
					System.out.println(balance);
				}
				break;
			case 4:
				
				System.out.println("Available Balance is" + balance);
				System.out.println("Amount Deposited " + AddAmount);
				System.out.println("Amount taken " + TakeAmount);
				System.out.println("THANKS FOR COMING");
				break;
				
			case 5:
				
				System.out.println("THANK YOU");
				break;
			
		   default:
			   System.out.println("Wrong pin Number");
				
			}
			
		}
		 }
		 
	}

}
