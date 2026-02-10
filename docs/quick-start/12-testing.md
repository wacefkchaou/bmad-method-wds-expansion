# Quick Start: Testing

**Agent: Idunn** | **Time: 10 min**

---

## Start the Dialog

```
You are Idunn, a WDS implementation partner.

I need to verify the implementation matches the spec.

Specification: [paste page spec]
Implementation: [describe or share URL]

Let's compare element by element.
Flag any differences.
```

---

## When Idunn Finds a Match

Confirm and move on:

```
Idunn: "The email field label says 'Email' — matches spec."

You: "Good. Check the placeholder next."
```

---

## When Idunn Finds a Mismatch

Decide what to do:

```
Idunn: "The button says 'Sign Up' but spec says 'Create Free Account'."

You: "The spec is correct. Fix the implementation."
```

OR:

```
Idunn: "The button padding is 24px but spec says 16px."

You: "24px is better for touch targets. Update the spec to match."
```

---

## Run Through Acceptance Criteria

```
Let's verify the acceptance criteria.
Go through each checkbox:

Happy Path:
- [ ] User can enter email and password
- [ ] Real-time validation works
...

For each one, tell me: PASS or FAIL with details.
```

---

## Document Test Results

```
Generate a test results document:

## Test Results: S01-User-Registration
Date: [today]
Status: [X issues found]

### Content
- [x] All text matches

### States
- [x] Default
- [ ] Error — color differs (spec: #DC2626, impl: #EF4444)

### Actions Required
1. Fix error color to match spec
```

---

## Handle Mismatches

Three options:

| Situation | Action |
|-----------|--------|
| Spec unclear | Clarify spec, implementation might be right |
| Implementation wrong | Fix the code |
| Better idea found | Update spec, document why |

**Never leave mismatches undocumented.**

---

## Sign Off

When all checks pass:

```
All acceptance criteria verified.
Test results documented.
Ready for production.
```

---

## Done

Ship it.
