---
layout: essay
type: essay
title: "Learning to Build an Online Portfolio with Techfolios Designer"
date: 2018-08-23
labels:
  - Techfolios Designer
  - Portfolio
  - Onboarding
  - Experience
  - ICS 491
---
## Introduction
Back in my ICS 314 (Software Engineering) class in Fall 2017, I was tasked with building a portfolio online by forking [Techfolios](https://github.com/techfolios/template) and modifying the files myself. This was rather cumbersome and error-prone due to needing to follow specific non-obvious formats, and directly interact with the file base. 

Enter [Techfolios Designer](https://github.com/techfolios/techfoliodesigner) developed primarily by my ICS 314 professor [Phillip Johnson](http://philipmjohnson.org/). Now, for ICS 491, I will also be contributing to the project. By developing for Techfolios Designer, I hope to gain experience with developing desktop applications, and contribute to solving the problem of creating a seemless experience for people to develop their own online portfolios with ease.

## Main Issues

### What Problems can Techfolio Designer Solve?
When creating my Techfolio during ICS 314, I (as well as my classmates) ran into some problems. The main issue we had was with file formatting. 

- **Essay formatting:** When creating an essay or project, the header needed to follow a perfect format or it wouldn't display on the Essays page. The lack of any error log also made it difficult to troubleshoot a potential error, and manually typing or copy/pasting the header made the process extremely error-prone.
- **Bio.json formatting** The JSON format is not obvious, especially for ICS 314 students who have most likely not been exposed to JSON before. JSON is also difficult to debug properly in the GitHub UI and extremely error-prone. In fact, when setting up Techfolio Designer by importing my Techfolio, I found a couple JSON errors that I had not known about prior.

Hopefully Techfolio Designer will be able to address these formatting issues and make implementing a portfolio a smooth and simple experience.

### What Problems does Techfolio Designer Have?
Techfolio Designer, as it is still under development, can definitely be improved. As I tried out and explored the binary release of Techfolio Designer, I noticed a number of issues, bugs, and possible improvements:

- **The Simple Bio Editor's Activities tab does not work, and breaks the functionality of all other tabs.** When I click the tab, nothing happens, and all the other tabs no longer bring me to their respective forms (or do anything at all, in fact) when clicked on. This is a straight-up bug that needs to be fixed. Possibly occurs if the bio.json file contains no Activities section. This may in fact be an issue for all tabs/fields.
- **Error messages are not accurate enough to my liking.** I mainly noticed that the outputs doesn't seem to have any significant form of error messages. For example, when I had the issues with my bio.json format, it would be nice if the in-client editor would identify the issues that existed within my bio.json file. Instead, I had to open the file in IntelliJ and have it tell me where the errors were. Another example is the command log, which doesn't seem to tell me if there are issues with using Git. The log would hang on the "Clone Repo into Directory" step, and I ended up having to ***git pull*** to make sure my local repo was up to date. The best way to solve this would be to have more detailed error logs and error catching.
- **Forced to clone, even if the repo already exists locally.** I already have a local copy of my Techfolio on my machine, yet you still are forced to clone a new repo anyway. This can potentially lead to discrepencies between my original local copy and the clone, not to mention creates a new repo for no reason. Instead it would be nice to be able to select a Techfolio to use and edit directly instead of having to create an unnecessary clone.

I also noticed that Live Reload doesn't seem to be implemented, at least on my machine, as I made a mild change to my local version of the project, and had to restart the application to see it.

### Improving Techfolio Designer
Hopefully as a new developer of Techfolio Designer, I can contribute to the project in a significant way. I am primarily interested in doing backend development, perhaps implementing new features, or writing the test code that this project desperately needs. I also would possibly be interested in improving the usability and clarity of Techfolio Designer to better allow both developers and users to work with the application.





