## Question  
Talk about 5 build targets that you use on a day-to-day basis in Maven.

### 📝 Short Explanation  
Maven uses **build lifecycle phases** (also called build targets) to automate project compilation, packaging, testing, and deployment. These phases are executed using `mvn <goal>` commands.

## ✅ Answer  

Here are 5 Maven build targets I commonly use in my day-to-day workflow:

---

### 1. `mvn clean`
- **Purpose:** Deletes the `target/` directory to ensure a clean slate before a new build.
- **When I use it:** Before any fresh build to avoid conflicts from previous build artifacts.

---

### 2. `mvn compile`
- **Purpose:** Compiles the source code in the `src/main/java` directory.
- **When I use it:** To verify that there are no compilation issues before moving to packaging.

---

### 3. `mvn test`
- **Purpose:** Runs unit tests using a testing framework like JUnit or TestNG.
- **When I use it:** Regularly during development or in CI pipelines to ensure code stability.

---

### 4. `mvn package`
- **Purpose:** Packages the compiled code into a distributable format like a `.jar` or `.war`.
- **When I use it:** When the build is stable and I need to generate an artifact.

---

### 5. `mvn install`
- **Purpose:** Installs the built artifact into the **local Maven repository** (`~/.m2/repository`) so it can be used by other local projects.
- **When I use it:** When I’m developing shared libraries or modules that are reused by other internal projects.

---

> Summary:  
> The most frequently used Maven targets in my daily work include: `clean`, `compile`, `test`, `package`, and `install`. They ensure a complete and reliable build pipeline from development to artifact distribution.

---

The 5 core build targets used across almost all Gradle projects are:

---

### 1. build
- **Purpose:** Performs a complete project assembly and validation.
- **Action:** Compiles production code, processes resources, runs all unit tests, and packages the final binaries (such as a JAR, WAR, or APK) into the build directory.

---

### 2. assemble
- **Purpose:** Compiles and packages artifacts without running verification tests.
- **Action:** Speeds up development cycles by skipping the test suite. It focuses purely on generating the main outputs like executables or libraries.

---

### 3. clean
- **Purpose:** Deletes the local build outputs to reset the environment.
- **Action:** Erases the entire build directory. This removes all previously compiled class files, cached data, and generated artifacts to guarantee that the next run is a completely fresh build.

---

### 4. check
- **Purpose:** Runs all quality assurance and verification tasks.
- **Action:** Executes every unit test, code coverage analysis, and linting tool (such as SpotBugs, PMD, or Checkstyle) configured in the project. It ensures the code meets safety and quality standards before deployment.

---

### 5. publish
- **Purpose:** Distributes the finalized build artifacts to external environments.
- **Action:** Uploads the compiled packages and metadata files (like Maven POMs or Gradle Module Metadata) to a specified local or remote repository, such as Maven Central or a private Nexus instance.

---
