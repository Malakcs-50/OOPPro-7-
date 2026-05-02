
package module;

public class StaffMember extends Participant{
    private int yearsOfExperience;
    public StaffMember(int ID, String password, String firstName, String lastName, String email, int age) {
        super(ID, password, firstName, lastName, email, age);
    }
    public int getYearsOfExperience(){
        return yearsOfExperience;
    }
    public void setYearsOfExperience(int yearsOfExperience){
        this.yearsOfExperience = yearsOfExperience;
    }

}
