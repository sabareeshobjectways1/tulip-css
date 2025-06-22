
---

```markdown
# Tulip CSS Library 🌷

Tulip is a modern, highly customizable, and production-ready CSS library built to provide a clean and consistent design foundation for your web projects. Inspired by the polished aesthetic and user-friendly principles of Google's design systems, Tulip offers a robust set of pre-styled components and utility classes, all managed through easily overrideable CSS variables for effortless theming.


## Installation

To start using Tulip, simply include the `tulip.css` file in the `<head>` section of your HTML document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Tulip Project</title>
  <!-- Link to your tulip.css file -->
  <link rel="stylesheet" href="path/to/your/tulip.css">
</head>
<body>
  <!-- Your content here -->
</body>
</html>
```

## Customization

Tulip is designed for flexibility. You can easily customize its appearance by overriding its CSS variables.

### CSS Variables

All core design tokens (colors, fonts, spacing, etc.) are exposed as CSS variables within the `:root` scope. These are defined at the top of the `tulip.css` file.

You can override these variables in your own custom CSS file, which should be linked *after* `tulip.css`.

### Theming

Here's an example of how to override variables to change the primary color and font family:

```css
/* your-custom-styles.css */

/* Ensure this file is linked after tulip.css */

:root {
  /* Override primary color to a vibrant blue */
  --tulip-color-primary: #007BFF;

  /* Override secondary color to a soft gray */
  --tulip-color-secondary: #6c757d;

  /* Change the base font family */
  --tulip-font-family-base: 'Open Sans', sans-serif;

  /* Change border-radius for a softer look */
  --tulip-border-radius-md: 0.4rem;
}
```

#### Available Variables

Refer to the `tulip.css` file for a complete list of all CSS variables, but here are some key categories:

*   **Colors:** `--tulip-color-*` (e.g., `--tulip-color-primary`, `--tulip-color-gray-500`)
*   **Typography:** `--tulip-font-family-*`, `--tulip-font-size-*`, `--tulip-font-weight-*`, `--tulip-line-height-*`
*   **Spacing:** `--tulip-spacing-*` (e.g., `--tulip-spacing-sm`, `--tulip-spacing-lg`)
*   **Borders:** `--tulip-border-width`, `--tulip-border-color`, `--tulip-border-radius-*`
*   **Shadows:** `--tulip-shadow-*`
*   **Transitions:** `--tulip-transition-base`
*   **Z-Index:** `--tulip-z-index-*`

## Components

### Buttons (`.tulip-btn`)

**Base Button:**

```html
<button class="tulip-btn">Default Button</button>
```

**Variants:**

```html
<button class="tulip-btn tulip-btn-primary">Primary</button>
<button class="tulip-btn tulip-btn-secondary">Secondary</button>
<button class="tulip-btn tulip-btn-success">Success</button>
<button class="tulip-btn tulip-btn-danger">Danger</button>
<button class="tulip-btn tulip-btn-warning">Warning</button>
<button class="tulip-btn tulip-btn-info">Info</button>
<button class="tulip-btn tulip-btn-light">Light</button>
<button class="tulip-btn tulip-btn-dark">Dark</button>
```

**Outline Variants:**

```html
<button class="tulip-btn tulip-btn-outline-primary">Outline Primary</button>
```

**Sizes:**

```html
<button class="tulip-btn tulip-btn-sm">Small Button</button>
<button class="tulip-btn">Medium Button</button>
<button class="tulip-btn tulip-btn-lg">Large Button</button>
```

**Disabled State:**

```html
<button class="tulip-btn tulip-btn-primary" disabled>Disabled Button</button>
```

**Button Group:**

```html
<div class="tulip-btn-group">
  <button class="tulip-btn">Button 1</button>
  <button class="tulip-btn">Button 2</button>
  <button class="tulip-btn">Button 3</button>
</div>
```

### Forms (`.tulip-form-control`, `.tulip-form-check`, etc.)

**Input Fields & Textarea:**

```html
<input type="text" class="tulip-form-control" placeholder="Enter text...">
<textarea class="tulip-form-control" rows="3" placeholder="Enter message..."></textarea>
```

**Select Element:**

```html
<select class="tulip-form-control">
  <option>Select an option...</option>
  <option>Option 1</option>
  <option>Option 2</option>
</select>
```

**Validation States:**

```html
<input type="text" class="tulip-form-control is-valid" placeholder="Valid input">
<input type="text" class="tulip-form-control is-invalid" placeholder="Invalid input">
```

**Checkboxes & Radios:**

```html
<div class="tulip-form-check">
  <input class="tulip-form-check-input" type="checkbox" id="exampleCheck1">
  <label class="tulip-form-check-label" for="exampleCheck1">
    Check me out
  </label>
</div>

<div class="tulip-form-check">
  <input class="tulip-form-check-input" type="radio" name="exampleRadio" id="exampleRadio1" value="option1" checked>
  <label class="tulip-form-check-label" for="exampleRadio1">
    Default radio
  </label>
</div>
<div class="tulip-form-check">
  <input class="tulip-form-check-input" type="radio" name="exampleRadio" id="exampleRadio2" value="option2">
  <label class="tulip-form-check-label" for="exampleRadio2">
    Second radio
  </label>
</div>
```

**Input Groups:**

```html
<div class="tulip-input-group mb-3">
  <div class="tulip-input-group-prepend">
    <span class="tulip-input-group-text">@</span>
  </div>
  <input type="text" class="tulip-form-control" placeholder="Username">
</div>

<div class="tulip-input-group">
  <input type="text" class="tulip-form-control" placeholder="Recipient's email">
  <div class="tulip-input-group-append">
    <span class="tulip-input-group-text">@example.com</span>
  </div>
</div>
```

### Cards (`.tulip-card`)

```html
<div class="tulip-card">
  <div class="tulip-card-header">
    Featured
  </div>
  <div class="tulip-card-body">
    <h5 class="tulip-card-title">Special title treatment</h5>
    <p class="tulip-card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="tulip-btn tulip-btn-primary">Go somewhere</a>
  </div>
</div>
```

### Alerts (`.tulip-alert`)

```html
<div class="tulip-alert tulip-alert-primary" role="alert">
  This is a primary alert! Check it out.
</div>
<div class="tulip-alert tulip-alert-success" role="alert">
  Success message! Everything is fine.
</div>
<div class="tulip-alert tulip-alert-warning" role="alert">
  Be careful, this is a warning.
</div>
<div class="tulip-alert tulip-alert-danger" role="alert">
  Something went wrong!
</div>

<!-- Alert with close button -->
<div class="tulip-alert tulip-alert-info" role="alert">
  This is an informational alert.
  <button type="button" class="tulip-alert-close" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
```

### Badges (`.tulip-badge`)

```html
<span class="tulip-badge tulip-badge-primary">Primary</span>
<span class="tulip-badge tulip-badge-secondary">Secondary</span>
<span class="tulip-badge tulip-badge-success">Success</span>
<span class="tulip-badge tulip-badge-danger">Danger</span>
<span class="tulip-badge tulip-badge-warning">Warning</span>
<span class="tulip-badge tulip-badge-info">Info</span>
<span class="tulip-badge tulip-badge-light">Light</span>
<span class="tulip-badge tulip-badge-dark">Dark</span>

<!-- Pill Badges -->
<span class="tulip-badge tulip-badge-pill tulip-badge-primary">Pill Primary</span>
```

### Navigation (`.tulip-nav`, `.tulip-nav-tabs`, `.tulip-nav-pills`)

**Tabs:**

```html
<ul class="tulip-nav tulip-nav-tabs">
  <li class="tulip-nav-item">
    <a class="tulip-nav-link active" href="#">Active Tab</a>
  </li>
  <li class="tulip-nav-item">
    <a class="tulip-nav-link" href="#">Link</a>
  </li>
  <li class="tulip-nav-item">
    <a class="tulip-nav-link" href="#">Another Link</a>
  </li>
  <li class="tulip-nav-item">
    <a class="tulip-nav-link disabled" href="#">Disabled Tab</a>
  </li>
</ul>
```

**Pills:**

```html
<ul class="tulip-nav tulip-nav-pills">
  <li class="tulip-nav-item">
    <a class="tulip-nav-link active" href="#">Active Pill</a>
  </li>
  <li class="tulip-nav-item">
    <a class="tulip-nav-link" href="#">Link</a>
  </li>
</ul>
```

### Dropdowns (`.tulip-dropdown`)

*Note: JavaScript is required to toggle dropdown menus.*

```html
<div class="tulip-dropdown">
  <button class="tulip-btn tulip-btn-secondary dropdown-toggle" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown
  </button>
  <div class="tulip-dropdown-menu" aria-labelledby="dropdownMenuButton">
    <a class="tulip-dropdown-item" href="#">Action</a>
    <a class="tulip-dropdown-item" href="#">Another action</a>
    <a class="tulip-dropdown-item" href="#">Something else here</a>
    <div class="tulip-dropdown-divider"></div>
    <a class="tulip-dropdown-item" href="#">Separated link</a>
  </div>
</div>
```

### Modals (`.tulip-modal`)

*Note: JavaScript is typically required to show, hide, and manage modals. The CSS provides the structure.*

```html
<!-- Basic Modal Structure -->
<div class="tulip-modal show"> <!-- Add 'show' class to display -->
  <div class="tulip-modal-dialog">
    <div class="tulip-modal-content">
      <div class="tulip-modal-header">
        <h5 class="tulip-modal-title">Modal Title</h5>
        <button type="button" class="tulip-alert-close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="tulip-modal-body">
        <p>This is the modal body. It contains the main content.</p>
      </div>
      <div class="tulip-modal-footer">
        <button type="button" class="tulip-btn tulip-btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="tulip-btn tulip-btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

### Tooltips (`.tulip-tooltip`)

*Note: JavaScript is needed for dynamic positioning and showing/hiding.*

```html
<div class="tulip-tooltip">
  <span class="tulip-tooltip-text">This is a tooltip!</span>
  Hover over me
</div>

<div class="tulip-tooltip tulip-tooltip-bottom">
  <span class="tulip-tooltip-text">Tooltip on the bottom</span>
  Hover over me (bottom)
</div>
```

### Pagination (`.tulip-pagination`)

```html
<nav aria-label="Page navigation example">
  <ul class="tulip-pagination">
    <li class="tulip-page-item disabled">
      <a class="tulip-page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a>
    </li>
    <li class="tulip-page-item"><a class="tulip-page-link" href="#">1</a></li>
    <li class="tulip-page-item active" aria-current="page"><a class="tulip-page-link" href="#">2</a></li>
    <li class="tulip-page-item"><a class="tulip-page-link" href="#">3</a></li>
    <li class="tulip-page-item">
      <a class="tulip-page-link" href="#">Next</a>
    </li>
  </ul>
</nav>
```

## Utility Classes

Tulip provides a set of utility classes prefixed with `tulip-` for quick styling and layout adjustments.

**Examples:**

*   **Display:** `tulip-d-flex`, `tulip-d-none`, `tulip-d-inline-block`
*   **Spacing (Margins & Padding):** `tulip-mt-md`, `tulip-pb-lg`, `tulip-mx-auto` (margin left/right auto)
*   **Text Alignment:** `tulip-text-center`, `tulip-text-right`
*   **Text Styling:** `tulip-text-truncate`, `tulip-fw-bold`
*   **Colors:** `tulip-text-primary`, `tulip-bg-success`
*   **Borders:** `tulip-rounded-lg`, `tulip-border`
*   **Visibility:** `tulip-invisible`

Refer to the `tulip.css` source file for a comprehensive list of available utility classes.

## Browser Support

Tulip is designed to work with modern browsers. Support for **CSS Variables** means it's best experienced on:

*   Chrome 64+
*   Firefox 65+
*   Safari 11.1+
*   Edge 79+
*   Opera 51+

For older browsers, a graceful degradation might occur, or specific components might not render as intended. Fallbacks for critical styles can be implemented in your custom CSS if broader support is required.

## Contributing

We welcome contributions! If you'd like to improve Tulip, please:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature`).
3.  Make your changes.
4.  Ensure your code adheres to the existing style and naming conventions.
5.  Commit your changes (`git commit -am 'Add some feature'`).
6.  Push to the branch (`git push origin feature/your-feature`).
7.  Open a Pull Request.

Please ensure any new components or modifications are well-documented in the README.

## License

This project is licensed under the [Your Chosen License, e.g., MIT License] - see the `LICENSE.md` file for details.
```

---
