# Car REST API Kata

The following is a TDD Kata, an exercise in using the Spring test utilities for JPA and REST.

## Before you start
* Try not to read ahead.
* Do one task at a time. The trick is to learn to work incrementally.
* Make sure you only test for correct inputs. There is no need to test for invalid inputs for this kata.

## The kata

This exercise is created to use TDD with integration tests using a database and a REST API.  
It is also useful to get familar with the [Spring test features](https://spring.io/blog/2016/04/15/testing-improvements-in-spring-boot-1-4).

### Step 1 (JPA / db): Get all cars from the database
Use the embedded H2 instance and the `src/test/resources/data.sql` as basis for the tests.
* Create a repository that makes it possible to return all persisted cars.

The car entity should contain the following information:
* License number
* Make
* Model
* Year

### Step 2 (JPA / db): Get a single car by license number
* Get a specific car by sending in a license number. If no car is present, null should be returned.

### Step 3 (JPA / db): Persist a new car
* Persist a new car in the database. After persisting the car make sure the new value is present in the database.

### Step 4 (REST API): Get all cars
We shall now expose the functionality created with the repository as a REST API.
Remember to create proper REST API, where the exposed value is the car resource and using the HTTP verbs.

The tests should call the REST endpoints and not just the methods:
* Use JSON as the content-type.    
* Use the `MockMvc` support in Spring.

* Get all cars by using the repository.

### Step 5 (REST API): Get a car by license number
* Get a single car by using the license number. If no car is present return `404 - Not Found`.

### Step 6 (REST API): Post a new car
* Post a new car. The car entity should be serialized as JSON in the request body. Return `401 - Created` with the `Location` header set.
