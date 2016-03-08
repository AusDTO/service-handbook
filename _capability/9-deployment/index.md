---
title: "Deployment"
section: 9-deployment
index: true
---

Deployment is the process of releasing new features to the users, which should be quick, simple and bullet-proof.

>"Releasing software is too often an art;
>it should be an engineering discipline."
>
>"There should be be two tasks for a human being to perform to deploy
>software into a development, test, or production environment:
>to pick the version and environment and to push the 'deploy' button"
>
>-- David Farley
>
>
>Done means "released". This implies ownership of a project right up
>until it’s in the hands of the user, and working properly.
>There’s none of this "I’ve checked in my code so it’s done as far as I’m concerned"
>
>-- James Betteley


# Level 0
When you only release software every 6-18 months deployments can be a very big deal. Typically individual teams are responsible for planning, scheduling, performing and testing the process.

Because of the time, effort and money involved in releasing software, organisations can be  protective of their release process leading to stagnation. This makes iteration, optimisation and innovation difficult.

### Indications that you're operating at level 0

 - Code, dependencies and configurations are manually copied between environments by the release team, who haven't been involved in any of the research, design or development activities, meaning they haven't developed any empathy for the users, and aren't necessarily focused on the user's needs, like timeliness.
 - There isn't any certainty about weather or not the deployment succeeded. Typically it is your users who find out if something has gone wrong.
 - Pushing to production goes directly from the developer's machine to production, but because every developer has a slightly different machine the published product is always a little bit different.
 - Deployments require the users to stop using the product, wait for the deployment process to complete, and then try to pick up where they left off. The release team doesn't know if a user is working on something urgent or time critical, they take the system down at the scheduled time.

### Working towards level 1

 - The time between releases is making it difficult for you get better at them. Try to release more frequently by including smaller and fewer new features. This will help you deliver new features to your users sooner and with less interruption. [If it hurts, do it more often](http://martinfowler.com/bliki/FrequencyReducesDifficulty.html)
 - Manual processes are slow, costly and error prone - start to investigate some automated build and integration tools - there are plenty of great free and open source ones out there if your development environment didn't come with any.
 - Use a dedicated environment for performing your automated builds, preferably a cloud environment. If you have restrictions about using external cloud services, set up a virtual environment inside your organisation instead.

# Level 1

Automating the release process allows for releases to happen more frequently. The release system can identify if the build  has succeeded or not, but not that the new features work properly.

Although there is little human involvement in releases, they still require the system to be taken offline while the release happens.

### Indications that you're operating at level 1

 - There are environments specifically for performing deployments, and an environment pipeline, (typically: development &rarr; pre-production &rarr; production). This helps to ensure that deployments are consistent, and that only successful deployments are made available to users.
 - The development team are able to schedule a release when they choose, based on user needs, and don't require help from outside the team, once the relevant approvals have been given.
 - Smoke screen testing is performed to ensure that the deployment didn't silently fail, but doesn't demonstrate that user functionality has been delivered, or that the system performs as expected.
 - Deployments are typically scheduled to happen outside of the user's regular usage times, in order to minimize disruption for the users.


### Working towards level 2
 - Start using automated acceptance testing tools which will help verify that the expected functionality has been released successfully. There are plenty of free and open source ones available if your development environment didn't come with one.
 - Consider some new release techniques: such as [Blue Green Deployment](http://martinfowler.com/bliki/BlueGreenDeployment.html) which will help you remove any interruptions to your users when releasing new features.
 - Aim to release multiple times within the same day. If something has been developed that your users want or find valuable, you should try to give it to them as quickly as possible.
 - Get up-to-date on best practices by reading about what others are doing, and what is working well. There is lots of great content out there, and most of the best bits are free.


# Level 2

Automating the end-to-end release process has resulted in multiple releases per day, of small but valuable features and changes, allowing you to respond to user needs quickly.

### Indications that you're operating at level 2

 - Deployments are completely automated for all components of the system, and don't require any intervention from any internal or external team members. This puts the control of flow of features in the hands of the team who have the most empathy for the users.
 - There are no impacts to the users when new features are released. Deployments happen instantaneously and are guaranteed to have the correct set of features which function exactly as expected without any surprises.
 - Individual features are atomically deployable and don't impact / aren't impacted by the in-progress development of other features. If a feature isn't wanted, it can be pulled from production without impacting the rest of the system.
 - Virtualization or configuration management tools, such as docker chef or puppet, are used to ensure consistency between  developers, eliminating any systemic issues due to environmental configuration
