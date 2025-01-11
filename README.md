import java.util.Scanner;


public class StringOperationsEnhanced {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        // Input strings
        System.out.print("Enter the first string: ");
        String str1 = scanner.nextLine();
        System.out.print("Enter the second string: ");
        String str2 = scanner.nextLine();


        // Display menu for string operations
        System.out.println("\nChoose a string operation:");
        System.out.println("1. Find Length");
        System.out.println("2. Convert to Uppercase");
        System.out.println("3. Convert to Lowercase");
        System.out.println("4. Reverse the String");
        System.out.println("5. Concatenate Strings");
        System.out.println("6. Compare Strings");
        System.out.println("7. Check if Substring Exists");
        System.out.println("8. Replace a Character");
        System.out.println("9. Find Character at Index");
        System.out.println("10. Split the String");
        System.out.println("11. Trim Whitespaces");
        System.out.println("12. Check if String is Empty");
        System.out.println("13. Convert to Character Array");
        System.out.println("14. Exit");


        int choice;
        do {
            System.out.print("\nEnter your choice: ");
            choice = scanner.nextInt();
            scanner.nextLine(); // Consume newline


            switch (choice) {
                case 1:
                    System.out.println("Length of first string: " + str1.length());
                    System.out.println("Length of second string: " + str2.length());
                    break;


                case 2:
                    System.out.println("First string in uppercase: " + str1.toUpperCase());
                    System.out.println("Second string in uppercase: " + str2.toUpperCase());
                    break;


                case 3:
                    System.out.println("First string in lowercase: " + str1.toLowerCase());
                    System.out.println("Second string in lowercase: " + str2.toLowerCase());
                    break;


                case 4:
                 System.out.println("Reversed first string: " + new StringBuilder(str1).reverse());
                System.out.println("Reversed second string: " + new StringBuilder(str2).reverse());
                    break;


                case 5:
                    System.out.println("Concatenated string: " + str1.concat(str2));
                    break;


                case 6:
                    int comparison = str1.compareTo(str2);
                    if (comparison == 0) {
                        System.out.println("Strings are equal.");
                    } else if (comparison > 0) {
                        System.out.println("First string is lexicographically greater.");
                    } else {
                        System.out.println("Second string is lexicographically greater.");
                    }
                    break;


                case 7:
               System.out.print("Enter a substring to check in the first string: ");
               String substring = scanner.nextLine();
               System.out.println("Substring exists in the first string: " + str1.contains(substring));
                    break;


                case 8:
                    System.out.print("Enter the character to replace: ");
                    char oldChar = scanner.next().charAt(0);
                    System.out.print("Enter the new character: ");
                    char newChar = scanner.next().charAt(0);
       System.out.println("First string after replacement: " + str1.replace(oldChar, newChar));
      System.out.println("Second string after replacement: " + str2.replace(oldChar, newChar));
                    break;


                case 9:
                    System.out.print("Enter the index to find the character (0-based): ");
                    int index = scanner.nextInt();
                    try {
System.out.println("Character at index " + index + " in first string: " + str1.charAt(index));
System.out.println("Character at index " + index + " in second string: " + str2.charAt(index));
                    } catch (IndexOutOfBoundsException e) {
                        System.out.println("Index out of range!");
                    }
                    break;


                case 10:
                    System.out.print("Enter the delimiter to split the first string: ");
                    String delimiter = scanner.nextLine();
                    String[] parts = str1.split(delimiter);
                    System.out.println("First string split into parts:");
                    for (String part : parts) {
                        System.out.println(part);
                    }
                    break;


                case 11:
                    System.out.println("First string after trimming: [" + str1.trim() + "]");
                    System.out.println("Second string after trimming: [" + str2.trim() + "]");
                    break;


                case 12:
                    System.out.println("Is the first string empty? " + str1.isEmpty());
                    System.out.println("Is the second string empty? " + str2.isEmpty());
                    break;


                case 13:
                    System.out.println("Character array of first string:");
                    for (char c : str1.toCharArray()) {
                        System.out.print(c + " ");
                    }
                    System.out.println();
                    break;


                case 14:
                    System.out.println("Exiting...");
                    break;


                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 14);


        scanner.close();
    }
}


OUTPUT:
Enter the first string:
divya
Enter the second string:
dharika


Choose a string operations:
1.Find Length
2.Convert to Uppercase
3.Convert to Lowercase
4.Reverse the String
5.Concatenate Strings
6.Compare Strings
7.Check if Substring Exists
8.Replace a Character
9.Find Character at Index
10.Split the String
11.Trim Whitespaces
12.Check if String is Empty
13.Convert to Character Array
14.Exit


Enter your choice
4
Reversed first string:ayvid
Reversed second string:akirahd


Enter your choice
5
Concatenated string:divyadharika


27.ArrayExamples(1D,2D,Multidimensional)


CODING:
public class ArrayExamples {
    public static void main (String [] args) {
        // Single-dimensional array
        Int [] singleArray = {1, 2, 3, 4, 5};
        System.out.println("Single-dimensional array:");
        for (int i = 0; i < singleArray.length; i++) {
            System.out.print(singleArray[i] + " ");
        }
        System.out.println();


        // Two-dimensional array
        int[][] twoDimensionalArray = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        System.out.println("\nTwo-dimensional array:");
        for (int i = 0; i < twoDimensionalArray.length; i++) {
            for (int j = 0; j < twoDimensionalArray[i].length; j++) {
                System.out.print(twoDimensionalArray[i][j] + " ");
            }
            System.out.println();
        }


        // Multi-dimensional array (3D array)
        int[][][] multiDimensionalArray = {
            {
                {1, 2, 3},
                {4, 5, 6}
            },
            {
                {7, 8, 9},
                {10, 11, 12}
            }
        };
        System.out.println("\nMulti-dimensional array (3D):");
        for (int i = 0; i < multiDimensionalArray.length; i++) {
            for (int j = 0; j < multiDimensionalArray[i].length; j++) {
                for (int k = 0; k < multiDimensionalArray[i][j].length; k++) {
                    System.out.print(multiDimensionalArray[i][j][k] + " ");
                }
                System.out.println();
            }
            System.out.println();
        }
    }
}


OUTPUT:
Single-dimensional array:
1 2 3 4 5 


Two-dimensional array:
1 2 3 
4 5 6 
7 8 9 


Multi-dimensional array (3D):
1 2 3 
4 5 6 


7 8 9 
10 11 12


28. Sum of array


CODING:
public class SumOfArray {
    public static void main(String[] args) {
        int[] numbers = {5, 10, 15, 20, 25};
        int sum = 0;
        for (int num : numbers) {
            sum += num;
        }


        System.out.println("Sum of elements: " + sum);
    }
}


OUTPUT:
Sum of elements: 75


