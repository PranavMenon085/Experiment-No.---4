**Experiment No. 4**

Name: Pranav Menon

PRN No.: 25070123085

Batch: ENTC - B1

**Aim:** To study Sets in Python and understand set operations, methods, and their practical applications.

**THEORY**

**1) Introduction to Sets**

A set is an unordered collection of unique elements in Python. Sets are defined using curly braces {} or the set() constructor.

**Key Characteristics:**
• Unordered - Elements have no defined order or index position
• Unique elements - Duplicate values are automatically removed
• Mutable - Elements can be added or removed after creation
• Iterable - Can be traversed using loops
• No indexing - Cannot access elements by position

**Syntax:**
my_set = {element1, element2, element3}
OR
my_set = set([element1, element2, element3])

**2) Duplicate Handling in Sets**

Sets automatically eliminate duplicate values. When a set is created with duplicate elements, only one instance of each unique element is retained.

**Example:**
Input: thisset = {"apple", "banana", "cherry", "apple"}
Output: {'banana', 'cherry', 'apple'}

**3) Boolean Values in Sets**

**Key Points:**
• True is considered equivalent to 1
• False is considered equivalent to 0
• If both a boolean and its numeric equivalent exist, only the first occurrence is retained

**Example:**
Input: thisset = {"apple", "banana", True, 1, 2}
Output: {True, 2, 'cherry', 'apple', 'banana'}

**4) Membership Testing**

The 'in' keyword is used to check whether an element exists in a set. It returns True if the element is found, otherwise False.

**Syntax:** element in set_name
**Time Complexity:** O(1) - Constant time (highly efficient)

**5) Adding Elements to a Set**

**Method 1: add(element)**
• Adds a single element to the set
• If element already exists, no change occurs
• Returns None

**Syntax:** set_name.add(element)

**Method 2: update(iterable)**
• Adds multiple elements from an iterable (list, tuple, set, etc.)
• Can add elements from multiple iterables simultaneously

**Syntax:** set_name.update([element1, element2, element3])

**6) Removing Elements from a Set**

**Method 1: remove(element)**
• Removes the specified element from the set
• Raises KeyError if element does not exist
• Use when element existence is certain

**Method 2: discard(element)**
• Removes the specified element from the set
• Does not raise an error if element does not exist
• Preferred when element existence is uncertain

**Detailed Comparison: discard() vs remove()**

**DISCARD(element):**
1. Error Handling - Does not raise an error if element is not found; continues execution silently
2. Use Case - Suitable when element existence is uncertain; ideal for defensive programming
3. Program Flow - Does not interrupt program execution; safe for removing potentially non-existent elements
4. Return Value - Returns None regardless of whether element was removed

**REMOVE(element):**
1. Error Handling - Raises KeyError exception if element is not found in the set
2. Use Case - Suitable when element existence is certain and errors should be caught
3. Program Flow - May interrupt program flow with exception; requires try-except block for safe handling
4. Return Value - Returns None if successful; raises exception if element not found

**Example:**
my_set = {"apple", "banana", "cherry"}
my_set.discard("orange")  # No error, continues normally
my_set.remove("orange")   # Raises KeyError: 'orange'

**When to Use:**
• Use discard() when removing elements that might not exist (safer approach)
• Use remove() when you want to ensure the element exists (explicit error detection)

**7) Set Operations**

**a) Union (A | B or A.union(B))**
Combines all unique elements from both sets.
Example: A = {1, 2, 3}, B = {3, 4, 5}
Result: {1, 2, 3, 4, 5}

**b) Intersection (A & B or A.intersection(B))**
Returns elements that are common to both sets.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
Result: {3, 4}

**c) Difference (A - B or A.difference(B))**
Returns elements present in set A but not in set B.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
A - B: {1, 2}
B - A: {5, 6}

**d) Symmetric Difference (A ^ B or A.symmetric_difference(B))**
Returns elements present in either set but not in both.
Example: A = {1, 2, 3, 4}, B = {3, 4, 5, 6}
Result: {1, 2, 5, 6}

**8) Frozenset**

A frozenset is an immutable version of a set. Once created, elements cannot be added or removed.

**Key Characteristics:**
• Immutable - Cannot be modified after creation
• Can be used as dictionary keys (unlike regular sets)
• Can be elements of other sets
• Supports all set operations except modification methods

**Syntax:** frozen = frozenset([element1, element2, element3])

**Use Cases:**
• When a constant set of values is required
• As dictionary keys
• As elements within another set

**ALGORITHMS**

**Algorithm 1: Finding Unique Participants from a List**

**Objective:** Remove duplicate student names from a list of participants.

**Procedure:**
1. Start
2. Input a list containing student names (may include duplicates)
3. Convert the list to a set using the set() function
   - This operation automatically removes all duplicate entries
4. Store the resulting set in a new variable
5. Display the unique participants
6. Stop

**Time Complexity:** O(n), where n is the number of elements in the list

**Algorithm 2: Finding Common Subjects Among Students**

**Objective:** Identify subjects that are common to all three students.

**Procedure:**
1. Start
2. Create three sets representing subjects enrolled by each student:
   - Student1_subjects = {subject1, subject2, subject3, subject4}
   - Student2_subjects = {subject1, subject2, subject3, subject4}
   - Student3_subjects = {subject1, subject2, subject3, subject4}
3. Compute the intersection of all three sets using:
   - Method 1: Student1 & Student2 & Student3
   - Method 2: Student1.intersection(Student2, Student3)
4. Store the result in a variable (common_subjects)
5. Display the common subjects
6. Stop

**Time Complexity:** O(n), where n is the total number of unique subjects

**Algorithm 3: Analyzing Club Membership**

**Objective:** Determine members common to both clubs, members unique to each club, and exclusive members.

**Procedure:**
1. Start
2. Create two sets representing members of each club:
   - Cricket_Club = {member1, member2, ...}
   - Football_Club = {member1, member2, ...}
3. Find common members using intersection:
   Common = Cricket_Club & Football_Club
4. Find members unique to both clubs using symmetric difference:
   Unique_to_both = Cricket_Club ^ Football_Club
5. Find members exclusive to Cricket Club using difference:
   Only_Cricket = Cricket_Club - Football_Club
6. Find members exclusive to Football Club using difference:
   Only_Football = Football_Club - Cricket_Club
7. Display all computed results:
   • Common members
   • Members unique to both clubs
   • Cricket-exclusive members
   • Football-exclusive members
8. Stop

**Time Complexity:** O(n + m), where n and m are the sizes of the two sets

**Algorithm 4: Identifying Absent Students**

**Objective:** Determine which students are absent based on attendance records.

**Procedure:**
1. Start
2. Create a set containing all enrolled students:
   All_students = {student1, student2, student3, student4, student5}
3. Create a set containing students present in class:
   Present_students = {student1, student2, student3, student4, student5}
4. Compute absent students using set difference:
   Absent_students = All_students - Present_students
5. Display the list of absent students
6. Stop

**Time Complexity:** O(n), where n is the number of students

**Algorithm 5: Updating Course List**

**Objective:** Remove specific courses from the current course list using different removal methods.

**Procedure:**
1. Start
2. Create a set containing current courses:
   Current_courses = {course1, course2, course3, course4, course5 ,course6}
3. Using the discard() method:
   • Execute Current_courses.discard("Course_Name")
   • No error is raised if course does not exist
   • Display the updated course list
4. Using the remove() method:
   • Execute Current_courses.remove("Course_Name")
   • KeyError is raised if course does not exist
   • Display the updated course list
5. Stop

**Time Complexity:** O(1) for both operations

**SET METHODS SUMMARY**

• add(element) - Adds a single element; no error if element already exists
• update(iterable) - Adds multiple elements; no error if duplicates present
• remove(element) - Removes specified element; raises KeyError if not found
• discard(element) - Removes specified element; no error if not found
• union() or | - Returns the union of sets
• intersection() or & - Returns elements common to all sets
• difference() or - - Returns elements in the first set but not in the second
• symmetric_difference() or ^ - Returns elements in either set but not in both

**PRACTICAL APPLICATIONS OF SETS**

1. Removing Duplicates - Converting lists to sets eliminates duplicate entries efficiently
2. Membership Testing - Provides fast lookup to verify element existence
3. Finding Common Elements - Identifies shared items between multiple collections
4. Data Comparison - Facilitates comparison of datasets to identify differences and similarities
5. Mathematical Operations - Enables implementation of mathematical set theory operations
6. Data Filtering - Efficiently removes unwanted elements from collections
7. Network Analysis - Assists in finding connections and overlaps in network structures
8. Database Operations - Supports operations like joins, unions, and intersections

**ADVANTAGES OF SETS**

• Fast membership testing with O(1) time complexity
• Automatic removal of duplicate values without manual intervention
• Built-in support for mathematical set operations
• Memory efficient storage of unique elements only
• Flexible structure allowing easy addition and removal of elements

**LIMITATIONS OF SETS**

• Unordered nature prevents reliance on element order
• Absence of indexing prevents positional access to elements
• Cannot contain mutable elements such as lists or dictionaries
• Cannot store duplicate values by design

**CONCLUSION**

Sets are a fundamental data structure in Python that provide efficient operations for managing unique collections of elements. They are particularly valuable for performing mathematical set operations, eliminating duplicate entries, and conducting fast membership tests. A thorough understanding of set operations and methods is essential for developing efficient Python programs, especially in applications involving data comparison, filtering, and analysis.

The study of sets in Python was completed successfully. Various set operations including union, intersection, difference, and symmetric difference were demonstrated. The practical applications of sets in removing duplicates, membership testing, and data manipulation were observed and verified through implementation.
