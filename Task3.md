Task 3: OOP with Classes
Create a Java program demonstrating classes, inheritance, and method overriding.


// Base class
class Student {
    String name;
    int rollNo;

    public Student(String name, int rollNo) {
        this.name = name;
        this.rollNo = rollNo;
    }

    public void displayInfo() {
        System.out.println("Student Name: " + name);
        System.out.println("Roll Number: " + rollNo);
    }
}

// Subclass
class GraduateStudent extends Student {
    String thesisTopic;

    public GraduateStudent(String name, int rollNo, String thesisTopic) {
        super(name, rollNo); // Call parent class constructor
        this.thesisTopic = thesisTopic;
    }

    // Overriding the displayInfo method
    @Override
    public void displayInfo() {
        super.displayInfo(); // Optionally call the superclass version
        System.out.println("Thesis Topic: " + thesisTopic);
    }
}

// Main class to run the program
public class StudentDemo {
    public static void main(String[] args) {
        Student student1 = new Student("Alice", 101);
        GraduateStudent gradStudent1 = new GraduateStudent("Bob", 202, "Artificial Intelligence");

        System.out.println("== Undergraduate Student ==");
        student1.displayInfo();

        System.out.println("\n== Graduate Student ==");
        gradStudent1.displayInfo();
    }
}

== Undergraduate Student ==
Student Name: Alice
Roll Number: 101

== Graduate Student ==
Student Name: Bob
Roll Number: 202
Thesis Topic: Artificial Intelligence
