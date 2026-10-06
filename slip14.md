1) Write a java program to accept names of ‘n’ cities, insert same into array list 
collection and display the contents of same array list, also remove all these 
elements. 

```java 

import java.util.Scanner; 
class NumberIsZeroException extends Exception{ 
NumberIsZeroException(String msg){ 
super(msg); 
} 
} 
public class PrimeDemo{ 
public static void main(String[] args){ 
Scanner sc=new Scanner(System.in); 
System.out.print("Enter a number: "); 
int n=sc.nextInt(); 
try{ 
if(n==0) 
throw new NumberIsZeroException("Number is 0"); 
boolean prime=true; 
if(n<2) 
prime=false; 
else{ 
for(int i=2;i<=n/2;i++){ 
if(n%i==0){ 
prime=false; 
break; 
} 
} 
} 
if(prime) 
System.out.println(n+" is Prime"); 
else 
System.out.println(n+" is Not Prime"); 
} 
catch(NumberIsZeroException e){ 
System.out.println(e.getMessage()); 
} 
} 
} 
```
2) Construct a linked List containing names of colours: red, blue, yellow and 
orange. Then extend your program to do the following: i. Display the contents of the 
List using an Iterator ii. Display the contents of the List in reverse order using a 
ListIterator iii. Create another list containing pink and green. Insert the elements of 
this list between blue and yellow. 

```java 

import java.util.*; 
public class ColorList{ 
public static void main(String[] args){ 
LinkedList<String> list=new LinkedList<String>(); 
list.add("red"); 
list.add("blue"); 
list.add("yellow"); 
list.add("orange"); 
           System.out.println("List using Iterator:"); 
           Iterator<String> i=list.iterator(); 
while(i.hasNext()) 
           System.out.println(i.next()); 
          System.out.println("List in reverse order:"); 
           ListIterator<String> li=list.listIterator(list.size()); 
while(li.hasPrevious()) 
               System.out.println(li.previous()); 
               LinkedList<String> list2=new LinkedList<String>(); 
list2.add("pink"); 
list2.add("green"); 
list.addAll(2,list2); 
                   System.out.println("List after inserting pink and green:"); 
Iterator<String> i2=list.iterator(); 
while(i2.hasNext()) 
                       System.out.println(i2.next()); 
} 
} 
```
OR 

2) Write a program to read the contents of “abc.txt” file, Display the contents of file 
in uppercase as output. 

```java 
Step 1: vim abc.txt 
Add text data in this txt file 
Step 2: vim FileUpper.java 
import java.io.*; 
public class FileUpper{ 
public static void main(String[] args){ 
try{ 
FileReader fr=new FileReader("abc.txt"); 
int ch; 
while((ch=fr.read())!=-1){ 
System.out.print(Character.toUpperCase((char)ch)); 
} 
fr.close(); 
} 
catch(IOException e){ 
System.out.println(e); 
} 
} 
}
```