# Table of Contents

- [Milestone 0 (M0) – Project Setup and Initial Configuration](#milestone-0-m0-–-project-setup-and-initial-configuration)
  - [1. Key Achievements](#1-key-achievements)
  - [2. Key Learnings & Concepts](#2-key-learnings-&-concepts)
  - [3. Challenges & Solutions](#3-challenges-&-solutions)
    - [Challenge 1: H2 Console and Spring Security](#challenge-1:-h2-console-and-spring-security)
    - [Challenge 2: Incorrect DataSource Injection](#challenge-2:-incorrect-datasource-injection)
    - [Challenge 3: Spring Profile-Specific Context Loading](#challenge-3:-spring-profile-specific-context-loading)
    - [Challenge 4: Application Property Syntax and H2 Configuration](#challenge-4:-application-property-syntax-and-h2-configuration)
  - [4. Reflection](#4-reflection)
  - [Milestone 1 – AbstractEntity (Model) Summary](#milestone-1-–-abstractentity-model-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [Milestone 1 – Jump Entity and JumpTests – Summary](#milestone-1-–-jump-entity-and-jumptests-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [M1 – JumpInsertDTO and JumpInsertDTOTest – Summary](#m1-–-jumpinsertdto-and-jumpinsertdtotest-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [M1 - M2 – Lookup DTOs & MapStruct Mappers — Milestone Summary](#m1---m2-–-lookup-dtos-&-mapstruct-mappers-—-milestone-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (Lessons Learned)](#challenges-&-solutions-lessons-learned)
    - [Reflection (Notes for Future Self)](#reflection-notes-for-future-self)
    - [Next logical steps (short checklist)](#next-logical-steps-short-checklist)
  - [Milestone 1 – Static Data Entities (Aircraft, Dropzone, Jumptype) and Repositories – Summary](#milestone-1-–-static-data-entities-aircraft,-dropzone,-jumptype-and-repositories-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [Milestone 1 – User Entity and Repository Tests – Summary](#milestone-1-–-user-entity-and-repository-tests-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [M2 - Exceptions - ErrorDTOs - ErrorHandler - JacksonConfig](#m2---exceptions---errordtos---errorhandler---jacksonconfig)
    - [Key achievements — what I completed](#key-achievements-—-what-i-completed)
    - [Key learnings & concepts I absorbed](#key-learnings-&-concepts-i-absorbed)
    - [Challenges I faced and how I solved them — a lessons-learned log](#challenges-i-faced-and-how-i-solved-them-—-a-lessons-learned-log)
    - [Reflection — notes for future me / design reminders](#reflection-—-notes-for-future-me-/-design-reminders)
    - [Concrete next steps checklist (practical & prioritized)](#concrete-next-steps-checklist-practical-&-prioritized)
    - [Final note (meta)](#final-note-meta)
- [M2 – JumpService (IJumpService & JumpServiceImpl) — Summary](#m2-–-jumpservice-ijumpservice-&-jumpserviceimpl-—-summary)
    - [Overview — subjects we covered](#overview-—-subjects-we-covered)
  - [Key achievements — what I completed and decisions I made](#key-achievements-—-what-i-completed-and-decisions-i-made)
  - [Key learnings & concepts — what I learned while doing this](#key-learnings-&-concepts-—-what-i-learned-while-doing-this)
    - [Spring Data & repository patterns](#spring-data-&-repository-patterns)
    - [Specification API & CriteriaBuilder](#specification-api-&-criteriabuilder)
    - [Mapping & DTO design](#mapping-&-dto-design)
    - [Transactional & exception handling behaviors](#transactional-&-exception-handling-behaviors)
    - [Testing patterns and pitfalls](#testing-patterns-and-pitfalls)
    - [Miscellaneous practical learnings](#miscellaneous-practical-learnings)
  - [Challenges & solutions — problems I hit and how I fixed them](#challenges-&-solutions-—-problems-i-hit-and-how-i-fixed-them)
    - [1. Tests passed individually but failed as a suite (0 vs expected counts)](#1-tests-passed-individually-but-failed-as-a-suite-0-vs-expected-counts)
    - [2. `ObjectOptimisticLockingFailureException` on save in tests](#2-objectoptimisticlockingfailureexception-on-save-in-tests)
    - [3. `DataIntegrityViolationException` when creating Jumptype in seed](#3-dataintegrityviolationexception-when-creating-jumptype-in-seed)
    - [4. Mapping update pattern confusion (MapStruct)](#4-mapping-update-pattern-confusion-mapstruct)
    - [5. Recursion bug when calculating totals](#5-recursion-bug-when-calculating-totals)
    - [6. Specification and tie-breaker ordering / pagination](#6-specification-and-tie-breaker-ordering-/-pagination)
    - [7. Unchecked cast warnings in test seed map](#7-unchecked-cast-warnings-in-test-seed-map)
  - [Reflection — notes for future work / how this changed my approach](#reflection-—-notes-for-future-work-/-how-this-changed-my-approach)
  - [What I’ll do next (practical TODOs)](#what-i’ll-do-next-practical-todos)
    - [Closing note (first-person)](#closing-note-first-person)
  - [M2 – StaticData + UserService (Exceptions / Service layer) — Learning Summary](#m2-–-staticdata-+-userservice-exceptions-/-service-layer-—-learning-summary)
    - [Key achievements](#key-achievements)
    - [Key learnings & concepts (what I learned)](#key-learnings-&-concepts-what-i-learned)
    - [Challenges, bugs, and how I solved them (lessons learned)](#challenges,-bugs,-and-how-i-solved-them-lessons-learned)
      - [1) StaticDataService unit tests initially failing](#1-staticdataservice-unit-tests-initially-failing)
      - [2) Validator in DTO unit tests — `validator` was null](#2-validator-in-dto-unit-tests-—-validator-was-null)
      - [3) MapStruct unmapped properties warning](#3-mapstruct-unmapped-properties-warning)
      - [4) Unit tests with Mockito: NPEs because mapper returned `null`](#4-unit-tests-with-mockito:-npes-because-mapper-returned-null)
      - [5) Mockito matchers & Spring context: `InvalidUseOfMatchersException`](#5-mockito-matchers-&-spring-context:-invaliduseofmatchersexception)
      - [6) DataIntegrity / “User already exists” debugging saga](#6-dataintegrity-/-“user-already-exists”-debugging-saga)
      - [7) Transactional/test isolation issues](#7-transactional/test-isolation-issues)
      - [8) Password change logic gotchas](#8-password-change-logic-gotchas)
      - [9) Pagination & listing](#9-pagination-&-listing)
    - [Reflection — what I’ll carry forward](#reflection-—-what-i’ll-carry-forward)
    - [Short list of concrete “do / don’t” reminders for future](#short-list-of-concrete-“do-/-don’t”-reminders-for-future)
  - [M3 – AuthController, AuthenticationService & Tests – Summary](#m3-–-authcontroller,-authenticationservice-&-tests-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [The Exact Lesson Learned (BadCredentialsException → UnauthorizedException)](#the-exact-lesson-learned-badcredentialsexception-→-unauthorizedexception)
    - [Challenges & Solutions (Lessons Learned / Bugs & Fixes)](#challenges-&-solutions-lessons-learned-/-bugs-&-fixes)
    - [Reflection](#reflection)
    - [Action Items / Next Steps](#action-items-/-next-steps)
  - [M3 – AuthenticationService (Authentication — Security) — Summary](#m3-–-authenticationservice-authentication-—-security-—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (lessons learned)](#challenges-&-solutions-lessons-learned)
    - [Reflection](#reflection)
    - [Next Steps](#next-steps)
    - [Actionable checklist (for repo notes)](#actionable-checklist-for-repo-notes)
  - [M3 – IJwtService / JwtServiceImpl & Tests — Summary](#m3-–-ijwtservice-/-jwtserviceimpl-&-tests-—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (lessons learned)](#challenges-&-solutions-lessons-learned)
    - [Reflection](#reflection)
    - [Next steps ](#next-steps)
  - [M3 – JwtAuthenticationFilter & SecurityFilterChain – Summary](#m3-–-jwtauthenticationfilter-&-securityfilterchain-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (Lessons Learned — detailed)](#challenges-&-solutions-lessons-learned-—-detailed)
      - [1) Circular dependency at ApplicationContext startup](#1-circular-dependency-at-applicationcontext-startup)
      - [2) `MockMvc` configuration and 404 / content-type surprises](#2-mockmvc-configuration-and-404-/-content-type-surprises)
      - [3) Header usage mistakes (mock request vs header string)](#3-header-usage-mistakes-mock-request-vs-header-string)
      - [4) `SecurityContextHolder` principal confusion in unit tests](#4-securitycontextholder-principal-confusion-in-unit-tests)
      - [5) Exceptions thrown by the filter vs AuthenticationEntryPoint handling](#5-exceptions-thrown-by-the-filter-vs-authenticationentrypoint-handling)
      - [6) Deterministic token helpers & ReflectionTestUtils timing](#6-deterministic-token-helpers-&-reflectiontestutils-timing)
      - [7) How I created expired and invalid-signature tokens (test helpers)](#7-how-i-created-expired-and-invalid-signature-tokens-test-helpers)
      - [8) Parameterized tests gotchas](#8-parameterized-tests-gotchas)
    - [Reflection](#reflection)
    - [Compact checklist / TL;DR (for future reference)](#compact-checklist-/-tl;dr-for-future-reference)
  - [M4 – REST Controllers & API Endpoint Tests](#m4-–-rest-controllers-&-api-endpoint-tests)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts (what I learned, phrased as new knowledge)](#key-learnings-&-concepts-what-i-learned,-phrased-as-new-knowledge)
    - [Challenges, Bugs, and Solutions (detailed lessons learned)](#challenges,-bugs,-and-solutions-detailed-lessons-learned)
    - [Reflection — Lessons for future development](#reflection-—-lessons-for-future-development)
    - [Final notes](#final-notes)
  - [M4 – REST Controllers (Auth, Users, Jumps, Lookups) — Summary](#m4-–-rest-controllers-auth,-users,-jumps,-lookups-—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection & Lessons Learned](#reflection-&-lessons-learned)
    - [Remaining TODOs / Next Steps](#remaining-todos-/-next-steps)
  - [M6 – Frontend UI (Dashboard & Jumps Page) – Fixes & Debugging Summary](#m6-–-frontend-ui-dashboard-&-jumps-page-–-fixes-&-debugging-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [M6 – Frontend UI (Dashboard & Jumps Page) — Summary](#m6-–-frontend-ui-dashboard-&-jumps-page-—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions](#challenges-&-solutions)
    - [Reflection](#reflection)
  - [M6 – Frontend UI (Delete, Edit & Ordinal Bug Fix) – Summary](#m6-–-frontend-ui-delete,-edit-&-ordinal-bug-fix-–-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (detailed, lesson-by-lesson)](#challenges-&-solutions-detailed,-lesson-by-lesson)
    - [Reflection](#reflection)
    - [Notes for future work / checklist](#notes-for-future-work-/-checklist)
  - [M6 – Frontend UI (Client for the REST API) (Register & Login)— Summary](#m6-–-frontend-ui-client-for-the-rest-api-register-&-login—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (Lessons Learned)](#challenges-&-solutions-lessons-learned)
      - [Major Bug - Login Form Not Sending POST Request & Page Reload After Successful Login](#major-bug---login-form-not-sending-post-request-&-page-reload-after-successful-login)
    - [Reflection](#reflection)
  - [M6 – Frontend UI - Styling (Auth Pages & Navbar) — Summary](#m6-–-frontend-ui---styling-auth-pages-&-navbar-—-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts (What I learned)](#key-learnings-&-concepts-what-i-learned)
    - [Challenges & Solutions (Bugs I ran into and how I fixed them)](#challenges-&-solutions-bugs-i-ran-into-and-how-i-fixed-them)
    - [Reflection (Lessons learned & notes for future reference)](#reflection-lessons-learned-&-notes-for-future-reference)
  - [M6 – Frontend UI (Dashboard & Jumps) — Reflective Summary](#m6-–-frontend-ui-dashboard-&-jumps-—-reflective-summary)
    - [Key Achievements](#key-achievements)
    - [Key Learnings & Concepts](#key-learnings-&-concepts)
    - [Challenges & Solutions (Lessons Learned / Bugs & Fixes)](#challenges-&-solutions-lessons-learned-/-bugs-&-fixes)
    - [Reflection](#reflection)
    - [Practical Notes for Future Reference](#practical-notes-for-future-reference)

# Milestone 0 (M0) – Project Setup and Initial Configuration

## 1. Key Achievements

During this milestone, I successfully:

* **Created the MySQL database** for my Skydiving Logbook REST API project and verified connectivity.
* **Configured application properties** with multiple profiles (`dev` and `test`) to separate development and testing environments.
* **Implemented initial Spring Boot configuration** for the application, including the `spring.datasource`, JPA, Hibernate, and logging properties.
* **Set up the H2 in-memory database** for the test profile, including enabling the H2 console for interactive inspection.
* **Configured initial smoke testing** to ensure the Spring Boot application boots correctly under the `test` profile.
* **Integrated JaCoCo for code coverage** to monitor which parts of the project are exercised by tests.
* **Verified that the application runs without Spring Security** temporarily, allowing me to focus on configuration and database connection without authentication interfering.

---

## 2. Key Learnings & Concepts

Through this milestone, I deepened my understanding of:

* **Spring Boot Profiles:** How `spring.profiles.active` allows me to separate development and test configurations, and why this is important for isolating environment-specific settings like databases.
* **H2 In-Memory Database:** How to configure H2, the purpose of `DB_CLOSE_DELAY=-1`, and how the console works for testing without Spring Security interfering.
* **Spring Boot Auto-Configuration:** How Spring Boot automatically provides a `DataSource` bean when a supported database driver is on the classpath and JPA starter is included.
* **JUnit 5 & Spring Boot Testing Integration:** How to write a simple smoke test with `@SpringBootTest` and `@ActiveProfiles` to confirm that the context loads and the application can start.
* **JaCoCo Coverage Reporting:** Why certain methods like `main(String[])` show 0% coverage and how coverage differs from test execution percentages.
* **Separation of Concerns in Testing:** Why I should defer Spring Security configuration until Milestone 3 to avoid unnecessary complexity during early testing.

---

## 3. Challenges & Solutions

### Challenge 1: H2 Console and Spring Security

* **Problem:** Visiting the H2 console redirected me to `/login` and required a username and password.
* **Solution:** I temporarily commented out the Spring Security dependency. This allowed me to access the console directly and verify the H2 in-memory database was functioning. I noted that Spring Security would be properly configured in Milestone 3.

### Challenge 2: Incorrect DataSource Injection

* **Problem:** Attempts to `@Autowired` a `DataSource` failed, giving `No beans of 'DataSource' type found`. Initially, I had imported `jakarta.activation.DataSource` instead of `javax.sql.DataSource`.
* **Solution:** Corrected the import to `javax.sql.DataSource`. I also verified that `spring-boot-starter-data-jpa` and H2 were on the classpath, and that my test class was located in the same package or subpackage as the main application class to ensure proper component scanning.

### Challenge 3: Spring Profile-Specific Context Loading

* **Problem:** I wanted a smoke test to load the `test` profile context, but initial attempts with `@Profile("test")` on the test method did not work.
* **Solution:** I learned to use `@ActiveProfiles("test")` at the class level, combined with `@SpringBootTest` and `@AutoConfigureTestDatabase` to ensure the context loads using the H2 test database.

### Challenge 4: Application Property Syntax and H2 Configuration

* **Problem:** There were small syntax issues in properties (e.g., misplaced comments in `spring.jpa.hibernate.ddl-auto`). Also, I initially tried a `create-drop # comment` value which Spring Boot could not parse.
* **Solution:** I removed inline comments from property values and used valid options (`create-drop`, `update`, `none`) to let Hibernate manage schema creation in the test database.

---

## 4. Reflection

* I learned that **setting up a project properly with multiple profiles and a test database** requires careful attention to classpath, imports, and package structure. Small mistakes like the wrong import or mislocated test class can completely prevent Spring Boot auto-configuration from working.
* Smoke testing is a powerful first step: it allows me to **verify the application boots, the context loads, and the database connection is functional** before writing any functional code.
* Separating concerns (deferring Spring Security) is important; it allows early progress without being blocked by features that are not yet implemented.
* Maintaining a **clean, readable `application-{profile}.properties` structure** prevents confusion and makes switching between environments reliable.
* Using **JaCoCo coverage early** highlighted gaps in testing and reinforced the idea that even simple bootstrap code (like `main()`) needs coverage if I want 100% metrics.
* I now have a solid foundation to start Milestone 1, confident that my **project structure, database setup, profiles, and basic testing framework** are all correctly in place.


## Milestone 1 – AbstractEntity (Model) Summary

### Key Achievements

During this milestone, I successfully:

1. **Designed and implemented `AbstractEntity`**

   * Created a base class for my domain entities to provide common audit fields: `createdAt` and `updatedAt`.
   * Applied JPA annotations `@MappedSuperclass`, `@EntityListeners(AuditingEntityListener.class)`, and Hibernate’s `@DynamicInsert`.
   * Integrated Spring Data JPA auditing annotations `@CreatedDate` and `@LastModifiedDate` to automatically populate the timestamps.

2. **Created a test-only entity**

   * Implemented `TestOnlyEntityTest` that extends `AbstractEntity` to enable unit testing of the auditing behavior without impacting real domain entities.
   * Configured this entity with a simple `id` and `name` to test persistence and timestamp handling.

3. **Developed and executed unit tests**

   * **Test 1 – Creation timestamps:** Verified that upon saving a new entity, both `createdAt` and `updatedAt` are populated and initially equal.
   * **Test 2 – Update timestamps:** Verified that when updating an entity, `updatedAt` changes while `createdAt` remains unchanged, including a small delay to ensure timestamp difference is detectable.
   * **Test 3 – Constraint testing (revised):** Explored testing database constraints, realized auditing prevents nulls, and instead verified that auditing ensures timestamps are never null.

4. **Configured the test environment**

   * Leveraged `@DataJpaTest` with the `test` profile and H2 in-memory database for fast, isolated testing.
   * Ensured `saveAndFlush` was used to trigger JPA events and persist data immediately for accurate testing of timestamps.

---

### Key Learnings & Concepts

Through completing this milestone, I deepened my understanding of several important Spring Boot and JPA concepts:

1. **Spring Data JPA Auditing**

   * Learned how `@CreatedDate` and `@LastModifiedDate` annotations automatically populate audit fields when `AuditingEntityListener` is active.
   * Understood that auditing runs **before Hibernate persists the entity**, meaning database constraints on timestamps are effectively handled by auditing.

2. **JPA Entity Inheritance**

   * Learned how to use `@MappedSuperclass` to create reusable base entities.
   * Recognized that base entities don’t correspond to their own table, but their fields are inherited by subclasses.

3. **Unit Testing with JPA**

   * Gained practical experience using `@DataJpaTest` to test repository-layer interactions.
   * Understood the difference between setting a field in memory versus persisting it to trigger database constraints.
   * Learned the correct usage of `saveAndFlush` to immediately synchronize the persistence context with the database.

4. **Lambda Expressions in Tests**

   * Reinforced my understanding of lambdas in Java, specifically in exception testing (`assertThrows`).
   * Learned that the lambda must **wrap the action that actually triggers the exception**, not just setters in memory.

5. **Testing Strategy Refinement**

   * Learned that tests for database constraints on audited fields are not meaningful while auditing is active, leading me to adjust the focus of Test 3 to verifying correct automatic timestamp population.

---

### Challenges & Solutions

1. **Null timestamp constraint failure**

   * **Challenge:** Attempted to persist an entity with `createdAt = null` and `updatedAt = null` and expected a `ConstraintViolationException`.
   * **Solution:** Realized auditing automatically fills these fields, so the exception never occurs. Revised the test to assert that timestamps are **always populated**, which aligns with actual application behavior.

2. **Using `assertThrows`**

   * **Challenge:** Initially tried `assertThrows(ConstraintViolationException.class, savedEntity.setCreatedAt())`, which failed to compile.
   * **Solution:** Learned that the argument to `assertThrows` must be a **lambda or method reference**, wrapping the **actual code that triggers the exception**, e.g., `() -> repository.saveAndFlush(entity)`.

3. **Timing differences in update test**

   * **Challenge:** Needed to ensure `updatedAt` differs from `createdAt` in update tests.
   * **Solution:** Introduced a `Thread.sleep()` delay between creation and update operations, confirming timestamp difference reliably.

4. **JaCoCo coverage confusion**

   * **Challenge:** Coverage reports did not show `AbstractEntityTest`.
   * **Solution:** Learned that JaCoCo reports **coverage of main code only**, not test classes. Verified that `AbstractEntity` itself was being exercised through repository operations, which is what matters for coverage.

---

### Reflection

* This milestone reinforced the **importance of understanding the behavior of frameworks** (Spring Data JPA, Hibernate) rather than blindly testing database constraints.
* I learned to **adjust testing strategies** to align with actual runtime behavior, which prevents writing brittle or meaningless tests.
* Understanding **lambda expressions** in the context of testing strengthened my ability to write concise and correct unit tests.
* Using a **test-only entity** was a smart strategy to isolate auditing behavior without affecting production entities.
* Going forward, I should remember that **auditing intercepts persistence operations**, so tests expecting database exceptions must account for any framework-level pre-processing.

## Milestone 1 – Jump Entity and JumpTests – Summary

### Key Achievements

During this milestone, I successfully:

1. **Designed and implemented the `Jump` entity**

   * Created the `Jump` entity with JPA annotations, mapping it to the `jump` table in the database.
   * Added both a numeric primary key (`id`) and a public `UUID`) for external references.
   * Applied validation annotations such as `@Positive` for `altitude` and `freeFallDuration`, and `@PastOrPresent` for `jumpDate`.
   * Implemented `@PrePersist` to automatically generate UUIDs before saving if none exists.
   * Established `@ManyToOne` relationships with the static data entities: `Aircraft`, `Dropzone`, and `Jumptype`.
   * Enforced `nullable = false` on critical fields and relationships to prevent invalid persistence.

2. **Created repository and persistence layer integration**

   * Leveraged Spring Data JPA to implement `JumpRepository`.
   * Ensured repository operations such as `save`, `saveAndFlush`, and `findById` function correctly.
   * Used H2 in-memory database with `@DataJpaTest` and active `test` profile for fast, isolated persistence testing.

3. **Developed comprehensive positive and negative tests**

   * Wrote a positive test to confirm that a valid `Jump` is persisted successfully, asserting scalar fields, UUID generation, and relational mappings.
   * Tested nullability constraints using a parameterized test, asserting `DataIntegrityViolationException` is thrown when required fields or relationships are null.
   * Tested validation constraints (altitude > 0, freeFallDuration > 0, jumpDate not in the future) with parameterized tests, asserting `ConstraintViolationException` is thrown when violated.
   * Verified UUID generation behavior, including preserving a pre-set UUID and automatically generating a UUID when none is provided.
   * Implemented helper methods for creating and persisting related static entities (`Aircraft`, `Dropzone`, `Jumptype`) to ensure relational integrity in tests.

4. **Structured test data preparation**

   * Used helper methods for creating and persisting related entities to simplify test setup.
   * Discussed the option of using `@BeforeEach` to persist static entities once per test to reduce duplication and maintain clean H2 state across tests.

---

### Key Learnings & Concepts

Through completing this milestone, I deepened my understanding of several important concepts:

1. **Entity relationships and `@ManyToOne` mapping**

   * Learned how `@ManyToOne` works in practice, assigning foreign keys and managing directionality from the owning side (Jump) to static entities.
   * Understood the importance of persisting related entities before assigning them to the Jump entity to avoid transient object errors.

2. **Bean validation vs database constraints**

   * Reinforced the difference between application-level validations (`@Positive`, `@PastOrPresent`) and database-level constraints (`nullable = false`, `unique = true`).
   * Learned that `ConstraintViolationException` is triggered by Bean Validation, whereas `DataIntegrityViolationException` arises from DB constraints during flush.

3. **TDD practices with JPA entities**

   * Learned to write tests first for both positive and negative scenarios before implementation.
   * Learned the importance of testing both scalar fields and relational fields to confirm full persistence.
   * Applied parameterized testing to loop over fields, maintaining DRY test structure while verifying multiple constraints.

4. **UUID management and identity handling**

   * Learned how to use `@PrePersist` to generate UUIDs automatically.
   * Reinforced the pattern of combining numeric primary keys for internal references with UUIDs for external references.

5. **Test data preparation and reusability**

   * Learned to persist static reference entities in helper methods and the option of using `@BeforeEach` to reduce duplication.
   * Recognized the impact of creating new persisted entities per test on H2 database state and test predictability.

---

### Challenges & Solutions

1. **Handling transient related entities**

   * **Challenge:** Initially, assigning freshly instantiated Aircraft, Dropzone, and Jumptype to a Jump caused persistence errors because they were transient.
   * **Solution:** Created helper methods that save and flush these entities first, returning managed instances for use in Jump creation.

2. **Testing nullability and constraints properly**

   * **Challenge:** Parameterized tests were initially calling `createValidJump()` inside the assertion, which ignored modifications to fields and invalid values.
   * **Solution:** Updated tests to modify the actual `jump` instance before calling `saveAndFlush`, ensuring exceptions are triggered correctly.

3. **Validating future dates**

   * **Challenge:** Needed to enforce that `jumpDate` cannot be in the future.
   * **Solution:** Applied `@PastOrPresent` on `jumpDate` and wrote tests setting a future date, asserting `ConstraintViolationException` is thrown.

4. **UUID generation and immutability**

   * **Challenge:** Ensuring UUID is generated automatically when missing but preserved if pre-set.
   * **Solution:** Implemented `@PrePersist` logic and wrote tests for both automatic generation and pre-set UUID preservation.

---

### Reflection

* This milestone reinforced my ability to **design and test entities with proper validation, relationships, and identity management** in Spring Boot.
* I learned that **persistence tests must reflect actual constraints and relationships**; modifying the wrong object or using unsaved entities can invalidate the test.
* Parameterized testing proved extremely useful for **maintaining DRY tests across multiple fields**.
* I gained confidence in handling **positive and negative persistence scenarios**, including null constraints, validation rules, relational integrity, and automatic UUID management.
* Using helper methods and potentially `@BeforeEach` ensures clean and reusable test setup, improving test clarity and performance.

**Notes for future reference:**

* When adding more relational entities, always persist dependencies first to avoid transient object errors.
* Maintain clear separation between positive creation tests and negative constraint tests.
* Continue leveraging parameterized tests to test multiple fields with minimal boilerplate.
* UUIDs should remain immutable once set, and automatic generation should only occur if missing.


## M1 – JumpInsertDTO and JumpInsertDTOTest – Summary

### Key Achievements

During this milestone, I successfully:

* **Designed and implemented the `JumpInsertDTO` class**

  * Created a Data Transfer Object for creating new Jump entries in the REST API.

  * Applied validation annotations (`@NotNull`, `@Min`, `@Max`, `@PastOrPresent`, `@Size`) to enforce correctness for fields such as `altitude`, `freeFallDuration`, `jumpDate`, `jumpNotes`, `aircraftId`, `dropzoneId`, and `jumptypeId`.

  * Carefully distinguished between mandatory fields (`@NotNull`) and optional fields (like `jumpNotes` with max-length constraint only).

  * Ensured the DTO is decoupled from the Jump entity, maintaining proper RESTful architecture and enabling validation without persistence dependencies.

* **Created comprehensive DTO validation tests (`JumpInsertDTOTest`)**

  * Developed a happy path test (`jumpInsertDTOSuccessTest`) to verify that valid DTO input passes all constraints.

  * Implemented multiple parameterized tests using different approaches:

    * **`@ValueSource`** for primitive types (`altitude`, `freeFallDuration`) to test min/max boundary conditions efficiently.
    * **`@MethodSource`** with `Stream<Arguments>` for more complex types (`jumpDate`, `jumpNotes`) and for fields needing multiple parameters like validity flags.
    * **`@MethodSource`** for null testing, dynamically setting each `@NotNull` field to `null` and asserting violations.

  * Asserted both positive and negative cases for all fields, covering edge cases such as altitude outside allowed range, future dates, negative free fall durations, and notes exceeding maximum length.

  * Programmatically used Jakarta Bean Validation (`Validator.validate(dto)`) to collect constraint violations and assert expectations.

* **Established a TDD workflow for DTO validation**

  * Wrote all tests first, prior to any service or controller integration.

  * Defined explicit scenarios for both happy and negative paths, including nulls, boundary values, future dates, and string length limits.

  * Built confidence that DTO validation rules are robust and deterministic before moving on to mapping or persistence logic.

---

### Key Learnings & Concepts

Through completing this milestone, I deepened my understanding of several critical concepts:

* **DTO role in REST APIs**

  * Reinforced why DTOs provide a clean separation between API inputs and entity persistence.

  * Understood that DTOs allow precise validation and control over incoming data while keeping entities isolated from client-side manipulation.

* **Jakarta Bean Validation**

  * Learned how `Validator.validate(dto)` can be used programmatically to test DTOs without a database.

  * Clarified the behavior of annotations like `@NotNull`, `@Min`, `@Max`, `@PastOrPresent`, and `@Size` in combination, and learned which edge cases trigger violations.

* **Parameterized testing**

  * Explored different ways to implement parameterized tests:

    * **`@ValueSource`** – quick for primitives, very readable, but limited to single values and types.
    * **`@MethodSource`** – flexible for complex objects, multiple parameters, nulls, and dynamic validity flags.
    * **`Stream<Arguments>`** – allows structured input and multiple arguments per test case.
  * Learned how to use parameterized tests to reduce repetitive code while still covering a wide range of valid and invalid scenarios.

* **Streams and violation inspection**

  * Practiced interpreting `Set<ConstraintViolation<T>>` and asserting expected violations.

  * Learned to dynamically manipulate DTO fields in tests (e.g., setting a field to `null` or invalid values) and assert that validation captures the correct violation.

---

### Challenges & Solutions

* **Testing complex types with parameterized tests**

  * Challenge: Could not use `@ValueSource` with `LocalDateTime` or object types.

  * Solution: Switched to `@MethodSource` with `Stream<Arguments>` for dates, notes, and null testing. This allowed passing complex objects along with validity flags.

* **Dynamic null testing for multiple fields**

  * Challenge: Needed a single parameterized test to check all `@NotNull` fields, but fields were of different types (`Integer`, `Long`, `LocalDateTime`).

  * Solution: Passed `Object value` from the method source and cast to the correct type inside a switch statement. This enabled testing all null constraints in one reusable test.

* **Boundary and invalid value assertions**

  * Challenge: Initially, separate tests were repetitive for altitude, freeFallDuration, and notes length.

  * Solution: Used parameterized tests with clear switches or flags to assert violations only when expected. This reduced boilerplate while preserving clarity.

* **Streams and lambda syntax**

  * Challenge: Misused `anyMatch` lambda syntax when trying to assert specific violations.

  * Solution: Corrected to `anyMatch(v -> v.getPropertyPath().toString().equals("fieldName"))` to correctly identify violations.

---

### Reflection

This milestone reinforced the importance of **rigorous DTO validation** and **TDD discipline**:

* Explicitly testing nulls, boundary values, future/past dates, and string lengths ensures robust API input validation before even touching services or controllers.

* Parameterized tests are powerful tools for reducing redundancy, but they require careful design when fields are of mixed types or require multiple parameters.

* The combination of `Validator.validate()`, `Set<ConstraintViolation<T>>`, and Java Streams allows precise, expressive assertions about which fields fail validation.

* My exploration of `@ValueSource` vs `@MethodSource` solidified when to use each approach:

  * Quick primitives → `@ValueSource`.
  * Complex types, multiple arguments, or nulls → `@MethodSource` with `Stream<Arguments>`.

**Notes for future reference:**

* Keep DTO tests independent from entity persistence to maintain separation of concerns.
* Always handle null and empty inputs explicitly in tests; Bean Validation annotations behave differently depending on nullability.
* Consider adding helper methods to construct valid DTOs and reduce repetitive setup in future parameterized tests.
* In subsequent milestones (service layer, mapping, and controller integration), rely on this robust validation foundation to catch input errors early.


## M1 - M2 – Lookup DTOs & MapStruct Mappers — Milestone Summary

### Key Achievements

During these tasks I completed the Lookup/Read-only DTOs and the MapStruct mapping layer, and exercised them with focused tests. Concretely I:

* **Implemented Lookup DTOs for static data and jumps**

  * Created `AircraftLookupDTO`, `DropzoneLookupDTO`, `JumptypeLookupDTO` (Lombok-based, all-args + no-args constructors, getters/setters).
  * Created `JumpLookupDTO` with the read-only fields I need for responses: `createdAt`, `updatedAt`, `id`, `uuid`, `altitude`, `freeFallDuration`, `jumpDate`, `jumpNotes`, and flattened reference fields as `String` values (`aircraft`, `dropzone`, `jumptype`, `user`).

* **Integrated MapStruct into the build**

  * Added MapStruct dependencies and annotation processor entries to Gradle (`org.mapstruct:mapstruct` + `org.mapstruct:mapstruct-processor`) along with the `testAnnotationProcessor` entry for test mappers.
  * Added compiler options to remove generator timestamps/version comments and to get verbose processing output during build.

* **Set up Lombok + MapStruct interoperability**

  * Chose Lombok for DTOs (kept `@Getter`, `@Setter`, `@NoArgsConstructor`, `@AllArgsConstructor`) and made sure to handle MapStruct/Lombok annotation processing (lombok-mapstruct-binding where needed).

* **Built mappers for the static data and Jump**

  * Created mapper interfaces with `@Mapper(componentModel = "spring")` so MapStruct generates Spring beans: `AircraftMapper`, `DropzoneMapper`, `JumptypeMapper`, `JumpMapper`, `UserMapper`, etc.
  * For simple cases where entity and DTO field names matched (e.g. `aircraftName` ↔ `aircraftName`) relied on MapStruct’s automatic name-based mapping.
  * Implemented `JumpMapper` mapping both `JumpInsertDTO → Jump` and `Jump → JumpLookupDTO`; handled the complexity of nested entity fields (entity references) vs DTO flattened string fields.

* **Wrote and iterated mapper tests**

  * Wrote `AircraftMapperTest`, `JumpMapperTest`, `UserMapperTest` to verify mappings (happy paths, null input, null-field edge cases).
  * Tested both injection scenarios: using Spring (`@SpringBootTest` + `@Autowired`) and recognizing the alternative of `Mappers.getMapper()` for pure unit tests.

* **Made pragmatic design decisions for relationship handling**

  * Decided to keep mappers simple and defer entity resolution (aircraft, dropzone, jumptype, user) to the service layer rather than forcing ID→entity logic into MapStruct. This keeps mappers pure transformers and the lookup/validation logic where it belongs.

---

### Key Learnings & Concepts

These are the main technical concepts and practical techniques I internalized while completing this milestone:

* **MapStruct fundamentals**

  * MapStruct is a compile-time code generator — you write mapper interfaces and MapStruct produces a `...Impl` class at build time.
  * `@Mapper(componentModel = "spring")` instructs MapStruct to generate a Spring bean implementation, which can then be `@Autowired` into services and tests.
  * MapStruct matches properties by **name and type**. If names/types match, mappings are generated with no extra configuration. If they differ, I must provide `@Mapping` or helper methods.

* **When to add explicit mappings or helper methods**

  * If target and source types differ (for example `Aircraft` → `String`), MapStruct needs either:

    * a custom `@Mapping` expression/qualifier or
    * a helper method in the mapper (`default String map(Aircraft a) { return a == null ? null : a.getAircraftName(); }`),
    * or to receive fully-resolved objects (resolve in service before saving).
  * For DTO → Entity where DTOs only carry `id`s but entities require references, common options are:

    * create lightweight placeholder entities (`new Aircraft(id)`), or
    * perform repository lookups in the service layer and set the entity references there (what I chose).

* **Testing strategy for mappers (TDD)**

  * Unit tests for mappers: fast, do not require Spring context (use `Mappers.getMapper()`), but integration tests with `@SpringBootTest` are useful to ensure generated beans are available via DI.
  * Tests should assert mapping correctness (field values), behavior on `null` inputs, and mapping of collections (order preservation), not validation that belongs at the DTO or DB level.
  * DTO validation belongs at the DTO layer and is tested separately with Bean Validation tests — not in mapper tests.

* **Where validation belongs**

  * I reinforced the architectural principle: **validate at the edge** (DTOs, controller input), and keep mappers free of validation logic. The DB constraints are the second safety net.
  * As a consequence I removed tests that expected mappers to throw `IllegalArgumentException` on missing required fields — those assertions were wrong because validation should have prevented nulls earlier.

* **Useful practical tips**

  * If MapStruct does not generate implementations:

    * check annotation processor configuration,
    * verify `@Mapper(componentModel = "spring")` syntax (I actually forgot the parentheses once — that caused `No qualifying bean` errors),
    * rebuild and inspect `build/generated/sources/annotationProcessor/...` for generated classes.
  * Avoid `LocalDateTime.now()` directly in assertions — precompute expected dates for deterministic tests.
  * Java `switch` does not create scopes for `case` labels — I hit variable re-declaration issues in parameterized tests until I wrapped cases in `{}` or used pre-declared variables.

---

### Challenges & Solutions (Lessons Learned)

Below I list the specific problems I encountered and the concrete solutions I implemented or considered — this is my lessons-learned log.

1. **Instantiating interface mappers incorrectly**
   *Problem:* I attempted to instantiate a mapper with `new AircraftMapper() { ... }` in a test.
   *Why it was wrong:* `AircraftMapper` is an interface, and MapStruct generates the implementation; you must use `Mappers.getMapper(AircraftMapper.class)` for fast unit tests or `@Autowired` with `@SpringBootTest` when using `componentModel = "spring"`.
   *Fix:* Use `Mappers.getMapper()` for pure mapper unit tests, or annotate mapper interfaces with `@Mapper(componentModel = "spring")` and `@Autowired` them in integration tests.

2. **Mapper method signature mistake**
   *Problem:* I wrote `Aircraft aircraftToLookupDTO(Aircraft aircraft)` (returning `Aircraft`) by accident.
   *Why it was wrong:* The mapper must return the DTO type, e.g., `AircraftLookupDTO aircraftToLookupDTO(Aircraft aircraft)`.
   *Fix:* Correct method signatures so source type ≠ target type reflect DTO ↔ entity mapping.

3. **`@Mapper(componentModel = "spring")` syntax missing parentheses**
   *Problem:* After missing the parentheses, Spring couldn’t find the generated bean (`No qualifying bean` error).
   *Fix:* Add the parentheses and rebuild: `@Mapper(componentModel = "spring")`.

4. **MapStruct error mapping entity object to string**
   *Problem:* MapStruct reported: *"Can't map property `Aircraft aircraft` to `String aircraft`. Consider a mapping method: `String map(Aircraft)`."*
   *Root cause:* I had `JumpLookupDTO.aircraft` typed as `String` while `Jump.aircraft` was an `Aircraft` object. MapStruct doesn’t know how to convert an `Aircraft` instance to a `String`.
   *Solutions I considered and implemented:*

   * add helper mapping methods in the mapper (e.g., `default String map(Aircraft a) { return a == null ? null : a.getAircraftName(); }`), or
   * change DTO to contain nested lookup DTO (`AircraftLookupDTO aircraft`) if richer data is needed, or
   * keep the mapper simple and set flattened string fields in the service layer (I chose to resolve relationships in service or use helper methods as needed).

5. **Unmapped target properties when mapping DTO → Entity**
   *Problem:* MapStruct complained about unmapped targets (`id`, `uuid`, `aircraft`, `dropzone`, `jumptype`, `user`) for `jumpInsertDTOtoJumpEntity`.
   *Why:* the DTO intentionally did not contain `id`/`uuid` (generated) or entity references (it only had IDs). MapStruct expects all target properties mapped unless configured otherwise.
   *Fixes and options:*

   * explicitly ignore generated fields: `@Mapping(target = "id", ignore = true)` and `@Mapping(target = "uuid", ignore = true)`,
   * either add mapping helper methods for ID→entity transformations (placeholder entities) or **resolve related entities in service** before saving (I chose the latter for cleaner separation).
     *Decision:* Leave `id` and `uuid` ignored in the mapper and resolve `aircraft/dropzone/jumptype/user` in the service implementation.

6. **Tests expecting mapper to throw on nulls**
   *Problem:* I wrote tests asserting mappers throw exceptions for null fields, but mappers did not throw — validation lives upstream.
   *Lesson:* Don’t duplicate validation in mapper tests; update tests to assert mapping behavior (mapping nulls to nulls or mapping to safe defaults) rather than expecting exceptions. I removed or refactored those failing tests.

7. **Switch-scoping and parameterized test gotchas**
   *Problem:* Redeclaring local variables inside `switch` `case` labels caused compiler errors. Also a `case` fall-through caused unintended behavior.
   *Fix:* Use `{}` blocks inside each `case` or pre-declare variables outside the `switch`, or use `if/else` instead. Always include `break` to avoid unintended fall-through.

8. **Using `LocalDateTime.now()` in tests**
   *Problem:* Assertions comparing `LocalDateTime.now()` created flaky tests.
   *Fix:* Use deterministic values or truncate to date-only `LocalDateTime` values computed once in the test setup.

9. **Duplicate or paste mistakes**
   *Problem:* I pasted `DropzoneLookupDTO` twice by mistake when sharing code — no functional problem, but a reminder to watch copy/paste errors.
   *Lesson:* Keep an eye on PRs/commits to avoid accidental duplicates.

---

### Reflection (Notes for Future Self)

* MapStruct is powerful and keeps mappers concise — but the design choices matter: decide early whether mapping should handle ID→entity resolution or if that must be done in services. I found keeping mappers pure and handling lookups in services leads to clearer responsibilities and easier testing.

* Keep validation at the edge (DTOs) and the DB; avoid duplicating `@NotNull` checks in mappers. Tests should verify that validation occurs at the DTO layer and mapping correctness separately.

* When field names match, rely on MapStruct’s automatic mapping. When they differ or types differ, choose between:

  * `@Mapping` annotations on methods,
  * helper/default mapping methods inside the mapper,
  * or higher-level service logic for entity resolution.

* Central `MapperConfig` (`@MapperConfig`) is a useful future enhancement: it can set `componentModel = "spring"`, `unmappedTargetPolicy = ERROR`, `nullValueMappingStrategy = RETURN_DEFAULT`, etc., so every mapper inherits consistent behavior. I can add this when I have more mappers and want stricter compile-time guarantees.

* Use immutable DTOs where appropriate. I picked Lombok for convenience now, but Java `record`s are a good future option for simple read-only lookup DTOs because they express immutability and are concise. If using Lombok, remember `lombok-mapstruct-binding` to avoid processor ordering issues.

* Test strategy recap:

  * Keep mapper unit tests fast and focused (use `Mappers.getMapper()`), and add a small set of `@SpringBootTest` integration checks to ensure mappers are discoverable as beans.
  * Test DTO validation separately using `Validator.validate(dto)` and assert violations via `Set<ConstraintViolation>`.
  * Do not assert exceptions at the mapper layer for things that the DTO validation already prevents.

* Small practical tips:

  * Run `./gradlew clean build` after changing MapStruct/Lombok configuration and inspect `build/generated/sources/annotationProcessor` to confirm generated implementations.
  * Use `assertAll` to group multiple related assertions in mapper happy-path tests.
  * When mapping nested objects to primitives (e.g., `Aircraft` → `String`), prefer explicit helper methods for clarity and to avoid subtle null dereferences.

---

### Next logical steps (short checklist)

1. (Optional) Create a central `MapperConfig` and apply it across mappers for consistent policies.
2. Finalize the decision about whether `JumpInsertDTO` should carry `userId` (I leaned toward resolving current user from security context in service but it’s worth documenting).
3. Add service-layer tests that assert repository lookups (aircraft/dropzone/jumptype) are performed and proper exceptions are thrown when references are missing.
4. Consider swapping read-only Lookup DTOs to `record`s if I want strict immutability later (evaluate trade-offs with Lombok in current project).
5. Add controller-level integration tests to confirm serialized DTO shape on the API endpoints (`GET /api/aircrafts`, `GET /api/jumptypes`, `GET /api/jumps/{id}`).
6. If I need even stricter mapping guarantees, set `unmappedTargetPolicy = ERROR` (via `@MapperConfig`) and run the build to discover missing mappings early.

---

This milestone deepened my practical understanding of MapStruct, DTO responsibilities, and where validation and entity resolution belong in a layered application. I now have working Lookup DTOs, mappers, and a set of tests verifying the contracts. The key behavioral decisions (keep mappers pure; resolve relationships in services) and the test patterns I established will make the next milestones (services, controllers, auth) much smoother.



## Milestone 1 – Static Data Entities (Aircraft, Dropzone, Jumptype) and Repositories – Summary

### Key Achievements

During this milestone, I successfully:

1. **Designed and implemented static data entities**

   * Created three domain entities: **Aircraft**, **Dropzone**, and **Jumptype**.
   * Annotated them with `@Entity` to map them to database tables.
   * Defined primary keys with `@Id` and `@GeneratedValue`.
   * Added basic attributes such as names or descriptions for each entity to represent core static reference data in the application.

2. **Created repositories**

   * Implemented repositories by extending Spring Data JPA’s `JpaRepository` for each entity (`AircraftRepository`, `DropzoneRepository`, `JumptypeRepository`).
   * Gained access to built-in CRUD methods (`findAll`, `save`, `delete`, etc.) with no boilerplate code.

3. **Validated persistence through tests**

   * Wrote repository tests using `@DataJpaTest` and H2 in-memory database to confirm entities could be saved, retrieved, and deleted successfully.
   * Used methods like `findById(...).orElseThrow()` to enforce strict validation of retrieval operations.
   * Explored constraint-related tests and learned how validation and database enforcement interact with JPA and Spring Boot.

---

### Key Learnings & Concepts

Through completing this milestone, I solidified my understanding of several key concepts:

1. **Entity modeling for static data**

   * Learned how to represent fixed reference data (e.g., aircraft types, jump types, dropzones) as persistent JPA entities rather than hardcoding them.
   * Understood that treating static data as first-class entities keeps the design extensible and consistent across the domain model.

2. **Spring Data JPA repositories**

   * Learned that extending `JpaRepository` provides a powerful abstraction over persistence, giving me a full set of CRUD operations out of the box.
   * Understood how repository interfaces fit into a clean, domain-driven structure, separating persistence concerns from business logic.

3. **Testing repositories with JPA**

   * Practiced using `@DataJpaTest` with H2 for lightweight, isolated repository testing.
   * Reinforced that `saveAndFlush()` can be used to force immediate synchronization with the database, which is crucial when validating exceptions or persistence state.
   * Learned how `Optional` works in practice with repository results, specifically using `orElseThrow()` to avoid null handling and enforce strict presence of data.

4. **Constraint validation and auditing interactions**

   * Learned that exceptions like `ConstraintViolationException` or `DataIntegrityViolationException` only occur if validation annotations (`@NotNull`, etc.) or database-level constraints exist.
   * Understood that auditing (from earlier AbstractEntity work) may fill certain fields before persistence, preventing some constraint violations from surfacing.

---

### Challenges & Solutions


1. **Understanding `Optional.orElseThrow()`**

   * **Challenge:** Needed to clarify how `orElseThrow()` works when calling `findById(...)`.
   * **Solution:** Realized it’s a way to enforce strict handling of missing values — if the entity isn’t found, the lambda inside `orElseThrow()` is executed, throwing a clear exception instead of returning null. This strengthens repository test correctness.

2. **Testing for exceptions**

   * **Challenge:** Expected `ConstraintViolationException` or `DataIntegrityViolationException` to be thrown when saving invalid entities, but no exceptions occurred.
   * **Solution:** Learned that without explicit validation annotations (`@NotNull`, `@Size`, etc.) or actual database constraints, JPA will not raise these errors. Adjusted testing expectations accordingly.

---

### Reflection

* This milestone gave me confidence in **structuring the persistence layer** for static reference data and reinforced the power of Spring Data JPA repositories.
* I learned that **tests must align with actual persistence behavior**, not assumptions — exceptions only occur if validation or constraints are explicitly present.
* I became more comfortable using `Optional` in repository results and recognized how `orElseThrow()` is a clean way to enforce non-null retrievals in tests and business logic.
  
Notes for future reference:

* Always annotate entity fields with the appropriate validation constraints if I want predictable database exceptions.
* Use repository tests not only for CRUD correctness but also as a feedback loop to ensure my entity design matches my expectations.
* Remember that repository interfaces are deceptively powerful — they save effort but require careful entity design to behave as expected.



## Milestone 1 – User Entity and Repository Tests – Summary

### Key Achievements

During this milestone, I successfully:

1. **Designed and implemented the `User` entity**

   * Created a fully functional `User` entity with JPA annotations for mapping to the database.
   * Added both a numeric primary key (`id`) and a public `UUID` for external references.
   * Applied validation annotations like `@Email` for the username and `nullable = false` constraints for critical fields (`username`, `password`, `firstname`, `lastname`).
   * Implemented `@PrePersist` to automatically generate UUIDs before saving.

2. **Created repository and persistence layer integration**

   * Leveraged Spring Data JPA to implement `UserRepository`.
   * Ensured repository operations such as `save`, `saveAndFlush`, and `findById` function correctly.
   * Tested persistence behavior using `@DataJpaTest` with an H2 in-memory database, verifying CRUD operations.

3. **Validated entity behavior through comprehensive tests**

   * Wrote positive tests to ensure a valid `User` persists successfully.
   * Tested nullability of fields in a loop, asserting `DataIntegrityViolationException` is thrown when required fields are null.
   * Tested invalid email formats with `ConstraintViolationException`.
   * Verified the uniqueness constraint by writing a duplicate username test.
   * Ensured UUIDs are automatically generated on save.

4. **Prepared for future security and domain enhancements**

   * Marked TODOs for password encryption, `Role` enum implementation, and Spring Security integration (`UserDetails` interface).

---

### Key Learnings & Concepts

Through completing this milestone, I deepened my understanding of several important concepts:

1. **Entity design and identity management**

   * Learned how to use a combination of numeric IDs and UUIDs for internal vs public identifiers.
   * Understood how `@PrePersist` can automate UUID generation for consistency and immutability.

2. **Bean validation vs database constraints**

   * Learned the difference between **application-level validation** (`@Email`, `@NotNull`) and **database-level constraints** (`nullable=false`, `unique=true`).
   * Reinforced that exceptions only occur if either validation annotations or DB constraints are in place.

3. **Spring Data JPA repositories and persistence testing**

   * Learned how to use `saveAndFlush` to immediately synchronize entities with the database to trigger constraints.
   * Gained hands-on experience testing CRUD operations and exception handling in a transactional, rollback-enabled context with `@DataJpaTest`.

4. **Parameterized testing techniques**

   * Explored iterating over multiple fields to test null constraints in a single function.
   * Learned how to write DRY tests by looping through a list of field names while maintaining clear assertion messages.

5. **Handling uniqueness and referential expectations**

   * Learned to test database uniqueness constraints explicitly by attempting to save duplicate usernames and asserting the correct exception is thrown.
   * Reinforced understanding of how primary keys and unique columns interact with persistence.

---

### Challenges & Solutions

1. **Managing dual identifiers (`id` and `uuid`)**

   * **Challenge:** Initially tried to make both `id` and `uuid` primary keys, which caused mapping errors.
   * **Solution:** Kept `id` as the primary key for JPA relationships and used `uuid` as a regular column with `@PrePersist` generation for external references.

2. **Testing nullability and constraints**

   * **Challenge:** Needed a clean way to test multiple required fields for null without duplicating test code.
   * **Solution:** Implemented a loop over a `List<String>` of field names and nullified each field in turn, asserting `DataIntegrityViolationException`.

3. **Email format validation**

   * **Challenge:** Ensuring invalid email formats were caught by validation.
   * **Solution:** Applied `@Email` annotation and tested invalid email input, confirming `ConstraintViolationException` was thrown.

4. **Duplicate username testing**

   * **Challenge:** Ensuring the `unique` constraint on `username` is enforced.
   * **Solution:** Wrote a dedicated test to save a second user with the same username and asserted a `DataIntegrityViolationException` is thrown.

---

### Reflection

* This milestone reinforced my ability to **design and test entities with proper validation and identity management** in Spring Boot.
* I learned that **tests must reflect actual persistence and validation rules**, and that exceptions only occur when rules exist either at the Bean Validation layer or the DB layer.
* Parameterized testing and iteration over fields helped me maintain **DRY and readable test code**.
* I now feel confident handling both **positive and negative persistence scenarios**, including uniqueness, null constraints, and format validation.

**Notes for future reference:**

* Implementing password encryption and roles should happen in a separate milestone to avoid coupling security concerns with basic persistence tests.
* Always generate UUIDs consistently before persistence and mark them immutable to prevent accidental changes.
* Continue using loops or parameterized techniques to test repetitive constraints for new entities (like `Jump`) to maintain concise and maintainable test code.


### Key Achievements

During this task, I successfully:

- **Designed and implemented the `UserInsertDTO` class**
    
    - Created a Data Transfer Object specifically for user registration input in the REST API.
        
    - Applied validation annotations (`@NotEmpty`, `@Email`, `@Pattern`) to enforce input correctness for `username` and `password`.
        
    - Included optional fields (`firstname`, `lastname`) without mandatory constraints, reflecting flexible input requirements.
        
    - Ensured the DTO is decoupled from the entity, preparing the system for proper RESTful architecture and future mapping.
        
- **Created comprehensive DTO validation tests (`UserInsertDTOTest`)**
    
    - Wrote a happy path test to ensure valid input passes all validation rules.
        
    - Covered invalid input scenarios for `username` and `password`, including malformed emails, insufficient password complexity, null values, and empty strings.
        
    - Used Jakarta Bean Validation (`Validator.validate(dto)`) to programmatically test constraints and assert failures.
        
    - Printed violations during test execution to observe which fields fail and the corresponding error messages, aiding debugging and understanding of validation mechanics.
        
- **Established a TDD workflow for DTO validation**
    
    - Defined tests first before any service or controller integration.
        
    - Ensured that all edge cases were anticipated and explicitly tested, including nulls and empty strings, giving me confidence that the DTO enforces input rules reliably.
        

* * *

### Key Learnings & Concepts

Through completing this milestone, I deepened my understanding of several important concepts:

- **Role and purpose of DTOs in a REST API**
    
    - Learned why using DTOs instead of entities is crucial for security, decoupling, and maintaining a clean API contract.
        
    - Understood that DTOs allow precise control over what fields are exposed and validated without directly exposing entity structure.
        
- **Jakarta Bean Validation framework**
    
    - Learned how to use `Validator` to programmatically check constraints on DTOs.
        
    - Understood the behavior of `@NotEmpty`, `@Email`, and `@Pattern` annotations under different edge cases (null, empty, malformed input).
        
    - Discovered that `@Pattern` does not run on `null` values, so `@NotEmpty` must also be used to catch null or empty inputs.
        
- **TDD for DTOs**
    
    - Learned to define both happy path and negative test cases before implementing services or mapping logic.
        
    - Learned to think systematically about edge cases beyond simple invalid inputs, including null and empty values.
        
- **Collections and streams for test assertions**
    
    - Understood that `Validator.validate` returns a `Set<ConstraintViolation<T>>`.
        
    - Learned to use Java Streams to assert that at least one violation corresponds to a specific property, making tests readable and precise.
        

* * *

### Challenges & Solutions

- **Understanding how to test validation without a database**
    
    - Challenge: Initially tried to test DTO behavior like entities, which doesn’t involve persistence.
        
    - Solution: Learned to use Jakarta Bean Validation’s `Validator` to programmatically validate DTOs without relying on database constraints.
        
- **Handling null vs empty strings**
    
    - Challenge: My original invalid tests only included malformed emails and weak passwords; null and empty strings were not tested.
        
    - Solution: Added explicit tests for `null` and `""` for both `username` and `password`, ensuring full edge case coverage.
        
- **Asserting validation violations**
    
    - Challenge: I tried to use lambda shorthand incorrectly with `anyMatch(() -> ...)`, which failed because `anyMatch` expects a `Predicate<T>` that takes a parameter.
        
    - Solution: Corrected to `anyMatch(v -> v.getPropertyPath().toString().equals("username"))`, using the proper stream lambda syntax.
        
- **Avoiding repetitive assertion code**
    
    - Challenge: Each test repeated the same validation and stream assertion logic.
        
    - Solution: Recognized that helper methods or parameterized tests could reduce boilerplate, and I plan to refactor accordingly for maintainability.
        

* * *

### Reflection

This milestone reinforced my understanding of **robust input validation in REST APIs** and the TDD mindset applied to DTOs. I learned that:

- Explicitly testing null and empty strings is critical, even if other invalid inputs exist.
    
- Jakarta Bean Validation provides a clean way to enforce and test rules without touching the database.
    
- Streams and Sets allow precise, expressive validation assertions.
    
- Structuring tests thoughtfully prepares the system for mapping, service logic, and controller integration later, ensuring early detection of input issues.
    

**Notes for future reference:**

- Consider refactoring repeated assertion logic into a helper or parameterized tests for all future DTO validation tests.
    
- Remember that `@Pattern` does not check nulls; always pair with `@NotEmpty` or `@NotNull` if nulls must be disallowed.
    
- Keep DTO validation independent from entity persistence to maintain clean separation of concerns.
    
- Future milestones (mapping to `User` entity, service validation, password encryption) should rely on this robust foundation.
    

&nbsp;

## M2 - Exceptions - ErrorDTOs - ErrorHandler - JacksonConfig

### Key achievements — what I completed

I implemented a coherent, test-driven error-handling surface for my Skydiving Logbook REST API and exercised it with focused unit tests. Concretely, during this milestone I:

- Designed and implemented a small exception hierarchy in `core/exceptions` (including `GenericException`, `InvalidArgumentException`, `ValidationException`, `ResourceNotFoundException`, `ResourceConflictException`, `UnauthorizedException`, `InternalServerException`) and standardized that exceptions carry a human message and an application error code.
- Created `ApiErrorResponseDTO` and `FieldErrorDTO` (error response shape), settled the JSON error structure (timestamp, status, error, code, message, path, fieldErrors) and documented the contract in `ERRORS.md`.
- Implemented `JacksonConfig` to register `JavaTimeModule` and disable `WRITE_DATES_AS_TIMESTAMPS`, ensuring `LocalDateTime` serializes to ISO-8601 strings across the app.
- Built `ErrorHandler` (a `@ControllerAdvice` extending `ResponseEntityExceptionHandler`) with `@ExceptionHandler` methods mapping each custom exception to the correct HTTP status and a standardized `ApiErrorResponseDTO`. I centralized response creation (`createErrorResponse`) and logging (`logException`) as helpers.
- Wrote deterministic tests for DTOs: builder tests, serialization tests and deserialization tests for `ApiErrorResponseDTO` and `FieldErrorDTO`. I verified timestamp formatting, nested `fieldErrors`, and JSON ↔ DTO mapping.
- Moved from relying exclusively on `@SpringBootTest` to writing pure unit tests with Mockito for the `ErrorHandler` class. I wrote a full `ErrorHandlerTest` suite that invokes each handler method directly, stubs `HttpServletRequest` values, asserts `ResponseEntity` status/body, and validated `ValidationException` produces `fieldErrors`.
- Documented an error code convention and saved it to `ERRORS.md` (I chose to use HTTP status numbers as part of the application code strings for now).

* * *

### Key learnings & concepts I absorbed

These are the concrete, technical things I learned and internalized by doing the work:

- **Exception → HTTP mapping (why a unified handler):** a single `@ControllerAdvice` that returns a standardized error DTO produces consistent error shapes, correct HTTP semantics, prevents leaking stack traces, and improves client experience. The handler’s job is translation: map domain/business exceptions to precise HTTP response semantics and machine-friendly error payloads.
- **DTO vs HTTP fields semantics:** `error` should be the HTTP status reason phrase, `message` is the domain/exception message, and `code` is an application-specific error code. Deciding and documenting this split prevents test confusion later.
- **Jackson and Java Time:** Jackson does not support `java.time.*` types by default. Registering `JavaTimeModule` and disabling `WRITE_DATES_AS_TIMESTAMPS` is necessary to produce ISO-8601 strings. For tests, reuse the same configured `ObjectMapper` (inject it in Spring tests) or configure a local mapper in plain unit tests.
- **Deterministic times in tests:** using `LocalDateTime.now()` in tests leads to flaky assertions. Use a fixed `LocalDateTime` for expected values (or capture `now` in a variable before building the DTO) or inject/test a `Clock` when you need better control.
- **JSON testing strategy:** string `contains(...)` checks are brittle. Prefer either (a) deserialize JSON back into `JsonNode`/Map and assert on structure/fields, or (b) assert on DTO fields directly. Use `TypeReference` with Jackson when parsing into generic containers to avoid unchecked-assignment warnings.
- **Unit tests vs Spring tests:** plain unit tests (JUnit + Mockito) are fast and ideal for testing single classes in isolation (like `ErrorHandler`), while `@SpringBootTest` / `@WebMvcTest` + `MockMvc` are integration-style and validate full wiring and serialization to HTTP. I should use unit tests first, then add a couple of integration tests for end-to-end contracts.
- **Mockito basics and gotchas:** `@ExtendWith(MockitoExtension.class)` + `@Mock` + `@InjectMocks` is a clean pattern for pure unit tests. `when(mock.method()).thenReturn(value)` must call the stubbed method inside `when(...)`. All argument matchers must be consistent (if one parameter uses a matcher, all must). `eq()` means “exact match” while `contains()` and `any()` are useful flexible matchers.
- **Logger testing caveat:** Lombok `@Slf4j` generates a private logger; injecting a Mockito mock into that private field is non-trivial. Spying or refactoring to make logging testable is possible but was deemed advanced; I postponed verifying log calls and focused on behavior.

* * *

### Challenges I faced and how I solved them — a lessons-learned log

**1\. Jackson failed to serialize `LocalDateTime`.**

- **Symptom:** `InvalidDefinitionException` complaining `LocalDateTime` not supported.
- **Fix:** Register `JavaTimeModule` and disable `WRITE_DATES_AS_TIMESTAMPS` on the `ObjectMapper`. I centralized this configuration in `JacksonConfig` and used that `ObjectMapper` in Spring tests.

**2\. Flaky timestamp assertions in DTO tests.**

- **Symptom:** comparing `LocalDateTime.now()` in test to runtime-created timestamp caused nanosecond differences.
- **Fix:** Use a fixed `LocalDateTime` (or capture `now` once before building) for deterministic assertions.

**3\. JSON substring assertions were brittle.**

- **Symptom:** `json.contains(...)` mismatches due to whitespace, ordering or formatting.
- **Fix:** Prefer parsing JSON to `JsonNode` or `Map<String,Object>` (with `TypeReference` to avoid unchecked warnings) and assert on values; or assert on DTO objects directly.

**4\. Unchecked assignment warning when parsing JSON to `Map`.**

- **Symptom:** `Map` raw type warning when doing `readValue(json, Map.class)`.
- **Fix:** Use `new TypeReference<Map<String, Object>>() {}` with `readValue` to preserve generic type information and remove warnings.

**5\. Used `getFirst()` on a `List` by mistake.**

- **Symptom:** `getFirst()` doesn’t exist on `List` (it exists on `Deque`/`LinkedList`), test errors.
- **Fix:** Use `get(0)` for `List` indexing.

**6\. Mockito stubbing syntax errors.**

- **Symptom:** attempted `when(request.getMethod().thenReturn(...))` and similar broken calls; IDE said `thenReturn` unresolved.
- **Fix:** Correct pattern is `when(request.getMethod()).thenReturn("GET")`. Also verified Mockito is available through `spring-boot-starter-test`.

**7\. Trying to mock Lombok `@Slf4j` logger directly.**

- **Symptom:** `@Mock Logger` with `@InjectMocks` did not inject into the Lombok-generated `private static final` (or private final) logger. Verify calls would not capture `log.error(...)`.
- **Fix/Decision:** I deferred logger verification and focused on behavior (response body/status). If needed later, I can use a spy, reflection to replace the field, or wrap logging calls in a protected method for easier testing.

**8\. Confusion between `error` vs `message` vs `code`.**

- **Symptom:** I gave an exception a code `"500"` but the handler returned status `400` and `error` `"Bad Request"` — test passed and I was puzzled.
- **Lesson:** Handler sets HTTP status (`BAD_REQUEST`) and `error = status.getReasonPhrase()`; `message` is `exception.getMessage()`, and `code` is `exception.getErrorCode()`. The code string does not control HTTP status; the handler does.

**9\. Creating `ValidationException` with `fieldErrors`:**

- **Symptom:** I initially passed `null` or forgot to wrap a `FieldErrorDTO` in a list.
- **Fix:** Create `FieldErrorDTO` and wrap it with `List.of(...)` or `Collections.singletonList(...)` and pass that to the exception constructor; assert the response `fieldErrors.size()` and content.

**10\. NPE static analysis on `response.getBody().getError()`.**

- **Symptom:** IDE warning `Method invocation may produce 'NullPointerException'`.
- **Fix:** Add `assertNotNull(response.getBody())` before dereferencing. This documents the assumption and silences the warning.

* * *

### Reflection — notes for future me / design reminders

- Keep the separation of concerns: mappers should be pure transformers; validation should happen at DTO/controller input boundary; entity resolution (ID → entity lookup) belongs to the service layer. That made MapStruct mapping simpler and testing easier.
- Centralize cross-cutting behavior (timestamps, error shape) early — documenting the JSON structure in `ERRORS.md` paid off by removing ambiguity in tests and client expectations.
- For JSON contract tests, prefer *structure-driven checks* (parse into a tree/map) rather than brittle string comparisons. This scales much better as DTOs evolve.
- Use unit tests (Mockito) to assert internal behavior quickly and integration tests (`@WebMvcTest` / `MockMvc`) to validate end-to-end HTTP serialization and real Spring wiring. Start with unit tests for core logic; add a few integration tests for contract assurance.
- When working with logging: if I actually need to assert log messages later (coverage or forensic reasons), plan a logger-testing strategy early — either spy on the class, wrap logging in a testable protected method, or refactor to inject a testable logging adapter.
- Maintain a single source of truth for `ObjectMapper` configuration. For unit tests that do not load Spring, create a small helper to produce the same configured mapper so tests represent production behavior.

* * *

### Concrete next steps checklist (practical & prioritized)

1.  **Finish non-logger unit tests** for `ErrorHandler` (done for main cases, but:
    
    - add content assertions for `FieldErrorDTO` inside the `ValidationException` test).
2.  **Add `@WebMvcTest` MockMvc test(s)** for a small `TestController` that throws each exception and assert the full JSON payloads (end-to-end verification).
    
3.  **Optionally address logger coverage** if JaCoCo indicates the helpers are uncovered:
    
    - either add a spy-based test for `logException`, or wrap logging in a small testable method.
4.  **If mapping layer remains in flight** (MapStruct/other mappers), add `@MapperConfig` with consistent policies (`unmappedTargetPolicy`, `componentModel`) and run full build to expose missing mappings early.
    
5.  **Document & reuse test utilities**: a small factory to create common `ApiErrorResponseDTO`/`FieldErrorDTO` test objects and a shared `ObjectMapper` helper for plain unit tests.
    

* * *

### Final note (meta)

This milestone was highly practical: I converted design choices into runnable, test-driven code and learned multiple real-world, repeatable patterns for REST error handling and robust testing. I now have:

- a documented error contract (`ERRORS.md`),
- a centralized `JacksonConfig`,
- a `ControllerAdvice` mapping exceptions → consistent, useful error DTOs,
- and a suite of deterministic unit tests using Mockito to verify the mapping logic.

These foundations will make it straightforward to continue with services and controllers, and to add integration tests and client apps (Angular/React/Android) that rely on a stable error contract.

# M2 – JumpService (IJumpService & JumpServiceImpl) — Summary

### Overview — subjects we covered

* Service API design (IJumpService signatures, transactional boundaries)
* MapStruct mapping (insert → entity, entity → lookup DTO, update with `@MappingTarget`)
* DTOs (JumpInsertDTO, JumpUpdateDTO, JumpLookupDTO) and validation rules
* Repository work: Spring Data derived queries, custom `@Query` JPQL, `countBy...`, `sum(...)`
* JpaSpecificationExecutor and Criteria API (Specification, Predicate, Root, CriteriaBuilder)
* Pagination (`Pageable`, `Page`) and tie-breaker ordering
* Ordinal (jump number) computation strategies (dynamic / hybrid) and performance considerations
* Exception design and propagation (GenericException, ResourceNotFoundException, InternalServerException, DataIntegrityViolationException)
* Test strategy: Spring integration tests (`@SpringBootTest`, `@Transactional`, H2), seed helpers, deterministic dates
* Mapping `jumpNumber` into DTOs and MapStruct update patterns
* JPA lifecycle pitfalls (unsaved/transient instances, optimistic locking errors)
* Seed data shaping and test isolation (avoiding hard-coded IDs)
* Formatting aggregate results (total freefall seconds → `hours:minutes:seconds`)
* Authorization strategy planning (`@PreAuthorize` and where to apply it)

---

## Key achievements — what I completed and decisions I made

* I implemented `IJumpService` and `JumpServiceImpl` with the core CRUD operations and search:

  * `createJump`, `updateJump`, `deleteJump`, `getJump`, paginated `getAllJumps`, `searchJumps(...)`, and aggregate helpers (`getTotalFreefallTime`, `getTotalNumberOfJumps`).
  * I chose to apply `@Transactional` at the service method level for create/update/delete operations.

* I integrated MapStruct mapping patterns and enforced the service responsibility to set associations:

  * `jumpInsertDTO → Jump` mapping ignores associations; the service looks up `User`, `Aircraft`, `Dropzone`, and `Jumptype` and sets them on the mapped entity before saving.
  * I added/confirmed the `jumpToJumpLookupDTO` mapper to convert persisted entities into `JumpLookupDTO`.

* I added `JumpUpdateDTO` and designed the MapStruct update pattern:

  * I verified the approach of mapping `JumpUpdateDTO` into an existing `Jump` entity using MapStruct’s `@MappingTarget` (service still sets associations after mapping).
  * I learned the correct MapStruct update pattern (mapper updates the entity in-place).

* I implemented and used JPA repository methods needed by business logic:

  * `countByUserIdAndIdLessThanEqual(...)` for computing an individual jump’s ordinal.
  * `@Query`-based `sumTotalFreeFallDurationByUser(...)` for total freefall seconds.
  * I used `JpaSpecificationExecutor<Jump>` and a `JumpSpecifications.filterJumps(...)` helper to implement flexible search filters (user, dateFrom, dateTo, jumptype).

* I built a robust Spring-test-oriented TDD approach:

  * Wrote integration-style Spring tests (`@SpringBootTest`, `@ActiveProfiles("test")`, `@Transactional`) that seed the H2 test DB, call service methods, and assert expected behavior.
  * Created deterministic seed data (fixed base dates, not `now()`), dynamic assertions based on persisted returned entities, and avoided hardcoded IDs.

* I made error-handling decisions consistent with the rest of the project:

  * Service throws `ResourceNotFoundException` when referenced related entities don’t exist.
  * I catch `DataIntegrityViolationException` around save and translate to `InternalServerException` (consistent with other services/exceptions).

---

## Key learnings & concepts — what I learned while doing this

### Spring Data & repository patterns

* **Derived queries** (`findBy...`, `countBy...`) come from **Spring Data JPA** and are declarative — you can express many queries by naming conventions. For edge cases I used `@Query` JPQL.
* Methods like `findByJumpDateBetween(...)` and `greaterThanOrEqualTo` / `lessThanOrEqualTo` correspond to inclusive range semantics (use `<=`/`>=` when you want inclusive comparisons).
* `@Query("SELECT SUM(...) ...")` returns `Long` (nullable) — use `Long` not `long` because the sum may be `null` when no rows are present.

### Specification API & CriteriaBuilder

* `JpaSpecificationExecutor` + `Specification<T>` let me build dynamic queries without hardcoding a lot of repository methods.
* **Predicate, Root, CriteriaBuilder**:

  * `Root<Jump>` is the root entity path in the query (equivalent to `FROM jump`).
  * `CriteriaBuilder` is a factory for predicates and expressions (e.g., `greaterThanOrEqualTo`, `equal`).
  * `Predicate` objects are combined (via `cb.and(...)` / `cb.or(...)`) to form the WHERE clause. The Specification returns one predicate representing the composed filter.
* Using Specification makes handling optional filters (null `jumpDateFrom`, null `jumptype`) straightforward: only add predicates when the filter param is not null.

### Mapping & DTO design

* Keep DTOs lean and validated with Bean Validation (`@NotNull`, `@Min`, `@Max`, `@PastOrPresent`, `@Size`) and let the service handle relationship existence (DB lookups).
* MapStruct best practice:

  * Map insert/update payloads to entities while ignoring associations; service resolves related entities and sets them.
  * Use `@MappingTarget` to map update DTO into an existing entity (MapStruct can update the target in place — the method typically returns `void` or the modified entity, but the principal point is mapping into the provided `@MappingTarget`).
* For `JumpLookupDTO` I added a `jumpNumber` field and decided the service will populate it after mapping (service computes ordinal and sets it on the DTO). Alternative would be a repository projection returning `jump_number` directly, but I kept the logic in service for now.

### Transactional & exception handling behaviors

* I used `@Transactional` on service methods to keep write operations atomic and to rely on Spring’s exception translation for database exceptions.
* I favored runtime (unchecked) custom exceptions (extending a GenericException with `HttpStatus` stored) for cleaner propagation; controller advice maps them to structured `ApiErrorResponseDTO`s.
* I learned that catching `DataIntegrityViolationException` and wrapping it into `InternalServerException` gives consistent API error semantics.

### Testing patterns and pitfalls

* Always **seed deterministic data** for tests (fixed `LocalDateTime` base), avoid `now()` for reproducibility.
* Use persisted returned instances from `save` / `saveAll` — don’t assume IDs or call `new Entity(1L,...)`: hard-coding IDs leads to brittle tests, optimistic-locking errors, and flakiness when tests run as a suite.
* Seed helpers must set entity properties before calling `save(...)`; saving before setting required unique fields causes `DataIntegrityViolationException` (e.g., saving a `Jumptype` with a null name into a unique column).
* Use dynamic assertions: compute expected counts by filtering the in-memory seeded objects (after persistence) rather than hardcoding expected numbers; that prevents failures when insertion order or data content changes.
* When returning structured maps from seed helpers, use typed containers (or a small `SeedData` holder) instead of raw `Map<String, Object>` to avoid unchecked-cast warnings.

### Miscellaneous practical learnings

* `Duration.ofSeconds(totalSeconds)` is the correct base for converting seconds → hours/minutes/seconds; compute `hours = d.toHours()`, `minutes = d.toMinutes() % 60`, `seconds = d.getSeconds() % 60`.
* Using `Pageable` as a service parameter: accept a `Pageable` from caller (controller or test); service can also construct defaults if needed — but tests should pass explicit `PageRequest` objects for determinism.
* Authorization decision (owner check): `@PreAuthorize` on service methods is the cleanest place to enforce owner rules and avoid scattering owner checks throughout code; it throws Spring security exceptions (can be mapped to custom exceptions by an `ExceptionHandler` if desired).

---

## Challenges & solutions — problems I hit and how I fixed them

### 1. Tests passed individually but failed as a suite (0 vs expected counts)

**Problem:** Tests that passed in isolation failed when run with the full `gradlew test` suite — expected counts were zero or mismatched.
**Root causes:**

* Hard-coded assumptions about IDs (e.g., `new Jumptype(1L, "Belly")`) which aren’t guaranteed.
* Seed helper saved entities in the wrong order or mutated after save, creating inconsistent persisted state.
* Reused application context / DB state between tests caused unintended interactions.

**Solution I implemented:**

* Rewrote seed helper to persist fully-initialized entities and to return the persisted instances (use the returned entities from `save` / `saveAll`).
* Replaced hard-coded IDs with the persisted entity IDs from the seed helper (`belly.getId()` etc).
* Made tests compute expected results dynamically by filtering the seeded returned jump lists so tests no longer rely on magic numbers.

**Lesson:** Always treat test data as ephemeral and self-contained — don’t assume ID values or DB state across tests.

---

### 2. `ObjectOptimisticLockingFailureException` on save in tests

**Problem:** Tests threw optimistic-locking / transient-value errors.
**Root cause:** Helper functions created entities with non-null IDs (e.g., `new User(1L, ...)`) so when saving, JPA treated them as detached/managed incorrectly and caused optimistic lock / unsaved-value problems.

**Solution:** Ensure helper-created entities have `null` id before saving; always let the persistence provider generate IDs. After saving, use the returned managed instance for further operations and assertions.

**Lesson:** Never instantiate test entities with pre-set primary keys unless intentionally working with managed/detached semantics — prefer `null` id and call `save()`.

---

### 3. `DataIntegrityViolationException` when creating Jumptype in seed

**Problem:** Unique constraint violation on `jumptype_name NULLS FIRST` — insert failed because a `Jumptype` with a null name was saved.
**Root cause:** I called `save()` before setting the `jumptypeName`. The DB unique constraint rejected the `NULL` value.

**Solution:** Set required fields before calling `save()`; rebuild the seed helper so entities are fully initialized before persisting.

**Lesson:** Set entity invariants first; tests must create valid entities before `save()`.

---

### 4. Mapping update pattern confusion (MapStruct)

**Problem:** I was uncertain whether MapStruct update methods should return the entity or be `void`. I also initially tried a mapper signature that returned a DTO from an update mapping which didn't make sense.
**Resolution / learning:** Use MapStruct’s `@MappingTarget` to populate an existing entity in-place. The mapper method can be `void` (MapStruct will update the provided target) or return the updated entity, but the important part is mapping into the existing JPA-managed entity and then setting associations in the service. The service must still fetch and set related entities (user/aircraft/..), not rely on MapStruct for relationship resolution.

**Lesson:** Use MapStruct for field-level mapping; keep association resolution in the service.

---

### 5. Recursion bug when calculating totals

**Problem:** I accidentally wrote a method that called itself (recursive) while computing total freefall time.
**Fix:** Call repository aggregation (`sumTotalFreeFallDurationByUser`) rather than re-entering the service method. Use `Duration` utilities to format seconds into `h:m:s`.

**Lesson:** Keep service aggregation methods simple and delegate heavy-lifting to repository queries.

---

### 6. Specification and tie-breaker ordering / pagination

**Problem:** I needed deterministic ordering for paginated tests, especially for same-day multiple jumps. Without explicit sort, page results can be non-deterministic.
**Solution:** Use explicit Sort (e.g., `jumpDate` ASC then `id` ASC) in `Pageable` used in tests and service calls. Add an index `(user_id, jump_date, id)` to the DB model to support performance and stable ordering. I added the index annotation in the entity definition.

**Lesson:** When testing pagination, always pass `PageRequest.of(page, size, Sort.by(...))` to make ordering deterministic.

---

### 7. Unchecked cast warnings in test seed map

**Problem:** I stored a heterogeneous `Map<String, Object>` inside `Map<Long, Map<String, Object>>` and then cast `Object` to `List<Jump>` — compiler warns about unchecked casts.
**Solution:** I learned to prefer a typed holder (a simple `SeedData` class or `Map<Long, Map<String, ?>>` with generics) to retain type-safety. I postponed refactoring in the interest of finishing service functionality, but retained the knowledge to refactor later.

**Lesson:** Strong typing in test helpers saves headaches and compiler warnings.

---

## Reflection — notes for future work / how this changed my approach

* **Service is the right place for business rules + existence checks.** DTO-level validation ensures shape/format, but the service must check relational integrity (that `userId`, `aircraftId` etc exist) and enforce domain rules (e.g., owner matches authenticated user — implemented later with `@PreAuthorize`).
* **Dynamic test expectations are more robust than hard-coded assertions.** Using the seeded returned entities to compute expected counts makes tests resilient to data changes and ordering differences.
* **MapStruct + service separation of concerns works well.** MapStruct is great for field-level mapping; I must not let it hide the need to explicitly resolve associations and transactional context in the service.
* **Prefer returning persisted instances from seed helpers.** Use those returned instances for test input and assertions to avoid brittle tests.
* **Exception model consistent across layers helps API clarity.** Storing `HttpStatus` in `GenericException` and mapping to `ApiErrorResponseDTO` through controller advice results in consistent, testable API error behavior.
* **Performance considerations aren't optional.** I selected the dynamic ordinal strategy for correctness and started with per-jump counts (the hybrid approach); I’ll implement the N+1 avoiding optimizations later when performance measurement indicates a problem (e.g., windowed query or a projection).
* **Keep security orthogonal.** Owner checks belong to the security layer; `@PreAuthorize` at the service layer will be my chosen integration point when I add authorization.

---

## What I’ll do next (practical TODOs)

* Refactor test seed helpers into a typed `SeedData` holder to eliminate unchecked casts and make tests cleaner.
* Implement the hybrid optimization for jump ordinals (batched/windowed projection) when working on list endpoints to avoid N+1.
* Add `@PreAuthorize` checks on service methods and update tests to account for authenticated user context. Map `AccessDeniedException` to my `UnauthorizedException` (or translate appropriately).
* Replace any remaining hard-coded assumptions with dynamic references to persisted entities.
* After service is stable, add controller-level integration tests (web layer) to verify HTTP semantics and error payloads.

---

### Closing note (first-person)

I completed the Jump service milestone and its tests with a lot of practical learning: handling JPA lifecycle correctly in tests, writing stable Specification-based search, implementing the ordinal computation strategy, and building robust, deterministic Spring integration tests. I learned to avoid brittle assumptions (hard-coded IDs, mutable saved entities) and to prefer dynamic assertions based on persisted seed data. The service is now functionally complete for the CRUD/search/aggregate behaviors I planned; the main future work is performance optimization for large result sets and hooking in the authorization layer.

This milestone tightened my understanding of the interplay between DTO validation, MapStruct mapping, repository queries (both derived and custom JPQL), Specifications, and Spring Boot integration testing — a lot of small, easily-missed details that make services robust in practice.


## M2 – StaticData + UserService (Exceptions / Service layer) — Learning Summary

### Key achievements

* Implemented **Static data layer**

  * `IStaticDataService` + `StaticDataServiceImpl`.
  * Unit/integration tests validating `findAllAircraft()`, `findAllDropzones()`, `findAllJumptypes()` (mocking repositories and returning lists).
* Implemented **User service layer**

  * `IUserService` interface (create, update, deactivate, get, list, changePassword).
  * `UserServiceImpl` with the full **DTO → Entity → resolve refs → set relations → save → DTO** flow for `createUser`, `updateUser`, `deactivateUser`, `getUser`, `getAllUsers(page,size)` and `changePassword`.
  * Password encoding wired via `PasswordEncoder` bean (BCrypt).
  * Use of `@Transactional` boundaries for read/write methods and `readOnly = true` for queries where appropriate.
* Mappers & DTOs

  * Continued MapStruct use (entity ↔ lookup DTOs).
  * Added `UserUpdateDTO` and `PasswordUpdateDTO`, wrote validation tests.
* Tests

  * Wrote a suite of **Spring test** integration tests (H2/test profile) covering many service behaviors (create, update, deactivate, list pagination, change password).
  * Also experimented extensively with **pure unit tests** (Mockito + `@ExtendWith(MockitoExtension.class)`) and learned the tradeoffs.
* Error & exception handling

  * Refactored exceptions and `ErrorHandler` to a consistent approach; verified behavior through tests.
* Important model changes

  * Added `active` boolean to `User` for soft-delete behavior and ensured defaults via `@PrePersist` to avoid DB `NOT NULL` failures.

---

### Key learnings & concepts (what I learned)

1. **Service layer responsibilities**

   * Service = business logic + transaction boundary. Controllers translate HTTP ↔ DTOs; repositories are purely data access. Services map DTO → entity, resolve relation references, enforce domain rules (uniqueness, role defaults), persist, and map back to DTOs for responses.
2. **TDD/test layering tradeoffs**

   * **Unit tests (Mockito)** are fast and isolate the service, but require stubbing every dependency and return value (mappers, repository responses). You must stub mapper outputs and repository behaviors, or you’ll get NPEs or meaningless tests.
   * **Integration tests (`@SpringBootTest` + H2)** exercise Spring Data, JPA mappings, constraints and are more realistic for behavior that depends on DB semantics (e.g., unique constraints, Hibernate defaults). They’re slower but catch real DB problems.
   * Best practice: a mix — unit test pure business flow, integration tests for DB/mapper/transaction behavior.
3. **Mockito gotchas**

   * Mockito matchers (`any()`, `anyString()`) only work on mocks — not on real Spring beans created by the context. In `@SpringBootTest` you either must replace beans with mocks (historically `@MockBean`) or do pure Mockito unit tests with `@ExtendWith(MockitoExtension.class)` and `@InjectMocks`.
   * `@MockBean` deprecation in SB 3.4 made me notice that pure unit tests with `@Mock`/`@InjectMocks` are the modern, quicker way to isolate service logic.
4. **MapStruct behavior**

   * MapStruct will warn about unmapped target properties (createdAt, updatedAt, id, uuid, active, role) when mapping DTO→entity if those fields are intentionally handled elsewhere (prePersist, DB). This warning is expected if I purposely leave automatic fields out of mapper mapping.
   * Mapping collections: MapStruct can produce mapping methods for `List` and also for `Page` if declared in the mapper. Generated mapper classes are `@Generated` and should not be edited directly.
5. **Transactions & tests**

   * `@Transactional` on tests or on methods affects persistence/flush/visibility. Tests that use `@Transactional` might roll back, so make sure the test context and repository usage align with what you expect (flush, find, assert).
6. **Entity lifecycle defaults**

   * Use `@PrePersist` (single method) to set defaults (UUID, `active=true`) — avoids `NULL not allowed` DB errors and keeps defaulting centralized. Combining UUID generation and default `active` in the same `@PrePersist` is the clean, reliable approach.
7. **Password handling**

   * Never compare raw strings to encoded passwords. Use `passwordEncoder.matches(raw, encoded)` to verify old password. To check "new password is different", compare new raw password with encoded by `passwordEncoder.matches(newRaw, storedEncoded)`.
8. **DTO design**

   * Use `InsertDTO` for creation (includes password), `UpdateDTO` for non-sensitive updates (no password) and a separate `PasswordUpdateDTO` for password change flow. Lookup DTOs exclude sensitive fields (e.g., password).
9. **Pagination**

   * Use `Pageable`/`Page` for paginated repository calls. `PageRequest.of(page, size)` is zero-indexed. Example: 25 elements, `page 0 size 10` → pages: 10,10,5 (`totalPages=3`, `totalElements=25`).

---

### Challenges, bugs, and how I solved them (lessons learned)

#### 1) StaticDataService unit tests initially failing

* **Problem:** I tried to mock entity instances as `@Mock` and stubbed their getters, and then attempted to `when(aircraftRepository.findAll()).thenReturn((List<Aircraft>) aircraft);` — nonsense: returning a mock instance cast to list.
* **Fix:** Create real instances (`new Aircraft(1L, "plane1")`) and stub `when(aircraftRepository.findAll()).thenReturn(List.of(aircraft1, aircraft2, aircraft3));`. Assert service returns lists via `staticDataService.findAllAircraft()` (not repository direct calls).
* **Lesson:** When testing simple repository returns, return real objects in lists; mocks are for behavior, not replacement for simple data.

#### 2) Validator in DTO unit tests — `validator` was null

* **Problem:** Trying to use `Validator` without initializing it or making it static in the wrong context (`@BeforeAll` static vs instance).
* **Fix:** Initialize `Validator` in `@BeforeEach` (instance method) by creating `Validation.buildDefaultValidatorFactory().getValidator()`.
* **Lesson:** Bean Validation can be used in pure JUnit tests by creating a `ValidatorFactory`/`Validator` manually.

#### 3) MapStruct unmapped properties warning

* **Problem:** Warnings about unmapped target properties when mapping DTO→entity.
* **Decision:** Accept the warning when fields are intentionally handled by the entity lifecycle, but be mindful if missing mapping means a bug (e.g., forgetting to set an important business field).
* **Lesson:** Explicit is better — either add mapping or confirm the missing fields are intentionally managed elsewhere.

#### 4) Unit tests with Mockito: NPEs because mapper returned `null`

* **Problem:** In pure unit tests, `userMapper` is a mock and returns `null` unless stubbed; service then tries to call `user.setRole(...)` and NPEs.
* **Fix:** Stub `when(userMapper.userInsertDTOtoUser(any())).thenReturn(mockUser)` with a real `User` instance. Also stub `userRepository.save(...)` behavior as needed.
* **Lesson:** With `@InjectMocks` you must stub every collaborator method that the service invokes — otherwise you’re not testing the service behavior meaningfully.

#### 5) Mockito matchers & Spring context: `InvalidUseOfMatchersException`

* **Problem:** Using Mockito `any()` on real Spring beans in `@SpringBootTest` (not mocks) caused the matcher error.
* **Fix/Decision:**

  * Either switch to **pure unit tests** with `@ExtendWith(MockitoExtension.class)` and `@InjectMocks`, or
  * Replace the Spring bean with a mock inside the context (previously `@MockBean`, but note deprecation and prefer unit tests or explicit test slice wiring).
* **Lesson:** Understand whether the test is a Spring integration test (real beans) or a unit test (mocks). Don’t mix mocking idioms across those boundaries.

#### 6) DataIntegrity / “User already exists” debugging saga

* **Symptoms:** Integration test `createUser` threw `ResourceConflictException` from the `catch` block, even though pre-check `findByUsernameAndActiveIsTrue(...)` returned empty and `userRepository.count()` was 0.
* **Deep-dive steps & findings:**

  * I added debug prints — found DB count 0 and `findByUsername...` returned `Optional.empty()`.
  * Insert attempt failed with SQL error `NULL not allowed for column "active"`, causing a `DataIntegrityViolationException` from `userRepository.save(...)`. The `catch` was wrapping this into a conflict message — misleading but correct as negotiated logic.
  * Root cause: I had not set `active` default on the entity at persist time. The DB `active` column is `NOT NULL`, so the insert fails with `active = NULL`.
* **Fix:** Implemented a combined `@PrePersist` that sets both `uuid` **and** `active = true` in one method, ensuring defaults at persist time and avoiding the `NULL` DB error.
* **Lesson:** Always ensure entity lifecycle defaults for `NOT NULL` DB columns. Don’t rely on service layer to set every default; entities can enforce sane defaults with `@PrePersist`.

#### 7) Transactional/test isolation issues

* **Problem:** Spring tests sometimes “leaked” state or test DB had pre-existing rows causing conflicts.
* **Fixes / decisions:**

  * Use `spring.jpa.hibernate.ddl-auto=create-drop` in test profile (already set).
  * Clean DB with `userRepository.deleteAll()` in `@BeforeEach` for tests that require it.
  * Prefer annotating test methods/classes with `@Transactional` so state rolls back and tests are isolated as needed.
* **Lesson:** Transactional behavior + context caching/flushing can confuse test expectations; explicitly clear or flush where needed, and align test strategy (unit vs integration).

#### 8) Password change logic gotchas

* **Initial issue:** I checked equality by comparing raw strings to stored encoded password -> failed.
* **Fix:** Store encoded password in DB before testing (e.g., `user.setPassword(passwordEncoder.encode("a@123456")); userRepository.save(user);`). Then in service use `passwordEncoder.matches(dto.getOldPassword(), user.getPassword())` and ensure `passwordEncoder.matches(dto.getNewPassword(), user.getPassword())` is used to detect “same password” cases.
* **Lesson:** Never compare raw ↔ encoded directly; always use `matches()`.

#### 9) Pagination & listing

* **Learning:** `PageRequest.of(page, size)` is zero-indexed; with 25 items and page = 0, size = 10 → pages: 10,10,5; `totalPages = 3`.
* **Test approach:** persist multiple users in test DB, call `userService.getAllUsers(page,size)` and assert `page.getContent().size()`, `page.getTotalElements()`, `page.getTotalPages()`.

---

### Reflection — what I’ll carry forward

* **Testing strategy:** I now prefer a pragmatic mix. For repository/DB-sensitive behavior (constraints, entity lifecycle, MapStruct integration) I use **integration tests with H2**. For pure business logic paths that should be fast and isolated, I write **pure unit tests** with Mockito and `@InjectMocks`. Trying to force every scenario to be a fast Mockito test made many tests brittle and expensive to author; integration tests saved hours by exposing real DB semantics.
* **Service design validation:** Implementing the `DTO → mapper → resolve refs → set relations → save → mapper → DTO` pattern repeatedly reinforced why service layers are the place to coordinate mapping, reference resolution, and transaction boundaries. The pattern works and aligns well with TDD when I write tests first.
* **Entity lifecycle & defaults are crucial:** missing defaults cost me hours (the `active` null bug). I’ll prefer centralizing such defaults in entity `@PrePersist` hooks to avoid DB errors.
* **Testing discipline:** small, focused tests + clear setup helpers (e.g., `createValidUser()` that encodes passwords / sets role) saved repetition and made debugging easier.
* **Error handling & user experience:** Make error messages accurate. Catching a `DataIntegrityViolationException` and returning a generic conflict message can mask the original problem (e.g., `active` null) — but it still prevents leaking DB internals; logs should keep the root cause to aid debugging.
* **Document the journey:** I’ll keep this session’s steps (static data tests, DTO tests, MapStruct mapping notes, unit vs integration choices, the username-exists debugging trail) as part of the project’s learning log so I don’t re-trace the same debugging path later.

---

### Short list of concrete “do / don’t” reminders for future

* Do: keep DTO validation fast and separate from DB operations; test DTOs with `Validator`.
* Do: set DB-required defaults in entity `@PrePersist`.
* Do: use `passwordEncoder.matches()` for password checks.
* Do: use real integration tests for DB constraint behavior.
* Don’t: mix Mockito matchers with real beans in `@SpringBootTest`.
* Don’t: assume MapStruct warnings are always errors — inspect and confirm intention.
* Use a mix of unit + integration tests: unit for business logic, integration for persistence behavior.

---


## M3 – AuthController, AuthenticationService & Tests – Summary

### Key Achievements

* **Implemented the `AuthController` REST endpoint**

  * Added `AuthController` under the `rest` package with a focused responsibility: accept login requests at `/api/auth/login`, delegate authentication to the service layer, and return `200 OK` with an `AuthenticationResponseDTO` containing the generated JWT and user info on success.
  * Kept the controller thin—delegation only—so business logic and error mapping live in the service/error handler.

* **Finalized `AuthenticationServiceImpl` behavior and exception mapping**

  * Used `AuthenticationManager` to authenticate `UsernamePasswordAuthenticationToken`.
  * Injected and used `JwtService` to generate tokens upon success.
  * Wrapped the `authenticate(...)` call in a `try/catch` and rethrew a domain-specific `UnauthorizedException` (instead of letting Spring Security’s `BadCredentialsException` bubble up). This made controller behavior predictable and tests able to assert my custom exception type.

* **Wrote comprehensive `AuthControllerTest` cases**

  * Created tests that exercise the controller → service → repository pipeline (using the Spring test context and the real `UserRepository`).
  * Covered happy path (valid login) and negative scenarios:

    * invalid username
    * invalid password
    * missing username (null)
    * missing password (null)
  * Ensured test data uses `passwordEncoder.encode(...)` before saving users and used `saveAndFlush(...)` to persist entities reliably for the test.

* **Stabilized supporting test infra and JWT testing**

  * Continued with `JwtServiceImpl` unit tests using injected `Clock` for deterministic timestamps and `ReflectionTestUtils` to set secret key and expiration.
  * Identified and solved several test flakiness sources (bean conflicts, persistence visibility, and lingering threads).

---

### Key Learnings & Concepts

* **Controller responsibilities (thin controllers)**
  Controllers should just map requests and responses and delegate business logic to services. Keeping `AuthController` minimal made testing and reasoning simpler.

* **Spring Security authentication flow**
  `AuthenticationManager.authenticate(...)` delegates to `AuthenticationProvider` and throws `BadCredentialsException` for missing/wrong credentials. To present API-friendly errors, I must catch Spring Security exceptions and map them to domain exceptions or status codes.

* **Separation: registration vs authentication**
  Registration must explicitly check for existing users (return `409 Conflict`), while authentication returns `401 Unauthorized` for invalid credentials. Mixing those flows causes confusion and brittle tests.

* **Request mapping and validation**
  `@RequestBody` maps JSON to DTOs; using `@Valid` + Bean Validation on DTOs produces automatic `400 Bad Request` on invalid input, keeping controllers cleaner.

* **Deterministic JWT testing with `Clock`**
  Injecting `Clock` into `JwtService` made JWT tests deterministic. Important gotcha: generating and validating a token with the same fixed `Clock` will never show expiration — to test expiry I must generate with one instant and validate with a later instant (or swap the service clock).

* **Test layering & strategy**
  For early progress I called controllers directly in `@SpringBootTest` (no real HTTP) to avoid coupling with security filter setup; later I’ll add `SecurityFilterChain` and `TestRestTemplate` integration tests. Use `@WebMvcTest` for focused controller layer tests when speed matters.

---

### The Exact Lesson Learned (BadCredentialsException → UnauthorizedException)

Spring Security throws `BadCredentialsException` when authentication fails (missing or wrong credentials). Relying on that exception to bubble up makes my controller/tests depend on Spring Security internals and prevents returning consistent API error shapes. I learned to **catch `BadCredentialsException` (and related Spring Security exceptions) inside my `AuthenticationService`**, then rethrow a domain-level `UnauthorizedException`. This keeps controllers thin, centralizes authentication error mapping, and makes tests assertable against my own exception types and messages.

---

### Challenges & Solutions (Lessons Learned / Bugs & Fixes)

* **Context failed to start (no test output)**

  * **Symptom:** Tests didn’t reach `System.out.println` and appeared not to run.
  * **Cause:** `ConflictingBeanDefinitionException` — I had two `SecurityConfig` classes with the same bean name.
  * **Fix:** Removed the stray empty `SecurityConfig` and left the proper `config.SecurityConfig`. After that, tests started running.

* **401 Unauthorized with `TestRestTemplate`**

  * **Symptom:** Full HTTP calls returned 401 before I implemented filters.
  * **Cause:** No `SecurityFilterChain` defined, so Spring Security default required auth for everything.
  * **Decision:** Focus first on controller → service tests (direct calls). Implement `SecurityFilterChain` and `JwtAuthenticationFilter` next, then test end-to-end with `TestRestTemplate`.

* **Authentication failing due to unencoded password / not persisted user**

  * **Symptom:** AuthenticationManager failed to find or match the user.
  * **Cause:** I saved users with raw passwords or didn’t flush persistence.
  * **Fix:** Use `passwordEncoder.encode(raw)` before saving and call `saveAndFlush(...)` to ensure DB visibility in tests.

* **Spring Security exceptions in tests (`BadCredentialsException`)**

  * **Symptom:** Tests expecting my `UnauthorizedException` were getting Spring exceptions.
  * **Cause:** I let `AuthenticationManager` exceptions bubble up.
  * **Fix:** Catch `BadCredentialsException` within `AuthenticationServiceImpl` and rethrow `UnauthorizedException`. This centralizes error handling and makes test assertions straightforward.

* **Tests kept running after completion**

  * **Symptom:** JUnit / IntelliJ process stayed alive after tests passed.
  * **Cause:** Lingering non-daemon threads (Hikari pool, async executors) or resources not closed.
  * **Fixes & mitigations:**

    * Close Hikari DataSource in an `@AfterAll` cleanup if required.
    * Clear `SecurityContextHolder` in `@AfterEach`.
    * Prefer `webEnvironment = MOCK` or direct controller calls when server not needed.
    * Use `@DirtiesContext` sparingly to force context cleanup when necessary.

* **JWT expiration tests failing when switching to fixed `Clock`**

  * **Symptom:** Tokens never expired when tests used the same fixed clock for generation and validation.
  * **Cause:** Fixed `Clock` freezes “now,” so token `exp` is always in the future relative to that same instant.
  * **Fix:** Generate token with a `Clock` fixed at issuance time; validate with the same service instance after injecting a later fixed `Clock` (or change the service’s clock via reflection). Also confirmed `validateToken()` must use the injected `Clock`, not `Instant.now()` directly.

* **Wrong test scenario (invalid password test used wrong username too)**

  * **Fix:** Correct tests to ensure each negative test changes only the intended parameter (e.g., wrong password but correct username), and consolidate invalid scenarios with parameterized tests.

---

### Reflection

This milestone taught me several practical truths about building secure REST APIs with good test coverage:

* **Design for testability** — accepting a `Clock` in `JwtService`, making secret keys configurable in tests, and centralizing exception mapping in the service layer made tests deterministic and easier to write.

* **Fix the infra first** — security config, unique bean names, and password encoder must be correct before integration tests with real HTTP make sense. Start by getting controller → service → repo flow stable, then add filters and HTTP-level tests.

* **Make error mapping explicit** — catching Spring Security exceptions in the service and translating them to `UnauthorizedException` gives consistent API responses and prevents leaking framework exceptions to clients.

* **Deterministic tests avoid flakiness** — controlling time and secrets is worth the upfront effort. Tests that depend on system time or environment are fragile.

* **Clean up resources** — explicitly closing connection pools and clearing security context prevents the "tests keep running" annoyance and avoids test interference across classes.

---

### Action Items / Next Steps

1. Implement `SecurityFilterChain` and `JwtAuthenticationFilter` (stateless session management; permit `/api/auth/**`, protect `/api/**`).
2. Add end-to-end integration tests with `TestRestTemplate` once the security filter chain is in place and stable.
3. Create `UserController` registration flow: validate input (`400`), check duplicates (`409`), persist new users (`201`).
4. Replace repetitive negative login tests with `@ParameterizedTest` for maintainability.
5. Add test cleanup hooks (close Hikari DataSource in `@AfterAll`, clear security context) in a test base class to avoid lingering threads.
6. Add a short README entry documenting the `BadCredentialsException` → `UnauthorizedException` pattern and JWT testing notes (Clock usage).



## M3 – AuthenticationService (Authentication — Security) — Summary

### Key Achievements

* **Designed and implemented authentication DTOs**

  * Created `AuthenticationRequestDTO` with validation for `username` (email) and `password` (pattern enforcing at least 8 chars, letters, numbers and a special character).
  * Created `AuthenticationResponseDTO` that returns `token`, `username` and `role` to clients — keeping responses decoupled from the `User` entity.

* **Built the User → Spring Security adapter**

  * Implemented `CustomUserDetails` (adapter) that implements Spring Security’s `UserDetails` and wraps my JPA `User` entity.
  * Implemented `getAuthorities()` to map my domain `Role` (enum) into `SimpleGrantedAuthority("ROLE_<ROLE>")`.
  * Implemented `CustomUserDetailsService` (loader) that implements `UserDetailsService`, queries `UserRepository` and returns `new CustomUserDetails(user)` or throws `UsernameNotFoundException`.

* **Wired core security beans**

  * Confirmed and registered a `PasswordEncoder` (`BCryptPasswordEncoder`) bean.
  * Exposed Spring’s `AuthenticationManager` (the real manager built from my `UserDetailsService` and `PasswordEncoder`) so it can be injected into my service logic.

* **Implemented `AuthenticationServiceImpl` — the authentication orchestration**

  * Called `authenticationManager.authenticate(...)` with a `UsernamePasswordAuthenticationToken` built from the DTO credentials.
  * Extracted the authenticated principal as `CustomUserDetails` and retrieved authorities from the returned `Authentication`.
  * Normalized the single role by mapping `GrantedAuthority::getAuthority()` and stripping the `ROLE_` prefix to produce a single role string (e.g., `"SKYDIVER"`).
  * Called `JwtService` to create a JWT with subject and the single role claim and returned a populated `AuthenticationResponseDTO`.

* **Refactored JWT handling to match domain**

  * Moved from a multi-role design (`List<String> roles`) to a single-role design (`String role`) because `User` has a single `Role` enum.
  * Updated tests and JWT claim key to a single `"role"` claim and used injected `Clock` for deterministic timestamp tests.

---

### Key Learnings & Concepts

* **AuthenticationManager & Authentication lifecycle**

  * Learned that `AuthenticationManager` is the entry point I call in application code; it delegates to one or more `AuthenticationProvider`s (`DaoAuthenticationProvider` by default) to validate credentials.
  * Understood the two forms of `Authentication`: an *unauthenticated* token I create (contains credentials) and an *authenticated* token returned by the manager (contains principal and authorities, `isAuthenticated=true`).

* **UserDetails vs UserDetailsService responsibilities**

  * `UserDetails` is a framework-facing representation of a user (username, password, authorities, enabled flags). I created `CustomUserDetails` as an adapter rather than making my JPA `User` implement the interface.
  * `UserDetailsService` is the loader Spring calls during authentication; `CustomUserDetailsService` is responsible for fetching the `User` from the repository and returning the adapter.

* **Authority vs Role semantics**

  * Authorities are `GrantedAuthority` objects used by Spring to make access decisions; roles are a common authority type and use the `"ROLE_"` prefix convention so `hasRole("X")` works.
  * I learned to keep `CustomUserDetails` returning `ROLE_<ROLE>` for Spring compatibility and to strip the prefix only when producing JWT/DTO values.

* **Separation of concerns**

  * Authentication (credential verification) is handled by Spring-provided machinery (`AuthenticationManager`/`DaoAuthenticationProvider` + `PasswordEncoder`), while token issuance (JWT creation) is my service responsibility (`JwtService`).
  * `AuthenticationServiceImpl` becomes the thin orchestrator: authenticate → extract principal/role → create token → return DTO.

* **Testing and determinism**

  * Using an injected `Clock` in `JwtService` allows deterministic tests for issued/expiration times.
  * Tests must use the same `PasswordEncoder` and secret key used in the app (I used reflection in tests to set fixed secrets for assertions).

---

### Challenges & Solutions (lessons learned)

* **Tried to `@Autowired` a `User` entity**

  * *Symptom:* “No beans of type `User` found” and confusion about why DI failed.
  * *Cause:* Entities are not Spring beans — Hibernate produces them at runtime.
  * *Solution:* Stop attempting DI for entities; fetch via `UserRepository` and wrap into `CustomUserDetails` in the loader.

* **Merged adapter and loader into one class**

  * *Symptom:* Attempted DB calls at class-field scope, wrong interface implemented.
  * *Cause:* Confused `UserDetails` (adapter) with `UserDetailsService` (loader).
  * *Solution:* Split responsibilities: `CustomUserDetails` implements `UserDetails`; `CustomUserDetailsService` implements `UserDetailsService` and queries the repository.

* **Incorrect authorities types**

  * *Symptom:* Attempts such as returning `List<String>` or casting lists to `GrantedAuthority` and using `authorities.toString()` produced wrong values like `"[ROLE_SKYDIVER]"`, type errors, or logic bugs.
  * *Cause:* Misunderstanding of what Spring expects: a collection of `GrantedAuthority` objects, not strings.
  * *Solution:* Return `List.of(new SimpleGrantedAuthority("ROLE_"+user.getRole()))` from `getAuthorities()`. In service, map authorities to strings using `getAuthority()` and sanitize by stripping `"ROLE_"` for JWT/DTO.

* **Casting `authentication.getPrincipal()` to JPA `User`**

  * *Symptom:* ClassCastException risk and runtime errors.
  * *Cause:* Principal is the `UserDetails` adapter, not the entity.
  * *Solution:* Cast to `CustomUserDetails` and, if I need the entity, expose `getUser()` on that adapter.

* **AuthenticationManager bean not available / manual attempts**

  * *Symptom:* Tried returning a `UsernamePasswordAuthenticationToken` or building my own manager — didn’t work.
  * *Cause:* I didn’t realize Spring builds the manager from configured providers; you must expose it via `AuthenticationConfiguration`.
  * *Solution:* Return `authConfig.getAuthenticationManager()` from `SecurityConfig` so Spring supplies the properly wired manager (using my `CustomUserDetailsService` and `PasswordEncoder`).

* **JWT design mismatch (multi-role → single-role)**

  * *Symptom:* Tests and implementation used lists for roles while the domain has a single enum role.
  * *Cause:* Over-generalized initial design.
  * *Solution:* Refactor `JwtService` and tests to store a single `"role"` claim; change service code to extract a single role string. Update tests to assert the single claim and deterministic timestamps via injected `Clock`.

---

### Reflection

* **Separation of responsibilities paid off.** Keeping `User` (entity), `CustomUserDetails` (adapter), `CustomUserDetailsService` (loader), `AuthenticationService` (orchestration), and `JwtService` (token issuance) separate made root-cause debugging straightforward.
* **Trust Spring’s authentication plumbing.** I learned to rely on `DaoAuthenticationProvider` and `PasswordEncoder` for secure credential checks rather than trying to reimplement checks myself.
* **Types matter — be explicit.** Almost every early bug was a type mismatch (String vs `GrantedAuthority`, entity vs `UserDetails`, list vs single role). Being explicit about types early prevents subtle runtime errors.
* **Design for current domain, but keep extension points.** I simplified to single-role tokens because that matches the domain now; I left the code structure such that multi-role support (mapping multiple authorities) can be added later without major rework.
* **Testing practices:** using an injected `Clock` for JWT time control and keeping test secrets configurable made the JWT assertions reliable. Also, unit tests for `AuthenticationServiceImpl` (mocking `AuthenticationManager` and `JwtService`) plus an end-to-end integration test plan will give good coverage.

---

### Next Steps

1. **AuthController (thin)** — expose `POST /auth/login`, validate `AuthenticationRequestDTO`, call `IAuthenticationService.authenticateUser(...)`, and return `AuthenticationResponseDTO`; keep this controller logic-free and focused on validation and delegation.
2. **Integration test for login pipeline** — write a focused integration test that seeds a test user with an encoded password, posts credentials to `/auth/login`, asserts `200` and that the response contains a valid JWT (proper subject/role/expiry), and asserts `401` for wrong credentials.
3. **SecurityFilterChain + JwtAuthenticationFilter (wiring)** — after login flow is validated, add the JWT filter and configure the filter chain to permit `/auth/**`, protect `/api/**`, and set stateless session management so incoming requests are authenticated by tokens.

---

### Actionable checklist (for repo notes)

* [x] `AuthenticationRequestDTO` created + validation.
* [x] `AuthenticationResponseDTO` created.
* [x] `CustomUserDetails` adapter implemented (`UserDetails` implementation).
* [x] `CustomUserDetailsService` implemented (`UserDetailsService` loader).
* [x] `PasswordEncoder` bean registered (BCrypt).
* [x] `AuthenticationManager` exposed from `AuthenticationConfiguration`.
* [x] `AuthenticationServiceImpl` implemented (authenticate → extract role → issue JWT → return DTO).
* [x] `JwtService` refactored to use a single `role` claim and tests updated to use injected `Clock`.
* [ ] `AuthController` (next).
* [ ] Integration test for login (next).
* [ ] `SecurityFilterChain` + `JwtAuthenticationFilter` (later).



## M3 – IJwtService / JwtServiceImpl & Tests — Summary

### Key Achievements

* **Designed and implemented the JWT service contract and implementation**

  * Created the `IJwtService` interface as a clear contract for JWT operations (`generateToken`, `validateToken`, `extractUsername`).
  * Implemented `JwtServiceImpl` to produce signed JWTs containing `subject` (username) and a `roles` claim, to validate tokens (signature + expiration) and to extract the username from a token.

* **Made token signing and time deterministic and testable**

  * Introduced a `TimeConfig` to provide a `Clock` bean and refactored `JwtServiceImpl` to use the injected `Clock` so token `issuedAt`/`expiration` are deterministic in tests.
  * Centralized SecretKey handling: `JwtServiceImpl` decodes a Base64 secret and produces a `SecretKey` with `Keys.hmacShaKeyFor(...)` for type-safe signing and verification.

* **Built a focused unit test suite and test helpers**

  * Wrote unit tests for token generation, validation (happy path), expiration handling, wrong-signature behavior, and username extraction.
  * Used `ReflectionTestUtils` to inject private `@Value` fields (`secretKey`, `jwtExpiration`) for lightweight tests without booting the Spring context.
  * Achieved full line coverage for the JWT service (JaCoCo hit 100% for this component).

---

### Key Learnings & Concepts

* **JWT anatomy & lifecycle**

  * Learned and practiced that a JWT is `header.payload.signature`, that `header` describes algorithm/type, `payload` carries standard claims (subject, iat, exp) and custom claims (e.g., roles), and the `signature` proves integrity.
  * Understood that the secret used to sign the token must never be embedded in the token — you verify by trying to parse with the correct key; you prove a key is correct by *succeeding* to parse and failing with the wrong key.

* **JJWT 0.12.x modern API and type safety**

  * Learned why JJWT moved toward type-safe APIs: use `SecretKey` objects (not raw strings/bytes) and prefer `verifyWith(SecretKey)` and `parseSignedClaims(...)` over deprecated variants (`setSigningKey(byte[])`, `parseClaimsJws`).
  * Practiced decoding a Base64 secret and creating a `SecretKey` via `Keys.hmacShaKeyFor(...)` to satisfy the library’s type expectations.

* **Deterministic time testing**

  * Learned why injecting `Clock` is important: `Clock.fixed(...)` makes issued/expiration assertions deterministic and avoids flaky tests caused by `System.currentTimeMillis()`.
  * Discovered the nuance that the JJWT parser checks expiration against *system time* by default, so for expiry-related unit tests I must either use the same fixed Clock in validation logic or design the test to parse claims and compare to a controlled instant.

* **Unit testing strategies for JWT**

  * Learned to test token content by parsing the token with the *same* secret and asserting claims (subject, roles, issuedAt, expiration).
  * Learned to test negative cases:

    * Wrong signature — create a token signed with a different key (manual builder) and assert verification fails.
    * Expired token — generate with a fixed clock, validate with a later clock or parse claims and assert expiration is before the validation time.
    * Malformed tokens are structurally invalid (wrong segments / bad Base64 / broken JSON) — recognized but deprioritized because coverage goal was already met.

* **Practical test tooling**

  * Used `ReflectionTestUtils.setField(target, fieldName, value)` to inject `@Value` properties into the service in unit tests (careful: target object first, exact field name, correct type such as `60L` for long).
  * Used `Clock.fixed(...)` to freeze time, and `Instant.parse(...)` for precise expected Instants in assertions.
  * Used `Jwts.parser()/parserBuilder()` + `verifyWith(secretKey)` + `.parseSignedClaims(token)` to decode claims in tests without deprecated methods.

---

### Challenges & Solutions (lessons learned)

* **JJWT API & deprecation confusion**

  * **Problem:** Old tutorials and autocomplete suggested deprecated methods (`setSigningKey`, `parseClaimsJws`); IDE sometimes showed `.parser()` only.
  * **Solution:** Adopted JJWT 0.12+ idioms: produce a `SecretKey` (Base64 → bytes → `Keys.hmacShaKeyFor(...)`) and use `verifyWith(SecretKey)` + `parseSignedClaims(...)`. When IDE tooling misled me, I refreshed Gradle, invalidated caches, and checked External Libraries.

* **Secret format mismatch (hex vs Base64)**

  * **Problem:** I originally had a hex secret but code expected Base64; Base64 decoder failed on hex.
  * **Solution:** Standardised on Base64 in `application.properties` and decode consistently in `getSigninKey()`. I noted the alternative (explicit hex decoding) for future reference.

* **Clock / expiration test flakiness**

  * **Problem:** Parsing/validation used system time so tests using a fixed clock for generation failed in real time (parser threw ExpiredJwtException).
  * **Solution:** Refactored service to use injected `Clock` in validation checks (or alternatively use parse-then-compare with the injected Clock). For production the service still behaves with system time when injected `Clock.systemUTC()`.

* **ReflectionTestUtils pitfalls**

  * **Problems:** Wrong argument order, wrong field names (e.g. `expirationMinutes` vs `jwtExpiration`), and type mismatches (`int` vs `long`) caused reflection errors.
  * **Solution:** Always call `setField(targetObject, "fieldName", value)` with the exact private field name and correct Java type (`60L` for `long`).

* **Claims structure & date handling mistakes**

  * **Problem:** Tried to use `List` where a `Map<String,Object>` was required for claims; used `new Date(String.valueOf(...))` incorrectly.
  * **Solution:** Use `Map<String,Object>` for claims, `claims.put("roles", roles)`, and `Date.from(Instant)` for date fields. Also compute `issuedAt` and `expiresAt` inside `generateToken()` so timestamps are fresh per token.

* **Testing wrong signature**

  * **Problem:** Initially generated token via `jwtService.generateToken()` (signed with the correct key) then tried to assert `validateToken` would be false — naturally it passed.
  * **Solution:** Built a token manually signed with a different `SecretKey` and passed that to `jwtService.validateToken()`, which then failed as expected.

* **What can/cannot be asserted**

  * **Problem:** Attempted to assert the secret key appeared in token header.
  * **Solution:** Learned the secret never appears in the token; instead assert signature correctness by parsing with the correct key (success) and parsing with a different key (failure).

* **Deciding on malformed-token tests**

  * **Decision:** I recognised malformed-token tests exercise robustness, but given unit coverage (JaCoCo 100%) and scope, I deprioritised them for now. I documented how to build malformed tokens (remove segments, corrupt Base64, break JSON) for future integration tests if needed.

---

### Reflection

This milestone changed how I think about security code: the JWT service must be **small, testable, and single-purpose** — generate, parse, verify — and *not* mix in user identity resolution. My tests taught me to control the environment (time, keys) so unit tests are deterministic; integration tests will later validate end-to-end behavior. I also learned to respect library evolutions (JJWT 0.12.x) and to prefer type-safe APIs (`SecretKey` + `verifyWith`). The iterative debugging process (fix reflection, fix date handling, handle Base64 vs hex, refresh IDE caches) sharpened my troubleshooting workflow and gave me a repeatable pattern for future security work: choose formats explicitly, inject Clock, use type-safe crypto APIs, and write small, focused tests that prove only the intended responsibility.

---

### Next steps 

1. **Authentication controller & AuthenticationService (AuthController + DTOs)**
   *Purpose:* Implement `/auth/login` (and optionally `/auth/register`) that accepts credentials, delegates to an `AuthenticationService` which verifies credentials (via `UserService` / password encoder) and returns a JWT from `IJwtService.generateToken()`.
   *Why next:* This integrates token issuance into the API and provides a concrete way for clients to get JWTs.

2. **JwtAuthenticationFilter & Security configuration**
   *Purpose:* Implement a `OncePerRequestFilter` that extracts `Authorization: Bearer <token>`, calls `IJwtService.validateToken()` and `extractUsername()`, loads user details, and sets the `SecurityContext`, and configure a `SecurityFilterChain` that allows `/auth/**` but protects `/api/**`.
   *Why next:* This is the glue that converts tokens into an authenticated request context and enforces stateless security semantics.

3. **Integration tests for auth/read-protected endpoints**
   *Purpose:* Add integration tests (MockMvc or SpringBootTest with test profile) that assert `/auth/login` returns token, protected endpoints return 401 without token and 200 with valid token, and role-based access control returns 403 where applicable.
   *Why next:* This validates the whole auth pipeline end-to-end and catches environment/time/key issues that unit tests cannot.



## M3 – JwtAuthenticationFilter & SecurityFilterChain – Summary

### Key Achievements

- **Implemented JWT-based request authentication**

	- Developed a filter that validates JWTs on incoming requests, checking signature, expiration, and proper format.
	
	- Ensured the filter integrates properly with Spring Security’s filter chain and leverages `SecurityContextHolder` to set authentication for downstream processing.
	
	- Built `JwtAuthenticationFilter` (extends `OncePerRequestFilter`) to:
        
        - read `Authorization: Bearer <token>` headers,
            
        - extract and validate tokens with `IJwtService` / `JwtServiceImpl`,
            
        - load user details via `CustomUserDetailsService`,
            
        - populate `SecurityContextHolder` with a `UsernamePasswordAuthenticationToken`.
            
    - Wrote a unit test for the filter’s happy path using Mockito to validate that a valid token results in an authenticated `SecurityContext`.
        
- **Added JSON error handlers for security failures**

	- Validated that proper HTTP status codes (`401 Unauthorized` and `403 Forbidden`) are returned with meaningful error messages.
    
    - Implemented `CustomAuthenticationEntryPoint` to return a clean JSON 401 response (timestamp, status, error, message, path).
        
    - Implemented `CustomAccessDeniedHandler` to return a clean JSON 403 response and (optionally) include the authenticated user name when available.
        
- **Wired Spring Security configuration | Updated `SecurityConfig` with a `SecurityFilterChain`**

	- Configured authentication rules, including protected endpoints, permitted public endpoints, and integration of the JWT filter.
	- Ensured that the filter chain executes in the correct order to prevent circular dependencies or conflicts with Spring Security’s built-in filters.
    
    - Implemented `SecurityConfig` with a `SecurityFilterChain` bean:
        
        - stateless session (JWT-based),
            
        - CSRF disabled for API usage,
            
        - simple CORS using `CorsConfiguration().applyPermitDefaultValues()` for local frontend testing,
            
        - registered the `JwtAuthenticationFilter` before `UsernamePasswordAuthenticationFilter`,
            
        - registered `authenticationEntryPoint` and `accessDeniedHandler` for JSON responses,
            
        - created permit/require rules for endpoints (auth endpoints `permitAll`, protected endpoints `authenticated()`).
            
- **Built an integration test harness and helpers**
    
    - Created `SecurityIntegrationTest` using `@SpringBootTest`, `@AutoConfigureMockMvc`, H2/test profile and transactional context.
        
    - Added `JwtTestUtilsHelper` utilities to generate expired tokens (by overriding the clock) and invalid-signature tokens (by creating a temp JwtServiceImpl with another secret) ensuring valid, expired, and invalid JWT tokens for integration testing.
        
    - Wrote integration tests covering:
        
        - valid token happy path (calls test-only controller),
            
        - negative security cases: missing header, malformed header, invalid signature, expired token (asserting `401 Unauthorized`).
            
    - Created a minimal `TestOnlyBasicController` endpoint (`GET /api/jump/all`) to exercise routing and security behavior.
        

* * *

### Key Learnings & Concepts

- **Spring Security Filter Chain and `OncePerRequestFilter`**.
    
    - The filter intercepts every request once. Calling `filterChain.doFilter(request, response)` hands processing to the next filter (or the controller) — think of it as “pass the baton to the next step in the pipeline”.
        
    - The filter must either set `SecurityContextHolder` and call `doFilter` (pass through) or allow an exception to be handled by Spring Security’s exception handling (via `AuthenticationEntryPoint`/`AccessDeniedHandler`).
        
- **JWT Authentication Mechanism**

	- Learned how JWTs are used to authenticate requests without server-side sessions, including validation of signature, expiration, and claims.

	- Explored the role of `SecurityContextHolder` in Spring Security for storing authenticated user details during request processing.
    
    - JWT is like a stamped ticket: the server stamps (signs) it at login, and subsequent requests present the ticket; the filter checks stamp and expiry and, if valid, lets the user in without storing any session.

- **Custom Error Handling**

  - Learned how to implement structured error responses in JSON for security exceptions.

  - Explored the interplay between `AuthenticationEntryPoint` (for unauthenticated requests) and `AccessDeniedHandler` (for insufficient permissions).

- **SecurityContextHolder and Authentication**
    
	- Explored the role of `SecurityContextHolder` in Spring Security for storing authenticated user details during request processing. 

    - `SecurityContextHolder.getContext()` stores authentication for the current thread/request. Placing an `Authentication` object there makes the rest of Spring Security treat the request as authenticated.
        
    - The `principal` inside `Authentication` is usually the `UserDetails` object (not the username string). If you expect the username, call `getPrincipal().getUsername()` or use `getName()`.
        
- **Testing layered choices**

	- Learned how to mock and test HTTP requests with `MockMvc` in the presence of Spring Security filters.
	
	- Explored strategies to generate valid and invalid JWT tokens dynamically for testing multiple scenarios (happy path, expired, malformed, invalid signature).
	
	- Learned to isolate test controllers for authentication tests, preventing unnecessary dependencies on service or repository layers.
	
	- Unit tests (Mockito) for the filter are fast and let me isolate behavior (happy path, verify `SecurityContextHolder` population, verify `filterChain.doFilter` called).
	    
	- Integration tests (SpringBootTest + MockMvc) are essential to validate the actual Spring Security wiring: `SecurityFilterChain`, `AuthenticationEntryPoint`, `AccessDeniedHandler`, and how exceptions are converted into JSON responses.
        
- **Deterministic token generation for tests**
    
    - Overriding the Clock or the `secretKey` with `ReflectionTestUtils` (or using a test-only `JwtServiceImpl`) enables creating tokens that are expired or have invalid signatures in a deterministic way.

- **Troubleshooting Circular Dependencies**

  - Encountered issues with Spring beans in circular dependency (`JwtAuthenticationFilter` requiring `SecurityConfig` and vice versa).

  - Learned how constructor injection vs field injection affects bean creation and how to refactor to avoid circular initialization.

* * *

### Challenges & Solutions (Lessons Learned — detailed)

#### 1) Circular dependency at ApplicationContext startup

- **Symptom:** `BeanCurrentlyInCreationException` / `Requested bean is currently in creation` when loading the test application context; stacktrace pointed to `securityConfig` and the filter beans.
    
- **Root cause:** I had beans referencing each other in a way that created a circular initialization dependency (for example: the security config tried to autowire beans that themselves required `SecurityConfig` during creation).
    
- **Fix / Lesson:**
    
    - Break circular references. Provide handler beans with dedicated `@Bean` factory methods (in `SecurityConfig`) instead of trying to field-autowire them in a way that re-enters the config creation.
        
    - Prefer constructor injection for normal beans — but when wiring `SecurityFilterChain` and filter beans in the same configuration class, be careful to avoid direct cross-dependencies that cause circular creation.
        
    - Mental note: circular dependency = two or more beans need each other to be created, so Spring cannot complete instantiation. Detect it early when `ApplicationContext` fails to start; check the chain in the stacktrace and refactor wiring.
        

#### 2) `MockMvc` configuration and 404 / content-type surprises

- **Symptom:** Test returned `404` initially because the controller endpoint did not exist. After adding the test controller the response content-type was `text/plain` and my assertion expected `application/json`.
    
- **Fix / Lesson:**
    
    - Create a small test controller (`TestOnlyBasicController`) that returns JSON (e.g., `ResponseEntity<Map<String,String>>`) rather than plain `String` to satisfy content-type assertions.
        
    - Verify endpoint path and http method exactly in the test (leading/trailing slash or missing `/api` are common sources of 404).
        
    - For initial security-only tests a small stub controller is sufficient to exercise the security pipeline — don't wait to implement full controllers.
        

#### 3) Header usage mistakes (mock request vs header string)

- **Symptom:** Used a string like `"Authorization: Bearer "` as the header name in `mockMvc.perform(...).header(...)` (i.e., included the `Bearer` prefix in the header name), which confused MockMvc and caused failing requests.
    
- **Fix / Lesson:**
    
    - Correct usage: `.header("Authorization", "Bearer " + token)`. Header name is `"Authorization"`. Value is `"Bearer <token>"`.
        
    - Small detail but very common — pay attention to header name vs header value.
        

#### 4) `SecurityContextHolder` principal confusion in unit tests

- **Symptom:** Assert compared expected username string to `SecurityContextHolder.getContext().getAuthentication().getPrincipal()`, but `getPrincipal()` returned a `CustomUserDetails` instance string representation — assertion failed.
    
- **Fix / Lesson:**
    
    - Cast principal to `CustomUserDetails` and call `getUsername()` to assert the correct username.
        
    - Alternative checks: `SecurityContextHolder.getContext().getAuthentication().getName()` returns username; `getPrincipal()` returns a `UserDetails` object.
        

#### 5) Exceptions thrown by the filter vs AuthenticationEntryPoint handling

- **Symptom:** Filter threw `BadCredentialsException` or a custom `UnauthorizedException`, and tests saw stack traces or unexpected exceptions rather than an HTTP 401 JSON response.
    
- **Root cause:** If the filter throws an exception before Spring Security's exception handling is wired (or without correct `authenticationEntryPoint` registration), the exception bubbles differently in tests.
    
- **Fix / Lesson:**
    
    - Keep the filter simple: on malformed/missing header, **do not** throw — just `doFilter` through (so public endpoints still work). On invalid/expired token, throw an `AuthenticationException` (or let Spring Security handle `JwtException`) — but ensure `SecurityConfig` registers the `authenticationEntryPoint` so those exceptions produce a consistent JSON 401 response.
        
    - In tests, verify that invalid tokens produce `401` and the JSON body using MockMvc; ensure the `SecurityConfig` bean registers the `CustomAuthenticationEntryPoint`.
        

#### 6) Deterministic token helpers & ReflectionTestUtils timing

- **Symptom:** Parameterized method source needed tokens/user data but ran before `@BeforeEach`, causing `NullPointerException` when the static provider tried to access instance fields.
    
- **Fix / Lesson:**
    
    - `@MethodSource` provider methods must be `static` and parameterless when used directly by JUnit. They run before instance-level `@BeforeEach`, so they cannot rely on instance fields initialized in `@BeforeEach`.
        
    - Two approaches:
        
        - (a) Build tokens inside the test methods (or in `@BeforeEach`) and use non-parameterized tests; or
            
        - (b) Make the provider static and use static helpers and static test data set up in `@BeforeAll` (or set static fields in a `@BeforeEach` but then the provider still runs earlier — so `@BeforeAll` + static setup is the right place).
            
    - I solved by moving helper setup into places that guarantee availability when `@MethodSource` runs or by avoiding passing runtime instance data into static providers.
        

#### 7) How I created expired and invalid-signature tokens (test helpers)

- **Expired tokens:** temporarily override the clock inside `jwtService` (use `ReflectionTestUtils.setField(jwtService, "clock", pastClock)`), generate the token, then restore the normal clock. This produces a token whose `exp` claim is in the past.
    
- **Invalid signature tokens:** create a new `JwtServiceImpl` instance for testing, set a different `secretKey` (via `ReflectionTestUtils`) and generate a token — the real service (with the real secret) will reject that token’s signature.
    
- **Lesson:** Making tokens deterministic for tests requires controlling time and keys; ReflectionTestUtils is handy for test-only manipulations but keep it contained to test helpers.
    

#### 8) Parameterized tests gotchas

- **Symptom:** Attempted to make a `@MethodSource("unauthorizedRequests")` provider accept instance parameters (like `jwtService`, `user`) — method source is static and cannot accept instance members.
    
- **Fix / Lesson:**
    
    - Provider must be static (or in another class) and must not rely on instance state from `@BeforeEach`. Use static setup or generate tokens within each test case.

* * *

### Reflection

- **Small, isolated experiments save time. - "Fast is Slow and Slow is Fast"** Many hours were spent because a chain of small misconfigurations compounded. Next time I’ll run a very small test after each tiny change:
    
    - Add controller → run `MockMvc` smoke test to check path and response content-type.
        
    - Add filter unit test (Mockito) → validate `SecurityContextHolder` behavior.
        
    - Wire `SecurityConfig` → run a single integration test for a public endpoint and one protected endpoint.
        
- **Read stacktraces top-down and follow the bean creation chain.** The circular dependency error pointed to bean creation order — that’s a configuration-level issue, not a logic bug in the filter code. Security filters require meticulous ordering and careful injection management; minor misconfigurations can lead to subtle bugs or app context failures.
    
- **MethodSource and test lifecycle are subtle.** `@MethodSource` runs earlier than `@BeforeEach`. If a provider needs runtime data, build the data in `@BeforeAll`/static or inside the test itself.
    
- **Keep test helpers deterministic.** Using `Clock` injection and `ReflectionTestUtils` to set secrets and clocks gave me control for expired/invalid tokens — this is a pattern worth reusing. Centralizing token generation and using helper utilities improves test reliability and reduces repeated debugging sessions.
    
- **Prefer clarity over cleverness.** When I tried to be clever with dependency wiring and static tricks, it led to circular beans and brittle tests. Simpler wiring (beans returned from `@Bean` factory methods, small test controllers, explicit header names/values) made things stable.
    

**Notes for future reference:**

- Write the minimal controller endpoint first (stub) before writing integration security tests.
    
- Start with unit tests for filters using Mockito to validate internal behavior, then move to one simple integration test.
    
- When a provider method is needed for parameterized tests, make it static and ensure its inputs are static or pre-initialized in `@BeforeAll`.
    
- Prefer constructor injection for application beans, but avoid creating circular constructor dependencies — split config beans if needed.

- Maintain careful separation of concerns between security logic, controller endpoints, and service layers to avoid hidden coupling or initialization traps.
    
- Always assert exact header usage and content-type expectations early to detect simple mistakes quickly.
    

* * *

### Compact checklist / TL;DR (for future reference)

- JwtAuthenticationFilter:
    
    - reads `Authorization: Bearer <token>`,
        
    - extracts username via `jwtService.extractUsername(token)`,
        
    - validates token via `jwtService.validateToken(token)`,
        
    - if valid → load `UserDetails`, create `UsernamePasswordAuthenticationToken`, set it in `SecurityContextHolder`, then `filterChain.doFilter`.
        
    - if token missing or not Bearer → `filterChain.doFilter` (do not throw).
        
    - if token invalid/expired → throw an `AuthenticationException` and let `AuthenticationEntryPoint` convert it to a JSON 401.
        
- Test strategy:
    
    - Unit test the filter with Mockito for happy path and for verifying `filterChain.doFilter` is called.
        
    - Integration tests with `@SpringBootTest` + `@AutoConfigureMockMvc` to validate 401/403 JSON responses and the real `SecurityFilterChain`.
        
    - Use small stub controllers to exercise security endpoints.
        
- Common pitfalls to avoid:
    
    - Static provider methods executed before `@BeforeEach`.
        
    - Confusing header name vs header value in MockMvc.
        
    - Circular bean dependencies when wiring filters and the security config.
        
    - Asserting JSON content-type when controller returns `String` (`ResponseEntity<String>` defaults to `text/plain`), use `ResponseEntity<Map>` or `@ResponseBody` with proper produces.
        

* * *

This milestone taught me more than just the mechanics of JWT and Spring Security — it forced me to learn the testing lifecycle, Spring bean lifecycle, how the security filter pipeline actually works, and how small mistakes cascade into large debugging sessions. I now have a working authentication filter, JSON error handlers, security configuration, deterministic JWT test helpers, and an integration test suite that exercises the main negative scenarios. The next step is to expand controller-level authorization (`@PreAuthorize`) and to add tests for role-based access (SKYDIVER vs ADMIN).

## M4 – REST Controllers & API Endpoint Tests

### Key Achievements

* **Completed controller integration tests for core endpoints**

  * Wrote and stabilized integration tests (MockMvc + real `JwtService`) for `UserController`, `JumpController`, and `LookupController`. Tests cover create/read/update/delete flows, list/search/pagination, and aggregate endpoints (`totalFreefall`, `totalJumps`).
  * Tests assert HTTP status codes and deserialize responses (via `ObjectMapper`) into DTOs to verify payload fields rather than relying on fragile assumptions.

* **Added controller request/response logging**

  * Implemented a centralized logging interceptor and registered it in the MVC configuration so every controller request and response can be traced during tests and debugging.
  * Logged request method/URI, key headers (Authorization trimmed), and response information so I can diagnose runtime behavior quickly.

* **Aligned service tests with DTO changes**

  * Refactored `StaticDataServiceImpl` tests after Lookup DTOs were changed to return DTOs instead of entities. Reworked tests to verify repository→mapper→DTO interactions using mocked mappers and repositories.

* **Improved exception handling for security**

  * Enhanced `ErrorHandler` to handle `AccessDeniedException` and produce standardized JSON 403 responses, so clients get consistent error shapes for authorization failures.

---

### Key Learnings & Concepts (what I learned, phrased as new knowledge)

* **How Spring Security method-level checks operate**

  * I learned that `@PreAuthorize` must be enabled explicitly via `@EnableMethodSecurity` (or the older `@EnableGlobalMethodSecurity(prePostEnabled=true)`) for SpEL expressions like `#id == authentication.principal.id` to be evaluated. Without it, annotations are silently ignored and behavior is misleading.

* **What `authentication.principal` actually is**

  * The SpEL expression sees whatever object I put into `SecurityContextHolder` as the `principal`. That means my JWT filter must set a `CustomUserDetails` object as the principal (not a `String` username) if I want `principal.id` to work inside `@PreAuthorize`.

* **Ordering rules in security matchers**

  * In the `authorizeHttpRequests` DSL, specific matchers must come before the terminal `.anyRequest().authenticated()`. Putting `anyRequest()` too early produces `IllegalStateException` or effectively blocks subsequent matchers.

* **JWT test strategy for true end-to-end coverage**

  * Generating tokens inside tests and sending them in `Authorization: Bearer <token>` simulates real production authentication. For full-stack behavior I should generate real JWTs and make sure the filter reconstructs `CustomUserDetails` from those tokens.

* **MockMvc patterns to inspect responses**

  * Use `.andReturn()`→`MvcResult` → `getResponse().getContentAsString()` → `ObjectMapper.readValue(...)` to deserialize JSON into DTOs for robust assertions. Also learned when to use `jsonPath` (short checks, e.g., `$.content.length()`) vs full deserialization.

* **JSON shape differences: List vs Page**

  * If a controller returns `Page<T>` the JSON root is an object with a `content` array and pagination metadata, not a raw array. Trying to deserialize a `Page` response into `List<T>` throws `MismatchedInputException`. Use `$.content.length()` or parse into a `JsonNode`/`PageImpl` to inspect content size.

* **Testing discipline: assert behavior, not implementation**

  * Tests should validate actual API behavior (status, body shape, fields). Avoid hardcoding ID values (e.g., `1L`) — instead capture created resource IDs from responses, or query repository by user to find created resources.

---

### Challenges, Bugs, and Solutions (detailed lessons learned)

> I list the specific errors/bugs I encountered, how I discovered them, and the final solution I implemented.

* **Ambiguous request mapping caused `ApplicationContext` failure**

  * **Symptom:** `Ambiguous mapping. Cannot map 'jumpController' method ... There is already 'testOnlyBasicController' bean method mapped.` during test ApplicationContext startup.
  * **Cause:** Two controller methods were mapped to the same path (`/api/jumps/all`) — one in the real controller and one in a test-only controller used in other tests.
  * **Solution:** Make sure test controllers use unique paths or remove the test-only controller mapping collision. I changed the URI used by the SecurityIntegration test to avoid the clash.

* **`anyRequest()` placed before specific matchers → `IllegalStateException`**

  * **Symptom:** `Can't configure mvcMatchers after anyRequest`
  * **Cause:** I had `anyRequest().authenticated()` before other `requestMatchers(...)`.
  * **Solution:** Reordered the DSL: put specific `.requestMatchers(...)` rules first (e.g., `POST /api/users` permitAll), and `.anyRequest().authenticated()` last.

* **`@PreAuthorize` not evaluated — allowed unauthorized access**

  * **Symptom:** Users could access admin-protected endpoints; `@PreAuthorize` seemed ineffective.
  * **Cause:** I had `@EnableWebSecurity` but not `@EnableMethodSecurity`, so method-level security was not activated.
  * **Solution:** Add `@EnableMethodSecurity(prePostEnabled = true)` to security configuration. After enabling method security, `@PreAuthorize` expressions evaluated.

* **SpEL `#id == authentication.principal.id` didn’t behave as expected**

  * **Symptom:** Admin should have been allowed but manual in-method checks were blocking; later, normal user could see admin profile.
  * **Cause:** My JWT filter originally created an `Authentication` token whose principal was the `String` username, not `CustomUserDetails`. SpEL `authentication.principal.id` therefore did not resolve as intended.
  * **Solution:** Ensure the JWT filter loads `CustomUserDetails` and creates `UsernamePasswordAuthenticationToken(userDetails, null, userDetails.getAuthorities())`, so `authentication.principal` is a `CustomUserDetails` and `principal.getId()` exists for SpEL.

* **Redundant manual ownership checks in controller**

  * **Symptom:** Even when `@PreAuthorize` allowed access (e.g., admin), the manual check inside the controller threw `AccessDeniedException`.
  * **Cause:** I had both `@PreAuthorize` and an in-method `if (!id.equals(principal.getId())) throw AccessDeniedException(...)`. The manual check ignored the `hasRole('ADMIN')` branch.
  * **Solution:** Remove the redundant manual ownership checks and rely on `@PreAuthorize` to centralize authorization logic.

* **Change password test returned 401 / 403 unexpectedly**

  * **Symptom:** `PUT /api/users/{id}/password` tests returned 401 or 403 and failed even though tokens were generated the same way as other tests.
  * **Cause 1 (401):** The stored user password in the DB was plain text during test setup, but the service checks `PasswordEncoder.matches(old, stored)`. The old password comparison failed.
  * **Cause 2 (403):** Earlier the admin was blocked because of the redundant manual check inside the method (see above).
  * **Solution:** Encode the persisted user password using `passwordEncoder.encode(...)` before generating token and calling the endpoint; remove manual ownership checks and rely on `@PreAuthorize`.

* **Not persisting entities before asserting / using hardcoded IDs**

  * **Symptom:** Tests that fetched by ID returned 404 because the entity never existed in DB (I had set `id` in the object constructor but never saved).
  * **Cause:** Instantiating domain objects with a hard-coded id does not persist them; JPA generates ids on save.
  * **Solution:** Persist jumps via `jumpRepository.saveAndFlush(...)`, capture the returned entity and use `jump.getId()` when calling the endpoint. Avoid hardcoded ids like `1L`.

* **Helper methods accidentally created multiple persisted instances and caused mismatches**

  * **Symptom:** Update tests failed or behaved inconsistently because helper `persistAircraft()` / `persistDropzone()` were called multiple times producing different IDs for the initial jump and the update DTO.
  * **Cause:** Helpers persisted separate entities on each call; test used different persisted entities across create/update.
  * **Solution:** Persist the related entities once per test and re-use their returned instances for both the initial object and the update DTO. I simplified tests to pull IDs from the persisted jump (`jump.getAircraft().getId()`) to guarantee alignment.

* **Jackson `MismatchedInputException` when expecting List vs Page**

  * **Symptom:** `Cannot deserialize value of type ArrayList<JumpLookupDTO> from Object value (token START_OBJECT)` when I tried to read a page response into a `List`.
  * **Cause:** Controller returned `Page<T>` JSON structure (object with `content`, `totalElements`, etc.), while test expected a raw array.
  * **Solution:** Inspect response structure and use `jsonPath("$.content.length()")` for size assertions, or parse JSON into a `JsonNode` and read `content`. For more detailed checks deserialize `content` into `List<JumpLookupDTO>` using the `content` node.

* **AccessDeniedException testing confusion**

  * **Symptom:** `AccessDeniedException` constructors had different signatures than my custom exceptions and I was unsure what arguments to supply in tests. Also confusion around not having `getStatusCode()` on exception.
  * **Cause:** `AccessDeniedException` is a Spring Security runtime exception with various constructors; it does not expose an HTTP status. Error handler should map exception type to `HttpStatus.FORBIDDEN` explicitly.
  * **Solution:** In `ErrorHandler` add an `@ExceptionHandler(AccessDeniedException.class)` that constructs an `ApiErrorResponseDTO` with `HttpStatus.FORBIDDEN` and a standard message/code. In tests, instantiate `new AccessDeniedException("message")` and assert the returned `ResponseEntity` status is `HttpStatus.FORBIDDEN`. Rely on the handler to map exception → response status, rather than expecting the exception to carry HTTP status.

* **Security filter nuance: ensure `CustomUserDetails` is principal**

  * **Symptom:** SpEL security expressions misbehaved and debugging showed `authentication.principal` was a string.
  * **Cause:** `UsernamePasswordAuthenticationToken` was constructed with `username` as principal.
  * **Solution:** Load `CustomUserDetails` in the filter and construct auth token with `userDetails` as principal. Log principal class in the filter during tests to validate.

---

### Reflection — Lessons for future development

* **Enable the framework features you intend to use**

  * I learned the hard way that annotations like `@PreAuthorize` depend on enabling method security – missing this is a silent source of bugs. Always validate that infrastructure-level features are active when you rely on them.

* **Trust Spring Security but avoid duplication**

  * Put complex auth rules into method-level security (`@PreAuthorize`) or a dedicated security component (`@Service` used in SpEL), and avoid duplicating the same checks inside controllers. Redundant manual checks can create authorization contradictions and hard-to-find bugs.

* **Write tests that reflect real traffic patterns**

  * Generating real JWTs in tests and running the full security filter chain provides confidence that the system will behave the same in production. Tests that mock or bypass too much of the stack can give false confidence.

* **Prefer explicit persistence and response-driven IDs**

  * Always persist domain objects during setup and capture the real IDs returned by the DB. When asserting creation, prefer to read the returned resource from the controller (`201 Created` body) or query the repository by owner to find created resources — don’t hardcode ids.

* **Logging + structured error responses pay off**

  * Adding a logging interceptor and standardized error DTOs (including 403 handling) made diagnosing integration test failures far faster. Logging the principal type, request URI, and exception messages helped me find mismatches between tokens, users and persisted state.

* **Keep test scaffolding DRY but safe**

  * The `TestFactory` pattern (centralized helper component to persist users, jumps, lookups, and create tokens) is a great next step to reduce boilerplate without repeating buggy helper logic. Centralized helpers make it easier to ensure consistent entity relationships across tests.

---

### Final notes

* When introducing new cross-cutting features (security, logging), plan for a small suite of integration tests that specifically exercise those features (e.g., authentication happy/fail paths, role checks, filter ordering). This prevents regressions later.
* Keep the JSON contracts (DTO shapes) documented; when controllers change return types from `List<T>` to `Page<T>`, add tests asserting JSON shape (content vs root array) so callers (like the UI) won't be surprised.
* Use `ObjectMapper` deserialization into DTOs for deep assertions; use `jsonPath` for quick sanity checks (counts and presence). Both are valuable; pick the one that communicates intent best for the test.
* Maintain a compact `TestFactory` and a small set of “canonical” test users (skydriver vs admin) and test lookups to speed new test creation and reduce setup errors.
* Keep `ErrorHandler` mappings explicit: application exceptions → proper `HttpStatus`. Do not assume security exceptions contain HTTP status — map them centrally.

---

I recorded the bugs I encountered and the exact fixes I applied (ordering `authorizeHttpRequests`, enabling method security, making the JWT filter set `CustomUserDetails` as principal, encoding persisted passwords, persisting entities before assertions, returning and deserializing created resources, using `$.content` for pages, and updating static-data tests to assert DTO mapping). These are the precise patterns I should follow the next time I add features (e.g., UI) — they saved hours of debugging and gave me confidence the API behaves exactly as the front-end will expect.


## M4 – REST Controllers (Auth, Users, Jumps, Lookups) — Summary

### Key Achievements

* **Built and finalized core REST controllers**

  * Implemented `AuthController`, `UserController`, `JumpController`, and `LookupController`.
  * Created all main endpoints for users and jumps, including creation, retrieval, updating, deletion, aggregation, and search functionality.
  * Ensured static reference data (`Aircraft`, `Dropzones`, `Jumptypes`) is exposed via DTOs with proper mapping.
  * Returned paginated results where necessary (`/api/jumps/all`, `/api/jumps/search`).

* **Integrated security and ownership checks**

  * Applied `@PreAuthorize` with SpEL for both ownership and role-based access.
  * Programmatically confirmed ownership using `CustomUserDetails`’s `id` to prevent cross-user access.
  * Ensured JWT principal flows correctly through `@AuthenticationPrincipal`.

* **Refactored related services and mappers**

  * Updated `JumpService` and `StaticDataService` to return DTOs instead of entities.
  * Updated mappings to `*LookupDTO` for static data, keeping the API decoupled from persistence.
  * Centralized validations like date-range checks in the service layer for consistency.

* **Applied RESTful best practices**

  * Returned proper status codes (`201 Created` for creation with `Location` headers).
  * Maintained consistent resource paths and DTO-first response patterns.
  * Kept controllers lean, delegating business logic to services and mapping to mappers.

---

### Key Learnings & Concepts

* **Security integration is subtle but critical**

  * I realized that security is not just about using `@PreAuthorize` but also about how I expose the authenticated principal and reference it safely in SpEL.
  * Learned the importance of combining declarative security (SpEL) with programmatic checks for custom error messages and ownership verification.
  * Confirmed that exposing `id` in `CustomUserDetails` is essential for seamless SpEL and avoids leaking internal entity structure.

* **DTO-first design is foundational, not optional**

  * Returning entities directly was a tempting shortcut early on, but mapping everything to DTOs provided flexibility, future-proofing, and clear separation between persistence and API contract.
  * Learned that even static reference data benefits from DTO mapping, allowing changes in persistence structure without breaking the API.
  * Understanding that `List<Entity>` vs `List<DTO>` is invariant reinforced why mapping streams are necessary and clarified the correct way to handle type transformations in service layers.

* **Reflecting on controller responsibilities**

  * Controllers are not service layers; they should parse input, handle security and validation, and delegate business logic. Trying to push logic into controllers early caused messy code and confusion.
  * Handling programmatic ownership checks taught me the subtle balance between declarative SpEL security and explicit code-based validation.

* **Error handling and design discipline**

  * Centralizing exceptions in the service layer (`InvalidArgumentException`, `ResourceNotFoundException`) and propagating to controllers simplified controller logic and made error handling predictable.
  * Learned that consistent response structures (`MessageResponse` for confirmations, DTOs for resources) improve API clarity and consumer understanding.

* **Pagination and performance considerations**

  * Even though I currently return full lists for lookups, thinking ahead about pagination and streaming DTOs highlighted the trade-offs between simplicity and scalability.
  * Recognized that small design choices (like returning `Location` in POST responses) are part of API ergonomics that pay off in long-term maintainability.

* **Reflective awareness of testing needs**

  * The change to DTOs made me realize how tightly service and controller tests depend on the mapping layer.
  * Learned to anticipate what will break in tests when refactoring return types, which reinforces the importance of keeping unit and slice tests isolated but aware of structural changes.

---

### Challenges & Solutions

* **SpEL resolution issues**

  * Initially struggled with referencing `#id` in `@PreAuthorize`. Fix: confirmed method parameters match the SpEL reference and exposed `id` on principal.
  * *Problem:* `@PreAuthorize` expressions could not resolve `id` or returned compile errors.
  * *Fix:* Use `@PathVariable` (not `@RequestParam`) for path IDs and reference method parameters in SpEL with `#id`. Also ensure `CustomUserDetails` exposes `getId()` so `authentication.principal.id` is available.

* **Mapping collection types**

  * Couldn’t just switch `List<Entity>` → `List<DTO>`; needed explicit `stream().map().collect(Collectors.toList())`.
  * *Problem:* Tried to change method signature from `List<Entity>` to `List<DTO>` without mapping; generics are invariant.
  * *Fix:* Explicitly mapped entity lists to DTO lists using `stream().map(mapper::toDto).collect(toList())`.

* **Ownership vs path id confusion**

  * Early code sometimes mixed `principal.getId()` and `@PathVariable` id in services. Fix: standardized path id as target, confirmed ownership programmatically.
  * *Problem:* Some methods ignored the path `id` and used `principal.getId()` in service calls — confusing and inconsistent.
  * *Fix:* Standardized on using the path `id` as the target resource for service calls, and used `@PreAuthorize` + optional programmatic check to ensure caller is owner.

* **Date binding & validation in search**

  * *Problem:* Search endpoint accepting `LocalDateTime` needed explicit binding and validation; also needed to ensure `from <= to`.
  * *Fix:* Added `@DateTimeFormat(iso = DateTimeFormat.ISO.DATE_TIME)` at controller level (where applicable) and moved the date-range validation into `JumpService.searchJumps()` (with a guard at the top of the method to throw `InvalidArgumentException` on bad ranges).

* **Controller vs service responsibilities**

  * Initially overcomplicated controllers by embedding business logic. Fix: moved all logic to services, controllers handle delegation, input parsing, validation, and security.

* **Returning entities vs DTOs in lookups**

  * *Problem:* `LookupController` initially returned entities (`Aircraft`, etc.), which couples persistence to API.
  * *Fix:* Added `*LookupDTO` mappers and updated `StaticDataServiceImpl` to map `repository.findAll()` → `List<*LookupDTO>` with streams and MapStruct mappers.

* **Pageable injection and controller signatures**

  * *Problem:* Incorrect `@RequestParam Pageable pageable` usage caused binding problems.
  * *Fix:* Use Spring’s `Pageable` binding correctly (`@PageableDefault` or rely on Spring Data’s default resolver) and accept `Pageable` as an argument, or explicitly accept `page` and `size` query params to build `PageRequest`.

* **Delete semantics (soft vs hard delete)**

  * *Problem:* Deciding whether `DELETE` should be soft or hard.
  * *Resolution:* I used soft-delete (deactivate) for users, returning `UserLookupDTO` showing `active=false`; for jumps, I used hard delete and returned deleted jump info (or opted for `204` in some designs). Documented the decision and kept it consistent.

* **`changePassword` response**

  * *Problem:* Service returned `void` and controller had nothing to return for the action.
  * *Fix:* Kept service `void` and introduced a small `MessageResponse` record for controller responses (e.g., `"Password updated successfully"`), keeping the service layer free of API concerns.

* **Naming & mapper methods clarity**

  * *Problem:* Mapper method names like `jumpListToJumpLookupDTO` were confusing when passing `Page<Jump>`.
  * *Fix:* Noted to rename mapping methods to clearly reflect input/output (`toJumpLookupDTOPage` or similar) to improve readability.

---

### Reflection & Lessons Learned

* **Separation of concerns is essential** — I reinforced the value of keeping controllers thin: they parse requests, delegate to services, and format responses. Services do the business logic and repositories handle persistence. Mappers translate entities ↔ DTOs.

* **Security should be explicit and testable** — using `@PreAuthorize` with SpEL for ownership checks is powerful, but it requires correct method signatures and an explicit principal representation (`getId()` on `CustomUserDetails`). I also learned to combine declarative and programmatic checks when I want custom error messaging.

* **DTO-first thinking pays off** — returning DTOs everywhere avoids leaking entity internals and makes future changes easier. This required an explicit mapping step which I implemented across static data, users, and jumps.

* **Testing discipline** — I reinforced the testing pyramid: write fast slice tests for controllers (mapping, validation), robust unit tests for services, and targeted integration tests for security and important end-to-end flows. There are still TODOs for controller tests and adjusted static-data service tests.

* **Small pragmatic choices matter** — decisions like where registration should live, whether to return a `MessageResponse` for actions, how to return deleted resources, and whether to paginate static lists all influence API UX and maintainability.

* Security, mapping, and validation are intertwined — handling one without the others leads to brittle, insecure, or confusing APIs.
* DTO-first thinking is not just good practice; it shapes my design decisions, from service layer to testing.
* Explicit ownership checks are essential even when using `@PreAuthorize`; relying purely on declarative security is insufficient.
* Every small API design choice (response codes, headers, DTO structure) contributes to a maintainable and predictable system.

---

This milestone deeply strengthened my understanding of secure, testable, and maintainable REST controller design, emphasizing how controllers, services, mappers, DTOs, and security interact in a real-world application. It also forced me to reflect on design trade-offs, anticipate future requirements, and adapt testing practices proactively.

---

### Remaining TODOs / Next Steps

* Add controller logging for all endpoints.
* Update static-data service tests for DTO-based return types.
* Implement controller slice tests for User and Jump controllers.
* Add `AccessDeniedException` handling in `ErrorHandler` to produce standardized 403 JSON responses.
* Consider pagination and caching for static lookup endpoints to improve performance.








## M6 – Frontend UI (Dashboard & Jumps Page) – Fixes & Debugging Summary

### Key Achievements

* **Fixed dashboard ordering and pagination**

  * Adjusted the dashboard so jumps now load in descending order, with the most recent jump always displayed first. This change aligns the UI with how a logbook should naturally be read: newest entries at the top.
  * Corrected pagination to start at the last page when the data is displayed in descending order. Without this, the user was initially taken to the first page, which showed the oldest jumps, creating confusion. Now the first screen aligns with real user expectations.

* **Corrected `jumpNumber` calculation**

  * Identified and fixed a backend bug where the system was calculating `jumpNumber` based on database `id` rather than chronological `jumpDate`. This created inconsistencies, particularly when inserting or editing jumps retroactively.
  * Refactored backend logic so that `jumpNumber` is dynamically recalculated using `jumpDate`, ensuring consistent numbering that truly represents jump order. This is critical for skydiving logs, where sequence and chronology matter.

* **Restored and improved sorting functionality**

  * Debugged the custom sorting feature in the jumps table. At one point, sorting for the `jumpNumber` column stopped working after I had commented out the client-side sort logic, mistakenly thinking the server could handle everything.
  * Restored the dedicated client-side sorting for `jumpNumber`, since it cannot be derived properly from paginated server results. Other columns (e.g., altitude, date) remained server-side sorted via API queries. This gave a clean separation of concerns but also ensured the special case of `jumpNumber` sorting works correctly.
  * This was a valuable reminder that different fields sometimes require different strategies depending on whether they are domain-calculated or purely data-driven.

* **Implemented a reset sorting button**

  * Introduced a reset button next to pagination controls. This button restores the default descending-by-date view, giving users a one-click way to undo custom sorts.
  * Designed it to behave like a lightweight page refresh, ensuring simplicity and avoiding the need for complex state resets. This improves usability and saves users from having to manually navigate back to the “default view.”

* **Minor fixes and UI polish**

  * Made the header sticky, ensuring key dashboard statistics and context remain visible even while scrolling through long jump lists. This change improved usability for larger datasets.
  * Corrected sorting for static data entities such as aircraft, dropzones, and jump types, which were previously appearing inconsistently.
  * Improved table presentation by adjusting date formatting to display only the date (not the time) via `toLocaleString`. This simplified the view and removed unnecessary noise from the logbook.
  * Applied smaller styling tweaks: consistent spacing between elements, clearer section separation, and improved alignment. Collectively, these refinements made the UI easier to navigate and more visually balanced.

---

### Key Learnings & Concepts

* **Client-side vs. server-side sorting**
  I gained a deeper appreciation for the distinction between local in-memory sorting and backend-driven sorting through API queries. The `jumpNumber` column is a prime example of a case that must be handled locally because it is derived dynamically from chronological order, while other data fields (like altitude, free fall time, or jumpDate) can be sorted efficiently by the backend. Understanding when to split responsibilities between frontend and backend is crucial for performance and correctness.

* **Chronological integrity of domain data**
  Fixing the `jumpNumber` bug underscored how misleading it can be to rely on technical identifiers (like auto-incremented IDs) for domain logic. In a real-world application like a logbook, chronology matters more than database sequence. This reinforced the importance of designing domain logic that reflects the problem space rather than the persistence layer.

* **UI/UX considerations in logbook applications**
  By implementing sticky headers and a reset button, I learned how small UI decisions significantly improve usability. Sticky headers prevent users from “losing context” when scrolling through long tables, while reset controls give them confidence to experiment with sorting without fear of “breaking” their view. These are small but meaningful enhancements that raise the overall polish of the interface.

* **Meta-learning from debugging**
  I experienced firsthand how easy it is to break functionality by assuming code is redundant. Commenting out the custom `jumpNumber` sort seemed harmless but removed a critical edge-case solution. The lesson: redundancy sometimes exists because a specific scenario requires a different approach, and removing it without fully tracing the consequences can silently break features.

* **Additional knowledge absorbed through side questions**
  Along the way, I reinforced smaller but useful frontend techniques:

  * Using CSS `position: sticky` to keep headers visible without extra classes or IDs.
  * Formatting dates with `toLocaleString` for a cleaner UI.
  * Structuring buttons and pagination controls in a user-friendly layout.
  * Recognizing when to use JavaScript event handling for interactivity vs. when CSS alone can solve presentation issues.

---

### Challenges & Solutions

* **Dashboard initially ordered by ID**
  *Challenge:* Newest jumps were not displayed first, confusing the user flow.
  *Solution:* Enforced descending order by `jumpDate` and adjusted pagination to load the last page first.

* **Backend assigning jump numbers incorrectly**
  *Challenge:* Jump numbers followed database `id`, not actual jump order.
  *Solution:* Refactored backend logic so numbering is based on `jumpDate`, ensuring proper chronological order.

* **Broken sorting after removing code**
  *Challenge:* `jumpNumber` sorting stopped working when I removed the client-side sort.
  *Solution:* Reintroduced the local sort logic for `jumpNumber` while keeping backend sorting for other fields.

* **Need for reset functionality**
  *Challenge:* No quick way to return to default ordering after experimenting with sorts.
  *Solution:* Added a reset button next to pagination that refreshes the view into the default descending order.

* **UI/UX issues (header, entities, formatting)**
  *Challenge:* Header disappeared when scrolling, static entity sorting inconsistent, date formatting cluttered with time.
  *Solution:* Made header sticky, fixed static data sorting, and simplified date formatting to show only the date.

---

### Reflection

This milestone was less about building entirely new features and more about **debugging, refining, and polishing existing functionality**. The work revealed how intertwined frontend and backend logic can be, especially around sorting and ordering.

I learned that domain logic (like `jumpNumber`) often requires special treatment, because it represents business rules that can’t simply be delegated to database IDs or paginated results. I also learned that frontend polish — sticky headers, reset buttons, clean date formats — can greatly improve the experience without requiring major technical complexity.

One key lesson is the importance of **not discarding logic prematurely**. The sorting bug I introduced by removing code highlighted how important it is to fully understand why a piece of functionality exists before changing it. Debugging this mistake was a valuable reminder that "seemingly redundant" code may actually be guarding against subtle but critical scenarios.

Finally, this milestone reinforced that **debugging and troubleshooting are as much a part of software development as new implementation**. The hours spent carefully tracing through bugs, experimenting, and validating fixes were essential to producing a stable, polished UI. For future work, I will:

* Always confirm whether code is truly redundant before removing it.
* Design with both **backend correctness** and **frontend usability** in mind.
* Remember that polish (like sticky headers and reset buttons) often separates a functional project from a professional one.

---

https://chatgpt.com/share/68cd50c8-dc68-800d-983e-f69e739de80d

## M6 – Frontend UI (Dashboard & Jumps Page) — Summary

### Key Achievements

* **Implemented the Dashboard page**

  * Built a Dashboard layout with totals cards (total jumps, freefall time) and a sortable, paginated jumps table.
  * Added support for `jumpNumber` in the jumps table, ensuring a user-friendly display of sequential jump entries.
  * Integrated frontend JavaScript to fetch jump data from the REST API, handle sorting, and paginate results client-side.
  * Created a modular frontend structure with a main loader, page-specific JS modules, and a centralized API helper (`fetchWithAuth`).

* **Implemented the Jumps page with full CRUD client logic**

  * Built a jump creation form, wired to the backend API (`/api/jumps`) for POST requests.
  * Fetched lookup data (dropzones, aircraft, jumptypes) dynamically to populate dropdowns.
  * Added comprehensive client-side validation (altitude, free fall duration, jump date, notes, and required lookups).
  * Implemented error handling and success feedback for jump creation, including fetching and displaying the newly created jump details.
  * Ensured form reset and field-specific error clearing after successful submission.

* **Enhanced frontend-backend integration**

  * Handled authentication using JWTs stored in `localStorage`.
  * Centralized API request logic to attach tokens for protected endpoints and skip them for public endpoints.
  * Adjusted date formatting to align with backend expectations (`YYYY-MM-DDT00:00:00`) and displayed localized dates in the UI.
  * Decoupled frontend from backend static serving by using a standalone development server (VS Code Live Server).

---

### Key Learnings & Concepts

* **REST API Integration and Client-Server Alignment**

  * Learned the critical importance of aligning frontend field names, types, and required/optional status with the backend DTO.
  * Misalignment (e.g., sending a string instead of a number or misnaming fields) caused backend validation errors that were sometimes unclear.
  * Learned to verify backend responses such as `jumpNumber` or newly created IDs before rendering them in the UI.
  * Reinforced the principle that REST clients must respect API contracts and properly handle asynchronous responses to avoid runtime errors or inconsistent UI states.

* **Asynchronous Data Handling**

  * Learned to manage multiple concurrent fetches (dropzones, aircraft, jumptypes) efficiently using `Promise.all`.
  * Discovered that failure in a single fetch could disrupt the entire form population, emphasizing the need for granular error handling.
  * Implemented fallback/error messages for failed lookups to improve UX and allow retrying without breaking other dropdowns.
  * Recognized the importance of designing frontend flows assuming network instability and partial data responses.

* **Client-Side Validation**

  * Learned to implement robust client-side validation for numbers (altitude, freefall duration), dates, and optional strings.
  * Used `blur` events for immediate user feedback and form submission validation to catch any missed errors.
  * Learned that validation communicates constraints to the user, preventing backend errors and improving usability.
  * Reinforced the concept that validation is not just correctness—it’s part of the UX and error prevention strategy.

* **JWT Handling and Protected API Calls**

  * Learned to decode JWTs client-side to extract claims (e.g., user ID) for protected requests.
  * Recognized the importance of separating public and authenticated API calls to avoid sending tokens unnecessarily.
  * Learned that storing JWTs in `localStorage` is convenient for development but introduces XSS risks.
  * Centralizing fetch logic helped reduce repeated mistakes and improved maintainability, while making token handling consistent across the app.

* **Date and Time Handling**

  * Learned that date inputs must be converted from `YYYY-MM-DD` to backend-compatible ISO format (`YYYY-MM-DDT00:00:00`) to prevent validation errors.
  * Understood that frontend-backend misalignment in date formats can cause subtle, hard-to-detect bugs.
  * Learned to display dates in localized format while maintaining backend compliance.
  * Recognized the importance of consistent formatting for both sending and receiving timestamps in REST APIs.

---

### Challenges & Solutions

* **Backend ID sequence / jumpNumber issues**

  * **Challenge:** Early frontend testing failed because jump IDs and `jumpNumber` were inconsistent due to backend sequence misconfigurations and use of UUIDs. This made it difficult to display newly created jumps predictably.
  * **Solution:** I confirmed the backend sequence configuration and relied on the `jumpNumber` provided by the API instead of trying to generate it client-side. For local testing, I reset sequences and ensured predictable IDs. I also learned to always inspect backend logs or DB state when frontend creation fails unexpectedly, reinforcing the need for reproducible test data.

* **Jump creation errors (DataIntegrityViolationException / null IDs)**

  * **Problem:** Form submissions sometimes caused backend validation errors because of missing foreign keys (aircraft, dropzone, jumptype) or null `userId`.
  * **Solution:** Added thorough client-side validation and ensured proper serialization of IDs in the request body. Verified backend entity constraints and fixed any sequence gaps during local testing.

* **Dropdown population and asynchronous issues**

  * **Challenge:** Dropdowns sometimes appeared empty or partially populated due to asynchronous fetch order. Errors in one fetch disrupted the others, causing confusing UX.
  * **Solution:** I consolidated all lookup fetches using `Promise.all` and wrapped each in error handling to provide feedback for failed requests. I learned that concurrent async calls improve performance but must be paired with robust failure handling. I also confirmed the DOM was fully loaded before appending options to prevent null references.

* **Date formatting and display**

  * **Challenge:** Jump creation failed when sending the date in `YYYY-MM-DD` format because the backend expected ISO datetime with `T00:00:00`. This caused validation errors.
  * **Solution:** I transformed date inputs to ISO format before sending them and localized the display in the UI. This taught me the importance of consistent date-time handling across frontend and backend, especially in APIs that store or compare timestamps.

* **Frontend-backend sequencing of testing**

  * **Challenge:** Testing jump creation was tricky because backend sequences or missing data caused inconsistent IDs, making frontend display unreliable.
  * **Solution:** I established a predictable test environment with reset sequences and verified the created jump details immediately after POST. Logging ID and sequence values helped me debug and understand why certain jumps were skipped or misnumbered.

---

### Reflection

* **Big-picture lesson:** Implementing a full-featured frontend for a REST API requires careful alignment with backend sequences, DTO structures, and validation rules. Predictable backend behavior is essential for reliable client-side testing.

* **What I did well:**

  * Iteratively tested frontend and backend integration, correcting sequences and DTO mismatches as they appeared.
  * Centralized API helper logic to reduce repetitive code and prevent authorization errors.
  * Implemented robust client-side validation, improving UX and reducing invalid backend submissions.

* **What I would do differently next time:**

  * Establish a stable backend dataset and predictable sequences before frontend testing.
  * Predefine the DTO field types and constraints with the frontend team (or client module) to avoid repeated validation fixes.
  * Consider using a small frontend test harness to simulate backend responses for faster iterative development.

* **Overall:** This milestone consolidated my understanding of **modular frontend structure, client-side validation, REST API integration, asynchronous data handling, and frontend-backend troubleshooting**. The Dashboard and Jumps pages now work end-to-end, with robust error handling, predictable data display, and clear lessons learned for future enhancements.



## M6 – Frontend UI (Delete, Edit & Ordinal Bug Fix) – Summary

### Key Achievements

* **Implemented Delete jump from the Dashboard**

  * I added a delete action on the dashboard table that calls the REST API `DELETE /api/jumps/{id}` to remove a jump.
  * I added a confirmation dialog that shows a parachute emoji (🪂) and asks the user to confirm before deleting.
  * After deleting, I refresh the dashboard list so the UI reflects the deletion.

* **Implemented Edit jump flow using the existing jumps form**

  * I implemented an edit workflow that reuses `jumps.html` and `jumps.js` for both create and edit:

    * Dashboard "Edit" controls navigate to `jumps.html?edit=<id>`.
    * `jumps.js` detects `?edit=<id>`, fetches the jump (`GET /api/jumps/{id}`), and pre-fills the form.
    * When submitting in edit mode, the client issues `PUT /api/jumps/{id}` with a `JumpUpdateDTO`-shaped payload, then redirects back to the dashboard on success.
  * I adjusted the UI to indicate edit mode (changing the header and submit button text).
  * I wired the submit logic to await the PUT when `editId` is present, and return early to avoid executing the POST create logic.

* **Fixed the backend jump ordinal calculation bug**

  * I discovered and fixed a backend issue where jump ordinal numbers were calculated incorrectly when jumps were inserted out of chronological order or when multiple jumps shared the same date.
  * I updated the repository/service calculation to use `countByUserIdAndJumpDateLessThanEqualAndIdLessThanEqual(userId, jumpDate, id)` so the ordinal is computed deterministically by date and id.
  * I wired the service (`getAllJumps`) to map each `Jump` into a `JumpLookupDTO` and set `jumpNumber` using the corrected count query.

* **Refactored frontend lookups and validation wiring**

  * I refactored the lookup-loading code so `loadLookups()` is an exported function that both create-mode and edit-mode call.
  * To avoid duplicated `<option>` entries when `loadLookups()` runs multiple times, I clear select `.innerHTML` before appending options.
  * I reused form validation logic for both create and edit flows (same `validateField` and per-field blur handling).

---

### Key Learnings & Concepts

* **Event handling strategies for dynamic content**

  * I learned the difference between attaching listeners to elements individually and using event delegation. Individual listeners (via `querySelectorAll` + `addEventListener`) only attach to elements that exist at the moment of the call; delegated listeners (on a parent or `document`) handle current and future elements and are more robust for dynamic tables.
  * I deliberately chose a pragmatic approach: attach listeners after rendering when using `loadDashboard()` (this matched how I re-render the table). I also explored and considered the delegated approach as a more future-proof pattern.

* **How ids travel from backend → DOM → event handler**

  * I clarified that `jump.id` is a number inside the JS object parsed from the backend JSON, while `data-*` attributes on DOM elements (e.g., `data-jump-id`) are strings. I learned to embed `jump.id` into `data-jump-id` during row rendering and read it back with `element.dataset.jumpId` when handling click events.

* **Using URL query params for edit mode**

  * I learned the simple and reliable pattern of driving edit-mode behavior from the URL: `jumps.html?edit=<id>`. `jumps.js` can detect the `edit` parameter, fetch canonical server data, prefill the form, and switch submit behavior.

* **Timing and ordering of async UI updates**

  * I learned that selects must be populated before setting `.value`; setting `.value` before options exist silently fails. The correct flow is:

    1. Load lookup data (aircraft, dropzones, jumptypes) and populate `<select>`s.
    2. Only then assign `select.value = <id>` to preselect the option.
  * I also learned that calling a lookup loader multiple times without clearing selects causes duplicate `<option>` entries — and the fix is to clear `.innerHTML` before repopulating.

* **Backend calculation correctness matters to UI semantics**

  * The frontend depends on the server to provide canonical jump numbering (jumpNumber). When the backend’s ordinal calculation was wrong, the frontend displayed incorrect numbers. Fixing the backend repository logic restored UI correctness and highlighted the need to verify full-stack invariants, not only the UI.

* **Practical debugging techniques**

  * I used console logging and inspected network requests (DevTools) to reason about behavior: confirming the JSON shape returned by `GET /api/jumps/{id}`, identifying that `aircraftId` was `undefined` because the backend nested the object (`jump.aircraft.id`), and tracing why `.value` assignments failed.
  * I learned to check for places where code threw exceptions early (e.g., missing quotes in `getElementById` calls) and how a single runtime error stops execution, leading to partial prefill.

---

### Challenges & Solutions (detailed, lesson-by-lesson)

**1. Delete implementation — initial problems and final solution**
*Problem:*

* After wiring a `handleDelete()` that called `DELETE /api/jumps/{id}` and then `await loadJumps()`, I observed a confusing behavior: the jump was deleted on the backend but the page later showed an error (the catch block fired).
  *Diagnosis and fix:*
* I added debugging logs to inspect the HTTP responses and realized `loadJumps()` was the wrong function on the dashboard page. The dashboard uses `loadDashboard()` to fetch and render the jumps list. After changing to `await loadDashboard()` the deletion flow worked without the error.
  *Lesson learned:*
* Be sure the client-side refresh call matches the page’s data-fetching function. Re-using similar function names (loadJumps vs loadDashboard) can easily cause mismatches that hide the real error.

**2. `handleDelete` scope and attaching listeners**
*Problem:*

* Using inline `onclick="handleDelete(...)"` resulted in `ReferenceError: handleDelete is not defined` because the handler was module-scoped and not on `window`.
  *Solutions considered & final decision:*
* Option A: Expose handlers to `window` to make inline `onclick` work. This worked but pollutes the global namespace.
* Option B: Use event delegation (recommended) — attach a single listener on the table body or document and detect clicks on `.delete-btn` or `.edit-btn`. This is robust for dynamic rows.
* What I did: Because my dashboard re-renders rows and I reattach listeners after rendering, I pragmatically kept the `querySelectorAll(...).forEach(... addEventListener ...)` approach but made sure to execute it after each `loadDashboard()` render; I left open the option to refactor to delegation if needed.

**3. Edit-mode prefill edge cases**
*Problems encountered (multiple):*

* I had a number of small but tricky errors while implementing edit prefill:

  * I accidentally used unquoted identifiers in `getElementById(jumpDate)` and `getElementById(aircraftId)`, which caused `ReferenceError` and stopped execution.
  * Dropdowns remained unselected even though the backend returned the correct nested IDs (e.g., `jump.aircraft.id`) — `aircraftId` was `undefined` when I was reading `jump.aircraftId`.
  * Even after switching to `jump.aircraft.id`, selects still didn’t show selection because the select options were not present yet.
  * Calling `loadLookups()` repeatedly without clearing selects caused duplicate options.
    *Steps I took & fixes implemented:*
* Fixed the quoting errors (use `'jumpDate'` etc.).
* Read nested objects from the backend (`jump.aircraft.id`, `jump.dropzone.id`, `jump.jumpType.id`) instead of non-existent flat `aircraftId` fields.
* Made `loadLookups()` an exported function and ensured the edit flow `await loadLookups()` before `.value` assignment.
* To be defensive and avoid duplicates, I reset the `<select>` elements (`select.innerHTML = '<option value="">Select …</option>'`) before appending new options.
  *Lesson learned:*
* Pay attention to the actual JSON shape returned by the backend and ensure form population waits for dependent async data (lookup options) to exist before assigning values.

**4. PUT vs POST flow and concurrency**
*Problem:*

* Initially the submit handler attempted to run create logic even when in edit mode; I also invoked the update function without awaiting it, which permitted the code to continue and collide with the create path.
  *Fix:*
* In the submit handler I now `await putUpdateJump(editId)` when `editId` is present and then `return` to ensure the POST create logic does not run.
  *UX flow:*
* After a successful PUT I redirect back to `dashboard.html`. I chose to show an alert on success. I also discussed using `localStorage` to carry a success message to the dashboard for a one-time display; in practice I used a direct alert then redirect for immediacy in our tests.
  *Lesson learned:*
* Always await async update flows in submit handlers and stop further execution. Carefully separate branches for create and update.

**5. Lookup-loading scoping issue**
*Problem:*

* At first `loadLookups()` was declared inside `loadJumps()` so it wasn’t available to `loadJumpForEdit()`; attempts to call it from edit mode failed or were inconsistent.
  *Fix:*
* I exported `loadLookups()` so both create and edit code can call it. I also made it defensive by clearing select contents before appending options, so repeated calls won’t duplicate options.
  *Lesson learned:*
* Keep utility functions that are used by multiple flows at a scope accessible to both; clear DOM containers before repopulating them.

**6. Backend ordinal number bug — discovery and fix**
*Observation that exposed the bug:*

* I noticed jump numbering was wrong when I created a jump with an earlier date than existing jumps. For example, if the last jumps were numbers 23, 24, 25 (August), and I created a jump dated in July, it still got number 26 rather than inserting the ordinal relative to date order.
  *What I tried first and why it failed:*
* The initial repository method used `countByUserIdAndIdLessThanEqual`, which only considered id ordering and not the jump date. I then tried `countByUserIdAndJumpDateLessThanEqual`, which considered date but caused duplicate ordinal numbers when multiple jumps had the same date.
  *Final fix implemented:*
* I created and used `countByUserIdAndJumpDateLessThanEqualAndIdLessThanEqual(userId, jumpDate, id)` in the `JumpRepository` so the ordinal is computed first by date then by id, providing a deterministic and stable ordering even for same-day jumps and for backdated inserts.
  *Where I applied it:*
* In the `getAllJumps` service method I map the `Page<Jump>` and for each `jump` compute `jumpNumber` using the new repository count method and set it on the `JumpLookupDTO`.
  *Lesson learned:*
* Ordinal/sequencing logic that must respect a compound ordering (date then id) needs a repository-level query that expresses that ordering; relying only on id or only on date can break invariants in corner cases (backdated inserts, deletes, same-date entries).

**7. Diagnostic and pragmatic decisions**
*Logging and step-by-step checks:*

* I used console logs to verify JSON shapes and values during prefill (`console.log('Backend aircraftId:', jump.aircraft.id)`), and used DevTools Network tab to inspect `DELETE`/`PUT` requests and response statuses.
  *Trade-offs I made:*
* For `handleEdit`/`handleDelete` listeners I chose an approach that fit my current rendering lifecycle: re-attaching listeners after `loadDashboard()` renders rows. I kept the simpler pattern for now but noted delegation is the long-term cleaner solution.
  *Ignored non-critical warnings:*
* I observed an IntelliJ/git static analysis warning about `'throw' of exception caught locally`. It did not break runtime behavior, so I left it for later refactoring.

---

### Reflection

This milestone was a concentrated exercise in full-stack thinking: small frontend features (edit/delete) surfaced timing, scoping, and ordering issues in the client, and also revealed a subtle backend correctness bug in ordinal calculation. The major takeaways for me were:

* **Order matters.** Async ordering (load lookups first, then prefill) is a recurring source of bugs. Being explicit about "what must exist before X" saved me time.
* **Know your data shape.** I repeatedly tripped over differences between the backend representation and my frontend assumptions (`jump.aircraft.id` vs `jump.aircraftId`). Always inspect the JSON, especially after changing DTOs or mappers.
* **Event wiring needs to match rendering lifecycle.** Whether I attach listeners after render or use delegation, I must be consistent and think about re-renders.
* **Frontend debugging exposes backend gaps.** The ordinal-number bug is a great example: a UI inconsistency led to a repository fix. End-to-end thinking (and tests) avoids surprises.
* **Be pragmatic and iterative.** I tried quick fixes (call lookups multiple times, attach handlers globally) but eventually converged on safer, clearer solutions (clear selects, ensure proper await/return logic, export shared lookups).
* **Document the decisions.** I noted the trade-offs (global vs delegated handlers, where I left lint warnings) so future me knows why choices were made.

---

### Notes for future work / checklist

* Consider moving to event delegation for the dashboard actions to make listener management simpler and less error-prone.
* Implement a one-time dashboard success notification using `localStorage` or a query param instead of `alert` for a smoother UX.
* Add integration tests that simulate create/edit/delete flows to protect ordinal calculation invariants.
* Revisit `try/catch` patterns that triggered the `'throw' of exception caught locally` linter warning and either add context or handle errors locally.
* Consider auth-token storage hardening (HttpOnly cookies / refresh tokens) in the future; currently I’m using localStorage for ease of development.
* Add a small E2E smoke test that covers dashboard list rendering, edit navigation, edit prefill, successful PUT, and successful DELETE.


## M6 – Frontend UI (Client for the REST API) (Register & Login)— Summary

### Key Achievements

* **Built a minimal, working frontend for registration and login**

  * Implemented pages for Register and Login and wired them to the backend so I could create users and obtain JWTs.
  * Verified registration persisted to the database and login returned a valid token; I confirmed this with the H2 console and existing backend tests.

* **Designed a protected Dashboard flow**

  * Implemented a dashboard that only displays user data after a successful authentication check from the client side.
  * Implemented JWT extraction on the client to call the user profile endpoint using the user id contained in the token.

* **Refactored frontend into a modular structure**

  * Broke monolithic JS into small, focused modules (API helper, register, login, dashboard, main loader) for maintainability and clarity.
  * Centralized API request logic (including token handling) so authenticated and unauthenticated calls are clear and reusable.

* **Improved backend security/CORS alignment for frontend dev**

  * Adjusted CORS configuration and SecurityFilterChain rules to match the chosen frontend deployment (VS Code Live Server).
  * Tuned the JwtAuthenticationFilter and SecurityFilterChain to consistently allow public API endpoints (login/registration) and protect API endpoints.

* **Completed the migration to a separate frontend-app**

  * Extracted HTML/CSS/JS out of the Spring Boot static resources into a standalone `frontend-app` served by VS Code Live Server, achieving a clean separation of concerns between frontend and API.

---

### Key Learnings & Concepts

* **Static files vs. protected endpoints**

  * I learned that serving protected pages as static resources under Spring Boot is problematic: static assets are served without the usual JWT lifecycle and browsers do not attach JWTs for raw HTML navigations.
  * I learned why direct navigation to a static, protected page cannot rely on Authorization headers (the browser won’t attach them), so server-side guarding of static HTML is unreliable unless the HTML is produced via a controller.

* **Filter execution order and `permitAll()` semantics**

  * I learned the JWT filter runs before authorization matchers are evaluated, so `permitAll()` alone is insufficient if the JWT filter tries to validate the token and aborts the request early.
  * I learned to align filter skip logic exactly with what I permit in the SecurityFilterChain (explicitly skipping `/api/auth/**` and the registration `POST /api/users`).

* **CORS preflight & Authorization header**

  * I learned that custom headers like `Authorization` trigger preflight OPTIONS requests and that CORS must explicitly allow `Authorization` and `OPTIONS` to avoid opaque-blocking errors in the browser.
  * I learned that `allowedOrigins`/`allowedOriginPatterns`, `allowedMethods`, `allowedHeaders`, and `allowCredentials` must be configured carefully for local dev (Live Server origin) and for requests that include auth headers.

* **Client-side JWT handling**

  * I learned to store the JWT (for now) in `localStorage`, decode it safely on the client to extract claims (like the user id), and use it in `Authorization` headers for protected API calls.
  * I learned to distinguish public API calls (registration, login) that must never include an Authorization header from protected calls that require it.

* **Frontend architecture basics**

  * I learned the value of a small, pragmatic modular JS architecture for a vanilla JS app: separate files for API helpers, page-specific logic, and a main loader to wire events.
  * I learned why centralizing fetch logic (token attachment, headers) reduces bugs — and also why it must be used selectively (not for public endpoints).

---

### Challenges & Solutions (Lessons Learned)

* **Problem: Static HTML pages returning 401 on direct navigation**

  * **What happened:** I initially put frontend files under Spring Boot `static/`. Directly visiting `/dashboard.html` returned 401 because the JWT filter ran and no Authorization header was present for the HTML GET.
  * **Why it happened:** Static files are served as resources; the browser does a direct GET (no JWT in headers). Even with `permitAll()` configured for some paths, the JWT filter still executed and blocked requests if it attempted validation prematurely.
  * **Solution / decision:** I moved frontend files out of the Spring Boot static folder and decided to serve them from a separate development server (VS Code Live Server). This allowed the backend to be API-only and the client to perform authentication checks and call protected endpoints with the JWT in headers.

* **Problem: JWT filter blocking public requests**

  * **What happened:** Even when I added `permitAll()` for login and registration, the JWT filter still intercepted and sometimes returned 401 because it ran before authorization evaluation.
  * **Why it happened:** The filter’s logic attempted validation on all requests and returned errors instead of letting the security chain decide.
  * **Solution:** I changed the filter to explicitly skip (short-circuit) only the exact public API paths (e.g., `/api/auth/**` and `POST /api/users`) and dev tools (Swagger/H2). I aligned this skip-list with the SecurityFilterChain rules to avoid mismatches.

* **Problem: Registration failing with 401 or incorrect request handling**

  * **What happened:** Registration failed at first for multiple reasons: I called the wrong endpoint in places, I used a helper that appended Authorization where none existed, and I forgot `Content-Type: application/json`.
  * **Why it happened:** I mixed up endpoints (e.g., confusing `/register` vs `/api/users`), used `fetchWithAuth` for registration (which appended Authorization), and omitted headers.
  * **Solution:**

    * Confirmed and used the correct registration endpoint that the backend exposes.
    * Ensured public endpoints are called with plain `fetch` (no Authorization header) and include proper `Content-Type`.
    * Limited `fetchWithAuth` use to protected endpoints only.

* **Problem: OpaqueResponseBlocking / NS\_BINDING\_ABORTED from browser when calling protected API**

  * **What happened:** Dashboard fetch calls (with Authorization) were being blocked by the browser as an opaque response, not reaching the backend.
  * **Why it happened:** CORS preflight requests (OPTIONS) were not permitted for the `Authorization` header or OPTIONS method, so the browser aborted the main request.
  * **Solution:** Updated the backend CORS config to explicitly allow the Live Server origin(s) and to allow the `Authorization` header and the `OPTIONS` method. After this, preflight succeeded and requests proceeded.

* **Problem: Confusion over which pages to permit in SecurityConfig**

  * **What happened:** I tried multiple permutations of `requestMatchers` and static resource allowances which created confusion and intermittent 401s.
  * **Why it happened:** Some static resource matchers didn’t match exactly what Spring used, and static HTML are different from static resources matchers.
  * **Solution:** I removed static resource matchers from the backend (since the frontend moved out) and kept SecurityFilterChain focused on API paths only. If I needed to keep any static file served by Spring Boot, I used `PathRequest.toStaticResources().atCommonLocations()` to correctly match them.

* **Problem: Token extraction & using user id**

  * **What I needed:** My backend exposes `/api/users/{id}` and I needed to call the current user’s endpoint.
  * **Solution:** I implemented a small client-side JWT parsing utility to decode the token payload (without verifying signature on client) to extract the `id` claim, then used that id to call the protected endpoint with `Authorization` header.

* **Problem: Monolithic JS became unmanageable**

  * **What happened:** My single `app.js` grew large and mixed register/login/dashboard logic.
  * **Solution:** I split JS into modules: a shared API helper, page-specific handlers, a jwt util, and a `main` bootstrap. This improved readability and maintained separation of concerns.

#### Major Bug - Login Form Not Sending POST Request & Page Reload After Successful Login

* **Login Form Not Sending POST Request**
  * **Challenge**: I encountered an issue where my login form in `index.html` was not sending a POST request to the backend's `/api/auth/login` endpoint, as observed in the browser's Network tab. Initially, I suspected a problem with the form submission or event listener attachment in `main.js`. Despite adding debug logs, I found that the form was detected on page load, but the `submit` event was not triggering the `handleLogin` function, leading to no network activity. This was frustrating because the backend was correctly configured, and a user existed in the database, but the client-side JavaScript was failing silently.
  * **Solution**: I added detailed console logs to `main.js` and `login.js` to trace the event listener and form submission flow. I discovered that the form’s `submit` event wasn’t fithuring due to a potential issue with the event listener setup or browser validation. By ensuring `event.preventDefault()` was called early in `handleLogin`, I prevented default form behavior. I also verified script paths and CORS settings, ensuring `main.js`, `login.js`, and `api.js` loaded correctly. These changes resulted in a successful POST request with a 200 response and a JWT token.

* **Page Reload After Successful Login**
  * **Challenge**: After fixing the login form, I faced a new issue where the page reloaded immediately after a successful login, preventing the redirect to `dashboard.html` or causing issues there. The console logs showed that `dashboard.js` was redirecting back to `index.html` because the JWT payload used `sub` (email) instead of the expected `id` field, triggering the `if (!payload || !payload.id)` condition. This was my mistake, as I accidentally tried to retrieve the  `id`  from the JWT (it doesn't have it) instead of the `sub` field that contatins the `username` .
  * **Solution**: I updated `dashboard.js` to use `payload.sub` instead of `payload.id`, aligning with the JWT’s structure (`{ sub: "nikos@test.com", role: "SKYDIVER", ... }`). I also switched the fetch call to `/api/jumps/all`, an authenticated endpoint that didn’t require a user ID, and used the `sub` field to display a welcome message. I added logs to confirm the token and payload were parsed correctly and tested the endpoint with Postman to ensure it returned a 200 status. This fixed the redirect loop, and the dashboard now displays ` “Welcome nikos@test.com!” ` correctly. I learned to always verify JWT payload structures and test API endpoints early to avoid frontend-backend mismatches.

---

### Reflection

* **Big-picture tradeoff I learned:** Serving frontend as static assets inside Spring Boot looks convenient early on, but it creates complex and subtle security problems. Static serving bypasses the runtime flow that APIs rely on (Authorization headers, preflight behavior, dynamic checks). For realistic apps and for learning modern full-stack patterns, separating the frontend (client) and backend (API) is the right tradeoff: it simplifies security reasoning and aligns the app with real-world deployment patterns.

* **What I did well**

  * I tested frequently: I used the H2 console, backend tests, and browser devtools to verify each change.
  * I iteratively adjusted backend and frontend until behavior matched my security model.
  * I practiced defensive coding—centralizing fetch logic, and confirming which calls should be auth-free.

* **What I would do differently next time**

  * From the start, separate the frontend and backend for development. It avoids the static-resource pitfalls entirely and makes CORS an explicit, intentional configuration step.
  * Build a small checklist before changing security configuration: confirm endpoints, check filter ordering, and test preflight responses in the browser.
  * Keep a small set of “public vs protected” endpoints documented while developing so I don’t confuse which endpoints need token attachment.

* **Security note for later**

  * For learning and development, `localStorage` is okay, but I should eventually consider HttpOnly cookies or short-lived access tokens + refresh tokens to reduce XSS exposure. I should also implement token expiration handling and graceful logout/refresh flows in the client.

---

This milestone taught me the difference between “serving files” and “serving protected content” and forced me to apply a number of practical security and architecture fixes: a robust JWT filter that skips only what’s public, correct CORS for the dev frontend, clear separation of authenticated and unauthenticated requests in the client, and a modular frontend structure that is maintainable going forward. I ended this session with working registration and login flows, a protected dashboard access pattern, and a project layout that mirrors real-world SPA + API architectures.


## M6 – Frontend UI - Styling (Auth Pages & Navbar) — Summary

### Key Achievements

* **Implemented a polished, responsive Login and Register UI using Bootstrap**

  * I added Bootstrap 5, Font Awesome, and the Inter font to the auth pages via CDN, and included the viewport meta tag so the pages behave correctly on mobile.
  * I created a shared layout pattern: a two-column grid on medium+ screens (left: illustration/hero, right: card with form) and a stacked single-column layout on small screens by using Bootstrap utilities (`col-md-*`, `d-none d-md-flex`, `w-100`, flex centering).
  * I restyled the forms using Bootstrap cards, consistent spacing (`p-4`, `mb-*`), full-width buttons (`w-100`) and Font Awesome icons for visual affordances.
  * I added a simple site-wide navbar (brand + links) that appears on every page; links are currently always visible (simple option) with a TODO to toggle visibility when authenticated.

* **Kept all changes non-invasive to existing business logic**

  * I preserved existing form IDs and event hooks so the backend integration and JS logic stayed intact.
  * I avoided introducing modals or structural changes — only styling and minimal DOM/ID adjustments so existing handlers in `main.js`, `login.js`, and `register.js` continued to work.

* **Improved theming and layout foundations**

  * I introduced CSS variables for a sky/cloud palette (`--primary`, `--primary-600`, `--muted`, `--surface`, `--text`, etc.) at the top of `style.css`, and set base typography using Inter.
  * I added layout recommendations (card max-width, centered forms, icon sizes) to ensure consistent visual rhythm and mobile-first behavior.

---

### Key Learnings & Concepts (What I learned)

* **Bootstrap responsive grid & display utilities**

  * I learned exactly how `col-md-*`, `d-none d-md-flex`, and `w-100` combine to create a two-column desktop layout and a stacked mobile layout. The left illustration is hidden on small screens by `d-none d-md-flex`, which keeps the mobile UX uncluttered.

* **Why `meta viewport` matters**

  * I confirmed adding `<meta name="viewport" content="width=device-width, initial-scale=1">` is essential so Bootstrap’s responsive rules render correctly on mobile devices.

* **CSS cascade & Bootstrap media queries**

  * I learned that overriding `.container` max-width is not a simple single-rule fix because Bootstrap defines `.container` widths inside media queries. A plain `.container.register-container { max-width: ... }` can be overridden by Bootstrap rules unless I match the same media-query specificity (or use `container-fluid`). `!important` alone didn’t help because Bootstrap’s breakpoint rules still applied.

* **Background image handling**

  * I learned how `background-size: cover` crops the image to fill the container, whereas `contain` fits the whole image inside and `background-size: 80% auto` lets me control visible area. I also learned when to switch to an `<img class="img-fluid">` for precise scaling.

* **DOM wiring and defensive JS**

  * I discovered why a missing UI placeholder (the `message` div) breaks a flow: `document.getElementById(...)` returned `null`, and trying to set `textContent` on `null` threw an exception that stopped script execution — preventing even successful redirects. I learned to either keep the placeholder in the DOM or guard JS updates with `if (element) { ... }`.

* **Minimal auth UX decisions**

  * I reviewed options for showing navbar links only when authenticated. I learned that a minimal `isAuthenticated()` helper (checking `localStorage.getItem('jwtToken')`) is sufficient for the UI toggle; however I chose the simpler path for now — always-show links and a TODO to refine authentication-aware rendering later.

---

### Challenges & Solutions (Bugs I ran into and how I fixed them)

* **Broken Register flow after redesign**

  * **Problem:** After converting the register page to Bootstrap layout, registration stopped working.
  * **Cause:** I removed the `#register-message` div and didn’t wire event binding through `main.js`. The handler attempted to update a missing `messageDiv` and crashed.
  * **Solution:** Restored a `div id="register-message"` placeholder in the card and reattached the submit handler. I opted to wire events centrally in `main.js` (`DOMContentLoaded` → attach `handleRegister` when `#register-form` exists).

* **Login flow stopped working after renaming fields**

  * **Problem:** The redesigned login used `id="username"`/`"password"` while the old JS expected `#login-username`/`#login-password`.
  * **Cause:** ID mismatch between HTML and JS selectors.
  * **Solution:** Restored the original IDs in the Bootstrap form (`login-username`, `login-password`) so existing `login.js` logic continues to work without modification.

* **Missing `message` div caused full crash (no redirect)**

  * **Problem:** Even when login/register succeeded server-side, the client didn’t redirect.
  * **Cause:** JS threw `TypeError` when trying to update `messageDiv.textContent` on `null`, aborting the function before the redirect line executed.
  * **Solution:** Ensure message placeholder exists or add defensive checks in JS (e.g., `if (messageDiv) { ... }`) so a missing element doesn’t crash the flow. I kept the placeholder for clarity and immediate feedback on failures.

* **Overriding Bootstrap `.container` width didn’t take effect**

  * **Problem:** My `.container.register-container { max-width:1200px }` didn’t change the layout.
  * **Cause:** Bootstrap sets `.container` widths inside media queries; my override lacked the same breakpoint-specific rules.
  * **Solution:** Either override with matching media queries (e.g., `@media (min-width: 1200px) { .container.register-container { max-width: 1400px; } }`) or use `container-fluid` and control padding. I chose to keep the outer `.container` for mobile friendliness and instead adjusted the image and card dimensions.

* **Image cropping & composition**

  * **Problem:** Background image was either too cropped or too small.
  * **Solution:** Experimented with `background-size: cover`, `contain`, and percentage widths (`background-size: 110% auto`) and considered embedding an `<img>` inside the column for precise control. I ultimately preferred slight zoom-in (`110%`) plus small changes to card `max-width` to balance composition while keeping responsive behavior.

* **Navbar auth toggle decision**

  * **Problem:** I needed to decide whether to show/hide links based on authentication.
  * **Solution:** For simplicity and to avoid new JS changes during styling, I hard-coded links in the navbar and left a TODO to implement an `isAuthenticated()` UI toggle later using `localStorage` and `parseJwt()` if I want to check expiry later.

---

### Reflection (Lessons learned & notes for future reference)

* Keeping DOM placeholders for dynamic feedback is a small but critical detail. If I change HTML structure, I must check for all references used by JS — IDs and “message” placeholders are contract points between markup and scripts.
* Small naming/ID discrepancies are a common source of breakage — when refactoring markup, always search the JS for selectors and keep them synchronized or centralize wiring in `main.js`.
* When overriding framework styles (Bootstrap), match the framework’s specificity and breakpoints — sometimes the correct fix is to align with the same media-query rules, not to fight them with `!important`.
* Prefer non-breaking JS: add defensive checks (`if (elem)`) before attempting DOM updates, so missing presentation elements don’t abort important app logic (like redirects).
* Maintain a “styling only” discipline for UI polish sprints: limit changes to classes, CSS, and small DOM placeholders. Avoid touching API calls or complex flows during a styling milestone.
* Keep a short TODO list in the UI for future UX improvements (auth-aware navbar, toasts, guarded messaging, small animations) so styling iterations don’t get bloated with feature work.



## M6 – Frontend UI (Dashboard & Jumps) — Reflective Summary

### Key Achievements

* **Bootstrap-first styling of Dashboard and Jumps pages**

  * I rewrote the Dashboard and the Create Jump form to use Bootstrap utilities for layout, spacing, cards, forms, buttons and tables so the pages match the look & feel of the already-styled Auth pages (Register / Login).
  * I implemented the stat cards on the Dashboard as Bootstrap `.card` elements inside the grid (`.row` / `.col-*`) so they stack on mobile and sit side-by-side on desktop.
  * I converted the jumps table to use `<table class="table table-striped table-hover align-middle">` inside `.table-responsive`, relying on Bootstrap for desktop behavior.

* **Mobile-first refinements for the jumps table**

  * I implemented a mobile-friendly card-style presentation for table rows at small breakpoints: table headers are hidden and each `<tr>` becomes a stacked card where each `<td>` shows its column label (via `data-label`) and value.
  * I added `.cell-value` spans in JS-generated table cells so the value area can be targeted reliably by CSS for wrapping/shrinking.
  * I kept the original pagination JS and IDs intact while restyling the pagination controls with Bootstrap button classes for visual consistency.

* **Action icons & layout**

  * I replaced text links with Font Awesome icons for Edit and Delete to make actions compact and visually consistent.
  * I adjusted action cell markup/classes so icons remain usable and accessible across breakpoints (e.g., `justify-content-between` / removing `d-flex` when it interfered with normal table cell behavior).

* **Refactoring CSS and trusting Bootstrap**

  * I drastically reduced the amount of hand-rolled CSS by moving layout responsibilities to Bootstrap and leaving `style.css` mainly for theme variables (colors, typography, background images).
  * I removed an overriding `.container` rule that conflicted with Bootstrap and introduced a `.page-container` wrapper while later discovering reverting to `.container` was fine after removing conflicting rules.

* **Form UI parity**

  * I re-styled the Create Jump form to match the Register form: single-card centered form using Bootstrap card + `form-control`/`form-select`, error spans with `text-danger small`, and a `btn btn-primary w-100` submit.

* **Bug fixing and debugging**

  * I found and fixed several issues: a CSS parse error caused by a missing `}` in a media query, mobile overflow caused by custom CSS overrides (resolved by locating and removing conflicting rules), alignment issues with action icons, and missing DOM placeholder `#new-jump` required by JS.
  * After isolating and removing the conflicting rules, I restored the original `.container` usage and kept the layout working on both desktop and mobile.

---

### Key Learnings & Concepts

* **Bootstrap should be the first tool for layout**

  * I learned that Bootstrap’s grid, `.table-responsive`, and default forms/cards solve most layout/spacing problems reliably. Overriding Bootstrap prematurely is a frequent source of bugs.

* **Media queries (`@media`) vs Bootstrap responsive utilities**

  * I refreshed how `@media` works (apply CSS only when a condition like `max-width` is true) and when it is appropriate to use custom CSS vs rely on Bootstrap utilities (prefer utilities for typical responsive behavior; use `@media` for custom card-style transformations).

* **Table → card mobile pattern**

  * I learned the pattern for converting tables to vertical card layouts on mobile: hide `thead`, make `tr` display `block`, use `td::before` with `data-label` (or icons) to show the column names, and ensure `.cell-value` can wrap by using `min-width: 0`, `flex` rules and `word-break` settings.

* **Flexbox quirks with table cells**

  * I learned that turning `<td>` into a `d-flex` container can break a table’s natural behavior — table cells normally stretch to the row height. Using `d-flex` created vertical alignment issues; removing it in this case solved the problem. If I do use flex inside a cell, I now know to use `h-100` and `align-items-center` and carefully test desktop table behavior.

* **Reliable wrapping requires explicit targets**

  * Wrapping behavior in flex children is subtle: anonymous text nodes don’t behave reliably, so wrapping the values in `<span class="cell-value">` was essential. `min-width: 0` on flex children is a critical trick to allow shrinking/wrapping.

* **Font Awesome integration options**

  * I explored two ways to use icons for labels on mobile:

    * CSS `::before` with Font Awesome unicode (pure CSS) — works but requires mapping unicode codes.
    * Injecting `<i>` elements via JavaScript (JS approach) — more flexible and easier to maintain given dynamic content.
  * I ultimately kept CSS-first for simplicity where possible, and used `<i>` inside action buttons.

* **Debugging technique: isolate custom CSS**

  * I learned to always check for any custom CSS overrides that could conflict with framework defaults (a few lines in `style.css` were the root cause of many headaches). Tools: use DevTools to toggle rules and temporarily outline elements to find overflow source.

* **Progressive enhancement and non-breaking JS**

  * I kept JS IDs and structure intact when changing markup/styling (e.g., pagination buttons kept their IDs) to avoid breaking behavior, demonstrating the importance of separating styling from JS contract.

---

### Challenges & Solutions (Lessons Learned / Bugs & Fixes)

* **Problem: Mobile horizontal overflow (table and page)**

  * **What I saw:** On small screens the Dashboard and Jumps pages required horizontal scrolling even with `.table-responsive`.
  * **Diagnosis:** It wasn’t data length; the same overflow occurred with no data. Investigation revealed custom CSS rules (overriding `.container` and other styles) causing the layout to exceed viewport width.
  * **Solution:** Removed conflicting custom CSS overrides (notably the `.container` override and other legacy rules). After removing those rules Bootstrap’s responsive behavior worked correctly. I briefly switched to `container-fluid` to test but ultimately returned to `.container` as intended.

* **Problem: Table row values didn’t wrap reliably**

  * **What I saw:** Values in mobile card rows didn't wrap; content overflowed.
  * **Diagnosis:** Using `td` as flex with inline text nodes meant the anonymous content wouldn’t shrink. Also `td::before` label width constrained the available space.
  * **Solution:** Wrapped values in `<span class="cell-value">` from JS, applied `flex: 1 1 0`, `min-width: 0`, and `word-break` rules in `@media` to ensure wrapping. Also adjusted label `flex` so labels can shrink when needed, and added a stacked layout for very small screens (<520px) where labels sit above values.

* **Problem: Actions column vertical gap on desktop**

  * **What I saw:** When other cells grew (wrapped text), the Action cell’s icons were top-aligned leaving a gap.
  * **Diagnosis:** Turning `<td>` into `d-flex` interfered with normal table-cell vertical sizing.
  * **Solution:** Removing `d-flex` (and otherwise allowing the cell to remain a normal table cell) immediately fixed the issue. If flex is required, `h-100` + `align-items-center` would be used, but the simplest correct approach was to keep the cell as a table cell.

* **Problem: Pagination alignment and create-jump button placement**

  * **What I saw:** Pagination controls and the Create Jump button were misaligned and caused layout issues on small screens.
  * **Diagnosis:** They were in separate DOM containers and had margins that pushed layout.
  * **Solution:** Consolidated them into a single responsive Bootstrap flex container: `d-flex flex-column flex-md-row justify-content-between align-items-center`. Kept the existing JS IDs so pagination logic stayed intact. Used Bootstrap spacing utilities (`mb-2`, `ms-2`) to manage gaps without custom CSS.

* **Problem: CSS parse error**

  * **What I saw:** Linter complained about a parse error (line 256).
  * **Diagnosis:** I had an unmatched `{` inside the `@media` block (missing closing `}`).
  * **Solution:** Added the missing `}` and re-indented the block to make brace matching obvious.

* **Problem: Missing DOM placeholder for new jump**

  * **What I saw:** Add Jump didn’t show newly created jump; JS appended to a missing container.
  * **Diagnosis:** I had removed or never included `#new-jump`.
  * **Solution:** Restored `<div id="new-jump"></div>` under the form so JS could append/display newly added jumps.

* **Problem: Over-customization and premature overrides**

  * **What I saw:** I had many custom CSS rules used while building — they later clashed with Bootstrap defaults.
  * **Lesson & Solution:** I learned to prefer Bootstrap defaults for layout and keep custom CSS minimal (theme variables, backgrounds, small overrides). I audited `style.css` and removed unnecessary or conflicting rules.

---

### Reflection

* I repeatedly ran into the same theme: **Bootstrap works reliably**, and the root cause of many UI bugs was my custom overrides. This session reinforced discipline: treat the CSS I add as a last resort — first try Bootstrap utilities and only add CSS when something cannot be achieved with Bootstrap alone.

* I learned that small changes often have outsized effects (e.g., `d-flex` on a `<td>`, or a single missing brace). Two important habits to add to my workflow:

  * Use DevTools early — toggle rules, use outlines, and inspect computed widths to find the overflow source quickly.
  * Keep my CSS minimal and modular — prefer variables and scoped overrides rather than global rules that override framework styles.

* Debugging mindset improvement:

  * When something looks like “content is too big,” test with empty data. That can reveal whether the problem is structural (layout) vs content-driven.
  * Add simple visual debugging (temporary `outline: 1px solid red`) to identify the overflowing element quickly.

* Process-wise, I learned to avoid making broad sweeping changes as “solutions” (e.g., switching to `container-fluid`) before checking for simpler fixes (removing conflicting CSS). That one small audit (finding the conflicting rules) removed hours of work.

---

### Practical Notes for Future Reference

* Keep `style.css` focused on:

  * Theme variables (`--primary`, `--muted`, `--surface`, `--text`).
  * Only essential overrides of Bootstrap (e.g., custom brand navbar tweaks, background images).
  * Table → card media query only when Bootstrap can’t handle the desired mobile UX.

* When converting tables to mobile cards:

  * Add `data-label` attributes to `<td>` and `.cell-value` spans to target values.
  * Ensure `.cell-value` uses `min-width:0` and `flex: 1 1 0` for wrapping.
  * Consider stacking label above value for very narrow devices (<520px).

* When using Font Awesome icons as labels:

  * Prefer injecting `<i>` elements via JS if dynamic mapping is needed; use CSS `::before` with unicode for purely CSS solutions.

* Keep JS contracts unchanged when changing markup styling; keep IDs stable so behavior doesn’t break.
