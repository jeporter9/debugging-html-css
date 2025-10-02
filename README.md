# Debugging Results

## HTML Errors and Warnings

- Warning: This document appears to be written in English. Consider adding lang="en" (or variant) to the html start tag.
<!-- <html> -->
<html lang="en-US">

- Error: Element meta is missing one or more of the following attributes: charset, content, http-equiv, itemprop, name, property.
<!-- <meta> -->
<meta charset="UTF-8">

- Info: Trailing slash on void elements has no effect and interacts badly with unquoted attribute values.
<!-- <meta name="viewport" content="width=device-width, initial-scale=1.0" /> -->
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 

- Error: Layout CSS doesn't have the correct path and therefore doesn't load/apply to the site.
<!-- <link rel="stylesheet" href="layout.css"> -->
<link rel="stylesheet" href="css/layout.css">

- Error: The second import font style is a duplicate.
/* @import url('https://fonts.googleapis.com/css2?family=Architects+Daughter&family=Love+Ya+Like+A+Sister&display=swap'); */

- Error: An img element must have an alt attribute, except under certain conditions. For details, consult guidance on providing text alternatives for images.
-- Also, the image path wasn't properly set so it wasn't loading.
<!-- <img src="easter-bunny-150-profile.png"> -->
<img src="..\images\easter-bunny-150-profile.png" alt="easter bunny">

- Misuse/styling error: The wrong headings (h4/h5) were being used instead of h3.
<!-- <h4>The Easter Bunny</h4> -->
<h3>The Easter Bunny</h3>
<!-- <h5>Rabbits and Hares</h5> -->
<h3>Rabbits and Hares</h3>        


- Misuse Error: No <br>
<!-- <br><br><br><br><br> -->

- Error: Element p not allowed as child of element h3 in this context. (Suppressing further errors from this subtree.)
-- Element h3 is missing its closing tag, causing this error.
<!-- <h3>Enough Content
          <p>You need enough content to thoroghly populate your page. The content should cause the page to be long
            enough to need to scroll. Keep copy/pasting content from Wikipedia until you have enough content to scroll.
            You will use this page later to embellish it with styles, color, formatting and layouts.</p> -->
<h3>Enough Content</h3>
<p>You need enough content to thoroghly populate your page. The content should cause the page to be long enough to need to scroll. Keep copy/pasting content from Wikipedia until you have enough content to scroll. You will use this page later to embellish it with styles, color, formatting and layouts.</p>

- <!-- Closing body tag is/was missing -->
</body>  <!-- added by JP -->
</html>


## CSS Errors and Warnings
### style.css
- 33 	footer 	Value Error : color #B2 is not a valid color 3 or 6 hexadecimals numbers : #B2 
/* color: #B2; */
color: #B2D732;

- 43 	h1 	Value Error : font-size Too many values or values are not recognized : 5 vw 
-- There should no space between the 5 and the vw.
/* font-size: 5 vw; */
font-size: 5vw;
	

- 66 	p 	Value Error : line-height Unknown dimension 1.35me (corrected: 1.35em)
/* line-height: 1.35me; */
line-height: 1.35em;


- 88 	.error 	Value Error : color #FE27122 is not a valid color 3 or 6 hexadecimals numbers : #FE27122 
/* color: #FE27122; */
color: #FE2712;

- 97 	a:hover 	Value Error : text-decoration all is not a text-decoration value : all 
/* text-decoration: all; */
text-decoration: none;