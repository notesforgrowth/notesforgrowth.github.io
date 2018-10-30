---
layout: post
title: Capturing Design Rationale with QOC
author: Steven Clarke
---
One technique I keep coming back to time and time again is that of capturing design rationale in QOC (Questions, Options and Criteria) diagrams.

During any design process, designers ask and answer many questions about the design. At the end of the design process, an artifact is designed or created but the story of how that artifact came into being is often lost. That means any opportunity for learning why the artifact was designed that particular way depends on the availability and the memory of any of the designers involved.

### Questions, Options and Criteria
Over two decades ago, a classic text on design rationale was published: https://www.crcpress.com/Design-Rationale-Concepts-Techniques-and-Use/Moran-Carroll/p/book/9780805815672

The book was fascinating for me as it focused on understanding the design process and the way that design questions are resolved by designers. I loved the focus on the design process, especially since I was a student when the book was published and hadn't yet gained any real practical experience outside of academia. I felt that this book gave me a great insight into how design actually happens.

One chapter in particular that stood out was the second chapter in the first part of the book, "Questions, Options, and Criteria: Elements of Design Space Analysis". This chapter describes a notation for capturing the results of design discussions such that these results can be used to document the design and to ensure that a range of alternative design options are carefully considered and weighed up against each other.

The notation is very simple (it's really just a set of boxes and lines, with lines connecting boxes that contain text descriptions of question, options and criteria). The simplicity of the notation though doesn't really hint at how powerful it can be to use the notation during the design process.

### Simple power
In any design discussion, designers discuss how to resolve some design question. For example, imagine we are designing a new install experience for Visual Studio and are discussing how the user selects the individual components and tools that they want to install. We could simply provide them with a list of all of the components that they can install and allow them to check off each one that they want. That would give them fine grained control over what they want to install but it would make the process of choosing all the components they want considerably time consuming, given that the list of components is large. It could also lead to users making neglecting to choose some particular component which is essential for the type of development that they do (desktop, web, mobile etc)

Alternatively, we could offer a list of workloads or groups of components. These workloads would group together a set of individual components that are relevant to a specific workload or type of development. That way the user focuses on what they want to do (e.g., build a cross platform mobile app) and then selects the workload that is relevant for that task. This selects a set of individual components for them instead of them having to determine which of these components they would need in order to build a cross platform mobile app.

In this design discussion we have one question ("How should developers select the components they want to install?") and two options ("From a list of individual components" and "From a list of workloads"). We have three criteria to evaluate each option with ("Offer fine grained control", "Make users confident they have everything they need", "Decrease amount of time spent in install"). Given this, we can graph this design discussion like so:

![Simple QOC diagram](/images/QOC/simple.png) 

The diagram captures the questions, options and criteria and then visualises the evaluation of each option against each criteria by the use of a solid line to indicate a positive evaluation and a dashed line to indicate a negative evaluation.

The diagram above indicates that during the design discussiuon, the designers considered the option of showing a list of workloads as positive for making users feel confident that they have all the components that they need (since they select a workload and the group of components required for that workload are selected) and for decreasing the amount of time spent in install (since they don't have to check every component in a workload individually). It's considered negative though for providing fine grained control since users can't easily select individual components.

The diagram captures the discussions that happened during the design discussion. By reviewing it after the discussion, the rationale for the final decision that was made can be determined.

### Using QOC during a design discussion
The real power of the QOC notation becomes apparent though when using it during a design discussion, as opposed to once a discussion has happened.

It's quite common during a design discussion to converge very quickly on a solution to a problem. As soon as somebody comes up with an idea, it is very tempting to run with that idea and try to make it work (coming up with good ideas it can be hard to consider alternatives to that idea sin