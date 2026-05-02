import module.*;

import java.util.ArrayList;
import java.util.Scanner;

        import java.util.*;

        public class Main {
        public static void main(String[] args) {

                Scanner input = new Scanner(System.in);

                // --- ARENA SETUP ---
                System.out.println("=== Competition Initial Setup ===");
                System.out.print("Enter Arena Name: ");
                String aName = input.nextLine();
                System.out.print("Enter Arena City: ");
                Arena competitionArena = new Arena(aName, input.nextLine());

                System.out.print("Enter number of teams: ");
                int numTeams = input.nextInt();
                input.nextLine();

                Team[] teams = new Team[numTeams];

                for (int i = 0; i < numTeams; i++) {
                        System.out.println("\n--- Team " + (i + 1) + " ---");

                        Team team = new Team();

                        System.out.print("Enter team name: ");
                        team.setTeamName(input.nextLine());

                        System.out.print("Enter robot name: ");
                        team.setRobot(input.nextLine());

                        System.out.print("Enter coach name: ");
                        team.setCoachAssigned(input.nextLine());

                        System.out.print("Enter number of participants: ");
                        int numParticipants = input.nextInt();
                        input.nextLine();

                        for (int j = 0; j < numParticipants; j++) {
                                System.out.println("\nParticipant " + (j + 1));

                                System.out.print("ID: ");
                                int id = input.nextInt();
                                input.nextLine();

                                System.out.print("First Name: ");
                                String fname = input.nextLine();

                                System.out.print("Last Name: ");
                                String lname = input.nextLine();

                                System.out.print("Email: ");
                                String email = input.nextLine();

                                System.out.print("Password: ");
                                String password = input.nextLine();

                                System.out.print("Age: ");
                                int age = input.nextInt();
                                input.nextLine();

                                Participant p = new Participant(id, password, fname, lname, email, age);
                                team.addMember(p);
                        }

                        teams[i] = team;
                }

                // 🔹 Simulate Rounds
                System.out.println("\n===== STARTING COMPETITION =====");

                for (int round = 1; round <= 3; round++) {
                        System.out.println("\n--- Round " + round + " (5 minutes) ---");

                        for (Team t : teams) {
                                int score = (int) (Math.random() * 100);
                                t.setCurrentScore(t.getCurrentScore() + score);

                                System.out.println(t.getTeamName() + " scored: " + score);
                        }

                        // Simulate 5 minutes (fast version)
        try {
        Thread.sleep(2000); // 2 sec instead of 5 min
        } catch (InterruptedException e) {
        e.printStackTrace();
        }
       }

                        // 🔹 Final Results
                        System.out.println("\n===== FINAL RESULTS =====");

                        for (Team t : teams) {
                                System.out.println(t.getTeamName() + " Total Score: " + t.getCurrentScore());
                                t.displayTeam();
                        }

                        input.close();
                }
        }
