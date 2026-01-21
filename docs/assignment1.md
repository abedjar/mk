# Assignment 1


## Learning Objectives

By completing this task, you should be able to:

- Implement a Java interface correctly
- Use loops, conditionals, and basic algorithms
- Work with arrays and strings
- Handle edge cases such as `null` inputs
- Write readable and maintainable Java code

??? info "This assignment requires you to complete two tasks"

---

## **Task - 1**

This task evaluates your understanding of **core Java programming concepts**.  
You are required to implement an interface by writing correct, clean, and well-structured Java code.

This is **not** about shortcuts, libraries, or clever tricks.  
It is about showing that you understand how Java actually works.



## Implementing an Interface

You are given the following interface.  

!!! danger "Warning"

    Do not modify the interface. If you do and it works on your machine, it will not work on mine.

Here is the interface:
``` java title="BasicUtilsADT.java" linenums="1"

public interface BasicUtilsADT {
    boolean isPrime(int n);
    int countOccurrences(int[] values, int target);
    String removeVowels(String input);
}
```

## Method Descriptions

### ```boolean isPrime(int n)```

This method checks whether a given integer is a prime number.

- A prime number is greater than 1
- It is divisible only by 1 and itself
- Numbers less than or equal to 1 are not prime

**Expected behavior:** 

- Return true if n is prime
- Return false otherwise


### `int countOccurrences(int[] values, int target)`

This method returns how many times a specific value appears in an array.

**Expected behavior:** 

- Traverse the array and count how many elements equal target
- If the array is null, return 0
- Do not modify the array

### `String removeVowels(String input)`

This method removes all vowels from a given string and return the new string.

**Expected behavior:**  

- Remove lowercase and uppercase vowels (a e i o u A E I O U)
- Preserve the original order of characters
- If input is null, return an empty string
- The original string must not be modified

!!! danger "Warning"

    All methods return values and do not print them


!!! note "Your Task"
    1. Create a class named `BasicUtils.java`
    2. The class must implement the BasicUtilsADT interface
    3. Implement all methods exactly as defined
    4. Do not add extra public methods

---

## **Task - 2**

This task evaluates your understanding of using linear data structures implemented with an array. You need to review the example provided in the lecture about `Scoreboard` and `GameEntry` classes.

This is the **modified ADT** that you are required to implement:
```java title="ScoreboardADT.java" linenums="1" hl_lines="13-18"
public interface ScoreboardADT {

    //Original members

    void add(GameEntry e);
    GameEntry remove(int i);
    int getCapacity();
    int getNumEntries();
    GameEntry getEntry(int i);

    //Extra members 

    boolean contains(String name);
    int getRank(String name);
    GameEntry[] top(int k);
    boolean removeByName(String name);
    GameEntry getLowestScore();
    void updateScore(String name, int newScore);
}
```

Notice that the `original members` were already implemented in the lecture and you can use (copy/paste) that code as is. 

Your task is to implement the `Extra members` following the description in the slides.

!!! note "Your Task"
    1. The class named `Scoreboard.java` should implement `ScoreboardADT.java`
    2. Maintain the same implementation of the `original members` within `Scoreboard.java`.
    3. Implement the `Extra members` following the description in the slides.

## Submission
!!! question "Submission instructions"
    1. You will submit ** ONLY 2 files**:
          1. `BasicUtils.java`
          2. `Scoreboard.java`
    2. Submission will be in BrighSpace

!!! danger "Late Submission policy"
    -30% marks will be deducted for each day. And on Day 4 after the deadline, you will receive 0 marks even if you submit.