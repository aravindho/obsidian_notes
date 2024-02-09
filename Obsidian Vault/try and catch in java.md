/*try 
catch
throw
throws
exception
finally */*

[[java check list]]

try {
    // Code that might throw an exception
} catch (ExceptionType e) {
    // Code to handle the exception
} finally {
    // Optional block that always executes, whether an exception is thrown or not
}

//always in catch(Exception e) is last before any specification error 
public class ExceptionHandlingExample {
    public static void main(String[] args) {
        try {
            // Code that might throw an exception
            int result = divide(10, 0);
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            // Code to handle the ArithmeticException
            System.out.println("Arithmetic Error: " + e.getMessage());
        } catch (NullPointerException e) {
            // Code to handle the NullPointerException
            System.out.println("Null Pointer Error: " + e.getMessage());
        } catch (Exception e) {
            // Generic catch block for any other exception
            System.out.println("An unexpected error occurred: " + e.getMessage());
        } finally {
            // Optional block that always executes
            System.out.println("Finally block executed");
        }
    }

    static int divide(int a, int b) {
        if (b == 0) {
            // Throwing an ArithmeticException
            throw new ArithmeticException("Cannot divide by zero");
        }
        return a / b;
    }
}



throw
// `throw` statement in Java is used to explicitly throw an exception. It is //often used in situations where you want to signal that an error or //exceptional condition has occurred.

1. public class TestThrow1 {   
2.     //function to check if person is eligible to vote or not   
3.     public static void validate(int age) {  
4.         if(age<18) {  
5.             //throw Arithmetic exception if not eligible to vote  
6.             throw new ArithmeticException("Person is not eligible to vote");    
7.         }  
8.         else {  
9.             System.out.println("Person is eligible to vote!!");  
10.         }  
11.     }  
12.     //main method  
13.     public static void main(String args[]){  
14.         //calling the function  
15.         validate(13);  
16.         System.out.println("rest of the code...");    
17.   }    
18. }
//every throw catch is neccessary

`class` `ThrowExcep {`

    `static` `void` `fun()`

    `{`

        `try` `{`

            `throw` `new` `NullPointerException(``"demo"``);`

        `}`

        `catch` `(NullPointerException e) {`

            `System.out.println(``"Caught inside fun()."``);`

            `throw` `e;` `// rethrowing the exception`

        `}`

    `}`

    `public` `static` `void` `main(String args[])`

    `{`

        `try` `{`

            `fun();`

        `}`

        `catch` `(NullPointerException e) {`

            `System.out.println(``"Caught in main."``);`

        `}`

    `}`

`}`


//**Java throws**

%% throws is a keyword in Java that is used in the signature of a method to indicate that this method might throw one of the listed type exceptions. The caller to these methods has to handle the exception using a try-catch block %%



`class` `ThrowsExecp {`

    `static` `void` `fun()` `throws` `IllegalAccessException`

    `{`

        `System.out.println(``"Inside fun(). "``);`

        `throw` `new` `IllegalAccessException(``"demo"``);`

    `}`

    `public` `static` `void` `main(String args[])`

    `{`

        `try` `{`

            `fun();`

        `}`

        `catch` `(IllegalAccessException e) {`

            `System.out.println(``"caught in main."``);`

        `}`

    `}`

`}`