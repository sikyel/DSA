import java.util.Scanner;

public class LinearSearch {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = in.nextInt();

        int[] array = new int[n];

        System.out.println("Enter " + n + " integers:");
        for (int i = 0; i < n; i++) {
            array[i] = in.nextInt();
        }

        System.out.print("Enter value to find: ");
        int search = in.nextInt();

        boolean found = false;
        for (int c = 0; c < n; c++) {
            if (array[c] == search) {
                System.out.println(search + " is present at location " + (c + 1));
                found = true;
                break;
            }
        }

        if (!found) {
            System.out.println(search + " isn't present in the array.");
        }

        in.close();
    }
}
