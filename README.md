# SCSS Boilerplate
SCSS Boilerplate is a professional front-end template for building fast, robust, and adaptable web apps or sites.

[![Scrutinizer Build](https://img.shields.io/scrutinizer/build/g/filp/whoops.svg)](https://github.com/imransilvake/SCSS-Boilerplate/)
[![David](https://img.shields.io/david/expressjs/express.svg)](https://github.com/imransilvake/SCSS-Boilerplate)
[![David](https://img.shields.io/david/dev/expressjs/express.svg)](https://github.com/imransilvake/SCSS-Boilerplate)
[![GitHub issues](https://img.shields.io/github/issues/imransilvake/SCSS-Boilerplate.svg)](https://github.com/imransilvake/SCSS-Boilerplate/issues)
[![Software License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## SCSS
  - Lint SCSS: [Rules](https://stylelint.io/user-guide/rules/)
  - Compile SCSS to CSS
  - Add autoprefixer
  - Minify CSS
  - Auto update on changes in HTML & SCSS files

## Project Prefix
`cd`

## Requirements
```
node: v7.9.0 or greater
npm: v4.2.0 or greater
```

## Run
```
npm install
```
```
npm run scss-compile

OR

npm run scss-watch
```

## Functions

`npm run scss-compile`
  - SCSS Lint, SCSS-to-CSS, Add Autoprefixer, Minfiy CSS

`npm run scss-watch`
  - `npm run scss-compile` + Watch HTML & SCSS files

## Note
Bootstrap framework is included.

## Mixins and Functions
```javascript
	- A color palette having code values assigned to each color.
	@param $palette:	color | background | border | shadow
	@param $hex-code:	hexadecimal color code
	@param $opacity:	0-1
	cd-palette($palette, $hex-code, $opacity);

	- Media queries are used to target designs for many standard and popular devices.
	@param $media:	portrait | smartphone | tablet | desktop | widescreen
	cd-media($break-point);

	- Mixin for the property z-index.
	@param $key:	normal | float | modal | loader
	cd-zIndex($key)

	- Mixin for the property font-family.
	@param $key:	helvetica
	cd-fontFamily($key);

	- Mixin for the property font-size.
	@param $key:	h1 | h2 | h3 | h4 | h5 | h6 | p
	cd-fontSize($key);
```

## License
MIT
