# WDE04 Intermediate Flexbox

![Screenshot of the project](assets/images/example.png)

## Description
This assignment will cover how to create a responsive website using Flexbox. You will build a simple webpage that includes a navigation bar, a main section, and a footer. The website will be responsive, meaning it will look good on devices of all sizes.

## Project Structure

```
responsive_flexbox_website
│   index.html
│   style.css
```

## Steps

### Step 1: Create the Project Structure

1. Create a new folder for your project.
2. Inside the folder, create two files: `index.html` and `style.css`.

### Step 2: Set Up the HTML

Add the HTML boilerplate:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Responsive Flexbox Website</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <!-- Content goes here -->
  </body>
</html>
```

**Explanation:**
- `<!DOCTYPE html>` declares the document type and version of HTML.
- The `<html lang="en">` tag defines the language of the document as English.
- `<meta charset="UTF-8" />` sets the character encoding to UTF-8, which supports most characters from various languages.
- The `<meta name="viewport" content="width=device-width, initial-scale=1.0" />` tag ensures the website is responsive by setting the viewport to the width of the device and scaling the content accordingly.
- The `<title>` tag sets the title of the webpage, which appears in the browser tab.
- The `<link rel="stylesheet" href="style.css" />` tag links the external CSS file (`style.css`) to the HTML document for styling.

#### Add the Navigation Bar

In `index.html`, within the `<body>` tag, add the following code for the navigation bar:

```html
<header>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```

**Explanation:**
- The `<header>` tag defines the header of the webpage, which typically contains the navigation menu.
- `<nav>` defines a navigation section and contains the `<ul>` (unordered list) element.
- The `<ul>` element holds a list of links, each contained within an `<li>` (list item) element.
- `<a href="#">Home</a>` is a hyperlink that, when clicked, will take the user to the specified URL. The `href="#"` attribute is a placeholder link.

#### Add the Main Section

In `index.html`, below the navigation bar code after the `</header>` tag, add the following code for the main section:

```html
<main>
  <section class="hero">
    <h1>Welcome to Our Website</h1>
    <p>This is a responsive website using Flexbox.</p>
  </section>
  <section class="content">
    <div class="box">Content Box 1</div>
    <div class="box">Content Box 2</div>
    <div class="box">Content Box 3</div>
    <div class="box">Content Box 4</div>
    <div class="box">Content Box 5</div>
    <div class="box">Content Box 6</div>
  </section>
</main>
```

**Explanation:**
- The `<main>` tag defines the main content area of the webpage. It contains two sections: the hero section and the content section.
- `<section class="hero">` defines a section with a class of "hero", used for the introductory content.
- `<h1>Welcome to Our Website</h1>` is a top-level heading that serves as the main title of the hero section.
- `<p>This is a responsive website using Flexbox.</p>` is a paragraph providing a brief description.
- `<section class="content">` defines a section with a class of "content", which will hold the individual content boxes.
- `<div class="box">Content Box 1</div>` represents a content box. The `div` element is a block-level container, and the `class="box"` applies the CSS styles associated with the "box" class.

#### Add the Footer

In `index.html`, below the main section code after the `</main>` tag, add the following code for the footer:

```html
<footer>
  <p>&copy; 2024 Your Website</p>
</footer>
```

**Explanation:**
- The `<footer>` tag defines the footer of the webpage, which typically contains copyright information or additional links.
- `<p>&copy; 2024 Your Website</p>` is a paragraph that displays the copyright symbol and the year.


### Step 3: Now Style with CSS

Open `style.css` and add the following styles:

#### Add Basic Reset and Body Styles

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  height: 100%;
}

main {
  flex: 1;
}

body {
  font-family: Arial, sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: lightgray;
}
```

**Explanation:**
- The `*` selector resets the margin, padding, and sets `box-sizing` to `border-box` for all elements. This ensures consistency across different browsers.
- The `html` and `body` selectors set their height to 100% so that they take up the full height of the viewport.
- The `main` selector is set to flex-grow (`flex: 1`) so it can expand to fill the space between the header and footer.
- The `body` selector is styled as a flex container, using Flexbox to arrange the header, main, and footer in a column. The `min-height: 100vh` ensures that the body takes up at least the full height of the viewport, and the background color is set to light gray.

#### Style the Header and Navigation Bar

```css
header {
  background-color: #333;
  color: white;
  padding: 1em 0;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
}

nav ul li {
  margin: 0 1em;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}
```

**Explanation:**
- The `header` selector is styled with a dark background color and white text, with padding on the top and bottom.
- The `nav ul` selector is styled as a flex container with centered items (`justify-content: center`), and the list-style is removed.
- The `nav ul li` selector adds horizontal spacing between each navigation item.
- The `nav ul li a` selector styles the links in the navigation bar, making the text white, removing the underline, and setting the font to bold.

#### Style the Hero Section

```css
.hero {
  text-align: center;
  padding: 2em 0;
  color: Black;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 1;
}
```

**Explanation:**
- The `hero` section is centered both horizontally (`text-align: center`) and vertically using Flexbox. It also has padding on the top and bottom.
- The `display: flex` makes the hero section a flex container, with its children arranged in a column (`flex-direction: column`), centered horizontally (`align-items: center`), and vertically (`justify-content: center`).
- The `flex: 1` allows the hero section to grow and take up available space.

#### Style the Content Section

```css
.content {
  display: flex;
  justify-content: space-between;
  padding: 2em;
  flex-wrap: wrap;
  flex: 1;
}

.content .box {
  background-color: #f4f4f4;
  padding: 5em;
  width: 30%;
  text-align: center;
  border-radius: 5px;
  margin-bottom: 1em;
  flex: 1 1 400px;
  margin: 0.5em;
}
```

**Explanation:**
- The `content` section is styled as a flex container with `space-between` alignment, ensuring equal space between content boxes. Padding is added for spacing inside the section.
- The `flex-wrap: wrap` allows the content boxes to wrap to the next line if necessary.
- The `content .box` selector styles individual content boxes with a light background color, padding, a specific width, and centered text. The `flex: 1 1 400px` makes each box flexible and responsive, allowing them to grow or shrink as needed with a minimum width of 400px. The margin adds spacing around each box.

#### Style the Footer

```css
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1em 0;
}
```

**Explanation:**
- The `footer` selector is styled with a dark background color and white text, similar to the header, and centered text with padding on the top and bottom.

## Testing Your Layout:

- Resize the browser window to see how the Flexbox layout adapts to different screen sizes.
- Copy and paste the HTML boxes a few more times to see how Flexbox handles the additional content, automatically wrapping and adjusting the layout. Resize the window again to observe how the layout remains responsive.

## AI Assistance

If you have any questions or need further explanations, feel free to ask the AI for help. Here are some examples of what you might ask:

- "How do I create a layout using Flexbox?"
- "How can I ensure my Flexbox layout is responsive?"

Good luck, and have fun building with Flexbox!

##

© All rights reserved to ThriveDX
