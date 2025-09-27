# AI Specialist Technical Implementation Guide

## Overview

This guide provides step-by-step instructions for creating AI specialists from scratch using GitHub. After completing the [Product Planning Guide](product-planning-guide.md), follow these steps to build your specialist.

## Prerequisites

Before starting, ensure you have:
- GitHub account
- Git installed on your computer
- Text editor (VS Code, Sublime, or similar)
- Your completed Product Planning Guide

## Step 1: Create Repository Structure

### Initialize Your Repository

```bash
# Create a new directory for your specialist
mkdir my-specialist-name
cd my-specialist-name

# Initialize git repository
git init

# Create the required directory structure
mkdir -p configuration
mkdir -p content/ai-instructions
mkdir -p content/getting-started
mkdir -p protected-files

# Create placeholder file for protected-files (optional)
echo "# Protected Files\nPrivate configuration files go here" > protected-files/README.md
```

### Understanding the Structure

```
your-specialist/
├── configuration/          # Specialist metadata and settings
│   └── module.json        # REQUIRED: Defines your specialist
├── content/               # All specialist content
│   ├── README.md         # REQUIRED: User-facing documentation (auto-loaded)
│   ├── getting-started/   # OPTIONAL: User introduction (deleted after first use)
│   │   └── getting_to_know_this_specialist.md  # 3-5 min specialist introduction
│   ├── ai-instructions/   # REQUIRED: AI behavior programming
│   │   ├── getting_started.md  # REQUIRED: AI initialization (auto-loaded)
│   │   └── core-instructions.md # REQUIRED: Detailed AI programming
│   └── [your-domains]/   # Your custom content folders
└── protected-files/      # Optional: Private configurations
```

## Step 2: Configure Your Specialist

### Create `/configuration/module.json`

This file defines your specialist's identity and structure:

```json
{
  "module": {
    "id": "your-specialist-id",
    "name": "Your Specialist Name",
    "role": "Primary role and expertise description",
    "default-display-name": "Default Name for Users",
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
    "Key feature or capability 1",
    "Key feature or capability 2",
    "Key feature or capability 3",
    "Key feature or capability 4"
  ]
}
```

### Configuration Guidelines

**Module Section:**
- `id`: Unique identifier (lowercase, hyphens, no spaces)
- `name`: Short name for the specialist type
- `role`: Clear description of the specialist's primary role and expertise
- `default-display-name`: Default name shown to users (can be customized on import)
- `description`: One-line summary of specialist's purpose
- `version`: Semantic versioning (start with 1.0.0)

**Structure Section:**
- Map each content folder to its purpose
- Help users understand your organization
- Keep descriptions concise but clear

**Features Section:**
- List 3-5 core capabilities
- Focus on unique value propositions
- Use action-oriented language

### Real Example

Here's a complete example for a Development Manager specialist:

```json
{
  "module": {
    "id": "dev-manager",
    "name": "Development Manager",
    "role": "Sprint management and team coordination assistant",
    "default-display-name": "Dev Manager",
    "version": "1.0.0",
    "description": "Helps development teams track sprints, manage technical debt, and run effective standups",
    "created": "2025-09-27",
    "updated": "2025-09-27"
  },
  "structure": {
    "ai-instructions": "Sprint facilitation and team management behavior",
    "sprints": "Current and historical sprint tracking",
    "team": "Team member profiles and working patterns",
    "technical-debt": "Debt tracking and prioritization",
    "retrospectives": "Team learnings and process improvements"
  },
  "features": [
    "Context-aware standup facilitation",
    "Sprint progress and velocity tracking",
    "Technical debt identification and management",
    "Team pattern recognition and insights",
    "Blocker detection and resolution tracking"
  ]
}
```

## Step 3: Create Domain Structure

Based on your Product Planning Guide, create your domain-specific folders:

```bash
# Example for a fitness coach specialist
mkdir -p content/workouts
mkdir -p content/nutrition
mkdir -p content/progress
mkdir -p content/preferences

# Create README files to explain each folder's purpose
echo "# Workouts\nPersonalized exercise routines and training plans" > content/workouts/README.md
echo "# Nutrition\nMeal planning, dietary goals, and nutritional guidance" > content/nutrition/README.md
echo "# Progress\nFitness metrics, achievements, and progress tracking" > content/progress/README.md
echo "# Preferences\nUser's fitness style, constraints, and preferences" > content/preferences/README.md
```

### Domain Folder Best Practices

**Naming Conventions:**
- Use clear, descriptive names
- Lowercase with hyphens (kebab-case)
- Avoid abbreviations unless obvious

**Organization Principles:**
- **Make it self-explanatory**: Folder names should tell the AI what goes where
- Separate user data from reference material
- Keep related information together
- Include README files to explain purpose

**Design for AI Understanding:**
- `user-preferences/` is clearer than `prefs/`
- `current-projects/` is clearer than `work/`
- `progress-tracking/` is clearer than `progress/`
- The AI should understand your structure without extensive instructions

**Example Domain Structures:**

```
# Project Management Specialist
content/
├── projects/          # Active project tracking
├── team/             # Team member profiles
├── sprints/          # Sprint planning and tracking
├── retrospectives/   # Lessons and improvements
└── templates/        # Reusable project templates

# Learning Tutor Specialist
content/
├── subjects/         # Subject-specific content
├── study-plans/      # Personalized learning paths
├── progress/         # Learning metrics and achievements
├── resources/        # Educational materials
└── techniques/       # Study methods and strategies
```

## Step 4: Add Templates and Core Content

Create helpful templates and initial content for your specialist's domain:

**Remember**: Design your folder structure to be self-explanatory. The AI should understand what goes where just from the folder names and structure.

```bash
# Create templates directory
mkdir -p content/templates

# Add domain-specific templates
# Example for a project management specialist:
cat > content/templates/project-template.md << 'EOF'
# Project: [Name]

## Overview
- **Goal**:
- **Timeline**:
- **Priority**:

## Milestones
- [ ] Milestone 1:
- [ ] Milestone 2:
- [ ] Milestone 3:

## Resources
-

## Notes
-
EOF
```

### Core Content Guidelines

**Templates:**
- Create reusable structures for common tasks
- Include placeholders for user-specific information
- Keep templates simple and adaptable

**Reference Materials:**
- Add any domain-specific knowledge documents
- Include best practices or methodologies
- Create example workflows or processes

**Initial Structure:**
- Populate folders with at least README files
- Add any essential reference documents
- Create placeholder files for user data areas

## Step 5: Create User Documentation

### `/content/README.md` (Auto-Loaded First)

This is the user's first impression. Make it engaging and clear:

```markdown
# [Your Specialist Name] 🎯

[Compelling short-one-paragraph description of what your specialist does and why it's valuable]

## Core Capabilities

- **[Capability 1]**: [What it does and how it helps]
- **[Capability 2]**: [What it does and how it helps]
- **[Capability 3]**: [What it does and how it helps]

## How to Get Started

1. **First Step**: [What the user should do first]
2. **Share Context**: [What information to provide]
3. **Begin Using**: [How to start getting value]

---

**Ready to begin?** [Suggested first question or prompt for the user]
```

### Optional: Create User Introduction

If you want to provide a detailed introduction to your specialist (beyond the README), create:

#### `/content/getting-started/getting_to_know_this_specialist.md`

```markdown
# Getting to Know Your [Specialist Name]

*This is a 3-5 minute introduction to help you understand what makes this specialist special.*

## What Makes This Different

Unlike [generic alternatives], I'm designed to **remember everything about YOU**. While other tools start fresh every time, I build a comprehensive understanding of your preferences, patterns, and goals.

### The Power of Persistent Memory

**I Remember:**
- Your [domain-specific preferences]
- Your [working style/patterns]
- Your [goals and priorities]
- What works and what doesn't work for you

**I Learn Over Time:**
- [How the specialist adapts and improves]
- [Pattern recognition capabilities]
- [Personalization benefits]

**I Become Uniquely Yours:**
- [How it transforms the user experience]
- [Why this matters for your domain]
- [Specific examples of value]

## Your Journey with Me

### Week 1: Getting Acquainted
- [What happens in early interactions]
- [Initial learning and setup]

### Month 1: Finding Our Rhythm
- [How the relationship develops]
- [Improved recommendations and insights]

### Month 3+: True Partnership
- [Long-term value and capabilities]
- [Deep personalization examples]

## Getting Started

**Your First Steps:**
1. [Specific first action]
2. [What information to share]
3. [How to begin getting value]

**What to Expect:**
- [Initial experience description]
- [How quickly it improves]
- [When to see real benefits]

---

**Note**: This introduction folder will be removed once you're familiar with how I work, keeping your workspace clean and focused.
```

**Important**: This folder should be deleted after the user's first few interactions, once they understand the specialist's capabilities.

## Step 6: Program AI Behavior

Now that your structure and content are in place, create the AI instructions that can reference them.

### `/content/ai-instructions/getting_started.md` (Auto-Loaded)

Critical initialization instructions the AI reads first:

```markdown
# [Specialist Name] - Getting Started Instructions

## CRITICAL: Initialization Sequence

**You are a [domain] specialist designed to [primary purpose].**

### MANDATORY FIRST ACTIONS
1. **READ** `ai-instructions/core-instructions.md` for complete behavioral programming
2. **CHECK** existing user context in domain folders
3. **UNDERSTAND** the workspace structure and memory protocols
4. **NEVER** make assumptions - use stored context or ask for clarification

### YOUR IDENTITY
- **Role**: [Primary role and expertise]
- **Purpose**: [Main objective and value proposition]
- **Domain**: [Area of specialization]
- **Approach**: [How you interact and help]

### WORKSPACE STRUCTURE
Understand what each folder contains:
- `[folder-1]/`: [Purpose and what's stored here]
- `[folder-2]/`: [Purpose and what's stored here]
- `ai-instructions/`: Your behavior guidelines and protocols

### FIRST INTERACTION PROTOCOL (THIS SHOULD BE REMOVED AFTER FIRST INTERACTON)
When meeting a new user:
1. Introduce your role and capabilities
2. Understand their specific needs and context
3. Begin building their profile
4. Set clear expectations for ongoing interactions
5. Demonstrate immediate value

### MEMORY MANAGEMENT RULES
- **Update immediately**: User preferences, feedback, and important context
- **Reference consistently**: Past conversations and established patterns
- **Organize clearly**: Keep information findable and relevant
- **Evolve appropriately**: Adapt based on user feedback

---

**CRITICAL**: Now read `ai-instructions/core-instructions.md` for complete programming
```

### `/content/ai-instructions/core-instructions.md`

**IMPORTANT**: Keep this extremely simple and focused. Your folder structure should be logical enough that the AI can understand how to work without extensive instructions. Only include truly core, essential information.

**Minimalist Template (use only what you need):**

```markdown
# [Specialist Name] - Core Instructions

## Identity
You are a [role] helping with [specific domain/task].

## Key Behaviors
- [Essential behavior 1]
- [Essential behavior 2]
- [Essential behavior 3]

## Memory Protocol
Update files when user shares:
- [What type of info goes where - be specific about folders]

## Communication
[Brief description of tone/style - 1-2 sentences max]

---
*Keep it simple - let the folder structure guide the AI*
```

**Advanced Template (only if domain requires specific workflows):**

```markdown
# [Specialist Name] - Core Instructions

## Identity & Purpose
You are a [role] specializing in [domain]. Your purpose is to [main objective].

## Core Capabilities
1. [Capability 1]
2. [Capability 2]
3. [Capability 3]

## Memory Management
- **User info** → `[folder]/`
- **Current work** → `[folder]/`
- **Progress** → `[folder]/`

## Key Workflow
**[Primary Process Name]**
1. [Step 1]
2. [Step 2]
3. [Step 3]

## Communication Style
[Brief tone/approach description]

---
*Version: 1.0.0*
```

## Step 7: Finalize Repository

### Create Repository README

```bash
cat > README.md << 'EOF'
# [Your Specialist Name]

AI specialist for [domain/purpose]. Import this into Magic Context or AI Specialists Hub to get started.

## Features
- [Feature 1]
- [Feature 2]
- [Feature 3]
- [Feature 4]

## Structure
- `/configuration/` - Specialist configuration
- `/content/` - All specialist content and instructions
- `/protected-files/` - Private configuration (optional)

## Getting Started
1. Import this repository into your Magic Context platform
2. [First interaction suggestion]
3. Begin experiencing personalized AI assistance

## Repository
Created for use with Magic Context and AI Specialists Hub platforms.

## License
[Your chosen license]
EOF
```

### Initialize Git and Create Repository

```bash
# Add all files to git
git add .

# Create initial commit
git commit -m "Initial specialist creation: [Your Specialist Name]"

# Create GitHub repository (using GitHub CLI)
gh repo create your-specialist-name --public --source=. --remote=origin --push

# Or manually create on GitHub and push:
# 1. Create new repository on GitHub
# 2. Add remote: git remote add origin https://github.com/yourusername/your-specialist-name.git
# 3. Push: git push -u origin main
```

## Step 8: Import to Platform

### Import Your Specialist

Once your repository is on GitHub:

1. **Get your repository URL**: `https://github.com/yourusername/your-specialist-name`
2. **Use platform import**: Use the Magic Context or AI Specialists Hub import function
3. **Verify import**: Check that all files loaded correctly
4. **Test interaction**: Start a conversation to verify behavior

## Step 9: Testing and Validation

### Initial Testing Checklist

- [ ] **Repository Structure**: All required folders and files present
- [ ] **Configuration Valid**: module.json properly formatted
- [ ] **README Displays**: User documentation shows correctly
- [ ] **AI Initializes**: getting_started.md loads and executes
- [ ] **Core Instructions Work**: AI follows core-instructions.md
- [ ] **Domain Folders Accessible**: AI can read/write to domain folders
- [ ] **Memory Persists**: Information saved across sessions

### Behavior Testing

1. **First Interaction Test**
   - Does the specialist introduce itself properly?
   - Does it ask appropriate initial questions?
   - Does it start building user context?

2. **Memory Persistence Test**
   - Provide specific preferences or information
   - End session and start new one
   - Verify specialist remembers previous information

3. **Domain Expertise Test**
   - Ask domain-specific questions
   - Verify specialist applies correct methodology
   - Check that responses are personalized

4. **Edge Case Testing**
   - Test with unclear requests
   - Verify error handling
   - Check boundary conditions

### Iteration Process

1. **Identify Issues**: Note any problems during testing
2. **Update Files**: Modify instructions or structure as needed
3. **Commit Changes**: Push updates to GitHub
4. **Re-import**: Update specialist in platform
5. **Re-test**: Verify improvements

## Step 10: Maintenance and Evolution

### Version Management

```bash
# When making updates:
# 1. Update version in module.json
# 2. Commit with clear message
git commit -m "v1.1.0: Add new workout templates and improve memory management"

# 3. Tag release
git tag v1.1.0

# 4. Push updates
git push origin main --tags
```

### Continuous Improvement

**Regular Reviews:**
- Weekly: Check user feedback and interaction quality
- Monthly: Review and optimize memory organization
- Quarterly: Major feature additions or restructuring

**Documentation Updates:**
- Keep README current with new features
- Update AI instructions based on learnings
- Document any special considerations

## Troubleshooting

### Common Issues and Solutions

**Issue: AI doesn't follow instructions**
- Verify getting_started.md syntax and clarity
- Check core-instructions.md for conflicts
- Ensure instructions are specific and actionable

**Issue: Memory doesn't persist**
- Verify folder structure is correct
- Check that AI has clear update instructions
- Ensure memory update protocol is defined

**Issue: Responses too generic**
- Add more specific domain knowledge
- Enhance personalization instructions
- Include more examples in core instructions

**Issue: User confusion**
- Improve README.md clarity
- Simplify initial interaction flow
- Add clearer capability descriptions

---

## Quick Start Alternative

**Note**: If you want to quickly prototype or have a very similar use case to an existing specialist, you can:

1. Find an existing specialist on GitHub
2. Fork or download their repository
3. Replace the content while maintaining the structure
4. Update configuration and documentation
5. Test and deploy

This approach is faster but less customized. The full creation process above gives you complete control and understanding of your specialist.

---

**For Support**: Refer to the Magic Context documentation or community resources for additional help.
