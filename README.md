# ddsttraining

A static web portfolio site that includes a Home Page, an About Page, and a Contact Page. 

The Contact Page includes a contact form with Javascript validation.

## DOM and Event Listeners Explanation

### HTML Structure Overview

The portfolio website uses semantic HTML5 elements with a clear hierarchy:

```
html
├── head (meta tags, stylesheets, fonts)
├── body
    ├── header (navigation)
    ├── main (content sections)
    └── footer (contact info, social links)
```

### Key DOM Elements

#### 1. Navigation Elements
- **`.header`** - Fixed header container with backdrop blur
- **`.navbar`** - Navigation wrapper
- **`.nav-container`** - Flex container for logo and menu
- **`.nav-logo`** - Brand logo/initials
- **`.nav-menu`** - Unordered list of navigation links
- **`.nav-item`** - Individual navigation list items
- **`.nav-link`** - Navigation anchor links
- **`.hamburger`** - Mobile menu toggle button
- **`.bar`** - Hamburger menu lines (3 spans)

#### 2. Hero Section Elements
- **`.hero`** - Full-height hero section with gradient background
- **`.hero-container`** - Grid container for content and image
- **`.hero-content`** - Text content wrapper
- **`.hero-title`** - Main heading with typing animation
- **`.highlight`** - Highlighted name span
- **`.hero-subtitle`** - Professional title
- **`.hero-description`** - Introduction paragraph
- **`.hero-buttons`** - Call-to-action buttons container
- **`.hero-image`** - Profile card container
- **`.profile-card`** - Glassmorphism profile card
- **`.profile-avatar`** - Circular avatar with icon
- **`.profile-info`** - Name and title info

#### 3. Skills Section Elements
- **`.skills`** - Skills section with light background
- **`.container`** - Content wrapper
- **`.section-title`** - Section headings
- **`.skills-grid`** - CSS Grid for skill cards
- **`.skill-card`** - Individual skill cards with hover effects
- **`.skill-icon`** - Circular icon containers
- **`.skill-card h3`** - Skill category titles
- **`.skill-card p`** - Skill descriptions

#### 4. Projects Section Elements
- **`.featured-projects`** - Projects showcase section
- **`.projects-grid`** - CSS Grid for project cards
- **`.project-card`** - Individual project cards
- **`.project-image`** - Project image container
- **`.project-placeholder`** - Icon placeholder for images
- **`.project-content`** - Project information wrapper
- **`.project-content h3`** - Project titles
- **`.project-content p`** - Project descriptions
- **`.project-tags`** - Technology tags container
- **`.tag`** - Individual technology tags

#### 5. Call-to-Action Elements
- **`.cta`** - Call-to-action section with gradient
- **`.cta-content`** - CTA text wrapper
- **`.cta-content h2`** - CTA heading
- **`.cta-content p`** - CTA description

#### 6. Footer Elements
- **`.footer`** - Footer section with dark background
- **`.footer-content`** - Footer content grid
- **`.footer-section`** - Individual footer sections
- **`.social-links`** - Social media links container
- **`.social-link`** - Individual social media links
- **`.footer-bottom`** - Copyright section

#### 7. Button Elements
- **`.btn`** - Base button styles
- **`.btn-primary`** - Primary action buttons (yellow)
- **`.btn-secondary`** - Secondary action buttons (outlined)

### Event Listeners and JavaScript Functionality

#### 1. Mobile Navigation Toggle
```javascript
// Elements: .hamburger, .nav-menu
// Event: click
// Function: Toggle mobile menu visibility
```

#### 2. Navigation Link Click Handlers
```javascript
// Elements: .nav-link
// Event: click
// Function: Close mobile menu when links are clicked
```

#### 3. Smooth Scrolling
```javascript
// Elements: a[href^="#"] (anchor links)
// Event: click
// Function: Smooth scroll to target sections
```

#### 4. Active Navigation Highlighting
```javascript
// Elements: section, .nav-link
// Event: scroll
// Function: Highlight current section in navigation
```

#### 5. Intersection Observer Animations
```javascript
// Elements: .skill-card, .project-card
// Event: intersection
// Function: Animate elements when they come into view
```

#### 6. Form Validation (Contact Page)
```javascript
// Elements: #contact-form, form inputs
// Events: submit, input validation
// Functions: 
// - Validate form fields
// - Show/hide error messages
// - Handle form submission
```

#### 7. Typing Animation
```javascript
// Elements: .hero-title
// Event: DOMContentLoaded
// Function: Typewriter effect for hero title
```

#### 8. Parallax Effect
```javascript
// Elements: .hero
// Event: scroll
// Function: Parallax scrolling effect
```

#### 9. Loading Animation
```javascript
// Elements: body
// Event: load
// Function: Add loaded class for animations
```

#### 10. Scroll Reveal
```javascript
// Elements: .reveal
// Event: scroll
// Function: Reveal elements on scroll
```

### CSS Classes and Styling

#### Layout Classes
- **`.container`** - Max-width wrapper with padding
- **`.grid`** - CSS Grid layouts
- **`.flex`** - Flexbox layouts

#### State Classes
- **`.active`** - Active navigation states
- **`.error`** - Form validation error states
- **`.loaded`** - Page load completion state

#### Animation Classes
- **`.fadeInUp`** - Fade in from bottom animation
- **`.reveal`** - Scroll-triggered reveal animation

### Responsive Design Elements

#### Mobile Navigation
- **`.hamburger.active`** - Mobile menu open state
- **`.nav-menu.active`** - Mobile menu visible state

#### Breakpoint Classes
- **`@media (max-width: 768px)`** - Tablet and mobile styles
- **`@media (max-width: 480px)`** - Small mobile styles

### Accessibility Features

#### Semantic Elements
- **`<header>`** - Site header
- **`<nav>`** - Navigation menu
- **`<main>`** - Main content area
- **`<section>`** - Content sections
- **`<footer>`** - Site footer

#### ARIA Attributes
- **`lang="en"`** - Language declaration
- **`role`** attributes for interactive elements
- **`aria-label`** for screen readers

### Performance Optimizations

#### Event Delegation
- Navigation link handlers use event delegation
- Form validation uses efficient selectors

#### Intersection Observer
- Efficient scroll-based animations
- Reduces layout thrashing

#### CSS Transitions
- Hardware-accelerated animations
- Smooth hover effects and state changes
