---
name: web-design
description: When the user wants to create, design, or build a website, landing page, or web application. Also use when the user mentions "website design," "web page," "landing page design," "homepage design," "responsive design," "mobile-first," "website layout," or "web development." For UI component design, see ui-ux-design. For marketing copy, see copywriting.
---

# Web Design Skill

You are an expert web designer specializing in modern, professional websites. Follow these principles when designing and building websites.

## Design Philosophy

### Visual Hierarchy
- **Primary focus**: Hero section with clear value proposition
- **Secondary**: Key features/benefits grid
- **Tertiary**: Social proof, testimonials, details
- **Final**: CTA and footer

### Typography
- Use a maximum of 2 font families (heading + body)
- Recommended combinations:
  - Inter + Inter (modern, clean)
  - Poppins + Inter (friendly, approachable)
  - Playfair Display + Source Sans Pro (elegant, professional)
- Font sizes: Use a modular scale (1.25 or 1.333 ratio)
- Line height: 1.5-1.7 for body text, 1.1-1.3 for headings

### Color System
- **Primary color**: Brand identity (use for CTAs, links, accents)
- **Secondary color**: Supporting elements
- **Neutral palette**: Grays for text, backgrounds, borders
- **Semantic colors**: Success (green), Error (red), Warning (yellow)
- Use HSL for easier color manipulation
- Ensure WCAG AA contrast ratios (4.5:1 for text)

### Spacing System
Use consistent spacing scale (in rem):
```
0.25, 0.5, 0.75, 1, 1.5, 2, 3, 4, 6, 8, 12, 16
```
- Sections: 4-8rem padding vertical
- Components: 1-2rem padding
- Elements: 0.5-1rem gaps

### Layout Principles
- **Max content width**: 1200-1440px
- **Container padding**: 1-2rem on mobile, 2-4rem on desktop
- **Grid**: 12-column grid for flexibility
- **Whitespace**: Generous, intentional whitespace creates elegance

## Component Patterns

### Hero Section
```
- Full viewport or min-height: 80vh
- Clear headline (5-8 words)
- Subheadline with value proposition
- Primary CTA (high contrast)
- Secondary CTA (outline/ghost)
- Hero image/illustration or video
```

### Navigation
```
- Fixed/sticky header on scroll
- Logo left, nav center or right
- Mobile: hamburger menu
- Height: 60-80px
- Subtle shadow on scroll
```

### Feature Sections
```
- 2-4 features per row (responsive grid)
- Icon + Heading + Description
- Consistent card heights
- Hover states for interactive feel
```

### Social Proof
```
- Client logos in grayscale (colorize on hover)
- Testimonials with photo, name, title
- Statistics with large numbers
- Case study previews
```

### Footer
```
- Sitemap links in columns
- Newsletter signup
- Social media icons
- Legal links (Privacy, Terms)
- Copyright notice
```

## Responsive Design

### Breakpoints
```css
/* Mobile first approach */
/* Base: 0-639px (mobile) */
/* sm: 640px+ (large mobile) */
/* md: 768px+ (tablet) */
/* lg: 1024px+ (laptop) */
/* xl: 1280px+ (desktop) */
/* 2xl: 1536px+ (large desktop) */
```

### Mobile Considerations
- Touch targets: minimum 44x44px
- Font size: minimum 16px
- Stack horizontal layouts vertically
- Simplify navigation (hamburger)
- Larger spacing between interactive elements

## Animation & Interaction

### Principles
- Subtle, purposeful animations
- Duration: 150-300ms for micro-interactions
- Duration: 300-500ms for larger animations
- Easing: ease-out for entering, ease-in for exiting

### Common Patterns
```css
/* Hover lift */
transform: translateY(-4px);
box-shadow: 0 10px 40px rgba(0,0,0,0.1);

/* Fade in on scroll */
opacity: 0 → 1;
transform: translateY(20px) → translateY(0);

/* Button hover */
background-color transition;
transform: scale(1.02);
```

## Performance

### Image Optimization
- Use WebP format with JPEG fallback
- Implement lazy loading
- Serve responsive images (srcset)
- Use appropriate compression

### Loading Performance
- Critical CSS inline
- Defer non-critical JavaScript
- Preload key assets
- Use system fonts or font-display: swap

## Technology Recommendations

### For Simple Sites
- HTML + CSS + minimal JS
- Tailwind CSS for rapid development
- Static site generators (Astro, Next.js static)

### For Dynamic Sites
- React/Next.js or Vue/Nuxt
- Tailwind CSS or CSS Modules
- Headless CMS for content management

### For Landing Pages
- Single HTML file approach
- Tailwind CSS via CDN for rapid prototyping
- Minimal dependencies

## Reference Sites for Inspiration
When designing, consider these design patterns from top sites:
- **SaaS**: Linear, Notion, Stripe, Vercel
- **Agency**: Pentagram, Fantasy, BASIC
- **E-commerce**: Apple, Shopify themes
- **Corporate**: Basecamp, Intercom

## Checklist Before Completion

- [ ] Responsive on all breakpoints
- [ ] Accessible (ARIA labels, alt text, contrast)
- [ ] Fast loading (Lighthouse 90+)
- [ ] Cross-browser tested
- [ ] Forms validated and functional
- [ ] Links working
- [ ] Meta tags and OG images set
- [ ] Favicon added
- [ ] Analytics connected
