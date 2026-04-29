public class Round {

    private int roundNum;

    public Round(int roundNum) {
        this.roundNum = roundNum;
    }

    // Overloading
    public void start() {
        System.out.println("Round " + roundNum + " started.");
    }

    public void start(int time) {
        System.out.println("Round " + roundNum +
                " started. Duration: " + time + " minutes.");
    }
}
