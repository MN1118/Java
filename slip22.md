1) Write a Java program to accept a number from user and print all prime numbers 
upto that number (Use Buffered Reader class).

```java 
import java.io.*; 
public class PrimeNumbers{ 
public static void main(String[] args)throws IOException{ 
BufferedReader br=new BufferedReader(new InputStreamReader(System.in)); 
System.out.print("Enter a number: "); 
int n=Integer.parseInt(br.readLine()); 
System.out.println("Prime numbers:"); 
for(int i=2;i<=n;i++){ 
int count=0; 
for(int j=1;j<=i;j++){ 
if(i%j==0) 
count++; 
} 
if(count==2) 
System.out.print(i+" "); 
} 
} 
} 
```

2) Write a java program to accept ‘N’ student names through command line, store 
them into the appropriate Collection and display them by using Iterator and 
ListIterator interface. 

```java 
import java.util.*; 
public class StudentNames{ 
public static void main(String[] args){ 
ArrayList<String> list=new ArrayList<>(); 
for(String name:args) 
list.add(name); 
System.out.println("Using Iterator:"); 
Iterator<String> i=list.iterator(); 
while(i.hasNext()) 
System.out.println(i.next()); 
System.out.println("Using ListIterator:"); 
ListIterator<String> li=list.listIterator(); 
while(li.hasNext()) 
System.out.println(li.next()); 
} 
} 
```
OR

2) ) Write a Java program to create LinkedList of String objects and perform the 
following: 

i. Add element at the end of the list.    
ii. Delete first element of the list.   
iii. Display the contents of list in reverse order.   

```java 
import java.util.*; 
public class LinkedListDemo{ 
public static void main(String[] args){ 
LinkedList<String> list=new LinkedList<>(); 
list.add("Apple"); 
list.add("Banana"); 
list.add("Mango"); 
list.addLast("Orange"); 
System.out.println("After adding at end: "+list); 
list.removeFirst(); 
System.out.println("After deleting first element: "+list); 
System.out.println("List in reverse order:"); 
Iterator<String> i=list.descendingIterator(); 
while(i.hasNext()) 
System.out.println(i.next()); 
} 
}
```