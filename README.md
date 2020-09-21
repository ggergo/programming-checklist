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

- [ ] **S**RP is being followed (Single Responsibility Principle) A **class has** one and only **one reason to change**, meaning that a class has only one job.

- [ ] **O**CP is being followed (Open/Closed Principle) A software entity must be easily **extensible** with new features **without modifing existing code**.

- [ ] **L**SP is being followed (Liskov Substitution Principle) **Objects are replaceable by** instances of **their subtypes** without altering the correct functioning of our system.

- [ ] **I**SP is being followed (Interface Segregation Principle) **Interfaces belong to their clients** and not to the implementations. No client should be forced to depend on methods it does not use. Always **implement** atomic interfaces called **Role interfaces** to guarantee one specific related behavior by them. **In case of a third-party class create an AdapterClass and implement a new streamlined Interface** (or multiple Role interfaces)... **or** ... **create a Facade** by not Injecting the third party code rather creating a new instance in its constructor **and** also **implement a new streamlined Interface** (or multiple Role interfaces).

- [ ] **D**IP is being followed (Dependency Inversion Principle) **Depend on Interfaces** not concrete implementations.

- [ ] Not implementing interfaces by classes unique to the application: which has a state about the app (i.e. Entity) or has no reason to change (i.e. business logic, calculation)
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
