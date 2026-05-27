# Quick-Start: Using the Cagan Discovery Skill

## What You Have

Four core documents:

1. **SKILL.md** - The skill definition
2. **frameworks/01-discovery-process.md** - Deep dive into discovery process + 4 risks
3. **guides/REFERENCES.md** - Maps Cagan's books/SVPG blog to frameworks
4. **guides/QUICK_START.md** - This file

---

## How to Deploy This

### In Claude Code

**Step 1:** Create the skill in your Claude Code environment

Simply have this repository available when you run Claude Code, and reference:

```text
I want to use the Cagan product discovery skill from /path/to/cagan-product-discovery

Project folder: /Users/me/projects/my-project
Problem hypothesis: [your hypothesis]
North Star: [your north star]

Can you help us validate and plan discovery?
```

### As a Claude Project

1. Create a new Claude Project: "Product Discovery (Cagan Framework)"
2. Upload all files from this repository
3. Set project instructions to load the skill

---

## Using It in Practice

### Scenario 1: Starting Fresh Discovery

```text
Project: /Users/me/projects/checkout-redesign
Problem hypothesis: Checkout has too many steps, causing abandonment
North Star: Reduce checkout steps from 5 to 3

We want to validate this hypothesis and then run discovery.
```

### Scenario 2: Already Have Interview Data

```text
Project: /Users/me/projects/checkout-redesign

We've done 20 customer interviews.
We have raw notes but haven't synthesized yet.

Can you help us find patterns?
```

### Scenario 3: Ready to Define Strategy

```text
Project: /Users/me/projects/checkout-redesign

Discovery is complete. Key findings: [your findings]
We want to define our strategy.
```

---

## What Gets Generated

The skill creates a project structure:

```tree
/project-folder/
├── discovery/
│   ├── 01-problem-validation.md
│   ├── 02-discovery-plan.md
│   ├── 03-interview-guide.md
│   └── notes/ (team adds notes here)
├── synthesis/
│   ├── 01-raw-insights.md
│   ├── 02-patterns-and-themes.md
│   └── 03-discovery-readout.md
└── strategy/
    ├── 01-okr-definition.md
    ├── 02-strategic-bet.md
    └── 03-discovery-to-delivery-handoff.md
```

Each document gets generated as both:
1. A saved file (for version control, sharing)
2. An artifact (for viewing/editing in Claude)

---

## Next Steps

1. Save this repository to GitHub
2. Use it with your next discovery work
3. Update REFERENCES.md as you read Cagan
4. Customize templates for your domain
5. Share with your product team

