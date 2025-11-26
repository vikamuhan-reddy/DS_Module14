# EX 9 Group Strings that are Anagrams

## AIM:
To write a Java program to group strings that are anagrams of each other and print each group.

## Algorithm
1. Start  
2. Read the number of strings N  
3. Read N strings from the user  
4. For each string, sort its characters to form a key  
5. Use a Map<String, List<String>> to group strings by their sorted character key  
6. Add each string to its corresponding group in the map  
7. Print all groups (words space-separated, each group on a new line)  
8. End

## Program:
```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        
        Map<String, List<String>> map = new HashMap<>();
        
        for(int i = 0; i < n; i++){
            String word = sc.nextLine().trim();
            char[] chars = word.toCharArray();
            Arrays.sort(chars);
            String key = new String(chars);
            map.computeIfAbsent(key, k -> new ArrayList<>()).add(word);
        }
        for(List<String> group : map.values()){
            System.out.println(String.join(" ", group));
        }
    }
}
```


## Output:
<img width="548" height="208" alt="Screen Shot 1947-08-25 at 19 41 56" src="https://github.com/user-attachments/assets/476d4f69-1c6f-48d2-95f5-ff29bff182e7" />


## Result:
Thus the Java program to group strings that are anagrams and print each group is implemented successfully.

