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
Arithmetic, Relational, and Logical Operators in Java

1. Arithmetic Operators

Arithmetic operators are used to perform basic mathematical operations.

Example Code:

```java
public class ArithmeticExample {
    public static void main(String[] args) {
        int a = 10, b = 5;

        System.out.println("Addition: " + (a + b));       // 15
        System.out.println("Subtraction: " + (a - b));    // 5
        System.out.println("Multiplication: " + (a * b)); // 50
        System.out.println("Division: " + (a / b));       // 2
        System.out.println("Modulus: " + (a % b));        // 0
    }
}
```

---

2. Relational (Comparison) Operators

Relational operators are used to compare two values. The result is always a boolean (true or false).

Example Code:

```java
public class RelationalExample {
    public static void main(String[] args) {
        int x = 10, y = 5;

        System.out.println("Equal to: " + (x == y));       // false
        System.out.println("Not equal to: " + (x != y));   // true
        System.out.println("Greater than: " + (x > y));    // true
        System.out.println("Less than: " + (x < y));       // false
        System.out.println("Greater than or equal to: " + (x >= y)); // true
        System.out.println("Less than or equal to: " + (x <= y));    // false
    }
}
```

---

3. Logical Operators

Logical operators are used to combine two or more conditions. The result is always a boolean (true or false).

Truth Table for && (AND): | Condition 1 | Condition 2 | Result | |-------------|-------------|--------| | true      | true      | true | | true      | false     | false| | false     | true      | false| | false     | false     | false|

Truth Table for || (OR): | Condition 1 | Condition 2 | Result | |-------------|-------------|--------| | true      | true      | true | | true      | false     | true | | false     | true      | true | | false     | false     | false|

Example Code:

```java
public class LogicalExample {
    public static void main(String[] args) {
        int a = 10, b = 5;

        System.out.println("Logical AND: " + ((a > 5) && (b < 10))); // true
        System.out.println("Logical OR: " + ((a < 5) || (b < 10)));  // true
        System.out.println("Logical NOT: " + !(a > 5));              // false
    }
}
```

---

4. Combining Operators

You can combine these operators to create complex conditions.

Example:

```java
public class CombinedOperatorsExample {
    public static void main(String[] args) {
        int x = 10, y = 5, z = 20;

        // Check if x is greater than y AND less than z
        if ((x > y) && (x < z)) {
            System.out.println("x is between y and z.");
        }

        // Check if x is either less than y OR greater than z
        if ((x < y) || (x > z)) {
            System.out.println("x is out of the range.");
        }

        // Negate a condition
        if (!(x == z)) {
            System.out.println("x is not equal to z.");
        }
    }
}
```

Output:

```
x is between y and z.
x is not equal to z.
```

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