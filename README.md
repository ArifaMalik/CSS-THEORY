# CSS-THEORY

# Q1: What is CSS and how do you add it to an HTML page?


■What is CSS?

CSS stands for Cascading Style Sheets. It is used to style and design web pages.

HTML is used to create the structure of a webpage (like headings, paragraphs, etc.),
while CSS is used to make it visually attractive and user-friendly.


■What problem does CSS solve?

Without CSS:

•Web pages look plain and boring

•No colors, layout, or proper spacing

With CSS:

•Adds colors and styling 

•Controls layout and positioning

•Improves fonts and spacing 

•Makes websites responsive 


Three ways to add CSS

1. Inline CSS
   
CSS is written directly inside the HTML tag.


HTML
<p style="color: red;">This is Inline CSS</p>

Used for small, quick changes


2. Internal CSS

CSS is written inside the <style> tag in the same HTML file.


HTML
<style>
  p {
    color: blue;
  }
</style>

Useful for small projects

3. External CSS (Recommended )
   
CSS is written in a separate file and linked to HTML.


HTML
<link rel="stylesheet" href="style.css">
CSS
p {
  color: green;
}

Best for real-world projects


■Why External CSS is Recommended?

Keeps code clean and organized

Can be reused on multiple pages

Easy to maintain and update

Improves performance using browser caching


Combined Example


HTML File

HTML
<!DOCTYPE html>
<html>
<head>
  <title>CSS Example</title>

  <!-- External CSS -->
  <link rel="stylesheet" href="style.css">

  <!-- Internal CSS -->
  <style>
    h1 {
      color: blue;
    }
  </style>

</head>
<body>

  <!-- Inline CSS -->
  <p style="color: red;">This is Inline CSS</p>

  <h1>This is Internal CSS</h1>

  <h2>This is External CSS</h2>

</body>
</html>

style.css

CSS
h2 {
  color: green;
}


# Q2: Explain CSS Selectors with examples

What are CSS Selectors?

CSS selectors are used to target HTML elements so we can apply styles to them.

They help developers control which elements should be styled and how.

# Types of CSS Selectors (with examples)

1. Element Selector
   
Targets all elements of a specific type.

CSS

p {
  color: red;
}

3. Class Selector
   
Targets elements with a specific class.

CSS

.box {
  background-color: yellow;
}

HTML

<div class="box">Hello</div>

3. ID Selector
   
Targets a unique element using its ID.

CSS

#title {
  font-size: 30px;
}

HTML

<h1 id="title">Heading</h1>

4. Group Selector
   
Targets multiple elements at once.

CSS

h1, p {
  color: blue;
}

6. Descendant Selector
   
Targets elements inside another element (not necessarily direct).

CSS

div p {
  color: green;
}

9. Child Selector
   
Targets only direct children.

CSS

div > p {
  color: orange;
}

8. Universal Selector
   
Targets all elements.

CSS

* {
  margin: 0;
  padding: 0;
}



■Which selector has the highest specificity?


•ID selector (#) has the highest specificity

Order:

Inline > ID > Class > Element

Direct Child vs Descendant

•div p → selects all paragraphs inside div (even nested)

•div > p → selects only direct children


■Can you use the same class on multiple elements?


Yes (recommended)


■Can you use the same ID on multiple elements?


 No (must be unique)

Code : 
Using ALL 7 selectors


HTML

<!DOCTYPE html>
<html>
<head>
  <title>Selectors Example</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <h1 id="title">Main Heading</h1>

  <p>This is a paragraph</p>

  <div class="box">
    <p>Paragraph inside div</p>
    <span>
      <p>Nested paragraph</p>
    </span>
  </div>

  <h2 class="box">Another element with class</h2>

</body>
</html>
 


CSS (style.css)

CSS

/* Universal selector */
* {
  margin: 0;
  padding: 0;
}

/* Element selector */
p {
  color: red;
}

/* Class selector */
.box {
  background-color: lightgray;
}

/* ID selector */
#title {
  color: blue;
}

/* Group selector */
h1, h2 {
  font-family: Arial;
}

/* Descendant selector */
div p {
  color: green;
}

/* Child selector */
div > p {
  font-weight: bold;
}


# Q3: What is the CSS Box Model? Explain each layer.


■What is the CSS Box Model?

In CSS, every HTML element is treated as a rectangular box.

This box consists of different layers that control spacing, size, and layout.
The CSS Box Model has 4 main layers:

Margin → Border → Padding → Content

■Step-by-Step Explanation of Each Layer

1. Content (Innermost Layer)
   
This is the actual content of the element (text, image, etc.)

It is the innermost layer

Example:

CSS

width: 300px;
height: 100px;

3. Padding

Space inside the element, between content and border

•It increases space around content
•Padding is inside the border

CSS

padding: 20px;

4. Border
   
A line that wraps around padding and content
Used to give visible boundaries

CSS

border: 2px solid black;

6. Margin (Outermost Layer)
   
Space outside the element
Creates distance between elements

CSS

margin: 16px;

■Which layer is the innermost?

•Content is the innermost layer

■Is padding inside or outside the border?

Padding is inside the border 

■What does margin: 0 auto do?

It centers a block element horizontally

CSS

margin: 0 auto;

•Works only when:
Element has a fixed width

•Display is block
Box-Sizing Property
content-box (Default)
Width includes only content

•Padding and border are added separately

• Total size becomes bigger

▪︎border-box (Recommended )

Width includes:
content + padding + border

Layout becomes easier and predictable


■With border-box, does width include padding?

YES (width includes padding and border)


•Code Task (Required)

CSS

.box {
  width: 300px;
  padding: 20px;
  border: 2px solid black;
  margin: 16px;
  box-sizing: border-box;
}

Example with HTML

HTML

<div class="box">
  This is a box model example
</div>

# Q4. Explain CSS Colors. What are the different ways to define a color?

CSS colors are used to style text, backgrounds, borders, and other elements on a webpage.
CSS provides five main color formats:


1. Named Colors
   
CSS supports predefined color names.

CSS

color: orange;

3. HEX (Hexadecimal)
   
HEX colors start with # followed by 6 hexadecimal digits.

CSS

color: #F97316;

5. RGB (Red, Green, Blue)
   
Each color component ranges from 0 to 255.

CSS

color: rgb(249, 115, 22);

7. RGBA (RGB + Alpha)
   
RGBA adds transparency using the Alpha value.

CSS

color: rgba(249, 115, 22, 0.5);

9. HSL (Hue, Saturation, Lightness)
    
Hue = color angle (0–360°)

Saturation = intensity (%)

Lightness = brightness (%)

CSS

color: hsl(25, 95%, 53%);

■Which format is most commonly used by developers?

HEX is the most commonly used format because it is short, easy to read, and widely supported.

■What does the "A" in RGBA stand for?

A = Alpha, which controls transparency.

CSS

rgba(249,115,22,0.5)

0 = fully transparent

1 = fully visible


Difference between opacity: 0.5 and rgba(0,0,0,0.5)

Using Opacity

CSS

.box {
    opacity: 0.5;
}

Makes the entire element transparent.
Child elements are also affected.

Using RGBA

CSS

.box {
    background-color: rgba(0,0,0,0.5);
}

Only the specified color becomes transparent.
Child elements are NOT affected.

■Does opacity affect child elements?

Yes, opacity affects the parent and all child elements.

■Does rgba affect child elements?

No, rgba only affects the color where it is applied.


Code Task: Write the same orange color (#F97316) in all five formats

CSS

/* Named */
color: orange;

/* HEX */
color: #F97316;

/* RGB */
color: rgb(249, 115, 22);

/* RGBA */
color: rgba(249, 115, 22, 1);

/* HSL */
color: hsl(25, 95%, 53%);


# Q5. What are CSS Units? Explain px, %, rem, em, vh, and vw.


CSS units are used to define sizes for text, widths, heights, margins, padding, and layouts.

1. px (Pixels)
   
A fixed unit that does not change based on screen size.

CSS

font-size: 16px;

Use Case: Borders, icons, small fixed-size elements.

3. % (Percentage)
   
Relative to the parent element.

CSS

width: 50%;

If parent width is 800px:

Plain text

50% = 400px

% is relative to the parent or root?

 Usually relative to the parent element.
 
5. rem (Root EM)
   
Relative to the root (html) font size.

CSS

font-size: 2rem;

■What is 1rem equal to by default?

CSS

1rem = 16px

(Default browser font size)

■Why is rem better than px for accessibility?

Scales with user browser settings.

Improves responsiveness.

Better accessibility for visually impaired users.

7. em
   
Relative to the font size of the parent element.

CSS

.parent {
    font-size: 20px;
}

.child {
    font-size: 2em; /* 40px */
}
Use Case: Component-based sizing.

5. vh (Viewport Height)
   
Relative to the height of the browser window.

CSS

height: 100vh;

■vh stands for?

Viewport Height

CSS

100vh = Full screen height

50vh = Half screen height

7. vw (Viewport Width)
   
Relative to the width of the browser window.

CSS

width: 100vw;

CSS

50vw = Half screen width

100vw = Full screen width

General Rule
For Font Sizes
Prefer rem


CSS

font-size: 1.2rem;

Reason:

•Responsive
Accessible
Consistent
For Widths
Prefer %

CSS

width: 80%;

Reason:

•Adapts to parent container

•For Full-Screen Sections

•Prefer vh (and vw when needed)

CSS

height: 100vh;

Reason:

•Occupies the full viewport
Code Task: Hero Section CSS

CSS


.hero {
    height: 100vh;      /* Full viewport height */
    width: 100%;
    max-width: 80rem;   /* Max width using rem */
    margin: 0 auto;

    font-size: 3vw;     /* Font scales with viewport */
    display: flex;
    justify-content: center;
    align-items: center;
}


# Q6. What is CSS Specificity and how does the Cascade work?

When multiple CSS rules target the same element, the browser
decides which rule will be applied. This process is called CSS
Specificity and Cascade.

■What is CSS Specificity?

Specificity is a scoring system used by browsers to determine which CSS rule has higher priority.

Specificity Order (Highest to Lowest)

Selector Type
Specificity Score
Inline Style
1000

ID Selector (#id)
100

Class, Attribute, Pseudo-class (.class)
10

Element Selector (p, div)
1

Universal Selector (*)
0

■Which has higher specificity: a class or an element selector?

Class selector has higher specificity.

CSS

p {
    color: blue;
}

.text {
    color: red;
}

HTML

<p class="text">Hello</p>

Output: Red

Because .text (10) is higher than p (1).

■What specificity score does an inline style have?

Inline style has the highest normal specificity:

HTML

<p style="color: green;">Hello</p>
Specificity = 1000

■What is the CSS Cascade?

The cascade is the process by which the browser
chooses which CSS rule wins.

The browser checks:

1. Importance

!important wins first.

2. Specificity

Higher specificity wins.

3. Source Order

If specificity is equal, the rule written later wins.

■If two rules have equal specificity, which one wins?

The rule written later in the stylesheet wins.

CSS

p {
    color: blue;
}

p {
    color: red;
}

Output: Red

Because the second rule appears later.

■What does !important do?

!important overrides normal specificity rules.

CSS

p {
    color: blue !important;
}

#intro {
    color: red;
}

Output: Blue

Because !important has higher priority.


■Why should !important be avoided?

•Makes CSS difficult to maintain.

•Breaks the normal cascade.

•Causes debugging problems.

•Leads to CSS conflicts.

Use it only when absolutely necessary.

Code Task


HTML

<p id="intro" class="text">Hello</p>




CSS

p {
    color: blue;
}

.text {
    color: green;
}

#intro {
    color: red;
}

Specificity Scores
Plain text

p       = 1

.text   = 10

#intro  = 100

■Which color wins?

Red

Because the ID selector (#intro) has the highest specificity.


  Summary

Plain text

Inline Style = 1000

ID Selector  = 100

Class        = 10

Element      = 1


# Q7. Explain CSS Flexbox. How does it differ from block layout?

■What is Flexbox?

Flexbox (Flexible Box Layout) is a one-dimensional layout system used to arrange items in rows or columns.

To enable Flexbox:

CSS

.container {
    display: flex;
}

The parent becomes a flex container and its children become flex items.

Difference Between Flexbox and Block Layout

Block Layout

CSS

div {
    display: block;
}

Elements appear one below another.

Takes full available width.

Harder to align items horizontally.

Example:

Logo
Home
About
Contact
Flexbox Layout

CSS

.container {
    display: flex;
}

Items can be arranged in rows or columns.

Easy alignment and spacing.

Responsive layouts become simpler.

Example:


Logo  Home  About  Contact


Important Flexbox Properties


1. flex-direction
   
Defines the main axis direction.

CSS

.container {
    display: flex;
    flex-direction: row;
}


3. justify-content

Aligns items along the main axis.

CSS

.container {
    justify-content: center;
}


4. align-items
   
Aligns items along the cross axis.

CSS

.container {
    align-items: center;
}


Difference between justify-content and align-items?


justify-content → Left ↔ Right
align-items → Top ↕ Bottom

6. flex-wrap
   
Controls whether items move to the next line.

CSS

.container {
    flex-wrap: wrap;
}

■What does flex-wrap: wrap do?

 Items automatically move to the next line when there is not enough space.
 
8. gap
   
Adds spacing between flex items.

CSS

.container {
    gap: 20px;
}

10. flex: 1
    
Allows an item to grow and take available space.

CSS

.item {
    flex: 1;
}

■What does flex: 1 do?

Makes items expand equally and fill the available space.

■How do you center an element both horizontally and vertically?

CSS

.container {
    display: flex;
    justify-content: center;
    align-items: center;
}


Real-World Use Cases of Flexbox

1. Navigation Bar
   
Logo      Home About Contact

3. Card Layouts
   
Card 1   Card 2   Card 3

Flexible and responsive arrangement of cards.


Code Task: CSS Navbar Using Flexbox


HTML

HTML
<nav class="navbar">
    <div class="logo">Logo</div>

    <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>


CSS

.navbar {
    display: flex;
    justify-content: space-between; /* Logo left, links right */
    align-items: center;            /* Vertical center */
    padding: 15px 30px;
}

.nav-links {
    display: flex;
    gap: 20px;                      /* Space between links */
    list-style: none;
    margin: 0;
    padding: 0;
}

.nav-links a {
    text-decoration: none;
    color: black;
}


Output

Logo                     Home About Services Contact


# Q8. What are CSS Pseudo-classes and Pseudo-elements?

Pseudo-classes and pseudo-elements allow you to style elements based on their

state or add virtual content without changing the HTML.

Common Pseudo-classes

1. :hover
   
Applies styles when the mouse pointer is over an element.

CSS

button:hover {
    background-color: orange;
}

3. :focus
   
Applies styles when an element receives focus.

CSS

input:focus {
    border: 2px solid blue;
}

5. :nth-child()
   
Selects elements based on their position among siblings.

CSS

li:nth-child(2) {
    color: red;
}

■What does :nth-child(2n) select?

 It selects every even-numbered element.
 

2nd, 4th, 6th, 8th ...

Example:

CSS

li:nth-child(2n) {
    background-color: lightgray;
}

7. :not()
   
Selects all elements except those matching the given selector.

CSS

p:not(.active) {
    color: gray;
}


Common Pseudo-elements

1. ::before
   
Adds content before an element.

CSS

p::before {
    content: "★ ";
}

3. ::after
   
Adds content after an element.

CSS

p::after {
    content: " ✓";
}

5. ::placeholder

Styles placeholder text inside form fields.
CSS
input::placeholder {
    color: gray;
}


■Does ::before add a real HTML element?

 No
 
::before creates a virtual element for styling purposes only. It does not appear in the HTML document.

■What CSS property is required for ::before and ::after?

The content property is required.

Example:

CSS

p::before {
    content: "★";
}

Without content, ::before and ::after will not appear.

■How would you style every 3rd list item?

Use:

CSS
li:nth-child(3n) {
    color: blue;
}

■What is the content property used for?

The content property is used with ::before and ::after to insert text, symbols, icons, or other generated content.

Example:

CSS
h2::before {
    content: "📌 ";
}

Output:

📌 

Code Task


HTML
<button>Click Me</button>

<ul>
    <li class="featured">HTML</li>
    <li>CSS</li>
    <li class="featured">JavaScript</li>
</ul>

<input type="text" placeholder="Enter your name">
CSS
CSS
/* Turn button orange on hover */
button:hover {
    background-color: orange;
    color: white;
}

/* Add a star before every featured item */
.featured::before {
    content: "★ ";
    color: orange;
}

/* Style placeholder text grey */
input::placeholder {
    color: gray;
}

■Summary

Pseudo-classes (:)

CSS

:hover

:focus

:nth-child()

:not()

Used to style elements based on their state or position.

Pseudo-elements (::)

CSS

::before

::after

::placeholder

Used to style parts of elements or add virtual content.


# Q9. Explain CSS Transitions and Animations

CSS Transitions and Animations allow elements to change smoothly without using JavaScript.

■What is a CSS Transition?

A transition creates a smooth change from one state to another when a property changes.

Common Transition Triggers

:hover

:focus

:active

Adding/removing a class with JavaScript

Example:

CSS

button {
    background: blue;
    transition: background-color 0.3s ease;
}

button:hover {
    background: orange;
}

Transition Shorthand

CSS

transition: property duration timing-function delay;

Example:

CSS

transition: all 0.5s ease 0s;

■How long the transition takes
timing-function
Speed curve of animation
delay?

Wait time before starting
Timing Functions

ease

Starts slow, speeds up, then slows down.

CSS

transition-timing-function: ease;

ease-in

Starts slowly.

CSS

transition-timing-function: ease-in;

ease-out

Ends slowly.

CSS

transition-timing-function: ease-out;
linear

Constant speed throughout.

CSS

transition-timing-function: linear;

■Can you have multiple transitions on one element?

Yes.

CSS

transition:
    transform 0.3s ease,
    box-shadow 0.3s ease,
    background-color 0.3s ease;
    
■What is a CSS Animation?

Animations can run automatically and do not require a trigger.
They are created using @keyframes.

@keyframes Example

CSS

@keyframes fadeIn {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}

Apply it:

CSS
.box {
    animation: fadeIn 1s ease;
}

Animation Shorthand

CSS

animation:
    name
    duration
    timing-function
    delay
    iteration-count
    direction
    fill-mode;
Example:

CSS

animation: fadeIn 1s ease 0s 1 normal forwards;

■What does animation-fill-mode: forwards do?

CSS

animation-fill-mode: forwards;

Keeps the final animation state after the animation ends.
Without forwards, the element returns to its original state.

■What does animation-iteration-count: infinite do?

CSS

animation-iteration-count: infinite;
Repeats the animation forever.

Example:

CSS

.loader {
    animation: spin 2s linear infinite;
}

■Why should you prefer transform and opacity?

Good Performance

CSS

transform: translateY(-10px);
opacity: 0.8;

CSS

width: 300px;
margin-left: 50px;

Animating width or margin causes layout recalculations and is slower.


Code Task


HTML

<div class="card">
    Card Content
</div>

CSS

/* Fade-in animation from below */
@keyframes fadeUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.card {
    width: 300px;
    padding: 20px;
    background: white;
    border-radius: 10px;

    animation: fadeUp 1s ease forwards;

    transition:
        transform 0.3s ease,
        box-shadow 0.3s ease;
}

/* Hover effect */
.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

# Q10. What is Responsive Web Design? Explain Media Queries, CSS Variables, and Mobile-First Approach.

Responsive Web Design (RWD) ensures a website looks good and works properly on all screen sizes such as mobile phones, tablets, laptops, and desktops.


Part A — Media Queries

■What is a Media Query?

Media queries apply CSS only when specific conditions are met.

Syntax

CSS

@media (condition) {
    /* CSS Rules */
}
Example:

CSS

@media (max-width: 768px) {
    body {
        background: lightgray;
    }
}


In Mobile-First, do you use min-width or max-width?

 Use min-width
 
Example:

CSS

@media (min-width: 768px) {
    /* Tablet styles */
}

■What does @media (prefers-color-scheme: dark) do?

Detects if the user prefers dark mode.

CSS

@media (prefers-color-scheme: dark) {
    body {
        background: #121212;
        color: white;
    }
}


Part B — Mobile-First Approach

■What is Mobile-First?

Mobile-first means designing for mobile devices first and then adding styles for larger screens.

Example:

CSS

/* Mobile */
.container {
    padding: 10px;
}

/* Tablet */
@media (min-width: 768px) {
    .container {
        padding: 20px;
    }
}

■Why is Mobile-First the Industry Standard?

Better performance

Easier scaling

Cleaner code

Improved mobile experience

Supports responsive design naturally


■What are CSS Variables?

CSS Variables (Custom Properties) store reusable values.

Define Variables

CSS

:root {
    --primary-color: #2563eb;
    --spacing: 1rem;
}

Use Variables

CSS
button {
    background: var(--primary-color);
    padding: var(--spacing);
}

■Can JavaScript read and change CSS variables?

 Yes.
 
JavaScript

document.documentElement.style
.setProperty('--primary-color', 'red');

Difference Between var(--color) and var(--color, fallback)
Without Fallback

CSS

color: var(--primary-color);

If the variable does not exist, the property fails.

With Fallback

CSS

color: var(--primary-color, blue);

If the variable is missing, blue will be used.

Code Task


CSS

/* ==========================
   Design System Variables
========================== */

:root {
    --primary-color: #2563eb;
    --secondary-color: #f97316;

    --bg-color: #ffffff;
    --text-color: #222222;

    --font-size-base: 16px;

    --space-sm: 0.5rem;
    --space-md: 1rem;
    --space-lg: 2rem;
}

/* ==========================
   Global Styles
========================== */

body {
    background: var(--bg-color);
    color: var(--text-color);
    font-size: var(--font-size-base);
    margin: 0;
    padding: var(--space-md);
}

/* ==========================
   Dark Theme
========================== */

[data-theme="dark"] {
    --bg-color: #121212;
    --text-color: #ffffff;
}

/* ==========================
   Mobile First
========================== */

.container {
    width: 100%;
    padding: var(--space-md);
}

/* Tablet (768px) */
@media (min-width: 768px) {
    .container {
        max-width: 720px;
        margin: auto;
    }
}

/* Desktop (1024px) */
@media (min-width: 1024px) {
    .container {
        max-width: 960px;
    }
}
