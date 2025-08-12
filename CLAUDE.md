# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a static HTML website for Solastaa, an engineering company specializing in Telecom, Power, and Infrastructure solutions. The site consists of 5 main pages showcasing company services, projects, and contact information.

## Architecture
The website follows a traditional multi-page static HTML structure:
- **HTML Pages**: index.html (home), about.html, services.html, projects.html, contact.html
- **Styling**: Single CSS file at css/style.css using CSS custom properties for theming
- **JavaScript**: Minimal JS in js/main.js for mobile menu toggle and smooth scrolling
- **Assets**: Images stored in images/ directory with subdirectories for building photos

## Development Guidelines

### CSS Structure
- Uses CSS custom properties defined in :root for consistent theming
- Primary colors: --primary-color (#1976D2), --secondary-color (#2E7D32)
- Responsive design with mobile breakpoint at 768px
- BEM-like naming convention for components (e.g., .service-card, .hero-section)

### HTML Patterns
- Each page uses the same header/navigation and footer structure
- Navigation includes dropdown menus for Services and Projects
- Active page indicated via .active class on nav items
- Sections use alternating backgrounds (.light-bg, .dark-bg, .alternate-bg)

### JavaScript Functionality
- Mobile menu toggle for responsive navigation
- Smooth scrolling for anchor links
- Header scroll effect (adds .scrolled class when scrollY > 100)

## Common Tasks

### Adding a New Page
1. Create new HTML file following existing page structure
2. Include standard header with navigation (copy from existing pages)
3. Add .active class to appropriate nav item
4. Include footer section
5. Link to css/style.css and js/main.js

### Modifying Navigation
- Update nav menu in ALL HTML files (index.html, about.html, services.html, projects.html, contact.html)
- Dropdown menus use nested ul.dropdown-menu structure

### Adding New Services or Projects
- Services are displayed as cards in .services-grid
- Projects use .project-card within .projects-grid
- Follow existing HTML structure and class naming patterns

## Testing
This is a static website with no build process. To test:
- Open HTML files directly in a browser
- Check responsive design at mobile breakpoint (768px)
- Verify navigation dropdowns and mobile menu functionality
- Test smooth scrolling on anchor links