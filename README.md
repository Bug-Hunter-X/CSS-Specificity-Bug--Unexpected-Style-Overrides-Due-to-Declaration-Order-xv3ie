# CSS Specificity Bug: Unexpected Style Overrides

This repository demonstrates a subtle CSS bug related to the interplay between CSS selector specificity and the order in which styles are defined.  The bug showcases how a more specific selector can be overridden by a less specific selector if the latter is declared later in the stylesheet.

## Bug Description

The core problem involves the unexpected behavior resulting from the combination of CSS specificity and the order of style declarations.  While a more specific selector *should* take precedence, the order of appearance can sometimes override the specificity calculations, leading to unpredictable styling.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the problematic CSS.
3. Open the HTML file (or create your own) containing a `div` element with both `id="myID"` and `class="myClass"`.
4. Observe the color of the div – it will be green instead of the expected purple.

## Solution

The solution involves reorganizing the CSS to ensure that the more specific selectors are declared *before* the less specific selectors.  Check `bugSolution.css` for a corrected version.

## Key Learning

This bug highlights the importance of understanding the combined effects of CSS specificity and the order of style declarations when writing CSS.  While specificity is crucial, maintaining a logical and consistent declaration order can prevent such unexpected behavior.