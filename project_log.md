# Website Development Logic Plan & Log

| Step | Specific Step | Resources | Description | Time |
| :--- | :--- | :--- | :--- | :--- |
| **I** | **Project Setup** | | | **15m** |
| 1 | Initialize Folder Structure | File Explorer | I will create a designated `chayn_cc_website` root folder to house all project files and an `assets` subdirectory to organize images (such as the hero background) separately from source code. | 2m |
| 2 | Create Core Files | VSC | I will initialize `index.html` as the main entry point for the website and `style.css` to contain all global styling rules, ensuring separation of content and presentation from the start. | 3m |
| 3 | Setup Global Styles | `style.css` | I will define CSS variables in `:root` for brand colors (`--nav-bg`, `--text-white`) and fonts (`--primary-font`) to ensure consistency across the site, and implement a CSS reset (`* { margin: 0; box-sizing: border-box; }`) to remove browser default padding. | 5m |
| 4 | Import External Assets | `index.html` | I will link the Google Fonts 'Inter' family for modern typography and the FontAwesome CDN to enable the use of scalable vector icons (like the pencil and location markers) throughout the UI. | 5m |
| **II** | **Homepage (index.html)** | | | **45m** |
| 1 | Build Header Structure | HTML | I will construct a responsive `<header>` element containing the site logo ("Meet **your** neighborhood") and a `<nav>` element with links to internal pages (Login, About), ensuring the logo itself acts as a link to the homepage. | 10m |
| 2 | Implement Hero Section | HTML/CSS | I will develop the main visual banner using a flexbox container with a full-viewport height (`100vh`) and a background image (`assets/hero-bg.png`), ensuring the background is set to `cover` and `center` for responsiveness. | 15m |
| 3 | Style Main Navigation | CSS | I will apply Flexbox to the navbar to space the logo and links appropriately and style navigational links with a transparent bottom border that animates to white on hover for a subtle interactive cue. | 10m |
| 4 | Create Call-to-Action Area | HTML/CSS | I will design the primary "Show me events" button and the secondary "Create an event" button using flexbox for alignment, styling them with rounded corners, shadows, and hover lift effects to encourage user interaction. | 10m |
| **III** | **Events Page (events.html)** | | | **40m** |
| 1 | Structure Events Layout | HTML | I will clone the `index.html` header and footer structure to ensure visual consistency and create a main content area with a responsive container that adapts padding based on screen size. | 5m |
| 2 | Implement Filter Controls | HTML/CSS | I will create a control bar in the page header containing "Sort by" and "Filter by" dropdown buttons, styled to match the brand's primary color scheme, and add the "Create Event" button here for easy access. | 10m |
| 3 | Develop Event Card Grid | CSS Grid | I will implement a responsive CSS Grid layout (`grid-template-columns: repeat(auto-fill, minmax(250px, 1fr))`) that automatically arranges event cards into columns based on available screen width. | 10m |
| 4 | Design Event Cards | HTML/CSS | I will build reusable event card components featuring a title, a visual map placeholder, a detailed list of event information (Date, Cost, Location), and a prominent full-width "Join" button at the bottom. | 15m |
| **IV** | **Authentication (login.html)** | | | **45m** |
| 1 | Create Auth Page Structure | HTML | I will design a dedicated login page with a centered, rounded-corner card container on a light grey background to focus user attention on the form. | 5m |
| 2 | Build Toggle Logic | JavaScript | I will implement a JavaScript function (`showForm()`) that toggles the `.hidden` class on the Login and Signup forms based on user selection, ensuring only one form is visible at a time. | 15m |
| 3 | Design Input Fields | CSS | I will style all form inputs with consistent padding, border radius, and a focus state that highlights the border in the brand's primary blue color to improve accessibility and user experience. | 10m |
| 4 | Refine Button Interactions | CSS | I will style the primary "Log In" and "Sign Up" buttons to span the full width of the form container, adding a hover effect that slightly lifts the button and deeper shadow for tactile feedback. | 15m |
| **V** | **Information Pages (about.html)** | | | **30m** |
| 1 | Create Content Layout | HTML/CSS | I will design a specialized layout for text-heavy content using a narrow, centered column (`max-width: 800px`) to improve readability for the Mission Statement and Privacy Policy. | 5m |
| 2 | Implement Privacy Policy | HTML | I will insert the full, legally-worded Privacy Policy text, utilizing semantic HTML (`<h3>`, `<ul>`, `<li>`) and specific CSS classes to style the lists and headers distinctly from standard text. | 15m |
| 3 | Add Navigation & Footer | HTML | I will ensure the global navigation bar is present and active states are correctly set, and add a footer with a quick link to the privacy policy section for easy access from any page. | 10m |
| **VI** | **Feature Logic (create-event.html)** | | | **35m** |
| 1 | Build Event Creation Form | HTML | I will create a comprehensive form with specific input types for each data point: text for Title/Location, `datetime-local` for Date, number for Cost, and file input for Images. | 15m |
| 2 | Style Form Components | CSS | I will reuse the robust form styling from the Login page to ensure visual consistency across the application, specifically styling the file input and textarea for better usability. | 10m |
| 3 | Implement Navigation Logic | HTML | I will add a "Cancel" link next to the submit button that safely redirects the user back to the main Events listing page without submitting data. | 5m |
| 4 | Link to Navigation | HTML | I will update the "Create Event" button on the Events page header and the specific "Create an event" button on the Homepage to point to this new form. | 5m |
| **VII** | **Global Refinement & Polish** | | | **30m** |
| 1 | Unify Navigation Links | All Pages | I will review every HTML file to ensure the navigation bar links (Home, Events, Login, About) point to the correct relative paths and that the "Home" text link is removed in favor of the clickable logo. | 10m |
| 2 | Polish Logo Styling | CSS | I will write specific CSS rules for `a.logo` to override default link styles, forcing the text to be white and removing the underline decoration in all states (visited, hover, active). | 10m |
| 3 | Final Consistency Check | Browser | I will verify that common elements like the header, footer, and buttons look and behave identically across all pages, ensuring a seamless user experience. | 10m |