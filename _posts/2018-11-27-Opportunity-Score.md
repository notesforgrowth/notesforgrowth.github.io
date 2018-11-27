---
layout: post
title: What is the Opportunity Score?
author: JP Carrascal
---

The Opportunity Score is a tool that helps (among other things) to estimate market opportunity, to prioritize efforts in product development and to conduct competitive analysis. It is part of the _Opportunity-Driven Innovation_ framework created by Anthony W. Ulwick, that aims at "making innovation predictable". This article focuses specifically on the Opportunity Score calculation. Bear in mind it is not a silver bullet, and if you want to use properly, you should probably read a bit more on the Opportunity-Driven Innovation process to get the whole picture. To help with that, I have included a few links in the "Further Reading" section at the end of the article.

<style>
table{
    border-collapse: collapse;
    border-spacing: 0;
    border:2px solid #000000;
}

th{
    border:2px solid #000000;
    font-size: 0.8em;
}

td{
    border:1px solid #000000;
    padding: 5px;
    font-size: 0.8em;
}

.caption
{
  font-size: 0.8em;
}
</style>

## Background

Ulwick's work on Opportunity-Driven Innovation (ODI) is based on the idea that customers mainly pay to get a _job-to-be-done_. This means people do not actually care about tools, features or specs, what they care about is achieving a goal (this is nicely explained by Prof. Clayton Christensen in [this video](https://www.youtube.com/watch?v=Q63PZR7mG70)). If a product of service helps customers to achieve the goal (to get a job done), they will pay for it. Ulwick says that deeply understanding the customers' job-to-be-done is necessary to predict whether a product will be successfull, that is, people will pay for it. The ODI framework is a systematic approach towards analyzing jobs-to-be-done to decide whether to invest on a certain design space, and how to prioritize such investment. Analyzing a job-to-be-done is usually the result of deep qualitative research with customers (e.g. interviews). BTW, according to Ulwick, jobs-to-be-done generally don't change across time. This might be suggested by the example below.

## The Opportunity Score

The main metric used in the ODI framework is the Opportunity Score. This is the result of an [analysis of the gap](https://en.wikipedia.org/wiki/Gap_analysis) between the importance that customers assign to the expected outcomes of a job-to-be-done, and how satisfied they are with their current solutions.

Once a job-to-be-done has been understood, it should be broken down the into smaller job steps, and for each step, a series of _outcomes_ (as expected or desired by customers) should be enunciated. For instance, a job-to-be-done could be:

>  Surviving grad school.

And the steps and outcomes of this job-to-be-done and their outcomes could be:


| __Job step__                    | __Outcomes__                                        |
|---------------------------------|-----------------------------------------------------|
| Academic duties                 | Writing papers                                      | 
|                                 | Getting submitted paper accepted                    |
|                                 | Completing homework                                 |
|                                 | Passing exams                                       |
|                                 | Supervising master students                         |
|---------------------------------|-----------------------------------------------------|
| Daily activities                | Getting out of bed                                  |
|                                 | Having coffee                                       |
|                                 | Discreet napping                                    |
|                                 | Finding cheap food                                  |
|---------------------------------|-----------------------------------------------------|
| Spare time                      | Finding time to relax                               |
|                                 | Fleeing from meetings                               |
|                                 | Hiding from professors                              |

### Collecting the data
To obtain the Opportunity Score for each outcome, you first need to collect data from your customers about the desired outcomes. You should ask customers two questions:

1. __Importance:__ _When [job step], how __important__ is it to you that you are able to [outcome]?_ (1 to 5 scale, 1 = "Not at all important", 5 = "Extremely important")
2. __Satisfaction:__ _When using [solution], how __satisfied__ are you with your ability to [outcome]?_ (1 to 5 scale, 1 = "Not at all satisfied", 5 = "Extremely satisfied")

Where [solution] is the solution that the customer currently uses to get the job done.

### Computing the score

This is pretty easy:

1. Compute the _percentage of respondents who answered 4 or 5__ to both __importance__ (that is those who said the outcome is "Important" or "Extremely important") and __satisfaction__ (those who said they are "Satisfied" or "Extremely satisfied").

2. Insert these percentages in the Opportunity Score formula:


> ```OpScore = Importance + max(Importance - Satisfaction, 0)```

I made up some answer values for the "listening to music" example:

| __Outcomes__ | __Importance (%==4 or 5)__ | __Satisfaction (%==4 or 5)__ | __OpScore__ |
| Writing papers | 6.7 | 7.6 | 12.4 |
| Getting submitted paper accepted | 7.7 | 7.7 | 13.5 |
| Completing homework | 9.7 | 9.7 | 15.4 |
| Passing exams | 8.6 | 10.0 | 14.3 |
| Supervising master students | 3.3 | 3.3 | 9.1 |
| Getting out of bed | 9.6 | 9.2 | 15.4 |
| Having coffee | 9.0 | 9.3 | 14.8 |
| Discreet napping | 5.7 | 7.8 | 11.4 |
| Finding cheap food | 7.6 | 4.1 | 13.4 |
| Finding time to relax | 8.5 | 2.7 | 14.2 |
| Fleeing from meetings | 8.9 | 8.9 | 14.7 |
| Hiding from professors | 9.0 | 8.0 | 14.8 |

_NOTE: Ulwick normalizes the percentages to 10 instead of 100. I'm not sure why, but this sometimes leads to confusion as the first impulse is to normalize the 1-5 question scale to 10 (by multipliying by 2)._

### Interpreting the results

To interpret the OpScore results, data is usually plotted on a graph like this one:

<p style="text-align:center">
<img src="/images/Opportunity-Score/OpportunityLandscape.jpg" style="width:80%;"/>
<span class="caption">The "Opportunity Landscape". Data from the example was overlaid on a scan from the book.</span>
</p>

The graph illustrates how well customers' needs are satisfied with current solutions. It helps to indicate prioritization strategies for improving existing products or creating new ones. The _Overserved_ area suggests there is not much room for innovation and the way to compete there is mainly by offering a lower-priced solution. On the opposite side, the _Underserved_ area indicates there are stronger opportunities to innovate as there are a lot of important unsatisfied needs. People will be willing to pay more to have these needs solved. The upper right corner area represents needs that are important but are currently well satisfied. Ulwick indicate thet these are "table stakes" that necessarily must be be served if one considers developing a competitive product. 

Another interesting application of the opportunity score is for conducting competitive analysis. Breaking down features of two competing products (which are meant to lead to expected outcomes) and comparing their opportunity scores is a good way to compare how well they satisfy a customers' job-to-be-done.

Ulwick also suggests conducting regression and clustering analyses to discover market segments with latent opportunities. This is out of the scope of this article (see the Further Reading section below for more information).

### A word on sample sizes and other uses

For the type of market and innovation research that his original book aims for, Ulwick recommends asking the Importance and Satisfaction questions to a sample of at least 180 participants. To reach this sample sizes, a survey is probably the best method.
At the DevDiv UX Research team we sometimes adapt Ulwick's method when conducting Concept Value Testing (CVT) during 1 to 1 sessions with customers. In those cases, the OpScore allows us to get an idea of how critical a problem or ourcome is. Later on we present the features and conduct the actual CVT to assess whether the proposed solutions might help solving the problem or obtaining the desired outcome for the customer. In this kind of studies, sample sizes are usually lower (20+ participants), hence, although results can help guiding product development (e.g. for prioritizing engineering efforts), caution is needed before considering them significant.

## R script

Here is an R script that will calculate the Opportunity Scores and generate an Opportunity map:
[OppScore: yet another R script for calculating opportunity scores and plotting the Opportunity Map / Landscape.](https://github.com/jpcarrascal/OppScore)

## Further Reading

- You can buy Ulwick's original book from Amazon: ["What Customers Want: Using Outcome-Driven Innovation to Create Breakthrough Products and Services", by Anthony W. Ulwick.](https://www.amazon.com/What-Customers-Want-Outcome-Driven-Breakthrough/dp/0071408673/ref=sr_1_1?ie=UTF8&qid=1542985754&sr=8-1&keywords=What+Customers+Want%3A+Using+Outcome-Driven+Innovation+to+Create+Breakthrough+Products+and+Services)

- Ulwick's talk on ODI in the 2018 [From Business to Buttons](https://frombusinesstobuttons.com/), a Scandinavian conference on UX and Service Design. [Video.](https://www.youtube.com/watch?v=2ecwXEnQ6xY)

- [Jobs-to-be-Done + ODI](https://jobs-to-be-done.com/), a Medium blog by Ulwick. This is probably the most relevant post in that blog: [Outcome-Driven Innovation: JTBD Theory in Practice](https://jobs-to-be-done.com/outcome-driven-innovation-odi-is-jobs-to-be-done-theory-in-practice-2944c6ebc40e)

- This article is a nice and short summary of the main topics in the book: [Outcome-Driven Innovation](https://medium.com/@AlexJupiter/outcome-driven-innovation-3377252aec15)
