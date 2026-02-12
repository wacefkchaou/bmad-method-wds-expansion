# Model: Scenario Sketching (Whiteport Method)

**Source:** Whiteport Design Studio — 25 years of design practice
**Innovation:** One artifact serves the entire delivery chain

---

## Overview

Scenario Sketching is a design methodology that evolved from real project constraints where multiple conflicting needs had to be captured in a single way of working. It's the practice of designing complete user experiences as journeys rather than isolated screens, creating one universal blueprint that serves designers, clients, developers, QA, and testing.

**The core insight:** Design the forest, not the trees. Design the experience, not the screens.

---

## The Problem This Solves

### Multiple Conflicting Needs

Every software project has stakeholders with different needs:

**Client needs to understand:**
- What they're paying for
- How users will experience the product
- Whether this solves their business problem
- What to approve before development starts

**Designer needs to communicate:**
- Complete user journeys, not isolated screens
- Interaction patterns and transformations
- Edge cases and error states
- The logic behind visual decisions

**Developer needs to implement:**
- Clear specifications for each feature
- Understanding of user flows
- Edge cases and validation rules
- Testable acceptance criteria

**QA needs to test:**
- Expected behaviors at each step
- Error handling and edge cases
- User flow completeness
- Acceptance criteria validation

**Project Manager needs to plan:**
- Epics and user stories
- Incremental delivery milestones
- Dependency mapping
- Testing checkpoints

### The Traditional Problem

**Typical approach:**
```
Designer creates mockups
   ↓
Client reviews static screens (doesn't understand flow)
   ↓
Developer gets screen designs (doesn't understand logic)
   ↓
QA creates test plans from scratch (guesses at expected behavior)
   ↓
PM breaks into stories (guesses at natural boundaries)
```

**Problems:**
- Information loss at every handoff
- Screens shown in isolation lack context
- Client approval doesn't capture full journey understanding
- Developers must infer interaction logic
- QA must guess expected behaviors
- Stories don't align with natural user journeys

---

## The Scenario Sketching Solution

### One Artifact, Entire Chain

**Scenario-driven approach:**
```
Scenario (complete journey with transformations)
   ↓
Designer: Visual blueprint of experience
Client: Understandable walkthrough of user journey
Developer: Implementation spec with logic and states
QA: Test scenarios with expected outcomes
PM: Natural Epic/Story boundaries
```

**Benefits:**
- One source of truth for all stakeholders
- Client approves the actual experience, not just static screens
- Developers get interaction logic, not just visuals
- QA tests against documented expected behavior
- Stories map naturally to scenario steps
- Testing can begin before complete functionality exists

---

## What Is a Scenario?

### Not Pages — Journeys

A scenario is a complete user experience from trigger to resolution.

**Not this (screen-based thinking):**
- Login screen
- Dashboard screen
- Settings screen
- Profile screen

**This (scenario-based thinking):**
- Scenario: User logs in for the first time and sets up their profile
  - Entry point: Landing page
  - Trigger: "Sign up" button clicked
  - Journey: Sign up → Email verification → Welcome → Profile setup → Dashboard arrival
  - Outcome: User has functioning account and understands next steps

**The difference:**
- Screens are static snapshots
- Scenarios are dynamic journeys showing transformations

### Scenarios Capture Transformations

The power of scenarios is showing HOW things transform:

**Example: Adding item to cart**

Traditional mockup shows:
- Product page
- Cart page with item

Scenario shows:
1. Product page (default state)
2. User clicks "Add to Cart" (interaction)
3. Button transforms to "Adding..." (loading state)
4. Success message appears (confirmation)
5. Cart icon updates count (side effect)
6. "Added to cart" state persists (state management)
7. Error state if out of stock (edge case)

**This is what developers need. This is what QA tests. This is what clients understand.**

---

## The Whiteport Innovation

### Evolution from Real Constraints

Scenario Sketching wasn't designed in theory. It evolved from 25 years of real project constraints:

**Client communication constraint:**
- Clients couldn't understand isolated mockups
- Needed to see complete journeys to give meaningful approval
- Required context to make decisions

**Developer handoff constraint:**
- Developers needed interaction logic, not just visual design
- Static mockups left too many questions unanswered
- Implementation required understanding state transformations

**Testing constraint:**
- QA needed expected behaviors documented
- Test plans written from scratch created inconsistency
- Testing scenarios should come from design scenarios

**Incremental delivery constraint:**
- Clients wanted to see progress before completion
- Need to deliver value in pieces, not all-or-nothing
- Scenario order provides natural delivery milestones

**The synthesis:** What if one artifact solved all of these problems simultaneously?

### How Scenarios Align Stakeholders

**For Clients:**
- Understand the complete experience, not just screens
- Approve journeys they can mentally walk through
- See edge cases and error handling upfront
- Make informed decisions about scope and priority

**For Developers:**
- Receive interaction specifications, not just visual comps
- Understand state transformations and logic
- Have edge cases documented before coding
- Know exactly what "done" looks like

**For QA:**
- Test scenarios map directly to design scenarios
- Expected behaviors already documented
- Edge cases identified during design
- Clear acceptance criteria from approved scenarios

**For Project Management:**
- Scenarios map naturally to Epics
- Scenario steps become user stories
- Delivery order follows scenario priority
- Testing checkpoints built into scenario structure

---

## Scenarios Map to Agile

### Natural Epic and Story Boundaries

**Scenario = Epic**

Each scenario represents a complete user journey that delivers value:
- Scenario: "User creates first event"
- Epic: "Event creation flow"

**Scenario steps = Stories**

Each transformation in the scenario becomes a story:
- Story 1: "User navigates to create event"
- Story 2: "User enters event details with validation"
- Story 3: "User invites participants"
- Story 4: "User confirms and publishes event"
- Story 5: "User sees confirmation and next steps"

### Incremental Delivery

**Build in scenario order:**
1. Scenario 1: User signs up and creates profile (MVP foundation)
2. Scenario 2: User creates first event (core value delivery)
3. Scenario 3: User invites team members (collaboration)
4. Scenario 4: User manages recurring events (advanced feature)

**Test as you go:**
- When Scenario 1 is implemented → Test complete signup journey
- When Scenario 2 is implemented → Test complete event creation journey
- Don't need all features complete to test meaningful user value

**This enables:**
- Progressive client demos showing real working flows
- Early user testing with complete (if limited) experiences
- Validation of UX decisions before building everything
- Course correction while investment is still low

---

## Design Experiences, Not Screens

### The Forest vs The Trees

**Screen-based thinking (the trees):**
- Design each page in isolation
- Focus on visual layout of elements
- Lose sight of how pieces connect
- Miss interaction logic and transformations
- Create beautiful screens that don't flow

**Experience-based thinking (the forest):**
- Design complete user journeys
- Focus on how users move through the experience
- Understand how screens connect and transform
- Document interaction logic throughout
- Create cohesive experiences that work

### The Mindset Shift

**From:** "I need to design a login screen, a dashboard, and a settings page."

**To:** "I need to design the experience of a user logging in for the first time, understanding their dashboard, and customizing their preferences."

**Why this matters:**
- Users don't experience "screens" — they experience journeys
- Designing isolated screens creates disconnected experiences
- Scenarios force you to think about the complete flow
- Transformations reveal the real complexity of the experience

---

## The Scenario Structure

### Anatomy of a Scenario

**Every scenario contains:**

1. **Trigger** — What initiates this journey?
2. **Entry Point** — Where does the user start?
3. **Journey Steps** — What happens at each stage?
4. **Transformations** — How does each interaction change the state?
5. **Edge Cases** — What can go wrong and how is it handled?
6. **Resolution** — What's the outcome and next steps?

### Example: "User logs in for the first time"

**Trigger:** User clicks "Sign up" on landing page

**Entry Point:** Landing page

**Journey Steps:**
1. Landing page → "Sign up" clicked
2. Sign up form → Email/password entered → Validation
3. Email sent → Verification required message
4. Email opened → Verification link clicked
5. Welcome screen → Account confirmed
6. Profile setup → User enters name and preferences
7. Dashboard → User arrives at their new dashboard

**Transformations at each step:**
- Button states: default → hover → loading → success/error
- Form validation: empty → invalid → valid → submitting
- Progress indication: step 1 of 3 → step 2 of 3 → complete
- Navigation: next enabled/disabled based on completion

**Edge Cases:**
- Email already exists → Show helpful error, offer login
- Verification link expired → Show re-send option
- User navigates away mid-signup → Save partial progress
- Verification email not received → Show troubleshooting help

**Resolution:** User has a functioning account and understands next steps

---

## Benefits of Scenario-Based Design

### For Design Quality

**Scenarios prevent:**
- Orphaned states (screens with no way in or out)
- Incomplete flows (missing confirmation or error states)
- Inconsistent patterns (each screen designed differently)
- Missing edge cases (happy path only)

**Scenarios ensure:**
- Complete user journeys from trigger to resolution
- Documented transformations and interactions
- Consistent patterns across the experience
- Edge cases considered during design, not after

### For Development Efficiency

**Scenarios provide:**
- Clear specifications for each interaction
- Expected behaviors documented upfront
- Edge cases identified before coding
- Acceptance criteria built into the scenario

**This prevents:**
- Developers guessing at intended behavior
- Missing edge cases discovered in QA
- Rework due to unclear specifications
- Back-and-forth asking "what should happen when...?"

### For Testing Accuracy

**Scenarios enable:**
- Test plans written directly from scenarios
- Expected behaviors already documented
- Edge cases identified during design
- Consistent testing across features

**This prevents:**
- QA guessing at expected behavior
- Test cases written from scratch
- Inconsistent testing approaches
- Edge cases discovered by users, not QA

### For Client Confidence

**Scenarios allow clients to:**
- Understand complete user experiences
- Mentally walk through journeys before development
- See edge cases and error handling upfront
- Make informed decisions about scope

**This prevents:**
- Client surprises during development
- Misaligned expectations about UX
- Late-stage change requests
- Approval of screens without understanding flow

---

## How Scenarios Enable Testing Before Completion

### The Traditional Problem

**Typical approach:**
- Build all features
- Integrate everything
- Now you can test

**Problems:**
- Testing happens at the end
- Issues discovered late when changes are expensive
- Can't validate UX decisions until everything is built
- No early user feedback

### Scenario-Based Testing

**Scenario approach:**
- Build Scenario 1
- Test complete journey for Scenario 1
- Get user feedback on Scenario 1
- Build Scenario 2
- Test complete journey for Scenario 2
- Continue incrementally

**Benefits:**
- Test real user value early
- Validate UX decisions before building everything
- Get real user feedback while change is cheap
- Catch fundamental issues before heavy investment

**Example:**

Build Scenario 1: "User creates first event"
- Even if calendars, notifications, and analytics aren't built yet
- You can test the complete event creation journey
- Users can create events and see them appear
- Get feedback: Is this flow clear? Are we missing critical info?

Then build Scenario 2: "User invites team to event"
- Now test the complete invitation flow
- Still don't need advanced features
- Validate collaboration UX before building complex features

**This is possible because scenarios are complete journeys, not feature checklists.**

---

## Scenarios vs Feature Lists

### Not This (Feature-Based)

**Build:**
- User authentication
- Event creation
- Calendar view
- Notifications
- Team management
- Recurring events
- Analytics

**Problem:** You can't test a meaningful user journey until ALL features are complete.

### This (Scenario-Based)

**Build:**
1. Scenario: User signs up and creates first event
2. Scenario: User invites team to event
3. Scenario: User sets up recurring weekly meeting
4. Scenario: User reviews team analytics

**Benefit:** After Scenario 1, you can test a complete, valuable user journey.

---

## The Synthesis: Why This Works

### Multiple Problems, One Solution

Scenario Sketching simultaneously solves:

✅ **Client understanding** — Clients approve journeys, not isolated screens
✅ **Developer clarity** — Developers implement documented transformations
✅ **QA efficiency** — Test scenarios come from design scenarios
✅ **Incremental delivery** — Build and test scenario by scenario
✅ **Agile alignment** — Scenarios map naturally to Epics and Stories
✅ **Design quality** — Forces complete journey thinking
✅ **Early validation** — Test UX decisions before heavy investment

### The Whiteport Innovation

**What makes this unique:**

Not just "design user flows" (many do this)
Not just "document edge cases" (some do this)
Not just "create clickable prototypes" (common practice)

**The innovation is the synthesis:**

One artifact that simultaneously:
- Communicates experience to clients
- Specifies implementation for developers
- Provides test scenarios for QA
- Maps to Epics and Stories for PM
- Enables incremental delivery
- Forces complete journey thinking
- Documents transformations and edge cases

**This evolved from 25 years of real project constraints, not theoretical design.**

---

## Selective Ignorance: The Strategic Core

### The Design Paralysis Problem

**If you try to handle everything at once:**
- Figure out all edge cases on every step
- Design error states before the main flow
- Account for every variation upfront

**You make no progress designing the actual experience.**

### The Squeaky Wheel Trap

**The problem:** The squeaky wheel gets the grease.

Edge cases are emotionally compelling. They're annoying when they happen. They scream for attention. When you're focused on fixing the very annoying edge cases, you lose track of the whole picture.

**The trap:**
- Edge cases feel urgent because they're frustrating
- But emotional urgency ≠ strategic importance
- You spend time perfecting rare scenarios
- While the common experience suffers

**The result:**
- 100 buttons trying to handle every edge case
- Cluttered interfaces designed around exceptions
- Perfect handling of rare cases, broken handling of common ones
- Lost sight of what actually matters

### The Whiteport Approach: Strategic Focus

**Focus on what gives the best experience and value:**
- For the vast majority of your most valuable customers
- In the most valuable transactions
- When everything is working as intended

**This is selective ignorance — and it's strategic, not lazy.**

### The Progression

**Phase 1: Main Flow (Sunshine Path)**
- Design the most effortless journey when all is great and nothing goes wrong
- Focus 100% on making this perfect
- No distractions from edge cases yet

**Phase 2: Pressure Test**
- When you're happy with the main flow, test it with obvious variations
- Does the structure hold?
- If yes, proceed. If no, refine main flow.

**Phase 3: Edge Cases**
- Now bring in edge cases and error states
- Design for graceful failure
- System should fail elegantly

**Phase 4: Resilient Design**
- The ultimate goal: "User should be able to use it wrong and it should be right anyway"
- Forgiving interactions
- Smart defaults
- Helpful recovery

### Why This Works

**Starting with edge cases (chasing squeaky wheels):**
- Creates complex, cluttered designs
- Adds 100 buttons to handle every scenario
- No progress on core experience
- User confusion from trying to handle everything upfront
- Emotional urgency drives decisions, not strategic value
- Perfect rare cases, broken common cases

**Starting with main flow (strategic focus):**
- Clean, focused designs
- Progress on what matters most
- Edge cases inform refinement, not foundation
- Better overall experience
- Strategic value drives decisions, not emotional noise
- Perfect common cases, then handle exceptions

**Selective ignorance is not cutting corners. It's strategic design discipline that resists the squeaky wheel trap.**

### Ask "What If": The Linchpin Mindset

**Selective ignorance also means asking whether steps should exist at all.**

As a Linchpin designer, you ask the "what if" questions that reveal possibilities:

**Example: Login Flow**

> "We need to log in."

**What if** we didn't require login upfront?

- What if users arrived from email with magic links?
- What if users could browse freely?
- What if login was only required for sensitive data or changes?

**Be the kid pointing out the emperor has no clothes.**

Ask "what if" for every assumption in your scenario:
- "What if this step didn't exist?"
- "What if we combined these steps?"
- "What if we solved this completely differently?"

**The progression:**
1. Initial scenario: 8 steps
2. Ask "what if" for each step
3. Refined scenario: 4 steps
4. Ask "what if" again
5. Essential scenario: 2 steps

**Every step in a scenario must justify its existence.**

If you can't defend why a step is necessary with clear reasoning, remove it. The best scenarios aren't the most thorough — they're the most essential.

This is design discipline. This is being a Linchpin designer. This is what separates professionals from amateurs.

---

## Key Principles

### 1. Design Journeys, Not Screens

Users experience flows, not pages. Design the complete journey.

### 2. Document Transformations

Show how interactions change state. This is what developers need and QA tests.

### 3. One Artifact, Entire Chain

Scenarios serve designer, client, developer, QA, and PM simultaneously.

### 4. Build in Scenario Order

Each scenario is a testable, deliverable user journey.

### 5. Test Before Completion

Scenarios enable testing complete journeys before all features exist.

### 6. Map Naturally to Agile

Scenarios = Epics. Scenario steps = Stories. No forced translation.

### 7. Strategic Progression: Main Flow First

During design, you cannot focus on everything at once. Focus strategically:
- Main flow when everything works perfectly
- Pressure test with obvious variations
- Then introduce edge cases and graceful failure

### 8. The Ultimate Design Goal

"The user should be able to use it wrong and it should be right anyway."

### 9. Ask "What If"

Every step must justify its existence. Be the Linchpin designer who asks "what if" questions until the scenario shrinks from 8 steps to 2. The best scenarios aren't the most thorough — they're the most essential.

---

## Application to Practice

### When Building with AI Assistance

**Scenarios become specifications for AI agents:**

Traditional approach:
- "Build me a login screen"
- AI guesses at behavior, validations, error states
- You debug and refine endlessly

Scenario-based approach:
- Provide complete "User logs in" scenario with transformations
- AI implements documented behavior
- Edge cases already specified
- Testing criteria built-in

**The scenario IS the specification.**

### When Working with Clients

**Scenarios enable informed approval:**

Traditional: "Here are some mockups of screens"
- Client: "Looks nice!" (but doesn't understand flow)
- Later: "Wait, this isn't what I thought it would do..."

Scenario-based: "Walk through this signup journey with me"
- Client experiences the complete flow
- Sees edge cases and error handling
- Understands what they're approving
- Confident in the direction

---

## Further Resources

**Related WDS concepts:**
- [Specifications as the New Code](specifications-as-the-new-code.md)
- Storyboarding (Module 10)
- Scenario Specifications (Module 11)

**Application in WDS:**
- [Module 08: Outline Scenarios](../learn/module-08-outline-scenarios/)
- [Lesson 1: Design Experiences, Not Screens](../learn/module-08-outline-scenarios/lesson-01-design-experiences-not-screens.md)

---

## Conclusion

**Scenario Sketching is the practice of designing complete user experiences as journeys, creating one universal blueprint that serves the entire delivery chain.**

It evolved from real project constraints where designers, clients, developers, QA, and project managers all needed different things from the same artifact.

**The synthesis:** What if one way of working solved all these needs simultaneously?

**Design the forest, not the trees.**
**Design experiences, not screens.**
**Design journeys, not pages.**

This is the Whiteport Method.

---

*This model document captures the foundational methodology behind Scenario Sketching as practiced at Whiteport Design Studio. For application to the WDS workflow, see Module 08: Outline Scenarios.*
