# M² Medya Project Instructions

## Project Overview
- **Type:** Static HTML Website (No backend, no build process).
- **Brand:** M² Medya (Digital Marketing Agency).
- **Language:** Turkish (tr).
- **Root Directory:** `buyer-file/` (All edits happen here).

## Architecture & File Structure
- **HTML:** Independent `.html` files in `buyer-file/`.
  - **No Partials:** Header, Footer, and common sections are **duplicated** in every file.
  - **Editing Rule:** When changing a common element (e.g., Menu), you MUST apply the change to **ALL** `.html` files manually.
- **CSS:** `assets/css/main.css` (Main styles), `assets/scss/` (Source SASS, but we edit CSS directly or compile if setup).
- **JS:** `assets/js/main.js` (Main logic, jQuery-based).
- **Assets:** `assets/img/` (Images), `assets/fonts/` (Webfonts).

## Critical Workflows
- **Development:** Run a local server in `buyer-file/` (e.g., `python3 -m http.server` or VS Code Live Server).
- **Deployment:** Static file hosting. No build command required.
- **Design Preservation (CRITICAL):**
  - **NEVER** break the visual layout or CSS classes.
  - SEO changes should be invisible (meta tags) or text-only updates.
  - Do not change the folder structure or delete existing assets.
- **SEO Implementation (High Priority):**
  - Refer to `SEO_PLAN.md` for the detailed strategy.
  - Ensure `lang="tr"` on all pages.
  - Maintain unique `<title>` and `<meta name="description">` for every page.
  - Add Open Graph (`og:`) and Twitter Card tags to `<head>`.
  - Use Canonical URLs (`<link rel="canonical">`).
  - All images must have descriptive `alt` attributes (No `alt="img"`).

## Code Style & Conventions
- **HTML:** Semantic HTML5. Use `<header>`, `<footer>`, `<main>`, `<section>`.
- **CSS:** Bootstrap 5 based. Use utility classes where possible, custom classes in `main.css`.
- **JS:** jQuery syntax is prevalent. Wrap code in `(function($) { ... })(jQuery);`.
- **Content & Data:**
  - **Address:** "Konyaaltı, Antalya, Türkiye".
  - **Language:** Turkish only (for now).
  - **Logo:** Use a placeholder or text if image is missing. Recommend SVG for future.
  - All user-facing text must be **Turkish**.
  - Translate any leftover English text from the template (e.g., "Read More" -> "Devamını Oku").
  - Use "M² Medya" branding consistently.

## Key Files
- `buyer-file/index.html`: Homepage (Master template for header/footer changes).
- `buyer-file/assets/css/main.css`: Primary stylesheet.
- `buyer-file/assets/js/main.js`: UI interactions (Mobile menu, Sliders).
- `SEO_PLAN.md`: Comprehensive SEO checklist and strategy.
