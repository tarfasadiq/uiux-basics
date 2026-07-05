# Cards & Grids Fundamentals

Cards and grids are fundamental layout patterns. They organize content into scannable, digestible pieces. Master them and you'll solve most layout challenges.

## 📚 Table of Contents

1. [What are Cards](#what-are-cards)
2. [Card Design](#card-design)
3. [Grid Systems](#grid-systems)
4. [Card Layouts](#card-layouts)
5. [Responsive Design](#responsive-design)
6. [Practical Exercises](#practical-exercises)

## What are Cards

### Card Definition

A card is a container for related content with:
- Clear boundaries (usually border or shadow)
- Contained information
- Possible action(s)
- Visual consistency

### Why Cards Work

✅ **Scannable** - Easy to quickly understand
✅ **Modular** - Reusable, flexible
✅ **Mobile-friendly** - Stack easily
✅ **Information hierarchy** - Organize complexity
✅ **Visual interest** - Breaking up walls of text
✅ **Flexible layout** - Works in any grid

### Card Use Cases

- **Products**: E-commerce, marketplace
- **People**: Team members, user profiles
- **Content**: Blog posts, articles, news
- **Data**: Analytics, stats, metrics
- **Invites**: Event cards, CTAs
- **Settings**: Feature toggles, preferences

## Card Design

### Card Anatomy

```
┌─────────────────────────────┐
│ [Image / Icon]              │ ← Media (optional)
├─────────────────────────────┤
│ Card Title                  │ ← Headline
│                             │
│ Brief description or        │ ← Body text
│ summary of content          │
│                             │
│ [Primary Action] [Link]     │ ← Actions
└─────────────────────────────┘
```

### Card Components

**1. Media**
- Image, icon, or video
- Visual hook
- Aspect ratio: 16:9 common
- Optional but recommended

**2. Header**
- Title/headline
- Clear, concise
- Scannable
- Usually 1-2 lines

**3. Content**
- Body text, summary
- Keep brief (2-3 lines)
- Truncate with "..."
- Readable font size

**4. Footer/Actions**
- Primary action (button)
- Secondary action (link)
- Metadata (date, author)
- Status indicators

### Card Spacing

```
┌─────────────────────┐
│     Padding 16px    │ ← Outside edge
│  ┌───────────────┐  │
│  │               │  │ ← Media area
│  └───────────────┘  │
│   16px gap          │
│  Title              │
│  12px gap           │
│  Description text   │
│  truncated here...  │
│   16px gap          │
│  [Button]  [Link]   │
│                     │
└─────────────────────┘
```

### Card Variations

**Minimal Card**
```
┌──────────────┐
│  Title       │
│  [Action]    │
└──────────────┘
```

**Image Card**
```
┌──────────────┐
│ [Image]      │
│ Title        │
│ [Action]     │
└──────────────┘
```

**Product Card**
```
┌──────────────┐
│ [Image]      │
│ Title        │
│ $99.99       │
│ ★★★★☆       │
│ [Buy Now]    │
└──────────────┘
```

**Profile Card**
```
┌──────────────┐
│ [Avatar]     │
│ Name         │
│ @username    │
│ Bio text     │
│ [Follow]     │
└──────────────┘
```

## Grid Systems

### What is a Grid?

A grid is a structure of invisible lines organizing content layout.

### Grid Types

**Column Grid** (Most Common)
- Divides width into columns
- Usually 12 columns
- Content spans multiple columns

```
12-Column Grid:
1  2  3  4  5  6  7  8  9  10 11 12
│  │  │  │  │  │  │  │  │  │  │  │
└──────────────┘ └──────────────┘
  6 columns        6 columns
    (50%)            (50%)
```

**Row Grids**
- Create consistent height
- Good for cards
- Fixed aspect ratios

### Grid Breakpoints

```
Common Breakpoints:

Mobile:   < 768px  (1 column)
Tablet:   768-1024px (2 columns)
Desktop:  > 1024px  (3+ columns)

Or more specific:

XS: 320px
SM: 480px
MD: 768px
LG: 1024px
XL: 1440px
```

### Grid Calculations

```
Total width: 1200px
Number of columns: 12
Gutter (space between): 24px

Column width:
(1200 - (11 × 24)) / 12 = 88px

Card width for 4 columns:
(4 × 88) + (3 × 24) = 424px
```

## Card Layouts

### Single Column

**Use**: Mobile, simple layouts

```
┌─────────────┐
│   Card 1    │
└─────────────┘
┌─────────────┐
│   Card 2    │
└─────────────┘
┌─────────────┐
│   Card 3    │
└─────────────┘
```

### Two Column

**Use**: Tablets, moderate complexity

```
┌──────────┐ ┌──────────┐
│ Card 1   │ │ Card 2   │
└──────────┘ └──────────┘
┌──────────┐ ┌──────────┐
│ Card 3   │ │ Card 4   │
└──────────┘ └──────────┘
```

### Three Column

**Use**: Desktop, product layouts

```
┌────────┐ ┌────────┐ ┌────────┐
│ Card 1 │ │ Card 2 │ │ Card 3 │
└────────┘ └────────┘ └────────┘
┌────────┐ ┌────────┐ ┌────────┐
│ Card 4 │ │ Card 5 │ │ Card 6 │
└────────┘ └────────┘ └────────┘
```

### Four+ Column

**Use**: Large desktop, dashboards

```
Often 4-6 columns
Each card compact
Good for dashboards
```

### Masonry Layout

**Cards at different heights**

```
┌──────┐ ┌────────┐ ┌──────┐
│ Card │ │ Card   │ │ Card │
│ 1    │ │ 2      │ │ 3    │
│      │ │        │ │      │
│      │ └────────┘ │      │
│      │ ┌────────┐ │      │
└──────┘ │ Card 4 │ └──────┘
         │        │
         └────────┘
```

**Pros**: Fills space efficiently
**Cons**: Reading order confusing, complex code

## Responsive Design

### Breakpoint Strategy

**Mobile First**
```
Base: 1 column (mobile)
@768px: 2 columns (tablet)
@1024px: 3 columns (desktop)
```

**CSS Example**
```css
/* Mobile: 1 column */
.card-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 16px;
}

/* Tablet: 2 columns */
@media (min-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }
}

/* Desktop: 3 columns */
@media (min-width: 1024px) {
  .card-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
  }
}
```

### Card Sizing

**Don't**: Fixed width cards on mobile
```css
/* Bad: too small */
.card {
  width: 300px; /* Mobile gets crushed */
}
```

**Do**: Responsive sizing
```css
/* Good: scales with grid */
.card {
  width: 100%; /* Fills grid column */
}
```

### Image Aspect Ratio

```css
/* Maintain aspect ratio */
.card-image {
  aspect-ratio: 16 / 9;
  object-fit: cover;
  width: 100%;
}
```

## Practical Exercises

### Exercise 1: Card Design
1. Create 3 card types:
   - Product card
   - Article card
   - Profile card
2. Show all states (default, hover)
3. Include responsive sizing
4. Test on multiple devices

### Exercise 2: Grid Layout
1. Create grid system (12 columns)
2. Define 3 breakpoints
3. Design layout for each
4. Show card arrangements
5. Document gap/gutter values

### Exercise 3: Responsive Cards
1. Design card layout
2. Show mobile (1 col)
3. Show tablet (2 cols)
4. Show desktop (3+ cols)
5. Use CSS Grid

### Exercise 4: Card Variations
1. Design base card component
2. Create 5 variations
3. Show different content types
4. Document usage guidelines
5. Build in Figma

### Exercise 5: Grid Template
1. Create grid system document
2. Define columns and gutters
3. Show breakpoints
4. Include spacing guidelines
5. Show example layouts

## Key Takeaways

✅ **Cards organize content** - Clear, scannable chunks
✅ **Consistent spacing** - Padding, gaps, margins
✅ **Grid systems scale** - Work at all sizes
✅ **Mobile first** - 1 column → 2 → 3+
✅ **Responsive images** - Aspect ratios maintained
✅ **Whitespace matters** - Breathing room
✅ **Test responsiveness** - All breakpoints
✅ **Performance** - Lazy load images

## Resources

- **CSS Grid**: MDN Web Docs, CSS-Tricks
- **Tools**: Figma, Framer, design system tools
- **Learning**: Web.dev, A List Apart
- **Inspiration**: Pinterest, Dribbble, Behance

---

**Congratulations!** You've completed the UI Patterns module.

**Next Step**: Move on to [Accessibility](../04-accessibility/)
