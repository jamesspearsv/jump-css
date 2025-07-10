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
    - [Forms](#forms)
    - [Components](#components)
    - [Customization](#customization)
    - [Accessibility Best Practices](#accessibility-best-practices)

## Project Overview

**Objective:**  
Jump.css is a lightweight CSS framework build on semantic HTML that helps you jump start your apps and websites in style. Jump.css promotes accessibility, maintainability, and modern web standards to create visually appealing and accessible layouts using clean, semantic markup.

> [!NOTE] Jump.css is in active development and subject to breaking changes without notice. Try Pico CSS or Simple.css for a more robust and stable CSS framework.

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
  - [x] Navigation
  - [ ] Containers
  - [ ] Links
  - [ ] Tables
- Forms
  - [ ] Inputs, Labels, Fieldsets
  - [ ] Form Layout & Spacing
  - [ ] Form Validation
- Components
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

### Forms

### Components

### Customization

### Accessibility Best Practices
