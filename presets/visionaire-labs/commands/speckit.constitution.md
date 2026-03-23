---
description: Create or update the Visionaire Labs project constitution, enforcing our core principles — TypeScript, aesthetics-first, AI-native, Vercel deployment, and Solana-awareness where applicable.
handoffs:
  - label: Build Specification
    agent: speckit.specify
    prompt: Implement the feature specification based on the updated constitution. I want to build...
---

## User Input

```text
$ARGUMENTS
```

You **MUST** consider the user input before proceeding (if not empty).

## Outline

You are creating or updating the project constitution at `.specify/memory/constitution.md`. The Visionaire Labs preset provides an opinionated template — your job is to fill it with project-specific values while preserving all non-negotiable principles.

Follow this execution flow:

1. Load the existing constitution at `.specify/memory/constitution.md`.
   - If it doesn't exist yet, copy from `.specify/templates/constitution-template.md` first.

2. Fill all placeholder tokens `[ALL_CAPS]` with concrete project values:
   - `[PROJECT_NAME]` — from repo name or user input
   - `[RATIFICATION_DATE]` — today's date (ISO 8601) if new, else preserve original
   - `CONSTITUTION_VERSION` increment rules:
     - MAJOR: Principle removed or fundamentally redefined
     - MINOR: Principle added or meaningfully extended
     - PATCH: Wording, typo, clarification

3. **Non-negotiable sections**: Do NOT remove or soften the following principles. If user input conflicts with them, note the conflict and preserve the principle:
   - "Aesthetics Are Not Optional" — visual quality is mandatory, not a nice-to-have
   - "TypeScript First" — no JavaScript in source, strict mode required
   - "Stack Defaults" — deviations require written justification in the Complexity Log
   - "Code Quality Gates" — build, lint, typecheck must pass before merge

4. **Customize project-specific content** using user input (if provided):
   - Add project-specific aesthetic direction (dark/light preference, color palette notes, typography)
   - Add project-specific tech notes (e.g., "this project uses Clerk for auth", "Solana features not applicable")
   - Add any performance targets or compliance requirements
   - Extend the Stack Defaults table if the project uses specific libraries

5. **Solana section**: 
   - If the project involves tokens, wallets, or on-chain data — ensure this section is complete
   - If not applicable — replace the Solana section with: "## VII. Solana — Not Applicable\nThis project has no on-chain or token functionality."

6. Propagate changes to dependent templates:
   - Check `.specify/templates/plan-template.md` — ensure Constitution Check table reflects current principles
   - Check `.specify/templates/spec-template.md` — verify aesthetic requirements section is present

7. Write the completed constitution to `.specify/memory/constitution.md`.

8. Output a summary:
   - Version bump and rationale
   - Which principles were customized vs. left as defaults
   - Suggested commit: `docs: ratify constitution v[VERSION] for [PROJECT_NAME]`

**Style rules:**
- No bracketed placeholders left in the final output (except intentionally deferred TODO items)
- Each principle: a clear heading + declarative rules (MUST/MUST NOT, not "should")
- Keep the document scannable — bullet lists over paragraphs where possible
