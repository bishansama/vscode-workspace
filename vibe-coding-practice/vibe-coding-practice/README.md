# Vibe Coding Practice

This is a simple Spring Boot application that demonstrates a basic setup with a REST controller.

## Project Structure

```
vibe-coding-practice
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── example
│   │   │           └── vibecodingpractice
│   │   │               ├── VibeCodingPracticeApplication.java
│   │   │               └── controller
│   │   │                   └── HelloController.java
│   │   └── resources
│   │       └── application.properties
│   └── test
│       └── java
│           └── com
│               └── example
│                   └── vibecodingpractice
│                       └── VibeCodingPracticeApplicationTests.java
├── pom.xml
└── README.md
```

## Running the Application

1. Ensure you have Java and Maven installed on your machine.
2. Navigate to the project directory.
3. Run the following command to start the application:

   ```
   mvn spring-boot:run
   ```

4. Once the application is running, you can access the "Hello World" message by navigating to:

   ```
   http://localhost:8080/hello
   ```

## Dependencies

This project uses Spring Boot and its dependencies defined in the `pom.xml` file. Make sure to check the `pom.xml` for any additional dependencies that may be required.

## Testing

You can run the tests using the following command:

```
mvn test
```

This will execute the test cases defined in the `VibeCodingPracticeApplicationTests.java` file to ensure that the application context loads correctly.

## Java 21 Upgrade

This project has been updated to target Java 21. Before building, install JDK 21 and Maven locally. See `UPGRADE-JAVA-21.md` for detailed instructions.