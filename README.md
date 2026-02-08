Experiment No. 4

Name: Pranav Menon

PRN No.: 25070123085

Batch: ENTC - B1

Aim: To study Sets in Python and understand set operations, methods, and their practical applications.

THEORY: 

1) Introduction to Sets

A set in Python is an unordered collection of unique elements. Sets are useful when duplicate values are not allowed and when fast membership testing is required. They are defined using curly braces {} or the set() constructor.

Key Characteristics:
• Unordered – Elements have no fixed order or index position.
• Unique – Duplicate values are automatically removed.
• Mutable – Elements can be added or removed after creation.
• Iterable – Can be traversed using loops.
• No indexing – Elements cannot be accessed by position.

Syntax:
my_set = {element1, element2, element3}
my_set = set([element1, element2, element3])

2) Duplicate Handling in Sets

Sets automatically eliminate duplicate values. When duplicates are included during creation, only one instance of each unique element is retained.

Example:
thisset = {"apple", "banana", "cherry", "apple"}
Output: {'banana', 'cherry', 'apple'}

3) Boolean Values in Sets

In sets, True is treated as equivalent to 1, and False as equivalent to 0. If both a boolean and its numeric equivalent exist, only the first occurrence is retained.

Example:
thisset = {"apple", "banana", True, 1, 2}
Output: {True, 2, 'apple', 'banana'}

4) Membership Testing

The 'in' keyword is used to check whether an element exists in a set. It returns True if the element is found, otherwise False.

Syntax:
element in set_name

Example:
"apple" in thisset   # Returns True

5) Adding Elements to a Set

Sets allow insertion of new elements using two methods:
- add(element) → Adds a single element. If the element already exists, no change occurs.
- update(iterable) → Adds multiple elements from an iterable (list, tuple, set, etc.).

Syntax:
set_name.add(element)
set_name.update([element1, element2, element3])

6) Removing Elements from a Set

Elements can be removed using:
- remove(element) → Removes the specified element; raises KeyError if element does not exist.
- discard(element) → Removes the specified element; does not raise an error if element is absent.

Example:
myset = {"apple", "banana", "cherry"}
myset.remove("banana")
myset.discard("orange")   # No error raised

Detailed Comparison: discard() vs remove()

DISCARD(element):

1. Error Handling - Does not raise an error if element is not found; continues execution silently
2. Use Case - Suitable when element existence is uncertain; ideal for defensive programming
3. Program Flow - Does not interrupt program execution; safe for removing potentially non-existent elements
4. Return Value - Returns None regardless of whether element was removed

REMOVE(element):

1. Error Handling - Raises KeyError exception if element is not found in the set
2. Use Case - Suitable when element existence is certain and errors should be caught
3. Program Flow - May interrupt program flow with exception; requires try-except block for safe handling
4. Return Value - Returns None if successful; raises exception if element not found

Example:

my_set = {"apple", "banana", "cherry"}
my_set.discard("orange")  # No error, continues normally
my_set.remove("orange")   # Raises KeyError: 'orange'

7) Set Operations

a) Union (A | B or A.union(B))

Combines all unique elements from both sets.
Example: A = {1, 2, 3}, B = {3, 4, 5}
Result: {1, 2, 3, 4, 5}

b) Intersection (A & B or A.intersection(B))

Returns elements that are common to both sets.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
Result: {3, 4}

c) Difference (A - B or A.difference(B))

Returns elements present in set A but not in set B.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
A - B: {1, 2}
B - A: {5, 6}

d) Symmetric Difference (A ^ B or A.symmetric_difference(B))

Returns elements present in either set but not in both.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
Result: {1, 2, 5, 6}

8) Frozenset

A frozenset is an immutable version of a set. Once created, elements cannot be added or removed.

Key Characteristics:

• Immutable - Cannot be modified after creation

• Can be used as dictionary keys (unlike regular sets)

• Can be elements of other sets

• Supports all set operations except modification methods

Syntax: 

frozen = frozenset([element1, element2, element3])

9) PRACTICAL APPLICATIONS OF SETS

1. Removing Duplicates - Converting lists to sets eliminates duplicate entries efficiently
2. Membership Testing - Provides fast lookup to verify element existence
3. Finding Common Elements - Identifies shared items between multiple collections
4. Data Comparison - Facilitates comparison of datasets to identify differences and similarities

10) ADVANTAGES OF SETS

• Fast membership testing with O(1) time complexity

• Automatic removal of duplicate values without manual intervention

• Built-in support for mathematical set operations

11) LIMITATIONS OF SETS

• Unordered nature prevents reliance on element order

• Absence of indexing prevents positional access to elements

• Cannot contain mutable elements such as lists or dictionaries

ALGORITHMS:

Algorithm 1: Finding Unique Participants from a List

Step 1: Start
   - Begin the process of removing duplicate participants

Step 2: Initialize student list with duplicates
   - Command: student_Name = ["Pranav", "Praharsh", "Harsh", "Aditya", "Dhruv", "Pranav", "Aditya", "Dhruv"]
   - Function: List creation using square brackets []
   - Source: Built-in Python list data structure (no import required)

Step 3: Convert list to set to remove duplicates
   - Command: Student_Name = set(student_Name)
   - Function: set() - Built-in constructor that converts any iterable to a set
   - Source: Built-in Python function (no import required)

Step 4: Display unique participants
   - Command: print("Unique Participants : ", Student_Name)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 5: Stop
   - End the algorithm

Algorithm 2: Finding Common Subjects Among Students

Step 1: Start
   - Begin the process of finding common subjects

Step 2: Initialize subject sets for Student 1
   - Command: Student1 = {"Maths", "Physics", "Biology", "Python"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 3: Initialize subject sets for Student 2
   - Command: Student2 = {"Maths", "Chemistry", "Biology", "Python"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 4: Initialize subject sets for Student 3
   - Command: Student3 = {"Maths", "Physics", "Chemistry", "Python"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 5: Find intersection using & operator (Method 1)
   - Command: Student1 & Student2 & Student3
   - Function: & - Bitwise AND operator used for set intersection
   - Source: Built-in Python operator (no import required)

Step 6: Display result using & operator
   - Command: print("The Subjects Common to all the three Student is : ", Student1 & Student2 & Student3)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
   
Step 7: Find intersection using intersection() method ----> Alternate Method
   - Command: Student1.intersection(Student2, Student3)
   - Function: intersection() - Built-in set method that accepts multiple sets as arguments
   - Source: Built-in set method (no import required)
   - Command: print("The Subjects Common to all the three Student is : " , Student1.intersection(Student2,Student3))

Step 9: Stop
   - End the algorithm

Algorithm 3: Analyzing Club Membership

Step 1: Start
   - Begin the process of analyzing club memberships

Step 2: Initialize Cricket Club membership set
   - Command: Cricket_Club = {"Pranav", "Praharsh", "Aditya", "Amar", "Rahul"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 3: Initialize Football Club membership set
   - Command: FootBall_Club = {"Aditya", "Pranav", "Rahul", "Shyam", "Raju"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)
     
Step 4: Find common members using intersection
   - Command: Common = Cricket_Club & FootBall_Club
   - Function: & - Bitwise AND operator used for set intersection
   - Source: Built-in Python operator (no import required)

Step 5: Find members unique to both clubs using symmetric difference
   - Command: Not_Common = Cricket_Club ^ FootBall_Club
   - Function: ^ - XOR (exclusive OR) operator used for symmetric difference
   - Source: Built-in Python operator (no import required)

Step 6: Find members exclusive to Cricket Club
   - Command: Cricket = Cricket_Club - FootBall_Club
   - Function: - (minus) operator used for set difference
   - Source: Built-in Python operator (no import required)

Step 7: Find members exclusive to Football Club
   - Command: Football = FootBall_Club - Cricket_Club
   - Function: - (minus) operator used for set difference
   - Source: Built-in Python operator (no import required)

Step 8: Display common members
   - Command: print("The Members Common to both the clubs are : ", Common)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 9: Display unique members to both clubs
   - Command: print("The Members which are unique to the clubs are : ", Not_Common)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 10: Display Cricket-exclusive members
   - Command: print("The Members which are unique to the Cricket Club are : ", Cricket)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 11: Display Football-exclusive members
   - Command: print("The Members which are unique to the Football Club are : ", Football)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 12: Stop
   - End the algorithm

Algorithm 4: Identifying Absent Students

Step 1: Start
   - Begin the process of identifying absent students

Step 2: Initialize set of all enrolled students
   - Command: all_students = {"Pranav", "Praharsh", "Aditya", "Amar", "Rahul"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 3: Initialize set of present students
   - Command: present_student = {"Aditya", "Pranav", "Rahul", "Shyam", "Raju"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 4: Calculate absent students using set difference
   - Command: absent_student = all_students - present_student
   - Function: - (minus) operator used for set difference
   - Source: Built-in Python operator (no import required)
  
Step 5: Display absent students
   - Command: print("The Students who are absent are :", absent_student)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 6: Stop
   - End the algorithm

Algorithm 5: Updating Course List

Step 1: Start
   - Begin the process of updating course list

Step 2: Initialize current courses set
   - Command: current_courses = {"Physics", "Chemistry", "Biology", "Math", "Python", "Digital Circuits and Logic Design"}
   - Function: Set creation using curly braces {}
   - Source: Built-in Python set data structure (no import required)

Step 3: Remove course using discard() method
   - Command: current_courses.discard("Chemistry")
   - Function: discard(element) - Built-in set method for safe element removal
   - Source: Built-in set method (no import required)
  
Step 4: Display updated courses after discard
   - Command: print("Updated Courses : ", current_courses)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 5: Remove course using remove() method
   - Command: current_courses.remove("Math")
   - Function: remove(element) - Built-in set method for strict element removal
   - Source: Built-in set method (no import required)

Step 6: Display updated courses after remove
   - Command: print("Updated Courses : ", current_courses)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 7: Stop
   - End the algorithm

CONCLUSION

The study of sets in Python was completed successfully.
