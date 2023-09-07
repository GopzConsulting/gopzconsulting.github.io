---
layout: post
title:  "Nets vs Walls"
excerpt: "The Importance of Deploy Pipeline Process Architecture"
date:   2023-08-29 01:00:00 +0100
image: /assets/img/net-vs-wall.jpg
---

Most people working in technology are familiar with the great and unifying deployment pipeline. At any large organization the advancement from technical specification to real world feature is guarded by a series of automated and manual checks. In the perfect deploy pipeline you might have unit tests, integration tests, contract tests and more. Perhaps many checks are automated around version control. Maybe stress tests and dry run deploys dot the landscape as well. The options to build quality into the lifecycle of code are seemingly endless and yet something is amiss.

## Water, water, everywhere but not a drop to drink

One of the beautiful things about software development is that for every popular technology there exists some framework to ensure that technology is being used responsibly. Sophisticated, object oriented, programming languages? Use robust unit testing frameworks. Tools to make interfaces accessible? Axe and others certify that your apps are easy to use by everyone. Microservices with competing APIs? You can use tools like Pact to test the contracts. I call these guardrail frameworks as their primary function is to ensure the responsible use of the corresponding technologies. For now we will focus on them as a case study in process management, but semi-automated processes like content translation and localization can suffer from the same issues that I will be describing.

Like anything, the deploy pipeline has high tolerance for misuse, whether by ignorance or negligence, the smaller and and more isolated that it is. This tends to create a false sense of security, amongst engineers in particular, that as long as the guardrail frameworks are in place, there is nothing left to worry about. Alas, the pipeline can never be maintained in a vacuum and its eventual hundreds of users will amplify any tiny mistakes into an untenable Pandora's box of errors. Surrounded by a myriad of solutions, you may still feel like the deploy pipeline fails to provide any confidence around releases.

## Walls and Nets

Ultimately what will determine the success of a deploy pipeline is how its users interact with the various established guardrail frameworks that help define it. If people using the deploy pipeline are incentivized to respect the guardrails, then they will view those guardrails as a net that catches them in case they fall. Made a breaking API change by accident? No sweat, Pact is going to tell you about it. Important legal text is unreadable by someone who's colorblind? Axe has your back. On the other hand, if the people using the pipeline are okay with API errors and accessibility flaws, then they will tend to see the guardrails only as a wall that is blocking them from what they want.

Should you find yourself in a situation where a substantial portion of pipeline users see the guardrails as a wall rather than a net, the guardrails will become burdensome and enter into a negative feedback loop. Once inside this loop, pipeline users will begin to hate the guardrails and try their best to circumvent them. This will of course result in additional cruft in the pipeline and cause additional dissatisfaction and so on. It's obviously better to avoid this situation before it becomes a downward spiral, but there are ways to break out.

## Incentives

The key to pipeline health is procedure adherence and the key to procedure adherence is the management of incentives. Depending on the incentives of the pipeline users, they will see the procedure around it as either walls or nets. An example of procedure would be commitment to using the guardrail frameworks in a certain way. If the incentives of users are managed correctly then the pipeline will flourish. This may sound like a bit of a cop out, something like:

"How do you consistently meet deadlines?"

"Complete all tasks before the deadline arrives."

I promise there is more subtlety to it than that and as proof I offer you the hallmark of any nuanced insight: a graph.

| ![a graph illustrating incentive breakdowns](/assets/img/process_chart.png) |
|:--:|
| <sub>Red means an unhealthy pipeline owing to negligence of procedure, green means a healthy pipeline</sub> |


The basic constituents here related to pipeline health are cost of following procedure and reward for breaking procedure. High cost and high reward (of breaking procedure) results in an unhealthy pipeline, while low cost of following the rules and general condemnation for breaking them results in something that everyone likes using. For example, if your test suite must be green before merging to a trusted branch, but it takes more than an hour to run, then the cost of following procedure is high. Additionally, if meeting deadlines whilst flaunting something like unit specs is met with public congratulations then the reward for other teams to break procedure has increased.

## Conclusion

I hope that you are reading this article, shaking your head, and thinking to yourself "I didn't even know people had this problem!". It's never any fun to be in a situation where the fruits of modern software development become the monster under the bed. However, should you find yourself in a situation where your deploy pipeline is sophisticated, but failing to protect releases, it will help to think about whether the people interacting with it see it as a wall or a net.

> **_Key takeaways_** 
> * The usage of the correct "guardrail frameworks" does not a deploy pipeline make
> * Pipeline users may see the guardrails as "walls" and ignore them
> * Healthy pipelines have users that see the various checks as "nets" that will catch mistakes
