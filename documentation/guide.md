## Documentation

- [X] Normalize CSS
- [X] Media Queries
- [X] Container
- [X] Grid System
- [X] Properties Functions
	- [X] Color Palette: `cd-palette`
	- [X] Z Index: `cd-zIndex`
	- [X] Font Family: `cd-fontFamily`
	- [X] Font Size: `cd-fontSize`
	- [X] Font Weight: `cd-fontWeight`
	- [X] Line Height: `cd-lineHeight`
- [ ] Tooltip
- [ ] Modal


## Normalize CSS
For improved cross-browser rendering, Normalize.css is used, a project by Nicolas Gallagher and Jonathan Neal.


## Media Queries
```
Break Points: (in pixels)
	widescreen:		1201	- 	greater
	desktop:		993 	- 	1200
	tablet:			768 	- 	992
	smartphone:		481 	- 	767
	portrait:		0 	- 	480

Media queries has two styles:
	1. Mobile First: mobile friendly styles
		Sequence (top to bottom): portrait, smartphone, tablet, desktop, widescreen 
	
	2. Desktop First: desktop friendly styles
		Sequence (top to bottom): widescreen, desktop, tablet, smartphone, portrait

@param $platformFirst:	mobile | desktop
@param $device:		portrait | smartphone | tablet | desktop | widescreen

Example:
@include cd-media(mobile, smartphone) { }
@include cd-media(desktop, smartphone) { }
```


## Container
We need a containing element to wrap site contents and house our grid system. Containers are nestable.

```
widescreen			1200 - 30	=	1170px
desktop				992 - 30	=	962px
```


## Grid System
```
Columns: 			12
Gutter(margin): 		30px (15px on each side of a column)
Nestable: 			Yes
Offsets:			Yes
Column ordering:		Yes
```

###### Example:
- Mobile First

```
<div class="row">
  <div class="cd-col cd-col-p-12 cd-col-s-12 cd-col-t-6 cd-col-d-4 cd-col-w-4">content</div>
  <div class="cd-col cd-col-p-12 cd-col-s-12 cd-col-t-6 cd-col-d-8 cd-col-w-8">content</div>
</div>
```

- Desktop First

```
<div class="row">
  <div class="cd-col cd-col-w-4 cd-col-d-4 cd-col-t-6 cd-col-s-12 cd-col-p-12">content</div>
  <div class="cd-col cd-col-w-8 cd-col-d-8 cd-col-t-6 cd-col-s-12 cd-col-p-12">content</div>
</div>
```


## Properties Functions

###### Color Palette: `cd-palette`
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

###### Z Index: `cd-zIndex`
```
A function for the property z-index.

@param $key:	normal | float | modal | loader

Example:
z-index: cd-zIndex(normal);
```

###### Font Family: `cd-fontFamily`
```
A function for the property font-family.

@param $key:	helvetica

Example:
font-family: cd-fontFamily(helvetica);
```

###### Font Size: `cd-fontSize`
```
A function for the property font-size.

@param $key:	h1 | h2 | h3 | h4 | h5 | h6 | p | span

Example:
font-family: cd-fontSize(h1);
```

###### Font Weight: `cd-fontWeight`
```
A function for the property font-weight.

@param $key:	100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900

Example:
font-family: cd-fontWeight(100);
```

###### Font Height: `cd-lineHeight`
```
A function for the property line-height.

@param $key:	1 | 1.1 | 1.2 | 1.3 | 1.4 | 1.5 | 1.6 | 1.7 | 1.8 | 1.9 | 2

Example:
font-family: cd-lineHeight(1);
```

## Widgets

- ######Tooltip: [Link](widgets/tooltip.md)
