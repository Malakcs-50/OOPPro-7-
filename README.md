package module;

public class Judge extends Participant {
    private String category;
    private int certificationNumber;

    public Judge(int ID, String password, String firstname, String lastname, String email, int age, String category) {
        super(ID, password, firstname, lastname, email, age);
        this.category = category;
    }
    @Override
    public void Display_Info() {
        System.out.println("Judge: " + getFirstname() + " - Category: " + category);

    }
}
