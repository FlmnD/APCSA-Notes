# Array Insertion and Deletion

&nbsp;

#### Example integer array: `[1, 3, 5, 7]`

&nbsp;

## Deletion

#### Ex: Delete 5

1. Find the number or return -1 if not found.
2. Shift every number from starting at the index + 1 to the left once.
3. Set last non-zero value to 0.

#### Final result: `[1, 3, 7, 0]`

&nbsp;

## Insertion

#### Ex: Insert 2

1. Check for space, if no space return -1
2. Find the next largest value, get index
3. Move all elements to the right by starting at the end and shifting every element once to the right until index is reached (Make sure not to shift zeroes from right of the array)
4. Replace the value at index with num, in this case 2

#### Final result: `[1, 3, 7, 0]`