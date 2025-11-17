# Spring Boot 4.0 & Java 21/25 Upgrade Task List

## Overview
Upgrading from Spring Boot 3.1/Java 17 to Spring Boot 4.0/Java 21 (or 25).

**Reference:** [Spring Boot 4.0 Release Notes](https://github.com/spring-projects/spring-boot/releases)

**📊 See Summary Estimate:** `UPGRADE_ESTIMATE_SUMMARY.md` for comprehensive effort estimates (105 hours / ~13 days recommended, includes lab environment updates)

**🔒 See Spring Security Estimate:** `SPRING_SECURITY_UPGRADE_ESTIMATE.md` for detailed Workshop 09 breakdown (11.5 hours)

---

## 1. Content Repository Updates (This Repo)

### 1.1 Workshop Content Files
- [ ] **workshops/02-spring-initializr/workshop/content/01-spring-initializr.md**
  - Update Spring Boot version from "3.3.X" to "4.0.X" (line 15)
  - Update Java version from "17" to "21" or "25" (line 24)
  - Verify Initializr screenshot images are still accurate

### 1.2 Lesson Content Files
- [ ] Review all `content.md` files for version-specific references
- [ ] Update any Spring Boot version mentions in lesson descriptions
- [ ] Check for deprecated API references in code examples

### 1.3 Documentation Links
- [ ] Verify all Spring documentation links still point to current/relevant versions
- [ ] Update any version-specific documentation URLs if needed

---

## 2. Code Repository Updates
**Repository:** https://github.com/spring-academy/course-spring-brasb-build-a-rest-api-code

### 2.1 Project Bootstrap (Workshop 02)
- [ ] **Start Commit:** Regenerate project using Spring Initializr with:
  - Spring Boot 4.0.X
  - Java 21 (or 25)
  - Gradle - Groovy
  - Spring Web dependency
- [ ] **Stop Commit:** Verify generated project structure matches expectations
- [ ] Update `build.gradle` if any dependency management changes are needed

### 2.2 Dependencies Updates
- [ ] **workshops/06-spring-data:** Verify Spring Data JDBC compatibility with Spring Boot 4.0
  - Check `spring-data-jdbc` version alignment
  - Verify H2 database version compatibility
- [ ] **workshops/09-simple-spring-security:** Update Spring Security configuration
  - Spring Security 6.5.3 (included in Spring Boot 4.0)
  - Review `SecurityConfig` for any API changes
  - Test basic auth configuration still works

### 2.3 Code Changes for Breaking Changes

#### 2.3.1 Jakarta EE 11 Migration
- [ ] Verify all Jakarta imports are correct (should already be Jakarta from 3.x)
- [ ] Check for any remaining `javax.*` imports that need updating
- [ ] Test JAX-RS/Jakarta EE 11 compatibility

#### 2.3.2 Property Changes
- [ ] Review application properties for renamed properties:
  - `management.tracing.export.*` (if using observability)
  - `management.logging.export.*` (if using logging export)
- [ ] Update any custom configuration properties if needed

#### 2.3.3 Auto-Configuration Changes
- [ ] Test that all auto-configurations still work:
  - Spring Web MVC
  - Spring Data JDBC
  - Spring Security
  - H2 Database
- [ ] Verify test auto-configurations (`@WebMvcTest`, `@DataJdbcTest`, etc.)

### 2.4 Test Code Updates
- [ ] Review all test files for compatibility:
  - JUnit 5 (should be compatible)
  - AssertJ (should be compatible)
  - Spring Boot Test annotations
  - MockMvc usage
- [ ] Verify test execution with new Spring Boot version
- [ ] Check for any deprecated test utilities

### 2.5 Security Configuration
- [ ] **SecurityConfig.java:** Review for Spring Security 6.5.3/7.0 API changes
- [ ] Test `SecurityFilterChain` configuration
- [ ] Verify `BCryptPasswordEncoder` usage
- [ ] Test CSRF configuration (workshop 09, content 11-csrf.md)
- [ ] **See detailed estimate:** `SPRING_SECURITY_UPGRADE_ESTIMATE.md` for comprehensive breakdown
- [ ] **Note:** Lesson 09 and Workshop 09 require significant review (estimated 1.5 days)

### 2.6 Database Configuration
- [ ] Verify `schema.sql` and `data.sql` initialization still works
- [ ] Test H2 database compatibility
- [ ] Review Spring Data JDBC repository interfaces

---

## 3. Workshop Start/Stop Commits

Each workshop has start and stop commits that need to be regenerated:

- [ ] **Workshop 02:** Spring Initializr bootstrap
- [ ] **Workshop 04:** Test-first approach
- [ ] **Workshop 05:** First REST endpoint
- [ ] **Workshop 06:** Spring Data integration
- [ ] **Workshop 07:** POST endpoint creation
- [ ] **Workshop 08:** GET list endpoint
- [ ] **Workshop 09:** Spring Security integration
- [ ] **Workshop 10:** PUT endpoint implementation
- [ ] **Workshop 11:** DELETE endpoint implementation

**For each workshop:**
1. Create new start commit with Spring Boot 4.0/Java 21
2. Implement workshop steps
3. Create new stop commit
4. Verify all tests pass
5. Verify code matches workshop instructions

---

## 4. Java Language Features (17 → 21/25)

### 4.1 Consider Modern Java Features
- [ ] Review if records can be used instead of classes (if appropriate)
- [ ] Consider pattern matching for switch expressions (Java 21)
- [ ] Evaluate virtual threads usage (Java 21+) - though may be advanced for beginner course
- [ ] Review text blocks usage (Java 17+) if multi-line strings are used

### 4.2 Code Style Updates
- [ ] Ensure code examples follow Java 21 best practices
- [ ] Update any Java version-specific comments or documentation

---

## 5. Testing & Validation

### 5.1 Build Verification
- [ ] All projects build successfully with `./gradlew build`
- [ ] All tests pass: `./gradlew test`
- [ ] No deprecation warnings in build output

### 5.2 Runtime Verification
- [ ] Application starts successfully
- [ ] All REST endpoints work correctly:
  - GET /cashcards/{id}
  - GET /cashcards (with pagination/sorting)
  - POST /cashcards
  - PUT /cashcards/{id}
  - DELETE /cashcards/{id}
- [ ] Security endpoints work:
  - Basic authentication
  - Authorization checks
  - CSRF protection

### 5.3 Integration Testing
- [ ] Run full workshop flow from start to finish
- [ ] Verify each workshop's start → stop transition works
- [ ] Test that students can follow instructions and get expected results

---

## 6. Documentation & Metadata

### 6.1 Course Metadata
- [ ] Update course description if version-specific
- [ ] Review `course.template.json` for any version references
- [ ] Update module summaries if needed

### 6.2 Lesson Metadata
- [ ] Review all `lesson.json` files for accuracy
- [ ] Update any version-specific links or references

### 6.3 Workshop Metadata
- [ ] Verify `workshop.yaml` files don't have hardcoded versions
- [ ] Check `modules.yaml` files for accuracy

---

## 6A. Educates Platform Updates (Version 3.4.0)

### 6A.1 Workshop Content Migration to Hugo
- [ ] Migrate workshop content from classic format to Hugo format
- [ ] Review all workshop content files for Hugo compatibility
- [ ] Update content structure if needed for Hugo rendering
- [ ] Verify content renders correctly in Hugo format
- [ ] Test content in staging environment with Educates 3.4.0

**Note:** This migration is part of Educates 3.4.0 upgrade and affects all 9 workshops.

### 6A.2 Removal of Reconciler Configuration
- [ ] Remove reconciler configuration from workshop.yaml files
- [ ] Verify workshop functionality without reconciler
- [ ] Test workshop startup and execution
- [ ] Update documentation if reconciler references exist

**Note:** Reconciler configuration is deprecated/removed in Educates 3.4.0.

### 6A.3 Educates Authoring Flow Implementation
- [ ] **Separate Task:** Implement Educates authoring flow
- [ ] Review Educates 3.4.0 authoring flow documentation
- [ ] Update workshop creation/editing process to use new authoring flow
- [ ] Verify authoring flow works with updated workshop content
- [ ] Test authoring workflow in staging environment
- [ ] Document any authoring flow changes or requirements

**Note:** This is a distinctively separate task from content migration and should be tracked independently.

---

## 7. Key Spring Boot 4.0 Changes to Watch For

Based on release notes, pay special attention to:

### 7.1 Dependency Upgrades
- Spring Framework 6.2.10
- Spring Security 6.5.3
- Spring Data 2025.0.3
- Hibernate 6.6.26.Final (if using JPA later)
- Micrometer 1.15.3
- Tomcat 10.1.44

### 7.2 Property Renames
- `management.zipkin.tracing` → `management.tracing.export.zipkin`
- `management.opentelemetry.logging.export.*` properties renamed
- Various `management.tracing.export.{name}.enabled` properties

### 7.3 Auto-Configuration Changes
- OpenTelemetry auto-configuration refactored
- Micrometer tracing split into Brave and OpenTelemetry modules
- Jackson XML data format auto-configuration added

### 7.4 Test Changes
- `@JsonTest` and `@AutoConfigureJson` updates
- WebTestClient auto-configuration package changes
- Custom Jackson serializers handling

---

## 8. Migration Strategy

### Phase 1: Preparation
1. Review Spring Boot 4.0 migration guide (when available)
2. Review Java 21 migration guide
3. Set up new Spring Initializr project template

### Phase 2: Content Updates
1. Update all version references in content files
2. Review and update code examples
3. Update documentation links

### Phase 3: Code Updates
1. Start with Workshop 02 (bootstrap)
2. Progressively update each workshop
3. Test each workshop independently
4. Verify start/stop commits for each

### Phase 4: Integration Testing
1. Full course walkthrough
2. Student perspective testing
3. Fix any issues discovered

### Phase 5: Final Validation
1. Code review
2. Documentation review
3. Deployment testing

---

## 9. Notes & Considerations

- **Java Version Decision:** Choose between Java 21 (LTS) or Java 25 (latest). Java 21 is recommended for stability.
- **Spring Boot 4.0 Status:** Currently at RC2. Monitor for GA release before finalizing.
- **Backward Compatibility:** Spring Boot 4.0 may have breaking changes - test thoroughly.
- **Student Experience:** Ensure upgrade doesn't make course more complex for beginners.
- **Workshop Images:** May need to regenerate screenshots if UI changes in Spring Initializr.

---

## 10. Resources

- [Spring Boot 4.0 Release Notes](https://github.com/spring-projects/spring-boot/releases)
- [Spring Boot Migration Guide](https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-4.0-Migration-Guide) (when available)
- [Java 21 Features](https://openjdk.org/projects/jdk/21/)
- [Spring Initializr](https://start.spring.io/)

---

## Checklist Summary

- [ ] Content files updated (versions, examples)
- [ ] **Workshop content migrated to Hugo format (Educates 3.4.0)**
- [ ] **Reconciler configurations removed from all workshop.yaml files**
- [ ] **Educates authoring flow implemented and tested**
- [ ] All workshop start commits regenerated
- [ ] All workshop stop commits regenerated
- [ ] All tests passing
- [ ] Security configuration verified
- [ ] Database configuration verified
- [ ] Full course walkthrough completed
- [ ] Documentation reviewed and updated
- [ ] Ready for deployment
