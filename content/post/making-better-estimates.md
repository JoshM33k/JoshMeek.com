---
title: "Making Better Estimates by Refusing to Estimate"
date: "2019-10-01"
draft: false
tags: ["development"]
toc: false
---

Humans are inherently bad at estimating how long things will take. Seriously, just ask my wife: "I'll be there in 15 minutes" can easily become two hours if I get distracted by some new idea or project along the way.  Moreover, humans always estimate for the best-case scenario "happy path", typically failing to account for additional time should issues arise, even if those issues are incredibly likely. We're overly optimistic in our estimations.

Overcoming this natural tendency and learning how to give accurate, realistic estimations is seen as a mark of a skilled, professional developer. The excellent [Clean Coder](https://www.amazon.com/Clean-Coder-Conduct-Professional-Programmers/dp/0137081073) discusses how to properly make these estimates, and how to justify and defend them. While it is very important as a software engineer to be able to reasonably estimate how long a task will take, we can reframe the typical "how long do you think this will take?" conversation to make it more productive for the manager asking for an estimate, and less dangerous for the developer doing the estimating.

## Unspoken Parameters

The unspoken piece of an estimation conversation is that most managers asking a developer for an estimate have an idea in mind of how long they think that task should take. The manager comes in with a preconceived notion and a desired outcome. Essentially, they have a price, in development hours, they're willing to spend for a given task. If the developer comes in with an estimate under this magic number, they're praised! So fast! So productive! If the developer says a number higher, they're either thought of as less productive, or even worse, the manager may attempt to "talk them down" to the number they had in mind.

Obviously these behaviors are counter-intuitive, and neither party gets to play to their strengths. A manager should be employing developers that they trust to give them an accurate estimate, without any coaxing or pleading for different numbers, and a developer should be able to trust that their manager truly wants their opinion in how long something will take, rather than to start a bargaining match over development hours. However, in the real world, this harmonious relationship is rarely the reality.

## The Solution

So, the developer should instantly reframe any talk of "how long would this take?" with an initial question of their own: "When is the deadline?" This makes the unspoken initial bid of the manager apparent to both parties. The developer is no longer throwing a dart at a dartboard they can't see, they're presented with the actual business needs of the manager for the task at hand.

With this deadline in hand, the developer should **not** simply accept this number and go off to work! The developer's skill in estimating effort and time still comes into play, but now they have a new axis with which to measure: They now know the upper bound. With this information, they can now inform their manager of the _reality_ of completing the given task by the preferred deadline. Instead of "this task will take 3 weeks" when the manager had 2 weeks in mind, the developer can now say "If you need this done in 2 weeks, I'll only be able to account for 3 of the 5 use cases in that time". This should mean that both the manager and the developer have a clearer understanding of the business need and what proposed work will be completed by the deadline.