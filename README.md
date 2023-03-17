# sekxy
article with sekx


Pseudo-elements and pseudo-classes are commonly used in CSS and are essential components of web development in general. But what are they? What do they do? How do you differentiate between a pseudo-class and a pseudo-element?

In this article, we will take a short tour of the differences between a pseudo-class and a pseudo-element, as well as how to identify them at a glance.

Pseudo-classes

A CSS class is an attribute that is used to apply multiple CSS properties on an HTML element. A pseudo-class is a modifier of the initial properties of the class or element but only when those selectors meet certain conditions (we'll take a look at a conditions very soon). Generally, pseudo-classes are prefixed by one colon (:) before them, this is the fastest way to easily identify a pseudo-class.

Pseudo-classes deal with the state (properties), that is, they modify the initial state given to an element or a class after meeting a certain condition.

.demo {
    color: #ff0000;
    font-size: 1rem;
    font-weight: 500;
}

.demo:hover{
    color: #ffff00;
}

In the code example above, we have a class demo that has a color property initially set to #ff0000 (initial state), following it, we apply a pseudo-class (: hover), which is triggered only when we mouse over the element with the class demo, this is the condition that must be fulfilled for this effect to take place and the outcome of this effect is changing (modifying) the color to #ff0000 (yellow).

Another great fact to note about pseudo-classes is that it selects the entire element, this means that, if you are using a pseudo-class such as :active, :hover, :focus on a paragraph, the pseudo-class you have provided willbe applied on the whole paragraph irrespective of how long the paragrapgh is.

Pseudo-elements

Unlike pseudo-classes, pseudo-elements are prefixed by a double colon (::). Long ago, there were no differences between pseudo-elements and pseudo-classes because they were both prefixed by a single colon (:). Although most browsers still support using a single colon to prefix pseudo-elements.

A pseudo-element allows you to create or define elements that are not in the DOM. They are also known as fake elements or false elements. Pseudo-elements have no element type as far as the document language is concerned because they do not exist in the DOM. They can only be created using CSS. Unlike pseudo-classes, pseudo-elements, on the other hand, allow you to style a specific part of an element's content. For example, the pseudo-element ::first-line allows you to style only the first line of a paragraph, while ::first-letter allows you to select just the first letter of a paragraph and style it. It is worth noting that not all CSS properties can be used when using these pseudo-elements. Let's take the ::first-letter as an example; it can only take the font-size, color, font-weight, font-style properties, and a few more.

.text::first-letter{
  color: red;
  font-size: 30px;
  font-style: italic;
}

The above code example styles only the first letter of the element class with the text, as said ealier, the pseudo-element takes just a part of the element and styles it. The ::first-letter element in our case takes only the first letter of the elemet with the class text.

However, we can apply pseudo-classes and pseudo-elements on a class or element selector simultaneously,

 .text::first-letter{
  color: red;
  font-size: 30px;
  font-style: italic;
}
.text:hover::first-letter{
  color: blue;
}

This code example above is a practical example of how we can combine the pseudo-class and pseudo-element on a selector.

The first rule selects the first letter of any element with the class "text" and applies a red color, a font size of 30 pixels, and an italic font style to it.

The second rule selects the first letter of any element with the class "text" when it is being hovered over by the mouse cursor. It then applies a blue color to the first letter.

So, when the mouse cursor hovers over the element, the color of the first letter changes from red to blue.

A big thank you for reading thus far. I hope you gained a few things and you enjoyed yourself.

Please if you find a typo or something I can write better in this article, kindly reach out to me on Twitter at @DavidCanCode. Happy hacking!!!
