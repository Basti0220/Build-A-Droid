# Build-A-Droid

/*We’ve set up a robot workshop to build some droids. All that’s missing are the instructions on how to create the robots and what they’ll do.

Can we write a Java class to help?

We’ll need to define the state and behavior of the droids using instance fields and methods. Let’s get to work!*/

public class Droid{

  int batteryLevel;
  String name;

  public Droid(String droidName){
    name = droidName;
    batteryLevel = 100;
  }
  public String toString(){
    return "Hello, I'm the droid: " + name;
  }
  public void performTask(String task){
    System.out.println(name + " is performing task: " + task);
    batteryLevel -= 10;
  }
  public void energyReport(){
    System.out.println("The energy Level of: "  + name  + " is: " + batteryLevel);
  }
  public void energyTransfer(int Amount, Droid droName){
      batteryLevel -= Amount;
      droName.batteryLevel += Amount;
      
  }

    public static void main(String[] args){
        Droid codey = new Droid("Codey");
        Droid happy = new Droid("Happy");
        Droid sailor = new Droid("Sailor");
        System.out.println(codey);
        System.out.println(happy);
        System.out.println(sailor);
        codey.performTask("Turn on TV");
        codey.energyReport();
        codey.performTask("Turn off TV");
        codey.energyReport();
        codey.energyTransfer(20, happy);
        System.out.println(happy.batteryLevel);
        System.out.println(codey.batteryLevel);
    }

}
