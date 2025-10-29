# Getting Started with AI Product Owner Tool

Welcome! This tool transforms GitHub Copilot into your AI Product Owner assistant, helping you take ideas from concept to structured, documented product plans.

## What This Tool Does

The AI Product Owner Tool helps you:

- **Define and refine product ideas** through structured conversation  
- **Save context automatically** - Never lose important details  
- **Create comprehensive development plans** with architecture and timeline  
- **Generate organized epics and features** in numbered markdown files  
- **Maintain clear documentation** throughout the entire planning process  

## Quick Start

### 1. Present Your Idea

Simply start a conversation with GitHub Copilot about your product idea. You can be as brief or detailed as you like:

**Examples:**
- "I want to build a task management app"
- "I have an idea for a fitness tracking platform"
- "I'm thinking about creating a tool to help developers with code reviews"

### 2. Answer the Discovery Questions

Copilot will ask you clarifying questions to understand your idea better. These questions will cover:

- **Problem & Solution**: What problem are you solving?
- **Target Users**: Who will use this product?
- **Key Features**: What capabilities are needed?
- **Success Criteria**: How will you measure success?
- **Technical Constraints**: Any specific requirements or limitations?
- **Timeline & Priority**: When do you need this?

**Important:** All questions and your answers are automatically saved to `docs/discovery/questions-and-answers.md`

### 3. Review the Development Plan

After gathering information, Copilot will create a comprehensive plan including:

- Project overview and objectives
- Recommended technical architecture
- Development phases and milestones
- Technology stack suggestions
- Risk assessment
- Resource requirements

This plan is saved to `docs/planning/development-plan.md`

### 4. Explore Epics and Features

Copilot will break down your project into:

- **Epics** (major themes of work): `docs/epics/01-epic-name.md`, `02-epic-name.md`, etc.
- **Features** (specific capabilities): `docs/features/01-feature-name.md`, `02-feature-name.md`, etc.

Each document includes user stories, acceptance criteria, technical details, and dependencies.

## How to Get the Best Results

### 💡 Effective Prompts

**Good prompts that trigger the workflow:**

```
"Help me plan a mobile app for meal planning"

"I want to create a SaaS product for small business invoicing"

"Let's work on defining a developer tool for API documentation"

"I need help planning a marketplace platform"
```

**What happens next:**
- Copilot immediately starts asking clarifying questions
- Your conversation is documented automatically
- A structured plan emerges from your discussion

### 🎯 During Discovery

**Be conversational and honest:**
- Answer questions thoroughly but naturally
- Say "I'm not sure" if you don't know something
- Ask Copilot to explain if a question is unclear
- Let Copilot guide you through the exploration

**Example conversation:**

```
You: "I want to build a task management app"

Copilot: "Great! Let me understand your idea better. What specific 
problem with existing task management tools are you trying to solve?"

You: "Most task apps are too complex. I want something simple that just 
focuses on daily priorities"

Copilot: [Saves your answer] "That's helpful! Who is your target user?"

You: "Busy professionals who get overwhelmed by feature-heavy apps"

[Conversation continues...]
```

### 📝 Reviewing Generated Plans

When Copilot presents plans, epics, or features:

**Provide feedback like:**
- "Epic 3 seems too large, can we break it down?"
- "Feature 5 should be higher priority"
- "Add a feature for user authentication"
- "The timeline for Epic 2 seems too aggressive"

Copilot will update the documentation based on your feedback.

### 🔄 Iterating on Existing Projects

To continue working on a previous project:

```
"Let's continue working on the [project name]"

"I want to add more features to the task management app we planned"

"Can we revise Epic 2 from our previous planning session?"

"Show me the current development plan"
```

Copilot will read existing documentation and continue where you left off.

## File Structure Overview

Your project documentation will be organized like this:

```
docs/
├── discovery/
│   ├── questions-and-answers.md    # All Q&A exchanges with timestamps
│   └── research-notes.md            # Additional research and insights
│
├── planning/
│   ├── development-plan.md          # Comprehensive project plan
│   └── architecture-decisions.md   # Technical architecture notes
│
├── epics/
│   ├── 01-user-authentication.md   # Epic 1: User auth & accounts
│   ├── 02-core-features.md         # Epic 2: Main functionality
│   ├── 03-data-management.md       # Epic 3: Data handling
│   └── ...
│
└── features/
    ├── 01-user-registration.md     # Feature 1: Sign up flow
    ├── 02-login-system.md          # Feature 2: Login capability
    ├── 03-password-reset.md        # Feature 3: Password recovery
    └── ...
```

## Common Workflows

### Starting a New Project

1. **Introduce your idea** in a single sentence
2. **Answer discovery questions** - Copilot will ask 5-10 questions
3. **Review the plan** - Copilot generates a development plan
4. **Confirm or refine** - Give feedback on the plan
5. **Explore epics** - Copilot creates epic documents
6. **Review features** - Copilot breaks epics into features
7. **Prioritize and adjust** - Reorder or modify as needed

### Refining an Existing Idea

```
"I want to add [new capability] to the [project name]"

"Can we reconsider the technology stack for Epic 3?"

"Let's add a new epic for mobile support"

"Feature 7 needs more detail around authentication"
```

### Getting Specific Information

```
"Show me all high-priority features"

"What features depend on Epic 2?"

"Summarize the risks in our development plan"

"Which features can we build in parallel?"

"What's the estimated timeline for Epic 1?"
```

### Exploring Alternatives

```
"What if we used a different tech stack?"

"Can you suggest alternatives to Feature 5?"

"How would this change if we targeted enterprises instead?"

"What would a MVP version look like?"
```

## Understanding the Templates

### Epic Structure

Each epic file contains:
- **Status & Priority** - Current state and importance
- **Description** - What this epic encompasses
- **Business Value** - Why this matters
- **Acceptance Criteria** - How to know it's complete
- **Features List** - All features within this epic
- **Technical Considerations** - Architecture notes
- **Risks & Mitigation** - What could go wrong
- **Success Metrics** - How to measure success

### Feature Structure

Each feature file contains:
- **Epic Reference** - Which epic it belongs to
- **User Stories** - "As a... I want... So that..."
- **Acceptance Criteria** - Specific requirements
- **Technical Details** - Implementation notes
- **Dependencies** - What must be done first
- **Testing Requirements** - How to verify it works
- **Definition of Done** - Completion checklist

## Tips for Success

### ✅ Do's

- **Start simple** - A one-sentence idea is enough to begin
- **Be responsive** - Answer Copilot's questions thoroughly
- **Ask for clarification** - If something's unclear, speak up
- **Iterate freely** - Change your mind, refine ideas, explore alternatives
- **Trust the process** - Let Copilot guide the discovery
- **Review regularly** - Check generated docs and provide feedback

### ❌ Don'ts

- **Don't skip questions** - Each answer adds important context
- **Don't rush** - Take time to think through answers
- **Don't assume** - If Copilot asks, there's a reason
- **Don't ignore generated docs** - Review and refine them
- **Don't treat it as one-way** - This is a conversation

## Example: Complete Session

Here's what a typical session looks like:

```
You: "I want to build a Chrome extension for productivity"

Copilot: "Excellent! Let me help you refine this idea. I'll ask some 
questions and save our conversation. What specific productivity problem 
does this extension solve?"

You: "I want to block distracting websites during work hours"

Copilot: [Saves to docs/discovery/questions-and-answers.md]
"Great! Who is your target user?"

You: "Remote workers and students who struggle with focus"

Copilot: "Perfect. What are the key features you envision?"

You: "Website blocking, scheduling, and usage analytics"

[5-7 more questions...]

Copilot: "Based on our conversation, I'm creating a development plan..."
[Creates docs/planning/development-plan.md]

Copilot: "I've identified 4 main epics:
1. Core Blocking Engine
2. Scheduling System
3. Analytics Dashboard
4. User Settings & Customization

Shall I create detailed epic documents?"

You: "Yes, please"

Copilot: [Creates docs/epics/01-core-blocking-engine.md through 04-...]

Copilot: "I'm now breaking down each epic into features..."
[Creates docs/features/01-... through 18-...]

Copilot: "I've created a complete plan with 4 epics and 18 features. 
Your development plan suggests a 12-week timeline. Would you like to 
review any specific epic or feature?"

You: "Show me Epic 1"

Copilot: [Displays Epic 1 content]

You: "This looks good! What's the MVP version?"

Copilot: "For MVP, I recommend focusing on Features 1, 2, 3, 5, and 7..."
```

## Troubleshooting

### "Copilot isn't asking questions"

Try being more explicit:
```
"Help me plan this project by asking discovery questions"
"Let's start the product owner workflow for [idea]"
```

### "The generated plan is too generic"

Provide more specific answers:
```
"Let me give you more context about [topic]"
"Can you ask me more about [specific area]?"
```

### "I want to change something in the plan"

Just ask:
```
"Can we revise Epic 3?"
"I want to change the priority of Feature 8"
"Let's update the technology stack in the development plan"
```

### "Where are my files?"

All documentation is in the `docs/` folder:
```
"Show me the questions and answers file"
"Open the development plan"
"List all epics"
"What features are in Epic 2?"
```

## Next Steps

Ready to get started? Simply open GitHub Copilot Chat and say:

```
"I have an idea for [brief description]. Help me plan it out."
```

Copilot will take it from there! 🚀

---

**Need help?** Just ask Copilot:
- "How does this product owner workflow work?"
- "Show me an example of how to start"
- "What questions will you ask me?"
- "Can you explain the file structure?"