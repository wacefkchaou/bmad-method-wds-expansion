# Quick Start: Design Delivery

**Agent: Freya** | **Time: 10 min**

---

## Start the Validation Dialog

```
You are Freya, a WDS design agent.

I'm ready to deliver this design for implementation.
Audit my specifications for completeness.

Here's my scenario: [paste]
Here's my page spec: [paste]

Check:
1. Are all elements specified?
2. Are all states defined?
3. Is all content real (no placeholders)?
4. Does everything trace back to the Trigger Map?
5. Can a developer build this without asking questions?
```

---

## When Freya Finds Issues

Fix them before delivery:

```
Freya: "The error state for the submit button is missing.
What happens when form submission fails?"

You: "Button returns to default state.
Toast notification appears: 'Something went wrong. Please try again.'
Toast has a retry action."
```

---

## Generate Acceptance Criteria

```
Generate acceptance criteria for [scenario].

Include:
- Happy path checkboxes
- Error handling checkboxes
- Edge case checkboxes
- Accessibility requirements
```

---

## Example Output

```markdown
## Acceptance Criteria: S01-User-Registration

### Happy Path
- [ ] User can enter email and password
- [ ] Real-time validation shows feedback
- [ ] Submit disabled when form invalid
- [ ] Successful submit redirects to welcome
- [ ] Welcome shows user's email

### Error Handling
- [ ] Invalid email: "Please enter a valid email"
- [ ] Short password: "Password must be at least 8 characters"
- [ ] Server error: Toast with retry option
- [ ] Network error: "Check your connection"

### Edge Cases
- [ ] Duplicate email: "This email is already registered"
- [ ] Refresh during submit: No duplicate account created

### Accessibility
- [ ] All inputs have labels
- [ ] Errors announced to screen readers
- [ ] Focus moves to first error on submit
- [ ] Touch targets minimum 44px
```

---

## Create Delivery Package

```
Generate a delivery overview document for [scenario].

Include:
- Summary
- Scenarios included
- Pages with status
- Components used
- Dependencies
- Notes for development
```

---

## Handoff to Idunn

```
The design is complete.
Package ready at: docs/E-PRD/Design-Deliveries/DD01-xxx/

Idunn can begin implementation.
```

---

**Next:** [Agentic Development →](11-agentic-development.md)
