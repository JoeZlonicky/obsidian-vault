### Description
If two CSS rules are trying to change the same value, the winner will be the one with the higher selector precedence:
1. ID selectors
2. Class selectors
3. Type selectors

If they have the same selector precedence, then it is how many selectors. For example, two class selectors has higher precedence than one class selector, because it is more specific.

If the same number of selectors are used of the same precedence, then depends on the order in the CSS source (later overrides earlier).

Important note: universal selectors or combinator symbols (+, ~, >, empty space) do not add any specificity.

Important note: [[16 - CSS/Inheritance|Inheritance]] is overridden by direct selectors.