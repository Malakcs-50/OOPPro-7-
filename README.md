package module;

public class Participant {
private int ID;
private int age;
private String firstname;
private String lastname;
private String email;
private String password;


public  Participant(){}

public Participant(int ID, String password, String firstName, String lastName, String email, int age){
    this.ID = ID;
    this.password = password;
    this.firstname = firstName;
    this.lastname = lastName;
    this.email = email;
    this.age = age;

}

    public Participant(String id, String password, String firstName, String lastName, String email, int age) {
    }

    public int getID(){
    return ID;
}

public int getAge(){
    return age;
}
public void setAge(int age){
    this.age=age;
}
public void setID(int ID){
    this.ID = ID;
}

public String getFirstname(){
    return firstname;
}

public void setFirstname(String firstname){
    this.firstname = firstname;
}
public String getLastname(){
    return lastname;
}

public void setLastname(String lastname){
    this.lastname = lastname;
}
 public String getEmail(){
    return email;
 }

 public void setEmail(String email){
    this.email = email;
 }
public String getPassword(){
    return password;
}
public void setPassword(String password){
    this.password = password;
}
public void Display_Info(){
    System.out.println("Participant: " + firstname + " " + lastname + " | ID: " + ID + " | Email: " + email);
}
}
