import java.util.ArrayList;

public class Team extends Participant {

    private String schoolName;
    private ArrayList<String> students;

    public Team(String teamName, String teamId, String schoolName) {
        super(teamName, teamId);
        this.schoolName = schoolName;
        this.students = new ArrayList<>(); // مهم
    }

    public void addStudent(String studentName) {
        students.add(studentName);
    }

    @Override
    public void displayRole() {
        System.out.println("Team: " + name + " | School: " + schoolName);
        System.out.println("Members: " + students);
    }
}
    

