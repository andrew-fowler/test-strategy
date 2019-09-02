# Test Strategy

---

Test distribution / pyramid
Risk

- Exploratory
- Unit
 - Coverage
 - Mutation
- Integration
- Acceptance

---

# Web

## Functional

## Non-functional

---

# API

## Functional

## Non-functional

---

# Mobile

## Functional

## Non-functional



















---

Note:
Fast feedback.  The greater the age of a bug, the more impactful and more expensive it is to fix.

All test automation aims to enable **change with confidence and speed**.  

At a system level, we're primarily aiming to cover **regression risks** introduced to the wider system (specifically at the user/consumer interface) by **changes in its subcomponents**.
---
## Context: Test Pyramid

![Image of test pyramid](assets/pyramid.jpg)


Note:
The test pyramid is a model often used/abused to describe very different things roughly related to testing.

The most useful way to think of it is to see it as illustrating the **competing dimensions of isolation and system-confidence**.

Isolation (in the code under test) is **proportional** to system (and therefore test) **determinism** and the **speed** of execution.

However, isolation is **_inversely_ proportional** to the **system confidence** provided by the resulting information.

Touch on: Vocab: Integration testing in the large/small

Q: How does this relate to API testing?

Q: What’s the difference between system and acceptance testing?

---

Note:
As few as possible _to cover the risks we care about_

Write tests at the **lowest possible point** in the pyramid

E.g. Checking a validation message appears is a UI unit test.

Checking that the post-validation transition occurs is likely a system test.

Anti-pattern: _Test all the things!_

Anti-pattern: _Ice cream cone_
---
## When should we write system tests?

Note:
When the interface is stable.

When supporting test strata are in place.

UI churn is common early in development and should be taken into account when considering when to write tests.

---

Note:

High coverage but poor performance results in tests that aren't ran as they take too long.

High performance but poor stability results in tests that aren't ran as they're too expensive to extract information from.

In a nutshell: It's better to have one stable and performant test, than many tests that are slow and / or unstable.

Anti-pattern: Maximising test counts/coverage, e.g. in migration projects.

---
## Design pattern/s

Basic 3 layer
 - Test specification 
 - User behavior encapsulation
 - System abstraction 


---
## Common pitfalls
  - Degradation
    - Quarantine process
  - Silo’d ownership
    - Documentation and education
  - Over reliance
    - Mature and transparent test approach
  - Over engineering
    - KISS, YAGNI
