## Documentation

- Media Queries
- Functions
	- cd-palette
	- cd-zIndex
	- cd-fontFamily
	- cd-fontSize
	- cd-fontWeight
	- cd-lineHeight
- Grid System
- Container
- Tooltip
- Modal

## Media Queries
```
Media queries has two styles:
	1. Mobile First:	mobile friendly styles
		Sequence: portrait, smartphone, tablet, desktop, widescreen 
	
	2. Desktop First:	desktop friendly styles
		Sequence: widescreen, desktop, tablet, smartphone, portrait

@param $platformFirst:	mobile | desktop
@param $device:		portrait | smartphone | tablet | desktop | widescreen

Example:
@include cd-media(mobile, smartphone) { }
@include cd-media(desktop, smartphone) { }
```

##Functions
