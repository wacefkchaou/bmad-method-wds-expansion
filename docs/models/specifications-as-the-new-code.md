# Model: Specifications as the New Code

**Source:** "The New Code" by Sean Grove, OpenAI
**Video:** [Watch on YouTube](https://www.youtube.com/watch?v=8rABwKRsec4)

---

## Overview

This document captures key insights from Sean Grove's talk about how specifications have become the primary artifact in AI-assisted software development. Code is no longer the source of truth—specifications are.

---

## The Fundamental Shift

### Code Is 10-20% of Value

> "Code is sort of 10 to 20% of the value that you bring. The other 80 to 90% is in structured communication."

**What this means:**
- Writing code is the minor part of software development
- The majority of value comes from communication and alignment
- Specifications are how we achieve that structured communication

### Code Is a Lossy Projection

> "Code is actually a lossy projection from the specification."

**What this means:**
- The specification contains complete intent and context
- Code captures only what's executable
- Much valuable information is lost when you jump to code

**What's lost in code:**
- Why decisions were made
- What alternatives were considered
- Who the users are and what drives them
- How the feature fits in the larger system
- Edge cases that were discussed but not yet implemented
- Accessibility and internationalization intent
- Future evolution plans

---

## Specifications Align Humans

> "A written specification is what enables you to align humans on the shared set of goals."

**The alignment problem:**

Before specification:
- Stakeholder A has one vision
- Stakeholder B has another
- Developer has a third
- Designer has a fourth
- User expects something else

After specification:
- Everyone reads the same document
- Shared understanding emerges
- Alignment is achieved before code

**This alignment is the work.**

The code is just typing after you've aligned.

---

## Specifications as Compiler Source

> "You can think of a specification like source code that you would compile to different architectures."

**The compiler analogy:**

Traditional compilation:
```
C++ source code
    ↓
Compile for x86 → x86 binary
Compile for ARM → ARM binary
Compile for WASM → WebAssembly
```

Specification compilation:
```
Written specification
    ↓
Generate TypeScript → TypeScript code
Generate Rust → Rust code
Generate docs → User documentation
Generate tests → Test suites
Generate tutorials → Tutorial content
```

**Same source. Multiple targets.**

The specification is the source of truth. Code is just one compiled output.

---

## The OpenAI Model Spec Example

> "OpenAI put out their model spec, which is meant to describe how the model ought to behave. It's like 30 pages long, and it's almost incomprehensibly specific about the tiniest details of how it should behave."

**Why 30 pages of specification?**

Because the specification IS the source code.

The model behavior is the compiled output.

When behavior is wrong:
- ❌ Don't patch the output (model behavior)
- ✅ Fix the source (specification)
- ✅ Regenerate the output

**This is professional software development.**

---

## Engineering as Precise Exploration

> "Engineering is the precise exploration by humans of software solutions to human problems."

**Breaking this down:**

**Engineering** — Not just coding, but disciplined problem-solving

**Precise** — Specifications create precision where prompting creates ambiguity

**Exploration** — We're discovering solutions, not just implementing known patterns

**By humans** — AI assists, but humans drive strategy and alignment

**Software solutions** — Code is the output, not the primary work

**To human problems** — We're solving real problems for real people

**The specification is how we make exploration precise.**

Without specifications, you're wandering randomly.
With specifications, you're exploring systematically.

---

## Why Specifications Matter More Than Ever

### The Context Window Problem

You cannot fit an entire application in one prompt.

Even with 200k tokens, you're describing:
- Every user flow
- Every edge case
- Every interaction
- Every validation rule
- Every error state
- Accessibility requirements
- Responsive behaviors
- Loading states
- Empty states
- Animation timings
- Microcopy variations
- Error messages
- Success states
- Navigation patterns
- Data persistence
- Session management
- Permission systems

**And thousands more micro-decisions.**

### The Agent Guessing Problem

Without specifications, AI agents must guess:
- What happens on submit?
- What validation rules?
- What error messages?
- Where does it redirect?
- What if network fails?
- Mobile responsive how?
- Accessibility labels?
- Screen reader support?
- Keyboard navigation?

**Most guesses will be wrong for YOUR app, YOUR users, YOUR context.**

### The Multi-Dimensional Problem

Code captures execution logic.

Specifications capture:
- **Testing** — What "correct" means, how to validate
- **Accessibility** — ARIA labels, keyboard nav, screen reader behavior
- **Internationalization** — String IDs, translation keys, locale handling
- **SEO** — Semantic HTML, meta tags, structured data
- **Error handling** — Every error state, messages, recovery paths
- **Consistency** — Patterns used throughout the application
- **Maintenance** — Why decisions were made, how to evolve
- **Handoff** — New team members understand intent, not just code

**You cannot capture these in code alone.**

---

## The Professional Approach

### Prompt → Spec → Code

**The professional workflow:**

1. **Prompt phase:** Explore the problem space
2. **Spec phase:** Document the complete solution
3. **Code phase:** Generate implementation from specs
4. **Test phase:** Validate against specifications

**Characteristics:**
- ✅ Reliable, repeatable results
- ✅ Testable against clear criteria
- ✅ Maintainable and documented
- ✅ Multi-dimensional (accessibility, i18n, SEO)
- ✅ Credits spent on building, not debugging

### Prompt → Code (The Amateur Trap)

**The amateur workflow:**

1. **Prompt phase:** "Build me a login screen"
2. **Code phase:** Agent guesses everything
3. **Debug phase:** Fix what's wrong
4. **Re-prompt phase:** Fix what broke
5. **Debug again phase:** Fix new issues
6. **Repeat phases 2-5:** Until credits run out

**Characteristics:**
- ❌ Inconsistent output each time
- ❌ No testing reference
- ❌ Impossible to maintain
- ❌ Misses accessibility, SEO, translations
- ❌ Credits burned on endless regeneration

---

## Specifications Enable Autonomy

> "The specification enables you to align humans on the shared set of goals."

**For humans:**
- Stakeholders understand what's being built
- Designers know what to design
- Developers know what to implement
- QA knows what to test
- Documentation writers know what to document

**For AI agents:**
- No guessing required
- Complete context for each piece
- Consistency enforced across application
- Autonomous work without constant clarification
- Testing reference built-in

**Specifications enable AI agents to work autonomously while ensuring they build exactly what you want.**

---

## The Source of Truth Hierarchy

**Traditional software development:**
```
Code = Source of truth
Documentation = Nice to have (often skipped)
```

**AI-assisted professional development:**
```
Specifications = Source of truth (80-90% of value)
Code = Compiled output (10-20% of value)
```

**When you need to:**
- Rewrite in different framework → Keep specs, regenerate code
- Add accessibility → Update specs, regenerate implementation
- Support new language → Update specs, generate translations
- Create documentation → Specs ARE the documentation
- Onboard new developer → They read specs, not code archaeology
- Fix a bug → Check if spec is wrong, or if code deviated from spec

**The specification is the asset you maintain.**

The code is the artifact you ship.

---

## Key Principles

### 1. Specifications Are the Primary Artifact

Code is secondary. Specifications are primary.

When specifications and code disagree, the specification is correct.

### 2. Code Is a Lossy Projection

Code captures execution. Specifications capture intent, context, and reasoning.

### 3. Specifications Align Humans

The majority of software development is achieving alignment. Specifications are how we align.

### 4. Specifications Enable Multiple Outputs

Like compiler source code, specifications can generate code in any language, plus documentation, tests, and tutorials.

### 5. Specifications Enable Autonomous AI Work

AI agents can work autonomously when they have complete specifications. Without specs, they must guess.

### 6. Engineering Is Precise Exploration

Specifications provide the precision that makes exploration systematic instead of random.

### 7. Structured Communication Is 80-90% of Value

Writing code is 10-20%. The real work is communication and alignment.

---

## Quotes Summary

**On value distribution:**
> "Code is sort of 10 to 20% of the value that you bring. The other 80 to 90% is in structured communication."

**On code vs specification:**
> "Code is actually a lossy projection from the specification."

**On alignment:**
> "A written specification is what enables you to align humans on the shared set of goals."

**On specifications as source code:**
> "You can think of a specification like source code that you would compile to different architectures."

**On engineering:**
> "Engineering is the precise exploration by humans of software solutions to human problems."

**On the OpenAI Model Spec:**
> "OpenAI put out their model spec, which is meant to describe how the model ought to behave. It's like 30 pages long, and it's almost incomprehensibly specific about the tiniest details of how it should behave."

---

## Application to Practice

**When building software with AI assistance:**

1. **Start with specifications, not code**
   - Document what you want before generating implementation
   - Include context, edge cases, accessibility, error states

2. **Treat specifications as source code**
   - Version control them
   - Review them carefully
   - Update them when requirements change

3. **Generate code from specifications**
   - Use specifications as detailed prompts
   - Validate generated code against specs
   - Fix discrepancies in specs, regenerate code

4. **Maintain specifications, not code**
   - When bugs arise, check if spec is wrong or code deviated
   - Update specs first, regenerate code second
   - Specifications are the asset that persists

5. **Use specifications for alignment**
   - Share specs with stakeholders for review
   - Use specs to align team on goals
   - Reference specs in discussions and decisions

---

## Further Resources

**Watch the full talk:**
[The New Code — Sean Grove, OpenAI](https://www.youtube.com/watch?v=8rABwKRsec4)

**Related concepts:**
- [OpenAI Model Spec](https://cdn.openai.com/spec/model-spec-2024-05-08.html)
- Specifications as meta-prompts
- AI-assisted development workflows
- Structured communication in software teams

---

## Conclusion

**The paradigm has shifted.**

In traditional software development, code was the source of truth and documentation was secondary.

In AI-assisted software development, specifications are the source of truth and code is a generated artifact.

**This isn't a philosophical preference. This is a practical necessity.**

AI agents need complete specifications to work autonomously and correctly.

Humans need written specifications to align on shared goals.

**Specifications are the new code.**

The sooner you embrace this, the more effectively you'll build software with AI assistance.

---

*This model document captures key insights from Sean Grove's talk. For application to the WDS methodology, see [Lesson 2: Why Specifications Matter](../learn/module-07-design-phase/lesson-02-why-specifications-matter.md).*
