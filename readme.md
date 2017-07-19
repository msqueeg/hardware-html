# Hartville Hardware HTML Development Toolkit

This toolkit is intended to help web developers write html and css that will be compatible with Hartville Hardware's current stylesheet. This readme contains a few notes for creating html and css that can be easily incorporated into our system.

## Custom HTML
custom markup should go in `index.html` inside the content div:
```html
<div id="content">
	<div id="breadcrumb"><a href="/">Home</a>&nbsp;»&nbsp;template</div>
	<div id="custom-id here">
	  <!-- insert custom page markup here, replace 'custom-id here' with your own id attribute -->
	</div><!-- /custom-id -->
</div>
```
### Responsive Video markup

To display videos using the existing css, wrap the iframe tag with the _videoWrapper_ class:

```html
<div class="videoWrapper">
	<iframe width="1280" height="720" src="https://www.youtube.com/embed/1_DqrpZeR1Y?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>
</div>
```
also note the "rel=0&amp;showinfo=0"

### Responsive column markup:

The following is an example of a multi-column layout that is supported in the current CSS. Our stylesheet currently supports 3 and 4 column layouts using classnames with the general pattern of *span_x_of_y*

```html
<div class="section group">
	<div class="col span_3_of_4">
		<!-- content here -->
	</div>
	<div class="col span_1_of_4">
		<!-- content here -->
	</div>
</div>
```

## Images
project images should be placed in a project specific folder underneath `/
images/campaigns`.

Images can be optimized using free online services such as:
+[tinypng](https://tinypng.com/)
+[jpeg.io](https://www.jpeg.io/)

Image urls must be local, external image urls are not supported in our shopping cart platform.

## CSS & Javascript
project specific css should go in `css/main.css`.

project specific js should go in `downloads/js/main.js`.

## Fonts
if your project requires custom fonts, we support either Typekit fonts or custom web fonts can be placed in `/downloads/fonts` and referenced in the stylesheet.


