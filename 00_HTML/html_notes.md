# HTML

> Use MDN docs they are best resource for HTML as per requirement.

## 0.1 HTML Getting Started
> HTML is one of those languages which no one knows/confident in but nobody wants to learn as well.

> It can be considered a structure language rather than a programming language.

### Boilerplate
We use `!` to generate boilerplate code in HTML. understanding each element of this boilerplate code is important. ! is also a Emmet abbreviation. 

```xhtml
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"></meta>
    <title>Title</title>
</head>
<body>

</body>
</html>
```

### Apache
> Historically, **Apache HTTP Server**—commonly referred to as *Apache*—has been one of the most widely used open-source web servers. It is still actively used today on Linux systems and other platforms to host websites and web applications. though it shares market space with alternatives like Nginx and LiteSpeed.

> By default, when a specific file is not requested in a URL (e.g., accessing a directory path like `http://example.com/`), Apache serves a default file, typically `index.html`, if it exists in that directory. This behavior is controlled by the `DirectoryIndex` directive in Apache’s configuration.

### Emmet
https://docs.emmet.io/
Emmet is a plugin for many popular text editors which greatly improves HTML & CSS workflow

for eg if we type `ul>li.item$@3*5`
we get 
```xhtml
<ul>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
    <li class="item6"></li>
    <li class="item7"></li>
</ul>
```

when we run this HTML file (i.e. index.html) it is saved into the memory then hosted on the browser locally. as simple as that.
but when we open the file manually then we have to restart the file again and again to see the changes that the file is undergoing.
So to solve this problem and see the updates in real time we use and extension called `Live Server`. this is happening because live server inject a script to the file when it is opened with live server.

```xhtml
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
```
## 0.2 CORE Structure of HTML and META Tags

> difference between h1 and h2 tag is not the size of heading we get as that can be manipulated using CSS anytime. so dont misunderstand it as this concept

> HTML - Hyper Text Markup Language. it is a markup language but take it as a structure or syntatical language as it is used to build our pages. There are different type of structure language as presentational structure language or descriptive structure language. Markdown like this file or latex

Each tag in HTML holds its own importance and significance like H1 denote the core heading H2 denote the sectional heading. and this language and its tag are well understood by different browser engines. all tags are case insensitive.
```html
<!DOCTYPE html>
```
this tag is used to define what type of document it is as we used to have and still have different documents like html, xhtml etc.

```html
<html lang="en">
```
this is used to define what language this page cosists of. standard practice.

```html
<meta charset="UTF-8">	
```
use to define what characterset are used here. 

there are many more attributes like this which you can learn as you go. you dont need to understand anything deeper than that.

Next major thing to discuss is Parent-Child Strucutre of HTML. the most prominant of these is 

### HTML has two childs `head` and `body` tag

and we can furthur add child in head and body
> these concepts are very important as good understanding of these are needed for DOM manipulation and DOM is a core concept.

```html
<!-- parent -> child -> grandchild these are the only relations (just jargon) -->
<!-- lets take an example -->
 <!-- head and body tags are child of html -->
  <!-- html is child of document -->
   <!-- h1 is child of body and title is child of head -->
	<!-- good understanding of this nested behaviour help in better understanding of the DOM concepts which are rooted in HTML -->
 <head>
    
    <title>HTML Tutorial</title>
	<!-- only two things are visible from the head area that is the title (name which is shown on the tab) and the favicon (icon) -->
</head>
<body>
    <h1>Heading one</h1>
	<!-- the whole website is the body -->
</body>
```

### Meta Tags

```html
    <meta charset="UTF-8">
	<!-- charset sets the no of characters which we allow -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
	<!-- equiv sets the zoom level of the page -->
```
> meta: is the shortcut here and for a tags we use a:

[google meta tags reference](https://developers.google.com/search/docs/crawling-indexing/special-tags)

Meta tags are not shown on the page but they are important for the search engine as well as for the bot or crawler which the webiste will be visited by. 

## 0.3 Headings, Paragraph, Reading Docs

Targets 
* HTML Tags
* HTML Elements
* HTML Attributes

`Different tags have different attributes. tags have compulsory and non compulsory attributes.` 

> Closing are of two type either self closing or opening and closing tags.

**HTML ELEMENT** = tag(opening and closing) + property/attribute + content 

```html
	<h1 title = "Heading one">Heading one <span> two </span> </h1>
```
> we can have nested tags. so to target elements nore easily using CSS
> learn about different attributes and use them. 

```html
  <!-- anchor tag -->
   <a href + "#"> Google </a>
   <!-- # means no value yet -->
```

### Headings
> there are 6 level of headings h1 - h6

> lorem ipsum 

### pre tag

```html
<body>
	<pre>
        line 2
        line 3

        line 4
        line 5
    </pre>
</body>

<!-- the main difference between pre tag and the other tag is that the pre tag is used to format the text inside it in a certain way like the above line 2 to 4 will be printed in a way they are written but this doesnt happen with the other tags they are formatting insensitive but pre tag is formatting sensitive but most of pre tags attributes have been deprecated (basically are no longer compatable with the beowsers or are not in use) -->
```
## 0.4 Formatting style and global attributes

> shortcut for comment is `ctrl + /`

> comments are present in source code keep that in mind HTML comments are usually visible in `"View Page Source" and the browser’s Inspector`

> If you use a `build tool` (e.g., Webpack, Parcel, Vite) with `HTML minification,` it might remove comments during the build step, but this depends on the specific configuration. Even then, unless specifically configured otherwise, comments can remain in the HTML.

### bold vs strong vs em (emphasis)
> bold just change formatting but strong is emphasised. 

```html
<!-- read about all these formattings -->
	<ul>
        <li>b, strong </li>
        <li>i, em</li>
        <li>small</li>
        <li>sub, sup</li>
        <li>del, mark</li>
    </ul>
```

### Styling attribute is used to style a particular element or tag

```html
<h3 
    style="
    text-align: center; 
    background-color: aqua;
    "
    >
	<!-- readability is priority -->
        Heading 3</h3>
```
## 0.5 Values of Colour and CSS format


```html
<h3 
    style="
    text-align: center; 
    background-color: rgba(28, 186, 41);
    "
    >
	<!-- rgb and alpha channel there are two other ways alos like #vales and hsla values to do this -->
        Heading 3</h3>
```
> a (alpha) is opacity 


There are three ways to do CSS or styling in HTML.
* inline directly to the attributes like we did above.
```html
<h3 
    style="
    text-align: center; 
    background-color: rgba(28, 186, 41);
    "
    >
	<!-- rgb and alpha channel there are two other ways alos like #vales and hsla values to do this -->
        Heading 3</h3>
```
* or we can attach stylesheet and do the styling in a different style. css
```html
<head>
	<link ref="stylesheet" href="style.css">
</head>
```

```css
body{
	background-color: #414141;
	color: #FFFFF;
}
```

* styling directly in HTML using style tag in head

```html
<head>
	<style>
		body{
			color: aqua;
		}
	</style>
</head>
```

> learn about priority of these different type of styling which will have what level of priority. 


### Quotes tag in HTML

```html
	<blockquote cite="Elon">
		this is a quote
	</blockquote>
	<!-- this is important from the prespective of search engine where it search for quotes -->
```

### Abbreviations tag

### Address tag

### Cite tag

### BDO

## 0.6 Links and Images with Map

[code for this section](./linktags.html)
[images](./image.html)

## 0.7 Tables in HTML

[Tables.html](./tables.html)

## 0.8 List, Inline and Block Elements

[Lists](./lists.html)

## 0.9 Class and ID | iFrame

[Class](./class.html)
[iFrame](./iframe.html)

## 0.10 Head Tag in HTML

[headtag](./headtag.html)

## 0.11 HTML Semantics

[semantics](./semantics.html)