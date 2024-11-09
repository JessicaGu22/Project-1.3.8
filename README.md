# Project-1.3.8

import java.util.Scanner;
public class AdventureGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        boolean enteredCave = false;
        boolean usedSword = false;
        boolean foundRiver = false;

        System.out.println("You are standing at the entrance of a dark cave.");

        System.out.print("Do you enter the dark cave or stay outside? (enter/stay): ");
        String choice1 = scanner.nextLine().toLowerCase();

        if (choice1.equals("enter")) {
            enteredCave = true;
            System.out.println("You step into the cave. It's dark and cold.");

            System.out.print("You find a sword. Do you want to use it or give it up and run? (use/give up): ");
            String choice2 = scanner.nextLine().toLowerCase();

            if (choice2.equals("use")) {
                usedSword = true;
                System.out.println("You use the sword and defeat a lurking animal.");

                System.out.print("Do you follow the river or climb a tree to look around? (river/tree): ");
                String choice3 = scanner.nextLine().toLowerCase();

                if (choice3.equals("river")) {
                    foundRiver = true;
                    System.out.println("You follow the river and find a path leading to safety. You are saved!");
                } else if (choice3.equals("tree")) {
                    System.out.println("You climb a tree and spot a village in the distance. You are saved!");
                }

            } else if (choice2.equals("give up")) {
                System.out.println("You leave the sword behind and run, feeling more lost.");

                System.out.print("Do you search for food or search for a way out? (food/way): ");
                String choice4 = scanner.nextLine().toLowerCase();

                if (choice4.equals("food")) {
                    System.out.println("A local offers you some food, helping you survive for a while.");
                    System.out.print("Do you search for food or call for help? (food/help): ");
                    String choice5 = scanner.nextLine().toLowerCase();
                    if (choice5.equals("food")) {
                        System.out.println("You find a river that leads you out of the forest. You are saved!");
                    } else if (choice5.equals("help")) {
                        System.out.println("Rescue teams hear your calls and come to save you. You are saved!");
                    }
                } else if (choice4.equals("way")) {
                    System.out.println("You find a map, but it’s outdated. Sadly, you die due to lack of food.");
                }
            }

        } else if (choice1.equals("stay")) {
            System.out.println("You decide to stay outside and are suddenly attacked by wild animals.");

            System.out.print("Do you fight back or try to escape? (fight/escape): ");
            String choice6 = scanner.nextLine().toLowerCase();

            if (choice6.equals("fight")) {
                System.out.println("You fight back and manage to escape, but you're injured.");

                System.out.print("Do you search for food or call for help? (food/help): ");
                String choice7 = scanner.nextLine().toLowerCase();

                if (choice7.equals("food")) {
                    foundRiver = true;
                    System.out.println("You find a river that leads you out of the forest. You are saved!");
                } else if (choice7.equals("help")) {
                    System.out.println("Rescue teams hear your calls and come to save you. You are saved!");
                }

            } else if (choice6.equals("escape")) {
                System.out.println("You try to escape but get lost in the wilderness.");

                System.out.print("Do you search for food or call for help? (food/help): ");
                String choice8 = scanner.nextLine().toLowerCase();

                if (choice8.equals("food")) {
                    foundRiver = true;
                    System.out.println("You find a river that leads you out of the forest. You are saved!");
                } else if (choice8.equals("help")) {
                    System.out.println("Rescue teams hear your calls and come to save you. You are saved!");
                }
            }
        } else {
            System.out.println("Invalid choice. The adventure ends here.");
        }

        scanner.close();
    }
}
