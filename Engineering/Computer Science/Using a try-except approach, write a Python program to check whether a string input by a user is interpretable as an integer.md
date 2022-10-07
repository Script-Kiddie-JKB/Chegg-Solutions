## Question :
Using a try-except approach, write a Python program to check whether a string input by a user is interpretable as an integer - ie contains only the digits 0 to 9. If the string is not an integer, your program should check to see if the string is float - ie, contains only the digits 0 to 9 or the dot (.) character. If the string is an integer display "Is integer". If the string is a float, display "Is float". Otherwise, display "Not a number" and re-raise the exception.

## Solution :

```python
def funCheck(strNumber):

   try:

       if int(strNumber):

           print("String is Integer")

       elif float(strNumber):

           print("String is float")

   except ValueError:

       print("Not a number !")

strNumber=input('Enter a input String :- ')

funCheck(strNumber)
```

### Give this Project a Star :star:
