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