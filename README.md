# Student-management-systemm
import java.util.*;
class Student {
    int id;
    String name;
    double marks;
    Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }
    void display() {
        System.out.println(id + " " + name + " " + marks);
    }
}
public class StudentManagement {
    public static void main(String[] args) {
        ArrayList<Student> list = new ArrayList<>();
        list.add(new Student(1, "Ravi", 85.5));
        list.add(new Student(2, "Teja", 90.0));
        list.add(new Student(3, "Kumar", 78.0));
        System.out.println("Student Details:");
        for (Student s : list) {
            s.display();
        }
        Student top = list.get(0);
        for (Student s : list) {
            if (s.marks > top.marks) {
                top = s;
            }
        }

        System.out.println("\nTopper:");
        top.display();
    }
}
