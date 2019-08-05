# Setup
These two files are needed to use the scss framework.
```
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';
```

`main.scss` will let you use the following functions:
- [X] Color Palette: `cd-palette`
- [X] Z Index: `cd-zIndex`
- [X] Font Family: `cd-fontFamily`
- [X] Font Size: `cd-fontSize`
- [X] Font Weight: `cd-fontWeight`
- [X] Line Height: `cd-lineHeight`


## SCSS Usage

#### Color Palette
To define and use your own color palette, add it like:
```
$cd-custom: (
	1000: #000000,
	1001: #ffffff
);

body {
	color: cd-palette($cd-custom, 1000);
}
```

#### Property Functions
For other property functions, you can checkout the documentation to see how to use it in your project. In case, someone needs a custom list in any of these functions, then follow this `cd-fontFamily` example:
```
// font-family
$cd-custom-list: (
	comics-san:	'Comic Sans MS'
);

// added second argument for custom list
font-family: cd-fontFamily(comics-san, $cd-custom-list);
```


## Configuration

#### Angular
###### Use Inside SCSS Files
Include in your root scss file.
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors
```

###### Use Inside Component SCSS Files
Create a `main.scss` file inside `src/assets/scss` and include
```
// Functions
@import '../../../node_modules/@imransilvake/scss-framework/assets/scss/base/global';

// Colors (your color scss file)
@import 'colors';
```

Then set the following in `angular.json`
```
"styles": [
	"src/styles.scss"
],
"stylePreprocessorOptions": {
	"includePaths": [
		"src/assets/scss/"
	]
},
```

And in your `*.component.scss` file, you can use it like: 
```
@import 'main'; // short with the help of angular.json configuration

usage:
color: cd-palette($cd-color, 1001);
background-color: cd-palette($cd-background, 2017);
border-top: 1px solid cd-palette($cd-border, 3001, .1);
```

#### React Configuration
In your `styles.scss` / `app.scss` file, include:
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors
```
