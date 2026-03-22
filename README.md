# Key principles in Software – DRY, KISS, YAGNI, SOLID and other Acronyms

March 27, 2022 Nipun Programming, Software Craftsmanship

Software programmers use their own acronyms, some of which are core principles that provide depth and meaning to a software program. This language connects the coders and programmers across continents. It is difficult to find all the acronyms at one place because they are used in wide contexts. We will have a look at some of the important acronyms which are worth learning about. This article will help you to learn their basic concepts, applications, and advantages of the acronyms.

## DRY principle

Don’t Repeat Yourself (DRY) is a very common acronym used by programmers to denote that software programs are created to automate certain repetitive tasks that humans do not wish to waste time and energy. In case you are repeating the same command line in a coding array, there are methods available to reduce or eliminate the repetition completely. An example is given below. Beginners in programming will write the following program if they wish to display a multiplication table of 7 in different lines:

```
println(7 * 1);
println(7 * 2);
println(7 * 3);
println(7 * 4);
println(7 * 5);
println(7 * 6);
println(7 * 7);
println(7 * 8);
println(7 * 9);
println(7 * 10);
```

Supposing, someone wishes to display multiplication table till seven times a hundred, then this would add another 90 lines to the program!

This is where the DRY principle comes into the picture. Why repeat line items in a program when you can write the same program in three lines using the Loop command for n number of repetitions. Hence, the above example may be written as below:

```
for (var i = 1; i < 11; i++) {
println(7 * i);
}
```

Hence you can curb the repetition in coding. This applies to all languages across all platforms. All you need to do is to refer to basic concepts.

There are other applications of the DRY principle which help you create cleaner programming.

* **Avoid Duplication in Comments of code:** Often a developer would use //, *, or # sign to explain the functionality of a code and then start coding. Hence there is a known duplication in the functionality which deviates from the DRY principle. When due to a change in requirement or any other reason, the code must be changed, then comment also must be changed in accordance. This can be avoided by using the layout of the code in the program itself. So, there is no duplication and hence a lower margin for error or omission.
* **Avoid DATA/logic-based duplication:** You may choose to develop better data or logic-based code to avoid duplication. For example, if you wish to create a gaming program where your cursor should move in 4 directions to find a dot to gain points. You may write four lines of the code for each direction (North, east, South, & West) or you may use the move(direction) command to finish off the program in one line code. This is what the DRY principle states.
* **Avoid Algorithm duplication:** This can be avoided easily by analyzing your complete program and its objective. For example, you may have a program to go to Hotel A- then eat, sleep and dance, then go to Hotel B- then eat sleep and dance, then go to Hotel C…..and so on. You should be able to club going to the Hotel activity in the following manner:

```
public void GoToHotel*(Action activity)
{
Eat();
Sleep();
Dance();
}
```

This helps in applying the DRY principle to the algorithm.

These steps help you to avoid Copy Paste Programming.

Opposite of DRY is **WET (Write Everything Twice or Waste Everyone’s Time or We Enjoy Typing)**. The antonym itself indicates the usefulness of the DRY principle in coding.

## KISS Principle

Keep it Simple, Stupid (KISS) term was coined by Late Kelly Johnson, an aeronautical engineer at Lockheed Corporation (Now known as Lockheed Martin). The term was used by Kelly to explain to the Engineers how important it was to keep the design of an aircraft simple. The aircraft had to be repaired quickly in a combat situation and the man in the field should be able to fix the aircraft with the help of basic training and simple design.

This concept is very important in software. Programmers are always asked to avoid complex programming or create difficulties in understanding the code. The Key is to program only as much as is required, neither less nor more.

As the famous French Author and Pilot Antoine de Saint-Exupéry says:

> Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away.

Few ways by which a programmer can reduce complexity:

* The variable names in a program should serve their purpose well. They should be able to define the variable properly
* Method name should also be in line with the purpose for which the method is employed
* As mentioned in an earlier example in the DRY principle, comments in the method should be used only when your program is not able to define the method completely
* Classes should be designed in a way to own a single responsibility
* Delete redundant processes and algorithms as explained during the DRY process

Following are the advantages of applying the KISS principle in coding:

* It is vital to apply the KISS principle when you are working on the modification of an existing codebase. It helps clean the code and make it more readable and editable
* Application of this principle helps in maintaining continuity in the development of a code when the programmer changes.
* KISS principle enhances the efficiency during automated testing of the code.
* Fewer chances of errors during coding.

The following example in iOS programming language SWIFT gives a sneak peek into the application of the KISS principle:

We have a program to display blue color if a logic given is successful, else display red color.

```
if isSuccess {
label.textColor = .blue
} else {
label.textColor = .red
}
```

This same logic may be written using a ternary operator and hence the KISS principle is applied here:

```
label.textColor = isSuccess ? .blue : .red
```

Although usage of ternary operators may make the code complex in some cases, in the above example, they have made the code lighter, easier to understand, and compacted to one line in place of four lines.

A Few more ways are suggested in SWIFT by which you can remove complexity and apply the KISS principle in your code are given below:

* **Usage of Computed property** in place of the complex method as an adequate alternative. Computed properties may be defined as a special kind of property that does not store any value. Instead, they are used to calculate a value based on other properties.
* **Usage of Syntactic Sugars** like firstIndex(where: ), Trailing closures, if-let, etc., to avoid writing verbose codes.
* **Usage of Higher-order functions** which takes one or two other functions as arguments and returns a simpler function as a result. FlatMap, Reduce, and Sorted are examples of Higher-order functions that add simplicity to a code in line with the KISS Principle

## YAGNI (You Aren’t Gonna Need It)

In simple terms, YAGNI as a principle means the removal of unnecessary functionality or logic. The extreme programming practice (XP) founder Ron Jefferies puts it in the following fashion:

“Always implement things when you actually need them, never when you just foresee that you need them.”

Often programmers have a tendency of over-seeing the future and overloading the program with unnecessary logic, algorithms, methods, and codes which will never be used. Some do it as a business requirement and some do it in fear of not being able to incorporate it later when a certain situation arises. A few situations where a programmer should consider following YAGNI are:

* If you are asked to do validation of email and password fields through a program, there is no need to add coding to validate the name field also. You may never need it.
* If a programmer is asked to link different databases of cancer patients of a hospital with a health application, the developer should not consider the hospitals which are already closed. They may never open, and the patient database must have already moved to active hospitals.
* Some programmers may create abstractions even when they are having just one well-defined case in anticipation of the addition of cases. So, they write unnecessary codes and make assumptions about further cases. This should be avoided.
* Use of If-else logic even if the “else” part is always going to be negative in all the test scenarios encountered.

There are a few reasons why programmers choose to violate YAGNI:

1.  **Lack of understanding of the function or business.** Sometimes programmers are not aware of the complete business scenarios. For example, a salesforce software programmer develops accommodative logic for eight different business units in an organization as stated by their mission document. But he/she may not be aware that 3 of them may have got closed. Hence, the exceptions and rules considered for the closed units go waste.
2.  **Too much vision of the future.** This may be due to the over-sightedness of business teams in conveying scenarios that they may never need. It is always advisable to plan for good to have or must have scenarios, but it is foolish to program, I may require it one day type scenarios.
3.  In some cases where it is too expensive to change the coding in the future or it is not advisable to disturb an already cumbersome logic, the developers may choose to violate the YAGNI principle.

The Key to spotting YAGNI codes and nipping them in the development stage itself is a skill that comes with experience only.

## SOLID Principle

The SOLID Principle is an amalgamation of five different software design principles as stated below:

1) Single Responsibility Principle (SRP)
2) Open/Closed Principle (OCP)
3) Liskov Substitution Principle (LSP)
4) Interface Segregation Principle (ISP)
5) Dependency Inversion Principle (DIP)

This concept was initiated by Robert Martin also known as “Uncle Bob”. It is being used for the past many years.

Following are the objectives of applying the SOLID principle in a software program:

* Make it more understandable
* Easy to maintain even if done by other programmers
* Easy to replicate and reuse
* Easy to test. Compatible with Automated Testing
* Flexible to accommodate changes in Scenario

Usage of SOLID concepts differentiates professionals from amateurs. It is vital to learn the concepts and apply them at the right place.

You can read more about more about SOLID Design Principles in this blog post.

## Separation of Concerns (SoC)

The Separation of Concerns principle is simple. It states that a programmer should not write the program as one single block, instead the code should be broken into chunks, such that each component is able to complete a simple distinct job.

In the words of pioneer Dutch Computer Scientist, Edsger W. Dijkstra,

“Separation of Concerns, even if not perfectly possible, is yet the only available technique for effective ordering of one’s thoughts, that I know of.”

This is applicable to many aspects of Software and design as stated below:

* **SoC for Programming functions:** While programming, if you realize that the function being used is getting too voluptuous to handle and it is handling too many arguments, all at once, then it should immediately be segregated into smaller components.
* **SoC for Modules:** Similar to functions, when at a higher level, the functions should be grouped in such a way that they fulfill the desired tasks with a logical co-relation amongst them. Group up the features serving similar functionalities is the Mantra.
* **Cohesion:** When functionally similar codes are grouped together, it is known as increasing cohesion. Example functions like drawRectangle and drawSquare
* **Decoupling:** Sometimes similar-sounding functions with completely different purposes and executions are coupled together in a code. It is advisable to separate them out to achieve a cleaner program.

The key to a successful separation of concern is first to locate the entangled functions which need to be separated for simplicity and to avoid DRY.

At architectural levels, when a programmer is building layered applications, the SoC principle may be applied to segregate Business Logic, data access, and user interface(s).

## MVP- Minimum Viable Product

This is a very interesting concept for developers and their clients. Supposing a client gives a list of features as requirements to be developed by a developer. The developer knows that the client themselves will be able to give a more comprehensive requirement, once they have a working model of the requirements outlined by them. So, the developer goes ahead in developing a pre-cursor module of the final product, maybe with lesser automation, and manual functionalities at the back end. This helps the client in getting the initial taste of how the final product would function. On that basis, the client either gives more mature guidelines or asks the developer to retain the features as per the original vision.

In the words of Steve Blank, the developer who popularized this concept: “You’re selling the vision and delivering the minimum feature set to visionaries, not everyone”

Some people confuse the Minimum Viable product with a prototype. However, there are a few notable differences between MVP and what a developer means by a prototype

* A prototype is a quick fix method to test the basic idea and assumption behind the product, whereas MVP is a usable version of the product with core features, built with minimum money and efforts to act as a test case that results in the generation of feedback and useful data
* Prototype tests the concepts; MVP tests the features as the next step to prototype
* A Prototype is more of the representational or visual appearance of the final product, MVP is functional and can be used in a limited way

MVP term was first used by Frank Robinson in 2001. Later it was popularized by Steve Blank and Eric Ries.

## Proof of Concept (PoC)

Imagine driving for hundreds of miles on a highway and then spotting a Pizza shop. You approach the Pizza outlet, and you want to consume the Pizza. Before investing in the Pizza, you ask the owner about its features and how it can serve your appetite and taste preferences. The owner, in response, hands you over a pamphlet as below:

This pamphlet is analogous to Proof of Concept. It gives you a sneak peek into what you can expect if you order the Pizza and consume it.

Proof of Concept, is also sometimes known as proof of principle in which actions are taken to determine whether an idea is worthy enough, feasible, or possible to be turned into a reality. It also tests the viability of a software product for solving a business need. Compared to a prototype or minimum viable product (MVP), the Proof of Concept is the initial stage document, presentation, or demo prepared to outline the Features and benefits (FAB) of the product and its functions. A prototype and eventually an MVP follows a successful Proof of Concept duly accepted by the client or end user.

While creating the PoC, the following factors need to be kept in mind:

* **Identify the Champions (Key personnel)**- Champion of the cause may be the decision-maker at customer organization, process specialist, technical head, or maybe the finance executive. PoC should be designed as per the audience.
* **Success factors:** Identify the objective of the new requirement, expectations in comparison to the existing setup, time available, the money involved, etc.
* **Collaborate at each step:** Collaborating at each level and each step helps the developer to understand and deliver the requirements better.
* **Understand next steps in the beginning itself:** Clarity on the next steps will always help in creating an acceptable PoC.
* **Continuous improvement through feedback:** A developer should take feedback from their own organization in addition to customer feedback while evolving the PoC.

PoC is all about planning. The more you plan, the associated risks are reduced further, and you can achieve the desired outcome

## DIE (Duplication Is Evil)

This is similar to the DRY (Don’t Repeat Yourself) principle where they encourage to refrain from WET (Write Everything Twice). Specifically, the DIE principal outlines rules for code duplication. Following are the reasons are given to explain the perils associated with code duplication:

* Bugfix recurrence for each duplication in code
* The need to maintain more and more codes
* Occurrence of logical contradictions due to duplications
* Loss of Information or algorithm
* This shows that the programmer is careless and irresponsible.

Following types of duplications are generally observed while coding:

* **Imposed duplication**- A developer is forced to duplicate a code as he/she is left with no other choice as per his/her knowledge levels.
* **Inadvertent duplication**- A developer does not realize that he/she is duplicating a code. It sometimes happens when there are similar fields representing the same concept.
* **Impatient duplication:** A shortcut copy-paste coding activity by the developer to save time or due to boredom
* **Interdeveloper duplication:** Multiple developers working on the same application through shared working spaces or one after another may end up in duplication of efforts.

A proper code review after fixed intervals or milestones can help ward off evils of duplication. Sometimes, techniques like naming, style, and conventions also help in identifying duplications in coding.

## BDUF (Big Design Up Front)

Imagine planning a road trip to the hills near you. Before you finalize the trip, you chalk out the route, weather, ground clearance of vehicle required, food availability, stay arrangements, and best times to visit. Hence before visiting the place, you are fully prepared to undertake the journey. This is similar to the concept of BDUF in software. In this approach, the website, app, or program design is completed much before the implementation begins.

Following are the assumptions before engaging with BDUF:

* We know the requirements of the design and they are not subject to change much
* The design solution is effective
* Developmental challenges can be addressed while the product is still in a developmental stage

Following are the advantages of BDUF:

* Easy to budget, as all costs have been accounted for in the design stage itself
* Easy to develop as product design is already done
* Design leads the development. User requirements are already built-in at the design stage

Following are the pitfalls of using BDUF:

* Difficult to adapt when the client shifts the goalposts.
* Design validation becomes next to impossible due to all parts being functional after development only.

## GIGO- Garbage In, Garbage Out

The name itself is self-explanatory. A computer will always process data based on information input given to it. If the data provided is inaccurate, the results thrown by the computer shall be inaccurate too.

George Feuchsel, an IBM programmer and instructor is attributed to the popularization of the GIGO Concept.

In the words of the Scottish impressionist Rory Bremner:

> “If you put garbage in a computer nothing comes out but garbage. But this garbage, having passed through a very expensive machine, is somehow ennobled and none dare criticize it.” – Rory Bremner
