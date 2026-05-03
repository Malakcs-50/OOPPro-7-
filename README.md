Scanner input = new Scanner(System.in);

        System.out.println("Welcome to ROBO Competition System");
        System.out.println("**********************************");

        System.out.print("Enter number of teams: ");
        int numberOfTeams = input.nextInt();
        input.nextLine(); // clear buffer

        ArrayList<Team> teams = new ArrayList<>();
        ArrayList<Coach> coaches = new ArrayList<>();

        for (int i = 0; i < numberOfTeams; i++) {

            System.out.println("\n--- Team " + (i + 1) + " ---");

            System.out.print("Enter Team Name: ");
            String teamName = input.nextLine();

            System.out.print("Enter Team ID: ");
            String teamId = input.nextLine();

            System.out.print("Enter Coach Name: ");
            String coachName = input.nextLine();

            System.out.print("Enter Coach ID: ");
            String coachId = input.nextLine();

            System.out.print("Enter Coach Specialty: ");
            String specialty = input.nextLine();

            System.out.print("Enter First Player Name: ");
            String p1Name = input.nextLine();

            System.out.print("Enter First Player ID: ");
            String p1Id = input.nextLine();

            System.out.print("Enter Second Player Name: ");
            String p2Name = input.nextLine();

            System.out.print("Enter Second Player ID: ");
            String p2Id = input.nextLine();

            Team team = new Team(teamName, teamId,"School",  p1Name + " (ID: " + p1Id + ")",  p2Name + " (ID: " + p2Id + ")"
            );

            Coach coach = new Coach(coachName, coachId, specialty);

            teams.add(team);
            coaches.add(coach);
        }

        Arena arena = Arena.chooseArena();
        Round round = new Round(1);

        System.out.println("\n=================================");
        System.out.println("        COMPETITION DETAILS");
        System.out.println("=================================\n");

        System.out.println("Number of Teams: " + Team.getTeamCount());
        arena.displayArena();
        round.start(10);

        for (int i = 0; i < teams.size(); i++) {
            System.out.println("\n---------------------------------");
            teams.get(i).displayInfo();
            coaches.get(i).displayInfo();
        }

        System.out.println("\nCompetition Started Successfully ");
    }
}

