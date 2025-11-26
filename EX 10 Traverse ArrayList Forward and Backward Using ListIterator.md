# EX 10 Traverse ArrayList Forward and Backward Using ListIterator

## AIM:
To write a Java program to traverse an ArrayList in both forward and backward directions using a ListIterator.

## Algorithm
1. Start  
2. Read the number of names N  
3. Read N names and add them to an ArrayList<String>  
4. Obtain a ListIterator from the list  
5. Traverse the list forward and print each element  
6. Traverse the list backward and print each element  
7. End

## Program:
```java
import java.util.ArrayList;
import java.util.ListIterator;
import java.util.Scanner;

public class ListIteratorExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        ArrayList<String> list = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            list.add(sc.nextLine());
        }
        ListIterator<String> it = list.listIterator();
        while (it.hasNext()) {
            System.out.println(it.next());
        }
        while (it.hasPrevious()) {
            System.out.println(it.previous());
        }
    }
}
```

 
## Output:
<img width="346" height="419" alt="Screen Shot 1947-08-25 at 19 47 28" src="https://github.com/user-attachments/assets/024c55b6-a1b3-4572-bc2e-4381a4643e52" />



## Result:
Thus the Java program to traverse an ArrayList forward and backward using ListIterator is implemented successfully.

