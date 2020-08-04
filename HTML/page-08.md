# Attributes

Elements can also have attributes. Attributes look like this:

<img src="https://mdn.mozillademos.org/files/9345/grumpy-cat-attribute-small.png" alt="Illustration of the class attribute, added to a paragraph">

Attributes contain extra information about the element that won't appear in the content. In this example, the `class attribute` is an identifying name used to target the element (the image) with style information.

> An attribute should have:

- A space between it and the element name. (For an element with more than one attribute, the attributes should be separated by spaces too.)
- The attribute name, followed by an equal sign.
- An attribute value, wrapped with opening and closing quote marks.

Another example of an element is `<a>`. This stands for anchor. An anchor can make the text it encloses into a hyperlink. Anchors can take a number of attributes, but several are as follows:

- href: This attribute's value specifies the web address for the link. For example: `href="https://www.mozilla.org/"`.

- title: The title attribute specifies extra information about the link, such as a description of the page that is being linked to. For example, `title="The Mozilla homepage"`. This appears as a tooltip when a cursor hovers over the element.

- target: The target attribute specifies the browsing context used to display the link. For example, `target="_blank"` will display the link in a new tab. If you want to display the linked content in the current tab, just omit this attribute.

So the link with its attributes:

```
<a href="" title="" target="">Mozilla, home of Firefox</a>
```
And the link with attributes and values:

```
<a href="https://www.mozilla.org/" title="The Mozilla homepage" target="_blank">Mozilla, home of Firefox</a>
```
On the page this will simply look lik this. The attributes are not shown. Only the title appears as a Tool Tip.

<a href="https://www.mozilla.org/" title="The Mozilla homepage" target="_blank">Mozilla, home of Firefox</a>

> Tip - Note that the `target="_blank"` attribute and value are not the best for both usability and accessibility. This essentially **takes over the users computer**, opening up a new window or tab. Not cool. The user should be left to decide this for themselves. A visually impaired user may struggle to notice a new tab or window has been created.

## Boolean attributes

Sometimes you will see attributes written without values. This is entirely acceptable. These are called Boolean attributes. Boolean attributes can only have one value, which is generally the same as the attribute name. For example, consider the disabled attribute, which you can assign to form input elements. (You use this to disable the form input elements so the user can't make entries.) For example:

```
<input type="text" disabled="disabled">
```
As shorthand, it is acceptable to write this as follows:
```
<input type="text" disabled>
```
If you don't want it disabled, you just leave it out altogether.
```
<input type="text">  
```
This is more than you need to know at this stage as but the essential take away is: 
> If a boolean attribute is present, its value is true, and if it’s absent, its value is false.


## Omitting quotes around attribute values

If you look at code for a lot of other sites, you might come across a number of strange markup styles, including attribute values without quotes. This is permitted in certain circumstances, but it can also break your markup in other circumstances. For example, if we revisit our link example from earlier, we could write a basic version with only the href attribute, like this:

```
<a href=https://www.mozilla.org/>favorite website</a>
```

However, as soon as we add the title attribute in this way, there are problems:

```
<a href=https://www.mozilla.org/ title=The Mozilla homepage>favorite website</a>
```

As written above, the browser misinterprets the markup, mistaking the title attribute for three attributes:  a title attribute with the value The, and two Boolean attributes, Mozilla and homepage. Obviously, this is not intended! It will cause errors or unexpected behavior, as you can see in the live example below. Try hovering over the link to view the title text!

<a href=https://www.mozilla.org/ title=The Mozilla homepage>favorite website</a>

Always include the attribute quotes. It avoids such problems, and results in more readable code.

```
<a href=https://www.mozilla.org/ title="The Mozilla homepage">favorite website</a>
```

### Single or double quotes?

In this tutorial you will also notice that the attributes are wrapped in double quotes. However, you might see single quotes in some HTML code. This is a matter of style.  

Both of these lines are equivalent (and correct html):
```
<a href="http://www.example.com">A link to my example.</a>
```

```
<a href='http://www.example.com'>A link to my example.</a>
```

Make sure you don't mix single quotes and double quotes. This example (below) shows a kind of mixing quotes that will go wrong:

```
<a href="http://www.example.com'>A link to my example.</a>
However, if you use one type of quote, you can include the other type of quote inside your attribute values:
```

```
<a href="http://www.example.com" title="Isn't this fun?">A link to my example.</a>
```

To use quote marks inside other quote marks of the same type (single quote or double quote), use HTML entities (more on these later). For example, this will break:

```
<a href='http://www.example.com' title='Isn't this fun?'>A link to my example.</a>
```

Instead, you need to do this:

```
<a href='http://www.example.com' title='Isn&apos;t this fun?'>A link to my example.</a>
```

> **Please note** - For all of your coursework we want you to use double quotes.

## Deeper Learning

> LinkedIn Learning Video: [Jen Simmons - html attributes](https://www.linkedin.com/learning/html-essential-training-4/html-attributes?u=36102708) 3m 54s

> MDN: Attributes - [HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)

### &copy; Credit given
Materials used under the Creative Commons licence from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML).