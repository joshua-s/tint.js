# tint.js
Miscellaneous color tools for the web developer

## Usage
### Prerequisites
Download the project files or install it using NPM, Yarn, etc...
```sh
$ npm install tint.js --save
$ yarn add tint.js
```

Include the plugin files in your source.
> Note: the path will need to be changed if you downloaded or moved the files.
```html
<script src="node_modules/tint.js/tint.js"></script>
```

### Methods
#### tint.convert.hexToRGB
Converts **hex to sRGB**
Returns an array of the form [r,g,b] where r, g, and b are integers between 0
and 255

##### Example usage
```javascript
tint.convert.hexToRGB("#fff"); // Returns [ 255, 255, 255 ]
```

Hex can be:
- "fff"
- "ffffff"
- "#fff"
- "#ffffff"
- "0xffffff"

#### tint.convert.RGBToHex
Converts **sRGB to hex** where **rgb** is an **array** of the form [r,g,b] where
r, g, and b are integers between 0 and 255

Returns a string of the form "#ffffff"

##### Example usage
```javascript
tint.convert.RGBToHex([255, 255, 255]); // Returns #ffffff
```

#### tint.convert.RGBToLinearRGB

Converts **sRGB to linear RGB** where **rgb** is an **array** of the form
[r,g,b] where r, g, and b are integers between 0 and 255

Returns an array of the form [r,g,b] where r, g, and b are decimals between 0
and 1

##### Example usage
```javascript
tint.convert.RGBToLinearRGB([255, 255, 255]);
// Returns [0.003676507324047436,​​​​​​​​​​ 0.004024717018496307,​​​​ 0.024157632448504756 ]​​​​​
```

#### tint.getRelativeLuminance
Returns a decimal value representing the relative
[luminance](http://www.w3.org/TR/2008/REC-WCAG20-20081211/#relativeluminancedef)
of the given color.

Color must be an sRGB array of the form [r,g,b]

##### Example usage
```javascript
tint.getRelativeLuminance([255, 255, 255]); // Returns 0.9873055935982454​​​​​
```

#### tint.getContrastRatio
Returns the contrast ratio of the two given colors in fractional form.
Takes two parameters which must be sRGB arrays of the form [r,g,b]

##### Example usage
```javascript
tint.getContrastRatio([255,253,255], [1, 1, 1]); // Returns ​​​​​20.620931688099795
```

#### tint.randomColor
Returns a random RGB color in the form [r,g,b].

##### Example usage
```javascript
tint.randomColor(); // Returns ​​​​​[242,56,119]
```
