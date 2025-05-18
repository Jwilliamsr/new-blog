---
date: 2025-05-16
author: jw
title: "Building in Public: Some Notes on KitOps' Growth and Venturing into Enterprise Sales"
description: "What we've been up to at Jozu and KitOps"
categories: [KitOps, startups, open source]
tags: [Business]
---

A quick KitOps update–This week KitOps broke 85,000 installs. We launched open source KitOps in March of 2024, and since then have seen consistent week-over-week install growth. In addition to the installs, we've been seeing a ton of community engagement on our GitHub repo, and hosted our first community call on Wednesday. Despite the repo engagement, anytime I interact with an open source community for the first time, I get pretty nervous. I've been in the open source space for almost 15-years now and the reality is that events where no one shows up are painfully common (more common than you would probably think!) Luckily, this wasn't the case for the KitOps community call :)

Early in my tech career I read a post from a founder that had managed to build a highly-engaged community. This was back in the Seth Godin days, so I'm sure we called it a niche ... anyway, in the post they pointed out that there is a tipping point in community engagement, which happened when you reached 100-fans. To be clear, a fan is not a community member. A fan is someone who loves your product so much that they give you free promotion. Today we call these champions, and they aren't only important for community growth, but key to selling your product.

KitOps is currently being used in product by multiple enterprises. The KitOps value is clear. 

When we were at KubeCon EU last month we observed that if you aren't using KitOps, you're not really versioning your ML project. When you say this aloud, it feels like a massive stretch. In fact, most of the developers I spoke to argued the point, insisting that their current stack has versioning, and to that point they are correct. BUT, there's a big problem, all of these tools version independently. The data is versioned in DvC or S3, the code in GitHub, the model in Jupyter, the tuning in MLFlow, etc. These tools are excellent at what they do, but when I asked how they kept track of all these different versions, the answer was .... A SPREADSHEET! 

For me, it's music to my ears. After all, the best startups build software that replaces a spreadsheet right?!

But that's not all, replacing spreadsheets is only one reason ML teams love KitOps. The second is eliminating vendor lock-in. 

Vendor lock-in is an interesting problem to focus on. I've worked at Red Hat and AWS, so I've argued both sides of the vendor lock-in conversation. I'll be honest here, when it comes to how to run your cloud-workloads, going all in on a single vendor is a better choice for 90% of companies, and the other one is really just selling FUD. The idea that a cloud-vendor is going to randomly hike prices way above the market is unrealistic, compute cost is a race to the bottom.  

However, when it comes to AI workloads the race is happening incredibly fast ... like cut your costs in half overnight fast. This is where the vendor lock-in conversation comes back into view, but from a different angle. Enterprises want the ability to quickly migrate to the cloud provider that can give them the cheapest compute cost for their ML workloads–something that changes on a weekly basis.

<h2>We pioneered ML project adoption of the OCI (Open Container Initiative)</h2>

When we created ModelKits, we chose the OCI because reinventing the wheel is a waste of time. OCI artifacts seem to have been (unintentionally?) built to perfectly suit ML projects. Initially, our goal was just to eliminate the pain of re-packaging our ML projects from one vendor specific package type to the other ... not fun. As we engaged with other teams, we realized that others were thinking about this same thing, which led to contributing KitOps to the CNCF and leading the creation of the ModelPack spec, the Cloud Native Artificial Intelligence Model Format Specification, which establishes open standards for packaging, distributing and running AI artifacts in the cloud-native environment. We're currently going through the voting process, so fingers crossed the ModelPack spec becomes the defacto standard.

<h2>Keep in mind, open source software doesn't pay the bills</h2>

As a founder building an open source software, it's easy to become disillusioned. At the end of the day 85K open source installs means nothing for our bottomline. This is where Jozu comes in. How do you take something that in its organic form is valuable and create a product that amplifies that value 100x? 

I live in a small town in rural Virginia, that is about 50-miles outside of Washington DC. On Main St. we have a little bakery that is known for its amazing apple pie. The walls are covered with pictures of important people and foodie magazine articles featuring their pastries. When Thanksgiving comes around, an apple pie will cost you around $40, but only if you get your order in few months early. You can think of open source in the same way. Apples are valuable by themselves, but when you put that apple inside of the right wrapper (in this case a pastry from The Red Truck Bakery), the value increases exponentially. 

I like to think about ModelKits like apples and Jozu like the fully baked apple pie. You could take your ModelKit and host it in any OCI compatible registry, that's the beauty of open source. But when you use Jozu Hub, you can extract the full potential of that ModelKit. 

<h2>What exactly does Jozu add?</h2>

Let's start with versioning (since I mentioned it already). ModelKits are immutable and therefore versionable, but versioning in itself needs to take place somewhere. Additionally, ModelKits are signable, which also needs to take place somewhere, and let's not forget the ModelKit's rich meta data. You could push your ModelKit to Docker Hub or Artifactory, but since they weren't created for ML projects, they don't display the information that ML teams require to speed up their development process (by over 45% to be exact!)

We also add things like Hugging Face (HF) import, which allows you to easily curate a catalogue of HF models for your team, model scanning, to ensure that the model you pulled from HF is safe to use, an audit log which automated the tracking of all actions taken against the project, and inference to get your project to production quickly. 

These are things that are easy to say, but hard to do. For example, when we talk to customers, audit logging typically takes a team of 2 developers, one week per quarter to complete ... you heard that right 8-weeks of developer time annually!

Then there's inference. If you think Kubernetes is hard, try going from a Jupyter Notebook to a Kubernetes production environment, I bet you couldn't even say that 10x over without confusing yourself, much less actually do it. 

<h2>If we could only get one ...</h2>

This brings me to the current focus on my founder journey. Enterprise sales. 

I've spent a lot of time in the tech world, but I've never been in sales. Like all things we're approaching it from a trial and error standpoint, while gathering as much advice from smart people as possible. I find that the biggest challenge is getting in front of the right person. Developers love KitOps and Jozu, but developers aren't buyers. And, the path from an individual developer to a C-level decision maker is incredibly long, and if I'm honest a bit wishful.  

This is the challenge that I'm working on solving right now. How do we create a replicable process for finding CXOs with an initiative that aligns to the benefits that Jozu Hub offers? I'll let you know when we figure it out.

As always onwards and upwards!

/jw