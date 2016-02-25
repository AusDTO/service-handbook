---
title: "Integration"
section: 8-integration
index: true
---
Integration combines work performed by the team into a cohesive product that functions as expected.


>"Continuous Integration is a software development practice where members of a
>team integrate their work frequently, usually each person integrates at least daily
>- leading to multiple integrations per day."
>
>
>"When to use iterative development? You should use iterative development only
>on projects that you want to succeed."
>
>-- Martin Fowler


### Level 0
 - The only integration checks are performed by IDE or development environment, which identifies static 'compilation' miss-matches
 - At runtime, products crash in peculiar ways that don't occur during development
 - Each developer is responsible for setting up their own development environment, and obtaining any dependencies
 - Tests are only run when the developers remember them
 - The project is often in a broken state

### Level 1
 - Automated build scripts perform the integration, compilation and test processes
 - Dependencies are centrally and authoritatively stored within the version control repository
 - Tests are regularly run and often triggered by a development activity, such as modifying a source file or getting the latest code from the repository
 - The project routinely builds successfully, but the output depends on the setup of the developer's environment

### Level 2
 - Integration is performed by a dedicated CI server which watches for changes to the repository, then: fetches the latest code from the repository, manages dependencies, 'complies' the product and runs all the tests
 - Metrics are available to the team about how successful the integration has been and how the project is trending overall, which should be positive as the build should never be broken
 - The project's dependencies are specified in configuration files, which are fetched by a dependency management tool
