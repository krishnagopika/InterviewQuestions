1. There is a `Map` with keys as Restraunt names and values as an `ArrayList` of menu items and a user wants to order cream brule. Write a program to filter and return the Restaurant names that have cream brule in their menu?

2. There is `HashMap` with keys as Employee name and values as Employee contribution which is a number. Each employee contibution is evaluated once a month and new employees may be added at the start of the month. Write a program to print the leader board of empoyees and their contribution after 6 months.

3. The following code has a list of key and value pair of cards and the count, John is not sure if he added king of spades with count as 1, help john in adding the king of spades as count 1 to the deck,  Fill the empty lines to help John?

``` java
public class DeckOfCards {
    public static void main(String[] args) {
        // line 1
        Deck.put("Queen of Clubs", 1);
        Deck.put("Ace of Hearts",1);
        // line 2
    }
}

```

hint: remenber that a deck can not contain duplicate cards.

Ans: line 1: HashMap<String,Integer> Deck = new HashMap<>();
     line 2: Deck.put("King of Spades",1);

4. Cadbury wants to name their new choclate after the most common employee name in the company write a code to find out the most common name.

sol:

``` java

import java.util.*;

public class Election {
    public static void main(String[] args) {
        ArrayList<String> Names= new ArrayList<>();
        Names.add("aaa");
        Names.add("bbbb");
        Names.add( "aaa");
        TreeMap<String,Integer> NamesCount = new TreeMap<>();

        for( String i : Names){
            int frequency = Collections.frequency(Names,i);
            if(!NamesCount.containsValue(i))
            {
                NamesCount.put(i,frequency);
            }
        }
        

    }
}




```

5. Fill the empty lines in the given code to change all the list elements to "hello".

``` java

import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> Names= new ArrayList<>();
        Names.add("aaa");
        Names.add("bbbb");
        Names.add( "aaa");
        for( /*line 1*/)
        {
             // line 2   
                l.set("Hello");
        }
    }
}




```

Ans: 

- line 1: ListIterator<String> l = Names.listIterator(); l.hasNext(); 
- line 2: l.next(); 

6. Create a thread using lambda expression.

7. How to ignore case when sorting elements using `Treeset`?

ans: 

``` java
import java.util.*;

public class Main {

    /*
    code 
    */
   
    public static void main(String[] args) {
        TreeSet<String> words = new TreeSet<>(ignoreCase);
        words.add("AAAA");
        words.add("aaa");
        words.add("AAAA");
        words.add("aaa");
        words.add("AAAA");
        words.add("aaa");
        words.add("BBBB");
        words.add("bbb");
        for(String i: words)
        {
            System.out.println(i);
        }
    }
}

``` 
Ans: 

``` java

 static final Comparator<String> ignoreCase = new Comparator<String>() {
        @Override
        public int compare(String o1, String o2) {
            return o1.compareToIgnoreCase(o2);
        }
    };{

    }

``` 

8. How to create an object for Interface and Abstract Class?


9. Passesnger list is stored in the format of an object of Passenger with follwoung fields, there is a medical emergency, write a program to filterout the passengers with doctor as profession.

``` java

class Passenger{
    String firstName;
    String lastName;
    int age;
    String profession;
    String seatNo;

}

```





10. When is it possible to replace lambda expression with method reference?

11. How to create a method reference for constructor?

12. Is it possible to write a lambda expression withput ({})?

13. Is it mandatory to embend parameters of a lambda expression in ()?
    
14. Can you serealize a lambda expression?

15. When do we create a deafult method in an interface?

16. When do we create a static method in an interface?

17. Is it mandatory to override default methods of an Interface?

18. Declare an annotation type Book, with book name, author name, publishing data, genre as elemnts.

19. Is it possible to repeat an annotation? Justify your answer with an example.







  
