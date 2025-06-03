# Code Conventions

## Rule File Standards

### File Structure
- All rule files use `.mdc` extension (Markdown with Cursor metadata)
- Required frontmatter with `description`, `globs`, `alwaysApply` fields
- Consistent heading structure: `# Title`, `## Critical Rules`, `## Examples`

### Content Standards
- Use emojis for visual organization and quick scanning
- Bullet points for actionable rules
- Include both valid and invalid examples
- Focus on enforceable, specific directives
- Avoid unnecessary explanation - prioritize actionable content

### Naming Conventions
- File naming: `rule-name-{always|auto|manual|agent}.mdc`
- Rule titles: Clear, descriptive, action-oriented
- Section headers: Consistent formatting with emojis for categories

## Documentation Standards

### Markdown Style
- Use `**bold**` for emphasis on key terms
- Use `✅` for completed items, `🔄` for in-progress, `📋` for planned
- Code blocks with appropriate language specification
- Clear section hierarchy with meaningful headers

### Content Organization
- Lead with value proposition and clear benefits
- Provide practical installation and usage instructions
- Include comprehensive examples
- Structure for scanning and quick reference

## Project Organization

### Directory Structure
```
.cursor/rules/
├── core-rules/           # Core Cursor behavior
├── testing-rules/        # TDD and testing enforcement  
├── global-rules/         # Universal quality standards
└── tool-rules/           # Tool-specific rules

ai_context/               # Persistent AI context
├── project_status.md     # Current state and decisions
├── task_log.md          # Chronological task history
├── architecture_decisions.md # Technical choices
├── code_conventions.md  # This file - coding standards
├── dependencies.md      # Library and integration choices
└── known_issues.md      # Bugs and limitations
```

### File Organization
- Group related rules in appropriate category directories
- Maintain clear separation between rule types
- Use descriptive, searchable file names
- Keep rule files focused on single concerns

## Quality Standards

### Rule Quality Criteria
- Must be enforceable through AI interaction
- Must provide clear, actionable guidance
- Must include practical examples
- Must integrate with overall workflow
- Must avoid conflicts with other rules

### Documentation Quality
- Professional tone appropriate for technical audience
- Complete information without redundancy
- Clear installation and usage instructions
- Practical examples that demonstrate value
- Regular updates to maintain accuracy 