# Rethinking Colors in Design Systems: A CSS Approach to Idiomatic Design

## Overview

This project is a demo used in the talk "Rethinking Colors in Design Systems: A CSS Approach to Idiomatic Design" by Armagan Amcalar. The talk presents an innovative perspective on color management in design systems, aiming to simplify and enhance the developer experience.

## Slides

You can view the slides for the talk [here](https://slides.com/armaganamcalar/rethinking-color).

## Philosophy of Building Palettes and Using Colors

### Centralized Color Definitions

Colors are defined centrally in CSS variables (`:root` in `colors.scss`). This allows for easy updates and consistent usage across the project.

### Mixing Functions

Functions like `mixWhite` and `mixBlack` are used to create tints and shades of a base color. These functions take a weight parameter to determine the proportion of the base color in the mix. This approach ensures a consistent and scalable way to generate color variations.

### CSS Classes for Colors

CSS classes are defined for each color (e.g., `.turq`, `.blue`, `.red`). These classes set the `--color` variable to the corresponding color value. This makes it easy to apply colors to elements by simply adding the appropriate class.

### Defining Color-Related Rules in `styles.scss`

All color-related rules are defined in `styles.scss`. This file uses the centralized color definitions and mixing functions to apply tints and shades. The idea is to define only the tint in `styles.scss`, as the base color is applied via HTML classes.

### Consistent Design System

By using these centralized definitions and mixins, the design system remains consistent. Developers can easily apply and modify colors without worrying about inconsistencies.

## Getting Started

### Installation

1. Clone the repository:
   ```sh
   git clone git@github.com:dashersw/colors.git
   cd colors
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

### Running the Project

To start the development server, run:
```sh
npm run dev
```

This will start the Parcel development server and open the project in your default web browser.

## Usage

- **Main Page**: The main page (`index.html`) displays a login card that can be styled in different colors with a simple class change.
- **Palettes Page**: The palettes page (`palettes.html`) displays the color palettes implemented in CSS in a grid format, showing both an extended palette and a reduced palette.

## License

MIT License

Copyright (c) 2024 Armagan Amcalar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
