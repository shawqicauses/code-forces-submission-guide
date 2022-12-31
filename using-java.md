# How to read from the console in Java

To read input from the console in Java for CodeForces, you can use the `Scanner` class from the `java.util` package. Here is an example of how to read integers and other values from the console:

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    // A. Read An Integer
    int number = scanner.nextInt();

    // B. Read Multiple Integers
    int firstNumber = scanner.nextInt();
    int secondNumber = scanner.nextInt();

    // C. Read A Line Of Text
    String line = scanner.nextLine();

    // D. Read Multiple Words
    String firstWord = scanner.next();
    String secondWord = scanner.next();

    // E. Read An Array
    int size = scanner.nextInt(); // E.1. Read Array's Size
    int[] array = new int[size]; // E.2. Create An Array

    // E.3 Read/Store Array's Elements
    for (int index = 0; index < size; index++) {
      array[index] = scanner.nextInt();
    }

    // F. Close Scanner
    scanner.close();
  }
}
```

P.S: You can use the `Scanner` class to read other data types, such as floating point numbers, booleans, and strings. You can find more information about the `Scanner` class in the Java documentation.

Also, ensure that your code follows the CodeForces submission guidelines and adheres to the specified time and memory limits for the problem. You can find more information about these guidelines in the [README](./README.md) page.

Try to solve [this problem](https://codeforces.com/problemset/problem/677/A) 😉🏆 Try not to cheat, but if you got stuck, here is our recommended solution:

```java
import java.util.Scanner;

public class VanyaAndFence {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int friendsSum = 0;
        int friendsHeight = 0;
        int friendsNumber = scanner.nextInt();
        int fenceHeight = scanner.nextInt();

        for (int index = 0; index < friendsNumber; index++) {
            friendsHeight = scanner.nextInt();
            if (friendsHeight > fenceHeight) friendsSum += 2;
            else friendsSum += 1;
        }

        System.out.println(friendsSum);
    }
}
```
