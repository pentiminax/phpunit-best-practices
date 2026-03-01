---
name: phpunit-best-practices
description: PHPUnit testing best practices and conventions guide. This skill should be used when writing, reviewing, or refactoring PHPUnit tests to ensure consistent, maintainable, and effective test suites. Triggers on tasks involving test creation, test refactoring, test configuration, code coverage, data providers, mocking, or PHPUnit XML configuration.
license: MIT
metadata:
  author: pentiminax
  version: "1.0.0"
---

# PHPUnit Best Practices

Comprehensive testing best practices guide for PHPUnit applications, maintained by pentiminax. Contains 40 rules across 8 categories, prioritized by impact to guide automated test generation, refactoring, and code review.

## When to Apply

Reference these guidelines when:
- Writing new PHPUnit test classes or test methods
- Reviewing test code for quality and consistency
- Refactoring existing test suites
- Configuring PHPUnit XML settings
- Setting up code coverage and test organization

## Rule Categories by Priority

| Priority | Category | Impact | Prefix |
|----------|----------|--------|--------|
| 1 | Principles & Patterns | CRITICAL | `principle-` |
| 2 | Coding Standards | CRITICAL | `standard-` |
| 3 | Test Attributes | HIGH | `attr-` |
| 4 | Data Management | HIGH | `data-` |
| 5 | Test Documentation | MEDIUM | `doc-` |
| 6 | Mocking | MEDIUM | `mock-` |
| 7 | Integration Testing | MEDIUM | `integration-` |
| 8 | Configuration | LOW-MEDIUM | `config-` |

## Quick Reference

### 1. Principles & Patterns (CRITICAL)

- `principle-aaa-pattern` - Structure tests with Arrange-Act-Assert
- `principle-first-fast` - Keep tests fast
- `principle-first-isolated` - Ensure tests are independent
- `principle-first-repeatable` - Make tests deterministic
- `principle-first-self-validating` - Tests must have clear pass/fail
- `principle-first-timely` - Write tests alongside production code
- `principle-dry-vs-damp` - Balance DRY and readability in tests

### 2. Coding Standards (CRITICAL)

- `standard-strict-types` - Declare strict_types=1 in test files
- `standard-final-classes` - Make test classes final
- `standard-snake-case-methods` - Use snake_case for test method names
- `standard-psr4-naming` - Follow PSR-4 naming and namespace conventions
- `standard-psr12-formatting` - Apply PSR-12 code formatting
- `standard-this-over-self` - Use $this over self:: for assertions
- `standard-visibility-type-hints` - Explicit visibility and type hints

### 3. Test Attributes (HIGH)

- `attr-test-attribute` - Use #[Test] attribute with it_ prefix
- `attr-covers-class` - Use #[CoversClass] for coverage boundaries
- `attr-uses-class` - Use #[UsesClass] for dependency documentation
- `attr-size-categories` - Categorize tests by size
- `attr-group` - Use #[Group] for arbitrary categorization
- `attr-no-annotations` - Prefer PHP 8 attributes over PHPDoc annotations

### 4. Data Management (HIGH)

- `data-provider` - Use #[DataProvider] for multiple scenarios
- `data-provider-external` - Use #[DataProviderExternal] for shared data
- `data-test-with` - Use #[TestWith] for inline datasets
- `data-factory-method` - Factory methods for SUT instantiation
- `data-direct-instantiation` - Direct instantiation for simple constructors

### 5. Test Documentation (MEDIUM)

- `doc-testdox` - Use TestDox for executable specifications
- `doc-testdox-attribute` - #[TestDox] attribute for custom display
- `doc-readable-names` - Readable test names as specifications

### 6. Mocking (MEDIUM)

- `mock-chicago-vs-london` - Chicago vs London TDD schools
- `mock-prophecy` - Prophecy for expressive test doubles
- `mock-avoid-over-mocking` - Avoid over-mocking internal dependencies

### 7. Integration Testing (MEDIUM)

- `integration-smoke-http` - HTTP controller smoke tests
- `integration-smoke-cli` - CLI command smoke tests
- `integration-performance` - Performance-aware test setup
- `integration-singleton` - Singletons for stateless services
- `integration-transactions` - Database transactions for test cleanup

### 8. Configuration (LOW-MEDIUM)

- `config-testsuites` - Organize tests in named suites
- `config-strictness` - Enable strict mode settings
- `config-source-coverage` - Source directory for coverage analysis
- `config-order-by` - Test execution ordering strategies
- `config-cache` - Cache directory for performance
- `config-stop-on-failure` - Stop on first failure for fast feedback

## How to Use

Read individual rule files for detailed explanations and code examples:

```
rules/principle-aaa-pattern.md
rules/standard-final-classes.md
```

Each rule file contains:
- Brief explanation of why it matters
- Incorrect code example with explanation
- Correct code example with explanation
- Additional context and references

## Full Compiled Document

For the complete guide with all rules expanded: `AGENTS.md`
