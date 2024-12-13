# Inconsistent Behavior of `removeIf` for Lists and Sets in Kotlin

This repository demonstrates an uncommon, subtle bug related to the `removeIf` function in Kotlin when used with different collection types (Lists and Sets).  While both lists and sets are modified in-place, the function behaves consistently but might not be intuitive if the programmer isn't fully aware of these subtle differences. This can lead to unexpected results.

The `bug.kt` file shows the inconsistent behavior. The `bugSolution.kt` file offers a better strategy using a filter operation for achieving consistent removal across collections. 

## How to reproduce

1. Clone this repository.
2. Open `bug.kt` to see the demonstration of the unexpected behavior.
3. Open `bugSolution.kt` for a solution that demonstrates how to avoid this issue.

## Solution

The `bugSolution.kt` file provides a solution using the `filter` function, creating a new collection with the desired elements instead of modifying the original collection in-place. This leads to more predictable and consistent code.