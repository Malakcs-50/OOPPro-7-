package module;

public class Coach extends StaffMember{
private String specialty;

    public Coach(int ID, String password, String firstName, String lastName, String email, int age) {
        super(ID, password, firstName, lastName, email, age);
    }

    public String getSpecialty() {
        return specialty;
    }

    public void setSpecialty(String specialty) {
        this.specialty = specialty;
    }

@Override
    public void Display_Info() {
        System.out.println("Coach: " + getFirstname() + " | Specialty: " + specialty);
    }

}
