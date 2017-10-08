# The Range Styles
The public stylesheets for [The Range](http://www.therange.co.uk) website.


* **[Public Living Styleguide](https://therange.co.uk/styleguide)**

## Getting Started

Ensure **compass** is already installed ([install compass](http://compass-style.org/install)).

Then just use **npm**:

```javascript
npm install compass
```

## Usage

#### watch

Type: `Boolean`

Running `compass watch` will use Compass' native watch command to listen for changes to Sass files and recompile your CSS on changes. While much faster than running `compass compile` each time you want to compile your Sass, Compass becomes a blocking task. 

#### clean

Type: `Boolean`

Running `compass clean` will delete all auto generated compass files in the outputted directory
. 

## CSS Architecture

The methodology and ideas behind The Range stylehseet and structure are documented within the _base.scss.


```css
/*
A button suitable for giving stars to someone.

:hover             - Subtle hover highlight.
.stars-given       - A highlight indicating you've already given a star.
.stars-given:hover - Subtle hover highlight on top of stars-given styling.
.disabled          - Dims the button to indicate it cannot be used.

Styleguide 2.1.3.
*/
a.button.star{
  ...
}
a.button.star.stars-given{
  ...
}
a.button.star.disabled{
  ...
}
```