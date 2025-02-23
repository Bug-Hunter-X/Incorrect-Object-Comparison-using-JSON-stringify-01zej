# Incorrect Object Comparison in TypeScript

This repository demonstrates a common error in TypeScript when comparing objects: using `JSON.stringify` for deep comparison.  This approach is unreliable because it's sensitive to property order and cannot handle functions, Dates, or other complex data types.

The `bug.ts` file showcases the faulty comparison.  The `bugSolution.ts` file offers a more robust solution.

## Bug:
The function `compareObjects` uses `JSON.stringify` to compare two objects. This is flawed because it doesn't handle non-serializable properties, differences in property order, and nested object comparison intricacies.

## Solution:
The solution introduces a recursive deep comparison function that handles various data types and nested structures effectively.