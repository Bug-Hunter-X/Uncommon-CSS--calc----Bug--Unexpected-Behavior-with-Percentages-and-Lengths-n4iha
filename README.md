# Uncommon CSS `calc()` Bug

This repository demonstrates an uncommon bug related to the CSS `calc()` function. The bug arises when combining percentages and fixed lengths (like pixels) within the `calc()` function, which can lead to unexpected rendering results.

## Bug Description

The `calc()` function is powerful for dynamic calculations within CSS, but there are subtleties.  When mixing percentages and fixed units in a calculation, the percentage is calculated *relative to the parent element's size*. If the parent's size is not yet determined (e.g., due to the way the layout flows), the calculation may yield unexpected results.

## Reproduction

1. Clone this repository.
2. Open `index.html` in your web browser.
3. Observe the unexpected layout due to the `calc()` function in `bug.css`.

## Solution

The solution often involves restructuring your CSS to avoid the problematic combination or ensuring the parent element has its dimensions defined explicitly before the calculation is performed. The example in `bugSolution.css` provides a corrected approach.