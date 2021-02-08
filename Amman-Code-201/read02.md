# HTML

## HTML Text

When structuring our HTML page, we need to write elements with tags that are called markups. Tags give meaning to the text they enclose and tell the browser how to display them. Two main categories of markup can sort them into:

1. Structural markup
2. Semantic markup: imply extra meaning to the contents, such as content that must be emphasized.

### Structural markup

#### Heading tag

The heading tag is structural. There are six levels of heading in HTML h1 through h6. h1 is used for the main heading, and if there is sub headings we use h2 and h3 and so on.

```html

<h1>This is level 1 heading</h1>
<h2>This is level 2 heading</h2>
<h3>This is level 3 heading</h3>
<h4>This is level 4 heading</h4>
<h5>This is level 5 heading</h5>
<h6>This is level 6 heading</h6>

```

#### Paragraph tag

Enclosing a text with \<p> and \</p>, tells the browser to display the content as paragraph. The browser will give each paragraph a new line.

```HTML

<p>This is a paragraph
ant we can make it more that one lind
but lines do not show in the browser</p>
<p>This is another paragraph</p>

```

#### Bold, Italic, Superscript, Subscript

We use \<b> tag to make the text insde bold in color, \<i> to make it italic, \<sup> to make it superscript and \<sub> to display a subscript text as in references and chemical formulas. All of these elements are going to be displayed inline.

```html

<p>
This <b>word</b> will be displayed in bold, While the <i>word</i> will be italic.
I added this <sup>word</sup> as super script and last <sub>word</sub> as a subscript.
</p>

```

#### White spaces

Browsers display adjacent spaces as one space even if it was a new line, so however times you add newlines and spaces, they will show as one space on the same line.

```html

<p>This is a paragraph                                   but this space will be elemented and only one space will remain</p>
<p> Even new lines


will not be considered and will be eliminated getting back to the same line before</p>

```

#### Line breaks and Horizontal rules

If we want to add a line break and show the rest of the text on new lines, we can use \<br /> which will begin the text next to it in a new line.
If we want to add a horizontal separator, we can add \<hr />, and it will show a fine line between the contents of the page. 

### Semantic markup

#### Emphasis and Strong 

Strong element implay that the content has strong importance that other content and it is displayed as bold.

```html

<p>
This text contains a <strong>Strong content</strong>
and it will be displayed as bold</p>

```

Emphasis element <em> display extra emphasis on the content and slight change of the meaning. The content displayed italic by default.

```html
<p>
This <em>Content here</em> is displayed italic and it is emphasised
</p>
```

#### Quotation

\<blockquote> is used for quotes that take a full paragraph, and we still need to use the \<p> tag inside it to write the content. It is displayed indented be dafault.
\<q> is used for inline quotes. Browsers tend to add quotation marks at the beginning and the end of the quote.
Both tags can als use the **cite**

```html

<blickquote cite="www.something.com/something/content">
<p>
a quote must be writen gere 
</p>
</blickquote>

<p> some thing happend and <q cite="www.something.com/something/content">this quote is inline</q> and here continue the text</p>

```

#### Abbreviations and Acronyms

\<abbr> tag is used to enclose abbreviated words like prof and doc, etc. 
\<acronym> tag is used to inclose acronyms like NASA and NATO, etc.
They both can use the **title** attribute to indicate the full abbreviation or acronym.

```html
<p><abbr title="Professor">Prof</abbr> Stephen
Hawking is a theoretical physicist and
cosmologist.</p>
<p><acronym title="National Aeronautics and Space
Administration">NASA</acronym> do some crazy
space stuff.</p>

```

#### Citation and Definition

We can use \<cite> to reference a name or a book, it will be rendered italic.
\<dfn> is used when new terminology is mentioned for the first time in the document. Some browsers display the comtent italicised.

```html

<p><cite>A Brief History of Time</cite> by Stephen
Hawking has sold over ten million copies
worldwide.</p>
<p>A <dfn>black hole</dfn> is a region of space from
which nothing, not even light, can escape.</p>

```

#### Author Details

Web pages authors can use the \<addresss> tag to add their address, it can be physical or email address and some times a phone number. It will also be displayed in italics.

```html

<address>
<p><a href="mailto:homer@example.org">
homer@example.org</a></p>
<p>742 Evergreen Terrace, Springfield.</p>
</address>

```

### Changes to content

Three main tags to indicate that a content is changed such as deleted \<del> or inserted content \<ins> or content that is no longer accurate or relevent but should not be deleted \<s>. \<del> and \<s> contents are displayed with a line through, whereas \<ins> is underlined.

```html

<p>It was the <del>worst</del> <ins>best</ins> idea
she had ever had.</p>
<p>Laptop computer:</p>
<p><s>Was $995</s></p>
<p>Now only $375</p>

```

## CSS - Introduction to Cascading Style Sheets

It is a designing direction to tell HTML pages how to display their elements. It is used to add "style" to the web page in different ways. Its main features are:

* Positioning.
* Resizing.
* Coloring.
* Aligning.

These are the main concept for what CSS created. There are also other useful functions and capabilities that CSS can add to web pages.

### How to write CSS code:

There are three ways to write CSS code, whether we can write it inline, internal, or external.

#### Inline CSS

By adding the style attribute to any HTML tag and changing properties inside the value of the attributes, we can add CSS styling on that particular tag:

```html

<h1 style="color:red;"> Any text </h1>

```

in the previous code, the color:red; inside the style tag is an inline CSS command. It tells the heading tag to change its text color to red. Although we can still write inline CSS and browsers do not complain about it, it is now considered bad practice, and we have to write CSS outside HTML tags.

#### Internal CSS

We can add a special \<style> tag inside the head of the HTML page, and then we add CSS between the opening and the closing tag. We first have to select the element or the group of elements that we want to change its style properties and add the property's name inside a set of curly braces separated by semi-colons. We write the value of the property after we add a colon between the value and the name:

```html

<html> 
    <head> 
        <style> h1{ color:red; background-color: blue; } </style> 
    </head> 
</html>

```

This way of writing the code inside the head is not so acceptable. Unless you have a one-page web site, do not use this approach. CSS files should be separated from HTML files, and this is the best practice.

#### External CSS

The best practice to add CSS code to your HTML pages is by creating a separate file, most likely to be called styles.css. Notes the extension of the file .css, which refers to the code inside it. At the head of the HTML page, we add a unique self-closing tag called \<link> inside the link; we add three attributes, rel its value should be stylesheet which tells the HTML what the relation between the file we want to link to with our HTML file is, and the href which tells the HTML the location of the file, and last, the type attribute which tells the page what kind of files it is, most of the time we specify text/CSS as its value.

```html

<html> 
    <head> 
        <link rel="stylesheet" href="some/location.css" type ="text/CSS" /> 
    </head> 
</html>

```

inside the CSS file, we write the code just as we do if it was internal. Write the element selector, and inside a set of curlies, we add the properties and their values separated by semi-colons.

```css

h1 { 
    color: red; 
    background-color: blue; 
    }

```

## Decicion Making and Loops

We, most of the time, won't build our application imperatively. There must be a work flow based on conditions, re-executing a particular block of code for a desired number of times, or continuing the running code based on the user's input and interaction with the web page.

Let's discover two fundamental concepts of programming. Conditions and Loops:

### Conditional statements

Conditional statements are pieces of code that are run based on an evaluated condition inside the check. The code that is run after the evaluation depends on the returned result; if it was True, the execution transferred to the immediate block of code that 
follows. 

```javascript

if (condition){
    cond statements;
}

```

We can also add whatever conditions to be checked after the first block and have the main condition evaluated to False, the next one will be checked, and so on until the check returns true. 

```javascript

if (condition 2){
    cond statements 1;
} else if (condition 2) {
    cond statement 2;
}

```

In the end, if no condition returned True, we can choose to either add an Else statement, or we can leave the code to continue without executing any if statements. 

```javascript
if (condition 2){
    cond statements 1;
} else if (condition 2) {
    cond satement 2;
} else {
    statement when no True condition;
}

```

### Loops:

Suppose that we want to execute a particular code a specific number of times. Should we write the same code that many times? It looks that the code is going to be cluttered and hard to read. Besides, what if we want the user to determine how much that number will be? Then, we should think about all possible numbers and write code for it. In fact, this does not work like this. In programming, there is a concept looping, in which you give the computer the command to run a code the number of times you or the user might want.
There are three types of looping statements in JavaScript; For loop, While loop, and Do While loop.

The *For* loop is used when you know exactly how many times you want to loop. The sentence contains three parts; a declaration, a condition, and an update statements. We start by declaring a variable that will be our initial value to start the loop. A condition is then checked against this value in which the loop will continue looping until this condition fails. 

```javascript
 for ( declaration ; condition; update ){
     statemets to execute;
 }

```

*While* loop is used when you do not know the number of times to loop through the code. In addition, you can use it for input checking when you expect the user to enter something like a password or a user name, as well as to check whether the date type entered is valed or not.
It starts by the keyword **While**, then you type the condition you want to check each time of looping followed by statements to execute.

```javascript
 while ( condition ){
     statemets to execute;
 }

```

Last but not lease, the *Do While loop*. This loop ensures that the code inside the loop will be executed at least one time. After that execution, the condition will check. If it was true it will continue looping until it fails.

```javascript
do{
    statements to execute;
} while ( condition );

```
