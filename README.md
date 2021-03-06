# The Range Styles
The public stylesheets for [The Range](http://www.therange.co.uk) website. [Bootstrap v3](http://bootstrapdocs.com/v3.0.0/docs/) is used as a grid framework and custom imports are made on components as required. The Range styles are made with Sass at its core. It makes developing systems-based CSS faster, easier, and more fun.

Sass has two syntaxes. The most commonly used syntax is known as “SCSS” (for “Sassy CSS”), and is a superset of CSS3’s syntax. This means that every valid CSS3 stylesheet is valid SCSS as well. SCSS files use the extension .scss; we use this version for The Range.


#### The styleguide is a great place to view all currently deployed components 

* **[Public Living Styleguide](https://therange.co.uk/styleguide)**
* **This repo also has a local version of the styleguide at it's root `styleguide.html`**

## Getting Started

Ensure **compass** is already installed ([install compass](http://compass-style.org/install)).

Compass will compile `.scss` files in the `/sass` directory and place the generated complied `.css file` into the root directory as `main.css`. 

## Usage

```javascript
compass watch
```

Type: `Boolean`

Running `compass watch` will use Compass' native watch command to listen for changes to Sass files and recompile your CSS on changes. While much faster than running `compass compile` each time you want to compile your Sass, Compass becomes a blocking task. 

```javascript
compass clean
```

Type: `Boolean`

Running `compass clean` will delete all auto generated compass files in the outputted directory.

### Options

`The config.rb` file is the brain of a Compass project. It defines the relationship between files and their assets, how and where the CSS should be generated, and any dependencies for a project.

You can select your preferred output style here (can be overridden via the command line):
`output_style = :expanded or :nested or :compact or :compressed`
`output_style = :compressed`

To enable relative paths to assets via compass helper functions. Uncomment:
`relative_assets = true`

To disable debugging comments that display the original location of your selectors. Uncomment:
`line_comments = false`


If you prefer the indented syntax, you might want to regenerate the
project again passing `--syntax sass`, or you can add the following to the config:
`sass-convert -R --from scss --to sass sass scss && rm -rf sass && mv scss sass`

## CSS Architecture & Naming Convention

The naming convention used is [BEM — Block Element Modifier](http://getbem.com/). It is a methology that helps create reusable components and code sharing in front-end development.

The `main.scss` file is used to import `components`, `modules`, `partials` and `vendor` folders into it's main structure.


```css
scss
├── components
│   ├── _all-components.scss
│   ├── _attribute-select.scss
│   ├── _back-to-top.scss
│   ├── _banner.scss
│   ├── _cards.scss
│   ├── _checkout_header.scss
│   ├── _footer.scss
│   ├── _fultilment.scss
│   ├── _full-width-slider.scss
│   ├── _header-controls.scss
│   ├── _header-controls.scss
│   ├── _horizontal-product.scss
│   ├── _landing-page.scss
│   ├── _like.scss
│   ├── _navigation.scss
│   ├── _overlay-modal.scss
│   ├── _postcode-lookup.scss
│   ├── _like.scss
├── modules
│   ├── _base.scss
│   ├── _basket-add.scss
│   ├── _content.scss
│   ├── _delivery.scss
│   ├── _faq.scss
│   ├── _footer.scss
│   ├── _grids.scss
│   ├── _masthead.scss
│   ├── _my-account.scss
│   ├── _product-display.scss
│   ├── _product-display.scss
│   ├── _product-list.scss
│   ├── _store-finder.scss
│   ├── _style-guide.scss
├── vendor
│   ├───── bootstrap
│   ├── _slick-theme.scss
│   ├── _slick.css.scss
├── main.scss
```

### Components
Components are small, self-contained files that concern one type of thing, that crucially, are reusable. For example, lists, forms etc. We have included quite a few in the components directory: buttons & forms for example, but you should add your components there too. Please browse through the included components to see what Kickoff offers, or see some of them in action in our demo area.

### Partials
Partials are partial parts of a page, like a masthead, sidebar or footer. They typically have multiple ‘components’ inside them and can also be reusable. The partials directory should contain style partials.

### Modules
Directory reserved for Sass code that doesn't cause Sass to actually output CSS. Things like mixin declarations, functions and variable.
