import java.util.Scanner;

public class bubbleSort {

    public static void bubble_srt(int[] arr) {
        int n = arr.length;
        int t = 0;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 1; j < n - i; j++) {
                if (arr[j - 1] > arr[j]) {
                    t = arr[j - 1];
                    arr[j - 1] = arr[j];
                    arr[j] = t;
                }
            }
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the number of elements:");
        int n = scanner.nextInt();
        int[] array = new int[n];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }

        System.out.println("The elements before sorting are:");
        for (int i : array) {
            System.out.print(i + " ");
        }
        System.out.println();

        bubble_srt(array);

        System.out.println("The elements after sorting are:");
        for (int i : array) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}
