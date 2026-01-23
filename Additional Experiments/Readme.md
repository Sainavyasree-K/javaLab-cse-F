## Additional Experiments
## TITLE:1) Program to insert sub string into a main string from a given position.
```
import java.util.Scanner;

public class InsertSubstring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input main string
        System.out.print("Enter the main string: ");
        String mainString = sc.nextLine();

        // Input substring
        System.out.print("Enter the substring to insert: ");
        String subString = sc.nextLine();

        // Input position
        System.out.print("Enter the position to insert the substring: ");
        int position = sc.nextInt();

        // Check valid position
        if (position < 0 || position > mainString.length()) {
            System.out.println("Invalid position!");
        } else {
            // Extract parts of the main string
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);

            // Insert substring
            String resultString = firstPart + subString + secondPart;

            // Display result
            System.out.println("Resulting string: " + resultString);
        }

        sc.close();
    }
}
```
## output
![output of screenshot](add_1.output.jpeg)
## TITLE:3) Program to determine if a given string is palindrome or not.
```
import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input string
        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        // Initialize pointers
        int start = 0;
        int end = str.length() - 1;

        boolean isPalindrome = true;

        // Compare characters from both ends
        while (start < end) {
            if (str.charAt(start) != str.charAt(end)) {
                isPalindrome = false;
                break;
            }
            start++;
            end--;
        }

        // Display result
        if (isPalindrome) {
            System.out.println("String is a palindrome");
        } else {
            System.out.println("String is not a palindrome");
        }

        sc.close();
    }
}
```
## output
![output of screenshot](add_3.output.jpeg)
