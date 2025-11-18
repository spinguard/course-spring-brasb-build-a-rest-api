# Spring Boot 4.0 & Java 21 Course Upgrade Proposal

**Project:** Building a REST API with Spring Boot - Course Upgrade

**Date:** 2025

**Prepared For:** Broadcom VMware Tanzu Education Team

**Prepared By:** Bill Kable

**Status:** Initial Draft - For Scope & Budget Alignment

---

## Executive Summary

This proposal outlines the upgrade of the "Building a REST API with Spring Boot" course from Spring Boot 3.1/Java 17 to Spring Boot 4.0/Java 21. The upgrade ensures the course remains current with the latest Spring Boot framework and Java LTS version, maintaining its value for students and aligning with industry standards.

**Key Highlights:**

- **Timeline:** up to 4 weeks at 30 hours/week
- **Investment:** $8,000 - $12,000 (80-120 hours at $100/hour, T&E model with fixed scope and not-to-exceed billing model)
- **Approach:** Incremental PR-based development with staging environment testing
- **Risk Mitigation:** Early profiling, comprehensive iterative testing and staging verification before production,
  15hr buffer in estimation model

---

## Project Objectives

1. **Modernize Course Content:** Upgrade to Spring Boot 4.0 and Java 21 (LTS)
2. **Maintain Quality:** Ensure all code tests pass and course functionality is preserved
3. **Platform Updates:** Migrate to Educates 3.4.0 (Hugo content format, new authoring flow)
4. **Student Experience:** Verify complete course walkthrough works seamlessly

---

## Scope of Work

### Content & Code Updates

- Update 9 workshop content files and 11 lesson files at [OSS content repository](https://github.com/spinguard/course-spring-brasb-build-a-rest-api)
- Regenerate 9 workshop codebase start/stop commits with Spring Boot 4.0/Java 21 at [OSS codebase reposistory](https://github.com/spinguard/course-spring-brasb-build-a-rest-api-code)
- Update all version references and documentation links
- Migrate workshop content to Hugo format (Educates 3.4.0)

### Environment & Infrastructure

- Update 9 workshop environment configurations for Java 21
- Remove reconciler configurations (Educates 3.4.0) - work with Broadcom Education team to modernize deployment workflows
- Test all workshop environments in staging

### OSS Collaboration

No special Broadcom user or private access required.
Given the content and codebases are public OSS,
updates will be done via standard OSS contribution process:

- Author updates initiated externally from [OSS github user](https://github.com/billkable).

- Author updates will be initiated from Github pull requests from [forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks) of OSS
  [content](https://github.com/spinguard/course-spring-brasb-build-a-rest-api) and
  [codebase](https://github.com/spinguard/course-spring-brasb-build-a-rest-api-code) repositories.

- PR's will be submitted as part of standard [Github Flow](https://docs.github.com/en/get-started/using-github/github-flow).

- Broadcom VMware Tanzu team will:
  - Review, then either accept or reject PR submissions
  - Responsible for merging verfied updates to the upstream repositories
  - Handling the associated publishing to Spring Academy staging and/or production systems.

**Note**: **Nowhere in the flow does the external author have access to staging or production systems,
other than as a normal student user account for review/verification purposes.  It is recommended that the above mentioned user is given Spring Academy user access to staging (production access is already established via bkable@spinguard.io account)**

### Testing & Validation

- Comprehensive testing of all workshops
- Full course walkthrough verification
- Staging environment testing before production
- Implement and test Educates authoring flow

---

## Timeline

**Duration:** 4 weeks (120 hours conservative estimate)

| Week | Focus Area | Key Deliverables |
|------|-----------|------------------|
| **Week 1** | Environment Setup, Profiling & Workflow Establishment | OSS PR setup, initial content updates, capacity impact forecast, first module (Spring Initializr lab) complete, establish iterative authoring/update workflow, deploy to staging |
| **Week 2** | Module 2: First RESTful Endpoints | Content and lab updates for Module 2, iterative testing, VMware Tanzu Education team verification |
| **Week 3** | Module 3: Secure App | Content and lab updates for Module 3, iterative testing, VMware Tanzu Education team verification |
| **Week 4** | Module 4: CRUD Operations & Final Validation | Content and lab updates for Module 4, end-to-end verification, ready for production |

**Approach:** Sequential module-by-module updates with iterative testing throughout. Each module is completed, tested, and verified by the VMware Tanzu Education team before proceeding to the next module.

---

## Investment & Pricing

### Pricing Model

- **Hourly Rate:** $100/hour
- **Billing:** Time and materials with "Not to Exceed" cap
- **Payment:** Weekly or milestone-based invoicing

### Cost Estimate

| Scenario | Hours | Investment |
|----------|-------|------------|
| **Minimum (Optimistic)** | 80 hours | $8,000 |
| **Realistic Estimate** | 105 hours | $10,500 |
| **Not to Exceed Cap** | 120 hours | $12,000 |

**Note:** Client pays only for actual hours worked. If work completes early, client saves accordingly.

---

## Risk Management

### High-Risk Areas (Mitigated)

- **Spring Security API Changes:** Detailed estimate created, early verification planned
- **Environment Updates:** Early infrastructure coordination, 2 hours per workshop allocated
- **Platform Migration:** Staging environment testing throughout project
- **Increased Lab Resources**: Week one includes detailed profiling comparison of old/vs new versions

### Contingency Planning

- 15-hour buffer included in NTE cap for unexpected issues
- Incremental testing catches issues early
- Staging environment allows safe verification before production

---

## Success Criteria

### Technical Deliverables

- ✅ All content and code updated to Spring Boot 4.0/Java 21
- ✅ All 9 workshops regenerated and tested
- ✅ All environments updated and verified
- ✅ Educates 3.4.0 platform updates complete
- ✅ All tests passing

### Quality Assurance

- ✅ Complete course walkthrough successful
- ✅ Staging environment fully verified
- ✅ Ready for student testing and production deployment

---

## Approach & Methodology

### Incremental Development

- **PR-Based Process:** Topic branches and Pull Requests for each major component
- **Staging Testing:** All changes tested in Spring Academy staging environment
- **Early Detection:** Issues discovered and resolved incrementally, not at project end

### Quality Assurance

- Content rendering verified in staging
- Workshop environments tested individually
- Full course flow validated before production
- Documentation updated throughout

---

## Dependencies & Prerequisites

### Required Before Start

- Spring Boot 4.0 GA release (otherwise use latest 4.0-RC)
- Spring Academy staging environment available for user verification
- Infrastructure team coordination for environment updates

### Assumptions

- No new content - upgrade existing only
- No major breaking changes beyond those identified
- 30 hours/week availability
- PR review process accommodates incremental merges -
  will require VMware Tanzu Education team availability/coordination
- Access given to Spring Academy staging environment
  for user verification purposes
- Potential doubling of Educates footprint - assumed staging and production lab environments
  have sufficient scaling and capacity to accommodate