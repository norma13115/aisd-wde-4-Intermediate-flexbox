
# WDE05 Advanced Flexbox

This project is an assignment where you will learn how to create a responsive website using Flexbox. You will build a simple webpage that includes a navigation bar, a main section, and a footer. The website will be responsive, meaning it will look good on devices of all sizes.

## Prerequisites

- Basic knowledge of HTML and CSS
- Code editor (e.g., VS Code)
- Web browser for testing

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
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Flexbox Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

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

#### Add the Footer

In `index.html`, below the main section code after the `</main>`git a tag, add the following code for the footer:

```html
<footer>
    <p>&copy; 2024 Your Website</p>
</footer>
```

### Step 3: Style with CSS

Open `style.css` and add the following styles:

#### Add Basic Reset and Body Styles

```css
/* Reset margin, padding, and box-sizing for all elements */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Set height of html and body to 100% to ensure they take up the full height of the viewport */
html, body {
    height: 100%;
}

/* Ensure the main content area takes up remaining space between header and footer */
main {
    flex: 1;
}

/* Make body a flex container and set up flexbox layout */
body {
    font-family: Arial, sans-serif;
    min-height: 100vh; /* Ensures the body takes up at least the full height of the viewport */
    display: flex; /* Enables Flexbox on the body element */
    flex-direction: column; /* Arranges children (header, main, footer) in a column */
    background-color: lightgray;
}
```

#### Style the Header and Navigation Bar

```css
header {
    background-color: #333;
    color: white;
    padding: 1em 0;
}

/* Make the navigation menu a flex container */
nav ul {
    display: flex; /* Enables Flexbox on the ul element */
    justify-content: center; /* Centers the navigation items horizontally */
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

#### Style the Hero Section

```css
.hero {
    text-align: center;
    padding: 2em 0;
    color: Black;
    display: flex; /* Enables Flexbox on the hero section */
    flex-direction: column; /* Arranges children in a column */
    align-items: center; /* Centers content horizontally */
    justify-content: center; /* Centers content vertically */
    flex: 1; /* Allows the hero section to grow and take up available space */
}
```

#### Style the Content Section

```css
.content {
    display: flex; /* Enables Flexbox on the content section */
    justify-content: space-between; /* Distributes space between content boxes */
    padding: 2em;
    flex-wrap: wrap; /* Allows the content boxes to wrap to the next line if needed */
    flex: 1; /* Allows the content section to grow and take up available space */
}

/* Style for individual content boxes */
.content .box {
    background-color: #f4f4f4;
    padding: 5em;
    width: 30%; /* Sets the base width of each box */
    text-align: center;
    border-radius: 5px;
    margin-bottom: 1em;
    flex: 1 1 400px; /* Makes the boxes flexible and responsive: grow and shrink, with a minimum width of 400px */
    margin: 0.5em; /* Adds margin around each box */
}
```

#### Style the Footer

```css
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}
```


### Step 4: Test Your Website

Open `index.html` in your web browser and check if the website is responsive by resizing the browser window.


## Conclusion

You have successfully created a responsive website using Flexbox. You can further enhance the website by adding more content and styles. Keep practicing to master Flexbox!
