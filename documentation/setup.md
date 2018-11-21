## Setup
Include the following in your root scss file.
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

## Color Palette
To define and use your own color palette, add it like:
```
$cd-custom: (
	1000: #000000,
	1001: #ffffff
);
```
Now you can use it with the following way:
```
body {
	color: cd-palette($cd-custom, 1000);
}
```


## Angular Configuration

#### To use inside scss files, include in `styles.scss`:
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors

// include your custom scss
```

#### To use inside component scss files, create a `main.scss` file inside `src/assets/scss` and include:
```
// Functions
@import '../../../node_modules/@imransilvake/scss-framework/assets/scss/base/global';

// Colors
@import 'colors';
```

(1) Then set the following in `angular.json`
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

(2) And in your `*.component.scss` file, you can use it like: 
```
@import 'main'; // short with the help of angular.json configuration

usage:
background-color: cd-palette($cd-background, 2017);
border-top: 1px solid cd-palette($cd-border, 3001, .1);
color: cd-palette($cd-color, 1001);
```

## React Configuration
In your `styles.scss`/`app.scss` file, include:
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors

// include your custom scss
```