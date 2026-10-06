1) Define an Interface “Integer” with a abstract method check().Write a Java 
program to check whether a given number is Positive or Negative. 

```java 
interface Integer { 
    void check(); 
} 
class NumberCheck implements Integer { 
    int num; 
 
    NumberCheck(int num) { 
        this.num = num; 
    } 
 
    public void check() { 
        if (num > 0) 
            System.out.println(num + " is Positive"); 
        else if (num < 0) 
            System.out.println(num + " is Negative"); 
        else 
            System.out.println(num + " is Zero"); 
    } 
} 
 
public class PositiveNegative { 
    public static void main(String[] args) { 
        NumberCheck n = new NumberCheck(-10); 
        n.check(); 
    } 
} 
class Cylinder implements Operation { 
    double radius, height; 
    Cylinder(double radius, double height) { 
        this.radius = radius; 
        this.height = height; 
    } 
    public void area() { 
        System.out.println("Surface Area of Cylinder = " 
                + (2 * PI * radius * (radius + height))); 
    } 
    public void volume() { 
        System.out.println("Volume of Cylinder = " 
                + (PI * radius * radius * height)); 
    } 
} 
public class OperationDemo { 
    public static void main(String[] args) { 
        Circle c = new Circle(5); 
        c.area(); 
        c.volume(); 
       System.out.println(); 
 
        Cylinder cy = new Cylinder(3, 7); 
        cy.area(); 
        cy.volume(); 
    } 
} 
```
2) Write a java program to demonstrate Synchronization Example. 
```java 
class Table { 
    synchronized void printTable(int n) { 
        for (int i = 1; i <= 5; i++) { 
            System.out.println(n * i); 
 
            try { 
                Thread.sleep(400); 
            } catch (InterruptedException e) { 
                System.out.println(e); 
            } 
        } 
    } 
} 
 
class Thread1 extends Thread { 
    Table t; 
 
    Thread1(Table t) { 
        this.t = t; 
    } 
 
    public void run() { 
        t.printTable(5); 
    } 
} 
 
class Thread2 extends Thread { 
    Table t; 
 
    Thread2(Table t) { 
        this.t = t; 
    } 
 
    public void run() { 
        t.printTable(10); 
    } 
} 
 
public class SynchronizationDemo { 
    public static void main(String[] args) { 
 
        Table obj = new Table(); 
 
        Thread1 t1 = new Thread1(obj); 
        Thread2 t2 = new Thread2(obj); 
 
        t1.start(); 
        t2.start(); 
    } 
} 
```
OR

2) Write a program to create link list of integer objects. Do the following:  

i. Add element at first position.  
ii. Delete last element.  
iii. Display the size of link list.

```java 
import java.util.LinkedList; 
public class LinkedListDemo{ 
public static void main(String[] args){ 
LinkedList<Integer> list=new LinkedList<>(); 
list.add(10); 
list.add(20); 
list.add(30); 
list.add(40); 
System.out.println("Original LinkedList: "+list); 
list.addFirst(5); 
System.out.println("After adding at first position: "+list); 
list.removeLast(); 
System.out.println("After deleting last element: "+list); 
System.out.println("Size of LinkedList: "+list.size()); 
} 
}
```
