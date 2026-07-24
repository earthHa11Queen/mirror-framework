# mirror-framework

A test scenario generation framework that **finitely enumerates test scenarios**
through domain definition and relation patterns.

Inspired by routing path computation in network algorithms,  
the core idea is: **"test scenarios can be derived by SQL-style enumeration."**

---

## About This Repository

Test scenario generation is work that tends to depend on individual experience and intuition.  
This framework formalizes that process into a finite, reproducible pipeline:  
**domain definition → boolean operation → pattern enumeration.**

What distinguishes it from conventional decision tables or CPP (cause-effect graphs)  
is that input value domains are **structured through a network routing design analogy**,  
and it includes an **explicitly defined operational model that separates the roles of human, AI, and program.**

---

## Documents

### 1. [Theory, Design Philosophy, and Role Separation](./docs/01_theory.md)

The core ideas behind the Mirror Framework.

- The claim that test scenarios can be finitely enumerated from domain and relation patterns
- How test data is generated through boolean operations
- How YAML conversion enables structured input to AI
- A role model that clearly separates human, AI, and programmatic processing

### 2. [Input Value Pattern Catalog](./docs/02_input-patterns.md)

A systematic classification of input values required for test design.

- Numeric types (integers, decimals, dates, boundary values, signed numbers)
- String types (full-width, half-width, control characters, special characters)
- HTML encoding and injection-aware classifications
- Assigning boolean flags to each pattern enables AI-driven enumeration

### 3. [E2E Screen Transition Extension](./docs/03_e2e-transition.md)

A methodology for extending the Mirror Framework — strong in unit testing —  
into integration and system testing.

- Screen transition computation inspired by optical network path design (airport EPS routing)
- Full path enumeration using adjacency tables + LEFT JOIN
- Automatic test phase classification via path cost (0=unit, 1~n=integration, max=system)
- Includes a sample adjacency table built from an actual design document

---

## About the `schemas/` Directory

The `schemas/` directory contains YAML schema definitions of the structures described in each document.  
These serve as input formats for AI-driven test scenario generation.

---

## Related Repository

- [playwright-framework-guide](https://github.com/earthHa23Queen/playwright-framework-guide)  
  Design philosophy for Playwright E2E test automation — the intended implementation target of this framework.

---

## License

[CC BY-SA 4.0](./LICENSE)

This repository handles design philosophy and documentation rather than code,  
so the Creative Commons Attribution-ShareAlike license applies.  
When citing, adapting, or redistributing, please credit the original author  
and apply the same license.

---
