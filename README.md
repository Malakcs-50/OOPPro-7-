package module;

public class Volunteer extends StaffMember{

    private String assignedTask;
    private String shiftTime;
    private String workLocation;

    public Volunteer(int ID, String password, String firstName, String lastName, String email, int age,String assignedTask, String shiftTime) {
        super(ID, password, firstName, lastName, email, age);
        this.assignedTask = assignedTask;
        this.shiftTime = shiftTime;
    }

    public String getAssignedTask() {
        return assignedTask;
    }

    public void setAssignedTask(String assignedTask) {
        this.assignedTask = assignedTask;
    }

    public String getShiftTime() {
        return shiftTime;
    }

    public void setShiftTime(String shiftTime) {
        this.shiftTime = shiftTime;
    }

    public String getWorkLocation() {
        return workLocation;
    }

    public void setWorkLocation(String workLocation) {
        this.workLocation = workLocation;
    }

    @Override
    public void Display_Info() {
        System.out.println("Volunteer: " + getFirstname() + " | Task: " + assignedTask +" - Working at: " + workLocation);
    }

}
