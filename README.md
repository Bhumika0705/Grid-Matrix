# Grid-Matrix
Grid Matrix in java
import java.util.Scanner;

public class Gridmtrix {
    public Gridmtrix() {
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Dimensions of Array:");
        int n = sc.nextInt();
        int[][] arr = new int[n][n];
        System.out.println("Enter elements of the Array:");

        int i;
        int j;
        for(i = 0; i < n; ++i) {
            for(j = 0; j < n; ++j) {
                arr[i][j] = sc.nextInt();
            }
        }

        for(i = 0; i < n; ++i) {
            for(j = 0; j < n; ++j) {
                if (i == j || i + j == n - 1) {
                    if (arr[i][j] == 0) {
                        System.out.println("False");
                        return;
                    }

                    if (arr[i][j] != 0) {
                        System.out.println("True");
                        return;
                    }
                }
            }
        }

        System.out.println();
    }
}
