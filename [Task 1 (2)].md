import java.util.Scanner;

public class Main{

public static void main (String[]args){

    Scanner scanner= new Scanner(System.in);
    
    System.out.println("Enter a Sentence or Sequence: ");
    String input = scanner.nextLine();
    
    scanner.close();
    
    if(isPalindrome(input))
    System.out.println("The entered input is Palindrome...");
    
    else{
        System.out.println("The entered input is not a palindrome...");
    }
    
}

 public static boolean isPalindrome(String str){
     
     String cleaned=str.replaceAll("[^a-zA-Z0-9]"," ").toLowerCase();
     int left=0,right = cleaned.length()- 1;
     
     while(left<right){
         if(cleaned.charAt(left) != cleaned.charAt(right)){
             return false;
     }
     left++;
     right--;
 }
 return true;
 } 
}
