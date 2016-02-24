---
title: "Quality"
section: 6-quality
index: true
---

Testing ensures that:
 -  the users needs are met
 - the system operates as expected
 - bugs that are fixed don't come back

>"Program testing can be a very effective way to show the presence of bugs,
>but is hopelessly inadequate for showing their absence."
>
> -- Edsger Dijkstra
>
>
>"Sometimes things fall apart so that better things can fall together"
>
> -- Marilyn Monroe


Resources:

 - [Getting to Zero Exceptions](http://yellerapp.com/posts/2015-06-01-getting-to-exception-zero.html)
 - [Eradicating Non-Determinism in Tests](http://martinfowler.com/articles/nonDeterminism.html)

### Level 0
  - Automation products are used to record / describe the tests, which can be run on demand
  - Users report more bugs then the testing process
  - The team recognise false-positives by name, and dismiss them with "Oh, that's just the usual exception"
  - For no reason, tests that previously work start to fail, or tests that previously fail start to work


### Level 1
 - The project is built following TDD, and tests are run religiously throughout the development process, including on committing to the version control repository
 - There are several hard-coded integration tests, which rely on precise configurations of databases or responses from services.
 - Techniques such as MVC /  MVVM are used to decouple the business logic behind views from the presentation of views, allowing the logic to be 'headless' tested.
 - Whenever a defect is identified, an automated test is written to verify it's existence, and when the defect is fixed, the automated test ensures it never happens again


### Level 2
 - Code analysis tools are used to identify code coverage, which is 100% for the majority the code base
 - Automated integration and acceptance testing tools are used to ensure that the overarching system works as expected
 -  Dependency injection and mocking frameworks are used to isolate the components under-test from the rest of the system, allowing the components to be tested for a variety of circumstances independently of the dependencies, such as a database.
 - The team have a 'zero exceptions in production' mantra.
