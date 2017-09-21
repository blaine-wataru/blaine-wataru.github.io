---
layout: essay
type: essay
title: Coding Standards, Arbitrary Nonsense or Readable Perfection?
date: 2017-9-7
labels:
  - Coding Standard
  - ESLint
  - ICS314
---

## Introduction
Coding Standards make no sense. There I said it. "But Blaine, coding standards allow us dvelopers to have a standard for readable code!", you might say. And you'd be right. Kinda.

## Story Time!
In our ICS314 class, we have in-class WODs (see my [initial essay] (https://github.com/blaine-wataru/blaine-wataru.github.io/blob/master/essays/JavaScript_Thoughts.md) for details). In a nutshell, we do all-or-nothing programming exercises on Thursdays. Our objective was to change a normal array of string to one with "stutters" (e.g. "apple" -> "a-a-apple"). The main point of it was to follow ESLint coding standards.

I failed it. Do you wanna know why? This fragment of code in my _.map function was why:
```
return _.first(word) + '-' + _.first(word) + '-' + word; 
```
What's wrong with this? Well according to ESLint I needed to use this:
```
'${myVariableHere} myTextHere'
```
What error did I get in IntelliJ? "Unexpected String concatenation (prefer-template)." What's the template? Who knows! 

So, I looked it up and found (this)[https://eslint.org/docs/rules/prefer-template], and tried something like this:
```
return '${_.first(word)} - ${_.first(word)} - ${word}'
```
Seems like a reasonable attempt, doesn't it? Wrong. The editor told me I was disallowed to use curly braces in strings. That doesn't make any sense, right? If the example showed I needed to use curly braces inside the single quotes, why was I being denied usage of it here? I later came to the conclusion that Underscore functions weren't allowed in the '${}' notation (if I'm wrong about this please correct me!) when I saw the solution was:
```
return '${word[0]} - ${word[0]} - ${word}




