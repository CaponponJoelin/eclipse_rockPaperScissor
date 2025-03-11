import java.util.Random;
import java.util.Scanner;
public class RockPaperScissorMain {
	public static void main(String args[]) {
	Scanner s = new Scanner(System.in);
	Random random = new Random();

	boolean exit = false;
	
	try {
		while(!exit) {
    	System.out.println("----------------------------------------------------------");	
			System.out.println("Hello!, Welcome to Rock, Paper, Scissor. " + "\n'Press Enter to Continue...'");
			s.nextLine();
    	System.out.println("----------------------------------------------------------");
			System.out.println("Please Choose between: Rock, Paper, Scissor" + "\n\n'choose X to exit'");
			System.out.print("\nInput: ");
		String Choice =s.nextLine().trim();
		System.out.println("----------------------------------------------------------");
		
		if (Choice.equalsIgnoreCase("Rock")) {
			System.out.println("You chose a rock!");
		}
		else if(Choice.equalsIgnoreCase("Paper")) {
			System.out.println("You chose a paper!");
		}
		else if(Choice.equalsIgnoreCase("Scissor")) {
			System.out.println("You chose a scissor!");
		}
		else if(Choice.equalsIgnoreCase("X")) {
			System.out.println("Exiting....");
			
			break;
		}
		else {
			System.out.println("Invalid Input!!!, Choices should be: rock, paper,scissors only!");
			continue;
		}
		System.out.println("");
		int num;
		String bot = "";
		num = random.nextInt(3)+1;
		if(num == 1) {
			bot = "Rock";
		}
		else if(num == 2) {
			bot = "Paper";
		}
		else if(num == 3) {
			bot = "Scissor";
		}
		if (bot.equalsIgnoreCase("Rock")) {
			System.out.println("the bot chose a rock!");
		}
		else if(bot.equalsIgnoreCase("Paper")) {
			System.out.println("the bot chose a paper!");
		}
		else if(bot.equalsIgnoreCase("Scissor")) {
			System.out.println("the bot chose a scissor!");
		} 
		
		System.out.println("");
		if (Choice.equalsIgnoreCase("Rock") && bot.equals("Paper")) {
			System.out.println("You Lose!...");
		}else if (Choice.equalsIgnoreCase("Paper") && bot.equals("Scissor")) {
			System.out.println("You Lose!...");
		}else if (Choice.equalsIgnoreCase("Scissor") && bot.equals("Rock")) {
			System.out.println("You Lose!...");
		}else if (Choice.equalsIgnoreCase("Rock") && bot.equals("Scissor")) {
			System.out.println("You Win!...");
		}else if (Choice.equalsIgnoreCase("Paper") && bot.equals("Rock")) {
			System.out.println("You Win!...");	
		}else if (Choice.equalsIgnoreCase("Scissor") && bot.equals("Paper")) {
			System.out.println("You Win!...");
		}else if (Choice.equalsIgnoreCase("Rock") && bot.equals("Rock")) {
			System.out.println("Draw!...");
		}else if (Choice.equalsIgnoreCase("Paper") && bot.equals("Paper")) {
			System.out.println("Draw!...");
		}else if (Choice.equalsIgnoreCase("Scissor") && bot.equals("Scissor")) {
				System.out.println("Draw!...");
		}
		s.nextLine();


		
		System.out.println("Do you wish to make another choices?   Yes/ No");
		System.out.print("Input: ");
		String yesNo = s.nextLine().trim();
		
		if(yesNo.equalsIgnoreCase("No")) {
			System.out.println("Exiting...");
			break;
		}else if(yesNo.equalsIgnoreCase("Yes")) {
			System.out.println("As you wish...");
		}else {
			System.out.println("Wrong Input!.... Redirecting back to Welcome Page."); 
			continue;
		}
		}
	}catch(Exception e) {
		System.out.println("Invalid Input!.");
	}finally {
		System.out.println("Completed...");
		s.close();
	}
	}
}
