# AI Specialist Product Planning Guide

## Overview

This guide helps you design an effective AI specialist by focusing on core product design concepts. Use this to plan what you want to build before jumping into technical implementation.

## 📝 Save Your Planning Work

**As you work through this guide, save your answers in your workspace:**

1. **Create a new specialist folder**: Ask me to "create a new specialist planning folder for [your-specialist-name]"
2. **Use the planning template**: I'll set up a structured template for capturing all your planning decisions
3. **Work iteratively**: We can refine and update your plan as you work through each step

This ensures your planning work is saved and can be referenced during technical implementation.

## Learn from Existing Examples

Before starting, explore these existing specialists on GitHub for inspiration:

### Official Examples
- **[Personal Effectiveness (Friday)](https://github.com/erikashby/Friday-Personal-Planning)** - Personal productivity and planning assistant
- **[Game Collection Manager](https://github.com/magic-context/game-collection-manager)** - Collection tracking and wishlist management
- **[D&D Character Development](https://github.com/magic-context/dnd-character-development)** - Character creation and campaign management
- **[Specialist Creator Workshop](https://github.com/magic-context/creator)** - This workshop itself is a specialist!

### What to Look For
When reviewing these examples, pay attention to:
- How they structure their `/configuration/module.json`
- The tone and content of their `/content/README.md`
- How they organize domain-specific folders
- Their approach to AI instructions in `getting_started.md`

## Step 1: Define Your Specialist's Purpose

### Core Problem & Solution
**What specific problem will your specialist solve?**
- Be specific: "Help developers manage technical debt" vs "Help with programming"
- Focus on one domain: Avoid trying to solve everything
- Consider why AI + memory makes this better than regular AI assistance

**Examples:**
- ❌ Too broad: "Help with business"
- ✅ Focused: "Track and prioritize technical debt across sprints"
- ✅ Focused: "Manage personal fitness goals and workout planning"

### Primary Role & Capabilities
**Define your specialist's main role:**
- What is the specialist's primary identity? (e.g., "Fitness Coach", "Technical Debt Manager", "Daily Standup Facilitator")
- Who does it serve? (e.g., developers, managers, individuals, teams)
- What domain expertise does it embody?

**Core Capabilities (3-5 key abilities):**
List the main things your specialist can do:
- Capability 1: Specific action or service
- Capability 2: Specific action or service
- Capability 3: Specific action or service

**Example - Development Manager:**
- **Role**: Project management assistant for development teams
- **Capabilities**:
  - Track sprint progress and team velocity
  - Identify and manage technical blockers
  - Generate context-aware standup questions
  - Provide team performance insights
  - Maintain architectural decision records

### Unique Value of Persistent Memory
**Why does memory matter for this use case?**
- What context should it remember about users?
- How will it get smarter over time?
- What patterns will it recognize?

**Example - Fitness Coach:**
- Remembers: Exercise preferences, past injuries, progress metrics
- Gets smarter: Learns what motivates you, adjusts based on results
- Recognizes: When you're likely to skip workouts, what exercises you enjoy

## Step 2: Design the User Experience

### Communication Style
**How should your specialist "talk"?**
- Professional, friendly, direct, encouraging?
- Short responses or detailed explanations?
- Formal or casual tone?

### Interaction Patterns
**How will users typically interact with it?**
- Daily check-ins vs occasional deep sessions?
- Question-answer or proactive suggestions?
- Structured workflows or free-form conversation?

### Personalization Approach
**How will it adapt to individual users?**
- What user preferences matter most?
- How will it learn and adjust over time?
- What should stay consistent vs change?

## Step 3: Plan the Memory Architecture

### What to Remember About Users
**Core User Information:**
- Role/context (developer, manager, student, etc.)
- Communication preferences
- Success patterns and challenges
- Goals and priorities

**Domain-Specific Context:**
- Current projects or focus areas
- Historical patterns and progress
- Preferences within the domain
- Important background information

### Knowledge vs Memory Separation
**Specialist Knowledge (Same for Everyone):**
- Domain expertise and best practices
- Frameworks and methodologies
- Templates and workflows
- Reference materials

**Personal Memory (Unique Per User):**
- Individual preferences and patterns
- Personal goals and progress
- Interaction history and feedback
- Customized approaches

## Step 4: Content Architecture Planning

### Auto-Loaded Files (Critical First Impression)
**README.md** - What users see first:
- Clear explanation of what the specialist does
- How to get started
- What to expect

**ai-instructions/getting_started.md** - AI's first instructions:
- Core behavior rules
- How to interact with users
- Key capabilities overview

### Domain Structure Planning
**What content areas will you need?**

Example structures:
```
# Fitness Coach
├── workouts/          # Exercise routines and tracking
├── nutrition/         # Meal planning and goals
├── progress/          # Metrics and achievements
└── preferences/       # Personal workout style

# Technical Debt Manager
├── debt-tracking/     # Current technical debt items
├── prioritization/    # Frameworks for ranking debt
├── sprint-planning/   # Integration with development cycles
└── team-context/      # Team preferences and patterns
```

### Memory Flow Design
**How will information flow through your specialist?**

1. **Initial Setup**: What does it need to learn first?
2. **Daily Usage**: What gets updated regularly?
3. **Long-term Evolution**: How does understanding deepen?

## Step 5: Success Planning

### User Experience Goals
**How will you know it's working well?**
- Users save time compared to starting fresh each session
- Recommendations become more relevant over time
- Users proactively seek its input
- Context continuity enhances rather than interrupts assistance

### Specialist Effectiveness
**What makes this specialist successful?**
- Accurate context recall in responses
- Appropriate adaptation to user feedback
- Consistent application of domain expertise
- Progressive improvement in assistance quality

## Step 6: Implementation Readiness Checklist

Before moving to technical implementation, ensure you have:

- [ ] **Clear purpose**: One-sentence description of what it does
- [ ] **Primary role**: The specialist's identity and domain expertise
- [ ] **Core capabilities**: 3-5 key abilities that define what it can do
- [ ] **Target user**: Specific role/context it serves
- [ ] **Memory requirements**: What it needs to remember and why
- [ ] **Communication style**: How it should interact
- [ ] **Content structure**: Planned folders and organization
- [ ] **Success metrics**: How you'll know it's working

## Example: Complete Planning Summary

**Specialist: Personal Fitness Coach**

**Purpose**: Help individuals plan, track, and optimize their fitness journey through personalized workout and nutrition guidance.

**Role**: Personal fitness coach and wellness advisor

**Core Capabilities**:
- Create personalized workout plans based on goals and constraints
- Track progress metrics and adjust programs accordingly
- Provide nutrition guidance aligned with fitness goals
- Identify patterns in motivation and adherence
- Suggest recovery strategies and injury prevention

**Target User**: Busy professionals wanting structured fitness routines

**Memory Focus**:
- Exercise preferences and physical limitations
- Schedule constraints and workout timing
- Progress metrics and motivation patterns
- Nutrition goals and dietary restrictions

**Communication Style**: Encouraging but realistic, practical advice, celebrates progress

**Content Structure**:
- `/workouts/` - Personalized exercise routines
- `/nutrition/` - Meal planning and tracking
- `/progress/` - Metrics and achievements
- `/preferences/` - Personal style and constraints

**Success Metrics**:
- Workouts consistently match user's schedule and preferences
- Nutrition suggestions align with goals and restrictions
- Progress tracking shows improvements over time
- User feels motivated and supported

## Next Steps

Once your planning is complete, proceed to the [Technical Implementation Guide](technical-implementation-guide.md) to build your specialist.

---

**Remember**: Good planning prevents problems during implementation. Take time to think through these concepts before coding.