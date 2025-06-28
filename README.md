# orzech.me

This is a personal website for Paulina and Paweł Orzech. It serves as a central hub for their online presence, providing contact information and links to their individual projects and social media.

## Features:

- **Dynamic Theme Switching:** Users can switch between light, dark, and system-preferred themes. The site dynamically adjusts its appearance, including background animations (sun for light mode, moon and stars for dark mode).
- **Multi-language Support:** The website supports both Polish and English, with content dynamically updated based on user selection.
- **Real-time Clock:** Displays the current time with an appropriate emoji (sun, sunset, or moon) based on the time of day.
- **Contact Information:** Provides direct email links for Paulina and Paweł.
- **Navigation to Personal Pages:** Links to Paweł's blog and a placeholder for Paulina's page.
- **Responsive Design:** The layout adjusts for optimal viewing on various screen sizes.

## How it Works:

The website is built using plain HTML, CSS (with Tailwind CSS for utility classes), and JavaScript. 

- **Theme Management:** JavaScript handles theme switching by toggling CSS classes on the `<html>` element and storing the user's preference in `localStorage`. It also listens for system theme changes.
- **Language Switching:** Translations are stored in a JavaScript object. When a language is selected, JavaScript updates the `lang` attribute of the `<html>` element and iterates through elements with `data-translate-key` attributes to update their content. Language preference is also saved in `localStorage`.
- **Animations:** CSS animations are used for background effects (wind breeze, sun glow/drift, star twinkle, shooting stars, moon glow/drift) and subtle UI interactions (button hovers, content fade-in, GitHub link wiggle).
- **Favicon:** A dynamic SVG favicon is used to display an emoji (walnut) directly in the browser tab.