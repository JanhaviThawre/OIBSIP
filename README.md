# OIBSIP
import java.util.Scanner;

public class NumberGuessingGame {

	// Function that implements the
	// number guessing game
	public static void guessingNumberGame()
	{
		// Scanner Class
		Scanner sc = new Scanner(System.in);

		// Generate the numbers
		int number = 1 + (int)(100* Math.random());

		// Given  trials
		int Trails = 6;

		int user, guess;
		System. out.println("I'm thinking of a number between 1 and 100.");

		System.out.println("A number is chosen" + " between 1 to 100." + " \n Guess the number" + " within 6 trials.");

		// Iterate over Trials
		for (user = 0; user < Trails; user++) {

			System.out.println("Enter the number you Guess:");

			// Take input for guessing
			guess = sc.nextInt();

			// If the number is guessed
			if (number == guess) {
				System.out.println("Congratulations!" + " You guessed the number.");
				break;
			}
			else if (number > guess && user != Trails - 1) {
				System.out.println("The number is " + "greater than " + guess + "\nYou have " +  "less tries left.");
			    
			}
			
			else if (number < guess && user != Trails - 1) {
				System.out.println("The number is" + " less than " + guess + "\nYou have " +  "less tries left.");
				
			}
			
		}

		if (user == Trails) {
			System.out.println("You have exhausted " +  Trails + " trials." + "\n You lose!");

			System.out.println("The number was " + number);
		}
	}

	public static void
	main(String arg[])
	{

		// Function Call
		guessingNumberGame();
	}
}
