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

- `rules/principle-aaa-pattern` - Structure tests with Arrange-Act-Assert
- `rules/principle-first-fast` - Keep tests fast
- `rules/principle-first-isolated` - Ensure tests are independent
- `rules/principle-first-repeatable` - Make tests deterministic
- `rules/principle-first-self-validating` - Tests must have clear pass/fail
- `rules/principle-first-timely` - Write tests alongside production code
- `rules/principle-dry-vs-damp` - Balance DRY and readability in tests

### 2. Coding Standards (CRITICAL)

- `rules/standard-strict-types` - Declare strict_types=1 in test files
- `rules/standard-final-classes` - Make test classes final
- `rules/standard-snake-case-methods` - Use snake_case for test method names
- `rules/standard-psr4-naming` - Follow PSR-4 naming and namespace conventions
- `rules/standard-psr12-formatting` - Apply PSR-12 code formatting
- `rules/standard-this-over-self` - Use $this over self:: for assertions
- `rules/standard-visibility-type-hints` - Explicit visibility and type hints

### 3. Test Attributes (HIGH)

- `rules/attr-test-attribute` - Use #[Test] attribute with it_ prefix
- `rules/attr-covers-class` - Use #[CoversClass] for coverage boundaries
- `rules/attr-uses-class` - Use #[UsesClass] for dependency documentation
- `rules/attr-size-categories` - Categorize tests by size
- `rules/attr-group` - Use #[Group] for arbitrary categorization
- `rules/attr-no-annotations` - Prefer PHP 8 attributes over PHPDoc annotations

### 4. Data Management (HIGH)

- `rules/data-provider` - Use #[DataProvider] for multiple scenarios
- `rules/data-provider-external` - Use #[DataProviderExternal] for shared data
- `rules/data-test-with` - Use #[TestWith] for inline datasets
- `rules/data-factory-method` - Factory methods for SUT instantiation
- `rules/data-direct-instantiation` - Direct instantiation for simple constructors

### 5. Test Documentation (MEDIUM)

- `rules/doc-testdox` - Use TestDox for executable specifications
- `rules/doc-testdox-attribute` - #[TestDox] attribute for custom display
- `rules/doc-readable-names` - Readable test names as specifications

### 6. Mocking (MEDIUM)

- `rules/mock-chicago-vs-london` - Chicago vs London TDD schools
- `rules/mock-prophecy` - Prophecy for expressive test doubles
- `rules/mock-avoid-over-mocking` - Avoid over-mocking internal dependencies

### 7. Integration Testing (MEDIUM)

- `rules/integration-smoke-http` - HTTP controller smoke tests
- `rules/integration-smoke-cli` - CLI command smoke tests
- `rules/integration-performance` - Performance-aware test setup
- `rules/integration-singleton` - Singletons for stateless services
- `rules/integration-transactions - Database transactions for test cleanup

### 8. Configuration (LOW-MEDIUM)

- `rules/config-testsuites` - Organize tests in named suites
- `rules/config-strictness` - Enable strict mode settings
- `rules/config-source-coverage` - Source directory for coverage analysis
- `rules/config-order-by` - Test execution ordering strategies
- `rules/config-cache` - Cache directory for performance
- rules/config-stop-on-failure - Stop on first failure for fast feedback

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