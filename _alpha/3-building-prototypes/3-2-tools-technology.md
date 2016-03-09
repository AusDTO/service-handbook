---
title: "3.2. Tools and technology"
section: 3-building-prototypes
---

When choosing the technology for building prototypes in alpha, you should choose lightweight tools that allow for quick experimentation and rapid validation of the hypothesis. Technology should not be a blocker in prototyping a potential user journey, no matter how radical.

All teams should prototype by sketching in code, using HTML, CSS and JavaScript. We strongly advise against using software like Axure, Omnigraffle, or Balsamiq - these tools generally don't support a collaborative, multi-disciplinary working environment.

It's completely fine (and strongly recommended) to throw away the prototypes you build. You may choose to re-use some design patterns or components when you build the Beta, but you should not re-use a whole prototype.

## 3.2.1. Use a static-site generator

The best approach to building a lightweight user-facing prototype is to choose a static-site generator, like [Jekyll](https://jekyllrb.com/).

A static-site generator will allow you to keep your prototype simple, with just HTML, CSS and JavaScript, but allow you to easily share templates and stylesheets across multiple pages. It is also easy for designers and content designers to make changes directly to the prototype, without having to send changes 'over the wall' for a developer to make.

Use a version control system, like [GitHub](https://github.com/), to store the code for your prototype, so that everyone in the team can work across the same copy and collaborate on changes.

For the best results, deploy the prototype to a service like [Heroku](https://heroku.com) or [Amazon Web Services](https://aws.amazon.com/), so that you can easily share it around the team and with your stakeholders. If you configure the service to automatically deploy whenever changes are made (sometimes called 'creating a build pipeline'), then everyone will always be able to access the most up-to-date version.

## 3.2.2. Building interactive features

For most prototypes, you will want to include at least some level of interactivity to simulate a working service (eg. capturing user details on a form).

Whilst it is easy to make the case to use a server-side technology for this functionality (eg. Java, .NET, Ruby), keeping the technology simple will ensure updating the prototype remains as quick and easy as possible.

Use client-side technologies like [the Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API/Using_the_Web_Storage_API), combined with a JavaScript framework like [jQuery](https://jquery.com/), to quickly store and retrieve information for the user's session. Make it easy to reset and start again at the end of a user research session.

## 3.2.3. Don't support every browser

The potential audience for a prototype is often limited. Many users are likely to be accessing the prototype from a controlled environment (eg. a user research lab). This means that the potential browsers to support is smaller than a public website.

Consider targeting the latest version of each major browser (Chrome, Firefox, IE, Safari). You may also wish to target a specific browser or version if a specific group of users or stakeholders depend on it.

As part of the user research, you should test your prototypes with users who have accessibility needs. Therefore, it is strongly recommended to use semantic and accessible markup across prototypes, and test with screen reader software and other accessibility aids.
