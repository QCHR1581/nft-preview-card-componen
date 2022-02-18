## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)



## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

Screenshot of my solution: ![](images/screenshot-solution.jpg)

### Links

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process
  
  1. Implement the necessary elements: image, text and rectangle. - This was done in HTML and CSS. The correct images was linked in HTMl and the rectangle was created in CSS. Which was also linked to the HTML file.

  2. Step: Arrange every element so that they look like in the solution. - This was done in CSS. I used Flexbox to do this. 

  3. Edit the look of the elements so that they look like in the solution - This was done in CSS. The image and the rectangle had to have rounded corners. Furthermore I was necessary to have hover animations for following elements: the cube image (white eye and cyan background), the headline (cyan color) and the creators name (cyan color). 


### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

I learned how to use hover for displaying an other image when you move the cursor over an existing one and how you can edit the properties of it. 

Necesary for that was to create a parent class. 
Within this one were the the child classes for the different images:

```html
<!-- Cube image -->
        <div class="hover-images">
          <div class="cube"></div>
          <div class="eye"></div>
        </div>
```

The edited the properties of those classes: 

```css
/* Parent class */
.hover-images {
    position: relative;
    cursor: pointer;
    width: 100%;
    max-width: 18.75rem;
    height: auto;
    border-radius: 5px;
    overflow: hidden;
}
/* Child class - eye */
.eye {
    position: absolute;
    left: 9%;
    top: 8%;
    right: 70%;
    width: 18rem;
    height: 18rem;
    background-image: none;
}
/* Child class - cube */
.cube {
    background-image: url("image-equilibrium.jpg");
    background-repeat: no-repeat;
    background-size: cover; 
    border-radius: 1%;
    margin: 9%;
    height: 18rem;
    width: 18rem;
}
/* Pseudo class - eye(hover) */
.eye:hover {
    background-image: url("../nft-preview-card-component-main/images/icon-view.svg");
    background-color:hsl(178, 100%, 50%);
    background-repeat: no-repeat;
    background-position: 50% 50%;
    background-size: 20% 20%;
    opacity: 0.6;
    transition: background-color ease-in-out 0.3s;
}
```

### Useful resources

- [Stackoverflow](https://www.positioniseverything.net/css-background-image-not-working) - The answers gave different ideas how I can make the hover effect I want

- [Positioniseverything](https://www.positioniseverything.net/css-background-image-not-working) - This helped me when I had problems with background-image: ulr("").

- [Youtube](https://www.youtube.com/watch?v=6oHZOag0MH0) - This also helped me when I had problems with background-image: ulr("").

- [TutorialRepublic](https://www.tutorialrepublic.com/faq/how-to-change-image-on-hover-with-css.php#:~:text=Answer%3A%20Use%20the%20CSS%20background,change%20the%20image%20on%20mouseover.) - This showed me exactly how I wanted to have the hover animation in practice

