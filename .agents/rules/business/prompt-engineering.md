# Prompt Engineering for Prototype Generation

## Purpose

Best practices for crafting effective prompts for AI-powered prototype generation tools.

## Core Principles

### 1. Clarity and Specificity
- Be explicit about what you want
- Provide concrete examples
- Use unambiguous language

### 2. Context of Use
- Target users: role, skill level, environment
- Usage scenario: when, where, how often
- Decisions users make with this UI

### 3. Structured Information
- Clear sections and headers
- Bullet points for lists
- Numbered steps for flows

### 4. Constraints and Preferences
- Platform and device requirements
- Visual style and tone
- Layout approach and color semantics

### 5. Atmosphere Specification

When design specification exists, include concrete visual instructions derived from atmosphere keywords.

**Required elements:**
- Atmosphere keywords
- Color palette with hex values
- Border-radius, shadow, spacing direction
- Override instructions for default UI library styles
- Elements to avoid

**Platform-specific overrides:**

For v0 (shadcn/ui based):
```
Override shadcn/ui defaults:
- Colors: [custom palette replacing slate/gray]
- Border-radius: [value]
- Shadows: [style]
- Spacing: [direction]
```

For Genspark:
```
Design customization:
- Color palette: [hex values]
- Visual atmosphere: [keywords]
- Avoid: [specific elements]
```

## Prompt Structure Template

### Essential Sections

```markdown
1. CONTEXT
   - Product purpose and value
   - Target users (role, skill level)
   - Usage scenario (when, where, frequency)
   - Decisions users make with this UI

2. SCOPE
   - MVP features to build
   - Scope boundaries

3. USER FLOWS
   - Step-by-step user journeys
   - Key interactions and responses

4. FEATURES
   - Feature descriptions with acceptance criteria
   - Priority (Must/Should/Could)

5. TECHNICAL SPECS
   - Platform: Web/Mobile/Desktop
   - Responsive breakpoints
   - Mock data approach (LocalStorage, hardcoded)

6. DESIGN GUIDANCE
   - Visual style and tone
   - Color semantics (e.g., red=error, green=success)
   - Layout approach

7. SUCCESS CRITERIA
   - What "done" looks like
   - Key functionality to verify
```

## Platform-Specific Best Practices

### Genspark Developer

**Strengths:**
- Interactive HTML/CSS/JS prototypes
- Step-by-step implementation
- Component-based UI generation
- Iterative refinement

**Prompt Tips:**
- Focus on visual prototype scope
- Provide mock data examples
- Describe component interactions
- Specify responsive requirements
- Include atmosphere keywords and color palette
- Specify overrides from default styling

**Example Pattern:**
```
Build an interactive prototype for [product].

SCOPE: Visual prototype with mock data

Core Features:
1. [Feature 1] - [user interaction description]
2. [Feature 2] - [visual behavior description]

Mock Data: Use LocalStorage with sample JSON
Interactions: [Click, hover, form states]
```

### v0 (Vercel)

**Strengths:**
- React/Next.js components
- Tailwind CSS integration
- Modern UI patterns
- Quick iterations

**Prompt Tips:**
- Include user context (who, when, what decision)
- Describe component hierarchy
- Specify color semantics
- Define responsive behavior

**Example Pattern:**
```
Build [component] used by [user role] in [scenario] to [decision/action].

Atmosphere: [keywords]
Color palette: [hex values]

Override shadcn/ui defaults:
- [specific overrides]

Components:
- [Component]: [behavior]

Interactions: [state changes on user actions]
```

### General AI Tools

**Universal Prompt Pattern:**
```
Build [product] for [user role] to [goal].

CONTEXT:
- Users: [role, skill level]
- Scenario: [when, where they use it]
- Decision: [what they decide with this UI]

FEATURES:
1. [Feature]: [behavior]
2. [Feature]: [behavior]

USER FLOW:
1. User [action] → System [response]
2. User [action] → System [response]

CONSTRAINTS:
- Platform: [web/mobile]
- Style: [visual tone]
- Colors: [semantic meaning]

SUCCESS: [what working looks like]
```

## Effective Prompt Techniques

### 1. Use Concrete Examples
Bad: "Create a search feature"
Good: "Create a search bar that filters a list of products by name and category. When user types 'laptop', show only laptop products. Include autocomplete suggestions."

### 2. Specify Edge Cases
```
Search functionality:
- If no results: Display "No products found" message
- If search empty: Show all products
- If error: Display "Search unavailable" with retry button
```

### 3. Provide Visual Descriptions
```
Header layout:
- Logo on left (40px height)
- Navigation menu in center (Home, Products, About)
- User profile icon on right (circular, 36px)
- Background: white with subtle shadow
```

### 4. Define Data Structures
```
Product object:
- id (string)
- name (string)
- price (number)
- category (string)
- image_url (string)
- in_stock (boolean)
```

### 5. Describe Interactions
```
Add to Cart button:
- Default: Blue background, white text
- Hover: Darker blue
- Click: Show loading spinner
- Success: Change to "Added ✓" for 2 seconds
- Error: Shake animation + error message
```

## Quality Checklist

□ Context includes user role, scenario, and decisions
□ Scope boundaries clearly defined
□ User flows are step-by-step
□ Features have acceptance criteria
□ Design guidance with color semantics
□ Success criteria are verifiable

## Common Pitfalls

### Too Vague
❌ "Build a dashboard"
✅ "Build a dashboard showing 3 metrics cards (revenue, users, conversions) with a line chart below showing trend over last 30 days"

### Too Technical
❌ "Implement React hooks with useState and useEffect for async data fetching with error boundaries"
✅ "Fetch user data when page loads, show loading spinner while loading, display data in cards when ready, show error message if fails"

### Missing Context
❌ "Create a form"
✅ "Create a user registration form with fields: email, password, confirm password. Validate email format, password minimum 8 characters, passwords match. Show validation errors inline."

### No Success Criteria
❌ "Make it work"
✅ "Success criteria: User can submit form, data saves to database, user receives confirmation email, redirects to dashboard"

## Iterative Refinement

### Initial Prompt
- High-level overview
- Core features only
- Basic requirements

### Refinement Round 1
- Add specific details
- Clarify ambiguities
- Include edge cases

### Refinement Round 2
- Fine-tune interactions
- Optimize for platform
- Add polish requirements

### Final Prompt
- Complete and comprehensive
- Platform-optimized
- Ready for generation

## Testing Your Prompt

Before submitting:
1. Read prompt as if you know nothing about the project
2. Check if all features clearly described
3. Verify technical requirements complete
4. Ensure success criteria measurable
5. Confirm platform-specific optimizations applied
