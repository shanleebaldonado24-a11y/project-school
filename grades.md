
import java.util.*;

public class StudentGrades_icc {

    static Scanner console = new Scanner(System.in);
    static final int NUM_STUDENTS = 4;

    public static void main(String[] args) {
        int[] grades = new int[NUM_STUDENTS];
        int sum = 0;
        int highest = 0;
        int lowest = 100;

        System.out.println("========== STUDENT GRADES SYSTEM ==========");
        System.out.println("Enter grades for " + NUM_STUDENTS + " students:");
        System.out.println();

        for (int i = 0; i < NUM_STUDENTS; i++) {
            System.out.print("Enter grade for Student " + (i + 1) + ": ");
            grades[i] = console.nextInt();
            sum = sum + grades[i];
        }

        System.out.println("\n========== ALL GRADES ==========");

        for (int i = 0; i < NUM_STUDENTS; i++) {
            System.out.println("Student " + (i + 1) + ": " + grades[i]);
        }

        for (int i = 0; i < NUM_STUDENTS; i++) {
            if (grades[i] > highest) {
                highest = grades[i];
            }
            if (grades[i] < lowest) {
                lowest = grades[i];
            }
        }

        int average = sum / NUM_STUDENTS;

        System.out.println("\n========== GRADE STATISTICS ==========");
        System.out.printf("Average Grade: %d%n", average);
        System.out.printf("Highest Grade: %d%n", highest);
        System.out.printf("Lowest Grade: %d%n", lowest);
        System.out.printf("Total Sum: %d%n", sum);
    }
}
