# Oliver's Interactive Spaceship Controller (Dad-Ship Edition)

## Welcome Aboard! 👋

This is a simple, interactive web-based soundboard designed to look like a spaceship control panel. I built it for my son, Oliver, so he can press the buttons and 'control' me as I pretend to be his spaceship, responding to his commands with appropriate noises (or actions!). It's built purely with HTML, CSS, and JavaScript, requiring no backend.

It's hosted live using GitHub Pages here:
[**>>> Try the Live Controller Here <<<**](https://SEU_USUARIO.github.io/SEU_REPOSITORIO/)
*(Replace the link above with your actual GitHub Pages URL!)*

## How it Works ⚙️

*   **Image-Based Interface:** Uses a single image (`controlador.jpg` or your chosen file) as the controller background.
*   **Clickable Zones:** Invisible HTML `<div>` elements are precisely positioned over the buttons in the image using CSS absolute positioning.
*   **Sound Playback:** JavaScript listens for `click` events on these zones and plays the corresponding audio files stored in the `sons/` directory.
*   **Static Web App:** Runs entirely in the browser.

## Customization Guide 🔧

This project is designed to be easily customizable if you want to adapt it for your own use or just tinker with it. Here's what you can change:

### 1. Controller Image

*   **File:** Replace the `controlador.jpg` file (or whatever you named your image) in the main directory with your own controller design (e.g., a different graphic, a photo of a toy).
*   **CSS Adjustment (Crucial!):** If you change the image, you will **definitely** need to adjust the positions and sizes of the clickable button areas in the CSS.
    *   Edit the `<style>` section within the `index.html` file.
    *   Find the CSS rules for each button ID (e.g., `#botao-quadrado`, `#botao-x`, `#botao-cima`, etc.).
    *   Modify the `top`, `left`, `width`, and `height` properties (likely using percentages `%` for responsiveness) until the invisible clickable areas align perfectly over the buttons on *your* new image.
    *   **Tip:** Temporarily uncomment the `background-color` property within the `.botao-clicavel` CSS rule to make the areas visible while you adjust them using your browser's Developer Tools (F12 -> Inspector).

### 2. Sounds

*   **Files:** Place your desired sound files (e.g., `.mp3`, `.wav`, `.ogg`) inside the `sons/` directory.
*   **Mapping:** You need to ensure the sound files are correctly linked in `index.html`:
    *   Each clickable `div` (e.g., `<div class="botao-clicavel" id="botao-x" data-sound="som_x"></div>`) has a `data-sound` attribute.
    *   Each `<audio>` tag (e.g., `<audio id="som_x" class="audio-hidden" src="sons/som_x.mp3" preload="auto"></audio>`) has an `id` that matches the `data-sound` attribute and a `src` pointing to the actual sound file.
    *   **To change a sound:** You can either:
        *   Replace the existing file in the `sons/` folder with a new file *of the same name* (e.g., replace `sons/som_x.mp3` with your own sound named `som_x.mp3`).
        *   OR, use a new file name (e.g., `laser_blast.wav`) and update *both* the `data-sound` attribute on the corresponding `div` (`data-sound="laser_blast"`) and the `id` and `src` attributes on the corresponding `<audio>` tag (`id="laser_blast"` and `src="sons/laser_blast.wav"`).

### 3. Button Layout & Click Area Sensitivity

*   As mentioned in point 1, modifying the `top`, `left`, `width`, `height`, and `border-radius` properties for each button ID in the CSS within `index.html` allows you to change where the clickable areas are and how large they are. Increase `width` and `height` to make buttons easier to click.

### 4. Text & Basic Styling

*   **Text:** Edit the page title (`<title>`) and any other visible text directly within `index.html`. The "OLIVER SPACESHIP" text is part of the background image in the original example, so changing that would require editing the image itself.
*   **Styling:** Modify general appearance like the page background color (`body { background-color: ... }`) or add other visual flair within the `<style>` section of `index.html`.

## Have Fun Piloting! 🚀
