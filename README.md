# MarkdownToHTML
Convert Markdown or md URL to HTML - MarkdownToHTML
Markdown is a lightweight markup language for creating formatted text using a plain-text editor. John Gruber and Aaron Swartz created Markdown in 2004 as a markup language that is appealing to human readers in its source code form. [Wikipedia](https://en.wikipedia.org/wiki/Markdown)

Video Documentation :- https://youtu.be/omtgsLp9hOI
Article Source :- https://codexdindia.blogspot.com/2022/01/convert-markdown-or-md-url-to-html-using-javascript.html

---

> Using Markdown you will write(code) less and get more(static content).
> Code given below are basic JavaScript Codes. Easy to Understand you can modify it and make the functions more dynamic.

We will Use - [showdownjs](http://showdownjs.com/) to do so :- https://github.com/SH20RAJ/markdowntohtml 

Here is the code you can use to change your markdown to HTML and show the html on your Website.

---

```html
<script src="https://cdn.jsdelivr.net/npm/showdown/dist/showdown.min.js"></script>
<div id="mycontent"></div>
<script>

var converter = new showdown.Converter();
var md = '[**Showdown**](http://www.showdownjs.com) is *great*\n' +
         'because:\n\n' +
         ' - it\'s easy to use\n' +
         ' - it\'s extensible\n' +
         ' - works in the server and in the browser';
var html = converter.makeHtml(md);
  document.querySelector('#mycontent').innerHTML = html;

</script>
```
See the Result Here :-

---

[Showdown](http://www.showdownjs.com/) is great because:

- it's easy to use
- it's extensible
- works in the server and in the browser

---

To Know more about showdownjs functions Visit [GitHub]( https://github.com/showdownjs/showdown/) or I will embed the markdown of GitHub here using the following code.

> Pro Tip :- Instead of Writing Code of MD in Js or Js Variable.
> -> write the Markdown Inside a div
> -> Make a variable and get the inner text of the div into it.
> -> Convert the md to html using showdown and
> change the innerHTML of that div to the new generated HTML



# Convert a Markdown Containing URL to HTML and Show it.

For this we will Use [fetch Api](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch).
Here is the raw URL of showdownjs readme.md :- https://github.com/showdownjs/showdown/raw/master/README.md .

We will fetch content of this URL then convert it to HTML and show on our website. See Demo on [Codepen](https://codepen.io/SH20RAJ/pen/bGoyJqJ?editors=1010).

```html
<script src="https://cdn.jsdelivr.net/npm/showdown/dist/showdown.min.js"></script>
<div id="mypost"></div>
<script>
fetch('https://raw.githubusercontent.com/showdownjs/showdown/master/README.md').then(response => response.text())
  .then(data => {
  console.log(data);
  var converter = new showdown.Converter();
var md = data;
var html = converter.makeHtml(md);
  document.querySelector('#mypost').innerHTML = html;
});
</script>
```
See the result on Codepen :- https://codepen.io/SH20RAJ/pen/bGoyJqJ?editors=1010

### And One More option is to use this framework of showdownjs :- https://github.com/cs905s/md-in-blogger

#### To Add like this way

```html
      <pre class="markdown">
      #Woo hoo!
      [Markdown](http://daringfireball.net/projects/markdown/) is cool!
      ```javascript
          // Verify code highlighting
          if (today==rainy) {
            return false;
          }
      ```
      </pre>
```
