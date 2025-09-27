# AI Specialist Technical Implementation Guide

## Overview

This guide provides step-by-step instructions for creating AI specialists using GitHub and the Magic Context platform. After completing the [Product Planning Guide](product-planning-guide.md), use this to build your specialist.

## Two Creation Methods

### Method A: Quick Start (Modify Existing)
Best for: Learning, prototyping, similar use cases

### Method B: GitHub Creation (Recommended)
Best for: Original specialists, full control, sharing with others

---

## Method A: Quick Start (Modify Existing)

### Step 1: Find a Similar Specialist
```bash
# List available specialist types
# Look for one with similar domain or structure
```

Examples of existing types:
- `personal-effectiveness-v1` - Good for productivity/planning specialists
- `game-collection-manager` - Good for collection/tracking specialists
- `dnd-character-development` - Good for creative/gaming specialists

### Step 2: Import and Modify
1. Import the similar specialist
2. Navigate to its workspace
3. Replace content in key files:
   - `/content/README.md`
   - `/content/ai-instructions/getting_started.md`
   - `/content/ai-instructions/core-instructions.md`
4. Add your domain-specific folders

### Step 3: Test and Iterate
- Interact with your specialist
- Verify it behaves as expected
- Refine the AI instructions based on testing

---

## Method B: GitHub Creation (Recommended)

### Prerequisites
- GitHub account
- Git installed
- Text editor (VS Code, etc.)

### Step 1: Repository Setup

```bash
# Create new repository
mkdir my-specialist-name
cd my-specialist-name
git init

# Create required directory structure
mkdir -p configuration
mkdir -p content/ai-instructions
mkdir -p protected-files
```

### Step 2: Create Configuration Files

#### `/configuration/module.json`
```json
{
  "module": {
    "id": "your-specialist-id",
    "name": "Your Specialist Name",
    "version": "1.0.0",
    "description": "Brief description of what your specialist does",
    "created": "2025-09-27",
    "updated": "2025-09-27"
  },
  "structure": {
    "ai-instructions": "Core AI behavior and guidance",
    "your-domain-folder": "Description of what this folder contains",
    "another-folder": "Description of another folder"
  },
  "features": [
    "Key feature 1",
    "Key feature 2",
    "Key feature 3"
  ]
}
```

**Key Points:**
- `id` must be unique and lowercase with hyphens
- `structure` section describes each content folder's purpose
- `features` list helps users understand capabilities

### Step 3: Create Auto-Loaded Files

#### `/content/README.md` (Auto-loaded by platform)
This is the user's first impression. Include:

```markdown
# Your Specialist Name

Brief description of what this specialist does and why it's useful.

## What You'll Get

- Key benefit 1
- Key benefit 2
- Key benefit 3

## How to Get Started

1. First interaction suggestion
2. What to expect in early conversations
3. How it will learn about you

## Features

- Feature 1: Description
- Feature 2: Description
- Feature 3: Description

---

Ready to begin? [Suggested first question or action]
```

#### `/content/ai-instructions/getting_started.md` (Auto-loaded by platform)
Critical AI initialization instructions:

```markdown
# [Specialist Name] - Getting Started Instructions

## CRITICAL: Read Before Any Response

**You are a [domain] specialist designed to [primary purpose].**

### MANDATORY STARTUP SEQUENCE
1. **Read** `ai-instructions/core-instructions.md` for complete behavior
2. **Check** user's existing context in relevant folders
3. **Never** assume user knowledge - always personalize based on stored context

### WORKSPACE OVERVIEW
- `folder-1/`: Purpose and what's stored here
- `folder-2/`: Purpose and what's stored here
- `ai-instructions/`: Your behavior and memory protocols

### FIRST INTERACTION PRIORITIES
1. Understand user's context and goals
2. Begin building their profile
3. Demonstrate your specialized knowledge
4. Set expectations for ongoing relationship

### MEMORY PROTOCOLS
- **Update immediately**: When user provides preferences or feedback
- **Reference frequently**: Past conversations and established patterns
- **Organize clearly**: Keep information findable and relevant

---

**NOW READ**: `ai-instructions/core-instructions.md` for complete programming
```

### Step 4: Create Core Instructions

#### `/content/ai-instructions/core-instructions.md`
Comprehensive AI programming:

```markdown
# [Specialist Name] - Core Instructions

## Specialist Identity

### Primary Role
You are a [domain] specialist providing [specific service] through persistent memory and specialized expertise.

### Core Purpose
Your purpose is to [main objective] by:
- Key capability 1
- Key capability 2
- Key capability 3

### Expertise Areas
- Domain area 1: Brief description
- Domain area 2: Brief description
- Domain area 3: Brief description

## Memory Management

### Memory Hierarchy
**Immediate Context** (Current session):
- Active conversation topics
- Immediate goals and tasks

**Personal Profile** (Long-term):
- User preferences and patterns
- Established goals and priorities
- Success factors and challenges

**Domain Knowledge** (Permanent):
- Frameworks and methodologies
- Best practices and templates
- Reference materials

### Memory Update Rules
**Always update when user:**
- States explicit preferences
- Provides feedback on recommendations
- Shares important context about their situation
- Corrects previous information

**Update locations:**
- Personal preferences → `preferences/` folder
- Goal information → `goals/` folder
- Progress tracking → `progress/` folder

## Communication Style

### Tone & Approach
- [Define your specialist's personality]
- [Response length preferences]
- [Level of formality]

### Response Structure
1. **Acknowledge Context**: Reference relevant previous information
2. **Apply Expertise**: Provide domain-specific guidance
3. **Personalize**: Adapt based on user's patterns
4. **Request Feedback**: Ask for input when appropriate

## Domain Methodology

### Primary Framework
[Describe the main approach/methodology your specialist uses]

### Key Workflows
1. **[Workflow 1]**: Step-by-step process
2. **[Workflow 2]**: Step-by-step process
3. **[Workflow 3]**: Step-by-step process

### Assessment Process
1. Understand current situation
2. Apply domain framework
3. Customize based on user patterns
4. Provide specific recommendations
5. Track outcomes and adjust

## Quality Standards

### Response Quality
Your responses should demonstrate:
- **Context Awareness**: Reference relevant previous information
- **Expertise Application**: Apply domain knowledge effectively
- **Personalization**: Show understanding of user preferences
- **Actionability**: Provide specific, implementable guidance

### Continuous Improvement
- Track what recommendations work
- Learn from user feedback
- Refine understanding over time
- Maintain organization of stored information

---

*Last updated: [Date]*
*Version: 1.0.0*
```

### Step 5: Create Domain Structure

Create folders based on your planning:

```bash
# Example for fitness coach
mkdir -p content/workouts
mkdir -p content/nutrition
mkdir -p content/progress
mkdir -p content/preferences

# Add README files to explain each folder
echo "# Workouts\nPersonalized exercise routines and tracking" > content/workouts/README.md
echo "# Nutrition\nMeal planning and dietary goals" > content/nutrition/README.md
echo "# Progress\nFitness metrics and achievements" > content/progress/README.md
echo "# Preferences\nPersonal fitness style and constraints" > content/preferences/README.md
```

### Step 6: Add Templates and Examples

Create helpful templates for your domain:

```bash
# Example templates
mkdir -p content/templates
```

Add templates specific to your specialist's domain.

### Step 7: Repository Finalization

```bash
# Add README for the repository
echo "# [Specialist Name]

AI specialist for [domain]. Import this into Magic Context to get started.

## Features
- Feature 1
- Feature 2
- Feature 3

## Getting Started
1. Import this specialist
2. [First interaction suggestion]
3. Begin using specialized features" > README.md

# Commit everything
git add .
git commit -m "Initial specialist creation"

# Push to GitHub
gh repo create your-specialist-name --public
git push -u origin main
```

### Step 8: Import to Platform

```bash
# Import your specialist using the GitHub URL
# Use the platform's import functionality
```

## Testing Your Specialist

### Initial Testing Checklist
- [ ] Specialist loads without errors
- [ ] README.md displays correctly to users
- [ ] AI follows getting_started.md instructions
- [ ] Core instructions work as intended
- [ ] Memory updates properly when you provide information
- [ ] Domain-specific folders are accessible

### Behavior Testing
1. **Start a conversation** with your specialist
2. **Provide personal information** (preferences, goals, etc.)
3. **Check memory persistence** across sessions
4. **Test domain expertise** with specific questions
5. **Verify personalization** based on stored context

### Iteration Process
1. **Identify issues** through testing
2. **Update files** directly in platform or GitHub
3. **Test changes** with new conversations
4. **Refine instructions** based on performance
5. **Document improvements** for future reference

## Troubleshooting Common Issues

### Specialist Doesn't Follow Instructions
- Check `getting_started.md` is properly formatted
- Ensure `core-instructions.md` is clear and specific
- Verify file paths are correct

### Memory Not Persisting
- Confirm memory update rules are clear
- Check folder structure matches your design
- Verify AI is updating the correct files

### Responses Too Generic
- Add more specific domain knowledge
- Include more examples in instructions
- Refine the communication style guidelines

### User Experience Issues
- Review `README.md` for clarity
- Improve first interaction suggestions
- Add better onboarding guidance

## Maintenance and Updates

### Regular Maintenance
- **Weekly**: Review specialist performance and user feedback
- **Monthly**: Update domain knowledge and best practices
- **Quarterly**: Assess overall effectiveness and major improvements

### Version Control
- Use semantic versioning (1.0.0, 1.1.0, 2.0.0)
- Document changes in commit messages
- Tag releases for major updates

### Sharing and Collaboration
- Keep repository public for community benefit
- Document usage examples and success stories
- Accept contributions and feedback from users

---

## Next Steps

1. **Complete your specialist** using this guide
2. **Test thoroughly** with real use cases
3. **Share with others** who might benefit
4. **Iterate and improve** based on feedback

**Remember**: The best specialists evolve over time. Start with a solid foundation and continuously improve based on real-world usage.

---

*For questions or support, refer to the Magic Context documentation or community resources.*