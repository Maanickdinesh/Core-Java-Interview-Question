1. What is the difference between `==` and `.equals()` when comparing strings in Java?

   Answer: `==` compares object references, while `.equals()` compares the content of strings.
   
   Example:
   ```java
   String str1 = new String("Hello");
   String str2 = new String("Hello");
   System.out.println(str1 == str2);        // false (different objects)
   System.out.println(str1.equals(str2));   // true (same content)
   ```

2. How do you declare and initialize an array in Java?

   Answer: Arrays can be declared and initialized in several ways.
   
   Example:
   ```java
   int[] numbers = new int[5];              // Declare and allocate memory
   int[] primes = {2, 3, 5, 7, 11};         // Declare and initialize
   String[] names = new String[]{"Alice", "Bob", "Charlie"}; // Anonymous array
   ```

3. What is the purpose of the `final` keyword in Java?

   Answer: `final` can be used with variables, methods, and classes. For variables, it creates constants; for methods, it prevents overriding; for classes, it prevents inheritance.
   
   Example:
   ```java
   final int MAX_SIZE = 100;            // Constant variable
   public final void display() { ... }  // Cannot be overridden
   public final class Utility { ... }   // Cannot be inherited
   ```

4. Explain the difference between `public`, `private`, and `protected` access modifiers.

   Answer:
   - `public`: Accessible from any other class
   - `private`: Accessible only within the same class
   - `protected`: Accessible within the same package and by subclasses

   Example:
   ```java
   public class MyClass {
       public int publicVar;        // Accessible from anywhere
       private int privateVar;      // Accessible only in MyClass
       protected int protectedVar;  // Accessible in package and subclasses
   }
   ```

5. What is the syntax for creating a method that throws an exception?

   Answer: Use the `throws` keyword in the method declaration.
   
   Example:
   ```java
   public void readFile(String filename) throws IOException {
       // method implementation
   }
   ```

6. How do you define a constructor in Java?

   Answer: A constructor has the same name as the class and no return type.
   
   Example:
   ```java
   public class Person {
       private String name;
       
       public Person(String name) {
           this.name = name;
       }
   }
   ```

7. What is the difference between `break` and `continue` statements?

   Answer: `break` exits the loop entirely, while `continue` skips the rest of the current iteration and moves to the next.
   
   Example:
   ```java
   for (int i = 0; i < 5; i++) {
       if (i == 2) {
           continue;  // Skips printing 2
       }
       if (i == 4) {
           break;     // Stops the loop at 4
       }
       System.out.println(i);
   }
   // Output: 0 1 3
   ```

8. How do you create a multi-dimensional array in Java?

   Answer: Use multiple sets of square brackets.
   
   Example:
   ```java
   int[][] matrix = new int[3][3];
   int[][] jaggedArray = {{1, 2}, {3, 4, 5}, {6}};
   ```

9. What is the syntax for creating an anonymous inner class?

   Answer: Define and instantiate a class in a single expression.
   
   Example:
   ```java
   Runnable r = new Runnable() {
       @Override
       public void run() {
           System.out.println("Hello from anonymous class!");
       }
   };
   ```

10. How do you declare and use an enum in Java?

    Answer: Use the `enum` keyword to define a set of constants.
    
    Example:
    ```java
    public enum DaysOfWeek {
        MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
    }
    
    DaysOfWeek today = DaysOfWeek.MONDAY;
    ```

11. What is the difference between `static` and non-static methods?

    Answer: `static` methods belong to the class and can be called without creating an instance, while non-static methods require an instance of the class.
    
    Example:
    ```java
    public class MyClass {
        public static void staticMethod() {
            System.out.println("Static method");
        }
        
        public void nonStaticMethod() {
            System.out.println("Non-static method");
        }
    }
    
    MyClass.staticMethod();          // Correct
    MyClass obj = new MyClass();
    obj.nonStaticMethod();           // Correct
    ```

12. How do you implement a try-catch-finally block in Java?

    Answer: Use `try` to enclose the code that might throw an exception, `catch` to handle specific exceptions, and `finally` for code that should always execute.
    
    Example:
    ```java
    try {
        // Code that might throw an exception
        int result = 10 / 0;
    } catch (ArithmeticException e) {
        System.out.println("Division by zero!");
    } finally {
        System.out.println("This always executes");
    }
    ```

13. What is the syntax for creating a generic class in Java?

    Answer: Use angle brackets `<>` to specify the type parameter.
    
    Example:
    ```java
    public class Box<T> {
        private T content;
        
        public void set(T content) {
            this.content = content;
        }
        
        public T get() {
            return content;
        }
    }
    
    Box<Integer> intBox = new Box<>();
    ```

14. How do you declare and use a variable-length argument list (varargs) in a method?

    Answer: Use an ellipsis (`...`) after the type in the method parameter.
    
    Example:
    ```java
    public void printAll(String... args) {
        for (String arg : args) {
            System.out.println(arg);
        }
    }
    
    printAll("Hello", "World", "Java");
    ```

15. What is the purpose of the `super` keyword in Java?

    Answer: `super` is used to refer to the superclass (parent) of the current class. It can be used to call superclass methods and to access superclass constructors.
    
    Example:
    ```java
    class Animal {
        void makeSound() {
            System.out.println("Some sound");
        }
    }
    
    class Dog extends Animal {
        @Override
        void makeSound() {
            super.makeSound();  // Calls Animal's makeSound()
            System.out.println("Bark");
        }
    }
    ```

16. How do you create and use a lambda expression in Java?

    Answer: Lambda expressions provide a concise way to express instances of single-method interfaces (functional interfaces).
    
    Example:
    ```java
    Runnable r = () -> System.out.println("Hello, Lambda!");
    
    List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
    numbers.forEach(n -> System.out.println(n));
    ```

17. What is the syntax for creating a functional interface?

    Answer: A functional interface is an interface with exactly one abstract method. Use the `@FunctionalInterface` annotation.
    
    Example:
    ```java
    @FunctionalInterface
    public interface Converter<F, T> {
        T convert(F from);
    }
    
    Converter<String, Integer> stringToInt = (from) -> Integer.valueOf(from);
    Integer converted = stringToInt.convert("123");
    ```

18. How do you use the diamond operator (`<>`) in Java?

    Answer: The diamond operator allows type inference for generic class instances.
    
    Example:
    ```java
    List<String> list = new ArrayList<>();  // Instead of new ArrayList<String>()
    Map<String, List<String>> map = new HashMap<>();
    ```

19. What is the purpose of the `default` keyword in interface methods?

    Answer: `default` methods in interfaces provide a default implementation for methods, allowing interfaces to be extended without breaking existing implementations.
    
    Example:
    ```java
    public interface Vehicle {
        void start();
        
        default void horn() {
            System.out.println("Beep beep!");
        }
    }
    ```

20. How do you use the `instanceof` operator in Java?

    Answer: `instanceof` is used to test whether an object is an instance of a specific class or interface.
    
    Example:
    ```java
    Object obj = "Hello";
    if (obj instanceof String) {
        String str = (String) obj;
        System.out.println(str.length());
    }
    ```

