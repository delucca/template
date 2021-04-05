# Writting tests for <repository-name>

* [What is a test](#what-is-a-test)
* [Types of tests we use](#types-of-tests-we-use)
  * [Acceptance tests](#acceptance-tests)
  * [Unit tests](#unit-tests)
  * [Mutation tests](#mutation-tests)
* [Best practices](#best-practices)
  * [General best practices](#general-best-practices)
  * [Acceptance tests best practices](#acceptance-tests-best-practices)
  * [Unit tests best practices](#unit-tests-best-practices)

## What is a test

An test aims to make it easier to identify if our system is solving all functional and non-functional requirements. Keep in mind that your tests could be either **automated** or **not**, but you should always document them.

A non-automated test is not common, but it is a good way to start, specially if you're a new member to our project. Like an automated test, you can write them down and perform them manually when you want.

Our project has all the required structure to execute automated tests, and we encourage all contributors to write sa many as they can, but never forgetting [general best practices](#general-best-practices) while writting tests.

## Types of tests we use

### Acceptance tests

Those tests are reponsible for ensuring that a given requirement is met. They can focus on a single unit, or in the entire system, but acceptance tests always check if a given business requirement is met.

As a pattern, we suggest using [BDD][bdd-explanation] while writting acceptance tests.

Learn how to write acceptance tests [in our best practices section](#acceptance-tests-best-practices)

### Unit tests

An unit test isolate a given module and test if a given scenario in met on that module. Oposing to acceptance tests, the units tests typically focus on the **absense of a problem** instead of the presence of a feature.

Learn how to write unit tests [in our best practices section](#unit-tests-best-practices)

### Mutation tests

In this type of tests, mutations are inserted into our code, and we test if our current test coverage is being able to catch those mutations. We use this type of test to ensure that our tests are stable enought to prevent unwanted issues.

## Best practices

### General best practices

As a general rule, your tests should avoid testing implementation. While writting tests, keep in mind that your idea is to test the outcome, without having to create a dense couple between your test and the original code.

Mocking and other test tricks are oftern a good idea if they're isolated (like mocking a database, for example). Mocking an entire service, or a given business logic, usually damage the test coverage and allow unwanted behavior.

### Acceptance tests best practices

We suggest writting acceptance tests scenario as a part of the requirements definition, before coding. You can write those [in Gherkin][gherkin-reference] and attach your designed scenarios in the issue you're currently working on.

Try to keep your scenarios generic, since you should reuse as much steps as you can. Also, you should keep as close as spoken language, since it makes easier to evaluate the coverage of a given requirement.

### Unit tests best practices

While writting unit tests you should avoid duplicanting an concurring with acceptance tests. The main idea of unit tests is to prevent not wanted scenarios. Instead of writting `it should create an user`, your tests should be like `it should not create an user without an e-mail`. This may seem like a small difference, but it has a huge impact in our test structure and reliability.

[bdd-explanation]: https://cucumber.io/docs/bdd/
[gherkin-reference]: https://cucumber.io/docs/gherkin/reference/