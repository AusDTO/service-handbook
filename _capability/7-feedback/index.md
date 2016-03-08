---
title: "Feedback"
section: 7-feedback
index: true
---

Getting feedback is critical to the usefulness and ongoing health of the system, and ensures that you are continuing to be responsive to the needs of your users.


>"It's not a bug - it's an undocumented feature."
>
>-- Anonymous

# Level 0

Users don't think that you take issues and defects seriously, so they've stopped reporting them to you. Management think the lack of bugs is great, but your users are suffering.

### Indications that you're operating at level 0

- Each developer manages a list of the bugs that they've discovered and working on. The lists aren't shared with anyone else, so nobody really knows what the complete list of bugs are, and which ones are being worked on.
- Unless a user describes what they were doing in excruciating detail when they encountered a bug, their defect will be closed with a status of '[Works on my Machine](https://shkspr.mobi/blog/2016/01/works-on-my-machine/)' or 'Not a bug'
- Bugs take so long to be resolved, the users have collaboratively developed a 'workaround' list so they can keep using the system while they wait.


### Working towards level 1
 - Get serious about issues and defects by tracking and managing them in a tool, preferably one that is integrated with your version control system. Read up on how ways to manage issues, such as github's [Mastering Issues](https://guides.github.com/features/issues/) guide.
 - Actually use your product - build some user empathy by walking in their shoes and experiencing first-hand what their experience is like using your product.


# Level 1

Issues and bugs are being tracked and proactively worked on, but unless your users tell you things are wrong you assume that there is nothing to improve on.

### Indications that you're operating at level 1

- Bugs and issues are managed with a tool that is shared amongst the entire team. The tool is used to prioritise the bugs you should be working on, based on metrics like number of users impacted, severity, and time since reported.
- The product offers users the ability to send a feedback email, but the team doesn't know who monitors the inbox.

### Working towards level 2
- Be open to constructive criticism - offer your users the chance to talk to a human, by phone or email, about what's bothering them, and be responsive - let them know that you're working hard to remove the things that make using your services difficult and unenjoyable.
- Investigate tools and techniques that will allow your system to self-monitor and detect different types of configuration, instability and outage scenarios. There are plenty of great free and open source ones out there if your development environment didn't come with any.

# Level 2

Ongoing interaction between the team and users allows the team to really focus on where the pain points are, and what they can do to help.

### Indications that you're operating at level 2

- Users are able to request modifications and enhancements to the system, and the community vote and prioritise the things that are important to them.
- The system provides anonymised information about how the users actually use the system, allowing the developers to see if features are used as expected, and what optimisations can be made for a better user experience
- The system is able to identify when bugs occur, and automatically raise support tickets, alleviating the user from needing to describe what they were doing when the issue occurred
- The project team are involved with first line support, giving them a real appreciation for the impacts of their decisions on the users.
