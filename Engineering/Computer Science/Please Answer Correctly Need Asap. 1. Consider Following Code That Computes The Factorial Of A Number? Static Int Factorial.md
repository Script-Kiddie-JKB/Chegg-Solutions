## Question :
Consider following code that computes the factorial of a number?

static int factorial ( int n ) {

if ( n == 0 )

return 1 ;

e l s e

return n ∗ fact ( n − 1 ) ; }

• Explain what would be the result of n= -1

(IF N = NEGATIVE 1 NOT 1) Rewrite the code with Assertion or Exception handling mechanism to protect it from a stupid behavior.

## Solution :
The result of n = -1 is:
![image](https://user-images.githubusercontent.com/78461084/197183905-ffa61c9c-ef43-45dc-a2a0-52e0329566ae.png)

Explanation: if we put -1 then the program will always call the recursive stack and this cause the StackOverflow error because the recursive function does not know when to stop calling the recursive stack.

  

Updated Code:

We can protect the code using Exception Handling.

public class Main
{
static int factorial ( int n ) throws Exception{
//throwing Exception when the value is less than 0 or negative
if(n < 0) throw new Exception("Value is negative");
  
if ( n == 0 )
return 1 ;
else
return factorial(n-1) * n;
}
   public static void main(String[] args) throws Exception {
       System.out.println(factorial(-1));
   }
}

Screenshot of the program

![image](https://user-images.githubusercontent.com/78461084/197184007-73673e1f-d776-4cfb-84ab-b63bf50242b1.png)

Output:

![image](https://user-images.githubusercontent.com/78461084/197184078-3da0c944-f204-4f04-b687-7bce9b5e0117.png)
