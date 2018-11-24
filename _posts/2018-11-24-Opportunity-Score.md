---
layout: post
title: What is (Ulwick's) Opportunity Score?
author: JP Carrascal
---

<style>
table{
    border-collapse: collapse;
    border-spacing: 0;
    border:2px solid #000000;
}

th{
    border:2px solid #000000;
}

td{
    border:1px solid #000000;
    padding: 5px;
    font-size: 0.8em;
}
</style>

The Opportunity Score is a tool that helps (among other things) to estimate market opportunity, to prioritize efforts in product development and to conduct competitive analysis. It is part of the _Opportunity-Driven Innovation_ framework created by Anthony W. Ulwick, that aims at "making innovation predictable". This article focuses specifically on the Opportunity Score calculation. However, the Opportunity Score is not a silver bullet, and if you want to use properly, you should read a bit more on the Opportunity-Driven Innovation process to get the whole picture. To help with that, I have included a few links in the "Further Reading" section at the end of the article.

## Background

Ulwick's work on Opportunity-Driven Innovation (ODI) is based on the idea that customers mainly pay to get a _job-to-be-done_. This means people do not actually care about tools, features or specs, what they care about is achieving a goal (this is nicely explained by Prof. Clayton Christensen in [this video](https://www.youtube.com/watch?v=Q63PZR7mG70)). If a product of service helps customers to achieve the goal (to get a job done), they will pay for it. According to Ulwick, deeply understanding the customers' _job-to-be-done_ is necessary to predict whether customers will be willing to pay for a product. The ODI framework is a systematic approach towards analyzing jobs-to-be-done to decide whether to invest on a certain design space, and how to prioritize such investment.

Understanding the job-to-be-done for a specific product or market requires a whole research process that is outside of the scope of the article.

## The Opportunity Score

 The main metric used in the ODI framework is the Opportunity Score. This is the result of an [analysis of the gap](https://en.wikipedia.org/wiki/Gap_analysis) between the importance that customers assign to the expected outcomes of a job-to-be-done, and how satisfied they are with their current solutions.

Once a job-to-be-done has been defined, it should be broken down the into smaller job steps, and for each step, a series of _outcomes_ (as expected or desired by customers) should be enunciated. For instance, a job-to-be-done could be:


  Listening to music.

And the steps of this job-to-be-done and their outcomes could be:


| __Job step__                    | __Outcomes__                                        |
|---------------------------------|-----------------------------------------------------|
| Finding relevant music          | Discovering new music I might like                  |
|                                 | Finding music my friends recommend to me            |
|                                 | Identifying music I hear anywhere                   |
|---------------------------------|-----------------------------------------------------|
| Organizing my music             | Browsing through the music I have                   |
|                                 | Grouping my music according to different criteria   |
|                                 | Listening to the music in the order I choose        |
|---------------------------------|-----------------------------------------------------|
| Listening in different places   | Listening at home                                   |
|                                 | Listening on the go                                 |

(BTW, Ulwick's says that jobs-to-be-done generally don't change across time. This might be suggested by this example.)

## Collecting the data
To obtain the Opportunity Score for each outcome, one should ask customers two questions:

1. __Importance:__ _When [job step], how __important__ is it to you that you are able to [outcome]?_ (1 to 5 scale, 1 = "Not at all important", 5 = "Extremely important")
2. __Satisfaction:__ _When using [solution], how __satisfied__ are you with your ability to [outcome]?_ (1 to 5 scale, 1 = "Not at all satisfied", 5 = "Extremely satisfied")

Where [solution] is the solution that the customer currently uses to get the job done.

Ulwick recommends asking these questions to a sample of over 180 participants.

### Computing the score

Obtaining the opportunity score is easy:

1. Compute the percentage of respondents who answered 4 or 5 to both __importance__ (that is those who said the outcome is "Important" or "Extremely important") and __satisfaction__ (those who said they are "Satisfied" or "Extremely satisfied").

2. Insert these percentages in the Opportunity Score formula:



```OpScore = Importance + max(Importance - Satisfaction, 0)```



_(NOTE: Ulwick normalizes the percentages to 10 instead of 100. I'm not sure why.)_

To interpret the results, the data is usually plotted on a graph like this one:

<p style="text-align:center">
<img src="/images/Opportunity-Score/OpportunityLandscape.jpg" style="width:80%;"/>
<span class="caption">The "Opportunity Landscape".</span>
</p>

The graph illustrates how well customers' needs are satisfied with current solutions. It helps to indicate prioritization strategies for improving existing products or creating new ones. The _Overserved_ area suggests there is not much room for innovation and most likely way to compete there is by offering a lower-priced solution. On the opposite side, the _Underserved_ area indicates there are stronger opportunities to innovate as there are a lot of unsolved needs. People will be willing to pay more to have these needs solved. The middle area represents needs that are important but are currently well satisfied. Ulwick indicate thet these are "table stakes" that should be served if one considers developing a new product for a job-to-be-done. 

Another interesting application of the opportunity score is for conducting competitive analysis. Breaking down features of two competing products (which are meant to lead to expected outcomes) and comparing their opportunity scores is a good way to compare how well they satisfy a customers' job-to-be-done.

Ulwick also suggests conducting regression and clustering analyses to discover market segments with latent opportunities.

## R script

I will update this post shortly to include an R script for computing Opportunity Scores and generating a graph like the one avobe shortly.

## Further Reading

- You can buy Ulwick's original book from Amazon: ["What Customers Want: Using Outcome-Driven Innovation to Create Breakthrough Products and Services", by Anthony W. Ulwick.](https://www.amazon.com/What-Customers-Want-Outcome-Driven-Breakthrough/dp/0071408673/ref=sr_1_1?ie=UTF8&qid=1542985754&sr=8-1&keywords=What+Customers+Want%3A+Using+Outcome-Driven+Innovation+to+Create+Breakthrough+Products+and+Services)

- Ulwick's talk on ODI in the 2018 [From Business to Buttons](https://frombusinesstobuttons.com/), a Scandinavian conference on UX and Service Design. [Video.](https://www.youtube.com/watch?v=2ecwXEnQ6xY)

- [Jobs-to-be-Done + ODI](https://jobs-to-be-done.com/), a Medium blog by Ulwick. This is probably the most relevant post in that blog: [Outcome-Driven Innovation: JTBD Theory in Practice](https://jobs-to-be-done.com/outcome-driven-innovation-odi-is-jobs-to-be-done-theory-in-practice-2944c6ebc40e)

- This article is a nice and short summary of the main topics in the book: [Outcome-Driven Innovation](https://medium.com/@AlexJupiter/outcome-driven-innovation-3377252aec15)
