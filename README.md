import java.util.Scanner;

// Kenyah Collins, 1/29/2023, categorize wind speed limit with hurricane wind scale

public class Main {
    public static Scanner input = new Scanner(System.in);

    public static void main(String[] args) {
        long speed;
        String classification;

        // input for user to enter wind speed (mph)
        System.out.print("Enter wind speed (mph): ");
        speed = input.nextLong();

        // Be sure to make negatives invalid
        while (speed < 0) {
            System.out.print("Invalid input, please try again: ");
            speed = input.nextLong();
        }

        // nested if statements to categorize the user input wind speed into six categories
        if (speed <= 38) {
            classification = "Classification: not in scale ";
        } else if (speed <= 73) {
            classification = "Classification: tropical storm";
        } else if (speed <= 95) {
            classification = "Classification: Category One Hurricane";
        } else if (speed <= 110) {
            classification = "Classification: Category Two Hurricane";
        } else if (speed <= 129) {
            classification = "Classification: Category Three Hurricane";
        } else if (speed <= 156) {
            classification = "Classification: Category Four Hurricane";
        } else {
            classification = "Classification: Category Five Hurricane";
        }
        // output hurricane class to user
        System.out.print( classification );
        }
    }

