public class Robot {
  
    private String model;
    private double weight;

    public Robot(String model, double weight) {
        this.model = model;
        this.weight = weight;
    }

    @Override
    public String toString() {
        return "Robot Model: " + model + " | Weight: " + weight + "kg";
    }
    
}
