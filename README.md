public abstract class Participant {

    protected String name;
    protected String id;

    public Participant(String name, String id) {
        this.name = name;
        this.id = id;
    }

    public abstract void displayRole();
}
