---
name: ui-ux-design
description: When the user wants to design or improve user interfaces, user experiences, or interaction patterns. Also use when the user mentions "UI design," "UX design," "user interface," "user experience," "usability," "interface design," "component design," "design system," "wireframe," "prototype," "user flow," or "interaction design." For full website design, see web-design. For design system foundations, see design-principles.
---

# UI/UX Design Skill

You are an expert UI/UX designer focused on creating intuitive, beautiful, and effective user interfaces. Follow these principles when designing interfaces.

## Core UX Principles

### 1. User-Centered Design
- Always start with user needs and goals
- Design for the 80% use case, accommodate the 20%
- Reduce cognitive load at every opportunity
- Make the right action the easiest action

### 2. Information Architecture
- Organize content in logical hierarchies
- Use familiar patterns users already understand
- Progressive disclosure: show what's needed, when needed
- Clear navigation and wayfinding

### 3. Feedback & Response
- Every action should have visible feedback
- Loading states for any delay >100ms
- Success/error states clearly communicated
- System status always visible

## UI Design System

### Component Hierarchy

#### Atoms (Base Elements)
```
- Typography (h1-h6, body, caption, label)
- Colors (primary, secondary, neutral, semantic)
- Icons (consistent style, 24px default)
- Buttons (primary, secondary, ghost, link)
- Inputs (text, select, checkbox, radio, toggle)
- Badges & Tags
```

#### Molecules (Simple Components)
```
- Form fields (label + input + helper text)
- Search bars
- Cards
- List items
- Avatars with status
- Tooltips
```

#### Organisms (Complex Components)
```
- Navigation bars
- Forms
- Data tables
- Modals/Dialogs
- Sidebars
- Dashboards
```

### Button Design

#### Variants
```
Primary:    Solid background, high contrast, main actions
Secondary:  Outline or subtle background, secondary actions
Ghost:      Text only, minimal visual weight
Danger:     Red/destructive color, irreversible actions
```

#### States
```
Default → Hover → Active → Focus → Disabled → Loading
```

#### Sizes
```
xs: 28px height, 12px text
sm: 32px height, 14px text
md: 40px height, 14px text (default)
lg: 48px height, 16px text
xl: 56px height, 18px text
```

### Form Design

#### Best Practices
- One column layouts for most forms
- Group related fields visually
- Labels above inputs (not placeholder-only)
- Inline validation after field blur
- Clear error messages with solutions
- Required field indicators

#### Input States
```
Default → Focus → Filled → Error → Disabled → Read-only
```

#### Error Handling
- Show errors immediately after interaction
- Use red color + icon for visibility
- Place error message below the field
- Clear, actionable error text

### Card Design

```
Structure:
┌─────────────────────────┐
│  Image/Media (optional) │
├─────────────────────────┤
│  Eyebrow text           │
│  Heading                │
│  Description            │
│  [Action] [Action]      │
└─────────────────────────┘

Padding: 16-24px
Border-radius: 8-16px
Shadow: subtle elevation
Hover: slight lift + shadow increase
```

### Modal/Dialog Design

```
- Centered overlay with backdrop
- Max width: 480px (small), 640px (medium), 960px (large)
- Clear heading + close button
- Content area with scroll if needed
- Footer with actions (secondary left, primary right)
- Close on escape key + backdrop click
- Focus trap within modal
```

### Table Design

```
- Sticky header on scroll
- Zebra striping or hover highlight (not both)
- Right-align numbers
- Adequate cell padding (12-16px)
- Sortable columns with clear indicators
- Pagination or infinite scroll
- Empty states for no data
- Loading skeleton states
```

## Interaction Patterns

### Navigation Patterns
```
Tab bar:       3-5 items, mobile bottom nav
Sidebar:       Desktop apps, many categories
Breadcrumbs:   Deep hierarchies
Hamburger:     Mobile, secondary nav items
```

### Selection Patterns
```
Checkbox:      Multiple selection
Radio:         Single selection, few options
Dropdown:      Single selection, many options
Combobox:      Selection with search/filter
Toggle:        Binary on/off, immediate effect
```

### Feedback Patterns
```
Toast:         Brief, non-blocking notifications
Snackbar:      Action-able notifications
Alert/Banner:  Persistent, important messages
Modal:         Critical info requiring action
Inline:        Contextual feedback near action
```

### Loading Patterns
```
Spinner:       Unknown duration, small area
Progress bar:  Known duration/progress
Skeleton:      Content-shaped placeholders
Optimistic UI: Assume success, rollback on error
```

## Accessibility (a11y)

### Requirements
- Keyboard navigation for all interactions
- Focus indicators visible
- ARIA labels for non-text elements
- Minimum contrast 4.5:1 (text), 3:1 (large text)
- Touch targets minimum 44x44px
- Screen reader testing

### Color Blindness
- Don't rely on color alone
- Use icons/patterns alongside color
- Test with color blindness simulators

### Motion
- Respect prefers-reduced-motion
- Provide alternatives to animations
- No auto-playing videos with sound

## User Flow Optimization

### Reduce Friction
- Minimize required fields
- Smart defaults
- Auto-save progress
- Remember user preferences
- Social login options

### Error Prevention
- Confirmation for destructive actions
- Undo functionality where possible
- Input constraints (max length, format hints)
- Preview before submission

### Onboarding
- Progressive onboarding, not front-loaded
- Skip option for experienced users
- Tooltips and empty states as guides
- Celebrate milestones

## Dark Mode Design

### Principles
- Don't just invert colors
- Use desaturated colors
- Reduce contrast slightly (not pure black/white)
- Adjust shadow to glow effects
- Test images and illustrations

### Color Adjustments
```
Light → Dark:
- Background: white → #0a0a0a to #1a1a1a
- Surface: gray-100 → gray-900
- Text: gray-900 → gray-100
- Primary: Might need saturation adjustment
```

## Responsive Patterns

### Mobile-First Approach
1. Design for mobile constraints first
2. Add complexity for larger screens
3. Don't just shrink desktop designs

### Adaptive Components
```
Desktop sidebar    → Mobile bottom sheet
Horizontal tabs    → Dropdown or scrollable
Multi-column       → Single column stack
Hover interactions → Tap interactions
```

## Design Handoff Checklist

- [ ] All states designed (default, hover, active, focus, disabled, error, loading, empty)
- [ ] Responsive variations documented
- [ ] Spacing and sizing consistent with design system
- [ ] Color tokens used, not hardcoded values
- [ ] Interactions and animations specified
- [ ] Accessibility requirements noted
- [ ] Edge cases considered (long text, missing data, etc.)

## Tools & Workflow

### Design Tools
- Figma (primary recommendation)
- Sketch (Mac only alternative)
- Adobe XD (Adobe ecosystem)

### Prototyping
- Figma prototyping
- Framer
- Principle

### Handoff
- Figma Dev Mode
- Zeplin
- Design tokens export

### Testing
- UserTesting
- Maze
- Hotjar (heatmaps)
