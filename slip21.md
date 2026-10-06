1)Write a java program to calculate area of Cylinder and Circle.(Use super 
keyword). 
```java
class Circle{ 
double r; 
Circle(double r){ 
this.r=r; 
} 
double area(){ 
return 3.142*r*r; 
} 
} 
class Cylinder extends Circle{ 
double h; 
Cylinder(double r,double h){ 
super(r); 
this.h=h; 
} 
double area(){ 
return 2*3.142*r*(r+h); 
} 
} 
public class AreaDemo{ 
public static void main(String[] args){ 
Circle c=new Circle(5); 
Cylinder cy=new Cylinder(5,10); 
System.out.println("Area of Circle: "+c.area()); 
System.out.println("Area of Cylinder: "+cy.area()); 
} 
}   
```

2) Write a Java Program which define class Product with data member as id, name 
and price Store the information of 5products and Display the name of product 
having minimum price(Use array of object).

```java 
class Product{ 
int id; 
String name; 
double price; 
Product(int id,String name,double price){ 
this.id=id; 
this.name=name; 
this.price=price; 
} 
} 
public class ProductDemo{ 
public static void main(String[] args){ 
Product[] p=new Product[5]; 
p[0]=new Product(1,"Laptop",55000); 
p[1]=new Product(2,"Mobile",20000); 
p[2]=new Product(3,"Tablet",15000); 
p[3]=new Product(4,"Keyboard",1200); 
p[4]=new Product(5,"Mouse",500); 
Product min=p[0]; 
for(int i=1;i<p.length;i++){ 
if(p[i].price<min.price) 
min=p[i]; 
} 
System.out.println("Product having minimum price: "+min.name); 
} 
} 
```
OR

2) Define an interface “Operation” which has methods area(),volume(). Define a 
constant PI having a value 3.142. Create a class circle (member – radius), cylinder 
(members – radius, height) which implements this interface. Calculate and display 
the area and volume.

```java 
interface Operation{ 
double PI=3.142; 
void area(); 
void volume(); 
} 
class Circle implements Operation{ 
double radius; 
Circle(double radius){ 
this.radius=radius; 
} 
public void area(){ 
System.out.println("Area of Circle: "+(PI*radius*radius)); 
} 
public void volume(){ 
System.out.println("Volume of Circle: "+(4.0/3.0*PI*radius*radius*radius)); 
} 
} 
class Cylinder implements Operation{ 
double radius,height; 
Cylinder(double radius,double height){ 
this.radius=radius; 
this.height=height; 
} 
public void area(){ 
System.out.println("Area of Cylinder: "+(2*PI*radius*(radius+height))); 
} 
public void volume(){ 
System.out.println("Volume of Cylinder: "+(PI*radius*radius*height)); 
} 
} 
public class OperationDemo{ 
public static void main(String[] args){ 
Circle c=new Circle(5); 
Cylinder cy=new Cylinder(5,10); 
c.area(); 
c.volume(); 
cy.area(); 
cy.volume(); 
} 
} 
```