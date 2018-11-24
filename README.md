# SCSS Framework
SCSS Framework is a pure minimal framework (no JavaScript) for building responsive, fast, robust, and adaptable web apps or sites. This framework is especially designed according to developer's need.


## Install Package
Read how to include it in your project: [Setup](https://github.com/imransilvake/SCSS-Framework/blob/feature/publish/documentation/setup.md)
```
npm install @imransilvake/scss-framework --save
or
yarn add @imransilvake/scss-framework
```


## CORE
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
- [X] Helpers

#### WIDGETS
- [X] Tooltip
- [X] Modal
- [X] Navigation

#### Utilities
- [X] Triangle


## Media Queries

#### Break Points `(pixels)`
```
widescreen (w):		1201	- 	greater
desktop (d):		993 	- 	1200
tablet (t):		768 	- 	992
smartphone (s):		481 	- 	767
mini (m):		0 	- 	480
```

#### Media Queries Styles
```
@param $platformFirst:			mobile | desktop
@param $device:				mini | smartphone | tablet | desktop | widescreen
@param $orientation: 			portrait | landscape (optional)
```

###### Mobile First `(mobile friendly styles)`
min-width is used in the media queries

```
@include cd-media(mobile, mini) { }
@include cd-media(mobile, smartphone) { }
@include cd-media(mobile, tablet) { }
@include cd-media(mobile, desktop) { }
@include cd-media(mobile, widescreen) { }

@include cd-media(mobile, mini, portrait) { }
@include cd-media(mobile, mini, landscape) { }
```

###### Desktop First `(desktop friendly styles)`
max-width is used in the media queries

```
@include cd-media(desktop, widescreen) { }
@include cd-media(desktop, desktop) { }
@include cd-media(desktop, tablet) { }
@include cd-media(desktop, smartphone) { }
@include cd-media(desktop, mini) { }

@include cd-media(desktop, smartphone, portrait) { }
@include cd-media(desktop, smartphone, landscape) { }
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

#### Mobile First `pm`
```
<div class="cd-row">
	<div class="cd-col cd-col-pm-m-12 cd-col-pm-s-12 cd-col-pm-t-6 cd-col-pm-d-4 cd-col-pm-w-4">content</div>
	<div class="cd-col cd-col-pm-m-12 cd-col-pm-s-12 cd-col-pm-t-6 cd-col-pm-d-8 cd-col-pm-w-8">content</div>
</div>
```

#### Desktop First `pd`
```
<div class="cd-row">
	<div class="cd-col cd-col-pd-m-12 cd-col-pd-s-12 cd-col-pd-t-6 cd-col-pd-d-4 cd-col-pd-w-4">content</div>
	<div class="cd-col cd-col-pd-m-12 cd-col-pd-s-12 cd-col-pd-t-6 cd-col-pd-d-8 cd-col-pd-w-8">content</div>
</div>
```


## Properties Functions

#### Color Palette: `cd-palette`
List of colors palette: [Color Palette](https://github.com/imransilvake/SCSS-Framework/blob/feature/publish/documentation/color-palette.md)
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

#### Z Index: `cd-zIndex`
```
A function for the property z-index.

@param $key:	hide | initial | normal | float | modal | loader
@param $list:	custom list (optional)

Example:
z-index: cd-zIndex(normal);
```

#### Font Family: `cd-fontFamily`
```
A function for the property font-family.

@param $key:	roboto | comics-san
@param $list:	custom list (optional)

Example:
font-family: cd-fontFamily(roboto);
```

#### Font Size: `cd-fontSize`
```
A function for the property font-size.

@param $key:	h1 | h2 | h3 | h4 | h5 | h6 | s10 - s20 | se1 - se6
@param $list:	custom list (optional)

Example:
font-family: cd-fontSize(h1);
```

#### Font Weight: `cd-fontWeight`
```
A function for the property font-weight.

@param $key:	100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900
@param $list:	custom list (optional)

Example:
font-family: cd-fontWeight(100);
```

#### Font Height: `cd-lineHeight`
```
A function for the property line-height.

@param $key:	1 - 2.2
@param $list:	custom list (optional)

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
h1:			2.5rem
h2:			2rem
h3:			1.75rem
h4:			1.5rem
h5:			1.25rem
h6:			1rem
p: 			15px
a:			15px
span:			15px
pre:			14px
code:			14px
blockquote:		15px
```

#### Line Height
```
body:			1.4
```

#### Font Weight
```
400: 			p, a, span
500: 			h1-h6
700: 			b, strong
```


## Helpers

#### Positions (vertical, horizontal)
```
cd-vh-center
cd-h-center
cd-v-center
```

#### Alignment
```
cd-left-align
cd-right-align
cd-center-align
```

#### Overflow
```
cd-hide-overflow
cd-disable-overflow
```

#### Opacity
```
cd-opacity-high		(hover effect: .5 -> 1)
cd-opacity-low		(hover effect: 1 -> .9)
```

#### Visibility: Responsive Classes
```
cd-hide
cd-show
cd-visible
cd-hidden
```

![Visibility Chart](https://raw.githubusercontent.com/imransilvake/SCSS-Framework/feature/publish/documentation/resources/classes-visibility-chart.png)

###### Important Information
- You can combine `.cd-hide-on-*-up` and `.cd-hide-on-*-down` classes to show an element only on a given interval of screen sizes.
- `cd-hide-on-s-down` & `cd-hide-on-d-up`: shows the element only on tablet viewport. 
- Using multiple `.cd-hide-on-*-up` or `.cd-hide-on-*-down` classes is redundant and pointless.

#### List Style
```
cd-remove-bullets
cd-remove-bullets-nested
```


## Widgets
- Tooltip: [Link](https://github.com/imransilvake/SCSS-Framework/blob/feature/publish/documentation/widgets/tooltip.md)
- Modal: [Link](https://github.com/imransilvake/SCSS-Framework/blob/feature/publish/documentation/widgets/modal.md)
- Navbar: [Link](https://github.com/imransilvake/SCSS-Framework/blob/feature/publish/documentation/widgets/navbar.md)


## Utilities

#### Triangle
```
@include cd-triangle();

Default:
@param $size: 		105px
@param $direction: 	'bottom-left'
@param $pueudo:		false
@param $color:		transparent

Directions:
@include cd-triangle(60px, 'bottom-left');
@include cd-triangle(80px, 'bottom-right');
@include cd-triangle(100px, 'top-left');
@include cd-triangle(120px, 'top-right');

Pueudo Classes: (before | after)
@include cd-triangle(140px, 'bottom-right', true);

Color:
@include cd-triangle(140px, 'bottom-right', cd-palette($cd-color, 1001));
```


## Support
If you like this clean and minimal scss framework, please give a star at the repository: [SCSS-Framework](https://github.com/imransilvake/SCSS-Framework). And if possible help me improve this framework so that more people can use it in the future.
