Upgrade checklist to Java 21

This repository: /Users/shreyapaul/workspace/vscode-workspace/vibe-coding-practice/vibe-coding-practice

Summary of what I changed for you:
- Updated `<parent>` to Spring Boot Starter Parent 3.2.12 in `pom.xml`.
- Bumped `<java.version>` to 21 in `pom.xml`.
- Added `maven-compiler-plugin` with `<release>21</release>`.

Manual steps for you to complete (macOS, zsh):

1. Install JDK 21 (Adoptium/Eclipse Temurin recommended)
   - Using Homebrew:
     brew install temurin21
   - Or download from https://adoptium.net and install the pkg.

2. Verify Java 21 is the active JDK:

   java -version
   # Expect output containing "21"

3. Install Maven (if not installed):

   brew install maven

4. Verify Maven/Java:

   mvn -v
   # Ensure Maven reports Java 21 in the output

5. Build the project:

   cd /Users/shreyapaul/workspace/vscode-workspace/vibe-coding-practice/vibe-coding-practice
   mvn clean package

6. Fix compilation issues:
   - If there are compilation errors, update source code to avoid removed/changed APIs.
   - See notes below for Spring Boot compatibility.

Notes and compatibility:
- Spring Boot 3.2.x requires Jakarta EE 10 and Java 17+. You're moving to Spring Boot 3.2.12 which supports Java 21.
- Verify any third-party dependencies for compatibility with Spring Boot 3.2 and Java 21.

If you want, I can also:
- Try to detect and fix any code incompatibilities automatically (requires running mvn in this environment).
- Update README or CI configs to use Java 21.

Status: edits to pom.xml applied. Please run the steps above locally (installing JDK/Maven) and paste failing mvn output here if you want me to iterate on fixes.
