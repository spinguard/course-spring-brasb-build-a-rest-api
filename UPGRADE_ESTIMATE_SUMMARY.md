# Spring Boot 4.0 & Java 21/25 Upgrade - Summary Estimate

## Overview
**Upgrade:** Spring Boot 3.1/Java 17 → Spring Boot 4.0/Java 21 (or 25)
**Course:** Building a REST API with Spring Boot
**Total Workshops:** 9
**Total Lessons:** 11 (including orientation)

---

## Executive Summary

### Total Estimated Effort

| Estimate Type | Hours | Days (8hr/day) | Notes |
|--------------|-------|----------------|-------|
| **Optimistic** | 78 hours | 9.8 days | If APIs are highly compatible, minimal issues |
| **Realistic** | 105 hours | 13.1 days | Recommended estimate with buffer |
| **Conservative** | 135 hours | 16.9 days | If significant issues arise, extensive testing needed |

### Recommended Estimate: **105 hours (~13 days)**

**Note:** Updated to include lab environment resource upgrades (18 hours + 2 hours contingency)

---

## Breakdown by Major Area

### 1. Content Repository Updates (This Repo)
**Estimated: 12 hours**

**Repository:** [OSS content repository](https://github.com/spinguard/course-spring-brasb-build-a-rest-api)

#### 1.1 Workshop Content Files (6 hours)
- **Workshop 02 (Spring Initializr):** 1 hour
  - Update Spring Boot version (3.3.X → 4.0.X)
  - Update Java version (17 → 21/25)
  - Verify/regenerate Initializr screenshots
- **Workshops 04-11:** 5 hours
  - Review 8 workshops × ~40 content files
  - Update version references
  - Verify code examples
  - Check for deprecated API usage

#### 1.2 Lesson Content Files (4 hours)
- **11 lesson content.md files:** 3 hours
  - Review each for version-specific references
  - Update Spring Boot version mentions
  - Check for deprecated API references
- **Documentation links:** 1 hour
  - Verify all Spring documentation links
  - Update version-specific URLs

#### 1.3 Metadata & Configuration (2 hours)
- **20 lesson.json files:** 1 hour
  - Review for version references
  - Update links if needed
- **Workshop YAML files (basic):** 1 hour
  - Initial review for hardcoded versions
  - Note: Detailed environment updates estimated separately below

---

### 2. Code Repository Updates
**Estimated: 45 hours**

**Repository:** [OSS codebase repository](https://github.com/spinguard/course-spring-brasb-build-a-rest-api-code)

**Note:** Updates via OSS contribution process (forks, PRs, GitHub Flow)

#### 2.1 Workshop Start/Stop Commits (36 hours)
**9 workshops × 4 hours each = 36 hours**

Each workshop requires:
- Regenerate start commit with Spring Boot 4.0/Java 21
- Implement all workshop steps
- Create stop commit
- Verify tests pass
- Verify code matches instructions

**Breakdown by workshop:**
- **Workshop 02 (Bootstrap):** 3 hours - Simple, just Initializr setup
- **Workshop 04 (Test-First):** 4 hours - Test setup, JSON testing
- **Workshop 05 (First REST Endpoint):** 4 hours - Controller, path variables
- **Workshop 06 (Spring Data):** 5 hours - Repository, database setup
- **Workshop 07 (POST):** 4 hours - POST endpoint, validation
- **Workshop 08 (GET List):** 5 hours - Pagination, sorting
- **Workshop 09 (Spring Security):** 6 hours - **See detailed estimate: SPRING_SECURITY_UPGRADE_ESTIMATE.md**
- **Workshop 10 (PUT):** 4 hours - PUT endpoint, ownership
- **Workshop 11 (DELETE):** 3 hours - DELETE endpoint

#### 2.2 Dependency & Compatibility Verification (4 hours)
- **Spring Data JDBC:** 1 hour
  - Verify compatibility with Spring Boot 4.0
  - Test H2 database version
- **Spring Security:** 1 hour (included in Workshop 09 estimate)
- **Test Dependencies:** 1 hour
  - JUnit 5 compatibility
  - AssertJ compatibility
  - Spring Boot Test annotations
- **Build Configuration:** 1 hour
  - Verify Gradle wrapper version
  - Check dependency management

#### 2.3 Breaking Changes & Code Updates (5 hours)
- **Jakarta EE 11:** 1 hour
  - Verify all imports are `jakarta.*` (should already be from 3.x)
  - Test JAX-RS compatibility
- **Property Changes:** 1 hour
  - Review application properties
  - Update if using observability/logging export
- **Auto-Configuration:** 2 hours
  - Test Spring Web MVC
  - Test Spring Data JDBC
  - Test Spring Security
  - Test H2 Database
  - Verify test auto-configurations
- **Test Code Updates:** 1 hour
  - Review all test files
  - Verify MockMvc usage
  - Check for deprecated test utilities

---

### 3. Lab Environment Resource Updates
**Estimated: 20 hours**

#### 3.1 Workshop Environment Configuration (18 hours)
**9 workshops × 2 hours each = 18 hours**

Each workshop requires updates to `workshop.yaml` and related environment resources:

**Tasks per workshop:**
- Update JDK environment reference (`jdk17-environment` → `jdk21-environment` or appropriate)
- Verify/update package versions (e.g., `spring-academy-lab` package)
- Update VS Code Java tools image if needed
- Verify resource allocations (memory, CPU) are appropriate
- Test workshop environment startup
- Verify all file paths and references are correct
- Coordinate with infrastructure team if needed

**Breakdown by workshop:**
- **Workshop 02 (Bootstrap):** 2 hours - Initial environment setup
- **Workshop 04 (Test-First):** 2 hours - Standard environment update
- **Workshop 05 (First REST Endpoint):** 2 hours - Standard environment update
- **Workshop 06 (Spring Data):** 2 hours - Standard environment update
- **Workshop 07 (POST):** 2 hours - Standard environment update
- **Workshop 08 (GET List):** 2 hours - Standard environment update
- **Workshop 09 (Spring Security):** 2 hours - Standard environment update
- **Workshop 10 (PUT):** 2 hours - Standard environment update
- **Workshop 11 (DELETE):** 2 hours - Standard environment update

#### 3.2 Environment Testing & Validation (2 hours)
- **Environment startup testing:** 1 hour
  - Verify each workshop environment starts correctly
  - Test with new JDK version
  - Verify all tools and dependencies available
- **Infrastructure coordination:** 1 hour
  - Coordinate with infrastructure team if needed
  - Verify new environment images are available
  - Document any infrastructure requirements

**Note:** This is separate from code repository updates and focuses on the workshop execution environment (Kubernetes/container resources).

---

### 4. Testing & Validation
**Estimated: 15 hours**

#### 4.1 Profiling & Capacity Analysis (4 hours)
- **Week 1 Task:** Detailed profiling comparison of old vs. new versions
- **Resource Utilization:** Compare CPU, memory, disk usage
- **Capacity Impact Forecast:** Analyze Educates environment footprint changes
- **Documentation:** Document findings for infrastructure team
- **Risk Assessment:** Assess potential doubling of Educates footprint

#### 4.2 Build & Unit Testing (4 hours)
- **Build Verification:** 1 hour
  - All projects build successfully
  - No deprecation warnings
- **Test Execution:** 2 hours
  - Run all tests for each workshop
  - Fix any test failures
- **Test Coverage:** 1 hour
  - Verify test coverage maintained
  - Check for missing test scenarios

#### 4.3 Runtime Verification (4 hours)
- **Application Startup:** 1 hour
  - Verify all applications start
  - Check for startup errors
- **REST Endpoint Testing:** 2 hours
  - GET /cashcards/{id}
  - GET /cashcards (pagination/sorting)
  - POST /cashcards
  - PUT /cashcards/{id}
  - DELETE /cashcards/{id}
- **Security Testing:** 1 hour
  - Basic authentication
  - Authorization checks
  - CSRF configuration

#### 4.4 Integration Testing (7 hours)
- **Full Workshop Flow:** 5 hours
  - Complete each workshop from start to finish
  - Verify start → stop transitions
  - Test as a student would
- **End-to-End Course:** 2 hours
  - Complete entire course flow
  - Verify learning objectives met
  - Check for consistency issues

---

### 5. Documentation & Metadata Review
**Estimated: 5 hours**

#### 5.1 Course-Level Documentation (2 hours)
- **Course metadata:** 0.5 hours
  - Review `course.template.json`
  - Update if version-specific
- **Module summaries:** 1 hour
  - Review 3 module summaries
  - Update if needed
- **README & descriptions:** 0.5 hours
  - Review course description
  - Update if version-specific

#### 5.2 Workshop Metadata (2 hours)
- **9 workshop.yaml files:** 1.5 hours
  - Check for `jdk17-environment` references
  - Update to `jdk21-environment` or appropriate version
  - Verify image references
- **Workshop modules.yaml:** 0.5 hours
  - Review for accuracy

#### 5.3 Final Documentation Review (1 hour)
- **Code review:** 0.5 hours
- **Documentation consistency:** 0.5 hours

---

### 5A. Educates Platform Updates (Version 3.4.0)
**Estimated: Included in existing estimates**

#### 5A.1 Workshop Content Migration to Hugo
**Effort: Included in Content Repository Updates (Section 1) and Lab Environment Updates (Section 3)**

- Migrate workshop content from classic format to Hugo format
- Review all 9 workshop content files for Hugo compatibility
- Update content structure if needed for Hugo rendering
- Verify content renders correctly in Hugo format
- Test content in staging environment with Educates 3.4.0

**Note:** This work is integrated into the content update and environment testing phases.

#### 5A.2 Removal of Reconciler Configuration
**Effort: Included in Lab Environment Resource Updates (Section 3)**

- Remove reconciler configuration from all 9 workshop.yaml files
- Verify workshop functionality without reconciler
- Test workshop startup and execution
- Update documentation if reconciler references exist

**Note:** This work is integrated into the workshop environment update tasks (2 hours per workshop).

#### 5A.3 Educates Authoring Flow Implementation
**Effort: Included in Testing & Validation (Section 4) and Documentation (Section 5)**

- **Separate Task:** Implement Educates authoring flow
- Review Educates 3.4.0 authoring flow documentation
- Update workshop creation/editing process to use new authoring flow
- Verify authoring flow works with updated workshop content
- Test authoring workflow in staging environment
- Document any authoring flow changes or requirements

**Note:** This is a distinctively separate task tracked independently, but effort is included in existing testing and documentation estimates.

---

### 6. Java Language Features (Optional)
**Estimated: 3 hours (Optional Enhancement)**

#### 6.1 Modern Java Features Review (2 hours)
- **Records:** 1 hour
  - Evaluate if `CashCard` can be a record
  - Consider impact on Spring Data
- **Pattern Matching:** 0.5 hours
  - Review switch expressions (Java 21)
  - Evaluate if appropriate for course level
- **Text Blocks:** 0.5 hours
  - Review if multi-line strings are used

#### 6.2 Code Style Updates (1 hour)
- **Java 21 best practices:** 0.5 hours
- **Code comments:** 0.5 hours

**Note:** This is optional and may not be appropriate for a beginner course. Can be deferred.

---

### 7. Risk Areas & Contingency
**Estimated: 5 hours buffer** (in addition to environment upgrade contingency)

#### High-Risk Areas
- **Spring Security (Workshop 09):** Already estimated separately (11.5 hours)
- **Workshop YAML environment updates:** May require infrastructure changes
- **Screenshot regeneration:** If Spring Initializr UI changes

#### Medium-Risk Areas
- **Dependency compatibility issues:** Spring Data, H2, etc.
- **Test framework changes:** JUnit, AssertJ, MockMvc
- **Auto-configuration changes:** May require code adjustments

#### Low-Risk Areas
- **Content file updates:** Mostly find/replace
- **Metadata updates:** Mostly straightforward
- **Documentation links:** Mostly URL updates

---

## Detailed Task Breakdown by Phase

### Phase 1: Preparation & Research (4 hours)
- [ ] Review Spring Boot 4.0 migration guide (when available)
- [ ] Review Java 21 migration guide
- [ ] Set up test environment with Spring Boot 4.0
- [ ] Create upgrade checklist
- [ ] Review Spring Security 7.0 changes (if applicable)
- [ ] **Set up OSS forks and establish GitHub Flow process**

### Phase 2: Content Repository Updates & Week 1 Setup (12 hours)
- [ ] **OSS PR setup and workflow establishment (2 hours)**
- [ ] Update Workshop 02 content (Spring Boot/Java versions)
- [ ] Review and update 8 remaining workshop content files
- [ ] **Migrate workshop content to Hugo format (Educates 3.4.0)**
- [ ] Review and update 11 lesson content files
- [ ] Update documentation links
- [ ] Review and update metadata files
- [ ] Update workshop YAML files (JDK version)
- [ ] **Profiling and capacity impact forecast (4 hours)**
  - Detailed profiling comparison of old vs. new versions
  - Capacity impact analysis
  - Resource utilization comparison

### Phase 3: Lab Environment Resource Updates (20 hours)
- [ ] Update Workshop 02 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 04 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 05 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 06 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 07 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 08 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 09 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 10 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Update Workshop 11 environment (2 hours)
  - Remove reconciler configuration (Educates 3.4.0)
- [ ] Environment testing & validation (2 hours)
  - Verify Hugo content rendering
  - Test without reconciler configuration

### Phase 4: Code Repository - Workshop Regeneration (45 hours)
- [ ] Workshop 02: Bootstrap (3 hours)
- [ ] Workshop 04: Test-First (4 hours)
- [ ] Workshop 05: First REST Endpoint (4 hours)
- [ ] Workshop 06: Spring Data (5 hours)
- [ ] Workshop 07: POST (4 hours)
- [ ] Workshop 08: GET List (5 hours)
- [ ] Workshop 09: Spring Security (6 hours) - **See SPRING_SECURITY_UPGRADE_ESTIMATE.md**
- [ ] Workshop 10: PUT (4 hours)
- [ ] Workshop 11: DELETE (3 hours)
- [ ] Dependency verification (4 hours)
- [ ] Breaking changes review (5 hours)

### Phase 5: Testing & Validation (15 hours)
- [ ] **Profiling and capacity analysis (4 hours) - Week 1**
  - Detailed profiling comparison of old vs. new versions
  - Capacity impact forecast
  - Resource utilization comparison
- [ ] Build verification (1 hour)
- [ ] Unit test execution (2 hours)
- [ ] Runtime verification (4 hours)
- [ ] Integration testing (7 hours)
  - **Test Educates authoring flow (separate task)**
  - Verify Hugo content rendering
- [ ] End-to-end course testing (1 hour)

### Phase 6: Documentation & Final Review (5 hours)
- [ ] Course metadata review (2 hours)
- [ ] Workshop metadata review (2 hours)
- [ ] Final documentation review (1 hour)
  - **Document Educates authoring flow changes**
  - Document Hugo migration notes

### Phase 7: Optional Enhancements (3 hours)
- [ ] Java 21 features review (2 hours)
- [ ] Code style updates (1 hour)

**Total: 105 hours** (matches realistic estimate)

---

## Effort Distribution

```
Content Updates:             12 hours (11%)
Code Repository:             45 hours (43%)
Lab Environment Resources:   20 hours (19%)
Testing & Validation:        15 hours (14%)
  - Includes 4 hours profiling (Week 1)
Documentation:               5 hours (5%)
Buffer/Contingency:          5 hours (5%)
Optional Enhancements:       3 hours (3%)
───────────────────────────────────────────
Total:                      105 hours (100%)
```

---

## Timeline Estimate

### Sequential Approach (One Person)
- **Weeks:** 2.5-3.5 weeks (assuming 4-6 hours/day)
- **Days:** 13-17 working days

### Parallel Approach (Team)
- **Content Updates:** 1 person, 2 days
- **Lab Environment Resources:** 1 person, 2.5 days (can parallel with content)
- **Code Repository:** 1-2 people, 6-7 days
- **Testing:** 1 person, 2 days
- **Documentation:** 1 person, 1 day
- **Total:** 7-8 days with 2-3 people

---

## Critical Path Items

1. **Workshop 02 (Bootstrap)** - Must be done first, establishes baseline
2. **Workshop 02 Environment** - Must be updated to support Java 21
3. **Workshop 09 (Spring Security)** - Most complex, requires careful review
4. **Workshop Environment Updates** - May require infrastructure coordination, can be parallelized
5. **Full Integration Testing** - Must be done before completion

---

## Assumptions

1. **Spring Boot 4.0 GA** will be available before finalizing
2. **Spring Security version** in Spring Boot 4.0 GA is known (6.5.3 or 7.0)
3. **Java version** decision made (21 LTS recommended)
4. **Infrastructure** supports Java 21 (workshop YAML environment)
5. **No major breaking changes** beyond those identified
6. **Code repository** is accessible and can be updated
7. **Screenshots** can be regenerated if needed
8. **Educates 3.4.0** is available and Hugo migration is straightforward
9. **Educates authoring flow** documentation is available
10. **OSS contribution process** (forks, PRs, GitHub Flow) is acceptable workflow
11. **Access given to Spring Academy staging environment** for user verification purposes
12. **Potential doubling of Educates footprint** - assumed staging and production lab environments have sufficient scaling and capacity to accommodate

---

## Risks & Mitigation

### High Risk
1. **Spring Security API Changes**
   - **Mitigation:** Detailed estimate already created, early verification recommended

2. **Workshop Environment Updates** ⚠️ **NEW RISK AREA**
   - **Risk:** `jdk17-environment` → `jdk21-environment` may require infrastructure changes
   - **Risk:** New JDK environment images may not be available
   - **Risk:** Package versions may need updates
   - **Risk:** VS Code Java tools may need version updates
   - **Mitigation:**
     - Coordinate with infrastructure team early
     - Verify JDK 21 environment images are available
     - Test environment startup early in process
     - Allow 2 hours per workshop + 2 hours contingency (20 hours total)

3. **Increased Lab Resources** ⚠️ **NEW RISK AREA**
   - **Risk:** Potential doubling of Educates footprint may require additional capacity
   - **Risk:** Staging and production environments may not have sufficient scaling
   - **Mitigation:**
     - **Week 1 includes detailed profiling comparison of old vs. new versions**
     - Capacity impact forecast created early in project
     - Resource utilization analysis provided to infrastructure team
     - Early identification of capacity requirements
   - **Contingency:** +3 hours if capacity analysis reveals significant infrastructure changes needed

4. **Spring Initializr UI Changes**
   - **Risk:** Screenshots may be outdated
   - **Mitigation:** Regenerate screenshots after Spring Boot 4.0 GA

### Medium Risk
1. **Dependency Compatibility Issues**
   - **Mitigation:** Test early, have fallback versions ready

2. **Test Framework Changes**
   - **Mitigation:** Run tests early, update as needed

### Low Risk
1. **Content File Updates**
   - **Mitigation:** Mostly find/replace, easy to verify

---

## Success Criteria

- [ ] All content files updated with correct versions
- [ ] All 9 workshop start commits regenerated
- [ ] All 9 workshop stop commits regenerated
- [ ] All tests pass for all workshops
- [ ] All REST endpoints work correctly
- [ ] Security configuration works correctly
- [ ] Full course walkthrough successful
- [ ] Documentation links are current
- [ ] No deprecated patterns remain
- [ ] Course ready for deployment

---

## Dependencies

1. **Spring Boot 4.0 GA Release** - Required before finalizing
2. **Java 21 Environment** - Required for workshop infrastructure
   - **JDK 21 environment images** must be available
   - **Infrastructure team coordination** may be required
3. **Code Repository Access** - Required for workshop commits
4. **Infrastructure Team** - **Required** for environment updates and image availability
5. **Workshop Environment Resources** - All 9 workshop YAML files need updates

---

## Recommendations

1. **Start Early:** Begin with Workshop 02 to establish baseline
2. **Coordinate Environment Early:** ⚠️ **NEW** - Check with infrastructure team about Java 21 environment images **before** starting workshop updates
3. **Early Profiling:** ⚠️ **NEW** - Complete profiling and capacity analysis in Week 1 to identify resource requirements early
4. **OSS Process:** Establish GitHub Flow and fork repositories early in Week 1
5. **Test Incrementally:** Test each workshop as it's updated (both code and environment)
6. **Parallelize When Possible:** Environment updates can be done in parallel with content updates
7. **Monitor Releases:** Watch for Spring Boot 4.0 GA and Spring Security updates
8. **Document Changes:** Keep notes of any issues encountered, especially environment-related
9. **Peer Review:** Have another developer review security configurations
10. **Student Testing:** Have a test student complete the course before release, including environment testing
11. **Environment Validation:** Test each workshop environment startup after updates
12. **Capacity Planning:** Share profiling results with infrastructure team early for capacity planning

---

## Related Documents

- **UPGRADE_TASKS.md** - Detailed task checklist
- **SPRING_SECURITY_UPGRADE_ESTIMATE.md** - Detailed Spring Security upgrade estimate
- [Spring Boot 4.0 Release Notes](https://github.com/spring-projects/spring-boot/releases)
- [Spring Boot Migration Guide](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-4.0-Migration-Guide) (when available)

---

## Notes

- Estimates assume familiarity with Spring Boot and the course structure
- Times may vary based on experience level and unexpected issues
- Buffer time included for contingency
- Optional enhancements can be deferred if time is limited
- Some tasks can be parallelized with a team

---

**Last Updated:** Based on Spring Boot 4.0 RC2 and Spring Security 6.5.3
**Next Review:** After Spring Boot 4.0 GA release
