## Documentation

#### CORE
- [X] Normalize CSS
- [X] Media Queries
	- [X] Mobile First
	- [X] Desktop First
- [X] Container
- [X] Grid System
- [X] Properties Functions
	- [X] Color Palette: `cd-palette`
	- [X] Z Index: `cd-zIndex`
	- [X] Font Family: `cd-fontFamily`
	- [X] Font Size: `cd-fontSize`
	- [X] Font Weight: `cd-fontWeight`
	- [X] Line Height: `cd-lineHeight`
- [X] Typography
- [X] Utilities
- [X] Helpers

#### WIDGETS
- [X] Tooltip
- [X] Modal


## Normalize CSS
For improved cross-browser rendering, [Normalize.css](https://necolas.github.io/normalize.css/) is used, a project by Nicolas Gallagher and Jonathan Neal.


## Media Queries

#### Break Points `(pixels)`
```
widescreen (w):		1201	- 	greater
desktop (d):		993 	- 	1200
tablet (t):		768 	- 	992
smartphone (s):		481 	- 	767
portrait (p):		0 	- 	480
```

#### Media Queries Styles
```
@param $platformFirst:	mobile | desktop
@param $device:		portrait | smartphone | tablet | desktop | widescreen
```

###### Mobile First `(mobile friendly styles)`
```
Order:			p -> s -> t -> d -> w

Example:
@include cd-media(mobile, portrait) { }
@include cd-media(mobile, smartphone) { }
@include cd-media(mobile, tablet) { }
@include cd-media(mobile, desktop) { }
@include cd-media(mobile, widescreen) { }
```

###### Desktop First `(desktop friendly styles)`
```
Order:			w -> d -> t -> s -> p

Example:
@include cd-media(desktop, widescreen) { }
@include cd-media(desktop, desktop) { }
@include cd-media(desktop, tablet) { }
@include cd-media(desktop, smartphone) { }
@include cd-media(desktop, portrait) { }
```


## Container
We need a containing element to wrap site contents and house our grid system. Containers are nestable.

#### Container Fluid
```
<div class="cd-container-fluid">content</div>
```

#### Container
```
widescreen		1200 - 30	=	1170px
desktop			992 - 30	=	962px

<div class="cd-container">content</div>
```


## Grid System
```
Columns: 		12
Gutter:		 	30px (15px on each side of a column)
Nestable: 		Yes
Offsets:		Yes (cd-col-offset-device-column)
Ordering:		Yes (cd-col-order-device-column)
```

#### Mobile First
```
<div class="row">
  <div class="cd-col cd-col-p-12 cd-col-s-12 cd-col-t-6 cd-col-d-4 cd-col-w-4">content</div>
  <div class="cd-col cd-col-p-12 cd-col-s-12 cd-col-t-6 cd-col-d-8 cd-col-w-8">content</div>
</div>
```

#### Desktop First
```
<div class="row">
  <div class="cd-col cd-col-w-4 cd-col-d-4 cd-col-t-6 cd-col-s-12 cd-col-p-12">content</div>
  <div class="cd-col cd-col-w-8 cd-col-d-8 cd-col-t-6 cd-col-s-12 cd-col-p-12">content</div>
</div>
```


## Properties Functions

#### Color Palette: `cd-palette`
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
###### NOTE: Here you can find the list of colors palette: [Color Palette](color-palette.md)

#### Z Index: `cd-zIndex`
```
A function for the property z-index.

@param $key:	normal | float | modal | loader

Example:
z-index: cd-zIndex(normal);
```

#### Font Family: `cd-fontFamily`
```
A function for the property font-family.

@param $key:	roboto

Example:
font-family: cd-fontFamily(roboto);
```

#### Font Size: `cd-fontSize`
```
A function for the property font-size.

@param $key:	h1 | h2 | h3 | h4 | h5 | h6 | p | span | a | body

Example:
font-family: cd-fontSize(h1);
```

#### Font Weight: `cd-fontWeight`
```
A function for the property font-weight.

@param $key:	100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900

Example:
font-family: cd-fontWeight(100);
```

#### Font Height: `cd-lineHeight`
```
A function for the property line-height.

@param $key:	1 | 1.1 | 1.2 | 1.3 | 1.4 | 1.5 | 1.6 | 1.7 | 1.8 | 1.9 | 2

Example:
font-family: cd-lineHeight(1);
```


## Typography

#### Default Color
```
color:			cd-palette($cd-color, 1009)
```

#### Font Family
```
roboto:			'Roboto'
```

#### Font Size
```
h1:			36px
h2:			30px
h3:			26px
h4:			22px
h5:			18px
h6:			15px
p:			15px
span:			15px
a:			15px
body:			15px
a:			15px
```

#### Line Height
```
body:			1.4
```

#### Font Weight
```
h1-h6:			400
a:			400
p:			300
span:			300
b:			700
```


## Utilities

#### Font Face
```
With @font-face rule, you do not have to use one of the 'web-safe' fonts anymore.

@param $keys: fontName, fontPath, fontWeight, fontStyle, fontExtentions

Example:
@include cd-fontFace('Roboto', './../../app/assets/fonts/roboto/Roboto-Thin', 100, null, woff2 woff);
```


## Helpers

#### Alignment
```
cd-left-align
cd-right-align
cd-center-align
```

#### Overflow
```
cd-hide-overflow
```

#### Visibility: Responsive Classes
```
cd-hide
cd-show
cd-visible
cd-hidden
```

![Visibility Chart](https://github.com/imransilvake/SCSS-Boilerplate/blob/master/documentation/resources/classes-visibility-chart.png)
```
You can combine one .ts-hide-*-up class with one .ts-hide-*-down class to show an element only on a given interval of screen sizes.

For example:
ts-hide-on-s-down & ts-hide-on-d-up: shows the element only on tablet viewport. 

Using multiple .ts-hide-*-up or .ts-hide-*-down classes is redundant and pointless.
```

#### Position
###### v: vertical, h: horizontal
```
cd-vh-center
cd-h-center
cd-v-center
```

## Widgets

- Tooltip: [Link](widgets/tooltip.md)
- Modal: [Link](widgets/modal.md)
- Navbar: [Link](widgets/navbar.md)
