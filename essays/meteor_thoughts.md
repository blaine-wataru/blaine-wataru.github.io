---
layout: essay
type: essay
title: The Tunguska Event of Web Development (or How I Learned to Use Meteor)
date: 2017-10-19
labels:
  - Software Engineering
  - Meteor
  - Web Application
  - Client
  - Server
---

## Introduction

> The Tunguska Event is a famous explosion that occurred in Siberia in the morning of June 30, 1908. Believed to be an air explosion of possibly some sort of meteoroid, the Tunguska Event is often famous in popular culture as an crash landing an alien spaceship which introduced extraterrestrial technology to Earth.

That's super interesting and all, but what does any of that have to do with [Meteor,](https://www.meteor.com/) the web development platform? Absolutely nothing, to be quite honest (other than the fact that the word "Meteor" is involved). But I guess I would say that the idea of the Tunguska Event as a "first contact" with aliens, can be compared to my introduction to development with Meteor as my "first contact" with web development. And now, I'm gonna tell you guys all about how Meteor introduced me to the world of web development: you'll get to hear about the good times, and the bad times. So what are we waiting for? Let's jump right in.

## Getting Started

When I first downloaded Meteor, I didn't know what to expect. Was Meteor an IDE like IntelliJ or Eclipse ? Was it a client that compiler like gcc or CLISP? Or was it something else entirely? When I downloaded and installed Meteor, I heard from my ICS314 professor that one person had failed to get Meteor running for *weeks.* **WEEKS.** Was that going to be me? What if it was? Was I just going to be royally and completely screwed?

Turns out, that wasn't me. I got Meteor running pretty quickly. I tested it out, learned some things. I wasn't expecting Meteor to be based in the command line, so I got to learn how to use the Windows command prompt. It's definitely worse than Unix. One thing that stood out to me was that "cd" by itself doesn't take you back to home directory. Instead you have to use "cd .." which is kind of annoying and unitituitive. I also hated how much noise came up when using "dir" versus "ls", which cleanly displayed the files in the directory, compared to how messily "dir" does the same thing.

But anyway, I digress. The point is, I got Meteor running with virtually no hiccups whatsoever. Or so I thought.

As I began learning Meteor, I began to notice that it was slow. Like *REALLY* slow. On average, it would take up to 10 minutes (sometimes more) just to run "meteor create" and set up my project. And these were like basic, introductory, beginner projects, with basically nothing in them. By no means did I have a bad computer, so I began to suspect that something was wrong. I talked to other people and looked online, and noticed a bunch of people having the same issues with Meteor speed that I was. And I noticed a common correlation: Windows.

Is this what people mean when they say that Windows sucks for developing? I mean sure, the command line is kind of annoying to use compared to Unix, and that Metro nonsense in Windows 8 was just awful, but I like Windows 10. It works for me, everything that exists has a Windows version, and the UI is intuitive and very standard. But I was worried I would have to make some drastic changes to my setup. Would I have to buy an external SSD? Would I have to dualboot a Linux-based OS? I was hoping it wouldn't come to that (because upgrades and stuff cost time and money), so I looked a little deeper.

It turned out the main issue was package extraction. For whatever reason, the Windows version of Meteor comes with some crappy out-of-date version of 7zip for32-bit Operating Systems, which creates incompatibility issues with the 64-bit Windows 10, causing large amounts of slowdown when running Meteor commands. After updating the 7zip with my own locally installed version, the run times got a lot faster. Unforturnately, it still wasn't very good (10-20+ minutes down to 3-5 minutes), but I wasn't willing to do anything more about it.

I ended up getting Meteor to work properly in it's intended form, and as I became more familiar with the platform, I was ablt to formulate my ideas about it.

## Thoughts?



### Pros
- Reloads in real time
- MongoDB is very simple and easy to use


### Cons
- Command line is confusing, would prefer an actual desktop client
- Really slow and inefficient

## Conclusions


