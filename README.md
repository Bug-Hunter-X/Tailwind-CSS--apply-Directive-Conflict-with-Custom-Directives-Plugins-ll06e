# Tailwind CSS @apply Directive Conflict with Custom Directives/Plugins

This repository demonstrates a bug related to unexpected or missing styles when using Tailwind's `@apply` directive with custom directives or plugins.  The conflict arises from the order of style application when custom directives/plugins modify styles and `@apply` is used on the same element.

## Bug Description

When a custom plugin or directive modifies the style of an element, and an `@apply` directive with potentially conflicting styles is used on that same element, the result is unpredictable.  The final style might be incorrect or inconsistent.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the conflicting code.
3. Observe that the styling is unexpected.
4. Open `bugSolution.css` to see one way of solving the problem. 

## Solution

The solution involves careful consideration of the order of style application.  Prioritize styles from custom directives/plugins or use CSS specificity rules to ensure the correct style is applied.