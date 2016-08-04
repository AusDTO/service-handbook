---
title: "Version Control"
section: 2-tech
---

Developing digital products creates files, **lots** of files.
Each of these files specifies something important about the service: how it works, how it looks, what it's called.
The collective set of files *is* the service.

Version control systems protect these files from accidents, like deletions, by keeping track of every change that you and your team make.


>To support collective ownership, use a concurrent model of version control.
>Support time travel by storing tools, libraries, documentation, and
>everything else related to the project in version control. (On-site customers
>files, too.) Keep the entire project in a single repository.
>
>Keep your repository clean: never check in broken code. All versions should
>build and pass all tests. "Iteration" versions are ready for stakeholders;
>"release" versions are production-ready.
>
>  -- http://www.jamesshore.com/Agile-Book/version_control.html


# Level 0

The team use version control because they work on shared files, but treat the version control system like a shared directory. Checking in files is seen as an annoying, but necessary part of working in the team.

### Indications that you're operating at level 0

 - The only team members who have access to, or know how to use the version control system are the developers. Whenever a non-developer needs to access or change something, they need to track down and ask a developer to do the work for them.
 - The repository only has one branch, the trunk, that contains all the files for the system. Any in-progress work is stored on each developer's machine, and isn't shared with anyone until a big-ban check in. Developers are hesitant to integrate with other code because it might break what they're working on.
 - The repository's log is full of unhelpful and inconsistent commit messages, and it is impossible to recreate what, how, and why things were done. When issues occur in production, the team programmatically work back through each change-set to try and identify when things went wrong.
 - The changes introduced in single commits is haphazard, typically containing the files needed for the new feature, and whatever else has been changed on the developer's machine.


### Working towards level 1

 - Get the entire team onboard with version control. Content editors should be able to make changes just as easily and frequently as developers, but they can't iterate effectively if they're shackled to the developers.
 - Start using branches for feature development, bug fixes and refactoring. This will help to keep your trunk stable, working and reliable.
 - Focus on making commit messages useful ([How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)). When you're under the pump to fix a bug, a well written commit log really helps you figure out what, when, and why something happened.

# Level 1

The team's version control repository is seen as a key enabler for delivery and is consulted multiple times a day for authoritative information on how the team is tracking.

### Indications that you're operating at level 1

- The repository has multiple active branches that the team use for introducing new features - this helps keep the trunk clean, which makes it easier to work on bug fixes.
- The version control system is more than just code storage, and is used to hold dependencies, configuration, content and documentation.
- Commits to the repository are made daily, but typically at the end of the day before the team members go home. This helps ensure that effort isn't lost, but it leaves the repository in an inconsistent state, and is difficult to work out what has happened.
- Additional features of the version control system, such as issue tracking and collaboration, are being used by the team - for example to close or open a bug with a commit message.


### Working towards level 2

 - Work on getting your commits to be self-contained and focused on small units of work - [Atomic commits](http://www.freshconsulting.com/atomic-commits/).
 - Start to integrate your development processes with the version control system - trigger automated builds when somebody commits to the repository and use the code review features to work collaboratively.
 - Experiment with how you can use the repository to help with feature deployments and rollbacks.


# Level 2

A simple but rigorous process helps the team work on multiple features simultaneously, which can be deployed and pulled individually and quickly.

### Indications that you're operating at level 2

- There are several open and actively contributed to branches, each one containing the development on a new feature, bug fix, or refactoring existing code.
- The team use all of the features in the version control system (triggering builds, code reviews, comments, feature requests, notifications, etc)  to streamline the development process.
- The master branch always contains working code, and isn't ever in a broken state. Feature branches always compile, but are in varying stages of completion. This makes it easy for team members to pickup the code and contribute, knowing that everything is in a consistent state.
- Changes made to the repository are small, contained and atomic, resulting in lots of frequent commits that are targeted at a particular issue
- Important points in the project's history are tagged, such as milestone releases, and archived for future reference
- The repository's log communicates the context about why changes were made and what decisions were taken.
