# EX 7 Calculate the Length of a Singly Linked List

## AIM:
To write a Java program to calculate and print the length of a singly linked list.

## Algorithm
1. Start  
2. Read the number of nodes N  
3. Read N integers as node values  
4. Create a linked list with these nodes  
5. Traverse the linked list and count the nodes  
6. Print the length of the linked list  
7. End

## Program:
```java
import java.util.Scanner;

public class LinkedListLength {
    public static int getLength(ListNode head) {
        int n = 0;
        ListNode temp = head;
        while(temp != null){
            temp = temp.next;
            n++;
        }
        return n;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        if (!scanner.hasNextInt()) {
            System.out.println(0);
            return;
        }
        int n = scanner.nextInt();
        if (n <= 0) {
            System.out.println(0);
            return;
        }
        ListNode head = new ListNode(scanner.nextInt());
        ListNode current = head;
        for (int i = 1; i < n; i++) {
            if (scanner.hasNextInt()) {
                current.next = new ListNode(scanner.nextInt());
                current = current.next;
            }
        }
        int length = getLength(head);
        System.out.println(length);
    }
}

class ListNode {
    int data;
    ListNode next;
    ListNode(int data) {
        this.data = data;
        this.next = null;
    }
}
```

## Output:
<img width="402" height="140" alt="Screen Shot 1947-08-25 at 19 32 38" src="https://github.com/user-attachments/assets/1cd9973c-e72c-4868-861f-8131e2b24636" />


## Result:
Thus the Java program to calculate the length of a singly linked list is implemented successfully.

