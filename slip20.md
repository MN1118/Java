1) Write a Java program to accept a number using the BufferedReader class and 
generate the multiplication table of the given number. 

```java 
import java.io.*; 
public class MultiplicationTable{ 
public static void main(String[] args)throws IOException{ 
BufferedReader br=new BufferedReader(new InputStreamReader(System.in)); 
System.out.print("Enter a number: "); 
int n=Integer.parseInt(br.readLine()); 
for(int i=1;i<=10;i++) 
System.out.println(n+" x "+i+" = "+(n*i)); 
} 
}
```
2) Write a java program to show Multiple Threads Execution. 

```java 
class Thread1 extends Thread{ 
public void run(){ 
for(int i=1;i<=5;i++) 
System.out.println("Thread 1: "+i); 
} 
} 
class Thread2 extends Thread{ 
public void run(){ 
for(int i=1;i<=5;i++) 
System.out.println("Thread 2: "+i); 
} 
} 
class Thread3 extends Thread{ 
public void run(){ 
for(int i=1;i<=5;i++) 
System.out.println("Thread 3: "+i); 
} 
} 
public class MultipleThreads{ 
public static void main(String[] args){ 
Thread1 t1=new Thread1(); 
Thread2 t2=new Thread2(); 
Thread3 t3=new Thread3(); 
t1.start(); 
t2.start(); 
t3.start(); 
} 
} 
```

OR

2) Write a Java program to store city names and their STD codes using an 
appropriate collection and perform following operations: 

i. Add a new city and its code (No duplicates) .    
ii. Remove a city from the collection .   
iii. Search for a city name and display the code. 

```java 
import java.util.*; 
public class CityCode{ 
public static void main(String[] args){ 
TreeMap<String,Integer> map=new TreeMap<>(); 
map.put("Pune",20); 
map.put("Mumbai",22); 
map.put("Delhi",11); 
System.out.println("City and STD Code: "+map); 
if(!map.containsKey("Nagpur")) 
map.put("Nagpur",712); 
System.out.println("After adding: "+map); 
map.remove("Delhi"); 
System.out.println("After removing: "+map); 
String city="Pune"; 
if(map.containsKey(city)) 
System.out.println("STD Code: "+map.get(city)); 
else 
System.out.println("City not found"); 
} 
} 
```
