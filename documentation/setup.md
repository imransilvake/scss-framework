## Setup

#### Initial
First create a `_colors.scss` file under `src/assets/scss` with the following content (you can extend the colors later).
```
// Color
$cd-color: (
	1000: #000000,
	1001: #ffffff
);

// Background Color
$cd-background: (
	2000: #000000,
	2001: #ffffff
);

// Border
$cd-border: (
	3000: #000000,
	3001: #ffffff
);

// Box Shadow
$cd-shadow: (
	4000: #000000,
	4001: #ffffff
);
```

#### Angular Configuration
###### To use inside scss files, include in `styles.scss`:
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors

// include your custom scss
```

###### To use inside component scss files, create a `main.scss` file inside `src/assets/scss` and include:
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

#### React Configuration
In your `styles.scss`/`app.scss` file, include:
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';

// import your color scss file
@import 'assets/scss/colors

// include your custom scss
```