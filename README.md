# Frontend Mentor - Grid landing page solution

This is a solution to the [Grid landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/grid-landing-page). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

**Grid Landing Page** is a front-end showcase highlighting modern CSS layout techniques—specifically **CSS Grid**, **Flexbox**, and **CSS Custom Properties (Variables)**. It provides a clean, fast-loading, fully responsive web interface designed to scale seamlessly across all screen dimensions, from high-resolution desktop monitors to smartphones.

### The challenge

Users should be able to:

- View the optimal layout for the page depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- Open and close the navigation menu at any screen size (optional JavaScript)

### Screenshot

![](preview.jpg)

### Links

- solution URL: [GitHub Repository](https://github.com/MoMo97X/Grid-Landing-Page)
- Live Site URL: [GitHub Pages](https://momo97x.github.io/Grid-Landing-Page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Modern fluid sizing (`clamp()`, `min()`)
- Vinella java script

### What I learned

#### 1. Fluid Layouts with Responsive CSS Grid

Instead of relying heavily on rigid media queries, I leveraged CSS Grid with repeat() and minmax() to allow cards to automatically reflow across viewport sizes:

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  align-items: stretch;
}
```

#### 2. Structural Composition using Named Grid Areas

For desktop viewports, using explicit grid-template-areas allowed for clear spatial organization without polluting HTML markup with unnecessary wrapper divs:

```css
@media (min-width: 1024px) {
  .landing-layout {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-areas:
      "hero hero feature-a feature-b"
      "hero hero feature-c feature-d"
      "footer-a footer-b footer-c footer-c";
  }
}
```

#### 3. Writing JavaScript and manipulate the DOM

Using a script tag to integrate js into html file, intruducing addEventlistner function, variables.

```js
const openButton = document.querySelector(".open-button");
const closeButton = document.querySelector(".close-button");
const menu = document.querySelector(".side-menu");

openButton.addEventListener("click", () => {
  openButton.style.display = "none";
  closeButton.style.display = "block";

  menu.classList.add("active");
  document.querySelector("main").classList.add("layout-cover");
  document.querySelector(".stats-section").classList.add("layout-cover");
});
```

### Continued development

- Master modern layout tools like CSS subgrid for nested alignment across card elements.

- Deepen keyboard navigation testing and screen-reader accessibility auditing (WCAG compliance).

- Continue refining AI-assisted development workflows for rapid UI prototyping and refactoring

### Useful resources

- [A Complate Guide to CSS Grid (CSS-Tricks)](https://css-tricks.com/snippets/css/a-guide-to-grid/) - Comprehensive guide for understanding explicit/implicit tracks and template areas.

- [MDN Web Docs: CSS grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout) - Standard reference for modern CSS layout syntax and boundary rules.

### AI Collaboration

- Layout Optimization: Analyzed grid tracks and breakpoint transitions to eliminate unnecessary media queries.

- Git Workflow & Best Practices: Configured project commit standards, .gitignore rules, and automated documentation generation.

- Code Refactoring: Assisted in cleaning up repetitive utility classes and enforcing custom CSS properties across the stylesheet.

## Author

- Website - [@MoMo97X](https://www.your-site.com)
- Frontend Mentor - [@MuhammedArrujbani](https://www.frontendmentor.io/profile/yourusername)

## Acknowledgments

Thanks to the Frontend Mentor community for providing realistic design specs and challenges that mirror real-world front-end engineering projects.
