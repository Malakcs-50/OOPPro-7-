public class Coach extends Participant {

    private String specialty;

    public Coach(String name, String id, String specialty) {
        super(name, id);
        this.specialty = specialty;
    }

    @Override
    public void displayInfo() {
        System.out.println("Coach: " + name + " | Specialty: " + specialty);
    }
}
