## Question : 
Finding the correct place for a book on the shelves in the library requires librarians to be able to sort call numbers in numerical and then alphabetical order. For example, the call number for the prescribed book for this module is 005.73 JAM – the numbers indicate the book’s topic, and the letters are the first three letters of the author’s surname.

Write a C# software WPF application using visual studio that fulfils the following requirements:
- On startup, the application shall allow the user to choose between three tasks:
a. Replacing books.
b. Identifying areas.
c. Finding call numbers.
For this first task, only Replacing books, complete the following requirements:
- When the user selects Replacing books, the application shall randomly generate 10 different call numbers and display them to the user.
- The application shall allow the user to reorder the call numbers in ascending order and check whether the user got the ordering right.
- Implement a gamification feature to motivate users to keep learning.
Technical requirements:
- Make use of a list to store the generated call numbers.
- Choose an appropriate sorting algorithm to sort the call numbers to check the order that the user puts them in.

For this second task, only Identifying areas, complete the following requirements:

- Enable the Identifying areas task.
- When the user chooses the Identifying areas task, they should be presented with a user interface where they will match two columns: call number (top-level only) and description.
- The user shall be allowed to answer as many questions* as they want to.
- The questions should alternate between matching descriptions to call numbers and call numbers to descriptions.
- Each question should have four randomly selected items in the first column and seven possible answers (three of which are incorrect) in the second column.
- Implement a gamification feature to motivate users to keep using the application. You may use the same one as before or choose to implement a different one.

Technical requirements:
- Store the call numbers and their descriptions in a dictionary.

For this Third task, only Finding call numbers complete the following requirements:

- Create a file containing the research data of dewy decimal system in a format that your application can read.
- Enable the Finding call numbers task.
- When the user chooses Finding call numbers, the application must load the Dewey Decimal classification data into memory from the file created in Step 1.
- The quiz must work as follows:
a. For each question, randomly select a third-level entry from the data, for example, 752 Color. Display only the description, not the call number.
b. Display four top-level options to the user to choose between, one of which must be the correct one and the other three randomly selected incorrect answers. For example: 000 General 400 Language 700 Arts & Recreation (Correct answer) 800 Literature
c. For the options, display both the call number and description. Display the options in numerical order by call number.
d. If the user selects the correct option, show them four options from the next level until the most detailed level is reached.
e. If the user selects the wrong option anywhere along the way, indicate this and then ask the next question.
- Implement a gamification feature to motivate users to keep using the application. You may use the same one as before or choose to implement a different one.

Technical requirements:
- Make use of a tree to store the data in memory.


## Solution :
General Guidance
The answer provided below has been developed in a clear step by step manner.
Step: 1
Step 1:

A particular reading group from the shelf:

Users can locate a certain book whenever you need one since publications are sorted in call accordance with instructions. The digits and letters that make up call letters really follow a particular pattern: a letters or letters, preceded by a number, accompanied for one or two sets of alphanumeric characters, then with the year of publishing.



Explanation:
Every paperback novels are formally placed form top to bottom but from left to right, regardless of the classification scheme they are assigned to. Both technologies constantly read notation top to bottom, left to clockwise.

Step: 2
Step 2:

Elements make up a shelf quantity:

A libraries author's spines has a shelf number that indicates at which novel can be accessed on the library's shelf. It is made up of both numbers and letters such as 510.2462 STR. It's a categorization integer, that number.

When a bookshelf interpret:

When studying literature from the shelves, you should normally begin with the Roman Digit # on the spine, then by the first seven digits of something like the poster's last name. Items ought to be arranged on the shelves in ascending numbered order, beginning with 000. There will be several books that share the same French Numeric value in an area.

Explanation:
The ISBN should not be confused with a book's store call number. Since an ISBN solely contains hypens and no vowels or punctuation, the two can be distinguished. On the flipside of their article's title pages, publishing companies frequently list ISBNs and reference call number.

Answer:
Note:

For consumers who require items, appropriate placement makes them available and useable.

### Give this Project a Star :star:
