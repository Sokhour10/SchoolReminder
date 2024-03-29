**School Payment Reminder System**

*Introduction
The School Payment Reminder System simplifies payment management for university administrators. It maintains student records, tracks payment information (invoices), and generates automated reminders to notify students about pending fees. This project embraces key Object-Oriented Programming (OOP) concepts to provide a robust and adaptable structure.

Object-Oriented Programming Concepts
1. Inheritance
The User class serves as the Super class for Student and Admin classes, allowing them to inherit common features such as username and password.

2. Encapsulation
2.1 Public Access Modifier:
In the User class:
    The displayUserMenu() method is marked as public static, allowing other classes to access the user menu utility method.
In the Admin class:
    The displayAdminMenu() method is marked as public static, providing public access to the admin menu utility method.
2.2 Private Access Modifier:
In the User class:
    The password field is marked as private, ensuring that it can only be accessed within the same class.
    The changePassword() method accesses the password field directly since it is within the same class.
In the Student class:
    The setPassword() method is marked as private, restricting access to setting the password only from within the Student class.
2.3 Protected Access Modifier
    In the User class:
    The username field is marked as protected, allowing subclasses like Student to access it directly.
2.4  Default (Package-Private) Access Modifier:
    In the User class:
        The constructor and methods without any access modifier are using the default access, limiting access to classes within the same package.
    In the Student class:
        The default constructor (Student(String username, String password)) is package-private, allowing only classes within the same package to instantiate a student with a username and password.
3. Polymorphism
 Which is defined as abstract in the base User class and implemented differently in the Student and Admin subclasses.
+Method Overloading
-The Student class contains overloaded constructors. Both constructors have the same name (Student), but they differ in the number and types of parameters they accept. This is an example of method overloading.
+ Method Overriding:
The User class contains overridden methods:
User Class:
-public void changePassword() is overridden in the Student and Admin classes. The Student class provides a specific implementation for changing the student's password, and the Admin class does the same for an admin.
-public String toString() is overridden in the Student class to provide a custom string representation of a student.
-public boolean equals(Object obj) is overridden in the Student class to compare the equality of student objects.
Student Class:
The Student class overrides the following methods:
-public String toString(): This method overrides the toString() method in the User class, providing a custom string representation that includes specific information about a student.
-public boolean equals(Object obj): This method overrides the equals() method in the User class, comparing additional properties specific to a student.

4. Abstraction
In user class we use abtract classs and abtract metthod call  getUserType.
Abstract methods like getUserType() provide a blueprint for subclasses, ensuring a standardized structure across different user types.The purpose is to let subclasses specify the type of user they represen

5. Interfaces
Interfaces (ChangeMajorOperation) define specific operations. So, ChangeMajorOperation is implemented in the Student class, allowing the change of a student's major.

6. Anonymous Class
Anonymous classes are used when creating instances of classes with unique implementations . In this project, an anonymous class is used during student registration to create a custom User instance.

7. Exception Handling
Wrong Input Handling:
The system handles various wrong inputs using exception handling. For instance, in the user login process, incorrect inputs (like invalid usernames or passwords) are managed to prevent system crashes and provide user-friendly error messages.

8. File I/O Operations
Storage of Information
User, Admin, and Invoice Info Files:
Three separate files are used to store distinct types of information:
-User Info File: Stores authentication-related data for users.
-Admin Info File: Contains specific information related to administrators.
-Invoice Info File: Stores details regarding invoices, including payment-related information.
+ Static methods
 - Use static method in the User class dispay menu for student to choose the option. That can not change the information and in invoice class we Reads invoice information from a file, processes it, and prints each line.

+Project Structure
-User Package
User Class: Base class with common properties (username and password). Implements methods like toString() and equals().
Student Class: Subclass of User representing a student. Implements the ChangeMajorOperation interface and provides additional properties such as gender and major.
-Invoice Package
Invoice Class: Manages invoice details, including charges. Provides methods for setting charges, calculating total amounts, and viewing invoices.

Conclusion
By incorporating OOP principles, this project achieves a modular, extensible, and maintainable design. Inheritance, encapsulation, polymorphism, abstraction, interfaces, and anonymous classes contribute to the effectiveness of the School Payment Reminder System.




