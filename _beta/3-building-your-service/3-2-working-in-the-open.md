---
title: "3.2. Working in the open"
section: 3-building-your-service
---

Tips on being open

Working in the open is a great way to share what you&rsquo;ve done, and to attract contributions from people outside your service&rsquo;s development team. Being open means that you might have to do some things differently than before:

*	Keeping secrets &ndash; like passwords, credentials, and security keys &ndash; out of code is now very important. You should take this seriously, as one mistaken commit containing a secret makes that secret public for the whole world to see. At the DTO we store these in environment variables of the Platform as a Service which runs our applications. This keeps them separate from the code, but allows them to be configured easily by delivery teams.
*	Your code should be open source by default. It&rsquo;s important that agencies do not &ldquo;re-invent the wheel&rdquo;. If you are unable to release your code through the open source community, a case should be provided to explain the rationale. 
	-	The [Digital Service Standard](https://www.dto.gov.au/standard/8-make-source-code-open/ "read about criterion 8 of the Digital Service Standard") has more detail on the DTO website.
*	Consider adding some very simple checks in your application&rsquo;s build process that gets run out of Continuous Integration on every commit. A simple grep for credentials and data you think you might leak is enough to fail the build. This helps the team fix the data leak before it becomes an insurmountable problem to clean up.
*	If you do accidentally leak data into the code base, you can use the [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/ "visit the BFG Repo-Cleaner website") to strip out that data from all commits.

# Choosing an open source license

If you are making your source code open, you need to release it under a license that reflects your organisation&rsquo;s needs on how others can use your code. Licenses can be tricky, so you should consider seeking legal advice before choosing a license that best suits you and your users needs. Picking the wrong license can cause problems for others who want to reuse your code. 

At the DTO we try to release all of our code under the MIT license, which allows others to use our code in whatever way helps them. Talk with your department&rsquo;s Digital Transformation Coordinator for help on [picking a license](http://choosealicense.com/ "Choose an open source license") that works for your organisation.

# Contributing to the community

If you have used an open source product that helps you deliver your service, you should consider contributing something back to the project. Your contributions don&rsquo;t have to be code, simply raising issues or feature requests help keep the ecosystem growing. Just make sure you follow through with your contribution by participating in any follow-up discussions. You may need to get your organisation&rsquo;s permission before contributing to open source projects. If you&rsquo;re unsure about how to make contributions on behalf of your organisation, you should talk with the Digital Transformation Coordinator in your department.
