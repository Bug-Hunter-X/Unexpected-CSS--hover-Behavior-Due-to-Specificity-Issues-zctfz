# Unexpected CSS :hover Behavior

This repository demonstrates a common CSS issue where the `:hover` pseudo-class unintentionally affects elements outside its intended scope because of insufficient selector specificity.  The problem arises from the cascading nature of CSS; without careful consideration of specificity, hover effects can "bleed" into other elements, leading to unexpected behavior.

## Problem

The `bug.css` file contains a CSS snippet that illustrates this issue.  Hovering over the `.container` element changes the background color of the `.inner` element within the container.  However, this change can also unexpectedly affect other `.inner` elements elsewhere on the page if they aren't targeted by other more specific rules.

## Solution

The `bugSolution.css` file provides a solution by improving selector specificity.  This ensures that the `:hover` effect only applies to the intended `.inner` element within the `.container`.

## How to Reproduce

1. Clone this repository.
2. Open `index.html` (not included, you will have to create one and link to the stylesheets) in your browser.
3. Observe the behavior described above.