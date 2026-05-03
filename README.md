public class Team extends Participant {
    private static int teamCount = 0;
    private String schoolName;
    private String student1;
    private String student2;
    private Score score;

    public Team(String teamName, String teamId, String schoolName,
                String student1, String student2) {

        super(teamName, teamId);
        this.schoolName = schoolName;
        this.student1 = student1;
        this.student2 = student2;
        this.score = new Score();
        teamCount++;
    }

    public static int getTeamCount() {
        return teamCount;
    }

    public Score getScore() {
        return score;
    }

    @Override
    public void displayInfo() {
        System.out.println("Team Name: " + name);
        System.out.println("Team ID: " + id);
        System.out.println("School: " + schoolName);
        System.out.println("Players:");
        System.out.println("- " + student1);
        System.out.println("- " + student2);
        score.displayScore();
    }
}
    

