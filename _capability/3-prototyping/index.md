---
title: "Prototyping"
section: 3-prototyping
index: true
---

Why do engineers build models? Why do aerospace engineers build models of aircraft? Why to structural engineers build models of bridges? What purposes to these models serve?

These engineers build models to find out whether their designs will work. Aerospace engineers build models of aircraft to see whether they will fly. Structural engineers build models of bridges to see whether they will stand. Architects build models of buildings to see whether their clients will like the way they look.
*Models are built to find out whether something will work*
[Agile Principles, Patterns and Practices in C#](https://books.google.com.au/books?isbn=0132797143)



>"I have not failed 10,000 times. I have not failed once.
>I have succeeded in proving that those 10,000 ways will not work."
>
>-- Thomas Edison
>
>
>"If a picture is worth 1000 words, a prototype is worth 1000 meetings.
>—saying at @ideo"
>
>-- John Maeda


# Level 0

Time is short and you don't have the luxury of spending much time on throwaway prototypes, so you hack something together as quickly as possible.


### Indications that you're operating at level 0


 - Prototypes are developed in a [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) editor, without any real understanding of the underlying technology limitations. They're produced quickly and in isolation without co-design with the development team. This typically leads to unimplementable prototypes, disgruntlement and wasted effort.
 - To pad the prototype out, there are lots of [Lorem ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum), which may look pretty, but it doesn't help the team or users understand the intent of the service being prototyped
 - The prototype is entirely static with no dynamic behavior or navigation. This makes the prototype difficult to understand without the author guiding people through it, preventing it from being circulated to lots of users.
 - Either by technical or license limitations, the prototype is only available to people situated with the development team.


### Moving to level 1

 - Paper prototypes are more useful then static WYSIWYG produced mockups. They take less time to produce, are easy to modify and can be distributed easily.
 - Start to share your prototypes with a wider audience of users. This may mean that you need to rethink how you explain the flow of your prototypes, and what distribution mechanisms you use.
 - Focus on the high-value parts of the prototype, and skip everything else. Large amounts of text or content that doesn't help to evaluate this approach to the MVP will probably distract people.
 - Read up on [Sketching in Code](http://alistapart.com/article/sketchingincode), which gets you started on developing prototypes in the technologies used for the final product.

# Level 1

Prototypes are being used successfully during your service design process, and the team collaborate on the designs before they are given to developers to implement.

### Indications that you're operating at level 1

 - Designs are first tested on paper with the team and users before becoming digital. The paper designs go up on the wall for the team to refer to throughout the process.
 - The designers and developers collaborate on the prototypes, ensuring that all aspects of the design are implementable and technically sound
 - Developers implement the paper prototypes simple CSS, HTML and JavaScript, which introduces navigation and have just enough interactive components to demonstrate the particularly interesting functionality.
 - Although they're throwaways, the prototypes are treated as important team technical assets and are stored in the team's version control repository.

### Moving to level 2

 - Start pair-programming with your designers when implementing coded prototypes. [There](http://www.w3schools.com/html/default.asp) are [heaps](http://www.w3schools.com/css/default.asp) of free learning resources online to help people learn (or re-learn) how to build content for the web.
 - Start to publish with your prototypes on the open web. There are lots of free hosting options available and most of them support the agile delivery process.

# Level 2

Prototypes are a core part of your service design process, and the entire team works together to ensure that they are relevant to the users needs. The designers and developers both work together to develop working coded prototypes, leading to rapid turnaround of ideas and concepts.

### Indications that you're operating at level 2

- Designers are using the production development tools (such as HTML and CSS) to produce working prototypes. Developers help out with the particularly hairy sections, but the whole team gets their hands dirty.
- Prototypes are published to a 'live' environment, and deployed continuously throughout their development as improvements are made and alternatives are produced.
- The prototypes are used to supplement user research, with activities such as alpha-beta testing used to gather large amounts of supporting data  
