---
layout: post
---

HTML is the **language used by all browsers to render a website.**  HTML stands for **HyperText Markup Language,** and we need to unpack this name to get a better understanding of what that means.

### Hypertext
Hypertext is a term for text that is connected via links.  The idea is that if you need to learn more about a term or phrase, you can click on that term, and more information will be presented.

### Markup Language
Markup Language, in general, is a system for annotating a document.  You may think of modern websites today as interactive applications, and less document oriented, but the early Internet was really just a set of pages that you could read that were **hyperlinked** together.  All of these documents needed to be *marked up* to specify headings, hyperlinks, and so on for proper formatting.

Let's move on to a basic example to see how it works.  Check out the code and its rendered counterpart below:

#### HTML code
<a id="example"></a>
{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <title>My Website</title>
    <meta name="author" content="Matthew Prestifilippo">
  </head>
  <body>
    <h1>My Great Company</h1>
    <p>My company <strong>makes</strong> things:</p>
    <ul>
      <li>Lions</li>
      <li>Tigers</li>
      <li>Bears</li>
    </ul>
  </body>
</html>
{% endhighlight %}

#### HTML rendered
<pre><iframe style="border:none; height: 200px; width: 400px; overflow: hidden;" src="/demos/html/demo.html"></iframe></pre>

There are two things we should acknowledge:

* Not everything in the code was rendered
* The structure, or **syntax**, of HTML

### HTML syntax

HTML is made up of elements.  For example, `<h1>My Great Company</h1>` is an HTML element, and so is `<body>...</body>`.  The general form, or syntax, of an element is `<tagname>text</tagname>` where `tagname` is one of the defined HTML tags.    There are more than 100 types of HTML elements, and you can <a href="https://www.w3.org/TR/html-markup/elements-by-function.html" target="_blank" hack="_">click here to see a complete list of HTML elements</a>.

### DOCTYPE, html, head, and body
All html documents start with a line that specifies the HTML version, known as `DOCTYPE`.  The difference between this tag and the other elements that we have seen is that it has no closing tag.  It is also required to always be the very first line of your HTML document.  If you scroll back up to the <a href="#example">initial example</a>, you will notice we included `<!DOCTYPE html>` as the first line of the document.  At the time of this writing, HTML is currently on version 5 (you may have heard of HTML5).  The reason for the different versions is the addition of new tags, such as the `<video>`, to better suit demands for different types of of web content.  By specifying the `DOCTYPE`, it lets the browser know how to properly display the HTML since there are other versions of HTML that would use different rendering rules.

The `<html>` element represents the **root element** of the document, and there may be only one `<html>` element in your document.  Every HTML document has to have a **head element**.  None of its contents are ever rendered, which is why `<title>My Website</title>` was not rendered.  Instead, this part of the document contains **metadata** such as the title and author.  **Metadata is a general term for any data that describes other data**.

You may be wondering: If the browser doesn't use it, then who/what does?  The answer is that browsers aren't the only thing that read websites.  For example, the title is used by search engines when listing search results.  Here is an example of a google search result listing.

![html titles on google](/images/posts/html/titles-on-google.png "use of titles")

Every HTML document also needs a **body element**.  The browser uses the contents of the body element to render the website.

### Element Nesting

Some elements are "inside" other elements, just as the `<title>` element is inside the `<head>` element.  This is called **nesting**.  Nested elements are called **child elements**, and naturally, the elements that are doing the nesting are called **parent elements**.  So in our example above, `<title>` and `<meta>` are the child elements of the parent element `<head>`, and `<head>` and `<body>` are the child elements of the parent element `<html>`.

All child elements must end before their parent ends.

> **Good**
>
> `<p>This is a <em>good</em> example</p>`
>
> **Bad**
>
> `<p>This is a <em>bad</p> example</em>`
>
> Notice how the `<p>` element ended before the `<em>` element.


The end result of all of this nesting creates a **tree structure**.

![html tree](/images/posts/html/html-tree.png "html tree")

The tree structure doesn't embody a tree as in a maple tree.  Instead, it embodies something similar to a family tree which has parents, children, siblings, ancestors, and descendants.

<a id="exercise-1"></a>

### Exercise 1: Try HTML

> In this exercise, you will be able to edit HTML and see how the HTML affects the rendering.
>
> * Go to the <a href="https://jsbin.com/zasalakico/edit?html,output" target="_blank" hack="_">jsbin editor</a>
>
> * Edit the html to render two headings.  One that says: "Hello, World" and one that says "Hello, Venus".
>
> * Nest an `<h1>` element inside of a `<p>` element like this: `<p>beginning <h1>title</h1> ending</p>`.  What happens to the text?

### What tags do I use?

If you tried out <a href="#exercise-2">exercise 2</a>, you may have found yourself wondering what tags to use.  This is a common problem with first timers, and will happen throughout your career.  You may have listed your 3 interests in side of one paragraph with `<p>1. soccer, 2. football, 3. hockey</p>` or you may have used the `<ul>` tag that was used in the <a href="#example">example</a> at the beginning of this article.  So which tag should is the correct one?

### semantic html

When writing HTML, you are really just categorizing and describing your data.  For example, if you have a list of items, you should probably take advantage of the list tags `<ul>` and `<ol>` to display your data.  If you are presenting a navigation section, you should use the `<nav>` tag.  If you are displaying an article, you should use the `<article>` tag.  You could technically *mark up* a list with a `<p>` tag, but then you lose semantics.  In order to know when to use which tag, it's important to get comfortable with all of the HTML tags.  There is a <a href="https://www.w3.org/TR/html-markup/elements-by-function.html" target="_blank" hack="_">list of HTML elements by function here</a> to help decide which tags to use.  But, lets check out some of the most common tags, first.

## Common tags

#### a
The link is one of the most important HTML elements.  The format of a link is `<a href="http://example.com/">This is the link text</a>`.  Most of the elements we have seen did not have anything other than the tag name inside of the `<` and `>` symbols.  The `href="..."` part is called an **attribute**, and the general form of an attribute is **attributeName="attributeValue"**.  The **href** attribute specifies the webpage to go to when clicking on the `<a>` element.  Aside from linking to other webpages, you can link to other elements so that you can jump to other sections of the page.  One common usage of this is a table of contents.  You can do this by setting an **id** attribute on the element you want to jump to and linking them by setting the **href** to the same value as the id, but with a `#` in front.  Ex:
{% highlight html %}
<a href="#content">Click here to go to content</a>
<h1 id="content">This is the content</h1>
{% endhighlight %}
I suggest trying this in <a href="https://jsbin.com/" target="_blank" hack="_">jsbin</a> to get more comfortable with this behavior if it seems confusing.

#### article
Most of the web is made up of articles, such as news or blogs, so it makes sense that there is a special tag just for this use case.  A typical article is made up of a title and multiple paragraphs, which would look like this:
{% highlight html %}
<article>
  <h1>Principia Mathematica Proven Wrong</h1>
  <p>Physics doesn't exist.</p>
  <p>Newton didn't know what he was talking about...</p>
</article>
{% endhighlight %}

#### video
Prior to HTML5, there was no way to add a video to your HTML document without using Adobe Flash.  <a href="https://en.wikipedia.org/wiki/Apple_and_Adobe_Flash_controversy" target="_blank" hack="_">Recent decisions with major tech companies</a> has caused Flash to go the wayside, and so now there is native browser support for video playback.

<video controls><source src="http://vjs.zencdn.net/v/oceans.mp4" /></video>
{% highlight html %}
<video controls><source src="http://vjs.zencdn.net/v/oceans.mp4" /></video>
{% endhighlight %}

#### img
The syntax to add an image to your page is `<img src="http://prestifilippo.org/images/posts/html/html-tree.png" />`.  This tag is somewhat different than most of the other tags that we have seen since it does not have a closing tag.  Elements that do not have a closing tag are called <a href="http://www.w3.org/html/wg/drafts/html/master/syntax.html#void-elements" target="_blank" hack="_">void elements</a>.

#### ul and ol
When enumerating a list, from a search result, or a list of friends, etc..., a ol tag is a good choice.  Lists come in two forms: ordered (`<ol>`), and unordered (`<ul>`).  A somewhat handy display property of these tags is that they display numbers or bullet characters in front of each list item.
<h6>Unordered List</h6>
<ul><li>unordered item</li><li>unordered item</li></ul>
<h6>Ordered List</h6>
<ol><li>ordered item</li><li>ordered item</li></ol>
{% highlight html %}
<h6>Unordered List</h6>
<ul>
  <li>unordered item</li>
  <li>unordered item</li>
</ul>
<h6>Ordered List</h6>
<ol>
  <li>ordered item</li>
  <li>ordered item</li>
</ol>
{% endhighlight %}
#### header
This tag is for encapsulating header information, such as the page's title, table of contents, or search form.  This tag may be used more than once.  So if there are multiple sections in a page that require header information, like an article, then you may choose to use this tag to wrap things such as a title.

#### footer
This tag is for encapsulating footer information such as links, copyright info, and logos.  This is much like the header tag, except it's for what you would typically see at the end of a document.

### Core attributes

The `<a>` element has the special attribute `href`, but there are some attributes that every element may have, which are class, id, style, dir, lang and title.  Here are descriptions for the most commonly used attributes.

#### class

The `class` attribute provides a more detailed description of the element.  Sometimes just using the tag `<ul>` isn't enough in the case of creating a todo list on your web page, so you may add a class like so: `<ul class="todo-list">`.  Class names can be whatever you want them to be.  The only rules you have to follow when making class names is that they must start with a letter, and they may only contain letters, numbers, -, and _<span hack="_"></span>.  You may also specify more than one class name in the attribute by separating the names with spaces: `<ul class="todo-list shopping-list">`.  

#### id

The `id` attribute is used to set an arbitrary value as the element's identifier.  The identifier can be used just to provide a more detailed description, but it can also be used so that a link such as `<a href="#some-id">` would jump to the element with the id `id="some-id"`.  

#### style

The `style` attribute is used to change the way the element is displayed.  You can change the font size, color, add borders, etc.   Ex: `<div style="font-size: 20px; color: green; border: 1px solid black;">`.  The font is now set to size 20px, the color of the text (not the background) is green, and there will be a 1px wide solid black border around the entire element.  The value of the style attribute must be valid CSS, and <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference" target="_blank" hack="_">there are a lot of CSS styles to choose from</a>.  There will be another blog post where I go over basic CSS.

## Readability

We have covered all of the concrete technical aspects of coding, so now we should go over the unwritten, mostly argued aspect of coding: readability.  Yes, it has to work, but eventually you or others will have to come back to your code to make updates or fix errors.  **Indentation is essential for making HTML readable.**  If you look back at the <a href="#example">first example</a>, you will see that most the **child elements are offset one tab length further than their parents, and siblings are offset at the same tab length**.  This enables you to easily visualize where elements begin, end, and what elements they contain.  There is one exception, though, and that is the `<strong>` element.  So how do you know when you are supposed to indent on a new line or keep it inline?  If we take the example above, and try to reformat the `<strong>` element to be indented, it will look like this:

{% highlight html %}
<p>
  My company
  <strong>makes</strong>
  things:
</p>
{% endhighlight %}

This is also readable, but now it takes away from the actual flow of the prose that is in the `<p>` element.  Competing rules are cause for debate, so decisions like this come down to taste.  It is up to you to choose which style you'd like to follow.  Both are acceptable.

### Whitespace

The contents of the `<p>` element above were split on separate lines.  Won't this format the text in separate lines when it is rendered?  Surprisingly, no, it does not affect how the text is rendered.  When HTML is rendered, there is only one space between two text nodes no matter how much space you put between them.  If you need to add more space between text, there are two options.  You can either use the `<pre>` tag, or you could use something called a character entity reference.  The character entity reference for a blank space is `&nbsp;` where nbsp is an acronym for non-breaking space.

### Entities
Since we use the &lt; and &gt; symbol to denote the beginning of a tag, you might be wondering how to render a &lt;.  It might seem easy to know when a &lt; is the start of a tag or part of the text, but computers can't use any abstract contextual information (*yet*) to determine what was meant by the programmer.  So, long story short, &lt; is reserved to only be used when starting a tag.  In order to get around this limitation, an escape character is used: `&`.  An **escape character is a character that starts an alternative interpretation of the characters to follow**. So when the browser sees a &amp;, it "escapes" the normal rendering process, and starts a special rendering process to render the following sequence of characters.  The *subsequent characters* are what is known as the **character entity reference**.  Here is a <a href="https://dev.w3.org/html5/html-author/charref" target="_blank" hack="_">complete list of all of the HTML entities</a>.

So to render the &lt; symbol, you can type
{% highlight html %}
1 &lt; 10
{% endhighlight %}
which will render
{% highlight html %}
1 < 10
{% endhighlight %}


<a id="exercise-2"></a>

### Exercise 2: Create your own document

> You have the knowledge to create your first document, so we need to strengthen your confidence and skills by building a document from scratch.
>
> 1. Download a code editor if you don't have one already.  I recommend <a href="https://atom.io/" target="_blank" hack="_">Atom</a>.
>
> 2. Open your code editor, and create a file named "index.html"
>
> 3. Create a document that:
>
> 3. Has the title "My Interests"
>
> 3. Specifies you as the author in its metdata
>
> 3. Displays a headline "My Interests"
>
> 3. List 3 interests (they don't have to be real).
>
> 4. Style headline so that it is green.
>
> <a href="/demos/html/interests.html" target="_blank" hack="_">Click here to see a sample solution</a>


<br/><br/>

## Related topics
<br/>

#### CSS

CSS stands for **Cascading Style Sheets**, and it is the **style language for describing how the HTML elements are rendered**.  You can include stylesheets into your html by using the link tag which should be included inside of the head element.  Ex: `<link href="/main.css" rel="stylesheet" type="text/css"/>`.


#### The box model

![the box model](/images/posts/html/box-model.png "the box model")

The <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model" target="_blank" hack="_">box model describes how an element is rendered on the page</a>.  It is very important to understand this before trying to add complicated styles, but it is very simple.  Every element is rendered using the box model which has four parts:
**content width**, **padding**, **border**, and **margin**.

#### MDN

Mozilla has amazing documentation on everything web related called <a href="https://developer.mozilla.org/en-US/docs/Web/HTML" target="_blank" hack="_">the Mozilla Developer Network, or MDN</a>.

#### W3C

The W3C stands for World Wide Web Consortium, which is the international standards organization for the Web.  They wrote the <a href="https://www.w3.org/TR/html5/" target="_blank" hack="_">specification of how HTML5 works</a>.  They govern what elements should be included/removed, which attributes are legal, etc.

#### The DOM

The DOM stands for the <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model" target="_blank" hack="_">Document Object Model</a>.  It is an Application Programming Interface (API) for updating the HTML on the page.  You may hear something like "The DOM is ready."  This is because it takes time for the HTML downloaded, and once it is downloaded, the text has to be parsed by the browser to create an internal representation.  Once it has done that, the DOM is ready.  This is different than the page being "loaded".  Even though the DOM is complete, images, videos, or CSS must be loaded to render the page properly.  Once all other assets are loaded then the page has "loaded".  So just be aware that there are two important events related to loading the page.


#### XML &amp; DTD

XML is related to HTML in that they are both Markup Languages, but XML is a more general form of HTML.  You can specify a DTD which stands for **Document Type Definition**.  This is where all of the elements and attributes are defined for an XML document.  Ever since HTML5, though, <a href="https://www.w3.org/TR/html5/the-xhtml-syntax.html#writing-xhtml-documents" target="_blank" hack="_">there is no longer a DTD for HTML5</a>.  It turns out that DTDs are suited for some of the wanted features in HTML5 such as all attributes that start with `data-` are valid attributes.
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<!-- classes, ids -->
<!-- rendering, box model, css -->
<!-- forms -->
