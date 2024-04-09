## HackerRank-solutions
> ### Java Abstract Class | HackerRank
> A Java abstract class is a class that can't be instantiated.
> That means you cannot create new instances of an abstract class.
> It works as a base for subclasses.
> You should learn about Java Inheritance before attempting this challenge.

Following is an example of abstract class:
> abstract class Book{
>  String title;
>   abstract void setTitle(String s);
>   String getTitle(){
>       return title;
>   }
> }

```
import java.util.Scanner;
import java.util.regex.*;

public class Solution
{
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int testCases = Integer.parseInt(in.nextLine());
        while(testCases>0){
            String pattern = in.nextLine();


            try{
                Pattern.compile(pattern);
                System.out.println("Valid");

            } catch(Exception e){
                System.out.println("Invalid");
            }
        }
        in.close();
    }

}


```


Follow me on **[HackerRank](https://www.hackerrank.com/profile/bynk_verified)**.
