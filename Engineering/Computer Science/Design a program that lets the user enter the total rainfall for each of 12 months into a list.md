## Question :
Design a program that lets the user enter the total rainfall for each of 12 months into a list.
The program should calculate and display the total rainfall for the year, the average monthly
rainfall, and the months with the highest and lowest amounts.

## Solution :
```python
def main():
    data = [0 for i in xrange(12)]


print 'Enter the data: '
for i in xrange(12):
    data[i] = input()
data.sort()
total = sum(data)
average = total / 12
print average
print 'Highest: '
print data[0]
print 'Lowest: '
print data[11]
if __name__ == '__main__':
    main()
```
