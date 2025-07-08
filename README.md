# Insertion vs Selection Sort Performance Analysis

A comparative study of insertion sort and selection sort algorithms across different input conditions, demonstrating how algorithm choice impacts performance based on data characteristics.

## Overview

This project implements and analyzes two fundamental sorting algorithms:
- **Insertion Sort**: Adaptive algorithm that builds sorted array one element at a time
- **Selection Sort**: Non-adaptive algorithm that repeatedly selects minimum elements

The analysis reveals how input data ordering dramatically affects algorithm performance, particularly highlighting insertion sort's adaptive nature versus selection sort's consistent behavior.

## Key Findings

- **Best Case (Sorted Data)**: Insertion sort achieves O(n) performance while selection sort remains O(n²)
- **Worst Case (Reverse Sorted)**: Both algorithms converge to O(n²) performance
- **Random Data**: Insertion sort consistently outperforms selection sort due to adaptive behavior
- **Adaptability**: Insertion sort performance varies with input structure; selection sort remains constant

## Usage

```bash
python Sort.py <array_length> <increasing|decreasing|random>
```

**Examples:**
```bash
python Sort.py 1000 increasing    # Test with sorted data
python Sort.py 5000 decreasing    # Test with reverse sorted data
python Sort.py 10000 random       # Test with random data
```

## Implementation Details

### Insertion Sort
- **Time Complexity**: O(n) best case, O(n²) worst case
- **Space Complexity**: O(1)
- **Approach**: Compares each element with predecessors until correct position found

### Selection Sort
- **Time Complexity**: O(n²) all cases
- **Space Complexity**: O(1)
- **Approach**: Finds minimum element in unsorted portion for each position

## Performance Analysis

### Increasing Order (Best Case for Insertion Sort)
Insertion sort performs only n-1 comparisons total, achieving linear growth. Selection sort still performs n(n-1)/2 comparisons, showing quadratic growth despite sorted input.

### Decreasing Order (Worst Case for Insertion Sort)
Both algorithms approach O(n²) performance. Insertion sort loses its adaptive advantage as every element requires maximum shifting to reach its position.

### Random Order
Insertion sort outperforms selection sort by adapting to partial ordering in the data. Selection sort maintains consistent quadratic behavior regardless of input structure.

## Files

- `Sort.py` - Main implementation with both sorting algorithms
- Performance analysis graphs and detailed explanations included in project documentation

## Technical Insights

The analysis demonstrates a fundamental principle in algorithm design: **adaptive algorithms can significantly outperform non-adaptive ones when input conditions favor their approach**. However, adaptive algorithms may lose this advantage under worst-case conditions, while non-adaptive algorithms provide predictable performance regardless of input characteristics.
