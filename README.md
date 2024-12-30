# CSS `calc()` Bug: Unexpected Behavior with Mixed Units

This repository demonstrates a common yet easily overlooked bug involving the CSS `calc()` function and mixed units (percentages and pixels). The bug occurs when performing calculations that mix percentages and fixed units (such as pixels) without proper use of parentheses.  This leads to unexpected layout behaviors, often resulting in incorrect element sizing and positioning.

## Bug Description

The core issue lies in the order of operations within the `calc()` function.  When units are combined, the browser might interpret the calculation in an unexpected way unless each operation is clearly separated and prioritized with parentheses.  Mixing percentages and pixels without proper grouping can cause unexpected behavior and layout inconsistencies.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` and observe the usage of the `calc()` function in the `.buggy` class.
3. Load the HTML file (e.g., in a browser). Observe how the element's width does not render as expected.
4. Now, open `bugSolution.css` and see how the corrected usage of parentheses resolves the issue.

## Solution

The solution involves using parentheses to correctly group the operations, ensuring that the calculation is performed according to the desired order. See `bugSolution.css` for the corrected code. Always group operations with parentheses when mixing units within `calc()` to prevent unexpected results.