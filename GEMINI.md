# Vallarta Project Instructions

Welcome to the **Vallarta** repository. This document serves as the single source of truth for repository-wide conventions, architectural standards, and workflows. All developers and AI assistants working in this repository MUST adhere strictly to these mandates.

---

## 1. Project Overview & Philosophy

Vallarta is a clean-slate workspace. The goal of this project is to maintain a modular, robust, and highly maintainable codebase.

### Core Principles
- **Explicit over Implicit:** Prefer explicit composition, dependency injection, and clear interfaces over complex inheritance or prototype-based behaviors.
- **Strict Type Safety:** Leverage full capabilities of static typing (e.g., TypeScript or equivalent). Avoid `any`, type casting, or bypasses unless absolutely unavoidable and explicitly documented.
- **Surgical Changes:** Make minimal, focused, and precise edits. Avoid unrelated refactoring or "cleanup" of surrounding code unless explicitly directed.

---

## 2. Technical Stack & Conventions

As the workspace evolves, we align with the following standards:
- **Ecosystem Formatting:** Always use standard ecosystem formatters and linters (e.g., ESLint, Prettier, Ruff, Cargo Fmt) when available. Do not commit unformatted code.
- **No Hacks:** Never suppress linter warnings or compiler errors with inline overrides (e.g., `// @ts-ignore` or `eslint-disable`) unless there is no standard-compliant alternative.
- **Testing First:** A feature or bug fix is not complete without corresponding automated tests. All code changes must be verified using empirical validation.

---

## 3. Standard Workflows

We follow a disciplined **Research -> Strategy -> Execution** lifecycle for all tasks.

### Phase 1: Research
- Map the workspace structure and read relevant files to validate all assumptions.
- Seek empirical reproduction of any reported bugs before attempting a fix.
- Identify the exact testing/validation command required to verify changes.

### Phase 2: Strategy
- Formulate a clear, surgical, and minimal change plan.
- Ensure the plan aligns with the existing architecture and patterns.

### Phase 3: Execution (Iterative Plan -> Act -> Validate)
- **Plan:** Outline the specific changes and test cases.
- **Act:** Implement targeted changes.
- **Validate:** Run linting, type-checking, and unit tests to ensure no regressions.

---

## 4. Security & System Integrity

- **Credential Protection:** NEVER commit, print, or log secrets, API keys, private tokens, or sensitive credentials. Keep `.env` files and system configurations out of source control.
- **File Integrity:** Respect `.gitignore` and ensure temporary build artifacts or personal configuration files are never tracked.
