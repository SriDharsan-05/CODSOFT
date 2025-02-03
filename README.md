import java.util.Scanner;


public class Main {
    public static void main(String[] args) {
    
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter Temperature: ");
        double temperature = scanner.nextDouble();
        
        System.out.println("C for Celsius and F for Fahrenheit : ");
        char unit= scanner.next().toUpperCase().charAt(0);

        if(unit=='C'){
            double fahrenheit= (temperature*9/5)+32;
            System.out.println("The temperature is : "+fahrenheit+" °C");
        }
        else if(unit=='F'){
            double celsius=(temperature-32)*5/9;
            System.out.println("The tempearture is : "+celsius+"°F");
        }
        else{
            System.out.println("Invlaid Input!!!Verify Input!!!");
        }
        scanner.close();
    }
}
