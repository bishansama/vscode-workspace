Upgrade to Spring Boot 3.5
=================================

What I changed
---------------
- Updated the parent in `pom.xml` from Spring Boot `3.2.12` to `3.5.0`.

Why I couldn't finish the automated steps here
------------------------------------------------
- The automated GitHub Copilot app modernization tools are not available in this environment (requires a Pro/Business plan).
- The environment used to run commands in this session does not have `mvn` (Maven) installed, so I couldn't run a build/tests to validate the upgrade.

What you should run locally (macOS / zsh)
-----------------------------------------
If you have Homebrew:

```bash
# Install Maven if missing
brew install maven

# From the project root
cd /path/to/vibe-coding-practice/vibe-coding-practice

# Run a full build and tests (recommended)
mvn -U clean test

# Or to just compile without tests
mvn -U -DskipTests clean package
```

If you prefer a Maven wrapper (recommended for reproducible builds):

1. On a machine with Maven installed, run:

```bash
mvn -N io.takari:maven:wrapper
```

2. Commit the generated `mvnw`, `mvnw.cmd`, and `.mvn/wrapper/*` files to the repo.

Compatibility and follow-ups to check
-------------------------------------
- Check for dependency version conflicts. Spring Boot 3.5 will bring newer transitive versions.
- Run your unit/integration tests and fix any compilation or API changes (rare for simple apps, but possible with libraries you use).
- Review `spring.factories` or other deprecated extension points if present.
- If you use Spring Security, Jackson, or other libraries with breaking changes, consult their migration guides.

Suggested next steps (manual)
----------------------------
1. Install Maven or generate a Maven wrapper and run the build/tests locally.
2. Resolve any compile/test failures; update code or adjust dependency versions.
3. Run integration tests and smoke tests.
4. Commit changes and push; consider opening a CI job that runs `mvn -U -DskipTests=false test`.

If you want, I can:
- Help fix any compilation or test failures you paste here.
- Create and apply OpenRewrite recipes if you provide access to automated tooling or run the wrapper locally and share build failures.

Status of automated steps performed by me
----------------------------------------
- Automated planner: attempted but unavailable (requires Copilot Pro plan).
- Manual pom update: completed (parent version set to 3.5.0).

Contact
-------
If you'd like me to continue, run the build locally and paste the output/errors here; I will propose and apply exact code fixes.
