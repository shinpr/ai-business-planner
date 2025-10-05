# Prompt Engineering for Prototype Generation

## Purpose

Best practices for crafting effective prompts for AI-powered prototype generation tools.

## Core Principles

### 1. Clarity and Specificity
- Be explicit about what you want
- Provide concrete examples
- Avoid ambiguity
- Define technical terms

### 2. Context First
- Explain the product purpose
- Describe target users
- State core value proposition
- Set the scene before details

### 3. Structured Information
- Use clear sections and headers
- Bullet points for lists
- Numbered steps for flows
- Hierarchical organization

### 4. Completeness
- Include all necessary information
- Specify requirements fully
- Address edge cases
- Provide fallback behaviors

## Prompt Structure Template

### Essential Sections

```markdown
1. CONTEXT
   - What the product does
   - Who it's for
   - Core value proposition

2. SCOPE
   - What to build (MVP features)
   - What NOT to build (explicitly)

3. USER FLOWS
   - Step-by-step user journeys
   - Expected interactions
   - Success criteria

4. FEATURES
   - Detailed feature descriptions
   - Acceptance criteria
   - Priority indicators

5. TECHNICAL SPECS
   - Platform requirements
   - Technology preferences
   - Performance expectations
   - Integration needs

6. DESIGN GUIDANCE
   - UI/UX preferences
   - Visual style
   - Brand elements
   - Responsive requirements

7. SUCCESS CRITERIA
   - What "done" looks like
   - Key functionality to test
   - Expected outcomes
```

## Platform-Specific Best Practices

### Genspark Developer

**Strengths:**
- Step-by-step implementation
- Full-stack applications
- Complex features
- Iterative refinement

**Prompt Tips:**
- Break down into clear phases
- Specify tech stack preferences
- Provide detailed user flows
- Include data models if complex
- Request specific technologies

**Example Pattern:**
```
Build a [type] application that allows users to [core action].

Tech Stack: [Specify technologies]

Core Features:
1. [Feature 1] - Users should be able to [action]
2. [Feature 2] - The system should [behavior]

Step-by-step implementation:
Phase 1: [Basic structure]
Phase 2: [Core functionality]
Phase 3: [Enhancements]
```

### v0 (Vercel)

**Strengths:**
- React/Next.js components
- Modern UI/UX
- Responsive design
- Quick iterations

**Prompt Tips:**
- Emphasize visual design
- Describe component structure
- Specify Tailwind classes if needed
- Focus on user experience
- Request specific UI patterns

**Example Pattern:**
```
Create a [component/page] for [purpose].

Design: [Modern/minimal/etc.]
Layout: [Describe layout]
Components needed:
- [Component 1]: [Description]
- [Component 2]: [Description]

User interaction:
When user [action], the interface should [response]
```

### General AI Tools

**Universal Prompt Pattern:**
```
I need to build [product description].

PURPOSE: [Why this exists]

TARGET USERS: [Who will use it]

CORE FUNCTIONALITY:
1. [Feature 1 with detailed description]
2. [Feature 2 with detailed description]

USER FLOW:
1. User [action]
2. System [response]
3. User [next action]

TECHNICAL REQUIREMENTS:
- Platform: [web/mobile/etc]
- [Other tech requirements]

DESIGN REQUIREMENTS:
- Style: [Description]
- Key UI elements: [List]

SUCCESS CRITERIA:
- [What working looks like]
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

□ Context clearly explained
□ Scope explicitly defined (in and out)
□ User flows step-by-step
□ Features detailed with examples
□ Technical requirements specified
□ Design guidance provided
□ Edge cases addressed
□ Success criteria clear
□ Platform-specific optimizations applied
□ No ambiguous language

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
