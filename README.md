# Watch Effective Size Calculator

A tool to calculate how a watch will look on a wrist of a given size, accounting for wrist circumference, case type, and integrated bracelets.

## Overview

Watch sizing is subjective and depends on both the watch's stated diameter and the wearer's wrist circumference. This calculator provides a normalized "effective visual size" to help compare watches across different wrist sizes.

## Key Assumptions

- **6.75 inches (171 mm)** is the baseline wrist circumference for calibration
- At baseline, a **40mm watch** serves as the reference point
- For every **0.25" (6.35mm) below** baseline, add **1mm** to perceived sizing
- For every **0.25" (6.35mm) above** baseline, subtract **1mm** from perceived sizing

## Features

### Inputs
- **Wrist Size** - Enter circumference in inches or millimeters
- **Watch Diameter** - The stated diameter of the watch case in mm
- **Case Type** - Round, Square (+1.5mm), or Tonneau (+1.5mm)
  - Square and Tonneau cases appear larger due to their geometry
- **Integrated Bracelet** - Toggle whether the watch has an integrated bracelet
  - If yes and Round case: adds 1mm to perceived size
  - If yes and Square/Tonneau case: adds 0.5mm to perceived size

### Outputs
- **Effective Visual Size** - The perceived diameter of the watch on a standard 6.75" wrist
- **Maximum Lug-to-Lug** - Theoretical maximum lug-to-lug width that would fit comfortably on your wrist
  - Calculated as: `(circumference ÷ π) − 2mm` (comfort allowance)

### URL Sharing
All parameters are encoded in the URL, allowing you to share specific configurations with others.

## Usage

1. Enter your wrist circumference
2. Choose your preferred unit (inches or millimeters)
3. Enter the watch diameter
4. Select the case type
5. Toggle integrated bracelet if applicable
6. View the calculated effective size and maximum lug-to-lug
7. Share the URL with others to compare watches

## Hosting

### Local
Simply open `index.html` in a web browser.

### Public
- **GitHub Pages** - View at [heffergm.github.io/watch-sizing](https://heffergm.github.io/watch-sizing/index.html?wrist=171&unit=mm&size=40&case=round&integrated=no)

## File Structure

```
watch-sizing/
├── index.html      # Complete calculator (HTML + CSS + JavaScript)
└── README.md       # This file
```

## Browser Compatibility

Works in all modern browsers with ES6 support (Chrome, Firefox, Safari, Edge).
