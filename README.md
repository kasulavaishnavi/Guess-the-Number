# Guess-the-Number

    import java.util.Random;
    import java.util.Scanner;

    public class GuessTheNumber {
    public static void main(String[] args) {
        // Create a Random object to generate a random number
        Random random = new Random();
        int randomNumber = random.nextInt(100) + 1; // Generates a number between 1 and 100
        int userGuess = 0;
        int attempts = 0;
        Scanner scanner = new Scanner(System.in);
        System.out.println("Welcome to the Guess the Number game!");
        System.out.println("I'm thinking of a number between 1 and 100. Can you guess it?");

        // Game loop
        while (userGuess != randomNumber) {
            System.out.print("Enter your guess: ");
            userGuess = scanner.nextInt();
            attempts++;

            if (userGuess < randomNumber) {
                System.out.println("Too low! Try again.");
            } else if (userGuess > randomNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
            }
        }

        scanner.close();
    }
}
