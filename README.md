# Prompt Guide: Making GPT Work Like Claude

This guide provides prompts that help GPT models (especially GPT-5-mini) deliver complete, production-ready implementations similar to Claude's approach - giving you full working code immediately rather than step-by-step tutorials.

## Core Principle

Add this suffix to ANY coding request to get Claude-style responses:

```
Provide the complete, working implementation immediately. Include all necessary code, file structure, and imports. Skip step-by-step explanations - just give me the full solution ready to use. I'll ask about specific parts if I need clarification.
```

---

## Sequential Implementation Prompts

### Implementing Next Feature from Docs

```
Please read docs\implementation\implemented-2.1-enhanced-error-handling.md and docs\implementation\future-implementation-02.md 

We have implemented 2.1, thus implement 2.2 Advanced Risk Management.

Provide the complete, working implementation immediately. Include all necessary code, file structure, and imports. Skip step-by-step explanations - just give me the full solution ready to use. I'll ask about specific parts if I need clarification.
```

### Implementing Multiple Tasks

```
Implement all of the following tasks:

* Add CI workflow (GitHub Actions) to run these tests on push.
* Add deterministic tests that set EmergencyControls to live mode (require_approval=False, dry_run=False) via dependency injection to assert executed paths.
* Add unit tests that simulate RealTimeRiskMonitor threshold breach to automatically call emergency controls.
* Add coverage badge and integrate with coverage reporting.

Provide complete, working implementations for all tasks. Include all necessary files (.github/workflows, test files, configuration files, etc.) with full code ready to use. Show the complete file structure and where each file goes. Skip explanations - just give me all the code I need to implement these features.
```

---

## Common Development Tasks

### 1. Refactoring Code

```
Refactor [file/module name] to improve [performance/maintainability/readability]. 

Provide the complete refactored code with all changes applied. Show the full file, not just the changed sections. Skip the explanation of what changed - I can diff it myself.
```

**Example:**
```
Refactor src/trading/order-manager.ts to improve error handling and reduce complexity.

Provide the complete refactored code with all changes applied. Show the full file, not just the changed sections. Skip the explanation of what changed - I can diff it myself.
```

### 2. Bug Fixing

```
Fix the bug in [file/function]: [brief description of bug].

Provide the complete corrected code for the entire file/module. Include any related files that need changes. No step-by-step debugging process - just give me the working solution.
```

**Example:**
```
Fix the bug in src/risk/monitor.ts: threshold calculations are incorrect when portfolio value is negative.

Provide the complete corrected code for the entire file/module. Include any related files that need changes. No step-by-step debugging process - just give me the working solution.
```

### 3. Adding New Features

```
Add [feature description] to the existing codebase.

Provide all modified and new files in full. Show complete file contents, not snippets. Include imports, error handling, and integration points. Skip the implementation walkthrough.
```

**Example:**
```
Add real-time WebSocket price updates with automatic reconnection to the trading system.

Provide all modified and new files in full. Show complete file contents, not snippets. Include imports, error handling, and integration points. Skip the implementation walkthrough.
```

### 4. Architecture Design

```
Design the architecture for [system/feature description].

Provide complete code for all components, including folder structure, all necessary files, and how they connect. Give me production-ready implementation, not pseudocode or outlines.
```

**Example:**
```
Design the architecture for a multi-strategy trading system that can run strategies in parallel with independent risk limits.

Provide complete code for all components, including folder structure, all necessary files, and how they connect. Give me production-ready implementation, not pseudocode or outlines.
```

### 5. API Integration

```
Integrate [API/service/library] into the project for [purpose].

Provide all necessary code: configuration files, wrapper classes, error handling, and usage examples. Show complete implementations ready to deploy. No tutorial steps.
```

**Example:**
```
Integrate Binance API into the project for real-time market data and order execution.

Provide all necessary code: configuration files, wrapper classes, error handling, and usage examples. Show complete implementations ready to deploy. No tutorial steps.
```

### 6. Database Implementation

```
Implement [database schema/migrations/queries] for [feature].

Provide complete migration files, model definitions, and any necessary database interaction code. Include all files in full with proper error handling and edge cases.
```

**Example:**
```
Implement PostgreSQL schema and queries for trade history tracking with performance metrics.

Provide complete migration files, model definitions, and any necessary database interaction code. Include all files in full with proper error handling and edge cases.
```

### 7. Testing Suite

```
Create comprehensive tests for [module/feature].

Provide complete test files with all test cases, fixtures, mocks, and configuration. Include the full test suite ready to run. Skip explanations of testing strategy.
```

**Example:**
```
Create comprehensive tests for the risk management module including unit tests, integration tests, and edge cases.

Provide complete test files with all test cases, fixtures, mocks, and configuration. Include the full test suite ready to run. Skip explanations of testing strategy.
```

### 8. Configuration & Setup

```
Set up [tool/framework/environment] for the project.

Provide all configuration files, setup scripts, and necessary code in full. Include complete file contents for package.json, config files, env templates, etc. No setup instructions - just the files.
```

**Example:**
```
Set up TypeScript, ESLint, Prettier, and Jest for a new Node.js trading bot project.

Provide all configuration files, setup scripts, and necessary code in full. Include complete file contents for package.json, config files, env templates, etc. No setup instructions - just the files.
```

### 9. Performance Optimization

```
Optimize [component/query/algorithm] for better performance.

Provide the complete optimized implementation with all changes applied. Include any new files or dependencies needed. Skip the performance analysis explanation.
```

**Example:**
```
Optimize the backtesting engine to handle 1M+ data points efficiently.

Provide the complete optimized implementation with all changes applied. Include any new files or dependencies needed. Skip the performance analysis explanation.
```

### 10. Documentation to Code

```
Implement everything specified in [doc/spec file].

Provide complete working code for all requirements. Include all files, proper structure, error handling, and edge cases. Give me the full implementation ready to use, not a plan or outline.
```

**Example:**
```
Implement everything specified in docs/specs/order-execution-system.md.

Provide complete working code for all requirements. Include all files, proper structure, error handling, and edge cases. Give me the full implementation ready to use, not a plan or outline.
```

---

## Advanced Patterns

### Complex Multi-File Implementation

```
Build [complete feature/system] with the following requirements:
[List requirements]

Provide:
- Complete folder structure
- All files with full implementations
- Configuration and setup files
- Integration code
- Error handling throughout

Show everything ready to deploy. No explanations or tutorials.
```

### Migration/Upgrade

```
Migrate [current implementation] from [old tech] to [new tech].

Provide all migrated files in full, including:
- Updated dependencies and configuration
- Converted code with modern patterns
- Migration script if needed
- Any breaking changes handled

Skip the migration strategy explanation - just give me the migrated code.
```

### Security Hardening

```
Add security improvements to [module/system]:
[List specific security concerns or requirements]

Provide complete implementation with:
- All security measures applied
- Input validation and sanitization
- Authentication/authorization if needed
- Rate limiting, error handling
- Configuration for secrets management

Show production-ready secure code. No security lecture.
```

---

## Universal Template

Use this template for any coding task:

```
[Your specific request/requirement]

Provide the complete, working implementation immediately. Include:
- All necessary code files (full contents)
- File structure and organization
- Configuration files
- Imports and dependencies
- Error handling and edge cases

Skip step-by-step explanations. Just give me the full solution ready to use. I'll ask about specific parts if I need clarification.
```

---

## Tips for Best Results

1. **Be specific about what's already done**: "We've implemented X, now do Y"
2. **Reference existing files**: "Update src/risk/monitor.ts to add..."
3. **List multiple tasks clearly**: Use bullet points for multi-part requests
4. **Mention constraints upfront**: "Use existing error handling patterns", "Must work with Python 3.9+"
5. **Always include the instruction to skip explanations**: This is key to getting Claude-style responses

## What to Avoid

❌ "Can you help me with..." (too vague, invites explanation)
❌ "Please explain how to..." (explicitly asks for tutorial)
❌ "Walk me through..." (asks for step-by-step)
❌ Leaving out the "skip explanations" instruction

✅ "Implement X. Provide complete code. Skip explanations."
✅ "Add feature Y to existing module Z. Give me the full updated file."
✅ "Build system X with requirements A, B, C. Complete implementation only."

---

## Quick Reference

**Shortest effective suffix:**
```
Complete implementation only. Full files. No explanations.
```

**Standard suffix:**
```
Provide complete, working implementation. Include all necessary code and file structure. Skip explanations - give me the full solution ready to use.
```

**Detailed suffix (for complex tasks):**
```
Provide the complete, working implementation immediately. Include:
- All code files with full contents
- File structure and where each file goes
- Configuration and setup files
- Proper error handling and edge cases
Skip step-by-step explanations. Just give me everything I need to deploy this. I'll ask about specific parts if needed.
```
