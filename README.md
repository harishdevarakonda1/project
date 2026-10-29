# MAVEN LAB INTERNAL – COMPLETE PROCEDURE

## AIM
To create, compile, test, package, and install a simple Java application using Apache Maven.

## 1. INTRODUCTION TO MAVEN

Maven is a build automation and project management tool used for Java projects. It helps to compile code, manage dependencies, run tests, and package applications.

### Advantages of Maven
1. It simplifies Java project management.
2. It downloads required libraries automatically.
3. It compiles Java programs.
4. It runs test cases.
5. It creates JAR files.

### Important Terms
- **JDK:** Java Development Kit used to compile and run Java programs.
- **Maven:** A tool used to build and manage Java projects.
- **pom.xml:** The configuration file containing project information and dependencies.
- **Dependency:** An external library required by a project.
- **JAR:** Java Archive file used to package Java classes and resources.

---

# METHOD 1: EXECUTION USING COMMAND PROMPT (CMD)

## Step 1: Check Java Installation

Open Command Prompt and execute:

```bash
java -version
```

This command displays the installed Java version.

## Step 2: Check Maven Installation

Execute:

```bash
mvn -version
```

This command displays the installed Maven version.

If both commands work, continue to the next step.

## Step 3: Create a Maven Project

Execute the following command in Command Prompt:

```bash
mvn archetype:generate "-DgroupId=com.example" "-DartifactId=MavenDemo" "-DarchetypeArtifactId=maven-archetype-quickstart" "-DinteractiveMode=false"
```

This command creates a Maven project named `MavenDemo`.

## Step 4: Open the Project Directory

```bash
cd MavenDemo
```

This command moves into the project directory.

## Step 5: Understand the Project Structure

The project structure is:

```text
MavenDemo
│
├── pom.xml
│
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── example
│   │               └── App.java
│   │
│   └── test
│       └── java
│
└── target
```

- `pom.xml` – Maven configuration file.
- `App.java` – Main Java program.
- `src/test` – Contains test programs.
- `target` – Contains compiled files and packaged output.

## Step 6: Write the Java Program

Open `src/main/java/com/example/App.java` and write:

```java
package com.example;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello Maven");
    }
}
```

Save the file.

## Step 7: Compile the Program

Execute:

```bash
mvn compile
```

This command compiles the Java source code.

## Step 8: Run the Program

Execute:

```bash
java -cp target/classes com.example.App
```

Output:

```text
Hello Maven
```

## Step 9: Test the Project

Execute:

```bash
mvn test
```

This command runs the test cases in the project.

## Step 10: Package the Project

Execute:

```bash
mvn package
```

This command builds the project and creates a JAR file inside the `target` directory.

## Step 11: Install the Project

Execute:

```bash
mvn install
```

This command installs the packaged artifact into the local Maven repository.

---

# METHOD 2: EXECUTION USING VISUAL STUDIO CODE (VS CODE)

## Step 1: Install the Required Software

Install the following software:

1. Java Development Kit (JDK).
2. Apache Maven.
3. Visual Studio Code.

## Step 2: Install the Java Extension

1. Open VS Code.
2. Press `Ctrl + Shift + X`.
3. Search for **Extension Pack for Java**.
4. Click Install.

This extension provides Java language support in VS Code.

## Step 3: Open the VS Code Terminal

1. Open VS Code.
2. Click **Terminal → New Terminal**.
3. Execute the following commands one by one.

Check Java:

```bash
java -version
```

Check Maven:

```bash
mvn -version
```

If both commands display version information, continue.

## Step 4: Create the Maven Project

In the VS Code terminal, execute:

```bash
mvn archetype:generate "-DgroupId=com.example" "-DartifactId=MavenDemo" "-DarchetypeArtifactId=maven-archetype-quickstart" "-DinteractiveMode=false"
```

Wait until Maven finishes creating the project.

## Step 5: Open the Project in VS Code

Execute:

```bash
cd MavenDemo
```

Then execute:

```bash
code .
```

Alternatively, select **File → Open Folder** and open the `MavenDemo` folder.

## Step 6: Open App.java

In the Explorer panel, navigate to:

`src → main → java → com → example → App.java`

Replace the existing code with:

```java
package com.example;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello Maven");
    }
}
```

Save the file using `Ctrl + S`.

## Step 7: Compile the Program

Open the terminal and execute:

```bash
mvn compile
```

Maven compiles the program and creates the required class files.

## Step 8: Run the Program

Execute:

```bash
java -cp target/classes com.example.App
```

Output:

```text
Hello Maven
```

## Step 9: Test the Project

Execute:

```bash
mvn test
```

This command executes the project's test cases.

## Step 10: Package the Project

Execute:

```bash
mvn package
```

The generated JAR file will be available inside the `target` folder.

## Step 11: Install the Project

Execute:

```bash
mvn install
```

This command installs the project artifact in the local Maven repository.

---

# IMPORTANT MAVEN COMMANDS

| Command | Purpose |
|---|---|
| `mvn compile` | Compiles the source code |
| `mvn test` | Executes test cases |
| `mvn package` | Packages the project into a JAR file |
| `mvn install` | Installs the artifact in the local repository |
| `mvn clean` | Removes generated build files |
| `mvn deploy` | Publishes the artifact to a configured remote repository |

### Easy Way to Remember

**Compile → Test → Package → Install → Deploy**

The `clean` command removes generated build files and can be executed whenever required.

---

# VIVA QUESTIONS AND ANSWERS

**1. What is Maven?**

Maven is a build automation and project management tool for Java applications.

**2. What is pom.xml?**

It is the Project Object Model file used to configure a Maven project.

**3. What is a dependency?**

A dependency is an external library required by a project.

**4. What is the purpose of mvn compile?**

It compiles the Java source code.

**5. What is the purpose of mvn test?**

It executes the project's test cases.

**6. What is the purpose of mvn package?**

It builds the project and packages the output, usually into a JAR file.

**7. What is the purpose of mvn install?**

It installs the project artifact in the local Maven repository.

**8. What is a JAR file?**

JAR stands for Java Archive. It packages Java classes and resources into one file.

**9. What is the purpose of mvn clean?**

It removes generated build files, usually from the `target` directory.

**10. What is the output of the program?**

```text
Hello Maven
```

---

# RESULT

Thus, a simple Java application was created, compiled, tested, packaged, and installed successfully using Apache Maven through Command Prompt and Visual Studio Code.
