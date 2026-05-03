public class Arena {
    private String name;
    private String location;

    private Arena(String name, String location) {
        this.name = name;
        this.location = location;
    }

    public void displayArena() {
        System.out.println("Arena: " + name + " | Location: " + location);
    }

    static Arena chooseArena() {
        int count = Team.getTeamCount();

        if (count == 4) {
            return new Arena("Main Arena", "Central Hall");
        } else if (count == 3) {
            return new Arena("West Arena", "West Wing");
        } else if (count == 2) {
            return new Arena("Room B", "Building B");
        } else {
            return new Arena("Room A", "Building A");
        }
        
    }

    
    
}
