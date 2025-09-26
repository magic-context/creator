# Quick Reference Guide

A fast reference for key concepts and architectural patterns when working with AI specialists.

## Core Concepts

### AI Specialist
An AI assistant with persistent memory, domain expertise, and consistent methodology that builds understanding over time rather than starting fresh each interaction.

### Persistent Memory
The ability to remember and build upon previous interactions, preferences, and context across sessions and over extended periods.

### Workspace Architecture
The structured file system that enables persistent memory through organized storage of user profiles, preferences, knowledge, and active projects.

## Memory Types

| Type | Duration | Purpose | Example |
|------|----------|---------|---------|
| **Session Memory** | Current conversation | Maintain immediate context | "You mentioned the deadline earlier" |
| **Working Memory** | Days to weeks | Track active projects | "Since starting the mobile app project..." |
| **Core Memory** | Months to years | Store fundamental patterns | "Based on your morning energy preference..." |
| **Knowledge Base** | Permanent | Provide domain expertise | "Using agile retrospective framework..." |

## Standard Workspace Structure

```
specialist-workspace/
├── ai-instructions/          # How the specialist operates
│   ├── core-instructions.md
│   ├── memory-protocols.md
│   └── interaction-styles.md
├── memory/                   # User-specific information
│   ├── user-profile.md
│   ├── preferences.md
│   └── interaction-history.md
├── knowledge/                # Domain expertise
│   ├── frameworks.md
│   ├── methodologies.md
│   └── templates/
├── active-projects/          # Current focus areas
│   ├── current-goals.md
│   └── challenges/
└── historical/               # Archived context
    ├── completed-projects/
    └── lessons-learned/
```

## Memory Operations

### Creating Memory
- **Observation**: Notice patterns in user behavior
- **Validation**: Confirm patterns through multiple interactions
- **Storage**: Record in appropriate memory tier
- **Integration**: Connect with existing knowledge

### Updating Memory
- **Incremental**: Small adjustments based on new information
- **Pattern Recognition**: Individual events become patterns
- **Consolidation**: Merge related information to avoid redundancy
- **Archival**: Move outdated information to historical context

### Retrieving Memory
- **Relevance Scoring**: Weight information by importance to current query
- **Context Assembly**: Combine multiple memory sources
- **Hierarchical Search**: Check recent, then important, then historical
- **Pattern Matching**: Find conceptually related information

## Specialist Types & Use Cases

### Professional Specialists
- **Project Manager**: Track evolution, remember stakeholder preferences, maintain context across sprints
- **Research Assistant**: Maintain long-term research context, remember source patterns, track methodology evolution
- **Technical Writer**: Learn documentation styles, track product changes, maintain consistency

### Personal Specialists
- **Daily Planner**: Learn scheduling preferences, energy patterns, optimize productivity systems
- **Health Coach**: Track health goals, dietary preferences, exercise patterns, progress monitoring
- **Learning Tutor**: Adapt to learning style, track progress, customize teaching approaches

### Creative Specialists
- **Writing Coach**: Learn voice and style, track creative development, provide personalized feedback
- **Design Assistant**: Remember aesthetic preferences, track design evolution, provide contextual suggestions

## Key Success Patterns

### Memory Hierarchy
- **Critical Memory**: Core preferences that rarely change
- **Active Memory**: Current projects and immediate context
- **Historical Memory**: Past patterns and lessons learned

### Information Flow
1. **Input**: User interaction or feedback
2. **Analysis**: Extract relevant insights
3. **Integration**: Update existing memory appropriately
4. **Application**: Use updated understanding in response
5. **Validation**: Confirm accuracy through continued interaction

### Continuous Improvement
- **Pattern Detection**: Identify recurring themes and preferences
- **Adaptation**: Adjust approaches based on user feedback
- **Optimization**: Refine methods for better results
- **Learning**: Incorporate new insights into future interactions

## Common Architecture Patterns

### Layered Memory
- Store information at appropriate permanence levels
- Allow easy access to relevant context without overload
- Enable both stability and adaptation

### Template-Based Consistency
- Use proven frameworks and methodologies
- Customize templates based on user preferences
- Maintain consistency while allowing flexibility

### Feedback-Driven Learning
- Actively seek user feedback on effectiveness
- Track what works and what doesn't
- Continuously refine approaches based on results

## Troubleshooting Guide

### Issue: Specialist not remembering preferences
**Check**: Are preferences stored in core memory or just session memory?
**Solution**: Move validated preferences to persistent memory files

### Issue: Responses lack relevant context
**Check**: Is context retrieval finding the right information?
**Solution**: Improve tagging and organization of memory files

### Issue: Specialist suggests outdated approaches
**Check**: Is working memory being updated with recent feedback?
**Solution**: Implement regular memory maintenance and updates

### Issue: Information overload in responses
**Check**: Is memory retrieval prioritizing relevance appropriately?
**Solution**: Implement better filtering and context scoring

## Quick Commands for Memory Management

### Review Current Understanding
"Show me what you remember about my preferences"
"What patterns have you noticed in my work style?"

### Update or Correct Memory
"Actually, I prefer afternoon meetings now"
"That approach didn't work well for me"

### Request Specific Context
"Based on our previous discussions about X..."
"Considering my pattern of Y, what would you recommend?"

### Memory Maintenance
"What outdated information should we update?"
"Are there any conflicting preferences in your memory?"

## Best Practices Checklist

- [ ] **Memory Organization**: Clear separation between different types of information
- [ ] **Regular Updates**: Consistent incorporation of new insights and feedback
- [ ] **Context Relevance**: Appropriate retrieval and application of stored information
- [ ] **User Control**: Transparent memory that users can review and modify
- [ ] **Pattern Recognition**: Active identification of recurring themes and preferences
- [ ] **Continuous Learning**: Regular refinement of approaches based on results

## Performance Indicators

### Strong Memory System
- Proactive suggestions based on learned patterns
- Contextual responses that reference previous interactions
- Adaptation to changing preferences and circumstances
- Consistent improvement in recommendation quality

### Memory System Issues
- Forgetting previously established preferences
- Suggesting approaches that have been tried and failed
- Lack of context in responses
- Repetitive questions about established information

---

Use this guide as a quick reference when designing, implementing, or troubleshooting AI specialist systems.