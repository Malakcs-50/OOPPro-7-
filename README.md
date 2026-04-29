import java.util.ArrayList;

public class ROBOSystem {

    private ArrayList<Team> teams = new ArrayList<>();
    private ArrayList<Coach> coaches = new ArrayList<>();
    private ArrayList<Robot> robots = new ArrayList<>();
    private ArrayList<Arena> arenas = new ArrayList<>();

    public void addTeam(Team t) {
        teams.add(t);
    }

    public void addCoach(Coach c) {
        coaches.add(c);
    }

    public void addRobot(Robot r) {
        robots.add(r);
    }

    public void addArena(Arena a) {
        arenas.add(a);
    }
}
    

