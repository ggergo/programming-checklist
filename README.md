# Programming checklist
A checklist to fill out every time making a pull request
<br>
<br>

- [ ] The code is following a Coding Standard

- [ ] The code is linted
<br>

- [ ] Code is not Overengineered

- [ ] DRY principle is being followed (Do not Repeat Yourself)

- [ ] Guard Clauses are being used (Using a fast return when have something to assert in the beginning of a method)

- [ ] **S**RP is being followed (Single Responsibility Principle) Software entities have a single responsibility / function and that is entirely encapsulated.

- [ ] **O**CP is being followed (Open/Closed Principle) Software entities should be open for extension, but closed for modification.

- [ ] **L**SP is being followed (Liskov Substitution Principle) Child classes should never break the parent class' type definitions.

- [ ] **I**SP is being followed (Interface Segregation Principle) Interfaces belong to their clients and not to the implementations. No client should be forced to depend on methods it does not use. Create a new streamlined interface for the client and an AdapterClass which implements it and stores the implementation of the dependency which implements the heavy external interface.

- [ ] **D**IP is being followed (Dependency Inversion Principle) Depend on Interfaces not concrete implementations.
<br>

- [ ] Code is self-documenting. All variables, methods and classes have self explaining names and describing complete functionality.
- [ ] Strange choices and Complicated things are explained in comment.
<br>

- [ ] Constructors are only containing:
* assignments
* condition checks
* public method calls or simple implementation details
<br>

Controller Action
* [ ] only wires things up and only does following stuff:
  * handles a request and creates a response
  * creates forms as services, handles the form but does not check the handled form states
  * binds parameters for services i.e request parameters or i.e handled form or i.e a handled forms states
  * gets and sets session objects
  * redirects
 * ‘s Business Logic (BL)
   * [ ] is in a separate BL class method
   * [ ] ‘s method contains only the BL
   * [ ] is unittested
<br>

- [ ] All important scenarios are being tested
* - [ ] Exceptions are being tested (when a situation is expected to happen but has no sense)

- [ ] If it was a bug fix a test was written for the bug

All Unit Tests
- [ ] are testing only the subject of the test, and not mocking the subject
- [ ] are testing only the behaviour and not the implementation
- [ ] pass one last time
