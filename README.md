# Vector Sorting Program

## Overview

This program demonstrates the use of **sorting algorithms (Selection Sort and Quick Sort)** on a vector of bids loaded from a CSV file. It includes a menu-driven interface for loading bid data, displaying it, and sorting it using the implemented algorithms.

This project showcases:
- **Selection Sort**: A simple comparison-based sorting algorithm.
- **Quick Sort**: An efficient, divide-and-conquer sorting algorithm.
- **CSV File Handling**: Reading and parsing bid data from a CSV file using a custom CSV parser.
- **Performance Measurement**: Measuring the time taken by the sorting algorithms.

---

## Files in the Project

- **`VectorSorting.cpp`**: The main program containing the sorting logic, CSV file loading, and menu interface.
- **`CSVparser.hpp`**: A header file for parsing CSV files (assumed to be provided as part of the project or included in a library).
- **`eBid_Monthly_Sales.csv`**: A sample CSV file containing bid data (can be customized or replaced as needed).

---

## Program Structure

### Bid Structure
A `Bid` struct is used to store the following information:
- `bidId`: Unique identifier of the bid
- `title`: Title of the bid
- `fund`: Fund associated with the bid
- `amount`: Amount of the bid

### Main Features
1. **Loading Bids:**  
   The program reads bid data from a CSV file using `loadBids()`.
   
2. **Displaying Bids:**  
   The `displayBid()` function prints bid details to the console.

3. **Sorting Bids:**  
   Users can sort bids by title using:
   - **Selection Sort:** Simple comparison-based sorting.
   - **Quick Sort:** Efficient divide-and-conquer sorting.

4. **Performance Measurement:**  
   The program uses the `clock()` function to measure and display the time taken by each sorting algorithm.

---

## Compilation

To compile the program, run the following command:

```bash
g++ -o VectorSorting VectorSorting.cpp
```

Make sure the `CSVparser.hpp` file is in the same directory or correctly linked during compilation.

---

## Running the Program

After compiling, run the program:

```bash
./VectorSorting
```

### **Program Menu**
The program provides a menu interface with the following options:

```
Menu:
  1. Load Bids
  2. Display All Bids
  3. Selection Sort All Bids
  4. Quick Sort All Bids
  9. Exit
```

- **Option 1:** Load bids from the specified CSV file.
- **Option 2:** Display all loaded bids.
- **Option 3:** Sort bids using Selection Sort and display the time taken.
- **Option 4:** Sort bids using Quick Sort and display the time taken.
- **Option 9:** Exit the program.

---

## Sample CSV File (`eBid_Monthly_Sales.csv`)

The program expects a CSV file containing bid data. The format should be similar to:

```csv
Title,Bid ID,Fund,Amount
"Bid A",1001,Fund1,1500.00
"Bid B",1002,Fund2,2500.50
"Bid C",1003,Fund3,3000.75
```

You can modify the file path by changing the `csvPath` variable or passing it as a command-line argument.

---

## Key Functions

### `loadBids(string csvPath)`
- Loads bid data from a CSV file into a `vector<Bid>`.

### `selectionSort(vector<Bid>& bids)`
- Sorts the bids using Selection Sort.
- Time complexity: **O(n²)**.

### `quickSort(vector<Bid>& bids, int begin, int end)`
- Sorts the bids using Quick Sort.
- Time complexity: **O(n log n)** on average, but **O(n²)** in the worst case.

### `partition(vector<Bid>& bids, int begin, int end)`
- Helper function for Quick Sort to partition the vector.

---

## Example Output

**After loading bids:**

```
1001: Bid A | 1500.00 | Fund1
1002: Bid B | 2500.50 | Fund2
1003: Bid C | 3000.75 | Fund3
```

**After sorting using Selection Sort:**
```
1001: Bid A | 1500.00 | Fund1
1002: Bid B | 2500.50 | Fund2
1003: Bid C | 3000.75 | Fund3
```

**Performance Measurement Output:**
```
time: 123456 clock ticks
time: 0.123456 seconds
```

---

## Notes and Improvements
- **Error Handling:** Enhance error handling for CSV parsing and invalid input scenarios.
- **Efficiency:** Optimize Quick Sort to handle worst-case inputs.
- **Memory Management:** Review and improve memory usage when working with large data sets.

---

## Author
Zachary Huff  
Version 1.1  

---
