
# Experiment No. 2 – Binary Search

**Created By:** Krish Mhatre

## Aim
To implement Binary Search using C.

## Theory
Binary Search is a searching algorithm used to find an element in a sorted array.

It works by repeatedly dividing the search range into two halves until the element is found or the search ends.

## Algorithm
1. Start with a sorted array.
2. Find the middle element.
3. If the middle element equals the key, return its index.
4. If the key is greater, search the right half.
5. If the key is smaller, search the left half.
6. Repeat until the element is found or the range is empty.

## C Program

```c
#include <stdio.h>

int main() {
    int a[] = {10, 20, 30, 40, 50, 60, 70};
    int n = 7, key, low = 0, high = n - 1;
    int mid, pos = -1;

    printf("Enter element to search: ");
    scanf("%d", &key);

    while(low <= high) {
        mid = (low + high) / 2;

        if(a[mid] == key) {
            pos = mid;
            break;
        }
        else if(a[mid] < key)
            low = mid + 1;
        else
            high = mid - 1;
    }

    if(pos == -1)
        printf("Element not found.");
    else
        printf("Element found at index %d.", pos);

    return 0;
}
```

## How to Run

**Step 1:** Save the file as `binary.c`.

**Step 2:** Open the terminal and compile:

```bash
gcc binary.c -o binary
```

**Step 3:** Run the program in PowerShell:

```powershell
.\binary
```

## Output

```text
Enter element to search: 50
Element found at index 4.
```

## Time Complexity

| Case | Complexity |
|------|------------|
| Best Case | O(1) |
| Average Case | O(log n) |
| Worst Case | O(log n) |

**Space Complexity:** O(1)

## Conclusion
Successfully implemented Binary Search in C to find an element in a sorted array.
