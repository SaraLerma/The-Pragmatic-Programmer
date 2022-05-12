# Intro

<img src=assets/the_pragmatic_programmer.png align="right" width=150 height=200>  

The book “[The Pragmatic Programmer, 20th Anniversary Edition](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/)” by David Thomas and Andrew Hunt is one of the “must-read” for a developer.

This book comes from the authors' experience of developing many software projects.
It is not a purely technical book, it gives us applicable tips to improve the process of developing software, going through concepts of concurrency, patterns, communication, estimations, debugging, testing, refactoring, agile methodology, ETC and DRY principles, and so on.  
From my point of view, it explains concepts that we have to keep in mind to be a good programmer since as we already know, technical skills are not enough.

# Disclaimer

This is my summary of the concepts that I have highlighted from each chapter. I have written these notes as a quick reference guide.  
This summary is not intended to be a replacement for the book, in the book are explained concepts with examples and develops deeply more concepts, has exercises with proposed solutions, and much more.

So please, if you are interested, get the [original book](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/) for the full overview. I think it is a book that must have at home, underline and reread. 🤓

If the publisher thinks this guide should be private, please let me know (saralerma2@gmail.com) and I will make it private.

Feel free to send suggestions, I will be really grateful 🤍

# Contents

- [Preface](#preface)
- [Chapter 1. A Pragmatic Philosophy](#chapter-1-a-pragmatic-philosophy)
  - [1.-It's Your Life](#1-its-your-life)
  - [2.-The Cat Ate My Source Code](#2-the-cat-ate-my-source-code)
  - [3.-Software Entropy](#3-software-entropy)
  - [4.-Stone Soup and Boiled Frogs](#4-stone-soup-and-boiled-frogs)
  - [5.-Good enough software](#5-good-enough-software)
  - [6.-Your Knowledge Portfolio](#6-your-knowledge-portfolio)
  - [7.-Communicate](#7-communicate)
- [Chapter 2. A Pragmatic Approach](#chapter-2-a-pragmatic-approach)
  - [8.-The Essence of Good Design](#8-the-essence-of-good-design)
  - [9.-The Evils of Duplication](#9-the-evils-of-duplication)
  - [10.-Orthogonality](#10-orthogonality)
  - [11.-Reversibility](#11-reversibility)
  - [12.-Tracer Bullets](#12-tracer-bullets)
  - [13.-Prototypes and Post-it Notes](#13-prototypes-and-post-it-notes)
  - [14.-Domain Languages](#14-domain-languages)
  - [15.-Estimating](#15-estimating)
- [Chapter 3. The Basic Tools](#chapter-3-the-basic-tools)
  - [16.-The Power of Plain Text](#16-the-power-of-plain-text)
  - [17.-Shell Games](#17-shell-games)
  - [18.-Power Editing](#18-power-editing)
  - [19.-Version Control](#19-version-control)
  - [20.-Debugging](#20-debugging)
  - [21.-Text Manipulation](#21-text-manipulation)
  - [22.-Engineering Daybooks](#22-engineering-daybooks)
- [Chapter 4. A Pragmatic Paranoia](#chapter-4-a-pragmatic-paranoia)
  - [23.-Design by Contract](#23-design-by-contract)
  - [24.-Dead Programs Tell No Lies](#24-dead-programs-tell-no-lies)
  - [25.-Assertive Programming](#25-assertive-programming)
  - [26.-How to Balance Resources](#26-how-to-balance-resources)
  - [27.-Don't Outrun Your Headlights](#27-dont-outrun-your-headlights)
- [Chapter 5. Bend or Break](#chapter-5-bend-or-break)
  - [28.-Decoupling](#28-decoupling)
  - [29.-Juggling the Real World](#29-juggling-the-real-world)
  - [30.-Transforming Programming](#30-transforming-programming)
  - [31.-Inheritance tax](#31-inheritance-tax)
  - [32.-Configuration](#32-configuration)
- [Chapter 6. Concurrency](#chapter-6-concurrency)
	- [33.-Breaking Temporal Coupling](#33-breaking-temporal-coupling)
	- [34.-Shared State Is Incorrect State](#34-shared-state-is-incorrect-state)
	- [35.-Actors and Processes](#35-actors-and-processes)
	- [36.-Blackboards](#36-blackboards)
- [Chapter 7. While You Are Coding](#chapter-7-while-you-are-coding)
  - [37.-Listen to Your Lizard Brain](#37-listen-to-your-lizard-brain)
  - [38.-Programming by Coincidence](#38-programming-by-coincidence)
  - [39.-Algorithm Speed](#39-algorithm-speed)
  - [40.-Refactoring](#40-refactoring)
  - [41.-Test to Code](#41-test-to-code)
  - [42.-Property-Based Testing](#42-property-based-testing)
  - [43.-Stay Safe Out There](#43-stay-safe-out-there)
  - [44.-Naming Things](#44-naming-things)
- [Chapter 8. Before The Project](#chapter-8-before-the-project)
  - [45.-The Requirements Pit](#45-the-requirements-pit)
  - [46.-Solving Impossible Puzzles](#46-solving-impossible-puzzles)
  - [47.-Working Together](#47-working-together)
  - [48.-The Essence of Agility](#48-the-essence-of-agility)
- [Chapter 9. Pragmatic Projects](#chapter-9-pragmatic-projects)
  - [49.-Pragmatic Teams](#49-pragmatic-teams)
  - [50.-Coconuts Don't Cut It](#50-coconuts-dont-cut-it)
  - [51.-Pragmatic Starter Kit](#51-pragmatic-starter-kit)
  - [52.-Delight Your Users](#52-delight-your-users)
  - [53.-Pride and Prejudice](#53-pride-and-prejudice)
- [Tips](#tips)

# Preface

## What makes a Pragmatic Programmer?

Characteristics of a pragmatic programmer:

1. **Early adopter/fast adapter** – when something new comes along, you try it out, quickly understand it, and integrate it with the rest of your knowledge. Your confidence is born from your experience.
2. **Inquisitive** – ask questions, be curious.
3. **Critical thinker** – don't take things as given without thinking critically about them. No run on auto-pilot and take control. Constantly think and critique your work.
4. **Realistic** – understand the underlying nature of each problem. You know how difficult things are and how long things will take.
5. **Jack of all trades** – maybe you are specialized in some area but you will always be able to move on to new areas or challenges.

## Individual pragmatists, large teams

On large teams, within the overall structure of a project, there is always room for individuality and craftsmanship. So, when you are developing something, keep the overall structure of the project in mind and try to be pragmatic.

## It’s a continuous process

“Kaizen” is a Japanese term that captures the concept <span style="color:lightgreen;">**continuously making many small improvements**</span>. Every day, work to redefine the skills you have and add new tools to your project.

# Chapter 1. A Pragmatic Philosophy

## 1. It’s Your Life

Developers seem to resist change. Fix it, make time to study new stuff (in your own time). Invest in yourself, be proactive and take the opportunities that the software development industry gives you.

Take responsibility for everything you do.

## 2. The Cat Ate My Source Code

Take responsibility for your career and don’t be afraid to admit ignorance or error. When you make a mistake, admit and <span style="color:lightgreen;">**provide options - don’t make lame excuses**</span>, or blame someone or something else.  
*Tip – talk to the rubber duck before your coworker.*

<span style="color:lightgreen;">**Don’t say it can’t be done; explain what can be done**</span> to salvage the situation. Think: “I don’t know but I will find out”.

## 3. Software Entropy

Entropy refers to the amount of disorder in a system.

Technical debt (aka software rot) is like a broken window in a house.
Ignoring a broken situation reinforces the idea that you don't care and nothing can be fixed. In this way, negative thoughts are spread among team members creating a vicious spiral. People lose the will to fight entropy because they perceive that no one else cares.

<span style="color:lightgreen;">**Don’t live with broken windows unrepaired**</span> like bad designs, wrong decisions, or poor code.

## 4. Stone Soup and Boiled Frogs

If you think something needs to be changed, <span style="color:lightgreen;">**be a catalyst for change**</span> – develop the proposal, show people and say "it would be better if we added…" and they will ask and will join an ongoing success.  
You can’t force change on people. Instead, show them how the future might be and help them participate in creating it.

On the other side, keep an eye on the big picture, don’t get so engrossed in the details that you forget to check what’s happening around you. Review what is happening around you, not just what you are doing (the frog just doesn’t notice the change).

## 5. Good Enough Software

Produce good enough software, don’t frustrate yourself trying to produce perfect software without bugs, you need to know when to stop (discuss the scope and quality of the system).

Your systems must meet users’ requirements, basic performance, privacy, and security standards. <span style="color:lightgreen;">**Involve your users in determining the project’s real quality requirements.**</span>
Involve them by giving them something to play with early and get feedback.

> Feature bloat – software that contains more features than you would ever use, each implemented feature introduces more opportunities for bugs and security vulnerabilities.

<span style="color:lightgreen;">**Keep it simple.**</span>

## 6. Your Knowledge Portfolio

The most important thing is your experience, knowledge, and ability to learn new things. <span style="color:lightgreen;">**Invest in your knowledge portfolio regularly**</span>, make learning an habit.  

To think critically, ask the “[Five Whys](https://en.wikipedia.org/wiki/Five_whys)” and ask *who does this benefits?, what is the context?, when or where would this work?, why is this a problem?...* 🤔  
<span style="color:lightgreen;">**Critically analyze what you read and hear**</span>, don’t be swayed by vendors, media hype, or dogma. Analyze information in terms of you and your project.

## 7. Communicate

<span style="color:lightgreen;">**It’s both what you say and the way you say it**</span>, there’s no point in having great ideas if you don’t communicate them effectively.

Some tips:

- Treat **English** as another programming language.
- Know your **audience** (their needs, interest, and capabilities)
- Get **feedback** (ask them, check body language, listen to them! 👂)
- Plan what you want to say (write down your ideas and strategies for exposing them).
- Choose the **moment** to comment idea (ask if it’s a good moment to comment on it).
- Adjust the style of your talk to your audience (their skill level and experience).
- Make a prettied document or presentation (with good format and spelling),
- Always **respond** (even if you respond "I’ll get back to you later" to they don’t feel that you have forgotten them)
- **Document** (why something is done, its purpose and its goal, engineering trade-offs, why decisions were made, discarder alternatives, and so on). <span style="color:lightgreen;">**Build documentation in, don’t bolt it on**</span>, documentation created separately from code is less likely to be correct and up to date.

> Reminder: tl;dr – too long; didn’t read.  

# Chapter 2. A Pragmatic Approach

## 8. The Essence of Good Design

ETC (Easier to change) principle:
> Good design is easier to change than bad design - a thing is well designed if it must adapt by changing.

ETC helps you to make decisions. Ask yourself “did the thing I just did make the overall system easier or harder to change?”. It’s important to think about keeping code decoupled and cohesive.

## 9. The Evils of Duplication

📖  [whole topic](https://media.pragprog.com/titles/tpp20/dry.pdf)  

Knowledge is not stable (your understanding of a requirement, business logic, user requirements, etc.). Maintenance is a routine of the entire development process.

The DRY (Don’t repeat yourself) principle is:
> "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system"  

DRY is about duplication of knowledge (express the same thing in two different places, even possibly in two totally different ways).

Examples of duplication:

1. **Duplication in code**: code that does not duplicate knowledge. Note that maybe two function bodies are the same but the knowledge they represent is different.
Check [topic](https://media.pragprog.com/titles/tpp20/dry.pdf) for clear example.
2. **Duplication in documentation**: If you comment on a function and you changed the function, you have to update the document and code. The function’s name already says what it does, and if you need details, they are shown in the source code.  
**DRY violation in data** – A data structure represents knowledge and it may have duplicated data. Maybe you violate for performance reasons because you need to cache data to avoid repeating expensive operations.  
Tip: localize the impact. Always try to use accessor functions to read/write the attributes of the object to decouple the data structure from the implementation of the module that exposes the data structure.
3. **Representational Duplication**: Your code and the external entity have to have knowledge of the representation of their interface. If the interface change, the external entity that uses it may break.
This duplication is inevitable, but can be migrated with some strategies:
    1. **Dup across Internal APIs**: use a tool to specify API in a neutral format.
    2. **Dup across External APIs**: public APIs are documented using OpenAPI, so import API spec into your local API tools.
    3. **Dup with Data Source**: Don’t write code that represents external data in a fixed structure – stick it into a key/value data structure.  
    To not lose the security of the data that you are working on, you can use table-driven validation that verifies that the map you have created contains needed data in the correct format.
    4. **Interdeveloper Duplication**: Occurs when different developers work on the same project. You don’t know if the other dev did something similar.  
    Solution: communication (daily, threads to discuss common problems, appoint a ‘project librarian’ who facilitates the exchange of knowledge, code reviews).  

<span style="color:lightgreen;">**Make the code easy to reuse**</span>, if it’s easy to reuse, people will. Create an environment that supports reuse. ♻️

## 10. Orthogonality

In computing, orthogonality means independency and decoupling. If you change one thing it doesn’t affect the others. So, the goal is to reduce interdependency among the system’s components. A clear example; Interface is independent/orthogonal of the database.

### Benefits of writing orthogonal systems

- **Increase productivity**: changes localized, less time developing and testing, reusing components, and combining orthogonal components.
- **Reduce risk**: diseased components are isolated so less likely to spread symptoms to the rest of the system. The resulting system is less fragile because if you make changes in a particular area and provoke problems, they are restricted to that area. Orthogonal systems are better tested.

<span style="color:lightgreen;">**Eliminate effects between unrelated things**</span> - design components that are self-contained, independent, and have a single, well-defined purpose.

### Design orthogonal systems

Systems should be composed of a set of cooperating modules, each of which functionality is independent of the others. If components are organized in layers, each provides a level of abstraction.

### Toolkits and libraries

Choose wisely the technologies that you introduce in your system to maintain orthogonality. If the toolkit imposes changes on your code or it requires you to create or access objects in a concrete way, then is not orthogonal.

### Coding

You must be constantly critical with your code.

Techniques to maintain orthogonality:

- **Keep your code decoupled**: write shy code where modules don't reveal anything unnecessary to other modules and don’t rely on the implementation of others.

  Apply Law of Demeter:

  >“An object should avoid invoking methods of an object returned by another method”

  So if you need to change the state of an object, get the object to do it for you.

- **Avoid global data**: when you reference global data, you tie it into the other components that share that data. Just pass the required context into your modules.

- **Avoid similar functions**: Don’t duplicate code – a symptom of a structural problem.

### Testing

An orthogonal system is easier to test because interactions between components are formalized and limited, and more of the system testing can be performed at the individual module level (unit testing).

### Documentation

Content must be independent of presentation. Focus on content (using markup system – example: Markdown) and leave the presentation to whichever tool to render it.

## 11. Reversibility

Requirements, users, and hardware change faster than we can get the software developed.  
<span style="color:lightgreen;">**Don’t assume any decision is final/definitive**</span>, prepare for contingencies that might arise - plan for change.  

### Flexible arquitecture

Maintain flexibility in your code, architecture, deployment, and vendor integration. Break your code into components and make it easy to change.  

Forgo following fads - Neal Ford says, “Yesterday’s Best Practice Becomes Tomorrow’s Antipattern.” Choose architectures based on fundamentals, not fashion.

## 12. Tracer Bullets

Tracer bullets technique is an easy way for machine gunners to

- See where their bullets are going (getting the immediate feedback)
- Reactively adjust the trajectory to make the bullets go to the aim

We can also apply this technique in software development to visually illustrate the need for immediate feedback under actual conditions with a moving goal. Because projects take time to complete and the environment you are working in will change before you are done.

Tracer bullets is a style development that allows you to gather requirements, test designs, and implement code at the same time.
So first, you need to prioritize these areas to code:

- Important requirements (the ones that define the system)
- Areas where you have doubts
- Areas where you see the biggest risks

<span style="color:lightgreen;">**Use tracer bullets to find the target**</span> - Tracer bullets let you home in on your target by trying things and seeing how close they land.

Tracer code designs the skeleton of the final system. Every major application component is represented in your code, it’s not fully functional, but you will adjust and add more functionalities – it’s an **incremental approach**. Tracer code is agile and lean but complete.  

<p align="center">
  <img src=assets/tracer_bullets.png width=400 height=300>  
</p>  

Advantages of the tracer code:

- Users get to see something working early
- Developers build a structure to work in
- You have an integration platform
- You have something to demonstrate
- You have a better feel for progress

### Tracer Code versus Prototyping

Otherwise, the prototype is not a tracer bullet. With prototyping, you gather knowledge by exploring specific aspects of the final system. Meanwhile, the tracer bullets technique shows how the components of the application interact through an architectural skeleton of the final system.

## 13. Prototypes and Post-it Notes

Prototype is for analyzing and exposing risk, to identify potential problem spots early in the development process. To test specific aspects of the system being considered. <span style="color:lightgreen;">**Prototype to learn**</span> - prototyping is a learning experience. Its value lies not in the code you produce, but in the lessons you learn.

- For prototype dynamic things such as workflow and application logic you can use post-it notes.
- For a prototype user interface you can draw on a whiteboard or use a tool that lets you focus on the appearance and interactions without worrying about code or markup.

Samples you can prototype:

- Architecture
- New functionality in an existing system
- Structure or contents of external data
- Third-party tools or components
- Performance issues
- User interface design

Details to ignore in the prototyping:

1. Correctness
2. Completeness
3. Robustness
4. Style

Make sure everyone understands that the prototype code is disposable, incomplete, and unable to be completed. This way you will prevent the stakeholders think that the prototype is ready for use in production.

## 14. Domain Languages

Domain Language that lets us express solutions to problems in a way that is closer to a specific domain.  
> DSL (Domain Specific Language): particular computer language to solve a specific problem or specialized language for a particular application domain.

- **Internal DL**: use some general-purpose language(Ruby) for a specific purpose (testing - Rspec). So they are within the constraints of the host language’s syntax
- **External DL**: complete programming language with its own syntax and compiler. They need a parser that interprets the language or parses to another one. It’s not intended for general use; rather, it solves some targeted problems. For instance, SQL is an instance of Domain-Specific Language targeted at data manipulation.  

  > Suggestion: use external DSL only in cases where your language will be written by the users of your application.

<span style="color:lightgreen;">**Program close to the problem domain**</span> - design and code in the language of the problem domain.

## 15. Estimating

Estimate to avoid surprises - estimate before you start. You’ll spot potential problems up front.

### How estimate?

First, know the context in which your answer will be taken, do they need high accuracy or are they looking for a ballpark figure?

Units are important - the units you use make a difference in the interpretation of the result (130 days are different than 6 months).  

|  Duration       | Quote estimate in  |
|  :--------------: |:------------------:|
|  1-15 days      | Days       |
|  3-6 weeks      | Weeks        |
|  8-20 months    | Months        |
|  20+ weeks      | Think hard before giving an estimate  |

### Where do estimates come from?

All estimates are based on models of the problem. Ask someone who’s already done the same model or who’s been in a similar situation in the past and how he solved it.  

1. **Understand the scope of the domain**: your answer can include assumptions like "Assuming we keep our database tables the way they are, this feature will take X days".
2. **Build a bare-bones(skeleton) mental model**: doing so you can reveal things that wouldn’t have been immediately apparent and identify inaccuracies in the estimation.
3. **Break(decompose) the model into components**: each component will have parameters that affect how it contributes to the overall model – identify each parameter of these components.
4. **Give each parameter a value**: justify the way of calculating these critical parameters.
5. **Calculate answer**: couch your answer in terms of these parameters.
6. **Keep track of your estimating prowess**(skill) and find why you missed something in previous estimations.  

### Estimating project schedules

For estimating project schedules, estimating large development projects is difficult. The best way to make good estimations is to iterate on the same project and see how it progresses.

1. Check requirements.
2. Analyze risk and prioritize the riskiest items earlier
3. Design, Implement, Integrate.
4. Validate with the users.  

As you finish an iteration, you can use that to refine your project estimates, and you continue to do this and gain confidence in the estimates over time.

# Chapter 3. The Basic Tools

## 16. The Power of Plain Text

<span style="color:lightgreen;">**Store knowledge persistently in plain text**</span>, which must be understandable to humans(self-describing data).  
You can place the file in plain text in a version control system to automatically keep a history of all changes (file comparison tools).  
Plain text won’t become obsolete. It helps leverage your work and simplifies debugging and testing. All parties can communicate using a common standard → plain text.

## 17. Shell Games

Use the shell when graphical user interfaces don’t cut it.  
Use command shells to use the full capabilities of your environment, like invoke full repertories of tools, launch applications, search files, automate common tasks (build complex macro commands for activities you perform often), configure the prompt (for example info showed in zsh), use alias for commands you use a lot, customize completion depending on the current directory, etc.

## 18. Power Editing

<span style="color:lightgreen;">**Achieve editor fluency**</span> - An editor is your most important tool. Know how to make it do what you need, quickly and accurately.  
Gain fluency with your IDE (also try other editors), check if you are doing something repetitive, get into the habit of thinking "there must be a better way", try not to use the mouse (jot down key sequences), look for integrations and if you don’t find an extension for something - build it.

## 19. Version Control

Keep track of every change you make in your source code and documentation and it lets you do bug tracking, audit, performance, and quality purposes.  
It keeps the files in a **central repository** and allows more users to work currently on the same set of files, even making concurrent changes in the same file.  
Version Control (VC) let you isolate islands of development into branches. And you will roll it back.  
> Tip: use VC  to save everything that defined the configuration and usage of the original machine including; user preferences and dotfiles, the editor configuration, a list of software installed using homebrew, and current projects.

## 20. Debugging

Some of the strategies for finding elusive bugs:

- Think that debugging is just problem solving so concentrate on **fixing the problem, not the blame**. It doesn’t really matter whether the bug is your fault or someone else’s. It is still your problem, and it still needs to be fixed.
- Get yourself comfortable and **don't panic**. Very aware of myopia when debugging, try to discover the root because of a problem, not just this particular appearance of it.
- Gather all the relevant data, you may need to interview the user who reported the bug.
- Reproduce the bug with a single command.
- Get a **failing test before fix the code**. Create a focussed test that reveals the bug before you try fixing it. And amend tests to catch bugs and check if any other places in the code may be susceptible to this same bug.
- **Read the error message**. Most exceptions tell both what failed and where it failed. If you’re lucky you might even get parameter values.
- Get data set is failing, run it in local and isolate input values are leading to crash.
- Examine the call stack and jot down notes. ✍️  
You can use binary chop/search(divide and conquer) for large stack traces, certain datasets, during a set of releases, etc.
- Use tracing statements (print messages). Tracing is not valid in systems where time itself is a factor like concurrent processes, real-time systems, and event-based applications.
- Explain to someone else - [rubber duck](https://rubberduckdebugging.com/).
- It is possible that a bug exists in the OS or the compiler, or even a third-party product, but this should not be your first thought - think that the bug exists in the application code under development. **The bug is most likely in the application**.
- **Don't assume something works, prove it** in the actual environment - with real data and boundary conditions.

## 21. Text Manipulation

Use text manipulation language (example: Ruby) to manipulate plain text (like for code inclusion, index generation, website update), this will bring a lot of benefits.

## 22. Engineering Daybooks

Use a daybook to take notes in meetings, jot down what we’re working on, leave reminders, to record ideas.📝  
Benefits:

- It will provide you a place to store ideas.
- Acts as a rubber duck in debugging process.
- It’s more reliable than memory.

# Chapter 4. A Pragmatic Paranoia

**You can’t write perfect software** - Software can’t be perfect. Protect your code and users from the inevitable errors.

## 23. Design by Contract

Design By Contract (DBC) is a technique that focuses on documenting the responsibilities of software modules to ensure program correctness (a program which do the claimed, no more nor less).  
Use contracts to document and verify that code does no more and no less than it claims to do.

To describe the expectation and claims we can follow:

- **Preconditions**: requirement of routine to be called, it must be checked by the caller.
- **Postconditions**: what the routine is guaranteed to do (routine must finish)
- **Class invariants**: class that ensures this condition is always true from the perspective of a caller during a certain phase of execution.

If all the *preconditions* of the routine are met by the caller, the routine must guarantee that all *postconditions* and *invariants* will be **true** when it completes.

<p align="center">
  <img src=assets/design_by_contract.svg.png width=300 height=300>  
</p>  

In other words, the code has contracts that it meets: you meet the conditions when you feed it input, and it will make certain guarantees about the outputs it produces.  
There are also code *invariants*, things that remain true about some piece of state when it’s passed through a function. For example, if you sort a list, the result will have the same number of elements as the original—the length is invariant.

DBC and testing are different approaches to the topic of program correctness.

### Implementing DBC

Define at design time:

- what the input domain range is
- what the boundary conditions are
- what the routine promises to deliver or, more importantly, what it doesn’t promise to deliver

## 24. Dead Programs Tell No Lies

You must code defensively, thinking everything can happen, for this reason, each and every case/switch statement needs to have a default clause: we want to know when the “impossible” has happened.  
Don't catch or rescue all exceptions, better propagate them automatically.  

Basic principle: when your code discovers that something that was supposed to be impossible just happened, your program is no longer viable. Anything it does from this point forward becomes suspect, so terminate it as soon as possible. 💣  

<span style="color:lightgreen;">**Crash early - a dead program normally does a lot less damage than a crippled (invalid) one.**</span>

## 25. Assertive Programming

<span style="color:lightgreen;">**Use assertions to prevent the “impossible”**</span>. If it can’t happen, use assertions to ensure that it won’t. Assertions validate your assumptions.  
Use them to protect your code from an uncertain world. Because testing doesn’t find all bugs and your program runs in a dangerous world (during testing you are mocking communications, etc.).  
Assertions give you feedback and allow you to fix hard-to-reproduce bugs.

## 26. How to Balance Resources

When we code, we manage resources like memory, transactions, threads, network connections, files, timers, etc. All of them have limited availability.  
For this reason, we need to <span style="color:lightgreen;">**allocate the resource, use it, and then deallocate it**</span>.  
**The function or object that allocates a resource should be responsible for deallocating it** because if allocation and deallocation occur in different functions deallocation can not be done or you can try to deallocate something that is not allocated by an error.  

Act locally - keep the scope of mutable variables and open resources short and easily visible.

### Nest allocations

For nest allocations, routines that need more than one resource at a time. There are just two more suggestions:

- Deallocate resources in the opposite order to that in which you allocate them. That way you won’t orphan resources if one resource contains references to another.
- When allocating the same set of resources in different places in your code, always allocate them in the same order. This will reduce the possibility of deadlock.

### Balancing and Exceptions

For Languages that support exceptions; if an exception is thrown, to guarantee that everything allocated prior to the exception, you can:

- Use variable scope, for example, stack variables in C++ or Rust.
- Use a `finally` clause in a `try…catch` block, for example, in Ruby.

## 27. Don’t Outrun Your Headlights

📖  [whole topic](https://media.pragprog.com/titles/tpp20/dont-outrun-your-headlights.pdf)

We can't see too far ahead into the future, so better <span style="color:lightgreen;">**take small steps always**</span>; checking for feedback and adjusting before proceeding. Consider that the rate of feedback is your speed limit. You never take on a step or a task that’s “too big”.

## Avoid Fortune-Telling 🔮

Just estimate as far ahead as you can see. For that, ensure make code replaceable will also help with cohesion, coupling, and DRY, leading to a better design overall.

# Chapter 5. Bend, or Break

## 28. Decoupling

Coupling occurs anytime when two pieces of code share something. Our code must be flexible, individual components should be coupled to as few other components as possible.  
<span style="color:lightgreen;">**Decoupled code is easier to change**</span> - coupling ties things together, so that it’s harder to change just one thing.

### The Law of Demeter (LoD)

Use Demeter’s law to keep your functions clearer and decoupled. LoD says:
> “An object should avoid invoking methods of an object returned by another method”

Don’t get values from an object, transform them, and then stick them back. Make the object do the work.

Authors from the book express this law in a simple way with the tip <span style="color:lightgreen;">**“Don't chain method calls”**</span>, try not to have more than one dot when you access something.

```java
a.getB().methodB(); //Violated Demeter's law
a.methodB(); //Don't violated Demeter's law
```

### Chains and pipelines

Pipelines transform data, passing it from one function to the next. The difference is that pipelines are not relying on hidden implementation details.  
Pipelines also introduce coupling because the format of the data returned by one function in a pipeline must be compatible with the format accepted by the next.

### Globalization

Global data is available inside every method so changing the implementation of the global, potentially affects all the code in the system.
Any mutable external resource is global data, like database, file system, service API…  
If you really want it to be global, the solution is **wrap it in an API**, make sure you always wrap these resources behind code that you control.

### Inheritance

Subclassing is dangerous → Inheritance Tax ([chapter 31](#31-inheritance-tax))

### Again, it’s all about change

Coupled code is hard to change, make code easy to change and reusable. ♻️

Give clean interfaces decoupling them from the rest of your code.

## 29.  Juggling the Real World

This section talks about **responsive applications**, applications that respond to events, which represent the availability of information.

Strategies to write a responsive application:

1. **Finite state machines**: A state machine is just a specification of how to handle events. It consists of a set of states, one of which is the current state.  

- For each state, we list the events that are significant to that state.
- For each of those events, we define the new current state of the system.

<p align="center">
  <img src=assets/finite_state_machine.svg.png width=200 height=300>  
</p>  

2. **The observer pattern**: we have **observables** (a source of events) and the **observers** (a list of clients who are interested in those events).  
An observer registers its interest with the observable, typically by passing a reference to a function to be called.  
Subsequently, when the event occurs, the observable iterates down its list of observers and calls the function that each passed it.  
The event is given as a parameter to that call.
Used in user interface systems, where the callbacks are used to inform the application that some interaction has occurred.  
Drawbacks:
    1. **Coupling**: each of the observers has to register with the observable
    2. **Performance bottleneck**: because in the typical implementation the callbacks are handled inline by the observable synchronously.  
    <p align="center">
      <img src=assets/observer_pattern.png width=400 height=200>  
    </p>  

3. **PubSub**: is a message-passing system, we have ***publishers*** (write events to channels/topics) and ***subscribers*** (who register interest in one or more channels). Communication between pub and sub is **asynchronous** and is done through channels, which are implemented in a separate body of code (other libraries…)

4. **Reactive Programming, Streams, and Events**
    1. **Reactive Programming** - events are used to trigger reactions in code.
    2. **Streams** - let us treat events as if they were a collection of data (when events arrive, we have a collection of events and we can manipulate, combine, filter…)
    3. **Event streams** - Event streams are normally populated as events occur, which implies that the observables that populate them can run in parallel. Event streams unify synchronous and asynchronous processing behind a common, convenient API.

## 30. Transforming Programming

<span style="color:lightgreen;">**Programming is about code, but programs are about data - all programs transform data, converting an input (what we have) into an output (what we want)**</span>.  
Start designing using transformations. The easiest way to find the transformations is to start with the requirement (a function that represents the overall program) and determine its inputs and outputs.

Pipe operator (`|>`) helps to think in terms of transforming data, seeing a place where data is following between one transformation and the next.

In object-oriented (OO) programming, the idea is to hide data, encapsulating it inside objects. This introduces a lot of coupling, and it is a big reason that OO systems can be hard to change.  
<span style="color:lightgreen;">**Don’t hoard state; pass it around**</span>. Don’t hang on to data within a function or module, take one down and pass it around.  

To manage Error Handling during the state transformations, not pass raw data between transformations, wrap them in a data structure (ex: `{:ok, value}` or `{:error, reason}`). You can handle checking for errors inside your transformations or outside them.  
<span style="color:lightgreen;">**Think in code as a series of (nested) transformations.**</span>

## 31. Inheritance Tax

📖  [whole topic](https://media.pragprog.com/titles/tpp20/inheritance-tax.pdf)  

There are 2 reasons why Object Oriented (OO) developers use inheritance:

1. Don’t link typing, so they add common functionality from a base class into child classes: `class User` and `class Product` are both subclasses of `ActiveRecord::Base`.
2. To express the relationship between classes: a `Car is-a-kind-of Vehicle`.

Problem → **Inheritance is coupling**

The code that uses the child is also coupled to all the ancestors (parent’s parent and so on), so if you change something from the ancestors classes, you could break the child code.  
In the end, diagrams grow and you will have layer-upon-layer adding complexity where it’s hard to change → <span style="color:lightgreen;">**Don't pay inheritance tax.**</span>  
Alternatives to not using inheritance:

1. **Interfaces and protocols**  
Interfaces just specify that any class that implements X interface must implement all methods declared in X interface, but don't dictate how the code should be written. Interfaces and protocols give polymorphism without the coupling introduced by inheritance.

    > Polymorphism: ability by which when calling the same method (example: `sound()`) from different objects (example: `Cat`, `Dog`, `Cow`), each of these objects can respond in a different way (example: "meow", "woof", "moo").
2. **Delegation**  
Delegate to services: has X trumps is X. <span style="color:lightgreen;">**Don’t inherit from services, contain them.**</span>  
Delegation allows split the methods of the class to not rely on the parent class API. We can either write the method directly in the class or create another class that delegates the method that is related to the class.  
In other words, receiving object handles operations by delegating to its delegate, which is a helper object with the original context. Delegation pattern explanations - [page](http://best-practice-software-engineering.ifs.tuwien.ac.at/patterns/delegation.html) and [wiki](https://en.wikipedia.org/wiki/Delegation_pattern).
3. **Mixins** (aka traits, categories, protocol extensions…) - for share functionality.  
Mixins extend classes and objects merging functionality between existing things and new things. Creating a set of these functions, give that set a name, and then somehow extend a class or object with them. At that point, you’ve created a new class or object that combines the capabilities of the original and all its mixins.  
Mixins add functionality to classes without the inheritance tax. Combine with interfaces for painless polymorphism.

## 32. Configuration

Keep values that may change after the application has gone live, **external** to the application → <span style="color:lightgreen;">**Parameterize your app using external configuration.**</span>  
Wrap the configuration information behind a (thin) API to access to this configuration. This decouples your code from the details of the representation of the configuration.  

Benefits of store config data behind service API:

- Multiple applications can share configuration information, with authentication and access control limiting what each can see
- Configuration changes can be made globally
- The configuration data can be maintained via a specialized UI
- The configuration data becomes dynamic
- When configuration values change, there’s no need to rebuild (stop and restart) the app code.  

Make your code adaptable and flexible with external configuration or die.

# Chapter 6. Concurrency

**Concurrency** (software mechanism) is when the execution of two or more pieces of code act as if they run at the same time. To have concurrency, you need to run code in an environment that can switch execution between different parts of your code when it is running. This is often implemented using things such as fibers, threads, and processes.

**Parallelism** (hardware concern) is when they do run at the same time. To have parallelism, you need hardware that can do two things at once. This might be multiple cores in a CPU, multiple CPUs in a computer, or multiple computers connected together.  

Concurrency is a requirement if your application needs to deal with asynchronous things.

## 33. Breaking Temporal Coupling

There are two ways of coupling dependencies and two temporary coupling, which happens when your code imposes a sequence on things that are not required to solve the problem at hand.  

There are two aspects of time that are important to us:

- **concurrency** (things happening at the same time)  
- **ordering** (the relative positions of things in time).  

We need to allow for concurrency and to think about decoupling any time or order dependencies.  
<span style="color:lightgreen;">**Analyze workflow to improve concurrency**</span> - exploit concurrency in your user’s workflow.  
To find out what can happen at the same time, and what must happen in a strict order, we can use a notation such as the activity diagram.
> An activity diagram consists of a set of actions drawn as rounded boxes.  
The arrow leaving an action leads to either another action (which can start once the first action completes) or to a thick line called a synchronization bar.  
Once all the actions leading into a synchronization bar are complete, you can then proceed along any arrows leaving the bar.  
An action with no arrows leading into it can be started at any time.  

<p align="center">
  <img src=assets/activity_diagram_example.png width=300 height=300>  
</p>  

**Opportunity for concurrency**: find activities that take time but not time in our code - things that normally stall our program until they complete; querying a database, accessing an external service, waiting for user input…  

**Opportunity for parallelism**: pieces of work that are relatively independent—where each can proceed without waiting for anything from the others.  
A common pattern is to take a large piece of work, split it into independent chunks, process each in parallel, then combine the results.

## 34. Shared State Is Incorrect State  

📖  [whole topic](https://media.pragprog.com/titles/tpp20/shared-state.pdf)

When several processes are reading and updating a value from a shared memory, neither process can guarantee that its view of that memory is consistent. This is all because fetching and then updating the value is not an atomic operation: the underlying value can change in the middle.

To make it atomic, we can use a **semaphore** 🚦 - a technique where only one process can own at a time and control access to some resource. When both processes run at the same time, one of them will proceed while the other will be suspended until the semaphore becomes available again.  
Not only shared state, but problems can also pop up anywhere where your code shares mutable resources: files, databases, external services, and so on.  Whenever two or more instances of your code can access some resource at the same time, you're looking at a potential problem.

<span style="color:lightgreen;">**Random failures are often concurrency issues**</span>. Variations in timing and context can expose concurrency bugs, but in inconsistent and irreproducible ways. For example, the current directory is shared between threads.

## 35. Actors and Processes

<span style="color:lightgreen;">**Use actors for concurrency without shared state**</span>. It is a way of implementing concurrent state without synchronizing access to shared memory (without a shared state).

- An **actor** is an independent virtual processor with its own local (and private) state.
- A **process** is typically a more general-purpose virtual processor, often implemented by the operating system to facilitate concurrency.

There are a few things that you won't find in the definition of actors:

- There's no single thing that's in control. Nothing schedules what happens next, or orchestrates the transfer of information from the raw data to the final output.
- The only state in the system is held in messages and in the local state of each actor. Messages cannot be examined except by being read by their recipient, and the local state is inaccessible outside the actor.
- All messages are one way, there's no concept of replying.
- An actor processes each message to completion, and only processes one message at a time.  

Actors execute concurrently, asynchronously, and share nothing. There’s no need to write any code to handle concurrency, as there is no shared state. And the code running in the actors is the same, the actors work it out for themselves based on the messages they receive.
> hot-code loading: you can replace code in a running system without stopping that system.

## 36. Blackboards

The **datastore** is active and its **clients** are passive. Therefore the logical flow is determined by the current data status in the data store.  
It has a blackboard component, acting as a central data repository, and an internal representation is built and acted upon by different computational elements (clients).

- A number of components that act independently on the common data structure are stored in the blackboard. Data gathering may be done by different people.
- The components interact only through the blackboard (None of the detectives needs to know of the existence of any other detective)
- The current state of the solution is stored in the blackboard and processing is triggered by the state of the blackboard.
- The system sends notifications, known as trigger, and data to the clients when changes occur in the data. The data store alerts the clients whenever there is a data-store change.
- Responses can arrive in any order.

<span style="color:lightgreen;">**Use blackboards to coordinate workflow.**</span>  
Use blackboards to coordinate disparate facts and agents, while maintaining independence and isolation among participants.  

The actor and/or blackboard and/or microservice approach to architecture removes potential concurrency problems from your applications, but these approaches are harder to reason about because a lot of the action is indirect.  
You'll find it helpful to keep a central repository of message formats and/or APIs (particularly if the repository can generate the code and documentation for you).  
You’ll also need a tool to be able to trace messages and facts as they progress through the system.

# Chapter 7. While You Are Coding

## 37. Listen to Your Lizard Brain

Our instincts, aka the lizard brain 🦎, are simply a response to patterns packed into our nonconscious brain. Some are innate, and others are learned through repetition.  
As you gain experience as a programmer, your brain is laying down layers of tacit knowledge.  
When it feels like your code is pushing back (for example: getting nervous, or feeling like this is just too much work), it’s really your subconscious trying to tell you something’s wrong.  
First to notice it is happening, and then to work out why.

1. Fear of the blank page  
Everyone fears the empty screen, starting a new project, or even a new module. It could be by doubt or because you are afraid that you'll make a mistake. It’s normal because developers put a lot of ourselves into our code: we can take errors in that code as reflections on our competence. Personal advice: read about [Imposter syndrome](https://www.geeksforgeeks.org/imposter-syndrome-in-software-developers-am-i-a-fake-developer/).
2. Fighting yourself  
 When you are coding, the code is trying to tell you something. It's saying that this is harder than it should be. Whatever the reason, your lizard brain is sensing feedback from the code, and it's desperately trying to get you to listen.
3. How to talk lizard  
A. First, stop what you're doing. Give yourself a little time and space to let your brain organize itself. Let the ideas percolate up through the layers of your brain on their own: you can’t force it.  
B. Second, If that's not working, try to externalize the issue by writing a doodle of your code, or talking to your coworker or the [rubber duck](https://www.geeksforgeeks.org/imposter-syndrome-in-software-developers-am-i-a-fake-developer/).  
C. Third, if you are still stuck, then it's time for action by creating a prototype.
4. It's Playtime! → Prototype  
If you're working on existing code and it's pushing back, then stash it away somewhere and prototype something similar instead.  
    1. Write “I’m prototyping” on a sticky note, and stick it on the side of your screen.
    2. Remind yourself that prototypes are meant to fail. There is no downside to doing this.
    3. In your empty editor buffer, create a comment describing in one sentence what you want to learn or do.
    4. Start coding.  
    If you start to have doubts, look at the sticky note.  
    If, in the middle of coding, that nagging doubt suddenly crystallizes into a solid concern, then address it.
5. Not just your code  
You learn to deal with existing code written by other developers asking yourself why they did the code in this way (Not necessarily worse, just different).

## 38. Programming by Coincidence

We should avoid programming by coincidence, relying on luck and accidental successes, in favor of programming deliberately (with intention). Maybe there are routines in the existing code that are not designed to be called in the wrong order or in the wrong context, they seem to work but that's really a coincidence.  
If we don't know why the code is failing because we didn't know why it worked in the first place.  
Human beings are designed to see patterns and causes, even when it's just a coincidence.  

<span style="color:lightgreen;">**Don't assume it, prove it.**</span>
Finding an answer that happens to fit is not the same as the right answer. Assumptions that aren't based on well-established facts are the bane of all projects.

### How to program deliberately

1. Always be aware of what you are doing. Can you explain your code, in detail, to a more Junior developer?
2. Don't code in the dark. If you are not sure why it works, you won't know why it fails.
3. Rely on reliable things, don't depend on assumptions. Document your assumptions, for example using a Design by contract.
4. Test your code and also test your assumptions (Assertive Programming).
5. Prioritize your effort, spend time on the important aspects.
6. Don't be a slave to history. Don't let existing code dictate future code (Refactor).  

> Tips: Use UTC to represent time. And don’t save a phone number in a numeric field, store it in a string field.  

Rely only on reliable things. Beware of accidental complexity, and don’t confuse a happy coincidence with a purposeful plan. So next time something seems to work, but you don’t know why, make sure it isn’t just a coincidence.

## 39. Algorithm Speed

Pragmatic Programmers estimate the resources that algorithms use such as time, processor, memory, and so on.  
Normally, the size of the input will affect the algorithm: the larger the input, the longer the running time, or the more memory used.  
We find that whenever we write anything containing loops or recursive calls, we subconsciously check the runtime and memory requirements.

### Big-O notation

The Big-O notation, written `O()`, is a mathematical way of dealing with approximations (time, memory consumption, etc.).  
Big-O is never going to give you actual numbers for time or memory or whatever: it simply tells you how these values will change as the input changes.

<p align="center">
  <img src=assets/algorithms_runtimes_graphic.png width=350 height=300>  
</p>  

Common sense estimation:

- Simple loops: `O(n)`. Linear, sequential search, for example, the loop runs from 1 to `n`.
- Nested loops: `O(m x n)` → `O(n²)`. For example: sorting algorithms.
- Binary chop: `O(log(n))`. Algorithm which halves the set of inputs considers each time around the loop.
- Divide and conquer: `O(n log(n))`. Algorithms that partition their input, work on the two halves independently, and then combine the result.
- Combinatoric: `O(Cⁿ)`. Algorithm starts looking at the permutations (permutations involve factorials) - Hard problems like the traveling salesman problem.  

### Algorithm speed in practice

<span style="color:lightgreen;">**Estimate the order of your algorithms**</span> (time, memory, etc.).  
Get a feel for how long things are likely to take before you write code.  
If you’re not sure how long your code will take, or how much memory it will use, try running it, varying the input record count, or whatever is likely to impact the runtime. Then plot the results. You’ll get an idea of the shape of the curve (three or four points should give you an idea).  

**Test your estimates**. Mathematical analysis of algorithms doesn’t tell you everything. Try timing your code in its target environment.  

You also need to be pragmatic about choosing appropriate algorithms, <span style="color:lightgreen;">**the fastest one is not always the best for the job.**</span>  
It's always a good idea to make sure if an algorithm is really a bottleneck before investing your precious time trying to improve it.⌛

## 40. Refactoring

<span style="color:lightgreen;">**Code needs to evolve; it's not a static thing.**</span>

Refactoring definition by Martin Fowler:
> “Refactoring is a disciplined technique for restructuring an existing body of code, altering its internal structure without changing its external behavior.”  

To guarantee that the external behavior hasn’t changed, you need to make automated unit testing that validates the behavior of the code.
You should refactor:

- **Duplication.** You've discovered a violation of the DRY (Don't Repeat Yourself) principle.
- **Non Orthogonal design.** You've discovered some code or design that could be made more orthogonal (decoupled).
- **Outdated knowledge.** Things change, requirements drift, and your knowledge of the problem increases. Code needs to keep up.
- **Usage.** Perhaps using the application, you realize now exists other ‘must have’ features.
- **Performance.** You need to move functionality from one area of the system to another to improve performance.
- **The tests pass.** Tidy up tests.  

<span style="color:lightgreen;">**Refactor early, refactor often**</span> because in the future there will be more dependencies and it will be harder. And make sure that the refactor gets placed on the schedule and that users of the affected code know that it is scheduled to be rewritten and how this might affect them. 📅

Martin Fowler offers simple tips to refactor without doing more harm than good:

- Don't try to refactor and add functionality at the same time.
- Make sure you have good tests before you begin refactoring.
- Take short, deliberate steps, and test after each step to avoid prolonged debugging.

## 41. Test to Code

<span style="color:lightgreen;">**Testing is not about finding bugs**</span>, the major benefits of testing happen when you think about and write the tests, not when you run them. 🤔  
Thinking about writing a test for our method made us look at it from the outside as if we are a client of the code, not the author. A test is a perspective into your code, and gives you feedback about its design, api, and coupling. Thinking about testing made us reduce coupling in our code and increase flexibility.  

### Test Driven Development

The basic cycle of TDD ([Test Driven Development](https://en.wikipedia.org/wiki/Test-driven_development)) is:

1. Decide on a small piece of functionality you want to add
2. Write a test that will pass once that functionality is implemented
3. Run all tests. Verify that the only failure is the one you just wrote
4. Write the smallest amount of code needed to get the test to pass and verify it
5. Refactor your code: see if there's a way to improve on what you just wrote, and make sure the test is still passed when you're done

<p align="center">
<img src=assets/tdd.png width=250 height=200> 
</p>

### Build End-to-End, Not Top-Down or Bottom Up

The only way to build software is incrementally. Build small pieces of end-to-end functionality, learning about the problem as you go. Apply this learning as you continue to flesh out the code, involve the customer at each step, and have them guide the process.

Tests can definitely help drive development. But, as with every drive, unless you have a destination in mind, you can end up going in circles. 😵‍💫  

### Back to code

You need to build testability into the software from the very beginning, and test each piece thoroughly (rigorously) before trying to wire them together.

### Unit testing

Test each module, in isolation, to verify its behavior. And when we have the confidence that individual parts work as expected, then we assemble the complete system to test it as a whole.

### Testing against contract

Write test cases that ensure that a given unit honors its contract, this tells us; whether the code meets the contract, and whether the contract means what we think it means.

<span style="color:lightgreen;">**Design to test**</span> - start thinking about testing before you write a line of code.

### Build a test window

Even the best sets of tests are unlikely to find all the bugs. So you'll often need to test a piece of software once it has been deployed with real-world data.
To test in beta or production environments, where you don't have a debugger, you can use:

- Log files containing trace messages are one such mechanism.
- Another mechanism for getting inside running code is the "hot-key" sequence or magic URL, to show a debugging message on the fly or show a diagnostic control window with status messages. Don't reveal it to end-users. 🤫
- Feature switch to enable extra diagnostics for a particular user or class of users. Aka feature flag.

### A culture of testing

Keep tests decoupled, clean, and robust. Remind that tests are also a way of communicating with other developers.  
Test your software, or your users will - test ruthlessly. Don’t make your users find bugs for you.

Testing, design, and coding are all part of programming.

## 42. Property-Based Testing

There could be incorrect assumptions while writing unit tests. The code passes the tests because it does what it is supposed to do, based on your understanding.  
Reminder:  
> In design by contract: The code has contracts that it meets: you meet the conditions when you feed it input, and it will make certain guarantees about the outputs it produces.  
There are also code invariants, things that remain true about some piece of state when it’s passed through a function. For example, if you sort a list, the result will have the same number of elements as the original—the length is invariant.

So you can use contracts and invariants to automate our testing.

<span style="color:lightgreen;">**Use property-based tests to validate your assumptions**</span> - property-based tests will try things you never thought to try, and exercise your code in ways is wasn’t meant to be used.  

One suggestion is that when a property-based test fails, find out what parameters it was passing to the test function, and then use those values to create a separate, regular, unit test.  
This test acts as a regression test because property-based tests generate random values that get passed to your test, there’s no guarantee that the same values will be used the next time you run tests, and in this way, this bug won’t slip through.  

Property-based testing is complementary to unit testing: they address different concerns, and each brings its own benefits.

## 43. Stay Safe Out There

Analyze the code for ways it can go wrong and add those to your test suite, consider passing bad parameters, leaking or unavailable resources, etc.  
Consider how an external actor could deliberately screw up the system (don't think that your system is not important).  

Basic principles that you should always bear in mind:

1. **Minimize attack surface area** - The attack surface area of a system is the sum of all access points where an attacker can enter data, extract data, or invoke the execution of a service. Examples:
      1. Code complexity - Keep your code simple and smaller. Less code means fewer bugs, and fewer opportunities for a crippling security hole.
      2. Input data - Never trust data from an external entity, always sanitize it before passing it on to a database, view rendering, or other processing.
      3. Unauthenticated services - any user anywhere can call unauthenticated services and provoke a DoS (Denial of Service) attack at the very least.
      4. Authenticated services - Keep the number of authorized users at an absolute minimum. Remove unused, old, or outdated users and services.
      5. Output data - ​​Don't give away information that may reveal credential knowledge, for example: "Password is used by another user" or “User does not exist”, better “User or password invalid”.
      6. Debugging info - Make sure any testing window and runtime exception reporting is protected from spying eyes. 🥷

2. **Principle of Least Privilege** - Don't automatically grab the highest permission level, such as *root* or *Administrator*, use the least amount of privilege for the shortest time you can get away with. If needed, then take it, do the minimum amount of work, and relinquish your permission quickly to reduce the risk. And implement in your app different levels of access (*admin*, *PM*, *developer*, *user*, etc.)  

3. **Secure default** - The default settings on your app, or for your users on your site, should be the most secure values.  

4. **Encrypt sensitive data** - Don't leave personally identifiable information, financial data, passwords, or other credentials in plain text. Keys and secrets need to be managed separately, generally via config files or environment variables as part of build and deployment.🔒  

5. **Maintain security updates** - Apply security patches quickly, otherwise know your system is vulnerable to a known exploit because attackers deploy exploits as quick as they can, you have to be quicker.

### Common sense vs. Cryptography

Better use a third-party authentication provider, don't do it yourself.

## 44. Naming Things

How we name things (like apps, subsystems, functions, variables) is important because they express your intent and belief to readers.  
Never use single letter variables (such as `i`, `j`, …)  

It's important that everyone on the team knows what the common names are being used and that they use them consistently. You can spread the jargon by communication like pair programming or creating a project glossary.  

<span style="color:lightgreen;">**Name well; rename when needed**</span> - If you see a name that no longer expresses the intent or is misleading or confusing, rename it.

# Chapter 8. Before The Project

## 45. The Requirements Pit

It’s not enough simply being told what to do or listening to users, you need to dig for the requirements.  
Requirements are buried deep beneath layers of assumptions, misconceptions, and politics. Even worse, often they don’t really exist at all. → <span style="color:lightgreen;">**Don't Gather Requirements—Dig for Them.**</span>

### No one knows exactly what they want

They might know a general direction, but they won’t know the twists and turns. So <span style="color:lightgreen;">**programmers help people understand what they want**</span>.  
Usually, the initial statement of need given by the client is not an absolute requirement, it’s really an invitation to explore. We need to look for edge cases and ask about them.  

Your role in this is to interpret what the client says and to feedback to them the implications. You’re thinking and contributing to a solution.

### Requirements are a process

<span style="color:lightgreen;">**Requirements are learned in a feedback loop.**</span> Understanding requirements requires exploration and feedback, so the consequences of decisions can be used to refine the initial ideas.  
Produce mockups and prototypes and let the client play with them. It’s better to make short iterations that end with client feedback, this makes you sure you are in the right direction and you minimize a lot of time.  

A technique for getting client ideas is to **become a client**, and <span style="color:lightgreen;">**work with a user to think like a user**</span>. It’s the best way to gain insight into how the system will really be used. This will give you feedback and learn their expectations.  

### Requirements vs. Policy

When policy (business policy) changes (and it will!), only the metadata for that system will need to be updated. In fact, gathering requirements in this way naturally leads you to a system that is well factored to support metadata.  
An example of policy could be: “Only supervisors and personnel department may view records from the employees”. But in reality, developer should interpret “Only authorized users may access an employee record” and design some kind of access control system.

<span style="color:lightgreen;">**Think policy as metadata**</span>, think policy information as an example of the type of thing the system needs to support. Don’t hardcode policy into a system; instead express it as metadata used by the system.

Early feedback, with prototypes or tracer bullets, will let your clients say “yes, it does what I want, but not how I want.”

### Document requirements

<span style="color:lightgreen;">**Requirements documents are not for clients.**</span>  
The requirements document is a document understanding of what the client wants.  
It is written for developers and contains information and subtleties that are sometimes incomprehensible and frequently boring to the client.  
It’s needed because developers on a team need to know what they’ll be doing.

<span style="color:lightgreen;">**Requirements documents are for planning.**</span>
They are short descriptions (user stories) that describe what a small portion of the app should do from the perspective of a user of that functionality.  
Keeping this statement of requirements short, you’re encouraging developers to ask clarifying questions. You’re enhancing the feedback process between clients and coders before and during the creation of each piece of code.  
Many project failures are blamed on an increase in scope.  

The key to avoiding that is **feedback** - If you’re working with the client in iterations with constant feedback, then the client will experience first-hand the impact of “just one more feature.” 🙃

### Maintain a project glossary

Create and maintain a project glossary, a single source, that defines all the specific terms and vocabulary used in a project. All participants use the glossary to ensure consistency.

## 46. Solving Impossible Puzzles

<span style="color:lightgreen;">**Don't think outside the box → Find the box.**</span> 📦  
Identify the real (not imagined) constraints, and find a solution therein.  
The key to solving puzzles is both to recognize the constraints placed on you and to recognize the degrees of freedom you do have, for in those you'll find your solution.  
Ask yourself: “Does it have to be done this way? Does it have to be done at all?”  

When you think a problem is “impossible.” - This is an ideal time to do something else for a while. Work on something different or go for a walk.

If not, rubber ducking in practice. Have them ask you questions such as:  
Why are you solving this problem? What’s the benefit of solving it? Are the problems you’re having related to edge cases? Can you eliminate them? Is there a simpler, related problem you can solve?

**Don’t panic** 🧘‍♀️

## 47. Working Together

Working with someone means asking questions and having discussions while you’re actually coding.

- **Pair programming**:  the developer acting as typist must focus on the low-level details of syntax and coding style, while the other developer is free to consider higher-level issues and scope.
- **Mob programming**: like pair programming but with more people (4-5). Can include users, project sponsors, and testers. And the typist swaps out every 5-10 minutes.

<span style="color:lightgreen;">**Don't go into the code alone**</span>. Programming can be difficult and demanding. Take a friend with you.

## 48. The Essence of Agility

Agility is your style, how you do something, not you.  
Values from the [Agile manifesto](https://agilemanifesto.org/), while there is value in the items on the right,
we value the items on the left more:

- **Individuals and interactions** *over processes and tools*
- **Working software** *over comprehensive documentation*
- **Customer collaboration** *over contract negotiation*
- **Responding to change** *over following a plan*

Agility, both in the physical world and in software development, is all about responding to change, responding to the unknowns you encounter after you set out.  
Values are about gathering and responding to feedback.

### So what do we do?

To work in an agile way:

1. Work out where you are.
2. Make the smallest meaningful step towards where you want to be.
3. Evaluate where you end up, and fix anything you broke.

🔁 Repeat these steps until you’re done and use them recursively at every level of everything you do.

This drives design, a good design makes things easy to change. And if it’s easy to change, we can adjust, at every level, without any hesitation. That is agility.

# Chapter 9. Pragmatic Projects

## 49. Pragmatic Teams

You need to establish some ground rules and delegate parts of the project accordingly.

### Maintain small, stable teams

A pragmatic team is small, with under 10-12 or so members. If the team size is large, communication begins to break down and becomes ineffective.  
Teams should stable, where everyone trusts each other and depends on each other.

### No broken windows

Quality is a team issue, quality can come only from the individual contributions of all team members.

### Boiled frogs

People assume that someone else is handling an issue, or that the team leader must have OK'd a change that your user is requesting. Fight this. Encourage everyone to actively monitor the environment for changes.

### Schedule your knowledge portfolio 📅

<span style="color:lightgreen;">**Schedule it to make it happen**</span> - trying to get things done “whenever there’s a free moment” means they will never happen.  
Teams need to consider their knowledge and skill investments as well. Schedule reflection, experimentation, learning and skills improvement.

So don't reserve it for only feature development, the team works in more tasks, like:

- Old systems maintenance
- Process reflection and refinement - continuous improvement
- New tech experiment - don’t adopt new tech, frameworks, or libraries just because “everyone is doing it,” or based on something you saw at a conference or read online. Deliberately vet candidate technologies with prototypes. Put tasks on the schedule to try the new things and analyze the results.
- Learning and skill improvements - learning is more effective when spread team-wide than personal learning. 🧑‍🏫

## Team identity

Generate a team brand helps the team communicate as one - team speaks with one voice to the rest of the organization.

Good communication between teammates is instant and frictionless. Tip - daily meetings.

## Organize fully functional teams

Organize around functionality, not job functions. Don’t separate UI/UX designers from coders, frontend from backend, testers from data modelers, design from deployment. Build teams so you can build code end-to-end, incrementally and iteratively.

## Automation

Make sure the team has skills at tool building to construct and deploy the tools that automate the project development and production deployment.

## 50. Coconuts Don’t Cut It

It’s easy and tempting to fall into the cargo cult trap: by investing in and building up the easily-visible artifacts, you hope to attract the underlying, working magic.  

### Context matters

<span style="color:lightgreen;">**Do what works, not what’s fashionable**</span>. Don’t adopt a development method or technique just because other companies are doing it. Adopt what works for your team, in your context.
Beware if you imitate the form but not the content, like adopting policies and processes of successful companies, think that each company has different context.  
If you want to try something, pilot the idea with a small team or set of teams. Keep the good bits that seem to work well, and discard anything else as waste or overhead.

### The real goal

Deliver when users need it. Don’t wait weeks or months to deliver just because your process demands it.

## 51. Pragmatic Starter Kit

Three critical and interrelated topics:

1. **Version Control**: keep everything needed to build your project under version control, it allows build machines to be ephemeral.  
<span style="color:lightgreen;">**Use version control to drive builds, tests, and releases.**</span> - That is, use commits or pushes to trigger builds, tests, releases, and built in a container in the cloud.  
Release to beta or production is specified by using a tag in your version control system.

2. **Regression Testing**: <span style="color:lightgreen;">**Test early. Test often. Test automatically.**</span>
Tests that run with every build are the most effective.  
The earlier a bug is found, the cheaper it is to remedy. "Code a little, test a little". <span style="color:lightgreen;">**Coding ain't done until all the tests run.**</span>  
“test for real” - the test environment should match the production environment closely. Any gaps are where bugs breed.

    The build may cover:

    - **Unit testing**: code that exercises a module. And later you need to test how all the modules use and interact with each other throughout the system.
    - **Integration testing**: the major subsystems that make up the project, work and play well with each other. Testing how entire subsystems honor their contracts.
    - **Validation and verification**: test if you are delivering what users needs - get user feedback
    - **Performance or stress testing**: the software meets the performance requirements under real-world conditions (is it scalable?).  

    **Testing the tests**: <span style="color:lightgreen;">**Use saboteurs to test your testing**</span>. After you have written a test to detect a particular bug, cause the bug deliberately and make sure the test catch it.  

    **Testing thoroughly**: Testing just lines of code isn’t enough. Coverage analysis tools that watch your code during testing and keep track of which lines of code have been executed and which haven’t (don’t expect to see 100% coverage). But knowing that you executed this line of code doesn’t tell you that—you would need to identify all possible states of the program.  
    So <span style="color:lightgreen;">**Test State Coverage, Not Code Coverage.**</span>  
    Identify and test significant program states. You can test state coverage with Property-Based Testing - a way to explore how your code handles unexpected states is to have a computer generate those states. Use property-based testing techniques to generate test data according to the contracts and invariants of the code under test.  

    **Tightening the Net**: If a bug slips through the net of existing tests, you need to add a new test to trap it next time → <span style="color:lightgreen;">**Find bugs once**</span>

3. **Full Automation**: Bugs would appear on one machine but not on others.  
Tracking down version differences of any one component usually revealed a surprise → <span style="color:lightgreen;">**Don’t use manual procedures**</span>. A shell script or program will execute the same instructions, in the same order, time after time.

## 52. Delight Your Users

Our goal as developers is to delight users. Users have a business problem that needs solving within the context of their objectives and budget.  
<span style="color:lightgreen;">**Delight users, don’t just deliver code**</span>. Develop solutions that produce business value for your users and delight them every day.
Ask a simple question: How will you know that we’ve all been successful a month (or a year, or whatever) after this project is done?  
Once expectations of value behind the project, you can think about how you can deliver against them:

1. Make sure everyone on the team is totally clear about these expectations.
2. When making decisions, think about which path forward moves closer to those expectations.
3. Critically analyze the user requirements in light of the expectations. Don’t be afraid to make suggestions that change the requirement if you can demonstrate that they will move the project closer to the objective.
4. Continue to think about these expectations as you progress through the project.

Our knowledge of the domain increases, and we’re better able to make suggestions. Remind that we solve problems.

## 53. Pride and Prejudice

Don’t shirk from responsibility. Instead, we rejoice in accepting challenges and in making our expertise well known. Treat other people’s code with respect. 🙏

Be proud of your code - sign your work. People should see your name on a piece of code and expect it to be solid, well written, tested, and documented. A really professional job.

# Tips

You can find all the tips [here](https://pragprog.com/tips/)

___

*I have learned many things from this book and I hope it helps you as much as it helped me!* 🤗 🤍

___

Content from The Pragmatic Programmer, 20th Anniversary Edition, by Andrew Hunt and David Thomas.  
Visit [www.pragprog.com](https://pragprog.com/)  
Copyright 2020 by Pearson Education, Inc.
