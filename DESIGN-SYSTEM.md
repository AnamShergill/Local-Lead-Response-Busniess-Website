# Local Lead Response - Unified Design System

## Overview
This document outlines the comprehensive design system applied to ensure absolute visual consistency across all sections of the website.

---

## 1. Typography System

### Font Families
- **Display/Headlines**: Sora (600-800 weight)
- **Body/UI Text**: Inter (400-600 weight)

### Type Scale (Consistent Across All Sections)
```
Display Large:    64px / 1.1 line-height / -0.02em letter-spacing
Headline XL:      48px / 1.2 line-height / 700 weight
Headline Large:   32px / 1.3 line-height / 600 weight
Headline Mobile:  24px / 1.3 line-height / 600 weight
Body Large:       18px / 1.6 line-height / 400 weight
Body Medium:      16px / 1.6 line-height / 400 weight
Label Bold:       14px / 1.2 line-height / 600 weight / 0.05em spacing
```

### Usage Guidelines
- **Section Titles**: Headline XL (48px) on desktop, Headline Large (32px) on mobile
- **Card Titles**: Headline Large (32px) or Headline Mobile (24px)
- **Body Text**: Body Large (18px) for important content, Body Medium (16px) for secondary
- **Labels/Tags**: Label Bold (14px) with uppercase and letter-spacing

---

## 2. Spacing System

### Consistent Spacing Scale
```css
--spacing-xs:   8px    (icon padding, micro spacing)
--spacing-sm:   12px   (tight spacing, small gaps)
--spacing-md:   24px   (standard spacing, card padding)
--spacing-lg:   48px   (section spacing, large gaps)
--spacing-xl:   64px   (major section breaks)
--spacing-2xl:  100px  (section padding top/bottom)
```

### Application
- **Section Padding**: 100px (desktop) / 64px (mobile) top and bottom
- **Container Max Width**: 1280px (7xl)
- **Gutter**: 24px horizontal padding
- **Card Padding**: 24px-32px depending on card size
- **Element Gaps**: 12px (tight), 24px (standard), 48px (loose)

---

## 3. Color Palette (Unified Theme)

### Primary Colors
- **Primary Blue**: #b4c5fc (text, accents, icons)
- **Secondary Orange**: #ff7a00 (CTAs, highlights, active states)
- **Background**: #061B49 (deep navy)

### Surface Colors
- **Surface Container**: #1d2022
- **Surface Dim**: #101415
- **Surface Bright**: #363a3b

### Text Colors
- **On Surface**: #e0e3e5 (primary text - white)
- **On Surface Variant**: #c5c6d0 (secondary text - gray)
- **Error**: #ffb4ab
- **Tertiary**: #adc6ff

### Semantic Usage
- **Headings**: Always white (#e0e3e5)
- **Body Text**: On Surface Variant (#c5c6d0)
- **CTAs**: Secondary Orange (#ff7a00)
- **Links/Hover**: Secondary Orange (#ff7a00)
- **Icons**: Primary Blue or Secondary Orange based on context

---

## 4. Border Radius System

### Consistent Radius Scale
```css
--radius-sm:   12px   (small elements, tags)
--radius-md:   16px   (buttons, small cards)
--radius-lg:   24px   (medium cards)
--radius-xl:   32px   (large cards)
--radius-2xl:  40px   (feature cards)
--radius-3xl:  48px   (hero elements, major sections)
--radius-full: 9999px (pills, buttons)
```

### Application
- **Buttons**: Full radius (pill shape)
- **Cards**: 24px-40px depending on size
- **Icons Containers**: 12px-16px
- **Hero Elements**: 48px (3xl)

---

## 5. Glass Morphism System

### Three Variants
```css
.glass-card (Standard)
- Background: rgba(255, 255, 255, 0.05)
- Backdrop Filter: blur(20px)
- Border: 1px solid rgba(255, 255, 255, 0.15)

.glass-card-strong (Emphasized)
- Background: rgba(255, 255, 255, 0.08)
- Backdrop Filter: blur(24px)
- Border: 1px solid rgba(255, 255, 255, 0.2)

.glass-card-subtle (Minimal)
- Background: rgba(255, 255, 255, 0.03)
- Backdrop Filter: blur(16px)
- Border: 1px solid rgba(255, 255, 255, 0.1)
```

### Usage
- **Header**: Strong variant for maximum visibility
- **Feature Cards**: Standard variant
- **Background Elements**: Subtle variant

---

## 6. Glow Effects System

### Orange Glow (CTAs, Secondary Actions)
```css
Standard: 0 0 20px rgba(255, 122, 0, 0.4)
Strong:   0 0 30px rgba(255, 122, 0, 0.5)
```

### Blue Glow (Primary Elements, Header)
```css
Standard: 0 0 40px rgba(58, 134, 255, 0.3)
Strong:   0 0 50px rgba(58, 134, 255, 0.4)
```

### Application
- **Header**: Blue glow (enhanced visibility)
- **CTA Buttons**: Orange glow
- **Hover States**: Intensified glow

---

## 7. Animation & Transitions

### Timing Functions
```css
--transition-fast: 200ms ease   (micro interactions)
--transition-base: 300ms ease   (standard interactions)
--transition-slow: 600ms ease-out (scroll reveals, major animations)
```

### Scroll Reveal Pattern
- **Opacity**: 0 → 1
- **Transform**: translateY(30px) → translateY(0)
- **Duration**: 600ms ease-out
- **Stagger**: 100ms delay between elements

### Hover Effects
- **Cards**: translateY(-8px) + enhanced shadow
- **Buttons**: scale(1.05) + brightness(1.1)
- **Links**: Underline animation (width: 0 → 100%)

---

## 8. Enhanced Header Design

### Visibility Improvements
- **Background**: rgba(6, 27, 73, 0.85) - More opaque
- **Backdrop Blur**: 24px (increased from 20px)
- **Border**: Primary blue with 0.25 opacity
- **Shadow**: Dual-layer blue glow + depth shadow
- **Hover State**: Increased opacity and glow intensity

### Typography
- **Logo**: 24px (desktop) / 20px (mobile), bold weight
- **Nav Links**: 16px, medium weight, white color
- **Underline Animation**: Bottom border on hover

---

## 9. Section Consistency

### Standard Section Structure
```html
<section class="py-24 px-4 md:px-6 max-w-7xl mx-auto">
  <div class="text-center mb-12">
    <span class="section-label">CATEGORY</span>
    <h2 class="section-title">Main Heading</h2>
    <p class="section-subtitle">Supporting text</p>
  </div>
  <!-- Content -->
</section>
```

### Padding Pattern
- **Vertical**: 100px (desktop) / 64px (mobile)
- **Horizontal**: 24px (gutter)
- **Max Width**: 1280px (7xl container)

---

## 10. Button System

### Primary Button (CTA)
- **Background**: #ff7a00 (secondary orange)
- **Padding**: 16px 32px
- **Border Radius**: Full (pill)
- **Font**: Label Bold (14px, 600 weight)
- **Glow**: Orange shadow
- **Hover**: scale(1.05) + brightness(1.1)

### Secondary Button (Ghost)
- **Background**: Glass card effect
- **Border**: 1px solid rgba(255, 255, 255, 0.15)
- **Padding**: 16px 32px
- **Hover**: Increased background opacity

---

## 11. Card System

### Standard Card Pattern
```css
.glass-card + .card-hover
- Padding: 24px-32px
- Border Radius: 24px-40px
- Hover: translateY(-8px)
- Shadow: Enhanced on hover
```

### Icon Container Pattern
- **Size**: 56px × 56px (14 × 14 in Tailwind)
- **Border Radius**: 12px-16px
- **Background**: Color/30 opacity
- **Icon Size**: 32px-40px

---

## 12. Responsive Breakpoints

### Mobile First Approach
```css
Mobile:  < 768px  (base styles)
Tablet:  768px+   (md: prefix)
Desktop: 1024px+  (lg: prefix)
Wide:    1280px+  (xl: prefix)
```

### Adjustments
- **Typography**: Reduce by 25-40% on mobile
- **Spacing**: Reduce section padding to 64px
- **Grid**: Stack to single column
- **Header**: Reduce padding and font sizes

---

## 13. Accessibility

### Focus States
- **Outline**: 2px solid #b4c5fc
- **Offset**: 4px
- **Border Radius**: 4px

### Motion Preferences
- **Reduced Motion**: All animations set to 0.01ms
- **Keyboard Navigation**: Clear focus indicators
- **Color Contrast**: WCAG AA compliant

---

## Implementation Checklist

✅ Unified typography scale across all sections
✅ Consistent spacing system (8px base)
✅ Standardized color palette usage
✅ Unified border radius scale
✅ Glass morphism system with variants
✅ Glow effects system (orange/blue)
✅ Enhanced header visibility
✅ Consistent animation timing
✅ Standardized card patterns
✅ Responsive design tokens
✅ Accessibility features

---

## Usage Guidelines

1. **Always use design tokens** from the CSS variables
2. **Maintain spacing rhythm** using the 8px base scale
3. **Apply consistent typography** - no random font sizes
4. **Use semantic colors** - primary for navigation, secondary for CTAs
5. **Follow the card pattern** - glass effect + hover animation
6. **Respect the animation system** - consistent timing functions
7. **Test responsiveness** - mobile-first approach
8. **Ensure accessibility** - focus states and reduced motion support

---

Last Updated: 2026-05-13
Version: 1.0
