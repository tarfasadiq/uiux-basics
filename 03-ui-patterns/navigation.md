# Navigation Design Fundamentals

Navigation is the backbone of your product. Good navigation helps users find what they need. Great navigation disappears—users don't think about it.

## 📚 Table of Contents

1. [Navigation Principles](#navigation-principles)
2. [Navigation Types](#navigation-types)
3. [Mobile Navigation](#mobile-navigation)
4. [Desktop Navigation](#desktop-navigation)
5. [Navigation Patterns](#navigation-patterns)
6. [Practical Exercises](#practical-exercises)

## Navigation Principles

### Core Goals

✅ **Findability** - Users find what they need
✅ **Discoverability** - Users discover new features
✅ **Wayfinding** - Users know where they are
✅ **Efficiency** - Users reach goals quickly
✅ **Consistency** - Same navigation everywhere
✅ **Accessibility** - Works for everyone

### Navigation Rules

1. **Limit main items** - 5-7 maximum
2. **Logical grouping** - Related items together
3. **Clear labels** - Familiar, specific terms
4. **Consistent placement** - Same spot always
5. **Show current location** - User knows where they are
6. **Simple hierarchy** - 2-3 levels maximum

### Breadcrumbs

Show user's location and path:

```
Home > Products > Electronics > Phones > iPhone 15
 ↓       ↓         ↓           ↓        ↓
 Click to go back to any level

Context: You're deep in iPhone 15 product page
Path: You came through Products > Electronics > Phones
Backtrack: Click any level to go back
```

## Navigation Types

### 1. Horizontal Navigation (Top Menu)

**Best for**: Websites, multiple main categories

```
┌─────────────────────────────────────────────┐
│ Logo  [Home] [Products] [Pricing] [Blog] │
│                              [Sign In] │
└─────────────────────────────────────────────┘
```

**Pros**:
- Always visible
- Familiar pattern
- Clear hierarchy
- Desktop-friendly

**Cons**:
- Limited space
- Hard on mobile
- Limited submenus

### 2. Vertical Navigation (Sidebar)

**Best for**: Apps, dashboards, complex hierarchies

```
┌──────────┬────────────────────────┐
│ [Home]   │                        │
│ [Users]  │  Main content area     │
│ [Posts]  │                        │
│ [Stats]  │                        │
│ [Help]   │                        │
└──────────┴────────────────────────┘
```

**Pros**:
- More space for items
- Supports submenus
- Clear hierarchy
- Easy to expand/collapse

**Cons**:
- Takes horizontal space
- Hard on mobile
- Can feel cramped

### 3. Hamburger Menu (Mobile)

**Best for**: Mobile, limited space

```
┌──────────────────┐
│ ☰ Logo   [Icon] │  ← Hamburger menu icon
└──────────────────┘
    ↓ (when clicked)
┌──────────────────┐
│ [Home]           │
│ [Products]       │
│ [Pricing]        │
│ [Blog]           │
│ [Sign In]        │
└──────────────────┘
```

**Pros**:
- Saves space
- Conventional
- Mobile-optimized

**Cons**:
- Hidden menu
- Less discoverable
- Extra click needed

### 4. Tab Navigation (Mobile)

**Best for**: Mobile, 3-5 main sections

```
┌──────────────────────────────┐
│      Content Area            │
│                              │
├──────────────────────────────┤
│ [Home] [Search] [Cart] [Me]  │ ← Always visible
└──────────────────────────────┘
```

**Pros**:
- Always visible
- Quick access
- Clear current section

**Cons**:
- Limited items (3-5)
- No submenus
- Takes bottom space

### 5. Accordion Navigation

**Best for**: Collapsible categories

```
▼ Products
  ▶ Electronics
  ▶ Clothing
  ▶ Home
▶ About
▶ Contact
```

**Pros**:
- Shows hierarchy
- Compact
- Expandable

**Cons**:
- More clicks
- Less discoverable

### 6. Mega Menu

**Best for**: Complex sites with many categories

```
Products ▼
┌─────────────────────────────────┐
│ Electronics      Clothing        │
│ • Phones        • Men's         │
│ • Laptops       • Women's       │
│ • Tablets       • Kids          │
│                                 │
│ Home & Garden   Sports          │
│ • Furniture     • Equipment     │
│ • Decor         • Apparel       │
│ • Tools         • Accessories   │
└─────────────────────────────────┘
```

**Pros**:
- Show many categories
- All items visible
- No submenus needed

**Cons**:
- Takes space
- Can overwhelm
- Complex code

## Mobile Navigation

### Hamburger Menu Best Practices

✅ **Icon + Text** - "Menu" or ☰
✅ **Top right corner** - Standard location
✅ **Always accessible** - Fixed or sticky
✅ **Close button** - X to close
✅ **Full screen or sidebar** - Depends on content
✅ **Prioritize items** - Most important first
✅ **Search option** - Include search

### Mobile Navigation Pattern

```
Hamburger Menu Pattern:

1. Tap hamburger icon ☰
2. Menu slides in from left (or side)
3. Items in priority order
4. Deep items indented
5. Tap item to go there
6. Or tap X to close
7. Tap outside to close (optional)
```

### Bottom Tab Navigation

```
When to use:
- 3-5 main sections
- Equal importance
- Frequent switching

Examples:
- YouTube: Home, Shorts, Subscriptions, Library, Account
- Instagram: Home, Search, Create, Inbox, Profile
- Twitter: Home, Explore, Notifications, Messages, Bookmarks
```

### Mobile-Specific Issues

❌ **Hover states** - No hover on mobile!
❌ **Small targets** - 44px minimum
❌ **Too many items** - Scrolling required
❌ **Nested menus** - Easy to get lost
❌ **Vertical scrolling** - Causes confusion

## Desktop Navigation

### Header Navigation

```
┌─────────────────────────────────────────────┐
│ Logo    [Nav1] [Nav2] [Nav3] [Nav4]    [CTA]│
└─────────────────────────────────────────────┘
          ↓ (hover)
      ┌────────────┐
      │ Subitem 1  │
      │ Subitem 2  │
      └────────────┘
```

**Best practices**:
- Logo on left
- Main nav items centered or left
- CTA on right
- Hover shows submenus
- Submenus appear below
- Close on click away

### Sidebar Navigation

```
┌─────────────────────────────────┐
│ ☰ Dashboard                     │
├─────────────────────────────────┤
│ Dashboard                       │
│ > Reports                       │
│   > Sales                       │
│   > Users                       │
│ > Settings                      │
│ > Help                          │
└─────────────────────────────────┘
```

**Best practices**:
- Logo/app name at top
- Current item highlighted
- Hierarchy clear
- Collapsible sections
- Icons + text
- Collapse on mobile

## Navigation Patterns

### 1. Sticky/Fixed Navigation

**Stays at top while scrolling**

**Pros**:
- Always accessible
- Never need to scroll up

**Cons**:
- Takes space
- Can distract
- Bad on mobile

**When to use**: Main navigation

### 2. Persistent Navigation

**Always visible, doesn't move**

**Pros**:
- Always available
- Doesn't distract
- Good for hierarchy

**Cons**:
- Takes space
- Hard on mobile

**When to use**: Sidebar navigation

### 3. Contextual Navigation

**Changes based on context**

**Pros**:
- Relevant items only
- Cleaner interface
- Mobile-friendly

**Cons**:
- Less discoverable
- Users might miss items

**When to use**: Dynamic UIs, dashboards

### 4. Utility Navigation

**Secondary navigation for meta items**

```
┌─────────────────────────────────────┐
│ [Help] [Login] [Language]           │ ← Utility nav
├─────────────────────────────────────┤
│ Logo    [Main Nav]                  │ ← Main nav
└─────────────────────────────────────┘
```

**Pros**:
- Keeps main nav clean
- Meta items grouped
- Secondary priority

**When to use**: Multiple navigation levels

## Practical Exercises

### Exercise 1: Navigation Audit
1. Find 3 website/app navigation
2. Identify navigation type(s)
3. Analyze structure and hierarchy
4. Note any issues
5. Suggest improvements

### Exercise 2: Mobile Navigation
1. Design hamburger menu
2. Show 8-10 menu items
3. Include icons
4. Show open/closed states
5. Test on mobile device

### Exercise 3: Desktop Navigation
1. Design top navigation bar
2. Include main items + submenus
3. Show hover states
4. Mobile responsive design
5. Include breadcrumbs

### Exercise 4: Navigation Testing
1. Create navigation prototype
2. Test with 3 users
3. Give them tasks ("Find...")
4. Observe pain points
5. Iterate design

### Exercise 5: Create Navigation System
1. Define navigation patterns
2. Show mobile & desktop
3. Document component states
4. Include spacing guidelines
5. Add accessibility notes

## Key Takeaways

✅ **Limit main items** - 5-7 maximum
✅ **Logical hierarchy** - 2-3 levels maximum
✅ **Show current location** - User always knows where
✅ **Different for mobile** - Hamburger or tabs
✅ **Keyboard accessible** - Tab through items
✅ **Screen reader friendly** - Semantic HTML
✅ **Mobile touch targets** - 44px minimum
✅ **Test with real users** - Validate assumptions

## Resources

- **Books**: "Don't Make Me Think" by Steve Krug
- **Resources**: Material Design, Apple HIG, Web.dev
- **Learning**: Nielsen Norman Group, UX Matters
- **Tools**: Figma, Axure, Framer

---

**Next Step**: Learn about [Cards & Grids](./cards-grids.md)
