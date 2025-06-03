# Cursor Rules: Ultimate TDD Enforcement System

A comprehensive collection of **Cursor Rules** designed to enforce world-class development practices, with a focus on **Test-Driven Development (TDD)**, code quality, and systematic software engineering workflows.

## 🎯 What This Provides

This repository contains a meticulously crafted rule system that transforms your Cursor AI experience into a **strict TDD enforcement engine**. Every interaction with Cursor will follow professional software development standards, ensuring:

- ✅ **Mandatory Test-Driven Development** - No production code without tests
- ✅ **Comprehensive Quality Checks** - Static analysis, linting, formatting
- ✅ **Current Documentation Usage** - Always uses latest API docs via Context7
- ✅ **Systematic Problem Breakdown** - Complex problems split into manageable pieces
- ✅ **Step-by-Step Verification** - Every step confirmed before proceeding
- ✅ **Regression Prevention** - Full test suite validation after changes
- ✅ **SOLID Principles Enforcement** - Clean code practices mandatory
- ✅ **AI Context Persistence** - Maintains project memory across conversations

## 🚀 Quick Start

### Installation

1. **Clone this repository** into your development workspace:
```bash
git clone https://github.com/yourusername/cursor-rules.git
cd cursor-rules
```

2. **Copy the rules** to your project:
```bash
# Copy all rules to your project
cp -r .cursor/rules /path/to/your/project/.cursor/

# Or copy individual rule categories as needed
cp -r .cursor/rules/testing-rules /path/to/your/project/.cursor/rules/
cp -r .cursor/rules/core-rules /path/to/your/project/.cursor/rules/
```

3. **Activate in Cursor**: The rules will automatically activate when you open your project in Cursor.

### Immediate Benefits

Once installed, Cursor will **automatically enforce**:
- TDD workflow for all code changes
- Static quality checks (linting, formatting, type safety)
- Current documentation lookup for any library usage
- Comprehensive test planning and execution
- Professional code quality standards
- Persistent project context and decision tracking

## 📁 Rule Categories

### 🎯 Core Rules (`core-rules/`)
- **`master-development-workflow-always.mdc`** - Orchestrates all development activities
- **`ai-context-persistence-always.mdc`** - Maintains project memory across AI conversations
- **`rule-generating-agent.mdc`** - Guidelines for extending the rule system

### 🧪 Testing Rules (`testing-rules/`)
- **`tdd-development-always.mdc`** - Enforces strict Test-Driven Development
- **`test-quality-inspection-always.mdc`** - Ensures test effectiveness
- **`test-planning-strategy-always.mdc`** - Systematic test case identification
- **`problem-analysis-breakdown-always.mdc`** - Problem decomposition methodology
- **`regression-testing-always.mdc`** - Prevents regression with full test suite validation
- **`step-by-step-verification-always.mdc`** - Granular workflow verification

### 🏗️ Global Rules (`global-rules/`)
- **`code-quality-standards-always.mdc`** - SOLID principles and clean code enforcement
- **`static-analysis-enforcement-always.mdc`** - Mandatory linting and quality checks

### 🛠️ Tool Rules (`tool-rules/`)
- **`context7-documentation-always.mdc`** - Current documentation research requirements

## 🔄 Development Workflow Enforced

### Phase 1: Preparation & Research
1. **Context Reading** - Read ai_context folder for project state and decisions
2. **Problem Analysis** - Break into small, testable pieces
3. **Documentation Research** - Get current docs via Context7 MCP
4. **Test Case Planning** - Identify ALL possible test scenarios

### Phase 2: TDD Cycle (For Each Piece)
5. **Write Failing Test** - One test for current functionality
6. **Verify Red** - Confirm test fails for right reason
7. **Write Production Code** - Minimal code to pass test
8. **Static Quality Checks** - Linting, formatting, type safety
9. **Verify Green** - Confirm test passes
10. **Regression Testing** - Full test suite validation
11. **Test Quality Inspection** - Ensure test effectiveness

### Phase 3: Iteration & Completion
12. **Context Updating** - Update ai_context with progress and decisions
13. **Refactoring** - Clean code while maintaining green tests
14. **Next Iteration** - Move to next piece or test case

## 💡 Example Workflow

```typescript
// ❌ FORBIDDEN: Writing code without test
export class UserService {
  createUser(data: UserData) { /* implementation */ }
}

// ✅ ENFORCED: TDD Workflow
describe('UserService', () => {
  it('should create user with valid data and return success', () => {
    const service = new UserService();
    const userData = { email: 'test@test.com', name: 'John' };
    
    const result = service.createUser(userData);
    
    expect(result.success).toBe(true);
    expect(result.userId).toBeDefined();
  });
});

// Only AFTER test fails, write minimal production code:
export class UserService {
  createUser(userData: any) {
    return { success: true, userId: crypto.randomUUID() };
  }
}
```

## 🧠 AI Context System

The AI Context Persistence rule automatically creates and maintains an `ai_context/` folder containing:

- **`project_status.md`** - Current project state and active decisions
- **`task_log.md`** - Chronological history of all AI-completed tasks
- **`architecture_decisions.md`** - Technical choices and rationale
- **`code_conventions.md`** - Project-specific coding standards
- **`dependencies.md`** - Library choices and integration decisions
- **`known_issues.md`** - Current limitations and technical debt

This ensures project consistency and decision continuity across all AI interactions.

## 🎛️ Rule Configuration

All rules are configured with `alwaysApply: true`, meaning they:
- ✅ **Apply to ALL files** in the workspace
- ✅ **Cannot be bypassed** or ignored
- ✅ **Enforce consistently** across all development activities
- ✅ **Work together** as an integrated system

## 🔧 Customization

### Adding Custom Rules
1. Create new `.mdc` files in appropriate category directories
2. Use the `rule-generating-agent.mdc` guidelines
3. Set `alwaysApply: true` for workspace-wide enforcement

### Modifying Existing Rules
- Edit rule files to adjust enforcement levels
- Maintain consistency with master workflow
- Test rule interactions thoroughly

### Selective Application
```markdown
# For project-specific rules
description: "Custom rule for this project"
globs: ["src/**/*.ts", "test/**/*.spec.ts"]
alwaysApply: false
```

## 🎯 Quality Guarantees

With these rules active, Cursor will **guarantee**:

- 🔴 **No production code without failing tests first**
- 🟢 **All tests pass before proceeding**
- 🔧 **Zero linting errors or warnings**
- 📚 **Current documentation usage for all libraries**
- 🧪 **Comprehensive test coverage and quality**
- 🏗️ **SOLID principles and clean code practices**
- 🔄 **Full regression testing after any change**

## 📊 Benefits

### For Individual Developers
- **Enforced Best Practices** - No shortcuts or quick fixes
- **Professional Habits** - TDD becomes automatic
- **Quality Assurance** - Consistent, high-quality output
- **Learning Acceleration** - Learn proper patterns through enforcement

### For Teams
- **Consistent Standards** - Everyone follows same practices
- **Reduced Code Review** - Quality built-in from start
- **Knowledge Sharing** - Rules encode team knowledge
- **Onboarding** - New developers immediately follow best practices

### For Projects
- **Technical Debt Prevention** - Quality enforced from day one
- **Maintainable Codebase** - Clean, tested, documented code
- **Reliable Deployments** - Comprehensive testing prevents bugs
- **Scalable Architecture** - SOLID principles ensure extensibility

## 🤝 Contributing

We welcome contributions to improve and extend this rule system!

### Guidelines
1. **Follow the master workflow** defined in core rules
2. **Use TDD** for any rule modifications or additions
3. **Test rule interactions** thoroughly
4. **Document new rules** comprehensively
5. **Maintain consistency** with existing rule patterns

### Process
1. Fork the repository
2. Create feature branch following TDD workflow
3. Add/modify rules with proper documentation
4. Test in real development scenarios
5. Submit pull request with detailed explanation

## 📜 License

MIT License - Feel free to use, modify, and distribute these rules to improve development quality everywhere.

## 🙏 Acknowledgments

Built for the Cursor community to elevate AI-assisted development through systematic quality enforcement.

---

**Transform your development workflow. Install these rules and experience the power of enforced TDD and quality practices.** 🚀 