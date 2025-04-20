# Java Maven Jenkins Pipeline

## 📌 Overview

This project demonstrates a basic Java application built and packaged using **Apache Maven** and integrated with **Jenkins** for Continuous Integration (CI). It is part of a DevOps internship task focused on understanding the fundamentals of CI/CD pipelines using open-source tools.

---

## 🧰 Technologies Used

- **Java (JDK 8)**
- **Apache Maven**
- **Jenkins (via Docker)**
- **Git & GitHub**

---

## 📁 Project Structure

ava-maven-jenkins-pipeline/ 
├── src/ │
└── main/ │ 
└── java/ │ 
└── HelloWorld.java
├── pom.xml
└── jenkins console output.png

---

## 📝 Source Code

### HelloWorld.java

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}


🚀  POM. XML

<project>
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>hello</artifactId>
    <version>1.0</version>
    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>

🚀 Jenkins Setup & Job Configuration

1. Run Jenkins (Docker-based):

docker run -p 8080:8080 jenkins/jenkins:lts

2. Configure Global Tools:

Add JDK 8

 Add Maven (e.g., Maven 3.8.6)

3. Create a Freestyle Project:

Source Code Management: Git (use this repository URL)

Build Step: Invoke top-level Maven targets

Goals: clean package

4. Build & Verify:

Run the job manually

Observe console output

Confirm BUILD SUCCESS


✅ Outcome
By completing this task, I gained hands-on experience with:

Creating Jenkins freestyle jobs

Using Maven to build Java applications

Configuring CI pipelines

Debugging Jenkins builds via console output



