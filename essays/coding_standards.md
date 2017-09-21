---
layout: essay
type: essay
title: Coding Standards, Arbitrary Nonsense or Readable Perfection?
date: 2017-9-7
labels:
  - Coding Standard
  - ESLint
  - IntelliJ
  - ICS314
---

## Introduction
Coding Standards make no sense. There I said it. "But Blaine, coding standards allow us developers to have a standard for readable code!", you might say. And you'd be right. Kinda.

## Story Time!
In our ICS314 class, we have in-class WODs (see my [initial essay](https://github.com/blaine-wataru/blaine-wataru.github.io/blob/master/essays/JavaScript_Thoughts.md) for details). In a nutshell, we do all-or-nothing programming exercises on Thursdays. Our objective was to change a normal array of string to one with "stutters" (e.g. "apple" -> "a-a-apple"). The main point of it was to follow ESLint coding standards.

I failed it. Do you wanna know why? This fragment of code in my _.map function was why:
```
return _.first(word) + '-' + _.first(word) + '-' + word; 
```
What's wrong with this? Well according to ESLint I needed to use this:
```
'${myVariableHere} myTextHere'
```
What error did I get in IntelliJ? "Unexpected String concatenation (prefer-template)." What's the template? Who knows! 

So, I looked it up and found [this](https://eslint.org/docs/rules/prefer-template), and tried something like this:
```
return '${_.first(word)} - ${_.first(word)} - ${word}'
```
Seems like a reasonable attempt, doesn't it? Wrong. The editor told me I was disallowed to use curly braces in strings. That doesn't make any sense, right? If the example showed I needed to use curly braces inside the single quotes, why was I being denied usage of it here? I later came to the conclusion that Underscore functions weren't allowed in the '${}' notation (if I'm wrong about this please correct me!) when I saw the solution was:
```
return '${word[0]} - ${word[0]} - ${word}
```
How is anyone supposed to know Underscore was not allowed in this format when it is not documented in any way? And furthermore, why does it matter? Is there anything wrong in particular with using _.first over word[0]? ESLint doesn't seem to be able to tell me, that's for sure.

I think my main gripe with this incident was the lack of clarity about the ESLint coding standard. If using Underscore (or rather functions in general) inside of a template literal is wrong, why doesn't the documentation tell you? Coding standards need to be very precise and deliberate. If there are random fringe cases that the editor will mark as incorrect, that are unlisted on the documentation of the actual coding standard, what use is the standard? How is anyone supposed to follow a coding standard if it'll flag you for whatever it chooses to? 

## Thoughts

I don't think coding standards in of themselves are wrong. It's important to have a standard so we as developers can understand and read each others code without having to wade through something like a web of nested if statements when a switch statement would've worked. I myself, have been irritated to read through someone's nonsensical code when something much simpler would've sufficed. But coding standards are not laws, and it makes no sense to subject ourselves to laws which we may not even agree with as a community.

I am a firm advocator of "as long as it works." Coding is tough, no question about that. So why would we lock ourselves away from possible options in the name of coding standards? What if the "incorrect" way makes more sense to read, or results in a faster algorithm, but we have to adapt it to fit some random coding standard written by a guy who has nothing to do with the project?

Let's use an example related to English. Do you think it matters if we use the oxford comma or not? Do you even know what the oxford comma is? What about more obvious things, like starting a sentence with "and" or "because". Or proper placement of punctuation relating to quotation marks? Does any of that make a sentence easier or harder to read? No, right? Sometimes the sentence sounds better when we break these rules. Those are the same kind of limits that improper coding standards can put on us.

If we are going to use coding standards, we need to make sure they are *good* standards, with no arbitrary rules, no weird fringe cases, and no limits on our options. I experienced first hand how it feels to have a solution stuffed (or even just made more difficult to implement) because coding it the way that made sense to me would not have fit the coding standards. And I think that's just unfortunate.

So next time a coding standard tells you to do something, ask yourself, "Why not?" The answer may surprise you. 








