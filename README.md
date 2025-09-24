# STRING.JAVA


import java.util.Scanner;

public class StringDemo {
    /**
     * Main method - entry point of the program
     * Demonstrates basic string operations and user interaction
     * @param args command line arguments (not used)
     */
    public static void main(String[] args) {
        // Create Scanner object for reading user input from console
        Scanner sc = new Scanner(System.in);
        
   // ===== STRING INITIALIZATION =====
        // Initialize two strings using different methods
        String str1 = "hellow";           // String literal initialization
        String str2 = new String("java"); // String object initialization using constructor
        
  // ===== USER INPUT FOR SINGLE WORD =====
        // next() method reads a single word (stops at whitespace)
        System.out.println("enter the single word :");
        String word = sc.next();
        
  // Clear the input buffer to handle nextLine() properly
        // nextLine() after next() requires this to consume the remaining newline character
        sc.nextLine();
        
   // ===== USER INPUT FOR FULL SENTENCE =====
        // nextLine() method reads the entire line including spaces
        System.out.println("enter the full sentence :");
        String sentence = sc.nextLine();
        
   // ===== CHARACTER ACCESS OPERATIONS =====
        // charAt() method returns character at specified index (0-based indexing)
        System.out.println("first char of str1 :" + str1.charAt(0));
        
 // Access last character using length()-1 as index
        System.out.println("last char of str2 :" + str2.charAt(str2.length()-1));
        
  // ===== STRING LENGTH CALCULATION =====
        // length() method returns the number of characters in the string
        System.out.println("length of word :" + word.length());
        
  // ===== STRING CONCATENATION =====
        // Combine multiple strings using the + operator
        String newstr = str1 + " " + str2;
        System.out.println("concatenated string :" + newstr);
        
 // ===== CHARACTER-BY-CHARACTER TRAVERSAL =====
        // Loop through each character in the sentence and display them
        System.out.println("character at sentence :");
        
  // For loop to iterate through each character index
        for(int i = 0; i < sentence.length(); i++) {
            // Print each character followed by a space
            System.out.print(sentence.charAt(i) + " ");
        }
        
   // Close Scanner to free up system resources and prevent memory leaks
        sc.close();
    }
}
