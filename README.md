# Styling Web Pages using Bootstrap
This tutorial guides you through the building blocks of designing webpages using **Bootstrap 5**, leveraging the provided code snippets as sequential, modular blocks to create a responsive layout using modern components and utility classes.

**Objective:**
1. Bootstrap Inclusion & Version
2. Implementing Bootstrap Components
3. Layout and Utility Usage
4. Applying Addtional Dependencies

> **What is BootStrap:** [Bootstrap](https://getbootstrap.com/) is a widely popular front-end open-source toolkit for building responsive projects on the web. It includes HTML, CSS, and JavaScript framework templates for common user interface components, such as typography, forms, buttons, navigation, modals, and much more. The primary goal of Bootstrap is to allow developers to build professional, consistent, and responsive web layouts quickly, utilizing its vast library of utility classes and pre-built components.

> **Bootstrap Examples (Themes/Templates):** The official documentation offers starter templates and comprehensive example pages that showcase complex layouts built entirely with Bootstrap. For more details, click on the link: [https://getbootstrap.com/docs/5.3/examples/](https://getbootstrap.com/docs/5.3/examples/)

---

## 📖 1. Bootstrap Inclusion & Version
The project utilizes **Bootstrap v5.3.3** by including its CSS and JavaScript bundle via Content Delivery Network (CDN) links.

### 1.1. CSS (In the `<head>` tag)
The primary Bootstrap stylesheet is included for styling and utility classes:

```html
<!-- Import Bootstrap 5's utility classes and components via its CDN -->
<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
  crossorigin="anonymous"
/>
```

### 1.2. JavaScript (Before the closing </body> tag)
The Bootstrap JavaScript bundle, which includes Popper.js (necessary for components like the Navbar toggle), is included to enable interactive elements:

```html
<script
  src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
  integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
  crossorigin="anonymous"
></script>
```

Click on the [link](https://getbootstrap.com/docs/5.3/getting-started/introduction/) for the quick start guide on [Bootstrap](https://getbootstrap.com/docs/5.3/getting-started/introduction/).

---

## 📖 2. Implmenenting Bootstrap Components

This following outlines the standard **Bootstrap** components implemented in the project's markup. These components are essential for the layout, navigation, and user interaction design.

| Component | Description | Example Classes/Attributes |
| :--- | :--- | :--- |
| **Navbar** | A fully responsive **navigation bar** with branding and a collapsible toggle for smaller screens. | `navbar`, `navbar-expand-md`, `navbar-toggler`, `data-bs-toggle="collapse"`, `data-bs-target="#navbarNav"` |
| **Card** | Used for displaying content in a **structured, grouped format** (e.g., product/feature previews, testimonials). | `card-group`, `card`, `card-body`, `card-img-top` |
| **Form** | Used primarily for the **email newsletter subscription section** and any user input fields. | `form-control`, `input-group` |
| **Button** | Standardized, themed, and stylized **call-to-action buttons** for user interaction. | `btn`, `btn-primary` (or other contextual color classes like `btn-secondary`, `btn-info`) |

Click on the [link](https://getbootstrap.com/docs/5.3/components/) for the full documentation and usage details of [Bootstrap 5 Components](https://getbootstrap.com/docs/5.3/components/).

---

## 📖 3. Layout and Utility Usage
**Bootstrap 5 utility and layout classes** are utilized within this exercise to achieve styling, responsiveness, and positioning.

### 3.1. Layout and Grid System 

The page structure relies heavily on Bootstrap's responsive **Grid** and **Flexbox** utilities for alignment and positioning.

| Category | Utility Class | Context (index.html) | Description |
| :--- | :--- | :--- | :--- |
| **Containers** | `container` | Used multiple times (e.g., around Navbar, Newsletter, and Cards). | Wraps and centers page content, providing responsive fixed-width or fluid behavior. |
| **Grid Sizing** | `col-md-8`, `col-lg-3` | Used in the Newsletter section. | Defines column widths for **medium** (`md`) screens and up (8/12 width) and **large** (`lg`) screens and up (3/12 width). |
| **Centering** | `mx-auto` | Used on the Newsletter wrapper (`col-md-8`). | Sets left and right margins to auto, horizontally **centering** a block-level element within its parent. |
| **Flex Container** | `d-flex`, `flex-column` | Used on the Header/Banner element. | Initializes a **Flexbox container** (`d-flex`) and stacks its children vertically (`flex-column`). |
| **Flex Alignment** | `align-items-center`, `justify-content-center` | Used on the Header/Banner element. | Centers children **vertically** (`align-items-center`) and **horizontally** (`justify-content-center`) within the Flexbox container. |

### 3.2. Spacing and Typography

These utilities are used for fine-tuning the look of text and managing the space around elements (margins and padding).

| Category | Utility Class | Context (index.html) | Description |
| :--- | :--- | :--- | :--- |
| **Spacing** | `mt-4`, `pt-2`, `pb-2`, `mx-3` | Used across containers, headers, and cards. | Applies responsive **Margin** (`m`) or **Padding** (`p`) in the designated direction (top, bottom, x-axis, etc.), using a scale of 1 to 5 (`4` is a larger space than `2`). |
| **Display Headings** | `display-1`, `display-6` | Used on the hero text in the Header. | Styles headings dramatically larger than default `h1` through `h6`. |
| **Font Weight** | `fw-lighter`, `fw-light` | Used throughout the Navbar, Header, and Card text. | Sets the font weight to **lighter** or **light**, often resulting in a more refined look. |
| **Text Styling** | `text-white`, `text-uppercase`, `text-center` | Used on the Header and Newsletter text. | Sets text color to white, converts text to all uppercase, and centers the text alignment. |

---

### 3.3. Styling Utilities and Sizing

These classes apply specific visual treatments and control the dimensions of key page elements.

| Category | Utility Class | Context (index.html) | Description |
| :--- | :--- | :--- | :--- |
| **Borders/Rounding** | `rounded-4`, `rounded-top-3` | Used on the Header/Hero Banner and Card images. | Applies a large **border-radius** (scale 4) to all corners, or a medium border-radius (scale 3) only to the top two corners. |
| **Background/Color** | `text-bg-dark`, `btn-primary` | Used on the Footer and CTA buttons. | Sets the element's background to the dark theme color and adjusts text color for accessibility (Footer). Applies the theme's **primary color** to a button. |
| **Sizing** | `min-vh-75` | Used on the main content wrapper container. | Sets the **minimum height** of the element to **75%** of the viewport height (`vh`), ensuring the header area is always prominent. |

---

## 📖 4. Applying Addtional Dependencies

While not Bootstrap itself, the project also includes **Font Awesome** (v6.6.0 via CDN) for icons, which is a common complement to Bootstrap projects:

```html
<link 
    rel="stylesheet" 
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" 
    integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" 
    crossorigin="anonymous" 
    referrerpolicy="no-referrer" 
/>
```

Font Awesome is a popular toolkit that provides web designers and developers with a large collection of scalable vector icons that can be customized with CSS. Now, the button code would look like this:

```html
<button class="btn btn-primary" type="submit" id="button-addon2">
  <i class="fa-regular fa-paper-plane"></i>
  Send
</button>
```
Click on the [link](https://fontawesome.com/?o=r) for the full list of icons and styles available at [Font Awesome](https://getbootstrap.com/docs/5.2/components/).

Using an external dependency like Font Awesome for icons offers trade-offs between development efficiency and project control.

### 👍 Advantages of External Dependencies (e.g., Font Awesome)

| Advantage | Description |
| :--- | :--- |
| **Speed of Development** | You save **significant time** by not having to create, optimize, or manage your own icon assets. Icons are immediately ready to use with simple classes. |
| **Scalability & Quality** | Since the icons are **vector-based (fonts/SVGs)**, they look sharp on any screen resolution or zoom level without requiring multiple image files. |
| **Ease of Customization** | Icons can be styled effortlessly using **standard CSS**. You can change their color, size, shadows, and opacity just as you would with text. |
| **Wide Selection** | You gain immediate access to **thousands of professionally designed icons** that are continuously updated. |
| **Browser Support** | Popular dependencies are generally **well-tested and maintained**, ensuring good cross-browser compatibility. |

### 👎 Disadvantages of External Dependencies

| Disadvantage | Description |
| :--- | :--- |
| **Performance/Loading Time** | Even though efficient, loading an external CSS file and font/SVG files (especially via CDN) adds **extra HTTP requests** and initial page load time. |
| **Dependency on External Source** | If the CDN server (e.g., cdnjs.cloudflare.com) goes down or is slow, your icons will fail to load or load slowly, impacting the user experience. |
| **Security Risks** | While rare for major CDNs, using any external script or file introduces a small **security risk**. If the external source is compromised, it could potentially affect your website. |
| **Increased Project Bloat** | If you only need five icons, you are still loading the **entire library** (thousands of icons) and its associated CSS, increasing the overall file size of your project. |
| **Versioning Issues** | If the external library updates its CSS or classes, your project might **break unexpectedly** if you haven't pinned a specific version or managed the update correctly. |

---

## 📖 5. Custom Styling and Bootstrap Overrides

This project uses a custom stylesheet (`styles/styles.css`) to define the overall look, including background treatments, typography, and specifc overrides on one of Bootstrap's default primary color scheme.

```html
<!-- Import custom stylesheet -->
<link rel="stylesheet" href="styles/styles.css" />
```

### 5.1. Custom Styling and Bootstrap Overrides

| Category | Selector/Property | Description | Key Customization |
| :--- | :--- | :--- | :--- |
| **Global Setup** | `html` / `body` | Sets the base font family to **Poppins** and establishes a root font size of `16px`. | Applies a fixed, semi-transparent background image (`motorsport.png`) with a **`background-blend-mode: overlay`** to ensure text readability over the image. |
| **Primary Color Override** | `.btn-primary` and `.bg-primary` | **Crucial Override:** Redefines Bootstrap's default blue primary color to a custom red/orange shade (`#ea383c`). | Uses the **`!important`** keyword to ensure the custom color successfully overrides Bootstrap's built-in specificity for buttons and backgrounds. |
| **Header/Hero Styling** | `.herobanner` | Defines the background image (`sneaker.jpg`) and ensures it covers the area without repetition. | Applies a **`min-height: 50dvh`** (50% of dynamic viewport height) for visual impact, complementing the Bootstrap `min-vh-75` on the outer container. |
| **Visual Effects** | `.shadow-effects` | Applied to the header text elements (`h1`, `h4`). | Creates visual depth using **`text-shadow`** and applies a wide **`letter-spacing`** (`0.8rem` and `0.10em`). |
| **Gradient Effect** | `.herobanner h1` | Applied to the main title "Sole Runner." | Uses a **`linear-gradient`** as a background for the text, fading from transparent to a bright orange/yellow, for a striking visual effect. |
| **Image Fallback** | `.homepage-card img` | Sets a fallback placeholder image and background properties. | Provides a visual **`imgplaceholder.png`** for card images if the actual image files are missing. |

---

## 🛠️ Activity

Refer to the step-by-step guide below. Use the provided code to construct the webpage, focusing on the components and utility classes made available through **Bootstrap** and **Font Awesome**.

### Step 1: Setup and Foundation (HTML Structure & CDN Links)
- [ ] Start with the basic HTML document structure and immediately link the **Bootstrap 5 CSS Content Delivery Network(CDN)** to enable all utility classes and components.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Airstream</title>

    <!-- Import Bootstrap 5's utility classes and components via its CDN -->
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
      crossorigin="anonymous"
    />
    
    <!-- Import fonts awesome stylesheet -->
    <link 
        rel="stylesheet" 
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" 
        integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" 
        crossorigin="anonymous" 
        referrerpolicy="no-referrer" 
    />
    
    <!-- Import custom stylesheet -->
    <link rel="stylesheet" href="styles/styles.css" />

  </head>
  <body>
    <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
    crossorigin="anonymous"
    ></script>

    <!-- Step 2 -->
    <!-- Container hosting the site main navigation, and header (aka "hero") Section -->

    <!-- Step 3 -->
    <!-- Container hosting the newsletter form -->
    
    <!-- Step 4 -->
    <!-- Container hosting a card group component -->

    <!-- Step 5 -->
    <!-- Footer hosting copyright information -->

  </body>
</html>
```

### Step 2: Navbar, and Header/Hero Section
- [ ] **Section:** _Container hosting the site main navigation, and header (aka "hero") Section_
- [ ] Wrap the navigation bar and header content in a container to create a responsive Navbar and Header.
- [ ] Place this code immediately inside the `<body>` tag.

```html
<!-- Step 2 -->
<!-- Container hosting the site main navigation, and header (aka "hero") Section -->
<div class="container min-vh-75 p-4">
  <nav class="navbar navbar-expand-md navbar-dark fw-lighter">
    <div class="container-fluid">
      <a class="navbar-brand" href="#"
        ><img src="img/logo.png" alt="Company Logo" class="img-fluid"
      /></a>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="index.html"
              >Home</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="contact.html">Contact</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Sign-in/Login</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <header
    class="herobanner rounded-4 text-center mt-4 pt-2 pb-2 d-flex flex-column align-items-center justify-content-center"
  >
    <h1 class="display-1 text-white fw-lighter shadow-effects">
      Sole Runner
    </h1>
    <h4 class="display-6 text-white fw-light text-uppercase shadow-effects">
      Autumn Gear
    </h4>
    <a
      class="btn btn-primary btn-primary-shadow text-uppercase fw-light"
      href="#"
      >enter</a
    >
  </header>
</div>
```

### Step 3: Newsletter Subscription Form
- [ ] **Section:** _Container hosting the newsletter form_
- [ ] Add the newsletter form using Bootstrap's Grid System (col-md-8, mx-auto for centering and width control) and the Input Group component.

```html
<!-- Step 3 -->
<!-- Container hosting the newsletter form -->
<div class="container mt-5">
  <div class="d-flex flex-column">
    <div class="col-md-8 mx-auto">
      <div class="text-white text-center fw-light pt-2 pb-2">
        Subscribe to our Newsletter:
      </div>

      <form action="" method="post">
        <div class="input-group mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="e.g. john@email.com"
            aria-label="Recipient's username"
            aria-describedby="button-addon2"
          />
          <button class="btn btn-primary" type="submit" id="button-addon2">
            <i class="fa-regular fa-paper-plane"></i>
            Send
          </button>
        </div>
      </form>
    </div>
  </div>
</div>
```

### Step 4: Feature Cards Section
- [ ] **Section:** _Container hosting a card group component_
- [ ] Create a responsive group of three product/feature previews using the Card Group component, which ensures the cards have equal height and are well-spaced.

```html
<!-- Step 4 -->
<!-- Container hosting a card group component -->
<div class="container mt-4 mb-4">
  <div class="card-group homepage-card">
    <div class="card mx-3 border-0 rounded-4">
      <img
        src="img/comfort.jpg"
        class="card-img-top rounded-top-3"
        alt="..."
      />
      <div class="card-body">
        <h5 class="card-title text-secondary fw-light">Uber Comfort</h5>
        <p class="card-text fw-light small">
          This is a wider card with supporting text below as a natural
          lead-in to additional content. This content is a little bit
          longer.
        </p>
      </div>
    </div>

    <div class="card mx-3 border-0 rounded-4">
      <img
        src="img/performance.jpg"
        class="card-img-top rounded-top-3"
        alt="..."
      />
      <div class="card-body">
        <h5 class="card-title text-secondary fw-light">
          Made for Performance
        </h5>
        <p class="card-text fw-light small">
          This card has supporting text below as a natural lead-in to
          additional content.
        </p>
      </div>
    </div>

    <div class="card mx-3 border-0 rounded-4">
      <img
        src="img/outdoor.jpg"
        class="card-img-top rounded-top-3"
        alt="..."
      />
      <div class="card-body">
        <h5 class="card-title text-secondary fw-light">All-weather Suit</h5>
        <p class="card-text fw-light small">
          This is a wider card with supporting text below as a natural
          lead-in to additional content. This card has even longer content
          than the first to show that equal height action.
        </p>
      </div>
    </div>
  </div>
</div>
```

### Step 5: Footer and Copyright Section
- [ ] **Section:** _Footer hosting copyright information_
- [ ] Conclude the page with a `footer` that contains the copyright information, using Bootstrap utility classes for text color, alignment, and padding.
- [ ] **IMPOTANT:** Place this code block directly after the closing </div> from the Cards section, but before the Bootstrap JavaScript link.

```html
<!-- Step 5 -->
<!-- Footer hosting copyright information -->
<footer class="text-white fw-lighter text-lg-start">
  <div class="text-center p-3 small">
    &copy; 2025 Copyright:
    <a class="text-white text-decoration-none" href="#"
      >Airstream &trade; - All rights reserved.</a
    >
  </div>
</footer>
```