# Duplicate Elements at Even Indices

## Description
This Java program identifies and prints duplicate elements that appear at even indices in an array. The program prompts the user to enter the size of the array and the elements, then iterates through the array to check for duplicate values at even index positions.

## How It Works
1. The program uses the `Scanner` class to take user input for the size of the array and its elements.
2. It stores these elements in an integer array.
3. A nested loop structure is used to compare elements and identify duplicates at even indices.
4. If a duplicate element is found at an even index, it is printed.

## Code Explanation
### **1. Importing Scanner Class**
```java
import java.util.Scanner;
```
- The `Scanner` class is used to take user input.

### **2. Main Method**
```java
public static void main(String[] args)
```
- This is the entry point of the program.
- It initializes the `Scanner` object and takes user input.

### **3. Taking User Input**
```java
Scanner s = new Scanner(System.in);
System.out.println("Enter the Size of array");
int size = s.nextInt();
int [] arr = new int [size];
System.out.println("Enter the Elements");
for(int i=0; i<=arr.length-1; i++)
{
    arr[i] = s.nextInt();
}
```
- The user is prompted to enter the array size and elements.
- A `for` loop runs from `0` to `size-1` to store values in the array.

### **4. Checking for Duplicates at Even Indices**
```java
for(int i=0; i<=arr.length-1; i++)
{
    for(int j=0; j<=i-1; j++)
    {
        if(i % 2 == 0)  // Check if index is even
            if(arr[j] == arr[i]) // Check for duplicate values
                System.out.println(arr[j]);
    }
}
```
#### **Outer Loop (`for` loop with index `i`)**
- Iterates through each element in the array.
- `i` represents the current index being checked.

#### **Inner Loop (`for` loop with index `j`)**
- Runs from `0` to `i-1`, checking all previous elements.
- Compares the current element at index `i` with previous elements at index `j`.

#### **Conditions Used**
1. `if(i % 2 == 0)`: Checks whether `i` (index) is even.
2. `if(arr[j] == arr[i])`: Compares the values at indices `j` and `i` to find duplicates.
3. `System.out.println(arr[j]);`: Prints the duplicate value if found.

## Example Execution
### **Input:**
```
Enter the Size of array
5
Enter the Elements
3 5 3 8 5
```
### **Processing:**
- The array: `[3, 5, 3, 8, 5]`
- Checking for duplicates at even indices (0, 2, 4)
- `arr[2]` (3) is a duplicate of `arr[0]`
- `arr[4]` (5) is a duplicate of `arr[1]`

### **Output:**
```
3
5
```

## Potential Improvements
- Optimize by using a `HashSet` to reduce time complexity.
- Handle edge cases like empty arrays or all unique elements.
- Allow the user to specify whether they want to check for duplicates at even or odd indices.

## Conclusion
This program demonstrates how to use nested loops and conditional statements to detect duplicates at specific positions in an array. It helps in understanding array traversal, index manipulation, and element comparison in Java.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Duplicate_At_Even_Index.git
```
