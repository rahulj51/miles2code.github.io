---
layout: post
title: Guiding principles for a data engineering team
date: '2020-08-29T11:09:40.468Z'
categories: Data-Engineering Principles
---

All engineering leaders must spend some time creating a set of guiding principles for their teams. Any good engineering team should be rooted in a core set of values. These values act as the north-star for a team and enable it to align its activities with meaningful business outcomes.

Data Engineering teams are no different, but they have some unique challenges. Data Engineering teams often work in silos, sandwiched between data producers and data consumers (see [https://martinfowler.com/articles/data-monolith-to-mesh.html](https://martinfowler.com/articles/data-monolith-to-mesh.html) for more on this topic). It is common for these teams to feel isolated and lose sight of the larger purpose of their function.

Having a list of guiding principles is a first step in creating a sense of identity for the data engineering team in a complex organizational setup.

For our data team at [Omio](http://www.omio.com), we use the following principles to guide us. These values are, by no means, exhaustive. They are also highly contextualized to our unique environment and challenges. But these principles help us take the right decision in moments of doubt.

### **Data, Analytics and Business**

*   We deeply understand Omio’s business and how Analytics can help us offer a better Travel product to our customers while allowing us to prosper as a profitable business. We believe that this helps us adopt a product oriented mindset to our solutions.
*   All of us, data engineers and data analysts, deeply care about data. We look at it not just as bytes moving across the network from one storage system to the other but as a living, breathing entity that has semantic meaning and the power to drive business decisions.
*   We believe in equal participation and joint ownership from both data producers and consumers in building end-to-end Analytics products. We are not just “data-merchants” for the organization.
*   Our approach to data quality is to never hide data-quality issues or compensate for them but to make them transparent to all parties.

### **Technology and Processes**

*   As much as possible, we trust and favor open source technologies.
*   We do not do self-indulgent Engineering. We do not follow engineering practices that are not tied to a business outcome but merely exist to scratch our own itch.
*   We prefer boring but battle tested technologies over tech-fetishism.
*   We follow the principles of second order thinking and strive to build engineering systems that outlast us in the organization.
*   Experiments/Bets are highly encouraged. But only code that runs in production is celebrated.
*   We write it, we run it, we own it.
*   We believe that low-fidelity tools and processes are often good enough to get the work done.
*   We are not overly-attached to our own code/solutions/products. If a solution does not age well, we deprecate it.
*   Everyone in the team participates equally in investigating and debugging data issues, writing data pipelines or helping with on-call support.
*   We strive towards a data-ops approach to data engineering. This means that we build platforms and products to enable self-servability of Analytics.