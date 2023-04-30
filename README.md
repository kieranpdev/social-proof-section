# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Create a social proof section:

- Mobile version for smaller displays witha column layout
- DEsktop version for larger displays has row based layout and subtle positioning changes for elements

### Screenshot

![](./images/social-proof-screenshot.png)

### Links

- Solution URL: [URL to solution files](https://github.com/kieranpdev/social-proof-section)
- Live Site URL: [URL to live site](https://kieranpdev.github.io/social-proof-section/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

The SVG star rating image was provided however I wanted to add this in a way which did not affect the accessibility of the site. I added the stars using the CSS ::before selector

```
.ratings p::before {
    content: 
    url(../images/icon-star.svg) " " 
    url(../images/icon-star.svg) " " 
    url(../images/icon-star.svg) " " 
    url(../images/icon-star.svg) " " 
    url(../images/icon-star.svg);
    display: block;
}
```

There was also some subtle alignment styling on the ratings and reviews - the nth-child selector allowed me to style the elements using flexbox. I could have achieved something similar with margins instead

```
.ratings > p:nth-child(1) {
        align-self: flex-start;
    }

    .ratings > p:nth-child(2) {
        align-self: center;
    }

    .ratings > p:nth-child(3) {
        align-self: flex-end;
    }
```

## Author

- Frontend Mentor - [@kieranpdev](https://www.frontendmentor.io/profile/kieranpdev)

## Acknowledgments

As always CSS Tricks was invaluable for looking up techniques [css-tricks.com/](https://css-tricks.com/)

