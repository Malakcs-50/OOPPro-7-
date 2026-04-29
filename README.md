public class Arena {

    private String arenaName;
    private String location;

    public Arena(String arenaName, String location) {
        this.arenaName = arenaName;
        this.location = location;
    }

    public void displayArena() {
        System.out.println("Arena: " + arenaName + " | Location: " + location);
    }
}
