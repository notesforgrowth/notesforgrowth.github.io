---
layout: post
title: What is (Ulwick's) Opportunity Score?
author: JP Carrascal
---

The Opportunity Score is a tool that helps (among other things) to estimate market opportunity, to prioritize efforts in product development and to conduct competitive analysis. It is part of the "Opportunity-Driven Innovation" framework created by Anthony W. Ulwick, that aims at making "innovation predictable". This article focuses specifically on the Opportunity Score calculation. However, the Opportunity Score is not a silver bullet, and if you want to use properly, you should read a bit more on the Opportunity-Driven Innovation process to get the whole picture. To help with that, I have included a few links in the "Further Reading" section at the end of the article.

## Background

Ulwick's work on Opportunity-Driven Innovation (ODI) is based on the idea that customers mainly pay to get a _job-to-be-done_. This means people do not actually care about tools, features or specs, what they care about is achieving a goal (this is nicely explained by Prof. Clayton Christensen in <a href="https://www.youtube.com/watch?v=Q63PZR7mG70" target=_blank>this video</a>). If a product of service helps customers to achieve the goal (to get a job done), they will pay for it. According to Ulwick, deeply understanding the customers' _job-to-be-done_ is necessary to predict whether customers will be willing to pay for a product. The ODI framework is a systematic approach towards analyzing jobs-to-be-done to decide whether to invest on a certain design space, and how to prioritize such investment.

(Understanding the job-to-be-done for a specific product or market requires a whole research process outside of the scopr of the article.)

### What is the Opportunity Score?

 The main metric used in the ODI framework is the Opportunity Score. This is the result of an <a href="https://en.wikipedia.org/wiki/Gap_analysis" target=_blank>analysis of the gap</a> between the importance that customers assign to the expected outcomes of a job-to-be-done, and how satisfied they are with their current solutions.

Once a job-to-be-done has been understood, it should be broken down the into smaller job steps, and for each step, a series of _outcomes_ (as expected or desired by customers) should be defined. For instance, a job-to-be-done could be:


  Listening to music.

And the steps of this job-to-be-done and their outcomes could be:


| Job step        | Outcomes|
| ------------- |:-------------:|
| Finding relevant music      | Finding new music I might like |
|       | Getting music my friends recommend to me |
|       | Identifying music I hear anywhere |
| Organizing my music | Browsing the music I have |
|       | Grouping my music according to different criteria |
|       | Listening to the music in the order I choose |
| Listening in different places | Listening at home |
|       | Listening on the go |


### Obtaining the data
To obtain the Opportunity Score for each outcome, one should ask customers two questions:

1. __Importance:__ _When [job step], how __important__ is it to you that you are able to [outcome]?_ (1 to 5, 1 = "Not at all important", 5 = "Extremely important")
2. __Satisfaction:__ _When using [solution], how __satisfied__ are you with your ability to [outcome]?_ (1 to 5, 1 = "Not at all satisfied", 5 = "Extremely satisfied")

(Where [solution] is any current product or service used by the customer to get the job done.)

Bear in mind that these questions should be asked to a representative pool of participants.

### Computing the score

Computing the opportunity score is easy:

1. Compute the percentage of respondents who answered 4 or 5 to both __importance__ (that is those who said the outcome is "Important" or "Extremely important") and __satisfaction__ (those who said they are "Satisfied" or "Extremely satisfied").

2. Include the percentages in the Opportunity Score formula:

´´´
OpScore = Importance + max(Importance - Satisfaction, 0)
´´´


Computing it
Plotting it
Description of the zones in the map

### Zones

### Prioritization

### Competitive analysis

## How to collect the data?

First, define outcomes (collect data)
Then collect data about Importance and Satisfaction


## R script

## Further Reading

- You can buy Ulwick's original book from Amazon: ["What Customers Want: Using Outcome-Driven Innovation to Create Breakthrough Products and Services", by Anthony W. Ulwick.](https://www.amazon.com/What-Customers-Want-Outcome-Driven-Breakthrough/dp/0071408673/ref=sr_1_1?ie=UTF8&qid=1542985754&sr=8-1&keywords=What+Customers+Want%3A+Using+Outcome-Driven+Innovation+to+Create+Breakthrough+Products+and+Services)

- Ulwick's talk on ODI in the 2018 [From Business to Buttons](https://frombusinesstobuttons.com/), a Scandinavian conference on UX and Service Design. [Video.](https://www.youtube.com/watch?v=2ecwXEnQ6xY)

- [Jobs-to-be-Done + ODI](https://jobs-to-be-done.com/), a Medium blog by Ulwick.

- This article is a nice and short summary of the main topics in the book: [Outcome-Driven Innovation](https://medium.com/@AlexJupiter/outcome-driven-innovation-3377252aec15)

- Another summary of the ODI method: [Quantify Your Customer’s Unmet Needs](https://jobs-to-be-done.com/quantify-your-customers-unmet-needs-fda5b20fce54)
