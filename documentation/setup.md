# Setup
There are two files provided by scss framework.
```
@import '../node_modules/@imransilvake/scss-framework/dist/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';
```

`main.scss` will let you use the following functions:
- [X] Z Index: `cd-zIndex`
- [X] Font Size: `cd-fontSize`
- [X] Font Weight: `cd-fontWeight`
- [X] Line Height: `cd-lineHeight`


## Usage of Property Functions
For property functions, you can check the documentation to see how to use it in your project. 
An example to create a custom list of the above functions:
```
// font-size
$cd-custom-list: (
	s60:    60px,
	s61:    61px,
	s62:    62px
);

// add second argument for custom list
font-size: cd-fontSize(comics-san, $cd-custom-list);
```


## Configuration

#### Angular & React
Include in your root scss file.
```
// scss framework
@import '../node_modules/@imransilvake/scss-framework/assets/scss/main.scss';
@import '../node_modules/@imransilvake/scss-framework/dist/css/main.min.css';
```
