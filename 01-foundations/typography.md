# Typography Fundamentals

Typography is the art and technique of arranging type to make written language legible and visually appealing. It's one of the most critical skills in UI/UX design.

## 📚 Table of Contents

1. [Typeface vs. Font](#typeface-vs-font)
2. [Font Classifications](#font-classifications)
3. [Anatomy of Type](#anatomy-of-type)
4. [Readability & Legibility](#readability--legibility)
5. [Font Sizing & Hierarchy](#font-sizing--hierarchy)
6. [Font Pairing](#font-pairing)
7. [Practical Exercises](#practical-exercises)

## Typeface vs. Font

### Typeface
- The design of the characters (e.g., "Helvetica", "Georgia")
- The artistic design family
- Example: "Helvetica" is a typeface

### Font
- A specific variation of that typeface
- Includes weight, style, and size
- Example: "Helvetica Bold 16px" is a font

**Simple way to remember**: Typeface is the design, font is the specific implementation.

## Font Classifications

### 1. Serif Fonts
- **What**: Small lines (serifs) at the ends of characters
- **Personality**: Traditional, formal, trustworthy, established
- **Use cases**: Books, articles, formal documents, corporate sites
- **Examples**: Georgia, Times New Roman, Garamond, Lora

### 2. Sans-Serif Fonts
- **What**: No serifs, clean lines
- **Personality**: Modern, clean, casual, straightforward
- **Use cases**: Web design, app interfaces, digital products
- **Examples**: Helvetica, Arial, Roboto, Open Sans

### 3. Display Fonts
- **What**: Decorative, stylized fonts
- **Personality**: Unique, creative, expressive
- **Use cases**: Headlines, branding, special occasions
- **Examples**: Playfair Display, Lobster, Bebas Neue

### 4. Script/Cursive Fonts
- **What**: Mimics handwriting, flowing strokes
- **Personality**: Elegant, personal, artistic
- **Use cases**: Invitations, branding accents
- **Examples**: Pacifico, Great Vibes, Dancing Script

### 5. Monospace Fonts
- **What**: Each character takes equal width
- **Personality**: Technical, code-like, precise
- **Use cases**: Code examples, programming interfaces
- **Examples**: Courier New, Monaco, Fira Code

## Anatomy of Type

### Key Terms

| Term | Definition |
|------|------------|
| **Cap Height** | Height of uppercase letters |
| **X-Height** | Height of lowercase "x" |
| **Ascender** | Parts above x-height (b, d, h) |
| **Descender** | Parts below baseline (g, j, p, y) |
| **Baseline** | Imaginary line text sits on |
| **Kerning** | Space between specific letter pairs |
| **Leading** | Space between lines of text |
| **Tracking** | Overall space between all letters |
| **Weight** | Thickness of strokes |
| **Style** | Slant or variation (Italic, Normal) |

## Readability & Legibility

### Legibility
- How easily individual letters are distinguished
- Affected by: Font choice, size, color, contrast

### Readability
- How easily text is read and understood
- Affected by: Line length, line spacing, paragraph spacing, font size

### Best Practices

✅ **Font Size**
- Body text: 14-16px (minimum)
- Mobile: 16px+ recommended
- Headlines: 24px+

✅ **Line Length**
- Ideal: 50-75 characters per line
- Too long: Hard to track to next line
- Too short: Too many line breaks

✅ **Line Spacing (Leading)**
- Body text: 1.5-1.75 line height
- Headlines: 1.2-1.3 line height
- Minimum 1.4 for accessibility

✅ **Color & Contrast**
- Minimum 4.5:1 contrast ratio for body text
- Ensure readable on light and dark backgrounds

## Font Sizing & Hierarchy

### Recommended Type Scale

```
Display: 48px (or 3rem)
Heading 1: 36px (or 2.25rem)
Heading 2: 28px (or 1.75rem)
Heading 3: 24px (or 1.5rem)
Heading 4: 20px (or 1.25rem)
Body: 16px (or 1rem)
Small: 14px (or 0.875rem)
Tiny: 12px (or 0.75rem)
```

### Creating Hierarchy

1. **Use different sizes** - Larger = more important
2. **Use different weights** - Bold = emphasis
3. **Use color** - Primary color = primary information
4. **Use spacing** - More space = more important
5. **Use position** - Top of page = more important

## Font Pairing

### Rule 1: Contrast
- Pair serif with sans-serif
- Pair different weights
- Create clear visual distinction

### Rule 2: Respect Personality
- Modern sans-serif + Modern sans-serif: Clean
- Serif + Sans-serif: Traditional + Modern
- Display + Sans-serif: Creative + Readable

### Rule 3: Proportion
- Large display font needs smaller body font
- Avoid fonts of similar visual weight

### Classic Pairings

| Heading | Body | Combo |
|---------|------|-------|
| Playfair Display | Roboto | Elegant + Clean |
| Montserrat Bold | Open Sans | Modern + Accessible |
| Georgia | Verdana | Traditional + Practical |
| Lobster | Lato | Playful + Professional |
| Raleway | Lora | Contemporary + Classic |

## Web Fonts

### System Fonts vs. Web Fonts

**System Fonts** (Fast, Reliable)
- Available on all devices
- No loading time
- Limited options

**Web Fonts** (Flexible, Unique)
- Custom fonts loaded from server
- Slight loading delay
- Unlimited options

### Popular Web Font Services

- **Google Fonts**: Free, vast selection
- **Adobe Fonts**: Professional, extensive library
- **Font Face**: Self-hosted, full control

### Using Google Fonts

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700" rel="stylesheet">

<style>
  body {
    font-family: 'Roboto', sans-serif;
  }
</style>
```

## Practical Exercises

### Exercise 1: Font Analysis
1. Find 3 websites you admire
2. Identify their fonts
3. Analyze their font pairing strategy
4. Document why it works

### Exercise 2: Font Pairing Challenge
1. Choose 2 fonts (serif + sans-serif)
2. Create a landing page mockup
3. Assign roles (heading, body, accent)
4. Test readability and balance

### Exercise 3: Type Hierarchy Practice
1. Take a news article
2. Redesign with clear hierarchy
3. Use 3+ different sizes
4. Ensure good readability

### Exercise 4: Accessibility Testing
1. Create text sample
2. Test contrast ratios
3. Test different font sizes
4. Document accessibility score

### Exercise 5: Create Type System
1. Define type scale (6-8 levels)
2. Assign sizes, weights, colors
3. Create visual reference
4. Document usage guidelines

## Key Takeaways

✅ **Understand font categories** - Serif, sans-serif, display, script
✅ **Know type anatomy** - Ascenders, descenders, baselines
✅ **Prioritize readability** - Size, spacing, contrast
✅ **Use type hierarchy** - Size, weight, color, spacing
✅ **Pair fonts strategically** - Contrast + cohesion
✅ **Test on the web** - Different browsers, devices

---

**Next Step**: Learn about [Spacing & Layout](./spacing-layout.md)
