
# WDE05 Advanced FLexbox


# Responsive Website with Flexbox

## Overview

In this assignment, you will learn how to create a responsive website using Flexbox. You will build a simple webpage that includes a navigation bar, a main section, and a footer. The website will be responsive, meaning it will look good on devices of all sizes.

## Getting Started

### Prerequisites

- Basic knowledge of HTML and CSS
- Code editor (e.g., VS Code)
- Web browser for testing

### Files Needed

1. `index.html` - The main HTML file for your webpage.
2. `style.css` - The CSS file to style your webpage.

### Step-by-Step Instructions

#### Step 1: Create the Project Structure

1. Create a new folder for your project.
2. Inside the folder, create two files: `index.html` and `style.css`.

#### Step 2: Set Up the HTML

##### Add the HTML Boilerplate

Open `index.html` and add the following boilerplate code:

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

##### Add the Navigation Bar

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

##### Add the Main Section

In `index.html`, below the navigation bar code, add the following code for the main section:

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

##### Add the Footer

In `index.html`, below the main section code, add the following code for the footer:

```html
<footer>
    <p>&copy; 2024 Your Website</p>
</footer>
```

#### Step 3: Style with CSS

Open `style.css` and add the following styles:

##### Add Basic Reset and Body Styles

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
```

##### Style the Header and Navigation Bar

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

##### Style the Hero Section

```css
.hero {
    text-align: center;
    padding: 2em 0;
    background: url('https://www.pexels.com/photo/beautiful-view-of-sea-847393/') no-repeat center center/cover;
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex: 1;
}
```

##### Style the Content Section

```css
.content {
    display: flex;
    justify-content: space-around;
    padding: 2em;
    flex-wrap: wrap;
    flex: 1;
}

.content .box {
    background-color: #f4f4f4;
    padding: 1em;
    width: 30%;
    text-align: center;
    border-radius: 5px;
    margin-bottom: 1em;
    flex: 1 1 200px; /* Makes the boxes responsive */
}
```

##### Style the Footer

```css
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}
```

### Step 4: Add Images

Download the images you want to use from Pexels and place them in your project folder. Update the URL in the `hero` section's `background` property in `style.css` with the correct path to your image.

### Step 5: Test Your Website

Open `index.html` in your web browser and check if the website is responsive by resizing the browser window.

## Conclusion

You have successfully created a responsive website using Flexbox. You can further enhance the website by adding more content and styles. Keep practicing to master Flexbox!
