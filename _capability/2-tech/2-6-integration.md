---
title: "Integration"
section: 2-tech
---

Building [simpler, clearer, faster public services](http://www.dto.gov.au) means reusing what's out there, working with others, and sharing what you've done.

Integration is the exercise of combining work performed by the team and others into a cohesive product that solves a user need.


>"Continuous Integration is a software development practice where members of a
>team integrate their work frequently, usually each person integrates at least daily
>- leading to multiple integrations per day."
>
>
>"When to use iterative development? You should use iterative development only
>on projects that you want to succeed."
>
>-- Martin Fowler

# Level 0

The difficulty of incorporating freely available technology into your solutions means they aren't used, and users don't receive the experience they've come to expect from other online providers.


### Indications that you're operating at level 0
 - The only integration checks are performed by your IDE or development environment. Your solution compiles and runs, but often crashes in peculiar ways because dependencies aren't met, or configurations weren't correct.
 - Each team member is responsible for configuring their own development environment. They find and download dependencies, trying different versions until something works. When code is merged from other team members or projects, developers struggle through [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).
 - The project is often in a broken state, requiring several hours or days of effort to get the entire system compiling and running again.

### Working towards level 1
 - Explore and start using automated build tools, which will help ensure your team are building the project the same way. There are plenty of great free and open source ones out there if your development environment didn't come with any.
 - Share the required dependencies with the team by putting them in your version control repository, this will ensure your team are all using the correct versions.
 - Work on integrating new work more frequently - the longer you wait, the more things will diverge and it will be more difficult to pull them back together.


# Level 1

The project has some automated build processes defined which the team use to configure and run the builds, but builds are blindly run at the same time each night. Team members need to wait until the next day to find out if everything worked.

### Indications that you're operating at level 1

- The team all use the same automated build scripts that perform the integration and compilation process, which helps ensure that the product is consistent, repeatable and predictable.
- Dependencies are centrally and authoritatively stored within the version control repository. When a dependency is updated, it is pushed to the entire team next time they update their working directory.

### Working towards level 2
- Use a dedicated environment for performing your automated builds, preferably a cloud environment. If you have restrictions about using external cloud services, set up a virtual environment inside your organisation instead.
- Learn about some [workflows](https://guides.github.com/introduction/flow/) that will help to keep the build compiling and working properly. If something goes wrong and the build breaks, getting it working again is _everybody's_ top priority.


# Level 2

Keeping your product up to date with the latest dependencies and trends helps your users get the experience they have come to expect from the rest of their service providers.

### Indications that you're operating at level 2

- Dependencies are managed with a dependency management tool, which will fetch and update dependencies for you.
- All team members follow a consistent workflow, which ensures they are iteratively integrating with each other and getting the project building quickly.
- Integration is performed by a dedicated integration server which watches for changes to the repository, 'complies' the product and runs all the tests
- Metrics are available to the team about how successful the integration has been and how the project is trending overall, which should be positive as the build should never be broken.
