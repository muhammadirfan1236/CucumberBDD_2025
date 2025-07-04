#  Cucumber BDD Framework

## What is Cucumber?

Cucumber is an open-source software testing tool that supports **Behavior-Driven Development (BDD)**. It enables writing test scenarios in a natural, human-readable language called **Gherkin**.
Cucumber supports various programming languages including:

* Java
* JavaScript
* Ruby
* Python

✅ **Free to use** and integrates easily with automation tools like **Selenium**.

---

## 📘 What is BDD?

**Behavior-Driven Development (BDD)** is an agile software development practice that encourages collaboration between developers, testers, and business stakeholders.

Key characteristics:

* Test cases are written in **plain English** (Gherkin syntax)
* Focus is on **behavior** of the application, not internal code
* Improves **communication** and shared understanding between technical and non-technical teams

---

## ✍️ What is Gherkin?

**Gherkin** is the domain-specific language used in Cucumber to write feature files.
It is simple, structured, and **readable by both humans and machines**.

### 🔑 Gherkin Keywords:

| Keyword    | Description                                 |
| ---------- | ------------------------------------------- |
| `Feature`  | Describes the overall feature under test    |
| `Scenario` | Defines a specific test case                |
| `Given`    | Specifies preconditions                     |
| `When`     | Describes the action/event                  |
| `And`      | Connects multiple actions or conditions     |
| `Then`     | Describes expected outcome or result        |
| `But`      | Represents negative or alternate conditions |

Example:

```gherkin
Feature: Login functionality

  Scenario: Successful login
    Given user is on the login page
    When user enters valid credentials
    Then user should be redirected to the dashboard
```

---

## 🔁 What are Hooks?

**Hooks** in Cucumber allow you to run code **before or after** scenarios or steps. They are commonly used for **setup and teardown** operations.

### Types of Hooks:

* **Scenario Hooks:**

  * `@Before` – Runs before each scenario
  * `@After` – Runs after each scenario
* **Step Hooks:**

  * `@BeforeStep` – Runs before every step
  * `@AfterStep` – Runs after every step

Hooks help in tasks like:

* Opening/closing browser
* Initializing test data
* Taking screenshots on failure

---

## 🏷️ What are Tags?

**Tags** help organize and control the execution of scenarios. You can assign tags at the:

* Feature level
* Scenario level
* Scenario Outline / Examples level

### Example:

```gherkin
@smoke @login
Scenario: Login with valid credentials
```

### Logical Operations:

* `@smoke and @regression`
* `@smoke or @regression`
* `not @wip` (exclude tests)

Tags function similarly to groups in TestNG.

---

## ⚙️ Installation

Add the following dependencies to your `pom.xml` (Maven project):

### 🧪 Selenium Dependency:

```xml
<dependency>
  <groupId>org.seleniumhq.selenium</groupId>
  <artifactId>selenium-java</artifactId>
  <version>3.141.59</version>
</dependency>
```

### 🥒 Cucumber Dependencies:

```xml
<dependency>
  <groupId>io.cucumber</groupId>
  <artifactId>cucumber-java</artifactId>
  <version>4.2.2</version>
</dependency>

<dependency>
  <groupId>io.cucumber</groupId>
  <artifactId>cucumber-testng</artifactId>
  <version>4.2.2</version>
</dependency>
```


