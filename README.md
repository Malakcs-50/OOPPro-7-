public class Robot {
    private String model;
    private double weight;

    private Robot(String model, double weight) {
        this.model = model;
        this.weight = weight;
    }

    // ✅ اختيار الروبوت حسب عدد التيمز
    public static Robot chooseRobot() {

        int count = Team.getTeamCount();

        if (count == 1) {
            return new Robot("Mini-Bot", 5);
        } else if (count == 2) {
            return new Robot("Small-Bot", 10);
        } else if (count == 3) {
            return new Robot("Medium-Bot", 15);
        } else {
            return new Robot("Mega-Bot", 25);
        }
    }

   
    public String getrobot() {
        return "Robot Model: " + model + " | Weight: " + weight + " kg";
    }
}

