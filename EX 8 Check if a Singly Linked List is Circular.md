# EX 8 Check if a Singly Linked List is Circular

## AIM:
To write a Java program to create a singly linked list and check whether it is circular.

## Algorithm
1. Start  
2. Read the number of nodes N  
3. Read N integers as node values  
4. Create a linked list from the input  
5. Make the last node point back to head (to simulate circular list)  
6. Traverse the list to check if it loops back to head  
7. Print true if circular, otherwise false  
8. End

## Program:
```java
import java.util.Scanner;

public class CheckCircularList {
    public static Node createList(Scanner scanner, int n) {
        if(n <= 0){
            return null;
        }
        Node head = new Node(scanner.nextInt());
        Node temp = head;
        
        for(int i = 1; i < n; i++){
            temp.next = new Node(scanner.nextInt());
            temp = temp.next;
        }
        temp.next = head; // Make the list circular
        return head;
    }

    public static boolean isCircular(Node head) {
       if(head == null){
           return false;
       }
       Node temp = head.next;
       while(temp != null && temp != head){
           temp = temp.next;
       }
       return head == temp;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();
        Node head = createList(scanner, n);
        boolean circular = isCircular(head);
        System.out.println(circular);
    }
}

class Node {
    int data;
    Node next;
    Node(int data) {
        this.data = data;
        this.next = null;
    }
}
```

 
## Output:
<img width="363" height="140" alt="Screen Shot 1947-08-25 at 19 35 46" src="https://github.com/user-attachments/assets/1ebf1713-2bcd-4df7-9e23-f3b86bec165a" />


## Result:
Thus the Java program to create a singly linked list and check if it is circular is implemented successfully.

