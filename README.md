public class Score {
    

    private int points;

    public Score() {
        points = 0;
    }

    public void addPoints(int value) {
        points += value;
    }

    public int getPoints() {
        return points;
    }

    public void displayScore() {
        System.out.println("Score: " + points + " points");
    }
}

    

