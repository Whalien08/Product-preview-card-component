# Frontend Mentor - Product preview card component solution

This is a completed solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:
- View the optimal layout depending on their device's screen size (Desktop vs. Mobile).
- See hover and focus states for interactive elements (like the "Add to Cart" button changing shades).

### Screenshot

<img width="2879" height="1472" alt="Screenshot 2026-06-17 231250" src="https://github.com/user-attachments/assets/f8907b1f-77a4-4221-b4aa-8eb7edb205a9" />


### Links

- Solution URL: [GitHub repository link here]([https://your-solution-url.com](https://github.com/Whalien08/Product-preview-card-component.git))
- Live Site URL: []([https://whalien08.github.io/Product-preview-card-component/])

## My process

### Built with

- Semantic HTML5 markup
- CSS Flexbox (for structured card layouts and vertical page centering)
- Modern CSS Logical Properties (`margin-inline-start`)
- Responsive Web Design (`@media` queries)
- Google Fonts Integration (`Montserrat` & `Fraunces`)

### What I learned

This project provided fantastic practice for dealing with structural layout adjustments and handling responsive media natively in HTML. 

Key takeaways from this build:

1. **HTML `<picture>` Element over CSS Hacks:**
   Instead of using multiple image elements with `display: none` or relying on bulky CSS background images to change layouts, I learned how to cleanly serve different optimized images to mobile and desktop displays using native HTML.
   ```html
   <picture>
     <source media="(max-width: 600px)" srcset="images/image-product-mobile.jpg">
     <img src="images/image-product-desktop.jpg" alt="Gabrielle Essence perfume bottle surrounded by green leaves">
   </picture>

2. **Letting Flexbox Handle Layout Flow Instead of Absolute Positioning:**
    I originally relied on position: absolute; for placement, but realized it tears elements out of the document flow and breaks responsiveness. Switching to a clean Flexbox layout allowed columns to seamlessly transition into rows on smaller screens.
    ```CSS

    .card {
        display: flex;
        flex-direction: row; /* Desktop alignment */
    }

    @media (max-width: 600px) {
        .card {
            flex-direction: column; /* Mobile stack alignment */
        }
    }

3. **CSS Logical Properties:**
    I explored using margin-inline-start to position the text section safely based on text-direction workflow alignment, keeping layouts modern and localization-ready.

**Continued development**

In future projects, I want to keep refining:

    Mobile-First Workflows: Writing mobile styles first and scaling up to desktop using min-width queries rather than using max-width desktop-first overrides.

    Accessibility (a11y): Ensuring tags like <del> are styled cleanly for semantic price comparisons so screen readers scan them accurately.

