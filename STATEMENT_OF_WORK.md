# Statement of Work (SOW)
## Spring Boot 4.0 & Java 21 Upgrade Project

**Project:** Building a REST API with Spring Boot - Course Upgrade
**Version:** Informal SOW
**Date:** 2025
**Effort:** 105 hours (Realistic Estimate)
**Not to Exceed:** 120 hours ($12,000)
**Hourly Rate:** $100/hour
**Timeline:** ~3.5 weeks at 30 hours/week

---

## 1. Project Overview

### 1.1 Scope
Upgrade the "Building a REST API with Spring Boot" course from:
- **Current:** Spring Boot 3.1 / Java 17
- **Target:** Spring Boot 4.0 / Java 21 (or 25)

### 1.2 Objectives
- Update all course content and code to Spring Boot 4.0
- Upgrade Java version from 17 to 21
- Regenerate all workshop start/stop commits
- Update lab environment resources for Java 21
- Ensure all tests pass and course functionality is maintained
- Update documentation and remove deprecated patterns

### 1.3 Deliverables
- Updated content repository (this repo)
- Updated code repository (9 workshops with start/stop commits)
- Updated workshop environment configurations (9 workshop.yaml files)
- All tests passing
- Complete course walkthrough verified
- Documentation updated

---

## 1A. Pricing & Billing Model

### 1A.1 Hourly Rate
**Rate:** $100/hour

This rate reflects the maintenance/upgrade nature of the work (as opposed to new instructional design or major development).

### 1A.2 "Not to Exceed" Pricing Model
**Billing Structure:** Time and materials with a "Not to Exceed" cap

**Model:**
- Work will be billed at the hourly rate of **$100/hour**
- **Not to Exceed (NTE) Cap:** Based on realistic estimate plus contingency buffer
- If actual hours are less than the cap, client pays only for actual hours worked
- If actual hours reach the cap, work stops (or scope change process is initiated)

### 1A.3 Not to Exceed Cap Calculation

**Base Estimate:** 105 hours (realistic estimate)
**Contingency Buffer:** 15 hours (for risk mitigation)
**Total NTE Cap:** 120 hours

**Not to Exceed Amount: $12,000** (120 hours × $100/hour)

### 1A.4 Billing Scenarios

**Scenario 1: Work completes under estimate**
- Actual hours: 95 hours
- **Billed:** $9,500 (95 hours × $100/hour)
- Client saves: $2,500 vs. NTE cap

**Scenario 2: Work completes at estimate**
- Actual hours: 105 hours
- **Billed:** $10,500 (105 hours × $100/hour)
- Client saves: $1,500 vs. NTE cap

**Scenario 3: Work reaches NTE cap**
- Actual hours: 120 hours
- **Billed:** $12,000 (120 hours × $100/hour)
- At this point, either:
  - Project is complete, or
  - Scope change process is initiated for additional work

**Scenario 4: Work exceeds NTE cap (requires approval)**
- If work exceeds 120 hours, a scope change must be approved
- Additional hours billed at $100/hour with new NTE cap or fixed price agreement

### 1A.5 Scope Protection
- The NTE cap is based on the defined scope in this SOW
- Any scope changes will require:
  - Written approval
  - Updated NTE cap calculation
  - Revised timeline if needed

### 1A.6 Time Tracking
- Time will be tracked in 15-minute increments
- Weekly time reports will be provided
- Client will be notified when approaching 80% of NTE cap (96 hours)
- Client will be notified when approaching 95% of NTE cap (114 hours)

### 1A.7 Payment Terms
- Invoices submitted weekly or upon milestone completion
- Payment terms: [To be specified - typically Net 15 or Net 30]
- Final invoice upon project completion

---

## 2. Work Categories & Estimates

### 2.1 Content Repository Updates
**Estimated: 12 hours**

**Scope:**
- Update workshop content files (9 workshops)
- Update lesson content files (11 lessons)
- Update documentation links
- Review and update metadata files (lesson.json, workshop.yaml basic review)

**Key Tasks:**
- Update Spring Boot version references (3.3.X → 4.0.X)
- Update Java version references (17 → 21/25)
- **Migrate workshop content to Hugo format (Educates 3.4.0)**
- Verify/regenerate Initializr screenshots
- Update Spring documentation links
- Review code examples for deprecated APIs

**Deliverables:**
- All content.md files updated
- All version references corrected
- Documentation links current

---

### 2.2 Code Repository Updates
**Estimated: 45 hours**

**Scope:**
- Regenerate 9 workshop start commits with Spring Boot 4.0/Java 21
- Regenerate 9 workshop stop commits
- Verify dependency compatibility
- Address breaking changes
- Update test code if needed

**Key Tasks:**
- Workshop 02: Bootstrap (3 hours)
- Workshop 04: Test-First (4 hours)
- Workshop 05: First REST Endpoint (4 hours)
- Workshop 06: Spring Data (5 hours)
- Workshop 07: POST (4 hours)
- Workshop 08: GET List (5 hours)
- Workshop 09: Spring Security (6 hours) - *See detailed estimate*
- Workshop 10: PUT (4 hours)
- Workshop 11: DELETE (3 hours)
- Dependency verification (4 hours)
- Breaking changes review (5 hours)

**Deliverables:**
- All 9 workshop start commits regenerated
- All 9 workshop stop commits regenerated
- All tests passing
- Code matches workshop instructions

---

### 2.3 Lab Environment Resource Updates
**Estimated: 20 hours**

**Scope:**
- Update workshop environment configurations for Java 21
- Test environment startup
- Coordinate with infrastructure team

**Key Tasks:**
- Update 9 workshop.yaml files:
  - Change `jdk17-environment` → `jdk21-environment`
  - **Remove reconciler configuration (Educates 3.4.0)**
  - Verify/update package versions
  - Update VS Code Java tools images if needed
  - Verify resource allocations
- Test each workshop environment startup
- **Verify Hugo content rendering in environments**
- Coordinate with infrastructure team for image availability

**Deliverables:**
- All 9 workshop.yaml files updated
- All environments tested and verified
- Infrastructure requirements documented

---

### 2.4 Testing & Validation
**Estimated: 15 hours**

**Scope:**
- Build verification
- Unit test execution
- Runtime verification
- Integration testing
- End-to-end course walkthrough

**Key Tasks:**
- Verify all projects build successfully
- Run all tests for all workshops
- Test all REST endpoints
- Test security configurations
- **Test Educates authoring flow (separate task)**
- **Verify Hugo content rendering**
- Complete full course flow as a student would
- Verify learning objectives are met

**Deliverables:**
- All builds successful
- All tests passing
- All endpoints verified
- Complete course walkthrough completed

---

### 2.5 Documentation & Metadata Review
**Estimated: 5 hours**

**Scope:**
- Review course-level documentation
- Review workshop metadata
- Final documentation consistency check
- **Educates 3.4.0 platform updates documentation**

**Key Tasks:**
- Review course.template.json
- Review module summaries
- Review workshop metadata
- **Document Educates authoring flow changes**
- **Document Hugo migration notes**
- Final documentation review

**Deliverables:**
- All documentation reviewed and updated
- Metadata consistent across course
- **Educates 3.4.0 migration documentation**

---

### 2.5A. Educates Platform Updates (Version 3.4.0)
**Estimated: Included in existing estimates (no additional hours)**

**Scope:**
- Migrate workshop content to Hugo format
- Remove reconciler configuration from workshop.yaml files
- Implement Educates authoring flow (separate task)

**Key Tasks:**

**2.5A.1 Workshop Content Migration to Hugo**
- Migrate all 9 workshop content files from classic to Hugo format
- Review content structure for Hugo compatibility
- Verify content renders correctly in Hugo
- Test in staging environment with Educates 3.4.0
- **Effort included in:** Content Repository Updates (Section 2.1) and Testing & Validation (Section 2.4)

**2.5A.2 Removal of Reconciler Configuration**
- Remove reconciler configuration from all 9 workshop.yaml files
- Verify workshop functionality without reconciler
- Test workshop startup and execution
- **Effort included in:** Lab Environment Resource Updates (Section 2.3)

**2.5A.3 Educates Authoring Flow Implementation**
- **Separate Task:** Implement Educates authoring flow
- Review Educates 3.4.0 authoring flow documentation
- Update workshop creation/editing process
- Verify authoring flow with updated content
- Test authoring workflow in staging
- **Effort included in:** Testing & Validation (Section 2.4) and Documentation (Section 2.5)

**Deliverables:**
- All workshop content migrated to Hugo format
- All reconciler configurations removed
- Educates authoring flow implemented and tested
- Documentation of authoring flow changes

---

### 2.6 Optional Enhancements
**Estimated: 3 hours** *(Optional - Can be deferred)*

**Scope:**
- Review Java 21 language features
- Consider modern code patterns
- Code style updates

**Note:** This is optional and may not be appropriate for a beginner course.

---

## 3. Timeline

### 3.1 Schedule Assumptions
- **Hours per week:** 30 hours
- **Total hours:** 105 hours (realistic estimate)
- **Timeline:** ~3.5 weeks

### 3.2 Phased Approach

**Week 1 (30 hours):**
- Content repository updates (12 hours)
  - Create topic branch and PRs
  - **Begin Hugo content migration (Educates 3.4.0)**
  - Merge to staging, test content rendering
- Begin lab environment resource updates (10 hours)
  - Create topic branch and PRs
  - **Begin reconciler configuration removal**
  - Test in staging environment
- Begin code repository - Workshop 02 & 04 (7 hours)
  - Create topic branches and PRs
  - Merge to staging, verify in staging course
- Buffer/coordination (1 hour)

**Week 2 (30 hours):**
- Complete lab environment resource updates (10 hours)
  - Complete PRs, merge to staging
  - Verify all environments in staging
- Code repository - Workshops 05-08 (18 hours)
  - Create topic branches and PRs
  - Merge to staging incrementally
  - Verify each workshop in staging course
- Initial testing in staging (2 hours)

**Week 3 (30 hours):**
- Code repository - Workshops 09-11 (13 hours)
  - Create topic branches and PRs
  - Merge to staging incrementally
  - Verify each workshop in staging course
- Testing & validation in staging (15 hours)
  - Incremental testing as PRs merge
  - **Test Educates authoring flow (separate task)**
  - **Verify Hugo content rendering**
  - Full course walkthrough in staging
- Documentation review (2 hours)
  - **Document Educates authoring flow changes**

**Week 4 (15 hours):**
- Final testing & validation in staging (10 hours)
  - Complete end-to-end verification
  - Content rendering final check
  - Lab environment final verification
- Documentation final review (3 hours)
- Project completion & handoff (2 hours)
  - All PRs merged to staging
  - Staging verification complete
  - Ready for production

**Total: 3.5 weeks at 30 hours/week**

---

## 4. Risks & Mitigation

### 4.1 High-Risk Areas

#### Risk 1: Spring Security API Changes
**Risk Level:** High
**Impact:** Workshop 09 may require significant rewrite
**Probability:** Medium

**Mitigation:**
- Detailed estimate already created (11.5 hours)
- Early verification of Spring Security APIs recommended
- Test security configuration early in process
- Allow buffer time in Workshop 09 estimate

**Contingency:** +5 hours if significant API changes discovered

---

#### Risk 2: Workshop Environment Updates
**Risk Level:** High
**Impact:** JDK 21 environment images may not be available
**Probability:** Medium

**Mitigation:**
- Coordinate with infrastructure team **before** starting
- Verify JDK 21 environment images are available
- Test environment startup early in process
- Allow 2 hours per workshop + 2 hours contingency (20 hours total)

**Contingency:** +5 hours if infrastructure coordination is complex

---

#### Risk 3: Spring Initializr UI Changes
**Risk Level:** Medium
**Impact:** Screenshots may be outdated
**Probability:** Low

**Mitigation:**
- Regenerate screenshots after Spring Boot 4.0 GA
- Verify Initializr UI matches screenshots

**Contingency:** +2 hours if screenshots need regeneration

---

### 4.2 Medium-Risk Areas

#### Risk 4: Dependency Compatibility Issues
**Risk Level:** Medium
**Impact:** Spring Data, H2, or other dependencies may have issues
**Probability:** Low

**Mitigation:**
- Test dependencies early
- Have fallback versions ready
- Review Spring Boot 4.0 dependency matrix

**Contingency:** +3 hours if dependency issues arise

---

#### Risk 5: Test Framework Changes
**Risk Level:** Medium
**Impact:** JUnit, AssertJ, or MockMvc may have breaking changes
**Probability:** Low

**Mitigation:**
- Run tests early in process
- Update test code as needed
- Review Spring Boot 4.0 test changes

**Contingency:** +2 hours if test framework updates needed

---

### 4.3 Low-Risk Areas

#### Risk 6: Content File Updates
**Risk Level:** Low
**Impact:** Mostly find/replace operations
**Probability:** Low

**Mitigation:**
- Systematic review process
- Version control for all changes

**Contingency:** Included in base estimate

---

## 5. Contingency Planning

### 5.1 Time Contingency
**Base Estimate:** 105 hours
**Contingency Buffer:** 15 hours (included in NTE cap)
**Total NTE Cap:** 120 hours

**Contingency Allocation:**
- Spring Security issues: +5 hours
- Environment infrastructure: +5 hours
- Dependency issues: +3 hours
- Test framework: +2 hours
- Screenshots: +2 hours
- General buffer: +3 hours

**Total NTE Cap:** 120 hours ($12,000)

**Note:** If work exceeds the NTE cap, a scope change process must be initiated with client approval before continuing.

---

### 5.2 Scope Contingency
**Optional Enhancements:** 3 hours (can be deferred)
**Can be removed if timeline is tight**

---

## 6. Dependencies & Prerequisites

### 6.1 External Dependencies
1. **Spring Boot 4.0 GA Release** - Required before finalizing
2. **Java 21 Environment Images** - Required for workshop infrastructure
3. **Infrastructure Team** - Required for environment updates and image availability
4. **Code Repository Access** - Required for workshop commits

### 6.2 Prerequisites
- Access to content repository
- Access to code repository
- Access to workshop environment infrastructure
- **Access to Spring Academy staging environment**
- **Ability to create new course instance in staging**
- **PR review and merge permissions**
- Spring Boot 4.0 migration guide (when available)
- Java 21 environment images available

---

## 7. Assumptions

1. Spring Boot 4.0 GA will be available before project completion
2. Spring Security version in Spring Boot 4.0 GA is known (6.5.3 or 7.0)
3. Java version decision made (21 LTS recommended)
4. Infrastructure supports Java 21 (workshop YAML environment)
5. No major breaking changes beyond those identified
6. Code repository is accessible and can be updated
7. Screenshots can be regenerated if needed
8. Infrastructure team is available for coordination
9. 30 hours per week availability
10. No major scope changes during project
11. **Spring Academy staging environment is available and accessible**
12. **PR review process can accommodate incremental merges**
13. **Content rendering system in staging matches production**
14. **Educates 3.4.0 is available and Hugo migration is straightforward**
15. **Educates authoring flow documentation is available**

---

## 8. Success Criteria

### 8.1 Technical Success
- [ ] All content files updated with correct versions
- [ ] **All workshop content migrated to Hugo format (Educates 3.4.0)**
- [ ] **All reconciler configurations removed from workshop.yaml files**
- [ ] All 9 workshop start commits regenerated
- [ ] All 9 workshop stop commits regenerated
- [ ] All 9 workshop environments updated and tested
- [ ] All tests pass for all workshops
- [ ] All REST endpoints work correctly
- [ ] Security configuration works correctly
- [ ] **Educates authoring flow implemented and tested**
- [ ] No deprecated patterns remain

### 8.2 Quality Success
- [ ] Full course walkthrough successful
- [ ] Documentation links are current
- [ ] Code examples are accurate
- [ ] Learning objectives maintained
- [ ] Course ready for deployment

### 8.3 Process Success
- [ ] All deliverables completed on time
- [ ] All PRs created and merged to staging
- [ ] Staging environment testing completed
- [ ] Content rendering verified in staging
- [ ] Lab environments verified in staging
- [ ] Risks identified and mitigated
- [ ] Issues documented and resolved
- [ ] Stakeholders informed of progress

---

## 9. Communication & Reporting

### 9.1 Progress Reporting
- Weekly status updates recommended
- Issues reported as they arise
- Risk escalation for high-risk items

### 9.2 Key Milestones
- **Week 1 End:**
  - Content updates complete (PRs merged to staging)
  - Environments started (PRs submitted)
  - Initial staging course created and tested
- **Week 2 End:**
  - Environments complete (PRs merged to staging)
  - 4 workshops regenerated (PRs merged to staging)
  - Staging verification in progress
- **Week 3 End:**
  - All workshops regenerated (PRs merged to staging)
  - Testing in progress in staging
  - Content rendering verified
- **Week 4 End:**
  - Project complete
  - All PRs merged to staging
  - Full course verified in staging
  - Ready for production deployment

---

## 10. Change Management

### 10.1 Version Control & Pull Request Process
**PRs and topic branches will be used in a coordinated OSS (Open Source Software) change process for the upgrade.**

**Process:**
- Create topic branches for each major work category or workshop
- Submit Pull Requests (PRs) for review and incremental verification
- PRs and associated merges will be done on the **Broadcom Spring Academy staging environment**
- Incremental verification and testing rather than waiting until end of effort
- Each PR should be:
  - Focused on a specific area (e.g., one workshop, content updates, environment updates)
  - Tested and verified before merge
  - Reviewed for quality and completeness

**Benefits:**
- Early detection of issues
- Incremental progress visibility
- Easier rollback if issues discovered
- Parallel review and testing
- Reduced risk of large-scale failures

### 10.2 Staging Environment Testing
**A new course will be created in the Spring Academy staging environment for testing purposes.**

**Staging Environment Usage:**
- **Content Update Rendering:** Test how content updates render in the actual course platform
- **Lab Environment Updates:** Test workshop environment configurations with Java 21
- **Incremental Verification:** Test each PR/merge incrementally rather than waiting until project end
- **Integration Testing:** Verify full course flow in staging before production deployment

**Staging Environment Benefits:**
- Catch rendering issues early
- Verify environment configurations work correctly
- Test student experience before production
- Validate all workshop environments
- Ensure course platform compatibility

**Staging Environment Requirements:**
- Access to Spring Academy staging environment
- Ability to create new course instance
- Workshop environment infrastructure available in staging
- Content rendering system access

### 10.3 Incremental Verification Process
**Recommended approach: Verify and test incrementally as work progresses.**

**Verification Points:**
1. **Content Updates:** Test rendering after each content PR merge
2. **Workshop Code:** Test each workshop after code repository PR merge
3. **Environment Updates:** Test each workshop environment after YAML update PR merge
4. **Integration:** Test full workshop flow after each workshop is complete
5. **End-to-End:** Final full course walkthrough in staging

**Benefits of Incremental Approach:**
- Issues discovered early and fixed immediately
- Reduced risk of cascading failures
- Better progress tracking
- Easier to identify root causes
- Stakeholder visibility throughout process

### 10.4 Scope Changes
Any changes to scope, timeline, or estimates should be:
- Documented
- Approved by stakeholders
- Reflected in updated estimates
- Managed through PR process if code/content changes

### 10.5 Risk Escalation
High-risk items should be escalated immediately:
- Spring Security API changes
- Environment infrastructure issues
- Major dependency compatibility problems
- Staging environment access issues
- Content rendering problems in staging

---

## 11. Project Completion

### 11.1 Final Deliverables
- Updated content repository (all PRs merged)
- Updated code repository with all commits (all PRs merged)
- Updated workshop environments (all PRs merged)
- **New course instance in Spring Academy staging environment**
- **All PRs reviewed and merged to staging**
- Test results documentation
- Migration notes (if applicable)
- **Staging environment verification report**

### 11.2 Handoff
- Code review completed
- Documentation reviewed
- **All PRs merged to staging**
- **Course verified in staging environment**
- **Content rendering tested and verified**
- **Lab environments tested and verified**
- Course walkthrough verified
- Ready for student testing in staging
- Ready for production deployment

---

## 12. Related Documents

- **UPGRADE_TASKS.md** - Detailed task checklist
- **UPGRADE_ESTIMATE_SUMMARY.md** - Comprehensive effort estimates
- **SPRING_SECURITY_UPGRADE_ESTIMATE.md** - Detailed Spring Security upgrade estimate
- [Spring Boot 4.0 Release Notes](https://github.com/spring-projects/spring-boot/releases)
- [Spring Boot Migration Guide](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-4.0-Migration-Guide) (when available)

---

## 13. Pricing Summary

### 13.1 Rate & Cap
- **Hourly Rate:** $100/hour
- **Minimum (Floor):** 80 hours ($8,000)
- **Not to Exceed Cap:** 120 hours
- **Not to Exceed Amount:** $12,000

### 13.2 Estimate Breakdown
- **Minimum (Floor) - Optimistic:** 80 hours ($8,000)
- **Realistic Estimate:** 105 hours ($10,500)
- **Contingency Buffer:** 15 hours ($1,500)
- **Total NTE Cap:** 120 hours ($12,000)

**Note:** The minimum (floor) of 80 hours is based on the optimistic estimate scenario where APIs are highly compatible with minimal issues.

### 13.3 Billing Model
- Time and materials at $100/hour
- Billed for actual hours worked (up to NTE cap)
- Client pays only for hours actually worked
- NTE cap provides cost protection

---

## 14. Approval & Sign-off

**Prepared By:** [Name]
**Date:** [Date]
**Reviewed By:** [Name]
**Date:** [Date]
**Approved By:** [Name]
**Date:** [Date]

**Pricing Acknowledgment:**
- Hourly Rate: $100/hour
- Not to Exceed: $12,000 (120 hours)
- Billing Model: Time and materials with NTE cap

**Client Signature:** _________________ **Date:** _________

---

## Notes

- This is an **informal** Statement of Work for planning purposes
- Estimates are based on realistic scenarios with appropriate buffers
- Timeline assumes 30 hours per week availability
- Contingency time is included for risk mitigation
- Regular communication recommended throughout project
- Scope changes should be documented and approved

**Last Updated:** Based on Spring Boot 4.0 RC2 and Spring Security 6.5.3
**Next Review:** After Spring Boot 4.0 GA release
