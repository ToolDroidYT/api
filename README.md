### **Phase 1: Foundations of Java**

**Goal**: Understand basic programming concepts and Java syntax.

**1. Setup**
- Install **JDK (Java Development Kit)**.
- Install an IDE (e.g., **IntelliJ IDEA**, **Eclipse**, or **VS Code**).

**2. Learn Java Basics**
#### Topics to Cover:
- **Variables & Data Types**  
  Examples:  
  ```java
  int age = 25;
  float price = 19.99f;
  char grade = 'A';
  String name = "John Doe";
  ```
	
Data Types in Java:
1. Primitive Data Types: Examples: int, float, char, boolean.
2. Non-Primitive Data Types: Examples: Arrays, Strings, Classes.

Input/Output
Example using Scanner:
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello, " + name);
    }
}
```

Operators: Arithmetic, Relational, Logical.

Control Flow:
Examples: if-else, switch, loops (for, while, do-while).

Example:

#### For Loop
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}
```

#### While Loop
```java
int i = 0;
while (i < 5) {
    System.out.println("Iteration: " + i);
    i++;
}
```

#### Do-While Loop
```java
int i = 0;
do {
    System.out.println("Iteration: " + i);
    i++;
} while (i < 5);
```

### Control Flow Statements

#### If Statement
```java
int number = 10;
if (number > 0) {
    System.out.println("Number is positive.");
}
```

#### If-Else Statement
```java
int number = -10;
if (number > 0) {
    System.out.println("Number is positive.");
} else {
    System.out.println("Number is negative or zero.");
}
```

#### Switch Statement
```java
int day = 2;
switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Other day");
        break;
}
```

### Different Kinds of For Loops

#### For-Each Loop (Enhanced For Loop)
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int number : numbers) {
    System.out.println("Number: " + number);
}
```

#### For-Loop with Iterator
```java
import java.util.ArrayList;
import java.util.Iterator;

ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
list.add("Cherry");

for (Iterator<String> iterator = list.iterator(); iterator.hasNext();) {
    String fruit = iterator.next();
    System.out.println("Fruit: " + fruit);
}
```

3. Introduction to Object-Oriented Programming (OOP)

Classes and Objects
Example:
```java
class Dog {
    String name;
    int age;

    void bark() {
        System.out.println(name + " says Woof!");
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.name = "Buddy";
        dog.age = 3;
        dog.bark();
    }
}
```

Access Modifiers: public, private, protected.

4. Practice Simple Projects
- Build a calculator app.
- Create a grade calculator.

---

### **Phase 2: Dive into OOP Concepts**

**Goal**: Develop a solid understanding of OOP principles.

1. Core OOP Concepts

Encapsulation: Use getters and setters.

Inheritance:
Example:
```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}
```
```java
class Dog extends Animal {
    void bark() {
        System.out.println("This dog barks.");
    }
}
```

Polymorphism: Method overloading/overriding.

Abstraction: Abstract classes/interfaces.

2. Exception Handling
Example using try-catch:
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero!");
}
```

3. Practice Projects
- Employee Management System.
- Library Management System.

---

### **Phase 3: Java Core APIs**

**Goal**: Get comfortable with Java’s built-in libraries and APIs.

1. Data Structures in Java

Arrays and Collections Framework:
Example:
```java
import java.util.ArrayList;
public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        System.out.println(list);
    }
}
```

Stacks and Queues.

2. File Handling
Example:
```java
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (FileWriter writer = new FileWriter("output.txt")) {
            writer.write("Hello, File!");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```

3. Multi-threading
Example:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();
    }
}
```

---

### **Phase 4: Advanced Java Topics**

**Goal**: Build larger applications and explore frameworks.

1. Databases and JDBC
Example of connecting Java with MySQL:
```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;

public class Main {
    public static void main(String[] args) {
        try {
            Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydb", "user", "password");
            Statement stmt = conn.createStatement();
            stmt.executeUpdate("INSERT INTO users (name) VALUES ('John')");
            System.out.println("Inserted successfully");
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

2. Web Development with Java
- Learn basics of Servlets and JSP.
- Use Spring Boot for REST APIs.

---

### **Phase 5: Build and Deploy Real-World Applications**

**Goal**: Work on real-world projects to enhance your skills.

- Focus on solving challenges on platforms like LeetCode, HackerRank.
- Build projects and deploy them on platforms like AWS or Heroku.

---

### **Additional Resources**

**Books:**
- Head First Java by Kathy Sierra & Bert Bates.
- Effective Java by Joshua Bloch.

**Online Courses:**
- Udemy: Java Programming Masterclass.
- Coursera: Object-Oriented Programming in Java.