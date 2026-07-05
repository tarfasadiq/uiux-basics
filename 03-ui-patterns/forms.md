# Form Design Fundamentals

Forms are where user intent becomes action. Great form design removes friction, guides users through the process, and makes data entry feel effortless.

## 📚 Table of Contents

1. [Form Principles](#form-principles)
2. [Form Inputs](#form-inputs)
3. [Form Layout](#form-layout)
4. [Validation & Errors](#validation--errors)
5. [Accessibility](#accessibility)
6. [Practical Exercises](#practical-exercises)

## Form Principles

### Why Form Design Matters

✅ **Conversions** - Well-designed forms convert more users
✅ **Data Quality** - Clear forms get better data
✅ **User Experience** - Forms can be enjoyable
✅ **Trust** - Clear forms feel trustworthy
✅ **Mobile** - Forms are critical on mobile
✅ **Accessibility** - Forms must work for everyone

### Form Design Goals

1. **Minimize Friction** - Make it easy
2. **Guide Users** - Show them the way
3. **Build Trust** - Be transparent
4. **Collect Quality Data** - Ask right questions
5. **Handle Errors Gracefully** - Help them fix issues

### Form Types

**Contact Form**
- Name, email, message
- Short and simple
- Single column

**Sign Up Form**
- Email, password, name
- Progressive disclosure (ask later)
- Single column

**Checkout Form**
- Billing, shipping, payment
- Multiple steps
- Show progress

**Profile Form**
- Many fields
- Grouped logically
- Save progress

**Search Form**
- Just a search input
- Auto-suggestions
- Mobile-optimized

## Form Inputs

### Text Input

**When to use**: Single line text
- Name, email, username
- Address, phone number
- Search queries

**Best practices**:
- Clear labels
- Helpful placeholder (not replacement for label)
- Adequate width
- Auto-focus first field

### Textarea

**When to use**: Multiple lines of text
- Messages, comments
- Bio, description
- Feedback

**Best practices**:
- Resizable (vertical only)
- Show character count (optional)
- Indicate required length
- Start focus at first field

### Select Dropdown

**When to use**: Choose from list
- Country, state, category
- Time, date
- Options

**Avoid when**:
- Less than 5 options → use radio buttons
- Mobile → hard to use
- Too many options → use search

**Best practices**:
- Clear label
- "Select one..." placeholder
- Alphabetical order (unless logical order exists)
- Grouped options if many

### Radio Buttons

**When to use**: Single choice from few options
- 2-5 options
- Mutually exclusive
- All options visible

**Best practices**:
- Show all options
- Default selection recommended
- Horizontal for few options
- Vertical for many options

### Checkboxes

**When to use**: Multiple selections
- Multiple options can be selected
- Optional fields
- Confirmations

**Best practices**:
- Clear labels
- Group related items
- Show all options
- Easy to toggle

### Toggle Switch

**When to use**: Binary choice
- Yes/No, On/Off
- Settings
- Preferences

**Best practices**:
- Use sparingly
- Clear label
- Indicate current state
- Mobile-friendly

### Date Input

**When to use**: Date selection
- Birth date
- Appointment date
- Event date

**Best practices**:
- Use native date picker when available
- DD/MM/YYYY format (or locale-specific)
- Show calendar picker
- Accept typed input

### File Upload

**When to use**: Upload files
- Profile picture
- Document
- Resume

**Best practices**:
- Show acceptable file types
- Show file size limit
- Drag and drop area
- Show upload progress
- Preview before upload

## Form Layout

### Single Column (Best)

**Pros**:
- Mobile-friendly
- Natural reading flow
- Fewer eye movements
- Better scanning

**When**: Most forms

```
[Name _______________]
[Email ______________]
[Message ___________]
[Submit]
```

### Two Column (Sometimes)

**Pros**:
- Saves vertical space
- Works for related fields

**Cons**:
- Harder to scan
- Confusing on mobile
- Reading order issues

**When**: Related pairs (first/last name, city/state)

```
[First Name ___] [Last Name ___]
[Email _______________________]
```

### Three+ Columns (Avoid)

**Cons**:
- Confusing on desktop
- Terrible on mobile
- Hard to read
- Poor accessibility

**Never use this**

### Grouping & Sections

```
PERSONAL INFORMATION
[First Name __________]
[Last Name ___________]
[Email _______________]

ADDRESS
[Street _______________]
[City _________] [State __]

PAYMENT
[Card Number _____________]
[Expiry __] [CVV ___]
```

### Progress Indication

For multi-step forms, show progress:

```
Step 1: Info  → Step 2: Address → Step 3: Payment
████░░░░░░░░ (33%)

Or: "Step 1 of 3"
```

### Required vs. Optional

**Mark required fields**:
- Asterisk (*) - traditional but unclear
- "Required" label - clearer
- Change color or add icon

**Better**: Mark optional instead
- Most fields required
- Mark rare optional fields
- Less visual clutter

```
Bad:
Name * (required)
Email * (required)
Phone * (required)
Company (optional)

Better:
Name
Email
Phone
Company (optional)
```

## Validation & Errors

### Validation Timing

**Inline Validation** (As user types)
- Real-time feedback
- Fixes errors immediately
- Reduces anxiety
- Don't show error until they leave field

**Submit Validation** (On submit)
- Show all errors at once
- Highlight problematic fields
- Show specific error messages
- Suggested fixes

### Error Messages

**Bad Error Messages**:
- "Error"
- "Invalid input"
- "Please try again"
- Unclear, unhelpful

**Good Error Messages**:
- "Email must be valid (example@email.com)"
- "Password must be at least 8 characters"
- "This email is already registered"
- Specific, helpful, actionable

### Error Design

```
❌ Bad Error Display           ✅ Good Error Display
────────────────────────────────────────────────────
Small red text               Large, clear error box
Bury error far away         Near problematic field
Just the code ("E001")       Human-readable message
No suggestion                Suggested fix
Red field only               Red field + message
```

### Success States

Show validation success:
- Green checkmark for valid email
- Green outline for password strength
- Success message on submit
- Confirmation page/screen

## Accessibility

### Labels

✅ **Always use labels**
```html
<label for="email">Email</label>
<input id="email" type="email">
```

❌ **Don't hide labels**
```html
<!-- Bad: placeholder is not a label -->
<input placeholder="Email" type="email">
```

### Keyboard Navigation

✅ **Tab through fields** - Logical order
✅ **Enter submits** - Default action
✅ **Escape clears** - Optional
✅ **Arrow keys** - For dropdowns/radios
✅ **Spacebar** - To toggle checkboxes

### Screen Readers

✅ **Descriptive labels** - Tells what field is
✅ **Error announcements** - Alert when errors occur
✅ **Required indication** - aria-required
✅ **Help text** - aria-describedby
✅ **Error linking** - Connect to field

### Color & Contrast

✅ **Don't rely on color alone** - Add text/icon
✅ **Error color** - Red with text: "Error:"
✅ **Success color** - Green with checkmark
✅ **Contrast ratio** - 4.5:1 minimum

## Practical Exercises

### Exercise 1: Form Audit
1. Find 3 web forms
2. Identify issues:
   - Input types (correct ones used?)
   - Error handling
   - Accessibility
   - Mobile experience
3. Document problems
4. Suggest improvements

### Exercise 2: Design Contact Form
1. Design simple contact form
2. Include: name, email, subject, message
3. Single column layout
4. Show success/error states
5. Mobile responsive

### Exercise 3: Build Checkout Form
1. Design multi-step checkout
2. Step 1: Shipping
3. Step 2: Billing
4. Step 3: Payment
5. Show progress
6. Save progress locally

### Exercise 4: Error Handling
1. Create form with validation
2. Design 5 error scenarios
3. Create helpful error messages
4. Show inline + submit validation
5. Design success state

### Exercise 5: Accessibility Testing
1. Create form prototype
2. Test keyboard navigation
3. Test with screen reader
4. Check color contrast
5. Test on mobile
6. Document improvements

## Key Takeaways

✅ **Single column is best** - Mobile-first, scannable
✅ **Clear labels always** - Never rely on placeholder
✅ **Right input types** - Email, password, date, etc.
✅ **Real-time validation** - Help users as they type
✅ **Helpful error messages** - Be specific and actionable
✅ **Accessible forms** - Keyboard, labels, screen readers
✅ **Mobile optimized** - Large touch targets, simple layout
✅ **Progress for long forms** - Show how far along

## Resources

- **Books**: "Web Form Design" by Luke Wroblewski
- **Resources**: Material Design, Apple HIG, WCAG
- **Tools**: Formspree, Typeform, Google Forms
- **Learning**: UXMatters, Nielsen Norman Group

---

**Next Step**: Learn about [Navigation Design](./navigation.md)
