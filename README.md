# article with sekx


Pseudo-elements and pseudo-classes are commonly used in CSS. If you have written css before, you have used them. You just might not have realized yet. But, what are Pseudo-elements and pseudo-classes? What do they do? How do you differentiate between them?
In this short article, I will help you answer these questions.

## Pseudo-classes

While a CSS class is an attribute that is used to apply multiple CSS properties on an HTML element, a pseudo-class is a modifier of the initial properties of the class or element. Pseudo-classes are used when selectors (classes or html elements) meet certain conditions. 

Generally, pseudo-classes are prefixed by a colon, `:`. This is the fastest way to easily identify a pseudo-class. Here are some popular ones : `:hover, :focus`.
Pseudo-classes deal with a css state that is **they modify the initial state given to an element or a class after meeting a certain condition**.

```bash
.demo {
    color: #ff0000;
    font-size: 1rem;
    font-weight: 500;
}

.demo:hover{
    color: #ffff00;
}
```

> In the code example above, we have a class demo that has a color property initially set to #ff0000 (red). Following it, we applied a pseudo-class, :hover, triggered only when we move a mouse over the element with the class demo; This is the condition that must be fulfilled for this effect to take place. The outcome of the event changes the color to #ff0000 (yellow).

Another fact to note about pseudo-classes is that it selects the entire element. This means that if you are using a pseudo-class such as :active, :hover, :focus on a paragraph, the pseudo-class you have provided will be applied on the whole paragraph irrespective of how long the paragrapgh is.

## Pseudo-elements

Unlike pseudo-classes, pseudo-elements are prefixed by a double colon `::`. Long ago, there were no difference between pseudo-elements and pseudo-classes because they both were prefixed with a single colon `:`. However, some browsers still support using a single colon to prefix pseudo-elements.

A pseudo-element allows you to define elements that are not in the DOM. Fake elements or false elements is another name Psuedo-elements are called. They have no element type as far as HTML is concerned because they do not exist in the DOM. They can only be created using CSS. 

Unlike pseudo-classes, pseudo-elements allow you to style a specific part of an element's content. For example, the pseudo-element `::first-line` allows you to style only the first line of a paragraph, while `::first-letter` allows you to select just the first letter of a paragraph and style it. 

It is worth noting that pseudo-elements does not work on all CSS properties. Let's take the `::first-letter` as an example. it can only take the font-size, color, font-weight, font-style properties, and a few more[A LINK SHOULD BE HERE].

```bash
.text::first-letter{
  color: red;
  font-size: 30px;
  font-style: italic;
}
```
> The above code example styles just the first letter of the element class with the text.

However, we can apply pseudo-classes and pseudo-elements on a class or element selector simultaneously,

```bash
 .text::first-letter{
  color: red;
  font-size: 30px;
  font-style: italic;
}
.text:hover::first-letter{
  color: blue;
}
```

> The code example above is a practical example of how we can combine the pseudo-class and pseudo-element on a selector.
> The first rule selects the first letter of any element with the class "text" and applies a red color, a font size of 30 pixels, and an italic font style to it.The    second rule selects the first letter of any element with the class "text" when it is being hovered. It then applies a blue color.
>  So, when the mouse cursor hovers over the element, the color of the first letter changes from red to blue.

A big thank you for reading thus far. I hope you gained a few things and you enjoyed yourself.

Please if you find a typo or something I can inprove on, kindly reach out to me on Twitter at @DavidCanCode. Happy hacking!!!
