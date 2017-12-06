---
layout: essay
type: essay
title: Design Patterns and How You Can Stand on the Shoulders of Giants
date: 2017-12-06
labels:
  -design
  -patterns
---

## Introduction to Design Patterns

At some point when reading this essay, it may be beneficial to [familiarize yourself](https://sourcemaking.com/design_patterns) with the different types of design patterns. I'm not gonna explain each pattern individually, as that's not what I want to talk about here, but rather I want to help you understand what design patterns are conceptually, and why you should (or shouldn't) use design patterns in your own software development process.

Back in the old days of programming, when no one knew anything about anything, people solved problems in their own ways, using their own methodology and ideas, sort of how you and me did starting out. If someone asked you to make a basic program that, for example, pulled information from a file line by line, you'd maybe think after some time: "I can use a for loop to go through the file line by line and save that information to an array!" And you'd be right.

Then let's say later down the line, some other guy wants to do the same thing you did (pull information from a file line by line). Instead of him struggling to come up with the algorithm, wouldn't it be easier to tell him: "Hey, you can solve that type of problem by doing something like this!" and you show him your algorithm.

Of course, this is kind of a gross oversimplification of the nature of design patterns, but it gets the concept across. Design patterns can be compared to keys and chord progressions in music. For example, a typical upbeat happy song might use something like the key of C or G, which are particularly keys that contain happy notes, and a I IV V chord progression, which makes the chords C/F/G to form the basic framework of your song. These musical tools are like design patterns because they are tools created by people who already solved the problem of "reading a file line by line," or "writing a happy song," so why not use what they know to solve the same problem instead of having to waste time thinking about a problem that already has a solution?

## How do I Use Design Patterns?

> "OK, you've convinced me. Design patterns are great. But how do I use them?" -You, probably.

In order to show you how to use design patterns, I first want to show you how I used design patterns in developing my own app: [CampusBeats](https://github.com/campusbeats/campusbeats), an app to allow UH Manoa students to connect with each other musically. You can view the GitHub Page [here.](https://campusbeats.github.io/) In this app, I used the following design patterns:

- JavaScript
  - **Prototype** for the Class construction 
- Meteor
  - **Observer** for the publish/subscribe methodology 
  - **MVC** for MongoDB, Blaze, and FlowRouter
  - **Front Controller** for FlowRouter 
- CampusBeats
  - **Singleton** for Collections
  - **Factory** for define methods
  
As you can see, design patterns pop up quite often when developing any sort of program or application. You can use the methodology of design patterns to approach any sort of problem that has already been solved by programmers who came before you.

For example, if you were looking to iterate through a collection, you might rack your brain attempting to look for a solution to implement it. Instead of doing that, you can check out the [Iterator](https://sourcemaking.com/design_patterns/iterator) design pattern and follow the steps presented there to give you a basic jumping-off point for developing your program.

## Beware

However, there are some things you need to be aware of when using design patterns.

1. **You might not understand exactly what you're doing.** Copying doesn't necessarily lead to understanding. It is important to take the steps to understand why the design pattern works for your problem, or even understand that there may be a more efficient solution for the same problem.

2. **Don't feel like you have to cram as many design patterns as possible into your program.** Sometimes design patterns simply don't apply to what you're doing, or it may be easier to take a straightforward approach to the problem and solve it directly rather than attempting to pidgeonhole it into a design pattern. In practice, design patterns are not always relevant, and if you feel it is not so, it probably isn't.

3. **Design patterns don't work the same way for each language.** Some languages don't use design patterns the same way as others. For example, how do you apply a design pattern involving classes or objects to a language that doesn't use them?

4. **Design patterns are not the end all be all of programming.** Sometimes design patterns are more of an inspiration than an actual implementation. The pattern may not be the best solution for your specific problem, even though your problem may fall under or be related to that specific design pattern.

## Conclusion

In conclusion, design patterns can be great for saving time on solving programming problems by applying solution paradigms that already exist rather than coming up with the ideas on your own. However, it is easy to fall into the trap of being "trigger-happy" with design patterns and searching to apply them everywehre you can rather than only when they are relevant. It is important to make this distinction when developing with design patterns, or your code may end up rather haphazard, inefficient, and difficult to understand as compared to a program that was developed in a more straightforward matter. Design patterns can be useful, but only when applied properly in the context to what you are attempting to accomplish.




