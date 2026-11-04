
# Experiment No. 2 – Binary Search

**Created By:** Krish Mhatre

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

## Terminal Input (Copy and Paste)

```text
50
```

## Output

```text
PS C:\AOA> gcc binary.c -o binary
PS C:\AOA> .\binary.exe

Enter element to search: 50
Element found at index 4.
```

## Aim
To implement Binary Search using C.

## Theory
Binary Search is a searching algorithm used to find an element in a sorted array.

It repeatedly divides the search range into two halves until the element is found.

## Algorithm
1. Start with a sorted array.
2. Enter the element to search.
3. Find the middle element.
4. If the key matches, return its index.
5. If the key is greater, search the right half.
6. Otherwise, search the left half.
7. Display the result.

## How to Run

Save as `binary.c`.

Compile:

```bash
gcc binary.c -o binary
```

Run:

```powershell
.\binary.exe
```

Paste the input from the Terminal Input section.

## Time Complexity

- Best Case: O(1)
- Average Case: O(log n)
- Worst Case: O(log n)
- Space Complexity: O(1)

## Conclusion
Successfully implemented Binary Search in C to find an element in a sorted array.
