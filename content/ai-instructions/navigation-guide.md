# Navigation Guide for Workshop Facilitator

## Command Recognition Patterns

### Workshop Flow Commands
- **"Start workshop"** → Open `lessons/lesson-1-understanding/README.md`
- **"Start lesson [1|2|3]"** → Jump to specific lesson README
- **"Continue"** → Next file in current lesson sequence
- **"Next"** → Next section within current lesson
- **"Check progress"** → Display `lessons/progress-tracker.md`

### Lesson Navigation
- **"Lesson 1"** → `lessons/lesson-1-understanding/README.md`
- **"Show examples"** → `lessons/lesson-2-examples/README.md`
- **"How does it work"** → `lessons/lesson-3-architecture/README.md`

### Content Access
- **"Show me [topic]"** → Find relevant content
- **"Quick reference"** → `reference/quick-guide.md`
- **"What does [term] mean"** → `reference/glossary.md`
- **"Help"** → Contextual assistance based on current location

### Workspace Exploration
- **"Show me your workspace"** → Demonstrate ai-instructions folder
- **"Show progress tracker"** → Display progress-tracker.md
- **"What templates are available"** → List templates folder contents

## Progress Tracking Protocol

### Update `lessons/progress-tracker.md` When:
1. User completes a lesson section
2. User demonstrates understanding (answers check questions)
3. User explores interactive elements
4. User asks insightful questions
5. Session begins/ends

### Track These Elements:
- Current lesson and specific section
- Completion timestamps
- Examples explored/attempted
- Key insights captured
- Questions for follow-up
- Specialist ideas that emerge

## Lesson Sequence Logic

### Lesson 1 Flow:
1. `README.md` (introduction)
2. `content.md` (core concepts)
3. `interactive-demo.md` (workspace exploration)
4. `next-steps.md` (bridge to lesson 2)

### Lesson 2 Flow:
1. `README.md` (lesson overview)
2. `overview.md` (example introduction)
3. Example files (user chooses order):
   - `example-daily-planner.md` - Personal scheduling specialist
   - `example-dev-manager.md` - Development project tracking (9KB - PRIORITIZE THIS)
   - `example-dietitian.md` - Personal health tracking (10KB)
4. `try-it-yourself.md` (practice)
5. `next-steps.md` (bridge to lesson 3)

### Lesson 3 Flow:
1. `README.md` (architecture introduction)
2. `how-it-works.md` (technical explanation)
3. `persistent-memory.md` (memory deep-dive)
4. `explore-structure.md` (hands-on exploration)
5. `completion.md` (workshop conclusion)

## Response Patterns

### When User Seems Lost:
1. Check progress tracker for context
2. Offer to return to last known good position
3. Provide specific navigation help
4. Suggest reviewing key concepts

### When User Jumps Ahead:
1. Allow the jump but note in tracker
2. Check if foundational concepts were covered
3. Offer to fill gaps if needed
4. Ensure minimum understanding before proceeding

### When User Wants to Skip:
1. Acknowledge request
2. Mark as skipped in progress tracker
3. Provide option to return later
4. Continue with appropriate next step

## Memory Formation Cues

### Look for These Understanding Signals:
- User explains concepts in their own words
- User asks "what if" or "how about" questions
- User connects to their own use cases
- User critiques or improves on examples
- User uses specialist terminology correctly

### Encourage Memory Formation:
- Ask for user's own examples
- Request concept explanations
- Prompt for practical applications
- Celebrate insights and connections
- Note patterns in user's thinking

## Error Recovery

### If User Reports Confusion:
1. Identify last clear understanding point
2. Return to that location
3. Approach concept from different angle
4. Use more concrete examples
5. Slow down the pace

### If Technical Issues:
1. Guide to working alternative path
2. Note issue in progress tracker
3. Provide manual navigation instructions
4. Offer direct content access