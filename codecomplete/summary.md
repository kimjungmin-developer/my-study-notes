# Chapter 5

- The phrase "software design" means the conception, invention, or contrivance of a scheme for turning a specification for computer software into operational software.
- Design is the activity that links requirments to coding and debuggin
- Programming assignment in school are devised to move you in a beeline from beginning to end
- you'd probably want to tar and feather a teacher who gave you a programming assignment, then chaged the assignment as soon as you finisehd the design and then changed it again just as you were about to turn in the colpleted program. But that very process is an everyday reality in profession programming
- Managing complexity is the most important technical topic in software development. It's so important that Software's Primary Technical Imperative has to be managing complexity
- Dijkstra pointed out that no one's skull is really big enough to contain a modern computer program which means that we as software developers should not try to cram whole programs into our skulls at once; we should try to organize our programs in such a way that we can safely focus on one part of it at a time
- The goal of all software-desing techniques is to break a complicated problem into simple pieces. Ths more independent the subsystems are, the more you make it safe to focus on one bit of complexity at a time
- Writing programs in terms of the problem domain, rather than in terms of low-level implementation details, and working at the highest level of abstraction reduce the load on your brain
- To brake complexity:
  1. Minimal Complexity: Make "simple" and easy to understand designs rather than clever designs
  2. Loose Coupling: Loose coupling meas desiging so that you hold different parts of a program to a minimum. Use the priciples of good abstractions in class interfaces, encapsulation, and information hiding to desing classes with as few interconnections as possible
  3. Extensibility: means that you can enhance a system without causing violence to the underlying structure
  4. Startification: means trying to keep the levels of decomposition stratified so that you can view the system ay any single level and get a consistent view. It compartmentalizes the messiness of the bad code and if you are ever allowed to jettison the old code or refactor it, you won't need to modify any new code excpe the interface layer
- Allow communication between subsystems only on a "need to know" basis - and it had better be a good reason
- SUBSYSTEMS:
  - Business Rules: Business rules are the laws, regulations, policies, and procedures that you encode into a computer system
- Class vs Object: An object is any specific entity that exists in your program at run time. A clss is the static thing you look at in the program listing. An object is the dynamic thing with specific values and attributes when you run the program
- Abstraction is the ability to engage with a concept while safely ignoring some of its details- handling different details at different levels
- Good programmers created abstractions at the routine-interface level, class-interface level, and package-interface-level 
- Abstraction says "you are allowed to look at an object at a high level of detail" Encapsulation says "Futhermore, you are not allowed to look at an object any other level of detail"
- Encapsulation is a way of saying that you can look at the outisde of the house but you cnat get close enough to make out the door's details
- You are allowed to know taht there's a door, and you are allowed to know wheter the door is open or closed
- but you are not allowed to know wheter the door is made of wood, fiberglass, steel, or some other material
- The benefit of inheritance is that it works synergistically with the notion of abstraction
- Abstraction deals with objects at different level of detail.
- The ability of a language to support operations without knowing until run time what kind object you are dealing with is called polymorphism
- Information Hiding : a powerful technique for eliminating rework, and he pointed out that it was particularly effective in incremental, high-change environemnts
- In information hiding, each class is characterized by the desing or construction decisions that it hides from all other classes
- The class's job is to keep this information hidden and to protect its own right to privacy
- Thbe interface to a class should reveal as little as possible about its inner workings
- Two kinds of information hiding: 
  1. Hiding complexity so that your brain does not have to deal with it unless you are specifically concerned with it
  2. Hiding sources of change so that when change occurs, the effects are localized, sources of complexity include complicted data types, file structures, boolean tests, involed algorithms and so on. 
- Information Hiding: the class' interface should protect its secrets
- Coupling describes how tightly a class or a routine is related to other cdlasses or routines. The goal is to create classes and routines with small direct visible and flexivle relations to other classes and routines
- Try to create modules that depend little on other modules. Make them detached as business assoicates are, reather than attached
- Coupling criteria:
  - size: small size is beautiful because it's less work to connec other moduels that a smaller interface
  - visibility: visibility refers to the prominence of the connection between two modules
- Semantic Coupling: the mose insidious kind of coupling occurs when one module makes use not of some syntatice element of another module but of some semantice knowledge of anoter module's inner workings
- Semantic coupling is dangerous because change code in the used module can break code in the using module in ways that are completely undetectable bt the compiler
- When code like this breaks, it breaks the subtle ways taht seem unrelated othe change made in the usde module
- The point of loose coupling is that an effective module provides an additional level of abstraction once you write it, you cna take it for granted
- It reduces overall program complexity and allows you to focus on one thing at a time
- If using a module requires you to focus on more than one thing at once, knowlede of its internal workings modification to global data, uncertain functionality, the abstractive power is lost and module's ability to help manage complexe is gone
- Cohesion refers to how closely all the routines in a class or all the code in a routiune support a central purpose- how focused the class is
- Classes that contain strongly related functionality are described as having strong cohesion, and the heuristic goal is to make cohesion as strong as possible
- A hierarcht is a tiered information structure in which the most general or abstract representation of concepts is contained at the top of the hierarcht, with increasingly detailed, specialized representations at the hierarchy's lower levels
- Desing HEURISTICS:
  - Find Real-World Objects
  - Form Consistent Abstractions
  - Encapsulate Impementation Details
  - Inherit When Possible
  - Hide Secrets
  - Identify Areas Likely To change
  - Keep Coupling Loose
  - Look for Common Desing Patterns

# Chapter 6: Working Classes
- A class is a collection of data and routines that share a cohesive, well-defined resposibility
- Abstract data types are exciting because you can use them to manipulate real-world entities rather than low-level implementation entities
- Tap into the power of being able to work in the probelm domain rather than at the low-level implementation domain!
- Hiding information about the font data type means that if the data type changes, you can change it in one place without affecting the whole program
- The difference is that you have isolated font operations in a set of routines. That provides a better level of abstraction for the rest of your program to work with fonts, and it gives you a layer of protection against changes in font operations
- The first and probably the most important step in creating a high-quality class is creating a good public interface
- The routines should be reorganized into more-foucused classes, each of which provides a better abstraction in its interface
- The idea of abstraction and cohesion are closely related: a class interface that presents a good abstraction usually has strong cohesion
- Classes with stron cohesion tend to present good abstractions, although the relationship is not as strong
- I have found that focusing on the abstraction presented by the class interface tends to provide more insight into class design than focusing on class cohesion
- Abstraction helps to provide manage complexity by providing models that allow you to ignore implementation details.
- Encapsulation is the enforcer that prevents you from looking at the details even if you want to
- Abstraction and encapsulation are related becasue withouch encapsulation abstraction tends to break down
- Exposing member data is a violation of encapsulation and limits your control over the abstraction
- With true encapsulation programmers would not be able to see implementation detail at all. They would be hidden figuratively and literally
- In general, friend classes violate encapsulation => They expand the amount of code you have to think about two at any one time, thereby increasing complexity
- Anytime you find yourself looking at a class's implementation to figure out how to use the class, you are not programming to the interface, you are programming through the interface to the implementation
- Make data type private rather than protected in a base class to make derived classes less tighthly coupled to base class
- Avoid exposing member data in a class's public interface
- Be wary of semantic violations of encapsulation
- Observe the Law Of Demeter
- Containment is the simple idea that a class contains a primitive data element or object
- The number "7 plus minus 2" has been found to be a number of discrete items a person can remember while performing other tasks.
- If a class contains more than about seven data members, consider whether the class should be decomposed into multiple smaller classes
- Inheritance is the idea that one class is a specialization of another class
- The purpose of inheritance is to create simple code by defining a base class that specifies common elements of two or more derived classes
- If the derived class is not goinig to adhere completely to the sam interface contract defined by the base class, inheritace is not the right implementation technique
- Design and codument for inheritance or prohibit it
- LSP: "Subclasses must be usable through the base class interface without the need for the user to know the difference"
- If a program has been written so that the Liskov Substitution Principle is true, inheritacne is a powerful tool for reducing complexity becasue a programmer can focus on the generic attributes of an object without worrying about the details
- If a programmer must be constatly thinking about semantic differences in subclass implementations, then inheritacne is increasing complexity ratther than reducing it
- If multiple classes share common data but not behavior => create a common object that those classes can contain
- If multiple classes share common behavior but not data, derive them from a common base class that defines the common routines
- If multiple classes share common data and behavior => inherit from a common base class that defines the common data and routines
- Inherit when you want the base class to contorl your interface, contain when you wan to control your interface
- A deep copy of an object is a member-wise copy of the object's member data; a shallow copy typically just points to or refers to a single reference copy, although the specific meanings fo "deep" and "shallow" vary
- The single most important reason to create a class is to reduce a program's complexity
- Create a class to hide information so that you won't need to think about it
- you will need to think about it when you write the class but after it's written you should be able to forget the details and use the classs without any knowledge of internal workings
- Isolate complexity by containing in a class
- Code put into well-factored classes can be reused in other programs more easily than the same code embedded in one larger class
- Avoid creating god classes

## Chapter 7: Routines
- The routine makes programs easier to read and easier to understand than any other feature of any programming, and it's a crime to abuse this senior statesmand of computer science with code like that in the example just shown
- Create a routine to hide information so that you won't need to think about it
- to avoid duplication
- A function like ConsineAndTan() has lower cohesion because it tries to do more than one thing => the goal is to have each routine do one thing well and not do anything else
- Functional cohesion is the strongest and best kind of cohesion occuring when a routine performs one and only one operation

## Chapter 8: Defensive Programming
- Exception = the program throwing up its hands and yelling " I don't know what to do about this - I sure hope somebody else knows how to handle it"
- The overriding benefit of exceptions is their ability to signal error conditions in such a way that they cannoy be ignored
- Exceptions should be reserved for conditions that are truly exceptional in other words, for conditions that cannot be addressed by other coding pratices
- Exceptions represent a tradeoff between a powerful way to handle unexpected conditions on the one hand and increased complexity on the other
- Production code should handle errors in a more sophiscated way than "garbage in, garbage out"
- Defensive programming techniques make errors easier to find, easier to fix, and less damaging to production code
- Assertions can help detect errors early, especially in large systems, high reliability systems, and fast-changing code bases
- The decision about how to handle ba inputs is a key error-handling decision
- Excpetion provide a means of handling errors that operates in a different dimension from the normal flow of the code. They are a valuable addition to the programmer's intellectual toolbox when used with care, and tehy should be weighed against other error-processing techniques
- Constraints that apply to the production system do not necessarily apply to the development version. you can use that to your advantage, addiing code to the development version that helps to flush out errors quickly

## Chapter 9: PPP

- Constructing classes and constructing routines tends to be an iterative process.
Insights gained while constructing specific routines tend to ripple back through
the class’s design.
- Writing good pseudocode calls for using understandable English, avoiding features specific to a single programming language, and writing at the level of
intent (describing what the design does rather than how it will do it).
- The Pseudocode Programming Process is a useful tool for detailed design and
makes coding easy. Pseudocode translates directly into comments, ensuring
that the comments are accurate and useful.
- Don’t settle for the first design you think of. Iterate through multiple approaches
in pseudocode and pick the best approach before you begin writing code.
- Check your work at each step, and encourage others to check it too. That way you’ll catch mistakes at the least expensive level, when you’ve invested the least
amount of effort.

## Chpater 10: Variables
- And as with span, the basic advantage of maintaining a low number is that it reduces the window of vulnerability
- you reduce the chance of incorretly or inadvertently altering a variable between the places in which you intend to alter it
- Data initialization is prone to errors, so use the initialization techniques described
in this chapter to avoid the problems caused by unexpected initial values.
- Minimize the scope of each variable. Keep references to a variable close together.
Keep it local to a routine or class. Avoid global data.
- Keep statements that work with the same variables as close together as possible.
- Early binding tends to limit flexibility but minimize complexity. Late binding
tends to increase flexibility but at the price of increased complexity.
- Use each variable for one and only one purpose.

## Chapter 11: The Power of Variable Names
- The most important consideration in naming a variable is that the name fully and accurately describe the variable represents
- Good variable names are a key element of program readability. Specific kinds of
variables such as loop indexes and status variables require specific considerations.
- Names should be as specific as possible. Names that are vague enough or general enough to be used for more than one purpose are usually bad names.
- Naming conventions distinguish among local, class, and global data. They distinguish among type names, named constants, enumerated types, and variables.
- Regardless of the kind of project you’re working on, you should adopt a variable
naming convention. The kind of convention you adopt depends on the size of
your program and the number of people working on it.
- Abbreviations are rarely needed with modern programming languages. If you do
use abbreviations, keep track of abbreviations in a project dictionary or use the
standardized prefixes approach.
- Code is read far more times than it is written. Be sure that the names you choose
favor read-time convenience over write-time convenience.

## Chapter 12: Fundamental Data Types
- Working with specific data types means remembering many individual rules for
each type. Use this chapter’s checklist to make sure that you’ve considered the
common problems.
- Creating your own types makes your programs easier to modify and more selfdocumenting, if your language supports that capability.
- When you create a simple type using typedef or its equivalent, consider whether
you should be creating a new class instead. 

## Chapter 14: Straight Line Code
- Ordering affects readability, performance, and maintainability, and in the absence of execution-order dependencies you can use secondary criteria to determine the order of statements of blocks of code
- The strongest principle for organizing straight-line code is ordering dependencies.
- Dependencies should be made obvious through the use of good routine names,parameter lists, comments, and—if the code is critical enough—housekeeping variables.
- If code doesn’t have order dependencies, keep related statements as close together as possible.

## Chapter 15: Using Conditionals
- Write your code so that the normal path through the code is clear.
- Make sure that the rare cases don't obscure the normal path of execution
- For simple if-else statements, pay attention to the order of the if and else clauses, especially if they process a lot of errors. Make sure the nominal case is clear.
- For if-then-else chains and case statements, choose an order that maximizes readability.
- To trap errors, use the default clause in a case statement or the last else in a chain of if-then-else
statements.
- All control constructs are not created equal. Choose the control construct that’s most appropriate for each section of code.

## Chapter 16: Conditional Loops
- Loops are complicated. Keeping them simple helps readers of your code.
- Techniques for keeping loops simple include avoiding
exotic kinds of loops, minimizing nesting, making
entries and exits clear, and keeping housekeeping
code in one place.
- Loop indexes are subjected to a great deal of abuse.
Name them clearly, and use them for only one purpose.
- Think through the loop carefully to verify that it operates normally under each case and terminates under all possible conditions.

## Chpater 17: Unusual Control Structures
- Multiple returns can enhance a routine’s readability and maintainability, and they help prevent deeply nested logic. They should, nevertheless, be used carefully.
- Recursion provides elegant solutions to a small set of problems. Use it carefully, too.
- In a few cases, gotos are the best way to write code that’s readable and maintainable. Such cases are rare. Use gotos only as a last resort.

## Chapter 18: Table-Driven Methods
- Tables provide an alternative to complicated logic and inheritance structures. If you find that you’re confused by a program’s logic or inheritance tree, ask yourself whether you could simplify by using a lookup table.
- One key consideration in using a table is deciding how to access the table. You can access tables by using direct access, indexed access, or stair-step access.
- Another key consideration in using a table is deciding what exactly to put into the table.

## Chapter 22: Developer Testing
- Unit testing is the execution of a complete class, routine, or small program that has been written by a single programmer or team of programmers, which is tested in isolation from the more complete system
- Component testing is the execution of a class, package, small program, or other program element that involves the work of multiple programmers or programming teams, which is tested in isolatrion from the more complete system
- Integration testing is the combined executiuon of two or more classes, packages components, or subsystems that have been created by multiple programmers, or programming teams. This kind of testing typically starts as soon as there are two classes to test and continues until the entire system is complete
- Writing test cases before writing the code does not take any more effort thatn writing test cases after the code; it simlply resequences the test-case-writing activity.
- Data-Flow-Testing: Data-flow testing is based on the idea that data usage is at least as error-prone as control flow
Testing by the developer is a key part of a full testing strategy. Independent testing is also important but is outside the scope of this book.
- Writing test cases before the code takes the same amount of time and effort as
writing the test cases after the code, but it shortens defect-detection-debug-correction cycles.
- Even considering the numerous kinds of testing available, testing is only one
part of a good software-quality program. High-quality development methods,including minimizing defects in requirements and design, are at least as important.
- Collaborative development practices are also at least as effective at detecting errors as testing, and these practices detect different kinds of errors.
- You can generate many test cases deterministically by using basis testing, dataflow analysis, boundary analysis, classes of bad data, and classes of good data.You can generate additional test cases with error guessing.
- Errors tend to cluster in a few error-prone classes and routines. Find that errorprone code, redesign it, and rewrite it.
- Test data tends to have a higher error density than the code being tested.
- Because hunting for such errors wastes time without improving the code, testdata errors are more aggravating than programming errors. Avoid them by
developing your tests as carefully as your code.
- Automated testing is useful in general and is essential for regression testing.
- In the long run, the best way to improve your testing process is to make it regular, measure it, and use what you learn to improve it.

## Chapter 23: Debugging
- Debugging is a make-or-break aspect of software development. The best
approach is to use other techniques described in this book to avoid defects in
the first place. It’s still worth your time to improve your debugging skills, however, because the difference between good and poor debugging performance is
at least 10 to 1.
- A systematic approach to finding and fixing errors is critical to success. Focus your debugging so that each test moves you a step forward. Use the Scientific
Method of Debugging.
- Understand the root problem before you fix the program. Random guesses about the sources of errors and random corrections will leave the program in worse condition than when you started.
- Set your compiler warning to the pickiest level possible, and fix the errors it reports. It’s hard to fix subtle errors if you ignore the obvious ones.
- Debugging tools are powerful aids to software development. Find them and use them, and remember to use your brain at the same time.

## Chapter 24: Introduction to Refactoring
- Reasons to refactor:
  1. Code is duplicated: Duplicated code almost always represents a failure to fully factor the design in the first place. Duplicate code sets you up to make parallel modifications-whenever you make changes in one place, you have to make parallel changes in another place.
  2. A routine is too long: In object-oriented programming, routines longer than a screen are rarely needed and usually represent the attempt to force-fit a strucutred programming foot into an object-oriented shoe
  3. A loop is too long or too deeply nested: Loop innards tend to be good candidates for being converted into routines, which helps to better factor the code and to reduce the loop's complexity
  4. A class has poor cohesion: If you find a class that takes ownership for a hodgepdoge of unrelated responsibilities, that class should be broken up into multiple classes
  5. A class interface does not provide a consistent level of abstraction: Even classes that begin life with a cohesive interface can lose their original consistency
  6. A parameter list has too many parameters: well-facotred programs tend to have many small, well-defined routines that don't need large parameter lists
  7. Changes within a class tend to be compartmentalized: Sometimes a class has two or more distince resposibilities
  8. A primitive data type is overloaded: Primitive data types can be used to represent an infinite number of real world entities. If your program uses a primitive data type like Monely class so that the compiler can perform type checking on Money variables, so that you can add safety checks on the values assigned to money, and so on. If Money and Temperature are integers, the compiler won't warn you about erroneous assignment like bankBalance=recordLowTemperature.
  9. A class does not do very much: Sometimes the result of refactoring code is that an olde class does not have much to do
  10. One class is over intimate with another: Encapsulation(information hiding) is probably the strongest tool you have to make your program intellectually manageable and to minimize ripple effects of code change. Anytime you see one class that knows more about another class than it should - including derived classes knowing too much about their parents- err onn the side of stronger encapsulation rather than weaker Data members are public: public data members are in my view always a bad idea. They blur the line between interface and implementation
  12. A subclass uses only a small percentage of its parents' routines: typically this indicates that that subclass has been created because a parent class happened to contain the routines it needed, not because the subclass is logically a descendant of the super-class
  13. Comments are used to explain: Comments have an important role to play, but they should not be used as a crutch to explain bad code
- Class implementation Refactoring:
  1. Change value objects to reference objects: if so large make reference object
- Class interface refactoring:
  1. Convert one class to two: If a class has two or more distince area of responsibility, break the class into multiple classes, each of which has a clearly defined responsibility
  2. Replace inheritance with delegation: If a class needs to use another class but wants more control over its interface, make the supercalss a field of the former subclass and then expose a set of routines that will provide a cohesive abstraction
  3. Replace delegation with inheritance: If a class exposes every public routine a delegate calss, inherit from the delegate class instead of just using the class
- Refactoring techniques:
  1. Define an interface between clean code and ugle code, and then move code across the interface: The real world is often messier than you'd like. The messiness might come from complicated business rules, hardware interfaces, or software interfaces. A common problem with geriatric systems is poorly written production code that must remian operation at all times => an effective strategy for rejuvenating geriatric production system is to designate some code as being in the messy real world, some as being in an idealized new world, and some code as being the interface between the two
- Program changes are a fact of life both during initial development and after initial release.
- Software can either improve or degrade as it’s changed. The Cardinal Rule of
Software Evolution is that internal quality should improve with code evolution.
- One key to success in refactoring is learning to pay attention to the numerous
warning signs or smells that indicate a need to refactor.
- Another key to refactoring success is learning numerous specific refactorings.
- A final key to success is having a strategy for refactoring safely. Some refactoring
approaches are better than others.
- Refactoring during development is the best chance you’ll get to improve your
program, to make all the changes you’ll wish you’d made the first time. Take
advantage of these opportunities during development!

## Chapter 25: Code-Tuning Strategies
- One common source of inefficiency: one of the most significant sources of inefficiency is unnecesary input/output. If you have a choice of working witha file memory vs. on disk, in a database, or across a network, use an in-memory data strucutre unleess space is critical

- You should take the following steps as you consider whether code tuning can help
- you improve the performance of a program:
  1. Develop the software by using well-designed code that’s easy to understand and
  modify.
  2. If performance is poor,
    a. Save a working version of the code so that you can get back to the “last
    known good state.”
    b. Measure the system to find hot spots.
    c. Determine whether the weak performance comes from inadequate design,
    data types, or algorithms and whether code tuning is appropriate. If code
    tuning isn’t appropriate, go back to step 1.
    d. Tune the bottleneck identified in step (c).
    e. Measure each improvement one at a time.
    f. If an improvement doesn’t improve the code, revert to the code saved in
    step (a). (Typically, more than half the attempted tunings will produceonly a negligible improvement in performance or degrade performance.)
  3. Repeat from step at 2

- Performance is only one aspect of overall software quality, and it’s usually not the most important. Finely tuned code is only one aspect of overall performance, and it’s usually not the most significant. Program architecture, detailed design, and data-structure and algorithm selection usually have more influence on a program’s execution speed and size than the efficiency of its code does.
- Quantitative measurement is a key to maximizing performance. It’s needed to find the areas in which performance improvements will really count, and it’s needed again to verify that optimizations improve rather than degrade the software.
- Most programs spend most of their time in a small fraction of their code. You won’t know which code that is until you measure it.
- Multiple iterations are usually needed to achieve desired performance improvements through code tuning.
- The best way to prepare for performance work during initial coding is to write clean code that’s easy to understand and modify.

## Chapter 26: Code-Tuning Techniques
- In some circumstances, a table look up might be quicker than traversing a complicated chain of logic. The point of a complicated chain is usually to categorize something and then to take an action based on its category
- Use integers rather than floats
- Usee gewest array dimenssions
- Minimize working in a loop
- Use Cacheing
- Results of optimizations vary widely with different languages, compilers, and
environments. Without measuring each specific optimization, you’ll have no
idea whether it will help or hurt your program.
- The first optimization is often not the best. Even after you find a good one, keep
looking for one that’s better.
- Code tuning is a little like nuclear energy. It’s a controversial, emotional topic.
Some people think it’s so detrimental to reliability and maintainability that they
won’t do it at all. Others think that with proper safeguards, it’s beneficial. If you
decide to use the techniques in this chapter, apply them with care.

## Chapter 27: How Program Size affects Construction
- As project size increases, communication needs to be supported. The point of
most methodologies is to reduce communications problems, and a methodology should live or die on its merits as a communication facilitator.
- All other things being equal, productivity will be lower on a large project than on
a small one.
- All other things being equal, a large project will have more errors per thousand
lines of code than a small one.
- Activities that are taken for granted on small projects must be carefully planned
on larger ones. Construction becomes less predominant as project size
increases.
- Scaling up a lightweight methodology tends to work better than scaling down a
heavyweight methodology. The most effective approach of all is using a “rightweight” methodology.

## Chpater 28: Managing Construction
- Assign two people to every part of the project: If two people have to work on each line of code, you will gurantee that at least two people think it works and is readable
- Review every line of code: A code review typically involves the programmer and at leat two reviewers. That means that at least three people read every line of code. Keep up the standard
- Require code sign-offs: Before code is considered to be complete, senior technical personnel mush sign the code listing
- One way to communicate your objects is to circulate good code yo your programmers or post it for public display
- Good coding practices can be achieved either through enforced standards or
through more light-handed approaches.
- Configuration management, when properly applied, makes programmers’ jobs
easier. This especially includes change control.
- Good software estimation is a significant challenge. Keys to success are using
multiple approaches, tightening down your estimates as you work your way into
the project, and making use of data to create the estimates.
- Measurement is a key to successful construction management. You can find
ways to measure any aspect of a project that are better than not measuring it at
all. Accurate measurement is a key to accurate scheduling, to quality control,
and to improving your development process.
- Programmers and managers are people, and they work best when treated as
such.

## Chapter 29: Integration
- Integration: the software-development activity in which you combine separate components into a single system
- Phased Integration:
  1. Design, code, test, debug each class => unit development
  2. Combine the classes into one whopping-big system => system integration
  3. Test and debug the whole system. This is called "system dis-integration)
- One problem with pahsed integration is when classes in a system are put together for the first time, new problems inevitably surface and the causes of the problems could be anywhere
- Incremental integration:
  1. Devleop a small functiona part of the system. It can be the smallest functional part, the hardest part, a key part, or some combination. Thoroughly test and debug it. It will serve as a skeleton on which to hang the muscles nerves and skin 
  2. Desing cod etest and debug a calss
  3. Integrate the new class with the skeleton. TEst and debug the combination of skeleton and new class. Make sure the combination works befor you add any new classes. if work remains to be done, repeat the prcess starting at step 2
  - Errors are easier to locate
  - the system succeeds early in the project
  - get improved progress monitoring
  - mroe comple unit-tests
  - top-down incremnetal integration: the class at the top of the hierachy is written and integrated first. interfaces between classes must be carefully specified but pure top-down integration leaves exercising the tricky system interfaces until last
  - bottom-up incremental integration: Adding the low level classes one at a time rather than all at once is what makes botoom-up integration an incremental startegy. bottom-up integration provides a limited set of incremental integration advantages, it restricts the possible sources of error to the single class being integrated, so errors are easy to locate. Desing has to be complete the whole design could be wrong
  - Sandwich integration: You first integrate the high-level business-object classes at the top of the hierarchy. Then you integrate the device-interface calsses and widely used utility classes at the bottom. These high-level and low-level classes are the bread of the sandwich
  - Feature-oriented integration: the term feature does not refer to anything fancy, just an identifiable function of the system you are integrating. if you are writing a word processor, a feature might be displaying underlining on the screen on reformatiing the document automatically 
  - Continuous-Integration: at-least daily integration

- The construction sequence and integration approach affect the order in which
classes are designed, coded, and tested.
- A well-thought-out integration order reduces testing effort and eases debugging.
- Incremental integration comes in several varieties, and, unless the project is trivial, any one of them is better than phased integration.
- The best integration approach for any specific project is usually a combination
of top-down, bottom-up, risk-oriented, and other integration approaches. Tshaped integration and vertical-slice integration are two approaches that often
work well.
- Daily builds can reduce integration problems, improve developer morale, and
provide useful project management information.

## Chapter 31: Layout and Style
- The fundamental theorem of formatting says that good visual layout shows  the logical structure of a program
- Making the code look pretty is worth something, but it's worth less than showing the code's strucutre. If one technique shows the structure better and another looks better, use the one that shows the strucutre better.
- Imporves readability
- The first priority of visual layout is to illuminate the logical organization of the
code. Criteria used to assess whether that priority is achieved include accuracy,
consistency, readability, and maintainability.
- Looking good is secondary to the other criteria—a distant second. If the other
criteria are met and the underlying code is good, however, the layout will look
fine.
- Visual Basic has pure blocks and the conventional practice in Java is to use pureblock style, so you can use a pure-block layout if you program in those languages. In C++, either pure-block emulation or begin-end block boundaries work
well.
- Structuring code is important for its own sake. The specific convention you follow is less important than the fact that you follow some convention consistently. A layout convention that’s followed inconsistently can actually hurt readability.
- Many aspects of layout are religious issues. Try to separate objective preferences
from subjective ones. Use explicit criteria to help ground your discussions about
style preferences.

## Chpater 32: Self-Documenting Code
- The main contributor to code-level documentation is not comments, but good programming style
- Styple includes good program structure, use of straightforward and easily understandable approaches, good variable names, good routine names, use of name constatns instead of literals, clear layout, and minimization of control-flow and data-structure complexity
- Endline comments are useful for annotating data declarations because they dont have the same systemic problems as endlie comments on code
- Overview comments that provide information that cannot readily be reverse-engineered form coding details are especially useful
- Similar to routines, be sure to describe any limitations imposed by the class's design
- The question of whether to comment is a legitimate one. Done poorly, commenting is a waste of time and sometimes harmful. Done well, commenting is
worthwhile.
- The source code should contain most of the critical information about the program. As long as the program is running, the source code is more likely than any
other resource to be kept current, and it’s useful to have important information
bundled with the code.
- Good code is its own best documentation. If the code is bad enough to require
extensive comments, try first to improve the code so that it doesn’t need extensive comments.
- Comments should say things about the code that the code can’t say about
itself—at the summary level or the intent level.
- Some commenting styles require a lot of tedious clerical work. Develop a style
that’s easy to maintain

## Chapter 33: Personal Character
- Your personal character directly affects your ability to write computer programs.
- The characteristics that matter most are humility, curiosity, intellectual honesty,
creativity and discipline, and enlightened laziness.
- The characteristics of a superior programmer have almost nothing to do with
talent and everything to do with a commitment to personal development.
- Surprisingly, raw intelligence, experience, persistence, and guts hurt as much as
they help.
- Many programmers don’t actively seek new information and techniques and
instead rely on accidental, on-the-job exposure to new information. If you
devote a small percentage of your time to reading and learning about programming, after a few months or years you’ll dramatically distinguish yourself from
the programming mainstream.
- Good character is mainly a matter of having the right habits. To be a great
programmer, develop the right habits and the rest will come naturally.

## Chapter 34: Themes in Software Craftsmanship
- The drive to reduce complexity is at the heart of software development:
  1. Dividing a system into subsystems at the architecture level so that your brain
  can focus on a smaller amount of the system at one time.
  2. Carefully defining class interfaces so that you can ignore the internal workings of the class.
  3. Preserving the abstraction represented by the class interface so that your brain
  doesn’t have to remember arbitrary details.
  4. Avoiding global data, because global data vastly increases the percentage of the code you need to juggle in your brain at any one time.
  5. Avoiding deep inheritance hierarchies because they are intellectually demanding.
  6. Avoiding deep nesting of loops and conditionals because they can be replaced by simpler control structures that burn up fewer gray cells.
  7. Avoiding gotos because they introduce nonlinearity that has been found to be difficult for most people to follow.
  8. Carefully defining your approach to error handling rather than using an arbitrary proliferation of different error-handling techniques.
  9. Being systematic about the use of the built-in exception mechanism, which can
  become a nonlinear control structure that’s about as hard to understand as gotos
  if not used with discipline.
  10. Not allowing classes to grow into monster classes that amount to whole programs in themselves.
  11. Keeping routines short.
  12. Using clear, self-explanatory variable names so that your brain doesn’t have to
  waste cycles remembering details like “i stands for the account index, and j
  stands for the customer index, or was it the other way around?”
  13. Minimizing the number of parameters passed to a routine, or, more important,
  passing only the parameters needed to preserve the routine interface’s abstraction.
  14. Using conventions to spare your brain the challenge of remembering arbitrary,
  accidental differences between different sections of code.
  15. In general, attacking what Chapter 5 describes as “accidental difficulties” wherever possible.