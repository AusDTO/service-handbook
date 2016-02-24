---
title: "Version Control"
section: 5-version-control
index: true
---

Developing digital products creates files. Lots of files.
Each of these files specifies something about the solution: how it works, how it looks, what it's called.
The collective set of files *is* the solution.

Version control systems protect these files from accidents, like deletions, by keeping track of every change that you, and your team, make.




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



Resources:

 - [InfoQ](http://www.infoq.com/articles/agile-version-control)
 - [The Art of Agile](http://www.jamesshore.com/Agile-Book/version_control.html)
 - [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
 - [A Simple Git Branching Model](https://gist.github.com/aussielunix/59957626d6eace17be64)
 - [Atomic Commits](http://www.freshconsulting.com/atomic-commits/)

### Level 0
 - The developers are the only team members who know what a version control repository is
 - The repository only has one branch, the trunk, that contains the code for the system. Any in-progress work is stored on the developer's machine
 - The repository's log is full of unhelpful and inconsistent commit messages, and it is impossible to recreate what, how, and why things were done
 - The changes introduced in single commits is haphazard, and typically contains whatever has been changed on the local machine

### Level 1
 - Multiple branches are used to introduce new functionality
 - The version control system is used to authoritatively hold the projects code, dependencies and configuration
 - Commits to the repository are made daily, typically at the end of the day before the team members go home.
 - Ancillary features of the version control system, such as identifying differences are being used

### Level 2
 - There are lots of open branches, each one containing the development on a new feature or refactoring existing ones
 - The team exploit all features of the version control system: triggering builds, code reviews, comments, feature requests, notifications, etc
 - The master branch always contains working code, and isn't ever in a broken state. Feature branches always compile, but are in varying stages of completion
 - Changes made to the repository are small, contained and atomic, resulting in lots of frequent commits
 - Important points in the project's history are tagged, such as milestone releases, and archived for future reference
 - The repository's log communicates the context about why changes were made and what decisions were taken
