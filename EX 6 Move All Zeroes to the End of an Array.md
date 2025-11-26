# EX 6 Move All Zeroes to the End of an Array

## AIM:
To write a Java program to move all zeroes in an array to the end while maintaining the order of non-zero elements.

## Algorithm
1. Start  
2. Read the size of the array N  
3. Read N elements into an array or list  
4. Create two lists: one for non-zero elements, one for zeroes  
5. Add all non-zero elements to the non-zero list, and 0s to the zero list  
6. Append zero list at the end of non-zero list  
7. Display the final array  
8. End
   

## Program:
```java
import java.util.*;

public class MoveZeroesToEnd {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        ArrayList<Integer> list = new ArrayList<>();
        ArrayList<Integer> zero = new ArrayList<>();

        int n = scan.nextInt();
        for(int i = 0; i < n; i++){
            int num = scan.nextInt();
            if(num != 0){
                list.add(num);
            }
            else{
                zero.add(0);
            }
        }
        
        Collections.sort(list);
        list.addAll(zero);
        System.out.println("Array after moving zeroes to end:");
        for(int i = 0; i < n; i++){
            System.out.print(list.get(i) + " ");
        }
    }
}
```

## Output:
<img width="694" height="142" alt="Screen Shot 1947-08-25 at 19 30 24" src="https://github.com/user-attachments/assets/9d27634c-09e9-4830-8dcb-b745eab07956" />


## Result:
Thus the Java program to move all zeroes to the end of an array while maintaining the order of non-zero elements is implemented successfully.

