import java.util.Scanner;

public class Game {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        int playerX = 0;
        int playerY = 0;

        System.out.println("=== MY JAVA GAME ===");
        System.out.println("W = Up");
        System.out.println("S = Down");
        System.out.println("A = Left");
        System.out.println("D = Right");
        System.out.println("Q = Exit");

        while (true) {
            System.out.println("Player Position: X=" + playerX + " Y=" + playerY);
            System.out.print("Enter Move: ");

            String move = input.nextLine().toLowerCase();

            switch (move) {
                case "w": playerY++; break;
                case "s": playerY--; break;
                case "a": playerX--; break;
                case "d": playerX++; break;
                case "q":
                    System.out.println("Game Over!");
                    input.close();
                    return;
                default:
                    System.out.println("Invalid Move!");
            }
        }
    }
