# She Templates

[View Demo](https://apennell.github.io/she-templates/)

**She Templates** is the most basic responsive site template needed for the girl who's ready to build an empire and needs to start right away!

By [Annie Pennell](http://anniepennell.com/) | [LinkedIn](https://www.linkedin.com/in/anniepennell/)


## Table of Contents

1. [Technologies](#technologies-and-dependencies)
2. [Getting Started](#getting-started)
3. [Code Structure](#code-structure)
    * [`index.html`](#indexhtml)
      * [`<!DOCTYPE html>`](#doctype-html)
      * [`HEAD`](#head)
      * [`BODY`](#body)
4. [HTML: Make it say what you want](#html-make-it-say-what-you-want)
    * [Tags](#elements)
    * [Attributes](#attributes)
5. [CSS: Make it look good](#css-make-it-look-good)
    * [Syntax](#syntax)
    * [Selectors and specificity](#selectors-and-specificity)
    * [Common CSS properties](#common-css-properties)
    * [CSS variables](#css-variables)
    * [Responsiveness](#responsiveness)
6. [Javascript: Make it do cool stuff](#javascript-make-it-do-cool-stuff)
7. [Materialize CSS](#materialize-css)
8. [Customizing your site](#customizing-your-site)
    * [Colors and fonts](#colors-and-fonts)
    * [Navigation bar](#navigation-bar)
    * [Header](#header)
    * [Additional content](#additional-content)
    * [Icons](#icons)
9. [Releasing your site](#releasing-your-site)
10. [Making your site do even more](#making-your-site-do-even-more)
11. [Alternatives to coding your own](#alternatives-to-coding-your-own)


## Technologies and Dependencies

This simple boilerplate uses HTML, CSS, Javascript, [jQuery](https://jquery.com/), and [Materialize](https://materializecss.com/).

[To top :arrow_up:](#she-templates)


<!-- TODO: expand on specifics/ensure this works -->
## Getting Started

1. [Clone locally](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository) using `git clone https://github.com/apennell/she-templates.git`, or simply download
2. Open the `she-templates` directory in your favorite text editor (my favorite is [Sublime Text](https://www.sublimetext.com/3))
3. Add content to the `index.html` file, style it up in the `styles/style.css` file, or even make it do anything you can imagine by adding JavaScript to `scripts/script.js`!
4. To view your changes, open `index.html` in your web browser

[To top :arrow_up:](#she-templates)


## Code Structure

* **`README.md`**
  * Includes information about your project, instructions on how to get the code running, etc.
  * Good practice to include if someone else is going to be looking at your code—or even for your future self!
* **`index.html`**
  * Where we put our main content
  * HTML describes the content and structure of a web page, and is the standard markup language for web pages
* **`/styles`**
  * Where we put our CSS files, which is how we style our HTML content
  * CSS is a language that describes how the web browser should display an HTML document’s content
  * Can include custom CSS files, eg `style.css`
  * Can include imported CSS files from other libraries, eg `materialize.min.css` and `materialize.css`
* **`/scripts`**
  * Where we put our JavaScript code, which makes our site interactive
  * JavaScript is a language that allows us to program the behavior of web pages
  * Can include custom JS files, eg `script.js`
  * Can include imported JS files from other libraries, eg `materialize.min.js` and `materialize.js`
* **`/images`**
  * Where we put any images that we want to save and display

### `index.html`
Basic structure of an HTML document:
```html
<!DOCTYPE html>
<html>
<head>
  <!-- <meta> info -->
  <!-- <title> -->
  <!-- import CSS files and fonts -->
</head>
<body>
  <!-- page content -->
  <!-- import scripts -->
</body>
</html>
```

#### `<!DOCTYPE html>`
`DOCTYPE` tells the browser how to interpret the document so it can display the content correctly.
Start your document with `<!DOCTYPE html>` to indicate that it's using HTML5, the latest version of HTML.

#### `<html>`
This is the root element of an HTML page.

#### `<head>`

* Wraps around all elements that aren't actual page content
* `<meta>` tags allow us to pass certain information that the browser needs to know
* `<title>` lets the browser know the site's name, which is used in the browser's title bar or page's tab
* `<link>` tag lets us import CSS files and fonts--either from local files (relative links) or
cloud-hosted sources (absolute links)
* You may add any scripts that are needed immediately when browser starts loading here, but for
improved performance, add scripts at the end of `body` wherever possible so that the content isn't
held up before beginning to render

#### `<body>`

* Page content that will render in the browser
* Import scripts at the bottom, before closing `</body>`

[To top :arrow_up:](#she-templates)


## HTML: Make it say what you want

### Tags

* Tell the browser how to format our content
* Need to start with an opening `<tag>` and end with a closing `</tag>`:
  ```html
  <div>
    <h1>Title</h1>
    <p>Content here</p>
  </div>
  ```
* Determine which tag to use by the purpose of the content. Common examples include:
  * `body`: this is used once and all tags are nested within this; to apply a style to all elements on a page, target `body`
  * `div`: a multipurpose tag that allows you to group and style multiple HTML elements together:
    ```html
    <div class="image-container">
      <img src="images/logo.png">
      <p>Image caption</p>
    </div>
    ```
  * Semantic tags, which say something useful about the content they contain and are helpful for
  developers understanding code and for screen readers rendering accessible code, eg:
    * `nav`, `main`, `footer`
    * `section`, `article`
  * Individual elements:
    * `p`: paragraph text
    * `h1`, `h2`, `h3`, `h4`, `h5`, `h6`: headings of diminishing size
    * `a`: a link; must include `href` attribute, set to the url to navigate to when clicked, eg:
    `<a href="http://sheleads.io/">`
    * `button`: styled as a button and should receive instructions of what to do when clicked
    * `img`: renders an image; should receive `src` attribute, set to the url or relative link
    where the image can be found, eg:
    `<img src="images/logo.png" class="brand-logo">`
  * `span`: can be used inside of an element tag to style a specific part of it, eg:
  `<p>This is <span class="bold">some</span> text.</p>`
  * `input`/form elements


### Attributes
* Attributes are like options that you can send to an HTML element, like:
  * class
  * id
  * type (eg, input type)
* `class` and `id` let you group and name tags, which can then be used to target with CSS and JavaScript.

[To top :arrow_up:](#she-templates)


## CSS: Make it look good
CSS controls the style of the HTML content

#### Syntax
```css
.primary-bg {
  background-color: #ba68c8;
}

h1, h2 {
  color: #ffffff;
  font-family: 'Libre Baskerville', serif;
}
```
* Every CSS rule-set contains at least one selector (`.primary-bg`) pointing to a declaration block (the curly braces `{}`)
* A declaration block contains one or more declarations separated by semicolons: `background-color: #ba68c8`
* A declaration includes a CSS property name (`color`, `font-family`) and value (`#ffffff`, `'Libre Baskerville', serif`), separated by a colon

#### Selectors and specificty
CSS stands for "Cascading Style Sheets" and "cascading" refers to how the language handles deciding
which rule to abide when multiple rules apply to one element. It follows this hierarchy:
  1. id, eg `#header-1`
  2. class, eg `.header-group`
  3. HTML tag type, eg `header`

Given the following HTML and CSS, what color do you think "Title" will be?
```html
<header id="header-1" class="header-group">Title</header>
```
```css
#header-1 {
  color: red;
}
.header-group {
  color: purple;
}
header {
  color: blue
}
```

The answer is red! Although all 3 CSS rules target the same element, `#header-1` wins with the greatest specificity. *However*, it's best to avoid using id for CSS and use classes or HTML tag types wherever possible.


#### Common CSS Properties

* display, position
* padding and margin
* text formatting
* colors: named, hex, rgb/rgba


#### CSS variables

* CSS variables allow us to define a property in one place and reuse it in many places.
<!-- TODO: expand on this -->


#### Responsiveness
Responsive design allows a site to look good on any device, regardless off the screen/browser size.
We can use CSS to make the appearance of our content adapt well to different browser widths, so that
it looks just as good on a phone as it does on a large desktop computer.

By applying a `media query`, we can specify at what browser size a certain style will apply.
For example:
```css
h1 {
  font-size: 40px;
}

@media (max-width: 720px) {
  h1 {
    font-size: 24px;
  }
}
```
The above code will set the font-size of all `h1` elements to `24px` if the browser is 720px wide
or smaller; if it's wider than 720px, it will be `40px`.

We always want to look at our website at many different browser widths, all the way down to common
mobile sizes. An iPhone X, for example, is 375px wide, while an iPad is 768px wide.

[To top :arrow_up:](#she-templates)


### JavaScript: Make it do cool stuff

JavaScript makes the page interactive. We can add this functionality between `<script></script>` tags at the bottom of the `<body>` tag in index.html, but if we have a lot, it's best to abstract it into a separate JavaScript file. You may even choose to create multiple JS files so that the code is more manageable, organized, and contained.

**jQuery** is a JavaScript library that provides utility functions for common chunks of code used
in JavaScript so we can skip to the fun stuff. When we use `$`, we're calling jQuery.
In order to use it, though, we need to import the library! That's what we're doing at the bottom of
index.html with `<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>`.
Because loading the library takes work, you only want to include it if you need and are using it.
The Materialize CSS library we're using requires it for actions like opening the mobile menu, but
if you're not using Materialize's JavaScript helpers and not using jQuery yourself, then remove
that link from index.html for a slightly faster load time.

[To top :arrow_up:](#she-templates)


## Materialize CSS

This template is using a CSS framework called `[Materialize CSS](https://materializecss.com/)`. Although we could do it all from scratch, CSS frameworks provide helpful startpoints for common code. In addition, the framework is based on Google's [Material Design](https://material.io), which has [guidelines](https://material.io/design/) you can follow to create a great looking site even if you don't have design experience.
Some very useful parts of Materialize include:
* [Grid](https://materializecss.com/grid.html) makes it easy to lay out rows and columns that change responsively so that the content looks good on any screen size
* [Helpers](https://materializecss.com/helpers.html) provide quick solutions to common CSS issues, like vertical alignment, hiding and showing content, and text truncation.
* [Styled buttons](https://materializecss.com/buttons.html)
* [Navbar](https://materializecss.com/navbar.html), which functions well on mobile device and desktop browsers
* [Icons](https://materializecss.com/icons.html)
* [Modals](https://materializecss.com/modals.html) open a smaller window above the other content for dialog boxes, confirmations, or additional content
* [Styled form components](https://materializecss.com/text-inputs.html)

If you don't want to use Materialize CSS, delete the JavaScript files (materialize.min.js and materialize.js) from `/scripts`, delete the CSS files (materialize.min.css and materialize.css), and remove the `<link>` to that stylesheet and `<script>` to that script file from index.js.

A popular alternative to consider is Twitter's [Bootstrap](https://getbootstrap.com/).

[To top :arrow_up:](#she-templates)


## Customizing your site

### Colors and fonts
<!-- TODO expand on this -->


### Navigation bar

* `nav` element
<!-- TODO expand on this -->


### Header
<!-- TODO expand on this -->


### Additional content
<!-- TODO expand on this -->


### Icons
* All of [Google's Material Design icons](https://material.io/resources/icons/?style=baseline) are
available because we imported them into the `HEAD` of our Index.html file using a CDN link. Search
for [all options here](https://material.io/resources/icons/?style=baseline).
* Another popular option is [Font Awesome](https://fontawesome.com/). If you'd like to use this
instead, remove `<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">`
from the `HEAD` of Index.html so that you don't import unnecessary code.

[To top :arrow_up:](#she-templates)


## Releasing your site
* [TODO: gitpages]

[To top :arrow_up:](#she-templates)


## Making your site do even more
* `create-react-app`
* Node.js
* Ruby on Rails

[To top :arrow_up:](#she-templates)


## Alternatives to coding your own from scratch
* Wordpress
* Squarespace
* Wix

[To top :arrow_up:](#she-templates)
