package module;

import java.util.ArrayList;

public class Team {

    private String teamName;
    private String coachAssigned ;
    private int currentScore;
    private String robot;

    private ArrayList<Participant> members = new ArrayList<>();

    //
    public void addMember(Participant p) {
        members.add(p);
    }

    public void displayTeam() {
        System.out.println("Team: " + teamName + " | Robot: " + robot +
                " | Score: " + currentScore);



        for (Participant p : members) {
            p.Display_Info();
        }
    }


    public String getTeamName() {
        return teamName;
    }

    public void setTeamName(String teamName) {
        this.teamName = teamName;
    }

    public String getCoachAssigned() {
        return coachAssigned;
    }

    public void setCoachAssigned(String coachAssigned) {
        this.coachAssigned = coachAssigned;
    }

    public int getCurrentScore() {
        return currentScore;
    }

    public void setCurrentScore(int currentScore) {
        this.currentScore = currentScore;
    }

    public String getRobot() {
        return robot;
    }

    public void setRobot(String robot) {
        this.robot = robot;
    }
}
