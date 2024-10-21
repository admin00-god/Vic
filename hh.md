import java.util.Scanner;

public class Fivehoursstraight {
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        
        System.out.print("Enter the number of rows:\t");
        int ROW = input.nextInt();
        System.out.print("Enter the number of columns:\t");
        int COL = input.nextInt();
        String[][] elements = new String[ROW][COL];
        
        for(int i = 0; i < ROW; i++) {
            for(int n = 0; n < COL; n++) {
                System.out.print("Enter element at Index[" + i + "]:\t");
                elements[i][n] = input.next();
            }
        }
        
        System.out.println("\nInput Array:");
        for(int i = 0; i < ROW; i++) {
            for(int n = 0; n < COL; n++) {
                System.out.print(elements[i][n] + "\t");
            }
            System.out.println();
        }
        
        System.out.print("Enter the item to search for:\t");
        String itemToSearch = input.next();


        for(int i = 0; i < ROW; i++) {
            for(int n = 0; n < COL; n++) {
                if(elements[i][n].equals(itemToSearch)) {
                    System.out.println("Item found in Row No." + (i + 1) + " on Column No. " + (n + 1));
                }
            } 
        }
    }
}
