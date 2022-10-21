## Java Questions
Q1) public static void main(String args[])
{
double x;
x++;
}

After executing main, what is the value of x?

## Solution :
```java
public static void main(String args[])
{
double x;
x++;
}
```

After executing main,there is a error occuring:

 error: variable x might not have been initialized       x++;
for resolving this error we have to either initialize the value of x in the program or take value of x from the user.

Q2)

Consider the below code:

-------------------------------------------------

double balance=0;
boolean state=true;


do
{
balance=50+balance;

}
while(balance<100 && state);

balance--;

-------------------------------------------------
after executing the above code, what is the final value of the variable "balance"?

## Solution :
```java
double balance=0;
boolean state=true;


do
{
balance=50+balance;

}
while(balance<100 && state);

 

balance--;
```
outpput)

 Main.java:7: error: illegal start of type     do     ^ Main.java:11: error: illegal start of type      while(balance<100 && state);      ^ Main.java:11: error: illegal start of type      while(balance<100 && state);                    ^ Main.java:11: error:  expected      while(balance<100 && state);                                ^ Main.java:12: error:  expected      balance--;             ^ 5 errors
these errors are occuring

### Give this Project a Star :star:
