# Dependencies

## Core Dependencies

### Cursor IDE
- **Purpose**: Primary development environment that consumes the rules
- **Version**: Latest stable version
- **Integration**: Rules automatically loaded from `.cursor/rules/` directory
- **Configuration**: Supports `.mdc` files with frontmatter for rule definition

### Git & GitHub
- **Purpose**: Version control and repository hosting
- **Configuration**: SSH-based authentication for multiple account support
- **Account**: Josematico-hq (secondary GitHub account)
- **Authentication**: SSH key-based (`~/.ssh/github_secondary`)

## Development Tools

### Markdown
- **Purpose**: Rule file format (`.mdc` extension)
- **Standards**: CommonMark with frontmatter metadata
- **Usage**: All rule content and documentation

### SSH Configuration
- **Purpose**: Multi-account GitHub access
- **Configuration**: Host alias `github.com-secondary`
- **Key Management**: Separate SSH keys per account

## Optional Integrations

### Context7 MCP
- **Purpose**: Current documentation lookup (referenced in rules)
- **Usage**: Automated library documentation retrieval
- **Integration**: Part of documentation research requirements

### Static Analysis Tools
- **Purpose**: Code quality enforcement (referenced in rules)
- **Examples**: ESLint, Prettier, TypeScript compiler, Pylint
- **Usage**: Mandatory quality checks defined in static-analysis-enforcement rule

### Testing Frameworks
- **Purpose**: TDD enforcement support
- **Examples**: Jest, Vitest, Pytest, Mocha
- **Usage**: Test execution and validation as part of TDD workflow

## System Requirements

### Operating System
- **Tested**: macOS (darwin 24.5.0)
- **Shell**: Zsh (/bin/zsh)
- **Compatibility**: Should work on Windows, Linux with appropriate SSH setup

### File System
- **Structure**: Standard Unix-style directory paths
- **Permissions**: Read/write access to project directories
- **Special Directories**: `.cursor/rules/` and `ai_context/`

## Integration Dependencies

### AI Context System
- **Purpose**: Persistent context across AI conversations
- **Dependencies**: File system access for context folder management
- **Requirements**: Read/write permissions for `ai_context/` directory

### Rule Loading System
- **Purpose**: Automatic rule application in Cursor
- **Dependencies**: Cursor's rule processing engine
- **File Format**: `.mdc` files with proper frontmatter

## Future Dependencies

### Potential Additions
- Language-specific tooling as new rule categories are added
- Additional MCP tools for enhanced automation
- CI/CD integration for rule validation
- Community contribution tools 