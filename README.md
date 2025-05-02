# Tabbed Multi-Calculator Deluxe++

This is an interactive web application featuring multiple "calculators" or visualizers presented in a tabbed interface, enhanced with dynamic effects, themed styling, and a bubble wrap clicker mini-game.

## Features

* **Tabbed Interface:** Switch between three distinct calculators:
    * **Pi Calculator:** Calculates and displays digits of Pi sequentially using a spigot algorithm. Features confetti effects linked to complexity.
    * **Matrix:** Simulates the "Matrix digital rain" effect on a 2D canvas, counting displayed characters. Complexity affects density, fading, and glow.
    * **Warp Drive:** Simulates a star field warp effect on a 2D canvas, counting stars passed. Complexity controls the number of stars.
* **Individual Controls:** Each tab has its own controls:
    * Start/Continue/Pause buttons.
    * Speed slider.
    * Complexity slider affecting visual effects specific to the tab.
    * Save/Load buttons to save/restore the state of the current tab (including global/bubble state).
* **Global Controls:** Sliders (typically bottom-left) to adjust the overall Hue, Brightness, and Saturation of the main application container.
* **Bubble Wrap Clicker:** A toggleable popup window (top-right button) containing "bubble wrap" bubbles that can be popped. Features a counter and a regeneration mechanic where bubbles reappear based on popping speed.
* **Dynamic Effects:** Subtle, randomized visual effects (hue shifts, glow intensity changes) applied periodically to the active tab for added visual interest.
* **Theming:** Each tab applies a distinct color theme to the main container and its elements.
* **Responsive Design:** Adapts layout for different screen sizes (desktop, tablet, mobile).

## How to Run

1.  **Save Files:**
    * Save the CSS code (from the relevant `style.css` artifact) as `style.css`.
    * Save the HTML & JavaScript code (from the relevant `index.html` artifact) as `index.html`.
    * Ensure both `index.html` and `style.css` are in the **same folder**.
2.  **Open:** Open the `index.html` file in a modern web browser (like Chrome, Firefox, Edge, Safari).

## Dependencies

This application relies on external libraries loaded via CDN:

* **Font Awesome:** For icons (used in the bubble toggle button).
    * `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">`

An internet connection is required on first load to fetch this library. (Note: three.js is *not* required for this version).

## File Structure

/your-project-folder|-- index.html  (HTML structure and all JavaScript logic)|-- style.css   (All CSS styling rules)
## Notes

* **Save/Load:** The save function stores the current visible state (counts, settings, Pi digits) and global/bubble state in a JSON file. Loading restores this state but does *not* perfectly resume the internal state of the Pi generator. You need to manually press Start/Continue after loading.
* **Pi Calculation:** The spigot algorithm used for Pi calculation is relatively simple and will become slow if left running to calculate a very large number of digits directly in the browser.
* **Browser Compatibility:** Developed and tested primarily on modern browsers. Some visual effects or features might behave differently on older browsers.
