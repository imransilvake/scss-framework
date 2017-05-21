## Documentation

- [X] Normalize CSS
- [X] Media Queries
- [ ] Properties Functions
	- [X] Color Palette: cd-palette
	- [X] Z Index: cd-zIndex
	- [ ] cd-fontFamily
	- [ ] cd-fontSize
	- [ ] cd-fontWeight
	- [ ] cd-lineHeight
- [ ] Grid System
- [ ] Container
- [ ] Tooltip
- [ ] Modal

## Normalize CSS
For improved cross-browser rendering, we use Normalize.css, a project by Nicolas Gallagher and Jonathan Neal.

## Media Queries
```
Media queries has two styles:
	1. Mobile First: mobile friendly styles
		Sequence: portrait, smartphone, tablet, desktop, widescreen 
	
	2. Desktop First: desktop friendly styles
		Sequence: widescreen, desktop, tablet, smartphone, portrait

@param $platformFirst:	mobile | desktop
@param $device:		portrait | smartphone | tablet | desktop | widescreen

Example:
@include cd-media(mobile, smartphone) { }
@include cd-media(desktop, smartphone) { }
```

## Properties Functions

###### Color Palette: cd-palette
```
A color palette having code values assigned to each color.

@param $palette:	color | background | border | shadow
@param $hex-code:	hexadecimal color code
@param $opacity:	0-1

Example:
color: cd-palette($cd-color, 1000);
background color: cd-palette($cd-background, 2000);
border: 1px solid cd-palette($cd-border, 3000);
box shadow: 1px 1px 1px cd-palette($cd-shadow, 4000);
```
Note: Here you can find the list of colors palette: [Color Palette](color-palette.md)

###### Z Index: cd-zIndex
```
A function for the property z-index.

@param $key:	normal | float | modal | loader

Example:
z-index: cd-zIndex(normal);
```

###### Font Family: cd-fontFamily
```
A function for the property font-family.

@param $key:	helvetica

Example:
font-family: cd-fontFamily(helvetica);
```
