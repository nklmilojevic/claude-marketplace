# Spec Interviewer Plugin

Interview users about their specifications to uncover hidden requirements, edge cases, and tradeoffs before implementation begins.

## Overview

Specifications often contain implicit assumptions, unexplored edge cases, and undocumented tradeoffs. This plugin provides a rigorous interviewing skill that systematically surfaces these issues, saving significant time and preventing costly mistakes.

## Skills

### Spec Interview

Trigger phrases:
- "interview me about my spec"
- "review my specification"
- "ask me questions about my spec"
- "help me flesh out my spec"
- "find gaps in my specification"

**What it does:**

1. Reads your specification document (default: `spec.md`)
2. Analyzes it for potential gaps, ambiguities, and implicit assumptions
3. Conducts a structured interview using targeted questions
4. Synthesizes answers into an enhanced specification

**Question categories covered:**
- Edge Cases & Boundaries
- Failure Modes & Error Handling
- Implicit Assumptions
- Tradeoffs & Alternatives
- State & Data Management
- User Experience
- Security & Privacy
- Performance & Scale
- Integration & Dependencies
- Evolution & Maintenance

## Example Usage

```
> Interview me about my spec

[Claude reads spec.md and begins asking targeted questions]

Question 1: "When the payment API returns a timeout after the user's card
has been charged but before confirmation - do we retry, refund, or queue
for manual review?"

[After several rounds of questions, Claude synthesizes the answers into
an enhanced specification with explicit edge cases, error handling, and
documented decisions]
```

## Installation

```bash
# Add the marketplace
/plugin marketplace add owner/repo

# Install the plugin
/plugin install spec-interviewer@marketplace-name
```

## File Structure

```
spec-interviewer/
├── .claude-plugin/
│   └── plugin.json                           # Plugin metadata
├── skills/
│   └── spec-interview/
│       ├── SKILL.md                          # Main skill definition
│       └── references/
│           └── question-patterns.md          # Detailed question patterns
└── README.md                                 # This file
```

## License

MIT
