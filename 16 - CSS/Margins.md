### Description
Margins increase (or decrease if negative) the space between the borders of a box and the borders of adjacent boxes.

The `margin` property accepts 
* four values: top, right, bottom, left
* three values: top, left-right, bottom
* two values: top-bottom, left-right
* one value: all four

Or individual margins can be set via `margin-top`, `margin-right`, `margin-bottom` and `margin-left`.

Margin properties also accept `auto` as a value, which will either be 0 or whatever space is available on that side of the element. 

One useful trick for `auto` is that setting left and right to `auto` will horizontally center the element. However the element has to have a specified width. It's important to remember that `auto` does not work for top/bottom margins and cannot be used to vertically center an element.
```css
.container {
	width: 980px;
	margin: 0 auto;
}
```
### See Also
* [[Margin Collapsing]]