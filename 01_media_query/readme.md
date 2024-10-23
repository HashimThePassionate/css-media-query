# CSS Grid and Media Queries 🖥️📱

Welcome! In this guide, we'll walk through building a responsive grid system using CSS Grid and media queries. Don't worry if you're new to these concepts—we'll explain everything from the ground up. Let's get started! 🚀

## Table of Contents 📖

- [CSS Grid and Media Queries 🖥️📱](#css-grid-and-media-queries-️)
  - [Table of Contents 📖](#table-of-contents-)
  - [1. Introduction](#1-introduction)
  - [2. What is CSS Grid?](#2-what-is-css-grid)
  - [3. What are Media Queries?](#3-what-are-media-queries)
  - [4. Setting Up Your Project](#4-setting-up-your-project)
  - [5. Creating the HTML Structure](#5-creating-the-html-structure)
  - [6. Styling with CSS](#6-styling-with-css)
    - [Basic Grid Setup](#basic-grid-setup)
    - [Making it Responsive](#making-it-responsive)
  - [7. Final Code](#7-final-code)
  - [8. Conclusion](#8-conclusion)

---

## 1. Introduction

Responsive design ensures that your website looks great on all devices, from large desktop monitors to small mobile phones. By using **CSS Grid** and **media queries**, we can create a flexible grid system that adapts to different screen sizes.

## 2. What is CSS Grid?

**CSS Grid** is a powerful layout system in CSS that allows you to create complex, responsive web layouts more easily and consistently across browsers. It works by defining rows and columns, and placing items into these grid areas.

## 3. What are Media Queries?

**Media queries** are a CSS feature that lets you apply styles based on the result of one or more media queries, such as the width or height of the viewport. They are essential for creating responsive designs that adapt to different screen sizes.

## 4. Setting Up Your Project

You'll need two files for this project:

- `index.html` (the HTML structure)
- `styles.css` (the CSS styling)

Make sure both files are in the same directory.

## 5. Creating the HTML Structure

Open `index.html` and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Grid System</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>My Responsive Grid System</h1>
  <div class="grid-container">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
    <div class="grid-item">Item 4</div>
    <div class="grid-item">Item 5</div>
    <div class="grid-item">Item 6</div>
  </div>
</body>
</html>
```

**Explanation:**

- We have a `<div>` with the class `grid-container` that will serve as our grid.
- Inside it, there are multiple `<div>` elements with the class `grid-item` that represent the grid cells.

## 6. Styling with CSS

Open `styles.css` and start by resetting some default styles:

```css
/* styles.css */

/* Reset default margins and paddings */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

### Basic Grid Setup

Now, let's set up the basic grid:

```css
body {
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  margin: 20px 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  padding: 0 20px;
}

.grid-item {
  background-color: #3498db;
  color: #fff;
  padding: 40px 0;
  text-align: center;
  border-radius: 8px;
}
```

**Explanation:**

- `display: grid;` turns the `.grid-container` into a grid layout.
- `grid-template-columns: repeat(3, 1fr);` creates three equal-width columns.
- `gap: 15px;` adds space between grid items.
- `.grid-item` styles each grid cell with a background color, text color, padding, and rounded corners.

### Making it Responsive

Now, let's add media queries to make the grid responsive:

```css
/* When the screen is 768px or smaller, display two columns */
@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* When the screen is 480px or smaller, display one column */
@media (max-width: 480px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
```

**Explanation:**

- The first media query applies when the screen width is **768 pixels or less**, changing the grid to two columns.
- The second media query applies when the screen width is **480 pixels or less**, changing the grid to a single column.

## 7. Final Code

**`index.html`:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Grid System</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>My Responsive Grid System</h1>
  <div class="grid-container">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
    <div class="grid-item">Item 4</div>
    <div class="grid-item">Item 5</div>
    <div class="grid-item">Item 6</div>
  </div>
</body>
</html>
```

**`styles.css`:**

```css
/* Reset default margins and paddings */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  margin: 20px 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  padding: 0 20px;
}

.grid-item {
  background-color: #3498db;
  color: #fff;
  padding: 40px 0;
  text-align: center;
  border-radius: 8px;
}

/* Responsive Design */

/* When the screen is 768px or smaller */
@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* When the screen is 480px or smaller */
@media (max-width: 480px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
```

## 8. Conclusion

Great job! 🎉 You've successfully created a responsive grid system using CSS Grid and media queries. You can now adjust the number of items, change styles, or even add more breakpoints to further customize the responsiveness.
