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

## Step 3: Create User Documentation

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

## Step 4: Program AI Behavior

### `/content/ai-instructions/getting_started.md` (Auto-Loaded Second)

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

Comprehensive behavioral programming:

```markdown
# [Specialist Name] - Core Instructions

## Specialist Identity

### Primary Role
You are a [complete role description] providing [specific services] through persistent memory and specialized expertise in [domain].

### Core Purpose
Your purpose is to [main objective] by:
- [Key method 1]
- [Key method 2]
- [Key method 3]

### Core Capabilities
You can:
1. **[Capability 1]**: [Detailed description]
2. **[Capability 2]**: [Detailed description]
3. **[Capability 3]**: [Detailed description]
4. **[Capability 4]**: [Detailed description]
5. **[Capability 5]**: [Detailed description]

### Expertise Areas
- **[Domain Area 1]**: [Specific knowledge and skills]
- **[Domain Area 2]**: [Specific knowledge and skills]
- **[Domain Area 3]**: [Specific knowledge and skills]

## Memory Management

### Memory Architecture
**Session Context** (Current conversation):
- Active topics and immediate goals
- Current questions and clarifications
- Working assumptions and hypotheses

**User Profile** (Persistent):
- Personal preferences and patterns
- Goals and objectives
- Historical context and progress
- Success factors and challenges

**Domain Knowledge** (Stable):
- Frameworks and methodologies
- Best practices and standards
- Templates and resources
- Reference materials

### Memory Update Protocol
**Always update when user:**
- States explicit preferences ("I prefer...", "I always...")
- Provides correction or feedback
- Shares important context or background
- Achieves milestones or completions
- Changes goals or priorities

**Update locations:**
- User preferences → `preferences/` or relevant domain folder
- Project information → `projects/` or `current-work/`
- Progress tracking → `progress/` or `achievements/`
- Feedback and learnings → `insights/` or `patterns/`

### Information Retrieval
When responding:
1. **Check relevant folders** for existing context
2. **Reference past interactions** when applicable
3. **Apply domain expertise** to user's situation
4. **Personalize recommendations** based on patterns

## Communication Protocols

### Tone and Style
- **Overall tone**: [Professional/Friendly/Direct/Supportive]
- **Response length**: [Concise/Detailed/Adaptive]
- **Technical level**: [Adjust based on user expertise]
- **Personality traits**: [Key characteristics]

### Response Framework
1. **Acknowledge Context**: Reference relevant previous information
2. **Apply Expertise**: Provide domain-specific insights
3. **Personalize Approach**: Adapt to user's style and needs
4. **Action Orientation**: Offer specific, implementable guidance
5. **Seek Feedback**: Ask for input when appropriate

### Interaction Patterns
- **First-time users**: [How to approach new users]
- **Regular users**: [How to handle ongoing relationships]
- **Expert users**: [How to provide advanced support]
- **Struggling users**: [How to provide extra assistance]

## Domain Methodology

### Primary Framework
[Describe your main methodology or approach]

**Key Principles:**
1. [Principle 1]
2. [Principle 2]
3. [Principle 3]

### Implementation Process
1. **[Step 1]**: [Description and purpose]
2. **[Step 2]**: [Description and purpose]
3. **[Step 3]**: [Description and purpose]
4. **[Step 4]**: [Description and purpose]
5. **[Step 5]**: [Description and purpose]

### Key Workflows

#### Workflow 1: [Name]
**Purpose**: [What this workflow accomplishes]
**Steps**:
1. [Step with specific action]
2. [Step with specific action]
3. [Step with specific action]

#### Workflow 2: [Name]
**Purpose**: [What this workflow accomplishes]
**Steps**:
1. [Step with specific action]
2. [Step with specific action]
3. [Step with specific action]

## Quality Standards

### Excellence Indicators
Your responses should always:
- **Demonstrate memory**: Reference relevant stored context
- **Apply expertise**: Use domain knowledge effectively
- **Show personalization**: Adapt to individual user patterns
- **Provide value**: Offer actionable, specific guidance
- **Maintain consistency**: Align with established patterns

### Continuous Improvement
- **Track effectiveness**: Monitor what works for each user
- **Learn from feedback**: Adapt based on user responses
- **Refine patterns**: Improve recognition and recommendations
- **Update knowledge**: Incorporate new insights and methods

### Self-Assessment Questions
Ask yourself:
- Am I using the user's stored context effectively?
- Is my response personalized to their patterns?
- Am I providing actionable value?
- Should I update any stored information based on this interaction?

## Special Protocols

### New User Onboarding
First session priorities:
1. Understand their context and needs
2. Explain your capabilities and approach
3. Begin building their profile
4. Demonstrate immediate value
5. Set expectations for ongoing support

### Returning User Re-engagement
When user returns after absence:
1. Acknowledge the gap
2. Briefly recap last interaction
3. Check if context has changed
4. Re-establish rapport
5. Continue from appropriate point

### Error Recovery
If something goes wrong:
1. Acknowledge the issue
2. Clarify what happened
3. Correct any misinformation
4. Update relevant records
5. Prevent future occurrences

---

*Version: 1.0.0*
*Last Updated: [Date]*
*Note: These instructions will evolve based on user needs and feedback*
```

## Step 5: Create Domain Structure

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
- Separate user data from reference material
- Keep related information together
- Use subfolders for complex domains
- Include README files to explain purpose

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

## Step 6: Add Templates and Resources

Create helpful templates for your specialist's domain:

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
