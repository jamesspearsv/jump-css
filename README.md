# Jump.css

- [Jump.css](#jumpcss)
  - [Project Overview](#project-overview)
  - [Goals](#goals)
  - [Core Features](#core-features)
  - [Roadmap](#roadmap)
  - [Technical Requirements](#technical-requirements)
  - [Documentation](#documentation)
    - [Colors](#colors)
    - [Semantic Containers](#semantic-containers)
    - [Utility Containers](#utility-containers)
    - [Clickables](#clickables)
    - [Forms](#forms)
    - [Components](#components)
      - [Navigation](#navigation)
      - [Modals](#modals)
      - [Tables](#tables)
      - [Cards](#cards)
    - [Accessibility Best Practices](#accessibility-best-practices)

## Project Overview

**Objective:**  
Jump.css is a lightweight CSS framework build on semantic HTML that helps you jump start your apps and websites in style. Jump.css promotes accessibility, maintainability, and modern web standards to create visually appealing and accessible layouts using clean, semantic markup.

> [!NOTE]
> Jump.css is in active development and subject to breaking changes without notice. Try Pico CSS or Simple.css for a more robust and stable CSS framework.

I started Jump.css to build a set of base CSS rules and styles for my hobby and side projects. Jump.css is tailored to my personal tastes and preferences but you are welcome to make it your own.

## Goals

- **Style semantic HTML elements out-of-the-box** for a polished, accessible UI.
- **Minimize or eliminate the need for classes**—only provide a handful of essential utility classes (e.g., for accessibility).
- **Ensure accessibility and responsive design** without class dependence.
- **Enable easy customization** through CSS variables and element/attribute selectors.

## Core Features

- **Element-Based Styling:**  
  Comprehensive default styles for all major semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<mark>`, `<time>`, etc.).
- **[WIP] Minimal Utility Classes:**  
  Only essential classes for accessibility (e.g., `.visually-hidden`, `.sr-only`, `.skip-link`).
- **[WIP] Attribute Selectors:**  
  Use selectors like `[aria-current="page"]`, `[disabled]`, and `[role]` for interactive and accessible states.
- **[WIP] Responsive Design:**  
  Mobile-first breakpoints and fluid layouts using element and attribute selectors.
- **Customizability:**  
  Theming and spacing via CSS variables.
- **[WIP] Accessibility:**  
  Built-in focus indicators, color contrast, and ARIA support.

## Roadmap

- Design System
  - [x] Color scheme
  - [x] Typography
  - [x] Spacing and sizing
  - [x] Light/Dark theme
  - [ ] Page layouts
- Element bases styles
  - [x] Buttons
  - [x] Containers
  - [ ] Links
- Forms
  - [ ] Inputs, Labels, Fieldsets
  - [ ] Form Layout & Spacing
  - [ ] Form Validation
- Components
  - [x] Tables
  - [x] Navigation
  - [x] Modals
  - [x] Cards
  - [ ] Groups
  - [ ] Drop Downs
- Documentation
  - [ ] Components
  - [ ] Design System
  - [ ] Customization

## Technical Requirements

Jump.css is minimal and performant and depends on the following technical requirements

| Requirement            | Description                                                   |
| ---------------------- | ------------------------------------------------------------- |
| **Element Selectors**  | Style semantic HTML elements directly, not through classes.   |
| **Minimal Classes**    | Provide only a handful of utility classes for accessibility.  |
| **Attribute Styling**  | Use attribute selectors for stateful and interactive styling. |
| **Custom Properties**  | Enable easy overrides and theming with CSS variables.         |
| **No Framework Bloat** | Avoid unnecessary CSS and class-based utilities.              |

## Documentation

### Colors

Jump.css uses a sensible color system that is simple, accessible, and customizable. The color system is build on four color properties that can be overwritten for customization.

1. `--clr-main`: Main color that is used for backgrounds, text, borders, etc.
2. `--clr-accent`: Accent color that is used for emphasis, clickables, and components
3. `--clr-danger`: Secondary accent color used to convey feedback for dangerous actions
4. `--clr-success`: Secondary accent color used to convey feedback for successful actions

A range of shades are available based on `--clr-main` and `--clr-accent`.

```css
/* lighter variants */
--clr-main-100: color-mix(in oklch, var(--clr-main), #ffffff 90%);
--clr-main-200: color-mix(in oklch, var(--clr-main), #ffffff 75%);
--clr-main-300: color-mix(in oklch, var(--clr-main), #ffffff 60%);
--clr-main-400: color-mix(in oklch, var(--clr-main), #ffffff 45%);

--clr-main-500: var(--clr-main); /* base */

/* darker variants */
--clr-main-600: color-mix(in oklch, var(--clr-main), #000000 20%);
--clr-main-700: color-mix(in oklch, var(--clr-main), #000000 35%);
--clr-main-800: color-mix(in oklch, var(--clr-main), #000000 50%);
--clr-main-900: color-mix(in oklch, var(--clr-main), #000000 65%);
```

Each variant can be used directly and customized by providing a custom value. View the source code for a complete list of derived color properties.

Sensible light and dark themes are available and applied using `prefers-color-scheme` media queries.

### Semantic Containers

When used as direct children of `<body />`, `<header />`, `<main />`, and `<footer />` function as landmark containers to help structure parts of the page.

```css
body > header {
  ...;
}
body > main {
  ...;
}
body > footer {
  ...;
}
```

When used as containers, `<header />` and `<footer />` are both `100dvw` wide by default.

As a container, `<main />` is set to the `--content-width` property and centered using `margin: auto;` by default.

### Utility Containers

There are two utility containers: `<section />`, and `<aside />`

`<section />` by default apply only `margin-block` for consistent spacing between page sections but does not provide any alignment on its own. `<section />` containers with 2 or more `<article />` children will automatically apply `display: flex;` with a uniform gap and flex wrapping.

`<aside />` by provide vertical stacking using `display: flex;` with a uniform gap between children.

Wrapping `<aside />` in `<section />` will apply consistent margins outside the element while also vertically stacking any inner elements.

### Clickables

Clickable include buttons and links

Buttons by default are styles with rounded corners, padding, and accent background color. Use `type=reset"` attribute to add a danger style button.

```html
<button>Button</button> <button type="reset">Reset Button</button>
```

Links by default use the accent color for the color property and include text underlining during hover states.

### Forms

<!-- TODO: Add form documentation -->

### Components

#### Navigation

Navigation components can be created using`<nav>`, `<ul>`, `<li>`, and `<a>` elements. `<nav>` uses flexbox and `justify-content: space-between` by default to easily define a navigation layout (ex. left aligned logo, center aligned, etc.)

Navigation with left aligned wordmark

```html
<nav>
  <ul>
    <h1>Starter.css</h1>
  </ul>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

Navigation with a center aligned wordmark

```html
<nav>
  <ul>
    <li><a href="#" aria-current="page">Home</a></li>
    <li><a href="#">About</a></li>
  </ul>
  <ul>
    <h1>Starter.css</h1>
  </ul>
  <ul>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

Navigation links include default padding and simple hover animation

#### Modals

Create a modal component by wrapping an `<article>` in a `<dialog>` element and include any content as a child of the `<article>` element.

Add a `<button type="reset">` after any modal content to automatically include a closing button.

```html
<dialog>
  <article>
    <button type="reset" />
  </article>
</dialog>
```

Jump.css does not include any JavaScript so a script to handle opening and closing a modal is required to enable interactivity.

#### Tables

Tables automatically include a styled header row, rounded corners, responsive width, and consistent cell spacing.

Each table component should include a `<thead>` and a `<tbody>`. Include at least one `<tr>` with relevant `<th>` elements inside the table head.

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>30</td>
      <td>New York</td>
    </tr>
    <tr>
      <td>Jane Smith</td>
      <td>25</td>
      <td>Los Angeles</td>
    </tr>
    <tr>
      <td>Mike Johnson</td>
      <td>35</td>
      <td>Chicago</td>
    </tr>
  </tbody>
</table>
```

#### Cards

Add cards to your HTML by wrapping any elements or content with `<article />` elements. Any elements or content inside is centered using flexbox.

```html
<article>[put any content here]</article>
```

### Accessibility Best Practices
