---
date: 2025-08-12
author: jw
title: "The Beautiful Contradiction: Public Code, Private Clouds"
description: "Enterprise AI is stuck between security and innovation. Here's how open source models plus on-prem deployment solves both challenges at once."
categories: [work, jozu, open source]
tags: [Jozu, KitOps, Open Source, Startup, GTM]
---

Last week, OpenAI released two open source models. Ironically, this release (by the company with "open" in its name) caught me, and from what I can tell most of the tech world by surprise. Open sourcing models isn't a new thing, Meta, Google, Microsoft, and several others have been doing it for quite a while, however, the consensus was that these releases were made to undercut OpenAI's dominant position in the market.

The reality is that **the industry is talking about AI, much more than it's building AI.** This is because it's complicated, it's moving really fast, and let's be honest pushing a model to production takes a ton of trust … afterall, what if this thing goes completely rogue on you?

Being able to lean on a vendor like OpenAI, that has a seemingly infinite budget for AI talent, is a move that ensures you can sleep at night (when your AI support bot isn't).

This is good for simple tasks, like the one I mentioned above … connecting your documentation and support data to a GPT for a 24/7 support chat bot. This all changes when you start talking about data that can't be found by a determined googler on a support forum. **The type of data that if your competitor found could cause irreparable damage, or data that if exposed violates regulations and leads to massive fines (think HIPAA).** Do you really want to push that over to OpenAI or any other SaaS vendor?

**The answer is NO–and this is where on-prem comes into play.**

## Shifting from Impressing to Impacting

When AI came onto the scene, everyone jumped on it. That AI support bot I mentioned above was viewed as proof that your company was ahead of the AI-native learning curve … a real leader. It was impressive, but outside of customer support efficiency gains (which I just googled and found are really hard to actually prove), it's not really that impactful.

**The real impact of AI is going to emerge when it has access to proprietary business data at scale, and for this it needs to go on-prem.**

## Security, Security, Security

If Steve Ballmer was still dancing around at Microsoft he almost certainly would evolve his iconic chant from "Developers!, Developers!, Developers!" to "Security!, Security!, Security!" … besides with [Cursor](https://cursor.sh/), you only need a few of them right?

This is where open source comes back into view. For on-prem to be a valid move, you need a model that can be deployed on-prem. In the past these models were built internally, largely by research and investment firms, who had a real business need for AI.

Now, everyone has a real business need for AI (at least that's what the board wants to hear), and talent is hard to come by. And open source makes this accessible to all ([more on the relationship between open source and enterprise growth](https://jesse-williams.com/open-source-enterprise-growth)).

## Great, I Have a Model, Now What?

> "If you build it, they will struggle to deploy it" –Kubernetes

The model is only one part of the equation. To this point, most teams are either trying to shove it through their existing pipeline or building an AI specific pipeline to run in parallel. The problem with this is that existing pipelines lack the orchestration and governance capabilities that are required by AI/ML. They're also not friendly to your peers on the data science side of the house, who have a completely different set of tools. On the other hand, building an AI specific pipeline means moving away from the best practices and workflows that you've put in place for your app code.

## Making On-Prem, Open Source ML Attainable

This is where solutions like [Jozu](https://jozu.com) come in. [Jozu](https://jozu.com) originated out of our own struggles with ML development and deployment ([read more about this journey](https://jesse-williams.com/kitops-modelpak-jozu)). The same struggles that were faced by developers pre-Docker. AI/ML is unique and needs use case specific tools, however, we don't need to reinvent the wheel, we just need a different type of wheel.

Containers solved the "it works on my machine" problem, and though you can use a tool like Docker (and many do) to package up your ML project, it's not optimized for the ML use case.

Sticking with our wheel analogy, you could think of the [Open Container Initiative (OCI)](https://opencontainers.org/) as a rubber circle. It's the foundation of what we call a tire. Docker would be your typical Goodyear all weather tire that should be on 90% of all road vehicles, because it just works. ML on the other hand, is not a road vehicle, it's a F1 car. Your Goodyears will allow it to roll forward, but you're not getting anywhere near the performance you should be getting.

This is why we built (and open sourced) [KitOps](https://kitops.ml) ModelKits. [ModelKits](https://kitops.ml/docs/modelkit/intro.html) are the container type that are purpose built for AI/ML ([learn about our journey from initial traction to product-market fit](https://jesse-williams.com/100k-kitops-installs)). The key thing here is that they are still a container type based on the same standard that Docker and Kubernetes are. This should dispel the misconception that we're trying to create a whole new ecosystem/standard. In fact, because ModelKits are in the OCI family, they are compatible with your existing pipelines … anywhere you can put a Docker container, you can put a ModelKit.

But, that's not where it ends. [ModelKits](https://kitops.ml/docs/modelkit/intro.html) make it easy to package up and deploy your open source models, but how do you govern them on-prem?

This is where [Jozu](https://jozu.com) comes in. At the very basic level, [Jozu](https://jozu.com) can be looked at as an on-prem [Hugging Face](https://huggingface.co/). It's where your open source model lives and is versioned. It gives your team the tools they need to work with [ModelKits](https://kitops.ml/docs/modelkit/intro.html) very efficiently, surfacing version diffs, allowing rollbacks, packaging inference, signing, audit logging, and much more.

Maybe more importantly, it adds the governance layer into your workflow that provides you and your team with the confidence you need to deploy models at scale. And, best of all, it lives on-prem. [Jozu](https://jozu.com) was built to enable the next wave of AI innovation, the one that will take place securely behind your firewall and lead to the massive business impact we've all been expecting.

---

*Learn more about [KitOps](https://kitops.ml) and [Jozu](https://jozu.com) to see how they can help your organization deploy AI/ML models securely on-premises.*