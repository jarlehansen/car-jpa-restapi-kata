# Car REST API Kata

The following is a TDD Kata, an exercise in using the Spring test utilities for JPA and REST.

## Before you start
* Try not to read ahead.
* Do one task at a time. The trick is to learn to work incrementally.
* Make sure you only test for correct inputs. There is no need to test for invalid inputs for this kata.

## The kata

### Step 1: JPA / database integration
Create a repository containing this functionality:
* Get all persisted cars
* Get car by license number
* Persist a new car

The car entity should contain the following information:
* License number
* Make
* Model
* Year

Use the embedded H2 instance and the `src/test/resources/data.sql` as basis for the tests.

### Step 2: REST API
Create a controller that uses the repository created in the previous step.  
Remember to create proper REST API, where the exposed value is the car resource and using the HTTP verbs.

The tests should call the REST endpoints and not just the methods.  
Use the `MockMvc` support in Spring.