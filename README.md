package module;

public class Robot {

    private String robotName;
    private String type;
    private int weight;
    private double batteryLevel;
    private double speed;
    private String status;
    private int totalScore;

    public Robot() {}

    public Robot(String robotName, String type, int weight,
                 double batteryLevel, double speed, String status) {

        this.robotName = robotName;
        this.type = type;
        this.weight = weight;
        this.batteryLevel = batteryLevel;
        this.speed = speed;
        this.status = status;
        this.totalScore = 0;
    }

    public String getRobotName() { return robotName; }
    public void setRobotName(String robotName) { this.robotName = robotName; }

    public String getType() { return type; }
    public void setType(String type) { this.type = type; }

    public int getWeight() { return weight; }
    public void setWeight(int weight) { this.weight = weight; }

    public double getBatteryLevel() { return batteryLevel; }
    public void setBatteryLevel(double batteryLevel) {
        if (batteryLevel >= 0 && batteryLevel <= 100)
            this.batteryLevel = batteryLevel;
    }

    public double getSpeed() { return speed; }
    public void setSpeed(double speed) { this.speed = speed; }

    public String getStatus() { return status; }
    public void setStatus(String status) { this.status = status; }

    public int getTotalScore() { return totalScore; }
    public void addScore(int score) { this.totalScore += score; }

    public void consumeBattery(double amount) {
        batteryLevel -= amount;
        if (batteryLevel < 0) batteryLevel = 0;
        if (batteryLevel == 0) status = "Offline";
    }


    public void Display_Info() {
        System.out.println("Robot: " + robotName +
                " | Battery: " + batteryLevel +
                "% | Status: " + status +
                " | Score: " + totalScore);
    }
}
