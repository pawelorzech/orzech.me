# orzech.me

This is the personal landing page for Paulina and Paweł Orzech. It's a simple, elegant, and feature-rich single-page application designed to serve as a digital business card.

## ✨ Features

- **Bilingual Content:** Supports both Polish (🇵🇱) and English (🇬🇧). The user's language preference is saved in `localStorage`.
- **Dynamic Theme Switching:**
    - **Light Mode (☀️):** A gentle, animated gradient background with a glowing, drifting sun.
    - **Dark Mode (🌙):** A deep, dark gradient background with twinkling stars, a glowing moon, and occasional shooting stars.
    - **System Mode (💻):** Automatically syncs with the user's operating system's color scheme.
    - Theme preference is saved in `localStorage`.
- **Real-time Clock:** Displays the current time, dynamically updating every minute. It also shows a relevant emoji (☀️, 🌇, or 🌙) based on the time of day.
- **Interactive Elements:**
    - Subtle animations on buttons and links.
    - A "wiggle" animation on the GitHub link in the footer on hover.
    - The nut emoji (🌰) in the footer grows and rotates on hover.
- **Responsive Design:** The layout is fully responsive and adapts to different screen sizes, from mobile phones to desktops.
- **Accessibility Features:** Full ARIA label support, semantic HTML structure, and keyboard navigation friendly.
- **SEO Optimized:** Comprehensive meta tags including Open Graph, Twitter Cards, canonical URLs, and structured data for improved search engine visibility and social media sharing.
- **Performance Optimized:** Clean, efficient code with optimized animations and minimal resource usage.
- **Modern Tech Stack:** Built with HTML, Tailwind CSS, and vanilla JavaScript, ensuring a lightweight and fast experience.

## 🛠️ How It Works

The entire site is a single `index.html` file, making it extremely portable and easy to deploy.

- **Styling:** [Tailwind CSS](https://tailwindcss.com/) is used for utility-first styling. All custom styles and animations are included within a `<style>` block in the head of the document.
- **Theme Management:** A JavaScript function, `applyTheme()`, handles the logic for switching themes. It adds or removes the `dark` class from the `<html>` element, which is then used by Tailwind's `dark:` variants to apply the correct styles. The theme choice is persisted in `localStorage`. The `(prefers-color-scheme: dark)` media query is used to detect the system theme.
- **Language Switching:** Translations are stored in a JavaScript object. A `setLanguage()` function updates the text content of elements based on `data-translate-key` attributes. The chosen language is also persisted in `localStorage`.
- **Dynamic Animations:**
    - The background animations (sun, moon, stars) are created and managed with JavaScript. Elements are dynamically added or removed from the DOM based on the current theme and time of day.
    - CSS keyframe animations are used for the twinkling stars, shooting stars, sun/moon glow and drift, and other interactive effects.
- **On-Load Initialization:** A `window.addEventListener('load', ...)` function initializes the theme, language, and all event listeners for the interactive elements once the page has fully loaded.