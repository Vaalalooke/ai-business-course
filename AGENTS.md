# AI Business Course - Agent Guidelines

This repository contains a simple HTML-based educational resource website for AI business applications. This document provides guidance for AI agents working on this codebase.

## Project Overview

- **Type**: Static HTML website with embedded CSS and JavaScript
- **Purpose**: Educational resource hub showcasing AI applications in business
- **Structure**: Single-page application with all styles and scripts embedded
- **Deployment**: Can be served statically from any web server

## Build Commands

Since this is a static HTML site with no build process:

```bash
# No build step required - files are ready to serve
# To run locally:
python3 -m http.server 8000
# or
npx serve .
```

## Testing Commands

```bash
# No formal test suite exists
# Manual testing approach:
# 1. Open index.html in browser
# 2. Validate all external links load correctly
# 3. Check responsive design on different screen sizes
# 4. Test JavaScript functionality (click tracking, greeting message)
```

## Linting and Formatting

No linting configuration exists. Recommended tools if adding:

```bash
# HTML validation:
npx html-validate index.html

# CSS formatting (if extracted):
npx prettier --write *.css

# JavaScript formatting (if extracted):
npx prettier --write *.js
npx eslint *.js
```

## Code Style Guidelines

### HTML Structure
- Use semantic HTML5 elements
- Keep embedded CSS in `<style>` tags within `<head>`
- Keep embedded JavaScript at end of `<body>`
- Maintain consistent indentation (2 spaces)
- Use lowercase for all tag names and attributes
- Close all tags properly

### CSS Conventions
- Use kebab-case for class names
- Follow BEM methodology for component naming: `.block__element--modifier`
- Organize styles logically: general → specific → utilities
- Use px units for consistent sizing
- Follow mobile-first responsive design
- Include hover states for interactive elements

### JavaScript Standards
- Use modern ES6+ syntax
- Implement event delegation for dynamic content
- Use const/let appropriately
- Include descriptive variable names in camelCase
- Add comments for complex logic
- Handle errors gracefully
- Use template literals for string concatenation

### File Organization
- Keep everything in index.html for this simple project
- If expanding, consider splitting into:
  - `css/styles.css`
  - `js/main.js`
  - `assets/images/`

## Naming Conventions

### HTML
- IDs: kebab-case (`#resource-section`)
- Classes: kebab-case (`.resource-list`)
- Data attributes: kebab-case (`data-resource-type`)

### CSS
- Classes: BEM methodology (`.resource-section__title--highlighted`)
- Variables: kebab-case with prefix (`--primary-color`)

### JavaScript
- Variables: camelCase (`resourceUrl`)
- Functions: camelCase with descriptive verbs (`handleResourceClick`)
- Constants: UPPER_SNAKE_CASE (`API_BASE_URL`)
- Events: kebab-case (`resource:clicked`)

## Error Handling

- Wrap async operations in try-catch blocks
- Provide user-friendly error messages
- Log errors to console for debugging
- Gracefully handle missing elements
- Validate user inputs before processing

## Performance Guidelines

- Optimize images for web (WebP format preferred)
- Minimize external dependencies
- Use semantic HTML for better SEO
- Implement lazy loading for large content sections
- Consider CDN for external resources

## Security Best Practices

- Validate all external links
- Use HTTPS for all resources
- Sanitize user inputs
- Avoid inline event handlers in production
- Implement CSP headers if deploying to production

## Content Guidelines

- Keep resource descriptions concise but informative
- Ensure all external links are current and relevant
- Focus on African AI initiatives where possible
- Maintain professional, educational tone
- Update content regularly to stay current

## Git Workflow

- Use descriptive commit messages
- Create feature branches for significant changes
- Tag releases for major content updates
- Keep git history clean and meaningful

## Browser Compatibility

- Target modern browsers (Chrome 90+, Firefox 88+, Safari 14+)
- Provide fallbacks for older browsers if necessary
- Test on mobile devices thoroughly
- Ensure accessibility standards are met

## Adding New Resources

1. Add to appropriate section in HTML
2. Include descriptive text and working URL
3. Test link validity
4. Consider adding click tracking if needed
5. Update any relevant documentation

## Deploying

- Can be deployed to any static hosting service
- Ensure base URL is correctly configured
- Test all links in production environment
- Monitor for broken links regularly