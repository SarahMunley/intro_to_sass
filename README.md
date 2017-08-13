# Intro to Sass

> Using Sass (scss) to build a basic Style Guide


## Installing Sass

Install **Ruby** :gem: on your computer: `brew install ruby` (Windows users will need to install Ruby from an installer online).
To globally install Sass on your computer, run `gem install sass`.

## Watching a File

We can watch our Sass files so they are automatically converted to usuable CSS. To do so, we run the following command in the same folder as our SCSS files:

`sass -w your_file.scss` **or**  `sass --watch your_file.scss:compiled_css_file.css`
Where we say **sass** please listen for changes in **your_file.scss** and output the changes to **compiled_css_file.css*

## Variables

To create and re-use variables:

```scss
$my_variable: 0px;
$my_other_variable: black;

body {
  font-size: $my_variable;
  color: $my_other_variable;
}
```

## Importing other SCSS files

We can import other SCSS files for code organization!

**variables.scss**
```scss
$my_variable: 0px;
$my_other_variable: black;
```

**style.scss**
```scss
@import 'variables.scss';

body {
  font-size: $my_variable;
  color: $my_other_variable;
}

```

## Comments
```scss
// sass allows us to use JS style comments... these won't be compiled into the CSS file
```

# Style Guide & Font Example

#### Rule of Thumb for Style Guides

Note that every style guide is unique. This is just a good starting point.

  * Headline Text: 300%
	* B-Head (sub) text: 150%
	* Nav Item: 100%
	* Body copy (text): 100% - starting point could be `body { font-size: 16px }`
  * Byline: 75%

#### Examples with Sass variables

* `1rem` = 100%
* `rem` is responsive and related to the `root` of the page.

```scss
// style guide variables

$headline-text: 3rem; // 300%
$body-text: 1rem;   // 100%
$nav-item: 1.25rem; // 125%
$sub-header: 1.50rem; // 150%
$byline: 0.75rem; // 75%

body {
  font-size: 16px;
}
```

## References
* Sass Guide: http://sass-lang.com/guide
* Sass Meister (validator): http://sassmeister.com/
