import java.util.Scanner;

public class QuickSort {

    public static void quick_srt(int array[], int lo, int hi) {
        if (lo >= hi) {
            return; // Exit condition
        }

        int mid = array[(lo + hi) / 2];
        int i = lo, j = hi;

        while (i <= j) {
            // Move the low pointer until an element greater than or equal to mid is found
            while (array[i] < mid) {
                i++;
            }
            // Move the high pointer until an element less than or equal to mid is found
            while (array[j] > mid) {
                j--;
            }
            if (i <= j) {
                // Swap elements at i and j
                int temp = array[i];
                array[i] = array[j];
                array[j] = temp;
                i++;
                j--;
            }
        }

        if (lo < j) {
            quick_srt(array, lo, j);
        }
        if (i < hi) {
            quick_srt(array, i, hi);
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int array[] = new int[n];

        System.out.println("Enter the elements:");
        for (int i = 0; i < n; i++) {
            array[i] = sc.nextInt();
        }

        System.out.println("The elements before sorting are:");
        for (int i = 0; i < n; i++) {
            System.out.print(array[i] + " ");
        }
        System.out.println();

        quick_srt(array, 0, n - 1);

        System.out.println("The elements after sorting are:");
        for (int i = 0; i < n; i++) {
            System.out.print(array[i] + " ");
        }
        System.out.println();

        sc.close();
    }
}
