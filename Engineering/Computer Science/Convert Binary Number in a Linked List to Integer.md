## Question :
Convert Binary Number in a Linked List to Integer

Given head which is a reference node to a singly-linked list. The value of each node in the linked list is either 0 or 1. The linked list holds the binary representation of a number.

Return the decimal value of the number in the linked list.

The most significant bit is at the head of the linked list.

 

Example 1:

![image](https://user-images.githubusercontent.com/78461084/197195070-d25771e3-fbf3-4448-b455-5c14cb7fcd85.png)

Input: head = [1,0,1]
Output: 5
Explanation: (101) in base 2 = (5) in base 10
Example 2:

Input: head = [0]
Output: 0

## Solution :
```java
class Solution {
    public int getDecimalValue(ListNode head) {
        //Initialize temp node with head
        ListNode temp = head;
        //Answer to collect the final index
        int ans = 0;
        //Loop through the linked list
        while(temp!=null){
            //build the answer. Answer = 2*Answer + present value
            ans = 2*ans+temp.val;
            //Move to the next node
            temp = temp.next;
        }
        return ans;
    }
}
```
