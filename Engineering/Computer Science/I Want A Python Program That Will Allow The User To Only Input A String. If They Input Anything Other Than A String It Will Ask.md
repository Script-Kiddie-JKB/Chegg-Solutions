## Question : I want a python program that will allow the user to only input a string. If they input anything other than a string it will ask the user to try again. For example, the program ask's the user to enter their name and they enter a number, the program ask's them again to Enter your name. This keeps on going until they enter their name.

## Solution :

```python
User = input('Enter Something:')
if User.isalpha():
    print ('Your name is', User)
else:
    print 'Invalid!,Entered input is Not an string,Try again')
```

## Output :
![image](https://user-images.githubusercontent.com/78461084/197186117-72ac1d52-5ec2-45a1-be11-0b8ff3479639.png)

