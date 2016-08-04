---
title: "Development"
section: 2-tech
---
Development converts ideas, assumptions, and user stories into a running, functioning, system.



>“If debugging is the process of removing bugs,
>then programming must be the process of putting them in.”
>
> -- Edsger Dijkstra


# Level 0

If you've been developing for a long time, it is inevitable to form habits in your approach and techniques, and to bring habits with you onto new projects.

Although these habits have served you well they're not always a good fit for every project, and you've noticed that your java code starts to smell like cobol and your ruby code starts to smell like visual basic.

### Indications that you're operating at level 0
- When people read your code, they struggle to understand what it's doing because the class, method, instance and variable names are meaningless:

> int i;
> String upn;

- Even though it works well and passes every test, the code is needlessly complex, difficult to read and poorly formatted
- There are large sections of commented out code that contain work in progress, or previous versions of methods.
- The code is clean and well written, but it doesn't reflect the user's vocabulary:

> patient.setShotType(ShotTypes.TYPE_FLU);
> patient.setDose(dose);
> patient.setNurse(nurse);


- Language specific conventions aren't being followed ( java's getters/setters, c#'s properties, ruby's attr_accessor, etc.. )
- Common functionality and behaviour are duplicated throughout the code base, sometimes they are identical but often with nigglingly small changes.
- Objects aren't encapsulated, and exhibit inappropriate intimacy and indecent exposure:

> return getWindow().getForm().getElements().getElementById('name').getLength();


- The team don't feel proud of the code; it's difficult to work with and very brittle, resulting in stagnation, degradation and abandonment.
- The code is difficult to work with and causes the team's velocity to be very low, haphazard and unpredictable.
- Programming is a stressful experience.


### Moving to level 1

 - Learn about some software design methodologies that help make your code more maintainable ([S.O.L.I.D](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)), and anti-patterns ([Big Ball of Mud](http://www.laputan.org/mud/)).
 - Start using [meaningful names](http://blog.goyello.com/2013/05/17/express-names-in-code-bad-vs-clean/) in your code
 - Use version control systems to remember what works and what doesn't - not commented out blocks of code.
 - Learn the conventions of the technology that you're using and stick to them - they've been chosen for a good reason, which typically is unique to that technology.

# Level 1

Code that is consistent and understandable is easier to work with and maintain. Fixing bugs is quicker, and features are simpler to introduce.

### Indications that you're operating at level 1


 - Class, method, instance and variable names convey their intent and purpose:

> int currentChild;
> String userPreferredName;

 - Code is clean and appropriately documented which makes it easier for others to read and maintain
 - Technical debt is continually measured, and given attention during planning
 - Classes have a single responsibility, and only have functionality to achieve their purpose.


### Moving to level 2

 - Start writing smaller methods, and refactoring large ones to be smaller and more reusable.
 - Carefully think about how the decisions you make impact others in your team: [Always code as if the person who ends up maintaining your code is a violent psychopath who knows where you live](http://c2.com/cgi/wiki?CodeForTheMaintainer), and [code like the world is watching](http://todaymade.com/blog/open-source-code/)
 - Begin using design techniques that build user empathy, such as [Getting started with DDD](http://www.informit.com/articles/article.aspx?p=1944876&seqNum=3)
 - Read up on what makes [clean, high quality code](https://www.butterfly.com.au/thinking/blog/entry/clean-high-quality-code-a-guide-on-how-to-become-a-better-programmer)



# Level 2

Treating form as importantly as function makes maintaining the system simple and quick, allowing the team to focus their efforts on responding to user needs quickly.


### Indications that you're operating at level 2


 - Methods are small, single purpose, and don't create side effects
 - Code is self-documenting, and the intent and structure are self-evident based on the user's vocabulary:

> Vaccine vaccine = vaccines.standardAdultFluDose();
> nurse.administerVaccine(patient, vaccine);

 - Code is continually refactored to be simpler, cleaner, easier to understand and work with
 - The team are proud of their code; it's a joy to work on and improve and introducing new features is quick and simple.
 - The team's velocity is high and consistent; features are delivered to users on time
 - Programming is fun again.
