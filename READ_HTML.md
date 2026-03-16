Advanced 1Features of HTML5 and CSS3
1. Editing content within the elements:
You can edit content within an element by using an HTML attribute called contenteditable. 
There is a CSS property -webkit-user-modify similar to contenteditable which determines whether or not a user can edit the content. 
The default value is always read-only and read-write value of -webkit-user-modify allows the user to edit the content. 
Here’s an example:

2
3
4	
<h2 contenteditable=true>You can edit me</h2>
h2{
-webkit-user-modify:read-write;
}
 

2. Form attribute required
This particular feature ensures that the form is not submitted if an input box with required attribute is empty.
The required attribute can also be used as a selector to style the element. 
Here’s an example:

 
1
2
3
4	<input type="text" name="required Field"  required="required">
input:required{
background:red;
}
 

3. Regular expressions
Verifying textbox is simple. 
For verifying any particular textbox, we can insert regular expression directly into an element. 
We can check a textbox value against the regular expression specified in the pattern attribute. 
Here’s an example
 
1	<input type="text"  name="rollno"  pattern="[0-9]{5}">
 
In the above example, input box should contain only five characters (the characters can only be numerals)

4. Figure tag
Figure tag includes figcaption tag through which we can associate captions with an image element. 
Apart from images, we can also include audio, video, chart, SVG, and canvas in the figure tag. 

. Video and Audio
Video and audio are the new tags which allow to embed a video in the website.
It helps the web to be more involved with multimedia. A new tag is also available in HTML5 and that is audio tag. Which is used to embed any audio in the web.

2. nav
The nav element is used for the part of a internet site that links to different pages at the website. The hyperlinks can be organized a number of approaches. 
below, the hyperlinks are displayed inside paragraph factors. An unordered list can also be used.

. header
The header element can be used to institution collectively introductory factors on a website, such as a business enterprise brand, navigation objects, and occasionally, a search form.

. canvas
Canvas is a tag of HTML which is newly introduced in HTML5. 
It is used to draw the images on the fly. It can be used for visual images, rendering graphs, game graphics.
The <canvas> element is a container that is used to draw graphics on the web page using scripting language like JavaScript. 
It allows for dynamic and scriptable rendering of 2D shapes and bitmap images.

5. footer
Footer is a tag, used to define the footer of a document or a section. 
Usually, it contains the information about author and copyright etc. 
Address tag may be used to mark up the contact information in the footer.
A document or section can have more than one footer.                            

6. New types for input tags
input is an attribute which is an old attribute but in HTML, it is reintroduced with new values like email, month, number, range, search, tel, color, week, url, time, date, datetime-local etc.
These are the new values which can be contain by the input tag.
•ContentEditable
It is an attribute which is used to permit the user to edit the content. It creates What You See What You Get so easy. Content will be editable by clicking on it.
•Progress
This tag is used to check the progress of a task during execution of that. Progress tag can used with the conjuction of JavaScript. It is like progress bar.
<progress value="22" max="100"></progress>
•section
Section tag is used to divide a document or in parts or sections. For example: An article can have many sections like header, footer, latest news and section for main content etc.
•main
main is a tag which is used to contain the main content of the page. 
More than one main tag is not accepted in the document and this tag can not be inside in article, aside, footer, header tags. 
It does not include the navigation bar, header and footer

Drag and drop – It supports to Drag and drop the items from one location to another location on the same Web page.
Name some new features which were not present in HTML but are added to HTML5?
Answer: Some new features in HTML5 include:
•DOCTYPE declaration: <!DOCTYPE html>
•section: Section tag defines a section in the document, such as a header, footer or in other sections of the document. It is used to define the structure of the document. <section></section>
•header: Header tag defines the head section of the document. A header section always sticks at the top of the document. <header></header>
•footer: Footer tag defines the footer section of the document. A footer section always sticks at the bottom of the document. <footer></footer>
•article: Article tag defines an independent piece of the content of a document. <article> </article>
•main: The main tag defines the main section in the document which contains the main content of the document. <main></main>
•figcaption: Figcaption tag defines the caption for the media elements such as an image or video. <figcaption></figcaption>

What are the different new form element types in HTML 5?
Following is a list of 10 frequently used new elements in HTML 5:
•Color
•Date
•Datetime-local
•Email
•Time
•Url
•Range
•Telephone
•Number
•Search


Q1. What is HTML?
HTML stands for Hyper Text Markup Language. 
It is a language of the World Wide Web. 
It is a standard text formatting language which is used to create and display pages on the Web. 
HTML makes the text more interactive and dynamic. 
It can turn text into images, tables, links.

HTML tag is just opening or closing entity. For example: <p> and </p> are called HTML tags
HTML element encompasses opening tag, closing tag, content (optional for content-less tags) Eg:
<p>This is the content</p> : This complete thing is called a HTML element

Name some common lists that are used when designing a page.
	Ordered list – The ordered list displays elements in a numbered format. 	It is represented by <ol> tag.
•Unordered list – The unordered list displays elements in a bulleted format. It is represented by <ul> tag.
•Definition list – The definition list displays elements in definition form like in a dictionary. The <dl>, <dt> and <dd> tags are used to define description list.

What is 1semantic HTML?
A semantic element clearly describes its meaning to both the browser and the developer.
Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.
Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.

In HTML there are some semantic elements that can be used to define different parts of a web page:  
•	<article>
•	<aside>
•	<details>
•	<figcaption>
•	<figure>
•	<footer>
•	<header>
•	<main>
•	<mark>
•	<nav>
•	<section>
•	<summary>
•	<time>

What is an image map?
An image map is used for linking many different web pages using a single image. 
It is represented by <map> tag. You can define shapes in images that you want to include as part of an image mapping.

Explain the layout of HTML.
	<header>: It is used to define a header for a document or a section.
•<nav>: This defines a container for navigation links
•<section>: It is used to define a section in a document
•<article>: This is used to define an independent, self-contained article
•<aside>: It is used to define content aside from the content
•<footer>: It is used to define a footer for a document or a section

What are the tags used to separate a section of texts?
There are three tags that can be used to separate the texts:
•<br> tag – Usually <br> tag is used to separate the line of text. It breaks the current line and conveys the flow to the next line
•<p> tag – This contains the text in the form of a new paragraph.
•<blockquote> tag – It is used to define a large quoted section. If you have a large quotation, then put the entire text within <blockquote>……….</blockquote> tag.

Is the <!DOCTYPE html> tag considered as a HTML tag?
No, the <!DOCTYPE html> declaration is not an HTML tag.
<!DOCTYPE html> is used to instruct the web browser about the HTML page.

What is the use of an 1iframe tag?
An iframe is used to display a web page within a web page.
The HTML <iframe> tag specifies an inline frame.
An inline frame is used to embed another document within the current HTML document.
Tip: It is a good practice to always include a title attribute for the <iframe>. This is used by screen readers to read out what the content of the iframe is.

An iframe is an HTML element that allows you to embed another website within your own page. While iframes can be useful for displaying external content within your website, they can also be used maliciously to display your website within a fake page or steal information from your website’s visitors.
Syntax:
X-Frame-Options: DENY
The X-Frame-Options header is used to control whether a website can be embedded in an iframe. It has 3 possible values.
•	DENY: Prevents the website from being embedded in any iframe, regardless of domain.
•	SAMEORIGIN: Allows the website to be embedded in iframes that are hosted on the same domain.
•	ALLOW-FROM uri: Allows the website to be embedded in an iframe that is hosted on a specified URI.

What is SVG?
Scalable Vector Graphics (SVG).
•The HTML5 <svg> element is a container for SVG graphics. It provides several methods for drawing boxes, paths, text, circles, and graphic images.
•SVG is beneficial as nowadays, people are using high-resolution devices (iPads and Monitors), so it becomes impressive as designs, logos, and charts scale according to the requirement, maintaining the picture quality.
•SVG is XML based, which means that every element is available within the SVG DOM. It treats every shape as an object. If the user changes the attributes of any SVG object, the browser will automatically re-render the shape.
•HTML SVG is used to describe the two-dimensional vector and vector/raster graphics. SVG images and their behaviors are defined in XML text files. So as XML files, you can create and edit an SVG image with the text editor.
• It is mostly used for vector type diagrams like pie charts, 2-Dimensional graphs in an X, Y coordinate system.
What is Cell Spacing and Cell Padding?
Cell Spacing is referred to as the space or gap between the two cells of the same table. Whereas, Cell Padding is referred to as the gap or space between the content of the cell and cell border.

Define attributes in HTML tag.
Answer: The HTML tag contains a field inside their tag which is called attributes of that tag.
For Example:
<img src=”#”> here in this tag src is img tag attributes.
<input type=” text”> here in this tag type is input tag attributes.


Can we modify the attribute's value of the HTML tag dynamically?
Answer: Yes, we can modify the value of the attributes by using JavaScript.
Below is the input element whose attribute will be modified from text to password, JS code to modify the attribute value:
 
<input type=“text” id=“inputField”>
document.getElementById(“inputField”).attr(“type”, “password”);
 

Why Meta tags are used in HTML?
Answer: Meta tags in HTML are used by the developer to tell the browser about the page description, author of the template, character set, keywords and many more.
Meta tags are used for search engine optimization to tell the search engine about the page contents.
 
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale = 1.0">
<meta name="description" content="HTML interview questions">
<meta name="author" content="Author Name">
<meta name="copyright" content="All Rights Reserved">

What is viewport in html?
The viewport is the user's visible area of a web page. 
It varies with the device - it will be smaller on a mobile phone than on a computer screen.
You should include the following <meta> element in all your web pages:
<meta name="viewport" content="width=device-width, initial-scale=1.0">
This gives the browser instructions on how to control the page's dimensions and scaling.
The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).
The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.
Before tablets and mobile phones, web pages were designed only for computer screens, and it was common for web pages to have a static design and a fixed size.
Then, when we started surfing the internet using tablets and mobile phones, fixed size web pages were too large to fit the viewport. To fix this, browsers on those devices scaled down the entire web page to fit the screen.
Differentiate between HTML and XHTML.
Answer: The differences between HTML and XHTML are:
•HTML stands for Hypertext Markup Language, whereas XHTML stands for Extensible Markup Language.
•A static webpage is an HTML web page and dynamic web pages are XHTML.
•XHTML are more stricter than HTML.
•An XML application of HTML is defined as XHTML.
•All modern browsers support XHTML.

What are Web Workers?
Answer: Web Workers is a code of JavaScript which runs in the background, independently of other scripts, without disturbing the performance of the page. 
It is used for computing-heavy tasks like an access database or function.

1Block Level and Inline Elements: The difference between <div> and <span>
HTML is made up of various elements that act as the building blocks of web pages. 
For the purpose of styling, elements are divided into two categories: 
1.	block-level elements 
2.	inline elements.
In summary, a <span> element is used as an inline element and a <div> element as a block level element.
Basically, an inline element does not cause a line break (start on a new line) and does not take up the full width of a page, only the space bounded by its opening and closing tag. 
It is usually used within other HTML elements.

Other examples of inline elements are:
•	anchor <a> tag
•	emphasis <em> tag
•	image <img> tag
•	Here are the inline elements in HTML:
•	<a>
•	<abbr>
•	<acronym>
•	<b>
•	<bdo>
•	<big>
•	<br>
•	<button>
•	<cite>
•	<code>
•	<dfn>
•	<em>
•	<i>
•	<img>
•	<input>
•	<kbd>
•	<label>
•	<map>
•	<object>
•	<output>
•	<q>
•	<samp>
•	<script>
•	<select>
•	<small>
•	<span>
•	<strong>
•	<sub>
•	<sup>
•	<textarea>
•	<time>
•	<tt>
•	<var>

A block-level element always starts on a new line and takes up the full width of a page, from left to right. 
A block-level element can take up one line or multiple lines and has a line break before and after the element.
Examples of the block-level tag are:
•	Heading tags <h1> to <h6>
•	List (Ordered, Unordered, Description and List Item) tags <ol> , <ul> ,<dl> , <li>
•	Pre-formatted text tag <pre>
•	<address>
•	<article>
•	<aside>
•	<blockquote>
•	<canvas>
•	<dd>
•	<div>
•	<dl>
•	<dt>
•	<fieldset>
•	<figcaption>
•	<figure>
•	<footer>
•	<form>
•	<h1>-<h6>
•	<header>
•	<hr>
•	<li>
•	<main>
•	<nav>
•	<noscript>
•	<ol>
•	<p>
•	<pre>
•	<section>
•	<table>
•	<tfoot>
•	<ul>
•	<video>
Difference between <b> & <Strong>
The difference between the two tags is that the bold tag is intended to draw attention to the text, while the strong tag also highlights the text semantically and indicates that this is an important word or section of text

https://codeengineered.com/blog/2013/html5-semantic-diff-bold-strong/

What is the difference between <p>, <div> and <span> in HTML&XHTML?

p and div elements are block level elements where span is an inline element and hence margin on span wont work. 
Alternatively you can make your span a block level element by using CSS display: block; or for span I would prefer display: inline-block;

Block elements start and end with a new line in the browser while inline elements do not. "Inline" means they are part of the current line.

<p> is a block level tag for paragraphs. <span> is a line level tag that in and of itself doesn’t do anything, but is useful for defining a specific style to a string.
<span> can be used within <p>, but <p> cannot be used within <span>

Tailwind 1CSS?
Tailwind CSS is a utility-first CSS framework that enables developers to quickly build modern and responsive user interfaces.
npm install tailwindcss postcss autoprefixer
// tailwind.config.js
module.exports = {
  content: [
    "./src/**/*.{js,ts,jsx,tsx}",
    "./public/index.html",
  ],
  theme: {},
  plugins: [],
};
/* src/index.css */
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';

Is it possible to change the color of the bullet?
The color of the bullet is always the color of the first text of the list. So, if you want to change the color of the bullet, you must change the color of the text.

Which type of video formats are supported by HTML5?
HTML 5 supports three types of video format:
•mp4
•WebM
•Ogg

Is audio tag supported in HTML 5?
Yes. It is used to add sound or music files on the web page. There are three supported file formats for HTML 5 audio tag.
1.mp3
2.WAV
3.Ogg

What is the difference between progress and meter tag?
The progress tag is used to represent the progress of the task only while the meter tag is used to measure data within a given range.
What is a marquee?
A marquee allows you to put a scrolling text in a web page. To do this, place whatever text you want to appear scrolling within the <marquee> and </marquee> tags.

what is difference between tag and element in html?
Tag: The individual markup that defines the start and end of an element, like <div>, </div>.
Element: The complete structure, including the opening tag, the content, and the closing tag (if any), like <div>Hello</div>.

How can we create a new HTML element?
Answer.
We can even create new elements for the document as follows.
<script>
document.createElement﴾"myElement"﴿
</script>
It can be used in the HTML as.
<myElement>hello</myElement>



What is the difference between HTML and 1DOM?
 

The Document Object Model (DOM) is a language-independent model made up of objects representing the structure of a document.
HTML is one language for writing such documents.
DOM is the tree model to represent HTML.

The HTML DOM (Document Object Model)
When a web page is loaded, the browser creates a Document Object Model of the page.
The HTML DOM model is constructed as a tree of Objects

Application Protocols: 1HTTP and the World Wide Web
One of the most commonly used services on the Internet is the World Wide Web (WWW). The application protocol that makes the web work is Hypertext Transfer Protocol or HTTP. 
Do not confuse this with the Hypertext Markup Language (HTML). HTML is the language used to write web pages. 
HTTP is the protocol that web browsers and web servers use to communicate with each other over the Internet. 
It is an application level protocol because it sits on top of the TCP layer in the protocol stack and is used by specific applications to talk to one another. In this case the applications are web browsers and web servers.
HTTP is a connectionless text based protocol. Clients (web browsers) send requests to web servers for web elements such as web pages and images. After the request is serviced by a server, the connection between client and server across the Internet is disconnected.

What is HTTPS and what does it do?
HTTPS takes the well-known and understood HTTP protocol, and simply layers a SSL/TLS (hereafter referred to simply as “SSL”) encryption layer on top of it. 
Servers and clients still speak exactly the same HTTP to each other, but over a secure SSL connection that encrypts and decrypts their requests and responses.
In short, both of these are protocols using which the information of a particular website is exchanged between Web Server and Web Browser. 
But what’s difference between these two? Well, extra s is present in https and that makes it secure!  
Very short and concise difference between http and https is that https is much more secure compared to http.
HTTP uses port number 80 for communication and HTTPS uses 443

CSS Overview of New Features
Box Shadow
box-shadow property that adds a shadow to an element. Instead of using multiple images around an item, this property lets you add shadow with a short line of code.
box-shadow: h-shadow v-shadow blur spread color;
div { box-shadow: 14px 22px 10px red; }

Opacity
The CSS opacity property is used to specify the transparency of an element.
opacity makes elements see-through or completely transparent.
For instance, you can apply opacity to images or other HTML elements. The transparency level depends on the indicated values.
div { opacity: 0.6; }
opacity: alpha;
The alpha level is a unitless number in the range from 0.0 (full CSS transparency) to 1.0 (full CSS opacity). 1.0 is also the default value of this property.
Another way to change the opacity for an element is using the filter property
div.first { opacity: 0.2; filter: alpha(opacity=20); /* For IE8 and earlier */ }
You can also define the color you want to use in RGBA or HSLA values. The A in the acronyms stand for the alpha channel which is defined as the fourth value.
The RGB value defines HTML color by mixing red, green, and blue values.
The value of each color can vary from 0 to 255.
While RGBA values are very similar, they have one more value in the mix. The additional fourth value A stands for alpha and represents the opacity. It can be defined in a number from 0 (not transparent) to 1 (completely transparent)
<h2 style="color: rgba(252, 156, 249, 0.25);"> RGBA values let you set custom opacity - compare these two lines </h2>
In HTML, colors can also be defined in HSL values. HSL stands for hue, saturation and lightness:
•Hue is defined in degrees from 0 to 360. On a color wheel, red is around 0/360, green is at 120 and blue is at 240.
•Saturation is defined in percentages from 0 (black and white) to 100 (full color).
•Lightness is defined in percentages from 0 (black) to 100 (white).
 in RGBA, the fourth value A in HSLA values stands for alpha and represents the opacity which defined in a number from 0 to 1
<h2 style="color: hsla(128, 95%, 25%, 0.25);"> HSLA values let you set custom opacity - compare these two lines </h2>

Rounded Corners
Before the release of CSS3, developers had to write long code to produce rounded corners. Now, it is enough to apply the border-radius CSS3 property to HTML elements.
border-radius property, you can define rounded corners for an element:
div { border: 3px solid; border-radius: 30px; }

It is actually a shorthand for four CSS border radius subproperties:
•border-top-left-radius
•border-top-right-radius
•border-bottom-left-radius
•border-bottom-right-radius
div { border: 4px solid green; border-top-left-radius: 4em; }

The syntax for border-radius is simple:
border-radius: value1 value2 value3 value4;


Attribute Selectors

CSS3 also introduced new selectors in addition to the ones in CSS2. Instead of applying IDs or classes for styling, developers can select HTML elements according to their attributes.

p { text-align: left; color: blue; }
CSS selector is the paragraph element <p>.
The CSS selector indicates an HTML element that you want to style.

grouping selectors is convenient for optimization of code. It also makes the code easier to debug.
h1, h2, p { text-align: left; color: blue; }

CSS selector:
It is a string that identifies the elements to which a particular declaration apply. It is also referred as a link between the HTML document and the style sheet. It is equivalent of HTML elements. There are several different types of selectors in CSS: -
•CSS Element Selector
•CSS Id Selector
•CSS Class Selector
•CSS Universal Selector
•CSS Group Selector
The universal selector matches the name of any of the element type instead of selecting elements of a specific type.
* {    
color: green;    
 font-size: 20px;    
}    


New Colors
One of the CSS3 features is the addition of new colors:
•RGBA
•HSL
•HSLA
•Gradient Colors
Color name declaration is not case-sensitive. Blue is the same as blue or BLUE.
Note: by using the :hover selector and opacity, you can change the transparency of images and colors on mouse-over.

CSS Gradients
CSS gradients let you display smooth transitions between two or more specified colors.
CSS defines two types of gradients:
•Linear Gradients (goes down/up/left/right/diagonally)
•Radial Gradients (defined by their center)
CSS Linear Gradients
To create a linear gradient you must define at least two color stops. Color stops are the colors you want to render smooth transitions among. You can also set a starting point and a direction (or an angle) along with the gradient effect.
Syntax
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
#grad {
  background-image: linear-gradient(red, yellow);
}
#grad {
  background-image: linear-gradient(to right, red , yellow);
}
Linear Gradient - Diagonal
You can make a gradient diagonally by specifying both the horizontal and vertical starting positions.
The following example shows a linear gradient that starts at top left (and goes to bottom right). It starts red, transitioning to yellow:

#grad {
  background-image: linear-gradient(to bottom right, red, yellow);
}
Using Angles
If you want more control over the direction of the gradient, you can define an angle, instead of the predefined directions (to bottom, to top, to right, to left, to bottom right, etc.).
Syntax
background-image: linear-gradient(angle, color-stop1, color-stop2);
The angle is specified as an angle between a horizontal line and the gradient line.
The following example shows how to use angles on linear gradients:
#grad {
  background-image: linear-gradient(-90deg, red, yellow);
}

More than Web-Safe Fonts
Instead of only using fonts labeled as web-safe, developers now can apply more unique fonts in their HTML documents. Before that, CSS wanted to ensure that all browsers and machines display fonts the same.

font-family	Defines the font family your text will have
font-style	Adds regular, italic or oblique effect to your letters
font-size	Specifies the size of your characters
font-weight	Describes the thickness of your characters
font-variant	Transforms text to smaller uppercase letters
font-stretch	Selects a condensed or expanded face from fonts
line-height	Specifies the height of your line box

Note: only font-size and font-family properties are mandatory in the font CSS shorthand. Others are optional.

Syntax Problems

	Syntax: if the shorthand does not have font-size and font-  	family, CSS will ignore the entire statement.
•Syntax: the value of font-family has to be last in the declaration.
•Syntax: the optional values must be before the font-size value in the shorthand. Otherwise, CSS ignores them and might do the same for the mandatory properties.
•Syntax: the font-stretch CSS property might not work in older browsers. It makes CSS ignore the entire statement. For safety, include a fallback function to run when the shorthand fails.
 What is the difference between the usage of an ID and a Class?
An ID is unique. A particular ID can be only assigned to a single element. IDs are used when specific styling is being tried to be achieved over a single element.

Class – Just like the word suggests, a class is a collective way of targetting HTML elements for styling. Classes are not unique and multiple elements can have the same class.

What is the z-index in CSS? 
Z index helps in specifying the overlapping element. It is a number which can be positive or negative, the default value being zero.

Z-Index can take the following values:
•Auto: Sets the stack order equal to its parents.
•Number: Orders the stack order.
•Initial: Sets this property to its default value (0).
•Inherit: Inherits this property from its parent element.

What are CSS Sprites? 
An image sprite is a collection of images put into a single image.
A web page with many images can take a long time to load and generates multiple server requests.
Using image sprites will reduce the number of server requests and save bandwidth.

CSS sprites combine multiple images into one single larger image. It is a commonly-used technique for icons (Gmail uses it)
	1.Use a sprite generator that packs multiple images into one and generates the appropriate CSS for it.
2.Each image would have a corresponding CSS class with background-image, background-position and background-size properties defined.
3.To use that image, add the corresponding class to your element.

img.add { width: 60px; height: 55px; background: url (image.god) 0 0; }

What are pseudo-elements in CSS?
Pseudo-elements are used to add special effects to some selectors.
A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). They can be used for decoration (:first-line, :first-letter) or adding elements to the markup (combined with content: ...) without having to modify the markup (:before, :after).
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}

@media Rule:
The @media rule is used in media queries to apply different styles for different media types/devices.
Media queries can be used to check many things, such as:
•width and height of the viewport
•width and height of the device
•orientation (is the tablet/phone in landscape or portrait mode?)
•resolution
You can also use media queries to specify that certain styles are only for printed documents or for screen readers (mediatype: print, screen, or speech).
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
CSS Syntax
@media not|only mediatype and (mediafeature and|or|not mediafeature) {
  CSS-Code;
}
meaning of the not, only and and keywords:
not: The not keyword reverts the meaning of an entire media query.
only: The only keyword prevents older browsers that do not support media queries with media features from applying the specified styles. It has no effect on modern browsers.
and: The and keyword combines a media feature with a media type or other media features.
They are all optional. However, if you use not or only, you must also specify a media type.

What are the different media types allowed by CSS?
There are four types of @media properties (including screen):
•all – for all media type devices
•print – for printers
•speech – for screenreaders that “reads” the page out loud
•screen – for computer screens, tablets, smart-phones etc.
Here is an example of print-media type’s usage:
/* On screens that are 992px or less, set the background color to blue */
@media screen and (max-width: 992px) {
  body {
    background-color: blue;
  }
}

/* If screen size is more than 600px wide, set the font-size of <div> to 80px */
@media screen and (min-width: 600px) {
  div.example {
    font-size: 80px;
  }
}
@media print {
h1 {
background-color: yellow;
 }
}

Different units used in CSS?
Relative Length
UNIT	DESCRIPTION
em	Relative to the font-size of the element (2em means 2 times the size of the current font)
ex	Relative to the x-height of the current font (rarely used)
ch	Relative to the width of the “0” (zero)
rem	Relative to font-size of the root element
vw	Relative to 1% of the width of the viewport*
vh	Relative to 1% of the height of the viewport*
vmin	Relative to 1% of viewport’s* smaller dimension
vmax	Relative to 1% of viewport’s* larger dimension
%	Relative to the parent element

Absolute Length
UNIT	DESCRIPTION
CM	Centimetres
MM	Millimetres
IN	inches (1in = 96px = 2.54cm)
PX	pixels (1px = 1/96th of 1in)
PT	points (1pt = 1/72 of 1in)
PC	picas (1pc = 12 pt)

What is the overflow property in CSS used for?
The overflow property specifies what should happen if content overflows an element’s box. 
This property specifies whether to clip content or to add scrollbars when an element’s content is too big to fit in a specified area. Below are the overflow options available in CSS – 
overflow: auto;
overflow: none;
overflow: scroll;
overflow: visible;
What is the property that is used for controlling image-scroll?
The background-attachment property sets whether a background image scrolls with the rest of the page, or is fixed. Here is an example of a background-image that will not scroll with the page (fixed):
body {
  background-image: url("img_tree.gif");
  background-repeat: no-repeat;
  background-attachment: fixed;
background-position: bottom right;
}
What is responsive web design?
Responsive design is an approach to web page creation that makes use of flexible layouts, flexible images and cascading style sheet media queries. 
The goal of responsive design is to build web pages that detect the visitor’s screen size and change the layout accordingly.
What is the difference between {visibility: hidden} and {display: none}? 
display: none not occupy space. It will not affect the layout of the document.
display:none means that the tag will not appear on the page at all. There will be no space allocated for it between the other tags.
visibility: hidden hides the element, but it occupies space and affects the layout of the document.
visibility:hidden means that unlike display:none, the tag is not visible, but space is allocated for it on the page. The tag is rendered, it just isn’t seen on the page.
For example:
test | <span style="[style-tag-value]">Appropriate style in this tag</span> | test
Replacing [style-tag-value] with display:none results in:
test |   | test
Replacing [style-tag-value] with visibility:hidden results in:
test |                        | test

What is the use of box-shadow in CSS?
The box-shadow CSS property adds shadow effects around an element’s frame. You can set multiple effects separated by commas. A box-shadow is described by X and Y offsets relative to the element, color, blur and spread radii. Below are a few implementations of box-shadow
box-shadow: 10px 5px 5px red;
box-shadow: 60px -16px teal;
box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2);
box-shadow: inset 5em 1em gold

What is CSS 1flexbox?
The flex box layout officially called CSS flexible box layout module is a new layout module in CSS3. 
It is made to improve the items align, directions and order in the container even when they are with dynamic, or even unknown size. 
The prime characteristic of the flex container is the ability to modify the width or height of its children to fill the available space in the best possible way on different screen sizes.
CSS Flexbox Properties
The flex container becomes flexible by setting the display property to flex:
The flex container properties are:
•	flex-direction
•	flex-wrap
•	flex-flow
•	justify-content
•	align-items
•	align-content

The flex-direction property defines in which direction the container wants to stack the flex items.
.flex-container {
  display: flex;
  flex-direction: column; / column-reverse; / row; / row-reverse;
}
The flex-wrap property specifies whether the flex items should wrap or not.
.flex-container {
  display: flex;
  flex-wrap: wrap; / nowrap; / wrap-reverse;
}

The flex-flow property is a shorthand property for setting both the flex-direction and flex-wrap properties.
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
The justify-content property is used to align the flex items:
.flex-container {
  display: flex;
  justify-content: center; / flex-start; / flex-end; / space-around; /space-between;
}
The align-items property is used to align the flex items.
.flex-container {
  display: flex;
  height: 200px;
  align-items: center; / flex-start; / flex-end; / stretch; / baseline;
}
The align-content property is used to align the flex lines.
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-between; / space-around; / stretch; / center; /flex-start; / flex-end;
}

how to align div center?
Set both the justify-content and align-items properties to center, and the flex item will be perfectly cantered:
.flex-container {
  display: flex;
  height: 300px;
  justify-content: center;
  align-items: center;
}

Child Elements (Items)
The direct child elements of a flex container automatically becomes flexible (flex) items.
The flex item properties are:
•	order
•	flex-grow
•	flex-shrink
•	flex-basis
•	flex
•	align-self
The order property specifies the order of the flex items.
The order value must be a number, default value is 0.
<div class="flex-container">
  <div style="order: 3">1</div>
  <div style="order: 2">2</div>
  <div style="order: 4">3</div>
  <div style="order: 1">4</div>
</div>

The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items.
Make the third flex item grow eight times faster than the other flex items:

The flex-shrink property specifies how much a flex item will shrink relative to the rest of the flex items.
The value must be a number, default value is 1.
Do not let the third flex item shrink as much as the other flex items:

The flex-basis property specifies the initial length of a flex item.
Set the initial length of the third flex item to 200 pixels:

The flex property is a shorthand property for the flex-grow, flex-shrink, and flex-basis properties.
Make the third flex item not growable (0), not shrinkable (0), and with an initial length of 200 pixels:

The align-self property specifies the alignment for the selected item inside the flexible container.
The align-self property overrides the default alignment set by the container's align-items property.
Align the third flex item in the middle of the container:


Align the second flex item at the top of the container, and the third flex item at the bottom of the container:

1Grid Layout
The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.

An HTML element becomes a grid container when its display property is set to grid or inline-grid.

The vertical lines of grid items are called columns.
The horizontal lines of grid items are called rows
The spaces between each column/row are called gaps

You can adjust the gap size by using one of the following properties:
grid-column-gap
grid-row-gap
grid-gap

The lines between columns are called column lines.
The lines between rows are called row lines.
Place a grid item at column line 1, and let it end on column line 3:
.item1 {
  grid-column-start: 1;
  grid-column-end: 3;
}

Grid Container
The grid-template-columns property defines the number of columns in your grid layout, and it can define the width of each column.
If you want your grid layout to contain 4 columns, specify the width of the 4 columns, or "auto" if all columns should have the same width.

Make a grid with 4 columns:
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
}

.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-gap: 5px;
  background-color: #2196F3;
  padding: 10px;
}

The grid-template-rows property defines the height of each row.
.grid-container {
  display: grid;
  grid-template-rows: 80px 200px;
}

The justify-content property is used to align the whole grid inside the container.

The align-content property is used to vertically align the whole grid inside the container.
.grid-container {
  display: grid;
  height: 400px;
  align-content: center; /
align-content: space-evenly; /
align-content: space-around; /
align-content: space-between; /
align-content: start; /
align-content: end; /
}

The grid-column property defines on which column(s) to place an item.

.grid-container {
  display: grid;
  justify-content: space-evenly;
justify-content: space-around;
justify-content: space-between;
justify-content: center;
justify-content: start;
justify-content: end;
}

The grid-row property defines on which row to place an item.

The grid-row property is a shorthand property for the grid-row-start and the grid-row-end properties.


Child Elements (Items)
A grid container contains grid items.
By default, a container has one grid item for each column, in each row, but you can style the grid items so that they will span multiple columns and/or rows.
The grid-column property defines on which column(s) to place an item.
You define where the item will start, and where the item will end.
Make "item1" start on column 1 and end before column 5:
.item1 {
  grid-column: 1 / 5;
}

Make "item1" start on column 1 and span 3 columns:
.item1 {
  grid-column: 1 / span 3;
}

The grid-row property defines on which row to place an item.
You define where the item will start, and where the item will end.
The grid-row property is a shorthand property for the grid-row-start and the grid-row-end properties.
The grid-area property can be used as a shorthand property for the grid-row-start, grid-column-start, grid-row-end and the grid-column-end properties.
Make "item8" start on row-line 1 and column-line 2, and end on row-line 5 and column line 6:
.item8 {
  grid-area: 1 / 2 / 5 / 6;
}

The grid-area property can also be used to assign names to grid items.

Item1 gets the name "myArea" and spans all five columns in a five columns grid layout:

.item1 {
  grid-area: myArea;
}
.grid-container {
  grid-template-areas: 'myArea myArea myArea myArea myArea';
}

Each row is defined by apostrophes (' ')
The columns in each row is defined inside the apostrophes, separated by a space.
Make "item1" span two columns and two rows:
.grid-container {
  grid-template-areas: 'myArea myArea . . .' 'myArea myArea . . .';
}

The Grid Layout allows us to position the items anywhere we like.

Difference between flexbox and grid
The basic difference between both is that 
Flexbox was designed for layout in one dimension - either a row or a column. 
Grid was designed for two-dimensional layout - rows, and columns at the same time. 

Flexbox: The CSS Flexbox offers a one-dimensional layout. It is helpful in allocating and aligning the space among items in a container (made of grids). It works with all kinds of display devices and screen sizes.
To get started you have to define a container element as a flext with display: flex;

Grid: CSS Grid Layout, is a two-dimensional grid-based layout system with rows and columns, making it easier to design web pages without having to use floats and positioning. Like tables, grid layout allow us to align elements into columns and rows.
To get started you have to define a container element as a grid with display: grid, set the column and row sizes with grid-template-columns and grid-template-rows, and then place its child elements into the grid with grid-column and grid-row.

•	CSS Grids helps you create the outer layout of the webpage. You can build complex as well responsive design with this. This is why it is called ‘layout first’.
•	Flexbox mostly helps align content & move blocks.
•	CSS grids are for 2D layouts. It works with both rows and columns.
•	Flexbox works better in one dimension only (either rows OR columns).

Transforms:
CSS transforms allow you to move(translate), rotate, scale, and skew elements.
	translate()
•rotate()
•scaleX()
•scaleY()
•scale()
•skewX()
•skewY()
•skew()
•matrix()
The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).

The 1position Property
The position property specifies the type of positioning method used for an element.
There are five different position values:
•static
•relative
•fixed
•absolute
•sticky
Elements are then positioned using the top, bottom, left, and right properties. 
However, these properties will not work unless the position property is set first. They also work differently depending on the position value.
Note: Internet Explorer, Edge 15 and earlier versions do not support sticky positioning. Safari requires a -webkit- prefix (see example below). You must also specify at least one of top, right, bottom or left for sticky positioning to work.
https://www.w3schools.com/css/css_positioning.asp

What effect would this piece of CSS code have? {box-sizing: border-box;}
By default, elements have box-sizing: content-box applied, and only the content size is being accounted for.
• box-sizing: border-box changes how the width and height of elements are being calculated, border and padding are also being included in the calculation.
• The height of an element is now calculated by the content’s height + vertical padding + vertical border width.
• The width of an element is now calculated by the content’s width + horizontal padding + horizontal border width.

What are Vendor-Prefixes? 
	-webkit- (Chrome, Safari, newer versions of Opera, almost all iOS browsers (including Firefox for iOS); basically, any WebKit based browser)
•-moz- (Firefox)
•-o- (Old, pre-WebKit, versions of Opera)
•-ms- (Internet Explorer and Microsoft Edge)

How can you integrate CSS on a web page?
There are three methods to integrate CSS on web pages.
1.Inline method - It is used to insert style sheets in HTML document
2.Internal method - It is used to add a unique style to a single document
3.External method - It is used when you want to make changes on multiple pages.


What is the CSS Box model and what are its elements?
The CSS box model is used to define the design and layout of elements of CSS.
The elements are:
•Margin - It removes the area around the border. It is transparent.
•Border - It represents the area around the padding
•Padding - It removes the area around the content. It is transparent.
•Content - It represents the content like text, images, etc.

The CSS Box Model
All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout.
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content

difference between CSS and SCSS
Introduction
•CSS : Cascading Style Sheet is the basically the scripting language. CSS is used for designing web pages.
CSS is the most important web technologies that are widely used along with HTML and JavaScript. CSS have file extension of .css.
•SCSS : Sassy CSS is the superset of CSS. SCSS is the more advanced version of CSS. SCSS have file extension of .scss.
•In SCSS we can shorten this code using a @mixin so we don’t have to write color and width properties again and again
Differences:
1.SCSS contains all the features of CSS and contains more features that are not present in CSS which makes it a good choice for developers to use it.
2.SCSS is full of advanced features.
3.SCSS offers variables, you can shorten your code by using variables. It is a great advantage over conventional CSS.
Example: In CSS
body{
 width: 800px;
 color: #ffffff;
}
body content{
 width:750px;
 background:#ffffff;
}

In SCSS
$color: #ffffff;
$width: 800px;

@mixin body{
 width: $width;
 color: $color;

 content{
  width: $width;
  background:$color;
 }
}

	Knowing SCSS helps you to customize Bootstrap 4.
1.SASS adds the feature of @import which lets you import your customized SCSS files.
Example:
@import "my theme";
@import "framework/bootstrap";
2.SASS allows us to use nested syntax. Let’s say if you have to style a specific ‘paragraph’ in ‘div’ in ‘footer’ you can definitely do that by SASS.
Example:
footer {
    div {
        p {
            margin: 2rem;
            color: #2f2f2f;
        }
    }
}
3.At last, what makes SASS a good option to use is that it is well documented.

SCSS Features
1.	Operators
2.	Variables
3.	Nesting
4.	Mixin
5.	Parameters
6.	Partial

What is 1mixin?
Mixin allow you to define a block of styles once and then include those styles in various selectors or rules as needed. This promotes code reusability and maintainability in your stylesheet.
It also helps you to write cleaner code without having to repeat yourself.
@mixin circle {
    width: 200px;
    height: 200px;
    background: red;
    border-radius: 50%;
}

div {
   @include circle;
}


Define Bootstrap.
Answer: Bootstrap is a front-end framework that is used for creating HTML, CSS, and JS web applications. Its layout is very responsive, fast and easy to use. It mostly focuses on building a mobile application with having design templates for creating UI like Dropdown, Forms, Buttons, Alerts Tab, etc.

Why Bootstrap is used for Mobile Web development?
Answer: It is used for Mobile Web development because it has responsive designs and templates which are easy to use.

Explain the features of Bootstrap.
Answer: Its features include:
•	Open source for use.
•	Compatibility with all browsers.
•	Responsive designs.
•	Easy to use and fast.

Define the key components of Bootstrap.
Answer: Its components include:
•	Scaffolding: It has the grid system, background, styles.
•	JS Plugins: Contains JS and jQuery plugins.
•	Customize: Can customize frameworks.
•	CSS: Contains CSS files.

Scaffolding. Bootstrap is built on responsive 12-column grids, layouts, and components

Give an example of a basic grid structure in Bootstrap

Bootstrap's grid system allows up to 12 columns across the page.
The Bootstrap 4 grid system has five classes:
•	.col- (extra small devices - screen width less than 576px)
•	.col-sm- (small devices - screen width equal to or greater than 576px)
•	.col-md- (medium devices - screen width equal to or greater than 768px)
•	.col-lg- (large devices - screen width equal to or greater than 992px)
•	.col-xl- (xlarge devices - screen width equal to or greater than 1200px)
<div class="col-sm-3 col-md-6">....</div>
<div class="col-sm-9 col-md-6">....</div>
Now Bootstrap is going to say "at the small size, look at classes with -sm- in them and use those. At the medium size, look at classes with -md- in them and use those".
Add the .no-gutters class to the .row container to remove gutters (extra space)
Example of a basic grid structure:
<div class = "container">
<div class = "row">
<div class = "col-*-*"></div>
<div class = "col-*-*"></div>
</div>
<div class = "row">...</div>
</div>
<div class = "container">....

Divide a row in 5 columns in Bootstrap 4? [duplicate]
Bootstrap 4 doesn't use floats like version 3 did so it can automatically space out your columns using just the col class. So for 5 equally spaced columns, just do this:
<div class="container">
  <div class="row">
    <div class="col col1">Column 1</div>
    <div class="col col2">Column 2</div>
    <div class="col col3">Column 3</div>
    <div class="col col4">Column 4</div>
    <div class="col col5">Column 5</div>
  </div>
</div>

Bootstrap 3:
<div class="row">
    <div class="col-md-2 col-md-offset-1"></div>
    <div class="col-md-2"></div>
    <div class="col-md-2"></div>
    <div class="col-md-2"></div>
    <div class="col-md-2"></div>
</div>

How many types of layouts are there in Bootstrap?
Answer: There are two types of layouts in Bootstrap.
They are:
•	Fluid Layout
•	Fixed Layout

Define Fluid Layout.
Answer: Fluid Layout is useful when you need to make an app that involves the full width of the screen i.e. Fluid Layout adjusts itself according to the browser size.

Define Fixed Layout.
Answer: A fixed layout is responsive and easy to use but just like the fluid layout, it cannot adjust itself according to the browser size. The fixed layout should be 940 px in most cases.

When will you use <code>tag and <pre>tag?
Answer: <code>tag is used to show the code inline and <pre>tag is used to show code with multiple lines.

What is a progress bar in bootstrap?
Answer: Progress bar is used with HTML tag style in HTML element using <progress> keyword. In bootstrap, we use html5 <progress> with CSS classes that have special features in bootstrap, which is only made for the progress bar.

What are the different button styles in Bootstrap?
Answer: In bootstrap, there are seven styles which we can use with the bootstrap button.
•	.btn-default.
•	.btn-primary
•	.btn-success
•	.btn-info
•	.btn-warning.
•	.btn-danger.
•	.btn-link.

Explain what is Bootstrap collapsing elements.
Answer: It allows you to collapse any particular element without using any JavaScript code.
To use this feature in bootstrap you have to add data-toggle=” collapse” to the controller element along with a data target to automatically assign the control of a collapsible element. We can use this by writing .collapse(options) etc.


Explain what are the steps for creating basic or vertical forms?
The steps for creating basic or vertical forms are
•	Add a role form to the parent <form> element
•	Wrap labels and controls in a <div> with class .form-group. To achieve optimum spacing this is needed
•	Add a class of .form-control to all texturl <input> , <textarea> , and <select> elements

Explain what is Bootstrap Container?
Bootstrap container is a class which is useful and creates a centred area within the page where our site content can be put within. The advantage of the bootstrap .container is that it is responsive and will place all our other HTML code.

