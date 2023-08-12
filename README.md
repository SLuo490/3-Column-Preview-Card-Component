# Frontend Mentor - 3-column preview card component solution

## Table of contents

- [Frontend Mentor - 3-column preview card component solution](#frontend-mentor---3-column-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [Documentation](#documentation)
    - [HTML](#html)
    - [Styling](#styling)
      - [Mobile](#mobile)
      - [Website](#website)
        - [Layout](#layout)
        - [Components](#components)
        - [Standard Stylings](#standard-stylings)
  - [Next Step](#next-step)
    - [Built with](#built-with)
  - [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## Documentation

### HTML

```html
<body>
  <main>
    <section class="sedan">
      <img src="/images/icon-sedans.svg" alt="sedan" />
      <h1>Sedans</h1>
      <p>
        Choose a sedan for its affordability and excellent fuel economy. Ideal
        for cruising in the city or on your next road trip.
      </p>
      <button>Learn More</button>
    </section>
    <section class="suv">
      <img src="/images/icon-suvs.svg" alt="suv" />
      <h1>SUVs</h1>
      <p>
        Take an SUV for its spacious interior, power, and versatility. Perfect
        for your next family vacation and off-road adventures.
      </p>
      <button>Learn More</button>
    </section>
    <section class="luxury">
      <img src="/images/icon-luxury.svg" alt="luxury" />
      <h1>Luxury</h1>
      <p>
        Cruise in the best car brands without the bloated prices. Enjoy the
        enhanced comfort of a luxury rental and arrive in style.
      </p>
      <button>Learn More</button>
    </section>
  </main>
</body>
```

For this project, I structured the project into three sections (columns). In each section, I added image, then the heading then the description of the car. In each section, I added a button to the `Learn More`.

### Styling

#### Mobile

```css
@media screen and (max-width: 375px) {
  main {
    flex-direction: column;
  }

  section {
    height: 442px;
    width: 327px;
  }

  .sedan {
    border-radius: 8px 8px 0 0;
  }

  .luxury {
    border-radius: 0 0 8px 8px;
  }

  .description {
    margin-bottom: 25px;
  }
}
```

I started developing the front end by doing [mobile first design](https://www.browserstack.com/guide/how-to-implement-mobile-first-design). I determined the mobile screen size using figma and then made the three columns centered on the screen vertically using `flex-direction`.

I then made the section's width and height to `327px` and `442px` according to the figma.

```css
section {
  height: 442px;
  width: 327px;
}
```

I then updated the border-radius to the columns, and the `margin-bottom` for description as the bottom would overlap.

```css
.sedan {
  border-radius: 8px 8px 0 0;
}

.luxury {
  border-radius: 0 0 8px 8px;
}

.description {
  margin-bottom: 25px;
}
```

#### Website

##### Layout

Starting out, for the website, I make the height of the body `100vh` and change its color to white. I then made the content center on the middle of the page using [flex box](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

```css
body {
  height: 100vh;
  color: var(--n-transparent-white);

  /* Center the 3-columns on the middle of the page */
  display: flex;
  justify-content: center;
  align-items: center;
}
```

Following that, I gave the `main` in HTML a `display: flex` too, so the content will become a column instead of row.

```css
main {
  /* Make the 3-columns a "column" */
  display: flex;
}
```

Using the figma, I made the section a width of `307px` and height of `500px`.

```css
section {
  width: 307px;
  height: 500px;
}
```

##### Components

I made a text component where I can use to style both the description and the text of the button so I don't repeat myself.

```css
.text {
  font-family: Lexend Deca, sans-serif;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: 25px;
}
```

##### Standard Stylings

The following steps were straight forward as I just followed the figma design and added the `color` for the background, the `border-radius` for the container, and paddings for each of the three columns.

```css
.sedan {
  background-color: var(--pm-bright-orange);
  border-radius: 8px 0 0 8px;
}

.sedan button {
  color: var(--pm-bright-orange);
}

.suv {
  background-color: var(--pm-dark-cyan);
}

.suv button {
  color: var(--pm-dark-cyan);
}

.luxury {
  background-color: var(--pm-very-dark-cyan);
  border-radius: 0 8px 8px 0;
}

.luxury button {
  color: var(--pm-very-dark-cyan);
}

/* Paddings */
.sedan,
.suv,
.luxury {
  padding: 48px 47.5px 0 48.5px;
}

.option {
  padding: 35px 0 25px 0;

  font-family: 'Big Shoulders Display', sans-serif;
  font-size: 40px;
  font-weight: 700;
  text-transform: uppercase;
  color: var(--n-very-light-gray);
}

.description {
  margin-bottom: 83px;
  color: var(--n-transparent-white);
  opacity: 0.75;
}
```

Similarly, I followed the figma design to add the styling for the buttons.

```css
.btn {
  width: 146px;
  height: 48px;
  border-radius: 25px;
  background-color: var(--n-very-light-gray);
  border: none;
  cursor: pointer;
}

.btn:hover {
  background-color: transparent;
  border: 2px solid var(--n-transparent-white);
  color: var(--n-transparent-white);
}
```

## Next Step

The next step would be to improve the readability of the code, and removing code so I don't repeat myself. One method that I could use is similar to what I have done in making a class `.text` and adding the class to the HTML so the classes would have the same styling.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
