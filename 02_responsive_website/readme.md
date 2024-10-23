# Responsive Website Design using Grid, Flexbox, and Media Queries 🌐✨

## Table of Contents 📖

- [Responsive Website Design using Grid, Flexbox, and Media Queries 🌐✨](#responsive-website-design-using-grid-flexbox-and-media-queries-)
  - [Table of Contents 📖](#table-of-contents-)
  - [1. Introduction](#1-introduction)
  - [2. Website Layout Overview](#2-website-layout-overview)
    - [Desktop Layout 🖥️](#desktop-layout-️)
    - [Mobile Layout 📱](#mobile-layout-)
  - [3. Setting Up Your Project](#3-setting-up-your-project)
  - [4. HTML Structure](#4-html-structure)
  - [5. CSS Styling](#5-css-styling)
    - [General Styles](#general-styles)
    - [Header](#header)
    - [Hero Section](#hero-section)
    - [Content Sections](#content-sections)
    - [Footer](#footer)
    - [Responsive Design with Media Queries](#responsive-design-with-media-queries)
  - [6. Final Code](#6-final-code)
    - [`index.html`](#indexhtml)
    - [`styles.css`](#stylescss)
  - [7. Conclusion](#7-conclusion)

---

## 1. Introduction

We will build a responsive website layout that adapts to various screen sizes using **CSS Grid**, **Flexbox**, and **Media Queries**. This layout will have a header, navigation menu, hero section, content sections, and a footer.

## 2. Website Layout Overview

### Desktop Layout 🖥️

- **Header**: Logo and navigation menu.
- **Hero Section**: Large, bold banner.
- **Content Sections**: Three main sections arranged in a grid.
- **Footer**: Basic footer with links.

### Mobile Layout 📱

- **Header**: Logo with a collapsible menu.
- **Hero Section**: Stacked banner.
- **Content Sections**: Stacked content in a single column.
- **Footer**: Stacked items.

## 3. Setting Up Your Project

Create the following files:

- `index.html`
- `styles.css`

Make sure both files are in the same directory.

## 4. HTML Structure

**`index.html`:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Website with Grid & Flex</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header -->
  <header class="header">
    <div class="logo">MyWebsite</div>
    <nav class="nav">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <h1>Welcome to My Beautiful Website</h1>
    <p>Your journey to amazing starts here.</p>
  </section>

  <!-- Content Sections -->
  <div class="content">
    <section class="card">Feature 1</section>
    <section class="card">Feature 2</section>
    <section class="card">Feature 3</section>
  </div>

  <!-- Footer -->
  <footer class="footer">
    <p>&copy; 2024 MyWebsite. All rights reserved.</p>
  </footer>
</body>
</html>
```

**Explanation:**

- **`<header>`** contains the logo and navigation links.
- **`<section>`** elements represent the hero and content areas.
- **`<footer>`** is for copyright information.

## 5. CSS Styling

**`styles.css`:**

### General Styles

```css
/* Reset default margins and paddings */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: #f4f4f4;
}
```

### Header

```css
.header {
  background-color: #333;
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}

.logo {
  font-size: 1.5em;
  font-weight: bold;
}

.nav ul {
  display: flex;
  list-style: none;
}

.nav ul li {
  margin: 0 15px;
}

.nav ul li a {
  color: #fff;
  text-decoration: none;
}

.nav ul li a:hover {
  text-decoration: underline;
}
```

### Hero Section

```css
.hero {
  background: url('https://via.placeholder.com/1920x600') no-repeat center/cover;
  color: #fff;
  text-align: center;
  padding: 100px 20px;
}

.hero h1 {
  font-size: 3em;
}

.hero p {
  font-size: 1.2em;
}
```

### Content Sections

```css
.content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 40px 20px;
}

.card {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  text-align: center;
  padding: 20px;
}
```

### Footer

```css
.footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 15px 0;
}
```

### Responsive Design with Media Queries

```css
/* Media Queries */

/* Tablets: Adjust grid to two columns */
@media (max-width: 768px) {
  .content {
    grid-template-columns: repeat(2, 1fr);
  }

  .hero h1 {
    font-size: 2.5em;
  }
}

/* Mobile Devices: Stack layout */
@media (max-width: 480px) {
  .header {
    flex-direction: column;
  }

  .nav ul {
    flex-direction: column;
  }

  .content {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 60px 20px;
  }

  .hero h1 {
    font-size: 2em;
  }
}
```

## 6. Final Code

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Website with Grid & Flex</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="header">
    <div class="logo">MyWebsite</div>
    <nav class="nav">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h1>Welcome to My Beautiful Website</h1>
    <p>Your journey to amazing starts here.</p>
  </section>

  <div class="content">
    <section class="card">Feature 1</section>
    <section class="card">Feature 2</section>
    <section class="card">Feature 3</section>
  </div>

  <footer class="footer">
    <p>&copy; 2024 MyWebsite. All rights reserved.</p>
  </footer>
</body>
</html>
```

### `styles.css`

```css
/* General */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: #f4f4f4;
}

.header {
  background-color: #333;
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}

.logo {
  font-size: 1.5em;
  font-weight: bold;
}

.nav ul {
  display: flex;
  list-style: none;
}

.nav ul li {
  margin: 0 15px;
}

.nav ul li a {
  color: #fff;
  text-decoration: none;
}

.nav ul li a:hover {
  text-decoration: underline;
}

.hero {
  background: url('https://via.placeholder.com/1920x600') no-repeat center/cover;
  color: #fff;
  text-align: center;
  padding: 100px 20px;
}

.hero h1 {
  font-size: 3em;
}

.hero p {
  font-size: 1.2em;
}

.content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 40px 20px;
}

.card {
  background-color: #fff;
  border-radius: 10px;


  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  text-align: center;
  padding: 20px;
}

.footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 15px 0;
}

/* Media Queries */
@media (max-width: 768px) {
  .content {
    grid-template-columns: repeat(2, 1fr);
  }

  .hero h1 {
    font-size: 2.5em;
  }
}

@media (max-width: 480px) {
  .header {
    flex-direction: column;
  }

  .nav ul {
    flex-direction: column;
  }

  .content {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 60px 20px;
  }

  .hero h1 {
    font-size: 2em;
  }
}
```

## 7. Conclusion

With this project, you've learned how to use **CSS Grid**, **Flexbox**, and **Media Queries** to create a stunning, responsive website. Feel free to modify the layout, add more sections, or tweak styles. Happy coding! 🎨🖥️📱