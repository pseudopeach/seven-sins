# The Seven Coding Sins

I find that in software organizations, like all organizations, it’s often more useful to enumerate behaviors that should be avoided, rather than ones that should be followed. There’s a reason why most law systems also work this way. It gives people the freedom to innovate and create without allowing total chaos.
In an attempt to compile my own personal list of software “don’ts”, I started finding myself unconsciously categorizing them. And the way that I was categorizing them seemed to map pretty well to the Seven Deadly Sins of catholic dogma. I thought this interesting because it suggested a certain universality to these rules—like even if they were applied in this case to software development, that they may be extendable to broader life.

## Pride / Vainglory
This was the first connection I drew from Dante to coding. Perhaps because I’ve seen it rear its ugly head so much in the San Francisco community, with all of its outsized egos. Here are the most common examples:
* Rolling your own “better” version of something that’s already become a standard. Like message protocols or testing frameworks.
* Applying some obscure pattern or data structure to something too simple to need it, where it yields some insignificant boost in efficiency, or prepares for some eventual future that won’t likely come to pass.
* Insisting on idealistic “purity” in the codebase—If the only reason for a change is “seems cleaner” you’re probably committing this sin.
* Implementing features no one asked for.
* Clever one-liners and other pretentious erudition in the codebase.

## Gluttony
This one is also pretty obvious. Gluttony means wasteful hunger, so code that needlessly consumes memory or compute-cycles for no good reason. Google and the other large tech companies have become so fixated on time-complexity in their hiring, though, that you don’t see much of this nowadays. It’s the first mistake most people learn to not make in computer science school. In terms of memory however, and at the risk of sounding like the grumpy old man I am: The kids these days are way too used to high-level languages and frameworks that tend to allocate vast swaths of memory for overly-complicated object schemas. People should take a moment to think about what needs to happen under the covers when they `array.push({ id: ‘element-7’  })`.

## Sloth
If I myself am guilty of one of these, it’s sloth. We all know we should:
* Write comprehensive tests
* Refactor and rename pieces of code regularly as requirements change their use
* Remove dead code
* Comment, document
… but we don’t always. Repent ye sinners!

## Lust
Unnatural and disgusting dependencies are usually pretty easy to spot—things like importing a method from the User model into the Message presenter—but there are more ambiguous abominations. There is such a thing as too much code reuse. Adding a 300k-line library to your project just so you don’t have to implement vector addition probably isn’t a good idea if you’re just using it once or twice.

## Wrath
Wrath is all about not letting go of your old grudges. I most commonly see this about tools or languages. An engineer has one bad experience with garbage collection in Java, and then pronounces it a useless language, thereafter avoiding any task, project, or entire company that requires Java. This can have profound negative effects on someone’s career if they meticulously avoid something that becomes ubiquitous. Always keep an open mind and be willing to give things another shot.

## Greed
At some point, every codebase or society becomes too decadent to survive. Where coding is concerned, I’m referring to the breaking of encapsulation by not having objects and methods with a clear, single purpose. A decade of small, incremental changes where someone adds “just one more line” **will** eventually create a hideous spaghetti monster. Telltale signs of greed include:
* Functions that span hundreds of lines
* 5-deep control structures
* God objects
* Tests that take more than 10 minutes to run
* Tables named something that isn’t what they contain

Really the only solution for greed is destruction and rebirth. Every once in a while, you need to burn down a section of your codebase and rebuild it from scratch to reflect the new design requirements of the day. This is where microservices can really shine.

## Envy
Initially, this was the hardest sin for me to place because I was thinking only of actual coding practices. But not all of software engineering is coding, there’s also code review. Envy is usually described as sadness over another’s joy—two need to be involved when it comes to Envy. 

Most of us have had the misfortune of working with that one always-right guy. The one that absolutely can’t resist critiquing every bit of your work he comes across, because he, in his ultimate perfection can always think of a better way. Often over time, his advice even contradicts itself. If you work with this person, you’ll eventually have to quit. To avoid becoming this person, save your feedback for situations in which it really matters, and check your biases before opening your mouth.
