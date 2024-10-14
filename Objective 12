import java.util.Scanner;

public class MergeSort {

    void merge(int arr[], int left, int mid, int right) {
        int n1 = mid - left + 1;
        int n2 = right - mid;

        int leftArray[] = new int[n1];
        int rightArray[] = new int[n2];

        for (int i = 0; i < n1; ++i)
            leftArray[i] = arr[left + i];
        for (int j = 0; j < n2; ++j)
            rightArray[j] = arr[mid + 1 + j];

        int i = 0, j = 0;
        int k = left;

        while (i < n1 && j < n2) {
            if (leftArray[i] <= rightArray[j]) {
                arr[k] = leftArray[i];
                i++;
            } else {
                arr[k] = rightArray[j];
                j++;
            }
            k++;
        }

        while (i < n1) {
            arr[k] = leftArray[i];
            i++;
            k++;
        }

        while (j < n2) {
            arr[k] = rightArray[j];
            j++;
            k++;
        }
    }

    void sort(int arr[], int left, int right) {
        if (left < right) {
            int mid = (left + right) / 2;

            // Sort first and second halves
            sort(arr, left, mid);
            sort(arr, mid + 1, right);

            // Merge the sorted halves
            merge(arr, left, mid, right);
        }
    }

    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);

        System.out.println("Enter number of integer elements: ");
        int n = scan.nextInt();

        int arr[] = new int[n];
        System.out.println("Enter " + n + " integer elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = scan.nextInt();
        }

        MergeSort mergeSort = new MergeSort();

        mergeSort.sort(arr, 0, n - 1);

        System.out.println("Elements after sorting:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
