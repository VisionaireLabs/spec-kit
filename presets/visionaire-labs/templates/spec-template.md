# Feature Specification: [FEATURE NAME]

**Feature Branch**: `[###-feature-name]`
**Created**: [DATE]
**Status**: Draft
**Input**: User description: "$ARGUMENTS"

---

## What We're Building

[One paragraph. Plain English. What is this, and why does it matter to the user? No technical jargon here — just what it does and who it's for.]

---

## User Stories *(mandatory — ordered by priority)*

Each story must be independently shippable. If you implemented only this one story, would it be a working, demo-able thing? It should be.

### User Story 1 — [Brief Title] (P1)

[Describe the user journey in plain language. What does the user want to accomplish?]

**Why P1**: [Why this is the core thing — what breaks if this isn't done?]

**Ships alone as**: [What minimal version of this is demo-able? Describe it concretely.]

**Acceptance Scenarios**:

1. **Given** [state], **When** [action], **Then** [outcome]
2. **Given** [state], **When** [action], **Then** [outcome]

---

### User Story 2 — [Brief Title] (P2)

[User journey description]

**Why P2**: [What value does this add beyond P1?]

**Ships alone as**: [Minimal demo-able version]

**Acceptance Scenarios**:

1. **Given** [state], **When** [action], **Then** [outcome]

---

### User Story 3 — [Brief Title] (P3)

[User journey description]

**Why P3**: [What value does this add?]

**Ships alone as**: [Minimal demo-able version]

**Acceptance Scenarios**:

1. **Given** [state], **When** [action], **Then** [outcome]

---

[Add more stories as needed]

---

## Aesthetic & Experience Requirements

<!-- This section is mandatory for any user-facing feature -->

### Visual Direction
- **Tone**: [e.g., "clean and minimal", "bold and high-contrast", "editorial"]
- **Key UI moments**: [e.g., "empty state should feel intentional, not blank", "loading states must feel alive"]
- **Animation**: [e.g., "none", "subtle fade transitions", "full page transitions on navigation"]
- **Dark mode**: [Required / Optional / Not applicable]

### Edge Cases That Must Feel Good
- Empty state: [What does the user see when there's no data yet?]
- Error state: [How do errors surface — inline, toast, modal?]
- Loading state: [Skeleton? Spinner? Progressive reveal?]

---

## AI Surface Area *(if applicable)*

<!-- Fill this in if the feature interacts with AI in any way -->

- **Where AI reads this data**: [e.g., "agent reads task list to prioritize work"]
- **Where AI writes to this feature**: [e.g., "agent posts summaries to feed"]
- **Semantic requirements**: [e.g., "status fields must use descriptive strings, not numeric codes"]
- **LLM-legibility notes**: [e.g., "include `description` on all entity types"]

---

## Functional Requirements *(mandatory)*

### Must Have (blocks launch)
- **FR-001**: [Specific capability — be concrete]
- **FR-002**: [Specific capability]
- **FR-003**: [Specific capability]

### Should Have (important but not blocking)
- **FR-004**: [Capability]
- **FR-005**: [Capability]

### Won't Have (explicitly out of scope)
- [Thing we are NOT building in this iteration — prevents scope creep]

### Key Entities *(if feature involves data)*

| Entity | Description | Key Fields |
|--------|-------------|------------|
| [Entity 1] | [What it represents] | [id, name, ...] |
| [Entity 2] | [What it represents] | [id, ...] |

---

## Success Criteria *(mandatory)*

How do we know this shipped successfully?

- **SC-001**: [Measurable outcome — e.g., "User can complete X in under 30 seconds"]
- **SC-002**: [Measurable outcome — e.g., "Page loads under 1.5s on mobile"]
- **SC-003**: [Aesthetic outcome — e.g., "Design review sign-off from Thor"]
- **SC-004**: [Technical outcome — e.g., "Vercel build passes, zero TypeScript errors"]

---

## Review & Acceptance Checklist

- [ ] All P1 user stories have concrete acceptance scenarios
- [ ] Aesthetic requirements are specified (not just "make it look good")
- [ ] Empty, error, and loading states are defined
- [ ] Out-of-scope items are explicitly listed
- [ ] Success criteria are measurable
- [ ] AI surface area documented (or marked N/A)
- [ ] No NEEDS CLARIFICATION items remain
