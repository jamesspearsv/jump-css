# Jump.css

- [Jump.css](#jumpcss)
  - [Project Overview](#project-overview)
  - [Goals](#goals)
  - [Core Features](#core-features)
  - [Roadmap](#roadmap)
  - [Technical Requirements](#technical-requirements)
  - [\[WIP\] Documentation](#wip-documentation)
    - [Design System](#design-system)
    - [Layouts and Containers](#layouts-and-containers)
    - [Buttons \& Links](#buttons--links)
    - [Forms](#forms)
    - [Components](#components)
      - [Navigation](#navigation)
      - [Modals](#modals)
      - [Tables](#tables)
    - [Customization](#customization)
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
  - [ ] Light/Dark theme
  - [ ] Layout
- Element bases styles
  - [x] Buttons
  - [ ] Containers
  - [ ] Links
- Forms
  - [ ] Inputs, Labels, Fieldsets
  - [ ] Form Layout & Spacing
  - [ ] Form Validation
- Components
  - [x] Tables
  - [x] Navigation
  - [x] Modals
  - [ ] Cards
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

## [WIP] Documentation

### Design System

### Layouts and Containers

### Buttons & Links

Buttons by default are styles with rounded corners, padding, and accent background color. Use `type=reset"` attribute to add a danger style button.

```html
<button>Button</button> <button type="reset">Reset Button</button>
```

Links by default use the accent color for the color property and include text underlining during hover states.

### Forms

<!-- TODO: Add form documentation -->

### Components

#### Navigation

Navigation components can be created using`<nav>`, `<ul>`, `<li>`, and `<a>` elements. `<nav>` elements use flexbox and `justify-content: space-between` by default to easily define a navigation layout (ex. left aligned loge, center aligned, etc.)

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

### Customization

Jump.css is easy to customize by overriding a few CSS properties. The complete list of CSS properties available to customize is below.

```css
:root {
  /** Color Properties */
  --clr-dark-500: #343a40;
  --clr-dark-400: #868e96;
  --clr-light-500: #f8f9fa;
  --clr-light-600: #f1f3f5;
  --clr-accent-500: #7950f2;
  --clr-accent-1: #9775fa;
  --clr-danger: #f03e3e;
  --clr-success: #2f9e44;

  /** Font Properties  */
  --weight-normal: 400;
  --weight-bold: 700;
  --weight-light: 200;

  /** Size & Spacing Properties  */
  --size-0: 0.75rem;
  --size-1: 1rem;
  --size-2: 1.25rem;

  --spacing-00: 0.5rem;
  --spacing-0: 0.75rem;
  --spacing-1: 1rem;
  --spacing-2: 1.25rem;

  --content-width: min(80ch, 80%);

  /** Border & Outline Properties */
  --border-radius: 0.375rem;
  --border-style: solid 1px var(--clr-dark-500);
  --outline-style: solid 3px var(--clr-accent-1);
}
```

Customize the default styling of any element by providing a higher specificity CSS rule in an additional stylesheet.

### Accessibility Best Practices
