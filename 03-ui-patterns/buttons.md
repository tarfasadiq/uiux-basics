# Buttons & CTAs Fundamentals

Buttons are one of the most important UI elements. They signal interactivity and guide users toward actions. A great button is clear, accessible, and impossible to miss.

## 📚 Table of Contents

1. [Button Basics](#button-basics)
2. [Button States](#button-states)
3. [Button Sizes & Hierarchy](#button-sizes--hierarchy)
4. [Button Types](#button-types)
5. [Call-to-Action Design](#call-to-action-design)
6. [Accessibility](#accessibility)
7. [Practical Exercises](#practical-exercises)

## Button Basics

### What Makes a Good Button

✅ **Clear** - Users know what will happen
✅ **Visible** - Easy to find and click
✅ **Responsive** - Shows feedback immediately
✅ **Accessible** - Works for everyone
✅ **Consistent** - Follows established patterns
✅ **Appropriately sized** - Easy to tap on mobile

### Button vs. Link

```
🔘 BUTTON
- Triggers an action
- Changes the page/app state
- Examples: Submit, Save, Delete
- Element: <button>

🔗 LINK
- Takes you somewhere
- Changes the URL
- Examples: Home, About, Next Page
- Element: <a>
```

## Button States

Every button should have multiple states to communicate status:

### 1. Default (Idle)
**When**: Button is ready to be clicked
**Visual**: Normal styling, no changes
**Example**: Blue button with normal opacity

### 2. Hover
**When**: User hovers over button (desktop)
**Visual**: Slight change to show interactivity
**Options**: Darker color, shadow, slight scale increase
**Never use**: Just color change (fails for colorblind users)

```
Good hover states:
- Color change + shadow
- Color change + slight scale
- Outline change
- Background change
```

### 3. Active/Pressed
**When**: Button is being clicked
**Visual**: Pressed-down appearance
**Options**: Darker color, inset shadow, scale down slightly

### 4. Focus
**When**: Button has keyboard focus
**Visual**: Visible indicator (usually outline)
**Important**: For accessibility, must be visible
**Never remove**: Focus indicator without replacing

```css
/* Good focus state */
button:focus {
  outline: 3px solid #0066CC;
  outline-offset: 2px;
}

/* Avoid */
button:focus {
  outline: none; /* Bad! */
}
```

### 5. Disabled
**When**: Button cannot be clicked
**Visual**: Grayed out, lower opacity
**Important**: Show why it's disabled
**Example**: Disabled submit button until form is valid

```
Good disabled state:
- Lower opacity (50-60%)
- Grayed out color
- Cursor changes to "not-allowed"
- Optional: Tooltip explaining why

Bad disabled state:
- Completely invisible
- No indication it exists
- No explanation
```

### 6. Loading
**When**: Action is processing
**Visual**: Shows progress/activity
**Options**: Spinner, loading dots, progress bar
**Important**: Prevent double-clicks during loading

```
Loading state best practices:
- Disable button to prevent double-click
- Show spinner or progress indicator
- Consider changing text: "Submitting..."
- Add feedback message
- Set reasonable timeout (fail after 10s)
```

### State Diagram

```
         User hovers
            ↙ ↖
      DEFAULT → HOVER
        ↑    ↘ ↙
        │    ACTIVE (pressed)
        │
    DISABLED  LOADING
        │
        └─ Show "Why?"

        FOCUS (keyboard)
        Must be visible always!
```

## Button Sizes & Hierarchy

### Size Hierarchy

**Primary Button** (Most Important)
- Largest, most prominent
- Primary color
- High contrast
- Everyone should see it
- Example: "Buy Now", "Sign Up"

```
┌─────────────────────────┐
│    BUY NOW (Primary)    │  ← Large, filled, primary color
└───────────────────────���─┘
  [Secondary Button]
  [Tertiary Button]
```

**Secondary Button** (Important)
- Medium size
- Secondary color or outline
- Less prominent than primary
- Example: "Save Draft", "Learn More"

```
┌─────────────────┐  ┌──────────────┐
│  SAVE DRAFT     │  │  LEARN MORE  │  ← Medium, outline style
└─────────────────┘  └──────────────┘
```

**Tertiary Button** (Less Important)
- Small size
- Text-only or subtle styling
- Least prominent
- Example: "Cancel", "Dismiss"

```
┌─────────────┐  ┌────────────┐
│   CANCEL    │  │  Dismiss   │  ← Small, text-only
└─────────────┘  └────────────┘
```

### Minimum Touch Target Size

- **Desktop**: 44px minimum
- **Mobile**: 44-48px recommended
- **Spacing**: 8px minimum between buttons

```
Poor mobile design:     Good mobile design:
Small    Small          ┌──────────────┐
button   button         │  Full Width  │  ← 48px tall
                        │    Button    │
                        └──────────────┘
                        ┌──────────────┐
                        │  Full Width  │  ← 8px space
                        │    Button    │
                        └──────────────┘
```

## Button Types

### 1. Primary (Filled)
**Use**: Main action, high priority
**Appearance**: Filled with primary color
**Examples**: "Submit", "Buy", "Sign Up"

### 2. Secondary (Outline)
**Use**: Alternative action, supporting action
**Appearance**: Outline with secondary color
**Examples**: "Cancel", "Learn More", "Back"

### 3. Tertiary (Text)
**Use**: Low-priority action
**Appearance**: Text only, no background
**Examples**: "Dismiss", "Skip", "Undo"

### 4. Danger (Red/Warning)
**Use**: Destructive action, be careful!
**Appearance**: Red/warning color, filled or outline
**Examples**: "Delete", "Remove Account"
**Important**: Require confirmation!

### 5. Success
**Use**: Confirmation, positive action
**Appearance**: Green color
**Examples**: "Confirm", "Yes", "Complete"

### 6. Disabled
**Use**: Not yet available
**Appearance**: Grayed out, lower opacity
**Important**: Show why it's disabled

### 7. Icon Buttons
**Use**: When space is limited
**Appearance**: Icon only, usually square
**Important**: Tooltip on hover
**Examples**: Menu icon, close icon, settings icon

## Call-to-Action Design

### What is a CTA?

A Call-to-Action (CTA) is a button designed to get user action. It's the most important element on the page.

### CTA Best Practices

✅ **Action-Oriented Text**
- Start with a verb
- "Get Started" not "Submit"
- "Buy Now" not "Click Here"
- "Learn More" not "Continue"

✅ **High Visibility**
- Contrasting color
- Strategic placement (not buried)
- Adequate whitespace
- Larger than other buttons

✅ **Clear & Specific**
- Tell what will happen
- "Free 14-Day Trial" not "Try"
- "Download PDF" not "Download"
- "Add to Cart" not "Go"

✅ **Creates Urgency (When Appropriate)**
- "Limited Time: Get 50% Off"
- "Spots Filling Up Fast"
- "Join 10,000+ Users"
- Time limits or scarcity

### CTA Examples

```
❌ Bad CTA                      ✅ Good CTA
──────────────────────────────────────────
"Click Here"                    "Start Free Trial"
"Submit"                        "Create Account"
"Go"                            "Buy Now" (with price)
"More Info"                     "Get Expert Advice"
"Continue"                      "Download Case Study"
"OK"                            "Confirm Order"
```

### CTA Placement Strategies

**Above the Fold** (First thing visible)
- Immediate action
- "Get Started"

**Bottom of Section**
- After value proposition
- "Learn More"

**Sticky Header/Footer**
- Always available
- Secondary CTA

**End of Page**
- Final opportunity
- "Sign Up"

**Throughout Content**
- Multiple opportunities
- Consistent messaging

## Accessibility

### Keyboard Navigation

✅ **Tab Order** - Logical order, left to right
✅ **Focus Visible** - Always show focus indicator
✅ **Enter to Activate** - Primary action buttons
✅ **Space to Activate** - All buttons
✅ **Escape to Cancel** - Dialog buttons

### Color & Contrast

✅ **Contrast Ratio**: Minimum 4.5:1
✅ **Not Relying on Color Alone**: Add text or icon
✅ **High Visibility**: Ensure button stands out

### Labels & Text

✅ **Descriptive Text**: "Save Draft" not "Save"
✅ **Active Language**: "Delete" not "Are you sure?"
✅ **Consistent Terminology**: Same action, same text
✅ **ARIA Labels**: If no visible text

```html
<!-- Good button -->
<button aria-label="Close menu">×</button>

<!-- Better button -->
<button aria-label="Close menu">
  <span aria-hidden="true">×</span>
</button>
```

## Practical Exercises

### Exercise 1: Button State Library
1. Create 6 button states: default, hover, active, focus, disabled, loading
2. Design primary, secondary, tertiary buttons
3. Test color contrast ratios
4. Document interactions
5. Export as components

### Exercise 2: CTA Redesign
1. Find 3 poorly-designed CTAs
2. Redesign each CTA
3. Improve text, color, placement
4. Test for accessibility
5. Compare before/after

### Exercise 3: Button Sizing
1. Design buttons at different sizes
2. Test minimum touch targets
3. Show responsive scaling
4. Document size guidelines
5. Create sizing system

### Exercise 4: Accessibility Audit
1. Create 5 button designs
2. Check color contrast (WebAIM)
3. Test keyboard navigation
4. Review focus states
5. Test with screen reader
6. Document fixes needed

### Exercise 5: Create Button System
1. Define button variants: primary, secondary, danger, success
2. Define sizes: small, medium, large
3. Create all state combinations
4. Document usage guidelines
5. Build in design tool (Figma)

## Key Takeaways

✅ **Button states matter** - Default, hover, active, focus, disabled, loading
✅ **Size communicates hierarchy** - Primary larger than secondary
✅ **Clear labels** - Action-oriented text
✅ **Accessibility first** - Keyboard navigation, focus visible, contrast
✅ **Consistent styling** - Use system, don't invent
✅ **Test on mobile** - 44-48px minimum touch target
✅ **Provide feedback** - Show loading and disabled states

## Resources

- **Books**: "Web Form Design" by Luke Wroblewski
- **Resources**: Material Design, Apple HIG, WCAG Guidelines
- **Tools**: Figma components, design systems
- **Learning**: Nielsen Norman Group, A List Apart

---

**Next Step**: Learn about [Form Design](./forms.md)
