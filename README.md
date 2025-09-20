# train-problem-code
//A train 150 m long passes a man walking at 5 km/h in 6 seconds. Find the speed of the train (in km/h)
public class TrainProblem {
    public static void main(String[] args) {
        double trainLength = 150; // in meters
        double time = 6;          // in seconds
        double manSpeed = 5;      // in km/h

        // Convert man's speed into m/s
        double manSpeedMS = (manSpeed * 1000) / 3600.0;

        // Speed of train relative to man = distance / time
        double relativeSpeed = trainLength / time;

        // Actual speed of train in m/s
        double trainSpeedMS = relativeSpeed + manSpeedMS;

        // Convert m/s to km/h
        double trainSpeedKMH = (trainSpeedMS * 3600) / 1000;

        System.out.println("Speed of train = " + trainSpeedKMH + " km/h");
    }
}
