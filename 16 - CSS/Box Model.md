### Description
Every single thing on a webpage is a rectangular box.

The standard CSS box model behaves so that giving a width or height defines the size of the content box only. This means the total size taken up by the element will actually be different than specified, as it will then add the padding and border sizes.

The alternative CSS box model can be used by setting `box-sizing: border-box`. This will make it subtract the final size by the padding and border to get the content size, resulting in a final size that is as specified by width/height.

The alternative box model can be set as the default for all elements via the following CSS:
```css
html {
	box-sizing: border-box;
}

*,
*::before,
*::after {
	box-sizing: inherit;
}
```
### See Also
* [[Margins]]
* [[Padding]]
* [[Borders]]
