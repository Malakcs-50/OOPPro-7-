public class Last {

    public static void main(String[] args) {
      
        Scanner input = new Scanner(System.in);

        System.out.println("Welcome to ROBO - Robot Competition System\n");

        ROBOSystem system = new ROBOSystem();

        // ===== Arenas =====
        Arena a1 = new Arena("Room C", "Building A");
        Arena a2 = new Arena("Room B", "Building B");
        Arena a3 = new Arena("West Arena", "West Zone");
        Arena a4 = new Arena("Main Arena", "Hall 1");

        system.addArena(a1);
        system.addArena(a2);
        system.addArena(a3);
        system.addArena(a4);

        // ===== Teams =====
        Team t1 = new Team("RoboMasters", "T1", "STEM School");
        t1.addStudent("Ahmed");
        t1.addStudent("Sara");

        Team t2 = new Team("TechBots", "T2", "Future School");
        t2.addStudent("Hassan");
        t2.addStudent("Mona");

        Team t3 = new Team("AlphaBots", "T3", "Modern School");
        t3.addStudent("Youssef");
        t3.addStudent("Nour");

        Team t4 = new Team("MegaBots", "T4", "Elite School");
        t4.addStudent("Omar");
        t4.addStudent("Laila");

        // ===== Coaches =====
        Coach c1 = new Coach("Mr. Ali", "C1", "Programming");
        Coach c2 = new Coach("Ms. Mona", "C2", "Mechanics");
        Coach c3 = new Coach("Eng. Samy", "C3", "AI");
        Coach c4 = new Coach("Dr. Hana", "C4", "Electronics");

        // ===== Robots =====
        Robot r1 = new Robot("X-Bot", 15);
        Robot r2 = new Robot("SpeedBot", 14);
        Robot r3 = new Robot("AlphaX", 16);
        Robot r4 = new Robot("MegaZ", 17);

        // ===== Round =====
        Round round = new Round(1);

        System.out.print("Enter your Team ID (T1 - T4): ");
        String id = input.nextLine();

        if (id.startsWith("T")) {
            switch (id) {

                case "T1":
                    t1.displayRole();
                    c1.displayRole();
                    System.out.println(r1);
                    a1.displayArena();
                    round.start(10);
                    break;

                case "T2":
                    t2.displayRole();
                    c2.displayRole();
                    System.out.println(r2);
                    a2.displayArena();
                    round.start(8);
                    break;

                case "T3":
                    t3.displayRole();
                    c3.displayRole();
                    System.out.println(r3);
                    a3.displayArena();
                    round.start(12);
                    break;

                case "T4":
                    t4.displayRole();
                    c4.displayRole();
                    System.out.println(r4);
                    a4.displayArena();
                    round.start(15);
                    break;

                default:
                    System.out.println("Team ID not found!");
            }
        } else {
            System.out.println("Invalid ID format.");
        }
    }
}
    
