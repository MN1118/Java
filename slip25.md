1) Write a Java program to reverse a number. Accept the number using command 
line arguments.

```java 
public class ReverseNumber{ 
public static void main(String[] args){ 
int n=Integer.parseInt(args[0]); 
int rev=0; 
while(n!=0){ 
rev=rev*10+n%10; 
n=n/10; 
} 
System.out.println("Reverse: "+rev); 
} 
}  
```
2) Write a package game which will have 2 classes Indoor & Outdoor. Use a function 
display() to generate the list of players for the specific game. Use default & 
parameterized constructor. 

```java 
Step 1: mkdir -p javaproject/game 
                 cd javaproject 
  
Step 2:vim package/Indoor.java 
package game; 
public class Indoor { 
    String game; 
    String[] players; 
    public Indoor() { 
        game = "Table Tennis"; 
        players = new String[]{"Rahul", "Amit", "Sneha", "Priya"}; 
    } 
    public Indoor(String game, String[] players) { 
        this.game = game; 
        this.players = players; 
    } 
    public void display() { 
        System.out.println("Indoor Game: " + game); 
        System.out.println("Players:"); 
        for (String player : players) { 
            System.out.println(player); 
        } 
    } 
} 
Step 3: vim package/Outdoor.java 
package game; 
public class Outdoor { 
    String game; 
    String[] players; 
    public Outdoor() { 
        game = "Cricket"; 
        players = new String[]{"Virat", "Rohit", "Rahul", "Hardik"}; 
    } 
     
    public Outdoor(String game, String[] players) { 
        this.game = game; 
        this.players = players; 
    } 
    public void display() { 
        System.out.println("Outdoor Game: " + game); 
        System.out.println("Players:"); 
        for (String player : players) { 
            System.out.println(player); 
        } 
    } 
} 
 
Step 4: vim mainprogram.java 
import game.Indoor; 
import game.Outdoor; 
 
public class mainprogram { 
    public static void main(String[] args) { 
        Indoor i1 = new Indoor(); 
        Outdoor o1 = new Outdoor(); 
 
        i1.display(); 
        System.out.println(); 
        o1.display(); 
        System.out.println(); 
        String[] indoorPlayers = {"Ajay", "Vijay"}; 
        String[] outdoorPlayers = {"Sachin", "Virat", "MS Dhoni"}; 
        Indoor i2 = new Indoor("Chess", indoorPlayers); 
        Outdoor o2 = new Outdoor("Football", outdoorPlayers); 
        i2.display(); 
        System.out.println(); 
        o2.display(); 
    } 
} 
Step5: javac game/Indoor.java game/outdoor.java mainprogram.java 
Step6: java mainprogram
```
OR

2) Write a Java program to create 2 files F1 and F2.Copy the contents of file F1 by 
changing the case into file F2.F2 = F1 Also copy the contents of F1 and F2 in F3.F3 = 
F1+F2 Display the contents of F3.

```java 
Step 1: vim F1 .txt 
Hello Java 
Welcome to Programming 
Step 2: vim F2.txt 
hELLO jAVA 
wELCOME TO pROGRAMMING 
 
Step 3: vim FileDemo.java 
import java.io.*; 
class FileDemo { 
    public static void main(String[] args) { 
        try { 
              FileWriter fw = new FileWriter("F1.txt"); 
            fw.write("Hello Java\nWelcome to Programming"); 
            fw.close(); 
            FileReader fr = new FileReader("F1.txt"); 
            FileWriter fw2 = new FileWriter("F2.txt"); 
 
            int ch; 
            while ((ch = fr.read()) != -1) { 
                if (Character.isUpperCase((char) ch)) 
                    fw2.write(Character.toLowerCase((char) ch)); 
                else if (Character.isLowerCase((char) ch)) 
                    fw2.write(Character.toUpperCase((char) ch)); 
                else 
                    fw2.write(ch); 
            } 
            fr.close(); 
            fw2.close(); 
            FileWriter fw3 = new FileWriter("F3.txt"); 
            fr = new FileReader("F1.txt"); 
            while ((ch = fr.read()) != -1) { 
                fw3.write(ch); 
            } 
            fr.close(); 
            fr = new FileReader("F2.txt"); 
            while ((ch = fr.read()) != -1) { 
                fw3.write(ch); 
            } 
            fr.close(); 
 
            fw3.close(); 
            FileReader fr3 = new FileReader("F3.txt"); 
            System.out.println("Contents of F3:"); 
            while ((ch = fr3.read()) != -1) { 
                System.out.print((char) ch); 
            } 
            fr3.close(); 
        } catch (IOException e) { 
            System.out.println("Error: " + e.getMessage()); 
        } 
    } 
}
```
