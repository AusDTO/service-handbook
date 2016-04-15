---
title: "Quality"
section: 6-quality
index: true
---

Good quality is difficult to define and achieve, but bad quality is easy to spot and painful for your users to experience.

By spending a little extra time to build quality in as you go, you'll save a lot of time later on when you're under pressure to make changes.

>"Program testing can be a very effective way to show the presence of bugs,
>but is hopelessly inadequate for showing their absence."
>
> -- Edsger Dijkstra
>
>
>"Sometimes things fall apart so that better things can fall together"
>
> -- Marilyn Monroe


# Level 0

When you're working to a tight deadline, every second counts and building in quality has lower priority. Promises are made to do better next time, but nobody really believes that you will.

### Indications that you're operating at level 0

- The majority of the testing is performed manually, following a prescribed test list. Attempts have been made to record and replay manual testing to increase test coverage, but the system changes too often for recording to be reliable.
- Although the testing process doesn't identify any defects, users routinely discover simple but critical issues that prevent them from using the system.
- There are some bugs that have been around for so long that the team recognise them by name and dismiss them with "Oh, that's just the usual exception".
- For no reason, tests that previously work start to fail, or tests that previously fail start to work. Your advice to users is "Try again, it usually works the second time".
- If the project has any automated quality checks, they are only run when developers remember they exist. Before the checks will even run, developers spend a long time trying to get them to compile before commenting out the difficult ones in frustration.


### Working towards level 1

- Implement automated testing - it's never too late to start, and every test helps. Not all automated tests need to be unit tests, find the features of your system that are causing the most user disruption and automate acceptance or system testing for them. There are plenty of great free and open source automated testing tools out there if your development environment didn't come with any.
- Start reading up on some automated testing strategies that will ensure your tests are accurately reflecting what's happening in your system - [Eradicating Non-Determinism in Tests](http://martinfowler.com/articles/nonDeterminism.html)
- When a bug is identified, write a test that recreates the problem. This strategy will start to build a regression suite of tests that will ensure that bugs don't come back - [Getting to zero exceptions](http://yellerapp.com/posts/2015-06-01-getting-to-exception-zero.html)
- Run the tests! - There is no point in having automated tests if they aren't run religiously.

# Level 1

Automation of testing has given the team the confidence to experiment with new ways of developing features. Some areas of the product are difficult to test accurately or take too long to be run regularly, so are often skipped.

### Indications that you're operating at level 1

- The project is built following [Test Driven Development](http://www.jamesshore.com/Agile-Book/test_driven_development.html), and tests are run religiously throughout the development process, including on committing to the version control repository.
- There are several hard-coded integration tests, which rely on precise configurations of databases or responses from services.
- Techniques such as [MVC](https://developer.chrome.com/apps/app_frameworks) /  [MVVM](https://www.objc.io/issues/13-architecture/mvvm/) are used to decouple the business logic behind views from the presentation of views, allowing the logic to be automatically tested.
- Whenever a defect is identified, an automated test is written to verify it's existence, and when the defect is fixed, the automated test ensures it never happens again.
- Tests are regularly run and often triggered by a development activity, such as modifying a source file or getting the latest code from the repository.


### Working towards level 2

- Start looking into techniques such as mocking and dependency injection, to test aspects of the system that depend on external input such as databases, time of day, and other systems.
- Explore alternative testing techniques, such as [Behaviour Driven Development](https://dannorth.net/introducing-bdd/), to complement your approach to automated testing. Try to keep in mind that there is no _one_ correct way to test, and that your approach should be developed based on your user needs.

# Level 2

The team have developed the confidence to experiment and innovate to help deliver the user needs simpler, clearer and faster. Code is continually refactored to remove technical debt, greatly accelerating the rate of delivering new features.

### Indications that you're operating at level 2

- Code analysis tools are used to identify code coverage which is near 80% to 90% of the code base, with particularly complex sections of the code having multiple tests to ensure the edge cases work. Code coverage metrics identify areas of the code which aren't tested enough, not that you've finished testing.
- Automated integration and acceptance testing tools are used to ensure that the overarching system works as expected.
- Dependency injection and mocking frameworks are used to isolate the components being tested from the rest of the system, allowing the components to be tested for a variety of circumstances independently of the dependencies, such as databases and time dependent actions like reminders.
