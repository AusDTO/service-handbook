---
title: "Development"
section: 4-development
index: true
---
Development converts ideas, assumptions, and user stories into a running, functioning, system.



>“If debugging is the process of removing bugs,
>then programming must be the process of putting them in.”
>
> -- Edsger Dijkstra



Resources:

 - [S.O.L.I.D](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)
 - [Big Ball of Mud](http://www.laputan.org/mud/)
 - [Express names in code](http://blog.goyello.com/2013/05/17/express-names-in-code-bad-vs-clean/)
 - [Getting started with DDD](http://www.informit.com/articles/article.aspx?p=1944876&seqNum=3)
 - [Clean, high quality code](https://www.butterfly.com.au/thinking/blog/entry/clean-high-quality-code-a-guide-on-how-to-become-a-better-programmer)

### Level 0
 - Class, method, instance and variable names are meaningless:

> int i;
> String upn;

 - Code is needlessly complex, difficult to read and poorly formatted
 - There are large sections of commented out code
 - The code doesn't reflect the user's vocabulary:

> patient.setShotType(ShotTypes.TYPE_FLU);
> patient.setDose(dose);
> patient.setNurse(nurse);


 - Language specific conventions aren't being followed ( java => getters/setters, c# => properties, ruby => attr_accessor, etc.. )
 - Common methods and behaviour are duplicated throughout the code base
 - Objects exhibit inappropriate intimacy and indecent exposure:

> return getWindow().getForm().getElements().getElementById('name').getLength();


 - The team don't feel proud of the code; it's difficult to work with and very brittle, resulting in stagnation, degradation and abandonment.
 - The team's velocity is very low, haphazard and unpredictable.
 - Programming is a stressful experience.

### Level 1
 - Class, method, instance and variable names convey their intent and purpose:

> int currentChild;
> String userPreferredName;

 - Code is clean and appropriately documented which makes it easier for others to read and maintain
 - Technical debt is continually measured, and given high priority during sprint planning
 - Classes have a single responsibility


### Level 2
 - Methods are small, single purpose, and don't create side effects
 - Code is self-documenting, and the intent and structure are self-evident based on the user's vocabulary:

> Vaccine vaccine = vaccines.standardAdultFluDose();
> nurse.administerFluVaccine(patient, vaccine);

 - Code is continually refactored to be simpler, cleaner, easier to understand and work with
 - The team are proud of their code; it's a joy to work on and improve. Introducing new features is quick, simple.
 - The team's velocity is high and consistent; features are delivered to users on time
 - Programming is fun again.


[Back]({{site.baseurl}}/)
